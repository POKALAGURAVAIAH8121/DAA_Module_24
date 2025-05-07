# EX 6D BRUTE FORCE ALGORITHM
## DATE:
## AIM:
To write a python program using brute force method of searching for the given substring in the main string.

## Algorithm
1. Get the lengths of the main string and the substring.

2. Iterate over the main string, up to the point where the substring can fit.

3. For each position, compare characters of the main string and the substring one by one.

4. If all characters match, report the index where the substring is found.

5. If no match is found after all checks, return -1.


## Program:
```
/*
To implement the program using brute force method of searching for the given substring in the main string.
Developed by: POKALA GURAVAIAH
Register Number:  212222040114
*/
```
```
def match(string,sub):
    l = len(string)
    ls = len(sub)
    start = sub[0]

    ########### Add your code here #######
    for i in range(l-ls+1):
        j=0
        while j<ls and string[i+j]==sub[j]:
            j+=1
        if j==ls:
            print('Found at index',i)
    return -1

str1=input()
str2=input()

```
## Output:
<img width="400" alt="image" src="https://github.com/user-attachments/assets/1456de64-9be8-4b45-ad8a-a15cf9c1d9ec"/>

## Result:
Thus the above program was executed successfully for searching the substring at respective index.
