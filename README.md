# Dos Amigos Website

A simple, clean website ready for deployment with GitHub Pages.

## 🚀 Quick Start - Upload Your Files

If you have your own website files on your local PC, follow these steps to upload and launch them:

### Option 1: Using Git (Recommended)

1. **Clone this repository** to your local PC:
   ```bash
   git clone https://github.com/Torbenkapp/dos-amigos-website.git
   cd dos-amigos-website
   ```

2. **Replace the template files** with your own:
   - Copy your HTML, CSS, JavaScript, and other files into the repository folder
   - Make sure you have an `index.html` file (this is your homepage)
   - Keep the `.github/workflows/deploy.yml` file for automatic deployment

3. **Upload your changes** to GitHub:
   ```bash
   git add .
   git commit -m "Upload my website files"
   git push origin main
   ```

4. **Your website will automatically deploy!** Check the Actions tab on GitHub to see the deployment progress.

### Option 2: Using GitHub Web Interface

1. **Go to the repository** on GitHub: https://github.com/Torbenkapp/dos-amigos-website

2. **Upload your files**:
   - Click "Add file" → "Upload files"
   - Drag and drop your website folder contents (HTML, CSS, images, etc.)
   - Make sure your main HTML file is named `index.html`
   - Click "Commit changes"

3. **Enable GitHub Pages**:
   - Go to Settings → Pages
   - Under "Build and deployment", select "GitHub Actions" as the source
   - Your site will be deployed automatically!

## 🌐 Accessing Your Live Website

Once deployed, your website will be available at:
```
https://torbenkapp.github.io/dos-amigos-website/
```

You can find the exact URL in:
- Repository Settings → Pages
- The Actions tab after a successful deployment

## 📁 Project Structure

```
dos-amigos-website/
├── index.html          # Your homepage (required)
├── styles.css          # Your CSS styles
├── .github/
│   └── workflows/
│       └── deploy.yml  # Automatic deployment configuration
├── .gitignore          # Files to ignore in git
└── README.md           # This file
```

## 🛠️ Local Development

To preview your website locally before uploading:

1. **Simple way**: Just open `index.html` in your web browser

2. **With a local server** (recommended for testing):
   ```bash
   # Using Python 3
   python -m http.server 8000
   
   # Using Python 2
   python -m SimpleHTTPServer 8000
   
   # Using Node.js (if you have npx)
   npx serve
   ```
   Then open http://localhost:8000 in your browser

## 📝 Customization Tips

### Replacing Template Content

The current files are templates. To add your own content:

1. **Update index.html** with your own text and structure
2. **Modify styles.css** to match your design preferences
3. **Add your images** to the repository (create an `images/` folder if needed)
4. **Add more pages** by creating additional HTML files (e.g., `about.html`, `contact.html`)

### Adding Your Own Files

- Place all website files in the root directory
- Images go in an `images/` or `assets/` folder
- JavaScript files can be in a `js/` or `scripts/` folder
- Additional CSS files can be in a `css/` folder

## 🔄 Updating Your Website

Whenever you want to update your website:

1. Make changes to your files locally
2. Commit and push to GitHub:
   ```bash
   git add .
   git commit -m "Update website content"
   git push origin main
   ```
3. The website will automatically redeploy with your changes!

## ⚙️ GitHub Pages Setup

If GitHub Pages is not enabled yet:

1. Go to repository **Settings**
2. Navigate to **Pages** in the left sidebar
3. Under "Build and deployment":
   - **Source**: Select "GitHub Actions"
4. Save and wait a few minutes for deployment

The workflow will automatically deploy your site whenever you push to the main branch.

## 🆘 Troubleshooting

**Website not showing up?**
- Check the Actions tab for deployment status
- Verify GitHub Pages is enabled in Settings → Pages
- Wait a few minutes after pushing changes

**404 Error?**
- Make sure you have an `index.html` file in the root directory
- Check that the file name is exactly `index.html` (lowercase)

**Changes not appearing?**
- Clear your browser cache (Ctrl+F5 or Cmd+Shift+R)
- Wait a few minutes for deployment to complete

## 📄 License

This project is open source and available for personal or commercial use.

## 🤝 Contributing

Feel free to fork this repository and customize it for your needs!