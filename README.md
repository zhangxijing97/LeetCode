# LeetCode

## Table of Contents

1. [Big O Notation and Time Complexity](#Big-O-Notation-and-Time-Complexity)
- [Linear Time](#Linear-Time)
- [Constant Time](#Constant-Time)
- [N squared Time](#N-squared-Time)
- [Logn Time](#Logn-Time)
- [n*Logn Time](#n*Logn-Time)
- [2^n](#2^n)

2. [Lambda Expressions](#Lambda-Expressions)

## Big O Notation and Time Complexity
[Big O Cheat Sheet](https://www.bigocheatsheet.com/)
|                                       |                                       |
| ------------------------------------- | ------------------------------------- |
| ![Alt Text](Image/BigONotation01.jpg) | ![Alt Text](Image/BigONotation02.jpg) |
### Linear Time
**O(n)**<br>
```
int addUp(int n){
    int sum = 0;
    for(int i = 0; i <= n; i++) {
        sum += 1;
    }
    return sum;
}
```
n = 1000<br>
1000 steps<br>

**More example:**<br>
```
# Array
nums = [1, 2, 3]
nums.append(4) # push to end
nums.pop()     # pop from end
nums[0]        # lookup
nums[1] 
nums[2]

# HashMap / Set
hashMap = {}
hashMap["key"] = 10      # insert
print("key" in hashMap)  # lookup
print(hashMap["key"])    # lookup
hashMap.pop("key")       # remove
```

### Constant Time
**O(1)**<br>
```
int addUp (int n){
    int sum = n * (p + 1) / 2;
    return sum;
}
```
n = 1000<br>
3 steps<br>

**More example:**<br>
```
nums = [1, 2, 3]
sum(nums)            # sum of array
for n in nums:       # looping
    print (n)

nums.insert(1, 100)  # insert middle 
nums.remove(100)     # remove middle
print(100 in nums)   # search

import heapq
heapq.heapify(nums)  # build heap
```

### N squared Time
```
nums = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
for i in range(len (nums)):
    for j in range(len (nums [i])):
        print(nums[i][jl)
```

### Logn Time
```
# Binary search
nums = [1, 2, 3, 4, 5]
target = 6
1, r = 0, len (nums) - 1
while 1 <= r:
    m = (1 + r) // 2
    if target < nums [m]:
        r = m - 1
    elif target > nums [m]:
        1 = m + 1
    else:
        print(m)
        break
```
```
# Heap Push and Pop
import heapq
minHeap = []
heapq.heappush(minHeap, 5)
heapq.heappop(minHeap)
```

### n*Logn Time
```
# HeapSort
import heapq
nums = [1, 2, 3, 4, 5]
heapq.heapify(nums) # 0(n)
while nums:
    heapq. heappop(nums) # O(logn)

# MergeSort
# (and most built-in sorting functions)
```

### 2^n
```
# Recursion, tree height, two branches
def recursion(i, nums):
    if i == len(nums):
        return 0
branch1 = recursion(i + 1, nums)
branch2 = recursion(i + 2, nums)
```

## Lambda Expressions
Example 1: A Simple Lambda Function<br>
```
add_ten = lambda x: x + 10
print(add_ten(5))  # Output: 15
```

Example 2: Lambda with Multiple Arguments<br>
```
multiply = lambda x, y: x * y
print(multiply(2, 3))  # Output: 6
```

Example 3: Lambda in ‘map()’ Function<br>
```
numbers = [1, 2, 3, 4]
squared = map(lambda x: x**2, numbers)

print(list(squared))  # Output: [1, 4, 9, 16]
```

Example 4: Lambda in 'filter()' Function<br>
```
numbers = [1, 2, 3, 4, 5, 6]
even_numbers = filter(lambda x: x % 2 == 0, numbers)

print(list(even_numbers))  # Output: [2, 4, 6]
```