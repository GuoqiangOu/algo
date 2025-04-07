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


