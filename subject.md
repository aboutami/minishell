# 🐚 MiniShell: Custom Subject

**Project Name:** `minishell`  
**Language:** C

---

##  Objective

Build a simplified UNIX shell that replicates basic behaviors of `bash`.  
The goal is to gain hands-on experience with:
- Process creation and control
- File descriptors
- Input parsing
- Signal handling
- Environment variables
- Memory management under strict constraints

---

##  Mandatory Features

The shell must:

- ✅ Display a custom prompt and wait for user input
- ✅ Support command execution using:
  - Built-in commands (see below)
  - System commands using `PATH`, relative, or absolute paths
- ✅ Implement redirections:
  - `>`  → redirect output
  - `>>` → append output
  - `<`  → redirect input
  - `<<` → heredoc input until a delimiter is found
- ✅ Implement pipes (`|`) between commands
- ✅ Handle single (`'`) and double (`"`) quotes correctly
- ✅ Handle environment variables:
  - `$VAR` → expands to the value of the variable
  - `$?`   → expands to the exit code of the last command
- ✅ Handle special keys in interactive mode:
  - `Ctrl+C` → interrupts command and redisplays prompt
  - `Ctrl+D` → exits the shell
  - `Ctrl+\` → does nothing

###  Built-in Commands

Your shell must implement the following builtins:
- `echo` with `-n` option
- `cd` with relative or absolute paths
- `pwd`
- `export`
- `unset`
- `env`
- `exit`

---

##  Technical Constraints

- Your shell must be written in **C**
- Code must follow the **42 Norm** strictly
- **No memory leaks** are allowed (except those from `readline()`)
- Only **one global variable** is allowed (to track received signals)
- Only allowed system functions may be used (e.g., `read`, `write`, `fork`, `execve`, etc.)
- `libft` may be included as a static library under a `libft/` folder

---

##  Bonus Features (Optional)

> Bonus features are only evaluated if the mandatory part is fully functional.

- Support for logical operators: `&&`, `||` (with priority using parentheses)
- Wildcard expansion using `*` for file/directory matching in the current folder

---

##  Testing & Evaluation

You're encouraged to create test scripts and edge case scenarios.  
During the defense, tests may be used to demonstrate functionality.

Your project will be graded based on:
- Correctness
- Stability (no crashes or unexpected behavior)
- Code quality and structure
- Memory safety

---
