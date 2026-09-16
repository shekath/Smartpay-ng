# SmartPay NG — redesigned payment app prototype

A working prototype of a Nigerian UPI-style payment app (NIP transfers, NQR scan-to-pay, offline USSD fallback), rebuilt against Nielsen's ten usability heuristics.

**Live preview:** https://<your-username>.github.io/smartpay-ng/

Open it on a phone and use *Add to Home screen* — it installs with its own icon, runs full screen and works offline.

## Publish this yourself

1. Create a new **public** repo named `smartpay-ng` at https://github.com/new (don't add a README — this folder already has one).
2. Upload every file in this folder, including the hidden `.nojekyll` and `.github/` folder. Either drag them into the web uploader, or:

```bash
git init -b main
git add -A
git commit -m "SmartPay NG prototype"
git remote add origin https://github.com/<your-username>/smartpay-ng.git
git push -u origin main
```

3. In the repo: **Settings → Pages → Source: GitHub Actions**.
4. The included workflow deploys on every push. The link appears under **Actions** in about a minute.

## What's in the prototype

Onboarding with live carrier detection · home with NIP virtual account and network state · scan-to-pay with NQR · send with account-name resolution · amount keypad with balance guard · slide-to-send and PIN · offline USSD fallback (toggle *Simulate weak network* in the audit panel) · history with pending and reversed states · account, security, notifications, cards, bills and help.

The left-hand panel documents the heuristic evaluation: what each of the ten heuristics flagged in the original screens, and what the redesign does instead. To hide it for a client demo, delete the `<aside class="audit">` element and the `#audit-toggle` button in `index.html`.
