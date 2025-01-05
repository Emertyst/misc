# 5 向量组的线性相关性与矩阵的秩

## 5.1 向量组的线性相关性和秩

### 线性表示

> 向量 $\boldsymbol b$ 能由向量 $\boldsymbol a_1, \boldsymbol a_2, \cdots, \boldsymbol a_n$ 线性表示 $\iff$ 存在 $n$ 个数 $k_1, k_2, \cdots, k_n$，使 $k_1 \boldsymbol a_1 + k_2 \boldsymbol a_2 + \cdots + k_n \boldsymbol a_n = \boldsymbol b$

### 线性相关

> 向量组 $\boldsymbol a_1, \boldsymbol a_2, \cdots, \boldsymbol a_n$ 线性相关 $\iff$ 存在 $n$ 个不全为零的数 $k_1, k_2, \cdots, k_n$，使 $k_1 \boldsymbol a_1 + k_2 \boldsymbol a_2 + \cdots + k_n \boldsymbol a_n = \boldsymbol 0$

### 结论

> $A = [\boldsymbol a_1, \boldsymbol a_2, \cdots, \boldsymbol a_n]$，且 $A$ 为方阵时，向量组 $\boldsymbol a_1, \boldsymbol a_2, \cdots, \boldsymbol a_n$ 线性相关（无关） $\iff$ $|A| = 0$（$|A| \ne 0$）

> 向量组 $\boldsymbol a_1, \boldsymbol a_2, \cdots, \boldsymbol a_n$（$n \geqslant 2$）线性相关 $\iff$ 该向量组中至少有一个向量可由其余的 $n - 1$ 个向量线性表示

> 若向量组 $\boldsymbol a_1, \boldsymbol a_2, \cdots, \boldsymbol a_n$ 线性无关，而向量组 $\boldsymbol a_1, \boldsymbol a_2, \cdots, \boldsymbol a_n, \boldsymbol b$ 线性相关 $\Rightarrow$ 向量 $\boldsymbol b$ 可由向量组 $\boldsymbol a_1, \boldsymbol a_2, \cdots, \boldsymbol a_n$ 线性表示且表达式唯一。

> 设向量组 Ⅰ 为 $\boldsymbol a_1, \boldsymbol a_2, \cdots, \boldsymbol a_r$，向量组 Ⅱ 为 $\boldsymbol a_1, \boldsymbol a_2, \cdots, \boldsymbol a_r, \boldsymbol a_{r + 1}, \cdots, \boldsymbol a_n$。
>
> 1. 若向量组 Ⅰ 线性相关，则向量组 Ⅱ 也线性相关。
> 1. 若向量组 Ⅱ 线性无关，则向量组 Ⅰ 也线性无关。

> 设 $r$ 元向量组 Ⅰ 为 $\boldsymbol a_1, \boldsymbol a_2, \cdots, \boldsymbol a_m$，$s$ 元向量组 Ⅱ 为 $\boldsymbol b_1, \boldsymbol b_2, \cdots, \boldsymbol b_m$，$r + s$ 元向量组 Ⅲ 为 $\boldsymbol c_1, \boldsymbol c_2, \cdots, \boldsymbol c_m$，其中，
>
> $$
> \boldsymbol c_i =
> \begin{bmatrix}
>     \boldsymbol a_i \\
>     \boldsymbol b_i \\
> \end{bmatrix}
> $$
>
> 1. 若向量组 Ⅰ 和 Ⅱ 中有一个线性无关，则向量组 Ⅲ 也线性无关。
> 1. 若向量组 Ⅲ 线性相关，则向量组 Ⅰ 和 Ⅱ 都线性相关。

## 5.2 矩阵的秩

### 矩阵的秩

> 设 $A$ 为 $m \times n$ 矩阵，$1 \leqslant k \leqslant \min\{m, n\}$，由矩阵 $A$ 的任意 $k$ 个行和 $k$ 个列相交处的 $k^2$ 个元素按照原来的相对位置所构成的方阵叫做矩阵 $A$ 的 $k$ 阶子阵，其行列式的值叫做矩阵 $A$ 的 $k$ 阶子式。
>
> 矩阵 $A$ 中非奇异子阵的最高阶数（即非零子式的最高阶数）称为矩阵 $A$ 的秩，记作 $r(A)$。

### 满秩矩阵

> 设 $A$ 为 $n$ 阶方阵，当 $r(A) = n$ 时，$A$ 叫做满秩矩阵；当 $r(A) < n$ 时，$A$ 叫做降秩矩阵。

### 结论

