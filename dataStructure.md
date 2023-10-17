### 指针pointer

```c
#include <stdio.h>

int tryPointer(int* a){
    (*a)++;
    return 0;
}

int main(){
    int i = 9;
    tryPointer(&i);
    printf("%d",i);
    return 0;
}
```



int转为char

```c
    int a = 3;
    char c = (char)a+'0';
```

```
i++ 先运算再自增
++i 先自增再运算
```







# 算法

## 算法的特性

- 有穷性
- 确定性
- 可行性
- 有输入
- 有输出

## 算法设计的目标

- 正确性
- 可使用性
- 可读性
- 健壮性
- 高效率与低储存量需求



### 线性表

```c
#include <stdio.h>

#define MAXSIZE 10000

typedef struct{
    int data[MAXSIZE];
}node;

int main(){
    node n;
    n.data[0] = 114;
    printf("%d",n.data[0]);

}
```

### 单链表

```c
typedef struct LNode{
	ElemType data;
	struct LNode *next;
}LNode,*LinkList;
```







### 栈

```c
#define MAXSIZE 100
typedef struct{
    SElemType *base;
    SElemType *top;
    int stacksize
}SqStack;
```





### 链栈

```c
typedef struct StackNode{
	ElemType data;
	struct StackNode *next;
}StackNode,*LinkStack;
```



### 队列

顺序

```c
#define MAXQSIZE 100
typedef struct{
	QElemType *base;
	int front;
	int rear;
}SqQueue;
```

链队

```c
typedef struct QNode{
	QElemType data;
	struct Qnode *next;
}QNode,*QueuePtr;
typedef struct{
    QueuePtr front;
    QueuePtr rear;
}LinkQueue;
```



- 循环队列元素个数

  - 设有一个用数组Q[1..m]表示的环形队列，约定f为当前队头元素在数组中的位置，r为队尾元素的后一位置(按顺时针方向),若队列非空，则计算队列中元素个数的公式应为（）

  - A、  (m+r-f)mod m

    B、  r-f

    C、  (m-r-f)mod m

    D、  (m-r+f)mod m

     

    答案为: A 

    分析: 

          对于顺序队列，头指针和尾指针开始时刻都指向数组的0下标元素。当加入新元素以后，尾指针向后移动，指向最后一个元素的下一个位置。

    但是尾指针不能超过数组的最大范围。当有元素删除时，头指针向后移动。但是头指针不能低于数组的0下标。这样就会引入一种“假溢出”现象，

    数组中存在空余的空间，但是由于尾指针已经在最大位置，不能加入元素。

        循环队列就可以用来解决 假溢出 问题, 当队列后面的满了，就从头在开始，形成头尾相接的循环. 
        
        出现的问题:  front=rear即头指针和尾指针相等，但是对应两种情况：一种是队列是空，一种是队列是满。
        
        所以，我们定义循环队列中空出一个位置为满队列状态。front指向头元素，rear指向尾元素的下一个位置。
        
        那么循环队列的长度如何计算呢? 
        
         情况一:  当rear大于front时，循环队列的长度：rear-front
        
        情况二:  当rear小于front时，循环队列的长度:分为两部分计算 0+rear   和   Quesize-front  ,  将两部分的长度合并到一起即为: rear-front+Quesize


        所以将两种情况合为一种，即为:  总长度是(rear-front+Quesize)%Quesize

### 串

- 空串应该用一对引号，中间不加空格来表示





# Tree

## 二叉树

顺序

```c
#define MAXSIZE 100
typedef TElemType SqBiTree[MAXTSIZE];
SqBiTree bt;
```



链式

```c
typedef struct BiTNode{
    TElemType data;
    struct BiTNode *lchild,*rchild;
}BiTNode,*BiTree;
```





$$\xymatrix{    &A   \ar@{-}[dr]  \\ B \ar@{-}[ur]  \ar@{-}[dr]  &C \ar@{-}[u] & D  \\  
 E\ar@{-}[u]&F      
 }$$

A为根节点 B为分支结点 E为叶子结点，$A\rightarrow B$的连线为边

空树：结点数为0

先序遍历

- 访问根结点
- 先序遍历左子树
- 先序遍历右子树

中序遍历

- 中序遍历左子树
- 访问根结点
- 中序遍历右子树

后序遍历

- 后序遍历左子树
- 后序遍历右子树
- 访问根结点

非空树的特性

- 有且仅有一个根结点
- 没有后继的结点称为“叶子结点”（或终端结点）
- 有后继的结点称为“分支结点”（或非终端结点）

 树的特性

- 除了根节点外，任何结点有且仅有一个前驱
- 结点的层次（深度）——从上往下数
- 结点的高度——从下往上数
- 数的高度（深度）——总共有多少层
- 结点的度——有几个孩子（分支）
- 数的度——各结点度的最大值

森林

- $m(m>0)$颗互不相交的树的集合

二叉树常考性质

- 非空二叉树中度为0，1，2的结点个数分别为$n_0,n_1,n_2$，则$n_0=n_2+1$
  - 假设树中结点总数为n 
  - $n=n_0+n_1+n_2$
  - $n=n_1+2n_2+1$
- 二叉树第i层至多有$2^{i-1}$个结点 
  - m叉树第i层至多有$m^{i-1}$个结点
- 高度为h的二叉树至多有$2^h-1$个结点
  - 高度为h的m叉树至多有$\frac{m^h-1}{m-1}$个结点

完全二叉树

- 叶子结点只能出现在最下层和次下层，且最下层的叶子结点集中在树的左部。需要注意的是，满二叉树肯定是完全二叉树，而完全二叉树不一定是满二叉树
- 一个结点，左孩子不为空，右孩子为空；或者左右孩子都为空，且则该节点之后的队列中的结点都为叶子节点，该树才是完全二叉树，否则就不是完全二叉树
- 一个结点，左孩子为空，右孩子不为空，则该树一定不是完全二叉树

- 具有n个$(n>0)$结点的完全二叉树的高度h为$[log_2(n+1)]或,[log_2n]+1$

- 可以由结点数n推出度为0，1，2的结点个数为$n_0,n_1,n_2$
  - 完全二叉树最有只有一个度为一的结点，即$n_1=0or1,n_0=n_2+1\quad n_0+n_2$一定是奇数

平衡二叉树

- $f(n)=f(n-1)+f(n-2)+1$
- $f(n)$为高度为n的平衡二叉树最少的结点数