# Key Differences Between Python and JavaScript

## 1. Defining Variables

### JavaScript

```javascript
let x = 10; // Using let (ES6+)
const name = "Alice"; // Using const for constants
```

### Python

```python
x = 10  # No need to declare type
name = "Alice"  # String
```

**Key Difference:** Python does not require explicit type declarations, whereas JavaScript requires `let`, `const`, or `var`.

---

## 2. Data Types

### JavaScript

```javascript
let x = 10;       // Number (no distinction between int and float)
let y = 3.14;     // Number
let isActive = true; // Boolean
let name = "Alice"; // String
```

### Python

```python
x = 10        # Integer
y = 3.14      # Float
is_active = True  # Boolean
name = "Alice"  # String
```

**Key Difference:** Python has separate `int` and `float` types, while JavaScript uses `Number` for both.

## 3. Lists vs. Arrays

### JavaScript (Arrays)
```javascript
let numbers = [1, 2, 3, 4];
numbers.push(5);  // Adding an element
```

### Python (Lists)
```python
numbers = [1, 2, 3, 4]
numbers.append(5)  # Adding an element
```

**Key Difference:** Python uses `list`, while JavaScript uses `Array`.

---

## 4. Dictionaries vs. Objects

### JavaScript (Object)
```javascript
let person = {name: "Alice", age: 25};
console.log(person.name); // Output: Alice
```

### Python (Dictionary)
```python
person = {"name": "Alice", "age": 25}
print(person["name"])  # Output: Alice
```

**Key Difference:** Python uses dictionaries (`dict`), while JavaScript uses objects (`{}`).

---

## 5. Null vs. None

### JavaScript
```javascript
let value = null;
```

### Python
```python
value = None
```

**Key Difference:** Python uses `None`, whereas JavaScript uses `null`.

---

## 6. Printing Output

### JavaScript
```javascript
console.log("Hello, World!");
```

### Python
```python
print("Hello, World!")
```

**Key Difference:** Python uses `print()`, whereas JavaScript uses `console.log()`.

---

## 7. Conditionals

### JavaScript
```javascript
let age = 18;
if (age < 18) {
    console.log("Minor");
} else if (age === 18) {
    console.log("Just turned 18");
} else {
    console.log("Adult");
}
```

### Python
```python
age = 18
if age < 18:
    print("Minor")
elif age == 18:
    print("Just turned 18")
else:
    print("Adult")
```

**Key Difference:** JavaScript uses `{}` for block scopes, while Python uses indentation.

---

## 8. Loops

### JavaScript (for loop)
```javascript
for (let i = 0; i < 5; i++) {
    console.log(i);
}
```

### Python (for loop)
```python
for i in range(5):
    print(i)
```

### JavaScript (while loop)
```javascript
let count = 0;
while (count < 3) {
    console.log(count);
    count++;
}
```

### Python (while loop)
```python
count = 0
while count < 3:
    print(count)
    count += 1
```

**Key Difference:** Python uses `range()` in loops, while JavaScript uses traditional `for` syntax.

---

## 9. Functions

### JavaScript
```javascript
function greet(name) {
    let answer = `Hello, ${name}!`;
    return answer;
}
console.log(greet("Alice"));
```

### Python
```python
def greet(name):
    answer = f"Hello, {name}!"
    return answer
print(greet("Alice"))

```

**Key Difference:** Python defines functions using `def`, while JavaScript uses `function`.

---

## 10. Classes

### JavaScript

```javascript
class Person {
    constructor(name) {
        this.name = name;
    }

    greet() {
        return `Hello, my name is ${this.name}!`;
    }
}

const alice = new Person("Alice");
console.log(alice.greet());
```

### Python

```python
class Person:
    def __init__(self, name):
        self.name = name

    def greet(self):
        return f"Hello, my name is {self.name}!"

alice = Person("Alice")
print(alice.greet())
```

**Key Difference**:** Python defines classes using `class ClassName:` with an `__init__` method for initialization, while JavaScript uses `class ClassName {}` with a `constructor` method.