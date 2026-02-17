---
name: meal-planner
description: "Creates meal suggestions and recipes fitting the client's calorie/macro targets and dietary preferences. Use when client requests meal ideas, after diet targets are set, or client says they don't know what to eat."
---

# Meal Planner / Recipe Recommender

This skill helps clients translate their calorie and macronutrient targets into practical, sustainable eating habits.

## Philosophy

- **Adherence Over Optimization:** The best diet is the one the client follows.
- **Flexibility:** Teach clients to think in macros rather than rigid meal plans.
- **Rotation:** Most clients benefit from 3-5 "go-to" meals they rotate, rather than a different meal every day.
- **Protein-Centric:** Every meal must contain a protein source.

## Workflow

1.  **Pull Targets:** Review the client's calorie/macro targets and dietary preferences (Vegan, Keto, allergies, etc.).
2.  **Create Framework:** Distribute protein evenly across the client's preferred number of meals.
3.  **Suggest Options:** For each meal slot, provide three types of ideas:
    - **Quick/Lazy:** Minimal prep (e.g., rotisserie chicken and bagged salad).
    - **Meal Prep:** Batch-cookable (e.g., chili, roasted chicken and veggies).
    - **Restaurant/Fast Food:** Macro-friendly choices when eating out.
4.  **Provide Recipes:** On request, provide recipes including ingredients, macros per serving, and prep time.
5.  **Educate:** Include the "Hand Portion Guide" (Palm = Protein, Fist = Carbs, Thumb = Fat) for situations where tracking isn't possible.
6.  **Present:** Use the format in `templates/meal_framework_template.md`.

## Guidelines

- **Vegetables:** Encourage vegetables in at least 2 meals daily for micronutrients and satiety.
- **Treats:** Help clients fit "fun foods" (like pizza or burgers) into their macros rather than banning them.
- **Protein Reference:** Use `references/high_protein_foods.md` to help clients find variety in their protein sources.

## Resources

- `templates/meal_framework_template.md`: The standard format for the daily meal framework.
- `references/high_protein_foods.md`: A categorized list of high-protein food sources.
