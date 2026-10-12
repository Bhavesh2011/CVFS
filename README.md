# Customized Virtual File System (CVFS)

**Author:** Bhavesh Narayan Gaikwad

## Project Overview

The **Customized Virtual File System (CVFS)** is a C++ project that simulates the basic functionality of a file system inspired by operating system concepts.

It provides a command-line interface for creating files, reading and writing data, deleting files, listing files, and viewing file statistics. The project uses linked lists, custom Inode structures, and dynamic memory allocation to manage file metadata and contents in memory.

## Features

- **File Creation:** Create files with specified permissions.
- **File Reading:** Read data using file descriptors.
- **File Writing:** Write data into files.
- **File Deletion:** Remove files using the `unlink` command.
- **File Listing:** Display available files using `ls`.
- **File Statistics:** View file size, permissions, and other metadata.
- **Permission Management:** Support read, write, and read-write permissions.
- **Inode Management:** Manage file metadata using custom Inode structures.
- **Memory Management:** Allocate and release memory dynamically.
- **Command-Line Interface:** Interact with the virtual file system through a custom shell.
- **Help System:** Display command descriptions and usage instructions.

## Technologies Used

- **Programming Language:** C++
- **Data Structures:** Singly Linked List
- **Memory Management:** Dynamic memory allocation
- **Concepts:** Object-Oriented and System Programming Concepts, Operating System Fundamentals
- **Libraries:** C++ Standard Library and standard system headers

## System Architecture

| Component | Purpose |
|---|---|
| `BootBlock` | Stores boot-related information. |
| `SuperBlock` | Tracks total and free Inodes. |
| `INODE` | Stores file names, sizes, permissions, and file contents. |
| `FILETABLE` | Maintains read/write offsets and access modes. |
| `UAREA` | Maintains the process information and file descriptor table. |

## Available Commands

| Command | Description | Example |
|---|---|---|
| `help` | Displays available commands. | `help` |
| `man` | Shows command-specific help. | `man creat` |
| `creat` | Creates a file with permissions. | `creat Demo.txt 3` |
| `ls` | Lists existing files. | `ls` |
| `write` | Writes data to a file. | `write 0` |
| `read` | Reads a specified number of bytes. | `read 0 5` |
| `stat` | Displays file statistics. | `stat Demo.txt` |
| `unlink` | Deletes a file. | `unlink Demo.txt` |
| `clear` | Clears the terminal screen. | `clear` |
| `exit` | Exits the application. | `exit` |

### File Permissions

- `1` — Read
- `2` — Write
- `3` — Read and Write

## How to Compile and Run

### Prerequisites

- A C++ compiler such as `g++`
- Linux or WSL recommended

### 1. Compile the program

```bash
g++ CVFS.cpp -o cvfs
```

Replace `CVFS.cpp` with your actual source filename.

### 2. Run the program

```bash
./cvfs
```

### 3. Try the commands

```text
creat Demo.txt 3
write 0
Hello CVFS
read 0 5
stat Demo.txt
ls
unlink Demo.txt
exit
```

## Learning Objectives

- Understand basic file-system architecture.
- Learn how Inodes store file metadata.
- Implement linked lists for file management.
- Understand file descriptors and access permissions.
- Practice dynamic memory allocation and deallocation.
- Apply operating system concepts through C++ programming.
- Develop a custom command-line interface.

## Limitations

- Supports a maximum of 5 Inodes in the current implementation.
- Maximum configured file size is 100 bytes.
- File contents are stored in RAM and are lost when the program exits.
- Implements a simplified virtual file system, not a complete operating system file system.

## Future Enhancements

- Add persistent file storage.
- Support larger files and more Inodes.
- Add file rename, append, and copy operations.
- Improve memory safety and error handling.
- Add directory management.
- Improve permission validation and file-offset handling.

## Author

**Bhavesh Narayan Gaikwad**

Computer Engineering student interested in C++, data structures, and operating system concepts.
