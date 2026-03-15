# C++ STL — Pair

`pair` is an STL utility that **stores two values together as a single unit**.

It is useful when we want to keep **two related values together** such as:

```text
Roll → Marks
Coordinates → (x , y)
Key → Value
```

Example:

```text
(1 , 90)
(2 , 85)
```

---

# Header File

```cpp
#include <utility>
```

---

# Declaration

```cpp
pair<int,int> p;
```

This pair stores **two integers**.

Other examples

```cpp
pair<int,string> student;
pair<char,double> data;
```

---

# Initialization

### Method 1 — Direct Initialization

```cpp
pair<int,int> p = {10,20};
```

---

### Method 2 — make_pair()

```cpp
pair<int,int> p = make_pair(10,20);
```

---

# Accessing Elements

A pair has **two members**.

| Member | Meaning      |
| ------ | ------------ |
| first  | first value  |
| second | second value |

Example

```cpp
pair<int,int> p = {10,20};

cout << p.first;
cout << p.second;
```

Output

```text
10
20
```

---

# Example Program

```cpp
#include <iostream>
#include <utility>
using namespace std;

int main()
{
    pair<int,int> p = {5,10};

    cout << "First value: " << p.first << endl;
    cout << "Second value: " << p.second << endl;

    return 0;
}
```

Output

```text
First value: 5
Second value: 10
```

---

# Pair Inside Vector

Pairs are often used with vectors.

Example:

```cpp
vector<pair<int,int>> v;
```

This means a vector storing pairs.

Example program:

```cpp
#include <iostream>
#include <vector>
using namespace std;

int main()
{
    vector<pair<int,int>> v;

    v.push_back({1,100});
    v.push_back({2,200});
    v.push_back({3,300});

    for(auto x : v)
        cout << x.first << " " << x.second << endl;
}
```

Output

```text
1 100
2 200
3 300
```

---

# Nested Pair

Pairs can also contain another pair.

```cpp
pair<int, pair<int,int>> p;
```

Example

```cpp
pair<int, pair<int,int>> p = {1,{10,20}};
```

Access

```cpp
p.first
p.second.first
p.second.second
```

---

# Time Complexity

| Operation           | Complexity |
| ------------------- | ---------- |
| Access first/second | O(1)       |
| Creation            | O(1)       |

---

# Quick Revision

`pair` = **stores two values together**

Important members

```text
first
second
make_pair()
```

Example

```cpp
pair<int,int> p = {10,20};
```

---

# Next Topic

```text
03_stack.md
```
