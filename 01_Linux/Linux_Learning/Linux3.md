## Day 3: Linux Navigation and Directory Control Commands

### **1. Basic Navigation and Directory Commands (with Examples)**

1. **mkdir**: Create a new directory.
   - Example: `mkdir Projects`
2. **ls**: List directory contents.
   - Example: `ls -l` (detailed listing)
3. **tree**: Display directories and files in a tree-like format.
   - Example: `tree /home/user`
4. **cd**: Change the current directory.
   - Example: `cd /var/log`
5. **pwd**: Display the current working directory.
   - Example: `pwd`
6. **rmdir**: Remove an empty directory.
   - Example: `rmdir OldFolder`
7. **rm**: Remove files or directories.
   - Example: `rm -rf temp_folder`
8. **touch**: Create empty files.
   - Example: `touch newfile.txt`
9. **basename**: Display the filename from a path.
   - Example: `basename /home/user/file.txt` (Output: `file.txt`)
10. **dirname**: Display the directory portion of a path.
    - Example: `dirname /home/user/file.txt` (Output: `/home/user`)

---

### **2. Linux vs DOS: Navigation and Directory Commands**

| **Linux Command** | **Equivalent DOS Command** |
|-------------------|----------------------------|
| mkdir             | md & mkdir                 |
| ls                | dir                        |
| cd                | cd or chdir                |
| pwd               | cd                         |
| rmdir             | rd & rmdir                 |
| rm                | del                        |
| touch             | echo. > filename           |

---

### **3. Command Usage Examples**

- **Create directories**:
  ```bash
  mkdir Test
  mkdir -v Test        # Verbose mode (shows output)
  mkdir -p Folder1/Folder2/Folder3  # Create nested directories
  ```

- **Tree command**:
  ```bash
  yum install tree -y  # Install tree utility
  tree                 # Display directory structure
  ```

- **System updates and package management**:
  ```bash
  yum update -y        # Update system packages
  yum remove -y <package>  # Remove a package
  ```

- **Listing files with custom options**:
  ```bash
  ls -l     # Detailed list view
  ls -m     # Output separated by commas
  ls -ltr   # Long listing sorted by access time in reverse order
  ls -lh    # Long listing with human-readable file sizes
  ls -a     # Show hidden files
  ls -d */  # List directories only
  ```

- **Directory permissions during creation**:
  ```bash
  mkdir -m 700 python  # Directory with specific permissions
  ```

- **Basename and Dirname**:
  ```bash
  basename /path/to/file.txt   # Output: file.txt
  dirname /path/to/file.txt    # Output: /path/to
  ```

---

### **4. Inode Information**
- **Inode**: A data structure that stores metadata about files/directories, excluding the filename.
  ```bash
  ls -i    # Display inode number
  ls -li   # Display inode number with detailed information
  stat file.txt  # Display detailed inode and file information
  ```

---

### **5. Essential Navigation Tips (with Examples)**

- **Navigating directories**:
  ```bash
  cd ~     # Go to home directory
  cd       # Shortcut to home directory
  cd -     # Switch to previous working directory
  cd ..    # Move up one directory level
  cd /     # Move to the root directory
  ```

- **Removing files and directories**:
  ```bash
  rm -rf dir  # Recursively remove directories and their contents
  rm -f file  # Forcefully remove a file without confirmation
  rmdir dir   # Remove empty directory
  ```

- **Creating and displaying files**:
  ```bash
  touch file.txt     # Create an empty file
  cat file.txt       # Display file content
  more file.txt      # View file content one page at a time
  less file.txt      # View file content with backward/forward navigation
  head file.txt      # Show the first 10 lines of a file
  tail file.txt      # Show the last 10 lines of a file
  ```

- **Finding Files and Directories**:
  ```bash
  find /path -name "file.txt"    # Find files by name
  locate file.txt                # Quickly find files (requires updatedb)
  which command_name             # Locate the executable of a command
  ```

---

### **6. Important Concept: Difference Between rm and rmdir**

- **rm**: Used to remove files and directories. It can delete non-empty directories with the `-r` (recursive) option.
  - Example: `rm -rf directory_name`

- **rmdir**: Used to remove **only empty directories**. It will not delete a directory if it contains files.
  - Example: `rmdir directory_name`

---

### **7. Viewing and Editing Files (with Examples)**

- **Viewing file content**:
  ```bash
  cat file.txt       # Display file content
  less file.txt      # View content with navigation options
  head -n 20 file.txt # Display the first 20 lines
  tail -n 20 file.txt # Display the last 20 lines
  ```

- **Editing files**:
  ```bash
  nano file.txt      # Open file in nano editor
  vi file.txt        # Open file in vi editor
  ```

- **Getting help for commands**:
  ```bash
  man ls             # Manual page for ls command
  ls --help          # Quick help for ls command
  ```

### Summary 
In Day 3, we explored essential Linux commands for navigating and managing directories. We covered the differences between Linux and DOS commands, practical examples of directory creation, file listing, and package management. Key concepts like **inodes**, **recursive deletion**, and **directory permissions** were also introduced, along with the distinction between `rm` and `rmdir`. Additional tools like **basename**, **dirname**, and file-finding commands enhance your navigation efficiency. Examples for each command were provided to reinforce practical understanding. These foundational skills are critical for efficient file management in Linux-based DevOps environments.

