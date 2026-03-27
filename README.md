# Kavita Reader LaunchBox Plugin

Integrates LaunchBox with Kavita so you can match games with strategy guides and open them directly from LaunchBox with cover art, metadata, and reader launch support.
<img width="1240" height="817" alt="2026-03-27 15_09_22-LaunchBox" src="https://github.com/user-attachments/assets/426f6858-2dbb-4189-8c71-844a207a782f" />

---

## Overview

Kavita Reader LaunchBox Plugin is a LaunchBox plugin designed to connect your game library with strategy guides stored in Kavita.

It allows you to:

- Link a LaunchBox game to a strategy guide in Kavita
- Search for and choose from multiple possible matches
- Launch the linked guide directly from LaunchBox
- Open the guide in either windowed or fullscreen reader mode
- Sync the linked guide as an Additional App entry
- Display cover art and metadata during guide selection
- Use publisher badge detection for supported publishers
- Enable optional debug logging when troubleshooting

This project is currently focused on **strategy guide integration**.

---

## Features

- **Kavita integration**
  - Connects to a Kavita server using your server URL and API key

- **Guide linking**
  - Search Kavita for potential strategy guide matches based on the selected LaunchBox game
  - Choose from one or more returned matches
  - Save the linked guide to the game

- **Guide relinking**
  - Re-run guide matching and replace an existing linked guide

- **Clear linked guide**
  - Remove the linked guide from the game
  - Remove the corresponding Additional App entry if one exists

- **Additional App sync**
  - Linked guides can be represented as a LaunchBox Additional App entry for easier visibility and management

- **Reader launch support**
  - Launch the linked guide in:
    - Windowed mode
    - Fullscreen mode

- **Cover and metadata display**
  - Show guide cover art when available
  - Display metadata such as title, publisher, and other helpful information during selection

- **Publisher badge logic**
  - Supports publisher badge detection for:
    - Prima
    - Nintendo
    - Brady / BradyGames / Brady Games

- **Configurable debug logging**
  - Debug logging can be enabled or disabled from the plugin tools menu
  - Logging should only be written when debug logging is enabled

---

## Current Scope

This plugin is currently intended for:

- **Strategy guides stored in Kavita**

It is **not yet intended as a general-purpose reader integration** for all books, comics, or manuals, even though some of those items may occasionally appear in search results depending on metadata and search behavior.

---

## Requirements

Before installing this plugin, make sure you have:

- **LaunchBox**
- **Kavita**
- A valid **Kavita API key**
- A Kavita library that contains your strategy guides
- Windows environment capable of running the plugin and WebView-based reader flow as configured by the project

---

## Installation

1. Build the plugin project in Visual Studio.
2. Copy the built plugin output into your LaunchBox `Plugins` folder.
3. Make sure any required dependencies are copied alongside the plugin DLL.
4. Ensure the plugin assets are present, including icon assets under:

   ```text
   Assets\Icons
