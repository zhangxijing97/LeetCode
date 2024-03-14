# LeetCode

## Table of Contents

1. [Big O Notation and Time Complexity](#Big-O-Notation-and-Time-Complexity)
- [Linear Time](#Training-Model)
- [Constant Time O(1)](#Constant-Time)

### Big O Notation and Time Complexity

#### Linear Time O(n)

```
int addUp(int n){
    int sum = 0;
    for(int i = 0; i <= n; i++) {
        sum += 1;
    }
    return sum;
}
```
n = 10000
10000 steps

#### Constant Time O(1)
```
int addUp (int n){
    int sum = n * (p + 1) / 2;
    return sum;
}
```


<!-- **Training Set:** The model learns patterns and relationships within the training set. It is the data on which the model is trained to make predictions.<br> -->