========================================================================
                 MIMI HD VINTAGE FILM PHOTOBOOTH
========================================================================

A lightweight, fully responsive, web-based analog photobooth application 
that captures live camera frames and composite-renders printable vintage 
photo strips directly in the browser using JavaScript, HTML5 Canvas, 
Alpine.js, and Tailwind CSS.

------------------------------------------------------------------------
TABLE OF CONTENTS
------------------------------------------------------------------------
1. Key Features
2. Technical Stack & Dependencies
3. File Structure
4. Getting Started
5. Application Usage Guide
6. Customization & Styling
7. Browser Compatibility & Notes

------------------------------------------------------------------------
1. KEY FEATURES
------------------------------------------------------------------------
• Live Webcam Stream & Capture:
  - WebRTC camera integration with automatic fallback to generated sample frames.
  - Interactive controls for video horizontal mirroring and synthetic sound effects.
  - Automated 4-shot sequence with a 3-second visual countdown and flash animation.
  - Single snap mode and individual frame retake capability.

• Vintage Filters & Post-Processing:
  - Real-time CSS live camera filters (Sepia, Monochrome, Warm Retro, Cyber Pink, B&W, 90s Color Film).
  - Canvas post-processing for Silver Halide Film Grain noise and Vintage Lens Vignette.

• Layout & Strip Customization:
  - Multiple strip dimensions:
      * 1.5 x 6" Photo Strip (Vertical 1:4)
      * 2 x 8" Extended Strip (Vertical 1:4)
      * 2 x 2" Photo Grid (1:1 Aspect)
  - Customizable theme backgrounds (Classic Black, Charcoal, Vintage Pink, Polaroid White).
  - Configurable outer padding, photo spacing (supports zero gap / seamless layout), and 35mm sprocket perforations.
  - Customizable text signatures, date stamps, and typography choices.

• Export & Printing:
  - High-resolution HTML5 Canvas rendering scaled for print output.
  - Direct PNG download and clean print window triggers.

------------------------------------------------------------------------
2. TECHNICAL STACK & DEPENDENCIES
------------------------------------------------------------------------
• HTML5 & HTML5 Canvas API (Vector/Bitmap rendering)
• Alpine.js v3.x (Reactive UI & state management)
• Tailwind CSS (Utility-first styling via CDN)
• FontAwesome v6.4.0 (UI Icons)
• Web Audio API (Synthesized shutter and countdown beeps)
• Google Fonts:
  - Fredoka (Sans-serif)
  - Caveat & Pacifico (Cursive / Script)
  - Playfair Display (Serif)
  - Courier Prime & Share Tech Mono (Monospace)

------------------------------------------------------------------------
3. FILE STRUCTURE
------------------------------------------------------------------------
photobooth/
│
└── index.html         # Main standalone application entry point containing
                       # HTML layout, Tailwind config, CSS filters,
                       # and Alpine.js state logic.

------------------------------------------------------------------------
4. GETTING STARTED
------------------------------------------------------------------------
1. Clone or download the source code files.
2. Open `index.html` in any modern web browser (Google Chrome, Mozilla Firefox,
   Microsoft Edge, or Safari).
3. Allow camera access permissions when prompted by your browser to activate 
   the live webcam view.

* Note: For camera permissions to function without prompt issues, serve the file 
  via a local server (e.g., Live Server extension in VS Code or `python -m http.server`) 
  or HTTPS environment.

------------------------------------------------------------------------
5. APPLICATION USAGE GUIDE
------------------------------------------------------------------------
1. Frame Your Shot:
   - Use the top control bar to mirror the feed or toggle audio effects.
   - Select a preferred Vintage Live Camera Filter from the filter tray.

2. Capture Photos:
   - Click "Start 4-Photo Countdown Sequence" for an automated shoot sequence.
   - Alternatively, click "Snap Single" to record one frame at a time.
   - Hover over captured thumbnails to retake a specific frame if needed.

3. Customize the Strip Layout:
   - Size & Ratio Tab: Choose 1.5x6", 2x8", or 2x2" grid layout, and set the background theme.
   - Margins & Text Tab: Adjust spacing sliders and edit the signature title/date.
   - Film & Effects Tab: Toggle sprocket holes, film grain, and lens vignette.

4. Download or Print:
   - Click "Download HD Strip (PNG)" to save the composite image.
   - Click "Print Output" to launch the print modal.

------------------------------------------------------------------------
6. CUSTOMIZATION & STYLING
------------------------------------------------------------------------
• Colors & Fonts:
  The Tailwind configuration inside `index.html` extends default colors with a 
  custom `hotpink` palette and loads google font mappings.

• Filter Formulas:
  Custom filter CSS classes (`.filter-sepia`, `.filter-grainy90s`, etc.) and matching 
  Canvas string definitions in `getCssFilterString()` can be modified to create new visual styles.

------------------------------------------------------------------------
7. BROWSER COMPATIBILITY & NOTES
------------------------------------------------------------------------
• WebRTC camera access requires HTTPS or `localhost` execution due to browser security policies.
• If camera access is denied, click "Load Sample Photos" to test strip layouts using generated sample images.
• Audio effects utilize the Web Audio API and may require user interaction with the page before sound plays.
========================================================================