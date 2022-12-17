# 隨機式列舉

```py
import random as rd

def rdCombined(pA, k):
    A = pA.copy()
    chooses = []
    for _ in range(k):
        i = rd.randrange(0, len(A))
        chooses.append(A[i])
        del A[i] #選到哪個就刪除哪個，防止隨機選擇到同樣的
    chooses.sort() #由大排到小
    return chooses # 將函式結果傳出去

A = [1,2,3,4,5]
for _ in range(10):
    print(rdCombined(A, 3)) #呼喚函式
```

## 運算結果

![image](https://user-images.githubusercontent.com/79677951/208236011-2dc8b8d8-5f89-49b9-a939-5e971b67e93d.png)


# 系統式列舉

```py
def combination(A, m): # 從 A 陣列中取出 m 個的所有可能性
    chooses = []
    c(A, len(A), m, chooses, m)

def c(A, n, k, chooses, m): # 從 A[0..n] 中選取 k 個補進 chooses，如果滿 m 個就印出
    if len(chooses)==m:
        print(chooses)
        return
    if n <= 0: return
    c(A,n-1,k,chooses,m) # C(n-1,k) // A[n-1] 沒取到

    chooses.append(A[n-1])
    c(A,n-1,k-1,chooses,m) # C(n-1,k-1) // A[n-1] 有取到
    del chooses[-1]

combination([1,2,3,4,5], 3)
```
## 運算結果

![image](https://user-images.githubusercontent.com/79677951/208236086-cb1c36eb-d3f7-42df-aa07-48ecb2965b4f.png)


