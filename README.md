# dotspin

15 dot-matrix CSS spinners. One element each. Zero JS. Zero dependencies.

**[Live demo →](https://naklitechie.github.io/dotspin/)**

---

## Usage

```html
<link rel="stylesheet" href="dotspin.css">

<i class="dotspin dotspin--orbit"></i>
<i class="dotspin dotspin--braille"></i>
<i class="dotspin dotspin--pulse"></i>
```

## Spinners

| Class | Description |
|---|---|
| `dotspin--braille` | 6-dot braille cell fills then empties |
| `dotspin--orbit` | single dot circles a 3×3 ring |
| `dotspin--breathe` | 3×3 block expands from center, collapses |
| `dotspin--snake` | 3-dot snake slithers through the grid |
| `dotspin--fill-sweep` | columns fill left-to-right, then drain |
| `dotspin--pulse` | center dot pulses against an outer ring |
| `dotspin--columns` | columns shift independently |
| `dotspin--checkerboard` | checkerboard inverts each step |
| `dotspin--scan` | column of dots sweeps left to right |
| `dotspin--rain` | dots fall at random positions |
| `dotspin--cascade` | activation cascades diagonally |
| `dotspin--sparkle` | scattered dots shift pseudo-randomly |
| `dotspin--wave-rows` | row of dots sweeps top to bottom |
| `dotspin--helix` | alternating diagonal strands cross |
| `dotspin--diagonal-swipe` | anti-diagonal wipes across and off |

## Customise

Three CSS variables plus `color`:

```css
.dotspin {
  --dotspin-size: 64px;   /* default: 1em — scales the whole thing */
  --dotspin-speed: 0.9s;  /* default: 1.2s */
  color: #ff5733;         /* dots use currentColor */
}
```

Override on any element or a parent — no build step needed.

## How it works

Each spinner is a single element. `::before` paints an anchor dot; `box-shadow` places (or hides) the other dots on an invisible 5×5 grid. Keyframes step through frames with `steps(1, end)` — no layout reflow, no JS, no SVG.

`prefers-reduced-motion` is respected: animations stop and the grid renders static.

## License

MIT © Chirag Patnaik

Inspired by [gunnar gray's unicode-animations](https://github.com/gunnargray-dev/unicode-animations).
