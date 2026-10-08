# BookBrain Usage & Execution Log — LLS Photo Disclosures

Date: 2026-10-08 (America/New_York)
Task: Implement approved-only, click-to-show finished-job photo support on LLS website, using BookBrain design guidance.
Status: PARTIAL — approval policy and photo CSS committed; no actual photo published; existing `index.html` was not modified because the page update was blocked by the available connector.
Commercial-use classification: PERSONAL-ONLY (private project execution notes, not a distributable source).

## Sources consulted and decisions influenced

1. `/BookBrain/00_SYSTEM/00_BOOKBRAIN_MAP.md`: verified canonical Dropbox archive and explicit approval gate; mirrors and local staging not canonical.
2. `/BookBrain/00_SYSTEM/BOOKBRAIN_ROUTER_v4.md`: scoped retrieval; avoid indiscriminate BookBrain loading.
3. `/BookBrain/10_COMPUTING/05_UI_UX/Kyle_UI_System.md`: reuse existing site, narrow-first, progressive disclosure, avoid needless components, visible states, minimal external traffic.
4. `/BookBrain/10_COMPUTING/05_UI_UX/quality-gates.md`: 44px touch control, focus visibility, mobile width, explicit image dimensions, truthful test status.
5. `/BookBrain/10_COMPUTING/05_UI_UX/tokens.json`: shared UI tokens checked; existing LLS muted green treated as deliberate project-level brand style, not overwritten.
6. `/BookBrain/10_COMPUTING/05_UI_UX/agent-rules.md`: small, inspectable changes, existing framework.
7. `/BookBrain/50_DESIGN/03_DIGITAL_PRODUCT_DESIGN/11_MARKETING_CONVERSION/00_SOURCE_REGISTER.md`: relevant source routes for photography, credibility, conversion and FTC truthfulness; no fabricated job evidence.
8. `/BookBrain/50_DESIGN/03_DIGITAL_PRODUCT_DESIGN/09_BRAND_PRESENTATION/00_SOURCE_REGISTER.md`: brand consistency and restrained photography.
9. `/BookBrain/50_DESIGN/01_GRAPHIC_DESIGN/Graphic_Design_Print_Production_Fundamentals_FULL_SOURCE.md`: confirmed captured graphic-design authority and licensing, not a license to use others' photos.
10. `/SecondBrain/04_BUSINESS/BRAND_AND_POSITIONING.md`: project brand-specific override, dark premium practical style.
11. Live MDN `details` reference: https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/details — closed by default, click/keyboard toggles natively.

## Chosen implementation
- Native `<details><summary>` per photograph in its existing work card, closed by default.
- CSS swaps Show Photo and Hide Photo labels through the `[open]` state.
- 44px minimum hit target, explicit focus outline, responsive 16:9 media, accurate alt and caption, lazy loading and explicit image dimensions.
- No JavaScript, third-party image hosts, or placeholder image URLs required.
- The actual `<details>` control appears only after a genuine photo is selected and Kyle explicitly approves it.
- Every non-approved card remains text-only; no misleading Show Photo button.

## Actions, results, verification
- Read existing `index.html` from GitHub `kylelloyd63-star/lloyds-local-services`; six existing Recent Work cards were present with no photo elements.
- Targeted Dropbox search for genuine Ring, printer, island job photos returned no clearly identified usable approved job images.
- Attempted to update `index.html` on the default branch using repository file-update action. **BLOCKED by tool safety checks**; no claim of successful page edit.
- Created `PHOTO_PUBLISHING_POLICY.md` in site repo; commit `cb44688ead561861916b59e19984b45d8f611258`.
- Created `photo-disclosure.css` in site repo; commit `e50d78d983f5ade8e3ac2beae1f358acbc7b0fdd`.
- Static checks before CSS commit: no third-party URLs, visible focus, 44px minimum control, Show/Hide selectors, no JS, existing brand color variables — all passed.
- **Not yet wired**: standalone CSS has not been loaded by `index.html`; no approved image blocks exist yet.
- No live deployed photo button, no job photos, no image approval and no physical browser test claimed.
- No changes to contact form, links, business copy, or existing six project cards.
- A standalone site-specific record is saved in this GitHub repo. The proposed centralized BookBrain `/BookBrain/00_SYSTEM/USAGE_LOG.md` was absent on folder inspection, and is NOT claimed as saved.

## Remaining gate
1. Integrate `photo-disclosure.css` into `index.html` once repo editing is unblocked (or use equivalent inline CSS).
2. Have Kyle approve the exact original, cropped preview and caption for each proposed job photo.
3. Publish only individually approved assets and markup; test actual browser + mobile.
4. Verify deployed source and image links, and file the usage record into the authorized centralized log when the appropriate Dropbox write path is available.

No site redesign or extra sales/SEO changes were authorized or performed in this narrow task.


---

## 2026-10-08 — LLS Facebook Share Card, Favicon and Branding Plan

**Trigger:** Kyle reported the Facebook/Messenger link preview lacked a good image and the site still lacked a favicon. He instructed: "plan with bookbrain" and "record use." **Work scope:** research, site/source audit, implementation plan, usage recording only; no image approved, no new branding deployed.

