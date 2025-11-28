# Black Mesa Content Setup

Welcome to Project Ordinance! To ensure you experience our Black Mesa environments correctly, you must **mount** the files from the game *Black Mesa* (by Crowbar Collective) into your *Garry's Mod* installation.

Failing to complete this process will result in **Missing Textures** (bright pink and black checkerboards) and **Missing Models** (giant red "ERROR" signs) across the facility.

## Prerequisites

Before following this guide, you must ensure two conditions are met:

1. **Ownership:** You must own a legitimate copy of the game ***Black Mesa*** (available on Steam).

2. **Installation:** The game ***Black Mesa*** must be installed on your computer. You do not need to run the game, just have it fully installed.

## Step-by-Step Guide: Manual mount.cfg Editing

This tutorial teaches you how to manually edit the `mount.cfg` file to integrate Black Mesa content, bypassing the in-game mounting menu.

### Step 1: Locate the Configuration Folder

First, locate your main `GarrysMod/garrysmod` installation folder.

**Default Windows Path:** `C:\Program Files (x86)\Steam\SteamApps\common\GarrysMod\garrysmod`

If you are unsure of your path, skip to the **How to Find Your File Path** section below. Once located, open the `cfg` folder inside your `garrysmod` folder.

### Step 2: Edit mount.cfg

In the `cfg` folder, find the file named `mount.cfg`. Open this file using a plain text editor like Notepad, Visual Studio Code, or Sublime Text.

### Step 3: Locate Your Black Mesa Path

You need the exact file path to your Black Mesa installation's content folder. If you do not know how to find this, scroll down to the **How to Find Your File Path** section.

For the Steam version, the content is usually located in the `bms` folder. A default Windows example is:
`C:\Program Files (x86)\Steam\SteamApps\common\Black Mesa\bms`

### Step 4: Add the Mounting Line

Inside the `mountcfg` section of the `mount.cfg` file, add a new line referencing your installation path. Ensure the line is **not** commented out (no double slash `//` before it).

**Example of the correctly formatted line to add:**

```

"bms" "C:/Program Files (x86)/Steam/Steamapps/common/Black Mesa/bms"

```

**Example of the complete mount.cfg structure:**

```

//
// Use this file to mount additional paths to the filesystem
// DO NOT add a slash to the end of the filename
//

"mountcfg"
{
// "cstrike"    "C:/steamcmd/steamapps/common/Counter-Strike Source/cstrike"
// "tf"         "C:/mytf2server/tf"
    "bms"       "C:/Program Files (x86)/Steam/Steamapps/common/Black Mesa/bms"
}

```

Save and close the `mount.cfg` file.

## How to Find Your File Path

If your installation is not in the default location (e.g., on a separate hard drive or non-Windows system), use Steam to find the path:

1. **Open Steam:** Go to your Steam Library.

2. **Right-Click Black Mesa:** Right-click on the **Black Mesa** entry in your games list.

3. **Select Properties:** Click on **Properties**.

4. **Go to Installed Files:** Navigate to the **Installed Files** tab/section.

5. **Click Browse:** Click the **Browse** button. This will open the file browser directly to the Black Mesa game folder.

6. **Locate `bms`:** From this folder, navigate to the `bms` subfolder.

7. **Copy Path:** Copy the full path from the file browser's address bar. This is the path you need to paste into your `mount.cfg` file.

## Ending

Once you have correctly edited and saved `mount.cfg`, **restart Garry's Mod completely.** Upon reloading, Black Mesa content should be successfully mounted, and you can join the server without missing textures or errors.

If problems persist, please visit our **#support** channel on Discord.
