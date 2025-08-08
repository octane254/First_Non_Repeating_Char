## 📌 first_non_repeating_char Function
Description
first_non_repeating_char is a Python function that returns the first character in a string that does not repeat. If all characters repeat, the function returns None.

## 🔧 Function Definition
python
Copy
Edit
def first_non_repeating_char(s):
    char_count = {}
    for char in s:
        char_count[char] = char_count.get(char, 0) + 1

    for char in s:
        if char_count[char] == 1:
            return char
    return None
## 🧪 Usage
Call the function by passing a string as an argument:

python
Copy
Edit
print(first_non_repeating_char("Hello"))  # Output: 'H'
print(first_non_repeating_char("swiss"))  # Output: 'w'
print(first_non_repeating_char("aabbcc")) # Output: None
## 📙 How It Works
The function creates a dictionary char_count to store the count of each character in the string.

It iterates through the string and updates the count.

It then scans the string again to return the first character whose count is 1.

## ✅ Requirements
Python 3.x

No external libraries are required.

