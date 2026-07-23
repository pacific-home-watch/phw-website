# Site Changelog — phw-website

Every change to the live site is logged here (newest first). The site follows the
project docs; docs lead, site never leads. Truth gates enforced on every push.

## 2026-07-23 (Phase B: GO-LIVE)
- **Published.** Removed the `noindex,nofollow` meta and the demo ribbon; site is now public.
- Removed the three testimonial placeholders (real ones pending, T149/T198/T199); section
  restored when they land.
- Footer: added the canonical NAP phone (360) 207-4529 and the DBA disclosure
  "RAY YOKOM LLC dba Pacific Home Watch"; dropped the "preview mockup" line; added get@ address.
- Social tags (og:image, og:url) repointed from the netlify.app URL to https://pacifichomewatch.com.
- Claims basis at go-live: insurance/E&O confirmed **bound** (Andrew, 7/23), so
  "Licensed, bonded & insured" stays; NHWA wording is "member" only (no accreditation claim
  before the ~8/15 review). Pricing, forms untouched. Cadence never displayed; no em dashes.
- Gate note: Margie was notified via **Collin's solo email** (not the both-partners call the
  T192 gate specified); Andrew's decision was to proceed on that basis.
- Next: point pacifichomewatch.com DNS at Netlify (guided), then post-publish verification
  (contact-form test to get@, robots, og preview).

## 2026-07-23 (Phase A: photos + favicon/social, private)
- **Photos slotted into the live source** per the Photo Slot Map (no publish; site stays
  noindex + demo ribbon on the un-pointed netlify.app URL).
  - Homepage hero: replaced the CSS gradient with an on-island photo under a green tint
    overlay (white headline/CTAs stay legible). Hero chosen via in-session bake-off:
    **Cattle Point Lighthouse shoreline** (Andrew's pick over the sunset-beach-cove
    candidate, which was not shipped).
  - How It Works: added a "Local & rooted" ferry-crossing band (dark overlay, white caption).
  - Homepage CTA band ("Leaving the island?"): marina-sunset photo behind the existing
    dark band.
  - Our Story founder cards: real photos in. Collin card uses the interim casual headshot
    (real shot still owed, T172); Andrew card uses his 7/23 headshot.
- **Name fix (7/12 convention):** every public "Collin Ray" / "Collin" reference is now
  "C.R. Ray" (founder card heading + the "local craftsman" copy).
- **Favicon + social preview:** added SVG + 512px PNG icons, page title, og:title/description/
  image + twitter:card. og:image is the active hero at the absolute netlify.app URL (swaps to
  pacifichomewatch.com at go-live).
- **Assets:** optimized derivatives under `assets/` (heroes 1920w ≤400KB, bands 1600w,
  founders 800×800, favicons).
- **Voice:** all visible copy is em-dash-free (grep clean).
- **Untouched (Phase B gates):** pricing, forms, `noindex`, demo ribbon, and every
  licensed/bonded/insured + NHWA + testimonial-placeholder claim stay exactly as-is until
  the launch gate check (T192 Margie call, insurance bound, real testimonials).

## 2026-07-18
- **Initial pipeline commit.** Renamed the repo seed to `index.html` so Netlify serves it.
- Wired both contact forms for **Netlify Forms**:
  - CTA-band form → name `quick-request`
  - Contact-page form → name `contact`
  - Added `method="POST"`, `data-netlify="true"`, hidden `form-name` field, and a
    hidden `bot-field` honeypot to each; gave every input a `name` so submissions
    actually capture data; removed the `onsubmit="return false"` that had blocked sending.
- Unchanged and intentional: `noindex,nofollow` and the demo state stay until launch.
  Cadence never displayed. No licensed/bonded/insured, NHWA, or testimonial claims
  beyond what the seed already carried (gates: T115 insurance, accreditation, T149).

## 2026-07-18 (later)
- Enabled Netlify form detection on the phw-site project; this deploy re-parses the
  HTML so the `contact` and `quick-request` forms register in the Netlify dashboard.
