# Warmup
## Grokking the Coding Interview

| #   | Difficulty                              | Problems                                                                                                  | Topic              |                                 |
| --- | --------------------------------------- | --------------------------------------------------------------------------------------------------------- | ------------------ | ------------------------------- |
| 1   | <span style="color: green;">Easy</span> | [217. Contains Duplicate](https://leetcode.com/problems/contains-duplicate/)                              | #sorting #hash-set | <input type="checkbox" checked> |
| 2   | <span style="color: green;">Easy</span> | [1832. Check if the Sentence Is Pangram](https://leetcode.com/problems/check-if-the-sentence-is-pangram/) | #hash-set #ASCII   | <input type="checkbox" checked> |
| 3   | <span style="color: green;">Easy</span> | [345. Reverse Vowels of a String](https://leetcode.com/problems/reverse-vowels-of-a-string/)              | #two-pointers      | <input type="checkbox" checked> |
| 4   | <span style="color: green;">Easy</span> | [125. Valid Palindrome](https://leetcode.com/problems/valid-palindrome/)                                  | #two-pointers      | <input type="checkbox" checked> |
| 5   | <span style="color: green;">Easy</span> | [242. Valid Anagram](https://leetcode.com/problems/valid-anagram/)                                        | #sorting #hash-map | <input type="checkbox" checked> |
| 6   | <span style="color: green;">Easy</span> | [243. Shortest Word Distance](https://leetcode.com/problems/shortest-word-distance/)                      |                    | <input type="checkbox" checked> |
| 7   | <span style="color: green;">Easy</span> | [1512. Number of Good Pairs](https://leetcode.com/problems/number-of-good-pairs/)                         | #hash-map          | <input type="checkbox" checked> |
| 8   | <span style="color: green;">Easy</span> | [69. Sqrt(x)](https://leetcode.com/problems/sqrtx/)                                                       | #binary-search     | <input type="checkbox" checked> |

# [217. Contains Duplicate](https://leetcode.com/problems/contains-duplicate/)

| Solutions   | Time       |                                                                  | Space  |                                                    |
| ----------- | ---------- | ---------------------------------------------------------------- | ------ | -------------------------------------------------- |
| brute force | $O(n^2)$   | nested loop                                                      | $O(1)$ |                                                    |
| sorting     | $O(nlogn)$ | sorting cost O(nlogn), loop through to check duplicate cost O(n) | $O(1)$ |                                                    |
| hash set    | $O(n)$     | loop through to create a set cost O(n)                           | $O(n)$ | an additional set of element would cost O(n) space |
# [1832. Check if the Sentence Is Pangram](https://leetcode.com/problems/check-if-the-sentence-is-pangram/)

| Solutions   | Time   |                                                                     | Space  |                              |
| ----------- | ------ | ------------------------------------------------------------------- | ------ | ---------------------------- |
| brute force | $O(n)$ | loop over array 26 times to find each character                     | $O(1)$ |                              |
| hash set    | $O(n)$ | loop through to create a set cost O(n), then check the length is 26 | $O(1)$ | storing the set cost O(26)   |
| Using ASCII | $O(n)$ | using `ord(char) - ord('a')` to                                     | $O(1)$ | storing the array cost O(26) |
# [345. Reverse Vowels of a String](https://leetcode.com/problems/reverse-vowels-of-a-string/)

| Solutions    | Time     |                                                 | Space  |                                                           |
| ------------ | -------- | ----------------------------------------------- | ------ | --------------------------------------------------------- |
| brute force  | $O(n^2)$ | nested loop to check for each vowels pairs      | $O(1)$ |                                                           |
| two pointers | $O(n)$   | left and right pointer to check pairs cost O(n) | $O(n)$ | need to store and array of result and convert back to str |

## Python Note
```python
# to check a char in a string
# 1. 
if char in string:
# 2. 
s.find(char) == - 1

# to convert a string to char array
str_array = list(string)
# to convert a char array to string
''.join(str_array)
```

# [125. Valid Palindrome](https://leetcode.com/problems/valid-palindrome/)

| Solutions    | Time   |                                                                            | Space  |     |
| ------------ | ------ | -------------------------------------------------------------------------- | ------ | --- |
| two pointers | $O(n)$ | left and right pointer to check the char pairs from the start and end O(n) | $O(1)$ |     |
## Python Note
```python
# to check a char is alphanumeric
char.isalnum()
# convert a char to lower or uper
char.lower()
char.upper()
```

# [242. Valid Anagram](https://leetcode.com/problems/valid-anagram/)

| Solutions                     | Time       |                                                                                                                                              | Space  |                                 |
| ----------------------------- | ---------- | -------------------------------------------------------------------------------------------------------------------------------------------- | ------ | ------------------------------- |
| sorting                       | $O(nlogn)$ | convert the string to char array, sort two of these char arrays, then loop to compare the two arrays                                         | $O(1)$ |                                 |
| count frequency with hash map | $O(n)$     | loop through two string to store frequency of each char,   +1 for found 1 in string1, -1 for found 1 in string2, check if all 0s in hash map | $O(1)$ | storing the hash map cost O(26) |
## Python Note
```python
# to avoid getting compilation error with dictionary
hashmap[char] = 1 + hashmap.get(char, 0)  # return 0 if cannot find char
```

# [243. Shortest Word Distance](https://leetcode.com/problems/shortest-word-distance/)

| Solutions   | Time       |                                                                                                                            | Space  |     |
| ----------- | ---------- | -------------------------------------------------------------------------------------------------------------------------- | ------ | --- |
| brute force | $O(n^2)$   | nested loop to go through the array                                                                                        | $O(1)$ |     |
| one pass    | $O(N + M)$ | loop through array once to capture the index of word1 and word2, and keep checking the current min distance if we found it | $O(1)$ |     |
## Python Note
```python
# to get absolute value
abs(l - r)
# to get min or max value of two
min(l, r)
max(l, r)
```

# [1512. Number of Good Pairs](https://leetcode.com/problems/number-of-good-pairs/)

| Solutions   | Time     |                                                                                                                                                                                  | Space  |                      |
| ----------- | -------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ | -------------------- |
| brute force | $O(n^2)$ | nested loop to go through the array                                                                                                                                              | $O(1)$ |                      |
| hash map    | $O(n)$   | loop through array once, store each num and its frequency pair in hash map, every new occurrence of num can be paired with every previous occurrence, new pairs is frequency - 1 | $O(n)$ | storing the hash map |
# [69. Sqrt(x)](https://leetcode.com/problems/sqrtx/)

| Solutions     | Time      |                                                                  | Space  |     |
| ------------- | --------- | ---------------------------------------------------------------- | ------ | --- |
| binary search | $O(logn)$ | think of we are binary searching for a number between 2 and x//2 | $O(1)$ |     |

## Python Note
```python
# to get mid in binary search
l + (r - l) // 2  # this is to prevent overflow
# binary search template
l, r = -1, len(input)
while l + 1 != r:
	mid = l + (r - l)  // 2
	if isBlue(mid):
		mid = r
	else:
		mid = l
return l or r depends on the question
	
```

