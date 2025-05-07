
# SURT Double Task WebApp

This repository contains a customizable implementation of a **Surrogate Research Task (SURT)** designed to be used during driving simulation experiments.

The task presents visual targets and distractors within four screen quadrants. Participants are required to touch the quadrant containing the red target while ignoring the green distractors. The interface supports full-screen interaction and is optimized for **touch devices (e.g. iPad)**.

## Features

- Sequential visual stimuli (target + distractors) per trial
- Conditional second task only if a response is given to the first
- Fully configurable: trial count, stimulus duration, total trial time
- Timed execution logic enforcing fixed-duration cycles
- Auditory cue playback at the start of each trial
- CSV export with millisecond precision response timing and accuracy

## Parameters

| Setting           | Description                                     |
|-------------------|-------------------------------------------------|
| `Number of Trials` | Total number of 10s (or user-defined) cycles    |
| `Stimulus Timeout` | Max duration (ms) of each task before timeout   |
| `Total Trial Time` | Fixed duration (ms) for each trial cycle        |

Trials proceed autonomously with no pauses between them.

## Data Logging

Each response (or timeout) is logged as a row in the exported `.csv`. Columns include:

- `Trial`: Sequential index (1-based)
- `Task`: 1 or 2
- `TargetQuadrant`: Correct location (1–4)
- `ClickedQuadrant`: User selection
- `Correct`: `true` or `false` (including timeouts)
- `ResponseTime_ms`: Latency in ms
- `ResponseTime_s`: Latency in seconds (2 decimals)
- `Timeout`: `true` if no response was recorded in time

## Usage

1. Open `double_task_timing_working.html` in a modern browser (Chrome recommended)
2. Configure parameters
3. Press **Start**
4. On completion or interruption, a CSV file will be downloaded

The auditory cue (`PLIN.mp3`) must be placed in the same directory as the HTML file.

## Deployment

No backend required. This app runs entirely client-side and offline. Suitable for lab-based cognitive experiments or remote deployment.

## License

MIT License — see [`LICENSE`](./LICENSE) for details.

## Maintainer

Developed and maintained by Roberta Presta - HumaDes @ Scienza Nuova - Università degli Studi Suor Orsola Benincasa.
Contact: roberta.presta@unisob.na.it
