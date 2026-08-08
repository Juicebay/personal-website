# Personal Website

A simple, warm static academic/career website made with plain HTML and CSS —
no framework or build step needed.

## Pages

- `index.html` — photo, bio, and “what I'm up to now”
- `publications.html` — published work and work in progress
- `projects.html` — research and coding projects
- `cv.html` — education, awards, experience, skills
- `blog.html` — blog posts plus collections, combined in one place
- `blog/welcome.html` — the first post (copy it to add more)
- `blog/hiking.html`, `blog/photography.html`, `blog/reading.html`,
  `blog/coffee.html`, `blog/research-notes.html` — running list pages

## Add your photo

Drop a photo named **`profile.jpg`** into `assets/img/`. The homepage will use
it automatically. A square or portrait crop works best.

## View it locally

Open a terminal in this folder and run:

```bash
python3 -m http.server 8000
```

Then visit [http://localhost:8000](http://localhost:8000) in your browser.

## Edit the content

- Bio, tagline, and “Now” strip: `index.html`
- Papers and talks: `publications.html`
- Projects: `projects.html`
- CV details: `cv.html`
- Blog posts and hobbies: `blog.html` + `blog/`
- Colors, fonts, and layout: `assets/css/style.css`

The CV content was filled in from `CV_guelph.pdf`. The phone number was left
off the public page; add it to `cv.html` if you want it there.

## Add PDFs or links

- Put PDFs in `assets/pdfs/`.
- To link a paper to an external page (DOI, journal, article), replace the
  `href` in `publications.html`.
- Each project card in `projects.html` can hold its own PDF or article link.

## Host it on GitHub Pages

1. Create a new repository on GitHub.
2. In this folder, run:

   ```bash
   git init
   git add .
   git commit -m "Initial website"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
   git push -u origin main
   ```

3. In the repo on GitHub, go to **Settings → Pages**.
4. Under **Build and deployment**, choose **Source: GitHub Actions**.
5. The included workflow (`.github/workflows/pages.yml`) will publish the site
   automatically.

The URL will be `https://YOUR-USERNAME.github.io/YOUR-REPO/`.

If you name the repo exactly `YOUR-USERNAME.github.io`, it will be available at
`https://YOUR-USERNAME.github.io/`.

## Connect a custom domain (optional)

If you have your own domain (for example `yourname.com`), here's how to point
it at GitHub Pages:

1. In the GitHub repo, go to **Settings → Pages**.
2. Under **Custom domain**, enter your domain (for example `yourname.com`) and
   click **Save**.
3. At your domain registrar or DNS provider, add one of these:
   - **Apex/root domain** (`yourname.com`): four `A` records pointing to
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`,
     `185.199.111.153`.
   - **`www` subdomain** (`www.yourname.com`): one `CNAME` record pointing to
     `YOUR-USERNAME.github.io`.
4. Wait for DNS to update (usually a few minutes, sometimes up to 24 hours).
5. To keep the domain attached to the repository, add a file named `CNAME` at
   the project root containing just your domain, for example:

   ```text
   yourname.com
   ```

   Commit and push it. The GitHub Actions workflow will include it in the
   deployment automatically.

Once verified, the site will be available at your custom domain.
