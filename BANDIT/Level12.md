# Bandit Level 12 -> Level 13

### 🎯 Objective
The password for the next level is stored in the file `data.txt`, which is a hexdump of a file that has been repeatedly compressed using different formats (Gzip, Bzip2, and Tar).

### 🛠️ Commands Used
* `mktemp -d`: Create a temporary directory to work in.
* `xxd`: To convert the hexdump back into a binary file (`-r` flag).
* `file`: To determine the file type at each stage.
* `gzip` / `gunzip`: To handle Gzip compression.
* `bzip2`: To handle Bzip2 compression.
* `tar`: To extract Tar archives.
* `mv`: To rename files with proper extensions for decompression.

### 💡 Solution (Step-by-Step)

Since we cannot create files in the home directory, I first created a workspace in `/tmp`:
```bash
mktemp -d
cd /tmp/tmp.NtVlhz9T47  # Example directory name
cp ~/data.txt .

Step 1: Reverse the Hexdump

Convert the text hexdump back into its original binary form.
Bash

xxd -r data.txt > data

Step 2: First Layer (Gzip)

file data showed: gzip compressed data, was "data2.bin"
Bash

mv data data.gz
gunzip data.gz

Step 3: Second Layer (Bzip2)

file data showed: bzip2 compressed data
Bash

bzip2 -d data  # Created data.out

Step 4: Third Layer (Gzip)

file data.out showed: gzip compressed data, was "data4.bin"
Bash

mv data.out data.gz
gunzip data.gz

Step 5: Fourth Layer (Tar)

file data showed: POSIX tar archive
Bash

tar -xf data  # Extracted data5.bin

Step 6: Fifth Layer (Tar)

file data5.bin showed: POSIX tar archive
Bash

tar -xf data5.bin  # Extracted data6.bin

Step 7: Sixth Layer (Bzip2)

file data6.bin showed: bzip2 compressed data
Bash

bzip2 -d data6.bin  # Created data6.bin.out

Step 8: Seventh Layer (Tar)

file data6.bin.out showed: POSIX tar archive
Bash

tar -xf data6.bin.out  # Extracted data8.bin

Step 9: Final Layer (Gzip)

file data8.bin showed: gzip compressed data, was "data9.bin"
Bash

mv data8.bin data8.gz
gunzip data8.gz

Step 10: Reading the Password

file data8 finally showed: ASCII text
Bash

cat data8
