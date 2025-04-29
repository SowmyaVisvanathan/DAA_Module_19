# EX 1A Sum of a Sequence
## DATE: 22/02/2025
## AIM:
Write a Python Program Using a recursive function to calculate the sum of a sequence
## Algorithm
- Start
- Input an integer num
- Define a function recursive_sum(n):
- If n == 0, return 0 (base case)
- Otherwise, return n + recursive_sum(n - 1) (recursive call)
- Call recursive_sum(num) and store the result in result
- Output the value of result
- End

## Program:
```
/*
Program to implement Reverse a String
Developed by: Sowmya V
Register Number: 212222110045
*/

def recursive_sum(n):
    if n == 0:
        return 0
    return n + recursive_sum(n - 1)
num = int(input())
result = recursive_sum(num)
print(result)
```

## Output:
![image](https://github.com/user-attachments/assets/a3c7c6af-d94a-42e9-9585-afef839aa8e6)

## Result:
The program successfully calculates the sum of the first n natural numbers using a recursive function. When a user enters a positive integer, the program computes the sum from 1 to n by recursively adding each number, and then displays the final total as output.
