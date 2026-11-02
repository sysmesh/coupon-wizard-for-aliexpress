# Changelog

All notable changes to Coupon Wizard for AliExpress.

## 1.1.1 — 2026-11-02

### Fixed

- **The promo code box still didn't open on the real AliExpress checkout.** The checkout shows
  a "Promo codes" row with an **Enter** action next to it. The extension clicked the title
  instead of **Enter**, so nothing opened. It now clicks **Enter**, and recognises the code
  box that appears even though it has no label.
- **Delivery text mistaken for the promo code area.** Text such as "₪4.00 coupon code if
  delayed" could be picked instead of the real "Promo codes" row. The real row now wins.
- **Working codes reported as failed.** The previous code's "invalid" message was often still
  on screen and was read as the new code's result. Old messages are now ignored, and a lower
  total always counts as success.
- **"Go to checkout first" on a page opened before an update.** After the extension is
  installed or updated, already-open tabs can't talk to it until they are reloaded. The popup
  now says so and offers a **Reload page** button.

### Changed

- **"Open cart" is now "Open checkout".** It opens your cart and presses its **Checkout**
  button for you. AliExpress has no direct checkout link: checkout needs the items picked in
  the cart.
- On the checkout page, the popup now goes ahead even if it can't see the code box yet, and
  opens it before trying the first code.
- When the code box can't be found, the popup and the on-page message now add:
  **"Already on the checkout page? Make sure that the coupon box is expanded"**.

### Notes

- No new permissions. Nothing about what data the extension reads or sends has changed.

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
