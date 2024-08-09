# Exercise 3: Working with Lists Solution

```python
a = [2, 4, 6, 1, 2, 3]
b = ["a", "b", "a", "a", "b"]

# Get the value of the first item in list a.
print(a[0])

# Get the value of the last item in list b.
print(a[-1])

# Get the values in list a in ascending order.
print(sorted(a))

# Get the values in list a in descending order.
print(sorted(a, reverse=True))

# Sort list a permanently.
a.sort()
print(a)

#  Join the elements of a and b in pairs.
print(list(zip(a, b)))

# Add a new element with value 7 to list a.
a.append(7)
print(a)

# Get the value of the first element in list a
# and remove it from the list at the same time.
print(a.pop(0))
print(a)

# Count the occurrences of value "b" in list b.
print(b.count("b"))

#  Get the index of the first occurrence of "a" in list b.
print(b.index("a"))

#  Get the number of items in list a.
print(len(a))

#  Extend list a with the following elements: [8, 9, 10].
a.extend([8, 9, 10])
print(a)

# Remove the first occurrence of "b" from list b.
b.remove("b")
print(b)
```
