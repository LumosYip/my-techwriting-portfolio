# Steps to Update GitHub

This document describes how I run the MkDocs site locally, update content, and deploy the latest version to GitHub Pages.

---

## Run the Site Locally

If you want to preview or build the documentation locally:

``` bash
		pip install mkdocs
		cd my-docs
		mkdocs serve
```

Then open the local preview:

```
 http://127.0.0.1:8000/
```

---

## Deployment Workflow

This project is deployed with GitHub Pages using ```mkdocs gh-deploy```

Below is the full setup and deployment process.

```bash
# Enter the project directory
cd my-docs

# Initialize Git (only for the first time)
git init
git add .
git commit -m "Initial commit: add MkDocs project"

# Connected to the remote repository
git remote add origin https://github.com/LumosYip/my-techwriting-portfolio.git
git branch -M main

# Pull existing remote content to avoid conflicts
git pull origin main --rebase
# (If conflicts occur：git add . && git rebase --continue)

# Push local content to GitHub
git push -u origin main

# Deploy to GitHub Pages
mkdocs gh-deploy
```

After deployment, the site is available at:

```
https://LumosYip.github.io/my-techwriting-portfolio/
```

## Update Workflow

Whenever new content is added or updated:

```bash
git add .
git commit -m "Update docs"
git push
mkdocs gh-deploy
```

---

## Collaboration & Review

This project follows GitHub's standard collaboration workflow:

- **Pull Requests**: For content changes, reviews, and version control
- **Issues**: For suggestions, feedback, and trackig documentation 
