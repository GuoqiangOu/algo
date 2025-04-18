# Two Pointers

## NeetCode
| Difficulty                                 | Problems                                                                                                   |                         |
| ------------------------------------------ | ---------------------------------------------------------------------------------------------------------- | ----------------------- |
| <span style="color: green;">Easy</span>    | [88. Merge Sorted Array](https://leetcode.com/problems/merge-sorted-array/)                                | <input type="checkbox"> |
| <span style="color: green;">Easy</span>    | [125. Valid Palindrome](https://leetcode.com/problems/valid-palindrome/)                                   | <input type="checkbox"> |
| <span style="color: orange;">Medium</span> | [167. Two Sum II - Input Array Is Sorted](https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/) | <input type="checkbox"> |
| <span style="color: orange;">Medium</span> | [15. 3Sum](https://leetcode.com/problems/3sum/)                                                            | <input type="checkbox"> |
| <span style="color: orange;">Medium</span> | [11. Container With Most Water](https://leetcode.com/problems/container-with-most-water/)                  | <input type="checkbox"> |
| <span style="color: red;">Hard</span>      | [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)                              | <input type="checkbox"> |


## Grokking the Coding Interview

| Difficulty                                 | Problems                                                                                                                                                       |                                 |
| ------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------- |
| <span style="color: green;">Easy</span>    | [345. Reverse Vowels of a String](https://leetcode.com/problems/reverse-vowels-of-a-string/)                                                                   | <input type="checkbox" checked> |
| <span style="color: green;">Easy</span>    | [167. Two Sum II - Input Array Is Sorted](https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/)                                                     | <input type="checkbox">         |
| <span style="color: green;">Easy</span>    | [Find Non-Duplicate Number Instances (easy)](https://www.designgurus.io/course-play/grokking-the-coding-interview/doc/find-nonduplicate-number-instances-easy) | <input type="checkbox">         |
| <span style="color: green;">Easy</span>    | [977. Squares of a Sorted Array](https://leetcode.com/problems/squares-of-a-sorted-array/)                                                                     | <input type="checkbox">         |
| <span style="color: orange;">Medium</span> | [15. 3Sum](https://leetcode.com/problems/3sum/)                                                                                                                | <input type="checkbox">         |
| <span style="color: orange;">Medium</span> | [16. 3Sum Closest](https://leetcode.com/problems/3sum-closest/)                                                                                                | <input type="checkbox">         |
| <span style="color: orange;">Medium</span> | [Triplet Sum Close to Target (medium)](https://www.designgurus.io/course-play/grokking-the-coding-interview/doc/triplet-sum-close-to-target-medium)            | <input type="checkbox">         |
| <span style="color: orange;">Medium</span> | [259. 3Sum Smaller](https://leetcode.com/problems/3sum-smaller/)                                                                                               | <input type="checkbox">         |
| <span style="color: orange;">Medium</span> | [75. Sort Colors](https://leetcode.com/problems/sort-colors/)                                                                                                  | <input type="checkbox">         |
| <span style="color: orange;">Medium</span> | [18. 4Sum](https://leetcode.com/problems/4sum/)                                                                                                                | <input type="checkbox">         |
| <span style="color: green;">Easy</span>    | [844. Backspace String Compare](https://leetcode.com/problems/backspace-string-compare/)                                                                       | <input type="checkbox">         |
| <span style="color: orange;">Medium</span> | [581. Shortest Unsorted Continuous Subarray](https://leetcode.com/problems/shortest-unsorted-continuous-subarray/)                                             | <input type="checkbox">         |

# [Find Non-Duplicate Number Instances (easy)](https://www.designgurus.io/course-play/grokking-the-coding-interview/doc/find-nonduplicate-number-instances-easy)
```python
# Input: [2, 3, 3, 3, 6, 9, 9] 
# Output: 4 Explanation: The first four elements after moving element will be [2, 3, 6, 9].
class Solution:
  def moveElements(self, arr):
    l, r = 0, 1
    res = 1
    while r <= len(arr) - 1:
      if arr[l] != arr[r]:
        res += 1
        l = r
      r += 1
    return res
```

## [977. Squares of a Sorted Array](https://leetcode.com/problems/squares-of-a-sorted-array/)
```python
# **Input:** nums = [-4,-1,0,3,10]
# **Output:** [0,1,9,16,100]
# **Explanation:** After squaring, the array becomes [16,1,0,9,100].
# After sorting, it becomes [0,1,9,16,100].
class Solution:
    def sortedSquares(self, nums: List[int]) -> List[int]:
        n = len(nums)
        res = [0 for x in range(n)]
        l, r, curr = 0, n - 1, n - 1
        while l <= r:
            l_square = nums[l] ** 2
            r_square = nums[r] ** 2
            if l_square <= r_square:
                res[curr] = r_square
                r -= 1
            else:
                res[curr] = l_square
                l += 1
            curr -= 1
        return res
```

## [15. 3Sum](https://leetcode.com/problems/3sum/)
```python
class Solution:
    def threeSum(self, nums: List[int]) -> List[List[int]]:
        # 1. sort the list
        nums.sort()
        res = []
        # 2. for each num skip if the element is duplicate
        for i, num in enumerate(nums):
            if i > 0 and num == nums[i - 1]:
                continue
            # 3. do two sum
            l = i + 1
            r = len(nums) - 1
            while l < r:
                if nums[l] + nums[r] + num == 0:
                    res.append([num, nums[l], nums[r]])
                    l += 1
                    r -= 1
                    # skip duplicate
                    while l < r and nums[l] == nums[l - 1]:
                        l += 1
                    # skip duplicate
                    while l < r and nums[r] == nums[r + 1]:
                        r -= 1
                elif nums[l] + nums[r] + num < 0:
                    l += 1
                else:
                    r -= 1
        return res
```

## [16. 3Sum Closest](https://leetcode.com/problems/3sum-closest/)
```python
class Solution:
    def threeSumClosest(self, nums: List[int], target: int) -> int:
        # 1. sort the list
        nums.sort()
        closest = float("inf")
        # 2. for each num skip if the element is duplicate
        for i, num in enumerate(nums):
            if i > 0 and num == nums[i - 1]:
                continue
            # 3. do two sum to check for cloest
            l = i + 1
            r = len(nums) - 1
            while l < r:
                curr_sum = nums[l] + nums[r] + num
                # check if we need to update closest
                if abs(target - curr_sum) < abs(target - closest):
                    closest = curr_sum
                # two sum pointers moving logic
                if curr_sum == target:
                    return curr_sum
                elif curr_sum < target:
                    l += 1
                else:
                    r -= 1
        return closest
```

## [Triplet Sum Close to Target (medium)](https://www.designgurus.io/course-play/grokking-the-coding-interview/doc/triplet-sum-close-to-target-medium)
Note: 
There is additional  condition need to be checked compare to 16. 3Sum Closest, because in addition to 16. 3Sum Closest, below requirement need additional logic:
	If there are more than one such triplet, return the sum of the triplet with the smallest sum
```python
class Solution:
  def searchTriplet(self, arr, target_sum):
    arr.sort()
    smallest_diff = float("inf")
    for i, num in enumerate(arr):
	  # skip duplicates
      if i > 0 and num == arr[i - 1]:
        continue
      l, r = i + 1, len(arr) - 1
      while l < r:
        curr_diff = target_sum - num - arr[l] - arr[r]
        # case 1: we found smaller diff
        # case 2: we found same diff and current diff is bigger than smallest diff 
        if abs(curr_diff) < abs(smallest_diff) \
	        or (abs(curr_diff) == abs(smallest_diff) \
		        and curr_diff > smallest_diff):
          smallest_diff = curr_diff
        # return target_sum if we found 0 diff
        if curr_diff == 0:
          return target_sum
        # update l, r pointers
        elif curr_diff > 0:
          l += 1
        else:
          r -= 1
    return target_sum - smallest_diff
```

## [259. 3Sum Smaller](https://leetcode.com/problems/3sum-smaller/)
```python
class Solution:
    def threeSumSmaller(self, nums: List[int], target: int) -> int:
        nums.sort()
        n = len(nums) - 1
        count = 0
        for i in range(n - 1):
            l, r = i + 1, n
            while l < r:
                curr_sum = nums[i] + nums[l] + nums[r]
                if curr_sum < target:
                    # [1, 2, 3, 5, 8]
                    # l = 2, r = 8
                    # because i < l < r < target,
                    # and we are going to update left but right will not move
                    # once we know 1 + 2 + 8 < target
                    # we know 1 + 2 + 5 < target
                    #         1 + 2 + 3 < target
                    # so we are adding 3 = 3(r) - 0(l) to the count
                    count += r - l
                    l += 1
                else:
                    r -= 1
        return count
```

## [75. Sort Colors](https://leetcode.com/problems/sort-colors/)
```python
class Solution:
    def sortColors(self, nums: List[int]) -> None:
        """
        Do not return anything, modify nums in-place instead.
        """
        def swap(i: int, j: int) -> None:
            tmp = nums[i]
            nums[i] = nums[j]
            nums[j] = tmp
        # left to keep 0s at front
        # right to keep 2s at end
        # i go through the array to check and swap
        #   0: swap with left
        #   2: swap with right
        #   1: skip it because 1s in the middle is fine
        n = len(nums) - 1
        i, l, r = 0, 0, n
        while i <= r:
            if nums[i] == 0:
                swap(l, i)
                l += 1
            elif nums[i] == 2:
                swap(r, i)
                r -= 1
                # not moving i because we need to recheck the new swapped num
                i -= 1
			i += 1
```
## [18. 4Sum](https://leetcode.com/problems/4sum/)
```python
class Solution:
    def fourSum(self, nums: List[int], target: int) -> List[List[int]]:
        nums.sort()
        n = len(nums)
        curr, res = [], []
		# 3 sums has an outerloop and 2sums within
		# 4 sums has an outerloop and 3sums within
		# 5 sums has an outerloop and 4sums within and so on.
		# so below kSum is to accomendate all the sums cases
		# and recursively getting the results
        def kSum(k, start, target):
            if k != 2:
                # we add the k nums to curr, then recursivly add the 2sums results
                # 4sum will be n - 4 + 1
                # [1,0,-1,0,-2,2] will be 1,
                # add index 0 and 1 num to curr then recursivly add 2 sums results
                for i in range(start, n - k + 1):
                    # skip duplicates
                    if i > start and nums[i] == nums[i - 1]:
                        continue
	                # add to current, then kSum will recursively add other results
                    curr.append(nums[i])
                    # get k-1Sum results
                    kSum(k - 1, i + 1, target - nums[i])
                    # undo the current so next recursive can use it as empty arrary, and backtrack
                    curr.pop()
                return
            # base case: 2 sums
            l, r = start, n - 1
            while l < r:
                curr_sum = nums[l] + nums[r]
                if curr_sum > target:
                    r -= 1
                elif curr_sum < target:
                    l += 1
                else:
                    res.append(curr + [nums[l], nums[r]])
                    l += 1
                    # skip duplicates
                    while l < r and nums[l] == nums[l - 1]:
                        l += 1

        kSum(4, 0, target)

        return res
```
## [844. Backspace String Compare](https://leetcode.com/problems/backspace-string-compare/)
```python
class Solution:
    def backspaceCompare(self, s: str, t: str) -> bool:
	    # loop backward to skip # and the char
        def nextCharIndex(i: int, str: str):
            backspace_count = 0
            while i >= 0:
                if str[i] == '#':
                    backspace_count += 1
                elif backspace_count > 0:
                    backspace_count -= 1
                else:
                    break
                i -= 1
            return i
		# two pointers to loop backward on each to compare
        l, r = len(s) - 1, len(t) - 1
        while l >= 0 or r >= 0:
            nextCharIndexInS = nextCharIndex(l, s)
            nextCharIndexInT = nextCharIndex(r, t)
            # both reach to the start
            if nextCharIndexInS < 0 and nextCharIndexInT < 0:
                return True
            # one reach to the start but the other is not
            elif nextCharIndexInS < 0 or nextCharIndexInT < 0:
                return False
            # string not the same
            elif s[nextCharIndexInS] != t[nextCharIndexInT]:
                return False
            l = nextCharIndexInS - 1
            r = nextCharIndexInT - 1

        return True
```

## [581. Shortest Unsorted Continuous Subarray](https://leetcode.com/problems/shortest-unsorted-continuous-subarray/)
```python
class Solution:
    def findUnsortedSubarray(self, nums: List[int]) -> int:
	    # [1, 3, 2, 0, -1, 7, 10]
	    # two things we need to find out, start and end index
	    # to find out end, left -> right (assending expected):
	    #  1. keep track of the max value
	    #  2. update the end if it is smaller than max
	    # to find out start, left <- right (desending expected):
	    #  1. keep track of the min value
	    #  2. update the start if it's bigger thn min
        n = len(nums)
        curr_max = float('-INF')
        curr_min = float('INF')
        start = 0
        end = 0
        for i in range(n):
	        # loop to check for the end
            curr_max = max(curr_max, nums[i])
            if nums[i] < curr_max:
                end = i
			# loop backward to check for the start
            j = n - 1 - i
            curr_min = min(curr_min, nums[j])
            if nums[j] > curr_min:
                start = j

  
		# if start and end were not updated, nums is already sorted
        return 0 if start == end else end - start + 1
```