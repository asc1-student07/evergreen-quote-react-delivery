# Risk Register

| # | Risk | Owner | Likelihood (L/M/H) | Impact (L/M/H) | Mitigation | Trigger to escalate |
|---|---|---|---|---|---|---|
| R1 | Dev server runs code the compiler would reject: app looks fine, build is broken | Delivery Lead | M | H | Run `type-check` after every assembly step, not just before merge | Type-check red at end of day → hold the push |
| R2 | Sponsor's rate values could produce an absurd premium for one coverage type | Delivery Lead | M | H | Sanity-check auto/home/life at default inputs right after editing rates | Any premium looks wrong → don't ship until resolved |
| R3 | Hook/context refactor silently changes existing behavior (e.g., duplicate saves, broken live estimate) | Delivery Lead | L | H | Confirm nothing customer-visible changed before adding new behavior on top | Any prior feature regresses → hold merge |

## How I'll use this register

Re-check at every mid-afternoon check-in and before any commit touching rates, types, or shared state. Visible to the team via the repo. Updated same-day, not retroactively.