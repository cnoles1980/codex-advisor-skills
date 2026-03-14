# Codex Advisor Skills

Opinionated Codex skills for product strategy, PRD critique, monetization decisions, startup judgment, and product-specific advisory workflows.

These skills are built for people who want more than generic brainstorming. They are designed to push on assumptions, clarify tradeoffs, and produce practical next-step recommendations.

## Who This Is For

This repo is useful if you use Codex for:

- product planning and roadmap decisions
- feature and PRD review
- pricing and monetization strategy
- startup idea evaluation
- portfolio-specific product advisory work

## Included Skills

### `product-manager-advisor`

Broad PM judgment for:

- planning
- prioritization
- feature tradeoffs
- launch readiness
- roadmap decisions
- AI-product critique

### `product-spec-critic`

Focused review for:

- PRDs
- feature specs
- launch briefs
- implementation proposals

Designed to find ambiguity, missing requirements, edge cases, rollout gaps, and handoff risk.

### `pricing-monetization-advisor`

Use this when the main question is:

- should this be monetized at all
- who should pay
- what belongs in free vs paid
- what pricing model to test first
- whether the product is really software, service, data, or intelligence

### `ycombinator-business-advisor`

YC-style startup judgment for:

- startup ideas
- founder-market fit
- wedge strategy
- distribution realism
- venture-scale potential

### `ai-matrix-map-advisor`

A product-specific advisor for AI Matrix Map.

This one is intentionally specialized. It focuses on:

- market-map product strategy
- taxonomy quality
- source trust and freshness
- editorial workflows
- premium intelligence layers
- roadmap and monetization decisions

## Repo Structure

```text
skills/
  product-manager-advisor/
  product-spec-critic/
  pricing-monetization-advisor/
  ycombinator-business-advisor/
  ai-matrix-map-advisor/
```

Each skill contains:

- `SKILL.md` with trigger metadata and instructions
- `agents/openai.yaml` for UI-facing metadata
- optional `references/` files for deeper guidance

## Installation

Copy one or more skill folders into your Codex local skills directory:

```text
$CODEX_HOME/skills/local/
```

Then invoke them explicitly in a prompt with `$skill-name`.

## Example Prompts

```text
Use $product-manager-advisor to evaluate this feature idea and tell me what to build next, what to cut, and how we would measure success.
```

```text
Use $product-spec-critic to review this PRD and tell me what is missing, risky, or underspecified before engineering starts.
```

```text
Use $pricing-monetization-advisor to tell me whether this product should be monetized, who should pay, and what pricing model to test first.
```

```text
Use $ycombinator-business-advisor to evaluate whether this is a real startup idea or just an interesting project, and tell me what the wedge should be.
```

```text
Use $ai-matrix-map-advisor to evaluate AI Matrix Map and recommend what belongs in the public map, what belongs in a premium layer, and what not to build yet.
```

## Design Philosophy

These skills are intentionally:

- skeptical
- practical
- concise
- decision-oriented
- willing to say "do not build this yet"

They are not designed to be soft, generic, or endlessly accommodating.

## Customizing

You can use this repo as-is or as a template:

- copy a skill and adapt its `description` to change trigger behavior
- add `references/` files for product- or company-specific context
- keep general-purpose skills general, and isolate specialized context into dedicated skills

That pattern is used here on purpose: most skills are broadly reusable, while `ai-matrix-map-advisor` is intentionally specific.

## License

[MIT](LICENSE)
