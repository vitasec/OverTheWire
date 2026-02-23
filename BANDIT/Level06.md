# Bandit Level 6 -> Level 7

### 🎯 Objective
Find the password for the next level, which is stored somewhere on the server and has the following properties:
* Owned by user **bandit7**
* Owned by group **bandit6**
* 33 bytes in size

### 🛠️ Commands Used
* `find`: To search for files based on ownership and size.
* `cat`: To read the password from the discovered file.

### 💡 Solution
I searched the entire root file system (`/`) using the specific criteria provided. To keep the output clean, I redirected all "Permission denied" errors to `/dev/null`.

**Command:**
```bash
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
