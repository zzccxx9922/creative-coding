**Interactive Galaxy**

An interactive, galaxy-inspired artwork made with **Processing Python Mode**. Move the pointer to push nearby stars, click to create a burst of new stars with a randomly selected sound, and press **R** to start a fresh star field.

Created by **Chenxu Zhao** as a creative coding coursework project, it explores how simple rules, randomness, movement, and sound can create an experience shaped by its viewer. It is an artistic interpretation of a galaxy, not an astronomical simulation.

## Table of Contents

- [Features](#features)
- [Visual Preview](#visual-preview)
- [Technologies and Requirements](#technologies-and-requirements)
- [Setup](#setup)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [Troubleshooting](#troubleshooting)
- [Project Status](#project-status)
- [Room for Improvement](#room-for-improvement)
- [Acknowledgements and Credits](#acknowledgements-and-credits)

- ## Features

- A 1000 x 700 canvas with 60 randomly generated starting stars.
- Random star positions, sizes, colours, directions, and initial speeds.
- Continuous movement with stars wrapping around the canvas edges.
- Mouse repulsion within a visible, 120-pixel-radius interaction area.
- Six faster-moving stars created at the pointer position on each click.
- One click sound randomly chosen from three WAV files per click.
- Background music that starts with the sketch and restarts after successful playback completion.
- An R-key reset and visible on-screen controls.

- ## Visual Preview
<img width="1000" height="696" alt="截屏2026-10-22 下午5 08 10" src="https://github.com/user-attachments/assets/e751cf7e-d851-4ecb-bbc6-3ae9ef8c24d9" />

*The final sketch also includes audio and music.

## Technologies and Requirements

Component | Details |
| --- | --- |
| Operating system | macOS, required by the current audio implementation |
| Graphics environment | Processing with a compatible Python Mode installation |
| Sketch language | Processing Python Mode (`.pyde`) |
| Audio | Python's `subprocess` module starts `/usr/bin/afplay` |
| Assets | Four WAV files in the sketch's `data/` folder |
| Input and output | Pointer or trackpad, keyboard, and speakers or headphones; a separate mouse is more comfortable

**Compatibility note:** No separate Processing audio library is used by the sketch.

## Setup

### Repository Layout

Keep the final sketch and its audio together.
