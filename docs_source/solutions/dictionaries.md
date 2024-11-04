# Working with Dictionaries Solution

```python
a = {
    "firstname": "Bill",
    "lastname": "Vernon",
    "age": 59,
    "is_active": True
}

b = {
    "firstname": "Sue",
    "hobbies": [
        "swimming",
        "reading",
        "hiking"
    ],
    "is_active": False
}

# Read the value of key "firstname" from dictionary a.
print(a["firstname"])

# Replace the value of key "lastname" from dictionary a with "Weasley".
a["lastname"] = "Weasley"
print(a)

# Get the value of key "hobbies" from dictionary a if existing.
print(a.get("hobbies"))

# Get all the keys of dictionary b.
print(b.keys())

# Get all the values of dictionary b.
print(b.values())

# Get all items of dictionary b.
print(b.items())
```
