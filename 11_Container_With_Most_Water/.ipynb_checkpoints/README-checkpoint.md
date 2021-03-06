[答案連結](https://nbviewer.jupyter.org/github/MagicUmom/leetcode_python/blob/master/11_Container_With_Most_Water/Ans.ipynb)

---

![Q2](pics/Q2.png)
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

