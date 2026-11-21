# Jamaica Credit Intelligence

An interactive HTML, CSS and SVG dashboard by Julian Devonish, using official Bank of Jamaica lending and loan-quality data. No synthetic financial observations.

**[Open the live dashboard](https://jdevonish25.github.io/Jdevonish25/)** · [Download the complete source](Jamaica-Credit-Intelligence-source.zip)

## Decision context
Where does Jamaican credit sit, how is lending changing, and which customer groups hold overdue balances? Four views connect the executive overview, business-sector exposure, overdue-loan composition and methodology.

## Data
115 monthly observations, March 2017–September 2026, retrieved 21 November 2026. Source population: commercial banks, building societies and merchant banks. All currency balances are expressed in JMD millions in the source; the UI converts to billions or trillions.

- `FS.DTI.07.TOT`: loans and advances by sector, all currencies in JMD.
- `FS.DTI.00B`: monthly non-performing and past-due loans by customer group.
- `FS.DTI.01`: local business loans by size.
- Source page: https://boj.org.jm/statistics/financial-sector/banking-system/

Raw workbooks, source URLs and SHA-256 hashes are retained under `source/`. Only named modern monthly panels are used, excluding legacy quarterly and unrelated embedded sheets. Source retrieval URLs can remain unchanged while workbook contents update; use hashes to identify this snapshot.

## Analytical rules
Balances are month-end stocks, never summed across months. Annual growth compares the same month of the prior year. NPL and past-due ratios use their published totals divided by same-month total DTI lending. Customer-group shares divide by the corresponding overdue total. Sector shares use resident business-purpose credit. Size shares use the four size categories' own total.

Lending and loan-quality sector classifications differ; no unverified sector NPL ratios or risk scores are constructed. Business-size totals are kept separate from business-sector totals. Nominal stock changes can include valuation, repayments and write-offs and are not new lending. This is descriptive analysis, not a default prediction or causal study.

## Implementation
Buildless static application with custom SVG line charts, composition ring, ranked bars, an exposure-growth scatterplot, monthly heatmap, linked sector selection, period controls, tooltips, CSV download and an accessible methodology view. Responsive CSS, keyboard-operable controls and reduced-motion support. No login or tracking.

## Reproduce
Python dependencies: pandas, xlrd, openpyxl. Node.js is used for static checks.

```text
python source/fetch_data.py
python source/prepare_data.py
node --check dist/app.js
node source/check_dashboard.cjs
python -m http.server 8766 --directory dist
```

`fetch_data.py` retrieves live source workbooks, which may be revised after this publication. `prepare_data.py` validates the documented snapshot and writes tidy CSV and JSON. Update its explicit coverage assertions for a new release rather than silently extending the reporting period.

## Validation
Unique, aligned monthly dates; finite, non-negative source balances; lending components reconcile to total; sector, NPL and past-due components reconcile to published controls within JMD 0.02 million. Renderer checks cover early-history missing comparisons, latest metrics, every view and all trend windows. Desktop visual inspection supplements programmatic checks.

## Design attribution
Visual direction informed by Michal Polewiak's Superstore 2026 dashboard: https://public.tableau.com/app/profile/michal.polewiak/viz/Superstore2026_17837711692360/Summary . Original interface, chart implementation and financial analysis for this project. Official data remains subject to BOJ's terms; this independent portfolio project is not affiliated with BOJ.
