---
name: sleep-stress-check-in
description: "Monitors sleep and stress trends and modifies training recommendations when recovery is compromised. Integrates with daily check-in data."
---

# Sleep/Stress Check-In

This skill provides the logic for identifying compromised recovery and implementing temporary program modifications to prevent burnout and injury.

## Trigger Conditions

Monitor daily check-in data for the following triggers:
- **Sleep Quality:** Drops below **5/10** for 3+ consecutive days.
- **Sleep Duration:** Drops below **6 hours** for 3+ consecutive days.
- **Stress Level:** Above **8/10** for 3+ consecutive days.
- **Life Events:** Client reports a major life stressor (e.g., exams, work crisis, personal loss).

## Response Protocol

### 1. Immediate Adjustment (Short-term)
- **Acknowledge:** Directly mention the trend to the client.
- **Reduce Intensity:** Drop RPE targets by **1** (e.g., RPE 8 -> RPE 7).
- **Volume:** Maintain volume unless the situation persists beyond 1 week.

### 2. Persistent Adjustment (1+ week)
- **Reduce Volume:** Cut total volume by **20-30%**.
- **Prioritize:** Keep compound movements; remove accessory/isolation work.
- **Nutrition:** Do NOT increase a caloric deficit. If the client is in a cut, move to **Maintenance** temporarily.

### 3. Sleep Hygiene Advice
Provide actionable tips:
- Consistent bed/wake times.
- No screens 30 minutes before bed.
- Cool, dark sleeping environment.
- Limit caffeine after early afternoon.

## Workflow

1.  **Monitor Data:** Use `daily-check-in` data to identify trends.
2.  **Apply Protocol:** If triggers are met, determine the level of adjustment needed.
3.  **Communicate:** Use the format in `templates/recovery_adjustment_template.md`.
4.  **Ramp Back:** Return to normal programming once sleep/stress metrics have improved for **3 consecutive days**.

## Resources

- `templates/recovery_adjustment_template.md`: Standardized message for communicating recovery-based adjustments and sleep hygiene tips.
