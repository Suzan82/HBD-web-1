# Birthday Page — Deploy to Vercel

## Folder structure (already set up for you)
```
birthday-site/
├── index.html
└── assets/
    ├── photos/   → put photo1.jpg ... photo6.jpg here
    ├── voice/    → put voice-message.mp3 here
    └── music/    → put background-music.mp3 here
```
The page works fine even if some/all of these files are missing (photos fall back
to a heart placeholder, voice/music buttons just won't play), so you can deploy
now and add media later.

## Option A — Deploy from your computer (no GitHub needed)
1. Install the CLI once: `npm i -g vercel`
2. From inside this `birthday-site` folder, run:
   ```
   vercel
   ```
3. Answer the prompts (link to a new project, defaults are fine — it's a static
   site, no build command needed).
4. Run `vercel --prod` to push it live.

## Option B — Drag-and-drop (easiest, no terminal)
1. Go to https://vercel.com/new
2. Choose "Deploy" → there's a drag-and-drop area for a folder/zip on that page
   (or use "Import" if you connect a GitHub repo instead — see Option C).
3. Drop the whole `birthday-site` folder in.
4. Vercel auto-detects it as a static site — click Deploy.

## Option C — GitHub + Vercel (best if you'll keep editing it)
1. Create a new GitHub repo, push this folder to it.
2. In Vercel, "Add New Project" → "Import Git Repository" → pick the repo.
3. Framework preset: "Other" (or it may auto-detect "Static").
4. Deploy. Every future `git push` auto-redeploys.

## Notes
- No `vercel.json` or build config is needed — this is plain HTML/CSS/JS.
- File names are case-sensitive on Vercel's servers (unlike Windows), so make
  sure your photo/audio filenames match exactly: `photo1.jpg`, `photo2.jpg`, etc.
- Recommended photo size: keep under ~500KB each so the gallery loads fast.
