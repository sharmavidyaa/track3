# Burnout & Stress Radar

Team Hackkennes · wHACKiest 2026 · Track: Know Thyself

A personal early-warning tool that combines body signals (sleep, resting heart rate, HRV), phone habits (late-night screen time) and calendar load (meetings) into one daily strain score, finds patterns in them, and gives a timely nudge. **Everything runs in the browser. No data is sent anywhere.**

## Run it
Open `index.html` in any browser (no install, no server). Or host it free with GitHub Pages.

## Try it
1. Click **Load 30 days of demo data** (synthetic data), or **Import CSV** with columns: `date,sleep_h,rhr,hrv,late_screen_min,meetings,steps`.
2. See today's strain score against your own baseline and the trend chart.
3. Read the detected patterns (correlations, with the number of days they are based on).
4. Change "Meetings tomorrow" to see the nudge change. **Read it aloud** uses the browser's built-in speech.
5. Open **What the AI saw** to see the only summary that would ever leave the device. **Wipe all data** deletes everything.

## How it works
- Strain score: HRV, resting HR and sleep compared with the user's own baseline (z-scores), scaled 0-100.
- Patterns: Pearson correlations (late screens → next-day HRV, meetings → sleep, sleep → next-day resting HR).
- Nudge: rule-based, using today's strain, late-screen time and tomorrow's meetings.
- Storage: browser localStorage only.

## Planned (see the PPT)
Opt-in cloud assist through AWS Lambda and Amazon Bedrock (anonymized summary only) and ElevenLabs voice nudges. The demo uses the browser's speech synthesis in the meantime.

Demo data is synthetic. This is a wellness awareness tool, not a medical device.
