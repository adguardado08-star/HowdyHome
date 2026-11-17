# HowdyHome — Texas A&M housing decision prototype

A self-contained responsive website made using **HTML, CSS, and JavaScript**. No subscription, build tools, framework, or database is required to run the first version.

## Run locally

**Simplest:** unzip the project folder and double-click `index.html` to open it in your browser. This prototype works offline (except the optional Google Fonts download).

**Using VS Code (recommended):** open the entire folder in VS Code. Install the optional **Live Server** extension, right-click `index.html`, and select **Open with Live Server**.

**Using a terminal (optional):** from the unzipped folder, run `python3 -m http.server 8000`, then open `http://localhost:8000` in your browser. Stop the server with `Ctrl+C`.

## What already works

- Seven-step housing preferences quiz, including budget and hard dealbreakers
- Preference-weighted matching, with ineligible options identified as trade-offs
- 18 **fictional** housing scenarios spanning dorms, university apartments, student apartments, conventional apartments, houses, and subleases
- Text search, type and price filters, sorting by matching, cost, name and unknown-count
- Saved listings and quiz answers retained in the browser via localStorage
- Details for each listing, including lease risks and explicitly UNKNOWN fees
- Editable calculator with recurring costs, one-time purchases, deposits, lease totals and upfront cash
- Responsive design for desktop and mobile

## Important data warning

**ALL listing names, prices, attributes, commute times, and contracts are fictional examples.** These are not verified College Station listings, real-time availability, quotes, or endorsements. No property record in this prototype should be used to make a housing decision. The match algorithm is a product demo rather than a validated recommendation model.

## Project structure

- `index.html`: page layout and quiz/detail modals
- `styles.css`: visual design and mobile layout
- `app.js`: sample property data, search, quiz, matching, saved entries, calculator

## How to add actual properties

In `app.js`, edit `SAMPLE_LISTINGS` (near the beginning of the file). For each real housing option, collect: official name, property/floorplan ID, housing type, unit rent vs bedroom rent, billing structure, lease term, what is included, all known fees, utilities calculation, deposits, furnishing, bedroom/bathroom configuration, location/transportation, source URLs, date verified, contact information, and student eligibility rules. The current array lacks the fields for actual source-linked production data; expand the schema **before** publishing real listings. Treat unknown costs as unknown, not zero, and never fabricate a range.

For long-term maintenance, move verified property records into a database, add administrator tools, and track per-field evidence, verification date, and pricing date. For real availability, require current property confirmation.

## Important prototype limitations

- Cost shown on cards is *illustrative monthly equivalent per person*, not an actual all-in cost or signed offer. In particular, dorm charges can be term-based and meal plans can be billed separately.
- In the calculator, **Use in calculator** loads an illustrative estimate by converting the per-person price to a two-person unit rent. It intentionally sets unknown utilities/fees/deposits to 0 as **editable placeholders** and triggers a warning. These zeroes must not be treated as actual estimates.
- Scoring uses invented attributes and simplified commute values, not actual route measurements.
- Browser localStorage is device-specific; there are no user accounts or syncing.
- No backend, automatic price updates, map, payment integration, or property submission workflow yet.
- Use only with proper authorization when collecting or importing third-party property data.

## Deploy later

Upload the three website files to a static hosting service (for example, Cloudflare Pages or GitHub Pages). Since this version needs no backend, static hosting is sufficient. Keep data clearly labeled as demonstrations until you verify all facts. Before a public launch, add a privacy policy and correction/reporting channel, and verify housing and fair-housing compliance.

This is an independent student concept and is not officially affiliated with Texas A&M University.
