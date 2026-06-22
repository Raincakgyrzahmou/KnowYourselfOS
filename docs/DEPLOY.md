# Deploying your own KYO on Vercel

KYO is a single static HTML file — Vercel hosts it with no build step. Your journal data is saved in your browser (`localStorage`) for the site's address, so once deployed, **always open the same Vercel URL in the same browser** and your history stays put.

## 1. Get the repo ready

Make sure `index.html` is in your GitHub repo. If you uploaded the whole `know-yourself-os` folder (so files live under `know-yourself-os/…`), either move them to the repo root, or note the subfolder name — you'll point Vercel at it in step 3.

## 2. Import the project

1. Go to **vercel.com** → sign in with GitHub.
2. **Add New… → Project**.
3. Find **KnowYourselfOS** → **Import**.

## 3. Configure (10 seconds)

- **Framework Preset:** `Other`
- **Build Command:** leave empty
- **Output Directory:** leave default
- **Root Directory:** if your files are inside a subfolder, click **Edit** and choose `know-yourself-os`. If `index.html` is at the repo root, leave it as is.

## 4. Deploy

Click **Deploy**. In ~20 seconds you get a live URL like `https://knowyourselfos.vercel.app`. Open it — that's your private KYO.

> Every future `git push` (or GitHub web edit) auto-redeploys.

## 5. Make it your daily journal

- **Bookmark the URL** and always use the same browser/profile. The data is tied to that address.
- **Turn on AI (optional):** open ⚙️ **AI Settings**, paste your Anthropic API key, hit **Test connection**.
- **Back up often:** ⚙️ Settings → **Back up all data (.json)**. KYO also reminds you on the Today screen if it's been a week. Keep these files somewhere safe (Drive, Dropbox) — they're your safety net.
- **Browse your past:** the 🕘 **History** tab shows every logged day and weekly review as a timeline.

## Moving existing entries from the local file

`localStorage` is per-address, so entries you made by opening the file directly (or on a different URL) won't appear automatically on the Vercel site. To bring them over:

1. Open the old version, go to ⚙️ Settings → **Back up all data (.json)**.
2. Open your Vercel URL, go to ⚙️ Settings → **Restore from backup**, pick that file.

## Notes

- **Privacy is unchanged.** Vercel only serves the static page; it never sees your entries. Your data stays in your browser. (AI generation, if enabled, sends only that section's text directly to Anthropic — see PRIVACY.md.)
- **No `vercel.json` needed.** It's a plain static site.
- **Clearing browser data wipes KYO** for that site — which is exactly why the backup file matters. Back up before clearing or switching machines.
