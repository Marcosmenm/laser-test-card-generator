# Laser Test Card Generator

**Free browser-based laser engraver calibration tool.** Find the perfect power and speed for any material — no install, no account.

🔗 **[Open the tool → marcosmenm.github.io/laser-test-card-generator](https://marcosmenm.github.io/laser-test-card-generator/)**

Promoted by **[Tag My Link](https://tagmy.link)** — the digital business card platform with physical QR tag integration.

---

## What is a laser test card?

A test card burns a grid of small cells onto your material, varying **laser power** across columns and **engraving speed** across rows. Each cell shows you what that combination looks like — making it fast to dial in the right settings for wood, acrylic, leather, cardboard, anodized aluminium, and more.

## Features

- **Live preview** — see the card update as you type
- **Responsive grid** — works cleanly from 2×2 to 20×20 cells
- **Outline or filled mode** — quick burn test or depth/contrast test
- **Adjustable hatch resolution** — control scanline density (lines/mm)
- **G-code download** — click the preview or button to save a `.nc` file
- **Zero dependencies** — single HTML file, works offline

## How to use

1. Open [index.html](index.html) in any browser (or use the [live link](https://marcosmenm.github.io/laser-test-card-generator/))
2. Enter your card size in mm
3. Set the power and speed ranges to test
4. Choose Outline or Filled mode
5. Click the card preview to download `TestCard.nc`
6. Load in **LaserGRBL**, frame, and burn
7. Pick the lightest cell with a clean mark — those are your settings

## Parameters

| Field | Description |
|---|---|
| Size X / Y (mm) | Physical card size |
| Columns / Rows | Power steps × Speed steps |
| Min / Max Speed (mm/min) | Speed range across rows |
| Min / Max Power (0–1000) | Power range across columns (1000 = 100%) |
| Filled | Hatch-fill cells instead of outlines |
| Resolution (lines/mm) | Hatch density when filled |

## Compatibility

- Works in Chrome, Firefox, Safari, Edge
- G-code targets **LaserGRBL** (`M4`/`M5` variable power mode)
- Adjust `header` / `footer` in source for other controllers (LightBurn, etc.)

---

## For engravers

If you engrave QR codes, business cards or tags for clients, **Tag My Link's partner program** lets you batch-generate branded QR tags, white-label the customer-facing PDFs, and offer a turnkey digital business card on top of every piece you sell. → [tagmy.link](https://tagmy.link)

---

## About this fork

Forked from [LsrSal/Laser_Test_Card_Generator](https://github.com/LsrSal/Laser_Test_Card_Generator). Original concept and G-code logic by LsrSal.

**Changes in this fork:**
- Full redesign — SaaS-style landing + embedded tool in a single page
- Responsive grid scales correctly for any column/row count
- Live preview with auto-fit canvas
- Cleaner G-code output (coordinate precision, header fix)
- Tag My Link branding and partner program integration

Original file preserved as `TestCardGenerator2.html`.

Licensed under [GPL-3.0](LICENSE).
