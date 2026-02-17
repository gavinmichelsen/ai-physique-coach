---
name: meal-photo-estimator
description: "Primary meal logging method. Analyzes food photos or text descriptions to estimate calories and macros. This is how ALL client nutrition is tracked — no external apps (MyFitnessPal, MacroFactor, etc.) are used. Clients simply send a photo or text message describing what they ate."
---

# AI Meal Logger

This is the primary and only method for tracking client nutrition. Clients do NOT use external tracking apps. Instead, they send:
- A **photo** of their meal, or
- A **text description** (e.g., "I just had a Fairlife protein shake" or "16oz NY strip with rice and broccoli")

The coach estimates calories and macros, maintains a running daily total, and logs everything to the client's tracker.

## Preferred Method: Text-Based Calculation

When the client provides ingredients with gram weights, this is the most credit-efficient approach:

1. **Use Python directly** to calculate macros from USDA/label data. No subtask or browser needed.
2. Look up calories, protein, fat, and carbs per 100g for each ingredient (or use label data per serving if a branded product).
3. Multiply by the client's portion size.
4. Sum totals and report back.
5. Keep a running daily total if multiple meals are logged in the same day.

## Photo-Based Workflow

1.  **Receive Photo:** Confirm it's clear enough for analysis.
2.  **Identify Items:** List all visible food items.
3.  **Estimate Portions:** Use visual cues to estimate quantity.
4.  **Calculate Macros:** Use standard nutritional data.
5.  **Present Breakdown:** Use the format in `templates/photo_estimation_template.md`.
6.  **Flag Hidden Calories:** Ask about cooking oils, sauces/dressings, and preparation methods.

## After Calculation

- Report the per-item and total breakdown to the client.
- Keep a running daily total and show remaining macros vs targets.
- Log to the client's tracker via the `excel-tracker` skill.

## Best Practices

- **Caveat Accuracy:** Photo estimates are approximations (±15-20%). Text with gram weights is more accurate.
- **Be Specific:** Use exact quantities, not vague descriptions.
- **Encourage Better Photos:** If the photo is blurry or items are hidden, ask for a better angle or ingredient list.

## Resources

- `templates/photo_estimation_template.md`: The standard format for presenting the nutritional breakdown of a photo.
