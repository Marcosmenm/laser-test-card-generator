# LaserGRBL Test Card Generator

**Free browser-based G-code test card generator for laser engravers.**  
Find the perfect power and speed settings for any material — no software to install.

🔗 **[Live tool → marcosmenm.github.io/laser-test-card-generator](https://marcosmenm.github.io/laser-test-card-generator/)**

---

## What is a laser test card?

A test card burns a grid of small cells onto your material, varying **laser power** across columns and **engraving speed** across rows. Each cell shows you exactly what that power/speed combination looks like — making it fast to dial in the right settings for wood, acrylic, leather, cardboard, anodized aluminium, and more.

## Features

- **Live preview** — see the card layout update as you type
- **Responsive grid** — works cleanly from 2×2 to 20×20 cells and beyond
- **Outline or filled mode** — outline for a quick burn test, filled for depth/contrast testing
- **Adjustable fill resolution** — control scanline density (lines/mm) for filled mode
- **G-code download** — click the preview or the Download button to save a `.nc` file ready for LaserGRBL
- **Zero dependencies** — single HTML file, works offline, no server needed

## How to use

1. Open [index.html](index.html) in any browser (or use the [live link](https://marcosmenm.github.io/laser-test-card-generator/))
2. Enter your card size in mm (measure your scrap material)
3. Set the power and speed ranges you want to test
4. Choose Outline or Filled mode
5. Click the card preview to download `TestCard.nc`
6. Load in **LaserGRBL**, frame, and burn

## Parameters

| Field | Description |
|---|---|
| Size X / Y (mm) | Physical card size — match your scrap material |
| Columns / X | Number of power steps (typically 5–10) |
| Rows / Y | Number of speed steps (typically 5–10) |
| Min / Max Speed (mm/min) | Speed range — rows go from fast (top) to slow (bottom) |
| Min / Max Power (0–1000) | Power range — columns go from low (left) to high (right). 1000 = 100% |
| Filled | Hatch-fill cells instead of outlines |
| Fill resolution (lines/mm) | Scanline density when Filled is on |

## Reading the results

After burning, look for the lightest cell that still produces a **clean, consistent, fully-burnt mark**. That's your optimal setting. Cells that are too light = underpowered or too fast. Cells that are charred or blow-through = too powerful or too slow.

## Compatibility

- Works in Chrome, Firefox, Safari, Edge
- G-code targets **LaserGRBL** (`M4`/`M5` variable power mode)
- Adjust the `header` / `footer` variables in the source for other controllers (LightBurn, etc.)

---

## About this fork

Forked from [LsrSal/Laser_Test_Card_Generator](https://github.com/LsrSal/Laser_Test_Card_Generator) — original concept and G-code logic by LsrSal.

**Changes in this fork:**
- Responsive grid — cell size scales correctly for any column/row count
- Proper margins reserved for axis labels at all grid sizes
- Font and stroke width scale with cell size
- Auto-fit preview canvas
- 3-pane UI (controls / preview / G-code)
- G-code coordinate precision fix and header typo fix

Original file preserved as `TestCardGenerator2.html`.

Licensed under [GPL-3.0](LICENSE).
