# CV Website - odd.skaflestad.no

A modern CV website with automatic deployment from GitHub to cPanel hosting.

## 🚀 Setup Instructions

### 1. Get Your cPanel FTP Credentials

Log into your cPanel and find your FTP credentials:
- **FTP Server**: Usually `ftp.odd.skaflestad.no` or your hosting provider's FTP server
- **FTP Username**: Your cPanel username (or a dedicated FTP account)
- **FTP Password**: Your FTP password
- **Server Directory**: Usually `/public_html/` or `/domains/odd.skaflestad.no/public_html/`

If you're unsure about the server directory, check in cPanel under "File Manager" to see where your domain files should go.

### 2. Create GitHub Repository

1. Go to [GitHub](https://github.com/new)
2. Create a new repository (e.g., `cv-website`)
3. Don't initialize with README (we already have files)

### 3. Add GitHub Secrets

In your GitHub repository, go to **Settings** → **Secrets and variables** → **Actions** → **New repository secret**

Add these four secrets:

| Secret Name | Example Value | Description |
|------------|---------------|-------------|
| `FTP_SERVER` | `ftp.odd.skaflestad.no` | Your FTP server address |
| `FTP_USERNAME` | `your-username@odd.skaflestad.no` | Your FTP username |
| `FTP_PASSWORD` | `your-password` | Your FTP password |
| `FTP_SERVER_DIR` | `/public_html/` | Directory where files should go |

### 4. Push Code to GitHub

```bash
# Initialize git repository (if not already done)
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit: Hello world with auto-deploy"

# Add your GitHub repository as remote
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git

# Push to GitHub
git push -u origin main
```

### 5. Watch the Magic Happen! ✨

1. Go to your repository on GitHub
2. Click on **Actions** tab
3. You'll see the deployment workflow running
4. Once complete, visit **odd.skaflestad.no** to see your site live!

## 🔄 How It Works

Every time you push changes to the `main` branch:
1. GitHub Actions automatically triggers
2. The workflow connects to your cPanel via FTP
3. Files are uploaded to your web directory
4. Your site is updated instantly!

## 📝 Next Steps

- Edit `index.html` to add your CV content
- Customize `styles.css` for your personal style
- Add images, PDFs, or other assets
- Consider adding sections like:
  - About Me
  - Work Experience
  - Education
  - Skills
  - Projects
  - Contact Information

## 🛠️ Troubleshooting

### Deployment fails?
- Check that all GitHub secrets are set correctly
- Verify FTP credentials work (try connecting with an FTP client like FileZilla)
- Check the Actions log for specific error messages

### Files not appearing on your site?
- Verify the `FTP_SERVER_DIR` path is correct
- Make sure the directory has write permissions

### Site shows old content?
- Clear your browser cache (Ctrl+F5 or Cmd+Shift+R)
- Check if the deployment completed successfully in GitHub Actions

## 📞 Support

If you encounter issues, check:
- GitHub Actions logs for deployment errors
- cPanel file manager to verify files were uploaded
- Your hosting provider's documentation for FTP details

