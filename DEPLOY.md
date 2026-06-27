# Deploy from GitHub to Vercel

## Step 1: Create a GitHub repo

1. Go to https://github.com/new
2. Repository name: `exynos-digital-service` (or whatever you like)
3. Choose **Public** or **Private** — doesn't matter
4. **Don't** initialize with README, .gitignore, or license (we have those already)
5. Click **Create repository**

## Step 2: Push the code

Open a terminal in the `exynos-site` folder and run:

```bash
cd exynos-site

git init
git add .
git commit -m "Initial commit - Exynos Digital Service landing page"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/exynos-digital-service.git
git push -u origin main
```

Replace `YOUR_USERNAME` with your actual GitHub username.

If GitHub asks you to authenticate, use a **Personal Access Token** (not your password):
- Go to https://github.com/settings/tokens
- Generate new token (classic) with `repo` scope
- Use it as the password when prompted

## Step 3: Deploy on Vercel

1. Go to https://vercel.com/new
2. Sign in with GitHub
3. Click **Import** next to your `exynos-digital-service` repo
4. Vercel will auto-detect it as a static site — leave all settings as default
5. Click **Deploy**

That's it. Your site will be live at `https://exynos-digital-service.vercel.app` in about 30 seconds.

## Optional: Custom domain

After deployment:
1. Go to your project on Vercel → **Settings** → **Domains**
2. Add your custom domain
3. Follow Vercel's instructions to update your DNS

## Auto-deploy

Every time you `git push` to GitHub, Vercel will automatically redeploy your site. No extra steps needed.

## If something breaks

**Build fails?**
- Check the Vercel deployment logs
- Make sure `public/index.html` exists
- Make sure `vercel.json` is valid JSON (no trailing commas)

**Site looks wrong on mobile?**
- Hard refresh on your phone (Ctrl+Shift+R on desktop browser, or clear cache on mobile)
- Vercel caches aggressively on first deploy