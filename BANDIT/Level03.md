# Bandit Level 3 -> Level 4

### 🎯 Objective
Find the password for the next level, which is stored in a hidden file in the `inhere` directory.

### 🛠️ Commands Used
* `cd`: To change the current working directory.
* `ls -la`: To list all files, including hidden ones (files starting with a dot).
* `cat`: To read the content of the hidden file.

### 💡 Solution
After entering the `inhere` directory, a standard `ls` command showed no files. In Linux, files starting with a `.` are hidden by default. By using `ls -la`, I revealed a hidden file named `...Hiding-From-You`. 

**Steps:**
1. Navigate to the directory: `cd inhere`
2. List all files (including hidden): `ls -la`
3. Read the hidden file: `cat ./...Hiding-From-You`

### 🔑 Password
*REDACTED / FOUND IN THE HIDDEN FILE*
