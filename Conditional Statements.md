### Conditional Statements: `if`, `elif`, `else`

Conditional statements allow a program to make decisions based on conditions. The program executes different blocks of code depending on whether a condition is **True** or **False**.

1. Check if a number is Positive, Negative, or Zero

input:

```python
num = int(input("Enter a number: "))

if num > 0:
    print("Positive number")
elif num < 0:
    print("Negative number")
else:
    print("Zero")
```

output:

```python
Enter a number: 10
Positive number
```

1.  **Check if a person is eligible to vote**

input:

```python

age = int(input("Enter your age: "))

if age >= 18:
    print("Eligible to vote")
else:
    print("Not eligible to vote")

```

output:

```python
Enter your age: 20
Eligible to vote
```
