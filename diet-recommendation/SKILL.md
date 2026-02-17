---
name: diet-recommendation
description: "Sets calorie and macronutrient targets based on TDEE, body fat %, and goal. Use after TDEE calculation, during phase transitions, or when adjusting nutrition."
---

# Diet Recommendation

This skill provides the logic for setting precise nutritional targets based on a client's physiological data and physique goals.

## Calorie Target Logic

### 1. Fat Loss
- **Client <=15% bf (male) / <=25% (female):** 15% deficit (TDEE x 0.85).
- **Client >15% bf (male) / >25% (female):** 25% deficit (TDEE x 0.75).
- **Calorie Floor:** Never prescribe below **bodyweight (lbs) x 10**. If the deficit would drop below this, increase activity/expenditure instead.

### 2. Lean Bulk
- **Target:** Eat at **Maintenance (TDEE)**.
- **Philosophy:** No explicit surplus is required. Muscle growth only requires ~40-100 extra kcal/day, which is achieved through ad libitum eating at maintenance. Focus on progressive overload.

### 3. Maintenance / Recomposition
- **Target:** Eat at **Maintenance (TDEE)**.

## Macronutrient Setup

1.  **Protein:** 0.75-0.82g per lb of **goal bodyweight**. Use the higher end during fat loss to preserve lean mass.
2.  **Fat:** Minimum 0.3g per lb of bodyweight, and never below 20% of total calories. Default to **0.35g/lb**.
3.  **Carbohydrates:** Remaining calories after protein and fat are set. Carbs are essential for fueling training performance.

## Adherence & Strategy

- **No Refeeds:** Not supported by evidence; do not prescribe.
- **Diet Breaks:** Available during extended cuts (6+ weeks) if the client is struggling. 1-2 weeks at maintenance (increase calories via carbs), then resume the deficit. Frame as a "strategic pause."
- **Fiber:** Recommend 25-35g/day.
- **Hydration:** Minimum half bodyweight (lbs) in ounces of water daily.

## Workflow

1.  **Pull Data:** Review TDEE, body fat %, and current goal.
2.  **Calculate Calories:** Apply the deficit or maintenance logic based on the goal and body fat.
3.  **Set Macros:** Follow the protein -> fat -> carb hierarchy.
4.  **Check Floor:** Ensure calories are not below the bodyweight x 10 threshold.
5.  **Present Plan:** Use the format in `templates/diet_plan_template.md`.
6.  **Onboarding Note:** For clients new to tracking, advise focusing on the protein target first for the first week.

## Resources

- `templates/diet_plan_template.md`: The standard format for presenting calorie and macro targets.
