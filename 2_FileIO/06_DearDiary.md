# 📓 06. Dear Diary - File Handling in Python

## 💾 Introduction to File Handling
In data analysis and development, interacting with files is essential. Python makes this easy through **file I/O (Input/Output)** operations.

### Common Use Cases:
- ✏️ Save information to files (write)
- 🔍 Read data from files (read)
- 🔧 Manage and automate file system tasks

You'll learn how to perform these actions in real-life scenarios, including working with formats like `.txt` and `.csv`. 🧑‍💻

---

## 📂 Files in Python
To work with files, we use the `open()` function. It allows you to create, read, or write files depending on the mode you specify.

```python
file = open('example.txt', 'w')
```

- `'w'`: write mode (creates the file if it doesn't exist or overwrites it if it does)

### Writing to a File:
```python
file.write('Hello, World! 🌎')
```
This writes text into the newly created or opened file. 📝

> 🧠 Pro Tip: Don't forget to **close** your file after writing or reading!

---

## 🗝️ Instructions: Build Your Own Diary
It’s time to start your digital diary — your secrets are safe (locally) 🔐

### What To Do:
1. Use the `open()` function to create a new file called `diaries.txt`.
2. Write several **diary entries** into the file.
3. Make sure each entry is on a **new line** using `\n`.

```python
# Use the open() method to create a new diaries.txt
file = open('diaries.txt','w')
file.write('I just bought an owala bottle because the colors were pretty\n')
file.write('And an Amazon fire TV stick')
file.close()
```
![image](https://github.com/user-attachments/assets/92df3f62-c3c4-482c-8917-ee12c97c6369)
