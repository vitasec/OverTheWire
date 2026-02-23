# Bandit Level 14 -> Level 15

### 🎯 Objective
Retrieve the password for the current level and submit it to port 30000 on localhost to get the next password.

### 🛠️ Commands Used
* `cat`: To read the password file located at `/etc/bandit_pass/bandit14`.
* `nc` (netcat): To communicate with a local network port.

### 💡 Solution
After logging in as `bandit14` using the private key, I retrieved the cleartext password from the system files. Then, I sent this password to port 30000 on the local machine using `nc`.

**Steps:**
1. `cat /etc/bandit_pass/bandit14` (Copy the output)
2. `nc localhost 30000`
3. Paste the password and press Enter.

### 🔑 Password
*REDACTED / RECEIVED FROM THE PORT RESPONSE*
