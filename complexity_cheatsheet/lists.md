# Lists Time Complexity Cheat Sheet

Python’s **list** is a versatile, ordered, and mutable sequence. This cheat sheet provides the average and worst-case time complexities for common list operations, helping developers write optimized and efficient Python code.

---

## 📋 Overview of List Operations

| **Operation**       | **Examples**         | **Average Case** | **Worst Case**    |
|----------------------|----------------------|-------------------|-------------------|
| Append              | `l.append(item)`    | O(1)             | O(1) (resize)     |
| Clear               | `l.clear()`         | O(1)             | O(1)             |
| Containment         | `item in l`         | O(N)             | O(N)             |
| Copy                | `l.copy()`          | O(N)             | O(N)             |
| Delete by Index     | `del l[i]`          | O(N)             | O(N)             |
| Extend              | `l.extend(another)` | O(N)             | O(N)             |
| Equality Check      | `l1 == l2`          | O(N)             | O(N)             |
| Indexing            | `l[i]`              | O(1)             | O(1)             |
| Iteration           | `for item in l:`    | O(N)             | O(N)             |
| Length              | `len(l)`            | O(1)             | O(1)             |
| Multiplication      | `k * l`             | O(k * N)         | O(k * N)         |
| Min/Max             | `min(l), max(l)`    | O(N)             | O(N)             |
| Pop from End        | `l.pop(-1)`         | O(1)             | O(1)             |
| Pop Intermediate    | `l.pop(i)`          | O(N)             | O(N)             |
| Remove              | `l.remove(x)`       | O(N)             | O(N)             |
| Reverse             | `l.reverse()`       | O(N)             | O(N)             |
| Slicing             | `l[x:y]`            | O(y - x)         | O(y - x)         |
| Sort                | `l.sort()`          | O(N log N)       | O(N log N)       |
| Store by Index      | `l[i] = x`          | O(1)             | O(1)             |

---

## 💡 Key Notes:

1. **Dynamic Resizing**:
   - Lists are implemented as dynamic arrays in Python. When a list exceeds its allocated memory, it resizes by allocating more memory, leading to an **amortized O(1)** complexity for append operations.

2. **Indexing and Slicing**:
   - Accessing or slicing a list uses **direct indexing**, making operations like `l[i]` O(1) and slicing `l[x:y]` proportional to the slice length (O(y-x)).

3. **Sorting**:
   - Python’s `list.sort()` uses the Timsort algorithm, which has a complexity of **O(N log N)** in the average and worst cases.

4. **Common Pitfall**:
   - Using operations like `x in l` for containment checks on large lists can be inefficient (O(N)). Consider using sets for such scenarios (O(1) containment).

---

## 📖 Example Usage

```python
# Example: Append and Sort
my_list = [3, 1, 4, 1]
my_list.append(5)        # O(1)
my_list.sort()           # O(N log N)
print(my_list)           # Output: [1, 1, 3, 4, 5]

# Example: Slicing
sub_list = my_list[1:3]  # O(2), as slice length is 2
print(sub_list)          # Output: [1, 3]
```

---

## 📥 When to Use Lists?
- Use lists when you need **ordered**, **mutable** sequences with frequent appends, indexing, or slicing.
- For **faster membership checks** or **unique elements**, consider using **sets**.

---

Explore the [Complexity Overview](complexity_overview.md) for comparisons across all data structures!