> $r(A^T) = r(A)$

> 三秩相等定理：$r(A) = A \text{ 的行秩} = A \text{ 的列秩}$

> 设 $A$ 为 $m \times n$ 矩阵，$P$ 为 $m$ 阶可逆矩阵，若 $B = PA$，则 $A$ 中任意 $r$ 个列向量 $\boldsymbol a_{i_1}, \boldsymbol a_{i_2}, \cdots, \boldsymbol a_{i_r}$ 和 $B$ 中相应的列向量 $\boldsymbol b_{i_1}, \boldsymbol b_{i_2}, \cdots, \boldsymbol b_{i_r}$ 满足相同的线性表达式，从而具有相同的线性相关性。
>
> 推论：
>
> 1. $A$ 和 $B$ 的列向量组的极大无关组一一对应，$r(B) = r(A)$。（求最大无关组的方法）
> 1. $\boldsymbol a_j = k_1 \boldsymbol a_{i_1} + k_2 \boldsymbol a_{i_2} + \cdots + k_r \boldsymbol a_{i_r} \iff \boldsymbol b_j = k_1 \boldsymbol b_{i_1} + k_2 \boldsymbol b_{i_2} + \cdots + k_r \boldsymbol b_{i_r}$

> （初等变换不改变矩阵的秩）设 $A$ 为 $m \times n$ 矩阵，$P$ 和 $Q$ 分别为 $m$ 阶和 $n$ 阶可逆矩阵，则
>
> $$
> r(PA) = r(AQ) = r(PAQ) = r(A)
> $$

> 设 $A, B, C$ 分别为 $m \times n, s \times t, m \times t$ 矩阵，则
>
> $$
> r\left(
> \begin{bmatrix}
> A & O \\
> O & B \\
> \end{bmatrix}
> \right) = r(A) + r(B) \\
> r\left(
> \begin{bmatrix}
> A & C \\
> O & B \\
> \end{bmatrix}
> \right) \geqslant r(A) + r(B) \\
> $$

> 设 $A$ 为 $m \times k$ 矩阵，$B$ 为 $k \times n$ 矩阵，则
>
> $$
> r(A) + r(B) - k \leqslant r(AB) \leqslant \min\{r(A), r(B)\} \\
> $$

> 设 $A$ 为 $m \times k$ 矩阵，$B$ 为 $k \times n$ 矩阵，则
>
> $$
> r([A, B]) \leqslant r(A) + r(B) \\
> $$

> 设 $A$ 和 $B$ 都是 $m \times n$ 矩阵，则
>
> $$
> r(A + B) \leqslant r(A) + r(B) \\
> $$

> 设 $A$ 是 $n$ 阶方阵，则
>
> $$
> r(A^*) =
> \begin{cases}
>     n, &r(A) = n \\
>     1, &r(A) = n - 1 \\
>     0, &r(A) \leqslant n - 2 \\
> \end{cases}
> $$

> 设 $A$ 为 $n$ 阶方阵，$x$ 和 $b$ 为 $n$ 元列向量，则下列命题互为充要条件
>
> 1. $A$ 为满秩矩阵
> 1. $A$ 为非奇异矩阵
> 1. $A$ 为可逆矩阵
> 1. $A \boldsymbol x = \boldsymbol 0$ 只有零解
> 1. $A \boldsymbol x = \boldsymbol b$ 只有唯一解
> 1. $A$ 的行向量组和列向量组都是线性无关的

## 5.3 矩阵的秩在向量组中的应用

### 等价向量组

> 若向量组 Ⅰ：$\boldsymbol b_1, \boldsymbol b_2, \cdots, \boldsymbol b_n$ 中的每个向量都能由向量组 Ⅱ：$\boldsymbol a_1, \boldsymbol a_2, \cdots, \boldsymbol a_m$ 线性表示，则称向量组 Ⅰ 能由向量组 Ⅱ 线性表示。
>
> 若向量组 Ⅰ 与向量组 Ⅱ 能够相互线性表示，责成这两个向量组等价。

### 结论

> 向量组 $\boldsymbol b_1, \boldsymbol b_2, \cdots, \boldsymbol b_n$ 能由向量组 $\boldsymbol a_1, \boldsymbol a_2, \cdots, \boldsymbol a_m$ 线性表示 $\iff$ 存在矩阵 $P$，使 $B=AP$，其中，$A = [\boldsymbol a_1, \boldsymbol a_2, \cdots, \boldsymbol a_m], B = [\boldsymbol b_1, \boldsymbol b_2, \cdots, \boldsymbol b_n]$

