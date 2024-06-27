# Array Abstract Data Type

## 1.Display

- To Display array we have to use a loop from 0 to the last index.

```c++
    for(int i=0;i<arr.len();i++)
        cout<<arr[i];
```

- And we can also use & this method is only used for array.

```c++
    for(int i : element)
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
