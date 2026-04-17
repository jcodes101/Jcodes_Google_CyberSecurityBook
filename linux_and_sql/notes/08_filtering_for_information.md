# Filtering for information

Filtering is an important skill for security analysts. **Filtering** means selecting data that match a certain condition. For example, if malware only affected `.txt` files, filtering could help you find those files quickly.

Filtering lets you search based on specific criteria, such as a **file extension** or a **string of text**.

---

## `grep`

`grep` searches a specified file and returns all lines in that file containing a specified string or text pattern.

It commonly takes two arguments:

- the string/pattern to search for
- the file to search through

Examples:

- `grep OS updates.txt` returns all lines containing `OS` in `updates.txt`.
- `grep error time_logs.txt` scans `time_logs.txt` and prints only the lines containing the word `error`.

---

## Piping (`|`)

The pipe character (`|`) sends the **standard output** of one command as the **standard input** to another command for further processing.

- **Standard output**: information returned by the OS through the shell
- **Standard input**: information received by the OS via the command line

Used with `grep`, piping helps filter output down to items that match a word or pattern.

Example:

- `ls /home/analyst/reports | grep users`

`ls` lists names of files/directories in `/home/analyst/reports`, then `grep users` filters that list down to only names that contain `users`.

**Note:** Piping is a general form of redirection and is useful beyond filtering—it’s a general way to make the output of one command become the input to another.

---

## `find`

`find` searches for directories and files that meet specified criteria. You can search for items that:

- contain a specific string in the name
- are a certain file size
- were last modified within a certain time frame

The first argument after `find` is where to start searching.

Example:

- `find /home/analyst/projects` searches everything starting at the `projects` directory.

After that, specify criteria. Without criteria, `find` can return a very large set of results.

Criteria are specified using **options**, which commonly begin with a hyphen (`-`).

---

## `-name` and `-iname`

To search for file/directory names that contain a specific string, use `-name` or `-iname` with the search string in quotes.

- `-name` is **case-sensitive**
- `-iname` is **case-insensitive**

Examples:

- `find /home/analyst/projects -name "*log*"`
- `find /home/analyst/projects -iname "*log*"`

In both cases, `*` is a wildcard that represents **zero or more unknown characters**.

With `-name`, a file named `LOGS.txt` would not match `*log*` because case differs. With `-iname`, it would match.

---

## `-mtime` (and `-mmin`)

To search for files/directories last modified within a time window, use `-mtime` (days).

Example:

- `find /home/analyst/projects -mtime -3` returns items modified within the last 3 days.

How to interpret values:

- `-mtime +1` → modified **more than** 1 day ago
- `-mtime -1` → modified **less than** 1 day ago

**Note:** Use `-mmin` instead of `-mtime` if you want to base the search on **minutes** instead of days.

---

## Key takeaways

Filtering helps security analysts quickly customize and locate information in the Linux file system.

Three key tools for filtering are:

- `grep`
- piping (`|`)
- `find`

