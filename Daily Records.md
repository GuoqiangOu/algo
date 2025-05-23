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