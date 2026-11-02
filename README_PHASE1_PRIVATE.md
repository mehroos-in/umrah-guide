# Umrah Guide — Phase 1 Private Preview

## Phase 1 scope
- Private preview only; do not enable public indexing.
- Priority languages: Hindi, Urdu and Malayalam.
- English and Arabic remain available as reference languages.
- Step-by-step guide, duas, transliteration/meanings and print-to-PDF support.
- Urdu right-to-left layout.
- Translation drafts are not yet independently proofread or scholar-approved.

## Deploy to Cloudflare Workers Static Assets
Prerequisites: Node.js and npm installed; a Cloudflare account.

1. In Cloudflare Zero Trust, create an Access application for the intended Workers hostname and add an Allow policy limited to the approved email addresses. Do this before making the deployment reachable.
2. From this folder, run:
   ```bash
   npx wrangler login
   npx wrangler deploy
   ```
3. In Cloudflare, confirm the Access application protects the exact `*.workers.dev` hostname created by the deployment. Test in a private/incognito browser: an approved email should pass; an unapproved email should be denied.
4. Do not share the URL as public access. Access control is the privacy boundary; an unlisted URL alone is not private.

## Important
- This package is deployment-ready, not deployed. No Cloudflare login or deployment was performed by preparing this archive.
- Keep the GitHub source repository private if you create one; do not enable GitHub Pages.
- Before any public launch, update canonical/SEO metadata, robots.txt and sitemap, then arrange independent native-speaker proofreading for Hindi, Urdu and Malayalam and qualified Islamic review of ritual content, Arabic text and references.
- Do not describe translations as fully verified or scholar-approved until those reviews are completed.
