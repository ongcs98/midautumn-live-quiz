# Mid-Autumn Live Quiz V3

V3 keeps the V2 live multiplayer features and adds a **Saved Quiz / Question Bank** workflow.

## New in V3

- Create multiple saved quizzes before the event.
- Save quiz title, time limit, A/B/C/D questions, and correct answers.
- Questions auto-save in the admin browser.
- Reorder questions with Up / Down buttons.
- Duplicate a quiz.
- Export a quiz to JSON for backup.
- Import a saved JSON quiz backup.
- On event day, open a saved quiz and press **Start New Room**.
- A new room code + QR code is generated and the saved quiz is copied into the live room.

## Important: where saved quizzes are stored

V3 saves the question bank in **browser localStorage on the admin computer**. This is intentional so the quiz survives Render server sleeping/restarting and does not require a separate database.

Use the **same browser/computer** for preparation and the event. After preparing the real questions, click **Export 备份** and keep the JSON file somewhere safe. If you switch computers or clear browser/site data, use **Import 题库** to restore it.

## Deploy / update from V2

1. Replace the files in your existing GitHub repository with the V3 files.
2. Commit the changes.
3. Render should automatically redeploy the existing service.
4. Keep the existing Render environment variable:
   - `ADMIN_PASSWORD=your-password`
5. Open `/admin.html`.

## Event-day workflow

1. Open `/admin.html` on the admin laptop.
2. Open your saved quiz.
3. Confirm all questions.
4. Enter Admin Password.
5. Click **Start New Room**.
6. Open the display page on the projector.
7. Guests scan the QR code / enter the Room Code.
8. Start the game when everyone is ready.

## Scoring

For a correct answer:
- 1,000 base points
- Up to 1,000 additional speed points

Wrong answer: 0 points.

Leaderboard order:
1. Total score
2. Correct answers
3. Lower total answering time
4. Earlier join time

## Recommendation for the actual dinner

Export a backup after the final question set is ready. Test with at least 5 phones before the event. For around 130 participants, use a paid/non-sleeping Render instance during the dinner if possible.
