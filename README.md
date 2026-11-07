# Roll20 Wide Character Sheet Style

A lightweight Chrome extension that enhances Roll20 character sheets for wide and ultrawide monitors.

## Overview

When you pop out a character sheet from Roll20 (right-click → "Pop out character sheet"), this extension adjusts the layout to better utilize the available screen width. It's especially useful for multi-monitor setups where you want the character sheet to fill a larger portion of the screen.

## Features

- **Expanded character sheet width** — the popped-out sheet expands to fit wide windows
- **Side-by-side columns** — columns are laid out horizontally instead of stacked vertically
- **Flexible traits & proficiencies** — traits and proficiencies wrap naturally across the wider layout
- **Responsive stat blocks** — ability scores and other stat rows stretch to fill available space

## Installation

1. Open Chrome (or a Chromium-based browser) and navigate to `chrome://extensions/`
2. Enable **Developer mode** (toggle in the top-right corner)
3. Click **"Load unpacked"**
4. Select this project's root directory

The style will automatically apply to any popped-out character sheet at `https://app.roll20.net/editor/character/*`.

## Usage

1. Open a character sheet in Roll20
2. Right-click the sheet tab and choose **"Pop out character sheet"**
3. Resize the window to your liking — the layout adapts automatically for wider windows

> **Tip:** Works best on screens 1441px wide or larger.

## Technical Details

This extension uses a **Manifest V3** content script to inject custom CSS into popped-out character sheet windows. The CSS:

- Changes the sheet layout from vertical stacking to a horizontal flexbox layout
- Fixes column widths for the left (col1) and middle (col2) columns at 247px
- Allows the right column (col3) to expand freely, filling remaining space
- Wraps traits, proficiencies, and ability scores in flexible rows with 10px gaps

## Files

| File | Description |
|------|-------------|
| `manifest.json` | Chrome extension manifest (Manifest V3) |
| `style.css` | Custom CSS rules applied to character sheets |

## License

MIT
