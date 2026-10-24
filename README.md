# Repository Town — independent GitHub Pages preview

This repository is an **alternate preview deployment**, not the canonical source or the approved production/backup mirror.

- Canonical source: https://github.com/joshualparris/JoshMemory/tree/main/repository-town
- Main game (existing saves): https://repository-town-claude-complete.vercel.app/
- Approved release mirror (existing saves): https://parris-tech-services.github.io/Repository-town/
- This independent preview (once GitHub Pages has been enabled and the workflow succeeds): https://joshualparris.github.io/repository-town/
- Deployment workflow: [Repository Town Pages Alternate](.github/workflows/town-pages-alt.yml)

## Safety and testing

The workflow checks out current canonical `JoshMemory/main`, runs `npm ci`, `npm run build:release` (full release, integration, privacy and integrity gates), verifies `dist/public/release.json`, and uploads the built game using official GitHub Pages actions. It **never** replaces the existing approved Parris-Tech-Services Pages mirror.

A different origin means browser `localStorage` and saved games do not automatically transfer. Use saved-progress export/import rather than assuming games from Vercel or another Pages domain appear here. Keep the original main game available.

Once deployed, test the mobile Dialogue settings switch under HUD + and the X dismiss control on an opted-in nearby yarn; confirm manual NPC conversations still work. Record the exact release SHA before recommending this as the primary URL.

If the Pages job reports that Pages isn't enabled, a repository administrator must set **Settings → Pages → Build and deployment → Source: GitHub Actions**. The workflow must be re-run after that. A failed workflow is not a published alternative.