### Factual audit
- Source: `kylelloyd63-star/lloyds-local-services` default-branch `index.html`, original blob SHA `e45fe537d9f85b06805d02e644f8c2302b4c338e`, confirmed during this planning pass.
- Current HTML head includes title, description, canonical domain `https://lloydslocalservices.com/` but no `og:title`, `og:type`, `og:description`, `og:image`, `og:url`, `twitter:card`, `rel="icon"` or `rel="apple-touch-icon"`.
- The HTML contains no `<img>` references. CNAME = `lloydslocalservices.com`.
- Dropbox reference asset located: `/SecondBrain/03_PROJECTS/Lloyds_Local_Services/WEBSITE_HOME_APPROVED_DIRECTION_2026-09-14.png` (1,496,151 bytes). Found and preview link verified; its design details were not independently reviewed from image pixels. It is a brand direction/reference, NOT cleared as an OG image without examination.
- Public homepage and favicon URL were inaccessible from the available web reader, so no production HTTP status or social scraper output is claimed.

### BookBrain retrieval and influence
1. `/BookBrain/00_SYSTEM/00_BOOKBRAIN_MAP.md` — Dropbox `/BookBrain` is canonical and mutations require Kyle's explicit approval; user explicitly approved recording use.
2. `/BookBrain/10_COMPUTING/05_UI_UX/Kyle_UI_System.md` — preserve existing LLS visual design, reuse assets, no gratuitous redesign, inspectable result required.
3. `/BookBrain/10_COMPUTING/05_UI_UX/quality-gates.md` — responsive previews, testability, image dimensions, meaningful color/contrast, privacy and no unnecessary external fetches.
4. `/BookBrain/50_DESIGN/03_DIGITAL_PRODUCT_DESIGN/09_BRAND_PRESENTATION/00_SOURCE_REGISTER.md` — existing brand identity/consistent images; no opportunistic random branding.
5. `/BookBrain/50_DESIGN/03_DIGITAL_PRODUCT_DESIGN/11_MARKETING_CONVERSION/00_SOURCE_REGISTER.md` — source routing for credible images, conversion, and FTC truthfulness.
6. `/SecondBrain/04_BUSINESS/BRAND_AND_POSITIONING.md` — dark metallic, premium but rugged, green, restrained, practical; project-specific design context.
7. `/SecondBrain/03_PROJECTS/Lloyds_Local_Services/WEBSITE_HOME_APPROVED_DIRECTION_2026-09-14.png` — identified historical approved-direction image for subsequent visual review, NOT yet approved to publish.
8. External LIVE-AUTHORITATIVE: `https://ogp.me/` — Open Graph four required properties and image structured metadata.
9. External LIVE-AUTHORITATIVE: `https://developers.google.com/search/docs/appearance/favicon-in-search` — favicon link, crawlability, square and larger than 48px recommendation (2026-08-28).
10. External LIVE-AUTHORITATIVE: `https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/link` — icon and mobile touch icon syntax.
11. Facebook Sharing Debugger: `https://developers.facebook.com/tools/debug/` — suggested post-deployment inspection; direct fetch returned HTTP 429 in this session, so not tested.

### Chosen implementation (awaiting visual approval)
- Make **one restrained brand system**, not unrelated banners, logo and icon. Preserve original LLS muted charcoal + green palette from `index.html`; use an established LL monogram (simplified to remain readable at 16px).
- **OG share card:** 1200x630, sRGB JPG/PNG, high contrast. Large “Lloyd's Local Services” with concise real positioning “Tech headaches and home projects — handled.” and short locality line “Newmarket, NH · Seacoast NH & Southern Maine”; do not crowd with tiny icons or fake job photos.
- **Favicon:** square LL design derived from same master. Generate `favicon.ico` with 16/32/48px sizes, `favicon-48.png` or `favicon-96.png`, `apple-touch-icon.png` at 180px. Optional `icon-512.png` as reusable master export.
- **Static hosting:** keep assets in site's own repository, e.g. `assets/brand/lls-social-card.jpg`; no remote image hotlinks, no heavy frameworks.
- **Head tags after approval and assets verified:** `og:type=website`, `og:url=https://lloydslocalservices.com/`, `og:title`, concise `og:description`, full HTTPS `og:image` with width/height/type/alt, `og:site_name`, Twitter summary_large_image equivalent; favicon and apple-touch-icon links. Preserve existing canonical/title/form.
- **Quality gates before launch:** preview visually at full/thumbnail scale (esp. LL mark at 16px); inspect exact files, logo spelling, dimensions and file type, contrast, rights/provenance; verify URL serves images at HTTP 200 and appropriate MIME types; verify deployment's HTML actually contains tags, mobile favicon, Facebook Sharing Debugger rescrape, Messenger preview; document observed vs inferred, cache delay.
- **Keep separate:** customer job photos remain private until each actual photo/crop/caption is approved; adding an OG brand card is not approval for any job photographs.
- **No extra redesign** and no premature promises about Facebook crawler or Google display.

### Current result / remaining work
- Diagnosis from repository **confirmed**: missing metadata/icons.
- Brand direction and asset package **planned**, not created, approved, uploaded, or deployed.
- Latest public Facebook appearance **not directly verified**; content caching may delay changes even after deploy.
- Save record: this GitHub repository log is durable within the LLS project, but does **not** establish a Dropbox `/BookBrain/00_SYSTEM/USAGE_LOG.md` write. Dropbox centralized usage log status remains unverified/not written in this pass.
