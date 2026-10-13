# Chai Rush — Nazaakat Edition

Live demo: https://yarragudisrinivasreddy.github.io/Chai-Rush/

A Hyderabad-themed catch game built for the Vibe Coding Lounge hackathon, Challenge 1. Catch falling Osmania biscuits and Irani chai before the timer runs out — played with mouse, keyboard, or your webcam.

## Challenge

Challenge 1 asked for a fast-paced incremental clicker where players catch falling Osmania biscuits or brew continuous cups of Irani chai before a timer runs out. This answers that, and borrows two ideas from the Biryani Challenge: a rare "secret" jackpot item and local slang in place of generic system messages.

## Features

- Falling Osmania biscuits (+10) and Irani chai (+25, builds a combo multiplier), with a bill (🧾 in-game) that costs points and resets the combo
- Rare biryani handi jackpot item, with a gold confetti burst on catch
- Two control modes: mouse/touch/arrow keys, or hands-free webcam control via MediaPipe's HandLandmarker — falls back to manual controls automatically if the camera isn't available
- Hyderabadi/Deccani slang on every catch, miss, and game-over message
- Scrolling ticker of real Hyderabad Irani-café and biryani landmarks (Pista House, Shah Ghouse, Nimrah, Café 555)
- GSAP-driven animation (cart squash-and-stretch, confetti, screen shake, overlay transitions) and procedurally generated sound effects via the Web Audio API — no external audio files

## Controls

- Mouse / touch: move the cart by moving the pointer
- Keyboard: arrow left / right
- Camera: select "Play with Camera" on the start screen and allow camera access, then move your hand left and right

## Tech stack

Vanilla HTML, CSS, and JavaScript. GSAP for animation. MediaPipe Tasks Vision (HandLandmarker) for webcam hand-tracking. Web Audio API for sound. No build step, no backend.

## Running locally

Open `index.html` directly in a browser for mouse/keyboard play. Camera mode requires HTTPS or `localhost`, so serve the folder with any static server (for example `python3 -m http.server`) rather than opening the file directly, if you want to test camera mode locally.

## Deployment

Static site, no build step. Currently hosted on GitHub Pages from the `main` branch. Also deployable to Firebase Hosting via the included `firebase.json`.
