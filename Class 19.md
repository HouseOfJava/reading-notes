# Automation 

How can you use regular expressions in Python to search for specific patterns in a string, and what is the primary library to work with them?

Import the re module:

import re


Define the regular expression pattern you want to search for using special characters that represent specific characters or character classes:
python

pattern = r'ab+c'

There are many other functions in the re module for working with regular expressions, including re.findall(), re.sub(), and re.split()

What is the purpose of the shutil library in Python, and provide an example of a common use case for file or directory management with this library?

The shutil module in Python provides a higher-level interface for file and directory operations that builds on top of the lower-level os module. It provides functions for copying, moving, and deleting files and directories, as well as for archiving and compressing files and directories.

Creating a new directory at the specified path with the same contents as the original directory.


Explain one automation idea from the assigned material and describe how it can be implemented using Python’s regular expressions and shutil libraries.

Searching for for files and on your local computer and then making copies of those files to another location 
