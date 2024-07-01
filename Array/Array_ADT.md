# Array Abstract Data Type

## 1.Display

- To Display array we have to use a loop from 0 to the last index.

```c++
    for(int i=0;i<arr.len();i++)
        cout<<arr[i];
```

- And we can also use & this method is only used for array.

```c++
    for(int element : arr)
        cout<<element;
```

## 2.Add()/append()

- We just take the last index and assign the element.

## 3.insert(intex,x)

- Just take a loop from the last index.
- And start copying the element of previous element.
- length increase by 1.

```c++
    for(i=last;i>index;i++)
        a[i]=a[i-1];
    a[index]=x;

```

## 4.Deletion(index)

- Start the loop from the index which you want to delete.
- Then just assign the value of the next element.
- length decrease by 1.

```c++
    for(i=0;i<len-1;i++)
        a[i]=a[i+1];
```

## 5.Searching :

### i. Linear Search Method :

- In linear Search Method we compare each index element with the search element.
- It is done one by one and when we found the element we break through the loop.
- It work for both the sorted and un-sorted Arrays.
- It's time complexity is O(n)

#### General Way :

```c++
for(i=0;i<len;i++)
{
    if(arr[i]==sr)
    {
        cout<<"The Number is present"<<endl;
        break;
    }
}
```

#### Improving Linear Search :

- If we talk in a open world way.
- lets say we went to the library then i took a book.
- After reading some pages i put it back to the shelves.
- So, i can conclude that i will need that book again in future as i read only some pages of it.
- So, if we work with the linear search algo it will take the same time.
- if i search for the book again.
- So, to over come this we can do something to make the linear search algo to work faster.
- Method :
  - 1.Transposition:
    - In this we move the book 1 place infront of the last location.
    - So, the next time we seach for the book it will take (n-1) time.
  - 2.Move to Front/Head.
    - In this approach we move the book to the front.
    - So, it can be found directly if we search for it.

### ii. Binary Search :

- Must condition for the binary search algorithm is that Array must be sorted.
- It check for the element by splitting it into 2 parts.
- It can be done in two methods :
- The time complexity for binarySearch is log(n)
  1.Using Loop :
  ```c++
      while(l<=h)
      {
          mid=(l+h)/2;
          if(arr[mid]==sr)
              cout<<"Found";
          if(arr[mid]<sr)
              l=mid+1;
          if(arr[mid]>sr)
              h=mid-1;
      }
  ```
  2.Using Recursion :
  ```c++
    int binarySearch(l,h,sr)
    {
        int mid=(l+h)/2;
        if(l<=h)
            {
                if(arr[mid]==sr)
                    return 1;
                if(sr<arr[mid])
                    return binarySearch(l,mid-1,sr);
                if(sr>arr[mid])
                    return binarySearch(mid+1,h,sr);
            }
        return 0;
    }
  ```

## 6.get(index) :

- This is used to element of a index.

## 7.set(index,x)

- This is used to replace element to a certain index.

## 8.max() :

- To find the maximum element from the array.

## 9.min() :

- To find the minimum element from the arrya.

## 10.sum() :

- To find the sum of the array.

## 11.reverse():

- This can be done in multiple ways:
  - 1.Using another Array and copying from the back.
    - This have a time complexity of o(n).
  - 2.Using swap
    ```c++
    for(i=0;j=len-1;i<j;i++;j--)
    {
        temp=arr[i];
        arr[i]=arr[j];
        arr[j]=temp;
    }
    ```

## 12.left Shift & Rotate:

- For left shift we just move all the element to the left and we loose the first element.
- In rotate all the element are move to the left but we do not loose the first element it is added to the last.
- _This things are quite useful in daily life for example in LED Banner where text move from one side to another._

  ```c++
  #include <iostream>

    using namespace std;

    void leftShift(int arr[], int);

    int main()
    {
        int arr[] = {5, 4, 3, 2, 1};
        int size = sizeof(arr) / sizeof(arr[0]);

        cout << "Before Function Call" << endl;

        for (int element : arr)
            cout << element << " ";
        cout << endl;

    leftShift(arr, size);

    cout << "After Function Call" << endl;
    for (int element : arr)
        cout << element << " ";
    cout << endl;
    }



    void leftShift(int arr[], int size)
    {
        int help = arr[0];
            for (int i = 0; i < size - 1; i++)
                arr[i] = arr[i + 1];
            arr[size - 1] = help;
    }

  ```

## 13.insertInSort() :

- To add element in the sorted array.

