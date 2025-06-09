# Binary Search

[二分查找为什么总是写错？](https://www.bilibili.com/video/BV1d54y1q7k7/?spm_id_from=333.337.search-card.all.click&vd_source=fb0d94742d314c399a695c3ec1b7dc6b)
[二分查找 红蓝染色法【基础算法精讲 04】](https://www.bilibili.com/video/BV1AP41137w7?vd_source=fb0d94742d314c399a695c3ec1b7dc6b&spm_id_from=333.788.videopod.sections)

# Steps
1. define the condition()
2. define what to return, l or r
3. use the template
4. any other thing to be handled

[34. Find First and Last Position of Element in Sorted Array](https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array/)
For integers, lower bound conditions are transferable:
1. `>= 8`
2. `> 8` 
	1. equals `(>= 8 + 1) -> (>= 9)`
	2. `binary_search(>= 9)`
3. `< 8` 
	1. equals `idx of (>= 8) - 1`
	2. which is the number on the LEFT of `binary_search(>= 8)`
4. `<= 8` 
	1. equals `(> 8) - 1` 
	2. equals `idx of (>= 8 + 1) - 1` by #2
	3. equals `idx of (>= 9) - 1`
	4. which is the number on the LEFT of `binary_search(>=9)`
# Template 0
左开右开区间
```python
def binary_search(arr: List[int], target: int) -> int:
    l, r = -1, len(arr)
    while l + 1 != r:
        mid = (l + r) // 2 # or mid = l + (r - l) // 2
        if condition(mid):
            r = mid
        else:
            l = mid
    return l or r

    # How to figure out what is the condition and what to return:
    # arr = [1, 2, 3, 5, 5, 5, 8, 9]
    # 1. find the 1st number which >= 5, [1, 2, 3, <5>, 5, 5, 8, 9]
    #    this is finding the lower bound
    #    condition => mid < 5
    #    return r
    # 2. find the last number which < 5, [1, 2, <3>, 5, 5, 5, 8, 9]'
    #    this is finding the lower bound - 1
	#    condition => mid < 5
    #    return l
    # 3. find the first number which > 5, [1, 2, 3, 5, 5, 5, <8>, 9]
    #    this is finding the upper bound
	#    condition => mid <= 5
    #    return r
    # 4. find the last number which <= 5, [1, 2, 3, 5, 5, <5>, 8, 9]
    #    this is finding the upper bound - 1
	#    condition => mid <= 5
    #    return l
```
# Template 1
左闭右闭区间
```python
def binary_search(arr: List[int], target: int) -> int:
    l, r = 0, len(arr) - 1
    first_true_index = -1
    while l <= r:
        mid = (l + r) // 2 # or mid = l + (r - l) // 2
        if condition(mid):
	        first_true_index = mid
            r = mid - 1
        else:
            l = mid + 1
    return first_true_index
```
## NeetCode
| Difficulty                                 | Problems                                                                                                         |                                 |
| ------------------------------------------ | ---------------------------------------------------------------------------------------------------------------- | ------------------------------- |
| <span style="color: green;">Easy</span>    | [704. Binary Search](https://leetcode.com/problems/binary-search/)                                               | <input type="checkbox" checked> |
| <span style="color: orange;">Medium</span> | [74. Search a 2D Matrix](https://leetcode.com/problems/search-a-2d-matrix/)                                      | <input type="checkbox" checked> |
| <span style="color: orange;">Medium</span> | [875. Koko Eating Bananas](https://leetcode.com/problems/koko-eating-bananas/)                                   | <input type="checkbox" checked> |
| <span style="color: orange;">Medium</span> | [153. Find Minimum in Rotated Sorted Array](https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/) | <input type="checkbox" checked> |
| <span style="color: orange;">Medium</span> | *[33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)             | <input type="checkbox" checked> |
| <span style="color: orange;">Medium</span> | [981. Time Based Key-Value Store](https://leetcode.com/problems/time-based-key-value-store/)                     | <input type="checkbox" checked> |
| <span style="color: red;">Hard</span>      | [4. Median of Two Sorted Arrays](https://leetcode.com/problems/median-of-two-sorted-arrays/)                     | <input type="checkbox">         |

## [704. Binary Search](https://leetcode.com/problems/binary-search/)
```python
class Solution:
    def search(self, nums: List[int], target: int) -> int:
        l, r = -1, len(nums)
        while l + 1 != r:
            mid = l + (r - l) // 2
            if nums[mid] > target:
                r = mid
            else:
                l = mid
        return l if nums[l] == target else -1
```

## [74. Search a 2D Matrix](https://leetcode.com/problems/search-a-2d-matrix/)
```python
class Solution:
    def searchMatrix(self, matrix: List[List[int]], target: int) -> bool:
        row_to_search = None
        # 1. find the row which could have the target
        for i, row in enumerate(matrix):
            if row[0] <= target and row[-1] >= target:
                row_to_search = matrix[i]
  
        if row_to_search is None:
            return False
		# 2. do binary search in the row
        l, r = -1, len(row_to_search)
        while l + 1 != r:
            mid = l + (r - l) // 2
            if row_to_search[mid] > target:
                r = mid
            else:
                l = mid

        return row_to_search[l] == target
```

## [875. Koko Eating Bananas](https://leetcode.com/problems/koko-eating-bananas/)
```python
# to get the smallest int <= to a/b
math.ceil(a/b)

class Solution:
    def minEatingSpeed(self, piles: List[int], h: int) -> int:
        def checkHrs(num: int) -> int:
            hr = 0
            for p in piles:
                hr += math.ceil(p / num)
            return hr

        l, r = 0, max(piles)
        while l + 1 != r:
            mid =  l + (r - l) // 2
            if checkHrs(mid) <= h:
                r = mid
            else:
                l = mid
        return r

```
## [153. Find Minimum in Rotated Sorted Array](https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/)
```python
# sometime if we need to check l or r in the first loop
# since we are using l=-1, r=len(arr), we will get index out of range
# we will need to change the initial value of l or r to avoid it
# in the solution of this problem we will need to set l=len(arr)-1 instead of len(arr)
class Solution:
    def findMin(self, nums: List[int]) -> int:
        l, r = -1, len(nums) - 1
        while l + 1 != r:
            mid = l + (r - l) // 2
            if nums[mid] > nums[r]:
                l = mid
            else:
                r = mid
        return nums[r]

```

## [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
```python
class Solution:
    def search(self, nums: List[int], target: int) -> int:
        # left sorted
        #   [4,5,6,7,8,9,<10>,0,1,2,3]
        #   target on sorted left
        #   target on non sorted right
        # right sorted
        #   [5,6,7,0,<1>,2,3,4,5]
        #   target on sorted right
        #   target on non sorted left
		# Note: couldn't find a way to use the template with l, r = -1, len(arr) and while l + 1 != r
        l, r = 0, len(nums) - 1
        while l <= r:
            mid = l + (r - l) // 2
            # 1. if we found the target
            if nums[mid] == target:
                return mid
            # 2. [left, mid] is sorted
            if nums[l] <= nums[mid]:
                # target on sorted left side
                if target >= nums[l] and target <= nums[mid]:
                    r = mid - 1
                else:
                    l = mid +  1
            # 3. [mid, right] is sorted
            else:
                # target on sorted right side
                if target >= nums[mid] and target <= nums[r]:
                    l = mid + 1
                else:
                    r = mid - 1
        # target not found
        return -1
```

## [981. Time Based Key-Value Store](https://leetcode.com/problems/time-based-key-value-store/)
```python
# Becasue the key value pairs are added base on time stamp, so it is sorted,
# that's why we can use binary search
class TimeMap:
    def __init__(self):
        self.store = {}
	# Time: O(1)
    def set(self, key: str, value: str, timestamp: int) -> None:
        if key not in self.store.keys():
            self.store[key] = []
        self.store[key].append([value, timestamp])

	# Time: O(logn)
    def get(self, key: str, timestamp: int) -> str:
        values = self.store.get(key, [])
        n = len(values)
        l, r = -1, n
        res = ''

        while l + 1 != r:
            mid = l + (r - l) // 2
            if self.store[key][mid][1] <= timestamp:
                res = self.store[key][mid][0]
                l = mid
            else:
                r = mid
        return res

# Your TimeMap object will be instantiated and called as such:
# obj = TimeMap()
# obj.set(key,value,timestamp)
# param_2 = obj.get(key,timestamp)
```

## Grind 75

| Difficulty                                 | Problems                                                                                                                                               |                                 |
| ------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------- |
| <span style="color: green;">Easy</span>    | [704. Binary Search](https://leetcode.com/problems/binary-search/)                                                                                     | <input type="checkbox" checked> |
| <span style="color: green;">Easy</span>    | [35. Search Insert Position](https://leetcode.com/problems/search-insert-position/)                                                                    | <input type="checkbox" checked> |
| <span style="color: green;">Easy</span>    | [278. First Bad Version](https://leetcode.com/problems/first-bad-version/)                                                                             | <input type="checkbox" checked> |
| <span style="color: orange;">Medium</span> | *[34. Find First and Last Position of Element in Sorted Array](https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array/) | <input type="checkbox" checked> |
| <span style="color: orange;">Medium</span> | [981. Time Based Key-Value Store](https://leetcode.com/problems/time-based-key-value-store/)                                                           | <input type="checkbox" checked> |
| <span style="color: red;">Hard</span>      | [1235. Maximum Profit in Job Scheduling](https://leetcode.com/problems/maximum-profit-in-job-scheduling/)                                              | <input type="checkbox">         |
## [34. Find First and Last Position of Element in Sorted Array](https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array/)
```python
# solution 1
class Solution:
    def searchRange(self, nums: List[int], target: int) -> List[int]:
        def findLowerBound(nums: List[int], target: int) -> int:
            if len(nums) == 0:
                return -1
            l, r = -1, len(nums)
            while l + 1 != r:
                mid = l + (r - l) // 2
                if nums[mid] < target:
                    l = mid
                else:
                    r = mid
            return r if r < len(nums) and nums[r] == target else -1

        def findUpperBound(nums: List[int], target: int) -> int:
            if len(nums) == 0:
                return -1
            l, r = -1, len(nums)
            while l + 1 != r:
                mid = l + (r - l) // 2
                if nums[mid] > target:
                    r = mid
                else:
                    l = mid
            return l if nums[l] == target else -1

        return [findLowerBound(nums, target), findUpperBound(nums, target)]

# solution 2
class Solution:
    def searchRange(self, nums: List[int], target: int) -> List[int]:
        def findLowerBound(nums: List[int], target: int) -> int:
            l, r = 0, len(nums) - 1
            while l <= r:
                mid = l + (r - l) // 2
                if nums[mid] == target:
                    r = mid - 1
                elif nums[mid] < target:
                    l = mid + 1
                elif nums[mid] > target:
                    r = mid - 1

            return l if l >= 0 and l < len(nums) and nums[l] == target else -1

  
        def findUpperBound(nums: List[int], target: int) -> int:
            l, r = 0, len(nums) - 1
            while l <= r:
                mid = l + (r - l) // 2
                if nums[mid] == target:
                    l = mid + 1
                elif nums[mid] < target:
                    l = mid + 1
                elif nums[mid] > target:
                    r = mid - 1

            return l - 1 if l - 1 >= 0 and nums[l - 1] == target else - 1

        return [findLowerBound(nums, target), findUpperBound(nums, target)]

