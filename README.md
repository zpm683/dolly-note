# DollyNote

DollyNote is a minimalist whiteboard that lives in a single HTML file.

It lets you sketch, write, pan, zoom, save the current canvas into the URL hash, and export a self-contained HTML copy that can be reopened and edited again. The exported file behaves like a clone of the current board, which is where the name DollyNote comes from.

## Features

- Single-file app with no build step
- Infinite-feeling canvas with pan and zoom
- Pen, text, and eraser tools
- Multiple colors and stroke sizes
- Undo and redo
- Save current board state into the URL hash
- Export the current board as a standalone HTML file
- Re-open exported HTML files and continue editing or re-exporting

## How It Works

DollyNote stores the current drawing and viewport state inside the page hash.

When you click the save button, the app serializes the current board into a compact hash string and writes it into the URL.

When you click the download button, DollyNote generates a new HTML file based on the current page, injects the latest hash as startup state, and downloads that file. Opening the exported HTML restores the board automatically.

## Usage

1. Open [index.html](index.html) in a browser.
2. Draw with the pen tool, add text, or erase content.
3. Use drag, wheel, or gesture controls to move around the canvas.
4. Click save to copy a shareable link with the current state in the URL.
5. Click download to export a standalone HTML copy of the current board.

## Controls

- `P`: pen
- `T`: text
- `E`: eraser
- `0`: reset view
- `Ctrl/Cmd + Z`: undo
- `Ctrl/Cmd + Y`: redo
- `Ctrl/Cmd + Shift + Z`: redo
- `Space` + drag: pan
- Mouse wheel / trackpad: pan
- `Ctrl` or `Cmd` + wheel: zoom

## Project Structure

- [index.html](index.html): the full application, including UI, rendering, state encoding, restore logic, and standalone HTML export

## Notes

- This project currently depends on Google Fonts and the LZ-String CDN.
- Exported HTML files preserve editing capability.
- Exported file names include a timestamp to avoid accidental overwrites.

## License
MIT License. See [LICENSE](LICENSE) for details.
