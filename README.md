# 🏎️ TypeRace Live — 2 Player Typing Racing Game

A real-time **2-player typing speed race**. Both players get the **same text**, race for **1 minute**, and the fastest (most correct) typist wins. Every race uses a **brand-new random text** from a bank of 25.

## How to play
1. **Host:** enter your name → **Create Room** → share the 6-letter code or invite link.
2. **Friend:** enter name + code → **Join Room**.
3. Host presses **Start Race** → 3-2-1-GO countdown → type!
4. Your car moves as you type correctly. Live WPM, accuracy and rival speed shown.
5. After 60 seconds (or when the text is finished) the winner is declared. Hit **Rematch** for a fresh text.

No friend around? Use **Solo Race vs Bot** 🤖 to practice against a robot racer.

## Tech
- Single-file static web app (`index.html`) — no build step, no backend cost.
- Real-time multiplayer via **WebRTC (PeerJS)** peer-to-peer data channels — host/guest connect directly with a room code.
- Anti-cheat: paste is blocked, big pasted chunks are rejected.
- Scoring: winner = most correct characters in 60s, tie-break on accuracy, then WPM.

## Run locally
Just open `index.html` in a browser, or:
```bash
npx serve .
```

## Deploy
- **Vercel:** import this repo in Vercel (framework preset: *Other*, no build command) — done.
- **GitHub Pages:** Settings → Pages → deploy from `main` branch root.
