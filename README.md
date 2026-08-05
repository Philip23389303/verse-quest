# Verse Quest — install on iPhone

This is a PWA (installable website), same approach as Luma. No App Store, no $99/year developer account, no review wait — just push it live and add it to your home screen.

## 1. Push to GitHub Pages
1. Create a new repo, e.g. `verse-quest`.
2. Upload these 5 files to the repo root: `index.html`, `manifest.json`, `sw.js`, `icon-192.png`, `icon-512.png`.
3. Repo Settings → Pages → Source: Deploy from branch → `main` / root. Save.
4. Wait ~1 minute, then your app is live at `https://<your-username>.github.io/verse-quest/`.

## 2. Install it on your iPhone
1. Open that URL in **Safari** (must be Safari, not Chrome — Chrome on iOS can't install PWAs).
2. Tap the **Share** button → **Add to Home Screen** → Add.
3. A "Verse Quest" icon appears on your home screen. Tap it — it opens full-screen, no Safari bar, works offline.

## How the game works
- One verse a day, same verse for everyone on a given date (KJV, public domain — no licensing issues).
- Tap the gold seal to break it and reveal the verse.
- A "Fill the Gap" challenge follows — guess the missing word from 4 choices for bonus XP.
- XP levels you up through Seed → Sprout → Sapling → Rooted → Flourishing → Steadfast → Unshaken.
- Daily streak (🔥) tracks consecutive days; badges unlock at 7/30/100 days and 50 verses read.
- Progress is stored locally on the phone (`localStorage`) — private to that device, no backend needed.

## Optional next step: real push notifications
iOS 16.4+ supports Web Push for installed PWAs, so you *can* get an actual "Today's verse is ready" notification — but it needs a small backend to send the push (same shape as the Render service behind Luma). Say the word if you want that added; it's a bigger lift than the app itself.
