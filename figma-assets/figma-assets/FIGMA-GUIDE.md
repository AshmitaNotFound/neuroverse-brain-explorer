# Neuroverse in Figma: build guide

Import the SVGs in this folder, then build the layout and components yourself. Rebuilding it in Figma takes a couple of hours and gives you a file that is really yours to show.

## 1. Import the assets
- **brain.svg**: drag into Figma. Layers are named (`wireframe`, `cortex-points`, `activity-fields`, `hotspots`), so you can recolor or hide each layer. It is a static three-quarter view.
- **logo-mark.svg**: the wordmark symbol.
- **icons/**: 24px outline icons (zoom, rotate, center, reset, help, chevrons, share, and one wave per brain state). Turn each into a component and use a color variable for the stroke.

## 2. Color styles
| Name | Hex | Use |
|---|---|---|
| bg/base | #080B12 | Page background |
| panel/elevated | #12161D | Panels, rail, timeline |
| panel/secondary | #1A1F28 | Cards, inputs |
| divider | #2A2E36 | 1px lines |
| text/primary | #EDE9E1 | Main text |
| text/muted | #928E85 | Labels |
| accent/pastel-red | #E8A0A0 | Selected states, toggles, links |
| ui/sage | #7FB8A4 | Chart line, markers |
| ui/terracotta | #E0745C | Positive change, high values |
| brain/violet | #8C7CFF | Baseline activity, shell |
| brain/cyan | #55D9E8 | Connected activity |
| brain/coral | #FF806F | High activation |
| brain/mint | #7DE5BF | Rest, balanced |

## 3. Text styles
- Display: **Space Grotesk** 600, 32 / 22 px
- UI: **Inter** 400 and 500, 13 and 14 px
- Numbers: **IBM Plex Mono** 500, 24–34 px
- Section heading: Inter 500, 12 px, uppercase, letter spacing 1.4 px

## 4. Frame and layout (1440 × 1024, Auto Layout)
| Area | Size |
|---|---|
| Top bar | 1440 × 72 |
| Left rail | 232 wide |
| Canvas | fills remaining width |
| Right panel | 320 wide |
| Timeline | 1440 × 92 |

Use 16px corner radius on panels, 10–12px on buttons, and 1px dividers instead of shadows. Keep generous space around the brain. Add a noise fill at 2–3% opacity on top of the background.

## 5. Components to build
- **Navigation:** Wordmark, SessionStatus, ProfileMenu
- **Rail:** ModeTab (default / active), BrainStateCard (Focus / Memory / Rest / Stress), LayerToggle (on / off), ResetButton
- **Canvas:** BrainViewport (place brain.svg), Hotspot, RegionLabel (opaque / dimmed), ViewControl, InstructionHint
- **Insight panel:** RegionHeader, ActivityMetric (positive / neutral), SignalChart, MetricRow, RegionPager
- **Timeline:** WaveformScrubber, RangeSelector (10 / 30 / 60 sec)

Use variants for state (default / hover / active / disabled) and component properties for text and numbers.

## 6. Prototype interactions
- Click a hotspot: Smart Animate to a frame with that region selected (other hotspots at lower opacity, label opaque, right panel content swapped).
- Click a state card: change the brain-state variant and show a toast with a 2s After delay.
- Hover: change fill on buttons, show region name tooltips.

## 7. Making it look hand-made
- Rotate the brain.svg copy to show a second angle, and blur a duplicate behind it for glow.
- Add a case-study frame showing the palette, type and components.
- Screenshot the working page as a reference only. Draw the real design over it in Figma.
- Keep the Figma file link in the GitHub README.
