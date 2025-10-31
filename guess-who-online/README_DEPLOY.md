
# Guess Who — Online Hosting Guide

This folder is ready to deploy your app online. It contains:
- `index.html` — your entire app (single file).
- `packs/index.json` — starter packs list (empty).

## Option A — GitHub Pages (free, quick)
1. Create a new GitHub repo (public is easiest).
2. Upload **both** files/folders from this zip:
   - `index.html`
   - `packs/index.json`
3. In your repo, go to **Settings → Pages**:
   - **Source**: Deploy from a branch
   - **Branch**: `main` (or `master`) → `/root`
   - Click **Save**
4. After a minute, your site will be live at:
   `https://<YOUR-USER>.github.io/<YOUR-REPO>/`

### Community packs (read-only GitHub mode)
- Copy the link to: `https://raw.githubusercontent.com/<YOUR-USER>/<YOUR-REPO>/main/packs/index.json`
- In the app's **Community** tab, paste that link into **Raw GitHub JSON URL** and click **Use URL**.
- To add a pack for everyone:
  1) Use **Export My Pack JSON** (in app) to download your pack file.
  2) Add that file to your repo at `/packs/your-pack.json`.
  3) Edit `/packs/index.json` and append an entry like:
     {
       "id": "p-abc123",
       "name": "My Pack",
       "author": "YourName",
       "description": "Short description",
       "createdAt": 1730380000000,
       "tags": ["tag1"],
       "jsonUrl": "https://raw.githubusercontent.com/<YOUR-USER>/<YOUR-REPO>/main/packs/your-pack.json",
       "thumb": ""
     }
  4) Commit. Hit **Refresh** in the Community tab.

## Option B — Netlify / Cloudflare / Vercel (drag & drop)
- Go to Netlify Drop, Cloudflare Pages, or Vercel.
- Create a new project and **upload the contents** of this folder (or connect the GitHub repo).
- Your site will deploy to a nice URL instantly.

## Notes
- App uses only browser features (no server). localStorage is used for autosave and local community posts.
- Fullscreen and file uploads require a user click (browser security requirement).
- If you paste a GitHub Raw URL, make sure the file is **public** and the URL is the **raw** link.

