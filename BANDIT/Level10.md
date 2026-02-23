# Bandit Level 10 -> Level 11

### 🎯 Objective
The password for the next level is stored in the file `data.txt`, which contains base64 encoded data.

### 🛠️ Commands Used
* `base64`: To encode or decode data using the Base64 standard.

### 💡 Solution
The content of `data.txt` was encoded in Base64 format. To retrieve the cleartext password, I used the `base64` command with the `-d` (decode) flag.

**Command:**
```bash
base64 -d data.txt
