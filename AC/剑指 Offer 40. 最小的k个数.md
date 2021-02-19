#### [剑指 Offer 40. 最小的k个数](https://leetcode-cn.com/problems/zui-xiao-de-kge-shu-lcof/)

难度简单192

输入整数数组 `arr` ，找出其中最小的 `k` 个数。例如，输入4、5、1、6、2、7、3、8这8个数字，则最小的4个数字是1、2、3、4。

 

**示例 1：**

```
输入：arr = [3,2,1], k = 2
输出：[1,2] 或者 [2,1]
```

**示例 2：**

```
输入：arr = [0,1,2,1], k = 1
输出：[0]
```

 

**限制：**

- `0 <= k <= arr.length <= 10000`
- `0 <= arr[i] <= 10000`



# Priority_queue

```c++
class Solution {
public:
    vector<int> getLeastNumbers(vector<int>& arr, int k) {
        if (k <= 0)
            return {};
        priority_queue<int> q;
        vector<int> res = {};
        for (auto i : arr) {
            if (q.size() == k) {
                if (i < q.top()) {
                    q.pop();
                    q.push(i);
                }
            } else {
                q.push(i);
            }
        }
        while(!q.empty()) {
            res.push_back(q.top());
            q.pop();
        }
        return res;
    }
};
```

