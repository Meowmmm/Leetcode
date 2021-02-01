## 题目描述

实现一个特殊功能的栈，在实现栈的基本功能的基础上，再实现返回栈中最小元素的操作。

示例1

## 输入

[复制](javascript:void(0);)

```
[[1,3],[1,2],[1,1],[3],[2],[3]]
```

## 返回值

[复制](javascript:void(0);)

```
[1,2]
```

## 备注:

```
有三种操作种类，op1表示push，op2表示pop，op3表示getMin。你需要返回和op3出现次数一样多的数组，表示每次getMin的答案


1<=操作总数<=1000000
-1000000<=每个操作数<=1000000
数据保证没有不合法的操作
```







```c++
class Solution {
public:
    /**
     * return a array which include all ans for op3
     * @param op int整型vector<vector<>> operator
     * @return int整型vector
     */
    vector<int> getMinStack(vector<vector<int> >& op) {
        stack<int> mins;
        stack<int> v;
        vector<int> res;
        
        // write code here
        for(auto& i : op) {
            if (i[0] == 1) {
                // push
                mins.push(mins.size() == 0 ? i[1] : min(mins.top(), i[1]));
                v.push(i[1]);
            } else if (i[0] == 2) {
                v.pop();
                mins.pop();
            } else if (i[0] == 3) {
                res.push_back(mins.top());
            }
        }
        return res;
    }
};
```

