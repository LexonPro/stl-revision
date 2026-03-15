# C++ STL — Algorithms

STL provides many **built-in algorithms** to perform operations on containers like vector, array, etc.

Algorithms help to **reduce code and increase efficiency**.

Most algorithms are defined in the header:

```cpp
#include <algorithm>
```

---

# Common STL Algorithms

| Algorithm       | Purpose                     |
| --------------- | --------------------------- |
| sort()          | Sort elements               |
| reverse()       | Reverse order               |
| find()          | Search element              |
| binary_search() | Fast search in sorted array |
| count()         | Count occurrences           |
| max_element()   | Find maximum element        |
| min_element()   | Find minimum element        |
| swap()          | Swap values                 |

---

# sort()

Sorts elements in **ascending order**.

```cpp
sort(v.begin(), v.end());
```

Example

```cpp
#include <iostream>
#include <vector>
#include <algorithm>
using namespace std;

int main()
{
    vector<int> v = {5,2,8,1};

    sort(v.begin(), v.end());

    for(int x : v)
        cout<<x<<" ";
}
```

Output

```text
1 2 5 8
```

---

# reverse()

Reverses the elements.

```cpp
reverse(v.begin(), v.end());
```

Example

```text
Input
1 2 3 4

Output
4 3 2 1
```

---

# find()

Searches an element in container.

```cpp
find(v.begin(), v.end(), value);
```

Example

```cpp
auto it = find(v.begin(), v.end(), 10);

if(it != v.end())
    cout<<"Found";
```

---

# binary_search()

Works only on **sorted containers**.

```cpp
binary_search(v.begin(), v.end(), 10);
```

Returns

```text
true  → element exists
false → element not found
```

---

# count()

Counts occurrences of an element.

```cpp
count(v.begin(), v.end(), value);
```

Example

```cpp
vector<int> v = {1,2,2,3};

cout << count(v.begin(), v.end(), 2);
```

Output

```text
2
```

---

# max_element()

Finds maximum element.

```cpp
max_element(v.begin(), v.end());
```

Example

```cpp
cout << *max_element(v.begin(), v.end());
```

---

# min_element()

Finds minimum element.

```cpp
min_element(v.begin(), v.end());
```

Example

```cpp
cout << *min_element(v.begin(), v.end());
```

---

# swap()

Swaps two values.

```cpp
swap(a,b);
```

Example

```cpp
int a = 5;
int b = 10;

swap(a,b);
```

Result

```text
a = 10
b = 5
```

---

# Complete Example Program

```cpp
#include <iostream>
#include <vector>
#include <algorithm>
using namespace std;

int main()
{
    vector<int> v = {5,3,8,1};

    sort(v.begin(), v.end());

    cout<<"Sorted: ";

    for(int x : v)
        cout<<x<<" ";

    cout<<"\nMax element: "<< *max_element(v.begin(), v.end());

    cout<<"\nMin element: "<< *min_element(v.begin(), v.end());

    return 0;
}
```

Output

```text
Sorted: 1 3 5 8
Max element: 8
Min element: 1
```

---

# Time Complexity

| Algorithm     | Complexity |
| ------------- | ---------- |
| sort          | O(n log n) |
| binary_search | O(log n)   |
| find          | O(n)       |
| count         | O(n)       |

---

# Quick Revision

Most used algorithms

```text
sort()
reverse()
find()
binary_search()
count()
max_element()
min_element()
swap()
```

---

# STL Learning Summary

STL containers studied:

```text
1 Vector
2 Pair
3 Stack
4 Queue
5 Set
6 Map
7 Algorithms
```

These form the **core STL used in competitive programming and software development**.
