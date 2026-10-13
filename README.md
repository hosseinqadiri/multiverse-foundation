# 🌌 Multiverse Foundation

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Status: v0.1 Feasibility](https://img.shields.io/badge/Status-v0.1_Feasibility-orange.svg)]()
[![Focus: Language & Micro-Engine](https://img.shields.io/badge/Focus-MFL_%26_Micro--Engine-brightgreen.svg)]()

> **"Persistence is secondary; the Foundation is everything."**  
> A simple, transparent foundation for creating, plugging in, and experiencing infinite virtual worlds through real-time **Presence**.

---

## 💡 What is Multiverse Foundation? (In Plain English)

Most virtual world platforms fail because they try to build **one giant, heavy world** and save every single detail forever in massive databases. 

**Multiverse Foundation** takes the exact opposite approach:
1. **A Multiverse of Infinite Worlds:** A multiverse is a network of independent worlds. Anyone should be able to create a new world with its own unique rules (custom gravity, speed, visuals, or sound) and plug it into the network in seconds.
2. **Presence in the Moment:** What matters most is **being there right now**. When you enter a world, your presence (where you are, where you look, how you interact) is experienced live by others in that same moment.
3. **Foundation Over Persistence:** We do not care about storing heavy history or permanent database states. Worlds can appear when someone enters them and disappear when everyone leaves. The **Foundation**—the language and the engine that make instant presence possible—is what matters.

---
ه
## 🎯 Phase 1 Goal (`v0.1`): The Language & The Micro-Engine

Before building complex 3D graphics or heavy servers, **Version 0.1** focuses on one clear, achievable goal:

**Creating the simplest, shortest, and most extensible language to define worlds and stream real-time presence—and building the smallest possible micro-engine to run it.**

### Why a New Language? (`MFL` — Multiverse Foundation Language)
Existing formats like JSON or YAML are made for static data, not living worlds. We designed **MFL (`.mfl`)** to be:
* **Simpler:** No messy brackets, quotes, or commas everywhere.
* **Clearer:** Anyone can read a file and immediately understand the rules of that world.
* **Shorter & More Concise:** Up to 70% smaller than JSON. Define an entire world in 4 lines; send a live presence update in 1 line.
* **Infinitely Extensible:** The core language only has a few basic words, but you can attach unlimited new features to any world using the `use` keyword.

---

## ⚡ How It Works (A 30-Second Look)

In **Multiverse Foundation**, everything—both **World Rules** and **Live Presence**—is written in the same simple language:

### 1. Define Any World (4 Lines)
You create a `.mfl` file to describe what your world looks like and how it behaves:

```mfl
world zero_gravity_station {
  law gravity(0, 0, 0) time(1.0) max_speed(50)
  space "[https://cdn.example.com/station.glb](https://cdn.example.com/station.glb)" spawn(0, 2, 0)
  use audio.spatial(radius: 30)
}

 * world names the realm.
 * law sets the physical rules expected in this world.
 * space points to the 3D environment and where users appear.
 * use plugs in extra features (like 3D voice, weather, or AI) without changing the core engine.
2. Experience Presence in the Moment (1 Line per Action)
When users enter the world, the micro-engine processes live signals starting with !:
!enter @user_101 -> zero_gravity_station at(0, 2, 0)
!pulse @user_101 pos(4.2, 5.0, -1.8) look(0, 90, 0) state(floating)
!shift @user_101 -> desert_planet_02 at(0, 0, 0)
!leave @user_101

 * !enter: Spawns the user's presence into a world.
 * !pulse: Updates their live position and state in real time.
 * !shift: Instantly moves their presence to a completely different world with new rules.
 * !leave: Cleanly removes their presence (zero database leftovers).
🏗️ The Micro-Engine Architecture
To prove this foundation works, the v0.1 Micro-Engine is designed to be ultra-lightweight, dependency-free, and fast:
  [ .mfl World Files & Live !Signals ]
                   │
                   ▼
      ┌─────────────────────────┐
      │   1. Micro-Parser       │  --> Reads MFL syntax in microseconds
      └────────────┬────────────┘
                   │
                   ▼
      ┌─────────────────────────┐
      │   2. In-Memory Worlds   │  --> Holds active worlds & their laws in RAM
      └────────────┬────────────┘
                   │
                   ▼
      ┌─────────────────────────┐
      │   3. Presence Router    │  --> Broadcasts live presence to everyone in that world
      └─────────────────────────┘

🗺️ Roadmap (Focused & Practical)
 * [x] Step 1 — Vision & Foundation Charter: Define the core philosophy (Foundation > Persistence) and repository structure.
 * [ ] Step 2 — MFL v0.1 Language Specification: Finalize the exact grammar rules for world, law, space, use, and ! signals.
 * [ ] Step 3 — The Micro-Parser: Write a zero-dependency parser that reads .mfl files and commands.
 * [ ] Step 4 — The Micro-Engine Prototype: Run multiple pluggable worlds in memory and test live !enter, !pulse, and !shift presence between them.
🤝 Contributing
We welcome thinkers, builders, and engineers who believe in simplicity.
When contributing to this repository, keep three rules in mind:
 * Keep it simple: If a child or a non-specialist can't understand the syntax, simplify it.
 * Keep it small: Do not add heavy dependencies or databases to the core engine.
 * Keep it extensible: Ensure any new world feature can be added via use without breaking the foundation.
📄 License
This project is open-source and available to everyone under the MIT License. See the LICENSE file for full details.

---

### ۳. متن کامل فایل `LICENSE` (مجوز MIT)

در صورتی که هنگام ساخت ریپازیتوری گزینه `Add a license -> MIT License` را از منوی گیت‌هاب انتخاب نکنید و بخواهید فایل `LICENSE` را دستی بسازید، متن استاندارد آن به شرح زیر است:

```text
MIT License

Copyright (c) 2026 Multiverse Foundation Contributors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

