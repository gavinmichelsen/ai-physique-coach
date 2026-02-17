---
name: excel-tracker
description: "Creates and manages the client's master tracking Excel file locally. Single source of truth for all client data. Use at onboarding (create file) and whenever data needs to be logged, read, or analyzed for coaching recommendations."
---

# Excel Tracker

This skill manages the master tracking spreadsheet as a local Excel file (.xlsx) using openpyxl. This approach is credit-efficient — no browser automation or API calls required.

## How It Works

- All client data is tracked locally in an Excel file stored in the sandbox.
- Use openpyxl (Python) to read, write, and update the file.
- When making coaching recommendations, program updates, or check-in feedback, always read the tracker first and perform any necessary calculations (averages, trends, rate of change) to inform data-driven decisions.
- Send the updated file to the client as an attachment after edits so they can preview or upload to their own Google Drive.

## Sheet Structure

The master file consists of five tabs:

1. **Daily Log:** Date, Weight (lbs), Sleep Duration (hrs), Sleep Quality (1-10), Stress (1-10), Steps, Calories, Protein (g), Notes.
2. **Training Log:** Date, Session Name, Exercise, Set 1-4 (Weight x Reps @RIR), Notes.
3. **Weekly Averages:** Week Start Date, Avg Weight, Avg Steps, Avg Calories, Avg Protein, Avg Sleep Duration, Avg Sleep Quality, Avg Stress, Weight Change vs Last Week, Weight Change vs Week 1.
4. **Measurements:** Date, Waist (belly button), Chest (fullest part), Arms (flexed, bicep peak), Notes.
5. **Program History:** Start Date, End Date, Phase, Calorie Target, Protein Target, Training Split, Notes.

Refer to `templates/sheet_schema.md` for detailed column definitions.

## Workflow

### Logging Data
- Use openpyxl to append rows to the appropriate tab.
- Morning check-ins: log weight, sleep, stress to Daily Log.
- Evening check-ins: fill in steps, calories, protein for the same day's row.
- Training sessions: append to Training Log.
- Measurements: append to Measurements tab every 2-4 weeks.

### Reading Data for Recommendations
- Before any program update, weekly check-in, or coaching recommendation, read the tracker and calculate relevant trends (weight averages, rate of loss, adherence rates, etc.).
- Use Python for all calculations — do not estimate mentally.

### Delivering Updates
- After any edit, save the file, re-read it with openpyxl to verify the data was written correctly, and ALWAYS send the updated file back to the client as an attachment. The client must be able to verify the data is logged. Never claim data was logged without actually writing it to the file and providing proof.

## Resources

- `templates/sheet_schema.md`: Detailed schema and measurement instructions.
