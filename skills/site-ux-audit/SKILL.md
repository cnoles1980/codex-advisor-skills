---
name: site-ux-audit
description: Audit a live website or web app by testing safe user flows, interactive elements, forms, navigation, accessibility basics, responsive behavior, and loading, empty, success, and error states. Produce evidence-backed UX findings and prioritized product recommendations. Use when asked to evaluate a website, web app, onboarding flow, landing page, or product experience.
---

# Site UX Audit

## Mission

Inspect a website or web app as a careful first-time user and product partner. Test the experience that is actually reachable, record what happens, and turn observed friction into specific, prioritized recommendations.

Do not treat a visual preview, source file, or confident assumption as proof that a user flow works. Verify the result at the surface where a user would experience it.

## Safety and permission boundaries

Operate read-only by default.

- Never purchase, delete, publish, send a message, submit a real application, change account settings, or alter production data without explicit approval for that exact action.
- Do not guess credentials, bypass authentication, or store, echo, or include secrets in the report.
- Ask before entering private or sensitive data. Use clearly fictional test data when possible.
- Treat payment, email, signup, upload, account creation, destructive controls, and external submissions as approval gates.
- If a required surface is inaccessible, report the blocker and continue with safe public or local checks where possible.

## Inputs

Establish these before testing:

1. Target URL, local development URL, or app surface.
2. Whether the target is public, authenticated, staging, or production.
3. The primary user or business goal, if known.
4. Any credentials, test account, device, browser, viewport, or feature scope the user has explicitly supplied.
5. Whether the user wants a quick pass, a complete reachable-surface audit, or a focused flow review.

If the user does not specify a scope, default to a public, read-only audit of the homepage, primary navigation, primary call to action, and the most obvious user journey. State that scope before beginning.

## Audit procedure

### 1. Map the experience

Record the starting URL, visible navigation, calls to action, major sections, and reachable pages. Identify the most likely first-time-user goal and the shortest path to it.

Create a coverage list of:

- Pages and routes visited.
- Primary navigation items.
- Buttons, links, menus, tabs, accordions, filters, and other interactive elements.
- Forms and fields.
- Important states such as loading, empty, success, validation error, server error, and unavailable content.
- Responsive or device surfaces included in the scope.

### 2. Test the core journey first

Walk the primary path as a first-time user. At each step, record:

- What the user is trying to do.
- What the interface appears to invite them to do.
- What action was taken.
- What actually happened.
- Whether the next step was obvious.
- Whether the result was confirmed at the correct surface.

Test the happy path before exploring edge cases, so a blocked core journey is visible early.

### 3. Test safe interactions

Test every reachable, safe interactive element within the agreed scope. Do not blindly click controls that could create external side effects.

For each element, check:

- Is the label understandable and the target easy to identify?
- Does it respond to the expected click, tap, keyboard, or focus action?
- Does it lead to the destination or state the label implies?
- Is feedback immediate and clear?
- Does the back button, refresh, deep link, and return path behave sensibly?
- Are disabled, loading, empty, and failure states understandable?

When the same component appears repeatedly, test representative instances plus any instance with different content, permissions, or state. Disclose this sampling rather than claiming every identical instance was tested.

### 4. Check basic accessibility and responsive behavior

Within the available tools and scope, check:

- Keyboard reachability and visible focus.
- Logical focus order.
- Form labels, error association, and accessible names for controls.
- Whether icon-only buttons explain their purpose.
- Text readability, contrast concerns, and content that is clipped or obscured.
- Narrow viewport behavior, horizontal overflow, touch target crowding, and persistent overlays.

Report these as observed checks or limitations, not as a formal compliance certification.

### 5. Separate findings from opportunities

Classify each result as one of:

- **Broken:** the expected action fails or produces an incorrect result.
- **Confusing:** the action works, but the user is likely to hesitate, misunderstand, or lose confidence.
- **Missing:** a needed state, explanation, recovery path, or affordance is absent.
- **Opportunity:** the current experience works, but a change could improve activation, retention, trust, or efficiency.

Do not present an inferred business hypothesis as a confirmed user problem. Label assumptions and explain what evidence would validate them.

### 6. Rank and recommend

For each finding, provide:

- Location or URL.
- User goal and action taken.
- Expected result versus actual result.
- Evidence, such as a screenshot, visible text, URL, console output, or reproduction path.
- Category and severity.
- User impact.
- Recommended change.
- Confidence and any limitation.

Use the report template in `references/audit-report-template.md`. Use the severity definitions in `references/heuristics.md`.

Prioritize recommendations by user impact, confidence, and implementation effort. Start with the smallest change that removes a meaningful point of friction, then identify deeper product opportunities separately.

## Output contract

Return a concise executive summary followed by:

1. Scope, environment, and coverage.
2. Core journey result.
3. Prioritized findings.
4. Product and UX opportunities.
5. Evidence appendix with reproduction paths.
6. Untested surfaces, permission gates, and remaining uncertainty.

Never say “everything works,” “all buttons were tested,” or “the site is ready” unless the coverage and evidence support that exact claim.
