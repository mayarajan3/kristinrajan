# kristinrajan.com

Static site for Kristin Bryant Rajan, hosted on GitHub Pages. Plain HTML/CSS, with no build step.

## Structure
```
index.html                Home: hero, Published Works tiles, Bio, Contact
book.html                 The Book!
poetry.html               Poetry
creative-nonfiction.html  Creative Nonfiction
critical-articles.html    Critical Articles
presentations.html        Conference Presentations
playlists.html            Krist-Spin Playlists (Spotify embeds)
files/                    PDFs of published pieces and playlist song lists
404.html                  Not-found page
css/style.css             All styles (colors and fonts are set at the top in :root)
js/main.js                Mobile menu toggle and footer year
images/                   Photos (see images/README.md)
CNAME                     Custom domain for GitHub Pages
.nojekyll                 Serves the files as they are, without Jekyll processing
```

## Content
All text, PDFs and Spotify links were copied from the old Wix site. Edit the HTML files directly to change them.

## Deploy
1. Push to the `main` branch.
2. Go to Settings → Pages → Build and deployment, choose "Deploy from a branch", then `main` / `(root)`.
3. Under Custom domain, enter `kristinrajan.com`. The `CNAME` file already contains it.
4. At the DNS provider, add these records:
   - `A` records for `@`: 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
   - `CNAME` record for `www`: `<your-username>.github.io`
   - Remove any old Wix A or CNAME records.
5. When the DNS check passes, turn on "Enforce HTTPS".

## Local preview
```
python3 -m http.server 8000
```
Then open http://localhost:8000.
