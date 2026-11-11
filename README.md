# Briefly — Daily Intelligence (v0.2)

A responsive, blue-and-green dark-mode PWA prototype for a daily current-affairs briefing tailored to UPSC / UPPCS and PSIR.

## Product requirements implemented in this prototype
- Ten priority editorial slots per daily edition (not an arbitrary five-story cap).
- Story categories and a priority-based reading feed.
- Article detail structure: Introduction, Significance, Challenges / Critical concerns, Way Forward, UPSC / PSIR relevance, Prelims fact file, and an expert-synthesis Conclusion.
- The editorial schema allows sections to be omitted when they are not materially relevant; the conclusion remains mandatory for every article.
- Save articles to a browser-local reading list.
- Select text in an article and save the selected passage to browser-local highlights.
- Responsive mobile and desktop layouts, installable PWA shell, and basic offline caching.

## Important limitations
- The ten entries in `app.js` are illustrative editorial templates, **not verified current news**. Do not publish them as live news. Replace each day's content with verified, dated source material and direct article links.
- Saved articles and highlights currently live in this browser's `localStorage`; they do not yet sync across devices.
- The “Save highlight to Notion” action is an integration placeholder. Secure Notion saving needs a server-side Notion integration/OAuth flow; never put a Notion secret in browser JavaScript. Once connected, selected text should be saved with article title, source URL, date, and the selected passage.
- Live RSS ingestion, automatic AI analysis, remote push notifications, and scheduled publishing are not connected yet. Browser notification permission alone does not deliver remote notifications while the app is closed.

## Local preview
From this folder run:

```bash
python -m http.server 8080
```

Then visit `http://localhost:8080`. Service workers require localhost or HTTPS; they do not work reliably from `file://`.

## Free deployment direction
- Host the static PWA on GitHub Pages.
- Use a scheduled GitHub Actions workflow for a daily feed build within free usage limits.
- Keep secrets in server-side repository secrets or a serverless worker, never in client files.
- Add Notion integration through a secure server-side endpoint. A Notion integration must be granted access to the destination page/database; consult the official API reference before implementing.
- Add Web Push/FCM only after deployment and device subscription testing. Free quotas and provider terms can change.

## Editorial standard for every published story
1. Rank by materiality, novelty, public impact, policy consequence and exam relevance.
2. Cite primary sources wherever possible; include publication date and direct source link.
3. Separate verified facts, official claims, estimates and analytical inference.
4. Use only relevant analytical sections (for example, do not force a “Challenges” section for a simple factual appointment).
5. Always end with a concise, defensible expert conclusion that synthesises the issue rather than merely repeating the introduction.
