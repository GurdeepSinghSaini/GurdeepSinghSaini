# Verification

Checked on 2026-10-09 UTC in Chromium via Qt WebEngine.

- Five SVG panels rendered at 0, 2, 5, 9 and 13 seconds with their timelines explicitly set.
- Each panel rendered with animations removed and embedded as an HTML img element.
- Reduced-motion and 375-pixel mobile previews checked; no horizontal overflow.
- All five images loaded; zero external asset requests during local rendering.
- SVG XML, unique namespaced IDs, data-only image references, embedded WOFF2 fonts and absence of scripts/foreignObject verified.
- Both original PNGs retain RGBA transparency and were checked on dark and light backgrounds.
- Public GitHub project targets and supplied LinkedIn/email paths checked against retrieved sources. An email address's deliverability is not tested.

GitHub may apply its own image sanitization and caching. Local rendering is not proof of pixel-identical behavior on every GitHub client.
