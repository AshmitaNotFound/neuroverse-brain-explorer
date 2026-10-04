# Neuroverse: Brain Explorer

Neuroverse is an interactive brain-activity dashboard concept. Explore a 3D brain, switch between activity states, inspect regions, and scrub through a session timeline.

**Live demo:** [ashmitanotfound.github.io/neuroverse-brain-explorer](https://ashmitanotfound.github.io/neuroverse-brain-explorer/)

## What you can explore

- **Brain states:** Focus, Memory, Rest, and Stress.
- **Anatomical layers:** Toggle the cortex, limbic system, neural pathways, and activity field.
- **Region inspection:** Select a brain region to view its name, a short functional description, and its displayed activity summary.
- **3D navigation:** Drag to rotate, scroll to zoom, reset the view, center on the selected region, or toggle auto-rotation.
- **Signal timeline:** Review the session trace and choose a 10-, 30-, or 60-second window.
- **Session controls:** The interface includes a live-session indicator and a share-session control.

## Motion and animation

The 3D brain scene is designed to feel active while keeping the dashboard readable. The model supports direct orbit and zoom interaction, and auto-rotation can be turned off. The activity field and neural-pathway layer visualize signal movement around the selected brain state. The signal chart and session timeline provide a second, time-based view of activity.

Motion should communicate state or direction, rather than act as decoration. For comfortable use, keep motion subtle, provide a way to pause continuous movement, and respect the operating system's reduced-motion preference.

## About the displayed data

This is a **visualization prototype**, not a brain scanner or medical product. Values displayed in the interface—including state percentages, activity index, connectivity, response latency, signal clarity, confidence, and timeline traces—are illustrative demo values. They are not measurements collected from a person, do not represent validated EEG analysis, and should not be used to make health decisions.

For a real-data version, document the signal source and consent process, electrode layout and units, sampling rate, preprocessing steps, and the exact definition and validation of every derived metric. Keep measured values distinct from simulated or estimated values, and show missing or uncertain data honestly.

## Run locally

The live project is published with GitHub Pages. To run a local checkout, serve the directory containing the site's `index.html` over HTTP; a static file server is sufficient. For example, with Node.js:

```bash
npx serve .
```

Open the local URL shown by the server. If the 3D scene uses remote model, library, or font assets, an internet connection is also required.

## Credits

The 3D anatomical model and its asset license should be credited in the deployed project. If using the Brain Project atlas model, retain attribution to [Brain Project / Z-Anatomy / BodyParts3D](https://github.com/itayinbarr/brainproject#attribution--licence) and comply with its CC BY-SA 4.0 terms, including share-alike requirements for adapted material.

## Project status

Neuroverse is a fictional UI/UX competition concept. Interface values and visualized activity are for demonstration only.
