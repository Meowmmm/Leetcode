#### [50. Pow(x, n)](https://leetcode-cn.com/problems/powx-n/)

难度中等327

实现 [pow(*x*, *n*)](https://www.cplusplus.com/reference/valarray/pow/) ，即计算 x 的 n 次幂函数。

**示例 1:**

```
输入: 2.00000, 10
输出: 1024.00000
```

**示例 2:**

```
输入: 2.10000, 3
输出: 9.26100
```

**示例 3:**

```
输入: 2.00000, -2
输出: 0.25000
解释: 2-2 = 1/22 = 1/4 = 0.25
```

**说明:**

- -100.0 < *x* < 100.0
- *n* 是 32 位有符号整数，其数值范围是 [−231, 231 − 1] 。





主要是n的 [−231, 231 − 1] 范围，容易踩坑，需要转化为一个long进行处理，因为 0 - (-2^31)会溢出等问题，同时首先处理特殊的情况，为0和1的情况，其次，通过平方来加快速度。

```c++
class Solution {
public:
    double myPow(double x, int n) {
        double res = x;
        bool needChange = false;
        long cur = 1;
        long n_2 = n;
        
        if (n == 0 || x == 1)
            return 1;
        if (x == -1)
            return n % 2 == 0 ? 1 : -1;

        if (n < 0) {
            needChange = true;
            n_2 = -n_2;
        }
        while(cur < n_2) {
            if (cur << 1 <= n_2) {
                res *= res;
                cur = cur << 1;
            } else {
                res *= x;
                ++cur;
            }
        }
        if (needChange)
            res = 1.0 / res;
        return res;
    }
};
```





