# Exit Game Solution

```python
A, B, C, D = 0, 0, 0, 0

max_value = 36

for A in range(1, max_value):
    for B in range(1, max_value):
        for C in range(1, max_value):
            for D in range(1, max_value):

                row_1 = (D + C + D + A) == 15
                row_2 = (B + A + A + D) == 22
                row_3 = (C + B + D + B) == 36
                row_4 = (D + C + A + C) == 23

                col_1 = (D + B + C + D) == 24
                col_2 = (C + A + B + C) == 35
                col_3 = (D + A + D + A) == 10
                col_4 = (A + D + B + C) == 27

                if row_1 and row_2 and row_3 and row_4:
                    if col_1 and col_2 and col_3 and col_4:
                        print(A, B, C, D)
```
