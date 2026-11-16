# Amana — Public Information Pages

A static companion website for the Amana mobile application, providing privacy information, contact and account-deletion request pages, and authentication handoff pages.

## Scope and stack

HTML, CSS and browser JavaScript. This repository is separate from the mobile application: Flutter, PostGIS and the mobile backend are not implemented here.

| File | Purpose |
| --- | --- |
| [`index.html`](index.html) | Navigation to information pages |
| [`privacy.html`](privacy.html) | Published privacy information |
| [`contact.html`](contact.html) | Personal-data contact form |
| [`account-deletion.html`](account-deletion.html) | Account-deletion request form |
| [`auth-confirmed.html`](auth-confirmed.html) | Confirmation landing page |
| [`auth/callback/index.html`](auth/callback/index.html) | Handoff to the application's custom URL scheme |
| [`styles.css`](styles.css) | Shared styles |
| [`CNAME`](CNAME) | Custom-domain configuration |

## Request flow

Contact and deletion forms use browser `fetch` to submit requests to an external Supabase Edge Function. That function is not included here. The pages provide submission feedback; delivery, backend processing and account deletion were not verified during review.

Authentication handoff relies on the separate mobile application and identity configuration.

## Verification and limitations

No dependency manifest, build pipeline or automated test suite was found. No form submissions were performed. Existing site copy is French; this English technical overview does not change published privacy text or application behavior.

This repository demonstrates a static web integration and public support surface. It does not represent the full mobile application or establish legal compliance.
