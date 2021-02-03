## 题目描述

给你一个非空模板串S，一个文本串T，问S在T中出现了多少次

示例1

## 输入

[复制](javascript:void(0);)

```
"ababab","abababab"
```

## 返回值

[复制](javascript:void(0);)

```
2
```

示例2

## 输入

[复制](javascript:void(0);)

```
"abab","abacabab"
```

## 返回值

[复制](javascript:void(0);)

```
1
```

## 备注:

```
空间O(n)时间O(n)的算法
```





```c++
class Solution {
public:
    /**
     * 代码中的类名、方法名、参数名已经指定，请勿修改，直接返回方法规定的值即可
     *
     * 计算模板串S在文本串T中出现了多少次
     * @param S string字符串 模板串
     * @param T string字符串 文本串
     * @return int整型
     */
    int kmp(string S, string T) {
        // write code here
        int res = 0;
        int s1 = S.size(), t1 = T.size();
        for (auto left = 0; left <= t1 - s1; ++left) {
            for(auto i = 0; i < s1; ++i) {
                if (S[i] != T[left + i]) {
                    --res;
                    break;
                }
            }
            ++res;
        }
        return res;
    }
};
```



发现mark下一个和S[0]相同的T pos，效率还没有暴力的好