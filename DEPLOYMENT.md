# Deployment Documentation

## How Long Does It Take to See Updates?

When you change a file in this repository and push to the `main` branch, your updated website will be live in approximately **1-2 minutes**.

### Detailed Timeline

Here's what happens after you push changes:

1. **GitHub Actions Trigger** (instant): The deployment workflow starts automatically
2. **Workflow Execution** (~15-20 seconds): GitHub Actions builds and deploys your site
   - Checkout code: ~2 seconds
   - Setup Pages: <1 second
   - Upload artifact: ~2 seconds
   - Deploy to GitHub Pages: ~5 seconds
3. **GitHub Pages Propagation** (~30-60 seconds): GitHub's CDN updates globally
4. **Browser Cache** (variable): Your browser may cache the old version

**Total time: Typically 1-2 minutes from push to seeing changes live**

## Deployment Method

This website is deployed using **GitHub Pages** with automated deployment via **GitHub Actions**.

### GitHub Actions Workflow

The deployment is handled by a GitHub Actions workflow which:
- Triggers automatically on every push to the `main` branch
- Can also be triggered manually via workflow dispatch
- Checks out the repository
- Configures GitHub Pages
- Uploads the site as an artifact
- Deploys to GitHub Pages

> **Note**: If you don't see a `.github/workflows/deploy.yml` file in the main branch yet, the workflow may need to be set up. A template workflow file exists in other branches of this repository.

### What Gets Deployed?

All files in the repository root are deployed, including:
- `index.html` - The main website
- `style.css` - Styling
- `Pictures/` - Images and videos

## How to Deploy Changes

### Standard Deployment Process

1. **Make your changes** to any files in the repository
2. **Commit your changes**:
   ```bash
   git add .
   git commit -m "Your descriptive commit message"
   ```
3. **Push to the main branch**:
   ```bash
   git push origin main
   ```
4. **Wait 1-2 minutes** for the deployment to complete
5. **Check the Actions tab** on GitHub to monitor progress
6. **Visit your website** to see the changes

### Viewing Deployment Status

You can monitor the deployment in real-time:

1. Go to your repository on GitHub
2. Click the **"Actions"** tab
3. Look for the "Deploy to GitHub Pages" workflow
4. Click on the latest run to see detailed progress

A green checkmark ✓ means deployment succeeded.

## Troubleshooting

### Changes Not Appearing?

If you don't see your changes after 2-3 minutes:

1. **Check the workflow status**: Visit the Actions tab to ensure deployment succeeded
2. **Hard refresh your browser**: 
   - Windows/Linux: `Ctrl + F5` or `Ctrl + Shift + R`
   - Mac: `Cmd + Shift + R`
3. **Clear browser cache**: Sometimes browsers aggressively cache static sites
4. **Try incognito/private mode**: This bypasses all caching
5. **Check your commit**: Make sure your changes were actually committed and pushed

### Workflow Failed?

If the GitHub Actions workflow fails:

1. Click on the failed workflow run in the Actions tab
2. Review the error messages in the job logs
3. Common issues:
   - Syntax errors in HTML/CSS
   - Missing files or broken links
   - GitHub Pages configuration issues

### Manual Deployment

You can manually trigger a deployment:

1. Go to the **Actions** tab on GitHub
2. Select **"Deploy to GitHub Pages"** workflow
3. Click **"Run workflow"** button
4. Select the `main` branch
5. Click **"Run workflow"**

## Website URL

Your website is accessible at: `https://<username>.github.io/<repository-name>/`

For this repository: `https://torbenkapp.github.io/dos-amigos-website/`

## Technical Details

- **Platform**: GitHub Pages
- **CI/CD**: GitHub Actions
- **Branch**: `main`
- **Build Time**: ~15-20 seconds
- **Deployment Time**: ~5 seconds
- **Total Propagation**: 1-2 minutes
- **CDN**: GitHub's global CDN
