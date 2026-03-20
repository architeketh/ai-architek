# 🚀 Your 3D App Website — Setup Guide

A clean, professional website for your 3D modeling app hosted on **GitHub Pages** (free).  
Features: app downloads, demo projects, live download counter, and donation buttons.

---

## ✅ STEP 1 — Create a GitHub Account

1. Go to **https://github.com** and sign up (it's free)
2. Choose a username — this will appear in your site's URL

---

## ✅ STEP 2 — Create a New Repository

1. Click the **"+"** icon → **"New repository"**
2. Name it: `YOUR-APP-NAME` (e.g. `forge3d`)
3. Set it to **Public**
4. Check **"Add a README file"**
5. Click **"Create repository"**

---

## ✅ STEP 3 — Upload the Website Files

1. In your new repo, click **"Add file"** → **"Upload files"**
2. Drag and drop `index.html` into the upload area
3. Click **"Commit changes"**

---

## ✅ STEP 4 — Enable GitHub Pages

1. Go to your repo's **Settings** tab
2. Scroll down to **"Pages"** in the left sidebar
3. Under **"Branch"**, select `main` and folder `/root`
4. Click **Save**
5. Wait ~60 seconds, then your site is live at:
   ```
   https://YOUR_USERNAME.github.io/YOUR_REPO/
   ```

---

## ✅ STEP 5 — Upload Your App as a "Release"

This is how downloads + download counting work.

1. In your repo, click **"Releases"** on the right sidebar → **"Create a new release"**
2. Click **"Choose a tag"** → type `v1.0.0` → click **"Create new tag"**
3. Add a title like `Version 1.0.0`
4. Scroll down to **"Attach binaries"** and upload your `.exe`, `.dmg`, or `.zip` files
5. Click **"Publish release"**

> 💡 GitHub automatically tracks how many times each file is downloaded — no backend needed!

---

## ✅ STEP 6 — Customize the Website

Open `index.html` in any text editor (Notepad works!) and find these spots to edit:

### Your App Name
```html
<title>YourApp — 3D Modeling Studio</title>
```
and:
```html
<a href="#" class="logo">Your<span>App</span></a>
```

### Connect to Your GitHub Repo (for live download counter)
Find these two lines near the bottom:
```javascript
const GITHUB_USERNAME = 'YOUR_USERNAME';  // ← your GitHub username
const GITHUB_REPO     = 'YOUR_REPO';      // ← your repo name
```

### Your Description
```html
<p class="hero-sub">
  A powerful, intuitive 3D modeling application...
</p>
```

### Features Section
Edit the 6 feature cards — change the icons, titles, and descriptions to match your app.

### Footer Links
```html
<a href="https://github.com/YOUR_USERNAME/YOUR_REPO" ...>GitHub</a>
```
Replace `YOUR_USERNAME` and `YOUR_REPO` everywhere in the footer.

---

## ✅ STEP 7 — Set Up Donations (optional, free)

Choose one or more platforms. All are free to set up:

### Ko-fi (recommended — 0% fees)
1. Sign up at **https://ko-fi.com**
2. Get your username (e.g. `ko-fi.com/janedoe`)
3. In `index.html`, replace:
   ```html
   href="https://ko-fi.com/YOUR_KOFI_NAME"
   ```

### Buy Me a Coffee
1. Sign up at **https://buymeacoffee.com**
2. Replace `YOUR_BMC_NAME` in the donate button

### GitHub Sponsors
1. Go to **https://github.com/sponsors** and apply
2. Replace `YOUR_USERNAME` in the sponsor button link

---

## ✅ STEP 8 — Add Demo Projects

For each demo project:

1. Create a folder called `demos/` in your repo
2. Upload your demo `.zip` or `.obj` files there
3. In `index.html`, find the demo cards and update the download link:
   ```html
   <a href="demos/your-file.zip" ... download>↓ Download</a>
   ```
4. Update the title, description, and emoji for each card

To add more demo cards, copy one of the existing `<div class="demo-card">` blocks and paste it inside `.demos-grid`.

---

## 📁 Folder Structure

```
YOUR_REPO/
├── index.html          ← main website file
├── demos/
│   ├── geometric-sculpture.zip
│   ├── arch-scene.zip
│   └── spacecraft.zip
└── README.md
```

---

## 🔄 Updating the Site

Whenever you make changes to `index.html`:
1. Go to your repo on GitHub
2. Click on `index.html`
3. Click the **pencil icon** (edit)
4. Make your changes
5. Click **"Commit changes"**

The site updates automatically within ~30 seconds.

---

## 🐛 Troubleshooting

| Problem | Fix |
|---|---|
| Site shows 404 | Wait 2 minutes after enabling Pages, or check the branch is set to `main` |
| Download count shows `—` | Make sure you updated `GITHUB_USERNAME` and `GITHUB_REPO` in the script |
| Download button doesn't work | Make sure you published a Release with attached files |
| Changes not showing | Hard refresh: `Ctrl+Shift+R` (Windows) or `Cmd+Shift+R` (Mac) |

---

## 📬 Need Help?

Open an Issue in the repo — or just update the README with your own notes as you go!
