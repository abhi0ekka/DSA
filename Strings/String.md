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