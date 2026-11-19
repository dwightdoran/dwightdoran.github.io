# Cybersecurity Portfolio

Edit the Markdown pages in `docs/`. Navigation is defined in `mkdocs.yml`.

## Preview on Windows

```powershell
py -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
.\.venv\Scripts\python.exe -m mkdocs serve
```

Open http://127.0.0.1:8000. Replace the `serve` command with `build --strict` to validate the site.

## Automatic deployment

The workflow in `.github/workflows/deploy.yml` builds the site with `mkdocs build --strict` and deploys it to GitHub Pages on every push to `main`. It can also be run manually from **Actions → Deploy portfolio to GitHub Pages → Run workflow**.

One-time setup: enable **Settings → Pages → Build and deployment → Source → GitHub Actions**. This public repository uses GitHub Pages on GitHub Free. Both the source repository and the deployed website are public.

Site URL: https://dwightdoran.github.io/

After deployment is enabled, publish changes with:

```powershell
git add docs mkdocs.yml requirements.txt README.md .github/workflows/deploy.yml
git commit -m "Update portfolio"
git push
```

Check the Actions run for build errors and deployment status. A failed build prevents deployment, leaving the last successful site in place. No personal access token or repository secret is needed by the workflow.
