# tradevis-legal

Static landing page for Tradevis legal documents (Privacy Policy and Terms of Use).
Hosted via GitHub Pages so the App Store submission has a working public URL.

## Deploy in 4 steps

```bash
# 1. From this folder, init the repo
cd /Users/roko2/Desktop/tradevis-legal
git init -b main
git add .
git commit -m "initial: privacy + terms"

# 2. Create a NEW PUBLIC repo on github.com/new named tradevis-legal
#    (don't initialize it with a README — leave it empty)

# 3. Push
git remote add origin https://github.com/RokoPavelic/tradevis-legal.git
git push -u origin main
```

4. On github.com, go to the repo's **Settings → Pages**, choose:
   - **Source:** Deploy from a branch
   - **Branch:** `main` / `(root)`
   - Save

Within ~60 seconds your site is live at:

```
https://rokopavelic.github.io/tradevis-legal/
https://rokopavelic.github.io/tradevis-legal/privacy.html
https://rokopavelic.github.io/tradevis-legal/terms.html
```

## When you buy `tradevis-trading.app`

In the same Pages settings:
- Add the custom domain
- Configure DNS at your registrar (GitHub Pages docs cover this)
- Update `jarvis/app/(tabs)/settings.tsx` lines that point at the legal URLs to the new domain (or leave them on the github.io URL — both work)

## Editing the documents

The HTML files are plain and self-contained. To update:

1. Edit `privacy.html` or `terms.html`
2. Update the "Last updated" date in the header
3. `git commit -am "update: ..."` and `git push`

GitHub Pages redeploys within a minute.
