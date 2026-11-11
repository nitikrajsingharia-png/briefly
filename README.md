# Briefly v0.4 — Midnight Editorial

Mobile-first dark editorial PWA for a daily current-affairs reading experience.

## Included in this release
- Midnight charcoal and warm champagne visual system.
- Responsive mobile-first briefing feed and bottom navigation.
- Entire story card opens its article; bookmark control remains independently clickable.
- Article reader with low-opacity decorative watermark treatment.
- Persistent bottom highlight / Notion action toolbar while an article is open.
- On-demand Samsung One UI-inspired `Aa` font-size bottom sheet (five sizes).
- Font preference persists in localStorage and applies to article text and value-added facts.
- Fluid transitions, touch feedback, glass-like surfaces and reduced-motion support.
- Value Added for UPSC block for relevant facts/concepts and syllabus links.
- Updated service-worker cache version to ensure clients fetch the new release.

## Important limitations
- Existing story entries are illustrative editorial templates, not verified current news.
- No real story-specific image assets have been supplied. The reader currently uses a subdued abstract watermark motif; replace with a relevant editorial image only when a verified image source is available.
- Court judgments, statistics and constitutional provisions are not fabricated. The Value Added block displays supplied facts and syllabus connections; specific judgments/data should be added only with verified references.
- Highlighting and saved articles are browser-local. Cross-device sync is not yet implemented.
- The Notion button is a UI placeholder. Real sync requires a secure server-side Notion integration and user authorisation.
- Live news ingestion, ranking and push notifications are not connected in this static GitHub Pages build.

## Deploy to the existing GitHub Pages repository
1. Extract the ZIP.
2. Open the existing `briefly` repository.
3. Choose **Add file → Upload files**.
4. Upload all files inside this folder to the repository root, replacing existing files when prompted.
5. Commit the changes.
6. Wait for GitHub Pages deployment.
7. On Android Chrome, reopen the site. If the old shell remains, close the installed PWA and reopen it after the service worker activates; if needed clear site data for the GitHub Pages site and reinstall.

No new repository is needed. The published URL stays the same.
