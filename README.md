# PastePad

PastePad is a browser-only page layout tool for arranging images and PDF pages on a white paper canvas, then exporting the result as PNG, JPEG, or PDF.

Planned GitHub Pages URL:

https://ytmknd.github.io/PastePad

## Features

- Runs as a static web app with no server-side processing.
- Supports A4 portrait, A4 landscape, A3 portrait, and A3 landscape canvases.
- Imports PNG, JPEG, GIF, WebP, and PDF files by file picker or drag and drop.
- Places link text (blue, underlined) on the paper; it is clickable in exported PDFs.
- Preserves physical size when importing PDFs and images with available resolution metadata.
- Prompts for a page number when importing a multi-page PDF.
- Supports transparent PNG placement.
- Move, resize, rotate, duplicate, delete, bring forward, and send backward.
- Attach a link URL (http, https, or mailto) to any item; it becomes a clickable link in exported PDFs.
- Hold `Shift`, `Ctrl`, or `Command` while resizing to keep the aspect ratio.
- Drag empty workspace areas to pan the viewport.
- Use `Ctrl+Z` or `Command+Z` to undo editing operations.
- Export at 150, 200, 300, or 600 dpi. The default is 600 dpi.
- UI language switches automatically: Japanese for Japanese browsers, English otherwise.

## Usage

Open the app in a browser, choose a paper size, and add files with the **Add images** button or by dragging files onto the canvas.

To place link text, enter a URL and optional display text under **Link text**, then press **Add link text**.

For each placed item:

- Drag the item to move it.
- Drag a blue corner handle to resize it.
- Hold `Shift`, `Ctrl`, or `Command` while resizing to keep the aspect ratio.
- Drag the green handle to rotate it.
- To attach a link, select the item, enter a URL in the field under **Add images**, and press **Set link** (or choose **Link** from the right-click menu). Linked items show a 🔗 badge, and the link is clickable in exported PDFs (PNG/JPEG cannot hold links). Clear the field and press **Set link** to remove it.
- Right-click an item to open the item menu: **Front**, **Back**, **Duplicate**, **Link**, **Delete**.
- Click or drag an empty workspace area to clear the menu and pan the viewport.

Use the zoom menu in the top bar to choose common preview scales such as 25%, 50%, 100%, 200%, or 300%.

## Export

Choose an output resolution in the left pane, then export as:

- PNG
- JPEG
- PDF

The preview zoom level does not affect export size or resolution.

## Local Use

You can open `index.html` directly in a browser:

```text
index.html
```

Keep the `vendor/` directory next to `index.html`, because PDF import depends on the bundled PDF.js files:

```text
vendor/pdf.min.js
vendor/pdf.worker.min.js
```

## GitHub Pages

This project is designed to be published as a static GitHub Pages site.

Expected URL:

```text
https://ytmknd.github.io/PastePad
```

For GitHub Pages, publish the repository root so `index.html` and `vendor/` are served together.

## Dependencies

PastePad uses PDF.js for browser-side PDF rendering. The PDF.js files are bundled locally under `vendor/` so the app can run without a backend server.

No user files are uploaded to a server by the app itself. Files are read and rendered locally in the browser.

## License

MIT License. See [LICENSE](LICENSE).
