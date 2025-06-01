# 🌍 12. Hola - Higher Order Functions

## 🚀 What Are Higher-Order Functions?
In Python (and functional programming), **higher-order functions** are functions that:
- Take other functions as arguments
- Return functions as results

They make your code more **modular, powerful, and reusable** — like a Swiss Army knife. 🛠️

---

## 🔁 Example: Applying an Operation
```python
# Higher-order function
def apply_operation(operation, numbers):
  result = []
  for num in numbers:
    result.append(operation(num))
  return result

# Operation to apply
def double(x):
  return x * 2

numbers_list = [1, 2, 3, 4, 5]
doubled_numbers = apply_operation(double, numbers_list)

print('Original Numbers:', numbers_list)
print('Doubled Numbers:', doubled_numbers)
```
- `apply_operation()` accepts a function and applies it to a list of numbers
- The result is dynamic and reusable depending on the function passed in

---

## 🧪 Practice: Language Translator
Let’s build a **higher-order function** that returns a function for language translation!

### Instructions:
1. Define a function `translator(language)`
2. Inside it, add a `translations` dictionary with common phrases in multiple languages:
```python
# Define Higher Order Function
def translator(language):
  # Create a dictionary for different languages
  translations = {
    'spanish': {'hello': 'hola', 'goodbye': 'adiós', 'thank you': 'gracias'},
    'french': {'hello': 'bonjour', 'goodbye': 'au revoir', 'thank you': 'merci'},
    'italian': {'hello': 'ciao', 'goodbye': 'arrivederci', 'thank you': 'grazie'}
  }
```
3. Define a nested `translate_word(word)` function that looks up a word in the correct language
4. Return the `translate_word()` function from `translator()`
```python
  def translate_word(word):
    if word.lower() in translations[language]:
      return translations[language][word.lower()]
    else:
      return 'Translation not available'

  return translate_word
```

### Example usage:
```python
translate_to_spanish = translator('spanish')
print(translate_to_spanish('hello'))  # Output: hola

translate_to_french = translator('french')
print(translate_to_french('hello'))  # Output: bonjour

translate_to_italian = translator('italian')
print(translate_to_italian('hello'))  # Output: ciao

translate_to_italian = translator('italian')
print(translate_to_italian('tonight'))  # Output: Translation not available
```
