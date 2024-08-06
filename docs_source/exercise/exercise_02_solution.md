# Exercise 2: String Operations Solution

```python
a = "You rock"
b = "you rule"


# Concatenate string `a` and string b.
print(a + b)

# Concatenate string `a` and string b, and put a space between them.
print(a + " " + b)

# Concatenate string `a` and string b, and put " and " between them using Python's f-string.
print(f"{a} {b}")

# Repeat string `a` three times with commas and spaces between each repetition
print((a + ", ") * 3)

# Print string `b` in capital letters
print(b.upper())

# Print string `a` in lower case letters
print(a.lower())

# Check if string `a` ends with "rock"
print(a.endswith("rock"))

# Check if string `b` starts with "YOU".
print(b.startswith("YOU"))

# Capitalize string b.
print(b.capitalize())

# Find the position of the space character in string a
print(a.find(" "))

# Slice string a, and get the first character.
print(a[0])

# Slice string a, and get the first three characters.
print(a[0:4])

# Slice string a, and get the last character.
print(a[-1])

# Slice string a, and get the last four characters.
print(a[-4:])

# Invert string b.
print(b[::-1])

# Slice string a, getting everything that is left of the space character
print(a[:a.find(" ")])
```