```c++
#include <iostream>
using namespace std;

void insert(int arr[], int, int);

int main()
{
    int arr[10] = {1, 2, 3, 4, 6, 7};
    int size = sizeof(arr) / sizeof(arr[0]);
    cout << "Before the Function Call" << endl;
    for (int element : arr)
        cout << element << " ";
    cout << endl;
    insert(arr, 5, size);
    cout << "After the Function Call" << endl;
    for (int element : arr)
        cout << element << " ";
}

void insert(int arr[], int n, int size)
{
    for (int i = size - 1; i >= 0; i--)
    {
        if (arr[i] != 0)
        {
            if (n < arr[i])
            {
                arr[i + 1] = arr[i];
                continue;
            }
            arr[i + 1] = n;
            break;
        }
    }
}
```

## 14.checkSort() :

- Check weather the entered array is sorted or not.

  ```c++
     #include <iostream>

     using namespace std;

     bool checkSort(int arr[], int);

     int main()
     {

        int arr[] = {1, 2, 3, 4, 5, 6, 7, 7, 8, 1};
        int size = sizeof(arr) / sizeof(arr[0]);
        if (checkSort(arr, size))
            cout << "It is Sorted";
        else
            cout << "It is not Sorted";
     }

     bool checkSort(int arr[], int size)
     {
        for (int i = 0; i < size - 1; i++)
        {
            if (arr[i] > arr[i + 1])
                return false;
        }
        return true;
     }
  ```

# Find Single Missing Element in a Sorted Array :

## For first n-Number :

- Finding the missing element form the first n-Natural Number.
- For Doing this we just have to iterate throught the loop and find the sum.
- Then find the actual sum of the numbers.

### Code as follows :

```c++
//Finding missing number from the first N-Natural Number.
#include <iostream>
using namespace std;

int missingNumber(int arr[], int);

int main()
{
    int arr[] = {1, 2, 3, 4, 5, 6, 7, 8, 10};
    int size = sizeof(arr) / sizeof(arr[0]);
    cout << "The missing number is :" << missingNumber(arr, size);
}

int missingNumber(int arr[], int size)
{
    int f, l, sum = 0, a_sum;
    f = arr[0];
    l = arr[size - 1];
    a_sum = ((size + 1) * (size + 2)) / 2;

    for (int i = 0; i < size; i++)
    {
        sum += arr[i];
    }

    return a_sum - sum;
}
```

## From some number to another :

- In this we find the missing number when it is not starting from 1.
- Logic, is simple we take the element and index difference.
- which is constant till we find the element which is missing.
- then we break through and print that number.

![Array](https://media.geeksforgeeks.org/wp-content/uploads/20240404124326/Array-data-structure-2.webp)<br>

### code as follows :

```c++
// In this we find the missing number in between of the natural number.
#include <iostream> //Header file
using namespace std;

int missingNumber(int arr[], int);

int main()
{
    int arr[] = {6, 7, 8, 9, 10, 11, 12, 13, 15, 16, 17, 18};
    int size = sizeof(arr) / sizeof(arr[0]);
    cout << "The missing number is :" << missingNumber(arr, size);
}

int missingNumber(int arr[], int size)
{
    int diff = arr[0];
    for (int i = 1; i < size; i++)
    {
        if ((arr[i] - i) != diff)
            return diff + i;
    }
    return -1;
}
```

# Find Multiple Missing Element in a Sorted Array :

## 1.In Consecutive Number List:

- In this we simply compare the differnce.
- And for multiple difference we take a while loop.
- till the new difference.

```c++
// To find multiple missing number in a continous sorted array.
#include <iostream>
using namespace std;

void mMissingNumber(int arr[], int);

int main()
{
    int arr[] = {1, 2, 3, 4, 7, 8, 9, 11};
    int size = sizeof(arr) / sizeof(arr[0]);
    mMissingNumber(arr, size);
}

void mMissingNumber(int arr[], int size)
{
    int diff = arr[0];
    for (int i = 0; i < size; i++)
    {
        if (arr[i] - i != diff)
        {
            while (diff < arr[i] - i)
            {
                cout << diff + i << " ";
                diff++;
            }
        }
    }
}
```

# Find duplicate element from the array :

- Just to print out the duplicate element from the given array.

## When the array is sorted :

```c++
#include <iostream>
using namespace std;

void duplicate(int arr[], int);

int main()
{
    int arr[] = {1, 2, 3, 4, 4, 5, 6, 7, 8, 8, 8, 9};
    int size = sizeof(arr) / sizeof(arr[0]);
    duplicate(arr, size);
}

void duplicate(int arr[], int size)
{
    int last_dup = -1;
    for (int i = 0; i < size; i++)
    {
        if (arr[i] == arr[i + 1] && last_dup != arr[i])
        {
            cout << arr[i] << " ";
            last_dup = arr[i];
        }
    }
}
```
