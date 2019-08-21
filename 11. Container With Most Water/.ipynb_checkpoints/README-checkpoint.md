Given n non-negative integers $a_1$, $a_2$, ..., $a_n$ , where each represents a point at coordinate ($i$, $a_i$). n vertical lines are drawn such that the two endpoints of line i is at ($i$, $a_i$) and ($i$, $0$). Find two lines, which together with x-axis forms a container, such that the container contains the most water.

Note: You may not slant the container and $n$ is at least 2.

![Q1](pics/Q1.jpg)

### Example
```
Input: [1,8,6,2,5,4,8,3,7]
Output: 49
```


## Solution 

取最左邊邊界為L, 最右邊邊界為R, R>L

步驟1: 取L與R可裝水的面積:
```
## 面積公式
min(height[L],height[R]) * (R - L) 
```
步驟2: 從左右往內縮，取height[L], height[R]較小的一端開始縮，假設是L開始縮，設新的邊界為L'，此時有兩種情況：
1. L' < L:
    這種情況下不會有更大的面積發生，所以繼續往內縮找L' > L的情況
2. L' > L:
    這種情庫有可能會有更大的面積，回步驟1 計算面積


**時間複雜度 O(n)**

---

