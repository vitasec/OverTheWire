# Bandit Level 15 -> Level 16

### 🎯 Objective
Submit the password for the current level to port 30001 on localhost using SSL encryption to retrieve the next password.

### 🛠️ Commands Used
* `openssl s_client`: A tool to create a secure connection to a server using SSL/TLS.
* `-connect`: Specifies the host and port to connect to.

### 💡 Solution
Unlike the previous level, port 30001 requires an encrypted connection. Using `netcat` would fail. I used `openssl` to establish a secure session and then provided the Bandit 15 password.

**Command:**
```bash
openssl s_client -connect localhost:30001
