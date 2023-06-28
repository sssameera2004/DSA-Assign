def getPairsCount(arr, n, sum):
 
    count = 0  # Initialize result
 
    # Consider all possible pairs
    # and check their sums
    for i in range(0, n):
        for j in range(i + 1, n):
            if arr[i] + arr[j] == sum:
                count += 1
 
    return count
 
 
# Driver function
arr = [1, 5, 7, -1, 5]
n = len(arr)
sum = 6
print("Count of pairs is",
      getPairsCount(arr, n, sum))




for i in range(0, len(arr)):  
    for j in range(i+1, len(arr)):  
        if(arr[i] == arr[j]):  
            print(arr[j]);  
QUESTION 5:-
def duplicates(arr, n):
    
    # Increment array elements by 1
    for i in range(n):
        arr[i] = arr[i] + 1
          
    # result vector
    res = []
      
    # count variable for count of
    # largest element
    count = 0
    for i in range(n):
        
        # Calculate index value
        if(abs(arr[i]) > n):
            index = abs(arr[i])//(n+1)
        else:
            index = abs(arr[i])
              
        # Check if index equals largest element value
        if(index == n):
            count += 1
            continue
              
        # Get element value at index
        val = arr[index]
          
        # Check if element value is negative, positive
        # or greater than n
        if(val < 0):
            res.append(index-1)
            arr[index] = abs(arr[index]) * (n + 1)
        elif(val>n):
            continue
        else:
            arr[index] = -arr[index]
              
    # If largest element occurs more than once
    if(count > 1):
        res.append(n - 1)
    if(len(res) == 0):
        res.append(-1)
    else:
        res.sort()
    return res
    
# Driver Code
numRay = [ 0, 4, 3, 2, 7, 8, 2, 3, 1 ]
n = len(numRay)
ans = duplicates(numRay,n)
for i in ans:
    print(i)

METHOD 2:-
class Solution(object):
    def findDuplicates(self, nums):
        """
        :type nums: List[int]
        :rtype: List[int]
        """


QUESTION 6:-
from typing import List




class Solution:
    def kth_Largest_And_Smallest_By_AscendingOrder(self, arr: List[int], k: int) -> None:
        arr.sort()
        n = len(arr)


        print(
            f"kth Largest element {arr[n - k]}, kth Smallest element {arr[k - 1]}")




if __name__ == "__main__":
    arr = [1, 2, 6, 4, 5, 3]
    Solution().kth_Largest_And_Smallest_By_AscendingOrder(arr, 3)



def move(arr):
  arr.sort()
 
# driver code
arr = [ -1, 2, -3, 4, 5, 6, -7, 8, 9 ]
move(arr)
for e in arr:
    print(e , end = " ")



 
def find(arr):
    # sort array
    arr.sort()

    # print array
    print("Array after moving all the elements to left:", arr)


array = [1, 3, -1, 4, -3, -5, -6, 3, 7]
# call function
find(array)




