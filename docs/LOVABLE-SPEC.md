# 721 Deals — Lovable Phase 1 Spec
**Paste-ready spec for Lovable, after the demo. Do NOT build in Lovable until Phase 0 passes.**
**Brand:** 721 Deals — 721deals.com — **Domain registered 2026-11-19, Order #12629782, $11.81, expires 2027-11-19, Porkbun VioTechGlobal.**
**Owner:** VioTech Global LLC (Wyoming, Single-member LLC, 30 N Gould St Ste N, Sheridan WY 82801). **CEO: Alesco Elvio Violenes.**
**VioTechBuild prompt (locked 2026-10-23):** Human art-directed, premium, brand-specific, not AI/SaaS template. Audit-first, remove generic AI defaults, type-as-identity, preserve IA/SEO/function/backend, mobile/a11y + substitution/adversarial tests. No purple/blue/neon gradients, glass/frost, blobs/glow, rounded-2xl everywhere, identical 3-col cards, icon-in-circle grids, centered hero by default, gradient text, excess pills/shadows, generic copy, fake stats/reviews, AI imagery. **Exception for this site only (CEO 2026-11-19): bright bento Amazon-style layout is the design — keep it, recoloured to Caribbean Punch below.**
**Real photos only — CEO hard line, no AI imagery. Reuse real retail photos from demo.**

## 1. What it is
Online marketplace in Sint Maarten connecting local stores to buyers to sell overstock and clearance inventory at discounted flash-sale prices, with in-store pickup and local delivery. Stores pay a monthly subscription and a percentage commission per sale; buyers pay the platform and stores are paid weekly after pickup or delivery is confirmed. Platform is ONLY the middleman — it does not sell stock itself or hold inventory in v1.

## 2. Phase 0 gate — MUST pass before Lovable build
- 3 founding clothing stores in writing (LOI + verification, see §6)
- 1 WhatsApp flash test, Sat 12–2pm, 20 items, announced Fri on Facebook/WhatsApp
- Bar: 15–20 reservations, ≥10 paid pickups. If it fails, it is a demand problem, not a website problem. Do not build Phase 1 until it passes.
- Stripe account activated (see §5), lawyer/accountant 1-hour check done (TOT, holding money, CBCS flag, games law).

## 3. Phase 1 scope — IN
- Landing + store directory + buyer browse/search/filter (search must match sizes, not just name/store/category)
- Store dashboard, phone-first: big buttons, photo upload front+back, name, category, size, colour, was-price proof, flash price, stock per size × colour, one button to start/stop a flash. Usable in ~2 minutes in-shop.
- Cart, reserve on WhatsApp (587-1698, no account/card first), Stripe Checkout (variable total, NOT fixed payment links)
- Flash timer: real countdown to next 12–2pm or 7–9pm window, price auto-reverts after. Never a fake/resetting timer.
- QR + last-4 pickup (§7) — server-signed, single-use, anti-reuse enforced server-side
- Delivery zone picker in cart (§8)
- EN / ES / FR toggle, PLUS language check-in at the very beginning of the page (visitor picks language before deals, choice remembered, whole page switches)
- All Tech B.V. is the ONE gadgets exception in v1 (see §18) — jewellery flash still OUT, other gadgets OUT.
- Size filter, sold-out sizes greyed out not hidden, not buyable. "Continue selling when out of stock" OFF always.
- Mystery boxes (§9), Done-for-you vs self-serve (§10)
- PWA push: opt-in only, 2 pushes/day max, at flash windows (alert ~11:45am and ~6:45pm), to opted-in followers of that store/category only. Never hourly.
- Admin approval: first 3 listings per store manually approved. Admin can pause a store/flash.
- Weekly payout statements (gross, Stripe fee, cut, refunds, net), separate ledger from Long Strokes.
- Weekly reconciliation: Stripe vs ledger vs Wise, mismatch >$0.01 blocks that store's payout.

