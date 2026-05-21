# Overlord

Overlord is an advanced graphical user interface (GUI) addon for Windower 4 (Final Fantasy XI), powered by ImGui. It allows players to dynamically scan, filter, load, and unload their Lua addons on the fly through an interactive in-game menu. 

With built-in command queuing, visual customization, and a global master switch, it streamlines addon management without cluttering the chat log or locking up the game client.

## Features

- **First-Time Path Configuration:** Prompts users instantly upon installation to approve or customize their target Windower addon folder path directly through the UI.
- **Dynamic Folder Scanning:** Automatically scans your custom configured directory to discover valid Lua addons.
- **Interactive UI (ImGui):** Styled with a clean dark theme and a dedicated top drag bar for effortless repositioning.
- **Command Queue System:** Prevents game crashes and network disconnects by spacing out sequential `load` and `unload` commands using a customizable delay timer.
- **Master Toggle Switch:** Mass-load or mass-unload all enabled addons simultaneously with a single click.
- **Real-Time Filtering:** Includes an instantaneous text search bar to quickly find specific addons in massive directories.
- **Persistent Configuration:** Saves your custom window sizes, font scales, colors, background textures, addon path, and states automatically to a configuration file (`config.json`).

## Installation

1. Download the script files.
2. Create a folder named `overlord` inside your Windower `addons` directory:
   ```text
   Windower4/addons/overlord/
   ```
3. Place the script file (named `overlord.lua`) into that folder.

## Usage

### First-Time Initialization
When loading the addon for the first time, an setup screen will appear. Confirm that the auto-detected path correctly points to your Windower `addons` folder, and click **Save & Initialize Directory** to unblock the main interface controls.

### In-Game Commands
Toggle the visibility of the graphical menu by typing either of the following commands into your game chat:
- `//overlord`
- `//ol`

### Interface Controls
- **Drag Bar:** Click and hold the top bar labeled `::: Overlord Menu (Drag Here) :::` to move the window around your screen.
- **⚙ Config Menu:** Expand this panel to adjust font scaling, background opacity, manual window dimensions, or text colors.
- **Background Images:** To use a custom background texture, place your image file inside the `overlord/` directory and type its exact filename into the image path field within the configuration panel.

## Configuration Defaults

The addon generates a standard configuration file upon its first execution with these properties:
- **Addon Directory:** User-selected absolute directory string.
- **Auto-Refresh:** Enabled (Automatically resorts the list, placing active addons at the top).
- **Default Size:** 350x500 pixels (Automatically overrides when Auto-Resize is active).
- **Queue Delay:** 500ms (Safely spaces out sequential script loading).

## Core Dependencies
- `imgui` (Windower ImGui library)
- `lfs` (LuaFileSystem)
- `config` (Windower configuration library)
