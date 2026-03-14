---
name: product-spec-critic
description: Critical review skill for PRDs, feature specs, product plans, launch briefs, feature requests, wireframe notes, and implementation proposals. Use when Codex should pressure-test a product spec for ambiguity, missing requirements, edge cases, metrics, sequencing, UX risk, technical handoff quality, or launch-readiness gaps.
---

# Product Spec Critic

Use this skill to find what a spec leaves unsaid. Optimize for clearer decisions, safer implementation handoff, and fewer avoidable surprises during build and launch.

## Review Workflow

1. Identify the user, problem, desired behavior, and product goal.
2. Separate what the spec defines from what it implies.
3. Look for ambiguity, omissions, edge cases, and contradictions.
4. Check whether success metrics, rollout logic, and non-goals are explicit.
5. Evaluate whether engineering, design, and product would make the same interpretation.
6. Return findings first, then proposed fixes.

## What To Check

Always inspect for:

- unclear user or target segment
- weak problem statement
- vague feature behavior
- missing scope boundaries
- missing non-goals
- edge cases and failure states
- permissions, trust, privacy, or abuse concerns
- data dependencies and source-of-truth confusion
- missing instrumentation or launch metrics
- rollout, fallback, and support implications
- handoff gaps likely to cause engineering rework

## Output Shape

Lead with findings, ordered by severity.

For each finding, include:

- issue
- why it matters
- what should be added or changed

After findings, include:

- open questions
- assumptions you made
- revised spec outline, if useful

If the spec is strong, say so explicitly and then name any remaining risks or testing gaps.

## Critique Rules

- Do not praise a spec into false confidence.
- Prefer precise criticism over broad "needs more detail" feedback.
- Focus on product risk, behavioral ambiguity, and launch risk.
- Call out when a spec is good for a prototype but not for production.
- Distinguish missing decisions from missing writing.
- Recommend the smallest clarifying additions that materially reduce confusion.
