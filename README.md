# Cybersecurity Portfolio

Edit the Markdown pages in `docs/`. Navigation is defined in `mkdocs.yml`.

## Preview on Windows

```powershell
py -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
.\.venv\Scripts\python.exe -m mkdocs serve
```

Open http://127.0.0.1:8000. Replace the `serve` command with `build --strict` to validate the site.

## Publish on GitHub Pages

Commit and push the source to a dedicated repository with a remote named `origin`. On GitHub Free, use a public repository. Run `.\.venv\Scripts\python.exe -m mkdocs gh-deploy` to push the generated site to the `gh-pages` branch. In **Settings → Pages**, select **Deploy from a branch**, then **gh-pages** and **/(root)**. Rerun the deploy command after committing future updates.
