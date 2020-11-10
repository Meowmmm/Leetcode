

| TOP  | 题目                                                         | 说明                                                         | flag                     |
| ---- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------ |
| TOP  | [1. 两数之和](https://leetcode-cn.com/problems/two-sum/)     | hash_map                                                     | STL                      |
| TOP  | [2. 两数相加](https://leetcode-cn.com/problems/add-two-numbers/) | 链表操作                                                     | 链表                     |
| TOP  | [3. 无重复字符的最长子串](https://leetcode-cn.com/problems/longest-substring-without-repeating-characters/) | 标记每次的begin，一旦发现重复，则需要从这个字母上一次出现的地方的下一个字符为begin | 数组                     |
| TOP  | [4. 寻找两个正序数组的中位数](https://leetcode-cn.com/problems/median-of-two-sorted-arrays/) | 两指针o(n)遍历<br />变形二分查找，第一个数组找cut点，第二个数组的cut点位置可以计算得到 |                          |
| TOP  | [5. 最长回文子串](https://leetcode-cn.com/problems/longest-palindromic-substring/) | 1、扩充法，从mid向两边遍历<br />2、马拉车算法                | **TODO**<br />马拉车算法 |
| TOP  | [7. 整数反转](https://leetcode-cn.com/problems/reverse-integer/) | unsigned int 判断溢出的小trick                               |                          |
| TOP  | [11. 盛最多水的容器](https://leetcode-cn.com/problems/container-with-most-water/) | 两端向中间逼近找答案                                         |                          |
| TOP  | [19. 删除链表的倒数第N个节点](https://leetcode-cn.com/problems/remove-nth-node-from-end-of-list/) |                                                              | fakeHead + 快慢指针      |
|      | [24. 两两交换链表中的节点](https://leetcode-cn.com/problems/swap-nodes-in-pairs/) | 4指针，遍历处理                                              |                          |
| bos  | [25. K 个一组翻转链表](https://leetcode-cn.com/problems/reverse-nodes-in-k-group/) | 一遍遍来                                                     |                          |
| TOP  | [29. 两数相除](https://leetcode-cn.com/problems/divide-two-integers/) | 傻逼题，用long long不香？                                    | 各种溢出边界             |
|      | [34. 在排序数组中查找元素的第一个和最后一个位置](https://leetcode-cn.com/problems/find-first-and-last-position-of-element-in-sorted-array/) | 二分查找                                                     | 二分查找                 |
| TOP  | [35. 搜索插入位置](https://leetcode-cn.com/problems/search-insert-position/) | 二分查找                                                     | 二分查找                 |
|      | [31. 下一个排列](https://leetcode-cn.com/problems/next-permutation/) | STL真香                                                      | Next_permutation         |
| TOP  | [38. 外观数列](https://leetcode-cn.com/problems/count-and-say/) | 类似斐波拉契，一层层处理                                     | 字符串处理               |
| TOP  | [39. 组合总和](https://leetcode-cn.com/problems/combination-sum/) | 完全背包                                                     | dfs                      |
|      | [41. 缺失的第一个正数](https://leetcode-cn.com/problems/first-missing-positive/) |                                                              | Trick                    |
| TOP  | [46. 全排列](https://leetcode-cn.com/problems/permutations/) | next_permutation                                             | dfs or stl               |
|      | [47. 全排列 II](https://leetcode-cn.com/problems/permutations-ii/) | next_permutation                                             | dfs or stl               |
| TOP  | [49. 字母异位词分组](https://leetcode-cn.com/problems/group-anagrams/) | 排序后的字符串作为key，map汇聚                               | STL                      |
| TOP  | [50. Pow(x, n)](https://leetcode-cn.com/problems/powx-n/)    | 超时警告⚠️，指数增长                                          |                          |
|      | [51. N 皇后](https://leetcode-cn.com/problems/n-queens/)     | 同下                                                         | DFS+位运算               |
|      | [52. N皇后 II](https://leetcode-cn.com/problems/n-queens-ii/) | n & -n得到最低位的1的位置<br />n &= (n-1): 把最低位1置0      | DFS+位运算               |
| 剑指 | [53. 最大子序和](https://leetcode-cn.com/problems/maximum-subarray/) |                                                              | O(N)                     |
| TOP  | [56. 合并区间](https://leetcode-cn.com/problems/merge-intervals/) |                                                              |                          |
|      | [57. 插入区间](https://leetcode-cn.com/problems/insert-interval/) | 原理同上                                                     | 56变形                   |
|      | [58. 最后一个单词的长度](https://leetcode-cn.com/problems/length-of-last-word/) |                                                              | 智障题目                 |
| TOP  | [69. x 的平方根](https://leetcode-cn.com/problems/sqrtx/)    | 溢出警告⚠️                                                    | 二分                     |
|      | [70. 爬楼梯](https://leetcode-cn.com/problems/climbing-stairs/) | dp[n] = dp[n-1] + dp[n-2]                                    | dp                       |
| TOP  | [75. 颜色分类](https://leetcode-cn.com/problems/sort-colors/) |                                                              | 排序                     |
| TOP  | [76. 最小覆盖子串](https://leetcode-cn.com/problems/minimum-window-substring/) |                                                              | 滑动窗口                 |
| TOP  | [77. 组合](https://leetcode-cn.com/problems/combinations/)   | 本位置【选中】、【不选中】                                   | dfs                      |
| TOP  | [78. 子集](https://leetcode-cn.com/problems/subsets/)        | 每个位置可选可不选                                           | dfs                      |
| TOP  | [79. 单词搜索](https://leetcode-cn.com/problems/word-search/) |                                                              | Dfs                      |
| TOP  | [91. 解码方法](https://leetcode-cn.com/problems/decode-ways/) | 26进制+dp                                                    | dp                       |
| TOP  | [102. 二叉树的层序遍历](https://leetcode-cn.com/problems/binary-tree-level-order-traversal/) |                                                              | queue                    |
| TOP  | [103. 二叉树的锯齿形层次遍历](https://leetcode-cn.com/problems/binary-tree-zigzag-level-order-traversal/) |                                                              | Queue + reverse          |
| TOP  | [104. 二叉树的最大深度](https://leetcode-cn.com/problems/maximum-depth-of-binary-tree/) |                                                              | 递归                     |
| TOP  | [105. 从前序与中序遍历序列构造二叉树](https://leetcode-cn.com/problems/construct-binary-tree-from-preorder-and-inorder-traversal/) |                                                              | 递归                     |
| TOP  | [108. 将有序数组转换为二叉搜索树](https://leetcode-cn.com/problems/convert-sorted-array-to-binary-search-tree/) |                                                              | 不断递归二分             |
|      | [111. 二叉树的最小深度](https://leetcode-cn.com/problems/minimum-depth-of-binary-tree/) |                                                              | 树的层次遍历             |
|      | [112. 路径总和](https://leetcode-cn.com/problems/path-sum/)  |                                                              | 递归                     |
|      | [113. 路径总和 II](https://leetcode-cn.com/problems/path-sum-ii/) |                                                              | DFS+递归                 |
|      | [114. 二叉树展开为链表](https://leetcode-cn.com/problems/flatten-binary-tree-to-linked-list/) |                                                              | 递归                     |
|      | [116. 填充每个节点的下一个右侧节点指针](https://leetcode-cn.com/problems/populating-next-right-pointers-in-each-node/) |                                                              | 树的层次遍历<br />递归   |
|      | [117. 填充每个节点的下一个右侧节点指针 II](https://leetcode-cn.com/problems/populating-next-right-pointers-in-each-node-ii/) |                                                              | 树的层次遍历<br />递归   |
|      | [118. 杨辉三角](https://leetcode-cn.com/problems/pascals-triangle/) |                                                              | 智障题                   |
|      | [119. 杨辉三角 II](https://leetcode-cn.com/problems/pascals-triangle-ii/) |                                                              | 数学                     |
| TOP  | [121. 买卖股票的最佳时机](https://leetcode-cn.com/problems/best-time-to-buy-and-sell-stock/) |                                                              | 智障题                   |
| TOP  | [122. 买卖股票的最佳时机 II](https://leetcode-cn.com/problems/best-time-to-buy-and-sell-stock-ii/) | 所有连续升序子序列首尾差的总和                               |                          |
| TOP  | [124. 二叉树中的最大路径和](https://leetcode-cn.com/problems/binary-tree-maximum-path-sum/) |                                                              | 递归                     |
|      | [125. 验证回文串](https://leetcode-cn.com/problems/valid-palindrome/) | 字符串操作+边界处理                                          | 字符串操作               |
| TOP  | [127. 单词接龙](https://leetcode-cn.com/problems/word-ladder/) | 双端bfs加快查找速度                                          | BFS                      |
|      | [129. 求根到叶子节点数字之和](https://leetcode-cn.com/problems/sum-root-to-leaf-numbers/) |                                                              | 树，递归                 |
| TOP  | [139. 单词拆分](https://leetcode-cn.com/problems/word-break/) |                                                              | DFS+MEM                  |
| TOP  | [141. 环形链表](https://leetcode-cn.com/problems/linked-list-cycle/) | 快慢指针                                                     | 快慢指针                 |
|      | [142. 环形链表 II](https://leetcode-cn.com/problems/linked-list-cycle-ii/) | slow = head，fast = fast->next<br />下次相遇就是找到了链表的环入口 | 快慢指针                 |
|      | [143. 重排链表](https://leetcode-cn.com/problems/reorder-list/) |                                                              | vector保存每个节点       |
|      | [144. 二叉树的前序遍历](https://leetcode-cn.com/problems/binary-tree-preorder-traversal/) |                                                              | 闭着眼都能写             |
| TOP  | [146. LRU缓存机制](https://leetcode-cn.com/problems/lru-cache/) | list + unordered_map                                         | List + hash              |
| TOP  | [150. 逆波兰表达式求值](https://leetcode-cn.com/problems/evaluate-reverse-polish-notation/) | Stack                                                        | stack                    |
|      | [155. 最小栈](https://leetcode-cn.com/problems/min-stack/)   | 双stack，其中一个stack存当前最小值。                         | 设计思想                 |
| TOP  | [160. 相交链表](https://leetcode-cn.com/problems/intersection-of-two-linked-lists/) | 1、第一遍求长度差，第二遍找交点<br />2、第一个链表尾巴指向第二个，相遇就是交点 |                          |
| TOP  | [162. 寻找峰值](https://leetcode-cn.com/problems/find-peak-element/) |                                                              | 分治                     |
|      | [167. 两数之和 II - 输入有序数组](https://leetcode-cn.com/problems/two-sum-ii-input-array-is-sorted/) | 两头向中间夹击                                               | 双指针                   |
| TOP  | [171. Excel表列序号](https://leetcode-cn.com/problems/excel-sheet-column-number/) | 26进制+字符串处理                                            | 傻瓜题                   |
|      | [172. 阶乘后的零](https://leetcode-cn.com/problems/factorial-trailing-zeroes/) | 因子5的个数                                                  | 数学                     |
| TOP  | [190. 颠倒二进制位](https://leetcode-cn.com/problems/reverse-bits/) | 位运算： <<、>>、&<br />result左移，ori_num右移              | 位运算                   |
| TOP  | [191. 位1的个数](https://leetcode-cn.com/problems/number-of-1-bits/) | 位运算：>>、&<br />原数右移32次判断最低位即可                | 位运算<br />bitset       |
| TOP  | [198. 打家劫舍](https://leetcode-cn.com/problems/house-robber/) | dp[i] = max(dp[i - 1], n[i] + dp[i - 2]);                    | Dp                       |
| TOP  | [202. 快乐数](https://leetcode-cn.com/problems/happy-number/) | 有限次穷举<br />模拟快慢指针判断有环                         | <-                       |
| TOP  | [204. 计数质数](https://leetcode-cn.com/problems/count-primes/) |                                                              | 鄂尔多塞筛法             |
| TOP  | [206. 反转链表](https://leetcode-cn.com/problems/reverse-linked-list/) | 三指针遍历                                                   | 三指针                   |
| TOP  | [208. 实现 Trie (前缀树)](https://leetcode-cn.com/problems/implement-trie-prefix-tree/) | 前缀树                                                       | 前缀树                   |
|      | [216. 组合总和 III](https://leetcode-cn.com/problems/combination-sum-iii/) | dfs                                                          | dfs                      |
| TOP  | [227. 基本计算器 II](https://leetcode-cn.com/problems/basic-calculator-ii/) | 第一次遍历解析字符串、第二次遍历进行计算                     | 字符串处理    STL queue  |
| TOP  | [230. 二叉搜索树中第K小的元素](https://leetcode-cn.com/problems/kth-smallest-element-in-a-bst/) | 树的中序遍历                                                 | 树                       |
| TOP  | [234. 回文链表](https://leetcode-cn.com/problems/palindrome-linked-list/) | 快慢指针+反转前半部分链表                                    | 链表                     |
|      | [235. 二叉搜索树的最近公共祖先](https://leetcode-cn.com/problems/lowest-common-ancestor-of-a-binary-search-tree/) | 二叉搜索树的特性<br />同下                                   | 树                       |
| TOP  | [236. 二叉树的最近公共祖先](https://leetcode-cn.com/problems/lowest-common-ancestor-of-a-binary-tree/) | 递归<br />树的后续遍历                                       | 树                       |
| TOP  | [237. 删除链表中的节点](https://leetcode-cn.com/problems/delete-node-in-a-linked-list/) | cur复制next node的值，释放next node                          | 值拷贝                   |
| TOP  | [238. 除自身以外数组的乘积](https://leetcode-cn.com/problems/product-of-array-except-self/) | 考虑多种情况：有0、1个0、多个0                               | 数学问题                 |
| TOP  | [240. 搜索二维矩阵 II](https://leetcode-cn.com/problems/search-a-2d-matrix-ii/) | 从右上或者左下开始搜索                                       | 矩阵                     |
| TOP  | [242. 有效的字母异位词](https://leetcode-cn.com/problems/valid-anagram/) | 统计每个字母的count是否一致即可                              | 字符串                   |
| TOP  | [268. 缺失数字](https://leetcode-cn.com/problems/missing-number/) | 减差 OR 位运算                                               | 位运算                   |
| TOP  | [279. 完全平方数](https://leetcode-cn.com/problems/perfect-squares/) | dp                                                           | dp                       |
| TOP  | [287. 寻找重复数](https://leetcode-cn.com/problems/find-the-duplicate-number/) |                                                              | **TODO**                 |
| TOP  | [289. 生命游戏](https://leetcode-cn.com/problems/game-of-life/) |                                                              | 傻逼题                   |
| TOP  | [322. 零钱兑换](https://leetcode-cn.com/problems/coin-change/) | 完全背包、dp（用stack会死循环）                              | 完全背包、DP             |
| TOP  | [326. 3的幂](https://leetcode-cn.com/problems/power-of-three/) |                                                              |                          |
| TOP  | [328. 奇偶链表](https://leetcode-cn.com/problems/odd-even-linked-list/) |                                                              | 指针操作                 |
| TOP  | [334. 递增的三元子序列](https://leetcode-cn.com/problems/increasing-triplet-subsequence/) |                                                              |                          |
|      | [338. 比特位计数](https://leetcode-cn.com/problems/counting-bits/) |                                                              | 位运算                   |
| TOP  | [341. 扁平化嵌套列表迭代器](https://leetcode-cn.com/problems/flatten-nested-list-iterator/) |                                                              |                          |
| TOP  | [344. 反转字符串](https://leetcode-cn.com/problems/reverse-string/) |                                                              | 头尾交换                 |
| TOP  | [347. 前 K 个高频元素](https://leetcode-cn.com/problems/top-k-frequent-elements/) | 小顶堆                                                       | priority_queue           |
|      | [349. 两个数组的交集](https://leetcode-cn.com/problems/intersection-of-two-arrays/) |                                                              | Set                      |
| TOP  | [371. 两整数之和](https://leetcode-cn.com/problems/sum-of-two-integers/) |                                                              | 位运算                   |
| TOP  | [380. 常数时间插入、删除和获取随机元素](https://leetcode-cn.com/problems/insert-delete-getrandom-o1/) | unordered_map + vector联动管理数据                           |                          |
|      | [381. O(1) 时间插入、删除和获取随机元素 - 允许重复](https://leetcode-cn.com/problems/insert-delete-getrandom-o1-duplicates-allowed/) | Unordered_map + unordered_set + vector                       |                          |
| TOP  | [384. 打乱数组](https://leetcode-cn.com/problems/shuffle-an-array/) | 随机数，两数交换                                             |                          |
| TOP  | [412. Fizz Buzz](https://leetcode-cn.com/problems/fizz-buzz/) |                                                              | 智障题目                 |
|      | [434. 字符串中的单词数](https://leetcode-cn.com/problems/number-of-segments-in-a-string/) |                                                              | 智障题目                 |
|      | [463. 岛屿的周长](https://leetcode-cn.com/problems/island-perimeter/) | 数边长                                                       | 简单                     |
|      | [485. 最大连续1的个数](https://leetcode-cn.com/problems/max-consecutive-ones/) | 一次遍历                                                     | 智障题目                 |
|      | [506. 相对名次](https://leetcode-cn.com/problems/relative-ranks/) |                                                              | Priority_queue           |
|      | [572. 另一个树的子树](https://leetcode-cn.com/problems/subtree-of-another-tree/) |                                                              | 递归                     |
|      | [645. 错误的集合](https://leetcode-cn.com/problems/set-mismatch/) |                                                              | 智障题目                 |
|      | [653. 两数之和 IV - 输入 BST](https://leetcode-cn.com/problems/two-sum-iv-input-is-a-bst/) |                                                              | 树的遍历+set             |
|      | [674. 最长连续递增序列](https://leetcode-cn.com/problems/longest-continuous-increasing-subsequence/) |                                                              | 序列                     |
|      | [692. 前K个高频单词](https://leetcode-cn.com/problems/top-k-frequent-words/) |                                                              | 自定义sort               |
|      | [763. 划分字母区间](https://leetcode-cn.com/problems/partition-labels/) | 滑动窗口+合并区间                                            | 滑动窗口                 |
|      | [783. 二叉搜索树节点最小距离](https://leetcode-cn.com/problems/minimum-distance-between-bst-nodes/) |                                                              | 树                       |
|      | [836. 矩形重叠](https://leetcode-cn.com/problems/rectangle-overlap/) | 简单的判断非重叠的情况就行                                   | 数学                     |
|      | [844. 比较含退格的字符串](https://leetcode-cn.com/problems/backspace-string-compare/) |                                                              | 字符串                   |
|      | [845. 数组中的最长山脉](https://leetcode-cn.com/problems/longest-mountain-in-array/) | 边界很烦                                                     | 双指针                   |
|      | [876. 链表的中间结点](https://leetcode-cn.com/problems/middle-of-the-linked-list/) |                                                              | 快慢指针                 |
|      | [925. 长按键入](https://leetcode-cn.com/problems/long-pressed-name/) |                                                              | 双指针                   |
|      | [941. 有效的山脉数组](https://leetcode-cn.com/problems/valid-mountain-array/) |                                                              | 智障题                   |
|      | [973. 最接近原点的 K 个点](https://leetcode-cn.com/problems/k-closest-points-to-origin/) |                                                              | priority_queue           |
|      | [977. 有序数组的平方](https://leetcode-cn.com/problems/squares-of-a-sorted-array/) | 找到中值，再向两边遍历                                       |                          |
|      | [1002. 查找常用字符](https://leetcode-cn.com/problems/find-common-characters/) |                                                              | 智障题                   |
|      | [1160. 拼写单词](https://leetcode-cn.com/problems/find-words-that-can-be-formed-by-characters/) | 统计单词                                                     | 智障题                   |
|      | [1207. 独一无二的出现次数](https://leetcode-cn.com/problems/unique-number-of-occurrences/) |                                                              | 智障题                   |
|      | [1347. 制造字母异位词的最小步骤数](https://leetcode-cn.com/problems/minimum-number-of-steps-to-make-two-strings-anagram/) | 统计两个单词字母出现次数差                                   | 字符串变换               |
|      | [1356. 根据数字二进制下 1 的数目排序](https://leetcode-cn.com/problems/sort-integers-by-the-number-of-1-bits/) |                                                              | 位运算 + map + multiset  |
|      | [1365. 有多少小于当前数字的数字](https://leetcode-cn.com/problems/how-many-numbers-are-smaller-than-the-current-number/) | 如何累加                                                     | 简单题                   |
| 剑指 | [剑指 Offer 18. 删除链表的节点](https://leetcode-cn.com/problems/shan-chu-lian-biao-de-jie-dian-lcof/) |                                                              | 智障题                   |
| 剑指 | [剑指 Offer 59 - II. 队列的最大值](https://leetcode-cn.com/problems/dui-lie-de-zui-da-zhi-lcof/) |                                                              | queue+deque              |
|      | [面试题 01.01. 判定字符是否唯一](https://leetcode-cn.com/problems/is-unique-lcci) |                                                              | 智障题                   |
|      | [面试题 01.02. 判定是否互为字符重排](https://leetcode-cn.com/problems/check-permutation-lcci/) |                                                              | 智障题                   |
|      | [面试题 01.03. URL化](https://leetcode-cn.com/problems/string-to-url-lcci/) |                                                              | 智障题                   |
|      | [面试题 01.06. 字符串压缩](https://leetcode-cn.com/problems/compress-string-lcci/) |                                                              | 字符串处理               |
|      | [面试题 01.09. 字符串轮转](https://leetcode-cn.com/problems/string-rotation-lcci/) | 每次找到头                                                   | 字符串处理               |
|      | [面试题 02.01. 移除重复节点](https://leetcode-cn.com/problems/remove-duplicate-node-lcci/) |                                                              | 链表操作                 |
|      | [面试题 02.06. 回文链表](https://leetcode-cn.com/problems/palindrome-linked-list-lcci/) | 同234                                                        |                          |
|      | [面试题 04.03. 特定深度节点链表](https://leetcode-cn.com/problems/list-of-depth-lcci/) |                                                              | 树的层次遍历             |
|      | [面试题 08.04. 幂集](https://leetcode-cn.com/problems/power-set-lcci/) |                                                              | Dfs                      |
|      | [面试题 16.02. 单词频率](https://leetcode-cn.com/problems/words-frequency-lcci/) |                                                              | map                      |
|      | [面试题 17.22. 单词转换](https://leetcode-cn.com/problems/word-transformer-lcci/) |                                                              | dfs                      |



