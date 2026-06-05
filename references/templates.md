# KCAS Research Templates

## Single Asset Prompt

```markdown
Use $kcas-research to produce a Deep Research Report on [Asset].
Reuse KCAS Core outputs where possible.
Focus on knowledge capital, compounding potential, reflexivity, and why this asset deserves long-term attention.
Do not recommend portfolio allocation or position sizing.
```

## Comparison Prompt

```markdown
Use $kcas-research to compare [Asset A] vs [Asset B].
Rank them by knowledge capital, compounding potential, asset quality, and 10-year opportunity.
Reuse KCAS Core outputs where possible.
Do not recommend position sizing.
```

## Ranking Prompt

```markdown
Use $kcas-research to rank these assets:
- [Asset 1]
- [Asset 2]
- [Asset 3]

Rank by Knowledge Capital, Compounding Potential, Asset Quality, and 10-year Opportunity.
Explain what makes the top asset special, what could destroy the thesis, and what evidence matters most.
```

## Sector Landscape Prompt

```markdown
Use $kcas-research to produce a Sector Landscape Report for [Sector].
Identify the highest-quality assets through Knowledge Capital, Compounding Potential, and Reflexivity.
Include a shortlist, ranking, research gaps, and the hardest assets to replicate.
Do not recommend portfolio allocation or position sizing.
```

## Asset Research Input

```json
{
  "mode": "Deep Research Report",
  "assets": ["Example Asset"],
  "asset_type": "public company",
  "research_question": "What makes this asset special, and does it deserve long-term attention?",
  "must_reuse_kcas_core": true,
  "constraints": [
    "Do not recommend portfolio allocation",
    "Do not recommend position sizing",
    "Prioritize knowledge capital",
    "Prioritize compounding",
    "Identify hardest asset to replicate"
  ]
}
```

## Ranking Fields

Use these fields when comparing assets:

```markdown
| Asset | Asset Quality | Investment Attractiveness | Final Allocation | Knowledge Capital | Moat Durability | Replicability Difficulty | Compounding | Reflexivity | Research Tier |
|---|---:|---:|---:|---:|---|---|---|---:|---|
```
