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

# Applying Loops and Conditions Together

1. Print Even and Odd Numbers from 1 to N

input:

```python
n = int(input("Enter a number: "))

i = 1

while i <= n:
    if i % 2 == 0:
        print(i, "is Even")
    else:
        print(i, "is Odd")
    i += 1
```

output:

```python
Enter a number: 5
1 is Odd
2 is Even
3 is Odd
4 is Even
5 is Odd
```

1. Count Positive and Negative Numbers in a List

input:

```python
numbers = [10, -5, 7, -2, 0, 15, -8]

positive = 0
negative = 0

for num in numbers:
    if num > 0:
        positive += 1
    elif num < 0:
        negative += 1

print("Positive numbers:", positive)
print("Negative numbers:", negative)
```

output:

```python
Positive numbers: 3
Negative numbers: 3
```

1.  Find the Largest Number in a List

input:

```python
numbers = [45, 12, 78, 34, 89, 23]

largest = numbers[0]

for num in numbers:
    if num > largest:
        largest = num

print("Largest number is:", largest)
```

output:

```python
Largest number is: 89
```

1. Print Multiples of 3 Between 1 and 20

input:

```python
for i in range(1, 21):
    if i % 3 == 0:
        print(i)
```

output:

```python
3
6
9
12
15
18
```
