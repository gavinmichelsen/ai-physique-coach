---
name: program-update
description: "Analyzes client data trends and makes evidence-based adjustments to training, nutrition, and cardio. Use when triggered by weekly check-in flags, client request, or scheduled program review (every 4-6 weeks)."
---

# Program Update

This skill provides the logic for making data-driven adjustments to a client's protocol based on their real-world response and adherence.

## Recalibration Triggers

### 1. Weight Trends
- **Fat Loss:** Client losing **>1% bodyweight per week** (on weekly averages, excluding week 1).
    - *Action:* Reduce deficit. Increase calories by 100-200 or reduce cardio.
- **Lean Bulk:** Client gaining **>0.5% bodyweight per week** (on weekly averages, excluding week 1).
    - *Action:* Verify intake; weight is likely increasing too fast. Adjust back to maintenance.

### 2. Performance Trends
- **Stalling:** Lifts stalling for **2+ weeks** across multiple exercises.
    - *Action:* Evaluate recovery (sleep, stress, nutrition) first. If recovery is fine, trigger a deload.

### 3. Adherence Trends
- **Missed Targets:** Client consistently missing sessions or macros.
    - *Action:* Simplify the program. Reduce frequency or tracking complexity.

## Adjustment Priority

When an update is needed, follow this hierarchy of changes:
1.  **Fix Adherence:** Address why targets are being missed.
2.  **Fix Recovery:** Address sleep and stress issues.
3.  **Adjust Cardio/Steps:** Increase or decrease expenditure.
4.  **Adjust Calories:** Modify intake.
5.  **Adjust Training:** Modify volume or exercise selection.

**Rule of Thumb:** Change only **one variable** at a time whenever possible to isolate the effect.

## Workflow

1.  **Analyze Trends:** Review the last 2-4 weeks of data from the master tracker.
2.  **Account for Water Weight:** Ignore the first 1-2 weeks of data when transitioning phases (e.g., starting a cut or bulk).
3.  **Consult Decision Tree:** Use `templates/update_decision_tree.md` to determine the appropriate adjustment.
4.  **Implement Change:** Update the relevant protocol (Diet, Training, or Cardio).
5.  **Communicate:** Explain the "why" behind the change to the client to maintain buy-in.

## Resources

- `templates/update_decision_tree.md`: Flowchart-style logic for common recalibration scenarios.
