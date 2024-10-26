# 🖥️ Interactive C Shell Documentation 📜

## Table of Contents

- [Overview](#overview)
- [Core Functionality](#core-functionality)
  - [System Commands](#system-commands)
  - [Process Management](#process-management)
  - [File Operations](#file-operations)
  - [Custom Commands](#custom-commands)
- [Advanced Features](#advanced-features)
  - [I/O Redirection](#io-redirection)
  - [Piping and Redirection](#piping-and-redirection)
  - [Networking](#networking)
- [Error Handling & Signals](#error-handling--signals)
- [Getting Started](#getting-started)

## Overview

Welcome to the **Interactive C Shell**! This shell offers a customized command-line experience with advanced functionality and enhanced command control, allowing you to manage files, processes, and networks effortlessly. Its features include custom-built commands, robust error handling, process signals, and network utilities, all within a responsive and user-friendly interface.

---

## Core Functionality

### System Commands 💻

The shell supports standard system commands as well as custom functionality:

- **Foreground and Background Execution:** Commands can be run in the background using `&` or sequentially using `;`.
- **Process Time Display:** For commands that exceed 2 seconds of runtime, the shell outputs the execution time.
- **Error Feedback:** Clear messages for invalid commands or improper syntax ensure smooth usage.

### Process Management 📊

- **`proclore` Command**: View real-time process information, including:
  - Process ID (PID), status, process group, virtual memory, and executable path.

- **`activities` Command**: Lists all active processes initiated by the shell, showing each:
  - Command name, PID, and state (Running or Stopped).

- **`fg` and `bg` Commands**:
  - `fg <pid>` brings a background process to the foreground.
  - `bg <pid>` resumes a stopped process in the background.

### File Operations 📁

- **`warp` Command**: Efficient directory navigation with support for `.`, `..`, `~`, and `-`.
- **`peek` Command**: File listing utility with options:
  - `-l` for detailed listing, `-a` to include hidden files.

- **`seek` Command**: File/directory search functionality with flexible options:
  - `-d` restricts search to directories, `-f` restricts to files, and `-e` executes or displays the first match found.

### Custom Commands 🔧

- **`pastevents` Command**: An enhanced history tool:
  - Tracks the 15 most recent commands and persists across sessions.
  - `pastevents execute <index>` to run a previous command.
  - `pastevents purge` clears the command history.

- **`neonate` Command**: Monitors and prints the PID of the most recent process every `[time_arg]` seconds until terminated.

---

## Advanced Features

### I/O Redirection 🔀

Supports input and output redirection with:
- `>` to overwrite, `>>` to append, and `<` to read from files.
- Displays "No such input file found!" if an input file is missing.

### Piping and Redirection ⛓️

Combines standard piping with redirection:
- Commands are piped in left-to-right order.
- For improper use, the shell returns "Invalid use of pipe."

### Networking 🌐

- **`iMan` Command**: Fetches online manual pages for any specified command:
  - `iMan <command_name>` displays documentation, combining functionality with network-based help retrieval.

---

## Error Handling & Signals 🚦

- **Signal Handling**:
  - `ping <pid> <signal_number>` sends a specified signal to a process.
  - Handles keyboard interrupts:
    - **Ctrl-C** sends SIGINT to the foreground process.
    - **Ctrl-D** exits the shell.
    - **Ctrl-Z** stops the foreground process.

- **Error Messaging**: The shell provides detailed feedback for command issues, flagging any unrecognized syntax or file access errors.

---

## Getting Started 🚀

To compile and start the Interactive C Shell:

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/Interactive-C-Shell.git

2. Navigate to the project directory:
  ```cd Interactive-C-Shell```

3. Compile the source code:
  ```make```

4. Start the shell:
```./shell```
