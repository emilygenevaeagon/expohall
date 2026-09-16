# Wisconsin or Wishconsin?

A booth-friendly League of Wisconsin Municipalities game for Civic Connection / expo-hall use.

## Live deployment

This folder is designed to run as a static GitHub Pages site. No build tools or dependencies are required.

## Game design

- Six questions per game
- Two City/Village questions, two Town questions, and two Made Up questions
- 72-question bank total: 24 in each category
- Real places are plotted on a Wisconsin locator map after the answer is revealed
- Touch-friendly and keyboard-friendly controls
- Responsive for a booth laptop, tablet, or large display

## Data verification

Real places and coordinates were checked against U.S. Census Bureau TIGERweb data dated January 1, 2026. Fake names were checked against both the Wisconsin incorporated-place and county-subdivision tables so they do not match a current Wisconsin city, village, or town.

## Branding

The page uses the League palette supplied for this project:

- Navy: `#19286B` (RGB 25, 40, 107)
- Gold: `#FDB714` (RGB 253, 183, 20)
- Light blue: `#96C0E6` (RGB 150, 192, 230)
- Green: `#B4BE35` (RGB 180, 190, 53)
- Magenta: `#B01E58` (RGB 176, 30, 88)

The League logo is loaded from the existing public `expohall` GitHub Pages asset.

## Files

- `index.html` - complete game UI and logic
- `game-bank.json` - question bank
- `assets/wisconsin-map.svg` - locator map background

## Editing questions

Each record in `game-bank.json` includes:

- `question`
- `answers`
- `correctAnswer`
- `actualType`
- `county`
- `lat` / `lng`
- `difficulty`
- `reveal`

Keep the three category labels exactly as `City or Village`, `Town`, and `Made Up` unless you also update the JavaScript in `index.html`.
