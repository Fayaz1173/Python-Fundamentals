# Python Data Types

Python has several built-in data types. The most commonly used are:

- Strings
- Lists
- Tuples
- Dictionaries
- Sets

---

## 1️ Strings (`str`)

### ➤ Definition

A string is a sequence of characters enclosed in quotes.

```
name="Python"
message='Hello World'
```

### ➤ Key Features

- Ordered (characters have index positions)
- Immutable (cannot change individual characters)
- Allow duplicates

### ➤ Accessing Characters

```
word="Cyber"
print(word[0])# C
print(word[-1])# r
```

### ➤ Common Methods

```
text="hello"
text.upper()# 'HELLO'
text.lower()# 'hello'
text.startswith("h")# True
text.replace("h","H")# 'Hello'
```

---

## 2️ Lists (`list`)

### ➤ Definition

A list is a collection of items stored in square brackets.

```
numbers= [1,2,3,4]
names= ["Alice","Bob","Charlie"]
```

### ➤ Key Features

- Ordered
- Mutable (can change items)
- Allow duplicates
- Can store different data types

```
mixed= [10,"Python",3.5]
```

### ➤ Accessing Elements

```
print(numbers[0])# 1
```

### ➤ Modifying List

```
numbers[1]=20
```

### ➤ Common Methods

```
numbers.append(5)
numbers.insert(1,100)
numbers.remove(3)
numbers.pop()
```

---

## 3️ Tuples (`tuple`)

### ➤ Definition

A tuple is similar to a list but uses parentheses.

```
coordinates= (10,20)
```

### ➤ Key Features

- Ordered
- Immutable (cannot change values)
- Allow duplicates

```
data= (1,2,2,3)
```

### ➤ Accessing Elements

```
print(coordinates[0])# 10
```

### ➤ Why Use Tuples?

- Faster than lists
- Used when data should not change
- Useful for fixed values like coordinates

---

## 4️ Dictionaries (`dict`)

### ➤ Definition

A dictionary stores data in key-value pairs using curly braces.

```
student= {
"name":"John",
"age":22,
"course":"Cybersecurity"
}
```

### ➤ Key Features

- Unordered (Python 3.7+ maintains insertion order, but conceptually key-based)
- Mutable
- Keys must be unique
- Values can be duplicated

### ➤ Accessing Values

```
print(student["name"])# John
```

### ➤ Modifying Dictionary

```
student["age"]=23
student["grade"]="A"
```

### ➤ Common Methods

```
student.keys()
student.values()
student.items()
student.pop("age")
```

---

## 5️ Sets (`set`)

### ➤ Definition

A set is a collection of unique elements enclosed in curly braces.

```
numbers= {1,2,3,4}
```

### ➤ Key Features

- Unordered
- Mutable
- Do NOT allow duplicates
- No indexing

```
data= {1,2,2,3}
print(data)# {1, 2, 3}
```

### ➤ Common Methods

```
numbers.add(5)
numbers.remove(2)
```

### ➤ Set Operations

```
a= {1,2,3}
b= {3,4,5}

print(a.union(b))# {1,2,3,4,5}
print(a.intersection(b))# {3}
print(a.difference(b))# {1,2}
```

---

# Quick Comparison Table

| Data Type | Ordered | Mutable | Duplicates Allowed | Syntax |
| --- | --- | --- | --- | --- |
| String | Yes | No | Yes | `" "` |
| List | Yes | Yes | Yes | `[ ]` |
| Tuple | Yes | No | Yes | `( )` |
| Dictionary | Key-based | Yes | Keys ❌ Values ✅ | `{key:value}` |
| Set | No | Yes | No | `{ }` |