> 若向量组 Ⅰ 能由向量组 Ⅱ 线性表示，则 $r(Ⅰ) < r(Ⅱ)$

> 若向量组 Ⅰ 与向量组 Ⅱ 等价，则 $r(Ⅰ) = r(Ⅱ)$

> 向量组 $\boldsymbol b_1, \boldsymbol b_2, \cdots, \boldsymbol b_n$ 能由向量组 $\boldsymbol a_1, \boldsymbol a_2, \cdots, \boldsymbol a_m$ 线性表示 $\iff r(\boldsymbol a_1, \boldsymbol a_2, \cdots, \boldsymbol a_m, \boldsymbol b_1, \boldsymbol b_2, \cdots, \boldsymbol b_n) = r(\boldsymbol a_1, \boldsymbol a_2, \cdots, \boldsymbol a_m)$

> 向量组 $\boldsymbol b_1, \boldsymbol b_2, \cdots, \boldsymbol b_n$ 与向量组 $\boldsymbol a_1, \boldsymbol a_2, \cdots, \boldsymbol a_m$ 等价 $\iff r(\boldsymbol a_1, \boldsymbol a_2, \cdots, \boldsymbol a_m, \boldsymbol b_1, \boldsymbol b_2, \cdots, \boldsymbol b_n) = r(\boldsymbol a_1, \boldsymbol a_2, \cdots, \boldsymbol a_m) = r(\boldsymbol b_1, \boldsymbol b_2, \cdots, \boldsymbol b_n)$

# 6 线性方程组

## 齐次线性方程组

> 齐次线性方程组 $A \boldsymbol x = \boldsymbol 0$ 只有零解（有非零解）$\iff$ $r(A) = n$（$r(A) < n$）

> 齐次线性方程组 $A \boldsymbol x = \boldsymbol 0$ 的解集 $S$ 的秩 $r(S) = n - r(A)$，即 $A \boldsymbol x = \boldsymbol 0$ 的基础解系所含向量的个数为 $n - r(A)$，其中，$n$ 为未知数的个数，即 $A$ 的列数。

> 设 $A$ 的行最简形为 $\begin{bmatrix} E_r & B \\ O & O \\ \end{bmatrix}$，其中，$B$ 为 $r \times (n - r)$ 矩阵，则 $A \boldsymbol x = \boldsymbol 0$ 的基础解系是 $\begin{bmatrix} -B \\ E_{n - r} \end{bmatrix}$ 的列向量组。

## 非齐次线性方程组

> 非齐次线性方程组 $A \boldsymbol x = \boldsymbol b$ 有唯一解（有无穷多解）$\iff$ $r(A) = n$（$r(A) < n$）

> 设 $u$ 为非齐次线性方程组 $A \boldsymbol x = \boldsymbol b$ 的一个已知解（称为特解），$\boldsymbol v_1, \boldsymbol v_2, \cdots, \boldsymbol v_{n - r}$ 为 $A \boldsymbol x = \boldsymbol 0$ 的基础解系，则 $A \boldsymbol x = \boldsymbol b$ 的通解为
>
> $$
> \boldsymbol x = k_1 \boldsymbol v_1 + k_2 \boldsymbol v_2 + \cdots + k_{n - r} \boldsymbol v_{n - r} + \boldsymbol u \\
> $$
>
> 其中 $k_1, k_2, \cdots, k_{n - r}$ 为任意常数。

## 结论

> 设 $A$ 为 $m \times n$ 实矩阵，$r(A^T A) = r(A A^T) = r(A)$

> $A^T A \boldsymbol x = A^T \boldsymbol b$ 一定有解

# 7 向量空间及向量的正交性

## 7.1 向量空间

### 向量空间

> 设 $V$ 是 $n$ 元向量的集合，如果 $V$ 非空，并且对于向量的线性运算封闭（即对任意 $v_1 \in V, v_2 \in V, k \in \mathbf R$，都有 $v_1 + v_2 \in V, kv_1 \in V$），则称 $V$ 是一个向量空间。

> 向量空间里一定有零向量。

> 向量空间 $V$ 的一个极大无关组被叫做 $V$ 的一个基，$V$ 的秩叫做 $V$ 的维数，记作 $\dim(V)$。若 $\dim(V) = r$，则称 $V$ 为 $r$ 为向量空间。

> 设 $V$ 是 $n$ 维向量空间，$m < n$，则 $V$ 中任一线性无关的向量组 $\boldsymbol v_1, \boldsymbol v_2, \cdots, \boldsymbol v_m$ 都可以扩充成 $V$ 的一个基。
>
> 可以用来求线性空间的基。

