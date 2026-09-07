# Portfolio site

Plain HTML/CSS/JS — no build step, deploys directly on GitHub Pages.

## Files
- `index.html` — page content
- `style.css` — all styling
- `script.js` — footer year (tiny, optional)

## Edit before publishing
- Replace `you@example.com`, GitHub, and LinkedIn links in `index.html`
- Replace the two "placeholder" projects with your own (title, year, description, tags)
- Adjust the hero line and About section wording to your taste

## Deploy on GitHub Pages (free)

1. Create a new GitHub repository, e.g. `yourusername.github.io` (using your GitHub username makes the URL the domain root; any other repo name works too, just under a `/reponame/` path).
2. Push these three files (`index.html`, `style.css`, `script.js`) to the repository's root (the `main` branch).
3. In the repo, go to **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**, pick `main` and `/ (root)`, then Save.
5. GitHub gives you a live URL within a minute or two, e.g. `https://yourusername.github.io`.

## Point your `.me` domain at it

1. Buy the `.me` domain from any registrar (Namecheap, Google Domains/Squarespace, GoDaddy, etc.).
2. In the repo, add a file named `CNAME` (no extension) at the root containing just your domain, e.g.:
   ```
   yourname.me
   ```
3. In your domain registrar's DNS settings, add:
   - Four **A records** for the apex domain (`yourname.me`) pointing to GitHub's IPs:
     ```
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```
   - One **CNAME record** for `www` pointing to `yourusername.github.io`
4. Back in **Settings → Pages**, enter `yourname.me` under **Custom domain** and save (this also creates/updates the `CNAME` file for you if you skip step 2).
5. DNS can take anywhere from a few minutes to 24 hours to propagate. Once it does, enable **Enforce HTTPS** in the same Pages settings panel.

That's it — no hosting bill, no WordPress server to manage.
