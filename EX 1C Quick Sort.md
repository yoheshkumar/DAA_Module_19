# EX:1C - Quick Sort
## DATE:

## AIM:
To write a python program to implement quick sort using tha last element as pivot on the list of float values.

## Algorithm

1. The last element of the array (`arr[r]`) is chosen as the pivot. This is done inside the `partition()` function.
2. Rearrange the array so that:
   - Elements less than or equal to the pivot are placed on the left.
   - Elements greater than the pivot are placed on the right.
3. Swap elements during iteration and finally place the pivot in its correct position.
4. Return the partition index `p` where the pivot is finally placed.
5. Recursively apply Quick Sort on the left (`l to p-1`) and right (`p+1 to r`) subarrays.
6. If the subarray has less than or equal to `1` element (`l >= r`), it is already sorted, and recursion stops.
7. After all recursive calls are complete, the array will be sorted in-place.


## Program:
```
# Program to implement implement quick sort using the last element as pivot on the list of float values

# DEVELOPED BY: YOHESH KUMAR R.M
# REGISTER NUMBER : 212222240118

def quickSort(arr,l,r):
    if l<r:
        p=partition(arr,l,r)
        quickSort(arr,l,p-1)
        quickSort(arr,p+1,r)
def partition(arr,l,r):
    pivot=arr[r]
    i=l-1
    for j in range(l,r):
        if arr[j]<=pivot:
            i+=1
            arr[i],arr[j]=arr[j],arr[i]
    arr[i+1],arr[r]=arr[r],arr[i+1]
    return i+1
arr=[]
n=int(input())
for i in range(n):
    arr.append(float(input()))
quickSort(arr,0,n-1)
print("Sorted array is:")
for i in range(n):
    print(arr[i])
```


## Output:

![image](https://github.com/user-attachments/assets/f191cea4-2e72-4a81-a0a9-25352fb59a4d)


## Result:

The program successfully sorts the input array using the QuickSort algorithm, arranging the elements in ascending order.
