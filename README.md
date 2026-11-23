# SkillSetu (prototype)

Mobile-first web app: skill-gap test, learning track, Skill Passport, employer dashboard.
Hindi/English, mobile-number OTP login (demo), saved progress. One file: `public/index.html`.

## Deploy (pick one)

### 1. Netlify Drop (fastest, 2 minutes)
1. Open https://app.netlify.com/drop
2. Drag the `public` folder onto the page.
3. Copy the link you get.

### 2. GitHub Pages (auto-deploys on every push)
1. Create a new GitHub repo and upload everything in this folder (keep `.github/workflows/deploy.yml`).
2. Repo Settings > Pages > Source: **GitHub Actions**.
3. Push to `main`. The site appears at `https://<username>.github.io/<repo>/`.

### 3. Vercel
1. Import the GitHub repo on vercel.com.
2. Framework: Other. Output directory: `public`. Deploy.

### 4. Run locally
Open `public/index.html` in any browser. No build step.

## Good to know
- **AI test generation** works only inside Claude. On your own site the "Create my test with AI" button falls back to the built-in electrician test. "Quick demo (offline)" always works.
- **Login is a demo.** OTP is simulated on screen and accounts are stored in the browser (localStorage) on that device only. For real users use Firebase Phone Auth or Supabase Auth.
- A real AI feature needs a small backend that keeps the Anthropic API key private. Never put the key in `index.html`.
