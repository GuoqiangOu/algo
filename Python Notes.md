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
