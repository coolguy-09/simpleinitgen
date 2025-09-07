# SimpleInitGen

A lightweight, user-friendly Linux init generator.

## What is an init?

The init is the first userspace program executed by the Linux kernel after boot. It’s responsible for:
  - Starting essential services and daemons
  - Mounting partitions and filesystems
  - Handing control over to the shell or login manager

Without a proper init, your system won’t know how to transition from kernel space to user space.

## Getting ready

First, we need to install some packages.

### On Debian/Ubuntu:

```bash
sudo apt install make gcc binutils
```

### On Arch:

```bash
sudo pacman -S make gcc binutils
```

## Configuring

### Just run:
```bash
chmod +x configure
./configure
```

It will prompt you with a few questions to customize how your init script behaves.

## Compiling

### After you answered the questions 2 files will be made:
  - init.c (Main C file)
  - Makefile (To easily compile)

### To compile, just run:
```bash
make
```
### And you have a init program that you could just put in your initramfs!
