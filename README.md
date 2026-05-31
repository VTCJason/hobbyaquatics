# 5th Sunday — Veritas

**AI for Real Life** — Veritas Life Group · 5th Sunday Presentation · May 2026  
Live at: [www.hobbyaquatics.com](https://www.hobbyaquatics.com)  
GitHub Pages — account: VTCJason

---

## What This Is

A single-page reference website prepared for the Veritas Life Group 5th Sunday presentation on AI tools, how they work, and how to use them well. Attendees scan a QR code to follow along on their phones during the presentation and keep the site as a take-away reference.

---

## Deploying to GitHub Pages

### Step 1 — Create the GitHub repository

```bash
# From inside this folder:
git init
git add .
git commit -m "Initial site build — Veritas 5th Sunday AI presentation"
git branch -M main
git remote add origin https://github.com/VTCJason/hobbyaquatics.com.git
git push -u origin main
```

### Step 2 — Enable GitHub Pages

1. Go to your repo on GitHub → **Settings** → **Pages**
2. Under **Source**, select **Deploy from a branch**
3. Branch: `main` / Folder: `/ (root)`
4. Click **Save**

Your site will be live at `https://vtcjason.github.io/hobbyaquatics.com` within a few minutes.

### Step 3 — Connect your custom domain

1. In **Settings → Pages → Custom domain**, enter `www.hobbyaquatics.com`
2. At your domain registrar, add a CNAME record:
   - Name: `www`
   - Value: `vtcjason.github.io`
3. Enable **Enforce HTTPS** once the domain verifies

### Step 4 — Generate a QR code for the presentation

Go to any free QR code generator (e.g., [qr.io](https://qr.io) or [qrcode-monkey.com](https://www.qrcode-monkey.com)) and enter `https://www.hobbyaquatics.com`. Print or display at each table so attendees can scan it.

---

## Project Structure

```
5thSunday-Veritas/
├── index.html                          ← The entire site (single self-contained page)
├── .nojekyll                           ← Tells GitHub Pages not to use Jekyll
├── README.md
└── resources/
    ├── documents/
    │   ├── AI_Voices_Assessment.html   ← Full fact-check document (linked from site)
    │   ├── SWOT_4x4_Final_3.html       ← Full SWOT 4×4 panel (linked from site)
    │   ├── Blog_SWOT Analysis.pdf
    │   ├── Best AI Tools May 2026.docx
    │   ├── Visual Prompt Guide (2).docx
    │   └── ChatGPTFullDiscussionContent.docx
    ├── graphics/
    │   ├── IBMBenchMarkAgenticCapability.jpeg
    │   └── Writing better AI Image Prompts.png
    └── video/
        ├── Presidential State of AI Address.mp4
        └── Dr Enzocto Dofleini.mp4
```

> **Note on videos:** Both videos are embedded from YouTube via `<iframe>` for reliable mobile playback.
> The local MP4 files are source copies. Do not commit large binary files to git.

---

## Updating the Site

All content lives in `index.html` — no build step, no framework, no dependencies.
Edit directly, commit, push. GitHub Pages updates within 1–2 minutes.