## 4. Phase 1 scope — OUT (do NOT build)
- Games on the front page. No Spin, Scratch, Hunt, check-in/coins live until SXM prize/lottery law sign-off. Keep code out, not hidden.
- Jewellery flash in v1 is OUT. Gadgets flash in v1 is OUT — except All Tech B.V., the one onboard gadgets store (§18). Clothes first, then shoes, toys. Jewellery/gadgets need receipt/serial, 7-day authenticity check — Phase 2 for other stores.
- Cross-border shipping in v1. SXM pickup only. Phase 2: Island Courier, $100 min, $25 flat, free over $150, customs on buyer.
- Warehouse / consignment. Phase 3 only, after 50+ stores.
- Referral trees / invite-to-unlock, farm games, cash prizes, transferable credit. Never.
- No fake "was" price, no fake Verified badge, no demo store names presented as live partners. All sample data must be labelled SAMPLE.

## 5. Stripe — account already created, DO NOT create another
- **New separate account: SXMDeals, acct_1UdadxLFhV5bSAOe, US, test/sandbox until activation submitted and approved.**
- Public name: **721 Deals**, website: **721deals.com**, statement descriptor: **721DEALS**
- Category: Other merchandise (Retail) — Stripe has no Marketplace category.
- Payouts: **Weekly on Monday, USD**. Radar Lite (Included) on, 3D Secure on for high-risk, payouts manual/weekly not instant/daily.
- **Do NOT touch the other accounts:** SXM Turnovers acct_1UU31dE0EK4xv3Va, Long Strokes acct_1UNUpJHMK0V0giuH (public name Long Strokes Deep Cleaning — viewed only, never rename).
- **Before checkout goes live:** CEO clicks "Agree and submit" on the Review page himself; connect bank/payout account when Stripe asks; confirm Radar/3DS; create subscription products below.
- **Products to create after activation:** Starter $100/mo, Pro 3mo $195/mo ($585), Pro 6mo $175/mo ($1,050), Pro 12mo $150/mo ($1,800). Cut is NOT a Stripe product — deducted at payout.
- **Fees (US card 2.9%+$0.30 = $3.20 on $100; international 4.4%+$0.30 = $4.70; FX 5.4%+$0.30 = $5.70). Chargeback $15, +$15 if contested and lost = $30 total if lost.**
- **Held-funds wording, everywhere, never "escrow" / "insurance":** "held at Stripe until pickup/delivery confirmation"
- Stripe MCP connector is reauthorization_required — do not rely on it; use Stripe Dashboard / webhooks.

## 6. Pricing — sell Starter first
- **Starter $100/mo + 10% cut. Pro $195/mo (3mo) / $175/mo (6mo) / $150/mo (12mo) + 6% cut.**
- **Pro is NOT always cheaper. Break-even vs Starter: Pro 3mo $2,375/mo sales, Pro 6mo $1,875/mo, Pro 12mo $1,250/mo.** At $500 sales Starter $150 total vs Pro 6mo $205 / 12mo $180. At $1,000 Starter $200 vs Pro 6mo $235 / 12mo $210. Sell Starter first.
- Founding offer: 30 days free, 10% cut only, then Starter/Pro.
- **Store nets, US card, item only (math 5-pass checked):** $50 Starter $43.25, $100 Starter $86.80, $100 Pro $90.80, $150 Pro $136.35. International: subtract $1.50 per $100 ($100 Starter INT $85.30, Pro INT $89.30).
- **TOT 5% is NOT in the net projections — lawyer/accountant must confirm treatment before launch. Do not present a gross figure as money in hand.**
- Projections (avg order $60, blended cut 8.8%, costs bags $0.40/order + WhatsApp $0.06/order + Meta $150/mo, before TOT, before founder time): 3×20 $495/mo, 3×40 $785/mo, 10×20 $2,002/mo, 10×40 $2,966/mo, 10×60 $3,930/mo, 20×40 $6,081/mo, 20×60 $8,009/mo, 30×60 $12,088/mo. After TOT 5% on platform revenue: 10×40 $2,801/mo, 20×40 $5,751/mo.

