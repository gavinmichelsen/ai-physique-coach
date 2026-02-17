---
name: diet-recommendation-v2
description: "Provides comprehensive, evidence-based nutrition protocols for physique coaching, covering calories, macros, food quality, and strategic adjustments. Use after TDEE calculation or when updating a client's nutrition plan."
---

# Advanced Diet Recommendation Protocol

This skill provides the logic for establishing precise, evidence-based nutritional targets tailored to a client's physiological data, goals, and long-term health. It moves beyond simple macro tracking to incorporate principles of food quality, strategic adjustments, and metabolic verification.

## 1. Calorie Target Logic

Calorie targets are determined by the client's primary goal, with adjustments based on their current body fat percentage to optimize for adherence, muscle preservation, and hormonal health.

| Goal | Body Fat (Male) | Body Fat (Female) | Caloric Adjustment | Rationale |
| :--- | :--- | :--- | :--- | :--- |
| **Fat Loss** | >15% | >25% | **25% Deficit** (TDEE x 0.75) | A more aggressive deficit is appropriate and effective at higher body fat levels. [1] |
| **Fat Loss** | ≤15% | ≤25% | **15% Deficit** (TDEE x 0.85) | A moderate deficit is crucial for preserving lean mass and mitigating hormonal disruption as the client gets leaner. [1] |
| **Lean Bulk** | Any | Any | **Maintenance** (TDEE x 1.0) | A significant caloric surplus is not required for muscle growth and often leads to unnecessary fat gain. Anabolism is supported by training stimulus and adequate protein, with a small surplus occurring naturally. [2] |
| **Maintenance** | Any | Any | **Maintenance** (TDEE x 1.0) | The target is to maintain current body composition. |

**Calorie Floor:** Never prescribe a caloric intake below **bodyweight (lbs) x 10**. If the calculated deficit falls below this floor, the primary strategy should be to increase the client's daily energy expenditure (e.g., through more steps or cardio) rather than further reducing calories.

## 2. Macronutrient & Micronutrient Setup

Macros are set in a hierarchical order to ensure critical physiological needs are met first.

### Step 1: Protein
- **Target:** **0.75-0.82g per pound of GOAL bodyweight** (1.6-1.8 g/kg). [3]
- **Rationale:** This range is optimal for supporting muscle protein synthesis, promoting satiety, and preserving lean body mass, especially during a caloric deficit. Use the higher end of the range (0.82g/lb) during fat loss phases. [4]

### Step 2: Fat
- **Minimum Threshold:** Set dietary fat to a minimum of **0.3g per pound of current bodyweight**, ensuring it does not fall below **20% of total daily calories**. [5]
- **Default Target:** A starting point of **0.35g per pound of bodyweight** is recommended for most clients.
- **Fat Quality:** Emphasize the importance of fat quality. Encourage consumption of monounsaturated and polyunsaturated fats from sources like avocados, nuts, seeds, and olive oil. For omega-3 fatty acids, recommend fatty fish (like salmon) 2-3 times per week. If the client does not consume fish, an omega-3 supplement (EPA/DHA) should be recommended. [1]

### Step 3: Carbohydrates
- **Target:** The **remaining calories** after protein and fat targets have been set.
- **Rationale:** Carbohydrates are the primary fuel source for high-intensity training and are crucial for performance and recovery. They are also protein-sparing. [2]

### Step 4: Fiber
- **Target:** **10-15g of fiber per 1,000 kcal consumed**, with an absolute minimum of 25g per day for women and 35g per day for men. [6]
- **Rationale:** Adequate fiber intake is critical for digestive health, satiety, and blood sugar management. This is best achieved through a high intake of fruits, vegetables, legumes, and whole grains. [1]

### Step 5: Micronutrients
- **Guidance:** While specific micronutrient targets are not set, the protocol emphasizes a **food-first approach**. A diet rich in a variety of colorful fruits and vegetables (aiming for ~800g total per day), lean proteins, and healthy fats will cover most micronutrient needs. This approach provides essential vitamins, minerals, and health-promoting phytochemicals. [1]

## 3. Lifestyle & Strategic Guidance

### Hydration
- **Guidance:** The primary recommendation is to **drink to thirst**. The body has a sensitive and effective thirst mechanism. [1]
- **Monitoring:** Advise clients to monitor their urine color; a pale yellow color indicates adequate hydration, while dark yellow suggests a need to increase fluid intake. [1]

### Meal Timing & Frequency
- **Guidance:** Total daily caloric and macronutrient intake are the most important factors for body composition. Meal timing and frequency are secondary. [1]
- **Recommendation:** Advise clients to adopt a consistent meal pattern that fits their lifestyle and preferences, as this can aid adherence. There is no inherent metabolic advantage to eating many small meals versus a few larger ones.

### Alcohol
- **Guidance:** Alcohol provides empty calories, can negatively impact recovery and sleep quality, and is directly toxic to testosterone production in men. [1]
- **Recommendation:** Advise clients to limit alcohol consumption, especially during fat loss phases. If consumed, it should be done in moderation. From a health perspective, red wine may be a less detrimental choice due to its polyphenol content, but abstinence is optimal. [1]

