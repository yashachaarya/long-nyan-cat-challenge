# Long Nyan Cat Challenge

A horizontally-scrolling Nyan Cat tribute to [longdogechallenge.com](https://longdogechallenge.com).
Scroll right (or use the mouse wheel — it's translated) and watch the rainbow trail grow.

## Live demo

Once GitHub Pages finishes building: https://yashachaarya.github.io/long-nyan-cat-challenge/

## How it works

- Cat starts 1/4 from the right of the viewport at scroll=0, vertically centered, facing left. As you scroll right, the cat slides off to the left and the rainbow fills the screen.
- Rainbow trail extends to the right. The document grows horizontally as more
  `.rainbow-piece` blocks are appended via `IntersectionObserver` watching the
  current last piece — same growth pattern as the Long Doge Challenge but
  rotated 90 degrees.
- Mouse wheel `deltaY` is translated to horizontal scroll (the only deviation
  from "no wheel hijack" — required because a wheel mouse only emits vertical
  delta and our scroll axis is horizontal).
- Arrow keys, PageUp/Down, Home/End, Space, and trackpad horizontal swipe all
  scroll natively.
- Click "CLICK TO PRINT!" to print the rainbow across multiple landscape pages.

## Credits

- Cat sprite: [Gowee/nyancat-svg](https://github.com/Gowee/nyancat-svg) (MIT) — animated 6-frame pixel Nyan Cat.
- Inspired by [Tim Holman](https://twitter.com/twholman)'s
  [Long Doge Challenge](https://longdogechallenge.com).

## Local dev

```sh
npx serve -l 8092 .
open http://localhost:8092/
```
