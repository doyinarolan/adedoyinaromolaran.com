# CLAUDE.md: adedoyinaromolaran.com (personal résumé website)

Read this before changing anything in this folder. It covers the website only. For CVs, cover letters and job tracking, read `..\RULES.md` (the Resume project rules) instead.

Last updated: 6 October 2026

---

## 1. What this is

- A static, single-page résumé site for **Adedoyin Aromolaran**, served at **https://adedoyinaromolaran.com** (the user owns this domain).
- Plain HTML + CSS + a little vanilla JS. **No build step, no framework, no Jekyll.**
- Hosted on **GitHub Pages** under the GitHub account **doyinarolan** (https://github.com/doyinarolan).
- Location on the user's PC: `C:\Users\doyin\Desktop\Work\Resumes\adedoyinaromolaran.com`
- The user previews it by opening `index.html` directly in a browser (file://). After an update, tell them to press **Ctrl + F5**.

## 2. Files

```
index.html                       the whole page (all content lives here)
styles.css                       theme: light default, dark via switch; responsive breakpoints 1000/820/640px
script.js                        dark-mode switch (saved in localStorage), scroll-reveal, active nav link, footer year
404.html                         custom not-found page (self-contained styles)
favicon.svg                      navy tile with green upward-trend arrow
Adedoyin_Aromolaran_Resume.pdf   download link target. TEMPORARY copy of ..\AdedoyinAromolaran_CV_Finance_UK.pdf
assets/                          web-sized images used by the page:
  olashore.png                     Olashore International School crest (experience row)
  ocufolio.png                     cropped tight to the logo frame so it fills its box
  lewalauncher.png                 cropped tight to the "L" (transparent background)
  cert-bloomberg-bff.jpg           certificate images (from ..\*Cert Image.png)
  cert-bloomberg-esg.jpg
  cert-lseg-workspace.jpg
  cert-lseg-finance.jpg
shapeswitchgame/                 Shape Switch minigame, live at /shapeswitchgame (added 6 Oct 2026)
  index.html                       self-contained page (inline CSS + JS); shares the site's theme switch (localStorage "theme")
  assets/*.png                     the user's 7 shapes: Circle, Triangle, Cross, Square, Star, Heart, Pentagon
  Shape Switch Web Game Description.txt   the user's spec (kept local, NOT pushed to the repo)
CNAME                            contains exactly: adedoyinaromolaran.com   (do not delete)
.nojekyll                        empty; tells Pages to serve files as-is      (do not delete)
README.md                        short repo readme
CLAUDE.md                        this file
```

Unused originals still in the folder (the user may delete them before pushing): `LewaLauncherLogo.png`, `LewaLauncherLogo.ico`, `ocufoliologo.png`, `olashorelogo.webp`.
Full GitHub Pages steps written for the user: `..\GitHub Pages Instructions.txt`.

## 3. Page structure (current, as agreed with the user)

1. **Top bar**: "AA" mark + name, section nav, sun/moon **dark-mode switch** (top right).
2. **Hero** (two columns, stacking on mobile):
   - Left: name; degrees line; **contact line with email, UK phone, "United Kingdom"**; short blurb; buttons for *Download résumé (PDF)*, LinkedIn and GitHub.
   - Right: **summary panel** (no heading; the user asked to remove the words "At a glance"). Rows: Education, Certifications (with month/year), Finance, Tools, Programming, Languages.
3. Profile
4. Technical skills, in the order **Finance domains → Analysis & tools → Programming**
5. Professional certifications: **one full-width row each** (image, issuer, name, completion date, "Verify credential" link)
6. Relevant experience (Olashore)
7. Education (UEA 2027, Emory 2024, with all modules as chips)
8. **Completed personal projects**: Ocufolio and LewaLauncher, one full-width row each, logos filling the box with no background
9. Activities | Languages (two columns)
10. Contact grid (email, phone, LinkedIn, GitHub, location, résumé PDF)

## 4. User preferences and decisions (do not undo)

- **Light theme by default for everyone** (ignores the OS dark setting). Dark mode only via the switch.
- **Professional, finance-flavoured but not gimmicky.** These were removed at the user's request, so don't bring them back: the scrolling ticker, the stock/candlestick "career chart", "Holdings"/"Track record"/"§01" style kickers, ▲ bullets, the pulsing "live" dot, the key-figures/count-up panel, and skill tags.
- Looking for **analyst** roles only. Never "developer" in the seeking line. Current wording (the user's choice): "Seeking an analyst in financial services or fintech." (Claude noted that "Seeking analyst positions…" reads better. The user hasn't changed it, so leave it unless asked.)
- Location is **"United Kingdom"** only. No "Norwich" and **no "Atlanta"** anywhere. Emory shows as "BA Computer Science · United States".
- **The UK phone number (+44 7378 978913) and email are shown at the top** (the user's request). No US number.
- Section name is **"Completed personal projects"** (not "Ventures").
- Order: Certifications **above** Experience and Education. Projects come after Education.
- Summary panel stays, **without** an "At a glance" title.

## 5. Content rules (from ..\RULES.md, applied to the site)

- **Never invent anything.** Every fact must come from `..\Raw Resume Data.xlsx` or `..\build_resume.py` (PROFILE, CERTS, ACTIVITIES, LANGUAGES). No new jobs, numbers, skills, tools or achievements. Decorative visuals must not imply fake data.
- Olashore: **January – September 2025**, a **nine-month internship** (never "one-year").
- Certificate completion dates must appear and each must link to its credential:
  - Bloomberg Finance Fundamentals: 26 Feb 2026, https://portal.bloombergforeducation.com/certificates/ZWjW6xRatQTPgC5jnnUdMzPP
  - Bloomberg ESG: 15 Jul 2026, https://portal.bloombergforeducation.com/certificates/mJZtaa8QaJFpDchfyj3VNCJr
  - LSEG Workspace: 19 Sep 2026, https://learningcentre.lseg.com/c/s/AVGdh1W5b7ZcjaaChvwaHkdcBsfZ2dDYMo_FuWf8_m0L-Psbik41pFnPgx1Z68zT
  - LSEG Finance Essentials: 22 Sep 2026, https://learningcentre.lseg.com/c/s/mhI0etEXYLchLk4gl4G8QoW4GG5HRKEatljbf9Wkvi1g09hyiYC1cN-kHMTQWWlm
- Links: LinkedIn https://www.linkedin.com/in/adedoyin-aromolaran-59b7b3204/ · GitHub https://github.com/doyinarolan · Ocufolio https://ocufolio.com/ · LewaLauncher https://lewalauncher.com/ · Olashore https://alumni.olashoreschool.com
- UK spelling throughout (organiser, authorisation).
- When the CV facts change (e.g. a new certificate), update **both** the summary panel and the matching full section.

## 6. Design system

- Fonts (Google Fonts): **Newsreader** (serif headings), **IBM Plex Sans** (body). (IBM Plex Mono is still loaded but barely used.)
- Light tokens: bg `#F6F4EE`, card `#FFFFFF`, ink `#0E1B33`, accent (CV navy) `#1F3864`, green `#0B6B43` (only for certificate dates), rules `#DCD7CA`.
- Dark tokens: bg `#0B0F16`, card `#10161F`, ink `#ECEFF4`, accent `#9DB7E6`, green `#4CC28A`.
- Theme switch: `<html data-theme="light|dark">`. The inline script in `<head>` applies a saved "dark" choice, and `script.js` toggles it and saves to localStorage.
- Section headings: serif with a 2px navy underline. Cards: white, 1px rule border, 10px radius, soft shadow.
- Keep it working at phone width (no horizontal scroll). Test at 390px and 1360px.

## 7. GitHub Pages / domain setup

Status at last update (6 Oct 2026): the repo `doyinarolan/adedoyinaromolaran.com` exists and is live; DNS (4 A records + `www` CNAME at Namecheap) is set. This local folder is still NOT a git repository: Claude pushes from a cloud clone (attach with `add_repo`, push access works now that the Claude GitHub App is installed), then mirrors changes here. Folder names in the repo are **case-sensitive** on GitHub Pages (`shapeswitchgame`, lowercase). Unused original logos are deliberately not in the repo. Shape Switch spec: Classic = 4 shapes, build the new order, 5:00, +20s; Hard = 4–7 shapes, hide original order / key / new order / random, 6:00, +20s + 7s per shape over 4.

Intended setup:
- Repo: `doyinarolan/adedoyinaromolaran.com`, **public**, branch `main`, Pages source "Deploy from a branch → main → / (root)".
- First push (from this folder):
  ```
  git init
  git add .
  git commit -m "Initial site"
  git branch -M main
  git remote add origin https://github.com/doyinarolan/adedoyinaromolaran.com.git
  git push -u origin main
  ```
- Later updates: `git add . && git commit -m "Update site" && git push` (live within about a minute).
- DNS at the registrar for the apex `@`:
  - A records: 185.199.108.153, 185.199.109.153, 185.199.110.153 and 185.199.111.153
  - optional AAAA records: 2606:50c0:8000::153 through 8003::153
  - `www` CNAME → `doyinarolan.github.io`
- In repo Settings → Pages: custom domain `adedoyinaromolaran.com`, then tick **Enforce HTTPS** once the certificate is issued. Recommended: verify the domain under the profile's Settings → Pages (TXT record).
- If Claude needs to push from a cloud session, attach the repo with the `add_repo` tool (owner `doyinarolan`, repo `adedoyinaromolaran.com`, access `push`). Otherwise give the user the git commands to run locally.

## 8. Working notes for Claude

- **Edit the files on the user's computer directly** (device shell, e.g. `python` read-modify-write or `sed -i`) when possible.
- If a file is built in the cloud container and copied over with device_commit_files, **always verify afterwards** (e.g. compare `md5sum` on both sides). On 4 Oct a copy reported success but left the old file in place. The user saw no change until it was re-copied with `force`.
- Check the page visually after changes (headless Chromium/Playwright at 1360px and 390px, light and dark). Note: logos use `loading="lazy"`, so full-page screenshots can show them blank. Scroll to them first.
- Don't reintroduce removed elements (section 4). Keep wording identical to the CV source unless the user asks otherwise.

## 9. Open items / to-dos

- [ ] Replace `Adedoyin_Aromolaran_Resume.pdf` with the user's **general** résumé when it exists (keep the same filename, or update the 3 links in index.html).
- [ ] `git init` and push to GitHub, set up DNS, then enable HTTPS (section 7).
- [ ] Optional: delete the unused original logo files before pushing.
- [ ] Optional: the user may want a LinkedIn profile photo on the site later (their notes mention taking one).
