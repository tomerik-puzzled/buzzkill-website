# Buzzkill Website

A single-page site for the film *Buzzkill*: concept, proof-of-concept video, story, visual language, investor snapshot, team, and timeline.

## Files
- `index.html` — the whole site (HTML + CSS + JS in one file)
- `assets/` — poster, stills, and team photos. Referenced by `index.html` using plain relative paths (e.g. `assets/poster.jpg`), so if you swap a photo, keep the same filename or update the reference in `index.html`.

## Before you publish
1. **Contact email** — the "Get in Touch" and "Request Full Deck" buttons currently point to `hello@buzzkillmovie.com`. Open `index.html`, search for `mailto:`, and swap in your real email address (twice).
2. **Investor numbers** — the Invest section shows budget, tax credit estimate, and comparables pulled from your pitch deck. Since this will be public, double check you're comfortable with those figures being visible to anyone, not just people you send the deck to.

## Publish with GitHub Pages (free)
1. Create a new GitHub repository (e.g. `buzzkill-site`).
2. Upload `index.html` **and** the `assets` folder to the repo (drag-and-drop both onto github.com works, or `git push`). Keep the folder named `assets` — that's what `index.html` expects.
3. In the repo, go to **Settings → Pages**.
4. Under "Build and deployment," set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`. Save.
5. GitHub will give you a URL like `https://yourusername.github.io/buzzkill-site/` within a minute or two.

## Adding your own domain (e.g. buzzkillmovie.com)
1. Buy the domain (Namecheap, Cloudflare Registrar, etc.).
2. In your domain's DNS settings, add:
   - An `A` record pointing `@` to GitHub Pages' IPs: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - A `CNAME` record pointing `www` to `yourusername.github.io`
3. Back in the repo's **Settings → Pages**, enter your custom domain in the "Custom domain" field and save. GitHub will create a `CNAME` file in your repo automatically — don't delete it.
4. DNS changes can take up to 24 hours to propagate, though it's often much faster.

That's it — no build step, no server, nothing to maintain.
