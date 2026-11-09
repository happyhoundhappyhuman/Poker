# PokerIQ V4 – Texas Hold’em Study App

An Android-installable Progressive Web App (PWA) for practice, post-hand review and poker study. It is not a native APK.

## Install on Android / host on GitHub Pages
1. Extract the ZIP and upload the four files in this folder to a GitHub repository.
2. In GitHub, open **Settings → Pages**, select the branch and root folder, then save.
3. Open the published HTTPS address in Chrome on Android.
4. Use Chrome’s menu → **Install app** / **Add to Home screen**.

## V4 features
- Manual 52-card picker for two hole cards and five community cards.
- Monte Carlo equity simulation against 1–8 opponents.
- Opponent presets: random, loose, standard and tight (heuristic approximations).
- Pot odds and simplified call expected-value estimate.
- Player position selector, included in saved hand notes.
- Board texture summary: paired/unpaired, suit texture, connectivity and high-card density.
- Next-card straight/flush completion counts from the flop or turn. These are raw completion cards, not guaranteed winning outs.
- Guided table-photo scanner: crop one card at a time, OCR rank suggestion, confirm suit and destination. Manual rank entry remains available if OCR is unavailable.
- Local hand history and CSV export.
- Offline app shell via service worker; OCR library is loaded from a CDN and needs internet.

## Important limitations
- The scanner is guided crop-and-confirm, not automatic recognition of every card in a table.
- This app does not monitor live play, connect to poker rooms or automate decisions. Use it for study and post-hand review, and follow the rules of any poker platform.
- Opponent range presets are simplified teaching heuristics, not statistically calibrated player models.
- Straight/flush counts indicate cards that complete those hand categories on the next street; they do not account for opponent cards, redraws, counterfeit cards or whether the improvement wins.
- Equity is a Monte Carlo estimate and varies between runs. Betting actions, folds, rake and future betting are not modelled.
- Data is stored in the browser on the device. Clearing site data can erase saved hands.

## Technical
All poker calculations run locally in the browser. OCR uses Tesseract.js from jsDelivr when internet access is available. The app is a PWA; creating a signed Android APK would require a separate Android packaging/build step.
