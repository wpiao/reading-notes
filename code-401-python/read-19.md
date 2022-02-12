# Read:19 - Python Regex - 02/12/2022

```python
import re

pattern = r"python"
sequence = "python is fun!"

re.match(pattern, sequence) # returns a match object, otherwise None

# wild card characters
# . - matches any single character except the newline character
# ^ - matches the start of the string
# $ - matches the end of string
# [abc] - matches a or b or c
# [a-zA-Z0-9] - matches any letter from (a to z) or (A to Z) or (0 to 9)
# \w - matches any single letter, digit, or underscore
# \W - matches any character not part of \w
# \s - matches a single whitespace - space, newline, tab, return
# \S - matches any character not part of \s
# \d - matches decimal digit 0-9
# \D - matches any character that is not a decimal digit
# \t - matches tab
# \n - matches newline
# \r - matches return
# \A - matches only at the start of the string, works across multiple lines as well
# \Z - Matches only at the end of the string.

```
