# LaserGRBL Test Card Generator

Test card generator for laser engravers — creates a power vs speed grid to find optimal settings for any material.

Written in pure HTML+JS. No installation needed, just open `index.html` in a browser.  
Click the preview (or the Download button) to save the `.nc` file, then load it in LaserGRBL.

---

## Improvements in this fork

- **Responsive grid** — cell size scales correctly for any column/row count; no more broken layout with high row counts
- **Proper margins** — space reserved for axis labels regardless of grid size
- **Font + stroke scaling** — labels and cell borders adapt to cell size
- **Auto-fit preview** — canvas scales to fit the screen
- **3-pane UI** — controls / preview / G-code side by side
- **G-code fixes** — header typo fixed, coordinates use `.toFixed(3)`, scanlines use correct cell dimensions

Original file (`TestCardGenerator2.html`) is kept in the repo unchanged.

---

## Usage

| Field | Description |
|---|---|
| Size X / Y (mm) | Physical card size — match your material |
| Columns / X | Number of power steps |
| Rows / Y | Number of speed steps |
| Min / Max Speed (mm/min) | Speed range across rows |
| Min / Max Power (0–1000) | Power range across columns (1000 = 100%) |
| Filled | Hatch-fill cells instead of outlines |
| Fill resolution (lines/mm) | Hatch density when Filled is on |

Darker cell = higher power. Top rows = fastest speed (less burn). Bottom rows = slowest (more burn).

---

## Original

Forked from [LsrSal/Laser_Test_Card_Generator](https://github.com/LsrSal/Laser_Test_Card_Generator).  
Original concept and G-code logic by LsrSal. Licensed under GPL-3.0.
