# Five-Minute Walkthrough

## 0:00 - 0:45

Borrower Copilot is a pre-loan check for an Indian borrower. The user answers a short questionnaire and gets four things:

1. Whether to borrow, borrow less, or not borrow right now.
2. What a lender may sanction versus what the borrower can safely carry.
3. A fair interest-rate range and all-in APR after processing fee.
4. The EMI limit the borrower should not cross.

I kept the app browser-only. There is no bureau call, login, backend, or stored personal data.

## 0:45 - 1:45

The form starts with the questions that are needed for everyone: loan purpose, amount, loan type, income type, income, age, existing EMIs, household expenses, and credit score if known.

After that it branches.

Salaried users are asked about employer type, years in current job, and variable pay. Self-employed users are asked about business vintage, cash-income range, ITR income, property collateral, and co-applicant income. Informal users are asked about income range, months of income history, dependents, high-cost app loans, and recent EMI bounce.

I tried to avoid curiosity questions. If a question is in the flow, it moves at least one output.

## 1:45 - 3:15

The most important modelling choice is that lender sanction and borrower safety are not the same number.

For lender sanction, I use assessed monthly income, a lender FOIR cap, credit quality, income stability, existing debt, collateral, co-applicant income, product limits, and tenure.

For borrower safety, I use a lower FOIR, household expenses, disposable income, emergency savings, high-cost debt, upcoming expenses, productive income lift, and a +2 percentage point rate stress.

Unknown credit score is handled as uncertainty, not as bad credit. The range gets wider and confidence falls, but I do not score it as a weak bureau profile.

APR is calculated from cash flows: the borrower receives principal minus processing fee, then repays EMIs. This makes fee-heavy loans look more expensive, which is the point.

## 3:15 - 4:15

Priya can borrow the requested ₹8,00,000 personal loan. Her salary, employer stability, and credit score support it. The app still warns her that a 20% income drop would make the EMI less comfortable.

Ravi is a "borrow less" case. He asks for ₹15,00,000 as a business loan, but because he owns an unencumbered shop property, the app points him toward LAP. Even then, it recommends about ₹9,80,000 because cash flow and emergency savings are the binding constraints.

Anita is the responsible hard-stop case. The scooter could help her earn more, but the combination of app loans, a recent bounced EMI, no emergency buffer, and tight household cash flow makes a new loan unsafe today.

## 4:15 - 5:00

If I had more time, I would add a quote-comparison screen where the borrower can enter real offers and see which quote beats the card. I would also add a printable/downloadable Negotiation Card.

I would avoid adding simulated lender matching or made-up bureau data. The useful thing here is not pretending to know more than the borrower gave us; it is turning those answers into a clear, editable lending judgement.
