# Creating and modifying directories and files

Managing the Linux file system is an important skill for security analysts. This note covers common commands for creating, removing, moving, copying, and editing files and directories.

---

## Creating and modifying directories

### `mkdir`

`mkdir` creates a new directory. You can use an **absolute** path (starts at `/`) or a **relative** path (starts at your current directory).

Examples:

- `mkdir /home/analyst/logs/network` creates a directory named `network` inside `/home/analyst/logs`.
- If you are already in `/home/analyst/logs`, `mkdir network` creates the same directory.

**Pro Tip:** Use `ls` to confirm the directory was created.

### `rmdir`

`rmdir` removes (deletes) a directory **only if it is empty**.

Example:

- `rmdir /home/analyst/logs/network` removes the empty `network` directory.

**Note:** `rmdir` cannot delete a directory that contains files or subdirectories (e.g., `rmdir /home/analyst` would return an error).

---

## Creating and modifying files

### `touch` and `rm`

- `touch` creates a new empty file (no content).
- `rm` removes (deletes) a file. Use it carefully because recovery is difficult.

Example:

- If your current directory is `/home/analyst/reports`, `touch permissions.txt` creates `permissions.txt` there.
- `rm permissions.txt` deletes it.

**Pro Tip:** Use `ls` to verify the file was created or removed.

### `mv` and `cp`

- `mv` moves a file or directory to a new location.
- `cp` copies a file or directory to a new location.

For both commands:

- first argument = the file/directory to move or copy
- second argument = the destination location

Examples:

- `mv permissions.txt /home/analyst/logs` moves `permissions.txt` into `/home/analyst/logs` (it will no longer be in the original location).
- `cp permissions.txt /home/analyst/logs` copies `permissions.txt` into `/home/analyst/logs` while keeping the original in place.

**Note:** `mv` can also rename files by using a new name as the second argument:

- `mv permissions.txt perm.txt` renames `permissions.txt` to `perm.txt`.

---

## `nano` text editor

`nano` is a command-line text editor available by default in many Linux distributions. It’s commonly used in the security profession and is often considered beginner-friendly.

Open an existing file:

- From the directory containing the file: `nano permissions.txt`
- Or using the absolute file path.

Create a new file (and open it for editing):

- `nano authorized_users.txt`

Because `nano` does not auto-save:

- **Save**: `Ctrl + O` (then confirm the filename)
- **Exit**: `Ctrl + X`

**Note:** `vim` and `emacs` are also popular command-line editors.

---

## Standard output redirection (`>` and `>>`)

Besides piping (`|`), Linux also supports redirecting **standard output** to a file using:

- `>` overwrite (replaces the file contents)
- `>>` append (adds to the end of the file)

When used with `echo`, these operators send output to a file instead of the screen.

Examples (from within the directory containing `permissions.txt`):

- `echo "last updated date" >> permissions.txt` appends the text to the end of the file.
- `echo "time" > permissions.txt` overwrites the entire file contents with `time`.

**Note:** Both `>` and `>>` will create the file if it doesn’t already exist.

---

## Key takeaways

- Useful file-system commands: `mkdir`, `rmdir`, `touch`, `rm`, `mv`, `cp`
- Common ways to write to files: `nano`, output redirection with `>` and `>>`