## 7. Security-first — protection from the jump (CEO directive 2026-11-18)
- Verify every store before listing: COCI + CRIB + licence + owner ID + bank name match + physical visit + storefront photo, first 3 listings manual, re-verify annually/on change.
- Buyer never pays store directly. Buyer pays platform Stripe, money held at Stripe, released only after pickup/delivery confirmed + 48h dispute window.
- **Hold: 48h after confirmed pickup. New stores (first 10 sales): 7-day hold + 10% rolling reserve 14 days, then graduate to 48h. Bank change: 3-day hold.**
- Dispute: **48h report with photo, 72h decision. 2 disputes pause flash, 3 = removal.** Seller pays seller faults, platform pays transit faults.
- Payouts weekly with statement. Separate ledger from Long Strokes. Chargeback budget 1–3% refunds.
- Performance: warn at >2% defect in 60 days, suspend at 5%, pause flash if refunds >5% in 30 days. Do NOT copy Amazon 1% at SXM volume.
- Terms: "not the seller / not a party" clause, seller indemnity, liability cap set by SXM lawyer, mediation first, short report window. No "insurance" / "escrow" wording without lawyer sign-off.

## 8. QR + last-4 pickup — ANTI-REUSE IS THE CORE
- **After paid purchase only, platform (and only platform) generates 1 QR per order, server-signed in Phase 1. Demo front-end QR is NOT secure — do not present it as live-secure.**
- QR holds order code, store, exact packages (item names, sizes, colours, quantities, mystery-box contents). QR holds order code/items/last-4 only, never full phone/name/card.
- **Single-use, first scan wins. Once scanned + handover confirmed, mark COLLECTED, deactivate QR, pass shows USED. Second scan — same store, different clerk, different device, screenshot — shows ALREADY COLLECTED in red, gives nothing, no money release.**
- **QR alone never opens an order. Last-4 alone never opens an order. Clerk needs all three: QR scan + buyer says last 4 digits + order code matches.**
- QR expires 48h after pickup window. Late pickup: flag after 48h, hold 1 more day, then refund + re-list (rule on order message before checkout).
- Buyer taps Received after handover. Money releases after 48h dispute window.
- Dead-phone fallback: clerk types order code + last-4 + buyer name, system checks all three (+ WhatsApp check to 587-1698 or ID). Never last-4 alone.
- Clerk offline: printed daily pickup list fallback, mark collected manually, reconcile same day.
- Delivery: rider scans same QR at door, buyer gives last-4 verbally. Delivery scan alone never releases money — needs tap Received + door photo with GPS.
- Privacy: never print price, store name, or fake "worth $X" on bag/QR sticker.

## 9. Delivery — $5 flat FAILS for hired riders
- **Pickup $0 default. Zone 1 <5km $8 (rider $6.50 / platform $1.50). Zone 2 5–12km $12 (rider $10.00 / platform $2.00). Zone 3 far/French $15 (rider $12.50 / platform $2.50). Heavy >5kg +$5. Minimum $50 for delivery. Free delivery only over $150, Zone 1–2, batched only.**
- $5 flat ONLY for founder self-delivery or batched flash windows (3–4 drops/run, same zone), labelled as launch batched delivery. Founder does first 20–30 self-deliveries.
- Why: $3.50/drop solo = $1.40/hr (cost $2.80 on 20km round trip at $0.14/km), fuel-only $5.40/hr — both below SXM min wage $6.11/hr (XCG 10.93/hr). Batched 3 drops = $8.40/hr.
- Delivery handover: prepaid, no cash to rider; sealed bag + order code photo at pickup; **random 4-digit PIN for delivery (NOT phone last-4)**, single-use, expires 2h; photo at door with house number + GPS/timestamp; buyer taps Received; PIN+photo+confirmation = release; auto-release if PIN+photo present and no dispute in 48h.
- Rider faults: steals/damages/never arrives → money stays held, buyer refunded, rider suspended after 1 confirmed case, removed after 2, rider liability capped at order value. Buyer no-show: wait 5 min, photo, return to store, refund minus delivery fee or free re-delivery next batch, 2 no-shows = pickup-only.
- Rider onboarding: ID/licence/scooter registration/insurance/phone/bank, same for all.

