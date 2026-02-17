# AI Physique Coach

A complete skill library for turning Manus into an evidence-based physique coach. Covers onboarding, training programming, nutrition, daily/weekly check-ins, progress tracking, and more.

## What This Is

This is a collection of 23 modular skills that give a Manus agent the knowledge and workflows to act as a personal physique coach. Each skill is a self-contained folder with instructions, templates, and references that the agent follows when handling specific coaching tasks.

The system is designed around science-based principles of hypertrophy, fat loss, and body recomposition. It uses a component-based TDEE calculation (Cunningham BMR, separate PAL, training expenditure, step expenditure, and thermic effect of food), double progression for training, and structured check-in workflows for accountability.

## Skills Overview

### Onboarding & Setup
| Skill | Description |
| :--- | :--- |
| `coaching-info` | First contact — explains coaching capabilities and guides clients to intake |
| `physique-coach-onboarding` | Comprehensive client intake process covering physical profile, goals, training history, nutrition, lifestyle, and medical history |
| `tdee-calculation` | Component-based TDEE using Cunningham BMR, PAL, training EE, step EE, and TEF |
| `goal-setting-milestones` | Sets targets and timeline during onboarding, revisited monthly |

### Program Building
| Skill | Description |
| :--- | :--- |
| `diet-recommendation` | Calorie and macro targets based on TDEE and goal (protein at 0.75-0.82g per lb of goal bodyweight) |
| `resistance-training-program` | Custom training programs with double progression and RIR-based intensity |
| `cardio-programming` | Step targets and optional LISS cardio |
| `excel-tracker` | Creates and manages the client's master Excel tracking file locally |

### Daily Use
| Skill | Description |
| :--- | :--- |
| `daily-check-in` | Morning and evening data collection — weight, sleep, stress, calories, protein, steps |
| `meal-photo-estimator` | Estimates calories and macros from food photos or text-based ingredient lists |
| `meal-planner` | Meal suggestions and recipes fitting macro targets |
| `exercise-demonstration` | Form guidance with YouTube video links |

### Weekly & Periodic
| Skill | Description |
| :--- | :--- |
| `weekly-check-in` | Sunday review analyzing the week's data with coaching feedback |
| `sleep-stress-check-in` | Monitors recovery trends and modifies training when needed |
| `program-update` | Evidence-based adjustments to training, nutrition, and cardio every 4-6 weeks |
| `progress-photos` | Biweekly/monthly photo collection and comparison |
| `phase-transition` | Manages switches between cut, maintenance, and lean bulk phases |
| `deload-fatigue-management` | Reactive deloads when lifts stall despite adequate recovery |
| `supplements` | Evidence-based supplement recommendations |

### Situational
| Skill | Description |
| :--- | :--- |
| `motivation-accountability` | Proactive accountability when client goes dark or needs a push |
| `injury-pain-modification` | Training modifications when client reports pain or injury |
| `travel-accommodations` | Maintains training and nutrition adherence while traveling |
| `lifestyle-integration` | Coaches on fitting fitness into work, family, and social life |

## How to Import to Your Manus Agent

1. Download the skill folders from this repo (either clone the repo or download as ZIP)
2. Each skill is a `.skill` file or a folder — both work
3. Open your Manus chat (Telegram, web, etc.)
4. Drag and drop the skill folders or `.skill` files directly into the chat
5. Tell Manus to install them — e.g., "Add all these skills to your arsenal"
6. Manus will unpack and install them automatically

That's it. Once installed, you can tell Manus to onboard you as a new client and it will walk you through the full intake process using these skills.

## Key Design Decisions

- **TDEE Calculation:** Uses Cunningham (1991) BMR based on fat-free mass, not total bodyweight. Separates daily activity (PAL), training expenditure, step expenditure, and thermic effect of food into independent components rather than a single crude multiplier.
- **Protein Targets:** Set at 0.75-0.82g per lb of goal bodyweight (not current bodyweight).
- **Progression Model:** Double progression with RIR (Reps in Reserve) as the default intensity metric. Weight increases when the client hits the top of the rep range on their last set at target RIR.
- **Tracking:** All data is tracked locally via Excel (openpyxl) to minimize API costs. The updated file is sent back to the client after every edit for verification.
- **Check-ins:** Morning check-in (sleep, weight, stress) + evening check-in (steps, calories, protein) + weekly Sunday review.
- **Lean Bulking:** Eat at calculated maintenance. It takes very few extra calories to build muscle, and at maintenance you'll naturally end up in a slight surplus.

## License

Open source. Use however you want.
