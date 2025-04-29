# EX 1C Quick Sort
## DATE: 01/03/2025
## AIM:
To write a python program to implement quick sort using tha last element as pivot on the list of float values.

## Algorithm
1. Start
2. Input an integer n (size of the array)
3. Initialize an empty list example
4. Loop from 0 to n-1:
   - Input an integer and append it to example
5. Call quicksort(0, len(example) - 1, example) and print the sorted array
6. Set pivot = nums[r] (last element is the pivot)
7. Initialize ptr = l (pointer for swapping smaller elements)
8. Loop from i = l to r - 1:
   - If nums[i] <= pivot:
   - Swap nums[i] and nums[ptr]
   - Increment ptr
9. After loop, swap nums[ptr] with nums[r] (place pivot in correct position)
10. Print the pivot value (for debugging/trace)
11. Return ptr (partition index)
12. If the list is empty (len(nums) == l), return
13. If l < r:
    - Call partition(l, r, nums) → returns pivot index pi
    - Recursively sort left subarray: quicksort(l, pi - 1, nums)
    - Recursively sort right subarray: quicksort(pi + 1, r, nums)
14. Return the sorted list

## Program:
```
/*
Program to implement implement quick sort using the last element as pivot on the list of float values.
Developed by: Sowmya V
Register Number: 212222110045
*/

def partition(l,r,nums):
    pivot,ptr=nums[r],l
    for i in range(l,r):
        if nums[i]<=pivot:
            nums[i],nums[ptr]=nums[ptr],nums[i]
            ptr+=1
    nums[ptr],nums[r]=nums[r],nums[ptr]
    print("pivot: ",pivot)
    return ptr

def quicksort(l,r,nums):
    if len(nums)==l:
        return nums
    if l<r:
        pi=partition(l,r,nums)
        quicksort(l,pi-1,nums)
        quicksort(pi+1,r,nums)
    return nums

example=[]
n=int(input())
for i in range(n):
    example.append(int(input()))
print(quicksort(0,len(example)-1,example))
```

## Output:
![image](https://github.com/user-attachments/assets/e98713cb-94f8-4cb5-9acb-181f43f3c349)

## Result:
The program successfully sorts the input array using the QuickSort algorithm, arranging the elements in ascending order.
