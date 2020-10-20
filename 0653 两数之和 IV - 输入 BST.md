#### [653. 两数之和 IV - 输入 BST](https://leetcode-cn.com/problems/two-sum-iv-input-is-a-bst/)

难度简单130

给定一个二叉搜索树和一个目标结果，如果 BST 中存在两个元素且它们的和等于给定的目标结果，则返回 true。

**案例 1:**

```
输入: 
    5
   / \
  3   6
 / \   \
2   4   7

Target = 9

输出: True
```

 

**案例 2:**

```
输入: 
    5
   / \
  3   6
 / \   \
2   4   7

Target = 28

输出: False
```

 

就是有序数字求数字和的变形

```c++
/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     TreeNode *left;
 *     TreeNode *right;
 *     TreeNode(int x) : val(x), left(NULL), right(NULL) {}
 * };
 */
class Solution {
public:
    bool findTarget(TreeNode* root, int k) {
        // 二叉树的前序遍历，转换为有序链表
        TreeNode* p = root;
        stack<TreeNode*> s;
        vector<int> v;
        while(p || !s.empty()) {
            while(p) {
                s.push(p);
                p = p->left;
            }
            
            if(!s.empty()) {
                p = s.top();
                //cout << p->val << endl;
                v.emplace_back(p->val);
                s.pop();

                p = p->right;
            }
        }
        // 两头夹击找到答案
        int left = 0, right = v.size() - 1;
        while(left + 1 <= right) {
            if (v[left] + v[right] < k) 
                left++;
            else if (v[left] + v[right] > k) 
                right--;
            else
                return true;
        }
        return false;
    }
};
```



# 遍历的时候找答案

```c++
/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     TreeNode *left;
 *     TreeNode *right;
 *     TreeNode() : val(0), left(nullptr), right(nullptr) {}
 *     TreeNode(int x) : val(x), left(nullptr), right(nullptr) {}
 *     TreeNode(int x, TreeNode *left, TreeNode *right) : val(x), left(left), right(right) {}
 * };
 */
class Solution {
public:
    bool findTarget(TreeNode* root, int k) {
        unordered_set<int> us;
        stack<TreeNode*> s;
        TreeNode* cur = root;
        while(!s.empty() || cur) {
            while(cur) {
                if (us.find(k - cur->val) != us.end()) 
                    return true;
                
                us.insert(cur->val);
                s.push(cur);
                cur = cur->left;
            }
            if(!s.empty()) {
                cur = s.top();
                s.pop();
                cur = cur->right;
            }
        }
        return false;
    }
};
```

