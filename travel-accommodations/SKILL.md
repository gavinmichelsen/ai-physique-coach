---
name: travel-accommodations
description: "Helps clients maintain training and nutrition adherence while traveling with different equipment or schedules. Use when client reports upcoming or current travel."
---

# Travel Accommodations

This skill provides the logic for modifying a client's training and nutrition protocol to accommodate travel, ensuring they maintain progress without unnecessary stress.

## Travel Modes

### 1. Gym Access
- **Scenario:** Client has access to a hotel gym or a local commercial gym.
- **Action:** Swap exercises in the current program to match available equipment using the `exercise-library`.
- **Goal:** Maintain the same split, volume, and intensity targets as closely as possible.

### 2. Minimal Equipment / No Gym
- **Scenario:** Client has no gym access or only minimal equipment (e.g., bands, dumbbells).
- **Action:** Provide a bodyweight or minimal equipment program (e.g., push-ups, inverted rows, Bulgarian split squats).
- **Goal:** Focus on maintaining the training habit and preserving muscle mass rather than progression.

### 3. Time Off
- **Scenario:** Client wants to take a complete break from training.
- **Action:** Reassure the client that a few days off will not set them back.
- **Goal:** Focus on recovery and enjoyment. Adjust the program schedule for their return.

## Nutrition While Traveling

- **Priority:** **Protein Target.** Advise the client to prioritize protein above all other macros.
- **Practical Strategies:** Suggest portable protein sources (shakes, jerky, Greek yogurt).
- **Flexibility:** Encourage the client to "eat reasonably" and stay hydrated without stressing over exact macro counts.

## Workflow

1.  **Identify Mode:** Determine the client's travel situation and equipment access.
2.  **Modify Program:** Use the appropriate mode to adjust the training plan.
3.  **Set Nutrition Strategy:** Provide practical tips for maintaining protein intake.
4.  **Communicate:** Use the format in `templates/travel_program_template.md`.
5.  **Plan Return:** Set a clear date for resuming the normal protocol.

## Resources

- `templates/travel_program_template.md`: Standardized format for communicating travel-based training and nutrition adjustments.
