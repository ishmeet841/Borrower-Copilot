# Demo run-throughs

I used these three profiles as regression cases while building. The numbers below come from `src/lib/calculations.ts` and the demo inputs in `src/data/demoProfiles.ts`.

## Priya

### Answers used

| Question | Answer |
|---|---|
| Loan purpose | Wedding expenses |
| Amount requested | ₹8,00,000 |
| Loan type | Personal loan |
| Income type | Salaried |
| Net monthly income | ₹1,10,000 |
| Age | 29 |
| Existing monthly EMIs | ₹14,000 car loan |
| Monthly household expenses | ₹48,000, including rent and regular household spend |
| Credit score | Known, 780 |
| Years in current job | 5 |
| Employer type | Large company / MNC |
| Variable pay share | 8% |
| Emergency savings | 4 months |
| Recent bounced EMI | No |
| High-cost app loans | No |
| Upcoming large expenses beyond this loan | ₹0 |

### Outputs

| Output | Result |
|---|---|
| O1 verdict | Borrow |
| O2 likely lender sanction | ₹8,00,000 on this request; lender eligibility estimate ₹21,35,000 |
| O2 safe borrower amount | ₹8,00,000 on this request; safe eligibility estimate ₹11,70,000 |
| O3 fair rate and APR | 9.6% - 16.3% headline rate; 10.0% - 17.7% all-in APR including 1% - 3% processing fee |
| O4 safe EMI ceiling | ₹27,850 per month |

### Tenure and stress

| Tenure | Requested EMI | Recommended EMI | Interest on recommended amount |
|---|---:|---:|---:|
| 3 years | ₹26,926 | ₹26,926 | ₹1,69,346 |
| 5 years | ₹18,172 | ₹18,172 | ₹2,90,306 |
| 7 years | ₹14,521 | ₹14,521 | ₹4,19,762 |

Stress read: if the rate is 2 percentage points higher, EMI is about ₹19,000. If income falls 20%, safe EMI headroom falls to about ₹14,592. That is why I would tell Priya not to increase the loan just because a lender offers more.

### Negotiation Card summary

| Card field | Summary |
|---|---|
| Purpose and requested amount | Wedding expenses, ₹8,00,000 |
| Recommended product | Personal loan |
| Safe borrowing amount | ₹8,00,000 |
| Safe EMI limit | ₹27,850 |
| Fair interest range | 9.6% - 16.3% |
| All-in APR | 10.0% - 17.7% |
| Why this is fair | Her credit score, large-company salary, and manageable existing EMI support the personal-loan band. |

## Ravi

### Answers used

| Question | Answer |
|---|---|
| Loan purpose | Second stock line and delivery vehicle |
| Amount requested | ₹15,00,000 |
| Loan type | Business/MSME loan |
| Income type | Self-employed |
| Net monthly income | ₹60,000 midpoint input |
| Age | 42 |
| Existing monthly EMIs | ₹0 |
| Monthly household expenses | ₹34,000 |
| Credit score | I don't know |
| Years in business | 14 |
| Lower monthly income month | ₹40,000 |
| Higher monthly income month | ₹80,000 |
| ITR annual income | ₹4,20,000 |
| Unencumbered property available | Yes |
| Property collateral value | ₹45,00,000 |
| Co-applicant income | ₹18,000 per month |
| Expected monthly income lift | ₹7,000 |
| Emergency savings | 2 months |
| Recent bounced EMI | No |
| High-cost app loans | No |

### Outputs

| Output | Result |
|---|---|
| O1 verdict | Borrow less |
| O2 likely lender sanction | ₹15,00,000 on this request; lender eligibility estimate ₹19,50,000 |
| O2 safe borrower amount | ₹9,80,000 |
| O3 fair rate and APR | 8.6% - 16.4% headline rate; 8.8% - 16.9% all-in APR including 0.75% - 1.5% processing fee |
| O4 safe EMI ceiling | ₹18,676 per month |

