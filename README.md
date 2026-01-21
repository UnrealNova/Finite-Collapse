# Finite Collapse

**Finite Collapse** is a systems-driven, decision-based roguelike prototype built in **Unreal Engine 5**.  
The player assumes the role of a station engineer managing a failing space station governed by a **closed resource system**. There is no victory state—only the challenge of delaying inevitable collapse for as long as possible.

This project emphasizes **systems design, mathematical tradeoffs, and UI-driven gameplay**, with no player character, movement, or traditional narrative elements.

---

## Core Concept

All station resources exist within a fixed total allocation:

- Power  
- Oxygen  
- Cooling  
- Structural Integrity  

Each operational cycle, the player reallocates these resources and executes the configuration.  
System drains, cascading failures, and escalating anomalies push the station toward failure.

Every decision trades stability in one system for degradation in another.

**Failure is guaranteed. Survival is measured in time.**

---

## Key Design Pillars

- **Closed-System Math**  
  All resources are conserved. Increasing one value necessarily decreases others.

- **Systems Over Characters**  
  There are no avatars or NPCs. The station itself is the “character.”

- **Readable Consequences**  
  Visual emblems represent anomalies, conditions, and system stress instead of text-heavy logs.

- **Roguelike Structure**  
  Endless runs with escalating pressure, randomized anomalies, and run-specific modifiers.

- **UI-First Gameplay**  
  The entire game is played through an engineer console interface.

---

## Gameplay Loop

1. Allocate resources across systems (total must equal 100)
2. Execute the configuration
3. System drains and penalties resolve
4. Anomalies or conditions may trigger
5. The station degrades
6. Repeat until collapse

Score is determined by **cycles survived**.

---

## Features (Current / Planned)

### Implemented
- Engineer console UI (UMG)
- Core resource model
- Cycle execution framework
- GameState-driven architecture

### In Progress
- Threshold-based cascading failures
- Emblem-based anomaly system
- Endless run scoring
- Visual system degradation feedback

### Planned
- Roguelike upgrade choices
- Expanded anomaly/emblem pool
- Audio feedback and polish
- Optional diagnostic AI (non-directive)

---

## Technical Overview

- **Engine:** Unreal Engine 5
- **Language:** Blueprints
- **Architecture:**
  - `GameState` handles all simulation logic
  - UI widgets act purely as visualization and input
  - Modular, data-driven design for anomalies and modifiers

The project is intentionally scoped to avoid:
- Character controllers
- World traversal
- Procedural level generation
- Narrative branching

---

## Project Goals

Finite Collapse is designed as:
- A **portfolio project** demonstrating systems design
- An exploration of **math-forward gameplay**
- A contained, finishable prototype with replay value

The focus is clarity, restraint, and mechanical depth—not content volume.

---

## Status

🛠 **Active Development**  
This project is currently in early prototype stage and evolving iteratively.

---

## Author

Developed by **Nathan Juranek**

---

## License

This project is currently private / unlicensed.  
Licensing will be determined if the project is released publicly.
