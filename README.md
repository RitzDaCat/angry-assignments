# Angry Assignments

A World of Warcraft addon for managing and sharing raid assignments. Originally developed by the guild Angry (US-Illidan), this addon provides raid leaders and officers with tools to create, edit, and display raid assignments to all raid members in real-time.

## Table of Contents

- [Features](#features)
- [Compatibility](#compatibility)
- [Installation](#installation)
- [Usage Guide](#usage-guide)
  - [For Raiders](#for-raiders)
  - [For Officers and Raid Leaders](#for-officers-and-raid-leaders)
- [Commands](#commands)
- [Text Formatting](#text-formatting)
- [Permissions](#permissions)
- [Contributing](#contributing)
- [License](#license)

## Features

- **Real-time Synchronization**: Assignment changes are instantly shared with all raid members
- **Permission System**: Restricts editing to guild officers and raid assistants
- **Customizable Display**: Configure font, size, colors, and positioning
- **Smart Highlighting**: Automatically highlight your name, role, or group assignments
- **Combat Awareness**: Option to auto-hide during combat
- **Icon Support**: Use raid markers, spell icons, and custom icons in assignments
- **Version Control**: Track addon versions across raid members
- **Backup System**: Save and restore previous versions of assignments

## Compatibility

Angry Assignments supports all current World of Warcraft game versions:

- **Retail**: The War Within (11.0.5)
- **Cataclysm Classic**: 4.4.0
- **Wrath Classic**: 3.4.3
- **Vanilla Classic**: 1.15.2

## Installation

1. Download the latest release from the [Releases](https://github.com/Ermad/angry-assignments/releases) page
2. Extract the `AngryAssignments` folder to your World of Warcraft addons directory:
   - Retail: `World of Warcraft/_retail_/Interface/AddOns/`
   - Classic: `World of Warcraft/_classic_/Interface/AddOns/`
3. Restart World of Warcraft or reload your UI

## Usage Guide

### For Raiders

#### Initial Setup

1. **Configure Keybinding**
   - Open the game's Key Bindings menu
   - Find "Angry Assignments" section
   - Bind "Toggle Display" to your preferred key

2. **Access Configuration**
   - Type `/aa` to open the configuration panel
   - Or navigate to Interface > AddOns > Angry Assignments

3. **Position the Display**
   - Click "Toggle Lock" or type `/aa lock`
   - Drag the red anchor bar to your desired position
   - Adjust the width by dragging the edges
   - Use the arrow button to set text direction (up/down)
   - Lock the display when positioned

#### Configuration Options

| Setting | Description |
|---------|-------------|
| **Highlight** | Enter words to highlight (your name, nickname, "Group" for group assignments) |
| **Hide on Combat** | Automatically hide assignments when entering combat |
| **Font Face** | Choose from available fonts |
| **Font Size** | Adjust text size for readability |
| **Font Outline** | Add outline for better visibility |
| **Colors** | Customize text and highlight colors |

### For Officers and Raid Leaders

#### Accessing the Edit Window

1. Set a keybinding for "Toggle Window" (recommended)
2. Or use `/aa window` command
3. Scale the window using the configuration panel or `/aa scale <value>`

#### Managing Assignments

**Page Management**
- **Add**: Create new assignment pages
- **Rename**: Change page names for organization
- **Delete**: Remove pages locally (others retain their copies)

**Editing Controls**
- **Accept**: Save changes and broadcast to all guild members online
- **Revert**: Cancel current edits and restore previous version
- **Restore**: Recover your last personally edited version
- **Send and Display**: Broadcast page and display it to the raid
- **Clear Displayed**: Remove current display from all raid members

#### Conflict Resolution

When multiple officers edit simultaneously:
- You'll receive a notification if someone else saves changes
- Options:
  - Continue editing and overwrite their changes with "Accept"
  - Abandon your edits with "Revert" to see their version
  - Copy your changes (Ctrl+C), revert, then paste (Ctrl+V) to merge

## Commands

| Command | Description |
|---------|-------------|
| `/aa` | Open configuration panel |
| `/aa help` | List all available commands |
| `/aa toggle` | Toggle assignment display |
| `/aa lock` | Lock/unlock display position |
| `/aa window` | Toggle edit window |
| `/aa scale <value>` | Scale the edit window |
| `/aa version` | Check addon versions in raid |
| `/aa backup` | Save all current pages for restore |
| `/aa deleteall` | Delete all stored pages locally |

## Text Formatting

### Raid Markers
- `{star}`, `{rt1}` - Star marker
- `{circle}`, `{rt2}` - Circle marker  
- `{diamond}`, `{rt3}` - Diamond marker
- `{triangle}`, `{rt4}` - Triangle marker
- `{moon}`, `{rt5}` - Moon marker
- `{square}`, `{rt6}` - Square marker
- `{cross}`, `{x}`, `{rt7}` - Cross marker
- `{skull}`, `{rt8}` - Skull marker

### Icons
- `{hs}`, `{healthstone}` - Healthstone icon
- `{bl}`, `{bloodlust}` - Bloodlust icon
- `{hero}`, `{heroism}` - Heroism icon
- `{icon IconName}` - Custom icon (e.g., `{icon spell_holy_sealofprotection}`)
- `{spell 12345}` - Spell icon by ID

### Class Colors
- `|cwarrior`, `|cpaladin`, `|chunter`, `|crogue`
- `|cpriest`, `|cshaman`, `|cmage`, `|cwarlock`
- `|cmonk`, `|cdruid`, `|cdemonhunter`, `|cdeathknight`, `|cevoker`

### Text Colors
- `|cblue`, `|cgreen`, `|cred`, `|cyellow`
- `|corange`, `|cpink`, `|cpurple`

## Permissions

Assignment editing is restricted to:
- Guild officers (detected by officer chat permissions)
- Raid assistants (when raid is led by a guild officer)

Each player's addon validates permissions and rejects unauthorized changes.

## Contributing

Contributions are welcome! Please:

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to your branch
5. Create a Pull Request

## License

This addon is provided as-is for use by the World of Warcraft community. See the repository for detailed license information.