# Exercise 5: Working with Coding Helpers Solution

```python
instructions = input("Give me the list:")

try:
    instructions = instructions.split(",")
    x = 0
    y = 0
    for instruction in instructions:

        print(f"Your game piece is at x={x} and y={y}.")

        direction = instruction[0]
        distance = int(instruction[1:])

        print(f" --> You now hop {direction}-{distance}.")

        if direction == "u":
            y += distance
        if direction == "d":
            y -= distance
        if direction == "r":
            x += distance
        if direction == "l":
            x -= distance

except IndexError:
    print(f"The passed instruction was not correct. '{instruction}' was given.")
except ValueError:
    print(f"The passed instruction was not correct. '{instruction[1:]}' is not numeric.")
```