### 过渡矩阵

> 从旧基 $\boldsymbol a_1, \boldsymbol a_2, \cdots, \boldsymbol a_n$ 到新基 $\boldsymbol b_1, \boldsymbol b_2, \cdots, \boldsymbol b_n$ 的过渡矩阵 $P$（$B = AP$）的求法：记 $A = [\boldsymbol a_1, \boldsymbol a_2, \cdots, \boldsymbol a_n], B = [\boldsymbol b_1, \boldsymbol b_2, \cdots, \boldsymbol b_n]$，使用初等行变换将 $[A, B]$ 左侧 $n \times n$ 化成单位矩阵，右侧即为 $P$。

> 过渡矩阵是可逆矩阵。

## 7.2 向量的正交性

### 向量的内积

> 设 $\boldsymbol a = [a_1, a_2, \cdots, a_n]^T, \boldsymbol b = [b_1, b_2, \cdots, b_n]^T$ 是两个实向量，$\boldsymbol a$ 与 $\boldsymbol b$ 的内积记作 $(\boldsymbol a, \boldsymbol b)$，规定
>
> $$
> (\boldsymbol a, \boldsymbol b) = a_1 b_1 + a_2 b_2 + \cdots + a_n b_n = \boldsymbol a^T b \\
> $$

> 1. $(\boldsymbol a, \boldsymbol b) = (\boldsymbol b, \boldsymbol a)$
> 1. $(k \boldsymbol a, \boldsymbol b) = k (\boldsymbol a, \boldsymbol b)$
> 1. $(\boldsymbol a + \boldsymbol b, \boldsymbol c) = (\boldsymbol a, \boldsymbol c) + (\boldsymbol b, \boldsymbol c)$
> 1. $(\boldsymbol a, \boldsymbol a) \geqslant 0$，且 $(\boldsymbol a, \boldsymbol a) = 0 \iff \boldsymbol a = \boldsymbol 0$

### 向量的长度（范数）

> 实向量 $\boldsymbol a = [a_1, a_2, \cdots, a_n]^T$ 的长度（也叫做范数）记作 $||a||$，规定 
>
> $$
> ||a|| = \sqrt{(\boldsymbol a, \boldsymbol a)} = \sqrt{a_1^2 + a_2^2 + \cdots + a_n^2} \\
> $$

> 对于非零向量 $\boldsymbol a$，称 $\dfrac{\boldsymbol a}{||\boldsymbol a||}$ 为 $\boldsymbol a$ 的单位化向量。

> 1. $||\boldsymbol a|| \geqslant 0$，且 $||\boldsymbol a|| = 0 \iff \boldsymbol a = \boldsymbol 0$
> 1. $||k \boldsymbol a|| = |k| \times ||\boldsymbol a||$
> 1. $||\boldsymbol a + \boldsymbol b|| \leqslant ||\boldsymbol a|| + ||\boldsymbol b||$
> 1. $|(\boldsymbol a, \boldsymbol b)| \leqslant ||\boldsymbol a|| \times ||\boldsymbol b||$

### 正交向量组

> 由两两正交的非零向量组成的向量组称为正交向量组，由单位向量组成的正交向量组成为标准正交向量组。

> 正交向量组一定线性无关。

### 施密特正交化方法

> 设 $\boldsymbol a_1, \boldsymbol a_2, \cdots, \boldsymbol a_n$ 是一个线性无关的向量组，若令
>
> $$
\begin{cases}
    b_1 = a_1, \\
    b_j = a_j - \displaystyle\sum_{i = 1}^{j - 1} \frac{b_i^T a_j}{||\boldsymbol b_i||^2} b_i \\
\end{cases}
> $$
>
> 则 $\boldsymbol b_1, \boldsymbol b_2, \cdots, \boldsymbol b_n$ 是与 $\boldsymbol a_1, \boldsymbol a_2, \cdots, \boldsymbol a_n$ 等价的正交向量组。

### 正交矩阵

> 若实方阵 $A$ 满足 $A^T A = E$，则称 $A$ 为正交矩阵。

> 设 $A, B$ 为同阶正交矩阵，则
>
> 1. $A$ 可逆，且 $A^{-1} = A^T$
> 1. $A^T$ 为正交矩阵（即 $A^{-1}$ 为正交矩阵）
> 1. $AB$ 为正交矩阵
> 1. $|A| = \plusmn 1$

> 实方阵 $A$ 为正交矩阵 $\iff$ $A$ 的列向量组为标准正交向量组
