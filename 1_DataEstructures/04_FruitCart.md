# 🍉 04. Fruit Cart - Sets in Python

## 🪄 What Are Sets?
Sets are **unordered collections of unique elements**.

### Key Characteristics:
- No duplicates
- No specific order
- Useful for filtering and comparing unique items

Perfect when you don’t care about order but need to eliminate duplicates or identify shared data!

---

## 🛠️ Use Cases for Sets
- Database of unique IDs
- Filtering search results by category
- Identifying common tags, keywords, or categories

---

## 🧺 Creating Sets
You can use:
```python
set_example = {val1, val2, val3}
```
Or:
```python
set_example = set(['item1', 'item2'])
```

> ⚠️ While sets and dictionaries both use curly braces, **sets do not have key:value pairs**.

### Example:
```python
fruits = {'🍎 apple', '🍌 banana', '🍊 orange'}
```

---

## 🧮 Set Operations
Sets come with powerful methods:

- `.union()` – Combines two sets
- `.intersection()` – Finds common elements
- `.difference()` – Finds items in one set but not the other

### Example:
```python
set1 = {1, 2, 3, 4}
set2 = {3, 4, 5, 6}

set1.union(set2)         # {1, 2, 3, 4, 5, 6}
set1.intersection(set2)  # {3, 4}
set1.difference(set2)    # {1, 2}
```

---

## 🧰 Set Methods
- `.add(item)` – Adds a new item if it doesn’t already exist
- `.remove(item)` – Removes an item if it exists

### Example:
```python
my_set = {1, 2, 3}
my_set.add(4)      # {1, 2, 3, 4}
my_set.remove(2)   # {1, 3, 4}
```

---

## 🧪 Practice Activity: Fruit Cart
Let’s work with your favorite fruits and your bestie’s:

### Instructions:
- Create two sets: one for you, one for your friend
- Print the union of both sets (all fruits combined)
- Print the intersection (fruits you both like)
- Print the difference (fruits only in your set)

```python

fav_fruits = {'🍑 Peach', '🍎 Apple', '🍉 Watermelom', '🍒 Cherries', '🫐 Blueberries'}
ras_fav = {'🫐 Blueberries', '🍒 Cherries', '🥭 Mango', '🍍 Pineapple', '🍋 Lemon'}


# Operations:
union_fruits = fav_fruits.union(ras_fav)
print(union_fruits)

inter_fruits = fav_fruits.intersection(ras_fav)
print(inter_fruits)
```

![image](https://github.com/user-attachments/assets/295284d5-6193-40cc-b303-90bb3a209f6c)

