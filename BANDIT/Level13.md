# Bandit Level 13 -> Level 14

### 🎯 Objective
Log in to the next level (bandit14) using the private SSH key stored in the home directory.

### 🛠️ Commands Used
* `ssh -i`: Log in using a private key instead of a password.
* `cat`: To read the password file after successful login.

### 💡 Solution
I used the provided `sshkey.private` to connect to `localhost` as the `bandit14` user. Once logged in, I read the password for the next level from the standard location.

**Command:**
```bash
ssh -i sshkey.private bandit14@localhost -p 2220
cat /etc/bandit_pass/bandit14
