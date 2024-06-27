# Array Abstract Data Type

## Display

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

## Add()/append()

- We just take the last index and assign the element.

## insert(intex,x)

- Just take a loop from the last index.
- And start copying the element of previous element.

```c++
    for(i=last;i>index;i++)
        a[i]=a[i-1];
    a[index]=x;
```
