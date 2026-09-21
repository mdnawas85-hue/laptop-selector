# Laptop Selector

Single-file HR/IT tool for allocating laptops from available stock.

The **job title drives everything** — it derives a user category (Lite / Standard /
Power) and allocates a specific machine from available stock. Category can be
overridden manually; changing the title re-derives it.

- Printable issue form, CSV export, allocation log
- Selection never downgrades: if a category is empty it steps **up** and flags the
  upgrade; if nothing fits, submit is disabled rather than allocating wrongly
- Grading is derived from the register, not hardcoded, so stock edits flow through

## Stock sources

1. **IT Asset Manager API** — enter the URL and API key in the UI (stored in
   `localStorage` only, never in this file)
2. **CSV import** — an Asset Manager export
3. **Sample data** — fictitious demo rows shipped with the page so it works
   before a source is connected. No real asset data is in this repository.

## Running it

Open `index.html` in a browser, or use the hosted page. No server, no build step.

## Notes

- The allocation log is stored per-browser in `localStorage`
- Allocating here does **not** reassign the asset in the register
