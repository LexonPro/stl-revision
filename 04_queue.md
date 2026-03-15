# C++ STL — Queue

A **queue** is a container adapter that follows the principle:

**FIFO (First In First Out)**

This means the **first element inserted is the first one removed**.

Example:

```text id="que1"
Insert order: 10 20 30 40

Queue structure

10 → 20 → 30 → 40
↑              ↑
front          back
```

Element **10** will be removed first.

---

# Header File

```cpp id="que2"
#include <queue>
```

---

# Declaration

```cpp id="que3"
queue<int> q;
```

Other examples

```cpp id="que4"
queue<string> names;
queue<char> letters;
```

---

# Important Functions

| Function | Purpose                 |
| -------- | ----------------------- |
| push(x)  | Insert element          |
| pop()    | Remove front element    |
| front()  | Access first element    |
| back()   | Access last element     |
| size()   | Number of elements      |
| empty()  | Check if queue is empty |

---

# push()

Adds an element at the **back of the queue**.

```cpp id="que5"
q.push(10);
q.push(20);
q.push(30);
```

Queue becomes

```text id="que6"
10 → 20 → 30
↑         ↑
front     back
```

---

# pop()

Removes the **front element**.

```cpp id="que7"
q.pop();
```

Example

```text id="que8"
Before

10 → 20 → 30

After

20 → 30
```

---

# front()

Returns the **first element**.

```cpp id="que9"
cout << q.front();
```

Output

```text id="que10"
10
```

---

# back()

Returns the **last element**.

```cpp id="que11"
cout << q.back();
```

Output

```text id="que12"
30
```

---

# size()

Returns number of elements.

```cpp id="que13"
cout << q.size();
```

Example

```text id="que14"
Queue = 10 20 30
Size = 3
```

---

# empty()

Checks if queue is empty.

```cpp id="que15"
q.empty();
```

Returns

```text id="que16"
true  → queue empty
false → queue not empty
```

Example

```cpp id="que17"
if(q.empty())
    cout<<"Queue empty";
```

---

# Complete Example Program

```cpp id="que18"
#include <iostream>
#include <queue>
using namespace std;

int main()
{
    queue<int> q;

    q.push(10);
    q.push(20);
    q.push(30);

    cout<<"Front element: "<<q.front()<<endl;
    cout<<"Back element: "<<q.back()<<endl;

    q.pop();

    cout<<"After pop, new front: "<<q.front()<<endl;

    cout<<"Size: "<<q.size()<<endl;

    return 0;
}
```

Output

```text id="que19"
Front element: 10
Back element: 30
After pop, new front: 20
Size: 2
```

---

# Applications of Queue

Queues are widely used in many systems.

Common uses:

• CPU scheduling
• Printer queue
• Breadth First Search (BFS)
• Handling requests in servers
• Task scheduling

---

# Time Complexity

| Operation | Complexity |
| --------- | ---------- |
| push      | O(1)       |
| pop       | O(1)       |
| front     | O(1)       |
| back      | O(1)       |

---

# Quick Revision

Queue follows

```text id="que20"
FIFO (First In First Out)
```

Important functions

```text id="que21"
push()
pop()
front()
back()
size()
empty()
```

---

# Next Topic

```text id="que22"
05_set.md
```
