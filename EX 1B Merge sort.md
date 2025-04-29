# EX 1B Merge Sort
## DATE: 25/02/2025
## AIM:
To write a python program to sort the first half of the list using merge sort.

## Algorithm
1. Start
2. Input an integer n (size of the array)
3. Initialize an empty array arr
4. Loop from 0 to n-1:
   - Input a float number and append it to arr
5. Print the original array
6. Calculate half = n // 2 (index marking the middle of the array)
7. Call mergesort(arr, 0, half) to sort only the first half of the array
8. In the mergesort function:
   - If size > 1:
   - Find the midpoint of the list (mid = size // 2)
   - Divide the list into two subarrays: left and right
   - Recursively sort left
   - Merge the sorted halves:
   - Compare and insert the smallest elements from left and right into the original array
   - Add any remaining elements from left or right
9. Print the array after sorting the first half
10. End  

## Program:
```
/*
Program to implement Merge Sort
Developed by: 
Register Number:  
*/

def mergesort(arr,start,end):
    size=len(arr)
    if size>1:
        mid=size//2
        left=arr[start:mid]
        right=arr[mid:end]
        mergesort(left,0,len(left))
        i=j=k=0
        left_size=len(left)
        right_size=len(right)
        while i<left_size and j<right_size:
            if left[i]<right[j]:
                arr[k]=left[i]
                i+=1
            else:
                arr[k]=right[j]
                j+=1
            k+=1
        while i<left_size:
            arr[k]=left[i]
            i+=1
            k+=1
        while j<right_size:
            arr[k]=right[j]
            j+=1
            k+=1

n=int(input())
arr=[]
for i in range(n):
    arr.append(float(input()))
print("Original array:")
print(*arr)
half=n//2
mergesort(arr,0,half)
print("Sorted first half and unchanged second half:")
print(*arr)
```

## Output:
![image](https://github.com/user-attachments/assets/30a93a98-a6b1-4827-beb4-e426beb70ceb)

## Result:
The program successfully sorts the first half of the given array using merge sort. where only the first half is sorted, and the second half remains unchanged.
