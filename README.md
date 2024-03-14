# LeetCode

## Table of Contents

1. [Big O Notation and Time Complexity](#Big-O-Notation-and-Time-Complexity)
- [Linear Time](#Linear-Time)
- [Constant Time](#Constant-Time)
- [N squared Time](#N-squared-Time)

## 1. Big O Notation and Time Complexity
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

<!-- **Training Set:** -->