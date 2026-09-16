# SmartPay — Nigerian payment app prototype

A working, installable prototype of a UPI-style Nigerian payment app: NIP transfers with account-name resolution, NQR scan-to-pay, bills and airtime, and an offline USSD fallback for when data drops mid-transfer.

**Live preview:** https://<your-username>.github.io/smartpay-ng/

Open it on a phone and choose *Add to Home screen* (Chrome) or Share → *Add to Home Screen* (Safari). It installs with its own icon, launches full screen and works with no network.

## Flows you can walk through

- Onboarding — phone entry with live carrier detection, OTP that auto-reads and self-verifies
- Home — balance, NIP virtual account with one-tap copy, live network state
- Scan — camera opens immediately, NQR detection, torch, My-code
- Send — contacts or 10-digit NUBAN with bank name resolution, amount keypad with balance guard, review, slide-to-send, PIN or fingerprint
- Offline USSD — tap the network pill on the home screen to cycle 4G → weak → no data, then send money. The transfer is intercepted and converted into a pre-filled USSD string.
- History — pending, completed and reversed states with shareable receipts
- Account — security, notifications, cards and banks, help

## Publish it

1. Create a public repo named `smartpay-ng` at https://github.com/new — no README, no .gitignore.
2. Push this folder, including the hidden `.nojekyll` and `.github/`:

```bash
git init -b main
git add -A
git commit -m "SmartPay prototype"
git remote add origin https://github.com/<your-username>/smartpay-ng.git
git push -u origin main
```

3. **Settings → Pages → Source: GitHub Actions**. The link appears under **Actions** in about a minute and redeploys on every push.

## Build a native APK or IPA

This same `index.html` is the web bundle in the Capacitor build kit. Drop it into `www/` there and run `npm run apk:debug`.
