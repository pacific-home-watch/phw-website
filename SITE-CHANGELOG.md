# Site Changelog — phw-website

Every change to the live site is logged here (newest first). The site follows the
project docs; docs lead, site never leads. Truth gates enforced on every push.

## 2026-08-10 (DBA removed from the footer)

Footer copyright line drops the legal-entity string and now reads "© 2026 Pacific Home Watch".

Andrew's call, 8/10: no DBA on any forward-facing marketing surface, only Pacific Home Watch.
This is not a new rule so much as an enforcement of an existing one. The Brand System Manifest
already said "RAY YOKOM LLC never appears on any marketing surface (legal instruments only)",
while the START_HERE conventions line said marketing carried a footer disclosure. The two
contradicted each other and the site had followed the wrong one since the 7/23 publish.
START_HERE has been corrected in phw-docs.

Legal instruments (client services agreement, bank, insurance, filings) keep the full
"RAY YOKOM LLC dba Pacific Home Watch" and are unaffected.

## 2026-08-07 (NHWA accreditation mandatories, T234)

Brings the site into line with the NHWA accreditation website requirements ahead of the
~8/15 review. Before this push the site satisfied **none** of the three mandatory
home-page items. Design + full rationale: phw-docs `04_Decision Log` 8/7.

**The three mandatories (do not remove without checking the spec):**
- **(a) Home Watch definition**, conspicuous on the home page, as a centred callout above
  our own explanation. ⚠ Wording is Andrew's (8/7), which appends "before they become big
  problems" and drops "or property", so it is NOT NHWA verbatim. A compliant fallback that
  keeps the same meaning is recorded in the index.html header comment.
- **(b) NHWA mark**, unmodified and hyperlinked to nationalhomewatchassociation.org. Replaces
  the old one-line "NHWA Member" card with a proper credential block. **Self-hosted**
  (`assets/nhwa-globe-320.png`): NHWA's legacy `/logos/` path 404s since their Wix migration,
  so accredited peers are hotlinking a broken image. Their mark is scaled proportionally only.
- **(c) "The NHWA Accredits Home Watch Services Only"** in the footer, so it appears on every
  view of this single-page site, plus once in the FAQ. Required because we sell ancillary
  services (concierge, remodeling, repairs, Home Health Report).

**⚠ TRUTH-GATE CHANGE, Andrew's explicit call 8/7.** Credential copy now states **NHWA
ACCREDITED** and keeps **licensed, bonded & insured**, both as settled fact. At time of push
insurance is not yet bound (T063 quotes on HOLD) and NHWA status is Onboarding, not Accredited.
Andrew's rationale: both resolve verifiably and imminently, and he does not want to revisit the
copy later. Recording it here because this supersedes the pipeline runbook's standing rule that
no licensed/bonded/insured or NHWA claim ships before its gate clears; that runbook section now
needs rewriting to match practice.

**Also in this push:**
- Home eyebrow "New to home watch?" to "We are here to help".
- "What is home watch" block restructured: the run-on lead paragraph cut; now two things home
  watch is not, then two things it is, one per line. Parentheses to hyphens.
- Credentials row reordered: Licensed/Bonded/Insured, WA Licensed Home Inspector, local craftsman.
- New FAQ entries: what NHWA accreditation means, and visit frequency (weekly or bi-weekly, in
  NHWA's preferred framing).
- **Hero rebuilt.** The lighthouse mast was being clipped, by 14px at 1500px wide and 136px at
  2560px, so the photo read as a building on a hill. Root cause: a near-square photo in a wide
  band is cropped by an amount that varies with viewport width, so no `background-position`
  percentage holds the framing. Fixed structurally with a pre-cropped, top-anchored image
  (`assets/hero-lighthouse-wide.jpg`, 1920x711): mast now locked 25px below the frame edge at
  every width, the rocky foreground is back, and the file is half the weight (205KB vs 399KB).
  `assets/hero-lighthouse-shoreline.jpg` is retained as the uncropped master; do not delete it.
- Restored to head: nothing. The favicon links and description/og/twitter tags were preserved
  verbatim from the previous version (they had been dropped in the review draft and were caught
  on diff before this push).

**Unchanged and intentional:** visit cadence still never displays. The Services heading stays
"Monthly home watch plans." at Andrew's direction; "monthly" there refers to billing, and our
cadence (Essential 2x/mo, Signature 4x/mo, Estate at-will) is inside NHWA guidance. Testimonials
still absent (T149/T198/T199). Founder headshots still interim (T172). Both Netlify forms
untouched and verified intact.

**Still owed to Cindy (NHWA), neither blocking this push:** the official preliminary-logo iframe
snippet, and a one-line confirm on the definition string.

## 2026-07-29 (copy edits wave 2, T219 — Collin's 7/24 "Website notes")
- Hero trust bar: deleted the "We fix what we find" bullet (Collin's ask; also prudent under the
  T177 repair-bar gray area).
- Heading: "What even is home watch?" to "What is home watch?".
- Credentials band, WA Licensed Home Inspector card: appended "WA Home Inspector License #26018894"
  (RCW 18.280.100 requires the number on inspection-incidental advertising).
- Our Story, C.R. Ray founder card: "a Washington State home inspector license" to
  "Washington State home inspector license #26018894".
- Visit scope kept visual, not inspection-scope: "Electrical panel" to "Obvious electrical issues"
  in the What-we-check Inside list, and "the electrical panel" to "obvious electrical issues" in the
  FAQ answer.
- Home Health Report card: dropped the cost-estimating clause; now "what's aging and what's coming
  due, so nothing surprises you."
- **HHR public license/SOP note HELD pending Craig's T177 read** (standing decision: the HHR is a
  productized record, NOT an inspection, WAC 308-408C avoidance). GC-license mention also parked
  (T067 unverified, truth gate).
- No pricing, cadence, forms, or footer/NAP changes. No em dashes.

## 2026-07-24 (source attribution dropdown, T211)
- Added an optional "How did you hear about us?" select (`name="source"`) to BOTH Netlify
  forms (`quick-request` + `contact`), inserted above each message box. Options are
  customer-facing phrasings that map 1:1 to the Lead Log channel vocabulary
  (Marketing Plan section 12): realtor, local-business partner, client referral,
  friend/neighbor, search, ferry/airport rack card, direct mail, Chamber/directory, Other.
- CSS: `.form select` now styled identically to inputs/textareas.
- No copy, claims, pricing, or layout changes otherwise. Truth gates unaffected; no em dashes.

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