## 10. Mystery boxes — defined purchase, NOT chance
- Kids **$50 / 8 items / was-value ≥$100**. Mens **$75 / 10 / ≥$150**. Womens **$75 / 10 / ≥$150**. XL Large Adult **$100 / 10 / ≥$200**. Was-value floor exactly 2.0× price.
- **1 box per customer per flash per store.** Buyer chooses ONLY Kids/Mens/Womens/XL; store picks contents in-store; no cherry-picking.
- Mix disclosed before sale, same for every buyer in batch. Size ranges: Kids 2T–16, Mens S–XL, Womens XS–XL, XL Adult 1X–3X. One size per box, no mixed-size box.
- New overstock only, tags on where possible, no used/damaged/stained. **NO return for dislike/style/colour/"didn't like the surprise" (bold before checkout).** Exchange ONLY for wrong size (same box another size, in stock, in-store only), defective/damaged item, or total was-value below guaranteed floor (refund shortfall or replace to floor). Unopened box return within 48h, sealed only.
- Money held at Stripe until pickup confirmed, buyer opens/confirms count+size at pickup, photo of sealed box + order code at handover, 48h dispute window for wrong size/defect/floor breach only. 2 confirmed box disputes = pause box sales, 3 = removal.
- Kids boxes: no adult items, no small-parts/choking-hazard toys, no child models in photos (flat-lay/hanger only). XL: never put XL stock in Mens/Womens box as filler.
- Box assembly needs backend-generated pick list, not memory. Do NOT ship boxes cross-border in v1.

## 11. Done-for-you vs self-serve + founder picker
- Self-serve $0, store runs dashboard, first 3 listings admin-approved.
- **DFY flat per visit: $75 for 10 items, $150 for 20, $375 for 50 — all $7.50/item.** Includes 1 visit, photos front+back (2/item), name, category, size, colour, was-price proof, flash price, per-size stock, size chart, upload, live check with owner, 1 correction round. Excludes restocking, re-photographing sold items, jewellery/gadget serial verification (separate $25/item).
- **Waiver: DFY waived for Pro 12-month sign-up only, half-price ($75) for Pro 6-month; NEVER waive for Starter.** Cap: 1 store/day, 20 items max per visit; over 20 = second visit at same rate.
- Picker fields in order: Photo (front+back, min 2, 1200×1200 min, <500KB, real photos only) → Name (human types, no AI naming) → Category dropdown (Mens/Womens/Kids/Shoes/Toys/Gadgets/Jewellery; jewellery/gadgets gated) → Size dropdown per category → Colour multi-select max 3 → Pieces per size (number per size, NOT one total) → Colours left (count per colour, must sum to total pieces) → Deadstock count left (auto = sum of per-size stock, editable only with a reason) → Was price (proof photo of tag/price list required) → Flash price → Save/Publish (first 3 admin-approved).
- Variant rule: stock per **size × colour**, variant SKU e.g. TEE-BLK-M, max 3 options/product; box/bundle stock = bottleneck component; sold-out size greyed out, not hidden, not buyable; reserve stock on checkout (30-min hold), decrement on payment not add-to-cart; first paid wins on last unit, second gets auto-refund + alternative size offer; immutable stock ledger, corrections as new entries.

## 12. Colours — Caribbean Punch (LOCKED 2026-11-19)
- Deep sea ink **#0F2A2E**, teal **#00A896** (brightened vivid teal in logo), coral **#FF5A3C**, sun yellow **#FFC300**, warm paper **#FFF8E7**.
- Psychology: teal = trust + Caribbean sea (main colour, header/buttons/links). Coral = urgency (big deal prices, % OFF badges, countdown digits ONLY, never small body text — coral on white 3.1:1). Deeper coral **#C93A1E (~5:1 on white)** for small text where red was used. Sun yellow = attention/optimism (flash banner, flash pills ONLY). Ink = authority/premium (white on ink 15.1:1). Warm paper = warm human market background.
- Do NOT add lime/violet/pink (Shein/Temu look). Do NOT use Amazon orange/navy. Closest match found in research is Sahela (small brand, not a giant, not in SXM) — stay as is, no tweak decided.
- Logo: wide one-line banner, **721 Deals.com capital D**, 721 once only in red/white/blue on wing, Deals.com bold black, pelican big in tag, wing inside tag, Saint Martin island on chest with black outline only, middle see-through teal, no lightning, no large 721 DEALS text. File: `media-generation-721deals-logo-banner-capital-d-0-362c04fc-04bc-4edf-8306-12b89818c6e2.webp`. Landing page uses tall Version B (721deals.com inside tag). Social set: square (profiles), wide banner v2 (covers), tall story v2 (TikTok/IG Stories), circle v2.
- **Logo cache lesson: never reuse the same logo filename on a swap — use a new filename every time, or phones serve the cached old logo.**

