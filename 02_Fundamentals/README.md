# 02 Fundamentals

## 1. Defining Variables

```python
# Integer
x = 10

# Float
y = 3.14

# String
name = "Alice"

# Boolean
is_active = True
```

---

## 2. Printing Variables

```python
print(x)          # Output: 10
print(name)       # Output: Alice
print(f"Hello, {name}!")  # Output: Hello, Alice!
```

---

## 3. Basic Calculations

```python
# Arithmetic operations
sum_value = 5 + 3      # Addition
product = 4 * 2        # Multiplication
division = 10 / 3      # Division (float result)
floor_div = 10 // 3    # Floor division
modulus = 10 % 3       # Remainder
power = 2 ** 3         # Exponentiation

print(sum_value, product, division, floor_div, modulus, power)
```

---

## 4. Data Types

```python
print(type(x))      # Output: <class 'int'>
print(type(y))      # Output: <class 'float'>
print(type(name))   # Output: <class 'str'>
print(type(is_active))  # Output: <class 'bool'>
```

---

## 5. Conditions (if-elif-else)

```python
age = 18
if age < 18:
    print("Minor")
elif age == 18:
    print("Just turned 18")
else:
    print("Adult")
```

---

## 6. Loops

### **For Loop**
```python
for i in range(5):
    print(f"Iteration {i}")
```

### **While Loop**
```python
count = 0
while count < 3:
    print(f"Count: {count}")
    count += 1
```

---

## 7. Functions

```python
def greet(name):
    return f"Hello, {name}!"

print(greet("Alice"))  # Output: Hello, Alice!
```

---

## 8. Lists and Tuples

```python
# List (mutable)
numbers = [1, 2, 3, 4]
numbers.append(5)  # Add element
print(numbers)

# Tuple (immutable)
coordinates = (10, 20)
print(coordinates[0])  # Output: 10
```

---

## 9. Dictionaries

```python
person = {"name": "Alice", "age": 25, "city": "New York"}
print(person["name"])   # Output: Alice
person["age"] = 26      # Modify value
print(person)
```

---

## 10. List Comprehension

```python
squares = [x**2 for x in range(5)]
print(squares)  # Output: [0, 1, 4, 9, 16]
```

---

