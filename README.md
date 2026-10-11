<div align="center">

# ASCENDO NEXUS OS

### An operator-focused eVTOL fleet operations prototype

Fleet health, asset diagnostics, geospatial context, and safety workflows in one interactive showcase.

[Source application](https://github.com/HenryyyW/AeroNexus-OS) · [Showcase repository](https://github.com/HenryyyW/AeroNexus-OS-showcase)

</div>

> **Project status:** production-minded prototype, not a production flight-operations system. The interface demonstrates an end-to-end operator workflow and engineering direction; data, models, authentication, and operational integrations are not certified or ready for aircraft use.

## Overview

Ascendo Nexus OS explores how an urban air-mobility team could review fleet condition, investigate an aircraft, understand its position in city context, and consult structured safety information from a single workspace. The showcase is built around complete operator-facing surfaces rather than isolated charts: fleet overview, digital-twin view, diagnostics, safety review, and configuration.

The implementation includes reusable React views, sensor-range validation, rule- and trend-based diagnostic logic, animated route playback, interactive map layers, and a Cesium-based 3D scene. These are meaningful foundations for a product prototype, but they do not imply validated aircraft models, a deployed backend, or operational approval.

## Product Showcase

### Fleet Health

The fleet overview brings aircraft status, health indicators, state of charge, temperature, mission context, and maintenance signals into a status-first view. Fleet readings and flight context currently originate from seeded example data and a local simulation, not connected aircraft.

![Fleet health overview](assets/screenshots/fleet-health-overview.png)

### Asset Diagnostics

The diagnostics workspace organizes battery, rotor, avionics, and sensor indicators alongside time-series trends, anomaly scores, and maintenance context. The prototype includes input-range validation and experimental rule/statistical analysis to make the diagnostic path inspectable. Its warnings and remaining-life figures are demonstrative outputs, not maintenance instructions or validated prognostics.

![Asset diagnostics](assets/screenshots/asset-diagnostics.png)

### Safety Review

The safety surface presents a structured review format for risk level, visual/audio observations, possible causes, and recommended follow-up. Current assessments are example content loaded with the aircraft data; no production computer-vision, audio, or multimodal inference service is connected.

![AI-assisted safety context](assets/screenshots/ai-safety-context.png)

### Spatial Operations

The spatial workspace pairs an interactive 2D map with a 3D geospatial view, aircraft markers, and route playback. Road-speed context can use a public Hong Kong traffic feed in the local Vite development setup; route positions remain predefined demo trajectories. External map tiles and optional road-network KML files require network access and local setup.

![Spatial synchronization](assets/screenshots/spatial-synchronization.png)

### Configuration

Configuration controls expose the kinds of choices an operations product needs to make explicit, including display, map, telemetry, retention, and model options. In this prototype, selections are stored in browser local storage and do not configure a live service, data pipeline, or model deployment.

![System configuration](assets/screenshots/system-configuration.png)

## What Works in This Prototype

| Area | Implemented in the showcase | Boundary today |
| --- | --- | --- |
| Operator workflow | Fleet overview, selected-aircraft context, diagnostics, safety review, and settings views. | Demonstration workflow; no dispatch or aircraft-control commands. |
| Fleet state | Seeded eVTOL records with locally simulated telemetry updates and predefined routes. | No live aircraft, certified sensor feed, or authoritative fleet record. |
| Diagnostics | Sensor-range checks, anomaly indicators, trend displays, and rule/statistical analysis. | Experimental logic; not validated for safety-critical decisions or maintenance planning. |
| Battery analysis | Offline replay and exploratory remaining-life calculations are available in the source application. | The included LFP cell dataset is not an eVTOL battery pack; estimates are not certified SOH/RUL. |
| Geospatial view | Leaflet map overlays, route playback, and Cesium 3D visualization. | External map/feed availability varies; aircraft trajectories are examples. |
| Safety review | Structured assessment presentation with example observations and recommendations. | No connected production AI inference or verified cockpit evidence pipeline. |
| Configuration and access | Browser-persisted preferences and a demonstration sign-in screen. | No server-side identity, authorization, audit trail, or operational configuration backend. |

## Run the Application

The showcase repository contains this README and its screenshots. To run the interactive application, use the source repository:

```bash
git clone https://github.com/HenryyyW/AeroNexus-OS.git
cd AeroNexus-OS
npm install
npm run dev
```

The application uses Vite, React, and Node.js. Some spatial layers need network access; the strategic road overlay may also require the external KML files described in the source repository's README. Firebase configuration is optional for the frontend and must be supplied locally where needed. Never commit service-account credentials.

## Production Readiness

This project is intended to communicate a product direction and demonstrate an integrated, operator-oriented interface. Before any operational use, it would need, at minimum, authenticated and authorized services, verified aircraft data integrations, traceable data provenance, validated prognostic models, robust failure handling and observability, security and privacy review, and formal aviation safety assurance. None of those are claimed by this showcase.
