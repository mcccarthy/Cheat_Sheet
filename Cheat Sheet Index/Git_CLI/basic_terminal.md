# Command Line Cheat Sheet

## Basic Terminal Commands

| Command                  | Description                                         | Example                         |
|--------------------------|-----------------------------------------------------|---------------------------------|
| `pwd`                    | Print the current working directory.                | `pwd`                           |
| `ls`                     | List directory contents.                            | `ls -l` (long format)          |
| `cd <directory>`         | Change the current directory.                       | `cd Documents`                 |
| `cd ..`                  | Move up one directory level.                        | `cd ..`                        |
| `mkdir <directory>`      | Create a new directory.                            | `mkdir new-folder`             |
| `rmdir <directory>`      | Remove an empty directory.                          | `rmdir old-folder`             |
| `rm <file>`              | Remove a file.                                    | `rm file.txt`                  |
| `cp <source> <dest>`     | Copy files or directories.                         | `cp file.txt copy.txt`         |
| `mv <source> <dest>`     | Move or rename files or directories.               | `mv oldname.txt newname.txt`   |
| `touch <file>`           | Create a new empty file or update the timestamp of an existing file. | `touch newfile.txt`  |

* * *

## Useful Commands for Developers

| Command                            | Description                                         | Example                           |
|------------------------------------|-----------------------------------------------------|-----------------------------------|
| `grep <pattern> <file>`            | Search for a specific pattern in a file.           | `grep "hello" file.txt`          |
| `find <directory> -name <name>`    | Search for files in a directory hierarchy.         | `find . -name "*.txt"`           |
| `tar -cvf <archive.tar> <files>`   | Create a tar archive.                              | `tar -cvf archive.tar folder/`   |
| `tar -xvf <archive.tar>`           | Extract files from a tar archive.                 | `tar -xvf archive.tar`            |
| `cat <file>`                       | Concatenate and display the content of a file.     | `cat file.txt`                    |
| `head <file>`                     | Display the first 10 lines of a file.              | `head file.txt`                   |
| `tail <file>`                     | Display the last 10 lines of a file.               | `tail file.txt`                   |
| `chmod <permissions> <file>`      | Change the permissions of a file.                  | `chmod 755 script.sh`            |
| `chown <user>:<group> <file>`     | Change the owner and group of a file.              | `chown user:group file.txt`      |

* * *

## Package Management Commands

### npm Commands

| Command                     | Description                                         | Example                           |
|-----------------------------|-----------------------------------------------------|-----------------------------------|
| `npm init`                  | Initialize a new Node.js project.                  | `npm init -y` (to accept defaults) |
| `npm install <package>`     | Install a package and its dependencies.            | `npm install express`             |
| `npm uninstall <package>`   | Remove a package from the project.                 | `npm uninstall express`           |
| `npm update`                | Update all packages to the latest version.         | `npm update`                      |
| `npm list`                  | List installed packages.                            | `npm list`                        |
| `npm run <script>`          | Run a defined script from package.json.            | `npm run start`                   |

### Yarn Commands

| Command                     | Description                                         | Example                           |
|-----------------------------|-----------------------------------------------------|-----------------------------------|
| `yarn init`                 | Initialize a new Yarn project.                     | `yarn init -y` (to accept defaults) |
| `yarn add <package>`        | Add a package to the project.                      | `yarn add express`                |
| `yarn remove <package>`     | Remove a package from the project.                 | `yarn remove express`             |
| `yarn upgrade`              | Upgrade all packages to the latest version.       | `yarn upgrade`                    |
| `yarn list`                | List installed packages.                            | `yarn list`                      |
| `yarn run <script>`        | Run a defined script from package.json.            | `yarn run start`                 |

---

This cheat sheet provides a quick reference for essential command line operations, making it easier to navigate directories, manipulate files, and manage packages for development. Feel free to expand or modify it as needed!


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