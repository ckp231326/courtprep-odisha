# COURTPREP ODISHA

Public-facing catalogue for digital study materials for Odisha District Court recruitment examinations.

## Current phase
This repository contains the public catalogue and enquiry interface only. It does **not** process payments or grant Google Drive access yet. Do not tell customers that online checkout is active until the Google Apps Script backend, customer email verification, payment approval and Drive delivery have been deployed and tested.

## Privacy boundary
Never commit:
- Master PDF files or public Drive links
- Google Drive file IDs
- UPI QR images or payment credentials
- UPI PINs, OTPs, passwords, API keys or admin tokens
- Customer names, emails, phone numbers, UTRs or order records

The repository is public. Keep all backend configuration and customer data in the private Google account/backend.

## Files
- `index.html`: responsive catalogue and email enquiry basket
- `products.json`: public product descriptions and proposed prices

## Publish with GitHub Pages
1. Open repository **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select branch **main** and folder **/(root)**, then Save.
4. Wait for GitHub Pages to publish the site. The URL will normally be:
   `https://ckp231326.github.io/courtprep-odisha/`

## Next technical phase
Connect the catalogue to a secured Google Apps Script web app. Implement:
- Customer email verification before granting Drive access
- Server-side price and product validation
- Manual bank/UPI transaction verification
- Idempotent approval and fulfilment
- Drive viewer permissions and email notifications
- Admin authentication, audit log, retries and backups

Before accepting orders, add and review privacy, terms of sale, refund/cancellation and contact information.
