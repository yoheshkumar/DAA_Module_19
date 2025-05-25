# EX:1A - Reverse a String
## DATE: 

## AIM:

To write a program to create a recursive function to reverse a string.

## Algorithm
 
1. Base case checking, if the string s is empty (`len(s) < 1 `), return s itself (This is the termination condition of the recursion).
2. Extract the last character of the string using `s[-1]`.
3. Call the same function `rev()` on the remaining string (excluding the last character):  `rev(s[:-1])`.
4. Combine the last character (`s[-1]`) with the result of the recursive call.
5. The function returns the reversed string step by step as the recursive calls unwind.

## Program:

```
# Program to implement Reverse a String

# DEVELOPED BY: YOHESH KUMAR R.M
# REGISTER NUMBER : 212222240118

def rev(s):
    if(len(s)<1):
        return s
    return s[-1]+rev(s[:-1]) 
s=input()
print(rev(s))
```

## Output:

![image](https://github.com/user-attachments/assets/b63d8c56-0dfa-4e82-9ba1-690c422d89c8)


## Result:

The program successfully reverses the input string using recursion. When the user provides an input string, the output displays the reversed version of the string
