# Strings :

- Basic of the Strings are in the Copy.

# char-String length :

- We know that in the char-string the last element is '\0'.
- So, to find the length of the string.
- we linearly scan the char array till we find the '\0'.
- after getting the value we breakthrough as that will be the length of the string.

```c++
#include <iostream>
using namespace std;

int main()
{
    char name[10];
    int i;
    cout << "Enter a word" << endl;
    cin >> name;
    for (i = 0; name[i] != '\0'; i++)
        ;
    cout << i;
}
```

- and this can be confirmed by the above code.

# To inverse its Case :

- Suppose it is given a string.
- So, we have to change each case.
- lower_case --> upper_case
- upper_case --> lower_case

```c++
#include <iostream>
using namespace std;

int length(char arr[]);
void toLowerCase(char arr[], int);

int main()
{
    char arr[10];
    cout << "Enter the String :" << endl;
    cin >> arr;
    cout << "Length is : " << length(arr) << endl;
    toLowerCase(arr, length(arr));
    cout << "In InverseCASE : " << arr << endl;
}

void toLowerCase(char arr[], int size)
{
    for (int i = 0; i < size; i++)
    {
        if (arr[i] >= 65 && arr[i] <= 90)
            arr[i] += 32;
        else if (arr[i] >= 97 && arr[i] <= 122)
            arr[i] -= 32;
    }
}

int length(char arr[])
{
    int i = -1;
    for (i = 0; arr[i] != '\0'; i++)
    {
    }
    return i;
}
```

# Reverse the String :

- Reversing a String can be done in various way :
  - 1. By using another Array (simple asf).
  - 2. By using swap-two-pointer.

```c++
#include <iostream>
using namespace std;

void swap(char arr[], int);

int main()
{
    char name[] = "abhishek";
    int s = sizeof(name) / sizeof(name[0]);
    cout << "Before funcion call : " << name << endl;
    swap(name, s);
    cout << "After function call : " << name;
}

void swap(char arr[], int size)
{
    int i, j = size - 2;                   //Here we divided by two becuause last element is '\0'.
    for (i = 0; i < j; i++, j--)
    {
        char temp = arr[i];
        arr[i] = arr[j];
        arr[j] = temp;
    }
}
```

- if you do not divide the by 2 then.
- it will not normally print the char-string.
- we have to use the array.

# Palindome and String comparison :

- we just have to compare each element one by one.
- For palindrome we can use 2 approach.
  - 1. To reverse and compare the strings.
  - 2. Just compare the elements of the strings (using two pointers).

# Finding Duplicate element of the array :

- It is same as to find the duplicate element in the array.
- The ways are :
  - 1. Linear Comparing each element with the remaining element.
  - 2. Using hash Table.
  - 3. Using bitWise.

# BitWise :

- 1. Checking a bit is on or not is called masking.
  - It is done by the use of Bit_AND operator.
- 2. Turning a bit on is called as merging.
  - It is done by the use of Bit_OR operator.
- Note : BitWise operator are call by not call by reference they are call by value.
  - So, if want to make any changes we have to store it.
  - We cannot count how many times it is repeated.
  - as bitwise is similar to hashing but in hasing we can increase a individual element.
  - but in memeory we cant as it is only 0s and 1s.

```c++
#include <iostream>
using namespace std;

void duplicate(char word[]);

int main()
{
    char word[100];
    cin >> word;
    duplicate(word);
}

void duplicate(char word[])
{
    int H = 0;
    for (int i = 0; word[i] != '\0'; i++)
    {
        int a = 1;
        a = a << (word[i] - 97);
        if ((a & H) > 0)
            cout << word[i];
        else
            H = a | H;
    }
}
```

# Anagram :

- In this we compare element of two strings.
- Means String2 should be made of of String1.

# Permutation of String :

- In this we have to find all the possible combination of a string.
- This can be obtained by using :
  - 1. Loop.
  - 2. recursion.

![alt text](https://miro.medium.com/v2/resize:fit:1024/format:webp/1*QBEePGu2SigGcbMeMqwTbA.png)
