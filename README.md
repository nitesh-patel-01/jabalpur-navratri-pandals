# Jabalpur Navratri Pandals

Created by Nitesh Patel for Jabalpur Navratri Darshan 2026.

## Review

Unzip the website archive and open `dist/index.html`. All pandal and navigation links open separate HTML pages. For device saving and full features, serve the folder with the local command below. Maps and social links need internet. PWA installation needs HTTPS or localhost.

## Website source

`dist/` is a complete static website. No Firebase, accounts, API keys or paid APIs are needed. `source-data.json` stores the public-page snapshot from 30 September 2026. The three available source photographs are included as optimized WebP images. All 117 pandal pages have images: 3 genuine source photographs and 114 clearly labelled representative images. Missing timings and exact coordinates remain labelled.

117 pandals; 53 individual area names (the original site groups Amanpur and Madan Mahal together in its 52-area filter); 31 Mahakali listings. 117 individual pandal pages, 53 area pages plus a main directory, an area index, routes, guide, FAQ and settings pages: 176 pages total.

## Local serving

Run `python3 -m http.server 8000 --directory dist` and visit http://localhost:8000. Use localhost or HTTPS for installation and service worker tests.

## Build and future publication

Node 20.11+ is sufficient. Run `node build.mjs` to rebuild an unpublished preview. Update `source-data.json` for corrected information and rebuild.

Before the approved public launch, run:

`node build.mjs --site-url https://YOUR-ACTUAL-DOMAIN`

Use the verified final origin. This adds canonical URLs, social image metadata, a complete sitemap and indexable robots rules. Preview builds deliberately use noindex and Disallow. Do not publish the preview build unchanged for search indexing.

Vercel: use Other as framework preset, `dist` as output directory, and `node build.mjs --site-url https://YOUR-ACTUAL-DOMAIN` as build command. No installation step is needed. Avoid an SPA rewrite; static pandal and area pages should keep their individual URLs.

After launch, submit sitemap.xml in Google Search Console and verify the final URL. Ranking and indexing are not guaranteed. llms.txt is provided as a readable directory summary; it does not guarantee AI inclusion.

## Functionality

Search by name, area, address and theme; area/category/schedule/saved/visited filters; browser-local saved and visited lists; personal routes; reordered stops; walking/driving Maps links split into mobile-compatible groups; native sharing or clipboard/manual fallback; area selection and optional geolocation with labelled approximate distances; light/dark and compact cards; creator contacts; correction link; FAQs; PWA manifest, service worker and icons.

No live crowd monitoring or backend synchronization is connected. Nearby distance uses source-provided area centroids where available, not exact venue pins. No location is stored or transmitted by the application. User preferences are local to the browser.

## Validation

JavaScript syntax checks passed. Programmatic checks passed for full directory counts, search, filters, saved lists, details, creator contacts and split route links. All generated internal links and local assets resolve. Browser visual QA and HTTPS installation testing remain for the hosted preview/launch.


## 2025 archive photos
Verified matching archive photos added for Maa Hitkarini Dham and Maa Sunarhai Pariwar. Photo pages include Wikimedia Commons sources, credits to Kanha Shivhare / Gamerzer, CC BY-SA 4.0 links and WebP conversion notes. Original watermarks are preserved. Five listings now have matching photos; 112 use labelled animated Jabalpur Navratri Darshan 2026 festival artwork.


Homepage: 12 main pandals, 12 popular area shortcuts and all 53 areas in the expanded directory. Search, category filters and area pages continue to expose the full 117-listing catalogue. Mobile header includes Areas and a native disclosure menu. Festival artwork uses subtle CSS animation with reduced-motion support.
