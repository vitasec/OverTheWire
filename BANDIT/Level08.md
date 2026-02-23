# Bandit Level 8 -> Level 9

### 🎯 Objective
The password for the next level is stored in the file `data.txt` and is the only line of text that occurs actually only once.

### 🛠️ Commands Used
* `sort`: To sort lines of text files.
* `uniq`: To report or omit repeated lines.
* `|` (pipe): To pass the output of one command as input to another.

### 💡 Solution
The `uniq` command only works on sorted data. Therefore, I first sorted the file and then used the `-u` flag with `uniq` to filter out all repeated lines and display only the unique one.

**Command:**
```bash
sort data.txt | uniq -u
