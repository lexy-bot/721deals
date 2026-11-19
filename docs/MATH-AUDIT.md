# SXMDeals — Math Audit, Corrected
Date: 2026-11-18, 5-pass re-run, before any build
Rule: every figure re-checked from inputs with exec. Unverified assumptions labelled.

## GAPS / ERRORS FOUND — and fixed

### 1. BIGGEST ERROR: Pro is NOT always cheaper than Starter
Earlier presentation implied Pro (6% cut) always beats Starter (10% cut). Wrong — Pro's higher subscription eats the cut saving until sales are high.
- Starter cost = $100 + 10% of sales
- Pro 3mo cost = $195 + 6% of sales → break-even $2,375/mo sales
- Pro 6mo cost = $175 + 6% of sales → break-even $1,875/mo sales
- Pro 12mo cost = $150 + 6% of sales → break-even $1,250/mo sales
Examples:
- $500 sales: Starter $150, Pro 6mo $205, Pro 12mo $180 — Starter wins by $30-$55
- $1,000 sales: Starter $200, Pro 6mo $235, Pro 12mo $210 — Starter wins by $10-$35
- $2,000 sales: Starter $300, Pro 6mo $295 (saves $5), Pro 12mo $270 (saves $30)
- $3,000 sales: Starter $400, Pro 6mo $355 (saves $45), Pro 12mo $330 (saves $70)
FIX: Sell Starter first. Pro only after a store proves >$1,250/mo (12mo) / >$1,875/mo (6mo) / >$2,375/mo (3mo).

### 2. Stripe fee on combined checkout — double-counted in earlier delivery research
Earlier: "$1.50 delivery keep, Stripe $0.45 on $5, leaves $1.05" — that treats delivery as a separate card charge. In real checkout, buyer pays ONE total, Stripe charges once on the total.
Corrected (US card, 2.9% + $0.30, proportional split):
- $50 item + $5 delivery = $55 total, Stripe $1.90 total, delivery share $0.17, SXMDeals delivery net $1.33 (not $1.05)
- $50 + $8 = $58, Stripe $1.98, delivery share $0.27, net $1.23 (not $0.97)
- $100 + $12 = $112, Stripe $3.55, delivery share $0.38, net $1.62 (not $1.35)
- $100 + $15 = $115, Stripe $3.63, delivery share $0.47, net $2.03 (not $1.77)
- $150 + $15 = $165, Stripe $5.08, delivery share $0.46, net $2.04
Store net changes only $0.02-$0.04 vs item-only fee, but delivery net was understated by $0.26-$0.28. FIXED in tables below.

### 3. International cards — earlier examples used US card only
SXM buyers include tourists / international cards. Fee is 4.4% + $0.30, FX 5.4% + $0.30, not 2.9% + $0.30.
- $100: US $3.20, INT $4.70, FX $5.70 — difference $1.50 / $2.50
- $50: US $1.75, INT $2.50, FX $3.00
- Store net $100 Starter: US $86.80, INT $85.30, FX $84.30
- Store net $100 Pro: US $90.80, INT $89.30, FX $88.30
FIX: Quote US net AND international net. Do not promise $86.80 to a store if the buyer used a foreign card.

### 4. Rider $0.14/km cost — unverified assumption, labelled now
Fuel is verified: XCG 2.853/L = $1.59/L, scooter 2.5 L/100km = $0.04/km.
The other $0.10/km (tyres/oil/maintenance/insurance) is a planning estimate, NO SXM quote found.
- Solo $3.50, 20km: fuel-only net $2.70, $5.40/hr — still below min wage $6.11/hr
- Solo $3.50, 20km: full-cost net $0.70, $1.40/hr
Conclusion stands either way: $3.50 solo fails. But the $1.40/hr figure depends on the unverified $0.14/km. FIX: show both.

### 5. Rider batched $27.90/hr is best-case, not guaranteed
3 drops Zone 2, $30 revenue, $2.10 cost, $27.90 net in 60 min — assumes zero waiting, zero bridge delay, zero no-show, 15km loop total.
- With +30 min bridge delay (Simpson Bay Bridge, 7 openings/day, 20-40 min cost): $27.90 / 1.5h = $18.60/hr — still above min wage, but lower.
- Zone 1 batched 3x $6.50 = $19.50, cost $2.10, net $17.40/hr best-case.
FIX: Quote best-case AND bridge-delay case. Do not promise $27.90/hr.

