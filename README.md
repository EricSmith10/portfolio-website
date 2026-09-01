# Eric Smith — Portfolio

A single-page portfolio site. Plain HTML/CSS/JS, no build step, ready for GitHub Pages.

## Files
- `index.html` — page content and structure
- `style.css` — all styling
- `script.js` — active-section nav highlighting
- `assets/eric-smith-resume.pdf` — downloadable résumé

## Deploy on GitHub Pages
1. Create a new GitHub repository (e.g. `portfolio`).
2. Upload all files in this folder to the repository (keep the `assets` folder as-is).
3. In the repo, go to **Settings > Pages**.
4. Under **Build and deployment**, set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`. Save.
5. GitHub will give you a URL like `https://yourusername.github.io/portfolio`. It can take a minute to go live.

## Connect jgsmith.ca
1. In the same **Settings > Pages** screen, enter `jgsmith.ca` under **Custom domain** and save. GitHub will create a `CNAME` file in your repo automatically.
2. In Cloudflare DNS for jgsmith.ca, add:
   - Four `A` records for `@` pointing to GitHub's IPs: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - One `CNAME` record for `www` pointing to `yourusername.github.io`
3. Set these records' proxy status to **DNS only** (grey cloud, not orange) — GitHub Pages requires this for its own certificate to work.
4. Back in GitHub Pages settings, check **Enforce HTTPS** once it becomes available (can take a few minutes to an hour after DNS updates).

## Updating content later
All the résumé content lives directly in `index.html`, split into `<section>` blocks (Experience, Projects, Skills, Publications, Contact) — edit the text there and refresh.
