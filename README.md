# Virtual Controller Release



## About

VirtualController is a simple tool written in C#/WPF to help people with a physical disability play games using their cursor only (by either a physical mouse or other tools like an eye-tracking device).

What it does, is to create a transparent, resizable window containing the following controls (Buttons)

- 8 Action Buttons at the windows' borders
- 8 Movement Buttons around the center of the window

**IMPORTANT** / **WARNING**:

There might be games who consider software triggered key presses as cheating. I never had any issues yet, but I will can not take any responsibility in case of any issues.

Further, VirtualController is still in development. If you encounter any issues, please let me know

## Installation (Windows)

1. Download and extract VirtualController.zip
2. Launch by double clicking VirtualController.exe

## Controls/Buttons

### Overview

Both the Action and Movement Buttons can be modified in terms of 

- button color
- text color
- key mapping
- trigger delay time
- position (action button only)
- visibility

The size is currently not manually adjustable, but will adapt to the windows' size automatically.

By default, all buttons will fire after waiting for the **trigger delay time**. In click mode, they will fire immediately at the click.

![](https://github.com/oldShatteredHands7/virtcontroller_build/blob/main/img/button_overview.PNG?raw=true)

### Movement buttons

There are two types of movement buttons.

**Constant movement buttons** will hold the mapped key until the cursor leaves them (in click mode, until the mouse button is released). This will result in a smooth, constant movement in games.

**Step movement buttons** will press & release the mapped key, wait for a specified interval and then press & release the key again until the cursor leaves them. This will result in moving step by step and is useful whenever accurate movement is required (e.g. move by one unit in top-view RPG games like the old Pokemon, Zelda, ... titles)

In click mode, they just press & release the mapped key per click.

#### Adjustable properties

- button color (via .config)
- key mapping (via .config or GUI)
- trigger delay (via .config)

### Action buttons

By default (hover mode), action buttons will press & release the mapped key, wait for a specified interval and then press & release the key again until the cursor leaves them.

In click mode, they just press & release the mapped key per click.

#### Adjustable properties

- button color (via .config)
- text color (via .config)
- key mapping (via .config or GUI)
- trigger delay time (via .config)
- horizontal position (via GUI)
- visibility (via .config or GUI)

### Window control buttons

- Close application
- Open settings
- Maximize window
- Move window (by dragging)

### Settings

Settings can be defined the via **UI** or **.config file**. Not all settings are available in the GUI yet.

**Changing settings in the GUI will automatically update the .config file. Make sure to close the .config file before launching VirtualController.**

#### Settings GUI

Check https://github.com/michaelnoonan/inputsimulator/blob/master/WindowsInput/Native/VirtualKeyCode.cs to find out the correct value for the key you want to assign (e.g. 7 --> VK_7, W --> VK_W, etc...) **as action button mapping**

![](https://github.com/oldShatteredHands7/virtcontroller_build/blob/main/img/settings_gui.png?raw=true)

#### Settings .config

Open VirtualController.exe.config in the text editor of your choice.

![](https://github.com/oldShatteredHands7/virtcontroller_build/blob/main/img/settings_file_expl.PNG?raw=true)



**VirtualKey** values define the key binding for the movement/action button. 

Check https://github.com/michaelnoonan/inputsimulator/blob/master/WindowsInput/Native/VirtualKeyCode.cs to find out the correct value for the key you want to assign (e.g. 7 --> VK_7, W --> VK_W, etc...) 

For a list of available **Color** names, check https://docs.microsoft.com/en-us/dotnet/api/system.windows.media.colors?view=net-5.0

All **delay** values are defined in ms.

![](https://github.com/oldShatteredHands7/virtcontroller_build/blob/main/img/settings_file.PNG?raw=true)

### Attributions

**Window control icons**

Icon by [Raj Dev](https://freeicons.io/profile/714) on [freeicons.io](https://freeicons.io)

**Application icon**

<div>Icons made by <a href="https://www.freepik.com" title="Freepik">Freepik</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div>