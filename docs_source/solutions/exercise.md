# Übungsblatt Musterlösungen

## Darts (<span style="color:#33FF7D ">Einfach</span>, 15 Punkte)

```python
def calculate_score(x:float, y:float) -> int:
    """Calculates score of a dart based on its x and y coordinates

    Args:
        x: The x-coordinate measured from the center
        y: The y-coordinate measured from the center

    Returns:
        Score of the dart (int)

    Raises:
        None
    """

    # calculate the radius of the dart-hit
    center_distance:float = (x ** 2 + y ** 2) ** 0.5

    # determine circle in which the arrow has landed
    if center_distance <= 1:
        return 10
    elif center_distance <= 5:
        return 5
    elif center_distance <= 10:
        return 1
    return 0

print(
    calculate_score(-3.5, 3.5),
    calculate_score(7.1, -7.1),
    calculate_score(0, 10),
    calculate_score(-0.1, -0.1)
)
```

## Palindrom prüfen (<span style="color:#33FF7D ">Einfach</span>, 15 Punkte)

```python
def palindrom(word:str) -> bool:
    """Checks if a word is a palindrom word or not

    Args:
        word: The word to be checked

    Returns:
        Boolean output
    """

    # check the word in lowercase against the reversed wordin lower case
    return word.lower() == word.lower()[::-1]

print(
    palindrom("Otto"), # True
    palindrom("Anna"), # True
    palindrom("Reliefpfeiler"), # True
    palindrom("Racecar"), # True
    palindrom("Palindrom"), # False
    palindrom("Haus"), # False
    palindrom("Auto") # False
)
```

## Fizz-Buzz (<span style="color:#33FF7D ">Einfach</span>, 15 Punkte)

```python
def fizz_buzz(to:int) -> None:
    """Plays the game fizz-buzz outputting numbers or placeholders

    Args:
        to: The number to be countet to

    Returns:
        None

    Raises:
        None
    """
    n_fizz:int = 0
    n_buzz:int = 0
    n_fizzbuzz:int = 0

    # loop all numbers from 1 to to
    for number in range(1, to+1):

        # check if number can be divided by 5 and 3 without rest
        if (number%3 == 0) and (number%5 == 0):
            print("fizzbuzz")
            n_fizzbuzz += 1

        # check if number can be divided by 3
        elif number%3 == 0:
            print("fizz")
            n_fizz += 1

        # check if number can be divided by 5
        elif number%5 == 0:
            print("buzz")
            n_buzz += 1

        # else, print the number itself
        else:
            print(number)

    # print the aggregated values
    print("---")
    print("n_fizz =", n_fizz)
    print("n_buzz =", n_buzz)
    print("n_fizzbuzz =", n_fizzbuzz)

fizz_buzz(8)
fizz_buzz(17)
```
