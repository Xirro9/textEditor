# C-Based Text Editor

A lightweight, terminal-based text editor written in C. This editor provides essential text editing functionalities while maintaining efficiency and responsiveness.

## Features
- **Text Buffer**: Stores the text being edited in memory, allowing efficient modifications.
- **Terminal Handling**: Uses raw mode to capture user input directly without interference from the operating system's line buffering.
- **Rendering System**: Dynamically updates the screen using ANSI escape codes to maintain smooth and flicker-free rendering.
- **Input Handling**: Captures keystrokes and processes them to support character insertion, deletion, navigation, and command shortcuts.
- **File I/O**: Implements functions to load text files into memory and save changes back to disk.
- **Status Bar and UI Elements**: Displays helpful information such as file name, cursor position, and unsaved changes.

## Terminal Control
The editor operates in a terminal environment and disables canonical mode and echoing, allowing it to handle every keystroke immediately. It utilizes:
- `tcgetattr()` and `tcsetattr()` for configuring terminal behavior.
- `read()` for low-level input handling.
- ANSI escape sequences for cursor movement, clearing lines, and text formatting.

## Editing Features
A minimal implementation includes:
- Character insertion and deletion.
- Line-based navigation with arrow keys.
- Scrolling support when the text exceeds the terminal size.
- Basic search functionality.

## Performance Considerations
- Efficient screen rendering using a single buffer instead of updating the screen line by line.
- Handling large files without excessive memory usage.
- Avoiding unnecessary redrawing to improve responsiveness.

## Extensibility
Though initially simple, the editor can be expanded with:
- Configurable key bindings.
- Multiple file support.
- Advanced text manipulation (cut, copy, paste).
- Undo/redo functionality.

## License
This project is open-source and available under the BSD 2-Clause License.