## 13. Backend — Lovable + Supabase (Phase 1)
- Frontend PWA, backend Lovable + Supabase (Postgres + Edge Functions + Realtime + cron) for stores/listings/orders/subscriptions/push subscriptions/ledger.
- Stripe webhooks → Edge Function → state machine (paid → confirmed → payable → paid out). Server cron for flash scheduler, order expiry, payout job, dispute timer, rider dispatch.
- VAPID keys in vault, never in browser/chat/repo. WhatsApp Cloud API keys server-side only. Muse cannot run 24/7 — backend must run the loop, Muse monitors via crons 30–60 min.
- Server-signed QR generator (Phase 1, not demo). Push subscription store. Email sender. Audit log.
- **Never automate:** dispute decisions, chargeback contests, bank changes, store suspension, TOT/tax filings, lawyer questions. Human rota, 72h SLA, auto-refund from held funds if no decision.
- Messaging failure rule: log, retry once after 15 min, fall back push → WhatsApp → email, then flag human. Never silently drop PIN, dispute notice, or payout statement.
- Math automation: lock tier on order not payout time, idempotency on every payment mutation, name-match before every payout.

## 14. WhatsApp / PWA push — what is real
- WhatsApp Business App (free, 587-1698): manual only, broadcast 256, only people who saved the number receive it. wa.me links free, good for v1 reserve.
- **Do NOT migrate 587-1698 to Cloud API until coexistence is confirmed for that number — test on a test number first. One-way-door warning: migrating may make it unusable on the App ever again. Registering 587-1698 is CEO-only tap.**
- WhatsApp Cloud API direct: Meta Business Account + verification (1–5 days), WABA, phone verified, HTTPS webhook. System User permanent token. Rates SXM (+1721) indicative only: Marketing $0.0604/msg, Utility $0.0077 — re-check in WhatsApp Manager before budgeting. New portfolio 250 unique people/24h, then 2,000 / 10,000 / 100,000 / unlimited. Templates Meta-approved (24–48h). Per-user marketing cap, error 131049.
- **Hourly alerts FAIL on both channels — corrected to 2/day max (see §3).**
- PWA push: HTTPS + manifest + service worker + Push API. iOS 16.4+ only, and only if PWA added to Home Screen. Android Chrome/Firefox/Samsung Internet. Permission: ask after install/intent, never on first pageview. Self-hosted via FCM/APNs $0. OneSignal Free up to 1,000 MAU.
- **2026-01-15 rule: general-purpose AI assistants banned from WhatsApp Business Platform; business-specific transactional automation is permitted. Muse orchestrates transactional flows, not an open-ended chatbot on WhatsApp.**

## 15. Bags
- Start: plain black poly mailer + vinyl sticker ~$0.36–$0.45/bag, platform pays in v1 out of its cut, do NOT charge stores per bag in v1. Sizes: Medium 10×13", Large 14×18" gusseted. TVs not bagged.
- Bag front: wordmark, 721deals.com, WhatsApp 587-1698, "Dead stock. Real discounts. Pickup today." White box for QR + order code + last-4, applied by clerk at sealing. "Sealed by 721 Deals — do not open until pickup is confirmed. If this seal is broken, tell the clerk before you pay / before you leave." Do NOT print price, store name, or fake "worth $X".
- **Check TEATT/Customs before a 5,000-unit import (SXM plastic ban / Plastic Free SXM law).** No bag order placed yet.

