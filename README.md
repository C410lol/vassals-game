# Vassals

**Vassals** is a 2D platform game developed with **C++ and SFML**. The project focuses on applying Object-Oriented Programming, organizing game entities, managing game states, and implementing custom systems to control the game's execution.

One of the project's main aspects is the implementation of the game engine structure and core game systems in C++, using SFML as the library for graphics, window management, audio, and input.

## 🎮 About the game

The game features platform levels with playable characters, enemies, and obstacles with distinct behaviors. Its structure includes:

- Menus for navigation, player selection, and level selection.
- Separate states for the menu and gameplay.
- Levels organized into their own classes.
- Playable characters and an enemy system.
- Ground enemies, flying enemies, and a boss.
- Obstacles such as platforms, spikes, and slime, each with specific behaviors.
- Projectiles and interaction elements for entities in the game world.
- Pause, score, and ranking menus.
- Local files used to persist game data and scores.

## 🧩 Architecture and applied concepts

The code is divided into modules representing the game's main responsibilities:

- **Entities:** base classes and specializations for characters, enemies, projectiles, and obstacles.
- **Levels:** construction and management of game levels.
- **States:** controls transitions between the menu and gameplay.
- **Managers:** graphics, collision, and state management.
- **Menus:** components and screens for navigation, pause, players, scores, and rankings.
- **Observer:** structure for communicating input events between the subject and observers.

This organization separates the game logic into components with specific responsibilities, making the project easier to maintain and extend.

## 🧰 Technologies

- **C++11**
- **SFML 2.x** — window, graphics, audio, and input.
- **CMake 3.16+**
- Object-Oriented Programming
- Observer pattern

## 📁 Project structure

```
vassals-jogo/
├── assets/       # Images, fonts, backgrounds, and game resources
├── fases-template/ # Level configuration files
├── includes/     # Header files organized by module
├── src/          # Class implementations
├── salvamentos/  # Local score and save files
├── main.cpp
└── CMakeLists.txt
```

## ▶️ How to build and run

### Prerequisites

- CMake 3.16 or higher.
- A C++ compiler with C++11 support.
- SFML with the `system`, `window`, `graphics`, and `audio` modules.

On Debian/Ubuntu-based Linux distributions, the library can be installed with:

```bash
sudo apt update
sudo apt install build-essential cmake libsfml-dev
```

### Build

From the repository root:

```bash
cmake -S . -B build
cmake --build build
```

CMake is configured to generate the executable in the `bin/` directory. On Linux, run:

```bash
./bin/jogo
```

On Windows, the `CMakeLists.txt` file expects to find the SFML 2.6.2 distribution at `tools/SFML-2.6.2`, according to the platform-specific configuration.

---

Project developed as part of the academic course on Programming Techniques.
