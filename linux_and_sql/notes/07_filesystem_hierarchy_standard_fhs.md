# Filesystem Hierarchy Standard (FHS)

Previously, you learned that the **Filesystem Hierarchy Standard (FHS)** is the component of Linux that organizes data. The FHS is important because it defines how directories, directory contents, and other storage are organized in the operating system.

Under the FHS, a file’s location can be described by a **file path**. A file path is the location of a file or directory. In a file path, levels of the hierarchy are separated by a forward slash (`/`).

---

## Root directory

The **root directory** is the highest-level directory in Linux and is represented by a forward slash (`/`). All subdirectories branch off the root directory, and subdirectories can continue branching to as many levels as needed.

---

## Standard FHS directories

Directly below the root directory are standard FHS directories. Examples include:

- **`/home`**: Each user in the system gets their own home directory.
- **`/bin`**: “Binary” directory that contains binary files and other executables. **Executables** are files that contain a series of commands a computer follows to run programs and perform functions.
- **`/etc`**: Stores system configuration files.
- **`/tmp`**: Stores many temporary files. `/tmp` is commonly used by attackers because anyone on the system can modify data in these files.
- **`/mnt`**: “Mount” directory that stores media, such as USB drives and hard drives.

**Pro Tip:** Use `man hier` to learn more about standard FHS directories.

---

## User-specific subdirectories

Under `/home` are subdirectories for specific users (e.g., `analyst`, `analyst2`). Each user can have personal subdirectories such as `projects`, `logs`, or `reports`.

**Note:** When the path leads to a subdirectory below the user’s home directory, the home directory can be represented with a tilde (`~`). For example, `/home/analyst/logs` can be represented as `~/logs`.

---

## Absolute vs relative file paths

You can navigate using either **absolute** or **relative** paths:

- **Absolute file path**: The full path starting from the root (`/`). Example: `/home/analyst/projects`.
- **Relative file path**: A path starting from the current directory.

**Note:** Relative paths can use:

- `.` to represent the current directory
- `..` to represent the parent directory

Example: `../projects`.

---

## Key commands for navigating the file system

### `pwd`

`pwd` prints the working directory (the directory you are currently in). The output is the **absolute path** to the current directory.

Example: if the user is `analyst` and you are in the home directory, `pwd` returns `/home/analyst`.

**Pro Tip:** Use `whoami` to display the username of the current user (e.g., `analyst`).

### `ls`

`ls` displays the names of files and directories in the current working directory.

You can also list the contents of another directory by specifying its absolute or relative path, e.g.:

- `ls /home/analyst/projects`
- `ls projects`

### `cd`

`cd` changes the current directory.

- To move into a subdirectory of the current directory: `cd projects`
- To move to a specific directory by absolute path: `cd /home/analyst/logs`

**Pro Tip:** Use `cd ..` to go up one level (e.g., from `/home/analyst/projects` to `/home/analyst`).

---

## Common commands for reading file content

### `cat`

`cat` displays the full content of a file. Example: `cat updates.txt`.

### `head`

`head` displays the beginning of a file (default: 10 lines). Example: `head updates.txt`.

**Pro Tip:** Change the number of lines with `-n`, e.g. `head -n 5 updates.txt`.

### `tail`

`tail` displays the end of a file (default: 10 lines). Example: `tail updates.txt`.

**Pro Tip:** Use `tail` to read the most recent information in a log file.

### `less`

`less` displays file contents one page at a time (e.g., `less updates.txt`) so you can move forward and backward.

Keyboard controls in `less`:

- **Space bar**: forward one page
- **`b`**: back one page
- **Down arrow**: forward one line
- **Up arrow**: back one line
- **`q`**: quit

---

## Key takeaways

Security analysts should be able to navigate Linux and the FHS file system.

- Key navigation commands: `pwd`, `ls`, `cd`
- Key file-reading commands: `cat`, `head`, `tail`, `less`

