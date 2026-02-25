Loops are used to execute a block of code repeatedly.

Python mainly provides:

- `for` loop → used when the number of iterations is known.
- `while` loop → used when the number of iterations depends on a condition.

# 1. The `for` Loop

### Purpose

Used to iterate over a sequence (list, tuple, string, range, etc.).

### Syntax

```python
for variable in sequence:
    # block of code
```

Find the Sum of Even Numbers in a List

input:

```python
numbers = [10, 15, 22, 33, 40, 55, 60]
even_sum = 0

for num in numbers:
    if num % 2 == 0:
        even_sum += num

print("Sum of even numbers:", even_sum)
```

output:

```python
Sum of even numbers: 132
```

# 2. The `while` Loop

### Purpose

Executes as long as the condition is True.

Print Multiplication Table of a Number

input:

```python
num = int(input("Enter a number: "))

i = 1

while i <= 10:
    print(num, "x", i, "=", num * i)
    i += 1
```

output:

```python
Enter a number: 5
5 x 1 = 5
5 x 2 = 10
5 x 3 = 15
5 x 4 = 20
5 x 5 = 25
5 x 6 = 30
5 x 7 = 35
5 x 8 = 40
5 x 9 = 45
5 x 10 = 50
```
