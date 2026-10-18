<p align="center">
  <img src="./assets/header.svg" width="100%" alt="rory herriman — systems administrator by profession, developer by accident">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/profession-systems_administrator-0078D4?style=flat-square&logo=windows&logoColor=white" alt="Profession: systems administrator">
  <img src="https://img.shields.io/badge/developer-by_accident-e6c35c?style=flat-square" alt="Developer by accident">
  <img src="https://img.shields.io/badge/code-mostly_AI--generated-a371f7?style=flat-square" alt="Code: mostly AI-generated">
  <img src="https://img.shields.io/badge/currently_hyperfocused_on-Pathwarden-4f8cf0?style=flat-square" alt="Currently hyperfocused on: Pathwarden">
</p>

<h3 align="center">Systems Administrator by profession. Developer by accident.</h3>

I don't really know how to code. I just have an unreasonable number of ideas and access to AI tools willing to entertain them.

This GitHub is a collection of passion projects, random experiments, and things that started with:

> *"I wonder if AI could build that..."*

Most of the code is AI-generated. I handle the ideas, requirements, testing, troubleshooting, and the occasional existential crisis when something breaks.

**Fair warning:** I have ADHD, so project completion is... optional. Some projects work. Some are actively being developed. Others were abandoned because my brain found something more interesting about 37 minutes later.

Welcome to the lab. Nothing here is guaranteed to work, but that's half the fun.

```console
rory@accidental-dev-lab:~$ whoami
systems administrator: Azure, Windows Server, PowerShell, SQL Server, DevOps

rory@accidental-dev-lab:~$ cat ~/.how-things-get-built
1. have an idea at 1 a.m.
2. write the requirements like it's a change request
3. let the AI write the code
4. test it like a sysadmin: assume it's lying until the logs agree
5. troubleshoot whatever breaks (something always breaks)
6. ship it ... or notice a shinier idea

rory@accidental-dev-lab:~$ ls ~/projects
completed/  in-development/  experimental/  on-hold/  abandoned/   # no judgement here
```

### 🧠 Who does what

| | Me | The AI |
|---|---|---|
| Ideas, scope and requirements | ✅ | |
| Architecture decisions and "no, not like that" | ✅ | 🤝 |
| Writing most of the code | | ✅ |
| Testing against real game data and real logs | ✅ | |
| Troubleshooting when it breaks | ✅ | 🤝 |
| Getting distracted by a new idea | ✅✅✅ | |

The day job taught me monitoring, change control and "don't trust it until it's measured". That's the part I bring to every project here. Work I do for employers stays behind their walls. Everything on this page is a personal project.

---

## 🗺️ Quest log: featured builds

<p align="center">
  <a href="#pathwarden"><img src="./assets/cards/pathwarden.svg" width="49%" alt="Pathwarden: in development"></a>
  <a href="#ascend"><img src="./assets/cards/ascend.svg" width="49%" alt="Ascend: completed"></a>
  <a href="#wow-coach"><img src="./assets/cards/wow-coach.svg" width="49%" alt="WoW Coach: on hold"></a>
  <a href="#miq"><img src="./assets/cards/mplusiq.svg" width="49%" alt="M+IQ: on hold"></a>
</p>

### Pathwarden

