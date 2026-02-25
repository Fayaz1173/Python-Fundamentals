# 1. Functions in Python

A **function** is a reusable block of code that performs a specific task.

## 1.1 Defining a Function

Use the `def` keyword.

### Syntax:

```
deffunction_name(parameters):
# code block
returnvalue
```

---

## 1.2 Function with Parameters

Parameters allow passing values into a function.

### Example:

```
defgreet(name):
print("Hello",name)

greet("John")
```

---

## 1.3 Function with Return Value

The `return` statement sends a result back to the caller.

### Example:

```
defadd(a,b):
returna+b

result=add(10,20)
print(result)
```

Without `return`, a function returns `None` by default.

---

# 2. Function Arguments

## 2.1 Default Arguments

A default value is used if no argument is provided.

### Example:

```
defgreet(name="Guest"):
print("Hello",name)

greet()# Uses default value
greet("Alice")# Overrides default
```

Important rule:

- Parameters with default values must come after non-default parameters.

Correct:

```
deffunc(a,b=5):
pass
```

Incorrect:

```
deffunc(a=5,b):
pass
```

---

## 2.2 Keyword Arguments

You can specify arguments by parameter name.

```
defdisplay(name,age):
print(name,age)

display(age=25,name="John")
```

---

# 3. Variable Scope

Scope determines where a variable can be accessed.

## 3.1 Local Scope

A variable defined inside a function is local.

```
defmy_func():
x=10
print(x)

my_func()
```

`x` cannot be accessed outside the function.

---

## 3.2 Global Scope

A variable defined outside all functions is global.

```
x=20

defmy_func():
print(x)

my_func()
```

---

## 3.3 Global Keyword

To modify a global variable inside a function:

```
x=10

defchange():
globalx
x=20

change()
print(x)
```

---

# 4. OOP Basics (Object-Oriented Programming)

OOP is a programming paradigm based on **classes and objects**.

It helps in:

- Code organization
- Reusability
- Maintenance

---

# 5. Class and Object

## 5.1 Class

A class is a blueprint for creating objects.

### Example:

```
classCar:
pass
```

---

## 5.2 Object

An object is an instance of a class.

```
classCar:
pass

car1=Car()
```

---

# 6. Attributes

Attributes are variables that belong to a class or object.

## 6.1 Instance Attributes

Defined inside the `__init__()` method.

```
classPerson:
def__init__(self,name,age):
self.name=name
self.age=age

p1=Person("John",25)
print(p1.name)
```

`name` and `age` are instance attributes.

---

# 7. Methods

Methods are functions defined inside a class.

## 7.1 Instance Method

```
classPerson:
def__init__(self,name):
self.name=name

defgreet(self):
print("Hello, my name is",self.name)

p1=Person("Alice")
p1.greet()
```

---

# 8. The self Parameter

- `self` refers to the current object.
- It must be the first parameter of instance methods.
- It is used to access attributes and other methods of the class.

Example:

```
classExample:
defshow(self):
print("This is a method")
```
