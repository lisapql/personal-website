# Hao Li — personal website

A plain HTML/CSS personal site. No build step, no Node.js, no frameworks. Just open the files in a browser.

## Files

```
personal-site/
├── index.html          ← Home (photo + bio + featured research)
├── experience.html     ← Research, teaching, industry, awards
├── projects.html       ← Working papers
├── writing.html        ← Published papers + conferences
├── contact.html        ← Email and social links
├── styles.css          ← Shared styles for every page
├── assets/             ← Put portrait.jpg here
└── pdf/                ← Put Hao_Li_CV.pdf here
```

## Step 1 — Add your portrait photo

Put a portrait photo at `assets/portrait.jpg` (3:4 aspect ratio works best — roughly 540×720 px).
Then in `index.html`, replace this block:

```html
<div class="hero-photo">
  <div class="hero-photo-placeholder">Add a portrait at<br>assets/portrait.jpg</div>
</div>
```

with:

```html
<div class="hero-photo">
  <img src="assets/portrait.jpg" alt="Portrait of Hao Li">
</div>
```

## Step 2 — Add your CV PDF

Compile your LaTeX CV with `pdflatex` and copy the resulting PDF to `pdf/Hao_Li_CV.pdf`.
The CV link in the header already points there.

## Step 3 — Fill in your social links

Search-and-replace these placeholders in every `.html` file:

- `https://github.com/` → your GitHub profile URL
- `https://www.linkedin.com/` → your LinkedIn profile URL
- `https://scholar.google.com/` → your Google Scholar profile URL

In `contact.html`, also replace `your-username` and `your-handle` with the actual usernames.

## Step 4 — Preview locally

Just double-click `index.html` to open it in your browser. That's it.

## Step 5 — Put it on GitHub

1. Go to https://github.com and create a new repository called `personal-site` (public, no README).
2. On the new repo page, click **"uploading an existing file"**.
3. Drag the entire contents of this folder (not the folder itself — its contents) into the upload area.
4. Scroll down and click **Commit changes**.

## Step 6 — Deploy with GitHub Pages (free, no extra signup)

1. In your repo on GitHub, click **Settings** (top right of the repo page).
2. In the left sidebar, click **Pages**.
3. Under "Build and deployment" → "Source", choose **Deploy from a branch**.
4. Under "Branch", select **main** and **/ (root)**, then click **Save**.
5. Wait ~1 minute. Refresh the Pages settings page — it will show your site URL, something like:
   `https://your-github-username.github.io/personal-site/`

That's it. Your site is live. Every time you push changes to GitHub, the site auto-updates within a minute or two.

## (Optional) Deploy with Vercel instead

Same idea but with a nicer URL and faster updates:

1. Go to https://vercel.com and sign in with GitHub.
2. Click **Add New → Project** and import your `personal-site` repo.
3. Click **Deploy** (default settings work — Vercel auto-detects plain HTML).
4. Get a URL like `personal-site-yourname.vercel.app`. You can also add a custom domain later.

## Making changes later

Open any `.html` file in a text editor (or ask Claude Code), edit the content, save, then either:

- **GitHub web edit:** open the file on github.com → click the pencil icon → edit → commit.
- **Locally:** edit → drag the changed file back to GitHub to upload.

The site updates automatically after you commit.
