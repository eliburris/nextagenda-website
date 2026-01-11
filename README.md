# NextAgenda Website - GitHub Pages Setup

## Quick Start (5 minutes)

### Option 1: Host in This Repo

1. **Commit these files:**
   ```bash
   cd /Users/eliburris/Projects/nextagenda-mobile
   git add website/
   git commit -m "Add website files for Google OAuth"
   git push
   ```

2. **Enable GitHub Pages:**
   - Go to your repo on GitHub: `https://github.com/YOUR_USERNAME/nextagenda-mobile`
   - Click "Settings"
   - Scroll to "Pages" (left sidebar)
   - Under "Source", select "Deploy from a branch"
   - Under "Branch", select "main" and "/website"
   - Click "Save"

3. **Your URLs will be:**
   - Home: `https://YOUR_USERNAME.github.io/nextagenda-mobile/`
   - Privacy: `https://YOUR_USERNAME.github.io/nextagenda-mobile/privacy.html`
   - Terms: `https://YOUR_USERNAME.github.io/nextagenda-mobile/terms.html`

### Option 2: Separate Repo (Cleaner URLs)

1. **Create new repo on GitHub:**
   - Name: `nextagenda-website`
   - Public
   - Don't initialize with README

2. **Move files and push:**
   ```bash
   # Copy website files to new directory
   cd ~
   mkdir nextagenda-website
   cd nextagenda-website
   cp /Users/eliburris/Projects/nextagenda-mobile/website/* .

   # Initialize git
   git init
   git add .
   git commit -m "Initial commit"

   # Push to GitHub
   git remote add origin https://github.com/YOUR_USERNAME/nextagenda-website.git
   git branch -M main
   git push -u origin main
   ```

3. **Enable GitHub Pages:**
   - Go to repo settings
   - Pages → Source → "main" branch → "/ (root)"
   - Save

4. **Your URLs will be:**
   - Home: `https://YOUR_USERNAME.github.io/nextagenda-website/`
   - Privacy: `https://YOUR_USERNAME.github.io/nextagenda-website/privacy.html`
   - Terms: `https://YOUR_USERNAME.github.io/nextagenda-website/terms.html`

## What to Put in Google OAuth

Once hosted, add these URLs to Google Cloud Console:

1. **Application home page:**
   ```
   https://YOUR_USERNAME.github.io/nextagenda-website/
   ```

2. **Application privacy policy link:**
   ```
   https://YOUR_USERNAME.github.io/nextagenda-website/privacy.html
   ```

3. **Application terms of service link:**
   ```
   https://YOUR_USERNAME.github.io/nextagenda-website/terms.html
   ```

## Customize Before Publishing

Replace these placeholders in the files:

### In all files:
- `YOUR_USERNAME` → Your GitHub username
- `support@nextagenda.app` → Your real email
- `privacy@nextagenda.app` → Your real email
- `legal@nextagenda.app` → Your real email

### In index.html:
- Update the "Download on App Store" link when you have your App Store URL

## Files Included

- `index.html` - Main landing page with features
- `privacy.html` - Comprehensive privacy policy (GDPR/CCPA compliant)
- `terms.html` - Terms of service with subscription terms
- `README.md` - This file

## After Hosting

1. Wait 5-10 minutes for GitHub Pages to build
2. Visit your URLs to verify they work
3. Add URLs to Google Cloud Console OAuth consent screen
4. Submit for Google verification

## Tips

- GitHub Pages is **free**
- Updates take 1-2 minutes to go live after pushing
- You can use a custom domain later (e.g., `nextagenda.com`)
- All pages are mobile-friendly and look professional

## Troubleshooting

**Pages not showing?**
- Wait 5-10 minutes after enabling GitHub Pages
- Check repo is public
- Verify files are in correct directory
- Check Settings → Pages shows green "Your site is published" message

**404 errors?**
- Make sure filenames match exactly: `privacy.html` not `Privacy.html`
- Check branch and folder settings in Pages
- URLs are case-sensitive

## Need Help?

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [GitHub Pages Troubleshooting](https://docs.github.com/en/pages/getting-started-with-github-pages/troubleshooting-404-errors-for-github-pages-sites)
