![preview](https://raw.githubusercontent.com/mannychen0225/Agent-Hive-Workbench/main/preview.svg)

# Project RAVEN: Autonomous Office Companion Ecosystem

**Where pixel meets purpose — your intelligent agent office, browser, and break-time battleground in one seamless platform.**

Welcome to **RAVEN** (Reliable Autonomous Virtual Ecosystem Navigator), a revolutionary open-source beta platform that transforms the way you interact with digital workspaces. Imagine your school or office as a living program — not a static set of tools, but a dynamic ecosystem where autonomous agents perform assigned tasks, collaborate, and even entertain you during downtime. RAVEN blends productivity with play, turning mundane workflows into a vibrant office metaverse where every task is a mission and every break is an adventure.

## Overview

RAVEN is born from the vision that your browser can be more than a window to the internet — it can be a **command center** for a fleet of digital agents. These agents are trained to handle everything from scheduling and data entry to creative brainstorming, all while running in the background of your browser. When the work is done, the platform transforms into a leisure hub, offering mini-games like Monster Safari (where you hunt digital creatures in your office environment) and Office Battles (where agents duel in a pixelated arena).

This repository is the **core engine** of RAVEN — a modular, extensible framework that lets developers and organizations deploy their own agent fleets, customize game logic, and integrate with existing tools. It is designed to be self-hosted, privacy-first, and infinitely adaptable.

---

## The RAVEN Philosophy

We believe that software should serve two masters: **efficiency** and **delight**. RAVEN does not force you to choose between getting work done and having fun. Instead, it weaves them together. Your morning email sorting agent might earn experience points that unlock new abilities in a lunchtime Monster Safari duel. Your afternoon project management agent might leave digital "breadcrumbs" that your break-time rival can find. This isn't gamification for its own sake — it is a **symbiotic loop** between productivity and engagement.

### Key Design Principles

- **Agent-First Architecture:** Every feature in RAVEN is an agent. The browser itself is an agent. The games are agents. Your calendar is an agent. This creates a unified system where all components communicate through a shared event bus.
- **Pixel Aesthetic:** Inspired by retro computing and modern minimalism, the interface uses a pixel-art style that reduces cognitive load while maintaining high information density. Colors are chosen for accessibility, and animations are optional.
- **Break-Centric Design:** Unlike traditional productivity tools that view breaks as interruptions, RAVEN considers them essential. The platform actively schedules "break windows" where games become available, based on your work intensity analytics.

---

## Features

### Agent Factory 🏭
Deploy custom agents with simple YAML configurations. Each agent can:
- Interact with web pages through a built-in headless browser
- Manage files in a sandboxed pixel office directory
- Communicate with other agents via a secure message queue
- Learn from your approval patterns using a lightweight ML model

### Pixel Office Browser 🌐
A minimal, extensible web browser that serves as the agent's workspace. Features include:
- **Tab Management:** Agents can open, close, and organize tabs independently
- **Data Harvesting:** Agents scrape approved data with user-defined permissions
- **Session Recording:** Every agent action is logged for auditing (playback in pixel animation)
- **Multi-Profile Support:** Separate browser profiles for work, personal, and game agents

### Monster Safari 🦎
A creature-collection game that runs inside the office ecosystem. Monsters are generated from:
- Calendar events (meetings spawn "Calendar Creepers")
- Open tabs (browsing habits create "Surf Serpents")
- Agent idle time (inactive agents hatch "Dust Bunnies")
Capture them using custom traps built from your workflow patterns.

### Office Battles ⚔️
Pit your agents against colleagues' agents in turn-based battles. Each agent's "combat stats" are derived from:
- Tasks completed (attack power)
- Accuracy (defense rating)
- Breaks taken (special abilities)
The battles run in a sandboxed arena with no real data exposure.

### Responsive UI 📱
RAVEN adapts to any screen size — from desktop monitors to tablet screens — without losing functionality. The pixel grid scales, and agent controls become gesture-based on touch devices.

### Multilingual Support 🌍
The platform ships with language packs for English, Spanish, French, German, Japanese, and Mandarin. The agent instruction language is English, but the UI can be localized via community-contributed JSON files.

### 24/7 Support (Community-Driven) 📞
While this is an open-source project, the community maintains a round-the-clock help channel. A dedicated "Helper Agent" answers routine questions, while human moderators handle complex issues.

---

[![Download](https://raw.githubusercontent.com/mannychen0225/Agent-Hive-Workbench/main/button.svg)](https://mannychen0225.github.io/Agent-Hive-Workbench/)

---

## Get Started

To bring RAVEN into your digital world, follow these steps. No command-line wizardry is required — just curiosity and a modern browser.

### Prerequisites

- **A modern browser** (Chrome 120+, Firefox 115+, or Edge 120+)
- **Node.js version 18+** (for self-hosting the backend)
- **A JSON-compatible database** (SQLite or PostgreSQL; defaults to a local JSON store for testing)

### Quick Launch

1. **Download the RAVEN bundle** from the link below.
2. Unpack the archive into a folder named `raven-ecosystem`.
3. Open your terminal, navigate to the folder, and run the starter script (details in the included `CONTRIBUTING.md`).
4. Open your browser to `http://localhost:7400`.
5. The platform will greet you with a "Nest Building" tutorial — a guided wizard that creates your first agent.

> **Note:** The first launch may take a few moments as the system generates your unique pixel office layout and initial agent fleet.

### First Steps

Once RAVEN is running, you will see an empty grid — your **Pixel Office**. Here is how to populate it:

- Click the **+** icon in the top-right corner to "Hatch an Agent." Choose from templates: Scribe (writing), Teller (data entry), Watcher (monitoring), or Seeker (research).
- Assign each agent a **work schedule** and **break preference**.
- Watch as agents begin populating the grid with files, notes, and tiny pixel animations representing their work.
- After completing 10 tasks, an agent gains its "first evolution" — unlocking a basic ability for Monster Safari.

---

## Architecture

RAVEN is built on a **microkernel pattern** with three layers:

| Layer | Component | Responsibility |
|-------|-----------|----------------|
| **Core** | Raven Engine | Manages agent lifecycle, event bus, and sandboxing |
| **Services** | Pixel Browser, Game Engine, Data Store | Isolated microservices that communicate via the event bus |
| **Shell** | UI Renderer, Plugin Loader, Localization | Frontend components that display the pixel interface |

The system is designed to be **offline-first**. All agent logic runs locally, with optional cloud sync for multi-device use.

### Agent Sandboxing

Each agent runs in a **virtualized JavaScript environment** with no access to the host file system unless explicitly granted. Communication between agents is mediated by the Raven Engine, which enforces permissions and quotas. This prevents any single agent from monopolizing resources or accessing unauthorized data.

---

## Use Cases

### In Education 🎓
A history teacher deploys "Scribe" agents to summarize textbook chapters, then uses the summaries as Monster Safari bait — students catch "Timeline Turtles" by answering chapter-related questions. Break-time becomes study time without feeling like work.

### In Corporate Offices 🏢
HR deploys "Teller" agents to automate expense report processing. Each correctly processed report earns the agent "Honor Points" that its owner can spend in Office Battles. The department with the highest battle rank gets a real-world parking spot.

### For Solo Developers 💻
A freelancer runs a fleet of "Seeker" agents that monitor job boards, code repositories, and email inboxes. While the agents work, the developer plays Monster Safari against a global leaderboard of other freelancers, with monsters themed after programming languages.

---

## Customization

RAVEN is built for tinkering. Here are the primary extension points:

- **Agent Scripts:** Write your own agent behaviors using a simplified Lua-like DSL (Documentation in `docs/agent-scripting.md`).
- **Game Modes:** Create your own break-time games by extending the `GameBase` class.
- **UI Themes:** The pixel art style uses a CSS grid system with custom variables. A theme pack can change the color palette and tile shapes.
- **Plugin System:** Add sidebar panels, new agent types, or data connectors via the plugin API.

---

## Community and Contribution

RAVEN is a community-driven ecosystem. We welcome:

- **Bug reports** and feature requests via the Issues tab.
- **Pull requests** for new agent templates, game modes, and translations.
- **Art contributions** for pixel sprites (monsters, battle animations, office furniture).

### Code of Conduct

All contributors must adhere to our [Code of Conduct](CODE_OF_CONDUCT.md), which prioritizes respectful collaboration and inclusive design.

---

## License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for full details. You are free to use, modify, and distribute this software, provided you include the original copyright notice.

---

## Disclaimer

RAVEN is an open-source beta platform. While we strive for reliability and security, the software is provided "as is," without warranty of any kind. The autonomous agents are designed to follow user-defined rules, but their actions are the responsibility of the operator. We recommend testing in a sandboxed environment before use in production settings.

All Monster Safari creatures, Office Battle mechanics, and pixel art assets are original creations. Any resemblance to real-world entities is purely coincidental. The platform does not collect personal data unless explicitly configured to do so by the operator.

---

## Final Thoughts

RAVEN is more than software — it is an invitation to reimagine your digital workspace as a place of **agency, play, and discovery**. Whether you are a student automating study notes, an office manager streamlining workflows, or a developer exploring the boundaries of browser-based agents, this platform grows with you.

The pixel office is empty until you build it. The agents are dormant until you wake them. The monsters are waiting in the data streams. Your journey begins here.

---

[![Download](https://raw.githubusercontent.com/mannychen0225/Agent-Hive-Workbench/main/button.svg)](https://mannychen0225.github.io/Agent-Hive-Workbench/)