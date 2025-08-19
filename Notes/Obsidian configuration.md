This vault comes pre-configured with a curated selection of plugins and settings optimized for knowledge management and writing.
## Community Plugins

### Workflow Enhancement
- **Obsidian Git** - Automatic version control and backup (auto-commits every 5 minutes, pulls on startup)
- **Homepage** - Set a default starting page (configured to Home.md)
- **Templater** - Advanced template system with dynamic content - `Alt+T`, `Alt+E`
- **Recent Files** - Quick access to recently opened files
### Navigation & Search  
- **Omnisearch** - Enhanced search with better indexing
- **Cycle Through Panes** - Keyboard navigation between open notes navigating by most recently used - `Ctrl+Tab` to cycle
- **Better Command Palette** - Improved command interface - `Ctrl+Shift+P` or `F1`
### Content Creation
- **Table Editor** - Enhanced markdown table editing - `Tab` to navigate cells
- **Excalidraw** - Drawing and diagramming integration
- **URL Into Selection** - Convert selected text to links quickly by pasting links over existing text
- **Heading Shifter** - Adjust heading levels efficiently - `Ctrl+<number>`
### Data & Queries
- **Dataview** - Query and display note data dynamically
### Productivity
- **Shortcuts Extender** - Additional customizable hotkeys, but seems unused.
## Keyboard Shortcuts Summary
| Shortcut | Function | Plugin/Core |
|----------|----------|-------------|
| `Ctrl+Tab` | Cycle through panes (MRU order) | Cycle Through Panes |
| `Ctrl+Shift+P` | Better command palette | Better Command Palette |
| `F1` | Better command palette (alt) | Better Command Palette |
| `Ctrl+P` | Standard command palette | Core |
| `Alt+T` | Templater menu | Templater |
| `Alt+E` | Templater insert | Templater |
| `Ctrl+Shift+↑` | Move line up | Core |
| `Ctrl+Shift+↓` | Move line down | Core |
| `F3` | Move/rename file | Core |
| `Tab` | Navigate table cells | Table Editor |
| `Ctrl+<number>` | Adjust heading level | Heading Shifter |

## Custom Settings (Non-Default)
### File Management
- **New files location**: `Seedbox/` folder (instead of root)
- **Attachments folder**: `Attachments/` (instead of default)
- **Always update links**: Enabled for better link maintenance
- **Prompt before delete**: Disabled for faster workflow
### Interface
- **Stacked tabs**: Must be enabled manually - Click the down arrow in the tab bar → "Stack tabs" (not shared in vault settings)
- **Backlinks in document**: Enabled at bottom of pages - Essential for evergreen notes as it shows which notes reference the current one, creating discoverable knowledge networks
### Version Control
- **Auto-sync enabled**: The vault automatically commits changes every 5 minutes with message "vault backup: {{date}}"
- **Pull on startup**: Automatically pulls remote changes when Obsidian opens



