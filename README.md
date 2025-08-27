# CVFS (Custom Virtual File System)

## 📌 Project Overview
The **Custom Virtual File System (CVFS)** is a C++ project that simulates the core functionalities of a real file system.  
It provides users with a command-line interface to perform **file creation, deletion, reading, writing, searching, listing, and permission management**.  

This project was built to strengthen understanding of **Operating System concepts, File System architecture, and Data Structures**.

---

## ⚙️ Features
- 📂 Create and delete files
- ✍️ Read and write file data
- 🔒 Manage file permissions (Read, Write, Both)
- 📑 List all files with details
- 🔍 Search files by name
- 🗂 Maintain a Superblock and Inode Table (like real OS)
- 👨‍💻 Supports multiple commands like an OS shell

---

## 🛠️ Tech Stack
- **Language:** C++  
- **Data Structures Used:**  
  - **Superblock** → Tracks free inodes (like free space manager)  
  - **Inode Table** → Stores file metadata (name, size, type, permissions)  
  - **File Table (UAREA)** → Stores runtime info of open files (R/W pointers, mode)  
  - **User File Descriptor Table (UFDT)** → Maps file descriptors to file tables  

---

## 📚 Libraries Used
- `<iostream>` → Input/Output operations  
- `<string>` → Handling file names and data  
- `<cstring>` → String manipulation  
- `<unistd.h>` (if used in Linux builds) → File handling utilities  
- `<stdlib.h>` → Memory management  

---

## 📂 File System Architecture (Simplified)
- **Superblock** → Tracks free inodes count  
- **Inode Table** → Each file has an inode with metadata  
- **File Table (UAREA)** → Keeps file mode, read/write offset  
- **UFDT** → Maps file descriptors to file tables  

This architecture mimics real OS file systems like **EXT3/EXT4** but implemented in C++ with dynamic memory.

---

## 📖 Commands Available
| Command       | Description |
|---------------|-------------|
| `create`      | Create a new file |
| `open`        | Open an existing file |
| `read`        | Read contents of a file |
| `write`       | Write data into a file |
| `ls`          | List all files with details |
| `stat`        | Show detailed info about a file |
| `fstat`       | Show file info using file descriptor |
| `truncate`    | Remove file content without deleting file |
| `rm`          | Delete a file |
| `close`       | Close a file |
| `exit`        | Exit from CVFS |

---

## 🚀 How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/CVFS.git
   cd CVFS

## Compile the Project

  g++ CVFS_Project_Parth.cpp -o cvfs

## Run the Project

  ./cvfs
