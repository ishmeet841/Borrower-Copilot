# Rules and assumptions

These are the rules I used for the prototype. They are deliberately simple enough to change during a follow-up call.

This is not a lender's credit decision. It is a borrower-side estimate based only on what the user enters.

## Product assumptions

| Product | Rule | Value | Why I used it | Source |
|---|---:|---:|---|---|
| Personal loan | Interest band | 11% - 22% | Unsecured personal credit needs a wide range. | my judgement |
| Personal loan | Processing fee | 1% - 3% | Typical enough fee range for a prototype. | my judgement |
| Personal loan | Default tenure | 5 years | Long enough to compare affordability, not so long that risk is hidden. | my judgement |
| Personal loan | Comparison tenures | 3 / 5 / 7 years | Asked for in the assignment. | challenge brief |
| Personal loan | Max ticket | ₹25,00,000 | Keeps unsecured output from becoming unrealistic. | my judgement |
| Personal loan | Income cap | 20x assessed monthly income | Stops FOIR alone from over-sizing the loan. | my judgement |
| Business/MSME loan | Interest band | 13% - 24% | Unsecured MSME credit can be expensive, especially for thin-file borrowers. | my judgement |
| Business/MSME loan | Processing fee | 1% - 2.5% | Simple upfront-fee assumption. | my judgement |
| Business/MSME loan | Default tenure | 5 years | Works for working-capital style borrowing. | my judgement |
| Business/MSME loan | Max ticket | ₹30,00,000 | Keeps the prototype conservative. | my judgement |
| Business/MSME loan | Income cap | 24x assessed monthly income | Productive credit gets slightly more room than personal credit. | my judgement |
| Loan Against Property | Interest band | 9.5% - 15% | Secured borrowing should usually be cheaper than unsecured MSME credit. | my judgement |
| Loan Against Property | Processing fee | 0.75% - 1.5% | Lower-fee assumption for secured credit. | my judgement |
| Loan Against Property | Default tenure | 7 years | Gives a secured business borrower some breathing room without using a 15-20 year tenure. | my judgement |
| Loan Against Property | LTV cap | 50% of property value | Conservative haircut for borrower-facing advice. | my judgement |
| Loan Against Property | Income cap | 36x assessed monthly income | Secured credit can support a longer repayment profile. | my judgement |
| Two-wheeler/EV loan | Interest band | 11% - 19% | Asset-backed, but still small-ticket retail credit. | my judgement |
| Two-wheeler/EV loan | Processing fee | 1% - 2.5% | Small-ticket loans can have meaningful fees. | my judgement |
| Two-wheeler/EV loan | Default tenure | 3 years | Closer to useful vehicle life than a long consumer-loan tenure. | my judgement |
| Two-wheeler/EV loan | LTV cap | 85% of vehicle value | Assumes some down payment and avoids 100% financing. | my judgement |
| Gold loan | Interest band | 8.5% - 18% | Secured by liquid collateral, but pricing still varies a lot. | my judgement |
| Gold loan | Processing fee | 0.5% - 1.25% | Lower-fee assumption than unsecured credit. | my judgement |
| Gold loan | Default tenure | 2 years | I treated it as short-tenure credit. | my judgement |
| Gold loan | LTV cap | 70% of gold value | Conservative collateral haircut. | my judgement |
| Home loan | Interest band | 8.5% - 11.5% | Lowest-rate secured product in this set. | my judgement |
| Home loan | Processing fee | 0.25% - 1% | Lower fee assumption for larger secured borrowing. | my judgement |
| Home loan | Default tenure | 7 years | I kept the same 3 / 5 / 7 comparison instead of hiding affordability inside a very long tenure. | challenge brief + my judgement |
| Home loan | LTV cap | 80% of property value | Conservative secured lending assumption. | my judgement |

## Affordability rules

