---
name: phase-transition
description: "Manages the transition between phases (cut → maintenance, maintenance → lean bulk, lean bulk → cut). Use when a client reaches their goal for the current phase or when a phase change is warranted."
---

# Phase Transition

This skill provides the evidence-based logic for transitioning clients between different physiological phases (cutting, maintenance, and bulking) while managing expectations and physiological responses.

## Core Philosophy

- **No Reverse Dieting:** Move directly to the estimated new maintenance calories (TDEE) when ending a cut.
- **Maintenance Buffer:** Recommend at least **2-4 weeks at maintenance** between a cut and a bulk for metabolic and psychological recovery.
- **Expect Water Weight:** Educate clients on the initial scale jump (2-4 lbs) from glycogen and water replenishment when increasing calories.

## Transition Protocols

### 1. Cut → Maintenance
- **Calories:** Increase directly to the new estimated TDEE (recalculate using current bodyweight).
- **Macros:** Increase primarily via carbohydrates.
- **Activity:** Maintain current training and step targets.

### 2. Maintenance → Lean Bulk
- **Calories:** Stay at maintenance (TDEE) or a very slight surplus (100-200 kcal).
- **Focus:** Shift primary focus to progressive overload in training.
- **Activity:** Step targets can relax slightly (e.g., 7,500+) but should not collapse.

### 3. Lean Bulk → Cut
- **Calories:** Recalculate TDEE and apply a 15-25% deficit based on body fat percentage.
- **Activity:** Increase step targets to drive expenditure.
- **Expectations:** Inform the client that strength may plateau or slightly decline.

## Workflow

1.  **Identify Goal:** Confirm the client has reached the target for the current phase.
2.  **Recalculate:** Use the `tdee-calculation` skill with the client's current weight.
3.  **Set New Targets:** Use the `diet-recommendation` and `cardio-programming` skills to set the new protocol.
4.  **Communicate:** Use the format in `templates/transition_protocol_template.md` to explain the "why" and manage scale expectations.
5.  **Log History:** Update the **Program History** tab in the master tracker via `google-sheet-manager`.

## Resources

- `templates/transition_protocol_template.md`: Standardized format for communicating phase changes and managing expectations regarding water weight.
