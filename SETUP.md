# GitHub Setup Instructions

## Files Prepared

✅ `index.html` - Main application file (renamed from planning-navigation-full.html)
✅ `README.md` - Documentation with embed codes
✅ `.nojekyll` - Ensures GitHub Pages serves files correctly

## To Push to GitHub

### Option 1: Using GitHub CLI (Recommended)
```bash
cd "/Users/tamkeen.kiani/Research Docs/Data Driven Personas/Planning-Navigator"
gh auth login
git push -u origin main
```

### Option 2: Using Personal Access Token
1. Go to GitHub.com → Settings → Developer settings → Personal access tokens → Tokens (classic)
2. Generate a new token with `repo` permissions
3. Run:
```bash
cd "/Users/tamkeen.kiani/Research Docs/Data Driven Personas/Planning-Navigator"
git push -u origin main
# When prompted, use your GitHub username and the token as password
```

### Option 3: Using SSH Key
1. Set up SSH key if not already done: https://docs.github.com/en/authentication/connecting-to-github-with-ssh
2. Run:
```bash
cd "/Users/tamkeen.kiani/Research Docs/Data Driven Personas/Planning-Navigator"
git remote set-url origin git@github.com:Tamkeen022/Planning-Navigator.git
git push -u origin main
```

## Enable GitHub Pages

After pushing:

1. Go to: https://github.com/Tamkeen022/Planning-Navigator/settings/pages
2. Under "Source", select:
   - Branch: `main`
   - Folder: `/ (root)`
3. Click "Save"
4. Wait 1-2 minutes for GitHub Pages to build

## GitHub Pages URL

Once enabled, your application will be available at:
**https://tamkeen022.github.io/Planning-Navigator/**

## Iframe Embed Code for Webflow

### Standard Embed
```html
<iframe 
    src="https://tamkeen022.github.io/Planning-Navigator/" 
    width="100%" 
    height="800px" 
    frameborder="0" 
    allowfullscreen
    style="border: none; min-height: 800px;">
</iframe>
```

### Responsive Embed (Recommended)
```html
<div style="position: relative; padding-bottom: 100%; height: 0; overflow: hidden; max-width: 100%; min-height: 800px;">
    <iframe 
        src="https://tamkeen022.github.io/Planning-Navigator/" 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: none;"
        frameborder="0"
        allowfullscreen
        scrolling="auto">
    </iframe>
</div>
```

### Webflow Custom Code Element
Paste the responsive embed code above into a Webflow Embed element.

## Iframe Compatibility

The application has been optimized for iframe embedding:
- ✅ Added `X-Frame-Options: ALLOWALL` meta tag
- ✅ Added `Content-Security-Policy: frame-ancestors *` meta tag
- ✅ Responsive viewport meta tag
- ✅ No external dependencies that could block iframe loading

## Testing

After enabling GitHub Pages:
1. Visit: https://tamkeen022.github.io/Planning-Navigator/
2. Test the application functionality
3. Test iframe embedding in a test HTML page or Webflow preview
