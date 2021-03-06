### Array理论基础

```
1.时间复杂度
按下标随机访问:O(1)
增/删元素:O(N)——>需要向前或向后移动元素
2.空间复杂度
O(N)——>需要开辟N个元素的数组
```



### 链表理论基础

```
1.链表分类
单向链表 Linked List
双向链表 Double Linked List
循环链表 Cycle Linked List
跳表    Skip List
2.时间复杂度
访问头节点或尾节点:O(1)——>借助头指针或尾指针直接访问
随机访问其他节点:O(N)——>需要从前往后或从后往前遍历
增/删元素:O(1)——>不需要移动元素位置
3.空间复杂度
O(N)——>虽然与Array处于同一量级,但是比Array占据的空间更多,因为每个节点包含 数据域+指针域 两部分
```



### 跳表理论基础

```
1.背景
当数据有序时，如果采用数组进行存储，根据二分查找会很快找到目标值；如果采用普通链表进行存储，需要从前往后或从后往前遍历元素进行查找，因为查找效率较低，所以对普通链表进行了优化，从而引出了跳表，跳表只适用于链表中的元素是有序排列的情况，平衡二叉查找树和二分查找是用来高效查找一堆有序元素的，而跳表可以用来替代二分查找和平衡树来对有序元素进行高效查找
2.算法思想
普通有序链表——>升级维度+以空间换时间——>有序链表+多级索引
3.时间复杂度
查找除头尾节点外的任意元素:O(logN)
增/删元素:O(logN)——>需要更新索引
4.空间复杂度
O(N)——>虽然与普通链表在同一个量级上,但是因为增加了索引,所以占据的空间会更多
5.工程中的应用
LRU Cache——>Double Linked List
Redis——>Skip List
LevelDB——>Skip List
```

