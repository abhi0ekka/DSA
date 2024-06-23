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
<img src="https://github.com/abhi0ekka/DSA/blob/master/image-used/pascal.jpg" width="500" height="450" /><br/>
## nCr formula : General and Advanced way
```c++
#include <iostream>
using namespace std;

int fact(int);
int fact(int n)
{
  if(n<=0)
    return 1;
  return n* fact(n-1);
}

int normal_ncr(int n,int r)
{
  int num,den;
  num= fact(n);
  den= fact(r)* fact(n-r);
  return num/den;
}

int advance_ncr(int n,int r)
{
  if(n==r||r==0)
    return 1;
  return advance_ncr(n-1,r-1)+ advance_ncr(n-1,r);
}

int main()
{
  cout<<normal_ncr(3,2)<<endl;
  cout<<advance_ncr(3,2);
}
```
# Tower Of Hanoi Problem :<br/>
![image](https://github.com/abhi0ekka/DSA/assets/75915784/80ac9a66-f21a-4417-92e4-a5bb60d37937)<br/>
## Code for Tower Of Hanoi Problem:<br/>
```c++
#include <iostream>
#include <stdio.h>
using namespace std;

void TOH(int , char, char, char);

int main()
{
  TOH(2,'A','B','C');
}
void TOH(int x, char a, char b, char c)
{
  if(x>0)
  {
    TOH(x-1,a,c,b);
    printf("%c to %c\n",a,c);
    TOH(x-1,b,a,c);
  }
}
```
## Recursion Call of the Tower Of Hanoi
<img src="https://github.com/abhi0ekka/DSA/blob/master/image-used/Recursion-flow.jpg" width="1000" height="500" /><br/>