| Area | Rule | Value | Why I used it | Source |
|---|---:|---:|---|---|
| Lender FOIR | Salaried | 55% of assessed income | Salaried income is usually the easiest to underwrite. | my judgement |
| Lender FOIR | Self-employed | 50% of assessed income | Business income needs more room for month-to-month variation. | my judgement |
| Lender FOIR | Informal | 36% of assessed income | Informal income needs a much larger buffer. | my judgement |
| Safe FOIR | Salaried | 42% of assessed income | Borrower advice should be stricter than lender eligibility. | my judgement |
| Safe FOIR | Self-employed | 38% of assessed income | Business cash flow can dip even when the borrower is doing well overall. | my judgement |
| Safe FOIR | Informal | 28% of assessed income | Protects a lower-income household from a fixed EMI trap. | my judgement |
| Disposable income | Base EMI share | 62% of income left after expenses and existing debt | Leaves room for shocks and normal household leakage. | my judgement |
| Emergency buffer | Savings < 1 month | 50% of disposable income can go to EMI | No savings means the borrower needs more cash outside EMI. | my judgement |
| Emergency buffer | Savings 1 - 3 months | 56% of disposable income can go to EMI | A thin buffer should reduce the safe amount even when FOIR is not binding. | my judgement |
| Emergency buffer | Savings 3 - 6 months | 62% of disposable income can go to EMI | Base case. | my judgement |
| Emergency buffer | Savings >= 6 months | 66% of disposable income can go to EMI | A stronger buffer allows slightly more flexibility. | my judgement |
| Salary income | Variable pay haircut | 0.35% income haircut per 1% variable pay | Incentive income is not as dependable as fixed pay. | my judgement |
| Self-employed income | Cash range | 65% lower month + 35% higher month | Avoids using the best month as normal income. | my judgement |
| Self-employed income | With ITR | 55% conservative cash estimate + 30% ITR monthly income + 15% stated monthly income | Balances actual cash flow, documented income, and the user's own monthly estimate. | my judgement |
| Self-employed income | Without ITR | 75% conservative cash estimate + 25% stated monthly income | Still lets the must-answer income field matter. | my judgement |
| Informal income | Income range | 85% conservative range estimate + 15% stated monthly income | Leans conservative while still using the user's stated monthly number. | my judgement |
| Co-applicant | Counted income | 80% of co-applicant monthly income | Leaves room for the co-applicant's own expenses. | my judgement |
| High-cost app loans | Monthly outflow estimate | Max(stated outflow, 16% of outstanding balance) | If the EMI is unclear, the outstanding balance still needs a stress estimate. | my judgement |
| Productive lift | Counted upside | 30% of expected monthly income lift | Productive upside helps, but it is not guaranteed. | my judgement |
| Productive lift | Maximum boost | 8% of assessed monthly income | Stops optimistic business projections from dominating the answer. | my judgement |
| Upcoming expenses | Monthly reserve | Min(expense / 12, 8% of assessed income) | Large near-term expenses reduce the room for EMI. | my judgement |
| Rate stress | Higher-rate case | +2 percentage points | Shows whether a worse quote breaks affordability. | challenge brief + my judgement |
| Income stress | Lower-income case | -20% assessed income | Shows how fragile the loan is if income drops. | challenge brief + my judgement |
| APR | All-in APR | IRR after subtracting processing fee from disbursal | More honest than showing only headline interest. | challenge brief |
| Rounding | Amount outputs | Rounded down to nearest ₹5,000 | Avoids pretending the estimate is more precise than it is. | my judgement |

## Credit and stability adjustments

