---
name: physique-coach-onboarding
description: "Guides the collection of comprehensive client data for physique coaching, including physical profile, training history, nutrition, and lifestyle. Use for: onboarding new fitness clients, gathering data for exercise/dietary protocols, and creating structured client profiles."
---

# Physique Coach Onboarding

This skill provides a structured workflow for gathering all necessary information from a client to create a professional physique transformation plan.

## Workflow

1.  **Initiate Interview**: Inform the client that you will be gathering information to build their custom physique protocol. Explain that this comprehensive intake process ensures the program is tailored to their unique circumstances, goals, and constraints.

2.  **Gather Data**: Systematically ask the questions outlined in the `templates/onboarding_form.md`. 
    - Group questions into logical sections (Basic Info, Goals, Training History, Nutrition, Lifestyle, Medical History) to avoid overwhelming the client.
    - Ask follow-up questions if the client's answers are vague or incomplete. For example:
      - If they say "I want to lose weight," ask for a specific target weight or body fat percentage.
      - If they mention an injury, ask about the severity, when it occurred, and any current limitations.
      - If they describe their training as "moderate," ask for specific exercises, sets, reps, and frequency.
    - **Provide context** for questions when appropriate. For example: "Knowing your occupation helps me estimate your daily energy expenditure and design a program that fits your schedule."
    - **Fitness Influence**: Ask the client if there's a figure in fitness they particularly like or follow. If so, research that figure's publicly available training and nutrition approach and use it to inform the program structure — while still adhering to science-based principles of hypertrophy and dieting.
    - **Encourage honesty over estimation**: For metrics like calorie intake and water consumption, advise clients that if they aren't currently tracking, they should say so rather than guessing. Honest "I don't know" answers are more useful than inaccurate estimates.

3.  **Assess Dedication and Commitment**: Use structured questions to understand the client's dedication level and training capacity:
    - Ask which approach resonates most: sustainability-focused, balanced results-to-effort, or maximum results without compromising health.
    - Determine how many days per week they are prepared to train for optimal results.
    - Identify specific times they are unable or unwilling to train (be detailed about work schedules, family commitments, etc.).

4.  **Evaluate Equipment and Training Environment**: Conduct a thorough assessment of available equipment to ensure program feasibility:
    - Identify gym type (commercial, home, CrossFit box, etc.)
    - Assess availability of specialized equipment (squat rack, cable systems, specific machines)
    - Note weight plate and dumbbell increment availability for progressive overload planning
    - Document any equipment limitations that require exercise substitutions

5.  **Generate Profile**: Once all information is gathered, populate the `templates/onboarding_form.md` and present the completed profile to the client for review and confirmation.

6.  **Trigger Downstream Skills**: Once the profile is confirmed, trigger the following skills in order:
    1. `tdee-calculation`
    2. `diet-recommendation`
    3. `resistance-training-program`
    4. `cardio-programming`
    5. `goal-setting-milestones`

7.  **Create Master Tracking Sheet**: Create an Excel file for the client using the `excel-tracker` skill. This file will be retained locally and updated every time significant data comes in (weekly check-ins, body measurements, progress photos, training performance, etc.). The tracking sheet should include:
    - Weekly body weight and measurements
    - Body composition estimates
    - Training performance metrics (key lifts, volume progression)
    - Nutrition adherence and average daily intake
    - Subjective metrics (energy, sleep quality, stress, recovery)
    - Progress photos timeline
    - Notes and adjustments made

8.  **Schedule Check-Ins**: Ask the client when they would prefer to do check-ins. Explain that you will:
    - Check in once in the morning (e.g., 7:00 AM)
    - Check in once at night (e.g., 10:00 PM)
    - Conduct a comprehensive weekly check-in on one day of the week (e.g., Sunday)
    
    Provide examples and ask for their preferred times. Once confirmed:
    - Update memory with the client's check-in schedule
    - Schedule these check-ins using the `daily-check-in` and `weekly-check-in` skills
    - Update memory context for the client based on the specific variables they are tracking for their routine (e.g., if they're tracking morning weight, sleep quality, training performance, meal adherence, energy levels, etc.)

9.  **Deliver Onboarding Package**: Send the client:
    - The completed onboarding profile document
    - The initial training and nutrition plan
    - The Excel tracking sheet
    - Clear instructions on how to use the tracking system and what to expect from check-ins

## Best Practices

### Communication
- **Professional Tone**: Maintain an encouraging yet professional "coach" persona throughout the process.
- **Clarity and Context**: Ensure the client understands why each piece of information is being requested. This increases compliance and helps them see the value in thorough data collection.
- **Active Listening**: Pay attention to nuances in client responses that might indicate underlying concerns, limitations, or opportunities for customization.

### Data Collection
- **Completeness**: Do not skip sections. A well-defined protocol requires a complete picture of the client's current state, history, and goals.
- **Specificity**: Push for specific, measurable answers rather than vague descriptions. Use follow-up questions to clarify.
- **Depth Over Breadth**: It's better to have detailed information in key areas than superficial coverage of everything.
- **Honesty Over Accuracy**: Encourage clients to admit when they don't know something rather than guessing. This is especially important for nutrition tracking and historical data.

### Assessment Approach
- **Structured Options**: When appropriate, provide multiple-choice options with clear descriptions rather than purely open-ended questions. This helps clients understand the range of possibilities and choose accurately.
- **Medical Thoroughness**: Take comprehensive notes on injuries, pathologies, and medical history. This information is critical for safe program design.
- **Lifestyle Integration**: Pay close attention to occupation, stress levels, sleep quality, and daily activity patterns. These factors significantly impact program design and recovery capacity.
- **Training History Detail**: Understand not just how long they've trained, but what programs they've followed, what worked, what didn't, and their current strength levels.
- **Equipment Reality Check**: Be thorough in equipment assessment to avoid designing a program the client cannot execute.

### Program Design Considerations
- **Genetic and Body Composition Indicators**: Use frame size indicators (wrist/ankle circumference), body composition history, and genetic background to inform realistic goal-setting and program expectations.
- **Dedication Alignment**: Match program intensity and volume to the client's stated dedication level and lifestyle capacity.
- **Progressive Tracking**: Design the tracking system to capture the metrics most relevant to the client's specific goals and program structure.

## Resources

- `templates/onboarding_form.md`: The master template for the client profile.
- `excel-tracker`: Skill for creating and managing the client tracking spreadsheet.
- `daily-check-in`: Skill for conducting daily progress check-ins.
- `weekly-check-in`: Skill for conducting comprehensive weekly assessments.
