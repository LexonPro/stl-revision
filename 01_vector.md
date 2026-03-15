\# C++ STL — Vector



Vector is a \*\*dynamic array\*\* provided by STL.

Unlike normal arrays, vectors \*\*automatically resize\*\* when elements are added or removed.



---



\# Header



```cpp

\#include <vector>

```



---



\# Declaration



```cpp

vector<int> v;

```



Other examples



```cpp

vector<string> names;

vector<double> marks;

```



---



\# Initialization



```cpp

vector<int> v = {10,20,30};

```



Fixed size



```cpp

vector<int> v(5);

```



Output



```

0 0 0 0 0

```



Same values



```cpp

vector<int> v(5,10);

```



Output



```

10 10 10 10 10

```



---



\# Important Functions



| Function    | Purpose             |

| ----------- | ------------------- |

| push\_back() | Add element         |

| pop\_back()  | Remove last element |

| size()      | Number of elements  |

| empty()     | Check if empty      |

| clear()     | Remove all elements |

| insert()    | Insert element      |

| erase()     | Delete element      |



---



\# Example



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



&nbsp;   for(int x : v)

&nbsp;       cout<<x<<" ";

}

```



Output



```

10 20 30

```



