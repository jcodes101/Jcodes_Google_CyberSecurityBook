# Responsible use of `sudo`

To manage authorization and authentication tasks in Linux, you typically need **root** access (also called the **super user**) or elevated privileges. Logging in directly as root is not recommended because it increases risk if the root account is compromised, makes irreversible mistakes easier, and reduces accountability.

Instead, it’s recommended to use `sudo` when you need elevated privileges.

---

## What `sudo` does

`sudo` temporarily grants elevated permissions to specific users. The name comes from “**super user do**.”

Users must be granted access to use `sudo` via a configuration file called the **sudoers file**.

Although `sudo` is preferable to logging in as root, users who can run `sudo` commands can be higher-value targets in an attack.

---

## Why least use matters (hotel master key analogy)

Think of `sudo` like a hotel **master key**:

- Some workers need it (e.g., a janitor cleaning rooms).
- If an attacker steals the janitor’s credentials and master key, they can access any room.

Because `sudo` can bypass typical security controls, only users who truly need it should have it—and they should use it only for the specific commands required.

**Note:** Be cautious when copying commands from online sources; don’t use `sudo` accidentally.

---

## Authentication and authorization with `sudo`

- **Authentication**: verifying who someone is
- **Authorization**: determining what they are allowed to access

`sudo` is commonly used with commands that manage users and ownership.

---

## `useradd`

`useradd` adds a user to the system.

Example:

- `sudo useradd fgarcia`

Important options:

- `-g` sets the user’s **primary** (default) group
- `-G` adds the user to **supplemental** (secondary) groups (comma-separated)

Examples:

- `sudo useradd -g security fgarcia`
- `sudo useradd -G finance,admin fgarcia`

---

## `usermod`

`usermod` modifies existing user accounts. It supports the same `-g` and `-G` options.

Examples:

- Change primary group:
  - `sudo usermod -g executive fgarcia`
- Add a supplemental group (append):
  - `sudo usermod -a -G marketing fgarcia`

**Note:** When modifying supplemental groups, omitting `-a` with `-G` will **replace** existing supplemental groups with only the groups you specify. Using `-a -G` appends without replacing.

Other useful options:

- `-d` change the user’s home directory
- `-l` change the user’s login name
- `-L` lock the account (prevents login)

Example (change home directory):

- `sudo usermod -d /home/garcia_f fgarcia`

---

## `userdel`

`userdel` deletes a user from the system.

Example:

- `sudo userdel fgarcia`

By default, `userdel` does not remove files in the user’s home directory. Use `-r` to remove the home directory and its contents:

- `sudo userdel -r fgarcia`

**Note:** Consider locking an account with `usermod -L` instead of deleting it (e.g., when someone leaves an organization). This preserves the account for investigation/ownership tracking while preventing login.

---

## `chown`

`chown` changes ownership of a file or directory (user and/or group).

Examples:

- Change the **user owner** of `access.txt` to `fgarcia`:
  - `sudo chown fgarcia access.txt`
- Change the **group owner** of `access.txt` to `security` (use `:` before the group name):
  - `sudo chown :security access.txt`

`chown` also supports additional options, similar to other admin commands.

---

## Key takeaways

- Use `sudo` for temporary elevated privileges instead of logging in as root.
- Limit `sudo` access and usage to align with least privilege.
- Common `sudo`-enabled admin commands: `useradd`, `usermod`, `userdel`, `chown`.

