![preview](https://raw.githubusercontent.com/bihari-bhau/auto-neverness-overseer/main/screen_3177759.svg)

# Atlas of the Unseen Hour 🌌

Every world has its hidden clockwork — the quiet machinery that turns daily routines into rituals and scattered tasks into a living economy. **Atlas of the Unseen Hour** is not another automation tool; it is a **sentient cartographer** for the games you love, mapping the invisible rhythms of your in-game life and turning them into a symphony of effortless progression.

Imagine a patient, tireless librarian who never sleeps, never blinks, and possesses an almost obsessive attention to detail. That is what we have built. Using the same robust computer-vision foundation that powers cutting-edge robotics, this project learns the *texture* of your game world — not just pixels, but patterns, timings, and the subtle choreography of daily quests, resource nodes, and combat cycles. It does not merely click; it *understands*.

---

## 🧭 Why Another Automation Project? Because This One *Listens*

Most automation tools are blunt instruments — they hammer at coordinates until something breaks. We built **Atlas** with a different philosophy: **observational elegance**. It watches your screen the way a seasoned naturalist watches a forest — patiently, precisely, and with a deep respect for the ecosystem.

This means:
- **No brittle macros** that break when the UI shifts by a pixel.
- **No memory-hogging overlays** that scream for attention.
- **A silent guardian** that works alongside you, not over you.

It is the difference between a marionette and a dancer. We chose the dancer.

---

## 🌠 Core Constellations (Features)

Below are the pillars that hold up the observatory dome.

### 🎯 Adaptive Quest Routing
The system does not follow a static checklist. It *reads* your current progress, cross-references it with known daily resets, and dynamically recalculates the most efficient path through your daily obligations. If a quest is already complete, it quietly skips it. If a new event appears, it adapts on the fly. It is a living map, not a printed atlas.

### ⚔️ Combat Choreography Engine
Think of this as a set of pre-written dance routines for your characters. The engine analyzes enemy attack patterns via visual cues, then executes a pre-approved response sequence — dodging, striking, and managing cooldowns with the grace of a metronome. It is not a cheat; it is a rehearsal. It plays the way a speedrunner practices.

### 💎 Resource Harvesting Logic
Scattered across the world are shimmering points of interest. The Atlas detects these via their unique light signatures and visual markers, then plots a minimalist route to collect them without triggering aggro or wasting time. It is a treasure map drawn in real-time.

### 📊 Gacha & Loot Ledger
A built-in memory palace for your pulls. It logs every single draw, categorizes rarity, and builds a statistical model of your luck. This is not just a record; it is a **fortune-teller's abacus** that helps you decide when the odds are in your favor based on historical patterns.

### 🌍 Multilingual Observatory
The interface and the underlying recognition engine understand that the gaming world speaks many dialects. The Atlas is fully localized for **English, Japanese, Korean, Simplified Chinese, and Spanish**, ensuring that the recognition profiles match the exact font rendering of your client version.

### 📱 Responsive Command Deck
While the engine runs on your desktop, you can check the status through a lightweight web interface on your phone. See what the Atlas is currently doing, pause a routine, or review the day's haul — all from the comfort of your couch.

### 🛎️ 24/7 Sentinel Support
Life happens. The Atlas is designed to be resilient. If the game crashes, if the network drops, or if a new patch shifts the UI, the system does not panic. It enters a **safe-holding pattern**, waits for conditions to stabilize, and then resumes from a secure checkpoint. It is the friend who never complains.

---

## 🗺️ How The Cartography Works (Deep Dive)

[![Download](https://raw.githubusercontent.com/bihari-bhau/auto-neverness-overseer/main/go_ebb2.svg)](https://bihari-bhau.github.io/auto-neverness-overseer/)

### Phase 1: Visual Signature Learning
On first run, the Atlas takes a series of high-resolution "snapshots" of your game window. It does not look for text strings; it looks for the *geometry and color histograms* of buttons, health bars, and inventory slots. This creates a unique **biological fingerprint** of your specific client settings.

### Phase 2: Pattern Recognition & State Machine
The core is a deterministic state machine driven by visual feedback. The engine transitions from `IDLE` to `NAVIGATING` to `COMBAT` based on what the camera sees, not on arbitrary timers. This makes it remarkably robust against lag spikes and inconsistent frame rates.

### Phase 3: The Rehearsal Loop
Before any action is taken in the live environment, the Atlas runs a *ghost simulation*. It plays out the next 10 seconds of potential actions in a virtual sandbox, checks for collision risks or unexpected pop-ups, and only then commits to the real input. This is the **difference between a genius and a lucky guess**.

### Phase 4: The Journaling System
Every action is logged into a local, encrypted SQLite database. This isn't spyware; it is your personal black box. You can review the exact timeline of the day, see where time was spent, and export reports to understand your gaming habits better.

---

## 🧪 The Alchemy of Setup (Getting Started)

Getting the Atlas running is less like "installing software" and more like "introducing a new friend to your home."

**Prerequisites:**
- A Windows 10/11 or Linux (Ubuntu 22.04+) environment.
- A display resolution of 1920x1080 or 2560x1440 (scaling supported).
- A modern GPU sufficient for the target game (any mid-range card from the last six years will suffice).
- The target game launched in **Windowed Fullscreen** or **Borderless Windowed** mode.

**The Onboarding Ritual:**
1. **The Handshake** – Download the release bundle for your OS. It is a single, self-contained archive. There are no hidden dependencies; the entire runtime is bundled.
2. **The Recognition** – Run the `atlas-init` binary. It will ask you to point it to your game's executable. It does not modify the game files. It only reads the screen.
3. **The Calibration** – A guided wizard will ask you to navigate to a few specific in-game menus (like the settings and inventory). This takes 90 seconds and establishes the baseline visual anchors.
4. **The Deployment** – Select which daily routes you want to automate, set your "energy budget" (how long you want the session to run), and press `Begin Observation`.

---

## 🛠️ Architecture & Philosophy

The project is built on a modified fork of the **MaaFramework** — a rock-solid, battle-tested computer vision engine known for its efficiency. We have stripped away the generic bloat and added our own **Contextual Awareness Layer (CAL)** .

```
[Game Render]
   |
   v
[Screen Capture API] --> [Vision Tokenizer] --> [State Mapper]
   |                                       |
   v                                       v
[Action Queue] <--- [Contextual Awareness Layer] <--- [Gesture Decoder]
   |
   v
[Simulated Input Stack] -> [Game Window]
```

- **Vision Tokenizer** converts raw screen data into symbolic tokens (e.g., `ENEMY_ALERT`, `DIALOG_OPEN`).
- **State Mapper** holds the current logical position in the game's flowchart.
- **Gesture Decoder** translates high-level goals into low-level mouse/keyboard events.
- **The Contextual Awareness Layer** is the *brain* — it holds the rules, the exceptions, and the "common sense" that prevents the bot from doing something stupid like attacking an NPC.

---

## 🔐 Safety & Ethical Boundaries

We operate strictly within the gray zone of "permitted macros." The Atlas does **not** read process memory, inject code, or alter game files. It is purely an optical observer that sends synthetic input signals, just like a human using a keyboard and mouse.

**We explicitly do not support:**
- Games with strict anti-cheat that prohibits macro usage.
- PvP environments where automation would ruin the competitive balance.
- Any form of account sharing or real-money trading.

If the game detects the input pattern and flags it, that is a risk the user assumes. We provide the tool; we do not guarantee immunity. This is a tool for **legitimate convenience**, not for disruption.

---

## 🌈 A Metaphor for the Journey

Think of this project as the **lighthouse keeper** for your digital harbor. You do not see it constantly, but you know the channels are clear every morning. It is not about replacing your joy of playing — it is about removing the *drudgery* that sits between you and the fun. If you love fishing in the game but hate the daily fetch quests, the Atlas clears the path so you can fish.

---

## 🤝 Contributing to the Constellation

We welcome astronomers of all skill levels. Whether you want to add a new game-specific recognition profile, improve the gesture decoder, or simply write better documentation, there is a place for you.

**Areas we are actively exploring:**
- Support for 1440p and 4K native resolutions (currently handled via scaling).
- A plugin system for community-created "quest packs."
- A headless mode for running on low-power servers.

Please read our `CONTRIBUTING.md` (in the repository root) for coding standards and the PR process. We prefer clean, readable code over clever one-liners. Comments are always appreciated — they are the signposts for future travelers.

---

## 🧩 Troubleshooting the Compass

**Q: The Atlas is seeing but not acting.**
- *A:* Check your game's input settings. Ensure "DirectInput" is enabled for mouse events, or switch to "Raw Input" if using the bundled driver.

**Q: The visual anchors are failing after a patch.**
- *A:* Run the Calibration Wizard again. Patches change pixel data, not the logical structure. A 60-second recalibration usually fixes everything.

**Q: Is it safe to run while I am actively playing the game?**
- *A:* We do not recommend it. The Atlas assumes exclusive control over the input queue to avoid conflicts. Let it do its job, or do it yourself. Choose one captain for the ship.

---

## 📜 License & Legal Clarity

This project is proudly released under the **MIT License**. You are free to use, modify, and distribute it for personal or commercial purposes, provided you retain the original copyright notice. We believe in open skies.

You can find the full legal text in the `LICENSE` file at the root of this repository. [View the License](LICENSE)

---

## 💬 Final Thought: The Unseen Hour

The name "Unseen Hour" comes from the idea of the quiet period just before dawn — when the world is still, and the day has not yet been written. That is where the Atlas operates. In the margins of your day. In the background of your screen. It turns wasted time into collected resources, scattered effort into concentrated progress.

We do not ask you to trust us. We ask you to **observe the results**.

Welcome to the observatory. Point us at the sky, and we will map the stars for you.

---

**Project Status:** Active development (v0.9.4 stable) • Year of release: 2026 • Looking for beta testers for the new "Dreaming City" route.

[![Download](https://raw.githubusercontent.com/bihari-bhau/auto-neverness-overseer/main/go_ebb2.svg)](https://bihari-bhau.github.io/auto-neverness-overseer/)