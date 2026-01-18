# Quant Manager Plugin Overview
Quant Manager is a Quantower plugin that provides a consolidated account dashboard and enforcement tools for trade management. It combines a summary view and account detail table, supports per-account settings, and enforces risk controls such as profit targets, loss limits, time-based locks, and trailing balance rules. It also includes scheduled flattening, account templates, and formula-driven metrics.

## Features
### Account Summary + Details Tables
The main window shows a summary table and a detailed account table with equity, P&L, drawdown, lock status, and other metrics. Summary grouping can be toggled (e.g., by Firm or Type) for quick aggregation.

### Account Visibility and Privacy
Accounts can be toggled visible/invisible in the main table. Privacy mode masks account names, and custom name display logic is supported for consistent identification.

### Edit Account Panel
A dedicated Edit Account plugin allows per-account configuration (firm/type, limits, formulas, trailing settings, and scheduled flatten time). Changes persist to local storage and immediately update the table.

### Manual Flatten and Lock Actions
You can flatten selected accounts, lock selected accounts for the day, and run bulk actions via toolbar buttons and context menu entries.

### Timed Locks and Session Locks
Accounts can be locked until a specific time, including session-based lock durations and configurable timeout buttons. Locks can optionally flatten positions when activated.

### Daily Reset at 5PM EST
Profit target and loss limit enforcement flags reset daily at 5PM EST, ensuring limits are enforced once per trading day and recover cleanly after reset.

### Profit Target Enforcement
When a configured profit target is reached, the account is flattened and locked for the remainder of the day. This is tracked per day and persists across restarts.

### Loss Limit Enforcement
When a configured loss limit is breached, the account is flattened and locked for the remainder of the day. This mirrors profit target enforcement behavior.

### Trailing Balance Protection
Trailing balance can be enforced in Realized or Unrealized mode. When the balance crosses the computed trailing threshold, the account is locked for a configurable duration.

### Peak Balance and Peak Open P&L Tracking
The plugin tracks peak balance and peak open P&L values for each account. Peak open P&L resets to 0 when the account becomes flat.

### Day Starting Balance Tracking
The plugin records a daily starting balance for each account and resets it at the 5PM EST daily reset. This value is also exposed in formulas via `[day starting balance]` for custom calculations.

### Scheduled Flattening
Accounts can be configured to flatten at a specific date/time. The scheduler runs automatically and updates the next scheduled time after flattening.

### Formula-Driven Metrics
Open/Closed/Total P&L, Drawdown, and Trailing Balance are calculated using editable formulas (e.g., `[openpnl]`, `IF()`, `MAX()`, `MIN()`), allowing customized logic per account.

### Templates and Bulk Apply
Templates bundle classification, limits, and formulas. They can be applied to multiple accounts at once via a context menu, making bulk setup fast and consistent.

### Local Storage and Persistence
All per-account settings and enforcement flags are persisted to a local JSON storage file, so settings survive restarts and reflect in the UI immediately.

