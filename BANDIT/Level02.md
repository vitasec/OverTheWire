# Bandit Level 2 -> Level 3

### 🎯 Objective
The password for the next level is stored in a file called `--spaces in this filename--` located in the home directory.

### 🛠️ Commands Used
* `ls`: To list the contents of the home directory.
* `cat`: To read the content of the file.

### 💡 Solution
This challenge presents two main issues:
1. **Dashes at the start**: Filenames starting with `--` are often misinterpreted by Linux commands as arguments or options (e.g., `cat --help`).
2. **Spaces in the name**: Spaces act as delimiters between arguments in the shell.

To solve this, I used the relative path `./` to explicitly tell the shell that the string is a filename, and wrapped the name in double quotes `""` to handle the spaces.

**Command:**
```bash
cat ./"--spaces in this filename--"
