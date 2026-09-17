# Mid-Autumn Live Quiz

A real-time multiplayer quiz for a dinner/event. One admin controls the game; participants join from their phones using a 6-character room code.

## Features
- Admin can create questions with 4 choices (A/B/C/D) and mark the correct answer.
- 5-60 second timer per question (default 15 seconds).
- Every participant answers independently on their own phone.
- Correct answer: 1,000 base points + up to 1,000 speed bonus points.
- Wrong answer: 0 points.
- Ranking: total score, then correct-answer count, then total answer time.
- Live leaderboard and final Top 20.
- Room codes allow multiple games on one server.
- Works on desktop + mobile browsers.

## Run locally
1. Install Node.js 18+.
2. In this folder run: `npm install`
3. Run: `npm start`
4. Open `http://localhost:3000/admin.html` on the host laptop.
5. Participants open `http://localhost:3000` and enter the room code.

## Put it online (Render - simple method)
1. Create a free GitHub account/repository if you do not already have one.
2. Upload all files in this project to the repository.
3. In Render, create a **Web Service** from that repository.
4. Build command: `npm install`
5. Start command: `npm start`
6. Deploy. Render will give you a public HTTPS address such as `https://your-quiz.onrender.com`.
7. Admin opens `/admin.html`; participants open the main address and enter the room code.

The included `render.yaml` can also be used as a Render Blueprint.

## Important for the actual dinner
Use stable venue Wi-Fi or a dedicated 4G/5G hotspot. Around 130 connected phones is fine for this application, but the venue network quality matters. Test it at the venue before the event.

## Data
Rooms and scores are stored in server memory. If the server restarts, active rooms are cleared. This is intentional for an event-night app and keeps setup simple.
