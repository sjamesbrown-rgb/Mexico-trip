# Setup — Mexico Trip Guide

Three pieces:
1. `index.html` — the trip guide app
2. `sw.js` — service worker (offline support)
3. `Google_Doc_Template.md` — paste into a blank Google Doc

Total setup time: ~15 minutes one-time.

---

## Part 1 — Google Doc (do this first, ~2 min)

1. Open [docs.google.com](https://docs.google.com) → blank doc
2. Open `Google_Doc_Template.md` in any text editor, copy everything
3. Paste into the blank Google Doc — Google will auto-format the headers and tables
4. Title it: **Mexico Trip — Live Notes**
5. Click **Share** (top right) → add Alyssa's email → set to **Editor**
6. Also click **Share** → **Copy link** → save the link somewhere — you need it next

---

## Part 2 — Add your Google Doc link to the guide (~1 min)

1. Open `index.html` in any text editor (TextEdit on Mac is fine)
2. Find this line near the bottom of the file (around line 801):
   ```
   const NOTES_URL = "PASTE_YOUR_GOOGLE_DOC_LINK_HERE";
   ```
3. Replace `PASTE_YOUR_GOOGLE_DOC_LINK_HERE` with your Google Doc share URL
4. Save the file

That's the only edit you need to make.

---

## Part 3 — Host on GitHub Pages (~10 min)

1. Go to [github.com/new](https://github.com/new)
2. Repository name: `mexico-trip` (or anything you want)
3. Set to **Public** (required for free GitHub Pages)
4. Check "Add a README file"
5. Click **Create repository**

Once created:

6. On the repo page, click **Add file** → **Upload files**
7. Drag in `index.html` and `sw.js`
8. Commit at the bottom of the page
9. Click **Settings** (top of repo) → **Pages** (left sidebar)
10. Under "Build and deployment" → Source → select **Deploy from a branch**
11. Branch: **main**, folder: **/ (root)** → **Save**
12. Wait 1–2 minutes. The page reloads showing your URL: `https://[your-username].github.io/mexico-trip/`

---

## Part 4 — Add to phones (~2 min each)

**iPhone/iPad (Safari):**
1. Open the GitHub Pages URL in Safari
2. Tap the **Share** button (square with up arrow)
3. Scroll down, tap **Add to Home Screen**
4. Name it "Mexico Trip" → **Add**
5. Opens like a real app from the home screen icon

**Android (Chrome):**
1. Open the URL in Chrome
2. Tap the **3-dot menu** → **Add to Home Screen** (or "Install app")
3. Done

**Send to Alyssa:** just text her the URL. She does the same steps on her phone.

---

## Updating the guide later

1. Edit `index.html` locally
2. Go to your repo on GitHub → click `index.html` → click the pencil icon to edit (or upload a new version)
3. Commit changes
4. Both phones get the update on next refresh (might need to fully close and reopen the home-screen app once)

---

## Troubleshooting

- **"Live notes link not set yet" alert:** You forgot Part 2. Edit `index.html`, paste your Google Doc URL, re-upload to GitHub.
- **Offline isn't working:** Open the URL with internet first, navigate around, then it caches. Try airplane mode after.
- **Tab bar looks weird:** Try fully closing Safari and reopening from home screen.
- **Wife's checklist doesn't match yours:** That's expected — checklists are per-device. Use the Google Doc for shared status.
