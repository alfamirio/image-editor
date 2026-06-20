# Image Editor

A single-page, browser-based image editor. No build step, no server, no dependencies to install — open `index.html` in a browser and start editing.

## Features

- Drag-and-drop, click-to-browse, or paste (`Ctrl+V` / `Cmd+V`) image loading
- Freehand drawing, shapes (rectangle, ellipse, line, arrow), text labels, and numbered map-style markers
- Censor tool to blur/redact regions of an image
- Crop and resize (by scale, max dimensions, or exact size with multiple fit modes)
- One-click black & white toggle and 90° rotation
- Undo / redo history
- Side-by-side **Preview** comparing the original image against your edited version, sized to fill the screen
- Copy the edited image straight to the clipboard
- Export as PNG, JPEG, or WebP with adjustable quality

## Getting Started

1. Open `index.html` in any modern browser (Chrome, Edge, Firefox, Safari).
2. Load an image by:
   - Dragging it onto the drop zone or the canvas, or
   - Clicking the drop zone to browse for a file, or
   - Pasting an image from your clipboard.
3. Pick a tool from the **Draw & Edit** panel and start editing.
4. Use **Preview** to compare your edit against the original, **Copy** to send the result to your clipboard, or **Export** to download the file.

## Tools

| Tool | Shortcut | Description |
|---|---|---|
| Select / Move | `V` | Default tool; pan/inspect without drawing |
| Pen | `P` | Freehand drawing |
| Rectangle | `R` | Draw a rectangle (filled or outlined) |
| Ellipse | `O` | Draw an ellipse or circle |
| Line | `L` | Draw a straight line |
| Arrow | `A` | Draw an arrow |
| Text | `T` | Place a text label |
| Marker | `N` | Place a numbered marker (auto-increments) |
| Censor | `B` | Blur/redact a rectangular region |
| Crop | `C` | Drag to select a crop region, then apply |
| Resize | `S` | Scale or resize the canvas |
| Black & White | `W` | Toggle grayscale |
| Rotate 90° | `Shift+R` | Rotate the canvas clockwise |
| Zoom / Pan | `Z` | Zoom and pan around the canvas |

> Shortcuts are disabled while typing in a text field, and `R` alone selects the Rectangle tool — use `Shift+R` to rotate.

### Tool options

Depending on the active tool, the right-hand panel exposes:

- **Color** — stroke color, fill color, and a fill toggle for shapes
- **Stroke width & opacity** — for pen, shapes, lines, and arrows
- **Text** — content, size, and font family
- **Blur strength** — for the censor tool
- **Marker size** — and a button to reset the numbering sequence
- **Crop** — an "Apply Crop" button once a region is selected
- **Resize** — mode selector (scale / max dimensions / exact size), plus a fit mode for exact-size resizing

## Keyboard Shortcuts

| Shortcut | Action |
|---|---|
| `Ctrl/Cmd + Z` | Undo |
| `Ctrl/Cmd + Y` or `Ctrl/Cmd + Shift + Z` | Redo |
| `Esc` | Exit crop mode |
| `Ctrl/Cmd + V` | Paste image from clipboard |
| Single-letter keys above | Switch tool |

## Preview

Click **Preview** to open a full-screen, side-by-side comparison of the original image and your current edit, each labeled with its dimensions. The modal is sized to fit entirely within the viewport — no scrolling required.

## Exporting

1. Choose an output format — **PNG**, **JPEG**, or **WebP** — from the format dropdown.
2. For JPEG/WebP, adjust the **quality** slider (1–100).
3. Click **Export** to download the result as `edited.<ext>`.

You can also click **Copy** to copy the current edited image (PNG) directly to your system clipboard, instead of downloading it.

## Other Actions

- **Undo / Redo** — step backward and forward through your edit history.
- **Clear drawings** — removes all drawings and resets the canvas to the original loaded image (asks for confirmation).
- **Reset numbering** — resets the marker tool's auto-incrementing counter back to 1.

## Browser Support

Requires a modern browser with support for the Canvas API and `ClipboardItem`. Copy-to-clipboard may not be available in all browsers — the editor will let you know if it isn't.

## Tech Stack

- Plain HTML, CSS, and JavaScript — no build tools or frameworks
- [Bootstrap 5.3.3](https://getbootstrap.com/) for layout and components
- [Bootstrap Icons 1.11.3](https://icons.getbootstrap.com/) for icons
- HTML5 `<canvas>` for all rendering and image manipulation

## File Structure

```
.
├── index.html   # Entire application — markup, styles, and logic in one file
└── README.md    # This file
```
