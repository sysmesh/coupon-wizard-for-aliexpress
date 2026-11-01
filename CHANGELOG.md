# Changelog

All notable changes to Coupon Wizard for AliExpress.

## 1.1.0 — 2026-11-01

### Fixed

- **Checkout page not recognised when the promo code box is collapsed.** On some checkouts
  AliExpress hides the code field behind a link such as "Have a coupon code?". The popup then
  said "Go to checkout first" even though you were on the checkout page. The extension now
  recognises the checkout page from its address, opens the promo code area for you, and
  carries on as normal.
- **The promo code area sometimes did not open.** When the "enter a code" link sat inside a
  larger box, the extension clicked the box instead of the link, so nothing happened. It now
  clicks the link itself.

### Notes

- The promo code area is only opened automatically on the checkout page, and only when you
  open the extension's popup. Other AliExpress pages are never clicked.
- No new permissions. Nothing about what data the extension reads or sends has changed.

## 1.0.0 — 2026-10-16

First public release.

- Reads publicly posted AliExpress promo codes from r/AliExpressCode.
- Picks the codes that fit your cart total and tries them one by one on the checkout page.
- Keeps the code that gives the lowest total, or tells you "No coupon worked".
- Runs entirely in your browser; no cart or personal data leaves it.
