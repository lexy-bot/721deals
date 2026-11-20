# 721 Deals — Background AI: Signup Assistant + Item Scanner

**Status:** SPEC ONLY (2026-11-20). Not built yet. Human approval before anything goes live.
**Rule:** The AI prepares, checks, and drafts. A human (platform admin, then the store) approves.
The AI never approves a store, never publishes a listing, never releases money,
never decides a dispute, and never changes bank details on its own.

## 1. Signup Assistant (background)

What the store does: opens WhatsApp / the signup form, answers in plain language,
takes a photo of their government ID or passport, and a selfie at in-person signup.

What the AI does in the background:
1. Reads the form answers and fills the store profile draft (name, categories,
   address, hours, WhatsApp, pickup address, delivery zones).
2. Checks the ID photo: is it a government ID or passport, is it readable,
   does the name match the form, is it expired? Flags blur / glare / mismatch.
3. Checks the business fields against what was given: COCI number format,
   CRIB number format, business licence present or marked "applying".
4. Individual-seller tier: if no licence yet, labels the account INDIVIDUAL,
   applies the caps (10 listings, $500 total sales, 60 days to show licence),
   and sets the deadline reminder.
5. Runs the prohibited-items and duplicate check: is this store already signed
   up under another name / phone / address?
6. Produces a one-page verification summary for the admin: green / amber / red
   per field, with the exact problem quoted. Admin approves or rejects in one tap.

What the AI NEVER does: approve a store, reject a store, or override an admin.
In-person signup stays in-person: the AI checks the photo, a human sights the
original ID at signup (owner, or store manager with the owner's name on file).

## 2. Item Scanner (background)

What the store does: takes 2 photos per item (front + back, or front + label),
or a photo of the shelf tag for was-price proof.

What the AI does in the background:
1. Names the item from the photos (e.g. "Men's cotton T-shirt, navy").
2. Suggests category (clothes / shoes / toys / gadgets), size(s) visible on the
   label, colour(s) (max 3), and condition (new / overstock / open-box).
3. Reads the price tag / label in the photo: brand, size, was-price.
4. Drafts the listing: title, short description, flash price suggestion
   (store's cost + minimum 20% off proven was-price, never below the floor),
   was-price ONLY if proof is in the photo (dated tag, receipt, or prior listing).
   No proof = no was-price shown.
5. Counts stock per size x colour from the photos the store took, and flags
   "sold out" sizes as greyed out, never buyable.
6. Flags risks: brand looks counterfeit, safety mark missing on toys/gadgets,
   photo is a stock image not the real item, was-price looks inflated vs the
   tag in the photo, price above the proven was-price or below the cost floor.
7. Sends the draft back to the store on WhatsApp: "Check this, edit the price,
   tap Approve." Only after the store approves does it go to the admin queue;
   only after admin approves does it go live.

What the AI NEVER does: publish a listing, set a final price, show a was-price
without proof, or approve a flagged item.

## 3. What the AI also runs in the background

- Pickup reminders: buyer booked pickup, AI sends the QR + last-4 reminder,
  and nudges the store if pickup is unconfirmed after the window.
- Money-hold clock: counts 48h after confirmed pickup, then queues the payout
  for admin release; new stores: 7-day hold + 10% rolling reserve, first 10 sales.
- Dispute triage: reads the buyer's message + photo, sorts it (wrong size /
  damaged / not as described / never picked up), drafts a reply for the admin,
  never decides the refund itself.
- Dead-stock watch: flags any listing priced like full retail, any was-price
  with no proof, any flash discount under 20% or over 50% without cost proof.

## 4. Human gates (never automated)

- Store approval: admin only.
- Listing publish: store approves draft, then admin approves.
- Money release: admin releases after the 48h clock; bank changes need the
  owner in person.
- Dispute decision: admin only, 48h report / 72h decision.
- Suspension / removal: admin only, warning-first ladder.

## 5. Build order (split, Lovable, batched)

1. Item scanner draft flow first (photo -> draft -> store approve) — highest value.
2. Signup assistant second (form + ID check -> admin summary).
3. Hold clock + reminders third.
4. Dispute triage last.
One Lovable message per step, after the step before it works live. No Lovable
message is sent for this spec alone.
