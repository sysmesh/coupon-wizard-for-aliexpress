# Privacy Policy — Coupon Wizard for AliExpress

_Last updated: 2026-11-27_

Coupon Wizard for AliExpress ("the extension") is an independent, open-source browser
extension by Gilad Ariav. It is not affiliated with, endorsed by, or connected to
AliExpress or Alibaba Group.

## What the extension does

On the AliExpress cart and checkout pages, the extension reads the order total shown on
the page, downloads publicly posted promo codes from community sources (by default the
public RSS feed of the Reddit community r/AliExpressCode; for shoppers whose AliExpress
ship-to country is Israel, also the public deals forum bee.deals), and enters those codes into
the promo-code box on the page so you can see which one lowers your total.

## Data collection

**The extension does not collect, store, transmit, sell, or share any personal data.**

- No account, sign-up, or login is required.
- No analytics, telemetry, tracking pixels, or crash reporting are included.
- Nothing you do on AliExpress — your cart, your orders, your addresses, your payment
  details, the pages you visit — is ever sent anywhere. All page reading happens locally
  in your browser and is discarded when the page closes, with one exception: the
  two-letter code of your AliExpress ship-to country (for example `IL`) is remembered
  in the browser's local extension storage, as described below.
- The developer has no server and receives no data from the extension.

## Network requests

The network requests the extension makes are to download the public coupon
sources you have enabled (by default `https://www.reddit.com/r/AliExpressCode/new.rss`).
If your AliExpress ship-to country is Israel, the extension offers to also read the public
AliExpress coupon posts on `https://bee.deals`. It contacts that site only after you allow
it in the browser's permission prompt, and never for other ship-to countries. To decide
this, the extension reads the ship-to country on the AliExpress page: from AliExpress's
own settings cookie, or from the country flag shown in the page header. The country code
is kept in local extension storage, because the checkout page does not always show it.
It never leaves your browser.

Promo codes mostly state their amounts in US dollars. When your cart and a promo code
are in different currencies, the extension downloads a public table of exchange rates so
it can compare the two: from `https://open.er-api.com` (Exchange Rate API), or from
`https://api.frankfurter.dev` if the first is unreachable. The request asks for the
general table of rates against the US dollar: it does not contain your currency, your
total, or anything else about your cart. The rates are kept in the browser's memory only
(session storage), never written to disk. They are refetched at most every few hours
while the services answer (and after a browser restart), and no more than every 10
minutes when the services are down. No such request is made when your cart and all the codes are in the same currency.

All of these requests are made without cookies or credentials and carry no information
about your cart. Like any web request, they show the site your IP address, and that the
request comes from this extension. The extension makes no other network requests.

## Local storage

The extension stores, in your browser only (Chrome's extension storage):

- the downloaded list of promo codes, cached for about an hour (codes from a source that
  cannot be reached are kept for up to a day);
- the last AliExpress ship-to country seen (a two-letter code such as `IL`), used to pick
  the coupon sources for your country;
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

- **storage** — keep the coupon cache, the last ship-to country code seen and your settings
  in your browser.
- **activeTab** — read the URL of the tab you opened the popup on, so the popup knows
  whether you are on an AliExpress cart/checkout page.
- **aliexpress.com / aliexpress.us** — run on AliExpress pages to read the cart total and
  the ship-to country (from AliExpress's settings cookie or the flag in the page header),
  enter promo codes, and bring you back to your cart after the optional affiliate click.
- **reddit.com** — download the public coupon feed.
- **bee.deals** (optional; the popup asks for it only when you ship to Israel, and Settings
  asks when you switch that source on yourself) — download public coupon posts. Switching
  the source off in Settings hands the permission back.

## Changes

If this policy changes, the updated version will be published at the same URL and the
extension's version number will be increased.

## Contact

Questions about this policy: open an issue at
https://github.com/sysmesh/coupon-wizard-for-aliexpress
