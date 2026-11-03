# Deployment and launch checklist

## 1. Publish the catalogue
In this repository, open **Settings → Pages**.
- Build and deployment: **Deploy from a branch**
- Branch: **main**
- Folder: **/(root)**
- Save

After GitHub Pages publishes, check:
https://ckp231326.github.io/courtprep-odisha/

## 2. Current status
The website is a public catalogue and email enquiry page. It is not a live checkout. It does not collect customer payment details, process UPI payments, or grant Drive access.

## 3. Proposed prices
The prices in products.json are recommendations only and are marked as subject to confirmation. Confirm the price list before advertising these amounts as final.

## 4. Keep private
Never add PDFs, Drive file IDs, QR images, UPI credentials, Apps Script secrets, admin tokens, customer lists, payment references or order data to this public repository.

## 5. Before live checkout
Complete and test a private Google Apps Script backend with server-side price validation, customer email verification, manual bank-credit verification, duplicate UTR protection, secure admin authentication, Drive permission grants, email delivery, error handling and audit logs. Add privacy, sale terms, refund/cancellation policy and support details.
