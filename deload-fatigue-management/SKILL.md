---
name: deload-fatigue-management
description: "Implements reactive deloads when the client needs them. Use ONLY when client requests a deload or lifts are seriously stalling despite adequate recovery."
---

# Deload / Fatigue Management

This skill provides the logic for implementing reactive deloads to manage accumulated fatigue and break through performance plateaus.

## Philosophy

- **Reactive, Not Proactive:** Do NOT schedule deloads every 4th week by default. Only implement when specific triggers are met.
- **Maintain Intensity:** The goal is to dissipate fatigue while maintaining the neuromuscular stimulus. Do NOT reduce the weight or RPE targets.
- **Reduce Volume:** Volume is the primary driver of fatigue. Reducing sets allows for recovery without losing strength adaptations.

## Trigger Conditions

Implement a deload ONLY when:
1.  **Client Request:** The client explicitly reports feeling "beat up," having persistent joint pain, or excessive soreness.
2.  **Performance Stall:** Lifts have stalled or regressed for **2+ consecutive weeks** across multiple exercises, and recovery (sleep, nutrition, stress) is not the obvious culprit.
3.  **General Fatigue:** Client reports persistent fatigue that isn't explained by external life factors.

## Deload Protocol

- **Duration:** 1 week.
- **Volume Reduction:** Reduce total sets by **40-50%** (e.g., cut 4 sets down to 2).
- **Intensity Maintenance:** Keep the **same weights** and **same RPE targets** as the previous week.
- **Exercise Selection:** Keep the same exercises; do not introduce new movements during a deload.

## Workflow

1.  **Identify Need:** Monitor weekly check-ins for stalling or fatigue reports.
2.  **Verify Recovery:** Ensure the stall isn't just due to a bad week of sleep or missed meals.
3.  **Prescribe Deload:** Use the format in `templates/deload_protocol_template.md` to explain the protocol to the client.
4.  **Monitor Rebound:** Expect performance to rebound within 1-2 weeks after the deload. If it doesn't, investigate other factors or consider a program restructure.

## Resources

- `templates/deload_protocol_template.md`: The standard format for prescribing a reactive deload week.
