# Hong Kong Monthly Temperature Matrix (CSCE 679 - Assignment 1)

This project visualizes Hong Kong temperature data as a matrix view using D3.js.

## Overview
- **Data source:** `temperature_daily.csv`
- **Time window:** last 10 years in the dataset (`2008-2017`)
- **Matrix encoding:**
  - **X-axis:** Year
  - **Y-axis:** Month
  - **Cell color:** Temperature value (with legend)
- **Inside each cell:** mini daily line charts for monthly max/min trends

## Features Implemented
- Matrix layout with year/month grid
- Hover tooltip showing month and temperature info
- Mini line charts in each cell for daily temperature changes
- Vertical legend showing color-to-temperature mapping (`0 Celsius` to `40 Celsius`)
- Click interaction to switch color mode between:
  - **Maximum temperature mode**
  - **Minimum temperature mode**

## Project Files
- `index.html` - page structure
- `styles.css` - visual styling
- `script.js` - D3 visualization logic
- `temperature_daily.csv` - input dataset

## How to Run
Use a local server (recommended, because browsers may block CSV loading from `file://`):

### Option 1: Python
```bash
python -m http.server 8000
```
Open: `http://localhost:8000`

### Option 2: VS Code Live Server
1. Open `index.html`
2. Right-click -> **Open with Live Server**

## Interaction Guide
- **Hover a cell:** see tooltip values
- **Click any cell:** toggle matrix coloring between max and min temperature modes

## Notes
- The dataset ends in late 2017, so some final month cells may be shown as missing/neutral.
- D3.js is loaded from CDN in `index.html`.

## AI Usage Reflection (Required by assignment)
I used AI assistance to:
- adjust color scale/legend consistency,

## Interaction Log
ok the first one is the example the second one is the one i implemented the colors arent really fully matching you see the color bar i want exactly this palatte of colors on the bar and also on the cells


Worked for 7m 15s
You’re right, and I fixed that.

What I changed in script.js:

Replaced the continuous color scale with a discrete stepped palette.
Used the same palette source for:
cell background colors
vertical legend blocks
Kept range fixed at 0 to 40 Celsius so the bar labels match.
This means the legend and cells now use identical bins/colors, so they should visually match much closer to your example.

If you want it even more exact, I can do one more pass where I tune the individual hex colors from your screenshot (pixel-picked), but this is now structurally correct and consistent.


