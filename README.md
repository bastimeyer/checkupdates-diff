checkupdates-colorized
====

A simple GNU Awk script which turns the output of Arch Linux's `checkupdates` utility (`pacman-contrib`) into a format that's easier to read and interpret.

The format is similar to `yay`'s verbose package format:

- It colorizes the version string diff of each package
- It aligns the data in columns
- It adds repository names to each package name
- It counts the number of out-of-date packages

```sh
checkupdates --nocolor | gawk -f checkupdates-colorized.awk
```

**Dependencies:**

1. `gawk`
2. `pacman-contrib`
3. `expac`


### Example

![Example](https://github.com/user-attachments/assets/e7788a7a-2a26-4c9c-8508-224cd92533df)
