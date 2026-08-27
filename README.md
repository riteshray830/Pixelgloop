# PIXELGLOOP
### Colorful Pixel Art Creation, Image Conversion & Creative Remover

Pixelgloop is a high-performance browser-based pixel-art creation, conversion, and sprite-processing tool. It imports PNG, JPEG, and WebP images, converts them into editable grid-based pixel representations, supports manual editing and reference tracing, provides automated creative background removal with whitespace trimming, and exports PNG/ZIP artwork.

---

### 1. Core Modes
1. **✨ AI Magic**: Converts uploaded pixel art or raster pictures into an editable pixel grid with customizable color quantization and palette generation.
2. **✍️ Tracer Mode**: Lets users load a background reference image at configurable opacity to trace and craft pixel art manually.
3. **🧹 Creative Remover**: Batch processes pixel art images to automatically detect and remove background colors (with smart edge-aware gradient flood-fill or global matching), crop empty whitespace, and export individual PNGs or a single ZIP archive.

---

### 2. Image Import & Native Pixel Art Sizing
- **Original Dimension Detection**: Automatically detects native pixel dimensions of imported pixel art (e.g. 16×16, 24×24, 32×32, 48×48, 64×64, 128×128) rather than forcing an arbitrary 64×64 grid.
- **Quick Original Size Toggle**: Allows 1-click resetting to the original uploaded image dimensions.
- **Crisp Nearest-Neighbor Sampling**: Uses unblurred pixel sampling (`imageSmoothingEnabled = false`) to maintain crisp pixel art edges.
- Supports file picker and drag-and-drop.

---

### 3. Background Removal & Color Eraser Features
- **🪄 Smart Auto-Erase Background**: One-click multi-seed edge-aware detection and removal of single-color or gradient/multi-tone backgrounds into transparent cells, with automatic floating sparkle speck cleanup.
- **🎯 Magic Color Eraser Tool**: Click any pixel on the canvas to immediately erase all occurrences of that color across the canvas.
- **🎯 Erase Specific Color Modal**: Inspects active canvas colors and lets users choose any specific color to erase completely.
- **Palette Swatch Quick-Erase**: Hover over any palette swatch and click `✕` to clear all cells of that color.
- **Creative Remover Tab**:
  - Detection modes: *Smart Edge-Aware & Gradient (Auto Multi-tone)*, *Contiguous Outer BG (Edge Flood-fill)* (protects internal sprite details like white eyes/teeth), *Global Match*, *Pure Whitespace & Off-White*, *Auto Corner/Border Color*, *Custom Color Pick*.
  - Configurable color match tolerance slider (0–80).
  - ✨ Auto-Clean Floating Specks / Sparkles: Automatically identifies and clears isolated background particles, stars, and bokeh artifacts.
  - Adjustable card size controls (S, M, L, XL presets and continuous size slider from 320px to 780px).
  - High-resolution 🔍 Full-Size Inspect Modal for pixel-level detail analysis.
  - Optional whitespace trimming / sprite auto-cropping with custom padding margins (0–4 px).
  - Interactive Before & After preview cards on transparent checkerboards.
  - 1-click "Open in Pixel Editor" to continue editing any processed sprite.
  - "Download All as ZIP" (client-side zero-dependency archive generator) and "Download All (PNGs)".

---

### 4. Creative Tools & Grid Controls
- **Tools**: Pan Hand, Magic Pencil, Cell Eraser, Magic Color Eraser, Paint Bucket (animated flood-fill), Color Picker (supports canvas & tracer sampling).
- **Shapes**: Square, Rounded Box, Circle, Triangle, Rectangle, Trapezium, Rhombus/Diamond, Pentagon, Hexagon, Octagon.
- **Grid Customization**: Grid lines toggle, custom grid line color, Activity Number pattern mode.
- **History & View**: Zoom (5%–500%), canvas panning, 30-step Undo/Redo with keyboard shortcuts (Ctrl/Cmd+Z, Ctrl/Cmd+Y).
- **Synthesizer SFX**: Dynamic Web Audio API feedback for tools, actions, and downloads.

---

### 5. Export Capabilities
- **Formats**: Color Only PNG, Color + Grid PNG, B&W Only PNG, B&W + Grid PNG, Grid Only transparent PNG.
- **Export Scales**: 1× (True-size pixel art), 10× Standard, 24× Super HD.
- **Batch Export**: ZIP archive export and sequential multi-file PNG downloads.

---

### 6. Technical Stack
- Vanilla HTML5 / CSS3 / JavaScript (ES6+).
- Client-side Web Worker for color clustering and LAB-space color quantization.
- Pure JS zero-dependency ZIP archive generator.
- Fully offline capable, responsive desktop and mobile design, dark and light themes.
