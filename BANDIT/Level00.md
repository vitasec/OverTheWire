## Bandit Level 0
Command used: ssh bandit0@bandit.labs.overthewire.org -p 2220
Password: bandit0

# Bandit Level 0 -> Level 1

### 🎯 Objective
The goal is to log into the game server via SSH and find the password for the next level stored in a file called `readme` in the home directory.

### 🛠️ Commands Used
* `ssh`: To connect to the remote server.
* `ls`: To list files in the current directory.
* `cat`: To read the content of the `readme` file.

### 💡 Solution
First, I connected to the OverTheWire server using the provided credentials. Once logged in, I located the password inside the `readme` file.

**Connection Command:**
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
