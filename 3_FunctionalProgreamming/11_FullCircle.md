# 🔁 11. Full Circle - Functional Programming

## 🧼 Pure Functions
A **pure function** is predictable: it always returns the same output given the same input and has **no side effects** (like printing, modifying external state, or relying on global variables).

### ✨ Characteristics of Pure Functions:
- No reliance on global variables
- No printing, logging, or modifying data outside the function
- Always returns the same output for a given input

---

## 🔍 Pure vs Impure Function Example
```python
# Impure Function
def impure_squared(number):
  result = number ** 2
  print('The square of', number, 'is', result)  # Side effect
  return result

# Pure Function
def pure_squared(number):
  return number ** 2
```
- The **impure** function has a side effect: `print()`
- The **pure** function does only one thing: return the square of the input

---

## 🧪 Practice: Area of a Circle
Create a pure function to calculate the area of a circle.

### Instructions:
- Define a function `calculate_circle_area(radius)`
- Use the formula: `area = π * r²`
- Use `math.pi` or `3.14159` as an approximation
- **Return** the result only (do not print it)

```python
# Example structure
import math

def calculate_circle_area(radius):
    return math.pi * radius ** 2
```
