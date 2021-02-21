## 题目描述

给定String类型的数组strArr，再给定整数k，请严格按照排名顺序打印 出次数前k名的字符串。

[要求]

如果strArr长度为N，时间复杂度请达到O(N \log K)*O*(*N*log*K*)

输出K行，每行有一个字符串和一个整数（字符串表示）。
你需要按照出现出现次数由大到小输出，若出现次数相同时字符串字典序较小的优先输出



示例1

## 输入

[复制](javascript:void(0);)

```
["1","2","3","4"],2
```

## 返回值

[复制](javascript:void(0);)

```
[["1","1"],["2","1"]]
```

示例2

## 输入

[复制](javascript:void(0);)

```
["1","1","2","3"],2
```

## 返回值

[复制](javascript:void(0);)

```
[["1","2"],["2","1"]]
```



# Unorderd_map  map

```c++
class Solution {
public:
    /**
     * return topK string
     * @param strings string字符串vector strings
     * @param k int整型 the k
     * @return string字符串vector<vector<>>
     */
    vector<vector<string> > topKstrings(vector<string>& strings, int k) {
        // write code here
        vector<vector<string> > res;
        unordered_map<string, int> times;
        for(auto i : strings) 
            times[i]++;
        
        map<int, vector<string>, greater<>> m;
        for(auto i : times) 
            m[i.second].push_back(i.first);
        
        for(auto i : m) {
            sort(i.second.begin(), i.second.end());
            for(auto j : i.second){
                res.push_back({j, to_string(i.first)});
                if (--k == 0)
                    return res;
            }
        }
        return res;
    }
};
```

