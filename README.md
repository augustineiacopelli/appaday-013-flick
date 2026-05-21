# appaday-013-flick

**AppADay · 013 · G · Game**

A pass-and-play physics puck game for two players, inspired by the classic mobile game OLO.

## What It Does

Two players take turns dragging and flicking pucks across a divided board, trying to land them in the opponent's half. Pucks bounce off all four walls including the white strips at each end. A gold blast token appears randomly in the opponent's half — hit it to trigger a shockwave that sends every puck flying. Colors randomize each game. Most pucks in the opponent's zone when all pucks are played wins.

## How to Play

1. Open the app, set how many pucks each player gets (3–9), and tap **play**.
2. Your puck appears in the white strip on your side. Touch anywhere to grab it and drag to aim — release with speed to flick.
3. Pass the phone to the other player after each turn.
4. Pucks that settle with their center in the white strip are removed and returned as a bonus puck to that side's player.
5. If a gold ★ blast token appears in your opponent's half, aim your puck at it — a shockwave will repel every puck on the board from the blast point.
6. The game ends when both players have played all their pucks. Most pucks in the opponent's colored zone wins.

## Technical Notes

- Vanilla HTML/CSS/JS — no frameworks, no dependencies
- Canvas-based physics: mass-weighted momentum exchange, wall bouncing with energy damping, puck-puck collision resolution
- Settled-puck OOB detection: puck center in white strip → removed and returned to that player's count
- Blast powerup: appears at most once per player per game, 0% chance on first turn scaling to 50% max, only when >1 puck remains, always placed in opponent's half, expires on turn change
- Six randomized color palettes chosen fresh each game
- Fully touch-enabled for iPhone and iPad; mouse support for desktop
- Responsive canvas sizing via `dvh` layout

## Definition of Complete

- [x] Two-player pass-and-play works end to end
- [x] Puck follows finger/cursor during drag; velocity sampled at release
- [x] Physics: wall bounce, puck-puck collision, friction settling
- [x] White-strip OOB rule: settled pucks returned to correct player
- [x] Uneven remaining pucks handled — player with pucks left keeps going
- [x] Blast powerup with all five specified rules implemented
- [x] Shockwave animation on blast trigger
- [x] Six randomized color palettes per game
- [x] Mobile-friendly touch controls on 375px viewport
- [x] AppADay header with home link

## Future Upgrades
- Need to fix glitch that allows a player to "pick up" and play their pucks from anywhere on the board instead of only from their end.
- Brainstorm additional upgrades that could be worked into the game
- Brainstorm player logins and upgrade store (various "surfaces" that mess with puck movement, ghost puck that can pass through other pucks, etc)
