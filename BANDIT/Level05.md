# Bandit Level 5 -> Level 6

### 🎯 Objective
Find the password for the next level stored in a file somewhere under the `inhere` directory with the following properties:
* Human-readable
* 1033 bytes in size
* Not executable

### 🛠️ Commands Used
* `ls`: To list directory contents.
* `cd`: To change directories.
* `find`: To search for files based on specific criteria (size, type, etc.).
* `cat`: To read the file content.

### 💡 Solution
Since the `inhere` directory contains many subdirectories and files, I used the `find` command to filter for the specific properties mentioned in the objective.

**Command:**
```bash
find . -type f -size 1033c ! -executable
