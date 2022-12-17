```py
# 7x 1  + 8x 2  + 2x 3  + 9x 4  + 6x 5 // 7 * x1 + 8 * x2 + 2 * x3 + 9* x4 + 6 * x5

a = b = c = d = e = 0
ans = 0
# 把答案算到最大值後丟入for迴圈

for a_num in range (0,51):
    for b_num in range (0,31):
        for c_num in range (0,20):
            for d_num in range (0,27):
                for e_num in range (0,43):
                        if(5*a+7*b_num+9*c_num+2*d_num+e_num<=250):
                            if(18*a_num+4*b_num-9*c_num+10*d_num+12*e_num <= 285):
                                if(4*a_num+7*b_num+3*c_num+8*d_num+5*e_num <= 211):
                                    if(5*a_num+13*b_num+16*c_num+3*d_num-7*e_num <=315):
                                        temp=7*a_num+8*b_num+2*c_num+9*d_num+6*e_num
                                        if(temp>ans):
                                            ans=temp
                                            a=a_num
                                            b=b_num
                                            c=c_num
                                            d=d_num
                                            e=e_num

print(ans,a,b,c,d,e)
```
