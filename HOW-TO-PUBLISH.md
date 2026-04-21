# How to Publish the NHA Licensure Guide on GitHub Pages

This folder is a self-contained website. When you follow these steps, anyone with the passcode **`Cottonwood1!`** and the public URL will be able to access the guide.

## What's in this folder

```
site/
├─ index.html              ← the guide (password-gated)
├─ .nojekyll               ← tells GitHub Pages to serve files as-is
├─ HOW-TO-PUBLISH.md       ← this file
└─ documents/              ← all original Colorado PDFs (linked from the site)
   ├─ 3-CCR-717-1.pdf
   ├─ NHA-Practice-Act.pdf
   ├─ NHA-Board-Policies.pdf
   ├─ Key-Definitions-and-Actions.pdf
   ├─ NHA-Experience-Verification.pdf
   ├─ Pathway-2-Overview-Example.pdf
   ├─ Colorado-NHA-License-Overview.pdf
   └─ Colorado-NHA-License-Overview-v2.pdf
```

## One-time setup

1. Create a free GitHub account at https://github.com/signup if you don't have one.
2. Click **New repository** (the green button on your GitHub home page).
3. Name it something like `nha-colorado-guide` and choose **Public** (required for free Pages hosting — the passcode keeps the content private).
4. Check **Add a README file** and click **Create repository**.

## Upload the site

1. On the new repo page, click **Add file → Upload files**.
2. Drag **everything inside this `site/` folder** into the upload box — `index.html`, `.nojekyll`, `HOW-TO-PUBLISH.md`, and the entire `documents/` folder.
3. Scroll down and click **Commit changes**.

## Turn on GitHub Pages

1. In the repo, click **Settings** (top-right of the repo menu).
2. In the left sidebar click **Pages**.
3. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
4. Under **Branch**, select **main** and **/ (root)**, then click **Save**.
5. Wait 1–2 minutes. Refresh the Pages settings page — you'll see a message: *"Your site is live at https://<your-username>.github.io/nha-colorado-guide/"*.

That URL is what you share. Anyone who opens it must enter `Cottonwood1!` to see the guide.

## Updating the site later

To change content or swap out a PDF:
1. Open the file in your repo on GitHub.
2. Click the pencil icon (edit), make your changes, and commit.
3. GitHub Pages redeploys automatically within a minute.

To upload new PDFs, go to the `documents/` folder in the repo and use **Add file → Upload files**.

## Changing the passcode

Open `index.html` in the repo, click the pencil icon, and search for `Cottonwood1!`. Replace both occurrences with your new passcode, then commit.

## Security note

This passcode gate keeps the page hidden from casual visitors, but the content is loaded by any browser that opens the page — a technically savvy user could still view the source. For truly sensitive material, host behind real authentication (e.g. a private web app). For an internal-only guide for new hires, this setup is appropriate.
