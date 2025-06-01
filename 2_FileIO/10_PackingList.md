# 📦 10. Packing List - Chapter Wrap-Up

### 🧠 Recap:
- Read and write text files using `.read()`, `.write()`, `.seek()`
- Use `with open()` context manager to manage files
- Interact with **CSV files** using the `csv` module

### Refresher Syntax:
```python
with open('filename.txt', 'r') as file:
  try:
    # Work with files
  except Error:
    # Handle file errors
```

---

## 🧳 Practice Project: Build a Packing List
Let’s use what we’ve learned to create a packing checklist program.

### Step 1: Import CSV and Define Data
```python
import csv

data = [
  ['Item', 'Quantity'],
  ['Blender', 2],
  ['Posters', 30],
  ['Shoes', 2]
]
```

### Step 2: Handle File Read or Create It If Missing
```python
try:
  with open('packing_list.csv', 'r') as file:
    reader = csv.reader(file)
    for row in reader:
      print(row)

except FileNotFoundError:
  print("Packing list file not found. Creating a new one.")
  with open('packing_list.csv', 'w', newline='') as file:
    writer = csv.writer(file)
    writer.writerows(data)
```

This structure:
- Tries to read and display an existing `packing_list.csv`
- If the file is not found, it creates it using the sample `data`

---

## 📝 Wrap-Up Task
- Add more items to the `data` list to expand your packing list
- Share your file with friends so they can review it too

You now have practical skills to manage and automate file-based tasks — from diaries to playlists to packing lists! 💪

Next up: error handling and making your programs more resilient. 🚨
