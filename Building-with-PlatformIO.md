## Installation

### Install Visual Studio Code

https://github.com/Microsoft/vscode

### Install the PlatformIO extension
Click on `View` > `Command Palette...`

![](./images/vscode_view_command_palette.png)

Find and click on `Extensions: Install Extensions`

![](./images/vscode_install_extensions.png)

Type `platformio` into the search box and click on `Install` under `PlatformIO IDE`.

![](./images/vscode_platformio_install.png)

## Usage

### 1. Open the OpenLRSng folder
Click on `File` > `Open Folder...`

![](./images/vscode_open_folder.png)

This brings up the `Open Folder` dialog. Select the folder that has the `platformio.ini` file in it.

![](./images/vscode_open_openlrsng.png)

### 2. Open the PlatformIO Project Activities

Click on the alien icon and select the drop-down menu for the board environment you are building to reveal all actions:

![](./images/vscode_build_verbose.png)

Firmware will be located at `.pioenvs/BOARD_TYPE_*/firmware.hex`