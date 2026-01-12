# CrisLink Control Plane – Architecture

## Overview

The CrisLink Control Plane (CLP) is responsible for:
- Visualizing system state
- Dispatching commands
- Logging events

CLP does NOT:
- Perform device logic
- Maintain device configuration
- Handle transport-specific details

---

## Control Plane Flow

Nodes → MQTT → CLP

Each node publishes state and events.
CLP subscribes and reacts.

---

## Node abstraction

All devices are represented as a generic Node:

- nodeId
- nodeType
- state
- lastSeen

Special behavior is derived from metadata, not hardcoded logic.

---

## Design goals

- Robust under degraded connectivity
- Suitable for training and real incidents
- Easy to extend without refactoring
