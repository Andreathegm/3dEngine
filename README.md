# Game Engine From Scratch

A modern reinterpretation of the game engine series by The Cherno.

## Overview

This project follows and documents the famous game engine development playlist created by The Cherno, while recreating the engine from scratch in C++ and modernizing the original implementation where improvements are possible.

The original series started in 2019 and covers the architecture and development of a complete game engine. Since many technologies, libraries, and best practices have evolved since then, this project aims not only to reproduce the engine but also to analyze design decisions and introduce modern alternatives when appropriate.

The goal is to deeply understand how professional game engines are built internally rather than simply using existing solutions such as Unreal Engine or Unity.

---

## Project Goals

* Recreate the engine developed throughout The Cherno's series.
* Document every major system and architectural decision.
* Understand low-level engine programming concepts.
* Compare the original 2019 implementation with modern approaches.
* Refactor and improve parts of the engine when newer techniques provide better performance, maintainability, or scalability.
* Build a personal knowledge base about game engine architecture.

---

## What We Are Building

The engine will gradually evolve to include:

* Window management
* Event system
* Rendering pipeline
* OpenGL graphics abstraction
* Entity Component System (ECS)
* Scene management
* Asset management
* Physics integration
* Scripting support
* Editor tools
* Serialization
* Resource loading

Each feature will be documented and analyzed throughout development.

---

## Technologies

### Core

* C++
* OpenGL
* GLFW
* Glad

### Potential Future Additions

* ImGui
* ECS frameworks
* Vulkan experimentation
* C# scripting support
* Modern rendering techniques

---

## Structure

```text
GameEngine
    │
    ├── Engine/
    ├── Sandbox/
    ├── Docs/
    ├── Assets/
    └── README.md
```

* **Engine** → Core engine source code.
* **Sandbox** → Testing application used during development.
* **Docs** → Notes, documentation, and episode summaries.
* **Assets** → Textures, models, shaders, and resources.

---

## Documentation

One of the main objectives of this repository is documentation.

For each episode we provide:

* Summary of concepts covered
* Notes and explanations
* Code analysis
* Improvements over the original implementation
* Additional references and resources

Example:

```text
Docs/
├── Episode01.md
├── Episode02.md
├── Episode03.md
└── ...
```

---

## Why This Project Exists

Following a tutorial series is useful.

Understanding why every system is designed the way it is is far more valuable.

This repository is intended to transform a passive tutorial into an active engineering study, documenting both the original implementation and possible modern improvements.

---

## Credits

This project is heavily inspired by the incredible work of The Cherno and his Game Engine Series.

Original playlist:

https://www.youtube.com/@TheCherno

All credit for the original educational content belongs to The Cherno.

---

## Disclaimer

This repository is an educational project.

The objective is to learn game engine architecture, graphics programming, software design, and modern C++ development through implementation, experimentation, and documentation.
