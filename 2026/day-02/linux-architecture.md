# Linux Architecture

## Core Components of Linux

### Kernel
- Core of the Linux operating system.
- Manages CPU, memory, processes, file systems, and hardware devices.
- Provides system calls that allow applications to communicate with hardware.

### User Space
- The area where user applications and services run.
- Examples: Bash shell, web servers, text editors, and scripts.
- Applications interact with the kernel through system calls.

### init / systemd
- The first process started by the kernel (**PID 1**).
- Initializes the system during boot.
- Starts, stops, and manages system services and background processes.

---

## Process Creation and Management

- A **process** is a running instance of a program.
- Every process has a unique **PID (Process ID)**.
- Processes are typically created using:
  1. **fork()** – Creates a copy of the parent process.
  2. **exec()** – Replaces the child process with a new program.
- The Linux kernel schedules processes and allocates CPU time.

### Process States
- **Running (R)** – Process is executing or ready to execute.
- **Sleeping (S)** – Waiting for an event such as user input or disk I/O.
- **Stopped (T)** – Process has been paused by a signal or debugger.
- **Zombie (Z)** – Process has finished execution but still has an entry in the process table because its parent hasn't collected its exit status.
- **Uninterruptible Sleep (D)** – Waiting for hardware or disk operations.

---

## What systemd Does

- Starts the operating system during boot.
- Manages system services and daemons.
- Automatically restarts failed services (when configured).
- Maintains service logs through `journalctl`.
- Handles service dependencies and startup order.

### Why systemd Matters
- Simplifies service management.
- Improves boot performance.
- Makes troubleshooting easier.
- Widely used across modern Linux distributions.

---

## 5 Daily Linux Commands

| Command | Purpose |
|---------|---------|
| `ps` | Display running processes |
| `top` | Monitor CPU and memory usage in real time |
| `systemctl` | Manage system services |
| `journalctl` | View system and service logs |
| `kill` | Terminate a process |

---

## Summary

- **Kernel** manages hardware and system resources.
- **User Space** is where applications and users interact with the system.
- **systemd** is the init system responsible for booting and managing services.
- Linux creates processes using **fork()** and **exec()**.
- Understanding processes and `systemd` is essential for Linux administration and DevOps troubleshooting.
