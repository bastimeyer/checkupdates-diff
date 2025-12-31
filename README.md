checkupdates-diff
====

A simple GNU Awk script which turns the output of Arch Linux's `checkupdates` utility (`pacman-contrib`) into a format that's easier to read and interpret.

The format is similar to `yay`'s verbose package format:

- It colorizes the version string diff of each package
- It aligns the data in columns
- It adds repository names to each package name
- It counts the number of out-of-date packages

```sh
checkupdates --nocolor | gawk -f checkupdates-diff.awk
```

**Dependencies:**

1. `gawk`
2. `pacman-contrib`
3. `expac`


### Example

![Example](https://github.com/user-attachments/assets/31f15326-c1d4-4f8e-a9a8-e349e96b8797)
