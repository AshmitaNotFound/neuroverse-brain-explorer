# Neuroverse — Brain Explorer

A single-page, dark-mode interface for exploring a stylized 3D brain. Select regions, switch between brain states, and read simulated signal data. Everything is drawn procedurally on an HTML canvas: no 3D library, no external models or images.

> **Note:** all readings are simulated for demonstration. Nothing here is medical data or a medical conclusion.

## Features

- **Interactive 3D brain** with lit cortex points, a ridge-line wireframe, glowing neural filaments, orbit rings, a floor grid and an X/Y/Z axis marker
- **12 selectable regions** (prefrontal cortex, hippocampus, amygdala, and more). Click a hotspot or use the pager. The camera eases to the region and the side panel updates
- **Four brain states:** Focus, Memory, Rest, Stress. Each moves the activity clusters, retints the brain and updates the chart
- **Layer toggles:** cortex, limbic system, neural pathways, activity field
- **Modes:** Explore (labels on) and Signals (stronger pathways and field)
- **Insight panel:** activity index, 60-second signal chart, connectivity, latency, clarity and confidence
- **Live timeline** with event markers and 10 / 30 / 60 second range
- **Camera controls:** drag to rotate, scroll to zoom, plus zoom, auto-rotate and center buttons
- Keyboard-accessible controls and `prefers-reduced-motion` support

## Run it

No build step or dependencies. Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

Fonts (Inter, Space Grotesk, IBM Plex Mono) load from Google Fonts. Without a connection the page falls back to system fonts.

## Deploy with GitHub Pages

1. Push the repo to GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, then select `main` and `/ (root)`.
4. Your site will be live at `https://<your-username>.github.io/neuroverse-brain-explorer/`.

## Tech

- Plain HTML, CSS and JavaScript in one file
- Canvas 2D with a custom perspective projection, depth shading and bucketed drawing
- Fonts: Space Grotesk (display), Inter (UI), IBM Plex Mono (numbers)

## Project structure

```text
neuroverse-brain-explorer/
├── index.html   # the entire app (markup, styles, script)
└── README.md
```

## Customizing

- **Regions and activity values:** edit the `R` array in the script (name, description, 3D position, activity per state)
- **Brain states:** edit the `SD` object (name, color, text)
- **UI colors:** edit the CSS variables in `:root`
- **Brain colors:** edit the `C` constants in the script

## License

MIT. Add a `LICENSE` file if you want to publish under it.
