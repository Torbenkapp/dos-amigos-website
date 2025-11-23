# Deployment Guide

## Setting Up GitHub Pages

To complete the deployment of the Dos Amigos website, follow these steps:

### 1. Enable GitHub Pages

1. Go to your repository on GitHub: `https://github.com/Torbenkapp/dos-amigos-website`
2. Click on **Settings** (gear icon)
3. In the left sidebar, click on **Pages** (under "Code and automation")
4. Under "Build and deployment":
   - **Source**: Select "GitHub Actions"
5. Click **Save**

### 2. Trigger the Deployment

The deployment will automatically start when you:
- Merge this PR to the `main` branch, OR
- Push changes to the `copilot/deploy-latest-version` branch (already done!)

Alternatively, you can manually trigger the workflow:
1. Go to the **Actions** tab in your repository
2. Click on **Deploy to GitHub Pages** workflow
3. Click **Run workflow** button
4. Select the branch and click **Run workflow**

### 3. Access Your Deployed Website

Once the workflow completes (usually takes 1-2 minutes), your website will be live at:

**Primary URL: https://dosamigos.dk**

Alternative GitHub Pages URL: https://torbenkapp.github.io/dos-amigos-website/

The custom domain `dosamigos.dk` is already configured and verified with GitHub Pages.

### 4. Verify the Deployment

1. Go to the **Actions** tab
2. You should see the "Deploy to GitHub Pages" workflow running or completed
3. Click on the workflow run to see details
4. Once it shows a green checkmark ✓, your site is deployed
5. The deployment summary will show the URL where your site is published

## Troubleshooting

### Workflow doesn't run
- Ensure GitHub Actions are enabled in repository settings
- Check that the workflow file is in `.github/workflows/deploy.yml`

### Deployment fails
- Check the workflow logs in the Actions tab for specific errors
- Ensure GitHub Pages is enabled and set to "GitHub Actions" as source
- Verify repository permissions allow GitHub Pages deployment

### Page not loading
- Wait a few minutes after deployment completes
- Clear your browser cache
- Check that all file paths in `index.html` are correct (case-sensitive)

## Custom Domain

Your website is configured to use the custom domain **dosamigos.dk**.

The CNAME file in the repository root ensures that GitHub Pages serves the site at this domain.

### DNS Configuration

Your domain `dosamigos.dk` is already verified and configured with GitHub Pages. The DNS records should be pointing to GitHub's servers.

## Continuous Deployment

This setup enables continuous deployment:
- Every push to `main` branch automatically deploys to GitHub Pages
- Changes are live within 1-2 minutes
- No manual intervention needed after initial setup

## Need Help?

If you encounter any issues:
1. Check the Actions tab for workflow run details
2. Review the workflow logs for error messages
3. Ensure all prerequisites are met
4. Contact GitHub Support if needed
