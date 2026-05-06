# Pip vs 10 Towers Website

Static App Store support, privacy, and terms site.

## Pages

- `index.html`: public landing page linking to support and privacy.
- `support.html`: use as the App Store Connect Support URL.
- `privacy.html`: use as the App Store Connect Privacy Policy URL.
- `terms.html`: use as the App Store Connect EULA or Terms of Use URL.

## Before App Store submission

1. Deploy this `Website` folder to a public HTTPS host.
2. Confirm `pondd.me@gmail.com` is monitored for support, privacy, and App Store review follow-up.
3. Use the deployed URLs in App Store Connect:
   - Support URL: `https://YOUR-DOMAIN/support.html`
   - Privacy Policy URL: `https://YOUR-DOMAIN/privacy.html`
   - Terms/EULA URL: `https://YOUR-DOMAIN/terms.html`
4. Confirm the privacy policy and terms still match the final binary. The current site assumes:
   - no account creation
   - no ads
   - one optional non-consumable StoreKit Full Adventure unlock
   - local progress/settings storage
   - Firebase Analytics
   - Firebase Crashlytics
   - boss-turn gameplay events are analytics only, not user identity or ad tracking

## Local preview

Open `index.html` directly in a browser, or run a static server from the repo root:

```sh
python3 -m http.server 8088 --directory Website
```

Then visit `http://localhost:8088`.
