# Evergreen Quote: Vision Brief

## Product
**Name:** Evergreen Insurance Quote (Phase 2 React rebuild)

**Delivery week:** 2

**Delivery Lead:** Marc Gagne

**Engineering team (represented by):** https://github.com/asc1-student07/evergreen-quote-react-delivery

**GitHub Project board:** https://github.com/users/asc1-student07/projects/2

## Who is the customer?
A first-time insurance shopper — often a new renter or new homeowner who was
told they "need insurance" and wants a fast, no-commitment number on their
phone. They aren't loyal to a carrier yet, and today their alternative is a
competitor's site (or ours) that asks for a dozen fields and an email before
showing a single dollar figure. If we make them wait or sign up, they leave.

## What pain does Evergreen Quote removes?
Phase 1 shipped a static page with a "Calculate" button — you filled in
fields, clicked, and waited for a number. Phase 2 removes even that friction:
the estimated premium updates live as the visitor types, with no button press
and no account. The pain we're removing isn't just speed — it's the moment of
doubt where a shopper wonders "is this going to make me sign up before I even
see a price?"

## What does "good" look like at end of the week?
- The live estimate updates correctly for auto, home, and life coverage as a visitor types.
- The Recent Quotes panel loads from the real data feed, with a visible loading state and a visible error state if the feed fails.
- A visitor can save their own quote and see it appear at the top of the list instantly.
- `npm run type-check` and `npm run build` both pass — the compiler's contracts hold.
- The work is merged to `main` via a reviewed PR with a green CI run.

## What are we explicitly NOT doing this week?
- No real rate engine or actuarial pricing — the rate model is a placeholder the sponsor sets.
- No customer accounts, persistent storage, or email capture.
- No payment, checkout, or policy purchase flow.
- No real back-end service — the JSON data feed stands in for the quotes API.
- No routing, no automated test suite, no production deployment.

## How will we know if it worked?
- CI is green on the merge commit into `main` (type-check + production build).
- All three visible data states (loading / error / success) are demonstrable in the browser, not just "handled" in code.
- A stranger can hear the delivery goal once and repeat it back accurately.