# Interviewing Library
This repository contains problems and solutions to common interview questions. Please look at the `template.py` for problem statements only. The `solution.py` contains a workable solution. 

For example, take the problem statement below:

```python
'''
Given a sorted array, A, with possibly duplicated elements, find the indices of the first and last occurrences of a target element, x. Return -1 if the target is not found.

Example:
Input: A = [1,3,3,5,7,8,9,9,9,15], target = 9
Output: [6,8]

Input: A = [100, 150, 150, 153], target = 150
Output: [1,2]

Input: A = [1,2,3,4,5,6,10], target = 9
Output: [-1, -1]
'''

class Solution: 
  def getRange(self, arr, target):
    # Fill this in.
  
# Test program 
arr = [1, 2, 2, 2, 2, 3, 4, 7, 8, 8] 
x = 2
print(Solution().getRange(arr, x))
# [1, 4]
```

- An example `solution.py`

```python
'''
Given a sorted array, A, with possibly duplicated elements, find the indices of the first and last occurrences of a target element, x. Return -1 if the target is not found.

Example:
Input: A = [1,3,3,5,7,8,9,9,9,15], target = 9
Output: [6,8]

Input: A = [100, 150, 150, 153], target = 150
Output: [1,2]

Input: A = [1,2,3,4,5,6,10], target = 9
Output: [-1, -1]
'''

class Solution: 
  def getRange(self, arr, target):
    start = -1
    end = -1
    for i in range(len(arr)):
      if arr[i] == target:
        start = i
        break
    
    for j in range(len(arr) - 1, -1, -1):
      if arr[j] == target:
        end = j
        break
    
    return [start, end]
    # Fill this in.
  
# Test program 
arr = [1, 2, 2, 2, 2, 3, 4, 7, 8, 8] 
x = 2
print(Solution().getRange(arr, x))
#[1, 4]

arr = [1,3,3,5,7,8,9,9,9,15] 
x = 9
print(Solution().getRange(arr, x))
# [6, 8]

arr = [100, 150, 150, 153] 
x = 150
print(Solution().getRange(arr, x))
# [1, 2]

arr = [1,2,3,4,5,6,10] 
x = 9
print(Solution().getRange(arr, x))
# [-1, -1]
```

- Enjoy problem solving!