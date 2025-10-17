# Advanced Autoclicker with Fluent UI

![Project Screenshot](https_placeholder_for_your_app_screenshot.png)
*(Note: You should replace the placeholder above with an actual screenshot of your application)*

A powerful, feature-rich autoclicker built with Python and PyQt6. This application goes beyond simple clicking, offering advanced targeting controls, multiple activation modes, and a sleek, modern user interface inspired by Fluent Design.

It is designed to be both highly functional for complex automation tasks and intuitive for everyday use.

## Core Features

This autoclicker is packed with features that provide precision, control, and convenience for a wide range of applications, from gaming to data entry.

### ⚙️ Clicking Engine
- **Adjustable Click Speed:** Set a precise number of clicks per second (CPS) using a responsive slider.
- **Dynamic CPS Modes:** Choose from pre-configured speed tiers to quickly change performance:
    - **Normal (1-30 CPS):** Safe for most applications.
    - **Fast (31-50 CPS):** High speed that may be suspicious in some contexts.
    - **Extreme (51-80 CPS):** Highly detectable speed for high-risk use.
    - **Insane (81-100 CPS):** Maximum output for experimental purposes, virtually guaranteed to be detected.
- **Mouse Button Selection:** Choose between **Left**, **Right**, or **Middle** mouse buttons.
- **Click Type Emulation:** Emulate **Single** or **Double** clicks.
- **Click Randomization:** Introduce slight, random delays between clicks to mimic human behavior, making automation less detectable.

### 🎯 Advanced Targeting System
- **Current Mouse Position:** The default mode, clicking at the current location of your mouse cursor.
- **Specific Coordinates:** Set a fixed X/Y coordinate on the screen for all clicks.
    - Includes a **Pixel-Perfect Location Picker**, an overlay tool with a crosshair and magnifier to precisely select screen coordinates.
- **Specific Window Targeting:** A powerful filter that restricts all clicking actions to a chosen application window. The autoclicker will automatically pause if the mouse moves outside the window and resume only when it re-enters, ensuring other applications are not accidentally clicked.

### ⚡ Activation & Control
- **Fully Customizable Hotkeys:** Set your own unique keys to start and stop the autoclicker.
- **Dual Activation Modes:**
    - **Toggle Mode:** The classic mode. Press the start hotkey to begin clicking and the stop hotkey to end.
    - **Hold Mode:** A more direct control method. Clicking is only active *while the activation hotkey is being held down* and stops instantly upon release.

### 💾 Automation & Persistence
- **Click Limiter:** Configure the autoclicker to stop automatically after a specific number of clicks has been reached. Ideal for tasks that require a finite number of actions.
- **Profile System:** Save complex configurations (CPS, targeting, hotkeys, etc.) as named profiles. Load any profile with a single click to instantly switch between setups for different tasks.
- **Session Logs:** View a history of past autoclicking sessions, including start/end times and total clicks.

## Technology Stack

- **Language:** Python 3
- **Framework:** PyQt6 for the graphical user interface.
- **Core Libraries:**
    - `pynput`: For listening to and controlling mouse and keyboard events.
    - `pygetwindow`: For finding and managing application windows for the targeting feature.

## Installation & Usage

To run this application, you will need Python 3 and a few external libraries.

#### 1. Prerequisites
- Python 3.x

#### 2. Setup
1.  Clone the repository to your local machine:
    ```bash
    git clone https://github.com/Arman-0909/smiteclickerautoclicker.git
    ```
2.  Navigate into the project directory:
    ```bash
    cd smiteclickerautoclicker
    ```
3.  Install the required Python libraries (it's recommended to use a virtual environment):
    ```bash
    pip install PyQt6 pynput pygetwindow
    ```
4.  Run the application:
    ```bash
    python main.py
    ```

## Project Structure

The project is organized into a modular structure for clarity and scalability.

/autoclicker
│
├── core/ # Backend logic (autoclicker thread, state management)
├── database/ # Database management for profiles and logs
├── resources/ # All static assets (icons, fonts, stylesheets)
├── ui/ # All frontend PyQt6 code
│ ├── views/ # Individual screens/pages of the application
│ └── custom_widgets.py # Reusable custom UI components
│
├── .gitignore # Specifies files for Git to ignore
├── main.py # Main entry point for the application
├── main_window.py # Defines the main application window structure
└── README.md # This file

## Contributing

Contributions are welcome! If you have ideas for new features or find a bug, please feel free to open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
