# Nexus Daily - Cross-Platform Setup Guide

Your habit tracker now supports **real-time sync** between devices!

## Quick Start (5 minutes)

### Step 1: Create Firebase Project (Free)

1. Go to [Firebase Console](https://console.firebase.google.com/)
2. **Add Project** → Name it "NexusDaily" → Continue
3. Disable Google Analytics (optional) → Create Project
4. Click **Build** → **Firestore Database** → **Create Database**
5. Select **Start in Test Mode** → Choose region → Enable

### Step 2: Get Your Config

1. In Firebase Console → ⚙️ **Project Settings**
2. Scroll to **Your apps** → Click **Web** icon (`</>`)
3. Register app (name: "Nexus Daily")
4. Copy the **config object** (looks like):
```javascript
{
  apiKey: "AIza...",
  authDomain: "nexusdaily-xxxxx.firebaseapp.com",
  projectId: "nexusdaily-xxxxx",
  ...
}
```

### Step 3: Connect Your App

1. Open `Nexus Daily.html` in browser
2. Click ⚙️ **Settings** → **☁️ Cloud** tab
3. Paste your config → Click **Connect**
4. You'll see "Synced" badge appear ✓

### Step 4: Host Online (For Multi-Device Access)

**Option A: GitHub Pages (Recommended)**
1. Create GitHub account → New Repository
2. Upload all 3 files: `Nexus Daily.html`, `manifest.json`, `sw.js`
3. Settings → Pages → Deploy from main branch
4. Access at: `https://yourusername.github.io/repo-name/Nexus Daily.html`

**Option B: Firebase Hosting**
```bash
npm install -g firebase-tools
firebase login
firebase init hosting
firebase deploy
```

## Files in This Folder

| File | Purpose |
|------|---------|
| `Nexus Daily.html` | Main app (enhanced with sync) |
| `manifest.json` | PWA app definition |
| `sw.js` | Service Worker (offline support) |

## Features Added

✅ **Real-time sync** - Changes appear instantly on all devices  
✅ **Offline support** - Works without internet, syncs when connected  
✅ **Install as app** - Add to home screen on mobile  
✅ **Mobile responsive** - Optimized for phone screens  

## Troubleshooting

- **Not syncing?** Check browser console for errors, verify Firebase config
- **Install banner not showing?** Must be served over HTTPS (works on GitHub Pages)
- **Offline not working?** Clear browser cache, reload page
