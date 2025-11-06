# CV Website - odd.skaflestad.no

A modern CV website deployed automatically with GitHub Pages.

## 🚀 Quick Deployment

### 1. Create GitHub Repository

1. Go to [GitHub](https://github.com/new)
2. Create a new repository (e.g., `cv-website`)
3. Don't initialize with README (we already have files)

### 2. Push Your Code

```bash
# Make your first commit
git commit -m "Initial commit: Deploy to GitHub Pages"

# Add your GitHub repository as remote (replace with your actual repo URL)
git remote add origin https://github.com/YOUR-USERNAME/cv-website.git

# Push to GitHub
git push -u origin main
```

### 3. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** → **Pages** (in the left sidebar)
3. Under "Source", select **Deploy from a branch**
4. Select branch: **main** and folder: **/ (root)**
5. Click **Save**

Your site will be live at `https://YOUR-USERNAME.github.io/cv-website/` in about 1 minute! 🎉

### 4. (Optional) Add Custom Domain

To use `odd.skaflestad.no`:

1. In GitHub Pages settings, enter `odd.skaflestad.no` in the "Custom domain" field
2. At your domain registrar (where you bought the domain), add DNS records:
   - **Option A**: CNAME record pointing to `YOUR-USERNAME.github.io`
   - **Option B**: A records pointing to GitHub's IPs:
     - `185.199.108.153`
     - `185.199.109.153`
     - `185.199.110.153`
     - `185.199.111.153`

## 🔄 How It Works

Every time you push changes to the `main` branch:
1. GitHub automatically detects the change
2. Rebuilds and deploys your site
3. Your site updates in seconds!

## 📝 Next Steps

- Edit `index.html` to add your CV content
- Customize `styles.css` for your personal style
- Add sections like:
  - About Me
  - Work Experience
  - Education
  - Skills
  - Projects
  - Contact Information

## 🛠️ Local Development

Just open `index.html` in your browser to preview changes before pushing!

## ✨ Benefits of GitHub Pages

- ✅ Completely free
- ✅ Automatic HTTPS
- ✅ No configuration needed
- ✅ Deploy by just pushing to GitHub
- ✅ Fast global CDN
