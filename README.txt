NEPSE COMPANY INTELLIGENCE DASHBOARD — MOBILE v4
================================================

FILES
- index.html: complete responsive website (not empty)
- companies.csv: 356 company profiles used for hosted refresh/import
- companies.json: source data copy
- README.txt: setup instructions

FEATURES
- 356 companies seeded from the supplied workbook
- Search by company name or symbol
- Filter by company type, positive profit, loss-making, and watchlist
- Company profiles: revenue, profit, borrowings, assets, headquarters, office count, period, source
- Derived screening ratios: profit margin, debt/assets, ROA
- Watchlist, personal notes, monitoring log
- Import CSV / Excel from your device
- Refresh Hosted CSV from the same folder as index.html
- Export watchlist CSV and research notes JSON
- Responsive layouts for desktop, tablet and mobile

GITHUB PAGES
1. Extract this ZIP.
2. Upload index.html and companies.csv into the same published folder of your repository.
3. Commit/push changes and wait for GitHub Pages deployment to complete.
4. Open the deployed site. Press “Refresh Hosted CSV” after you update companies.csv on GitHub.
5. For a CSV on your computer, press “Import CSV / Excel”.

IMPORTANT
- The hosted refresh button reads the deployed companies.csv; it cannot upload local changes back to GitHub.
- GitHub Pages is static hosting. It does not automatically generate new market data, prices, or financial reports.
- The supplied workbook has period labels such as FY 2080/81 (Q4); the dashboard should not be mistaken for a live data feed.
- Notes and watchlist are stored in local browser storage on this device. Export notes for backup.
- Derived ratios are indicative screening calculations, not audited investment advice.


IMPORT BUTTON FIX — v5
- The Import CSV / Excel control uses a native label linked directly to the file input.
- This avoids relying on a scripted click to open the operating system's file picker, which can be blocked by some browser contexts.
- After selecting a CSV, the page validates the required Symbol and Company Name columns and reloads the company table and profile data.


IMPORT FORMAT SUPPORT (v7)
- Import CSV files (.csv) directly.
- Import Excel workbooks (.xlsx, .xls) from the first worksheet. Excel import loads SheetJS from jsDelivr, so an internet connection is needed for Excel files. CSV import works without that library.
- Required column headers: Symbol and Company Name. Other headers should match the dashboard data columns.
