#### [412. Fizz Buzz](https://leetcode-cn.com/problems/fizz-buzz/)

难度简单70

写一个程序，输出从 1 到 *n* 数字的字符串表示。

\1. 如果 *n* 是3的倍数，输出“Fizz”；

\2. 如果 *n* 是5的倍数，输出“Buzz”；

3.如果 *n* 同时是3和5的倍数，输出 “FizzBuzz”。

**示例：**

```
n = 15,

返回:
[
    "1",
    "2",
    "Fizz",
    "4",
    "Buzz",
    "Fizz",
    "7",
    "8",
    "Fizz",
    "Buzz",
    "11",
    "Fizz",
    "13",
    "14",
    "FizzBuzz"
]
```

通过次数43,831

提交次数67,961





# 智障题目

```c++
class Solution {
public:
    vector<string> fizzBuzz(int n) {
        int circle3 = 0, circle5 = 0, circle15 = 0;
        vector<string> res;
        char num[20];
        for(int i = 1; i <= n; ++i) {
            ++circle3;
            ++circle5;
            ++circle15;
            if (circle15 == 15) {
                res.emplace_back("FizzBuzz");
                circle15 = 0;
                circle3 = 0;
                circle5 = 0;
            } else if (circle3 == 3) {
                res.emplace_back("Fizz");
                circle3 = 0;
            } else if (circle5 == 5) {
                res.emplace_back("Buzz");
                circle5 = 0;
            } else {
                sprintf(num, "%d", i);
                res.emplace_back(num);
            }
        }
        return res;
    }
};
```

