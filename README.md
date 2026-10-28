# Guess Battle

A responsive four-clue guessing game with AI practice mode and a real-time, two-player room mode.

## Run locally

1. Install Node.js 18 or newer.
2. In this folder, run `npm install`.
3. Run `npm start`.
4. Open `http://localhost:3000`.

For friends to connect from different devices, deploy this Node.js app to a host that supports persistent WebSocket connections (for example, Render, Railway, or a VPS). Share the deployed public URL, then one player creates a room and shares the five-character room code.

## Included
- Set a player name/profile display
- AI practice mode (10 rounds)
- Friend rooms with a room code and live Socket.IO updates
- Four clues, one at a time; 15-second timer per clue
- Answer submission and clue-giver judging
- Correct answer +1; incorrect/no answer after fourth clue −1
- Responsive mobile-friendly UI

## Notes
- The room state is held in server memory. Restarting the server clears active rooms; this is a prototype, not a persistent service.
- The AI mode is a local practice prototype: it checks the submitted answer against the secret answer and does not use a remote AI model.
- This MVP uses a starter set of 15 questions. Expand the `BANK` list in `server.js` and `public/index.html` for more content.
