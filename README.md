# CEWD Summit Booth Demo Site

Static site used for the "Beyond the Buzz: AI & the Next Generation Workforce" presentation. Everything needed for GitHub Pages lives in this folder—HTML, media assets, and the model badges/icons.

🔗 **Live Demo**: [https://gdatalabs.github.io/cewd-summit-2025/](https://gdatalabs.github.io/cewd-summit-2025/)

## Contents

### 📁 Project Structure
```
cewd-summit-2025/
├── index.html                    # Main landing page
├── assets/                       # Media and resource files
│   ├── images/                   # Images and logos
│   │   ├── ai_model_logos/       # Claude, Gemini, Codex, Sora, Veo, NotebookLM, Synthesia badges
│   │   └── *.png                 # G-Data logos and diagrams
│   ├── videos/                   # Video content
│   │   ├── cewd_summit_video.mp4
│   │   ├── AI_Transforming_Energy-podcast.mp4
│   │   └── ai_spokesperson/      # AI spokesperson videos
│   ├── audio/                    # Audio files
│   │   └── ai-energy-podcast.mp3
│   └── documents/                # PDF and presentation files
├── simulations/                  # Interactive 3D demos
│   └── grid-storage-vr-fixed_lights.html
├── demos/                        # Demo applications
│   ├── ai-energy-podcast-player.html
│   ├── ai_workflow_comparison.html
│   └── gdata_one_pager.html
└── practice_1/                   # Additional practice demos
```

## Local Preview
```bash
cd /path/to/cewd/summit
python3 -m http.server 4000
# open http://localhost:4000 in your browser
```

## Prepare for GitHub Pages
1. **Create a repo** on GitHub (e.g., `cewd-summit-2025`).
2. **Initialize locally** inside this folder:
   ```bash
   git init
   git add .
   git commit -m "Initial summit site"
   git branch -M main
   git remote add origin git@github.com:gdatalabs/cewd-summit-2025.git
   git push -u origin main
   ```
3. **Enable Pages**: in the GitHub repo, go to *Settings → Pages*, choose **Source: Deploy from a branch**, **Branch: main**, **Folder: / (root)**, and save. Within a few minutes, your site is live at `https://gdatalabs.github.io/cewd-summit-2025`.

## Large File Note
GitHub rejects files over 100 MB. Any large video files (>100 MB) should be tracked with Git LFS or hosted externally.

## Post-Deploy Checklist
- Ensure the Synthesia, video, and audio embeds play from the published URL.
- Click each "Copy Prompt" button to verify clipboard permissions.
- Update the `promptSets` data inside `index.html` if you need to swap in new scenarios later.
- Test the fullscreen button functionality in `simulations/grid-storage-vr-fixed_lights.html`
- Verify all asset paths resolve correctly in the organized folder structure