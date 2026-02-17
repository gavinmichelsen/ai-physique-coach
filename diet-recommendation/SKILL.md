# Diet Recommendation Skill

This skill provides comprehensive, evidence-based nutrition protocols, including a robust energy balance calculator, to support physique transformation goals. It integrates scientific principles of macronutrient distribution, meal timing, and dietary adherence to optimize results for various body compositions and activity levels.

## Key Features

*   **Personalized Macronutrient Calculation**: Dynamically adjusts protein, carbohydrate, and fat intake based on individual metabolic rate, activity level, and specific physique goals (e.g., fat loss, muscle gain, maintenance).
*   **Energy Balance Optimization**: Utilizes a sophisticated calculator to determine daily caloric needs, ensuring precise energy intake for desired outcomes while minimizing metabolic adaptation.
*   **Meal Timing Strategies**: Offers guidance on optimal meal frequency and timing to support nutrient partitioning, satiety, and workout performance.
*   **Dietary Adherence Support**: Provides practical strategies for meal preparation, food selection, and behavioral modifications to enhance long-term adherence to the nutrition plan.
*   **Evidence-Based Protocols**: All recommendations are grounded in current scientific literature and best practices in sports nutrition and exercise physiology.

## Usage

To generate a personalized diet plan, invoke this skill with the following parameters:

*   `goal`: (string, required) The primary physique goal (e.g., "fat loss", "muscle gain", "maintenance").
*   `weight_kg`: (number, required) Current body weight in kilograms.
*   `height_cm`: (number, required) Current height in centimeters.
*   `age`: (number, required) Current age in years.
*   `gender`: (string, required) Biological gender ("male" or "female").
*   `activity_level`: (string, required) Describes daily physical activity (e.g., "sedentary", "lightly active", "moderately active", "very active", "extremely active").
*   `body_fat_percentage`: (number, optional) Estimated body fat percentage. Used for more precise calculations.
*   `dietary_preferences`: (array of strings, optional) Any specific dietary preferences or restrictions (e.g., "vegetarian", "vegan", "gluten-free", "dairy-free").
*   `allergies`: (array of strings, optional) Known food allergies.

## Example Invocation

```json
{
    "goal": "muscle gain",
    "weight_kg": 75,
    "height_cm": 175,
    "age": 30,
    "gender": "male",
    "activity_level": "moderately active",
    "body_fat_percentage": 15,
    "dietary_preferences": ["no red meat"],
    "allergies": ["peanuts"]
}
```

## Output

The skill will return a detailed diet plan, including:

*   **Calculated Daily Caloric Intake**: Total calories recommended per day.
*   **Macronutrient Breakdown**: Grams and percentages of protein, carbohydrates, and fats.
*   **Sample Meal Plan**: A daily meal structure with suggested food items and portion sizes, tailored to the user's preferences and goals.
*   **Hydration Guidelines**: Recommendations for daily water intake.
*   **Supplement Recommendations**: Optional suggestions for supplements that may support the user's goals.

## Scientific Basis

The energy balance calculator and macronutrient recommendations are based on established equations and guidelines, including:

*   **Mifflin-St Jeor Equation**: Used for calculating Basal Metabolic Rate (BMR) [1].
*   **Activity Factor Multipliers**: Applied to BMR to determine Total Daily Energy Expenditure (TDEE) [2].
*   **Macronutrient Distribution Ranges**: Aligned with recommendations from leading sports nutrition organizations for optimal performance and body composition [3].

### References

[1] Mifflin, M. D., St Jeor, S. T., Hill, L. A., Scott, B. J., Daugherty, S. A., & Schundler, A. (1990). A new predictive equation for resting energy expenditure in healthy individuals. *The American Journal of Clinical Nutrition*, *51*(2), 241-247. [Link](https://pubmed.ncbi.nlm.nih.gov/2309541/)
[2] American College of Sports Medicine. (2018). *ACSM's Guidelines for Exercise Testing and Prescription* (10th ed.). Wolters Kluwer.
[3] International Society of Sports Nutrition. (2017). ISSN position stand: protein and exercise. *Journal of the International Society of Sports Nutrition*, *14*(1), 20. [Link](https://jissn.biomedcentral.com/articles/10.1186/s12970-017-0177-8)
