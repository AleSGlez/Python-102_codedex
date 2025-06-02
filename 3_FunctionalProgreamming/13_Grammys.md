# 🎶 13. Grammys - Data Transformation in Python

## 🔄 Data Transformation Tools
Python offers three powerful functions to **transform, select, and aggregate** data:
- `map()`
- `filter()`
- `reduce()`

Let’s break them down. 🧠

---

## 🧭 `map()`
**Use when:** You want to apply a function to **each item** in an iterable.

```python
map(function, data)
```
### Example:
```python
def divide_by_2(x):
  return x / 2

halved_numbers = map(divide_by_2, [1, 2, 3, 4, 5])
print(list(halved_numbers))  # Output: [0.5, 1.0, 1.5, 2.0, 2.5]
```

Use `list()` to see the actual values.

---

## 🧪 `filter()`
**Use when:** You want to **select elements** that meet a condition.

```python
filter(function, data)
```
### Example:
```python
def filter_even(x):
  return x % 2 == 0

even_numbers = filter(filter_even, [1, 2, 3, 4, 5])
print(list(even_numbers))  # Output: [2, 4]
```

The function must return `True` or `False`.

---

## 🧮 `reduce()`
**Use when:** You want to **aggregate** a collection into a **single value**.

```python
from functools import reduce
reduce(function, data[, initial])
```
### Example:
```python
from functools import reduce

def multiply(x, y):
  return x * y

product = reduce(multiply, [1, 2, 3, 4, 5])
print(product)  # Output: 120
```

---

## 🎧 Practice: Grammy Playlist Transformation
You have a list of Grammy-winning songs and their durations (in minutes):
```python
playlist = [
  ('What Was I Made For?', 3.42),
  ('Just Like That', 5.05),
  ('Song 3', 6.8),
  ('Leave The Door Open', 4.02),
  ("I Can't Breath", 4.47),
  ('Bad Guy', 3.14)
]
```

### Your Tasks:
```python
from functools import reduce

# List of songs with their durations (in minutes)
playlist = [('What Was I Made For?', 3.42), ('Just Like That', 5.05), ('Song 3', 6.8), ('Leave The Door Open', 4.02), ('I Can\'t Breath', 4.47), ('Bad Guy', 3.14)]

#First, use the filter() function to pick out the songs that are longer than 5 minutes (i.e., 5.00).
def longer_than_five_minutes(song):
  return song[1]>5.00

greater_than5  = filter(longer_than_five_minutes,playlist)

print(list(greater_than5))

#Next, use map() to convert all the durations of the songs in your playlist from minutes to seconds.
def minutes_to_seconds(song):
  duration = song[1]
  minutes=int(duration)
  seconds=(duration-minutes)*100
  total_seconds=minutes*60+round(seconds)  
  return total_seconds

min_2_sec = map(minutes_to_seconds, playlist)

print(list(min_2_sec))

#Lastly, add up the total playtime of the playlist with reduce().
def add_durations(total, song):
  duration=song[1]
  return total+duration

total_playtime = reduce(add_durations, playlist, 0)

print(total_playtime)
```
