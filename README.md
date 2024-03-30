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

3. [Regular Expressions](#Regular-Expressions)

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
### A Simple Lambda Function
```
add_ten = lambda x: x + 10
print(add_ten(5))  # Output: 15
```

### Lambda with Multiple Arguments
```
multiply = lambda x, y: x * y
print(multiply(2, 3))  # Output: 6
```

### Lambda in ‘map()’ Function
```
numbers = [1, 2, 3, 4]
squared = map(lambda x: x**2, numbers)

print(list(squared))  # Output: [1, 4, 9, 16]
```

### Lambda in 'filter()' Function
```
numbers = [1, 2, 3, 4, 5, 6]
even_numbers = filter(lambda x: x % 2 == 0, numbers)

print(list(even_numbers))  # Output: [2, 4, 6]
```

### Lambda in 'sorted()' Function
```
pairs = [(1, 'one'), (2, 'two'), (3, 'three'), (4, 'four')]
sorted_pairs = sorted(pairs, key=lambda pair: pair[1])

print(sorted_pairs)  # Output: [(4, 'four'), (1, 'one'), (3, 'three'), (2, 'two')]
```

### Lambda in 'max()' Function
```
people = [
    {"name": "John", "age": 45},
    {"name": "Diana", "age": 35},
    {"name": "Anna", "age": 25},
    {"name": "Mike", "age": 30}
]

oldest_person = max(people, key=lambda x: x['age'])
print(oldest_person)
```

## Regular Expressions

### Basic
```
pattern = r"\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Z|a-z]{2,}\b"
```
**\b:** This is a word boundary marker.<br>
**[A-Za-z0-9._%+-]:** This part matches the user name of the email address. It can contain letters (A-Za-z), numbers (0-9), dots (.), underscores (_), percent signs (%), plus signs (+), and hyphens (-).<br>
**[A-Za-z0-9.-]:** After the @ symbol, this part matches the domain name of the email. It can contain letters, numbers, dots, and hyphens.<br>
**\.:** This matches the dot before the top-level domain (like .com, .org).<br>
**[A-Z|a-z]{2,}:** This part matches the top-level domain (TLD). It must be at least two characters long. The TLD can contain letters only. The {2,} specifies that there should be at least two characters.<br>
**\b:** Another word boundary marker, ensuring the email address is recognized as a complete word.<br>
**'r'\w':** matches any character that's not a letter, digit, or underscore.<br>
**'r'\w+':**This pattern will match entire words or sequences of alphanumeric characters.<br>

### Matching a Pattern in a String
```
import re

text = "Hello, world!"
pattern = r"world"

match = re.search(pattern, text)

if match:
    print("Pattern found!")
else:
    print("Pattern not found.")
```

### Finding All Matches
```
import re

text = "The rain in Spain falls mainly in the plain."
pattern = r"in"

matches = re.findall(pattern, text)
print(matches)  # ['in', 'in', 'in', 'in', 'in', 'in']
```

### Splitting a String by a Pattern
```
import re

text = "The rain in Spain"
pattern = r" "

words = re.split(pattern, text)
print(words)  # ['The', 'rain', 'in', 'Spain']
```

### Replacing a Pattern in a String

```
import re

text = "The rain in Spain"
pattern = r"Spain"
replacement = "France"

new_text = re.sub(pattern, replacement, text)
print(new_text)  # The rain in France
```

### Complex Pattern Matching
```
import re

text = "Email me at email@example.com or at email2@example.org"
pattern = r"\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Z|a-z]{2,}\b"

emails = re.findall(pattern, text)
print(emails)  # ['email@example.com', 'email2@example.org']
```

### Compiling Regular Expressions
```
import re

pattern = re.compile(r"\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Z|a-z]{2,}\b")

text = "Contact us at support@example.com."
match = pattern.search(text)

if match:
    print("Email found:", match.group())
else:
    print("No email found.")
```