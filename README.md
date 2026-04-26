# Anal Roy Chowdhury — Academic Personal Website

Minimalist academic website built with plain HTML/CSS.
Ready for deployment on **GitHub Pages** (zero build step required).

---

## 📁 Folder Structure

```
analroy-site/
├── index.html          ← Home (bio, research focus, news)
├── publications.html   ← Full publications list
├── patent.html         ← Patent IN580844 B1 details
├── projects.html       ← Research & GitHub projects
├── cv.html             ← CV download page
├── contact.html        ← Contact & references
├── css/
│   └── style.css       ← Single stylesheet (all pages share this)
└── assets/             ← Place your compiled CV PDFs here
    ├── Anal_Roy_Chowdhury_CV_Detailed.pdf   ← compile from cv_version_a.tex
    └── Anal_Roy_Chowdhury_CV_OnePage.pdf    ← compile from cv_version_b.tex
```

---

## 🚀 GitHub Pages Deployment (Step-by-Step)

### Step 1 — Create a GitHub repository

1. Log in at [github.com](https://github.com).
2. Click **New repository**.
3. Name it exactly: `analroy.github.io`
   *(replace `analroy` with your actual GitHub username — must match exactly)*
4. Set visibility to **Public**.
5. Click **Create repository**.

### Step 2 — Add your CV PDFs

1. Compile `cv_version_a.tex` and `cv_version_b.tex` in Overleaf (or locally with pdflatex).
2. Download the PDFs and rename them:
   - `Anal_Roy_Chowdhury_CV_Detailed.pdf`
   - `Anal_Roy_Chowdhury_CV_OnePage.pdf`
3. Place them in the `assets/` folder.

### Step 3 — Push the site to GitHub

```bash
# In your terminal, navigate to the analroy-site/ folder
cd path/to/analroy-site

# Initialise git
git init
git add .
git commit -m "Initial commit: academic website"

# Add your GitHub remote (replace USERNAME)
git remote add origin https://github.com/USERNAME/USERNAME.github.io.git

# Push
git branch -M main
git push -u origin main
```

### Step 4 — Enable GitHub Pages

1. Go to your repository on GitHub.
2. Click **Settings** → **Pages** (left sidebar).
3. Under **Source**, select:
   - Branch: `main`
   - Folder: `/ (root)`
4. Click **Save**.

### Step 5 — Visit your site

After ~1–2 minutes, your site will be live at:

```
https://USERNAME.github.io
```

*(Replace `USERNAME` with your GitHub username)*

---

## 🔧 Customisation Tips

| What to change | Where |
|---|---|
| Photo / avatar | Replace the `🎓` emoji in `index.html` header with an `<img>` tag |
| Name & bio text | `index.html` — header and `.bio` section |
| Add new publications | `publications.html` — copy a `.pub-item` block |
| Add new projects | `projects.html` — copy a `.project-card` block |
| Update CV PDFs | Replace files in `assets/` |
| Color palette | `css/style.css` — edit `:root` CSS variables |
| Custom domain | GitHub Settings → Pages → Custom domain |

---

## 🌐 Custom Domain (Optional)

To use `www.analroychowdhury.com` instead of `username.github.io`:

1. Purchase a domain from Namecheap, GoDaddy, etc.
2. In your domain's DNS settings, add a CNAME record:
   - Name: `www`
   - Value: `username.github.io`
3. In GitHub Pages settings, enter your custom domain.
4. Create a file named `CNAME` in the root of your repo:
   ```
   www.analroychowdhury.com
   ```

---

## ✅ Checklist Before Going Live

- [ ] All links in `index.html` point to correct pages
- [ ] CV PDFs placed in `assets/` folder
- [ ] Social links (Scholar, GitHub, LinkedIn, Twitter) verified
- [ ] Email addresses correct
- [ ] Patent details match the granted document
- [ ] Repository name matches GitHub username exactly
- [ ] GitHub Pages enabled in repository settings
