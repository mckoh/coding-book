# Debugging in Python

This is, what you will learn in this exercise:

* Runtime assertion.
* Raising of errors.
* Using try-except clauses

## Scenario

Prepare the following object for this exercise

* Create a first function (`quotient(a, b)`) that calculates the quotient of two input values (`a/b`).
* Create a second function (`read_file(file_path)`) that reads the content of a file.
* Create a text file (`test.txt`) in the same folder.

## Your Task for the first function

* Create an assertion that checks, if the first input value (a) of your function is an integer; If not, print a proper error message.
* Create an assertion that checks, if the second input value (b) of your function is an integer; If not, print a proper error message.
* Create an assertion that checks, if the second input value (b) of your function is larger than zero; If not, raise a ValueError with a proper error message.

## Your Task for the first function

* Try to open the file from the given `file_path`.
* Catch possible exceptions that occur if the given file cannot be found (FileNotFoundError).
* Catch possible exceptions that occur if the operating system cannot find or read the file (OSError).

## Help

If you struggle with the above tasks, you can get help:

* [Woring with try/except (W3C)](https://www.w3schools.com/python/python_try_except.asp)
* [Working with exceptions (W3C)](https://www.w3schools.com/python/python_ref_exceptions.asp)
