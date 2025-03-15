# Binary Search

# [二分查找为什么总是写错？](https://www.bilibili.com/video/BV1d54y1q7k7/?spm_id_from=333.337.search-card.all.click&vd_source=fb0d94742d314c399a695c3ec1b7dc6b)
## Steps
1. define the condition()
2. define what to return, l or r
3. use the template
4. any other thing to be handled
# Template
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

## NeetCode
| Difficulty                                 | Problems                                                                                                         |                                 |
| ------------------------------------------ | ---------------------------------------------------------------------------------------------------------------- | ------------------------------- |
| <span style="color: green;">Easy</span>    | [704. Binary Search](https://leetcode.com/problems/binary-search/)                                               | <input type="checkbox" checked> |
| <span style="color: orange;">Medium</span> | [74. Search a 2D Matrix](https://leetcode.com/problems/search-a-2d-matrix/)                                      | <input type="checkbox" checked> |
| <span style="color: orange;">Medium</span> | [875. Koko Eating Bananas](https://leetcode.com/problems/koko-eating-bananas/)                                   | <input type="checkbox" checked> |
| <span style="color: orange;">Medium</span> | [153. Find Minimum in Rotated Sorted Array](https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/) | <input type="checkbox" checked> |
| <span style="color: orange;">Medium</span> | [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)              | <input type="checkbox">         |
| <span style="color: orange;">Medium</span> | [981. Time Based Key-Value Store](https://leetcode.com/problems/time-based-key-value-store/)                     | <input type="checkbox">         |
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


## Grind 75

| Difficulty                                 | Problems                                                                                                                                              |                         |
| ------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------- |
| <span style="color: green;">Easy</span>    | [704. Binary Search](https://leetcode.com/problems/binary-search/)                                                                                    | <input type="checkbox"> |
| <span style="color: green;">Easy</span>    | [35. Search Insert Position](https://leetcode.com/problems/search-insert-position/)                                                                   | <input type="checkbox"> |
| <span style="color: green;">Easy</span>    | [278. First Bad Version](https://leetcode.com/problems/first-bad-version/)                                                                            | <input type="checkbox"> |
| <span style="color: orange;">Medium</span> | [34. Find First and Last Position of Element in Sorted Array](https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array/) | <input type="checkbox"> |
| <span style="color: orange;">Medium</span> | [981. Time Based Key-Value Store](https://leetcode.com/problems/time-based-key-value-store/)                                                          | <input type="checkbox"> |
| <span style="color: red;">Hard</span>      | [1235. Maximum Profit in Job Scheduling](https://leetcode.com/problems/maximum-profit-in-job-scheduling/)                                             | <input type="checkbox"> |
