# 🖼️ 03. Met Museum - Dictionaries in Python

## 📚 What Are Dictionaries?
Dictionaries are **unordered** collections that store data in **key:value** pairs.

### Syntax:
```python
# single line
dictionary = {key: value}

# multi-line
dictionary = {
  key1: value1,
  key2: value2,
  key3: value3
}
```

- Items are enclosed in curly braces `{}`.
- Each key must be **unique** and **immutable** (e.g., strings).
- Values can be of any data type.

---

## 🔑 Accessing Data
Use square brackets and the key to access values:
```python
print(dictionary['key'])
```

---

## 🔄 Updating Data
You can update values by assigning a new value to an existing key:
```python
dictionary['key'] = new_value
```

---

## 🛠️ Dictionary Methods
- `.keys()` – returns all keys
- `.values()` – returns all values
- `.items()` – returns all key:value pairs as tuples

```python
print(dictionary.keys())
print(dictionary.values())
print(dictionary.items())
```

These methods are useful when you want to loop through or inspect a dictionary’s structure.

---

## 🗽 Practice Activity: Met Museum
Search the Met Museum website for your favorite artifact. Under "Artwork Details," create a dictionary in Python that includes:

```python
collection = {
  'title': 'Goa Stone and Gold Case',
  'period': 'late 17th–early 18th century' ,
  'geography': 'Probably made in India, Goa'}
}
```

Then:
```python
print(collection.keys())
print(collection.values())
print(collection.items())
```

See how easy it is to organize and access data with dictionaries? 🧠
