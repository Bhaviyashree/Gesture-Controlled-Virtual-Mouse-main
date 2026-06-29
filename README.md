# Gesture Controlled Virtual Mouse

[![Python 3.8.5](https://img.shields.io/badge/python-3.8.5-blue.svg)](https://www.python.org/downloads/)
[![Platform Windows](https://img.shields.io/badge/platform-windows-green.svg)](https://github.com/xenon-19/Gesture_Controller)

A Windows application that enables mouse control using hand gestures and voice commands. It includes:
- gesture-driven cursor movement, clicks, scrolls, and drag-and-drop
- a voice assistant named **Proton** for launching/stopping gestures, search, navigation, and clipboard control
- MediaPipe-based hand detection and optional glove-based gesture support

> Demo video: [https://www.youtube.com/watch?v=ufm6tfgo-OA&ab_channel=Proton](https://www.youtube.com/watch?v=ufm6tfgo-OA&ab_channel=Proton)

## Features

### Gesture controls
- Move cursor using hand landmarks
- Left, right, and double click gestures
- Scroll vertically and horizontally
- Drag and drop
- Select multiple items
- Volume and brightness control
- Neutral gesture to stop or pause gesture execution

### Voice assistant — Proton
- `Proton Launch Gesture Recognition`: starts gesture mode
- `Proton Stop Gesture Recognition`: stops gesture mode
- `Proton search <query>`: opens Google search in Chrome
- `Proton find a location`: searches Google Maps
- `Proton list files`, `Proton open <number>`, `Proton go back`: navigate files by voice
- `Proton date`, `Proton time`: get current date/time
- `Proton copy`, `Proton paste`: clipboard control
- `Proton bye` / `Proton wake up`: pause/resume voice commands
- `Proton exit`: close the assistant

## Requirements

- Windows
- Python 3.8.5
- Recommended: Anaconda / Miniconda

## Dependencies

Install using:

```bash
pip install -r requirements.txt
```

The repository uses:
- pyttsx3
- SpeechRecognition
- pynput
- pyautogui
- wikipedia
- opencv-python
- mediapipe
- pycaw
- screen-brightness-control
- eel
- comtypes

## Setup

1. Clone the repository:

```bash
git clone https://github.com/xenon-19/Gesture-Controlled-Virtual-Mouse.git
cd Gesture-Controlled-Virtual-Mouse-main
```

2. Create and activate a conda environment:

```bash
conda create --name gest python=3.8.5
conda activate gest
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Install additional Windows packages:

```bash
conda install pywin32
conda install pyaudio
```

## Running the app

Run from the `src` directory:

```bash
cd src
python Proton.py
```

This starts the Proton voice assistant. Use voice commands such as `Proton Launch Gesture Recognition` to enable gesture control.

## Gesture-only mode

If you only want gesture recognition without voice assistant, open `src/Gesture_Controller.py`, uncomment the last two lines at the bottom, then run:

```bash
python Gesture_Controller.py
```

## Notes

- Use Chrome for browser-based voice commands and search features.
- The application is designed for Windows and Python 3.8.
- The `src/Proton.py` file starts the voice assistant and integrates with `src/app.py`.

## Contributors

- Nishiket Bidawat — [xenon-19](https://github.com/xenon-19)
- Viral Doshi — [Viral-Doshi](https://github.com/Viral-Doshi)
- Ankit Sharma — [ankit-4129](https://github.com/ankit-4129)
- Parth Sakariya — [parth-12](https://github.com/parth-12)
