# Random.Event.Maze (Project_REM) 🟩
_An old-school, ASCII-flavored dungeon crawler built in Android Studio._

[![Platform](https://img.shields.io/badge/platform-Android-blue.svg)](#)
[![Language](https://img.shields.io/badge/language-Java%20%2B%20XML-green.svg)](#)
[![Status](https://img.shields.io/badge/status-v0.0.14-brightgreen.svg)](#)
[![License](https://img.shields.io/badge/license-MIT-lightgrey.svg)](#)

> Find the hidden **`D`** (Dungeon), defeat the boss, escape the maze—then do it again.
> Retro vibes, procedural generation, and a surprising number of cows.

---

## 📜 Table of Contents
- [About](#-about)
- [Core Features](#-core-features)
- [Gameplay Loop](#-gameplay-loop)
- [Controls](#-controls)
- [Screenshots](#-screenshots)
- [How It Works (Under the Hood)](#-how-it-works-under-the-hood)
- [Install & Run](#-install--run)
- [Save Data Format](#-save-data-format)
- [Roadmap](#-roadmap)
- [Contributing](#-contributing)
- [License](#-license)
- [Community](#-community)

---

## 🧭 About
**Project_REM** (Random.Event.Maze) is a lightweight dungeon crawler for Android that embraces a simple, readable style and a systems-first design. You spawn in a procedurally generated maze, explore points of interest (shops, characters, dungeon entrances), manage energy and stats, and trigger events on tiles. Your mission: locate the **Dungeon (`D`)**, clear the **Boss (`W`)**, grab the **Key**, and escape.

---

## 🧩 Core Features
- **Procedural Overworld**  
  A large ASCII-style maze with walls, paths, rubble clusters, barrels, rocks, homes, shops, and more.
- **Mini Dungeons & Bosses**  
  Enter the `D` to reach special maps and confront the **boss at `W`** for the Key item.
- **Turn & Energy System**  
  Movement and actions cost energy; **Rest** advances time and allows certain entities to act.
- **Seeker Enemies**  
  Smart “Seeker” entities move **only when you rest**, inching closer via A* pathfinding.
- **Cows (yes, really)**  
  Milk them (with cooldowns). If they can’t be milked, a UI popup tells you **“can milk again in X turns.”**
- **Shops with Unique Inventories**  
  Each shop generates its own item list and persists it by **`shopID`**.
- **Inventory & Equipment**  
  Weapons/Armor equip on click; Consumables use on click. Items come from `items.txt`.
- **Persistent Save System**  
  Stats, position, inventory, dungeon state, and more are written to formatted text files.
- **Retro UI**  
  Clean green-themed, pixel-inspired look with contextual action buttons (Speak, Milk, Break, Rest…).

---

## 🔁 Gameplay Loop
1. **Spawn** safely into the overworld (no walls).
2. **Explore** the maze; trigger events and collect items.
3. **Manage** health, gold, attack, defense, and energy.
4. **Visit** shops (`H`) to buy/sell; talk to characters.
5. **Find** the Dungeon (`D`), enter, and progress to the boss (`W`).
6. **Defeat** the boss → **Key** is added to your inventory.
7. **Escape** the maze and bask in glory. Repeat with a fresh world.

---

## 🎮 Controls
- **Move**: On-screen controls / swipe / D-pad (depending on your build).
- **Actions**: Context buttons appear when relevant (e.g., **Milk**, **Break**, **Speak**, **Rest**).
- **Inventory**: Open from the main screen (grid of 6+ slots).  
  - **Tap Item** → Equip (Weapon/Armor) or Use (Consumable)
- **Rest**: Recover energy; advances turns (seekers may move).

---

## 🖼️ Screenshots
> Put images in `assets/screenshots/` and update the links below.

<p align="center">
  <img src="assets/screenshots/overworld.png" alt="Overworld" width="45%">
  <img src="assets/screenshots/dungeon.png" alt="Dungeon" width="45%">
</p>

<p align="center">
  <img src="assets/screenshots/inventory.png" alt="Inventory" width="45%">
  <img src="assets/screenshots/shop.png" alt="Shop" width="45%">
</p>

---

## 🔬 How It Works (Under the Hood)
- **World Generation**  
  Grid-based ASCII map with safe spawn, special tiles (`D`, `W`, `H`, rubble `'`, etc.), and colorized rendering.
- **Entities & Behaviors**  
  Entity system with **SeekerBehavior** (A* pathing; acts during Rest), cows with milk cooldowns, and more.
- **Event System**  
  Terrain and entity interactions (barrel/rock break, rubble events, cow dialogs, shops, boss trigger).
- **Energy & Turns**  
  Every action has a cost. Resting restores energy and advances a discrete number of “rest steps.”
- **Persistence**  
  `Saved_Data` serializes player, inventory, map, dungeon flags, follower positions, and more across activities.

---

## 🛠 Install & Run
**Requirements**
- Android Studio (latest stable)
- Android SDK 24+
- Java 8+ (project uses Java + XML)


**Build Steps**
1. **Clone** the repo:
   ```bash
   git clone https://github.com/<your-username>/<your-repo>.git



**Install Directly to Your Android Device**
- Install the APK from the most recent release


