# PokerIQ – Android-ready first version

A responsive, installable Progressive Web App for Texas Hold'em study and post-hand review.

## Run it
1. Extract the ZIP.
2. Host the folder on an HTTPS static host (GitHub Pages works).
3. Open the published URL in Chrome on Android.
4. Chrome menu → **Install app** / **Add to Home screen**.

For local testing, serve the folder from a local web server; service workers require HTTPS or localhost.

## Included
- Manual 52-card picker for two hole cards and up to five board cards.
- Monte Carlo equity simulation against 1–8 random opponents.
- Win / tie / loss and split-pot equity estimates.
- Optional pot-odds threshold and simplified call EV.
- Local hand history, CSV export.
- Camera/file-picker capture for table photos or screenshots, with manual card entry.

## Current limitations
- This is a study tool, not a live poker-site assistant.
- Photo-assisted rank OCR is included for one card per photo. Suit confirmation and visual verification remain manual; full-table multi-card recognition and continuous live monitoring are not implemented.
- Opponents are modelled as random hands; player ranges, betting actions, folds, rake and future betting are not modelled.
- Equity is a Monte Carlo estimate, so results vary slightly with each run.

All calculations happen in the browser. OCR uses Tesseract.js from a CDN and therefore requires internet access; hand history is stored locally on the device.
