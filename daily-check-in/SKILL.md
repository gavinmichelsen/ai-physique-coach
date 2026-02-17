---
name: daily-check-in
description: "Manages daily data collection via morning and evening messages. Use on a scheduled basis aligned to the client's wake and bed times."
---

# Daily Check-In

This skill manages the daily interaction and data collection process to ensure consistent tracking and client accountability.

## Workflow

### 1. Morning Check-In
- **Setup:** During onboarding, recommend morning check-in variables based on the client's program and goals, then let the client choose which ones to keep. Ask what time they'd like the check-in. Default to their wake time.
- **Timing:** Trigger daily at the client's chosen time. Say good morning and ask for the check-in variables.
- **Recommended Morning Variables:** Sleep duration (hrs), Sleep quality (1-10), Morning weight (lbs), Stress level (1-10). Recommend variables based on the client's custom program — e.g., if sleep is a concern, include sleep metrics; if the client is cutting, weight is essential. Let the client opt in/out.
- **Daily Action Items:** After the client responds: (1) FIRST log the data to the tracker via `excel-tracker` skill and verify it wrote correctly, (2) THEN reply with the day's action items based on their program (e.g., calorie target, protein target, step target, training session if scheduled, any other relevant reminders) and attach the updated tracker file. Do NOT include action items in the initial check-in message — keep that clean and focused on data collection. Do NOT reply with action items until the data is actually written and verified in the file.
- **Workout Reminder:** If today is a scheduled training day, include a reminder in the morning check-in (e.g., "Reminder: you've got Workout A scheduled today at 5pm").
- **Weight Commentary:** Do NOT comment on day-to-day weight changes (e.g., "down a pound from yesterday"). Weight fluctuates daily. Simply acknowledge that the client weighed in — progress is measured on weekly averages, not daily swings.
- **Nudge Policy:** If no response within 2 hours, send one gentle nudge. If still no response, log as "no data" and do not pester.

### 2. Evening Check-In
- **Timing:** Trigger 1 hour before the client's reported bedtime.
- **Questions:** Ask about daily steps, stress level (1-10), and any additional notes (travel, illness, etc.).
- **Meal Logging Reminder:** If the client hasn't logged any meals today via the `meal-photo-estimator` skill, gently remind them: "Did you eat anything today you haven't logged yet? Just send a photo or tell me what you had." All nutrition tracking is done through the AI — no external apps.

### 3. Training Follow-up
- **Trigger:** When the client reports completing a training session.
- **Action:** Ask for the session details, including exercises, weights, reps, and RIR (or RPE if client prefers).

### 4. Data Logging
- Immediately log all received data to the client's master tracker using the `excel-tracker` skill.
- Accept and log proactive data sent by the client at any time, even outside of scheduled check-ins.

## Best Practices

- **Brief & Conversational:** Keep messages short and friendly. Use the client's name.
- **Positive Reinforcement:** Provide encouragement when the client shows consistency (e.g., "Solid work hitting your protein target 7 days in a row!").
- **No Judgment:** Maintain a supportive "coach" persona regardless of the data reported.
- **Efficiency:** Ask a maximum of 3-4 questions at a time to avoid overwhelming the client.

## Resources

- `templates/checkin_templates.md`: Standardized message templates for morning, evening, and follow-up interactions.