### Tenure and stress

| Tenure | Requested EMI | Recommended EMI | Interest on recommended amount |
|---|---:|---:|---:|
| 3 years | ₹50,180 | ₹32,785 | ₹2,00,244 |
| 5 years | ₹33,747 | ₹22,048 | ₹3,42,879 |
| 7 years | ₹26,882 | ₹17,563 | ₹4,95,276 |

Stress read: at rate +2%, EMI on the recommended amount is about ₹18,637, just inside the safe ceiling. If income falls 20%, safe EMI headroom falls to about ₹9,453. My read is that he should phase the expansion instead of taking the full ₹15,00,000 now.

### Negotiation Card summary

| Card field | Summary |
|---|---|
| Purpose and requested amount | Second stock line and delivery vehicle, ₹15,00,000 |
| Recommended product | Loan Against Property |
| Safe borrowing amount | ₹9,80,000 |
| Safe EMI limit | ₹18,676 |
| Fair interest range | 8.6% - 16.4% |
| All-in APR | 8.8% - 16.9% |
| Why this is fair | The shop property and business vintage support LAP pricing, but household cash flow does not safely support the full requested EMI. |
| Warning | Compare secured and unsecured quotes before pledging property. |

## Anita

### Answers used

| Question | Answer |
|---|---|
| Loan purpose | Electric scooter for delivery work |
| Amount requested | ₹1,50,000 |
| Loan type | Two-wheeler/EV loan |
| Income type | Informal |
| Net monthly income | ₹28,000 midpoint input |
| Age | 35 |
| Existing monthly EMIs | ₹3,500 formal monthly EMI |
| Monthly household expenses | ₹23,000 |
| Credit score | I don't know |
| Lower monthly income month | ₹26,000 |
| Higher monthly income month | ₹30,000 |
| Months income has been steady | 10 |
| Dependents | 2 children |
| Emergency savings | 0 months |
| High-cost app loans | Yes |
| Outstanding app loan balance | ₹35,000 |
| Monthly app-loan outflow | ₹6,000 |
| Recent bounced EMI | Yes, last month |
| Expected monthly income lift | ₹4,500 |
| Down payment available | ₹10,000 |

### Outputs

| Output | Result |
|---|---|
| O1 verdict | Don't borrow |
| O2 likely lender sanction | ₹0 responsible sanction in this self-assessment |
| O2 safe borrower amount | ₹0 |
| O3 fair rate and APR | 15.3% - 31.3% headline range if she sought new credit despite stress; 16.0% - 33.6% all-in APR including 1% - 3% processing fee |
| O4 safe EMI ceiling | ₹0 per month |

### Tenure and stress

| Tenure | Requested EMI | Recommended EMI | Interest on recommended amount |
|---|---:|---:|---:|
| 3 years | ₹5,826 | ₹0 | ₹0 |
| 5 years | ₹4,250 | ₹0 | ₹0 |
| 7 years | ₹3,631 | ₹0 | ₹0 |

Stress read: the stress test fails before adding a new loan because current cash flow is already strained. Rate +2% would put the requested EV-loan EMI near ₹5,984 on a 3-year comparison, while safe EMI remains ₹0.

### Negotiation Card summary

| Card field | Summary |
|---|---|
| Purpose and requested amount | Electric scooter for delivery work, ₹1,50,000 |
| Recommended product | No new loan now |
| Safe borrowing amount | ₹0 |
| Safe EMI limit | ₹0 |
| Fair interest range | Not useful until current repayment stress is repaired; modelled stressed range is 15.3% - 31.3% |
| All-in APR | 16.0% - 33.6% |
| Why this is fair | The bounced EMI and high-cost app loans mean a new quote would price distress more than productive use. |
| Warning | Clear or restructure app loans first, build at least one month of emergency savings, then reassess after two clean repayment cycles. |
