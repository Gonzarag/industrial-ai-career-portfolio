# GitHub Publishing Guide

This guide assumes two local repositories:

1. `engineering-report-generator`
2. `industrial-ai-career-portfolio`

## A. Publish Engineering Report Generator

From the `engineering-report-generator` folder:

```bash
git status
git add .
git commit -m "Complete milestone 1 engineering report generator MVP"
```

Create a new GitHub repository named:

```text
engineering-report-generator
```

Then connect and push:

```bash
git branch -M main
git remote add origin https://github.com/<your-github-username>/engineering-report-generator.git
git push -u origin main
```

If the remote already exists:

```bash
git remote -v
git remote set-url origin https://github.com/<your-github-username>/engineering-report-generator.git
git push -u origin main
```

## B. Update Industrial AI Career Portfolio

Copy these generated files into your `industrial-ai-career-portfolio` repository:

```text
README_updated.md
projects/report-automation/engineering-report-generator/README.md
case-studies/engineering-report-generator.md
assets/screenshots/engineering-report-generator/
```

Rename:

```text
README_updated.md
```

to:

```text
README.md
```

inside the portfolio repository.

Then commit and push:

```bash
git status
git add .
git commit -m "Add engineering report generator portfolio project"
git push
```

## C. Add GitHub links after publishing

After the engineering project repository is public, update the portfolio project README and case study with the repository link:

```text
https://github.com/<your-github-username>/engineering-report-generator
```

## D. Recommended pinned repositories

Pin these on your GitHub profile:

1. `industrial-ai-career-portfolio`
2. `engineering-report-generator`

## E. Final safety check before publishing

Before pushing:

```bash
git status
```

Confirm that these are not included:

```text
data/private/
*.env
real company data
real customer names
real supplier names
real operator names
real equipment IDs
real pseudonymization dictionaries
```

The Engineering Report Generator `.gitignore` should protect `data/private/`.
