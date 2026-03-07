---
title: "Abel 求和公式的一个行列式表达"
date: 2026-03-07
draft: false
weight: 1
---
# Abel 求和公式的一个行列式表达

## 1 问题

考虑有限和

$$
S=\sum_{k=1}^{n} a_k b_k
$$

我们希望将该求和改写为一种具有望远镜结构的表达式。

为此引入两个部分和序列

$$
A_k=\sum_{i=1}^{k} a_i
$$

$$
B_k=\sum_{i=1}^{k} b_i
$$

其中 $k\in\mathbb{N}$。

---

## 2 差分表示

由于

$$
b_k = B_k - B_{k-1}
$$

因此

$$
\sum_{k=1}^{n} a_k b_k = \sum_{k=1}^{n} a_k (B_k-B_{k-1})
$$

展开得到

$$
a_1B_1+a_2(B_2-B_1)+\cdots+a_n(B_n-B_{n-1})
$$

整理可得经典 Abel 求和公式

$$
\sum_{k=1}^{n} a_k b_k = A_n b_n - \sum_{k=1}^{n-1} A_k (b_{k+1}-b_k)
$$

该公式可以看作积分分部公式

$$
\int u dv = uv-\int v du
$$

在离散情形下的对应形式。

---

## 3 对称结构

同理也可以得到对称表达式

$$
\sum_{k=1}^{n} a_k b_k = B_n a_n - \sum_{k=1}^{n-1} B_k (a_{k+1}-a_k)
$$

---

## 4 行列式结构

考虑表达式

$$
A_k b_k - B_k a_k
$$

可以写为二维行列式

$$
\begin{vmatrix}A_k & B_k \cr a_k & b_k\end{vmatrix}
$$

进一步观察

$$
A_k b_{k+1}-B_k a_{k+1}
$$

对应

$$
\begin{vmatrix}A_k & B_k \cr a_{k+1} & b_{k+1}\end{vmatrix}
$$

于是可以得到如下望远镜求和形式

$$
\sum_{k=1}^{n}\left(\begin{vmatrix}A_k & B_k \cr a_{k+1} & b_{k+1}\end{vmatrix}-\begin{vmatrix}A_k & B_k \cr a_k & b_k\end{vmatrix}\right)=\begin{vmatrix}A_n & B_n \cr a_n & b_n\end{vmatrix}
$$

这给出了 Abel 求和的一种行列式表达形式。

---

## 5 几何解释

行列式

$$
\begin{vmatrix}x_1 & y_1 \cr x_2 & y_2\end{vmatrix}
$$

表示二维向量

$$
(x_1,y_1),(x_2,y_2)
$$

张成平行四边形的有向面积。

因此

$$
A_k b_k - B_k a_k
$$

可以理解为两个向量

$$
(A_k,B_k),(a_k,b_k)
$$

的外积（二维面积）。

从这个角度看，上述公式描述的是：

一系列面积差分构成的望远镜和。

---

## 6 总结

经典 Abel 求和公式为

$$
\sum_{k=1}^{n} a_k b_k = A_n b_n - \sum_{k=1}^{n-1} A_k(b_{k+1}-b_k)
$$

其中

$$
A_k=\sum_{i=1}^{k} a_i
$$

通过引入行列式

$$
\begin{vmatrix}A_k & B_k \cr 
a_k & b_k \cr
\end{vmatrix}
$$

可以得到一种对称且具有几何意义的行列式望远镜表达。

该表达揭示了离散求和中的一种面积结构。