# Power Grid Intelligence Console

An interactive 3D power-grid visualization built with React, Vite, Three.js, and React Three Fiber. The project presents a simplified smart-grid digital twin showing how electricity is generated, transmitted, stored, distributed, and monitored with IoT telemetry.

## Overview

This app combines a 3D scene with an analytics-style interface so users can explore major grid assets such as:

- Coal and nuclear generation
- Solar and wind generation
- Transmission and distribution substations
- Battery energy storage
- Smart meters and sensor networks

Each node can be inspected to view its role in the grid, a plain-language explanation, technical notes, and live-style operational metrics.

## Features

- Interactive 3D scene with orbit, zoom, and focus controls
- Clickable grid assets with detailed information panels
- Guided tour explaining the end-to-end electricity journey
- Energy journey rail for quick navigation across grid stages
- Asset legend for cycling through node types
- Operational analytics panel with demand, renewable, and utilization charts
- Glossary for core power-system and IoT terms
- Floor mode switching and label toggling
- Simulated telemetry and KPI summaries

## Tech Stack

- React 19
- Vite 8
- Three.js
- `@react-three/fiber`
- `@react-three/drei`

## Getting Started

### Prerequisites

- Node.js 18 or newer
- npm

### Installation

```bash
npm install
```

### Start the development server

```bash
npm run dev
```

Then open the local URL shown by Vite in your terminal, usually `http://localhost:5173`.

### Build for production

```bash
npm run build
```

### Preview the production build

```bash
npm run preview
```

## How to Use

- Drag to orbit around the 3D grid
- Scroll to zoom in and out
- Click a node to open its detail panel
- Click the same node again or press `Esc` to clear selection
- Use `Start Tour` for a guided walkthrough
- Use the legend to jump between similar asset types
- Use the journey rail to move through grid stages
- Toggle labels and floor styles from the top toolbar

## Project Structure

```text
power-grid-3d2/
|- src/
|  |- components/
|  |  |- Scene.jsx
|  |  |- GridNode.jsx
|  |  |- TransmissionLines.jsx
|  |  |- Ground.jsx
|  |  |- InfoPanel.jsx
|  |  |- DataPanel.jsx
|  |  |- TourModal.jsx
|  |  |- WelcomeModal.jsx
|  |  `- Glossary.jsx
|  |- data/
|  |  `- gridData.js
|  |- App.jsx
|  |- main.jsx
|  `- index.css
|- index.html
|- package.json
`- vite.config.js
```

## Data Model

The application is driven by static configuration in `src/data/gridData.js`, including:

- `GRID_NODES` for asset metadata and metrics
- `TRANSMISSION_LINES` for network connections
- `CHART_DATA` for analytics panel values
- `TOUR_STEPS` for the guided experience
- `GLOSSARY` for terminology help

This makes the project easy to extend with more assets, additional telemetry, or future API-backed data sources.

## Possible Enhancements

- Replace mock data with live API or WebSocket telemetry
- Add alerts, outage simulation, or fault propagation scenarios
- Introduce filtering by asset type or operating state
- Add mobile-specific interaction refinements
- Persist UI settings such as floor mode and labels

## License

Add a license file if you plan to distribute or publish this project.
