# Synchrony Test PWA - FIXED VERSION

## 🔧 What Was Wrong

The original version had the React component in a separate `.jsx` file using ES6 `import` statements, which don't work with Babel standalone in the browser. The new version embeds everything in a single `index.html` file.

## 📦 Files You Need

Only these 4 files are required:
- `index.html` - **Main file with embedded React component**
- `manifest.json` - PWA manifest
- `service-worker.js` - Offline support
- `vercel.json` - Vercel configuration

## 🚀 Quick Deploy to Vercel

### Method 1: GitHub + Vercel (Recommended)

1. **Create GitHub repo:**
   - Go to github.com and create a new repository
   - Name it: `synchrony-test`
   - Make it Public

2. **Upload files:**
   - Click "uploading an existing file"
   - Drag and drop these 4 files:
     - `index.html`
     - `manifest.json`
     - `service-worker.js`
     - `vercel.json`
   - Click "Commit changes"

3. **Deploy to Vercel:**
   - Go to vercel.com
   - Sign up/login with GitHub
   - Click "Add New..." → "Project"
   - Import your `synchrony-test` repository
   - Click "Deploy"
   - Done! ✅

### Method 2: Vercel CLI

```bash
# Install Vercel CLI
npm install -g vercel

# Navigate to folder with the 4 files
cd /path/to/your/folder

# Deploy
vercel

# Follow prompts, then done!
```

### Method 3: Drag & Drop (Easiest!)

1. Go to vercel.com
2. Sign up/login
3. Drag your folder (with 4 files) onto the page
4. Deploy automatically!

## 🧪 Testing

1. **Open the Vercel URL** in Safari on your iPhone
2. **You should see:**
   - "Synchrony Perception Test" title
   - FPS counter (will show detected refresh rate)
   - Animated dots below the FPS counter
   - Instructions
   - "Start Test" button

3. **If you see a white screen:**
   - Open browser console (F12 or Inspect)
   - Look for errors
   - Most common issue: Files not uploaded correctly

## 📱 Install as PWA

1. Open the URL in **Safari** (not Chrome!)
2. Tap the **Share** button
3. Tap **"Add to Home Screen"**
4. Launch from home screen

## ⚙️ Customization

All settings are in `index.html`:

### Change Offsets
Find this line (~108):
```javascript
const offsets = [0, -8.33, 8.33, -16.67, 16.67, -25, 25, -33.33, 33.33, -50, 50];
```

### Change Colors
Find the intro screen section (~258) and modify className values.

## 🐛 Troubleshooting

**White screen?**
- Check browser console for errors
- Verify all 4 files uploaded to Vercel
- Try hard refresh (Cmd+Shift+R)

**FPS not showing?**
- Wait 1-2 seconds for detection
- The animated dots should be bouncing

**Can't install as PWA?**
- Must use Safari on iOS
- Verify HTTPS (Vercel provides this)
- Check manifest.json is uploaded

**Changes not appearing?**
- Vercel auto-deploys on GitHub push
- Wait 30-60 seconds for deployment
- Clear browser cache

## ✅ Success Checklist

- [ ] All 4 files uploaded to GitHub/Vercel
- [ ] Vercel deployment successful
- [ ] URL loads in Safari
- [ ] FPS counter visible and updating
- [ ] Animated dots bouncing
- [ ] "Start Test" button works
- [ ] Can complete a trial
- [ ] Results page shows CSV/JSON

## 💡 Key Differences from Previous Version

1. **Single file:** Everything is in `index.html`
2. **No external JSX:** React component embedded directly
3. **No imports:** Uses standard browser script loading
4. **Simpler:** Only 4 files instead of 7

This version will work immediately on Vercel with no build step required!
