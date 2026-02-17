# Program Update Decision Tree

This reference provides flowchart-style logic for common recalibration scenarios.

## 1. Fat Loss Scenarios

### Weight Loss Too Fast (>1% bodyweight/week)
- **Check:** Is it Week 1? 
    - **Yes:** Ignore (water loss). Monitor for Week 2.
    - **No:** Reduce deficit. 
        - Increase calories by 100-200 (primarily carbs).
        - OR reduce daily step target by 1,000-2,000.
        - OR remove 1 LISS session.

### Weight Loss Stalled (0 change for 2+ weeks)
- **Check:** Adherence to calories/protein?
    - **No:** Address adherence first. Do not adjust program.
    - **Yes:** Increase expenditure.
        - Increase daily steps by 1,000.
        - OR add 1 LISS session (20-30 min).
        - If expenditure is already high, reduce calories by 100-150.

## 2. Lean Bulk Scenarios

### Weight Gain Too Fast (>0.5% bodyweight/week)
- **Check:** Is it Week 1?
    - **Yes:** Ignore (glycogen/water). Monitor for Week 2.
    - **No:** Check calorie intake.
        - Ensure client isn't drifting into a large surplus.
        - Re-verify TDEE and adherence.
        - Aim for maintenance or very slight surplus.

### Weight Gain Stalled / Strength Stalled
- **Check:** Recovery (Sleep/Stress)?
    - **Poor:** Address recovery first.
    - **Good:** Increase calories by 100-150. Ensure progressive overload is being attempted.

## 3. Training Scenarios

### Lifts Stalling (2+ weeks across multiple exercises)
- **Check:** Recovery (Sleep/Stress/Nutrition)?
    - **Poor:** Address recovery.
    - **Good:** Trigger `deload-fatigue-management` skill.

### Adherence Dropping (Missed sessions/macros)
- **Action:** Simplify.
    - Reduce training frequency (e.g., 4 days -> 3 days).
    - Focus on "Protein Only" tracking for 1 week.
    - Remove complex accessory movements.