## 16. Marketing — Phase 0 gate first
- **No Meta ads until flash test passes. Then Meta $5/day = $150/mo, WhatsApp-messages objective only; kill any ad set after $35 spent if cost per WhatsApp conversation >$5 or 0 reservations.**
- Audiences: locals (Cole Bay/Simpson Bay/Philipsburg), parents (Kids box $50), tourists Front Street, sneakerheads, Pelican Key hosts via Brenda Wathey. Buyer pool ~32,500 (not 44,000).
- Cadence: 5 Facebook posts/week (Lexy Voice Overs, cross-posts to Instagram), WhatsApp broadcast flash days only, flash windows 12–2pm and 7–9pm.
- Metrics per flash: 20+ reservations, ≥15 paid pickups, ≥75% pickup rate, ≤$5 cost/reservation, ≤$7 per paid pickup, <2% disputes.

## 17. Tax — general info, NOT tax advice
- Wyoming: no state corporate/personal income tax; $60/year annual report.
- US federal: single-member LLC disregarded, income flows to owner; non-resident owner pays no US federal income tax on profit from work done outside US with no US office/staff, **but must still file Form 5472 with pro forma Form 1120 every year, due April 15, $25,000 penalty for not filing.**
- SXM: TOT **5%** on goods/services sold in SXM, filed monthly, due by 15th of following month, applies on turnover even at a loss; profit tax **34.5%** on net taxable / SXM-source profit; Chamber + Belastingdienst registration, TOT registration if turnover expected > ANG 30,000/year. Personal income tax for SXM resident progressive 12.5%–47.5%.
- Disclosure: yes — Stripe, Wise, banks and SXM Tax Administration will ask where money comes from. Separate 721 Deals ledger, weekly payout statements, separation of subscription vs commission money.
- **Get a SXM accountant + US CPA for the 5472 filing before taking money in.**

## 18. Open decisions / gaps — do NOT invent answers in Lovable
- Cut rate: Starter 10% / Pro 6% recommended, NOT locked.
- Pro ladder: $195 / $175 / $150, Starter $100 — NOT formally approved as final.
- $175 Pro push feature as redefined (§3) — approve?
- Tagline: demo shows "721 DEALS TAKES THE CAKE" — not explicitly locked as 721 Deals tagline.
- Clothing as locked first category? (Asked, not confirmed in writing.)
- Store-names: demo uses Van Dorp / Boolchand's / Manrique / Kay's — NOT verified partners, must be SAMPLE or swapped to researched list (Top1Toys, Music Man, Klass, Tech Hub, Crocs, OVERSTOCKS, Michael Kors, Joe's, Shiva's, DK Gems).
- All Tech Electronics B.V., Walter Nisbeth Rd #99, +1 721 522 4884 / +1 721 587 8842 — **ONBOARD 2026-11-19, founding store #1, live partner, NOT sample.** TVs, security cameras, printers, phone cases, Starlink, used/refurbished phones.
- Repo: no 721deals repo yet. Legacy GitHub lexy-bot works via `~/workspace/custom-connectors/custom.legacy-github/bin/gh-api` — MCP connector shows not_connected, do not use it.
- Unverified: social handles for 721 Deals, FAC/local bank merchant quote, WhatsApp SXM rate in WhatsApp Manager, WATI live USD price, Wise payout fee/time to SXM banks, SXM lottery/prize law, .sx registry availability.

## 19. What to build first in Lovable (in order)
1. Store dashboard + listing picker (§11) — founder can onboard a store in one visit
2. Buyer browse + flash timer + WhatsApp reserve
3. Stripe Checkout + held-funds state machine + weekly payout
4. QR + last-4 pickup, server-signed, single-use (§8)
5. PWA push opt-in + 2/day flash alerts
6. Delivery zones + rider PIN flow (§9)
7. Admin approval + dispute queue + reconciliation

## 20. Audit rule for every Lovable build
- Run the math five times, show it before it reaches the CEO. Find gaps/errors, run audit test, deliver only at 100/100.
- No live browser render was run by the demo builder — verify live before presenting as final. Same rule in Lovable: verify live, on phone, after every publish.
- Prices on listings stay EXACT (Zephlon rule applies by analogy — appraisal prices exact, and here flash prices exact, no rounding in build).
- Keep prompts credit-minimal: shortest prompt that lands the change, no essays; rounded numbers wherever possible.
