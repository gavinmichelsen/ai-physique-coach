---
name: supplements
description: "Provides evidence-based supplement recommendations. Use when client asks about supplements or during onboarding when reviewing current supplements."
---

# Supplements

This skill provides a structured, evidence-based approach to supplement recommendations, prioritizing fundamentals over marketing claims.

## Philosophy

- **Supplemental Only:** Emphasize that supplements cannot replace a solid diet, consistent training, and adequate sleep.
- **Evidence-Based:** Only recommend supplements with strong or moderate scientific backing.
- **Cost-Effective:** Redirect clients away from expensive, ineffective products (e.g., fat burners, BCAAs).

## Supplement Tiers

### Tier 1: Strong Evidence (Recommend to Most)
- **Creatine Monohydrate:** 3-5g daily. Supports strength and recovery.
- **Protein Powder:** Situational tool to hit protein targets.
- **Vitamin D:** 1,000-2,000 IU daily, especially for those with limited sun exposure.
- **Caffeine:** 3-6mg/kg pre-workout for performance benefits.

### Tier 2: Moderate Evidence (Situational)
- **Omega-3:** 1-2g EPA/DHA if fish intake is low.
- **Magnesium:** For sleep and general health if dietary intake is low.
- **Melatonin:** 0.5-2mg for short-term sleep onset issues.

### Tier 3: Weak/No Evidence (Do Not Recommend)
- BCAAs, Testosterone Boosters, Fat Burners, Proprietary Blends.

## Workflow

1.  **Identify Need:** Trigger when a client asks about supplements or during the onboarding review.
2.  **Assess Current Use:** Review what the client is already taking.
3.  **Provide Recommendations:** Use the format in `templates/supplement_recommendations.md`.
4.  **Educate:** Explain *why* certain supplements are recommended and why others are not.
5.  **Research New Items:** If a client asks about a supplement not listed, use a web search to find current evidence before providing an assessment.

## Resources

- `templates/supplement_recommendations.md`: Standardized format for presenting evidence-based supplement advice.
