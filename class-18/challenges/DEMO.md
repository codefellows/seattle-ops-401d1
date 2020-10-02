# Ops Challenge - Automated Brute Force Wordlist Attack Tool Part 3 of 3

## Demo Code

The demo code below introduces concepts necessary to complete the challenge.

This example code is from [How to Brute Force ZIP File Passwords in Python](https://www.thepythoncode.com/article/crack-zip-file-password-in-python).

```python

import zipfile
from tqdm import tqdm

# the password list path you want to use, must be available in the current directory

wordlist = "rockyou.txt"

# the zip file you want to crack its password

zip_file = "secret.zip"

# initialize the Zip File object

zip_file = zipfile.ZipFile(zip_file)

# count the number of words in this wordlist

n_words = len(list(open(wordlist, "rb")))

# print the total number of passwords

print("Total passwords to test:", n_words)

```
"DEMO.md" 45L, 1015C                                                                                                                                                 1,1           Top


