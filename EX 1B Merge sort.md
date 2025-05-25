# EX:1B - Merge Sort
## DATE:

## AIM:

To write a python program to sort the first half of the list using merge sort.

## Algorithm:

1. Divide the array, if the array has more than one element (`l < r`), divide it into two halves then find the midpoint `m = l + (r - l) // 2`.
2. Recursively sort the right half: `mergeSort(arr, m+1, r)`.Then merge the sorted subarrays using the `merge()` function.
3. Inside the `merge()` function, copy elements from the subarrays (L and R) to temporary arrays.
4. Merge by comparing elements from both halves. Copy the smaller one into the original array `arr`.
5. Once one of the subarrays is exhausted, copy the remaining elements from the other subarray to `arr`.

## Program:
```
# Program to implement Merge Sort

# DEVELOPED BY: YOHESH KUMAR R.M
# REGISTER NUMBER : 212222240118

def merge(arr,l, m,r):
    n1 = m - l + 1
    n2 = r - m
    L = [0] * (n1)
    R = [0] * (n2)
    for i in range(0, n1):
        L[i] = arr[l + i]
 
    for j in range(0, n2):
        R[j] = arr[m + 1 + j]
 
    i = 0 
    j = 0 
    k = l    
    while i < n1 and j < n2:
        if L[i] <= R[j]:
            arr[k] = L[i]
            i += 1
        else:
            arr[k] = R[j]
            j += 1
        k += 1
    arr[k:]=L[i:]+R[j:]
def mergeSort(arr, l, r):
    if l < r:
        m = l+(r-l)//2
        mergeSort(arr, m+1, r)
        merge(arr,l,m,r)
arr =[]               #[12, 11, 13, 5, 6, 7]
n =int(input())
for i in range(n):
    arr.append(int(input()))
print("Given array is")
for i in range(n):
    print("%d" % arr[i],end=" ")
mergeSort(arr, 0, n-1)
print("\n\nSorted array is")
for i in range(n):
    print("%d" % arr[i],end=" ")
 
```


## Output:

![image](https://github.com/user-attachments/assets/26660a96-f157-4127-a843-5fdfa658872d)


## Result:

The program successfully sorts the first half of the given array using merge sort. where only the first half is sorted, and the second half remains unchanged.
