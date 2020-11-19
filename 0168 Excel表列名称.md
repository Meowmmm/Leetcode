#### [168. Excel表列名称](https://leetcode-cn.com/problems/excel-sheet-column-title/)

难度简单288

给定一个正整数，返回它在 Excel 表中相对应的列名称。

例如，

```
    1 -> A
    2 -> B
    3 -> C
    ...
    26 -> Z
    27 -> AA
    28 -> AB 
    ...
```

**示例 1:**

```
输入: 1
输出: "A"
```

**示例 2:**

```
输入: 28
输出: "AB"
```

**示例 3:**

```
输入: 701
输出: "ZY"
```





# n--，因为是从1开始算的

```c++
class Solution {
public:
    string convertToTitle(int n) {
        string res;
        while(n--) {
            res += n % 26 + 'A';
            n /= 26;
        }
        reverse(res.begin(), res.end());
        return res;
    }
};
```

