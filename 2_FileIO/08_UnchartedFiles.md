# 🧭 08. Uncharted Files - Advanced File Operations

## 🔧 Exploring File Operations
Beyond basic read/write, Python lets you navigate and manipulate files more precisely using tools like:
- `try-finally` blocks
- File cursor control with `.seek()`
- Truncating file content with `.truncate()`

---

## 🛡️ Using `try-finally`
Always ensure a file is closed — even if something goes wrong:
```python
try:
  file = open('example.txt', 'r')
  # Perform operations
finally:
  file.close()
```

---

## 📖 Reading a File with `with`
Using a `with` block ensures that the file is properly closed after operations:
```python
with open('example.txt', 'r') as file:
  content = file.read()
  print(content)
```

---

## 📍 File Cursor with `.seek()`
Move the file cursor to a specific byte location:
```python
with open('example.txt', 'r') as file:
  file.seek(10)  # Moves to the 10th byte
  content = file.read()
```

---

## ✂️ Truncating Files with `.truncate()`
Used to resize a file by cutting off content after a certain length:
```python
with open('example.txt', 'a') as file:
  file.truncate(20)  # Reduces file to 20 bytes
```

---

## 🧪 Project: Simulate Unsending a Message
Let’s simulate deleting a message using `.seek()` and `.truncate()`:

### Step 1: Write a secret message
```python
sent_message = 'Hey there! This is a secret message.'
with open('sent_message.txt', 'w') as file:
  file.write(sent_message)
```

### Step 2: Modify the file to "unsend" the message
```python
with open('sent_message.txt', 'r+') as file:
  original_message = file.read()
  file.seek(0)  # Go back to start of file

  unsent_message = 'This message has been unsent.'
  file.write(unsent_message)
  file.truncate(len(unsent_message))
```

This combination of `.seek(0)` and `.truncate()` lets you replace the original message and simulate an "unsend" action. 🪄
