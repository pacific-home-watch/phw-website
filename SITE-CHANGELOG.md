# Site Changelog — phw-website

Every change to the live site is logged here (newest first). The site follows the
project docs; docs lead, site never leads. Truth gates enforced on every push.

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
