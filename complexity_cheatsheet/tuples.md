# Tuples Time Complexity Cheat Sheet

Python’s **tuple** is an immutable sequence type that is lightweight and ideal for fixed collections of items. This cheat sheet provides the average and worst-case time complexities for common tuple operations, helping developers write efficient Python code.

---

## 📋 Overview of Tuple Operations

| **Operation**          | **Examples**             | **Average Case** | **Worst Case** |
|-------------------------|--------------------------|-------------------|----------------|
| Access by Index        | `t[i]`                  | O(1)             | O(1)          |
| Search                 | `x in t`                | O(N)             | O(N)          |
| Iteration              | `for x in t:`           | O(N)             | O(N)          |
| Slicing                | `t[start:end]`          | O(k)             | O(k)          |
| Concatenation          | `t1 + t2`               | O(len(t1) + len(t2)) | O(len(t1) + len(t2)) |
| Length                 | `len(t)`                | O(1)             | O(1)          |
| Count                  | `t.count(x)`            | O(N)             | O(N)          |
| Index of Element       | `t.index(x)`            | O(N)             | O(N)          |

---

## 💡 Key Notes:

1. **Immutable Structure**:
   - Tuples are immutable, meaning their contents cannot be changed after creation. This makes them lightweight compared to lists.

2. **Fast Access**:
   - Accessing elements by index is O(1) since tuples are stored as contiguous memory blocks.

3. **Iteration and Search**:
   - Operations that involve scanning the tuple (like iteration or membership checks) have a time complexity of O(N), where N is the tuple's length.

4. **Slicing**:
   - Slicing creates a new tuple with a subset of elements. The time complexity is proportional to the size of the slice (k).

---

## 📖 Example Usage

```python
# Example: Access and Search
my_tuple = (10, 20, 30, 40, 50)
element = my_tuple[2]  # O(1)
print(element)          # Output: 30

is_present = 20 in my_tuple  # O(N)
print(is_present)            # Output: True

# Example: Slicing
sub_tuple = my_tuple[1:4]  # O(k)
print(sub_tuple)           # Output: (20, 30, 40)

# Example: Concatenation
tuple1 = (1, 2)
tuple2 = (3, 4)
result = tuple1 + tuple2  # O(len(tuple1) + len(tuple2))
print(result)             # Output: (1, 2, 3, 4)
```

---

## 📥 When to Use Tuples?
- Use tuples when you need **fixed, immutable collections** of items.
- Ideal for use as **keys in dictionaries** or when working with **hash-based collections**.
- Avoid tuples if the data is likely to change (use lists instead).

---

Explore the [Complexity Overview](complexity_overview.md) for comparisons across all data structures!
