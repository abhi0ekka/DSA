# C++ DSA Journey
## Recursion 
### Types of Recursion
1. Tail Recursion
2. Head Recursion
3. Tree Recursion
4. In-direct Recursion
5. Nested Recursion

# Excessive recursion
 * When same function is called for multiple time is called excessive recursion.<br />
 * Like for example for the code of fibonacci calls same function for multiple times.<br />
 * the Fibonacci code can be optimised using the Array.<br />
 * And the method is called as "MEMOZATION"<br />
```c++
#include <iostream>
using namespace std;

int arr[10];

int fib(int);

int main()
{
  for(int i=0;i<10;i++)
    arr[i]=-1;

  cout<<fib(6);

}

int fib(int x)
{
  if(x<=1)
  {
    arr[x]=x;
    return x;
  }
  else
  {
    if(arr[x-2]==-1)
      arr[x-2]=fib(x-2);
    if(arr[x-1]==-1)
      arr[x-1]=fib(x-1);

    return arr[x-2]+arr[x-1];
  }

}
```
# Pascal's Triangle

<img src="https://github.com/abhi0ekka/DSA/blob/master/image-used/pascal.jpg" width="500" height="450" />
