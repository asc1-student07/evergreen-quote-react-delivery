# Decision Memo: Fix the bug now vs. keep moving

**Date:** 9/1/2026
**Author:**  Marc Gagne
**Decision area:** Day 2 — the blank coverage-type labels in Recent Quotes

## Context

Type-check flagged a real bug: `RecentQuotes.tsx` was reading a property that doesn't exist on the `Quote` type, which is why the coverage-type labels were showing up blank. Premiums still displayed fine though, so on the surface the app looked totally normal. I had to decide whether to have the team stop and fix it right away or keep pushing through the rest of Day 2's assembly and circle back later.

## Options considered

1. **Have it fixed right now, before moving on to anything else.** Takes a few minutes, but it's a one-line fix and the cause is already known.
2. **Log it, keep the team moving on assembly, fix it before wrapping for the day.** Keeps momentum on the rest of Day 2 (config, rates), but means running the rest of the day with a known error sitting there, and there's a real chance it slips through the cracks if something else comes up.
3. **Leave it for later in the week since the premiums still worked.** Fastest in the moment, but it ships a visible bug (blank labels) and leaves a red type-check sitting on the branch — which is basically the exact "looks fine but isn't" trap I'm supposed to be watching for as lead.

## Recommendation

Option 1: get it fixed now.

## Why

It's a one-liner and the fix is already known — there's no version of this where waiting actually saves time. Letting a compiler error sit around, even for a few hours, isn't a habit worth building on this team. The whole point of catching stuff like this early is catching it early, not carrying it forward and hoping nothing else breaks before we circle back.

## What would change my mind

If the fix had actually been complicated, like new logic, not a one-liner, I'd have logged it as a tracked issue and kept the team moving, instead of letting an open-ended fix eat into the rest of the day. We did end up creating a project task, but that was just for record keeping.