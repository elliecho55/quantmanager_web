# Features
## Unified Account Dashboard
View all accounts in one place with a high-level summary and a detailed account table. Instantly monitor equity, P&L, drawdown, lock status, and more. Accounts can be grouped (by firm, type, or other classifications) for quick comparison and aggregation.

## Per-Account Configuration Panel
Each account can be individually configured. Set firm/type classification, profit and loss limits, trailing rules, formulas, and scheduled flatten times. All changes save automatically and update the dashboard in real time.

## One-Click Flatten & Lock Actions
Quickly flatten positions or lock accounts directly from the toolbar or context menu. Perform actions on individual accounts or in bulk to respond instantly to risk events or rule violations.

## Automated Risk Enforcement
### Profit Target/Loss Limit Enforcement
If a profit target is hit or the loss limit is breached, the account is immediately flattened and locked for the remainder of the day.

### Trailing Balance Protection
Enable custom trailing balance rules based on realized or unrealized P&L. When the trailing threshold is crossed, the account is locked for a configurable duration, helping protect gains as equity grows.

### Timed & Session-Based Locks
Lock accounts until a specific time or for predefined session durations. Optional auto-flattening ensures no positions remain open when a lock activates.

## Advanced Controls & Automation
### Scheduled Flattening
Schedule accounts to flatten at a specific date and time. The scheduler runs automatically and updates future flatten events after execution.

### Formula-Driven Metrics
Customize how key metrics are calculated using editable formulas (e.g., [openpnl], IF(), MAX(), MIN()). Define your own logic for Open, Closed, and Total P&L, drawdown, and trailing balance calculations.

### Templates & Bulk Apply
Create templates that bundle classifications, limits, and formulas. Apply them to multiple accounts at once via the context menu for fast, consistent setup across all accounts.
