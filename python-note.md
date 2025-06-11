```python
# [345. Reverse Vowels of a String](https://leetcode.com/problems/reverse-vowels-of-a-string/)
# to check a char in a string
# 1. 
if char in string:
# 2. 
s.find(char) == - 1

# to convert a string to char array
str_array = list(string)
# to convert a char array to string
''.join(str_array)

# [125. Valid Palindrome](https://leetcode.com/problems/valid-palindrome/)
# to check a char is alphanumeric
char.isalnum()
# convert a char to lower or uper
char.lower()
char.upper()

# [242. Valid Anagram](https://leetcode.com/problems/valid-anagram/)
# to avoid getting compilation error with dictionary
hashmap[char] = 1 + hashmap.get(char, 0)  # return 0 if cannot find char

# [243. Shortest Word Distance](https://leetcode.com/problems/shortest-word-distance/)
# to get absolute value
abs(l - r)
# to get min or max value of two
min(l, r)
max(l, r)

# [704. Binary Search](https://leetcode.com/problems/binary-search/)
# nums[l] is target is not the same as nums[l] == target
# if checking number in arr the same as a number, use '==' instead of 'is'
nums[l] == target

# [875. Koko Eating Bananas](https://leetcode.com/problems/koko-eating-bananas/)
# to get the smallest int <= to a/b
math.ceil(a/b)

# [16. 3Sum Closest](https://leetcode.com/problems/3sum-closest/)
# to get infinity
infinite = float("inf")
negative_infinite = float("-inf")
# to get distance between two numbers
abs(num1 - num2)

# [202. Happy Number](https://leetcode.com/problems/happy-number/)
# to get last digit or a number
digit = n % 10
# to get other digits
other_digit = n // 10
# to get a square sum of a number (e.g. 123 -> 1^2 + 2^2 + 3^2 = 14)
def squareSum(n):
	squareSum = 0
	while n > 0:
		digit = n % 10
		squareSum += digit * digit
		n //= 10
	return squareSum

# [234. Palindrome Linked List](https://leetcode.com/problems/palindrome-linked-list/)
# to reverse linked list
# [206. Reverse Linked List](https://leetcode.com/problems/reverse-linked-list/)
prev = None
curr = head
while curr:
	tmp = curr.next
	curr.next = prev
	prev = curr
	curr = tmp
return prev

# to check more than one conditions in one line
# [1234. Replace the Substring for Balanced String](https://leetcode.com/problems/replace-the-substring-for-balanced-string/)
# `all()` checks if every value in the generator is `True`.
while all(counts[c] <= target for c in 'QWER'):
# equals to below 
while counts['Q'] <= target and counts['W'] <= target \\
and counts['E'] <= target and counts['R'] <= target:

# to compare two counters, python will ignore the key only appear in one counter
# [76. Minimum Window Substring](https://leetcode.com/problems/minimum-window-substring/)
A = {'A': 2, 'B': 2, 'C': 2, 'D': 1}
B = {'A': 3, 'B': 2, 'C': 2}
# A >= B is False

# to check if a str is palindrome
# [1616. Split Two Strings to Make Palindrome](https://leetcode.com/problems/split-two-strings-to-make-palindrome/)
s == s[::-1]

# to find lower bound, the idx of 1st num >= target
# [2563. Count the Number of Fair Pairs](https://leetcode.com/problems/count-the-number-of-fair-pairs/)
bisect_left(arr, target, startIdx, endEdx)

# to find upper bound, the idx of 1st num > target
# [2563. Count the Number of Fair Pairs](https://leetcode.com/problems/count-the-number-of-fair-pairs/)
bisect_right(arr, target, startIdx, endEdx)


