# SECOND SHIFT

**A real-time nuclear operations simulator, a social deduction game and an analogue horror story, played through one keypad.**

You are a licensed reactor operator on the night shift at a fictional coastal nuclear station. Every consequential action passes through a keypad: type a command, inspect its echo, and execute it. Run the plant, watch the instruments, and decide what to do as the shift unfolds.

[![Play in browser](https://img.shields.io/badge/Play-Second%20Shift-8B5CF6?style=for-the-badge)](index.html)
[![Single-file game](https://img.shields.io/badge/Format-Single%20HTML%20file-22C55E?style=for-the-badge)](index.html)
[![No install required](https://img.shields.io/badge/Setup-No%20install%20needed-FF8C00?style=for-the-badge)](index.html)
[![License](https://img.shields.io/badge/License-GPLv3-DC2626?style=for-the-badge)](LICENSE)

The game is a self-contained HTML document: no build step, dependencies, or network access are needed to play. Open `index.html` in a modern browser, or [play the published version](https://goldenration77.github.io/second-shift/).

## Recent updates

- The browser game is now served from `index.html` (replacing the old `Second_Shift.html` entry point); the play and setup links here point to the current file.
- GitHub Pages asset URLs for the app icons and web-app manifest now include the repository’s `/second-shift/` path, so those resources resolve correctly when hosted as a project site.
- The desktop-app build workflow now uses the published `index.html` URL.

## Screenshots

<p align="center">
  <img src="screenshots/secondshift1.jpeg" alt="SECOND SHIFT control room interface" width="48%" />
  <img src="screenshots/secondshift2.jpeg" alt="SECOND SHIFT reactor and annunciator view" width="48%" />
</p>

## Quick start

1. Open or download `index.html`.
2. Open it in a modern browser (Chrome, Firefox, Safari, or Edge).
3. Choose a mode and press **BEGIN SHIFT**.

No server or internet connection is required to play after the file is downloaded. The repository also includes a web-app manifest and icons for the published site.

## Game modes

| Mode | Players | What it asks |
|---|---:|---|
| **SIMULATOR** | 1 | Operate the plant, from hot standby to full power, or manage the channel-type RBMK. No timer or antagonist. |
| **NIGHT SHIFT** | 1 | Work three shifts while the building is quietly wrong. The horror director runs here. |
| **CREW** | 2–4, one screen | Find the fifth name on the log before the shift review. The plant is a shared alibi. |
| **STORY** | 1 | Play four historical-accident scenarios. |

## Two reactor models

- **Kaveri Delta Unit 3:** a fictional 540 MWe pressurised heavy-water reactor with pressurised coolant, boron shim, regulating rod banks, and on-power refuelling.
- **Unit 4:** a channel-type RBMK model with individually drivable control rods, a positive void coefficient, and a low operational reactivity-margin limit.

The simulation includes point kinetics, reactivity feedback, xenon and iodine, decay heat, primary and secondary heat balances, electrical systems, and fuel-damage effects. These are game models, not engineering or training tools.

## The control room

The 1600 × 900 logical board brings together an annunciator matrix, analogue instruments and recorder, plant mimic, safety-function display, command console, and keypad. The station also has nine explorable rooms, blast doors, multiple consoles, a survey meter, and equipment that may become inaccessible as conditions deteriorate.

Commands are entered through the keyboard or on-screen keypad. `TAB` completes an unambiguous tag, `HIST` or the up arrow recalls a command, `ESC` clears the buffer, and **EXECUTE** commits it. `F1` opens the handbook.

## Story scenarios

| Scenario | Year | Focus |
|---|---:|---|
| **SL-1** | 1961 | Rod worth and prompt criticality |
| **Three Mile Island** | 1979 | A stuck PORV and a misleading level indication |
| **Fukushima Daiichi** | 2011 | Station blackout, batteries, and decay heat |
| **Chernobyl Unit 4** | 1986 | Positive scram, void coefficient, and reactivity margin |

## Technical notes

- The game is delivered as a single HTML document with inline styling and JavaScript; artwork is inline SVG/canvas and sound is generated with WebAudio.
- The simulation runs at a fixed 10 Hz with a seeded random number generator. Plant-time settings change the simulation rate, not the tick rate.
- The repository includes a GitHub Actions workflow for building desktop-app release artifacts from the published game.

## What is not modelled

This project is a game, not a training simulator. The core is lumped rather than spatial; the parameters are tuned for play and are not licensed design-basis data. CREW uses simulated colleagues on one screen; it is not online multiplayer. Windscale and Tokaimura are not included.

## Disclaimer

SECOND SHIFT is a fictional plant with fictional procedures. It is **not** a training tool, a simulator of any real reactor, or a depiction of any real utility or event. Do not use it to make real-world operational decisions.

Rated T — tension and dread, no gore.

## Licence

Source and design © Soumyajit Roy, 2026. Concept and design by Soumyajit Roy. GNU GPLv3. Made with Sarvam.
