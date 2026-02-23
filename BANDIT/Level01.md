# Bandit Level 1 -> Level 2

### 🎯 Goal
The password for the next level is stored in a file called `-` located in the home directory.

### 🛠️ Commands Used
* `ls` - List directory contents.
* `cat` - Concatenate files and print on the standard output.

### 💡 Solution
In Linux, the `-` symbol is often used to represent **stdin** (standard input). If you try to run `cat -`, the terminal waits for user input instead of reading the file. To fix this, we provide the relative path to the file.

**Command:**
```bash
cat ./-
