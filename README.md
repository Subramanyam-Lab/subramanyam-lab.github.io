# Systems Optimization Laboratory @ Penn State — Website Contributor Guide

Welcome to the Systems Optimization Lab website repository!  
This README explains how to update your personal profile, add news items, and manage publications. Follow these instructions to keep our site accurate and up to date.

---

## Table of Contents

1. [Editing Your Profile](#1-editing-your-profile)
2. [Adding or Editing News Items](#2-adding-or-editing-news-items)
3. [Adding or Editing Publications](#3-adding-or-editing-publications)
4. [Adding Repositories](#4-adding-repositories)
5. [Previewing Your Changes Locally](#5-previewing-your-changes-locally)
6. [Submitting Your Changes](#6-submitting-your-changes)
7. [Need Help?](#need-help)

---

## 1. Editing Your Profile

Each lab member has a profile file in `_pages/about/`.

**To update your profile:**

1. Locate your profile file (e.g., `_pages/about/eduardo.md`).
2. Edit the file using Markdown. Update your name, research topic, email, and relevant links.

**To update your picture**

1. Add image to `/assets/img/team`
2. Change image name in your profile file

_Note:_ Only `.jpg` images are compatible for profile pictures. Please ensure your image file uses the `.jpg` extension.

**Profile Template:**

```markdown
## Your Name

_Joined group in [Semester Year]_

Research topic: [Your research topic]

Email: [mailto:your.email@domain.edu](mailto:your.email@domain.edu)
Links: [LinkedIn](https://linkedin.com/in/yourprofile)
```

3. Save and commit your changes. Use a descriptive commit message (e.g., `Update profile for Eduardo Lopez Ledezma`).

---

## 2. Adding or Editing News Items

News items are stored in the `_news/` directory as Markdown files.

**To add a news item:**

1. Create a new file in `_news/` named `YYYY-MM-DD-title.md`.
2. Use this template for an in-line news item:

```markdown
---
title: "Short News Title"
date: YYYY-MM-DD
author: Your Name
inline: true
---

Brief description of the news item.
```

**To edit an existing news item:**

- Open the relevant file in `_news/` and make your changes.

---

## 3. Adding or Editing Publications

Publications are listed in the `_bibliography/` directory.

**To add a publication:**

1. Create a new file in `_bibliography/` named `YYYY-title.md`.
2. Use this template:

```markdown
---
title: "Publication Title"
authors: Author1, Author2, Author3
journal: Journal Name
year: YYYY
doi: https://doi.org/xxxx
---

Short summary or abstract of the publication.
```

**To edit a publication:**

- Open the relevant file in `_bibliography/` and update details as needed.

---

## 4. Adding a Repository

1. Make sure your repository is ready to go public (no sensitive files, clear README, builds cleanly).

2. Set visibility to Public:

- GitHub → Settings → General → Change repository visibility → Public.

- Verify the link opens in a private/incognito window without login.

3. Send the repository link to the repository maintainer via Slack.

4. Wait for confirmation before making further changes.

## 5. Previewing Your Changes Locally

Before submitting a Pull Request, preview your updates on your machine to confirm formatting, links, and images render correctly.

### Recommended: Docker preview

1. Install [Docker](https://docs.docker.com/get-docker/) and [Docker Compose](https://docs.docker.com/compose/install/).
2. From the repository root, start the site:

```bash
docker compose pull
docker compose up
```

3. Open your browser to `http://localhost:8080`.

Edits to your profile, news, or publications (Sections **1–3**) will hot‑reload within a few seconds. If the container shows errors, check logs and enter the container:

```bash
docker compose logs
docker compose exec -it jekyll /bin/bash
bundle install
./bin/entry_point.sh
```

For more detail, see **al‑folio**’s guide: [Local setup using Docker (Recommended)](https://github.com/alshedivat/al-folio/blob/main/INSTALL.md#local-setup-using-docker-recommended).

### Alternative: Local Jekyll preview

If you already have Ruby, Bundler, and Python set up (legacy approach):

```bash
bundle install
pip install jupyter
bundle exec jekyll serve
```

Then open `http://localhost:4000`. See: [Local Setup (Legacy)](https://github.com/alshedivat/al-folio/blob/main/INSTALL.md#local-setup-legacy-no-longer-supported).

If everything looks good locally, proceed to Section **5. Submitting Your Changes**.

## 6. Submitting Your Changes

To contribute updates or new content to the Systems Optimization Lab website, follow these streamlined steps:

1. **Fork & Clone**  
   Fork the repository to your GitHub account, then clone it to your computer:

```bash
git clone https://github.com/your-username/subramanyam-lab.github.io.git
cd subramanyam-lab.github.io
```

2. **Create a Branch**  
   Make a new branch for your changes:

```bash
git checkout -b update-profile
```

3. **Edit Files**  
   Update your profile, add news, or publications as needed. Follow the templates in the repo for consistency.

4. **Commit Changes**  
   Add and commit with a clear message:

```bash
git add .
git commit -m "Update profile for [Your Name]"
```

5. **Push & Open Pull Request**  
   Push your branch and open a Pull Request on GitHub. Explain your changes briefly.

6. **Review**  
   Respond to any feedback, make adjustments if needed, and wait for merge.

This process keeps the site accurate and ensures every update gets reviewed.

---

## Need Help?

Questions or issues? Contact the repository maintainer or open a GitHub issue.

---

Happy contributing!
