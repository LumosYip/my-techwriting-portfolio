# Welcome to Lumos's Docs

This repo is basically my little corner for organizing notes, trying out different documentation styles, and building a personal documentation website with MkDocs.

I’ve been exploring technical writing, translation workflows, and a bit of forensics-related documentation, so I wanted a place to structure everything—and GitHub Pages happens to be a perfect fit.


---

## What’s Inside

This project uses MkDocs + Material Theme to turn Markdown files into a full documentation site.

```
		docs/
		├─ index.md                     ← homepage
		├─ writing/                     ← technical writing notes
		├─ translation/                 ← translation & CAT tools
		├─ forensics/                   ← digital forensics notes
		└─ tools/                       ← tools & writing utilities
```

Everything starts as a .md file in the docs/ folder, then MkDocs builds it into a static site.


---

## Run It Locally

If you want to take a look or build the site yourself:

```
		pip install mkdocs
		cd my-docs
		mkdocs serve
```

Then open:

```
 http://127.0.0.1:8000/
```

---

## Deployment

This project is deployed with GitHub Pages.
Once everything is set up, I just push my changes and GitHub takes care of the rest.

```bash
# Enter the project directory
cd my-docs

# Initialize Git (only the first time)
git init
git add .
git commit -m "Initial commit: add MkDocs project"

# Connected to remote repository
git remote add origin https://github.com/LumosYip/my-techwriting-portfolio.git
git branch -M main

# Pull existing remote content (prevent conflict)
git pull origin main --rebase
# (If there are conflicts：git add . && git rebase --continue)

# Push your local content to the remote
git push -u origin main

# Deploy to GitHub Pages
mkdocs gh-deploy
```

Then visit：

```
https://LumosYip.github.io/my-techwriting-portfolio/
```

When you update next time：

```bash
git add .
git commit -m "Update docs"
git push
mkdocs gh-deploy
```

---

## Collaboration & Review

* GitHub Pull Request
* GitHub Issues


