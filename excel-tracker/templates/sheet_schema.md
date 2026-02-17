# Physique Coach Master Tracker Schema

This schema defines the structure for the client's master tracking spreadsheet.

## Tab 1: Daily Log
**Purpose:** Daily tracking of weight, nutrition, and recovery metrics.
- **Date:** (Date)
- **Weight (lbs):** (Number) - Taken first thing AM after bathroom, before eating.
- **Steps:** (Number)
- **Calories:** (Number)
- **Protein (g):** (Number)
- **Sleep Duration (hrs):** (Number)
- **Sleep Quality (1-10):** (Number)
- **Stress (1-10):** (Number)
- **Notes:** (Text)

## Tab 2: Training Log
**Purpose:** Tracking progressive overload across training sessions.
- **Date:** (Date)
- **Session Name:** (Text)
- **Exercise:** (Text)
- **Set 1:** (Weight x Reps @RPE)
- **Set 2:** (Weight x Reps @RPE)
- **Set 3:** (Weight x Reps @RPE)
- **Set 4:** (Weight x Reps @RPE)
- **Notes:** (Text)

## Tab 3: Weekly Averages
**Purpose:** High-level trend analysis for check-ins and program updates.
- **Week Start Date:** (Date)
- **Avg Weight:** (Auto-calculated)
- **Avg Steps:** (Auto-calculated)
- **Avg Calories:** (Auto-calculated)
- **Avg Protein:** (Auto-calculated)
- **Avg Sleep Duration:** (Auto-calculated)
- **Avg Sleep Quality:** (Auto-calculated)
- **Avg Stress:** (Auto-calculated)
- **Weight Change vs Last Week:** (Auto-calculated)
- **Weight Change vs Week 1:** (Auto-calculated)

## Tab 4: Measurements
**Purpose:** Tracking body composition changes via circumference measurements.
- **Date:** (Date)
- **Waist:** (Number)
- **Chest:** (Number)
- **Left Arm:** (Number)
- **Right Arm:** (Number)
- **Hips:** (Number)
- **Left Thigh:** (Number)
- **Right Thigh:** (Number)
- **Notes:** (Text)
*Note: Measured every 2-4 weeks, morning, relaxed, same location each time.*

## Tab 5: Program History
**Purpose:** Historical log of all training and nutrition phases.
- **Start Date:** (Date)
- **End Date:** (Date)
- **Phase:** (Cut / Bulk / Maintenance)
- **Calorie Target:** (Number)
- **Protein Target:** (Number)
- **Training Split:** (Text)
- **Notes:** (Text)
