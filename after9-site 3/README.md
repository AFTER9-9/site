# AFTER9 — static site

Plain HTML/CSS/JS, no build step. Ready to push to GitHub Pages.

## Deploy to GitHub Pages

1. Create a new repo on GitHub (e.g. `after9-site`).
2. From this folder:
   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages → Source → Deploy from a branch → main → / (root) → Save**.
4. Your site goes live at `https://YOUR-USERNAME.github.io/YOUR-REPO/` within a minute or two.

If you'd rather skip the command line, you can also drag every file in this folder (keeping the `assets/img` structure intact) directly into a new GitHub repo through the "Add file → Upload files" button on github.com.

## Before you launch — 2 things still need your input

1. **Paystack key** — `script.js` still has a placeholder: `pk_test_xxxx...`. Swap in your real public key from your Paystack dashboard (Settings → API Keys) or no payment button on the site will work.
2. **Duplicate product photos** — `assets/img/le-tee-detail-1.jpg` is identical to `le-tee-front.jpg`, and `le-tee-detail-2.jpg` is identical to `le-tee-back.jpg`. The Limited Edition gallery currently shows the same two photos twice. Swap in two more distinct shots if you want a fuller 4-image gallery.

## What's not in here

The password-protected admin/preview panel from earlier drafts has been removed — this is the clean production version. Site behavior (locked countdown, blurred mystery photos, stock, drop date) is now controlled by editing the values directly in `script.js` under `DROP_CONFIG` and `LE_STATE`, and pushing the change.

## File structure

```
index.html       — markup
style.css        — all styles
script.js        — countdown, carousel, checkout, forms
assets/img/      — product + brand photos
```

Emails (contact form, drop notify signup, order notifications) route to caseyfoatykvs@gmail.com via FormSubmit — first submission after this goes live needs a one-time confirmation click.
