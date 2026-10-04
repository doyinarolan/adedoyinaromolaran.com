# adedoyinaromolaran.com

Static personal résumé site: plain HTML, CSS and JS with no build step. It's hosted on GitHub Pages.

```
index.html                       the page
styles.css                       finance theme (light default, dark-mode switch)
script.js                        dark-mode switch, scroll reveals, count-up figures
404.html                         custom not-found page
favicon.svg
Adedoyin_Aromolaran_Resume.pdf   downloadable résumé (temporary: replace with your general CV)
assets/                          logos and certificate images (web-sized)
CNAME                            tells GitHub Pages the custom domain
.nojekyll                        serve files as-is (skip Jekyll processing)
```

The original full-size logos (`LewaLauncherLogo.png`, `LewaLauncherLogo.ico`, `ocufoliologo.png`, `olashorelogo.webp`) are not used by the page. Delete them or move them out before pushing if you want a cleaner repo.

---

## Deploying with GitHub Pages

### 1. Create the repository
1. Go to https://github.com/new while signed in as **doyinarolan**.
2. Name it `adedoyinaromolaran.com` (any name works). Set it to **Public**, which free GitHub Pages requires, and leave out the README, .gitignore and licence.

### 2. Push this folder
From PowerShell or Git Bash, inside this folder:

```bash
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/doyinarolan/adedoyinaromolaran.com.git
git push -u origin main
```

If you don't use git, open the new repo on GitHub, click **uploading an existing file**, and drag in everything in this folder. That includes `CNAME`, `.nojekyll` and the `assets` folder. Windows Explorer hides dotfiles, so check that `.nojekyll` made it.

### 3. Turn on Pages
1. In the repo, go to **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to *Deploy from a branch*, **Branch** to `main`, and **Folder** to `/ (root)`, then click **Save**.
3. Within a minute or two the site is live at `https://doyinarolan.github.io/adedoyinaromolaran.com/`.

### 4. Point your domain at GitHub (at your domain registrar)
In the DNS settings for **adedoyinaromolaran.com**, delete any existing A/AAAA records on `@` (often a "parking" page). Then add:

| Type  | Host / Name | Value                    |
|-------|-------------|--------------------------|
| A     | @           | 185.199.108.153          |
| A     | @           | 185.199.109.153          |
| A     | @           | 185.199.110.153          |
| A     | @           | 185.199.111.153          |
| AAAA  | @           | 2606:50c0:8000::153      |
| AAAA  | @           | 2606:50c0:8001::153      |
| AAAA  | @           | 2606:50c0:8002::153      |
| AAAA  | @           | 2606:50c0:8003::153      |
| CNAME | www         | doyinarolan.github.io    |

The AAAA records are optional (IPv6) but recommended.

### 5. Connect the domain in GitHub
1. Go back to **Settings → Pages → Custom domain**. Enter `adedoyinaromolaran.com` and click **Save**. The `CNAME` file in this repo already contains this, so it may be pre-filled.
2. Wait for the DNS check to pass. This usually takes minutes, but it can take up to 24 hours.
3. Tick **Enforce HTTPS** once GitHub has issued the certificate. The option is greyed out until then.

`www.adedoyinaromolaran.com` will redirect to the apex domain automatically.

### 6. (Recommended) Verify the domain
To stop anyone else from claiming your domain on GitHub, go to **GitHub → Settings (your profile) → Pages → Add a domain**. Add the TXT record it shows you at your registrar, then click **Verify**.

---

## Updating the site
- **Résumé PDF:** replace `Adedoyin_Aromolaran_Resume.pdf` with a file of the same name, then commit and push. Or rename it and update the three `href="Adedoyin_Aromolaran_Resume.pdf"` links in `index.html`.
- **Content:** edit `index.html`, then commit and push. GitHub redeploys in about a minute.
- **Preview locally:** double-click `index.html`, or run `python -m http.server` in this folder and open http://localhost:8000.
