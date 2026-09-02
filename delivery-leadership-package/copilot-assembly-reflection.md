# Copilot Assembly Reflection: Liberty Mutual Style Pass

**Date:** 9/2/2026
**Author:** Marc Gagne
**Lab step:** Copilot-assisted assembly task (customized from provided example)

## Context

I used Copilot for a UI assembly step: match Liberty Mutual visual styling in the existing React quote app. The work was iterative and specific: apply the style using the same CSS mechanism already in place, tune color and typography toward the requested Liberty Mutual sections, keep original app copy when requested, and convert Recent Quotes into a yellow callout-card treatment.

## What Copilot produced in this session

- Updated global style tokens and component-class styling in `src/index.css`.
- Tuned headings, labels, spacing, and color contrast through multiple micro-passes.
- Restored original hero text values after an unintended copy edit.
- Reworked `Recent quotes` into a yellow side-card style, then refined it using screenshot feedback.

## Critique (~100 words)

Copilot got the iteration loop right: it made fast, targeted style updates and incorporated feedback quickly. It also got important things wrong that forced clarifications: first pass was too subtle, one pass changed text values when the request was style-only, and initial Liberty Mutual matching was not close enough until screenshot-guided tuning. I would not ship the early passes as-is, but I would ship the final pass after quick visual QA in-browser. Process improvement: explicitly lock copy and scope to styling-only before editing. Because this task’s final implementation touched presentation (primarily CSS), TypeScript contract checks were not the main risk surface for this specific change.
