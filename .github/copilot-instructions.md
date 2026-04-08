# ISF Flutter Instructions

This repository powers the member-facing mobile app for Al-Ihsan Savings Fund (ISF).

Product and domain priorities:

- ISF starts as a voluntary monthly office group savings fund focused on disciplined savings, transparency, and member trust
- Keep the MVP savings-first: dashboard, dues, deposits, statements, notifications, and member transparency
- Treat the first phase as a 3-month savings-only trial period
- Do not introduce investment, profit-sharing, dividend logic, or complex loan logic unless explicitly requested
- Qard-e-hasana is a possible later feature and must stay behind a separate policy and workflow

Core rules:

- Treat `users` as login accounts
- Treat `members` as fund memberships
- One user may manage multiple members, including family memberships if the product later enables it
- All financial records shown in the app must be member-based, not user-based
- Members may hold one or more units; keep unit counts explicit and simple in the UI
- Use 1000 BDT as the default monthly unit amount unless the user requests otherwise
- Participation is voluntary, and membership should not be auto-cancelled because of job change, relocation, or leaving the company

Member app scope:

- Focus on login, dashboard, deposit submission, deposit status, statements, balances, and notifications
- Members should be able to submit bank deposit proof and later see whether an admin verified it
- Show current balance, contribution history, and ledger entries in a clear and trustworthy way
- Use Bengali-friendly labels and flows where user-facing copy is added
- Avoid admin-heavy workflows in Flutter unless explicitly requested

Product behavior:

- Prefer bank-channel-first flows and avoid cash-first assumptions in UI or copy
- If notifications are implemented, use them for deposit verification and important account status changes
- Keep the UI simple, transparent, and easy to verify rather than decorative or abstract

Flutter implementation guidance:

- Keep widget structure simple and maintainable
- Use straightforward state flow and avoid unnecessary packages
- Prefer explicit domain naming that matches ISF concepts directly
- When adding financial UI, make statuses, amounts, dates, and references easy to read and reconcile

Decision principle:

- Optimize for member clarity, traceable financial data, low operational risk, and room to extend later without overbuilding now
