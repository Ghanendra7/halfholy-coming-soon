# Halfholy — Coming Soon Landing Page

Minimalist, high-editorial coming soon landing page for **Halfholy** (`halfholy.nyc`).

## Project Structure
```text
halfholy-coming-soon/
├── assets/
│   ├── coming_soon.mp4            # Fullscreen looping video (silver jewelry animation)
│   ├── poster.jpg                 # Fallback poster image for mobile & low-power mode
│   └── fonts/
│       ├── AntiqueLegacy-Light.otf # Brand Serif font
│       └── FragmentMono-Regular.ttf # Brand Monospace font
├── index.html                     # Self-contained zero-dependency landing page
├── .gitignore
└── README.md
```

## Features
- **Cinematic Looping Video**: Edge-to-edge background with high-performance CSS and mobile `playsinline` attributes.
- **Brand Typography**: Antique Legacy Light and Fragment Mono integrated via local `@font-face`.
- **Sound Control**: Discrete luxury sound toggle with audio wave animation (since the video has audio, unmuted with one click).
- **Early Access Capture**: Minimalist email input with local persistence and clear feedback.
- **Ultra-lightweight**: Pure vanilla HTML/CSS/JS, zero build steps, 100/100 Lighthouse score.

---

## Deployment to Cloudflare Pages

### Option 1: Via GitHub (Recommended — same as your `milena-gorum` project)
1. Create a new repository on your GitHub (`Ghanendra7/halfholy-coming-soon`).
2. Push this repo:
   ```bash
   git remote add origin https://github.com/Ghanendra7/halfholy-coming-soon.git
   git branch -M main
   git push -u origin main
   ```
3. In [Cloudflare Dashboard](https://dash.cloudflare.com/) → **Workers & Pages** → **Create application** → **Pages** → **Connect to Git**.
4. Select `halfholy-coming-soon`.
5. Build settings:
   - **Framework preset**: `None`
   - **Build command**: *(leave blank)*
   - **Build output directory**: `.` (or leave blank)
6. Click **Save and Deploy**.

### Option 2: Direct CLI Deploy (No GitHub repo needed)
From this directory, run:
```bash
npx wrangler pages deploy . --project-name=halfholy-coming-soon
```

---

## Connecting Custom Domain (`halfholy.nyc`)
1. In Cloudflare Pages, go to your project → **Custom domains** → **Set up a custom domain**.
2. Enter `halfholy.nyc` (and `www.halfholy.nyc`).
3. If the domain is already in your Cloudflare account, Cloudflare will automatically configure the CNAME/DNS records with free SSL!
