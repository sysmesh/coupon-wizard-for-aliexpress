# Privacy Policy — Coupon Wizard for AliExpress

_Last updated: 2026-10-16_

Coupon Wizard for AliExpress ("the extension") is an independent, open-source browser
extension by Gilad Ariav. It is not affiliated with, endorsed by, or connected to
AliExpress or Alibaba Group.

## What the extension does

On the AliExpress cart and checkout pages, the extension reads the order total shown on
the page, downloads publicly posted promo codes from community sources (by default the
public RSS feed of the Reddit community r/AliExpressCode), and enters those codes into
the promo-code box on the page so you can see which one lowers your total.

## Data collection

**The extension does not collect, store, transmit, sell, or share any personal data.**

- No account, sign-up, or login is required.
- No analytics, telemetry, tracking pixels, or crash reporting are included.
- Nothing you do on AliExpress — your cart, your orders, your addresses, your payment
  details, the pages you visit — is ever sent anywhere. All page reading happens locally
  in your browser and is discarded when the page closes.
- The developer has no server and receives no data from the extension.

## Network requests

The only network requests the extension makes are to download the public coupon
sources you have enabled (by default `https://www.reddit.com/r/AliExpressCode/new.rss`).
These requests are made without cookies or credentials and carry no information about
you or your cart. The extension cannot contact any other site: it has no permission to.

## Local storage

The extension stores, in your browser only (Chrome's extension storage):

- the downloaded list of promo codes, cached for about an hour;
- your settings (enabled sources, timeouts, and the optional affiliate-link override).

Chrome may sync the settings across your own signed-in Chrome profiles via Chrome Sync.
Uninstalling the extension deletes all of it.

## Affiliate link ("Support us" button)

The popup contains a clearly labelled button, **"Please click here to support us by
using our affiliate link."** Nothing happens unless you click it. If you do, your tab is
sent through an AliExpress affiliate tracking link and then returned to the page you
were on. This may earn the developer a commission from AliExpress on purchases you
make, at no extra cost to you. It does not change the coupons found or the prices you
pay. The extension never modifies links on the page and never uses the affiliate link
automatically.

## Permissions

- **storage** — keep the coupon cache and your settings in your browser.
- **activeTab** — read the URL of the tab you opened the popup on, so the popup knows
  whether you are on an AliExpress cart/checkout page.
- **aliexpress.com / aliexpress.us** — run on AliExpress pages to read the cart total,
  enter promo codes, and bring you back to your cart after the optional affiliate click.
- **reddit.com** — download the public coupon feed.

## Changes

If this policy changes, the updated version will be published at the same URL and the
extension's version number will be increased.

## Contact

Questions about this policy: open an issue at
https://github.com/sysmesh/coupon-wizard-for-aliexpress
