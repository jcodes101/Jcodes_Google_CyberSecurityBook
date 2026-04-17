# Reading and changing permissions

In Linux, permissions are represented with a **10-character string** (for example, `drwxrwxrwx`). Permissions determine what actions can be performed on a file or directory.

---

## Permission types

Permissions include:

- **read**
  - files: ability to read file contents
  - directories: ability to read all contents in the directory (files and subdirectories)
- **write**
  - files: ability to modify file contents
  - directories: ability to create new files in the directory
- **execute**
  - files: ability to execute the file (if it’s a program)
  - directories: ability to enter the directory and access its files

Permissions are granted to these owner types:

- **user**: the owner of the file
- **group**: a larger group the owner is part of
- **other**: all other users on the system

---

## 10-character permission string

Each character position has meaning:

- **1st character**: file type
  - `d` = directory
  - `-` = regular file
- **2nd–4th**: user permissions (`r`, `w`, `x`)
- **5th–7th**: group permissions (`r`, `w`, `x`)
- **8th–10th**: other permissions (`r`, `w`, `x`)

If a permission is missing, a hyphen (`-`) is shown instead (for example, `r--` means read only).

---

## Exploring existing permissions with `ls`

`ls` lists directory contents. Adding options can show more detail, including permissions:

- `ls -a`: display **hidden** files (names starting with `.`)
- `ls -l`: display **permissions** and other details (owner, group, size, last modification time)
- `ls -la`: display permissions + hidden files (combines `-l` and `-a`)

---

## Changing permissions with `chmod`

The **principle of least privilege** means granting only the minimum access needed to complete a task. Excess permissions increase security risk.

`chmod` changes permissions on files and directories. It takes two arguments:

- how to change permissions
- the file or directory to change

Examples:

- Add all permissions to `login_sessions.txt` for user, group, and other:
  - `chmod u+rwx,g+rwx,o+rwx login_sessions.txt`
- Remove all permissions:
  - `chmod u-rwx,g-rwx,o-rwx login_sessions.txt`

### Using `=`

Using `=` assigns permissions **exactly** as specified (it overwrites existing permissions).

Example:

- Set read-only for user, group, and other:
  - `chmod u=r,g=r,o=r login_sessions.txt`

If the user previously had write permission, it is removed because only read was assigned.

---

## `chmod` characters (first argument)

- `u` — change **user** permissions
- `g` — change **group** permissions
- `o` — change **other** permissions
- `+` — add permission(s)
- `-` — remove permission(s)
- `=` — assign permission(s) exactly

**Note:** When changing more than one owner type, separate changes with commas and do **not** add spaces after commas.

---

## Least privilege example

Scenario: `bonuses.txt` in a `compensation` directory is owned by an HR user `hrrep1`. Only `hrrep1` should access the file; others in the HR group should not.

If `ls -l` shows permissions `-rw-rw----`, the **group** has read/write access that isn’t needed.

To remove group read/write:

- `chmod g-rw bonuses.txt`

Now access better aligns with least privilege.

---

## Key takeaways

- `ls -l` and `ls -la` help you investigate permissions.
- `chmod` changes permissions and helps enforce least privilege.

