# 3DGyan Legal Pages — GitHub Pages Setup

## Quick Setup (5 minutes)

### Option A: New repo (Recommended)

```bash
# 1. Create a new repo on GitHub called "3dgyan-legal" (or any name)
# 2. Clone it and copy these files in:
git clone https://github.com/ersinghrajkr/3dgyan-legal.git
cd 3dgyan-legal

# 3. Copy all HTML files to the root:
#    index.html
#    privacy-policy.html
#    terms-and-conditions.html

# 4. Push
git add .
git commit -m "Add privacy policy and terms & conditions pages"
git push origin main
```

### Option B: Subfolder in existing 3dgyan repo

```bash
cd 3dgyan
mkdir -p docs
# Copy all 3 HTML files into docs/
git add docs/
git commit -m "Add legal pages for GitHub Pages"
git push
```

### Enable GitHub Pages

1. Go to **GitHub repo → Settings → Pages**
2. Under "Source", select:
   - **Option A**: Branch: `main`, Folder: `/ (root)`
   - **Option B**: Branch: `main`, Folder: `/docs`
3. Click **Save**
4. Wait 1-2 minutes for deployment

### Your URLs will be:

**Option A (separate repo):**
```
https://ersinghrajkr.github.io/3dgyan-legal/
https://ersinghrajkr.github.io/3dgyan-legal/privacy-policy.html
https://ersinghrajkr.github.io/3dgyan-legal/terms-and-conditions.html
```

**Option B (docs folder):**
```
https://ersinghrajkr.github.io/3dgyan/privacy-policy.html
https://ersinghrajkr.github.io/3dgyan/terms-and-conditions.html
```

## Custom Domain (Optional)

If you own `3dgyan.com` or `anirvanta.com`:

1. Add a `CNAME` file with your domain: `legal.3dgyan.com`
2. In your DNS provider, add a CNAME record: `legal` → `ersinghrajkr.github.io`
3. In GitHub Pages settings, enter the custom domain
4. Enable "Enforce HTTPS"

Final URLs:
```
https://legal.3dgyan.com/privacy-policy.html
https://legal.3dgyan.com/terms-and-conditions.html
```

## Where to Link These Pages

### Play Store Listing
- Privacy Policy URL field → `https://ersinghrajkr.github.io/3dgyan-legal/privacy-policy.html`

### App Store Connect
- Privacy Policy URL → same as above
- Terms of Use URL → `https://ersinghrajkr.github.io/3dgyan-legal/terms-and-conditions.html`

### In-App (Settings > About)
- Privacy Policy link → same URL, opened via `Linking.openURL()`
- Terms of Service link → same URL

## Files

| File | Description |
|------|-------------|
| `index.html` | Landing page linking to both legal pages |
| `privacy-policy.html` | Full privacy policy (GDPR, CCPA, DPDPA compliant) |
| `terms-and-conditions.html` | Full terms & conditions |
| `README.md` | This setup guide |
