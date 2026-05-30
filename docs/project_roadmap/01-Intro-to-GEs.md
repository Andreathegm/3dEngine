# Episode 1: What is a Game Engine?

## Overview

The goal of this project is to build a game engine from scratch, primarily using C++ (with potential use of other languages like C#). A game engine is essentially a platform used to build interactive applications. While primarily used for video games, engines can also power VR applications, simulations, and architectural visualizations.

## Core Definition

At its most fundamental level, a game engine is designed for **data transformation**.

* It reads existing files (assets) from a disk.
* It transforms that data into a format that can be rendered and displayed on a screen.
* It provides interactive capabilities so the user can interact with that visual data.

Because it relies heavily on loading existing files rather than creating data out of nowhere, game engine architecture is extremely **data-oriented**.

## Assets and Content Creation

- **Assets:** Any file or data input that the game engine reads (e.g., textures, 3D models, audio).
- **Content Creators:** Artists and level designers typically build these assets in external, third-party software like Photoshop, Blender, or Maya.
- **Engine Formatting:** The engine rarely takes raw formats (like generic `.obj` or `.png` files) directly for complex projects; instead, tools process and convert these assets into a custom format specific to the engine.
- **Tooling:** A major component of a game engine is its suite of tools (like a level editor). This allows content creators who are not programmers to author and place data within the world without writing raw source code.

## Engine Systems & Architecture

* **Platform Abstraction Layers:** These layers hide the specific details of different hardware platforms (Windows, Mac, Linux, mobile, or consoles) so developers can write generalized code that runs anywhere.
* **Core Systems:** Include rendering, audio processing, file input/output (I/O), and serialization.

## Why Build/Use an Engine?

Modern games are vastly complex. Without an engine, a development team would be forced to build core technologies from scratch for every single game they release. Game engines solve this by providing a robust, reusable foundation so developers and artists can focus simply on taking data and putting it on the screen.
