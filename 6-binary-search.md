# Binary Search
# Template
```python
def binary_search(arr: List[int], target: int) -> int:
    l, r = 0, len(arr) - 1
    first_true_index = -1
    while left <= right:
        mid = (l + r) // 2 # or mid = l + (r - l) // 2
        if feasible(mid):
            first_true_index = mid
            r = mid - 1
        else:
            l = mid + 1

    return first_true_index
```

# [二分查找为什么总是写错？](https://www.bilibili.com/video/BV1d54y1q7k7/?spm_id_from=333.337.search-card.all.click&vd_source=fb0d94742d314c399a695c3ec1b7dc6b)
## Steps
1. define the condition()
2. define what to return, l or r
3. use the template
4. any other thing to be handled
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
| Difficulty                                 | Problems                                                                                                         |                         |
| ------------------------------------------ | ---------------------------------------------------------------------------------------------------------------- | ----------------------- |
| <span style="color: green;">Easy</span>    | [704. Binary Search](https://leetcode.com/problems/binary-search/)                                               | <input type="checkbox"> |
| <span style="color: orange;">Medium</span> | [74. Search a 2D Matrix](https://leetcode.com/problems/search-a-2d-matrix/)                                      | <input type="checkbox"> |
| <span style="color: orange;">Medium</span> | [875. Koko Eating Bananas](https://leetcode.com/problems/koko-eating-bananas/)                                   | <input type="checkbox"> |
| <span style="color: orange;">Medium</span> | [153. Find Minimum in Rotated Sorted Array](https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/) | <input type="checkbox"> |
| <span style="color: orange;">Medium</span> | [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)              | <input type="checkbox"> |
| <span style="color: orange;">Medium</span> | [981. Time Based Key-Value Store](https://leetcode.com/problems/time-based-key-value-store/)                     | <input type="checkbox"> |
| <span style="color: red;">Hard</span>      | [4. Median of Two Sorted Arrays](https://leetcode.com/problems/median-of-two-sorted-arrays/)                     | <input type="checkbox"> |
