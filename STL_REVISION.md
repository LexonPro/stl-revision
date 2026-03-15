\# C++ STL Revision — 01 Vector



Vector is the \*\*most commonly used container in C++ STL\*\*.

It works like a \*\*dynamic array\*\*, meaning its size can \*\*grow or shrink automatically\*\*.



Unlike normal arrays, vectors \*\*manage memory automatically\*\* and provide many built-in functions.



---



\# 1. Header File



```cpp

\#include <vector>

```



---



\# 2. Declaration



```cpp

vector<int> v;

```



Vector storing integers.



Other examples:



```cpp

vector<string> names;

vector<double> marks;

vector<char> letters;

```



---



\# 3. Initialization



\### Empty Vector



```cpp

vector<int> v;

```



\### With Values



```cpp

vector<int> v = {10,20,30,40};

```



\### With Fixed Size



```cpp

vector<int> v(5);

```



Creates



```

0 0 0 0 0

```



\### With Same Value



```cpp

vector<int> v(5,10);

```



Creates



```

10 10 10 10 10

```



---



\# 4. Adding Elements



\### push\_back()



Adds element at end.



```cpp

vector<int> v;



v.push\_back(10);

v.push\_back(20);

v.push\_back(30);

```



Vector becomes



```

10 20 30

```



Example program



```cpp

\#include <iostream>

\#include <vector>

using namespace std;



int main()

{

&nbsp;   vector<int> v;



&nbsp;   v.push\_back(5);

&nbsp;   v.push\_back(10);

&nbsp;   v.push\_back(15);



&nbsp;   for(int x : v)

&nbsp;       cout << x << " ";

}

```



Output



```

5 10 15

```



---



\# 5. Removing Elements



\### pop\_back()



Removes last element.



```cpp

v.pop\_back();

```



Example



```

Before: 10 20 30

After : 10 20

```



---



\# 6. Accessing Elements



\### Using Index



```cpp

v\[0]

v\[1]

v\[2]

```



Example



```cpp

cout << v\[1];

```



Output



```

20

```



---



\### Using at()



Safer method.



```cpp

v.at(2)

```



If index is invalid → program throws error.



---



\# 7. Vector Size



\### size()



Returns number of elements.



```cpp

cout << v.size();

```



Example



```

Vector = 10 20 30

Size = 3

```



---



\# 8. Checking Empty



\### empty()



```cpp

v.empty()

```



Returns



```

true  → vector empty

false → vector not empty

```



Example



```cpp

if(v.empty())

&nbsp;   cout<<"Vector empty";

```



---



\# 9. Clearing Vector



\### clear()



Removes all elements.



```cpp

v.clear();

```



Example



```

Before: 10 20 30

After : empty

```



---



\# 10. Iterating Vector



\### Method 1 — For Loop



```cpp

for(int i=0;i<v.size();i++)

&nbsp;   cout<<v\[i];

```



---



\### Method 2 — Range Based Loop



```cpp

for(int x : v)

&nbsp;   cout<<x;

```



---



\### Method 3 — Iterator



```cpp

vector<int>::iterator it;



for(it=v.begin(); it!=v.end(); it++)

&nbsp;   cout<<\*it;

```



---



\# 11. Insert Element



\### insert()



```cpp

v.insert(v.begin()+1,50);

```



Example



```

Vector = 10 20 30



Insert 50 at index 1



Result



10 50 20 30

```



---



\# 12. Erase Element



```cpp

v.erase(v.begin()+2);

```



Example



```

Before



10 20 30 40



After



10 20 40

```



---



\# 13. Complete Example Program



```cpp

\#include <iostream>

\#include <vector>

using namespace std;



int main()

{

&nbsp;   vector<int> v;



&nbsp;   v.push\_back(10);

&nbsp;   v.push\_back(20);

&nbsp;   v.push\_back(30);



&nbsp;   cout<<"Vector elements:\\n";



&nbsp;   for(int x : v)

&nbsp;       cout<<x<<" ";



&nbsp;   cout<<"\\nSize: "<<v.size();



&nbsp;   v.pop\_back();



&nbsp;   cout<<"\\nAfter pop:\\n";



&nbsp;   for(int x : v)

&nbsp;       cout<<x<<" ";

}

```



Output



```

Vector elements

10 20 30



Size: 3



After pop

10 20

```



---



\# 14. Important Properties



• Dynamic size

• Fast random access

• Continuous memory

• Very commonly used in competitive programming



Time Complexity



| Operation | Complexity |

| --------- | ---------- |

| Access    | O(1)       |

| push\_back | O(1)       |

| insert    | O(n)       |

| erase     | O(n)       |



---



\# 15. Quick Revision



Vector = \*\*Dynamic Array\*\*



Most used functions



```

push\_back()

pop\_back()

size()

empty()

clear()

insert()

erase()

```



---



Next STL Topic



```

02 Pair

```



