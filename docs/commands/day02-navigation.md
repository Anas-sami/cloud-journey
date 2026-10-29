# Day 2 — Navigation & File Management

## Core ideas
- Linux is ONE tree that starts at `/` (root). No C: or D: like Windows.
- `~` (tilde) = my home (/home/s5rh) | `.` = current dir | `..` = parent dir
- Absolute path starts with `/` (works anywhere). Relative path depends on where I am.
- A command = COMMAND + space + OPTIONS + space + TARGET (e.g. `ls -la ~`)
- Linux is case-sensitive: `-r` (reverse) is NOT `-R` (recursive).
- A directory shows 4.0K because it is a small file holding a list of names,
  and ext4 stores data in 4KB blocks.
- `ls -l` first char: `-` file, `d` directory, `l` symbolic link.

## Commands
| Command | What it does | Trap I hit |
|---|---|---|
| `pwd` | Print where I am | - |
| `ls -lah` | List (long, all/hidden, human sizes) | `ls-a` fails: needs a space |
| `cd` | Change directory (`cd`, `cd ..`, `cd -`, `cd /abs/path`) | `cd` works on folders only |
| `mkdir -p` | Create folders (nested, many at once) | - |
| `touch` | Create empty FILES | touch makes files, not folders |
| `cp -r` | Copy (`-r` for folders, `-i` ask before overwrite) | source SPACE destination, not `/` |
| `mv` | Move OR rename | if destination folder doesn't exist, it RENAMES silently. Use `dir/` |
| `rm -ri` | Remove (`-r` folders, `-i` ask). No recycle bin! | can't delete a folder from inside it |
| `rmdir` | Remove EMPTY folder only (safe) | refuses if not empty |

## Golden rule before cp / mv / rm
1. Where am I? (`pwd`)  2. Can I see the source? (`ls`)  3. Where is the destination?

## Other lessons
- No spaces in file names — use `-` or `_`.
- `\` is an escape character, `/` is the path separator.
- Use TAB for autocomplete and ↑ to recall the last command.
