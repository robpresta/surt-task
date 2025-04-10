
# SURT Task – Adaptive Visual Attention Task for Driving Simulation

This repository contains a customizable implementation of a **Surrogate Research Task (SURT)** designed to be used during driving simulation experiments.

The task presents visual targets and distractors within four screen quadrants. Participants are required to touch the quadrant containing the red target while ignoring the green distractors. The interface supports full-screen interaction and is optimized for **touch devices (e.g. iPad)**.

## 🧪 Key Features

- ✅ Customizable parameters via configuration panel
- ✅ Participant ID entry
- ✅ Real-time response logging
- ✅ Timeout and IVI (Inter-trial Visual Interval) control
- ✅ Fixed 10-second rhythm between stimuli
- ✅ CSV export with file name based on participant ID and timestamp
- ✅ Fully offline, HTML-based implementation (no backend or internet required after loading)

## 🧰 Configuration Options

On launch, users can customize:

| Parameter             | Description                                                  | Default |
|-----------------------|--------------------------------------------------------------|---------|
| Participant ID        | Identifier used in the filename                              | `P01`   |
| Number of Trials      | Maximum number of trials (auto-stops at end)                 | `100`   |
| Distractors per Trial | Number of green outlined squares shown per trial             | `20`    |
| Stimulus Timeout      | Max time (ms) to respond before timeout is recorded          | `5000`  |
| Total Trial Time      | Fixed time (ms) between the start of two consecutive trials  | `10000` |

## 🗃️ Output Format

At the end of the task (or if stopped manually), a `.csv` file will be downloaded. The filename is automatically generated in the format:
  [id][yymmdd][hhmm].csv
For example:
  P01_250409_1746.csv
The file includes the following columns:
- `Trial`
- `TargetQuadrant`
- `ClickedQuadrant`
- `Correct` (true/false)
- `ResponseTime_ms`
- `ResponseTime_s`
- `Timeout` (true/false)

## 📱 Deployment & Usage

The SURT task is designed to run in a web browser and is compatible with both desktop and mobile devices.
You can access the official hosted version here:

👉 https://robpresta.github.io/surt-task/

This implementation is distributed as an open resource.  
Feel free to reuse, adapt, or integrate it in your own research or design workflow.  
If you do so, a citation or reference is always appreciated.

## 🎓 Credits

Developed by [Roberta Presta](mailto:roberta.presta@unisob.na.it) – University of Suor Orsola Benincasa (UNISOB), Naples  
Logo and visual identity: UNISOB

---

📬 For feedback, contributions, or collaboration proposals, feel free to open an issue or contact me directly.



