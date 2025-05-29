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
