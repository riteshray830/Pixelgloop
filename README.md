PIXELGLOOP
Product Read Me / Functional Overview
Based on supplied index.html.html implementation
Pixelgloop is a browser-based pixel-art creation and image-conversion tool. It imports PNG, JPEG and WebP images, converts them into an editable grid-based pixel representation, supports manual editing and reference tracing, and exports PNG artwork.
1. Core Modes
AI Magic is the image-conversion workflow. Tracer Mode lets the user load a reference image and manually create pixel artwork over it.
2. Image Import and Conversion
•	Accepts PNG, JPEG and WebP.
•	Supports file selection and drag-and-drop.
•	Initial imported grid preserves image aspect ratio with the largest dimension set to 64.
•	The conversion workflow is labelled “AI Magic”, but the supplied code uses local JavaScript processing rather than an external AI model/API.
•	Processing uses a Web Worker, RGB-to-LAB conversion, iterative color clustering, LAB-distance tolerance and indexed pixel mapping.
•	Maximum colors: 2–500; tolerance presets: 0, 5, 15, 30 and 50.
3. Grid and Art Controls
•	Configurable width and height; applied dimensions are clamped to 512.
•	Default grid: 64 × 64.
•	Ten pixel shapes: Square, Rounded Box, Circle, Triangle, Rectangle, Trapezium, Rhombus/Diamond, Pentagon, Hexagon and Octagon.
•	Grid visibility and grid color are configurable.
•	Activity Numbers / pattern mode displays palette indices.
4. Creative Tools
•	Pan: move the canvas.
•	Pencil: paint the selected palette color.
•	Eraser: clear cells.
•	Bucket: contiguous animated flood fill.
•	Color Picker: select an existing palette color; in Tracer Mode it can sample the reference image.
•	Custom palette colors can be added.
5. Tracer Mode
•	Loads PNG/JPEG/WebP reference images.
•	Reference opacity can be adjusted from 0% to 100%; default 50%.
•	Reference visibility can be toggled.
•	Loading a new tracing reference clears the current pixel matrix.
•	Reference colors can be sampled into the palette.
6. View and History
•	Zoom range: 5%–500%, with buttons and mouse-wheel control.
•	Canvas panning is supported.
•	Undo/redo is available from the UI.
•	Keyboard shortcuts: Ctrl/Cmd+Z, Ctrl/Cmd+Y and Shift+Ctrl/Cmd+Z.
•	History retains up to 30 states.
7. Export
•	Color Only PNG.
•	Color + Grid PNG.
•	B&W Only PNG.
•	B&W + Grid PNG.
•	Grid Only transparent PNG.
•	Export scales: 1×, 10× and 24×.
•	True-size export uses square pixels and suppresses pattern numbers.
•	Grid-inclusive true-size export is automatically upscaled to 10×.
•	Empty color/B&W canvases are not exported.
8. UI / Technical Behavior
•	Light and dark themes.
•	Responsive layout below 850px.
•	Processing overlay and toast notifications.
•	Web Audio API sound effects.
•	HTML Canvas 2D rendering.
•	Single-file HTML/CSS/JavaScript implementation.
9. Current Scope Boundaries
The supplied implementation does not evidence external AI services, vector conversion, cloud storage, accounts, collaboration or project-file persistence. These should be treated as future scope unless separately implemented.
10. Quick Start
1. Open the HTML file in a modern browser.
2. Upload or drag an image into Magic Image Import.
3. Adjust grid and Color Magic settings.
4. Choose a pixel shape.
5. Refine with the editing tools.
6. Use Tracer Mode when a reference image is needed.
7. Review with zoom/pan/undo/redo.
8. Export the required PNG.
Document Control
Version: 1.0 | Source: supplied index.html.html
