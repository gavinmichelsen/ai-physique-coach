---
name: exercise-demonstration
description: "Provides exercise demonstration videos via YouTube links and text-based coaching cues. Use when client doesn't know an exercise, asks for form guidance, or new exercises are introduced."
---

# Exercise Demonstration

This skill provides clients with high-quality visual and technical guidance for performing exercises safely and effectively.

## Workflow

1.  **Identify Need:** Trigger this skill when a client is unfamiliar with an exercise, requests form guidance, or when a new exercise is added to their program.
2.  **Search for Video:** ALWAYS search the web for a relevant YouTube video demonstration and include the link in the response. Do not skip this step.
    - **Criteria:** Prioritize channels known for technical accuracy (e.g., Renaissance Periodization, Jeff Nippard, Squat University).
    - **Duration:** Ideally under 5 minutes.
    - **Content:** Should show proper form and mention common mistakes.
    - **Method:** Use web search to find the video URL. Include the full YouTube link in the response.
3.  **Provide Coaching Cues:** Select **3-5 key text-based coaching cues** that are easy to remember and implement.
4.  **Highlight Mistakes:** Identify **1-2 common mistakes** to avoid.
5.  **Form Check Feedback:** If the client sends a video of themselves performing the exercise:
    - Provide constructive, encouraging feedback.
    - Focus on the **1-2 most important corrections** first to avoid overwhelming them.
6.  **Present:** Use the format in `templates/exercise_demo_template.md`.

## Best Practices

- **Clarity:** Use simple, actionable language for cues (e.g., "Pull your shoulder blades into your back pockets" instead of "Retract and depress the scapula").
- **Encouragement:** Always frame corrections positively (e.g., "You're doing great with the depth! Let's just focus on keeping the chest a bit higher on the next set").
- **Safety First:** If an exercise seems too advanced or risky for a client's current level/injuries, suggest a safer alternative from the `exercise-library`.

## Resources

- `templates/exercise_demo_template.md`: The standard format for providing exercise demonstrations and cues.
