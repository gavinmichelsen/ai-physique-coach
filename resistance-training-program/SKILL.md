---
name: resistance-training-program
description: "Creates a customized resistance training program for beginner to intermediate trainees. Use after onboarding, when client requests changes, or after phase transitions."
---

# Resistance Training Program

This skill provides the logic and structure for creating evidence-based resistance training programs tailored to a client's experience, equipment, and goals.

## Programming Philosophy

### 1. Structure and Autoregulation
- **Default Set Structure:** Straight sets with **RIR-based autoregulation** (Reps In Reserve). If a client prefers RPE, switch on their request (RPE 10 = RIR 0, RPE 9 = RIR 1, etc.).
- **Reverse Pyramid Training (RPT):** Only use if explicitly requested by the client.
- **Rest Periods:** 3 minutes for compound movements; 1-2 minutes for isolation movements.

### 2. Progressive Overload
- **Double Progression:** When a client hits the top of the rep range (or above) on their **last set** at the target RIR (1-3 RIR), increase weight by the minimum increment (5 lbs upper, 10 lbs lower) and reset to the bottom of the rep range. Earlier sets may exceed the rep range since the client is fresher — this is expected. What matters is intensity and proximity to failure on every set, not matching reps across sets.

### 3. Volume and Intensity
- **Volume:** 10-20 hard sets per muscle group per week.
  - Beginners: Lower end (10-12 sets).
  - Intermediates: Upper end (15-20 sets).
- **Frequency:** Minimum 2x frequency per muscle group per week.
- **Intensity (RIR):**
  - Working sets: 1-3 RIR.
  - Beginners: 2-3 RIR (focus on technique).
  - Intermediates: Can push to 1 RIR on key lifts.
  - **Failure (0 RIR):** No sets to absolute failure except the last set of isolation movements for intermediates.

### 4. Exercise Selection
- **Compounds First:** Every session starts with a compound movement.
- **Movement Patterns:** Ensure the weekly plan includes:
  - Vertical Push & Pull
  - Horizontal Push & Pull
  - Hip Hinge & Squat Pattern
  - Direct Arm & Lateral Delt work

## Split Selection Logic

Choose the split based on the client's available training days:
- **3 Days:** Upper / Lower / Upper rotation (best for beginners).
- **4 Days:** Upper / Lower split.
- **5 Days:** Upper / Lower / Push / Pull / Legs or custom.
- **6 Days:** Push / Pull / Legs x2.

## Workflow

1.  **Pull Profile:** Review the client's onboarding data (experience, equipment, injuries).
2.  **Determine Split:** Select the appropriate split based on available days.
3.  **Select Exercises:** Use `references/exercise_library.md` to match equipment and preferences.
4.  **Assign Targets:**
    - **Compounds:** 3-4 sets of 6-10 reps (1-3 RIR).
    - **Isolations:** 2-3 sets of 10-15 reps (1-2 RIR).
5.  **Define Progression:** Reiterate the double progression scheme.
6.  **Present Program:** Use the format in `templates/program_template.md`.
7.  **Explain "Why":** Briefly explain the reasoning behind exercise selection to increase adherence.

## Resources

- `templates/program_template.md`: The standard format for presenting the training plan.
- `references/exercise_library.md`: A categorized list of exercises and alternatives.
