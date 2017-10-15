# eduke32

revision R5700 that includes bug-fixes for joystick-related annoyances, especially for XInput controllers

## Installation
(tested under Windows 10)
- download 32-bit or 64-bit version [here](https://github.com/aybe/eduke32/releases)
- extract the archive to some folder, e.g. `c:\eduke32`
- copy `DUKE3D.GRP` and `DUKE.RTS` from your Duke Nukem 3D CD-ROM to that same folder
- install the included `Visual C++ Redistributable for Visual Studio 2015` if not already
- you are now ready to run `eduke32.exe` !

## Features

- XInput axes are being read from the official API instead of SDL
- user input is smoothed using cubic interpolation allowing for finer control, e.g. aiming
- pre-adjusted range for analog sticks, in-game GUI allows for further and finer adjustments
- startup GUI points to `All supported devices` by default
- no more assignment of default bindings for joystick, e.g. `eduke32.cfg` is as it should be
- a default `eduke32.cfg` file with an *FPS-like* layout has been included for convenience.

## Notes

If you didn't use the shipped `eduke32.cfg`, you will have to define joystick bindings as well as disabling *AutoRun* on first start. This is a little trade-off compared to the behavior of vanilla build, where invariably they were default-assigned each time the game was started.

You can navigate in the menus with the D-Pad, beware though, *accept* and *cancel* actions are hard-coded in the engine; their respective button on your game pad will depend of the layout you have decided of.

If you define *digital button* for a trigger, you will have to restart the game for the change to be effective.
