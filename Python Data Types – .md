## Python Data Types – 

In Python, **data types** define the kind of value a variable can store. The main built-in data types you need to understand are:

- **Strings**
- **Lists**
- **Tuples**
- **Dictionaries**

---

## 1️⃣ Strings (`str`)

A **string** is a sequence of characters enclosed in quotes.

```
name="Python"
message='Hello World'
```

### 🔹 Key Properties

- Ordered (characters have positions/index)
- Immutable (cannot change individual characters)
- Indexed (starts from 0)

### 🔹 Accessing Characters

```
text="Python"
print(text[0])# P
print(text[-1])# n
```

### 🔹 Common String Methods

```
text.lower()# convert to lowercase
text.upper()# convert to uppercase
text.startswith("P")# True
text.endswith("n")# True
text.replace("P","J")
```

### 🔹 String Concatenation

```
first="Hello"
second="World"
print(first+" "+second)
```

---

## 2️⃣ Lists (`list`)

A **list** is a collection of items stored in square brackets `[]`.

```
numbers= [1,2,3,4]
names= ["Alice","Bob","Charlie"]
```

### 🔹 Key Properties

- Ordered
- Mutable (can be changed)
- Allows duplicate values
- Can store mixed data types

```
mixed= [1,"Python",3.5]
```

### 🔹 Accessing Elements

```
print(numbers[0])# 1
print(numbers[-1])# 4
```

### 🔹 Modifying List

```
numbers[0]=10
print(numbers)
```

### 🔹 Adding Elements

```
numbers.append(5)# add at end
numbers.insert(1,20)# insert at index 1
```

### 🔹 Removing Elements

```
numbers.remove(20)
numbers.pop()
```

---

## 3️⃣ Tuples (`tuple`)

A **tuple** is similar to a list but uses parentheses `()`.

```
coordinates= (10,20)
```

### 🔹 Key Properties

- Ordered
- Immutable (cannot change after creation)
- Allows duplicates

### 🔹 Accessing Elements

```
print(coordinates[0])
```

### 🔹 Why Use Tuple?

- Faster than list
- Used when data should not change
- Good for fixed data (e.g., coordinates, days of week)

```
days= ("Mon","Tue","Wed")
```

---

## 4️⃣ Dictionaries (`dict`)

A **dictionary** stores data in **key-value pairs** using curly braces `{}`.

```
student= {
"name":"John",
"age":21,
"course":"Cybersecurity"
}
```

### 🔹 Key Properties

- Unordered (Python 3.7+ maintains insertion order, but conceptually key-based)
- Mutable
- Keys must be unique
- Accessed using keys (not index)

### 🔹 Accessing Values

```
print(student["name"])
```

### 🔹 Adding / Updating

```
student["age"]=22
student["grade"]="A"
```

### 🔹 Removing

```
student.pop("course")
```

---

# 🔎 Quick Comparison Table

| Feature | String | List | Tuple | Dictionary |
| --- | --- | --- | --- | --- |
| Ordered | ✅ | ✅ | ✅ | ✅ (3.7+) |
| Mutable | ❌ | ✅ | ❌ | ✅ |
| Indexed | ✅ | ✅ | ✅ | ❌ (key-based) |
| Duplicates | ✅ | ✅ | ✅ | Keys ❌, Values ✅ |
