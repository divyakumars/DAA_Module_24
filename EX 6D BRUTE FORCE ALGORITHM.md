# EX 6D BRUTE FORCE ALGORITHM
## DATE: 10/05/25

## AIM:
To write a python program using brute force method of searching for the given substring in the main string.


## Algorithm
1. Let l = len(string) and l2 = len(sub).

2. Loop i from 0 to l - l2:

3. If string[i : i + l2] == sub, print Found at index i.

## Program:
To implement the program using brute force method of searching for the given substring in the main string.

Developed by: DIVYA K

Register Number: 212222230035

```
def match(string,sub):
    l=len(string)
    l2=len(sub)
    for i in range(l-l2+1):
        if string[i:i+l2]==sub:
            print("Found at index",i)
str1=input()
str2=input()

```
## Output:
![image](https://github.com/user-attachments/assets/369b14b7-0b75-4421-8944-b3961c3f9e21)


## Result:
Thus the above program was executed successfully for searching the substring at respective index.
