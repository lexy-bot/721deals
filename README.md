# 721 Deals

SXM overstock / flash-sale marketplace — 721deals.com
VioTech Global LLC (Wyoming). Owner: Alesco Elvio Violenes.

Local stores sell overstock and clearance inventory at discounted flash-sale prices, with in-store pickup and local delivery. Platform is only the middleman — subscription + commission, no inventory held in v1.

## Status (2026-11-19)
- Domain: 721deals.com, registered 2026-11-19, Order #12629782, $11.81, expires 2027-11-19
- Stripe: new separate account acct_1UdadxLFhV5bSAOe, 721 Deals / 721deals.com / 721DEALS, weekly Monday payouts USD, test mode until activation submitted
- Founding store #1 onboard: All Tech Electronics B.V., Walter Nisbeth Rd #99, Pondfill — LIVE PARTNER, not sample
- Phase 0 gate: 3 founding stores in writing + 1 WhatsApp flash test, Sat 12–2pm, 20 items, bar 15–20 reservations / ≥10 paid pickups
- Demo: artifact sxmdeals-demo-page (721 Deals Demo Page) — Caribbean Punch palette, capital-D banner logo, QR + last-4 single-use pickup, EN/ES/FR language check-in

## Docs
- `docs/LOVABLE-PROMPT.md` — paste-ready Lovable prompt (VioTechBuild, minimum words)
- `docs/LOVABLE-SPEC.md` — full Phase 1 spec (pricing, security, QR anti-reuse, delivery, boxes, DFY, backend)
- `docs/MATH-AUDIT.md` — 5-pass math audit
- `docs/MARKETING-PLAN.md` — marketing plan

## Rules
- Security-first: money held at Stripe until pickup/delivery confirmed, never "escrow"/"insurance"
- QR + last-4: single-use, first scan wins, second scan = ALREADY COLLECTED, QR alone never opens, last-4 alone never opens
- Sell Starter first: $100/mo +10%; Pro $195/$175/$150 +6%, cheaper only above $1,250/$1,875/$2,375/mo sales
- Real photos only, no AI imagery
- No secrets in this repo — no EIN, no gov ID, no API keys, no Stripe keys

## Logo tags — floating / animated (transparent PNG, no white background)
- assets/logo-721deals.webp — header/footer banner, 721 Deals.com capital D
- assets/logo-tag-teal.png — teal tag #00A896
- assets/logo-tag-coral.png — coral tag #FF5A3C
- assets/logo-tag-sun.png — sun yellow tag #FFC300
- assets/logo-tag-ink.png — ink tag #0F2A2E, teal pelican
Welcome page: the tags float in and out of the open space, fading in and out, cycling teal → coral → sun → ink. Respect prefers-reduced-motion.
Languages: 6 — English, Español, Français, Kreyòl Ayisyen, Papiamento, Nederlands, each with its flag.