![In Development](https://img.shields.io/badge/status-in_development-4f8cf0?style=flat-square) ![Lua](https://img.shields.io/badge/Lua-2C2D72?style=flat-square&logo=lua&logoColor=white) ![WoW Forever](https://img.shields.io/badge/WoW-Forever-e6c35c?style=flat-square)

*Currently receiving dopamine.* A leveling companion for a **Protection Paladin + Mage duo** in WoW Forever. Its job is to answer "what should we do next?" using live game data instead of a spreadsheet. (It used to be called Forever Forge.)

- **Working in the code today:** event and saved-variable core · bag, equipped-item and bank snapshots · Smart Gear Advisor (per-role stat weights, upgrade comparison for both players) · dungeon prep (per-dungeon preferences, quest readiness and prerequisite chains for you *and* your partner) · "gear or gold?" quest-reward advice · profession materials with bank-aware totals · a gold budget built from real training costs · a read-only bridge to NaowhForever's data · waypoints via Polestar, TomTom, or a map pin
- **In progress:** the UI layer (dashboard, gear, route, dungeons, professions, gold, talents, pre-BiS pages), plus the talents, duo sync, discovery and next-action modules
- **Planned:** pre-BiS planning and a single "next best action" recommendation

> 🔒 Not public yet. It will get a repo once the UI layer can be loaded in game.

### Ascend

![Completed](https://img.shields.io/badge/status-completed-3fb950?style=flat-square) ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Qt](https://img.shields.io/badge/PySide6-41CD52?style=flat-square&logo=qt&logoColor=white) ![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)

*Against all odds, it works.* A Windows desktop app that turns a whole raid tier of Warcraft Logs into answers. Are you improving? Do you die early? Do you keep making the same mistake? Ascend looks at the tier as a whole instead of one parse at a time.

- Pull timelines, death breakdowns, and a 7-category performance score. Every number comes with a confidence rating based on how much data supports it.
- Roster comparison, guild report discovery, goals, encounter rules, a weekly summary for Discord, and JSON export
- Runs entirely on your machine: data lives in local SQLite and secrets in Windows Credential Manager
- **v1.0.0**: 389 pytest tests, GitHub Actions CI, and tagged releases that build a portable `.exe`

### WoW Coach

![On Hold](https://img.shields.io/badge/status-on_hold-8b949e?style=flat-square) ![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)

*The dopamine has left the building, but the prototype works.* A personal performance coach that rebuilds what actually happened in a pull. The aim is to separate *your mistakes* from *the mechanic that was always going to hit you*.

- **V0 works:** a local web app that reads your Warcraft Recorder library, matches each recording to the right combat log, and opens a pull review with a timeline and in-app video
- Found and worked around a real upstream quirk along the way: Warcraft Recorder's `uniqueHash` isn't unique across repeated wipes
- **When it comes back:** the actual coaching layer. Voice-comms analysis was tested in experiments and is not built yet.

### M+IQ

![On Hold](https://img.shields.io/badge/status-on_hold-8b949e?style=flat-square) ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Azure SQL](https://img.shields.io/badge/Azure_SQL-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)

*Started with a very ambitious master spec. Became a very careful data pipeline. Then WoW Coach happened.* A Mythic+ analysis engine.

- **Built:** a Warcraft Logs v2 client with rate limiting · ingest into SQL with migrations and a database-isolation guard · raw event storage and normalization · a feature-extraction engine (packs, pulls, enemy forces) · a multi-source reference framework (MDT and the Blizzard API) · reconstruction calibrated against 24 real runs
- **Not built:** the web UI, Title Mode comparisons, and AI coaching
- On hold while those ideas get tested in a smaller form in WoW Coach

---

## 🧭 The map: every project

| Status | What it means |
|---|---|
| ![Completed](https://img.shields.io/badge/-completed-3fb950?style=flat-square) | Against all odds, it works. |
| ![In Development](https://img.shields.io/badge/-in_development-4f8cf0?style=flat-square) | Currently receiving dopamine. |
| ![Experimental](https://img.shields.io/badge/-experimental-f0883e?style=flat-square) | We're seeing what happens. |
| ![On Hold](https://img.shields.io/badge/-on_hold-8b949e?style=flat-square) | The dopamine has left the building. |
| ![Abandoned](https://img.shields.io/badge/-abandoned-b0646b?style=flat-square) | It was a great idea for approximately six hours. |

#### 🎮 Game dev & WoW addons

| Project | What it does | Status | Stack |
|---|---|---|---|
| **Pathwarden** | Duo-leveling companion for WoW Forever (see above) | ![](https://img.shields.io/badge/-in_development-4f8cf0?style=flat-square) | Lua |
| **Tempest Reminder** | Big on-screen and audio alert for a raid tornado mechanic. Built on the new Encounter Timeline API, not the combat log. Not yet confirmed against a live cast. | ![](https://img.shields.io/badge/-experimental-f0883e?style=flat-square) | Lua |
| **Raid Consumable Reminder** | Shows the right flask and potion for your Warlock spec when you zone into a raid or M+. Its data table is meant to be regenerated from Raidbots results. Only backups remain. | ![](https://img.shields.io/badge/-abandoned-b0646b?style=flat-square) | Lua |
| **Fractured Starway** | Unreal Engine 5 sandbox: a third-person template plus my first blueprints (floating stones, an energy cube, a gate glow material). A classic six-hour idea. | ![](https://img.shields.io/badge/-abandoned-b0646b?style=flat-square) | Unreal Engine 5 |

#### 📊 Game analytics & data

| Project | What it does | Status | Stack |
|---|---|---|---|
| **Ascend** | Tier-wide raid progression analytics from Warcraft Logs | ![](https://img.shields.io/badge/-completed-3fb950?style=flat-square) | Python · PySide6 · SQLite |
| **WoW Coach** | Lines up recordings with combat logs for pull review | ![](https://img.shields.io/badge/-on_hold-8b949e?style=flat-square) | Node.js |
| **M+IQ** | Mythic+ ingest and feature-extraction engine | ![](https://img.shields.io/badge/-on_hold-8b949e?style=flat-square) | Python · SQLAlchemy · Azure SQL |
| **Multi-Spec Gear Optimizer** | Finds one shared gear setup that loses the least DPS across several specs, using Raidbots profilesets. Includes a Streamlit UI and Pareto ranking. The prototype works for three Warlock specs. | ![](https://img.shields.io/badge/-on_hold-8b949e?style=flat-square) | Python · Streamlit · pandas |

#### 🛠️ Automation & utilities

| Project | What it does | Status | Stack |
|---|---|---|---|
| **GuildScanner** | Scores guild recruitment posts you paste in against your class, schedule and rank preferences, then sends the best matches to a private Discord webhook. Never scrapes Discord. 51 tests passing. | ![](https://img.shields.io/badge/-completed-3fb950?style=flat-square) | Python |
| **Notorious** | My 2023 recruitment scraper: pulls players from WoWProgress LFG, adds Warcraft Logs and Battle.net data, filters them, and posts to Discord. GuildScanner is its spiritual successor. | ![](https://img.shields.io/badge/-abandoned-b0646b?style=flat-square) | Groovy · PostgreSQL · Docker |

#### 🧪 Experiments

| Project | What it does | Status | Stack |
|---|---|---|---|
| **JARVIS** | What if I built my own desktop AI agent? Phases 0–2 got done: a Tauri app with a WebGL "orb" that reacts to speech, a voice pipeline, and a wake word. Phases 3–14 (agent kernel, tools, memory) are... still on the roadmap. | ![](https://img.shields.io/badge/-on_hold-8b949e?style=flat-square) | TypeScript · React · Three.js · Tauri · FastAPI |

---

## 🔧 On the workbench (subject to change without notice)

```diff
+ now     Pathwarden: wiring the UI pages onto the engine modules
+ now     Pathwarden: duo sync, so both players see each other's quest and gear state
! next    Ascend: public release (the repo is private while I tidy it up)
! maybe   WoW Coach: the first real coaching pass on top of pull review
- parked  M+IQ coaching layer, JARVIS agent kernel, Gear Optimizer
- parked  whatever idea I have at 1 a.m. tonight
```

## 🧰 Toolbelt

**Day job (the stuff I actually trained for)**<br>
![Azure](https://img.shields.io/badge/Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![Windows Server](https://img.shields.io/badge/Windows_Server-0078D6?style=flat-square&logo=windows&logoColor=white)
![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?style=flat-square&logo=powershell&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=flat-square&logo=microsoftsqlserver&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

**AI co-pilots (they write it, I break it)**<br>
![Claude](https://img.shields.io/badge/Claude-D97757?style=flat-square&logo=claude&logoColor=white)
![ChatGPT](https://img.shields.io/badge/ChatGPT-74aa9c?style=flat-square&logo=openai&logoColor=white)

**Languages my projects ended up in**<br>
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Lua](https://img.shields.io/badge/Lua-2C2D72?style=flat-square&logo=lua&logoColor=white)
![Groovy](https://img.shields.io/badge/Groovy-4298B8?style=flat-square&logo=apachegroovy&logoColor=white)

**Frameworks & data**<br>
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Tauri](https://img.shields.io/badge/Tauri-24C8DB?style=flat-square&logo=tauri&logoColor=white)
![Qt](https://img.shields.io/badge/PySide6-41CD52?style=flat-square&logo=qt&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat-square&logo=sqlalchemy&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)

**Game data sources**<br>
![Warcraft Logs](https://img.shields.io/badge/Warcraft_Logs_API-1f2a3a?style=flat-square)
![Raidbots](https://img.shields.io/badge/Raidbots_%2F_SimC-1f2a3a?style=flat-square)
![Battle.net](https://img.shields.io/badge/Battle.net_API-148EFF?style=flat-square&logo=battledotnet&logoColor=white)

---

## 🐍 Activity

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/roryherriman/roryherriman/output/snake-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/roryherriman/roryherriman/output/snake.svg">
    <img alt="Contribution graph being eaten by a snake" src="https://raw.githubusercontent.com/roryherriman/roryherriman/output/snake-dark.svg" width="100%">
  </picture>
</p>

<p align="center"><sub>Most of my repos are private for now, so the graph is the best evidence of how often a new idea wins.</sub></p>

---

<p align="center">
  <sub>Not affiliated with Blizzard Entertainment, Warcraft Logs, or Raidbots. World of Warcraft is a trademark of Blizzard Entertainment.</sub>
</p>

### 🤖 One Last Thing...

Oh, and yes. Even this entire GitHub profile was written by AI.

I told it to make me look cool.

Teehee, enjoy! :0

**— The Accidental Developer**
