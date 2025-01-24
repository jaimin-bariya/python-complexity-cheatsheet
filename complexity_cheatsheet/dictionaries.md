# Dictionaries Time Complexity Cheat Sheet

Python’s **dictionary** is a hash table-based collection designed for fast key-value lookups. This cheat sheet provides the average and worst-case time complexities for common dictionary operations, helping developers optimize their Python code.

---

## 📋 Overview of Dictionary Operations

| **Operation**         | **Examples**            | **Average Case** | **Worst Case** |
|------------------------|-------------------------|-------------------|----------------|
| Clear                 | `d.clear()`            | O(1)             | O(1)          |
| Construction          | `dict(...)`            | O(len(d))        | O(len(d))     |
| Delete by Key         | `del d[k]`             | O(1)             | O(N)          |
| Get Value by Key      | `d.get(k)`             | O(1)             | O(N)          |
| Iteration (keys, vals, items) | `for k in d:`     | O(N)             | O(N)          |
| Length                | `len(d)`               | O(1)             | O(1)          |
| Pop by Key            | `d.pop(k)`             | O(1)             | O(N)          |
| Pop Item              | `d.popitem()`          | O(1)             | O(1)          |
| Returning Views       | `d.values()`           | O(1)             | O(1)          |
| Returning Keys        | `d.keys()`             | O(1)             | O(1)          |
| Set Default           | `d.setdefault(k, v)`   | O(1)             | O(N)          |
| Update                | `d.update({...})`      | O(len(update))   | O(len(update))|

---

## 💡 Key Notes:

1. **Hash-Based Structure**:
   - Dictionaries in Python are implemented as **hash tables**, enabling average O(1) complexity for key-based operations like `d[k]` or `d.get(k)`.

2. **Worst Case Scenarios**:
   - Rare collisions in hash functions or large deletions can lead to O(N) operations.

3. **Iteration**:
   - Iterating over keys, values, or items is O(N), where N is the size of the dictionary.

4. **Pop and Popitem**:
   - `d.pop(k)` removes a specific key and its value, while `d.popitem()` removes an arbitrary key-value pair (LIFO order).

---

## 📖 Example Usage

```python
# Example: Adding and Retrieving Values
my_dict = {"a": 1, "b": 2, "c": 3}
my_dict["d"] = 4       # O(1)
value = my_dict["a"]    # O(1)

# Example: Iteration
for key, value in my_dict.items():  # O(N)
    print(f"{key}: {value}")

# Example: Pop Operations
popped_value = my_dict.pop("b")    # O(1)
print(my_dict)                      # Output: {"a": 1, "c": 3, "d": 4}
```

---

## 📥 When to Use Dictionaries?
- Use dictionaries for **fast lookups**, **insertion**, and **deletion** by key.
- Avoid using dictionaries if order is critical (consider `OrderedDict` or Python 3.7+ where `dict` maintains insertion order).

---

Explore the [Complexity Overview](complexity_overview.md) for comparisons across all data structures!
