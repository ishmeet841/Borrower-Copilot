#  Borrower Copilot

This is my take-home implementation for Lokta's Borrower Copilot assignment.

I built it as a small React + Vite + TypeScript app that runs fully in the browser. There is no backend, login, database, bureau pull, CIBIL integration, Firebase setup, or external API call in the app. The borrower answers the questions, the browser runs the rules, and the result is shown immediately.

## Running it

```bash
npm install
npm run dev
```

Vite will print a local URL. On my machine it is usually:

```text
http://127.0.0.1:5173/
```

For a production build:

```bash
npm run build
```

For the finance-rule checks:

```bash
npm test
```

## What I focused on

The main product choice was to keep the borrower view and lender view separate.

A lender may be willing to sanction a higher amount because their lens is repayment probability and security. A borrower should often be more conservative because their lens is monthly cash flow, household expenses, emergency savings, and what happens if income drops. The app shows both numbers side by side and recommends the lower responsible amount.

The questionnaire starts with the common questions needed for every borrower, then branches:

- Salaried borrowers get job stability, employer type, and variable pay questions.
- Self-employed borrowers get business vintage, cash-income range, ITR income, collateral, and co-applicant questions.
- Informal borrowers get income range, income history, dependents, app-loan stress, and bounced EMI questions.

I kept every rule in normal TypeScript files so it is easy to inspect or change in a follow-up interview.

## Files

```text
.
├── README.md
├── RULES.md
├── RUN_THROUGHS.md
├── WALKTHROUGH.md
├── index.html
├── package-lock.json
├── package.json
├── src
│   ├── App.tsx
│   ├── data
│   │   ├── demoProfiles.ts
│   │   └── productRates.ts
│   ├── lib
│   │   ├── calculations.test.ts
│   │   ├── calculations.ts
│   │   ├── format.ts
│   │   └── rules.ts
│   ├── main.tsx
│   ├── styles.css
│   ├── types.ts
│   └── vite-env.d.ts
├── tsconfig.app.json
├── tsconfig.json
├── tsconfig.node.json
└── vite.config.ts
```

## What is included

- Adaptive multi-step borrower questionnaire
- Demo profiles for Priya, Ravi, and Anita
- Borrow / Borrow less / Don't borrow verdict
- Likely lender sanction amount
- Safer borrower amount
- Recommended amount to anchor on
- Fair interest-rate band
- Processing-fee band and all-in APR
- Safe EMI ceiling
- 3 / 5 / 7 year tenure comparison
- Income-drop and rate-rise stress case
- Confidence level with reasons
- Lender-facing Negotiation Card
- Unit tests for the important calculation paths

## Rule summary

The lending side uses FOIR-style capacity, credit score if known, income stability, existing EMIs, collateral, co-applicant income, product caps, and tenure.

The borrower-safety side is stricter. It looks at disposable income after household expenses, emergency savings, high-cost app loans, bounced EMI history, productive income lift, upcoming expenses, and a +2 percentage point interest-rate stress.

APR is calculated from the EMI cash flow after subtracting the processing fee from disbursal. That is why the all-in APR can be higher than the quoted interest rate.

## Known limitations

This is not a lender approval tool. It does not verify bank statements, salary slips, property title, ITR filings, gold value, employment, or app-loan balances. The rate bands are documented assumptions, not live market quotes. The point of this version is to make the reasoning visible enough that it can be challenged and edited.
