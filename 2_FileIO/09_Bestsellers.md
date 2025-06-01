# 📈 09. Bestsellers - Working with CSV Files

## 📄 What Are CSV Files?
CSV stands for **Comma-Separated Values** — a widely used format for storing tabular data.

Each row = a record  
Each column = a value separated by commas

Python provides the built-in `csv` module to read and write CSV files easily.

---

## 📖 Reading CSV Files
To read CSV content:
```python
import csv

with open('example.csv', 'r') as file:
  csv_reader = csv.reader(file)
  for row in csv_reader:
    print(row)
```
- `csv.reader()` creates a reader object
- Each row is a list of values (strings)
- Use a `for` loop to access each row

---

## ✍️ Writing CSV Files
To write data:
```python
import csv

data_to_write = [
  ['Name', 'Age', 'Grade'],
  ['Alice', 25, 'A'],
  ['Bob', 22, 'B'],
  ['Charlie', 28, 'A+']
]

with open('output.csv', 'w', newline='') as file:
  csv_writer = csv.writer(file)
  csv_writer.writerows(data_to_write)
```
- Use `csv.writer()` to create a writer object
- Use `.writerows()` to write multiple rows
- Use `newline=''` to avoid extra blank lines on some systems

---

## 🧪 Practice: Bestseller Detector
Let’s analyze data from a CSV and output the bestselling book 📚

### Instructions:
1. Open `Bestseller - Sheet1.csv` in **read mode**
2. Use `csv.reader()` to parse data
3. Loop through the file to find the book with the **highest sales (in millions)**
4. Create a new file `bestseller_info.csv`
5. Use `.writerow()` to save the result in the new file

```python
# Pseudocode structure
with open('Bestseller - Sheet1.csv', 'r') as file:
  reader = csv.reader(file)
  # Process to find the book with max sales

with open('bestseller_info.csv', 'w', newline='') as file:
  writer = csv.writer(file)
  writer.writerow(['Title', 'Author', 'Sales'])
  writer.writerow([title, author, sales])
```
