---
name: kcas-research
description: Research layer for the Knowledge Capital Allocation System. Use when Codex needs to identify, compare, rank, and explain high-quality assets through knowledge capital, compounding potential, asset quality, opportunity ranking, sector landscapes, and long-term research merit. Supports single asset research, pairwise comparisons, multi-asset rankings, and sector research for public companies, private companies, startups, AI businesses, SaaS companies, acquisitions, digital products, creator businesses, personal brands, real estate projects, and other cash-generating assets. Does not perform portfolio construction, position sizing, or allocation recommendations.
---

# KCAS Research

## Purpose

Use this skill to identify, compare, rank, and explain assets through the lens of Knowledge Capital. The goal is to answer:

```text
What are the highest-quality assets, and why?
```

KCAS Research sits above KCAS Core. It does not replace the core evaluation engine and does not perform portfolio construction.

## Relationship To KCAS Core

Reuse KCAS Core whenever possible. In this workspace, KCAS Core is the `knowledge-capital-investing` skill.

KCAS Research must reuse these KCAS Core outputs:

- Asset Quality Score
- Investment Attractiveness Score
- Final Allocation Score
- Knowledge Capital Analysis
- Compounding Potential
- Reflexivity Analysis

Do not duplicate KCAS Core scoring logic. For each asset, first obtain or reconstruct a KCAS Core evaluation, then use this skill to synthesize, compare, rank, and explain the research conclusions.

If KCAS Core results are missing:

1. Run or emulate KCAS Core evaluation for each asset using the core framework.
2. Clearly label scores as preliminary if current evidence is incomplete.
3. Continue to the research-layer rankings only after the core fields above are present.

## Critical Rules

- Do not recommend portfolio allocations.
- Do not recommend position sizing.
- Focus on understanding assets, not constructing portfolios.
- Prioritize knowledge capital.
- Prioritize compounding.
- Reward durability.
- Explicitly identify the hardest asset to replicate.
- Explain why an asset deserves long-term attention.
- Never predict short-term prices.
- Never guarantee returns.
- Distinguish facts, interpretations, and assumptions.
- Use current evidence when current valuation, market sentiment, capital flow, or ranking depends on timely data.

## Primary Use Cases

- Single Asset Research: NVIDIA, Palantir, Micron, Anthropic, Stripe.
- Comparative Research: NVIDIA vs Micron, Palantir vs Snowflake, Anthropic vs OpenAI, CRM vs NOW.
- Sector Research: Best AI infrastructure assets, best knowledge capital businesses, top enterprise software compounders, top creator economy assets.

## Output Mode Selection

Choose the mode based on the user request:

- `Mode A: Deep Research Report` for one asset.
- `Mode B: Comparison Report` for two to five named assets.
- `Mode C: Ranking Report` for a list of assets or "rank these" requests.
- `Mode D: Sector Landscape Report` for broad sector discovery or "best assets in X" requests.

Read `references/research-modes.md` for detailed structures when producing full reports. Read `references/templates.md` when the user wants reusable prompts or blank templates.

## Required Research-Layer Outputs

Beyond KCAS Core, include these outputs whenever relevant:

### Knowledge Capital Ranking

Rank assets by:

- Knowledge Capital Score
- Moat Durability
- Replicability Difficulty

Output a numbered ranking with concise reasoning.

### Compounding Ranking

Rank assets by:

- Revenue Compounding
- Profit Compounding
- Learning Loop Strength
- Capital Allocation Quality

Classify each as `Exceptional`, `Strong`, `Moderate`, or `Weak`.

### Asset Quality Ranking

Rank all compared assets as:

- `Top Tier`
- `High Quality`
- `Average`
- `Weak`

### Opportunity Ranking

Answer:

```text
If an investor could own only one of these assets for 10 years, which would it be?
```

Provide reasoning. This is a research conclusion, not a portfolio allocation or position-sizing recommendation.

### Research Conclusion

Always answer:

- What makes this asset special?
- What could destroy the thesis?
- What evidence matters most?

## Standard Workflow

1. Parse asset set, asset type, sector, geography, and research mode.
2. Gather user-provided evidence first; supplement with current sources when needed and available.
3. For every asset, obtain KCAS Core outputs: Asset Quality, Investment Attractiveness, Final Allocation, Knowledge Capital, Compounding Potential, and Reflexivity.
4. Normalize evidence quality across assets; flag missing data and avoid false precision.
5. Produce research-layer rankings and explanations.
6. End with the appropriate Research Conclusion for the selected output mode.

## Boundaries

KCAS Research may say an asset deserves deeper research, long-term attention, or ranks above alternatives by quality. It must not tell the user what percentage of a portfolio to allocate, how large a position to take, or how to construct a portfolio.
