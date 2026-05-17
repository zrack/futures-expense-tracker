# Trading Expense Ledger

A standalone, offline-first HTML app for tracking futures and prop trading expenses with tax-time supporting details.

## What It Tracks

- Date paid and tax year
- Expense, refund, or reimbursement type
- Category, payee/vendor, item or service, and business purpose
- Payment method
- Receipt/proof status and receipt reference
- Deductibility review status
- Notes for allocations, subscription periods, or CPA questions

## Trading Categories

The app includes common trading-expense categories:

- Prop firm evaluation fees
- Prop firm resets
- Account activation and monthly account fees
- Market data and exchange fees
- Trading platform software
- Trading journal tools
- VPS and cloud services
- News and research subscriptions
- Education and coaching
- Professional services
- Internet and home office allocation
- Hardware and equipment
- Bank, wire, and payment fees
- Refunds and credits

You can also type a custom category.

## Features

- **Offline app**: The tracker is a single HTML file with no external scripts or CDN dependencies.
- **Local storage**: Entries are stored in your browser on your device.
- **Legacy migration**: Older `futuresExpenses` records are migrated into the richer v2 schema.
- **Ledger workflows**: Add, edit, copy, delete, and undo deleted entries.
- **Filters**: Filter by tax year, category, deductibility status, or search text.
- **Monthly closeout**: Review one month at a time with monthly totals, category totals, missing proof, review items, and one-click month CSV export.
- **Tax review fields**: Mark entries as needs review, likely deductible, partial/allocation, not deductible, or reimbursed.
- **Proof checklist**: Track whether a receipt is missing, stored, linked, on a statement, or not needed.
- **Exports**: Export filtered CSV for tax review or bookkeeping, and JSON backup for full data recovery.
- **Imports**: Import JSON backups and merge them with existing records.

## Getting Started

1. Open `futures-expense-tracker.html` in your browser.
2. Add an entry using the form.
3. Keep receipts, statements, invoices, and payment confirmations in an organized folder.
4. Use the receipt reference field to point to the matching proof.
5. Use Monthly Closeout to clean up missing proof and review items before the month gets stale.
6. Export a JSON backup regularly.
7. Export CSV when preparing records for a spreadsheet, accountant, or tax software.

## Monthly Closeout

Use the Monthly Closeout panel as a simple habit loop:

- Pick the month you want to review.
- Check monthly net expenses, gross spend, refunds/reimbursements, and entry count.
- Review category totals for quick reasonableness checks.
- Clear the Missing Proof list by finding receipts, invoices, confirmations, or statements.
- Clear the Needs Review list by deciding what should be marked likely deductible, partial/allocation, not deductible, or reimbursed.
- Export the month CSV once the month is cleaned up.
- Export a JSON backup after making changes.

## Data Storage

All ledger data is stored in browser `localStorage` under `futuresExpenseTracker.v2`. That keeps the app simple and private, but it also means your records depend on that browser profile.

Recommended habit:

- Export a JSON backup after each recordkeeping session.
- Store backups somewhere durable, such as an encrypted cloud drive or external backup.
- Keep receipts and statements outside the browser, organized by tax year and expense type.

## Tax Note

This app is for recordkeeping only. It does not decide whether an expense is deductible, whether you qualify as a trader in securities, or how an expense should be reported. Use the deductibility status field as a review workflow and confirm the final treatment with a qualified tax professional.

IRS recordkeeping guidance generally expects records and supporting documents to identify things like payee, amount, proof of payment, date incurred or paid, and a description/business purpose. This tracker is designed to help collect those facts, but your supporting documents still matter.

## Browser Compatibility

Works in modern browsers that support localStorage, Blob downloads, and FileReader:

- Chrome / Edge
- Firefox
- Safari

## Privacy

The app itself does not send your expense data over the internet. It has no analytics, backend, or third-party script dependencies. Your browser and operating system still control local file downloads, imports, backups, and storage.
