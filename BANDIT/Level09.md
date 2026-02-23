# Bandit Level 9 -> Level 10

### 🎯 Objective
Find the password for the next level stored in the file `data.txt` as one of the few human-readable strings, preceded by several `=` characters.

### 🛠️ Commands Used
* `strings`: To find and print printable character strings from a binary file.
* `grep`: To search for specific patterns (the `=` signs).
* `|` (pipe): To chain the output of `strings` into `grep`.

### 💡 Solution
The `data.txt` file is a binary file, making it difficult to read with `cat`. I used the `strings` command to extract all readable text and then filtered the output with `grep` to find the line containing the `=` prefix mentioned in the challenge description.

**Command:**
```bash
strings data.txt | grep "=="