### Food Quality
- **Principle:** Emphasize a diet based on whole, minimally processed foods.
- **Healthy Staples:** Encourage a diet foundation built on non-starchy vegetables, seafood, berries, avocados, olives, nuts, seeds, and legumes. [1]
- **Healthy Additions:** Include whole fruits, poultry, fermented dairy (kefir, yogurt), tubers (potatoes), and whole grains. [1]
- **Foods to Limit:** Advise limiting intake of sugars, refined grains, and processed foods. [1]

## 4. Advanced Strategies & Adjustments

### Deficit/Surplus Selection Logic
- **Body Fat % as a Guide:** The initial deficit/surplus is set based on body fat percentage. As a client's body fat drops, the deficit should become less aggressive to preserve muscle and support hormonal function. [1]
- **Sustainable Leanness:** The lowest sustainable body fat levels are generally around **15-20% for women** (to maintain a regular menstrual cycle) and **~10% for men**. Pushing below these levels for extended periods can lead to negative health consequences and is generally reserved for short-term physique competitions. [1]

### Macro Cycling
- **Concept:** This is an optional, advanced strategy where carbohydrate and fat intake is varied between training and rest days, while protein and total weekly calories remain constant.
- **Application:** On training days, increase carbohydrates and decrease fats to fuel performance. On rest days, decrease carbohydrates and increase fats. This is not necessary for most clients but can be a useful tool for advanced individuals.

### Refeeds & Diet Breaks
- **Diet Breaks:** For extended fat loss phases (8+ weeks), a planned **1-2 week diet break** at maintenance calories (increasing carbs) can be beneficial for psychological relief, adherence, and potentially reversing some metabolic adaptations. [1]
- **Refeeds:** A refeed is a shorter, 1-2 day period of increased carbohydrate intake at or slightly above maintenance calories. This can help restore glycogen, boost performance, and provide a mental break from dieting.

### Adjustment Triggers
- **Primary Metric:** Progress should be assessed based on a combination of weekly average body weight, body composition measurements, and performance in the gym.
- **When to Adjust:** If a client's fat loss stalls for **2-4 consecutive weeks** (i.e., no change in weekly average weight or measurements), a downward adjustment of **100-200 calories** (primarily from carbs or fats) may be warranted. Conversely, if weight loss is too rapid (>1.5% of bodyweight per week), the deficit may be too aggressive.

## 5. Energy Balance Calculator

This tool helps verify a client's reported energy intake against their actual body composition changes, providing an objective measure of their true energy balance. It is most effective when two reliable body composition measurements (e.g., DEXA scans) are available over a specific time frame.

- **Metabolizable Energy Densities (Hall, 2008):** [7]
  - Glycogen: 4207 kcal/kg
  - Protein: 4708 kcal/kg
  - Fat: 9441 kcal/kg
  - Lean Body Mass (LBM): 1816 kcal/kg

- **Formula:**
  `Energy Balance = (Change in LBM (kg) × 1816) + (Change in Fat Mass (kg) × 9441)`

- **Interpretation:**
  - A **negative** result indicates a true caloric deficit.
  - A **positive** result indicates a true caloric surplus.
  - This calculated energy balance can be compared to the client's tracked caloric intake to identify discrepancies and guide coaching conversations.

## 6. Workflow

1.  **Gather Data:** Collect client's goal, TDEE, current bodyweight, and body fat %.
2.  **Calculate Calories:** Apply the appropriate deficit or maintenance logic.
3.  **Set Macros & Fiber:** Use the hierarchical approach (Protein -> Fat -> Carbs -> Fiber).
4.  **Check Calorie Floor:** Ensure the final calorie target is above the safety threshold.
5.  **Incorporate Qualitative Guidance:** Add notes on hydration, food quality, and alcohol.
6.  **Present Plan:** Use the updated `diet-recommendation-template.md` to deliver the comprehensive plan to the client.
7.  **Onboarding:** For new clients, advise them to focus on hitting their protein and calorie targets for the first 1-2 weeks before worrying about precise fat and carb numbers.

## References
[1] Health-PTC-2025.pdf (Provided document)
[2] Iraki, J., Fitschen, P., Espinar, S., & Helms, E. (2019). Nutrition Recommendations for Bodybuilders in the Off-Season. *Sports*, 7(7), 154. https://doi.org/10.3390/sports7070154
[3] Morton, R. W., Murphy, K. T., McKellar, S. R., Schoenfeld, B. J., Henselmans, M., Helms, E., ... & Phillips, S. M. (2018). A systematic review, meta-analysis and meta-regression of the effect of protein supplementation on resistance training-induced gains in muscle mass and strength in healthy adults. *British journal of sports medicine*, 52(6), 376-384.
[4] Helms, E. R., Zinn, C., Rowlands, D. S., & Brown, S. R. (2014). A systematic review of dietary protein during caloric restriction in resistance trained lean athletes: a case for higher intakes. *International journal of sport nutrition and exercise metabolism*, 24(2), 127-138.
[5] Lowery, L. M. (2004). Dietary fat and sports nutrition: a primer. *Journal of sports science & medicine*, 3(3), 106.
[6] Mancin, L., et al. (2025). Fibre: The Forgotten Carbohydrate in Sports Nutrition Recommendations. *Sports Medicine*, 1-21.
[7] Hall, K. D. (2008). What is the required energy deficit per unit weight loss?. *International journal of obesity*, 32(3), 573-576.
