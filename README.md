# Dwight Doran | Cybersecurity Portfolio

I'm a software engineer and Army veteran studying cybersecurity through SANS. My interests include incident response and industrial control systems security. This portfolio documents my CTF participation, the skills I practiced, and how my approach to investigations is developing.

My interest in cybersecurity started a few years ago when I picked up a backlog ticket to fix a potential SQL injection vulnerability flagged by a security scan. The Ruby backend used raw SQL in that part of the application rather than Active Record, its object-relational mapper. After fixing the issue, I wanted to find other vulnerabilities in the codebase. That curiosity grew into a broader interest in cybersecurity and led me to pursue further study through SANS.

[Visit my portfolio](https://dwightdoran.github.io/) · [Read my CTF reflection](docs/ctf-experience.md) · [Explore the techniques I practiced](docs/ctf-techniques.md)

## My CTF experience

Fall 2026 NCL was my first CTF, and I had a lot of fun. I was nervous going into it, especially the team portion, but working through the Gym exercises helped me realize I was more prepared than I had thought. Looking back, I wish I had participated in Spring 2026 as well. The experience gave me more confidence in applying what I already knew while continuing to learn.

One lesson was to inspect the underlying evidence before trusting a tool's summary or an application's display. Raw responses can reveal information the interface leaves out, and a readable result still needs verification. Recording unsuccessful attempts also helped me narrow the next question instead of repeating the same approach.

## Participation highlights

- **Team contribution:** completed all the questions in the Web App Exploitation section for my team. We divided the sections according to our strengths, and I took on an area my teammates had either not attempted in the Individual Game or felt less comfortable with.
- **Evidence-based analysis:** compared observations with a baseline and separated direct findings from assumptions.
- **Programming and analysis:** used small Python scripts and command-line tools to parse data, test transformations, and check results.
- **Technical documentation:** maintained Obsidian notes with hypotheses, actions, results, and unanswered questions.
- **Continued learning:** practiced moving between forensics, log analysis, packet inspection, and application analysis while recognizing the limits of each tool.

These are general reflections on my learning. This public portfolio does not reproduce NCL challenge prompts, artifacts, flags, or solution walkthroughs.

## CTF performance

| Event | Standard Student rank | Percentile | Points | Scouting report |
|---|---|---|---|---|
| NCL Fall 2026 Individual Game | 847th of 5,961 players | 86th | 1,890 / 3,000 | [Individual report](https://cyberskyline.com/report/B4NGLDP4VEDT) |
| NCL Fall 2026 Team Game (SANS.edu YARA) | 92nd of 3,034 teams | 97th | 2,915 / 3,000 | [Team report](https://cyberskyline.com/report/4AKJ7YUV32WU) |

Results are taken from the official scouting reports. Team results represent the combined performance of SANS.edu YARA. The report scores exclude the survey module.

## Training and interests

- GIAC Security Essentials (GSEC)
- Incident response and industrial control systems security

## About this site

The portfolio uses MkDocs with the Read the Docs theme and deploys through GitHub Actions. Edit the Markdown pages in `docs/`; navigation is defined in `mkdocs.yml`.

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
