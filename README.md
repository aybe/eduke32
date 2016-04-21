# eduke32
revision R5700 + bugfixes for XInput and joystick-related annoyances

## Bugfixes/improvements

- startup GUI points to `All supported devices` by default
- XInput axes are being read from the official API instead of SDL
- user input is smoothed using cubic interpolation allowing for finer control, e.g. aiming
- pre-adjusted range for analog sticks, in-game GUI allows for further and finer adjustments
- no more assignment of default bindings for joystick, e.g. `eduke32.cfg` is as it should be

## Notes

- as a result there are no default bindings set for joystick, i.e. they must be defined by the user the first time
- yet, this is better than having the default ones invariably being re-assigned each time you restart the game when you have explicitly set them to `None`, right ?
- movement tends to slow down a bit when you pitch far up or far down, I guess this is due to the implementation (it does happen for mouse too)
- only the first 6 axes are being fed from XInput (two thumbsticks and two triggers)
- buttons still rely on SDL (not an issue at all)
- it should work with any non-Microsoft XInput device (untested)
- tested on Windows 10 with a Xbox One Controller

## Development

SVN 'bits' have been pushed to the repository, it should be relatively easy to keep this fork updated with the official version.

## Usage

- download in the **Release** tab, above
- pick your flavor : 32-bit or 64-bit
- *Visual C++ Redistributable for Visual Studio 2015* is included, install it if you don't have it
- a default `eduke32.cfg` with a *FPS-like* layout is included
 
## Usage notes

- initially *AutoRun* is enabled by the game, make sure you disable it to be able to walk and run using analog axes
- you can navigate in the menus with the *D-Pad* but due to my configuration layout, button *X* is *Accept* and *Right shoulder* is *Cancel*, i.e. game is hard-coded to *open/crouch* actions for menu navigation
- if you ever change *digital button* for a trigger it seems that one has to restart the game for it to be effective
- patch has been succesfully tested with BloodCM, consequently it should work with any game based on eduke32 :D


