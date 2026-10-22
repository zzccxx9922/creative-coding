**Interactive Galaxy**

An interactive, galaxy-inspired artwork made with **Processing Python Mode**. Move the pointer to push nearby stars, click to create a burst of new stars with a randomly selected sound, and press **R** to start a fresh star field.

Created by **Chenxu Zhao** as a creative coding coursework project, it explores how simple rules, randomness, movement, and sound can create an experience shaped by its viewer. It is an artistic interpretation of a galaxy, not an astronomical simulation.

## Table of Contents

- [Features](#features)
- [Visual Preview](#visual-preview)
- [Technologies and Requirements](#technologies-and-requirements)
- [Setup](#setup)
- [Run the Sketch](#run-the-sketch)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [Project Status](#project-status)
- [Room for Improvement](#room-for-improvement)
- [Acknowledgements](#acknowledgements)
- [Contact](#contact)
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
The overall project includes a main sketch and four WAV audio files.

Keep the main sketch and its audio together.

The sketch folder and main file are both named `creative_coding`. Keep the WAV filenames exactly as shown because the audio functions use these names.


### Run the Sketch

1. Download or clone the repository and extract it if necessary.
2. Open a Processing installation with a working Python Mode. Select **Python**, not Java, in the mode selector.
3. Open `creative_coding/creative_coding.pyde`.
4. Check that all four WAV files are inside `creative_coding/data/`.
5. Set a comfortable system volume and click **Run**.
6. Click the sketch window to give it focus before using the reset key.

**Compatibility note:**This project is not guaranteed to run on all versions of Python models.

## Usage

Action | Response |
| --- | --- |
| Move the pointer near stars | Push nearby stars away within the interaction radius. |
| Click the canvas | Add six stars at the pointer and request one randomly selected click sound. |
| Press `r` or `R` | Replace the current stars with 60 newly randomised stars, without restarting music through the reset function.

## How It Works

Each `Star` object stores its position, size, colour, and velocity. The `stars` list holds the objects so that the drawing loop can update and display them repeatedly. Clicking appends new objects to that list.

The click handler deliberately separates repeated star creation from sound playback.

The sound call is outside the loop: one click creates six stars but makes only one playback request. `subprocess.Popen()` starts the audio player without waiting for playback to finish. The background track is restarted when `poll()` reports successful completion; a gapless musical loop is not guaranteed.

The source is organised into 12 commented parts covering settings, storage, setup, drawing, galaxy outlines, the mouse guide, title, clicking, the `Star` class, audio, reset, and on-screen instructions.

## Project Status

**Final  prototype.** The listed controls and audio logic are implemented in the source. Cross-platform compatibility, broader hardware testing, and the improvements below are not presented as completed work.

## Room for Improvement

One of my friend tried the project on the development computer and responded positively to the overall experience. Their feedback highlighted trackpad usability, audio compatibility beyond macOS, and opportunities for more varied background interaction. This was a playtest on one computer, not a cross-device test.

Planned improvements include:

- Keyboard alternatives for viewers without a separate mouse.
- Mute and volume controls.
- A cross-platform audio approach and testing on the intended devices.
- Subtle background brightness changes or responses to accumulated interaction.
- A star-count limit and checks for responsiveness during repeated clicks.
- Audio-process cleanup when stopping or restarting the sketch.

## Acknowledgements
-This project was inspired by space documentaries I'd watched before, as well as some science fiction games I'd played.
-This project was base on processing and Python Mode.
-Many thanks to my friend who help me test and give me feedback and some creator who upload case sketches and instructional videos.

## Contact
Created by Chenxu ZHAO-Have any ideas please to contact me!
