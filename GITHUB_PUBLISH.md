# GitHub Publish Guide

This folder is already initialized as a local Git repo with an initial commit.

## Create The GitHub Repo

Create a new public GitHub repo named:

```text
agent-skills-portfolio
```

Do not initialize it with a README, license, or `.gitignore`; this repo already has those files.

## Push From This Folder

From this folder:

```bash
git remote add origin https://github.com/YOUR-USERNAME/agent-skills-portfolio.git
git push -u origin main
```

If the remote already exists:

```bash
git remote set-url origin https://github.com/YOUR-USERNAME/agent-skills-portfolio.git
git push -u origin main
```

## Portfolio Site Step

Use `portfolio-site-prompt.md` with Lovable, v0, or another site builder. Use `skills.json` as the content source and link each card back to its GitHub folder.
