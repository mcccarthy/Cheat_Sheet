# Zsh and Bash Cheat Sheet

## Basic Commands

| Command                  | Description                                         | Example                           |
|--------------------------|-----------------------------------------------------|-----------------------------------|
| `ls`                     | List directory contents.                            | `ls -l`                           |
| `cd <directory>`         | Change the current directory.                       | `cd Documents`                    |
| `pwd`                    | Print the current working directory.                | `pwd`                             |
| `mkdir <directory>`      | Create a new directory.                            | `mkdir new-folder`                |
| `rm <file>`              | Remove a file.                                    | `rm file.txt`                     |
| `cp <source> <dest>`     | Copy files or directories.                         | `cp file.txt copy.txt`            |
| `mv <source> <dest>`     | Move or rename files or directories.               | `mv oldname.txt newname.txt`      |
| `echo <text>`            | Print text to the terminal.                        | `echo "Hello, World!"`           |
| `cat <file>`             | Display the content of a file.                     | `cat file.txt`                    |
| `touch <file>`           | Create a new empty file or update an existing file's timestamp. | `touch newfile.txt` |

* * *

## Shell Configuration

### Zsh Configuration

- **.zshrc**: The main configuration file for Zsh.
- Common settings:
    ```bash
    # Set the default editor
    export EDITOR='vim'

    # Enable command auto-completion
    autocompletion

    # Set the theme (using a popular theme)
    ZSH_THEME="agnoster"

    # Enable plugins
    plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
    ```

### Bash Configuration

- **.bashrc**: The main configuration file for Bash (executed for interactive shells).
- Common settings:
    ```bash
    # Set the default editor
    export EDITOR='vim'

    # Enable command auto-completion
    shopt -s progcomp

    # Custom prompt
    PS1='\u@\h:\w\$ '
    ```

* * *

## Command Line Shortcuts

### Zsh and Bash Shortcuts

| Shortcut            | Description                                         |
|---------------------|-----------------------------------------------------|
| `Ctrl + C`          | Cancel the current command.                         |
| `Ctrl + Z`          | Suspend the current command.                        |
| `Ctrl + D`          | Logout of the current shell.                        |
| `Ctrl + A`          | Move the cursor to the beginning of the line.      |
| `Ctrl + E`          | Move the cursor to the end of the line.            |
| `Ctrl + U`          | Delete from the cursor to the beginning of the line. |
| `Ctrl + K`          | Delete from the cursor to the end of the line.     |
| `Ctrl + R`          | Search the command history.                         |
| `!!`                 | Execute the last command again.                     |
| `!<number>`         | Execute a command from history by its number.      |

* * *

## Variables and Environment

### Setting Variables

| Command                  | Description                                         | Example                           |
|--------------------------|-----------------------------------------------------|-----------------------------------|
| `export VAR=value`       | Set an environment variable.                        | `export PATH=$PATH:/new/path`    |
| `echo $VAR`              | Print the value of a variable.                     | `echo $PATH`                      |
| `unset VAR`              | Remove an environment variable.                    | `unset VAR`                       |

* * *

## Common Features

### Zsh Features

- **Globbing**: Use `**` for recursive globbing.
    ```bash
    ls **/*.txt  # Lists all .txt files in the current directory and subdirectories.
    ```

- **History Management**: Easy access to command history with `history` command.

- **Spell Correction**: Automatically corrects minor spelling mistakes in commands.
    ```bash
    git comit  # Will suggest `git commit` instead.
    ```

### Bash Features

- **Brace Expansion**: Create multiple strings or commands.
    ```bash
    echo file{1..5}.txt  # Outputs: file1.txt file2.txt file3.txt file4.txt file5.txt
    ```

- **Command Substitution**: Use the output of a command as an argument.
    ```bash
    echo "Today is $(date)"  # Outputs: Today is [current date]
    ```

* * *

## Useful Commands

### Zsh Commands

| Command                     | Description                                         | Example                           |
|-----------------------------|-----------------------------------------------------|-----------------------------------|
| `alias <name>=<command>`    | Create an alias for a command.                     | `alias ll='ls -l'`               |
| `unalias <name>`            | Remove an alias.                                   | `unalias ll`                      |
| `history`                   | Show command history.                              | `history`                         |
| `!!`                        | Repeat the last command.                            | `!!`                              |

### Bash Commands

| Command                     | Description                                         | Example                           |
|-----------------------------|-----------------------------------------------------|-----------------------------------|
| `alias <name>=<command>`    | Create an alias for a command.                     | `alias ll='ls -l'`               |
| `unalias <name>`            | Remove an alias.                                   | `unalias ll`                      |
| `history`                   | Show command history.                              | `history`                         |

---

This cheat sheet provides a quick reference for essential Zsh and Bash commands, configuration options, command line shortcuts, and useful features for both shells. You can customize it further based on your specific needs or preferences!


Key Command
Ctrl/Cmd + B Toggle bold
Ctrl/Cmd + I Toggle italic
Alt+S (on Windows) Toggle strikethrough1
Ctrl + Shift + ] Toggle heading (uplevel)
Ctrl + Shift + [ Toggle heading (downlevel)
Ctrl/Cmd + M Toggle math environment
Alt + C Check/Uncheck task list item
Ctrl/Cmd + Shift + V Toggle preview
Ctrl/Cmd + K V Toggle preview to side