
# CabalRealm EP33 - Ingens Proelium

CabalRealm EP33 is an extension library for the MMORPG Cabal Online, specifically for the Episode 33 (EP33) version. This project provides custom modifications, enhancements, and tools for the game client.

## Overview

CabalRealm EP33 is an injection DLL that enhances the Cabal Online gameplay experience through various client features and modifications. The project focuses on extending the functionality of the original game client, providing additional features and quality of life improvements.

## Detailed Components and Features

### 1. Base System

#### Main Configurations (Base.h)
- Development environment settings with `DEV_MODE` option
- XignCode anti-cheat system configuration with `XIGNCODE_VERSION_NA`
- Code protection system through VMProtect with different security levels
- Support for running multiple instances (up to 6 in developer mode)

#### Game Modifications (Game.cpp)
- Bypassing anti-debug checks (in development mode)
- Changing the XignCode loading method
- Bypassing CRC and file integrity checks
- Removing working directory restrictions
- Modifying interface values, including increasing the chat limit to 160 characters
- Customizing the game window title to "Cabal Realm EP33 - Ingens Proelium"

### 2. Management System Packet Manager (PacketManager)

#### Packet Manipulation (PacketManager.cpp/PacketManager.h)
- Interception of packets between client and server
- Support for different socket types: Login, World, Party and Chat
- Packet encryption and decryption system with XorKeyTable
- Implementation of custom hooks for packet processing

#### Protocol Definitions (ProtosDef.h/ProtoDefEx.h)
- Complete packet header structures
- Custom packet identifier definitions
- Support for extending game communication features

### 3. BM3 Macro and Synergy System

#### Macro for Battle Mode 3 (BM3Macro.cpp/BM3Macro.h)
- Custom GUI for synergy management
- Support for up to 4 synergy sequences with 3 options each
- Configuration of fatal attacks with up to 3 variations
- Synergy System saving and loading settings
- Minimized/maximized interface view
- Automatic activation of synergies based on saved settings

#### Synergy System (BM3Sinergy.cpp/BM3Sinergy.h)
- Interception and modification of game synergy processing
- Tracking of active player synergies
- System for loading synergy information via JSON
- Manipulation of synergy level and proxying
- Visual interface for displaying information about active synergies

### 4. EventAlert System

#### Event Alerts (EventAlert.cpp/EventAlert.h)
- Visual notifications for important in-game events
- Queue system for displaying multiple alerts sequentially
- Support for different types of events (item drops, item creation)
- Customizable appearance and duration of alerts
- Integration with the chat system for event announcements
- Detailed display of obtained items including properties and statistics

### 5. Discord Integration

#### Rich Presence (Discord.cpp/Discord.h)
- Integration with Discord Game SDK to display player status
- Automatically update status based on player activity
- Display information such as character class, nation, current map
- Indication of group/party and guild status
- Support for different game states (lobby, character creation, playing)
- Timestamps to show the duration of the game session

### 6. DirectX Management

#### Graphics Handling (DirectX.cpp/DirectX.h)
- Custom hooks for DirectX9
- Font management system with different sizes and styles
- Loading and handling of game textures
- Functions for drawing custom interface elements
- Support for sprites, texts and UI elements
- Management of render states and DirectX objects

#### Custom Interface System (Objects.cpp/Objects.h)
- Complete framework for creating interface elements
- Support for buttons, text boxes, images and interactive elements
- Callback system for mouse and keyboard events
- Dynamic positioning of elements based on the game resolution
- Visual effects such as hover, selection and animations
- Transparency management and rendering layers

### 7. Memory System and Security

#### Memory Manipulation
- Utilities for safe reading and writing of memory
- Hook system for game functions
- Bypass of memory protections
- Functions for changing specific values in the client

#### DLL Protection (DLLSec)
- Protection against injection or manipulation attempts
- DLL integrity checks
- Anti-tamper system for critical libraries and files

### 8. Additional Features

#### Custom Descriptions (cDescription)
- Improved system for displaying tooltips and item descriptions
- Support for custom text formatting
- Display of additional statistics on items and abilities

#### Window Customization (WindowObj)
- Framework for creating and managing custom windows
- System for positioning and saving settings
- Handling of interface events for windows and objects

#### Custom Slots (Slot)
- System for manipulating and displaying items in custom slots
- Integration with the game's inventory system
- Support for drag-and-drop and interaction with items

#### Procedure Handling (Proc)
- System for hooking game procedures
- Callback management for client events
- Redirection of game functions to custom implementations

#### Battle Mode Custom (GameCustom/BattleMode)
- Improvements to the game's Battle Mode systems
- Performance and balancing tweaks
- Additional features for the different battle modes

## How to Use

### Requirements
- Cabal Online Episode 33 client
- Windows 10 or higher (32/64-bit)
- DirectX9 installed

### Installation
1. Place the CabalEP33.dll DLL in the game folder
2. Use a compatible DLL injector or configure the game to load the library
3. Start the game client

### Settings
- Interface settings are saved automatically
- BM3 Macro settings are saved in `\Data\UserData\BM3Macro`
- Custom visual elements are stored in `\Data\UserData\`

### Hotkeys and Commands
- F11: Show/hide interface BM3 Macro
- F12: Enable/Disable BM3 Macro
- Ctrl+Click on macro elements to assign synergies



## Technologies Used

- **C++**: Main language of the project
- **DirectX9**: For manipulating graphic elements
- **VMProtect**: Code protection system against reverse engineering
- **Discord Game SDK**: For Rich Presence integration with Discord
- **JSON**: For storing and reading settings
- **Boost**: Used for manipulating properties and JSON trees

## Technical Notes

- The library modifies the game client's memory at runtime
- Some modifications change the original behavior of the anti-cheat
- The system uses DirectX and Windows APIs hooks to implement features
- Most of the code is protected by VMProtect to prevent reverse engineering
- Developer mode (DEV_MODE) allows console output for debugging

## Legal Notes

This project is specific to the Episode 33 version of Cabal Online and may not be compatible with other versions of the game. The library is intended to be injected into the game client and modifies several internal functions, including memory manipulation and server communication.

**Note**: This project is intended for educational and development purposes only. Use of this library may violate the Cabal Online game terms of service. Users are responsible for their use of this library.


Credits: NEOGAMES, vodikatm
