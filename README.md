# Finite Collapse

**Finite Collapse** is a systems-driven roguelike prototype built in **Unreal Engine 5**. The player assumes the role of a station engineer managing a failing space station operating under a closed-resource economy. There is no victory condition — only the challenge of delaying inevitable collapse as long as possible.

This project emphasizes systems architecture, mathematical tradeoffs, and UI-driven gameplay. There are no characters, movement systems, or narrative layers — the station itself is the gameplay system.
---

## Core Concept

All station resources exist within a fixed total allocation:

- Power  
- Oxygen  
- Cooling  
- Structural Integrity  

Each cycle, the player reallocates resources (total must equal 100%) and executes the configuration.

After execution:

- System drains resolve

- Threshold penalties trigger

- Anomalies activate

- Cascading failures propagate

Every adjustment strengthens one subsystem while destabilizing another.

Failure is guaranteed. Survival is measured in cycles.

---

## Key Design Pillars

**Closed-System Resource Model**  
All resources are conserved within a fixed budget. Gains in one system necessarily reduce stability elsewhere. The design enforces tradeoff-based decision making.

**Systems Over Characters**  
The station is the primary gameplay entity. There are no avatars or NPCs. All tension is generated through systemic pressure.

**Readable Consequences**  
Visual emblems represent anomalies, stress states, and cascading failures, minimizing text and reinforcing UI clarity. 

**Roguelike Pressure Curve** 
Each run escalates in systemic instability through randomized anomalies and modifier interactions.

**UI-First Gameplay**  
The entire experience is delivered through a diegetic engineer console interface.

---

## **Core Gameplay Loop**
1. Allocate resources (must total 100%)
2. Execute configuration
3. Resolve drains and thresholds
4. Trigger anomalies and modifiers
5. Apply cascading system degradation
6. Repeat until collapse

Score is determined by **cycles survived**.

---

## Features (Current / Planned)

### Engineering Focus
- Modular resource allocation system
- Threshold-based cascading failure model
- Emblem-driven anomaly framework
- Event-based simulation cycle
- GameState-centered simulation architecture
- UI decoupled from core logic

This project intentionally avoids:
- Character controllers
- World traversal systems
- Procedural world generation
- Narrative systems

Scope restraint is a deliberate architectural choice to maintain clarity, determinism, and system integrity.

---

## Technical Overview

- **Engine:** Unreal Engine 5
- **Primary Implementation:** Blueprints (simulation and system logic)
- **Architecture Approach:**
  - GameState manages simulation and state transitions
  - UI widgets serve purely as visualization and input layers
  - Anomalies and modifiers are data-driven and modular
  - Cycle resolution operates through deterministic execution phases

The goal is clarity, maintainability, and system scalability.

---

## Architectural Notes
- Simulation executes in deterministic phases per cycle (allocation → validation → drain resolution → anomaly resolution → degradation).
- All resource mutations pass through a centralized validation layer to enforce conservation constraints.
- Anomalies are modular and data-driven, enabling expansion without modifying core simulation logic.
- UI layer is fully decoupled and does not mutate GameState directly.
- Architecture supports future migration of simulation logic to C++ without structural refactor.

---

## Project Goals

Finite Collapse is designed as:
- A gameplay system portfolio piece
- An exploration of math-forward decision mechanics
- A tightly-scoped, replayable prototype

The emphasis is mechanical depth and architectural clarity — not content volume.

---

## Status

**Active Development**  
Currently iterating on cascading failure logic and anomaly expansion.

---

## Author

Developed by **Nathan Juranek**

---

## License

This project is currently private / unlicensed.  
Licensing will be determined if the project is released publicly.
