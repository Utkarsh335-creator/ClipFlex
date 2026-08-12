# ClipFlex — Micro Video Editor

ClipFlex is a lightweight, single-file browser video editor built with vanilla HTML5, CSS, and JavaScript. It provides a multi-track editing workspace, keyframe animation, HSL/RGB color tools, and client-side rendering with no external server processing.

---

## Technical Stack & Architecture

- **Engine**: Pure JavaScript (ES6+), Web APIs (`HTML5 Canvas`, `HTML5 Media Elements`)
- **Styling**: Modern CSS variables, CSS Grid, Flexbox, custom UI tokens
- **Processing**: Fully client-side using native browser video/audio element synchronization
- **Storage**: Browser `localStorage` for automatic project recovery

---

## Core Features

- **Multi-Track Timeline**: Separate tracks for Video, Audio, Text overlays, and Picture-in-Picture (PIP).
- **Track Management**: Rearrange track order, control z-index layer ordering, and split/trim/duplicate clips.
- **In-Browser Exporting**: Live compositing and rendering directly to the user's filesystem without external server dependencies.
- **Color Grading**: Custom interactive RGB Curve canvas manipulation and three-wheel HSL adjustments (Hue, Saturation, Lightness).
- **Text & PIP Overlays**: Drag-and-drop interactive canvas positioning for text layers and PIP elements.
- **Transitions**: Native clip-to-clip transition support (Crossfade, Fade to Black, Wipes, Slides, and Zooms).
- **Magnetic Snapping**: Precision clip alignment snapping on the timeline grid.

---

## Project Structure

This application is designed as a self-contained web app. All code is contained in a single HTML document:

```text
index.html
 ├── <style>    — CSS design tokens, app grid layout, clip styles, theme variables
 ├── <body>     — Timeline elements, inspector controls, canvas stage, media pool
 └── <script>   — App state management, canvas compositor, video sync engine
