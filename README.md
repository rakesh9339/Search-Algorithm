# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```
Program for linear search method to match the item in a list
Developed by:Rakesh J.S
RegisterNumber:22009339

def linearSearch(array,n,k):
    # write your code for linear search
    for i in range(0,n):
        if array[i]==k:
            return i
    return -1
array = eval(input())
k = eval(input()) 
n = len(array)
array.sort()
result = linearSearch(array,n,k)
if result==-1:
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ", result)

```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by:Rakesh J.S
RegisterNumber:22009339
def binarySearchIter(array,k,low,high):
    while low <= high:
        mid = low + (high - low)//2
        if array[mid] == k:
            return mid
        elif array[mid] < k:
            low = mid+1
        else:
            high = mid-1
    return -1
array=eval(input())
array.sort()
k = eval(input())
result = binarySearchIter(array,k,0,len(array)-1)
if result==-1:
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)

```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
Program to find the element in a list using Binary Search (recursive Method).
Developed by: Rakesh J.S
RegisterNumber: 22009339
def BinarySearch(arr,k,low,high):
    if low <= high:
        mid = low + (high - low)//2
        if array[mid] == k:
            return mid
        elif array[mid] > k:
            return  BinarySearch(arr,k,low,mid-1) 
        else:
            return BinarySearch(arr,k,mid+1,high)
    else:
        return-1
array=eval(input())
array.sort()
k = eval(input())
result = BinarySearch(array,k,0,len(array)-1)
if result==-1:
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)









```
## Sample Input and Output
linear search method to match the item in a list
![Screenshot (13)](https://user-images.githubusercontent.com/121115650/214926741-9faf1386-5797-4e4a-9215-578b9ec21e4a.png)
![Screenshot (14)](https://user-images.githubusercontent.com/121115650/214926880-6031cdd2-4aee-4059-bfad-fb01d575dd96.png)

find the element in a list using Binary Search(Iterative Method) 
![Screenshot (16)](https://user-images.githubusercontent.com/121115650/214927677-a448e5fe-08d4-4e46-9562-7c1fcdba3b4c.png)


find the element in a list using Binary Search (recursive Method) 
![Screenshot (17)](https://user-images.githubusercontent.com/121115650/214927411-b0f44b8d-5c2a-4c62-a3fe-74fa6ff0d00b.png)


## Result
Thus the linear search and binary search algorithm is implemented using python programming.
