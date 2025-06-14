2025-05-17:
Opposite Direction Two Pointers
1. [LCP 28. 采购方案](https://leetcode.cn/problems/4xy4Wx/)
2. [611. Valid Triangle Number](https://leetcode.com/problems/valid-triangle-number/)
	1. made mistake on fixing a instead of c to use opposite direction two pointers
	2. need to think of c is the target, similar to 2 or 3 sums
3. [1471. The k Strongest Values in an Array](https://leetcode.com/problems/the-k-strongest-values-in-an-array/)
4. [1099. Two Sum Less Than K](https://leetcode.com/problems/two-sum-less-than-k/)
5. [2105. Watering Plants II](https://leetcode.com/problems/watering-plants-ii/)
6. [16. 3Sum Closest](https://leetcode.com/problems/3sum-closest/)
7. [259. 3Sum Smaller](https://leetcode.com/problems/3sum-smaller/)

2025-05-18:
Opposite Direction Two Pointers
1. [948. Bag of Tokens](https://leetcode.com/problems/bag-of-tokens/)

2025-05-19:
Opposite Direction Two Pointers
1. [1577. Number of Ways Where Square of Number Is Equal to Product of Two Numbers](https://leetcode.com/problems/number-of-ways-where-square-of-number-is-equal-to-product-of-two-numbers/)
	1. we need to count for all combinations (triplets, pairs) for
		1. square == multiple
		2. `nums1[i]² == nums2[j] * nums2[k]`
		3. `nums2[i]² == nums1[j] * nums1[k]`
	2. on `square == a * b`
		1. if `a == b` 
			1. we have n choose 2 combinations to be counted
				1. `nC2 = n * (n-1)//2`
		2. if a != b
			1. count duplicates from left
			2. count duplicates from right
			3. multiply counts of duplicates is the combinations we need

2025-05-20:
Opposite Direction Two Pointers
1. [1577. Number of Ways Where Square of Number Is Equal to Product of Two Numbers](https://leetcode.com/problems/number-of-ways-where-square-of-number-is-equal-to-product-of-two-numbers/)
2. [360. Sort Transformed Array](https://leetcode.com/problems/sort-transformed-array/)
	1. f(x) = ax2 + bx + c
	2. if a > 0: 
		1. upward parabola
		2. larger values are on the ends
		3. fill res from largest to smallest, then reverse
	3. if a < :
		1. downward parabola
		2. larger values are in the middle
		3. fill res from smallest to largest (no reverse)

2025-05-21:
Opposite Direction Two Pointers
1. [1577. Number of Ways Where Square of Number Is Equal to Product of Two Numbers](https://leetcode.com/problems/number-of-ways-where-square-of-number-is-equal-to-product-of-two-numbers/)
2. [360. Sort Transformed Array](https://leetcode.com/problems/sort-transformed-array/)
3. [2422. Merge Operations to Turn Array Into a Palindrome](https://leetcode.com/problems/merge-operations-to-turn-array-into-a-palindrome/)
	1. sum will be the same if palindrome
	2. move the smaller pointer, add the previous num and add count

2025-05-22:
Opposite Direction Two Pointers
1. [360. Sort Transformed Array](https://leetcode.com/problems/sort-transformed-array/)
2. [1577. Number of Ways Where Square of Number Is Equal to Product of Two Numbers](https://leetcode.com/problems/number-of-ways-where-square-of-number-is-equal-to-product-of-two-numbers/)
3. [923. 3Sum With Multiplicity](https://leetcode.com/problems/3sum-with-multiplicity/)
4. [2563. Count the Number of Fair Pairs](https://leetcode.com/problems/count-the-number-of-fair-pairs/)
	1. when result is with in a range, think of a set - another one
	2. figure out how to find the res of these two set

2025-05-23
Opposite Direction Two Pointers
1. [1616. Split Two Strings to Make Palindrome](https://leetcode.com/problems/split-two-strings-to-make-palindrome/)
	1. from left to right check pre and suf till the diff char
	2. check `[l : r + 1]` for either a or b is palindrome or not
	3. check for (a, b) or (b, a)

2025-05-24
Opposite Direction Two Pointers
1. [1498. Number of Subsequences That Satisfy the Given Sum Condition](https://leetcode.com/problems/number-of-subsequences-that-satisfy-the-given-sum-condition/)
	1. sort
	2. `while l <= r`
		1. because subsequence can have only 1 element
	3. `2^(r-l)`, not `nC2`
		1. if `nums[l] + nums[r] <= target`, then all sums using elements in `[l, r] <= target`
		2. nC2 counts all pairs, but question asks to count all subsequences including those has only 1 element
		3. fixing one element, and choosing the other, we have two options, to add or not to add it, so it's `2^(r-l)`
2. [1577. Number of Ways Where Square of Number Is Equal to Product of Two Numbers](https://leetcode.com/problems/number-of-ways-where-square-of-number-is-equal-to-product-of-two-numbers/)
3. [923. 3Sum With Multiplicity](https://leetcode.com/problems/3sum-with-multiplicity/)

2025-05-25
Rested

2025-05-26
Opposite Direction Two Pointers
1. [923. 3Sum With Multiplicity](https://leetcode.com/problems/3sum-with-multiplicity/)
	1. `left == right: nC2 = n(n - 1)/2`
	2. `left != right: left duplicates * right duplicates`
2. [1577. Number of Ways Where Square of Number Is Equal to Product of Two Numbers](https://leetcode.com/problems/number-of-ways-where-square-of-number-is-equal-to-product-of-two-numbers/)
	1. sort
	2. `count(nums1, nums2) + count(nums2, nums1)`
	3.  `left == right: nC2 = n(n - 1)/2`
	4. `left != right: left duplicates * right duplicates`
3. [1498. Number of Subsequences That Satisfy the Given Sum Condition](https://leetcode.com/problems/number-of-subsequences-that-satisfy-the-given-sum-condition/)
	1. sort
	2. `whlie l <= r`
	3. `left + right <= target`
		1. to count all **non-empty** combinations, we can either pick or not pick a num
		2. it is `2^n where n = r - l`

2025-05-27
Was preparing self introduction for BQ

2025-05-28
Opposite Direction Two Pointers
1. [11. Container With Most Water](https://leetcode.com/problems/container-with-most-water/)
	1. area depends on the smaller height, so `min(l, r) * (r - l)`
2. [15. 3Sum](https://leetcode.com/problems/3sum/)
	1. made mistake on using `l = 0` instead of `l = i + 1`
	2. made mistake on skipping duplicates
		1. if updated pointers, 
			1. left need to check `nums[l] == nums[l - 1]`
			2. right need to check `nums[r] == nums[r + 1]`
3. [611. Valid Triangle Number](https://leetcode.com/problems/valid-triangle-number/)
	1. the Triangle Inequality Theorem
		1. fixing the biggest `c` and `a <= b <= c` with sorted
		2. `a + c >= a + b > b` -> `a + c > b`
		3. `b + c >= a + a > a` -> `b + c > b`
		4. so we just need to check if `a + b > c`
	2. res to be updated with `r - l` because
		1. if `nums[l] + nums[r] > nums[i]`
		2. then `nums[l + 1] + nums[r] > nums[i]` since `nums[l] < nums[l + 1]`

Same Direction Two Pointers
1. [283. Move Zeroes](https://leetcode.com/problems/move-zeroes/)
	1. `left point to the 0`
	2. `right point to the next value`
	3. if right is non 0, we swap left with right


2025-05-29
Two Pointers
1. [75. Sort Colors](https://leetcode.com/problems/sort-colors/)
	1. `i` to go through each num
	2. `l and r` keep track of 0s and 2s
	3. 0: swap with left, update left and `i`
	4. 1: no swap, update `i`
	5. 2: swap with right, update right, do not update `i`
	6. made a mistake on updating `i` for all cases
2. [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
	1. create `pre_max` and `suf_max` arrays
	2. loop through heights to calculate and add up to res
		1. `volume = min(pre_max, suf_max) - current height`
	3. improvement to `O(1)` space:
		1. we store the `pre_max` and `suf_max` as variables instead of arrays
		2. two pointers 
			1. to update `pre` and `suf_max`
			2. move and update base on the smaller pointer
			3. calculate and update the volume with the smaller height

2025-05-30
Sliding Window
1. [3. Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
	1. need to check duplicates -> hashmap or set
	2. longest substring, unknown len -> flexible sliding window
	3. into window
	4. while invalid
		1. out of window
	5. update res
2. [424. Longest Repeating Character Replacement](https://leetcode.com/problems/longest-repeating-character-replacement/)
	1. looks like flexible sliding window but not sure
	2. need to check duplicates for frequency -> counter/hashmap
	3. valid: `r - l + 1 - most appear char num <= k`
	4. invalid: `r - l + 1 - most appear char num > k`
	5. into window: add count and update max frequency
	6. if invalid: out of window
	7. update res

sad, I almost forgot about how to solve sliding window problem ...

2025-05-31
Sliding Window
1. [Maximum Sum of Subarrays of Size K](https://www.hellointerview.com/learn/code/sliding-window/maximum-sum-of-subarrays-of-size-k)
2. [2461. Maximum Sum of Distinct Subarrays With Length K](https://leetcode.com/problems/maximum-sum-of-distinct-subarrays-with-length-k/)
	1. my approch
		1. into window
		2. shrink window while has duplicate and len > k
		3. update res
	2. 灵神
		1. into window
		2. extend to window size
		3. check hashmap  len == k to update res
		4. out of window
3. [1423. Maximum Points You Can Obtain from Cards](https://leetcode.com/problems/maximum-points-you-can-obtain-from-cards/)
	1. first k
	2. last k
	3. first + last = k
	4. loop to get score at start
	5. `while i > 0:`
		1. start out
		2. tail in
		3. update res
4. [1456. Maximum Number of Vowels in a Substring of Given Length](https://leetcode.com/problems/maximum-number-of-vowels-in-a-substring-of-given-length/)
	1. into window if right is vowels
	2. extend to k size
	3. update res
	4. out of window if left is vowels
5. [643. Maximum Average Subarray I](https://leetcode.com/problems/maximum-average-subarray-i/)
	1. res = -inf
	2. right into window to add sum
	3. extend to k size
	4. update res with max avg
	5. left out of window to reduce sum
6. 