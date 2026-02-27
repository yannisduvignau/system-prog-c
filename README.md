# 🖥️ system-prog-c

> Introduction to **Systems Programming in C** — a collection of university lab exercises (TPs) and a final project covering core OS-level programming concepts: file I/O, processes, threads, signals, sockets, and more.

---

## 📋 Description

**system-prog-c** is an academic repository documenting a systems programming course in C. It is structured around four practical lab sessions (TP1 through TP4) of increasing complexity, followed by a comprehensive final project (`ProgSYS_Projet`).

The course covers low-level Unix/Linux programming concepts, from basic system calls and file manipulation to process management, multithreading, inter-process communication, and network sockets.

---

## 🗂️ Project Structure

```
system-prog-c/
├── TP1/               # Introduction to C, system calls & file I/O
├── TP2/               # Processes, fork(), exec() & pipes
├── TP3/               # Threads (pthreads), signals & synchronization
├── TP4/               # Sockets & network communication
└── ProgSYS_Projet/    # Final project — combining all concepts
```

---

## 🔬 Lab Sessions Overview

### 🧱 TP1 — Introduction & File System
> Foundations of C systems programming and Unix system calls.

**Topics covered:**
- Basic I/O with `read()`, `write()`, `open()`, `close()`
- File manipulation and directory traversal
- Standard library vs. system call file operations
- Error handling with `errno` and `perror()`

---

### 🔀 TP2 — Processes
> Creating and managing processes in Unix.

**Topics covered:**
- `fork()` — creating child processes
- `exec()` family — replacing process images
- `wait()` / `waitpid()` — process synchronization
- Pipes (`pipe()`) and standard I/O redirection

---

### 🔄 TP3 — Threads & Signals
> Concurrent programming with POSIX threads and Unix signals.

**Topics covered:**
- `pthread_create()`, `pthread_join()`, `pthread_exit()`
- Mutexes and condition variables for synchronization
- Signal handling with `signal()` and `sigaction()`
- Race conditions and critical sections

---

### 🌐 TP4 — Network Sockets
> Client-server communication via the socket API.

**Topics covered:**
- TCP/UDP socket creation — `socket()`, `bind()`, `listen()`, `accept()`
- Client-side connection — `connect()`, `send()`, `recv()`
- Multi-client server design
- Network byte order — `htons()`, `ntohl()`

---

### 🏗️ ProgSYS\_Projet — Final Project
> A comprehensive systems project combining the concepts from all four lab sessions.

Integrates file I/O, process management, threading, and network communication into a functional C application.

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Language | C (C99 / C11) |
| OS | Linux / Unix |
| Compiler | GCC |
| Build | `gcc` / `Makefile` |
| Threads | POSIX Threads (`pthreads`) |
| Networking | POSIX Socket API |

---

## 🚀 Getting Started

### Prerequisites

- Linux or macOS (or WSL on Windows)
- GCC compiler
- POSIX-compliant system

---

### Compile & Run

Navigate into any TP folder and compile with `gcc`:

```bash
# Single file
gcc -o program main.c
./program

# With pthread support (TP3+)
gcc -o program main.c -lpthread
./program

# With a Makefile (if provided)
make
./program
```

**Example — TP1:**
```bash
cd TP1
gcc -o tp1 main.c
./tp1
```

**Example — TP4 (two terminals):**
```bash
# Terminal 1 — Start the server
cd TP4
gcc -o server server.c
./server

# Terminal 2 — Start the client
gcc -o client client.c
./client
```

---

## 🧠 Concepts Covered

| Category | Topics |
|----------|--------|
| System Calls | `open`, `read`, `write`, `close`, `stat`, `errno` |
| File I/O | File descriptors, buffered vs. unbuffered I/O |
| Processes | `fork`, `exec`, `wait`, `exit`, zombie processes |
| IPC | Pipes, named pipes (FIFO), signals |
| Threads | `pthreads`, mutex, condition variables, barriers |
| Networking | TCP/UDP sockets, client-server, multi-client |
| Memory | Pointers, dynamic allocation, buffer management |

---

## 💡 Useful Commands

```bash
# Compile with warnings and debug info
gcc -Wall -Wextra -g -o program main.c

# Check for memory leaks
valgrind ./program

# Inspect system calls at runtime
strace ./program

# List open files / sockets
lsof -p <pid>
```

---

## 🤝 Contributing

1. Fork the project
2. Create your branch (`git checkout -b feature/new-exercise`)
3. Commit your changes (`git commit -m 'Add TP exercise'`)
4. Push to the branch (`git push origin feature/new-exercise`)
5. Open a Pull Request

---

## 👤 Author

**Yannis Duvignau**  
[GitHub](https://github.com/yannisduvignau)

---

## 📄 License

This project is distributed under an open license. See the `LICENSE` file for more details.