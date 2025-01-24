# Strings Time Complexity Cheat Sheet

Python’s **string** is an immutable sequence of characters, optimized for text processing. This cheat sheet provides the average and worst-case time complexities for common string operations, helping developers write efficient Python code.

---

## 📋 Overview of String Operations

| **Operation**          | **Examples**             | **Average Case** | **Worst Case** |
|-------------------------|--------------------------|-------------------|----------------|
| Access by Index        | `s[i]`                  | O(1)             | O(1)          |
| Search                 | `x in s`                | O(N)             | O(N)          |
| Iteration              | `for c in s:`           | O(N)             | O(N)          |
| Slicing                | `s[start:end]`          | O(k)             | O(k)          |
| Concatenation          | `s1 + s2`               | O(len(s1) + len(s2)) | O(len(s1) + len(s2)) |
| Length                 | `len(s)`                | O(1)             | O(1)          |
| Count                  | `s.count(x)`            | O(N)             | O(N)          |
| Find/Index             | `s.find(x)`, `s.index(x)`| O(N)             | O(N)          |
| Replace                | `s.replace(a, b)`       | O(N)             | O(N)          |
| Split                  | `s.split(delimiter)`    | O(N)             | O(N)          |
| Join                   | `'delimiter'.join(list)`| O(N)             | O(N)          |

---

## 💡 Key Notes:

1. **Immutable Nature**:
   - Strings in Python are immutable, so any operation that modifies a string results in the creation of a new string.

2. **Access and Iteration**:
   - Accessing characters by index and iterating through a string is efficient with O(1) and O(N) complexities respectively.

3. **Concatenation and Join**:
   - Concatenating strings using `+` is O(N), as it creates a new string. Use `'delimiter'.join(list)` for efficient concatenation of multiple strings.

4. **Search and Replace**:
   - Operations like `find`, `index`, `replace`, and `split` scan the entire string, resulting in O(N) complexity.

---

## 📖 Example Usage

```python
# Example: Access and Search
my_string = "hello world"
element = my_string[4]  # O(1)
print(element)          # Output: o

is_present = "world" in my_string  # O(N)
print(is_present)                   # Output: True

# Example: Slicing and Concatenation
sub_string = my_string[0:5]  # O(k)
print(sub_string)            # Output: hello

concat_string = my_string + "!"  # O(len(my_string) + len("!"))
print(concat_string)          # Output: hello world!

# Example: Join and Split
words = my_string.split()    # O(N)
print(words)                 # Output: ['hello', 'world']

joined_string = " ".join(words)  # O(N)
print(joined_string)             # Output: hello world
```

---

## 📥 When to Use Strings?
- Use strings for **text manipulation** and **character sequences**.
- Opt for `bytearray` when working with **mutable sequences** of bytes for better performance.

---

Explore the [Complexity Overview](complexity_overview.md) for comparisons across all data structures!
