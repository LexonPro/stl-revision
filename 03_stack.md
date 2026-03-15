# C++ STL — Stack

A **stack** is a container adapter that follows the principle:

**LIFO (Last In First Out)**

This means the **last element inserted is the first one removed**.

Example:

```text id="stkex1"
Push order: 1 2 3 4

Stack structure:

4  ← top
3
2
1
```

Element **4** will be removed first.

---

# Header File

```cpp id="stkhd1"
#include <stack>
```

---

# Declaration

```cpp id="stkdec1"
stack<int> s;
```

Other examples

```cpp id="stkdec2"
stack<string> names;
stack<char> letters;
```

---

# Important Functions

| Function | Purpose                 |
| -------- | ----------------------- |
| push(x)  | Insert element          |
| pop()    | Remove top element      |
| top()    | Access top element      |
| size()   | Number of elements      |
| empty()  | Check if stack is empty |

---

# push()

Adds an element to the top of the stack.

```cpp id="stkpush1"
s.push(10);
s.push(20);
s.push(30);
```

Stack becomes

```text id="stkpush2"
30 ← top
20
10
```

---

# pop()

Removes the top element.

```cpp id="stkpop1"
s.pop();
```

Example

```text id="stkpop2"
Before
30 ← top
20
10

After
20 ← top
10
```

---

# top()

Returns the top element.

```cpp id="stktop1"
cout << s.top();
```

Output

```text id="stktop2"
30
```

---

# size()

Returns number of elements.

```cpp id="stksize1"
cout << s.size();
```

Example

```text id="stksize2"
Stack = 10 20 30
Size = 3
```

---

# empty()

Checks if stack is empty.

```cpp id="stkemp1"
s.empty();
```

Returns

```text id="stkemp2"
true  → stack empty
false → stack not empty
```

Example

```cpp id="stkemp3"
if(s.empty())
    cout<<"Stack is empty";
```

---

# Complete Example Program

```cpp id="stkprog1"
#include <iostream>
#include <stack>
using namespace std;

int main()
{
    stack<int> s;

    s.push(10);
    s.push(20);
    s.push(30);

    cout<<"Top element: "<<s.top()<<endl;

    s.pop();

    cout<<"After pop: "<<s.top()<<endl;

    cout<<"Size: "<<s.size()<<endl;

    return 0;
}
```

Output

```text id="stkprog2"
Top element: 30
After pop: 20
Size: 2
```

---

# Applications of Stack

Stacks are used in many real-world problems.

Common uses:

• Expression evaluation
• Parenthesis checking
• Undo/redo operations
• Function call management (call stack)
• Depth First Search (DFS)

---

# Time Complexity

| Operation | Complexity |
| --------- | ---------- |
| push      | O(1)       |
| pop       | O(1)       |
| top       | O(1)       |

---

# Quick Revision

Stack follows

```text id="stkrev1"
LIFO (Last In First Out)
```

Important functions

```text id="stkrev2"
push()
pop()
top()
size()
empty()
```

---

# Next Topic

```text id="stkrev3"
04_queue.md
```
