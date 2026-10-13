<div align="center">

# AERONEXUS OS

### A production-oriented eVTOL fleet operations platform

Unified fleet intelligence, Digital Twin, asset diagnostics, geospatial operations, and safety workflows.

</div>

> **Platform showcase:** A cohesive, end-to-end operations experience built around production-oriented workflows, structured aircraft assets, explainable diagnostics, and live city context.

## Overview

AeroNexus OS brings the core work of an urban air-mobility operations team into one workspace: monitor fleet condition, investigate aircraft and subsystems, assess city context, and review safety information. Fleet overview, Digital Twin, diagnostics, safety review, and configuration share a consistent aircraft-centered workflow.

The platform is engineered beyond a collection of dashboard mockups. Reusable React workflows sit on an inspectable aircraft-to-subsystem-to-component model, condition and alert logic, validation and provenance details, and a geospatial workspace combining Cesium, Leaflet, route playback, traffic, and weather context.

## Digital Twin Development

The Digital Twin connects aircraft structure, condition context, and spatial operations in one navigable model:

- **Hierarchical asset representation:** aircraft records expand into propulsion, power, avionics and sensors, and structure, with inspectable component nodes such as motor/rotor groups, battery pack, flight computer, LiDAR, navigation sensors, and airframe. Stable asset and parent identifiers support navigation through the hierarchy.
- **Component-level condition model:** components expose operating state, metrics, health proxies, alert levels, and remaining-life basis. Subsystem and aircraft views aggregate available health, highest-severity alerts, sensor validation, and anomaly flags.
- **Data credibility in the UI:** asset details expose source and evaluation method, event and processing times, sensor health, validation results, confidence, and explicit unknown states.
- **Spatial twin context:** a Cesium aircraft scene sits alongside a Leaflet fleet map, route playback, road context, and selectable Hong Kong weather stations, bringing asset and environmental context into the same operator workflow.

This is a substantial Digital Twin foundation: an asset model, condition logic, provenance-aware diagnostics, and spatial context designed to work together as the platform grows.

## Product Showcase

### Fleet Health

The fleet overview gives operators an at-a-glance picture of aircraft status, health, state of charge, temperature, mission context, and maintenance signals, with a direct path into each aircraft's diagnostics.

![Fleet health overview](assets/screenshots/fleet-health-overview.png)

### Asset Diagnostics

The diagnostics workspace brings battery, rotor, avionics, and sensor condition into a single asset hierarchy, supported by time-series trends, anomaly indicators, input validation, and transparent rule/statistical analysis. Each assessment keeps its contributing signals and evaluation basis close at hand.

![Asset diagnostics](assets/screenshots/asset-diagnostics.png)

### Safety Review

The safety workspace organizes risk level, visual and audio observations, possible causes, and recommended follow-up into a reviewable operator surface, with multimodal evidence categories presented alongside aircraft context.

![AI-assisted safety context](assets/screenshots/ai-safety-context.png)

### Spatial Operations

The spatial workspace pairs a Cesium 3D aircraft scene with an interactive 2D fleet map, route playback, public Hong Kong road-speed context, and selectable weather stations. Asset, route, and environmental views are brought together for fast geographic investigation.

![Spatial synchronization](assets/screenshots/spatial-synchronization.png)

### Configuration

The configuration surface organizes display, map, telemetry, retention, and model preferences in one place, reflecting the controls expected in an extensible operations platform.

![System configuration](assets/screenshots/system-configuration.png)

## Platform Capabilities

| Capability | Delivered experience |
| --- | --- |
| Fleet operations | Status-first fleet overview, mission context, health indicators, and aircraft-focused navigation. |
| Digital Twin | Navigable aircraft, subsystem, and component hierarchy with condition logic and spatial context. |
| Diagnostics | Validated input ranges, health and anomaly indicators, time-series context, and explainable evaluation basis. |
| Battery analytics | Offline cell-data replay with cycle inspection and relative-capacity trend analysis. |
| Geospatial operations | Cesium 3D scene, Leaflet fleet map, route playback, traffic context, and selectable weather stations. |
| Safety review | Structured risk, observation, cause, and follow-up presentation in aircraft context. |
| Platform controls | Centralized display, map, telemetry, retention, and model preference surfaces. |

## Production-Oriented Foundation

The showcase brings together the product and engineering patterns needed for a serious operations platform: aircraft-centered workflows, reusable interface modules, stable asset relationships, inspectable decision logic, explicit data provenance, and clear handling of unavailable signals. Its architecture provides a credible foundation for deployment hardening and connection to operational services as those integrations and assurance processes are brought online.

## Data and Deployment Scope

The fleet currently runs on seeded aircraft scenarios and locally simulated telemetry; routes are scenario playback. Public traffic and weather context can be fetched from configured feeds. Component estimates and safety assessments are engineering views, and the battery replay uses an independent 18650 lab dataset rather than an eVTOL pack. Live aircraft synchronization, deployed inference, server-side identity, and aviation certification are outside this showcase; preferences are stored in the browser.
