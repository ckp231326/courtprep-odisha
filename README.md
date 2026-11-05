# COURTPREP ODISHA

Public catalogue for independent digital study materials for Odisha District Court recruitment examination aspirants.

## Live service

- Public website: https://ckp231326.github.io/courtprep-odisha/
- The public website uses the Apps Script read-only catalogue endpoint to display active products, prices and packages from the private Google Sheet. If that endpoint is unavailable, it falls back to `products.json`.
- Checkout is handled by a Google Apps Script web app. It supports Gmail OTP verification, UPI payment-reference submission, manual bank-credit approval and Google Drive viewer-access delivery.
- Paid order delivery is not automatic on UPI submission. An administrator must verify actual payment credit before approving the order.
- Products with a price of zero are free resources. Gmail verification is required; after verification, the app attempts to grant Drive viewer access without a UPI step.

## Catalogue maintenance

The private Google Sheet is the source of truth for live catalogue information.

- Add or edit individual resources in the `PRODUCTS` sheet.
- Add or edit bundles in the `PACKAGES` sheet.
- The public site and checkout read the active rows from that sheet after the latest Apps Script version is deployed.
- `products.json` is retained as a static fallback if the live catalogue endpoint is unavailable.

The optional `COVER_URL` and `SAMPLE_URL` fields can be added to the PRODUCTS sheet to display a cover image and a sample-page link. Existing required columns remain unchanged.

## Product details on the public catalogue

Each product card includes an expandable **View book details** section. The live catalogue reads these optional public fields from the private Google Sheet's `PRODUCTS` tab:

- `CONTENTS` — topic or chapter coverage, with items separated by the pipe character (`|`)
- `FEATURES` — study features and included resources, separated by `|`
- `LANGUAGE` — language used in the book
- `SUITABLE_FOR` — intended learner or preparation need

These are columns K:N, following the existing `COVER_URL` and `SAMPLE_URL` columns I:J. The Apps Script catalogue endpoint exposes only these public product details; it does not expose Drive IDs, orders or customer data.

## Editable homepage content

The public homepage introduction, ordering notice, three benefit cards, complete-collection highlight, About text and closing message are designed to be edited through the private Google Sheet `SETTINGS` tab.

After installing the homepage-settings version of `Code.gs`, append the supplied `HOME_*` key/value rows to `SETTINGS`. To change homepage wording later, edit only the `VALUE` cell beside the relevant `HOME_*` key. Keep the key unchanged. The public catalogue endpoint exposes only the explicitly whitelisted homepage fields; other operational settings remain private. Ordinary copy changes do not require an Apps Script redeployment.

## Privacy and security boundary

Never commit:
- Master PDF files or private Google Drive links
- Google Drive file IDs
- UPI QR images or private payment credentials
- UPI PINs, OTPs, passwords, API keys or admin tokens
- Customer names, emails, phone numbers, UTRs or order records

The repository is public. Only public catalogue data and public cover/sample assets belong here. Keep backend configuration and customer data in the private Google account/backend.

## Website deployment

GitHub Pages publishes the `main` branch from the repository root. The public site URL is:
https://ckp231326.github.io/courtprep-odisha/

## Policies

Before broad public promotion, publish accurate privacy, terms of sale and refund/cancellation policies. Do not promise that screenshotting or photographing a screen can be prevented; Google Drive viewer restrictions are limited to supported download, print and copy controls.
