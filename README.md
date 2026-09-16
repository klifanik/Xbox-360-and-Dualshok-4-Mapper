# HID → Xbox 360 & Dualshock 4 Mapper

A minimalist alternative to x360ce: turns any HID joystick/gamepad into a virtual Xbox 360 controller or Dualshock 4 controller so that games and programs that only understand XInput can see your device.

Works only on **Windows** (uses the [ViGEmBus](https://github.com/ViGEm/ViGEmBus) driver via the [vgamepad](https://pypi.org/project/vgamepad/) library).

## Features

- Assigning any button/axis/hat (D-pad) of a physical joystick to any output of a virtual Xbox 360 or Dualshock 4 (sticks, triggers, buttons, D-pad).
- Quick calibration of one output or all of them at once, one after another.
- Digital axis mode (values only `0`/`±1`) — enabled via a checkbox.
- Direction inversion for each axis separately.
- The ability to assign an analog stick as a digital D‑pad (for example,  “left push” → LEFT button), without conflicting with the normal axis assignment.
- Several physical sources per output (for example, a stick **and**
  the crosspiece is simultaneously controlled by LX/LY) — what is active right now is working.
- The "Input test" button is a live window for viewing raw data from the joystick,
  to check if the program sees the device at all.
- The "Start" button/Stop" — you can pause the transfer to the virtual
gamepad without closing the program.
- Saving/loading the layout in `controller_mapping.json`.

## Installation

1. Download/clone the repository.
2. Install python 3.11 or newer manually. (AUTO INSTALL TEMPORARILY NOT WORKING)
   Link to download: https://www.python.org/downloads/
2. Run **`install.bat`** — it will install all dependencies
   (`pygame`, `vgamepad'). You may need to confirm
   installing the ViGEmBus driver (separate UAC/installer window).
3. If a virtual gamepad is not created after installation, install
   Driver manually: https://github.com/ViGEm/ViGEmBus/releases

## Launch

Just run **`run.bat`**.

## Usage

1. Select your device from the drop‑down list at the top.
2. Click “Assign” next to the desired output (for example, `LX`) and, within
   5 seconds, move/press the corresponding element on the physical joystick —
   The assignment will happen instantly as soon as the program recognizes the signal.
3. Or click “Calibrate all outputs” and go through all the axes and buttons in sequence.
4. “Input test” will show what the program physically sees — useful for diagnostics if the assignment doesn’t work.
5. “Save”/“Load” — so you don’t have to reconfigure the layout every time.

## License

MIT — do whatever you want with the code, see [LICENSE](LICENSE).