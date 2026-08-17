# Freeagent-Offline-viewer
If you've exported your data from freeagent but don't want to view it in Excel, this is for you


# Ledger Viewer for FreeAgent

A private, offline, read-only viewer for your [FreeAgent](https://www.freeagent.com) data export.It provides invoices, bank statements, payslips, dividends, VAT returns, Corporation Tax returns, PAYE & NI summaries, and more as a single static HTML file that runs entirely in your browser.


## Why

FreeAgent doesn't offer a lightweight way to browse historical data offline, or after you've cancelled a subscription. This tool reads FreeAgent's own data-export spreadsheet and attachments folder and renders them back out in a familiar, navigable format — for your own archival or reference use.

## Privacy

- This is a static HTML file with no backend and no network calls except loading Google Fonts and the [SheetJS](https://sheetjs.com/) library from a CDN (used only to parse the spreadsheet you provide).
- Your `.xlsx` export and attachments are processed **entirely in your browser**. Nothing is uploaded anywhere.
- Do **not** commit your own populated copy of this file to a public repository — see "Using it" below.

## Using it

1. In FreeAgent, go to **Settings → Import/Export Data** and download your full data export (`.xlsx`), plus your attachments folder if you want receipts and documents linked.
2. Open `index.html` in a browser (double-click it, or visit the GitHub Pages URL if hosted).
3. On first load you'll see a setup screen — upload your `.xlsx` export (and optionally your attachments folder), then click **Open My Ledger**.
4. Once loaded, use the **"Download self-contained copy"** button in the sidebar to save a personal file with your data baked directly in, so you don't need to re-upload each time. **Keep that personal copy private** — do not commit or publish it, since it will contain your real financial data.
5. You can re-run the import at any time (e.g. after a fresh FreeAgent export) from the same sidebar panel to refresh your data.

## What's included

- Dashboard with bank balances, outstanding invoices, and turnover
- Invoices, Contacts, Projects, Expenses, Bank Accounts (with year/month filters and invoice payment links), Payslips, Dividends
- Reports: VAT Returns, Corporation Tax (Computations + CT600 views), PAYE & NI Summary, Final Accounts, Capital Assets, Journals, Company & Users
- Search, filtering, and pagination throughout
- Receipts and documents linked inline where attachments are available

## Limitations

- Some figures (e.g. payslip year-to-date totals, Corporation Tax computation walk-throughs, PAYE & NI brought-forward balances) are reconstructed from the underlying transaction data rather than pulled from a field FreeAgent exports directly, since the export doesn't include every internally-computed figure. Individual transaction-level data matches your export exactly.
- Requires a one-time internet connection to load fonts and the spreadsheet-parsing library. Works fully offline after that.

## License

MIT — do whatever you like with the code. Just don't publish your own data with it.
