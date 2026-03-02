# ft_linux

Build your own linux distribution aka How_to_train_your_kernel.

## Overview

ft_linux is a minimal Linux distribution built from scratch.
The project includes a custom-compiled Linux kernel, a manually constructed root filesystem, and a lightweight userspace powered by BusyBox.

The system boots inside QEMU and demonstrates the full Linux boot process: kernel initialization, root filesystem mounting, init execution, and shell access.

## Objectives

- Understand the Linux boot process
- Compile and configure the Linux kernel
- Create a minimal root filesystem hierarchy
- Implement a functional init process
- Integrate a lightweight userspace (BusyBox)
- Enable basic networking

## Architecture

[ QEMU ]
      ↓
[ Linux Kernel ]
      ↓
[ Root Filesystem (/) ]
      ↓
[ init (PID 1) ]
      ↓
[ BusyBox Shell ]

## Project Structure

ft_linux/
├── kernel/     # Linux source code
├── rootfs/     # Root filesystem hierarchy
├── build/      # Compiled artifacts
└── tools/      # Utility scripts

## Key Concepts

### Kernel
The Linux kernel is the core of the operating system. It manages CPU scheduling, memory, devices, and process isolation. Applications interact with hardware through system calls.

### Root Filesystem
The root filesystem (/) is the top-level directory structure mounted at boot. It contains essential directories such as /bin, /etc, /proc, and /sys.

### Userspace
Userspace consists of all non-kernel programs. In this project, BusyBox provides essential utilities and the system shell.

### QEMU
QEMU is a machine emulator used to boot and test the system in a virtualized environment.

## Build & Run

 make kernel
 make rootfs
 make run
