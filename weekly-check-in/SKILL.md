---
name: weekly-check-in
description: "Comprehensive weekly review every Sunday. Analyzes the past week's data and provides coaching feedback. Use every Sunday at an appropriate time for the client."
---

# Weekly Check-In

This skill provides a structured framework for conducting a comprehensive weekly review of a client's progress, adherence, and recovery.

## Workflow

### 1. Data Collection
- Pull the **Weekly Averages** from the client's master tracker using the `google-sheet-manager` skill.
- Compare the current week's averages against the previous week and the set targets.

### 2. Analysis
- **Weight Trend:** Calculate the rate of change and determine if it aligns with the goal.
- **Adherence:** Evaluate nutrition (calories/protein) and training (sessions completed/lifts) adherence.
- **Recovery:** Review sleep and stress trends.
- **Activity:** Check average daily step counts.

### 3. Coaching Feedback
- **Celebrate Wins:** Always start by highlighting at least 1-2 positive achievements from the week.
- **Identify Focus Area:** Address **exactly one** area for improvement to avoid overwhelming the client.
- **Flag Recalibrations:** If data triggers recalibration thresholds (e.g., weight loss >1%/week), flag the need for a `program-update`.
- **Tone:** Maintain a supportive, professional "coach" persona. Be specific and data-driven.

### 4. Client Engagement
- Ask the client how they are feeling about the process.
- End with a specific question: "What's one thing you want to focus on improving this week?"

## Recalibration Thresholds
- **Fat Loss:** >1% bodyweight loss per week (excluding week 1).
- **Lean Bulk:** >0.5% bodyweight gain per week (excluding week 1).
- **Stalling:** Lifts stalling for 2+ weeks across multiple exercises.

## Resources

- `templates/weekly_review_template.md`: The standard format for presenting the weekly progress summary and feedback.
