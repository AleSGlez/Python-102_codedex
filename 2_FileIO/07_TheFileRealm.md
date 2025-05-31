# 🎵 07. The File Realm - Opening & Handling Files

## 🔓 Opening Files in Python
To begin working with any file, you must open it using the `open()` function:
```python
file = open('filename.txt', 'r')
```

### `open()` Parameters:
- **file_path**: Path to the file (e.g., `'diary.txt'`)
- **mode**:
  - `'r'` → Read mode 📖
  - `'w'` → Write mode ✍🏼 (overwrites content)
  - `'a'` → Append mode 📝 (adds to the end)

> ⚠️ Caution: `'w'` mode **overwrites** existing content. Use `'a'` to add without losing data.

---

## ✍️ Writing to Files
- Use `.write()` to add text:
```python
file.write('This is a line.\n')
```
- Use `.writelines()` to write multiple lines:
```python
lines = ['Line one.\n', 'Line two.\n']
file.writelines(lines)
```

---

## 📖 Reading from Files
- `.read()` → Reads the **entire content**:
```python
content = file.read()
```

- `.readline()` → Reads **one line at a time**:
```python
line = file.readline()
```

- `.readlines()` → Reads **all lines into a list**:
```python
lines = file.readlines()
for line in lines:
    print(line, end='')
```

> Use `end=''` in `print()` to avoid double newlines.

---

## 🧹 Closing Files
Always close the file when finished:
```python
file.close()
```

Or use a **with block** for auto-closing:
```python
with open('filename.txt', 'r') as f:
    content = f.read()
```

---

## 🎧 Practice: Create Your Playlist
Let's create a script to organize your favorite songs!

### Step 1: Define Dictionary
```python
liked_songs = {
  'Bad Habits': 'Ed Sheeran',
  "I'm Just Ken": 'Ryan Gosling',
  'Mastermind': 'Taylor Swift',
  'Uptown Funk': 'Mark Ronson ft. Bruno Mars',
  'Ghost': 'Justin Bieber'
}
```

### Step 2: Create Writing Function
```python
def write_liked_songs_to_file(songs, file_name):
    with open(file_name, 'w') as file:
        file.write("Liked Songs:\n")
        for song, artist in songs.items():
            file.write(f"{song} by {artist}\n")
    print(f"Successfully added Liked songs to {file_name} ❤️")

# Write liked songs to a .txt file
write_liked_songs_to_file(liked_songs, "liked_songs.txt")
```

This function will write your dictionary to a `.txt` file named `liked_songs.txt`.

---
[liked_songs.txt](https://github.com/user-attachments/files/20536042/liked_songs.txt)
