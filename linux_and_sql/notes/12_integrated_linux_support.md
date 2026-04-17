# Integrated Linux support

Linux provides several built-in commands to help you learn and troubleshoot.

---

## `man`

`man` displays information about other commands and how they work. It’s short for “manual.” The output is called a **man page**.

Example:

- `man chown` shows detailed information about `chown`, including options you can use.

---

## `apropos`

`apropos` searches man page **descriptions** for a specified string. This is useful when you don’t know the exact command name or when man pages are too long to scan.

Example:

- `apropos keyword`

You can also include `-a` to search for multiple words at once. With `-a`, results must match **all** words.

Example:

- `apropos -a graph editor` returns man pages that contain both “graph” and “editor” in their descriptions.

---

## `whatis`

`whatis` displays a one-line description of a command. It’s helpful when you only need a quick reminder or a general idea of what a command does.

Example:

- `whatis nano` prints a brief description of `nano`.

---

## Key takeaways

- Linux has a large global community of users on online resources (for example, Unix and Linux Stack Exchange).
- Integrated support commands include `man`, `apropos`, and `whatis`.

