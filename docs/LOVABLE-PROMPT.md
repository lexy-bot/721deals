# 721 Deals — Lovable prompt

721 Deals, 721deals.com. SXM marketplace: stores sell overstock at flash prices, pickup + delivery. VioTech Global LLC. Clothes first. Colours: ink #0F2A2E, teal #00A896, coral #FF5A3C, sun #FFC300, paper #FFF8E7. Logo: wide banner, 721 Deals.com, capital D, file media-generation-721deals-logo-banner-capital-d-0-362c04fc-04bc-4edf-8306-12b89818c6e2.webp.

VioTechBuild: Apply to this site/PWA/app.

GOAL: Human art-directed, premium, brand-specific. Not AI/SaaS/shadcn/template. Not quirky/messy.

FIRST, NO CODE: If existing — audit routes/components/content/assets/type/color/spacing/layout/motion/deps. List strengths, AI signals, brand signals, constraints, top fixes, risks. If new — skip audit. Then test 3 directions for brand fit/usability/a11y/mobile/perf/complexity, pick 1, explain, build incrementally: system first (type/color/spacing/nav/buttons), then top screen/page, then rest.

REMOVE unless brand-justified: purple/blue/neon gradients, glass/frost, blobs, glow/blur, rounded-2xl/3xl everywhere, identical 3-col cards, icon-in-circle/Lucide grids, centered hero by default, gradient text, excess pills/shadows/hover-scale/scroll-fade, bento grids, repeated sections, generic copy (Transform/Unlock/Future of), fake stats/testimonials/logos/reviews, AI imagery.

BUILD: Type as identity — max 2 families, display/body/UI roles, strong scale contrast. Editorial hierarchy, deliberate asymmetry on a grid, varied composition (split/offset/full-bleed/narrow width/rules), restrained color (1 primary + neutrals + 1 accent + semantic), fewer stronger components (editorial rows/numbered/split panels/lists/callouts, not card-for-everything), real brand imagery with intentional crop/ratio, purposeful motion only.

PRESERVE: Meaning, IA, routes, facts, SEO, conversions, backend/APIs/auth/DB/payments/analytics/integrations. No fabrication. No new deps/second system. Reuse primitives.

MOBILE/A11Y: Design mobile intentionally, not stacked desktop. Verify all routes at desktop/tablet/mobile/narrow: type, order, crops, touch, overflow. Preserve/improve contrast, semantics, headings, keyboard/focus, labels, alt, reduced-motion.

VERIFY: Substitution test (swap name/logo — must NOT still fit), Removal test (decor with no meaning/hierarchy/use = delete), Specificity/Consistency tests, Adversarial review (is this just a new AI trend? fix). Iterate to diminishing returns.

DELIVER: AI signals found, changes, preserved, design system, responsive/a11y check, limits.

---
## Phase 1 — build in order
Exception: bright bento layout stays, Caribbean Punch above. Real photos only.

1. Store dashboard, phone-first: photo front+back, name, category, size, colour, was-price proof, flash price, stock per size×colour. Start/stop flash, 1 tap.
2. Browse/search (search matches sizes), real flash timer to next 12–2pm / 7–9pm, price auto-reverts. No fake timer.
3. Stripe Checkout, variable total only. Acct acct_1UdadxLFhV5bSAOe, 721 Deals, 721deals.com, 721DEALS, weekly Monday USD, Radar Lite, 3DS. Never touch Long Strokes acct_1UNUpJHMK0V0giuH. Money "held at Stripe until pickup/delivery confirmation" — never "escrow"/"insurance".
4. QR + last-4, server-signed, single-use: first scan wins, second = ALREADY COLLECTED. QR alone never opens, last-4 alone never opens, need QR + last-4 + order code. Expires 48h. Buyer taps Received. Release after 48h.
5. PWA push opt-in, 2/day max, ~11:45am / ~6:45pm, followers only.
6. Delivery: Pickup $0, Zone 1 $8, Zone 2 $12, Zone 3 $15, heavy +$5, $50 min, free >$150 Zone 1–2. Delivery PIN random, NOT last-4, expires 2h, door photo + GPS.
7. Admin: first 3 listings/store manual approve, dispute 48h report / 72h decision, weekly payout statement.

Pricing: Starter $100/mo +10%, Pro $195/$175/$150 (3/6/12mo) +6%. Sell Starter first — Pro cheaper only above $1,250 (12mo) / $1,875 (6mo) / $2,375 (3mo). $100 sale: Starter $86.80 US / $85.30 intl, Pro $90.80 / $89.30. TOT 5% unverified.
Hold: 48h after pickup. New stores first 10 sales: 7-day hold + 10% reserve 14 days. 2 disputes pause flash, 3 = removal.
Boxes: Kids $50/8/≥$100, Mens $75/10/≥$150, Womens $75/10/≥$150, XL $100/10/≥$200. 1/customer/flash/store. No return for dislike.
DFY: $75/10, $150/20, $375/50. Waived Pro 12mo only, half Pro 6mo, never Starter.
IN: clothes, shoes, toys, EN/ES/FR + language check-in at start (choose language before deals, remembered), WhatsApp reserve 587-1698, sold-out greyed not hidden, stock per size×colour, 30-min reserve, first paid wins. All Tech B.V. ONBOARD — founding store #1, live, not sample, the ONE gadgets exception in v1 (TVs, phones, cameras, printers, cases, Starlink, used/refurbished — condition/serial checked). Jewellery flash still OUT v1, other gadgets OUT v1.
OUT: games front page, jewellery/gadgets flash v1, cross-border v1, warehouse, referral trees, cash prizes, fake was-prices, fake Verified badges.
Backend: Lovable + Supabase (Postgres, Edge Functions, Realtime, cron). Stripe webhooks → paid → confirmed → payable → paid out. Keys server-side only. Never automate disputes, chargebacks, bank changes, suspensions, tax.
Audit 5×, math shown, verify live on phone after every publish, 100/100 only.
