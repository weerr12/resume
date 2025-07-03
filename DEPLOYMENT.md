# 🚀 GitHub Pages Deployment Guide

## Quick Setup (First Time)

### 1. Push Your Code to GitHub

```bash
# Add the new GitHub Actions workflow
git add .
git commit -m "Add GitHub Actions deployment workflow"
git push origin main
```

### 2. Enable GitHub Pages

1. Go to your GitHub repository
2. Click on **Settings** tab
3. Scroll down to **Pages** section (left sidebar)
4. Under **Source**, select **"GitHub Actions"**
5. Save the settings

### 3. Wait for Deployment

- The workflow will automatically trigger on push
- Check the **Actions** tab to see deployment progress
- Your site will be live at: `https://yourusername.github.io/resume`

## How It Works

The GitHub Actions workflow (`.github/workflows/deploy.yml`) automatically:

1. **Triggers** on every push to `main` branch
2. **Sets up** Node.js environment
3. **Installs** dependencies with `npm ci`
4. **Builds** the project with `npm run build`
5. **Deploys** the `dist` folder to GitHub Pages

## Vite Configuration

The `vite.config.ts` is already configured for GitHub Pages:

```typescript
export default defineConfig({
  base: '/resume', // This matches your repository name
  // ... other config
})
```

**Important**: The `base: '/resume'` must match your GitHub repository name exactly.

## Daily Workflow

After the initial setup, your deployment is fully automated:

```bash
# Make changes to your code
# ... edit files ...

# Commit and push
git add .
git commit -m "Update portfolio content"
git push origin main

# Your site automatically updates in ~2-3 minutes!
```

## Troubleshooting

### Site Not Loading?
- Check that repository name matches the `base` in `vite.config.ts`
- Ensure GitHub Pages is set to "GitHub Actions" source
- Check the Actions tab for any build errors

### Build Failing?
- Check the Actions tab for error logs
- Ensure all dependencies are in `package.json`
- Test build locally: `npm run build`

### Custom Domain?
- Add a `CNAME` file to the `public/` folder
- Configure custom domain in repository settings

## Repository Settings Checklist

✅ Repository is public (required for free GitHub Pages)  
✅ Pages source is set to "GitHub Actions"  
✅ Workflow file exists at `.github/workflows/deploy.yml`  
✅ `vite.config.ts` has correct `base` path  

## Success! 🎉

Once set up, every push to `main` automatically deploys your latest changes to:
**https://yourusername.github.io/resume**

Your portfolio is now live and automatically updated!
