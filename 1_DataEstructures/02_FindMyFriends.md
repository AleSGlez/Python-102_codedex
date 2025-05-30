# 🌍 02. Find My Friends - Tuples in Python

## 📌 What Are Tuples?
Tuples are **ordered** and **immutable** collections in Python. Perfect for storing **fixed data** such as coordinates or color values.

### 🧠 Key Features:
- Tuples **cannot be changed** after creation.
- They **can contain duplicates**.
- Elements are separated by commas, optionally enclosed in parentheses.
- Tuples can be **unpacked** into separate variables.

---

## 🧱 Tuple Syntax
```python
tuple_example = (1, '2', True)
navy_blue = (0, 0, 128)
```

### One-item Tuples (don’t forget the comma!):
```python
t1 = ('a',)
t2 = 'a',
t3 = ('a')  # Not a tuple
```

---

## 🔬 Accessing Tuple Values
Tuples are indexed like lists:
```python
my_dna = ('GCT', 'AGC', 'AGG', 'TAA', 'ACT', 'CAT')
print(my_dna[2])  # Output: AGG
```

---

## 🔄 Tuple Operations
- **Unpacking:**
```python
full_name = ('Ada', 'Lovelace')
first_name = full_name[0]
print(first_name)  # Output: Ada
```

- **Combining Tuples:**
```python
t1 = 'a',
t2 = 'b',
t3 = t1 + t2
print(t3)  # Output: ('a', 'b')
```

---

## 🧑‍🤝‍🧑 Project: Find My Friends

Let’s store friend locations using tuples of **latitude** and **longitude**!

### Example:
```python
# My city
my_location = (19.4326, -99.1332)  # Mexico City

# Friends’ cities
friend_1 = (34.0522, -118.2437)  # Los Angeles
friend_2 = (51.5074, -0.1278)    # London
friend_3 = (35.6895, 139.6917)   # Tokyo

print(friend_1)
print(friend_2)
print(friend_3)
```
### Bonus: A tuple of tuples is a tuple where each element is itself a tuple. Woah!
```python
friends = (
  (37.7749, -122.4194), 
  (40.7128, -74.0060), 
  (4.624335, -74.063644)
)
```
![image](https://github.com/user-attachments/assets/8501ac49-b458-4ec6-8658-08ef1842b9da)
