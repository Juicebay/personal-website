# Personal Website

A simple, elegant static academic/career website made with plain HTML and CSS.
It includes a homepage, publications, CV, blog, and hobbies pages — no framework
or build step needed.

## View it locally

Open a terminal in this folder and run:

```bash
python3 -m http.server 8000
```

Then visit [http://localhost:8000](http://localhost:8000) in your browser.

The site is plain HTML, so you can also just double-click `index.html`, though
the local server is more accurate because it works exactly like GitHub Pages.

## Edit the content

- `index.html` — name, tagline, and about text
- `publications.html` — your papers
- `cv.html` — education, experience, skills
- `blog.html` + `blog/welcome.html` — posts (copy the post file to add more)
- `hobbies.html` — hobbies and interests
- `assets/css/style.css` — colors, fonts, and layout

Search for `[` in the HTML files to find the placeholder text to replace.

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
5. The included workflow (`.github/workflows/pages.yml`) will build and publish
   the site automatically.

For a personal site, the URL will be:
`https://YOUR-USERNAME.github.io/YOUR-REPO/`

If you name the repo exactly `YOUR-USERNAME.github.io`, it will be available at
`https://YOUR-USERNAME.github.io/`.
