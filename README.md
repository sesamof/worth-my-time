# Worth My Time v1.9

v1.9 is a maintenance release. It hardens the app and refreshes the service worker cache so installed devices reliably pick up the update. No feature behaviour changes from v1.8.

## v1.9 changes
- Service worker cache bumped to `worth-my-time-v1.9-1` so existing installs (PC, iPhone, Samsung) update instead of serving stale cached files.
- Fixed expense amount field now coerces to a valid number when rendering, preventing a blank or `NaN` value from ever showing in the input.
- Version labels updated across the app, manifest cache and documentation.
- Verified end to end: real available hourly rate, calculator, Want List, Allocate, History, Savings goals and the Buy Now vs Save First credit comparison all tested and passing.

## v1.8 features (retained)
- Buy Now vs Save First comparison on each Savings goal.
- Default credit interest rate 17.5% per year; payment periods of 3, 6, 12, 18 and 24 months.
- Estimated monthly payment, final credit cost and extra interest.
- TIME GIVEN TO THE BANK shown as working time represented by the interest.
- Available monthly cash and adjusted hourly rate while repaying, plus total credit repayment working time.
- Dark mode and Want List to Allocate integration.

Credit figures are estimates using a standard amortising monthly-payment model. Actual credit-card interest, fees and daily-interest calculations vary by provider.

## Files
- `index.html` — the whole app (HTML, CSS and JavaScript in one file).
- `sw.js` — service worker for offline / installable PWA support.
- `manifest.webmanifest` — PWA manifest (name, icons, theme).
- `icons/` — app icons (192, 512, 180).

Data is stored locally in the browser via `localStorage`. Nothing leaves the device.
