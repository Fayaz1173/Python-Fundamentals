# Learn Python Basics
### a. Understand Variables and Assignments

### 1) What Is a Variable?

A **variable** is a name that refers to a value stored in memory.

In Python, you create a variable the moment you assign a value to it.

```
x=10
name="Alice"
price=99.99
```

Here:

- `x` stores an integer
- `name` stores a string
- `price` stores a float

No need to declare the data type separately. Python determines it automatically (dynamic typing).

---

### 2) Assignment Operator (`=`)

The `=` symbol assigns a value to a variable.

```
age=25
```

This means:

- Store `25` in memory
- Label that memory as `age`

`=` does NOT mean “equals” in mathematics.

It means “assign this value”.

---

### 3) Reassigning Variables

You can change a variable’s value later.

```
x=5
x=10
```

Now `x` contains `10`, not `5`.

---

### 4) Multiple Assignments

Python allows assigning multiple variables at once.

```
a,b,c=1,2,3
```

Also:

```
x=y=100
```

Both `x` and `y` store `100`.

---

### 5) Variable Naming Rules

Valid:

```
username="admin"
user_1="John"
totalAmount=500
```

Invalid:

```
1name="John"# Cannot start with a number
user-name="John"# Hyphen not allowed
```

Rules:

- Must start with a letter or `_`
- Cannot start with a number
- Case-sensitive (`Age` and `age` are different)
- No spaces

---

### 6) Checking Variable Type

Use `type()`:

```
x=10
print(type(x))
```

Output:

```
<class 'int'>
```
