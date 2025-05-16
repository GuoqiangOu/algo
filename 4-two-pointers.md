# Two Pointers
## [灵茶山艾府](https://leetcode.cn/discuss/post/3578981/ti-dan-hua-dong-chuang-kou-ding-chang-bu-rzz7/)

### Opposite direction --><--
- Starts at both ends (`left=0`, `right=n-1`).
- Moves toward each other (`left++`, `right--`).
- Used in problems like **Two Sum, Palindrome checks, and partitioning**.
#### Template
```python
def two_pointers_opposite(arr):
    left, right = 0, len(arr) - 1
    while left < right:
        # Process current elements
        current = process(arr[left], arr[right])
        # Update pointers based on condition
        if condition(arr[left], arr[right]):
            left += 1
        else:
            right -= 1
```

| #   | Difficulty                                      | Problems                                                                                                                                                                                    |                                 |
| --- | ----------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------- |
| 1   | <span style="color: green;">Easy</span>         | [344. Reverse String](https://leetcode.com/problems/reverse-string/)                                                                                                                        | <input type="checkbox" checked> |
| 2   | <span style="color: green;">Easy</span>         | [125. Valid Palindrome](https://leetcode.com/problems/valid-palindrome/)                                                                                                                    | <input type="checkbox" checked> |
| 3   | <span style="color: orange;">Medium</span> 1502 | [1750. Minimum Length of String After Deleting Similar Ends](https://leetcode.com/problems/minimum-length-of-string-after-deleting-similar-ends/)                                           | <input type="checkbox" checked> |
| 4   | <span style="color: orange;">Medium</span> 1507 | [2105. Watering Plants II](https://leetcode.com/problems/watering-plants-ii/)                                                                                                               | <input type="checkbox" checked> |
| 5   | <span style="color: green;">Easy</span>         | [977. Squares of a Sorted Array](https://leetcode.com/problems/squares-of-a-sorted-array/)                                                                                                  | <input type="checkbox" checked> |
| 6   | <span style="color: orange;">Medium</span>      | [658. Find K Closest Elements](https://leetcode.com/problems/find-k-closest-elements/)                                                                                                      | <input type="checkbox" checked> |
| 7   | <span style="color: orange;">Medium</span>      | [1471. The k Strongest Values in an Array](https://leetcode.com/problems/the-k-strongest-values-in-an-array/)                                                                               | <input type="checkbox" checked> |
| 8   | <span style="color: orange;">Medium</span>      | [167. Two Sum II - Input Array Is Sorted](https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/)                                                                                  | <input type="checkbox" checked> |
| 9   | <span style="color: orange;">Medium</span>      | [633. Sum of Square Numbers](https://leetcode.com/problems/sum-of-square-numbers/)                                                                                                          | <input type="checkbox" checked> |
| 10  | <span style="color: green;">Easy</span>         | [2824. Count Pairs Whose Sum is Less than Target](https://leetcode.com/problems/count-pairs-whose-sum-is-less-than-target/)                                                                 | <input type="checkbox" checked> |
| 11  | <span style="color: orange;">Medium</span>      | * [2563. Count the Number of Fair Pairs](https://leetcode.com/problems/count-the-number-of-fair-pairs/)                                                                                     | <input type="checkbox" checked> |
| 12  | <span style="color: green;">Easy</span>         | [LCP 28. 采购方案](https://leetcode.cn/problems/4xy4Wx/)                                                                                                                                        | <input type="checkbox" checked> |
| 13  | <span style="color: orange;">Medium</span>      | [15. 3Sum](https://leetcode.com/problems/3sum/)                                                                                                                                             | <input type="checkbox" checked> |
| 14  | <span style="color: orange;">Medium</span>      | [16. 3Sum Closest](https://leetcode.com/problems/3sum-closest/)                                                                                                                             | <input type="checkbox" checked> |
| 15  | <span style="color: orange;">Medium</span>      | [18. 4Sum](https://leetcode.com/problems/4sum/)                                                                                                                                             | <input type="checkbox" checked> |
| 16  | <span style="color: orange;">Medium</span>      | * [611. Valid Triangle Number](https://leetcode.com/problems/valid-triangle-number/)                                                                                                        | <input type="checkbox" checked> |
| 17  | <span style="color: orange;">Medium</span>1711  | * [923. 3Sum With Multiplicity](https://leetcode.com/problems/3sum-with-multiplicity/)                                                                                                      | <input type="checkbox" checked> |
| 18  | <span style="color: orange;">Medium</span>      | * [1577. Number of Ways Where Square of Number Is Equal to Product of Two Numbers](https://leetcode.com/problems/number-of-ways-where-square-of-number-is-equal-to-product-of-two-numbers/) | <input type="checkbox" checked> |
| 19  | <span style="color: orange;">Medium</span> 1762 | [948. Bag of Tokens](https://leetcode.com/problems/bag-of-tokens/)                                                                                                                          | <input type="checkbox" checked> |
| 20  | <span style="color: orange;">Medium</span>      | * [11. Container With Most Water](https://leetcode.com/problems/container-with-most-water/)                                                                                                 | <input type="checkbox" checked> |
| 21  | <span style="color: red;">Hard</span>           | * [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)                                                                                                             | <input type="checkbox" checked> |
| 22  | <span style="color: orange;">Medium</span> 1868 | * [1616. Split Two Strings to Make Palindrome](https://leetcode.com/problems/split-two-strings-to-make-palindrome/)                                                                         | <input type="checkbox" checked> |
| 23  | <span style="color: orange;">Medium</span> 2276 | * [1498. Number of Subsequences That Satisfy the Given Sum Condition](https://leetcode.com/problems/number-of-subsequences-that-satisfy-the-given-sum-condition/)                           | <input type="checkbox" checked> |
| 24  | <span style="color: red;">Hard</span> 2457      | [1782. Count Pairs Of Nodes](https://leetcode.com/problems/count-pairs-of-nodes/)                                                                                                           | <input type="checkbox">         |
| 25  | <span style="color: green;">Easy</span>         | [1099. Two Sum Less Than K](https://leetcode.com/problems/two-sum-less-than-k/)                                                                                                             | <input type="checkbox" checked> |
| 26  | <span style="color: orange;">Medium</span>      | * [360. Sort Transformed Array](https://leetcode.com/problems/sort-transformed-array/)                                                                                                      | <input type="checkbox" checked> |
| 27  | <span style="color: orange;">Medium</span>      | [2422. Merge Operations to Turn Array Into a Palindrome](https://leetcode.com/problems/merge-operations-to-turn-array-into-a-palindrome/)                                                   | <input type="checkbox" checked> |
| 28  | <span style="color: orange;">Medium</span>      | [259. 3Sum Smaller](https://leetcode.com/problems/3sum-smaller/)                                                                                                                            | <input type="checkbox" checked> |
#### [344. Reverse String](https://leetcode.com/problems/reverse-string/)
```python
class Solution:
    def reverseString(self, s: List[str]) -> None:
        n = len(s)
        left, right = 0, n - 1
        while left < right:
            # swap
            s[left], s[right] = s[right], s[left]
            # update pointers
            left += 1
            right -= 1
```
#### [125. Valid Palindrome](https://leetcode.com/problems/valid-palindrome/)
```python
class Solution:
    def isPalindrome(self, s: str) -> bool:
        n = len(s)
        left, right = 0, n - 1
        while left < right:
            # skip left non-alphanumeric
            while left < right and not s[left].lower().isalnum():
                left += 1
            # skip right non-alphanumeric
            while left < right and not s[right].lower().isalnum():
                right -= 1
            # compare
            if s[left].lower() != s[right].lower():
                return False
            # update pointers
            left += 1
            right -= 1
        # is palindrome
        return True
```
#### [1750. Minimum Length of String After Deleting Similar Ends](https://leetcode.com/problems/minimum-length-of-string-after-deleting-similar-ends/)
```python
class Solution:
    def minimumLength(self, s: str) -> int:
        n = len(s)
        left, right = 0, n - 1
        while left < right:
            if s[left] != s[right]:
                break
            # update left
            left += 1
            # skip duplicates
            while left < right and s[left] == s[left - 1]:
                left += 1
            # update right
            right -= 1
            # skip duplicates
            while left < right and s[right] == s[right + 1]:
                right -= 1
        return right - left + 1
# improved solution
class Solution:
    def minimumLength(self, s: str) -> int:
        n = len(s)
        left, right = 0, n - 1
        while left < right and s[left] == s[right]:
            char = s[left]
            # update left
            while left <= right and s[left] == char:
                left += 1
            # update right
            while left <= right and s[right] == char:
                right -= 1
        return right - left + 1
```
#### [2105. Watering Plants II](https://leetcode.com/problems/watering-plants-ii/)
I made a mistake on updating before refiling and comparing `currA < 0` instead of the plant.
```python
class Solution:
    def minimumRefill(self, plants: List[int], capacityA: int, capacityB: int) -> int:
        n = len(plants)
        left, right = 0, n - 1
        currA = capacityA
        currB = capacityB
        res = 0
        while left < right:
            # refill left
            if currA < plants[left]:
                currA = capacityA
                res += 1
            # update left
            currA -= plants[left]
            # refill right
            if currB < plants[right]:
                currB = capacityB
                res += 1
            # update right
            currB -= plants[right]
            # update pointers
            left += 1
            right -= 1
        # handle the case of odd num of plants
        if left == right and max(currA, currB) < plants[left]:
            res += 1

        return res
```
#### [977. Squares of a Sorted Array](https://leetcode.com/problems/squares-of-a-sorted-array/)
```python
class Solution:
    def sortedSquares(self, nums: List[int]) -> List[int]:
        n = len(nums)
        left, right = 0, n - 1
        res = [0] * n
        # loop backward to update res array
        i = n - 1
        while i >= 0:
            # get squares
            left_square = nums[left] ** 2
            right_square = nums[right] ** 2
            # update res to be the bigger one
            if left_square > right_square:
                res[i] = left_square
                left += 1
            else:
                res[i] = right_square
                right -= 1
            # move pointer to left
            i -= 1
        return res
```
#### [658. Find K Closest Elements](https://leetcode.com/problems/find-k-closest-elements/)
```python
class Solution:
    def findClosestElements(self, arr: List[int], k: int, x: int) -> List[int]:
        n = len(arr)
        left, right = 0, n - 1
        while left < right:
            # we have the res
            if right - left + 1 == k:
                return arr[left:right + 1]
            # calculate the differences
            left_num = abs(arr[left] - x)
            right_num = abs(arr[right] - x)
            # if left is closer, we ignore right
            # from the problem statement we can use:
            # if left_num < right_num or left_num == right_num and arr[left] < arr[right]:
            # which is the same as below
            if left_num > right_num:
                right -= 1
            else:
                left += 1
```
#### [1471. The k Strongest Values in an Array](https://leetcode.com/problems/the-k-strongest-values-in-an-array/)
```python
class Solution:
    def getStrongest(self, arr: List[int], k: int) -> List[int]:
        n = len(arr)
        arr.sort()
        m = arr[(n - 1) // 2]
        left, right = 0, n - 1
        res = []
        while k:
            left_val = abs(arr[left] - m)
            right_val = abs(arr[right] - m)
            # pick left
            # from the problem statement we can use:
            # if left_val > right_val or left_val == right_val and arr[left] > arr[right]:
            # which is the same as below
            if left_val > right_val:
                res.append(arr[left])
                left += 1
            # pick right
            else:
                res.append(arr[right])
                right -= 1
            k -= 1
        return res
```
#### [167. Two Sum II - Input Array Is Sorted](https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/)
```python
class Solution:
    def twoSum(self, numbers: List[int], target: int) -> List[int]:
        n = len(numbers)
        left, right = 0, n - 1
        while left < right:
            curr_sum = numbers[left] + numbers[right]
            if curr_sum > target:
                right -= 1
            elif curr_sum < target:
                left += 1
            else:
                return [left + 1, right + 1]
```
#### [633. Sum of Square Numbers](https://leetcode.com/problems/sum-of-square-numbers/)
I made a mistake on thinking right is c instead of the square root of c
`right = isqrt(c)` is the main point of this problem
```python
class Solution:
    def judgeSquareSum(self, c: int) -> bool:
        # idea:
        # think of this problem as searching a and b
        # in the array of [a, a+1,...,b-1,b], where a^2 + b^2 = c,
        # where a = 0, b is the largest integer such that b^2 <= c
        left, right = 0, isqrt(c)
        while left < right:
            curr = left ** 2 + right ** 2
            if curr == c:
                return True
            elif curr < c:
                left += 1
            else:
                right -= 1
        return False
```
#### [2824. Count Pairs Whose Sum is Less than Target](https://leetcode.com/problems/count-pairs-whose-sum-is-less-than-target/)
```python
class Solution:
    def countPairs(self, nums: List[int], target: int) -> int:
        nums.sort()
        n = len(nums)
        left, right = 0, n - 1
        res = 0
        while left < right:
            _sum = nums[left] + nums[right]
            if _sum < target:
                # because it's sorted
                # left + right < target, left + 1 + right < target,...,
                # right-1 + right < target,
                # so we have right - left pairs
                res += right - left
                left += 1
            else:
                right -= 1
        return res
```
#### [2563. Count the Number of Fair Pairs](https://leetcode.com/problems/count-the-number-of-fair-pairs/)
```python
class Solution:
    def countFairPairs(self, nums: List[int], lower: int, upper: int) -> int:
        # we want lower <= nums[i] + nums[j] <= upper
        # if we are counting for each i to find the number of j,
        # we need to find num of j in:
        # 1. nums[j] <= upper - nums[i]
        #    --> count(upper)
        # 2. nums[j] < lower - nums[i] which is
        #    nums[j] <= lower - 1 - nums[i]
        #    --> count(lower - 1)
        # ans we need is count(upper) - count(lower - 1)
        # note: 
        # it can also be count(upper + 1) - count(lower),
        # but in the helper func, it's sum < upper instead of sum <= upper

        # How to find count(upper):
        # 1. if nums[i] + nums[j] <= upper
        #    then nums[i] + nums[j - 1] <= upper
        #    all js within [i + 1, j] can pair with i
        #    so, we can add j - i number of res

        # 2. if nums[i] + nums[j] > upper
        #    then all js withint [i, j - 1] can NOT pair with i
        #    so, we skip j
        nums.sort()

        def count(val: int) -> int:
            n = len(nums)
            left, right = 0, n - 1
            res = 0
            while left < right:
                _sum = nums[left] + nums[right]
                if _sum <= val:
                    res += right - left
                    left += 1
                else:
                    right -= 1
            return res
        return count(upper) - count(lower - 1)
```

#### [LCP 28. 采购方案](https://leetcode.cn/problems/4xy4Wx/)
Question as to find num of pair of components which smaller or equal to budget(target),
if `[left, right]` is smaller equal to target, `[left+1, right]` are all smaller equal to target,
so we need to add `right - lefet` to result

I still don't understand the use or meaning of `mod 1e9 + 7 (1000000007)`
```python
class Solution:
    def purchasePlans(self, nums: List[int], target: int) -> int:
        nums.sort()
        res = 0
        left, right = 0, len(nums) - 1
        while left < right:
            if nums[left] + nums[right] <= target:
                res += right - left
                left += 1
            else:
                right -= 1
        return res % 1000000007
```
#### [15. 3Sum](https://leetcode.com/problems/3sum/)
```python
class Solution:

    def threeSum(self, nums: List[int]) -> List[List[int]]:
        # idea, for each of num, we do two sum
        nums.sort()
        n = len(nums)
        ans = []
        for i in range(n - 2):
            # skip duplicates
            if i > 0 and nums[i] == nums[i - 1]:
                continue
            # improvement 1
            if nums[i] + nums[i + 1] + nums[i + 2] > 0:
                # becasue nums[i] + the rest of the nums on right side will always > 0 -> != 0
                # so we can break
                break
            # improvement 2
            if nums[i] + nums[-2] + nums[-1] < 0:
                # because nums[i] + the rest of the nums on the left side will always < 0
                # so we can skip to check for next
                continue
            # do two sum
            left, right = i + 1, n - 1
            while left < right:
                _sum = nums[i] + nums[left] + nums[right]
                if _sum == 0:
                    ans.append([nums[i], nums[left], nums[right]])
                    left += 1
                    right -= 1
                    # skip left duplicates
                    while left < right and nums[left] == nums[left - 1]:
                        left += 1
                    # skip right duplicates
                    while left < right and nums[right] == nums[right + 1]:
                        right -= 1
                elif _sum > 0:
                    right -= 1
                else:
                    left += 1
        return ans
```

#### [16. 3Sum Closest](https://leetcode.com/problems/3sum-closest/)
I made a mistake of forgetting to sort the arr, remember to sort!
```python
class Solution:
    def threeSumClosest(self, nums: List[int], target: int) -> int:
        nums.sort()
        n = len(nums)
        res = inf
        for i in range(n - 2):
            # skip duplicates
            if i > 0 and nums[i] == nums[i - 1]:
                continue
            # do two sum
            l, r = i + 1, n - 1
            while l < r:
                _sum = nums[i] + nums[l] + nums[r]
                # equal is the closest
                if _sum == target:
                    return _sum
                # update res if we find a closer sum
                if abs(target - _sum) < abs(target - res):
                    res = _sum
                # two sum logic to move pointers
                if _sum < target:
                    l += 1
                else:
                    r -= 1
        return res
```
#### [18. 4Sum](https://leetcode.com/problems/4sum/)
```python
class Solution:
    def fourSum(self, nums: List[int], target: int) -> List[List[int]]:
        # idea
        # for each num do 3 sum
        #   for each num do 2 sum
        nums.sort()
        n = len(nums)
        res = []
        # 4 sum
        for i in range(n - 3):
            if i > 0 and nums[i] == nums[i - 1]:
                continue
            # 3 sum
            for j in range(i + 1, n - 2):
                if j > i + 1 and nums[j] == nums[j - 1]:
                    continue
                # 2 sum
                l, r = j + 1, n - 1
                while l < r:
                    _sum = nums[i] + nums[j] + nums[l] + nums[r]
                    if _sum == target:
                        res.append([nums[i], nums[j], nums[l], nums[r]])
                        l += 1
                        # skip duplicates
                        while l < r and nums[l] == nums[l - 1]:
                            l += 1
                        r -= 1
                        # skip duplicates
                        while l < r and nums[r] == nums[r + 1]:
                            r -= 1
                    elif _sum < target:
                        l += 1
                    else:
                        r -= 1
        return res
```
#### [611. Valid Triangle Number](https://leetcode.com/problems/valid-triangle-number/)
From the example 1, we can see `(2,3,4)` in result but not `(4,3,2)`, 
so we need to skip duplicates,
then we can define `1 <= a <= b <= c`, 
this can prevent to double count `(a,b,c)` and `(c,b,a)`,
since the sum of two edges of triangle is bigger than the 3rd, we know
`a + b > c` 
`a + c > b` 
`b + c > a`
from above inequations, since `1 <= a <= b <= c`,
`a + c > b` has to be true because `a + c >= a + b > b,`
`b + c > a` has to be true as well because `b + c >= a + a = 2a > a`,
therefore, we just need to consider the first inequation `a + b > c`,
and the question now becomes as below:

Find the numbers of triplets where `1 <= a <= b <= c` and `a + b > c`

```python
class Solution:
    def triangleNumber(self, nums: List[int]) -> int:
        # Find the numbers of triplets
        # where 1 <= a <= b <= c
        # and a + b > c
        nums.sort()  # this make sure 1 <= a <= b <= c
        ans = 0
        # starting from index 2 because we are enumerating with c
        for k in range(2, len(nums)):
            c = nums[k]
            i, j = 0, k - 1
            while i < j:
                a, b = nums[i], nums[j]
                if a + b > c:
                    ans += j - i
                    j -= 1
                else:
                    i += 1
        return ans
```
#### [923. 3Sum With Multiplicity](https://leetcode.com/problems/3sum-with-multiplicity/)
##### * this problem ask for num of tuples which can have duplicates
If the result is a count, and duplicates are allowed — think combinatorics.
need to handle nC2, multiple of duplicates
```python
class Solution:
    def threeSumMulti(self, arr: List[int], target: int) -> int:
        arr.sort()
        n = len(arr)
        res = 0
        _mod = (10 ** 9 + 7)
        for i in range(n):
            j, k = i + 1, n - 1
            while j < k:
                _sum = arr[i] + arr[j] + arr[k]
                if _sum == target:
                    # handle duplicates
                    # case 1:
                    if arr[j] == arr[k]:
                        nums_to_choose = k - j + 1
                        # we are choosing 2 nums in these many nums_to_choose
                        # formula of n choose 2 = C(n, 2) = n(n-1)/2
                        res += nums_to_choose * (nums_to_choose - 1) // 2
                        # mod within loop is best practice instead of at the end
                        res %= _mod
                        # we have calculated all the combinations
                        break
                    # case 2:
                    else:
                        # count and skip on left/j duplicates
                        j_duplicates = 1
                        while j + 1 < k and arr[j] == arr[j + 1]:
                            j_duplicates += 1
                            j += 1
                        # count and skip on right/k duplicates
                        k_duplicates = 1
                        while k - 1 > j and arr[k] == arr[k - 1]:
                            k_duplicates += 1
                            k -= 1
                        # the pairs we need is the multiple of the duplicates
                        res += j_duplicates * k_duplicates
                        # mod within loop is best practice instead of at the end
                        res %= _mod
                        j += 1
                        k -= 1
                elif _sum < target:
                    j += 1
                else:
                    k -= 1
        return res
```

#### [1577. Number of Ways Where Square of Number Is Equal to Product of Two Numbers](https://leetcode.com/problems/number-of-ways-where-square-of-number-is-equal-to-product-of-two-numbers/)
##### * this problem ask for num of tuples which can have duplicates
If the result is a count, and duplicates are allowed — think combinatorics.
need to handle nC2, multiple of duplicates
##### brute force with hash map
Time: `O(n^2 + m^2)`
Space:  `O(n + m)`
```python
class Solution:
    def numTriplets(self, nums1: List[int], nums2: List[int]) -> int:
        # naive brute force solution:
        # we care about nums1[i]^2, but there could be duplicates,
        # e.g. [1,1,2,2],
        # we can skip the duplicates to store nums1[i]^2 freq in a counter
        # if we found nums1[i]^2 == nums2[j] * nums2[k]
        # we increase the res by the the freq
        # since there's two types,
        # the total res is count(nums1, nums2) + count(nums2, nums1)
        def count(nums: List[int], target: List[int]) -> int:
            # init counter to skip duplicates
            cnt = Counter()
            for num in nums:
                cnt[num * num] += 1
            # brute forece to check nums1[i]^2 == nums2[j] * nums2[k]
            n = len(target)
            res = 0
            for j in range(n):
                for k in range(j + 1, n):
                    mul = target[j] * target[k]
                    if mul in cnt:
                        res += cnt[mul]
            return res
        # the total res is count(nums1, nums2) + count(nums2, nums1)
        return count(nums1, nums2) + count(nums2, nums1)
```
##### two pointer + sorting
Time: `O(nlogn) + O(mlogm) + O(n * m) = O(n * m) = O(n^2) if len(n) == len(m)` 
Space: `O(1)`
The hard part is to figure out the math to increase the res
```python
class Solution:
    def numTriplets(self, nums1: List[int], nums2: List[int]) -> int:
        def count(targets: List[int], nums: List[int]) -> int:
            res = 0
            for target in targets:
                square = target * target
                j, k = 0, len(nums) - 1
                while j < k:
                    mul = nums[j] * nums[k]
                    if mul == square:
                        if nums[j] == nums[k]:
                            nums_to_choose = k - j + 1
                            # we are choosing 2 nums within these many nums_to_choose
                            # formula of n choose 2 = C(n, 2) = n(n-1)/2
                            res += nums_to_choose * (nums_to_choose - 1) // 2
                            # we have calculated all the combinations
                            break
                        else:
                            # count and skip on left/j duplicates
                            j_duplicates = 1
                            while j + 1 < k and nums[j] == nums[j + 1]:
                                j_duplicates += 1
                                j += 1
                            # count and skip on right/k duplicates
                            k_duplicates = 1
                            while k - 1 > j and nums[k] == nums[k - 1]:
                                k_duplicates += 1
                                k -= 1
                            # the pairs we need is the multiple of the duplicates
                            res += j_duplicates * k_duplicates
                            # update pointers
                            j += 1
                            k -= 1
                    elif mul > square:
                        k -= 1
                    else:
                        j += 1
            return res
  
        # sort
        nums1.sort()
        nums2.sort()
  
        # the total res is count(nums1, nums2) + count(nums2, nums1)
        return count(nums1, nums2) + count(nums2, nums1)
```
#### [948. Bag of Tokens](https://leetcode.com/problems/bag-of-tokens/)
I made a mistake on using `while left < right`, in this problem, the token on right index is not consumed yet, only the right - 1 is, so we need to include the case that left = right to consume the last token on right index, therefore we need to use `while left <= right`.
```python
class Solution:
    def bagOfTokensScore(self, tokens: List[int], power: int) -> int:
        # each token we can:
        # 1. power >= token[i]:
        #       power -= token[i]
        #       score += 1
        # 2. score >= 1:
        #       power += token[i]
        #       score -= 1
        # goal:
        #   max score
        # 1. sort the tokens
        # 2. if power is enough
        #       face up on left to get score
        # 3. if power is not enough and score >= 1
        #       face down on right to get power
        tokens.sort()
        n = len(tokens)
        left = 0
        right = n - 1
        score = 0
        while left <= right:
            if power >= tokens[left]:
                power -= tokens[left]
                score += 1
                left += 1
            elif score > 0 and left + 1 < right:
                score -= 1
                power += tokens[right]
                right -= 1
            else:
                break
        return score
```
#### [11. Container With Most Water](https://leetcode.com/problems/container-with-most-water/)
```python
class Solution:
    def maxArea(self, height: List[int]) -> int:
        # the area depends on:
        # 1. the shorter line
        # 2. the len between two lines
        # so we can remove the shorter line after we update the area
        ans = 0
        n = len(height)
        l = 0
        r = n - 1
        while l < r:
            area = (r - l) * min(height[l], height[r])
            ans = max(ans, area)
            # remove the shorter line
            if height[l] <= height[r]:
                l += 1
            else:
                r -= 1
        return ans
```
#### [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
[盛最多水的容器 接雨水【基础算法精讲 02】](https://www.bilibili.com/video/BV1Qg411q7ia?spm_id_from=333.788.videopod.sections&vd_source=fb0d94742d314c399a695c3ec1b7dc6b)
##### Main Idea
The water trap depends on the smaller height
##### Dynamic Programing (storing pre and suf maxs)
Idea:
The water trap depends on the smaller height,
we can store two arrays of maxs, pre maxs and suf maxs,
then calculate each bucket water using pre maxs and suf maxs in the same index,
the equation is `min(pre max, sul max) - h`

Time: `O(n)`
Space: `O(n)`
```python
class Solution:
    def trap(self, height: List[int]) -> int:
        n = len(height)
        # init pre maxs
        pre_maxs = [0] * n
        pre_maxs[0] = height[0]
        for i in range(1, n):
            pre_maxs[i] = max(pre_maxs[i - 1], height[i])
        # init suf maxs
        suf_maxs = [0] * n
        suf_maxs[-1] = height[-1]
        for i in range(n - 2, -1, -1):
            suf_maxs[i] = max(suf_maxs[i + 1], height[i])
        # check for ans using pre and suf maxs
        res = 0
        for h, pre, sul in zip(height, pre_maxs, suf_maxs):
            res += min(pre, sul) - h
        return res
```
##### Two pointers
We have solve it with Dynamic programing by storing pre and suf maxs,
we can improve the Space to be `O(1)`

Main Idea:
The water trap depends on the smaller height of the bucket.
We keep track of pre max and suf max as we move the pointers,
if pre max smaller than suf max, we update res with `pre max - height[left]`
else with `suf max - height[right]`

Time:  `O(n)`
Space: `O(1)`
```python
class Solution:
    def trap(self, height: List[int]) -> int:
        n = len(height)
        pre_max = suf_max = left = res = 0
        right = n - 1
        while left < right:
            pre_max = max(pre_max, height[left])
            suf_max = max(suf_max, height[right])
            # water trap depends on the smaller edge
            if pre_max <= suf_max:
                res += pre_max - height[left]
                left += 1
            else:
                res += suf_max - height[right]
                right -= 1
        return res
```

#### [1616. Split Two Strings to Make Palindrome](https://leetcode.com/problems/split-two-strings-to-make-palindrome/)
##### Idea: Greedy + Two Pointers
1. greedily taking prefix a and suffix b (prefix b and suffix a) until they are not palindrome
2. check the middle part of a or b is palindrome or not

```python
class Solution:
    def checkPalindromeFormation(self, a: str, b: str) -> bool:
        def check(a: str, b: str) -> bool:
            n = len(a)
            left = 0
            right = n - 1
            # greedy to check for a(b) prefix and b(a) suffix
            while left < right and a[left] == b[right]:
                left += 1
                right -= 1
            # check if either of the middle part left is palindrome
            a_mid = a[left: right + 1]
            b_mid = b[left: right + 1]
            return a_mid == a_mid[::-1] or b_mid == b_mid[::-1]
        return check(a, b) or check(b, a)
```
#### [1498. Number of Subsequences That Satisfy the Given Sum Condition](https://leetcode.com/problems/number-of-subsequences-that-satisfy-the-given-sum-condition/)
```python
class Solution:
    def numSubseq(self, nums: List[int], target: int) -> int:
	    # after sorted

        # observation 1:
        # if nums[left] + nums[right] <= target
        # then
        # nums[left + 1] + nums[right] <= target
        # nums[left + 2] + nums[right] <= target
        # ...
        # nums[right - 1] + nums[right] <= target
  
        # observation 2:
        # for each element, we can either include or exclude it,
        # we have 2^n - 1 subset if we include the empty option,
        # if we fixed to an element nums[left],
        # we are not counting the empty option [],
        # so we don't need to -1
        # we need the result of 2^(right - left)
        nums.sort()
        n = len(nums)
        _mod = 10**9 + 7
        res = 0
        left = 0
        right = n - 1
        # we need all subset, so we need <= in stead of <
        while left <= right:
            _sum = nums[left] + nums[right]
            if _sum > target:
                right -= 1
            else:
                res += 2 ** (right - left)
                res %= _mod
                left += 1
        return res
```
##### using python build in pow(x, y, mod)
```python
class Solution:
    def numSubseq(self, nums: List[int], target: int) -> int:
        nums.sort()
        n = len(nums)
        _mod = 10**9 + 7
        res = 0
        left = 0
        right = n - 1
        # we need all subset, so we need <= in stead of <
        while left <= right:
            _sum = nums[left] + nums[right]
            if _sum > target:
                right -= 1
            else:
                res += pow(2, right - left, _mod)
                # ensure no overflow for the sum
                res %= _mod
                left += 1
        return res
```
##### Improved version with precompute power values
```python
class Solution:
    def numSubseq(self, nums: List[int], target: int) -> int:
        nums.sort()
        n = len(nums)
        _mod = 10**9 + 7
        # precompute 2^i % MOD for quick reference
        power = [1] * n
        for i in range(1, n):
            # ensure no overflow for 2^n
            power[i] = power[i - 1] * 2 % _mod
  
        res = 0
        left = 0
        right = n - 1
        # we need all subset, so we need <= in stead of <
        while left <= right:
            _sum = nums[left] + nums[right]
            if _sum > target:
                right -= 1
            else:
                res += power[right - left]
                # ensure no overflow for the sum
                res %= _mod
                left += 1
        return res
```

#### [1099. Two Sum Less Than K](https://leetcode.com/problems/two-sum-less-than-k/)
I made a mistake on also decreasing r when `sum < k` which is not needed.
```python
# Input: nums = [34,23,1,24,75,33,54,8], k = 60
# Output: 58
# Explanation: We can use 34 and 24 to sum 58 which is less than 60.

# Input: nums = [10,20,30], k = 15
# Output: -1
# Explanation: In this case it is not possible to get a pair sum less that 15.
class Solution:
    def twoSumLessThanK(self, nums: List[int], k: int) -> int:
        nums.sort()
        n = len(nums)
        l, r = 0, n - 1
        res = -1
        while l < r:
            _sum = nums[l] + nums[r]
            if _sum < k:
                res = max(res, _sum)
                l += 1
            else:
                r -= 1
        return res
```

#### [360. Sort Transformed Array](https://leetcode.com/problems/sort-transformed-array/)
![a>0](https://leetcode.com/problems/sort-transformed-array/Figures/360/Slide1.PNG)

![[Pasted image 20250513221218.png]]
Since the input array is sorted, as above picture, 
for `a > 0`, we can two pointers to pick the bigger transformed value, the revers is the result
for `a < 0`, we can two pointers to pick the smaller transformed value

I figured out the `a > 0` part, but didn't try hard to figure out the `a < 0`
```python
class Solution:
    def sortTransformedArray(self, nums: List[int], a: int, b: int, c: int) -> List[int]:
        def transform(x: int) -> int:
            return a * x * x + b * x + c
        n = len(nums)
        res = []
        left = 0
        right = n - 1
        if a > 0:
            # When 'upward parabola' or a 'straight line'
            # we will put the edge element (bigger elements) first.
            while left <= right:
                left_val = transform(nums[left])
                right_val = transform(nums[right])
                if left_val > right_val:
                    res.append(left_val)
                    left += 1
                else:
                    res.append(right_val)
                    right -= 1
            # Reverse the decreasing 'answer' array.
            res = res[::-1]
        else:
            # When 'downward parabola'
            # we will put the edge element (smaller elements) first
            while left <= right:
                left_val = transform(nums[left])
                right_val = transform(nums[right])
                if left_val < right_val:
                    res.append(left_val)
                    left += 1
                else:
                    res.append(right_val)
                    right -= 1
        return res
```
#### [2422. Merge Operations to Turn Array Into a Palindrome](https://leetcode.com/problems/merge-operations-to-turn-array-into-a-palindrome/)
```python
class Solution:
    def minimumOperations(self, nums: List[int]) -> int:
        # [4,3,2,1,2,3,1]
        #    ^     ^
        # [4,7,9,10,12,15,16]
  
        # [16,12,9,7,6,4,1]
  
        # [4,3,2,1,2,4]

        # [4,3,2,3,4]

        # main point:
        # palindrome should have the same sum from
        # left to right or right to left

        # move the pointer which has less sum until the sum equal to the element
        # increase the operation counter when moving
        # if sum is the same, move both the pointers

        n = len(nums)
        left = 0
        right = n - 1
        l_sum = nums[0]
        r_sum = nums[-1]
        res = 0
        while left < right:
            if l_sum < r_sum:
                left += 1
                l_sum += nums[left]
                res += 1
            elif l_sum > r_sum:
                right -= 1
                r_sum += nums[right]
                res += 1
            else:
                left += 1
                l_sum += nums[left]
                right -= 1
                r_sum += nums[right]
        return res
```
##### Improved version
```python
class Solution:
    def minimumOperations(self, nums: List[int]) -> int:
        n = len(nums)
        left = 0
        right = n - 1
        res = 0
        while left < right:
            if nums[left] < nums[right]:
                # merge to next left
                nums[left + 1] += nums[left]
                left += 1
                res += 1
            elif nums[left] > nums[right]:
                # merge to next right
                nums[right - 1] += nums[right]
                right -= 1
                res += 1
            else:
                # skip both
                left += 1
                right -= 1
  
        return res
```
#### [259. 3Sum Smaller](https://leetcode.com/problems/3sum-smaller/)
I made a mistake on adding which is not needed, because the question is asking for all combination smaller than target
```python
if i > 0 and nums[i] == nums[i - 1]:
    continue
```

```python
class Solution:
    def threeSumSmaller(self, nums: List[int], target: int) -> int:
        nums.sort()
        n = len(nums)
        res = 0
        for i in range(n - 2):
            # skip the rest if sum bigger than target
            if nums[i] + nums[i + 1] + nums[i + 2] > target:
                break
            j = i + 1
            k = n - 1
            t = target - nums[i]
            while j < k:
                s = nums[j] + nums[k]
                if s < t:
                    # if nums[j] + nums[k] < t,
                    # nums[j] + nums[k - 1] < t, nums[j] + nums[k - 2] < t,
                    # we need to add all these combination to result
                    res += k - j
                    j += 1
                else:
                    k -= 1
        return res
```
## NeetCode
| #   | Difficulty                                 | Problems                                                                                                   |                         |
| --- | ------------------------------------------ | ---------------------------------------------------------------------------------------------------------- | ----------------------- |
| 1   | <span style="color: green;">Easy</span>    | [88. Merge Sorted Array](https://leetcode.com/problems/merge-sorted-array/)                                | <input type="checkbox"> |
| 2   | <span style="color: green;">Easy</span>    | [125. Valid Palindrome](https://leetcode.com/problems/valid-palindrome/)                                   | <input type="checkbox"> |
| 3   | <span style="color: orange;">Medium</span> | [167. Two Sum II - Input Array Is Sorted](https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/) | <input type="checkbox"> |
| 4   | <span style="color: orange;">Medium</span> | [15. 3Sum](https://leetcode.com/problems/3sum/)                                                            | <input type="checkbox"> |
| 5   | <span style="color: orange;">Medium</span> | [11. Container With Most Water](https://leetcode.com/problems/container-with-most-water/)                  | <input type="checkbox"> |
| 6   | <span style="color: red;">Hard</span>      | [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)                              | <input type="checkbox"> |

## Grokking the Coding Interview

| #   | Difficulty                                 | Problems                                                                                                                                                       |                                 |
| --- | ------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------- |
| 1   | <span style="color: green;">Easy</span>    | [345. Reverse Vowels of a String](https://leetcode.com/problems/reverse-vowels-of-a-string/)                                                                   | <input type="checkbox" checked> |
| 2   | <span style="color: green;">Easy</span>    | [167. Two Sum II - Input Array Is Sorted](https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/)                                                     | <input type="checkbox" checked> |
| 3   | <span style="color: green;">Easy</span>    | [Find Non-Duplicate Number Instances (easy)](https://www.designgurus.io/course-play/grokking-the-coding-interview/doc/find-nonduplicate-number-instances-easy) | <input type="checkbox" checked> |
| 4   | <span style="color: green;">Easy</span>    | [977. Squares of a Sorted Array](https://leetcode.com/problems/squares-of-a-sorted-array/)                                                                     | <input type="checkbox" checked> |
| 5   | <span style="color: orange;">Medium</span> | [15. 3Sum](https://leetcode.com/problems/3sum/)                                                                                                                | <input type="checkbox" checked> |
| 6   | <span style="color: orange;">Medium</span> | [16. 3Sum Closest](https://leetcode.com/problems/3sum-closest/)                                                                                                | <input type="checkbox" checked> |
| 7   | <span style="color: orange;">Medium</span> | [Triplet Sum Close to Target (medium)](https://www.designgurus.io/course-play/grokking-the-coding-interview/doc/triplet-sum-close-to-target-medium)            | <input type="checkbox" checked> |
| 8   | <span style="color: orange;">Medium</span> | [259. 3Sum Smaller](https://leetcode.com/problems/3sum-smaller/)                                                                                               | <input type="checkbox" checked> |
| 9   | <span style="color: orange;">Medium</span> | [75. Sort Colors](https://leetcode.com/problems/sort-colors/)                                                                                                  | <input type="checkbox" checked> |
| 10  | <span style="color: orange;">Medium</span> | [18. 4Sum](https://leetcode.com/problems/4sum/)                                                                                                                | <input type="checkbox" checked> |
| 11  | <span style="color: green;">Easy</span>    | [844. Backspace String Compare](https://leetcode.com/problems/backspace-string-compare/)                                                                       | <input type="checkbox" checked> |
| 12  | <span style="color: orange;">Medium</span> | [581. Shortest Unsorted Continuous Subarray](https://leetcode.com/problems/shortest-unsorted-continuous-subarray/)                                             | <input type="checkbox" checked> |

### [Find Non-Duplicate Number Instances (easy)](https://www.designgurus.io/course-play/grokking-the-coding-interview/doc/find-nonduplicate-number-instances-easy)
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

### [977. Squares of a Sorted Array](https://leetcode.com/problems/squares-of-a-sorted-array/)
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

### [15. 3Sum](https://leetcode.com/problems/3sum/)
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

### [16. 3Sum Closest](https://leetcode.com/problems/3sum-closest/)
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

### [Triplet Sum Close to Target (medium)](https://www.designgurus.io/course-play/grokking-the-coding-interview/doc/triplet-sum-close-to-target-medium)
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

### [259. 3Sum Smaller](https://leetcode.com/problems/3sum-smaller/)
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

### [75. Sort Colors](https://leetcode.com/problems/sort-colors/)
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
### [18. 4Sum](https://leetcode.com/problems/4sum/)
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
### [844. Backspace String Compare](https://leetcode.com/problems/backspace-string-compare/)
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

### [581. Shortest Unsorted Continuous Subarray](https://leetcode.com/problems/shortest-unsorted-continuous-subarray/)
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

