# The Solution

题目按CF顺序排序


## #A -Okabe and Future Gadget Laboratory 

> 时间限制：  2s
>
> 空间限制：  256MB
>
> 主要算法：  我不知道…

### 题意 我不知道…
### 题解 我不知道…


## #B Okabe and Banana Trees 

> 时间限制：  2s
>
> 空间限制：  256MB
>
> 主要算法：  数学知识

### 题意:求矩形内横纵坐标之和的最大值
### 题解：模拟，找规律，慢慢找，就会发现的。


## #C Okabe and Boxes 

> 时间限制：  3s
>
> 空间限制：  256MB
>
> 主要算法：  二叉堆，栈

### 题意:给定一些操作，使得出栈的序列有序
### 题解：完完全全的模拟，建立一个堆和栈，每一次如果加入的元素小于栈顶，就排序，用二叉堆排序。


## #D Okabe and City 

> 时间限制：  4s
>
> 空间限制：  256MB
>
> 主要算法：  最短路，构图

### 题意：给定一些灯泡，我们可以点一些临时灯泡，问点最少多少的灯泡可以到达目标点。
### 题解：建图，根据题意如果相邻边权为0，如果横纵坐标之差为为2则为1.然后跑一遍spfa or dij，求出最短路就可以了。
> 注意在终点的点的坐标为N+1，M+!，这是很巧妙的，因为初始的时候终点是没有灯的。


## #E Okabe and El Psy Kongroo 

> 时间限制：  2s
>
> 空间限制：  256MB
>
> 主要算法：  矩阵快速幂

### 题意：写炸了，打算重构代码，晚上补上。
### 题解：同上。
