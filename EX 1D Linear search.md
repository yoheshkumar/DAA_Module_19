# EX:1D - Linear search
## DATE:

## AIM:
To write a python program for a search function with parameter list name and the value to be searched using string values.

## Algorithm

1. Accept `n` number of elements from the user and store them in a list List.
2. Read the element `x` to be searched in the list.
3. Iterate through each element `i` in list `A` (i.e., `List`).
4. If any element `i == x`, print "Found" and exit the loop using break.
5. If the loop completes without finding the element (break not triggered), the else block executes and prints "Not Found".

## Program:
```
# Program to implement a search function with parameter list name and the value to be searched using string values

# DEVELOPED BY: YOHESH KUMAR R.M
# REGISTER NUMBER : 212222240118

def search(A,x):
    for i in A:
        if i==x:
            print("Found")
            break
    else:
        print("Not Found")
        
List=[input() for _ in range(int(input()))]
n=input()
```

## Output:

![image](https://github.com/user-attachments/assets/875111cd-10b6-4089-ab97-473603014ba5)


## Result:

The program was executed successfully, and it correctly checks if the input element is present in the list, printing "Found" if the element exists or "Not Found" if it does not.
