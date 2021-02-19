#### [剑指 Offer 38. 字符串的排列](https://leetcode-cn.com/problems/zi-fu-chuan-de-pai-lie-lcof/)

难度中等185

输入一个字符串，打印出该字符串中字符的所有排列。

 

你可以以任意顺序返回这个字符串数组，但里面不能有重复元素。

 

**示例:**

```
输入：s = "abc"
输出：["abc","acb","bac","bca","cab","cba"]
```

 

**限制：**

```
1 <= s 的长度 <= 8
```



# dfs

```c++
class Solution {
public:
    void func(string& s, set<string>& res, int pos) {
        if (pos == s.size()) {
            res.insert(s);
            return;
        }
        for(int i = pos; i < s.size(); ++i) {
            auto c = s[i];
            s[i] = s[pos];
            s[pos] = c;
            func(s, res, pos + 1);
            c = s[i];
            s[i] = s[pos];
            s[pos] = c;
        }
    }

    vector<string> permutation(string s) {
        set<string> res;
        func(s, res, 0);
        return vector<string>(res.begin(), res.end());
    }
};
```

