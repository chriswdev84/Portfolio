# Simple FTP-like Client-Server Program

[![C](https://img.shields.io/badge/C-ANSI-blue.svg)](https://en.cppreference.com/w/c) [![POSIX](https://img.shields.io/badge/POSIX-compliant-lightgrey.svg)](https://pubs.opengroup.org/onlinepubs/9699919799/)

## Overview

This is a simple FTP-like client and server implemented in C. It demonstrates core systems-programming concepts such as TCP socket communication, process management with `fork()`, and basic file I/O on POSIX systems. The project was created as a school assignment and is maintained here as a legacy example of networking fundamentals.

## Why this project?

This project began as a coursework assignment to learn low-level network programming and inter-process communication. It helped me practice socket APIs, process forking, and designing a minimal text-based protocol—skills that are useful when building robust backend or systems software.

## Features

- Client commands for local/remote directory browsing and file transfer (`local`, `remote`, `lchange`, `rchange`, `retrieve`, `upload`, `display`, `quit`).
- Server supports directory navigation and file transfers with simple acknowledgments.
- Demonstrates multi-process handling of client connections using `fork()`.

## Prerequisites

- POSIX-compatible OS (Linux, macOS, or Windows with WSL/MinGW)
- GCC or compatible C compiler

## Compilation

Compile the client and server with:

```bash
gcc -o myftp myftp.c
gcc -o myftpserve myftpserve.c
```

## Running

### Start the server

```bash
./myftpserve [-d]
```

- `-d`: enable debug output
- Server listens on port 49999 by default

### Run the client

```bash
./myftp [-d] <port> <hostname>
```

- `<port>`: server port (default 49999)
- `<hostname>`: server hostname or IP

### Example session

```bash
# Terminal 1: start server
./myftpserve -d

# Terminal 2: connect client
./myftp 49999 localhost

MFTP> remote
MFTP> retrieve example.txt
MFTP> upload myfile.txt
MFTP> quit
```

## Architecture

- **Client**: command-line interface that issues text-based requests
- **Server**: multi-process server that forks a handler per client
- **Protocol**: simple text commands over TCP; separate data connections used for file transfer

## Technical Details

- Uses POSIX sockets (`AF_INET`, `SOCK_STREAM`)
- Process management with `fork()` and `exec()`
- File I/O: `open()`, `read()`, `write()`
- Directory ops: `chdir()`, `opendir()`