| Area | Rule | Value | Why I used it | Source |
|---|---:|---:|---|---|
| Excellent credit | Score | 760 - 900 | Strong repayment signal. | my judgement |
| Excellent credit | FOIR adjustment | Lender +5 points, safe +2 points | Allows more headroom without making borrower safety too loose. | my judgement |
| Excellent credit | Rate adjustment | Min -0.75 points, max -4.5 points | Strong borrowers should have a better negotiation band. | my judgement |
| Good credit | Score | 700 - 759 | Positive but not top-tier. | my judgement |
| Good credit | FOIR adjustment | Lender +2 points, safe +1 point | Small headroom increase. | my judgement |
| Good credit | Rate adjustment | Min -0.25 points, max -2 points | Modest pricing improvement. | my judgement |
| Fair credit | Score | 650 - 699 | Approval may be possible, but risk is higher. | my judgement |
| Fair credit | FOIR adjustment | Lender -5 points, safe -2 points | Less room for debt. | my judgement |
| Fair credit | Rate adjustment | Min +1 point, max +2.5 points | Wider and higher band. | my judgement |
| Weak credit | Score | 300 - 649 | High-risk profile. | my judgement |
| Weak credit | FOIR adjustment | Lender -12 points, safe -5 points | Keeps the result conservative. | my judgement |
| Weak credit | Rate adjustment | Min +3 points, max +5 points | Reflects poor pricing power. | my judgement |
| Unknown credit | Score not known | Lender FOIR -3 points, safe 0 points, min rate -0.25, max rate +2.25, confidence -12 | Unknown is not the same as bad credit, but the answer should be less certain. | challenge brief |
| Salaried stability | Current job >= 3 years | Lender +3 points, safe +2 points, lower rate band | Stable employment improves repayment visibility. | my judgement |
| Salaried instability | Current job < 1 year | Lender -8 points, safe -4 points, higher rate band | A new job has more uncertainty. | my judgement |
| Employer type | Government / PSU / large company | Lender +2 points, lower rate band | Salary continuity is easier to rely on. | my judgement |
| Business vintage | >= 5 years | Lender +3 points, safe +2 points, lower rate band | An established shop or business is less fragile. | my judgement |
| Young business | < 2 years | Lender -8 points, safe -4 points, higher rate band | Early businesses can swing sharply. | my judgement |
| Business income volatility | (high - low) / average > 45% | Lender -3 points, safe -3 points, max rate +0.8 points | Wide income range means less dependable EMI capacity. | my judgement |
| ITR available | ITR annual income > 0 | Lender +2 points, confidence +7 | Documented income helps the lender side. | my judgement |
| Informal history | >= 12 months | Lender +2 points, safe +1 point | A year of income history is better than a short patch. | my judgement |
| Short informal history | < 12 months | Lender -5 points, safe -4 points, max rate +1.5 points | Less history means less confidence. | my judgement |
| Dependents | >= 2 | Safe -3 points, lender -2 points | More household obligations leave less EMI room. | my judgement |
| Free collateral | Collateral value > 0 and unencumbered | Lender +4 points, safe +1 point, lower rate band | Collateral lowers lender loss risk, but only slightly helps borrower safety. | my judgement |
| Co-applicant support | Co-applicant income > 0 | Lender +2 points, safe +1 point, max rate -0.25 points | Helpful, but not enough to ignore the main borrower's cash flow. | my judgement |
| Emergency savings | < 1 month | Safe -6 points, confidence -8 | No shock buffer is a real warning sign. | my judgement |
| Emergency savings | 1 - 3 months | Safe -3 points, confidence -4 | Thin buffer lowers the safe EMI. | my judgement |
| Emergency savings | >= 6 months | Safe +2 points, confidence +4 | Strong buffer supports a little more flexibility. | my judgement |
| High-cost app loans | Active | Lender -6 points, safe -7 points, rate min +2, rate max +4 | Expensive short-term debt is a stress signal. | challenge brief + my judgement |
| Recent bounced EMI | Last 3 months | Lender -15 points, safe -8 points, rate min +2.5, rate max +4.5 | Recent delinquency should matter a lot. | challenge brief + my judgement |
| Age guardrail | Age < 21 or > 60 | Lender -6 points, safe -4 points, max rate +1.5 | Needs lender policy beyond this prototype. | my judgement |

## Verdict and routing

| Area | Rule | Value | Why I used it | Source |
|---|---:|---:|---|---|
| Hard stop | Recent bounced EMI plus high-cost app loans | Verdict becomes "Don't borrow" | This is the clearest debt-spiral case in the brief. | challenge brief |
| Hard stop | Existing debt >= 50% of assessed income | Verdict becomes "Don't borrow" | There is not enough headroom for another EMI. | my judgement |
| Hard stop | Cash after expenses and existing debt <= 0 | Verdict becomes "Don't borrow" | A new loan cannot be called safe if monthly cash flow is already negative. | my judgement |
| Hard stop | Age < 18 or > 70 | Verdict becomes "Don't borrow" | Outside the scope I am comfortable estimating locally. | my judgement |
| Borrow | Request fits both lender and borrower limits | Verdict becomes "Borrow" | The requested amount does not exceed the safe amount. | my judgement |
| Borrow less | Safe amount or likely sanction is below request | Verdict becomes "Borrow less" | The borrower should anchor on the lower number. | challenge brief + my judgement |
| Product routing | Business borrower with free property >= 1.5x requested amount | Recommend LAP | Ravi should not be pushed toward expensive unsecured credit when a secured option is plausible. | challenge brief |
| Product routing | Personal loan >= ₹12,00,000 with useful free property | Recommend LAP | For a large unsecured ask, it is worth comparing a secured quote. | my judgement |

## What this does not know

- It does not claim RBI approval or live lender rates.
- It does not verify salary, ITR, bank statements, employment, property title, gold value, or existing app-loan balances.
- It does not include GST on processing fee, insurance bundling, foreclosure charges, tax benefits, or floating-rate reset schedules.
- Rate bands are assumptions for this exercise, not offers.
- Unknown credit score is treated as uncertainty, not as a poor score.
- "Don't borrow" is an intentional outcome, especially with bounced EMIs, app-loan stress, or negative cash flow.
