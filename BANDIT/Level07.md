# Bandit Level 7 -> Level 8

### 🎯 Objective
The password for the next level is stored in the file `data.txt` next to the word **millionth**.

### 🛠️ Commands Used
* `grep`: To search for a specific pattern/word within a file.

### 💡 Solution
Since the `data.txt` file is very large, I used the `grep` command to filter the contents and find the line containing the keyword "millionth".

**Command:**
```bash
grep "millionth" data.txt
