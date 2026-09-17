# Mid-Autumn Live Quiz V2

Event-ready realtime quiz for a dinner or association event.

## V2 features
- Admin creates A/B/C/D questions and chooses the correct answer
- Correctness + response speed scoring
- QR-code joining
- Dedicated projector/display page
- Admin password
- Reconnect protection using a private player token stored on the participant's phone
- Duplicate-name protection
- Manual answer reveal
- Live answer count and A/B/C/D statistics
- Top 10 leaderboard and final podium/ranking

## Deploy on Render
1. Upload all project files to your GitHub repository.
2. In Render, create/update a Node Web Service for that repository.
3. Build command: `npm install`
4. Start command: `npm start`
5. Add an Environment Variable in Render:
   - Key: `ADMIN_PASSWORD`
   - Value: choose your own private password, e.g. a strong event password.
6. Deploy.

Participant URL: `https://YOUR-SITE.onrender.com/`
Admin URL: `https://YOUR-SITE.onrender.com/admin.html`
Projector URL: open it from the Admin page after creating the room.

## Scoring
Correct answer: 1,000 base points + up to 1,000 speed points.
Wrong answer: 0 points.
Ranking tie-break: total score, correct answers, then lower total response time.

## Important event notes
- Test with several phones before the event.
- Use a reliable paid Render instance for a ~130-person live event rather than a sleeping/free instance.
- Have the admin laptop on stable internet; participants can use venue Wi-Fi or mobile data.
- Rooms are kept in server memory. Restarting/redeploying the server clears the current room, questions and scores. Prepare questions in advance but avoid redeploying during the event.
