# Bandit Level 11 -> Level 12

### 🎯 Objective
Find the password for the next level stored in `data.txt`, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions (ROT13).

### 🛠️ Commands Used
* `cat`: To output the file content.
* `tr`: To translate or delete characters.
* `|` (pipe): To pass the text to the translation command.

### 💡 Solution
I used the `tr` command to perform a ROT13 transformation. By mapping the alphabet `A-Za-z` to a 13-place shifted version `N-ZA-Mn-za-m`, I decoded the ciphertext into plain text.

**Command:**
```bash
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
