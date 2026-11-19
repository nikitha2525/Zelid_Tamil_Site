# தமிழ் AI படைப்பாற்றல் சவால் 2026 – Zelid Tech (Tamil event site)

A static site with no build step, ready to deploy on Vercel.

```
zelid-site/
├── index.html          ← Tamil event page (/)
├── vercel.json         ← clean URLs + asset caching
└── assets/
    ├── poster.jpg      ← official event poster
    ├── bharathi.webp   ← Bharathiyar artwork (cut from the poster)
    ├── og.jpg          ← social-share preview image
    ├── favicon.svg
    ├── zelid-logo-white.svg
    └── zelid-logo-navy.svg
```

## Deploy to Vercel (about 2 minutes)

**Option A – Vercel CLI (fastest)**

1. Install Node.js 18 or later from https://nodejs.org
2. Open a terminal inside the `zelid-site` folder and run:
   ```bash
   npx vercel@latest login
   npx vercel@latest --prod
   ```
3. Answer the prompts:
   - *Set up and deploy?* → **Y**
   - *Which scope?* → your account (nikithamurugan2525-6292's projects)
   - *Link to existing project?* → **N**
   - *Project name* → `tamil-ai-creative-challenge` (or any name)
   - *In which directory is your code located?* → `./`
   - *Want to modify these settings?* → **N** (there's no build step; it's plain HTML)
4. The CLI prints your live URL, for example `https://tamil-ai-creative-challenge.vercel.app`.

**Option B – GitHub + Vercel dashboard**

1. Create a new GitHub repository and upload everything inside `zelid-site/` to it.
2. Go to https://vercel.com/new and import that repository.
3. Framework preset: **Other**. Leave the build and output settings empty, then click **Deploy**.
4. From then on, every push to the repository redeploys the site automatically.

## After the first deploy

- **Social preview:** in `index.html`, change `<meta property="og:image" content="assets/og.jpg">`
  to the full URL, for example `https://tamil-ai-creative-challenge.vercel.app/assets/og.jpg`, so
  WhatsApp and LinkedIn show the poster when the link is shared. Then redeploy (`npx vercel@latest --prod`).
- **Custom domain:** Vercel → Project → Settings → Domains.

## Where to edit content

| What | Where |
|---|---|
| Registration link | `https://openmadurai.org/sl/MsQuFQP0`, in `index.html` (search for `MsQuFQP0`) |
| Dates (Dec 9 / Dec 11) | `index.html`: the hero facts, timeline and FAQ sections; countdown deadline in the `<script>` at the bottom (`2026-12-09T23:59:59+05:30`) |
| Fee (₹50) | `index.html`: hero facts, registration section and FAQ |
