# Bandit Level 4 -> Level 5

### 🎯 Objective
The password for the next level is stored in the only human-readable file in the `inhere` directory.

### 🛠️ Commands Used
* `cd`: To change the current working directory.
* `ls`: To list files.
* `file`: To determine the type of data within a file.
* `cat`: To display the content of the identified text file.

### 💡 Solution
The `inhere` directory contains multiple files starting with a dash (`-`). Most of these files contain binary data. To find the password, I used the `file` command with a wildcard to inspect all files at once.

**Steps:**
1. Navigate to the directory: `cd inhere`
2. Identify the file type of all files: `file ./*`
3. Locate the file labeled as **ASCII text**.
4. Read that specific file using `cat ./-fileXX` (replacing XX with the correct number).

### 🔑 Password
*REDACTED / FOUND IN THE ASCII TEXT FILE*
