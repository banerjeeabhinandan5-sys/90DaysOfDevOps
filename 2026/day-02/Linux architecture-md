Linux Architecture Notes
1. Core Components of Linux
Kernel
The core of the Linux operating system.
Manages CPU, memory, storage, devices, and processes.
Acts as a bridge between hardware and applications.
User Space
Where user applications and commands run.
Examples: Bash shell, web servers, text editors, and scripts.
Programs request kernel services using system calls.
init / systemd
The first process started by the kernel (PID 1).
Initializes the system during boot.
Starts and manages services like networking, SSH, and databases.
2. Process Creation and Management
Every running program is a process with a unique PID (Process ID).
New processes are usually created using fork(), then replaced with a new program using exec().
The kernel schedules processes and allocates CPU time.
A parent process can create child processes and wait for them to finish.
Common Process States
Running (R): Currently using the CPU or ready to run.
Sleeping (S): Waiting for an event (e.g., user input or disk I/O).
Stopped (T): Paused by a signal or debugger.
Zombie (Z): Process has finished but its parent has not collected its exit status.
Uninterruptible Sleep (D): Waiting for hardware or disk operations.
3. What systemd Does
Boots the system and starts essential services.
Manages background services (daemons).
Automatically restarts failed services (if configured).
Tracks service logs using journalctl.
Controls service startup order using dependencies.
Why It Matters
Simplifies service management.
Makes system boot faster and more reliable.
Essential for troubleshooting service failures in DevOps.
4. Five Commands Used Daily
ps – View running processes.
top – Monitor CPU and memory usage in real time.
systemctl – Start, stop, and check services.
journalctl – View system and service logs.
kill – Stop or terminate a process.
