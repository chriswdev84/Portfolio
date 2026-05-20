# Slime Climb

[![Unity](https://img.shields.io/badge/Unity-2021.3+-black.svg)](https://unity.com/) [![C#](https://img.shields.io/badge/C%23-8.0-blue.svg)](https://docs.microsoft.com/dotnet/csharp/) [![URP](https://img.shields.io/badge/URP-recommended-green.svg)](https://docs.unity3d.com/Packages/com.unity.render-pipelines.universal@latest)

## Overview

Slime Climb is a 2D vertical platformer made in Unity where you control a slippery slime and climb toward the top of each level using precise aiming and timed jumps. The game emphasizes mastery of movement through collectible power-ups that unlock mechanics like double jump, dash, and shooting.

## Why this project?

I built this game to become more comfortable with Unity and to showcase my game-development skills. I wanted to create a tight 2D platformer experience inspired by precision-climbing games such as Jump King. The project helped me explore player controllers, ability systems, level design, and polish in a small, focused game.

## Screenshots

<a href="screenshots/BigSlime.png"><img src="screenshots/BigSlime.png" width="300" alt="Big Slime & Vine Walls"></a>
<a href="screenshots/Breakable.png"><img src="screenshots/Breakable.png" width="300" alt="Breakable Stone"></a>
<a href="screenshots/Dash.png"><img src="screenshots/Dash.png" width="300" alt="Dash Power-Up"></a>

## Features

- **Precise Movement**: Custom character controller with aiming and jump control.
- **Ability Progression**: Collect power-ups to unlock Double Jump, Dash, and Projectile Shooting.
- **Physics Interactions**: Surfaces with different friction, wall bounce, and momentum-based traversal.
- **Level Design**: Vertical, layered challenges that reward sequencing and timing.
- **Visual & UX Polish**: Smooth camera, trajectory indicator, and clear feedback for player actions.

## Controls

- Move: A/D or Arrow Keys
- Jump: Space
- Dash: Right Mouse Button (requires power-up)
- Shoot: Left Mouse Button (requires power-up)
- Toggle Trajectory: T

## Prerequisites

- Unity 2021.3 LTS or later
- Universal Render Pipeline (URP) recommended

Verify your Unity installation via Unity Hub before opening the project.

## Setup & Running

1. Clone the repository:

```
git clone https://github.com/chriswdev84/slime-climb
cd slime-climb
```

2. Open the project folder in Unity Hub.
3. Open the main scene (Assets/Scenes/) and press Play in the Editor.

## Building a Standalone Player

1. Go to File > Build Settings.
2. Add the scenes you want to include.
3. Select your target platform and click Build.

## Project Structure

```
Assets/
├── Scripts/          # Core gameplay systems and controllers
├── Scenes/           # Game levels and test scenes
├── Art/              # Sprites and textures
├── Animations/       # Animations for characters and objects
├── Prefabs/          # Reusable game objects
└── Settings/         # Graphics, input, and pipeline settings
```

## Technical Details

- Physics: Rigidbody2D-based controller with custom movement logic
- Input: New Input System for flexible control mapping
- Rendering: URP for consistent 2D lighting and post-processing

---

Built with Unity. Inspired by precision climbing platformers.