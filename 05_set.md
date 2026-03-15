# C++ STL — Set

A **set** is an associative container that stores **unique elements in sorted order**.

Properties of set:

• Elements are **automatically sorted**
• **Duplicate elements are not allowed**
• Implemented internally using a **balanced binary search tree**

---

# Header File

```cpp id="set1"
#include <set>
```

---

# Declaration

```cpp id="set2"
set<int> s;
```

Other examples

```cpp id="set3"
set<string> names;
set<char> letters;
```

---

# Example of Set Behavior

Input

```text id="set4"
5 3 1 3 2
```

Stored in set

```text id="set5"
1 2 3 5
```

Duplicates removed and elements sorted.

---

# Important Functions

| Function  | Purpose                 |
| --------- | ----------------------- |
| insert(x) | Add element             |
| erase(x)  | Remove element          |
| find(x)   | Search element          |
| count(x)  | Check if element exists |
| size()    | Number of elements      |
| empty()   | Check if set is empty   |

---

# insert()

Adds an element to the set.

```cpp id="set6"
s.insert(10);
s.insert(20);
s.insert(30);
```

Set becomes

```text id="set7"
10 20 30
```

If duplicate inserted

```cpp id="set8"
s.insert(20);
```

Result

```text id="set9"
10 20 30
```

Duplicate ignored.

---

# erase()

Removes an element.

```cpp id="set10"
s.erase(20);
```

Example

```text id="set11"
Before

10 20 30

After

10 30
```

---

# find()

Searches an element.

```cpp id="set12"
s.find(10);
```

Returns **iterator** if found.

Example

```cpp id="set13"
if(s.find(10) != s.end())
    cout<<"Element found";
```

---

# count()

Checks whether an element exists.

```cpp id="set14"
s.count(10);
```

Returns

```text id="set15"
1 → element exists
0 → element does not exist
```

---

# size()

Returns number of elements.

```cpp id="set16"
cout << s.size();
```

Example

```text id="set17"
Set = 10 20 30
Size = 3
```

---

# Iterating Through Set

Using range loop

```cpp id="set18"
for(int x : s)
    cout<<x<<" ";
```

Output

```text id="set19"
10 20 30
```

---

# Complete Example Program

```cpp id="set20"
#include <iostream>
#include <set>
using namespace std;

int main()
{
    set<int> s;

    s.insert(10);
    s.insert(20);
    s.insert(10);
    s.insert(30);

    for(int x : s)
        cout<<x<<" ";

    cout<<"\nSize: "<<s.size();

    return 0;
}
```

Output

```text id="set21"
10 20 30
Size: 3
```

---

# Time Complexity

| Operation | Complexity |
| --------- | ---------- |
| insert    | O(log n)   |
| erase     | O(log n)   |
| find      | O(log n)   |

---

# Quick Revision

Set = **Sorted + Unique elements**

Important functions

```text id="set22"
insert()
erase()
find()
count()
size()
```

---

# Next Topic

```text id="set23"
06_map.md
```
