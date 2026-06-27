# Exynos Digital Service

Next-Gen API Topup Gateway landing page — mobile-friendly single-page site for the Exynos Razer Gold Telegram bot service.

## Stack

- Pure static HTML/CSS/JS
- Google Fonts (Syne, Lexend)
- Font Awesome 6

No build step required. No framework. Just static files.

## Local Development

```bash
# Option 1: Just open the file
open public/index.html

# Option 2: Use Vercel CLI for local dev with proper routing
npm install -g vercel
vercel dev
```

## Deploy to Vercel

### Option A: Vercel CLI (fastest)

```bash
cd exynos-site
npm install -g vercel
vercel login
vercel
```

For production:
```bash
vercel --prod
```

### Option B: GitHub + Vercel Dashboard

1. Push this folder to a GitHub repo:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/exynos-site.git
   git push -u origin main
   ```

2. Go to [vercel.com/new](https://vercel.com/new)
3. Import the repository
4. Vercel auto-detects it as a static site — just click **Deploy**

### Option C: Drag & Drop

1. Go to [vercel.com/new](https://vercel.com/new)
2. Drag the `exynos-site` folder into the browser
3. Done

## Project Structure

```
exynos-site/
├── public/
│   └── index.html       # Main page (the entire site)
├── vercel.json          # Vercel config (static, security headers)
├── package.json         # Project metadata
├── .gitignore
└── README.md
```

## Contact

- Email: tanenusg@gmail.com
- Phone: +251 909259439
- Telegram: @vx_lecter

© 2026 Exynos Digital Service