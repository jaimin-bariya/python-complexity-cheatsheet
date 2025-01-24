# Sets Time Complexity Cheat Sheet

Python’s **set** is a hash-based collection optimized for fast membership tests and set operations. This cheat sheet provides the average and worst-case time complexities for common set operations, helping developers write efficient Python code.

---

## 📋 Overview of Set Operations

| **Operation**          | **Examples**             | **Average Case**         | **Worst Case**         |
|-------------------------|--------------------------|---------------------------|-------------------------|
| Add                    | `s.add(item)`           | O(1)                     | O(N)                   |
| Clear                  | `s.clear()`             | O(1)                     | O(1)                   |
| Copy                   | `s.copy()`              | O(N)                     | O(N)                   |
| Containment            | `item in s`             | O(1)                     | O(N)                   |
| Creation               | `set(iterable)`         | O(len(iterable))         | O(len(iterable))       |
| Discard                | `s.discard(item)`       | O(1)                     | O(N)                   |
| Difference             | `s1 - s2`               | O(len(s1))               | O(len(s1))             |
| Difference Update      | `s1.difference_update(s2)` | O(len(s2))             | -                       |
| Equality Check         | `s1 == s2`              | O(min(len(s1), len(s2))) | O(min(len(s1), len(s2)))|
| Intersection           | `s1 & s2`               | O(min(len(s1), len(s2))) | O(min(len(s1), len(s2)))|
| Iteration              | `for item in s:`        | O(N)                     | O(N)                   |
| Is Subset              | `s1 <= s2`              | O(len(s1))               | O(len(s1))             |
| Is Superset            | `s1 >= s2`              | O(len(s2))               | O(len(s2))             |
| Pop                    | `s.pop()`               | O(1)                     | O(N)                   |
| Union                  | `s1 | s2`               | O(len(s1) + len(s2))     | -                       |
| Symmetric Difference   | `s1 ^ s2`               | O(len(s1))               | O(len(s1) * len(s2))   |

---

## 💡 Key Notes:

1. **Hash-Based Structure**:
   - Sets in Python use a hash table, enabling O(1) average complexity for operations like `add`, `discard`, and membership tests (`item in s`).

2. **Worst Case Scenarios**:
   - Hash collisions or resizing during operations can degrade performance to O(N).

3. **Set Operations**:
   - Operations like union (`|`), intersection (`&`), and difference (`-`) depend on the sizes of the sets involved.

4. **Pop Behavior**:
   - The `pop()` method removes and returns an arbitrary element from the set. If the set is empty, it raises a `KeyError`.

---

## 📖 Example Usage

```python
# Example: Add and Membership Test
my_set = {1, 2, 3}
my_set.add(4)            # O(1)
print(4 in my_set)       # True (O(1))

# Example: Union and Intersection
set1 = {1, 2, 3}
set2 = {3, 4, 5}
union_set = set1 | set2  # O(len(set1) + len(set2))
print(union_set)         # Output: {1, 2, 3, 4, 5}

intersection_set = set1 & set2  # O(min(len(set1), len(set2)))
print(intersection_set)         # Output: {3}
```

---

## 📥 When to Use Sets?
- Use sets for **fast membership checks**, **removing duplicates**, and performing **set operations** like union, intersection, and difference.
- Avoid sets when **order** or **duplicate values** are required (use lists or dictionaries instead).

---

Explore the [Complexity Overview](complexity_overview.md) for comparisons across all data structures!
