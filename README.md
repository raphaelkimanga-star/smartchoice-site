# SmartChoice Multi Services LLC — Website

Static website for SmartChoice Multi Services LLC (SDVOSB · UEI SFMFL4AM3EB7 · CAGE 0SQJ7).
No build step — plain HTML, CSS and a few lines of JavaScript.

## Structure

```
index.html                                  Home
capabilities.html                           Core competencies + NAICS by service line
past-performance.html                       Past performance timeline
contracting.html                            UEI/CAGE, certifications, NAICS & PSC tables
about.html                                  Company background, leadership, differentiators
contact.html                                Point of contact
404.html                                    Not-found page
.nojekyll                                   Tells GitHub Pages to serve files as-is
assets/styles.css                           Styles
assets/main.js                              Mobile menu, copy buttons
assets/favicon.svg                          Site icon
assets/SmartChoice_Capability_Statement.pdf Downloadable capability statement
```

## Deploy to GitHub Pages

```bash
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

Then on GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: `main` / `(root)` → Save.**
The site will be live at `https://<your-username>.github.io/<repo-name>/` within a minute or two.

### Custom domain (optional)

1. Add a file named `CNAME` at the repo root containing only your domain, e.g. `smartchoicemultiservices.com`.
2. At your DNS provider, point the domain to GitHub Pages (A records `185.199.108.153`, `.109.153`, `.110.153`, `.111.153`, or a `CNAME` for `www` to `<your-username>.github.io`).
3. In **Settings → Pages**, enter the domain and tick **Enforce HTTPS**.

## Updating content

- Each page is a standalone HTML file — edit text directly in the page you want to change.
- The header menu and footer are repeated in every page; if you change them, change all six files.
- To update the downloadable PDF, replace `assets/SmartChoice_Capability_Statement.pdf` with a file of the same name.

## Preview locally

```bash
python3 -m http.server 8000
# open http://localhost:8000
```
