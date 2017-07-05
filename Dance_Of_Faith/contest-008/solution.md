# The Solution

题目按CF顺序排序


## #A -New Year Candles

> 时间限制：  1s
>
> 空间限制：  256MB
>
> 主要算法：  模拟

### 题意
原有N个蜡烛，可以讲B个用过的蜡烛变成一根新蜡烛，求最多能用几根蜡烛。
### 题解
模拟，没有什么可说的。



## #B -New Year Present

> 时间限制：  1s
>
> 空间限制：  256MB
>
> 主要算法：  模拟

### 题意
一个机器人要在N个袋子里放分别放a[i]个金币，能往右走或往左走，或在此放一个金币，而且不能连续放金币，求任意一个可行的行走序列。
### 题解
纯模拟，特判在i=1的清况，其他都是RLP即可。



## #C -New Year Ratings Change

> 时间限制：  1s
>
> 空间限制：  256MB
>
> 主要算法：  贪心

### 题意
增大数列中的某些数，使其没有重复的，要求增加的数之和最小。
### 题解
先按数字大小排一遍序，操作时将每一个数字都改为前一个数加一（因为例如：1 1 2三个数,1->2 + 2->3和1->3是等价的），所以可以看到其正确性显然。
输出时再将数列按原先的ID再排一遍序。



## #D -New Year Letter

> 时间限制：  1s
>
> 空间限制：  256MB
>
> 主要算法：  递推+字符串

### 题意
原有s1,s2两个字符串，其长度N,M已经给出；用斐波那契数列将其连接起来：s[n]=s[n-2]+s[n-1]；要求使s[k]恰好包含x个"AC"子串。求符合条件的任意一对字符串，如不存在，输出"Happy new year!"。
### 题解
由于k比较小，枚举每个字符串中本有的"AC"子串，并枚举两个字符串首尾是否是'A'或'C'，构造好了以后进行递推，递推时注意两串连接时是否会出现多出的一个"AC"串，如果可行，直接输出。



## #E -New Year Tree Decorations

> 时间限制：  1s
>
> 空间限制：  256MB
>
> 主要算法：  计算几何

### 题意
给出在坐标系中的N个多边形，其满足以x轴为其一条边；每次按顺序将每个多边形插入到已有图形的后面，求每一个多边形在其被插入时的可见面积。
### 题解
使用微积分思想，将坐标系的，每一个单元分为2000个小单元，每次计算其高度（因为原本就有精度误差，在计算时可以先不用除法，在最后使用除法也能减小精度误差）。



## #F -New Year Tree

> 时间限制：  2s
>
> 空间限制：  256MB
>
> 主要算法：  LCA+树的直径

### 题意
给定一棵初始树，一个编号为1的根和2,3,4的叶；有Q次操作，每次在指定的节点下插入两个节点，并输出本次插入后树的直径。
### 题解
树的直径显然必须以深度最大的一个叶节点为一个端点（请回顾两次BFS求直径的方法），而且树的直径是单调递增的，且据题意每次最多加一。那只要在每次插入时先判深度，如果大于了已有最大深度，则直接增加1，并更新最深节点；否则求插入节点和最深节点的LCA，看是否能将直径更新。