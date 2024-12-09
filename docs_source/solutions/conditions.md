# Working with Conditions Solution

```python
def weekday(day:int, sunday_first:bool = False) -> str:
    """Converts a number into a weekday

    Args:
        day (int): Day number to be converted
        sunday_first (bool): Flag to indicate if Sunday is first day

    Returns:
        Weekday name (str)
    """
    assert day <= 7, "day must be smaller or equal to 7."
    shift = 1 if sunday_first else 0
    weekdays = [
        "Sunday",
        "Monday",
        "Tuesday",
        "Wednesday",
        "Thursday",
        "Friday",
        "Saturday",
        "Sunday"
    ]
    return weekdays[day-shift]

weekday(1, sunday_first=False)
weekday(1, sunday_first=True)
```
