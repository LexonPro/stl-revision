# C++ STL — Map

A **map** is an associative container that stores **key–value pairs**.

Each element has:

```text id="mapex1"
key → value
```

Example

```text id="mapex2"
1 → Shikhar
2 → Rahul
3 → Aman
```

Properties of map:

• Keys are **unique**
• Elements are **stored in sorted order by key**
• Implemented using a **balanced binary search tree**

---

# Header File

```cpp id="map1"
#include <map>
```

---

# Declaration

```cpp id="map2"
map<int,string> m;
```

This means

```text id="map3"
Key   → int
Value → string
```

Other examples

```cpp id="map4"
map<int,int> data;
map<string,int> marks;
```

---

# Inserting Elements

### Method 1 — Using Index Operator

```cpp id="map5"
m[1] = "Shikhar";
m[2] = "Rahul";
m[3] = "Aman";
```

Stored as

```text id="map6"
1 → Shikhar
2 → Rahul
3 → Aman
```

---

### Method 2 — Using insert()

```cpp id="map7"
m.insert({4,"Ravi"});
```

---

# Accessing Elements

```cpp id="map8"
cout << m[1];
```

Output

```text id="map9"
Shikhar
```

---

# Important Functions

| Function | Purpose               |
| -------- | --------------------- |
| m[key]   | Access value          |
| insert() | Insert key-value pair |
| erase()  | Remove element        |
| find()   | Search key            |
| count()  | Check if key exists   |
| size()   | Number of elements    |

---

# erase()

Removes a key-value pair.

```cpp id="map10"
m.erase(2);
```

Example

```text id="map11"
Before

1 → Shikhar
2 → Rahul
3 → Aman

After

1 → Shikhar
3 → Aman
```

---

# find()

Search for a key.

```cpp id="map12"
m.find(1);
```

Example

```cpp id="map13"
if(m.find(1) != m.end())
    cout<<"Key found";
```

---

# count()

Checks if key exists.

```cpp id="map14"
m.count(1);
```

Returns

```text id="map15"
1 → key exists
0 → key not found
```

---

# Iterating Through Map

```cpp id="map16"
for(auto x : m)
{
    cout<<x.first<<" "<<x.second<<endl;
}
```

Output

```text id="map17"
1 Shikhar
2 Rahul
3 Aman
```

---

# Complete Example Program

```cpp id="map18"
#include <iostream>
#include <map>
using namespace std;

int main()
{
    map<int,string> m;

    m[1] = "Shikhar";
    m[2] = "Rahul";
    m[3] = "Aman";

    for(auto x : m)
        cout<<x.first<<" "<<x.second<<endl;

    return 0;
}
```

Output

```text id="map19"
1 Shikhar
2 Rahul
3 Aman
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

Map = **Key → Value container**

Important functions

```text id="map20"
m[key]
insert()
erase()
find()
count()
size()
```

---

# Next Topic

```text id="map21"
07_algorithms.md
```
