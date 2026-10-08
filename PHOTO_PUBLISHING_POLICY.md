# LLS Completed-Job Photo Publishing Rule

Status: implementation specification, not approval to publish any photo.
Date: 2026-10-08.

## Owner decision
- Completed-job photographs are hidden by default.
- A card gets **Show Photo** only after Kyle explicitly approves the actual photograph, crop, alt text and caption.
- The opened control reads **Hide Photo**.
- A card with no approved asset stays text-only, without a dead or misleading button.
- Do not use stock, illustrative, generated, or customer-identifying images as evidence of completed work.
- Do not modify existing service copy, cards or design merely to add photo capability.

## Implementation
Use native HTML `<details>` / `<summary>` with no `open` attribute, and no custom JavaScript. For a specifically approved asset add inside that job's existing `<article class="work-card">`, after its existing description:

```html
<details class="work-photo">
  <summary>
    <span class="photo-show-label">Show Photo</span>
    <span class="photo-hide-label">Hide Photo</span>
  </summary>
  <figure>
    <img src="assets/approved-jobs/APPROVED-NAME.webp"
         alt="SPECIFIC ACCURATE DESCRIPTION"
         width="1200" height="675"
         loading="lazy" decoding="async">
    <figcaption>OWNER-APPROVED FACTUAL CAPTION</figcaption>
  </figure>
</details>
```

Do not add the snippet until the pictured job and rights/approval have been verified. Example file names are not actual files.

## Image production
- Use genuine completed-job originals only; retain originals unmodified and private.
- Confirm the photo proves the completed work; inspect focus, lighting and subject before selecting.
- Obtain relevant customer permission; remove visible names, addresses, screens, documents, faces, license plates, identifiable interiors and GPS/EXIF information as appropriate.
- Prepare a web-size WebP or JPEG with visually checked framing; 16:9 preferred, not required if cropping conceals meaningful details.
- Self-host under the repository's `assets/approved-jobs/` directory. No third-party image hotlinks.
- Verify that the exact asset URL loads over HTTPS after publication.
- Do not interpret hidden-by-default as private; a published image remains publicly retrievable.

## Acceptance checks
1. Default load shows text-only cards, no disclosed photographs.
2. Unapproved cards have no Show Photo control and no image element.
3. Approved card has closed details by default; click/Space/Enter toggles and closed label becomes Hide Photo while open.
4. Tab and focus indicators work; no hover required.
5. Image stays within card on 360px mobile; no horizontal scrolling.
6. Captions and alt text accurately describe the picture; no private identifying data.
7. All existing six job descriptions, form fields, link targets, branding, and navigation remain unchanged.
8. After deployment, test actual desktop/mobile browser and image availability. Source-only review is not a live test.

## BookBrain consulted for this decision
- `/BookBrain/00_SYSTEM/BOOKBRAIN_ROUTER_v4.md` — scoped research and anti-dilution.
- `/BookBrain/10_COMPUTING/05_UI_UX/Kyle_UI_System.md` — reuse, progressive disclosure, accessibility and no unnecessary external requests.
- `/BookBrain/10_COMPUTING/05_UI_UX/quality-gates.md` — visible focus, 44px controls, responsive quality, dimensions and privacy.
- `/BookBrain/10_COMPUTING/05_UI_UX/agent-rules.md` — preserve project patterns, apply minimal changes.
- `/BookBrain/50_DESIGN/03_DIGITAL_PRODUCT_DESIGN/11_MARKETING_CONVERSION/00_SOURCE_REGISTER.md` — truthful visual proof/marketing source routing.
- `/BookBrain/00_SYSTEM/00_BOOKBRAIN_MAP.md` — canonical Dropbox archive and approval gate.
- Current MDN HTML details reference: https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/details

No photograph is approved by this file.