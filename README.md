
# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
```
1.get the array as input.
2.use the array.sort() function to find the linear search and binary search.
3.print array.
4.print the result.
```
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
```python
#program to for linear search method to match the item in a list.
#Developed by : MOHAMED AZEEM N
#reference no : 22007405
def linearSearch(array,n,k):
    for i in range(0,n):
        if(array[i]==k):
            return 1
    return -1
array=eval(input())
k=eval(input())
n=len(array)
array.sort()
result=linearSearch(array,n,k)
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)

```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```python
#program to find the element in a list using Binary Search(Iterative method)
#Developed by : MOHAMED AZEEM N
#reference no : 22007405
def BinarySearch(array,k,low,high):
    while low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
             return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid-1
    return -1
array=eval(input())
array.sort()
k=eval(input())
result=binarySearch(array,k,0,len(array)-1)
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)

```
iii)	# Find the element in a list using Binary Search (recursive Method).
```python
#program to find the element in a list using Binary Search(recursive method)
#Developed by : MOHAMED AZEEM N
#reference no : 22007405

def BinarySearch(array,k,low,high):
    if high>=low:
        mid=low+(high-low)//2
        if array[mid]==k:
             return mid
        elif array[mid]<k:
           return BinarySearch(array,k,low,mid-1)
        else:
            return BinarySearch(array,k,mid+1,high)
    else:
        return -1
array=eval(input())
array.sort()
k=eval(input())
result=binarySearch(array,k,0,len(array)-1)
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
    
```
## Sample Input and Output

![WhatsApp Image 2023-01-26 at 16 16 58 new](https://user-images.githubusercontent.com/121040764/214817612-e397f72e-1094-4e50-9e41-bfc61b3c61e6.jpg)

#program 1
![Screenshot (30) new](https://user-images.githubusercontent.com/121040764/214813765-b48428ed-cd97-426b-ac20-2770f4e9dae5.png)
![Screenshot (31) new](https://user-images.githubusercontent.com/121040764/214813811-8c3f5938-2365-4040-931b-02efebdb2c17.png)

#program 2
![Screenshot (32) new](https://user-images.githubusercontent.com/121040764/214813941-b6c84aa1-d922-4b69-8bb9-96f582749005.png)
![Screenshot (33) new](https://user-images.githubusercontent.com/121040764/214813980-b733f23c-72fa-4720-b020-717fa71b593d.png)

#program 3
![Screenshot (34) new](https://user-images.githubusercontent.com/121040764/214814056-591942c3-b6a9-4d94-97dd-daf7d0a9bd2e.png)
![Screenshot (35) new](https://user-images.githubusercontent.com/121040764/214814097-f9b22055-1fbd-4c39-836d-ae7b1d74b845.png)



## Result
Thus the linear search and binary search algorithm is implemented using python programming.
