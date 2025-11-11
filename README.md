# CEWD Summit Booth Demo Site

Static site used for the “Beyond the Buzz: AI & the Next Generation Workforce” presentation. Everything needed for GitHub Pages lives in this folder—HTML, media assets, and the model badges/icons.

## Contents
- `index.html` – main landing page
- `ai_model_logos/` – Claude, Gemini, Oodex, Sora, Veo, NotebookLM, Synthesia badges
- `grid-storage-vr-fixed_lights.html` – embedded 3D demo
- `cewd_summit_video.mp4`, `AI_Transforming_Energy-podcast.mp4`, `ai-energy-podcast.mp3` – media featured on the page
- `ai-energy-podcast-player.html` – lightweight audio iframe used to render the inline podcast player

## Local Preview
```bash
cd /path/to/cewd/summit
python3 -m http.server 4000
# open http://localhost:4000 in your browser
```

## Prepare for GitHub Pages
1. **Create a repo** on GitHub (e.g., `cewd-summit-demo`).
2. **Initialize locally** inside this folder:
   ```bash
   git init
   git add .
   git commit -m "Initial summit site"
   git branch -M main
   git remote add origin git@github.com:YOUR-ORG/cewd-summit-demo.git
   git push -u origin main
   ```
3. **Enable Pages**: in the GitHub repo, go to *Settings → Pages*, choose **Source: Deploy from a branch**, **Branch: main**, **Folder: / (root)**, and save. Within a few minutes, your site is live at `https://YOUR-ORG.github.io/cewd-summit-demo`.

## Large File Note
GitHub rejects files over 100 MB. `ai-energy-podcast.wav` (≈165 MB) is optional and **not** used by the inline player (which streams the MP3). Delete it before committing or track it with Git LFS if you really need the raw WAV.

## Post-Deploy Checklist
- Ensure the Synthesia, video, and audio embeds play from the published URL.
- Click each “Copy Prompt” button to verify clipboard permissions.
- Update the `promptSets` data inside `index.html` if you need to swap in new scenarios later.
