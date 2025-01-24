# Complexity Overview of Python Data Structures

This overview summarizes the average and worst-case time complexities for common operations across Python's built-in data structures, including **lists**, **dictionaries**, **sets**, **tuples**, and **strings**. Use this cheat sheet to write efficient and optimized Python code.

---

## 📋 Data Structures and Their Operations

### Lists
Python's **list** is an ordered, mutable sequence, often implemented as a dynamic array.

| **Operation**          | **Examples**           | **Average Case** | **Worst Case**  |
|-------------------------|------------------------|-------------------|-----------------|
| Append                 | `l.append(x)`         | O(1)             | O(1)*           |
| Access by Index        | `l[i]`                | O(1)             | O(1)           |
| Search                 | `x in l`             | O(N)             | O(N)           |
| Delete by Index        | `del l[i]`           | O(N)             | O(N)           |
| Slice                  | `l[start:end]`       | O(k)             | O(k)           |
| Sort                   | `l.sort()`           | O(N log N)       | O(N log N)     |

[Learn more about lists here](lists.md).

---

### Dictionaries
Python's **dict** is implemented as a hash table, making it highly efficient for key-based operations.

| **Operation**          | **Examples**           | **Average Case** | **Worst Case**  |
|-------------------------|------------------------|-------------------|-----------------|
| Access by Key          | `d[k]`                | O(1)             | O(N)           |
| Insert/Update          | `d[k] = v`            | O(1)             | O(N)           |
| Delete by Key          | `del d[k]`            | O(1)             | O(N)           |
| Iteration (Keys/Values)| `for k in d:`         | O(N)             | O(N)           |

[Learn more about dictionaries here](dictionaries.md).

---

### Sets
Python's **set** is a hash-based collection optimized for membership tests and set operations.

| **Operation**          | **Examples**           | **Average Case** | **Worst Case**  |
|-------------------------|------------------------|-------------------|-----------------|
| Add Element            | `s.add(x)`            | O(1)             | O(N)           |
| Membership Test        | `x in s`             | O(1)             | O(N)           |
| Remove Element         | `s.remove(x)`         | O(1)             | O(N)           |
| Union                  | `s1 | s2`            | O(len(s1) + len(s2)) | O(len(s1) + len(s2)) |
| Intersection           | `s1 & s2`            | O(min(len(s1), len(s2))) | O(min(len(s1), len(s2))) |

[Learn more about sets here](sets.md).

---

### Tuples
Python's **tuple** is an immutable sequence, making it lighter than lists but with fewer operations.

| **Operation**          | **Examples**           | **Average Case** | **Worst Case**  |
|-------------------------|------------------------|-------------------|-----------------|
| Access by Index        | `t[i]`                | O(1)             | O(1)           |
| Search                 | `x in t`             | O(N)             | O(N)           |
| Slice                  | `t[start:end]`       | O(k)             | O(k)           |

[Learn more about tuples here](tuples.md).

---

### Strings
Python's **string** is an immutable sequence of characters, optimized for text processing.

| **Operation**          | **Examples**           | **Average Case** | **Worst Case**  |
|-------------------------|------------------------|-------------------|-----------------|
| Access by Index        | `s[i]`                | O(1)             | O(1)           |
| Concatenation          | `s1 + s2`             | O(len(s1) + len(s2)) | O(len(s1) + len(s2)) |
| Search                 | `x in s`             | O(N)             | O(N)           |
| Slice                  | `s[start:end]`       | O(k)             | O(k)           |
| Split                  | `s.split()`           | O(N)             | O(N)           |

[Learn more about strings here](strings.md).

---

## 🧠 Tips for Writing Efficient Code

1. **Choose the right data structure**:
   - Use **lists** for ordered, mutable sequences.
   - Use **dictionaries** or **sets** for fast lookups.
   - Use **tuples** or **strings** for immutable data.

2. **Avoid unnecessary operations**:
   - Minimize concatenation in loops (use `.join()` for strings).
   - Use slicing and comprehensions where possible.

3. **Profile your code**:
   - Use tools like `timeit` and `cProfile` to identify bottlenecks.

---

Optimize your Python code with this cheat sheet! 🎉
