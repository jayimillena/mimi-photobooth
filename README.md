# 📸 Mimi HD Vintage Film Photobooth

A lightweight, responsive, browser-based vintage photobooth web application. Built with **Alpine.js**, **Tailwind CSS**, and the native **HTML5 Canvas API**, this application captures live webcam feeds and processes high-definition composite film strips for instant download and printing.

---

## ✨ Features

- **Live Webcam Integration**
  - Real-time video stream using WebRTC (`navigator.mediaDevices.getUserMedia`).
  - Video mirror toggle for natural framing.
  - Automated **4-photo sequence** with a 3-second visual countdown and dynamic screen-flash animation.
  - Ability to snap single frames or retake specific frames individually.
  - Built-in fallback demo photos when camera access is restricted.

- **Vintage Camera Filters & Visual Effects**
  - Live CSS camera filters: *Vintage Sepia*, *Monochrome Film*, *Warm Retro*, *Cyber Pink*, *Grainy B&W*, *90s Color Film*, and *Standard Color*.
  - Real-time Canvas post-processing for **Silver Halide Film Grain** simulation and **Vintage Lens Vignette**.

- **Customizable Layouts & Themes**
  - **3 Preset Dimensions**:
    - `1.5 x 6"` Photo Strip (Classic 1:4 vertical layout)
    - `2 x 8"` Extended Strip (1:4 vertical layout)
    - `2 x 2"` Grid Layout (1:1 square ratio)
  - **Background Themes**: Classic Black, Charcoal, Vintage Pink, and Polaroid White.
  - Adjustable margin and inner padding sliders (supports **0px seamless layouts**).
  - Optional **35mm side film sprocket perforations**.
  - Customizable title signature, date stamps, and font choices (*Share Tech Mono*, *Courier Prime*, *Caveat*, *Pacifico*, *Playfair Display*).

- **Audio & Export Options**
  - Synthesized shutter sounds and countdown beeps via the **Web Audio API**.
  - One-click high-resolution **PNG download**.
  - Dedicated **Print Output** modal formatted for standard paper sizing.

---

## 🛠️ Tech Stack & Dependencies

- **Framework**: [Alpine.js](https://alpinejs.dev/) (v3.x) — Lightweight reactivity and state management.
- **Styling**: [Tailwind CSS](https://tailwindcss.com/) — Utility-first CSS framework (configured via CDN).
- **Icons**: [FontAwesome](https://fontawesome.com/) (v6.4.0)
- **Typography**: [Google Fonts](https://fonts.google.com/) (`Fredoka`, `Caveat`, `Pacifico`, `Playfair Display`, `Courier Prime`, `Share Tech Mono`).
- **Rendering Engine**: Native **HTML5 Canvas API** (2D Context).
- **Audio Engine**: Native **Web Audio API**.

---

## 📂 Project Structure

```
photobooth/
│
└── index.html       # Standalone HTML file containing UI layout, 
                     # Tailwind theme configurations, CSS filters, 
                     # and Alpine.js state logic.
```

---

## 🚀 Getting Started

### Prerequisites

All dependencies are loaded via CDN, so no installation of Node.js or npm packages is required. You only need a modern web browser (Google Chrome, Firefox, Safari, Edge).

### Running the Application

1. **Clone or Download** the repository:
   ```bash
   git clone https://github.com/your-username/mimi-vintage-photobooth.git
   cd mimi-vintage-photobooth
   ```

2. **Serve the project**:
   Because browser security policies limit WebRTC camera access on `file://` protocols, serve `index.html` via a local web server:

   - **Using VS Code**: Install the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension, right-click `index.html`, and select **Open with Live Server**.
   - **Using Python 3**:
     ```bash
     python -m http.server 8000
     ```
     Then navigate to `http://localhost:8000` in your web browser.

3. **Grant Camera Permissions**:
   When prompted, allow webcam permissions to start the live video feed. If denied, click **Load Sample Photos** to test the layout engine using demo images.

---

## 📖 Usage Guide

1. **Setup Feed & Filter**:
   - Toggle camera mirroring or sound effects in the header bar.
   - Choose a live camera filter preset from the lower panel.

2. **Capture Photos**:
   - Click **Start 4-Photo Countdown Sequence** to take 4 automatic shots in succession.
   - Click **Snap Single** to capture individual photos one at a time.
   - Hover over any captured frame thumbnail in the panel to retake that specific slot.

3. **Customize the Strip**:
   - **Size & Ratio**: Switch between `1.5x6"`, `2x8"`, or `2x2"` formats and select a background color.
   - **Margins & Text**: Adjust inner gaps and outer borders, and edit custom text labels.
   - **Film & Effects**: Toggle sprockets, grain, or vignette overlays on/off.

4. **Export**:
   - Click **Download HD Strip (PNG)** to save the generated image to your device.
   - Click **Print Output** to print the photo strip directly.

---

## 🔒 Security & Privacy Notes

- All image capturing, filter processing, and canvas rendering happen **entirely on the client side** (inside your browser).
- No image data or video feeds are transmitted to external servers.

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).