# Episode 2: Designing the Game Engine & Roadmap

## Overview & Development Philosophy

Building a game engine from scratch is a massive undertaking, typically requiring large teams and extensive resources. Since this is a duo project, compromises and a realistic scope are necessary. 

* **Built-in Tooling:** Rather than building standalone, complex desktop applications for tools (like a [WPF](related_concepts/WPF.md) level editor), tools such as the level editor will be built directly into the engine's runtime using libraries like ImGui.
* **Initial Constraints:** To accelerate early development, the engine will initially target **Windows only** and use **OpenGL only**. However, the codebase will be strictly abstracted so that other platforms (Mac, Linux) and APIs (DirectX, Vulkan, Metal) can be supported later without a full rewrite.

## Core Architecture & Subsystems

A game engine is composed of several critical systems working together. The roadmap for this engine includes:

### 1. Entry Point & Application Layer

* **Entry Point:** The engine needs to dictate what happens when the application launches. This involves determining who controls the `main` function (the game client or the engine itself).
* **Application Layer:** Manages the application lifecycle, the core run loop (which keeps frames rendering and time moving forward), and routes events.
* **Window Layer:** Specifically for desktop platforms, this handles the creation of the application window, which serves as the target for graphics rendering and the source of input events.

### 2. Events & Input System

* **Event Manager:** A messaging and broadcast system where different layers of the application can subscribe to be notified when specific events occur (e.g., window resize, key press).
* **State Polling:** Alongside event messaging, the engine needs to poll the current state of input devices (e.g., checking the exact mouse position or if a key is currently being held down).

### 3. The Renderer & API Abstraction

* **Delayed 3D Rendering:** Surprisingly, building the full 3D renderer will not be the first step. The first few months will focus on debugging layers, core systems, and basic text/UI rendering. Establishing the core infrastructure first makes building a complex 3D renderer much easier later on.
* **Render API Abstraction:** The renderer will be designed to be API agnostic. While starting with OpenGL (because it is simple and cross-platform), the system is built to eventually support DirectX, Vulkan, and Metal without major code rewrites.

### 4. Debugging & Memory Management

* **Scaffolding:** Robust logging and profiling systems are crucial. Profiling (instrumenting code to time how long functions take) allows the developer to pinpoint performance bottlenecks.
* **Memory Systems:** Custom memory allocators and tracking systems will be implemented to monitor memory usage and optimize CPU time spent on allocations.

### 5. Gameplay & Content Systems

* **Entity Component System (ECS):** A system to create game objects in the world and modularize them by attaching components (e.g., transform, physics, scripts, audio) to define their behavior.
* **Scripting:** Integration of a higher-level language (like Lua or C#) so content creators can write game logic without dealing with C++ memory management.
* **Asset Pipeline:** Raw assets (3D models, textures) authored in external software will be converted offline into a custom, optimized format for the engine. The engine will also feature **hot-swappable assets**, meaning you can modify a texture in Photoshop and see it instantly update in the running game.