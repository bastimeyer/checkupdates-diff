checkupdates-diff
====

A simple wrapper around Arch Linux's `checkupdates` utility (`pacman-contrib`) which transforms its output into a format that's easier to read and interpret.

The format is similar to `yay`'s verbose package format:

- It colorizes the version string diff of each package
- It aligns the data in columns
- It adds repository names to each package name
- It counts the number of out-of-date packages

## Install

```sh
git clone --branch=aur https://github.com/bastimeyer/checkupdates-diff.git
cd checkupdates-diff
makepkg -si
```

## Usage

```sh
checkupdates-diff
```

## Example

![Example](https://github.com/user-attachments/assets/31f15326-c1d4-4f8e-a9a8-e349e96b8797)
