# Touch Typing Practice

A single-file web app (`index.html`, no build step and no dependencies) that
drills the number row and symbols with a strict accuracy-first approach.

## How it trains you

- **No backspace.** Backspace and Delete do nothing.
- **Stop on error.** A wrong key does not move the cursor. You must type the
  correct key to continue, and only your *first* attempt at each character counts
  toward accuracy.
- **Immediate reinforcement.** Every key you miss is drilled again (with the
  characters around it) at the start of the next line.
- **Adaptive weighting.** Each key gets a weight from its recent error rate
  (last 30 tries) and how long you hesitate before it compared with your median
  key time. Weak and slow keys show up more often.
- **Focus keys.** Starts with `4 5 6 7 9 0`. Focus keys get extra weight until
  they are mastered (20+ tries, at least 95% accurate, and not slow). Edit the
  list in the settings bar or click keys in the *Key progress* grid.
- **Finger guide.** An on-screen keyboard colored by finger, with two
  outlined, see-through hands resting over it: fingertips on the home keys,
  thumbs on the space bar. For each key, the correct finger slides out to it,
  outlined in its finger color, and for shifted characters the other hand's
  pinky reaches for Shift. There is also a text hint for every key (for example "Left index, up two rows from F +
  Right Shift"). You can choose which index finger types `6`.
- **Lesson summary.** Shows accuracy, WPM, the keys you missed, mix-ups such as
  "typed 5 for 6", and mastery bars for your focus keys.

**Clean typing view.** While you type you see only the line, the finger hint and
the keyboard. Settings and per-key Progress sit behind two buttons in the
header. They close as soon as you start typing, and the header fades until you
move the mouse.

Drill modes: Adaptive (numbers + symbols + some words), Numbers only, Symbols,
Code & data, and Focus keys only.

Progress is saved in your browser's `localStorage`, so it is per browser and
per device.

## Use it

Live at **https://mukizar.github.io/touch-typing-practice-app/** (GitHub
Pages, deployed from `main`). Every push to `main` redeploys it within a
minute or two.

To run it locally, open `index.html` in a browser. There is no build step.

It assumes a **US QWERTY** layout. On "US International" or other layouts with
dead keys, switch to plain US so `'`, `"`, `` ` ``, `~` and `^` register on
the first press.

## Practice tips

1. Keep your fingers anchored on `F` and `J` (feel the bumps), and reach up to
   the number row without moving your whole hand.
2. Go slowly enough to make zero mistakes. Speed follows accuracy.
3. Use *Focus keys only* for 5 minutes as a warm-up, then switch to *Adaptive*.