### 6. TOT 5% — missing from ALL profit math
No earlier table included Turnover Tax. If TOT applies:
- $100 subscription: $5.00
- $175 subscription: $8.75
- $10 cut on $100: $0.50
- Delivery keep $1.50-$2.50: $0.08-$0.13
Whether TOT applies to subscription vs cut vs delivery fee is UNVERIFIED — lawyer/accountant must confirm. FIX: No net-profit figure is final until TOT is confirmed. Do not quote SXMDeals profit net of TOT.

### 7. Wise payout fee / time — unknown, cannot quote
Stripe payout is 2 business days (standard, free). Wise to SXM bank (WIB/RBC/Republic) fee and time was NOT found. Do not quote a payout date to a store beyond "weekly payout after 48h dispute window, Stripe 2 days + Wise transfer time TBD".

### 8. Founder $5 self-delivery net overstated
$5 delivery, $1.50 to SXMDeals, $3.50 to rider — if founder delivers, rider is $0, but fuel is real.
- 10km: fuel $0.40, net keep $1.10 (not $1.50)
- 30km batch loop, 3 drops: fuel $1.20, $0.40/drop, net $1.10/drop
FIXED.

### 9. Chargeback win still costs $15
- Accept, no contest: $100 + $15 = $115
- Contest and WIN: $100 + $15 = $115 (counter $15 refunded, standard $15 not)
- Contest and LOSE: $100 + $15 + $15 = $130
Earlier tables only showed the lose case. FIX: show all three.

### 10. Reserve is held, not lost
10% rolling reserve: $10 on $100, $5 on $50 — held 14 days, then released if no dispute. Earlier tables did not show the return. FIX: reserve = delayed cash, not a fee.

## CORRECTED TABLES

### Store net, item only, US card
- $50 Starter 10%: $50 - $1.75 - $5.00 = $43.25
- $100 Starter 10%: $100 - $3.20 - $10.00 = $86.80
- $100 Pro 6%: $100 - $3.20 - $6.00 = $90.80
- $150 Pro 6%: $150 - $4.65 - $9.00 = $136.35
International: subtract $1.50 per $100 ($0.75 per $50) from the above.

### Combined checkout, US card
- $50 + $5 delivery = $55 buyer pays, Stripe $1.90, store $43.27, SXMDeals delivery net $1.33, rider $3.50
- $50 + $8 delivery = $58, Stripe $1.98, store $43.29, SXMDeals net $1.23, rider $6.50
- $100 + $12 delivery = $112, Stripe $3.55, store $86.83 (Starter) / $90.83 (Pro), SXMDeals net $1.62, rider $10.00
- $150 + $15 delivery = $165, Stripe $5.08, store $136.38 (Pro), SXMDeals net $2.04, rider $12.50

### Subscription totals (verified)
- Starter: $100/mo, $1,200/yr
- Pro 3mo: $195 x 3 = $585
- Pro 6mo: $175 x 6 = $1,050
- Pro 12mo: $150 x 12 = $1,800
- User's original ladder: $450/3mo = $150/mo if total, $1,350 if per-month; $350 x 6 = $2,100; $250 x 12 = $3,000 — inversion stands, $150/mo cheaper than $250/mo if $450 is a total.

### Delivery zones (corrected)
- Pickup: $0
- Zone 1 <5km: $8 — rider $6.50, SXMDeals $1.50 gross / $1.23 net
- Zone 2 5-12km: $12 — rider $10.00, SXMDeals $2.00 gross / $1.62 net
- Zone 3 far/French: $15 — rider $12.50, SXMDeals $2.50 gross / $2.03 net
- Heavy >5kg: +$5
- Minimum $50 for delivery. $5 flat ONLY for founder self-delivery or batched flash windows, 3-4 drops/run.

### Rider pay check
- SXM min wage: XCG 10.93/hr / 1.79 = $6.11/hr
- Solo $3.50: $1.40/hr full-cost, $5.40/hr fuel-only — FAILS both
- Batched 3 Zone 2: $27.90/hr best-case, $18.60/hr with bridge delay — PASSES
- Batched 3 Zone 1: $17.40/hr best-case — PASSES

## What is still unverified — do not build on these
- TOT treatment (subscription / cut / delivery)
- Wise payout fee/time to SXM banks
- $0.10/km scooter maintenance component
- Rider insurance / SZV / gig classification in SXM
- Stripe descriptor / public name fix for new SXMDeals account (browser task running 2026-11-18 20:17 AST)
- Lawyer sign-off on holding buyer money, liability cap, CBCS flag
