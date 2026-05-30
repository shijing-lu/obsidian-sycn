# 27 基础阶段 线代讲义题 十习题

## 前言

同学你好，感谢你选择【Kira(张珊)·2027 考研数学全程班】！本书为内部学员基础阶段的线性代数基础通关讲义，旨在帮助各位学员从零基础起步到搭建出完整的线性代数知识框架。

考研线性代数学习必然要经历两个阶段，每个阶段都是先难后易的。

首先，从零起步最难，因为线代是完全独立于高数的、我们中学阶段几乎未接触过的数学分支。每一个概念定理题型计算都是新知识，光是记住和区分各种知识点就够头疼了。但 Kira 老师一直强调，一开始做 10 道题用各种公式会觉得多，但做 200 道、500 道题来来回回还是这些题型公式，便觉得不过如此。基础阶段对线代从生到熟的过程，也是感受从难到易的过程。

其次，强化阶段线代知识会继续交叉、深化、升华，各章节之间的联系开始浮现，此时会觉得“仿佛在学全新的线性代数”（但 Kira 老师有直达本质的醒脑的办法！）。把第二阶段咬牙啃下来，线代彻底通透之后，怎么做都是满分——每道题不是缺少方法，而是方法太多了，以至于不知道该选哪一个！Kira 老师每年带出的线代满分学员们，都完全理解上述真相！听话照做，必有所成！

线性代数只要吃透基础强化两阶段的全部例题，即可应对各种题目。以适量习题作为训练举一反三、加深对例题理解、自测能力的工具即可。

如有任何问题，可通过以下官方账号联系 Kira 老师

B 站：一高数/上交 Kira 老师

抖音：上交 Kira 老师

公众号：考研数学 Kira

微博：考研数学 Kira

---

## 目录

序篇 Hi，解线性方程组吗？ 1  
第一章 行列式 3  
第二章 矩阵 16  
第三章 向量 45  
第四章 线性方程组 59  
第五章 特征值与特征向量 69  
第六章 二次型 79

---

## 序篇 Hi，解线性方程组吗？

[引子]

《孙子算经》

### 【行列式是一种运算规则】

从线性方程组的角度：“线性”（Linear）——“常数乘变量”之和；一次的。

解二元线性方程组  
$$
\left\{ \begin{array}{l}a_{11}x_{1} + a_{12}x_{2} = b_{1}\\ a_{21}x_{1} + a_{22}x_{2} = b_{2} \end{array} \right.
$$  
当 $a_{11}a_{22} - a_{12}a_{21}\neq 0$ 时，做同解变形

由③得唯一解 $x_{2} = \frac{b_{1}a_{22} - a_{12}b_{2}}{a_{11}a_{22} - a_{12}a_{21}}$ ，代入①或同理消去 $x_{2}$ 得唯一解 $x_{1} = \frac{b_{2}a_{11} - a_{21}b_{1}}{a_{11}a_{22} - a_{12}a_{21}}$

(①.①.①)不好看也不好记！

为了便于表示，数学上规定运算规则 $\left| \begin{array}{ll}a_{11} & a_{12}\\ a_{21} & a_{22} \end{array} \right| = a_{11}a_{22} - a_{12}a_{21}$ ，故方程组的解可表示为

↑此结论称为“克拉默法则”

同理，用高斯消元法解三元线性方程组

并规定运算规则

则 $D_{3}\neq 0$ 时，线性方程组的解可以表示为

↑此结论称为“克拉默法则”

那么，能否进一步定义 $n$ 阶行列式，统一表示 $n$ 元线性方程组的解呢？

带着这个问题，我们开始第一章～

领取主线任务：「会解任何一个 n 元线性方程组」

---

## 第一章 行列式

### 考试要求

1. 了解行列式的概念，掌握行列式的性质。
2. 会应用行列式的性质和行列式按行（列）展开定理计算行列式。

---

### 二、行列式按行（列）展开定理

#### 1. 余子式（Minor）和代数余子式（Algebraic Cofactor）

1）余子式 $M_{ij}$ ：在 $n$ 阶行列式中，把元素 $a_{ij}$ 所在的第 $i$ 行第 $j$ 列划去后，由剩余的元素按原位置顺序所构成的 $n - 1$ 阶行列式，称为元素 $a_{ij}$ 的余子式，记作 $M_{ij}$

2）代数余子式 $A_{ij}$ ： $(-1)^{i + j}M_{ij}$ 称为元素 $a_{ij}$ 的代数余子式，记为 $A_{ij}$ ，即

$$
A_{ij} = (-1)^{i + j}M_{ij}.
$$

注：

1. 余子式和代数余子式都是行列式；
2. 余子式和代数余子式值与 $a_{ij}$ 的具体取值无关，只与 $a_{ij}$ 的位置有关。

#### 2. ☆行列式按行（列）展开定理

定理：行列式的值等于其任一行(列)的各元素与其对应代数余子式的乘积之和，即

$$
D = \sum_{k = 1}^{n}a_{ik}A_{ik} = a_{i1}A_{i1} + a_{i2}A_{i2} + \ldots +a_{in}A_{in} \quad (i = 1,2,3\dots n)
$$

$$
D = \sum_{k = 1}^{n}a_{kj}A_{kj} = a_{1j}A_{1j} + a_{2j}A_{2j} + \ldots +a_{nj}A_{nj} \quad (j = 1,2,3\dots n)
$$

---

### 三、行列式的性质

性质 1- 转置行列式的行与列(按原顺序)互换，行列式的值不变，即

注：互换后的行列式称为转置行列式

性质 2- 对换行列式的两行（列）互换，行列式的值反号

推论：如果行列式中有两行（列）完全相同，则行列式的值为零

性质 3- 倍乘行列式的某行(列)每个元素都乘常数 $k$ ，则等于用 $k$ 乘此行列式的值

推论：1）若行列式中某行（列）元素全为零，则行列式的值为零；

2）若行列式中两行（列）对应元素成比例，其值为零

性质 4- 拆分：如果行列式某行(列)元素都写成两数之和，则该行列式可以写成两个行列式之和，即

例：二阶行列式

性质 5- 将行列式的某行（列）的每个元素都乘常数 $k$ ，再加到另一行（列）的对应元素上，行列式的值不变，即

---

### 四、拉普拉斯公式

设 $A,B$ 分别为 $m$ 与 $n$ 阶矩阵，则

---

### [一起计算行列式吧～]

### 五、计算行列式的常见题型与方法

1. 化零降阶法（坚守原则：“打洞”、“降阶”）

方法：先利用性质将行列式的某一行或某一列化到只有一个元素不为 0，再用行列式展开定理化为低一阶的行列式（化零降阶法是计算行列式的主要方法）。

( $\bullet \bullet \bullet \bullet$ )/ $\triangledown$ 二八法则（不平衡法则）：

社会上 $20\%$ 的人占有 $80\%$ 的财富； $20\%$ 的员工为企业创造了 $80\%$ 的收益；你一生使用的 $80\%$ 的文句是用字典里 $20\%$ 的字组成的...

$80\%$ 的行列式可以用 $20\%$ 的常规方法（化零降阶法）计算。

考试中， $20\%$ 的核心知识能为你带来 $80\%$ 的分数。

### 重要小结论

(1)上、下三角行列式的值:

$$
\begin{vmatrix}
a_{11} & 0 & \cdots & 0 \\
a_{21} & a_{22} & \cdots & 0 \\
\vdots & \vdots & \ddots & \vdots \\
a_{n1} & a_{n2} & \cdots & a_{nn}
\end{vmatrix} = a_{11}a_{22}\cdots a_{nn}
$$

(2)次上、下三角行列式的值:

$$
\begin{vmatrix}
0 & \cdots & 0 & a_{1n} \\
0 & \cdots & a_{2,n-1} & a_{2n} \\
\vdots & \ddots & \vdots & \vdots \\
a_{n1} & a_{n2} & \cdots & a_{nn}
\end{vmatrix} = (-1)^{\frac{n(n-1)}{2}} a_{1n}a_{2,n-1}\cdots a_{n1}
$$

#### 2. 化三角形行列式

类型 1：各行(列)元素之和相等的行列式(各行全部加到第一行(列))

类型 2：爪型行列式（各行倍加到第一行，“消去平爪”）

类型 3：三对角行列式（逐行相减，化三角行列式；递推法）

#### 3. 递推法（强化）

#### 4. 数学归纳法（强化）

数学归纳法是证明（计算）行列式常用的方法。首先建立递推关系，当递推关系仅涉及相邻两阶行列式时，采用第一归纳法；当递推关系涉及相邻三阶行列式时，采用第二归纳法。

##### 1）第一数学归纳法：

① 设有一个与自然数 $n$ 有关的命题，若当 $n = 1$ 时命题成立 ② 假设当 $n = k$ 时命题成立，可以推出当 $n = k + 1$ 时命题成立，那么命题对一切自然数 $n$ 都成立。

##### 2）第二数学归纳法：

设有一个与自然数 $n$ 有关的命题，若 ① 当 $n = 1$ 和 $n = 2$ 时命题成立 ② 假设对 $n< k$ 的一切自然数都成立，则 $n = k$ 时命题也成立，那么命题对一切自然数 $n$ 都成立。

#### 5. 范德蒙行列式

定义：形如

$$
\begin{vmatrix}
1 & 1 & \cdots & 1 \\
x_1 & x_2 & \cdots & x_n \\
x_1^2 & x_2^2 & \cdots & x_n^2 \\
\vdots & \vdots & \ddots & \vdots \\
x_1^{n-1} & x_2^{n-1} & \cdots & x_n^{n-1}
\end{vmatrix} = \prod_{1 \leq i < j \leq n} (x_j - x_i)
$$

的行列式称为范德蒙行列式

范德蒙行列式的特点：

1）第一行全为 1。

2）每列元素 $1,x_{1},x_{1}^{2},\dots ,x_{1}^{n - 1}$ 按 $x_{i}$ 的升幂排列，构成一个以 $x_{i}$ 为公比的等比数列。

思考：将行列式最后一行换到第一行，其他行顺序不变，该如何操作？此时新行列式的值与原行列式的值有何关系？

---

### 六、行列式按行（列）展开定理的推论

行列式按行(列)展开定理的推论:

设行列式 $D = \begin{vmatrix}
a_{11} & a_{12} & \dots & a_{1 n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{i 1} & a_{i 2} & \dots & a_{in} \\
\vdots & \vdots & \ddots & \vdots \\
a_{j 1} & a_{j 2} & \dots & a_{jn} \\
\vdots & \vdots & \ddots & \vdots \\
a_{n 1} & a_{n 2} & \dots & a_{nn}
\end{vmatrix}$ 任一行(列)各元素与另一行(或列)对应元素的代数余子式的乘积之和等于零，即

$$
\sum_{k = 1}^{n}a_{ik}A_{jk} = a_{i1}A_{j1} + a_{i2}A_{j2} + \ldots +a_{in}A_{jn} = 0\quad (i\neq j)
$$

$$
\sum_{k = 1}^{n}a_{ki}A_{kj} = a_{1i}A_{1j} + a_{2i}A_{2j} + \ldots +a_{ni}A_{nj} = 0\quad (i\neq j)
$$

这是因为，当 $i\neq j$ 时，

更一般地，

---

### 七、 $n$ 阶行列式完全展开式（逆序数定义）

1. 排列：将 $n$ 个不同元素按一定顺序排成一列，叫做这 $n$ 个元素的全排列，简称排列。比如 354216 就是这 6 个元素的一个排列。

注：不同的 $n$ 元排列共有 $n!$ 个。

2. 逆序与逆序数： $n$ 级排列 $j_{1}\dots j_{n}$ 中，若一对数 $j_{s}j_{t}$ ，小数排在大数后面，即 $j_{s} > j_{t}$ ，则 $j_{s}j_{t}$ 构成了一个逆序。一个排列中逆序的总和叫做这个排列的逆序数，记为 $\tau (j_{1}\dots j_{n})$

逆序数的计算方法：数出每个数的逆序个数，所有数的逆序个数求和就是排列逆序数。例如，求 436512 的逆序数， $\tau (436512) = 3 + 2 + 3 + 2 + 0 + 0 = 10.$

3. 奇排列和偶排列：逆序数为偶数的排列称为偶排列，逆序数为奇数的排列为奇排列。

4. $n$ 阶行列式完全展开式（逆序数定义）：

$$
\begin{vmatrix}
a_{11} & a_{12} & \cdots & a_{1n} \\
a_{21} & a_{22} & \cdots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{n1} & a_{n2} & \cdots & a_{nn}
\end{vmatrix} = \sum_{j_1 j_2 \cdots j_n} (-1)^{\tau(j_1 j_2 \cdots j_n)} a_{1j_1} a_{2j_2} \cdots a_{nj_n}
$$

称此式为 $n$ 阶行列式的完全展开式，其值是所有取自不同行不同列的 $n$ 个元素乘积的代数和，各项正负号由列标对应的排列 $j_{1},j_{2}\dots j_{n}$ 的逆序数决定。当 $j_{1},j_{2}\dots j_{n}$ 是偶排列时，该项取正号，当 $j_{1},j_{2}\dots j_{n}$ 是奇排列时，该项取负号。

注：用完全展开式求行列式通常计算量很大。只在有行列式大量元素为 0，只有少数项不为 0 时，或在分析线性因子的特定问题中，才考虑使用定义法。

注：三对角行列式（递推法、归纳法）“体会一切递推的万能思路（高数都能用！）”

【步骤】 ① 直接按第一行（列）展开；

② 等式两端凑出相同形式并递推到最低阶，形如

$$
D_{n} - aD_{n - 1} = k\left(D_{n - 1} - aD_{n - 2}\right) = \dots = k^{n - 2}\left(D_{2} - aD_{1}\right)
$$

③ 由上一步得到 $D_{n} = f\left(D_{n - 1}\right)$ ，递推即得 $D_{n}$

注：么字型行列式——用手比一个“么”字，按指尖连线所在的行或列展开，得到递推式 $D_{n} = f\left(D_{n - 1}\right)$

---

## 第二章 矩阵

### 考试要求

1. 理解矩阵的概念，了解单位矩阵、数量矩阵、对角矩阵、三角矩阵、对称矩阵和反对称矩阵以及它们的性质。

2. 掌握矩阵的线性运算、乘法、转置以及它们的运算规律，了解方阵的幂与方阵乘积的行列式的性质。

3. 理解逆矩阵的概念，掌握逆矩阵的性质以及矩阵可逆的充分必要条件，理解伴随矩阵的概念，会用伴随矩阵求逆矩阵。

4. 理解矩阵初等变换的概念，了解初等矩阵的性质和矩阵等价的概念，理解矩阵的秩的概念，掌握用初等变换求矩阵的秩和逆矩阵的方法。

5. 了解分块矩阵及其运算。

### 【要矩阵有何用？——作为线性方程组的简单记法！】

回到【序篇】的线性方程组——

解二元线性方程组 $\left\{ \begin{array}{l}a_{11}x_{1} + a_{12}x_{2} = b_{1} \\ a_{21}x_{1} + a_{22}x_{2} = b_{2} \end{array} \right.$ 当 $a_{11}a_{22} - a_{12}a_{21}\neq 0$ 时，做同解变形

由③得唯一解 $x_{2} = \frac{b_{1}a_{22} - a_{12}b_{2}}{a_{11}a_{22} - a_{12}a_{21}}$ 代入①或同理消去 $x_{2}$ 得唯一解 $x_{1} = \frac{b_{2}a_{11} - a_{21}b_{1}}{a_{11}a_{22} - a_{12}a_{21}}$

$(\bullet ,\bullet ,\bullet)$ 方程组的解和求解过程，均与未知量字母无关，只与系数和右端常数有关～

对线性方程组 $\left\{ \begin{array}{l}a_{11}x_{1} + a_{12}x_{2} = b_{1} \\ a_{21}x_{1} + a_{22}x_{2} = b_{2} \end{array} \right.$ 的研究，可以转化为研究方程的

系数矩阵 $A = \left( \begin{array}{cc}a_{11} & a_{12} \\ a_{21} & a_{22} \end{array} \right)$ 和增广矩阵 $(A,b) = \left( \begin{array}{cc}a_{11} & a_{12} \\ a_{21} & a_{22} \end{array} ; \begin{array}{c}b_{1} \\ b_{2} \end{array} \right)$

---

### 知识讲解

### 一、矩阵（Matrix）的概念

#### 1. 定义

1）矩阵由 $m\times n$ 个数 $a_{ij}(i = 1,2,\dots ,m;j = 1,2,\dots ,n)$ 排成 $m$ 行 $n$ 列的数表

$$
A = \begin{pmatrix}
a_{11} & a_{12} & \cdots & a_{1n} \\
a_{21} & a_{22} & \cdots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1} & a_{m2} & \cdots & a_{mn}
\end{pmatrix}
$$

称为一个 $m$ 行 $n$ 列矩阵，简称 $m\times n$ 矩阵，记作 $\pmb{A}$ 或 $A_{m\times n}$ 。当 $m = n$ 时，称 $\pmb{A}_{n}$ 为 $n$ 阶矩阵(或 $n$ 阶方阵)。 $\vert A\vert$ 称为 $\pmb{A}$ 的行列式。

注：1）矩阵不一定方（行数 $=$ 列数）！！不方的矩阵没有“阶数”“n 阶"的说法！！

2）后续的逆矩阵、伴随矩阵、幂、行列式、特征值特征向量等的研究对象都是 n 阶方阵。

2）元素：这 $m\times n$ 个数 $a_{ij}$ 称为矩阵 $\pmb{A}$ 的第 $i$ 行第 $j$ 列元素，简称为元，以数 $a_{ij}$ 为元素的矩阵可简记作 $A = (a_{ij})$ 或 $(a_{ij})_{m\times n}(i = 1,2,\dots ,m;j = 1,2,\dots ,n)$ ，其中横排为行，竖排为列。

注：特别地， $1\times 1$ 矩阵 $\left(a_{11}\right)$ 是一个数，可以直接记为 $a_{11}$

3）实矩阵：元素是实数的矩阵称为实矩阵（考研仅考察实矩阵）

#### 2. 常见矩阵关系

1）同型矩阵：行数、列数都相同的矩阵称为同型矩阵。

2）矩阵相等：如果两个同型矩阵 $A = (a_{ij})_{m\times n}$ 和 $B = (b_{ij})_{m\times n}$ 的各元素也对应相等，即 $a_{ij} = b_{ij}(i = 1,2,\dots ,m;j = 1,2,\dots ,n)$ ，则称 $\pmb{A}$ 和 $\pmb{B}$ 相等，记作 $A = B$

#### 3. 矩阵与行列式的区别

1）矩阵是一个数表，行数和列数可以不相等；行列式是一个算式，行数和列数必须相等；

2）两个矩阵相等是指两个矩阵同型且对应元素完全相同；两个行列式的值相等不一定有对应元素相等，甚至阶数也不一定相等。

例如行列式 $\left| \begin{array}{ll}1 & 2\\ 0 & 1 \end{array} \right| = \left| \begin{array}{ll}1 & 1\\ 1 & 1 \end{array} \right| = 1$ ，但矩阵 $\left( \begin{array}{ll}1 & 2\\ 0 & 1 \end{array} \right)\neq \left( \begin{array}{ll}1 & 1\\ 1 & 1 \end{array} \right)$

---

### 二、矩阵的运算——“数据批量化处理”

#### 1. 矩阵的线性运算

##### 1) 矩阵的加法

■ 矩阵加法定义：设有两个 $m \times n$ 矩阵 $A = (a_{ij})$ 和 $B = (b_{ij})$ ，规定

$$
A + B = (a_{ij} + b_{ij})_{m \times n}
$$

注：只有同型矩阵才能相加。

■ 矩阵的加法满足运算律：

① 交换律： $A + B = B + A$ ； ② 结合律： $(A + B) + C = A + (B + C)$ ；

③ $A + O = A$； ④ $A + (-A) = O$。

##### 2) 矩阵的数量乘法（数乘）

■ 矩阵数乘定义：设 $k$ 是任意常数， $A = (a_{ij})$ ，将 $k$ 乘到矩阵的每个元素上，即

$$
kA = (k a_{ij})_{m \times n}
$$

■ 矩阵的数乘满足运算律

① 加乘分配律： $k(A + B) = kA + kB$ ， $(k + l)A = kA + lA$ ；

② 数乘结合律： $k(lA) = (kl)A$

③ $cA = O \Leftrightarrow c = 0$ 或 $A = 0$

#### 2. 矩阵的乘法

##### 1) 定义

设 $m \times n$ 矩阵 $A = \begin{pmatrix}
a_{11} & a_{12} & \dots & a_{1 n} \\
a_{21} & a_{22} & \dots & a_{2 n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m 1} & a_{m 2} & \dots & a_{mn}
\end{pmatrix}$ 和 $n \times s$ 矩阵 $B = \begin{pmatrix}
b_{11} & b_{12} & \dots & b_{1 s} \\
b_{21} & b_{22} & \dots & b_{2 s} \\
\vdots & \vdots & \ddots & \vdots \\
b_{n 1} & b_{n 2} & \dots & b_{ns}
\end{pmatrix}$ ，则 $A, B$ 的乘积

$AB = (c_{ij})_{m \times n}$ 是一个 $m \times s$ 矩阵，其中

即矩阵 $\pmb{C} = \pmb{A}\pmb{B}$ 的第 $i$ 行第 $j$ 列元素 $c_{ij}$ 是 $\pmb{A}$ 第 $i$ 行的 $n$ 个元素与 $\pmb{B}$ 第 $j$ 列对应的 $n$ 个元素分别相乘的乘积之和，有

$$
c_{ij} = \sum_{k=1}^{n} a_{ik} b_{kj}
$$

$(\oplus \dots \oplus) / \nabla$ 矩阵乘法可将线性运算表达得更简洁 $\downarrow$

【应用】

将线性方程组 $\left\{ \begin{array}{l}2x + 3y = 1 \\ - x + 5y = 2 \end{array} \right.$ 写成矩阵乘法形式。

【解答】

记 $A = \begin{bmatrix} 2 & 3 \\ -1 & 5 \end{bmatrix}$ （称为“系数矩阵”）， $x = \begin{bmatrix} x \\ y \end{bmatrix}, b = \begin{bmatrix} 1 \\ 2 \end{bmatrix}$ ，原线性方程组可改写为

$$
A x = b
$$

此为线性方程组的矩阵形式。

对线性方程组 $\left\{ \begin{array}{l}a_{11}x_{1} + a_{12}x_{2} = b_{1} \\ a_{21}x_{1} + a_{22}x_{2} = b_{2} \end{array} \right.$ 的研究，可以转化为研究方程的

注：在本章“初等变换与初等矩阵”一节中，矩阵乘法还可以作为矩阵初等行、列变换的“记录员”

$(\text{◍•ᴗ•◍})ﾉ♡$ 点＆向量可通过矩阵乘法做线性变换——让空间扭曲的”二向箔“

注：矩阵乘法与数的乘法的区别

① 矩阵乘法左边矩阵的列数必须与右边矩阵的行数相同，否则不能相乘；

② 矩阵乘法不满足交换律，一般 $AB \neq BA$ ；

③ 矩阵乘法中， $AB = O \not\Rightarrow A = O$ 或 $B = O$

##### 2）矩阵乘法满足的运算律

① 结合律： $(AB)C = A(BC)$

② 左、右分配律： $C(A + B) = CA + CB$； $(A + B)C = AC + BC$；

③ 数乘结合律： $(kA)(lB) = (kl)(AB)$

④ $E_m A_{m\times n} = A_{m\times n} E_n = A_{m\times n}$；

⑤ $AO = O$，$OA = O$

#### 3. 矩阵的转置

##### 1）矩阵转置的定义

将 $m\times n$ 矩阵 $A = \begin{pmatrix}
a_{11} & a_{12} & \dots & a_{1 n} \\
a_{21} & a_{22} & \dots & a_{2 n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m 1} & a_{m 2} & \dots & a_{mn}
\end{pmatrix}$ 的行与列的元素互换位置，得到的一个 $n\times m$ 矩阵，称为 $A$ 的转置矩阵，记作 $A^T$ ，即

$$
A^T = \begin{pmatrix}
a_{11} & a_{21} & \dots & a_{m1} \\
a_{12} & a_{22} & \dots & a_{m2} \\
\vdots & \vdots & \ddots & \vdots \\
a_{1n} & a_{2n} & \dots & a_{mn}
\end{pmatrix}
$$

##### 2）转置矩阵的运算性质

① $(A^T)^T = A$； ② $(A + B)^T = A^T + B^T$； ③ $(kA)^T = kA^T$； ④ $(AB)^T = B^T A^T$

结论： $\operatorname{tr}(\alpha \beta^T) = \beta^T \alpha$ （ $\alpha, \beta$ 为 $n$ 维列向量）。

证明：以 3 维为例，由 $\alpha^T \beta = (a_1, a_2, a_3) \begin{pmatrix} b_1 \\ b_2 \\ b_3 \end{pmatrix} = a_1 b_1 + a_2 b_2 + a_3 b_3$，

---

### 三、常见特殊矩阵

1) 行矩阵（列矩阵）：只有一行的矩阵 $A = (a_{11}, a_{12}, \dots, a_{1n})$ 称为行矩阵，又称行向量；只有一列的矩阵 $B = \begin{pmatrix} b_1 \\ b_2 \\ \vdots \\ b_n \end{pmatrix}$ 称为列矩阵或列向量。

2) 零矩阵： $m\times n$ 个元素全为零的矩阵称为零矩阵，记作 $\pmb{O}$

注：不同型的零矩阵不相等。

3) 三角矩阵：主对角线下方元素全为 0 的 $n$ 阶矩阵称为上三角矩阵，主对角线上方元素全为 0 的 $n$ 阶矩阵称为下三角矩阵，上、下三角矩阵合称为三角矩阵。形状分别如下：

上（下）三角矩阵具有如下性质：

① 如果 $A, B$ 为同类型的三角矩阵，则 $kA, A+B, AB$ 仍为三角矩阵；

② 如果 $A$ 为上（下）三角矩阵，则 $A^T$ 为下（上）三角矩阵；

③ $|A| = a_{11} a_{22} \dots a_{nn}$

4) 对角矩阵：主对角线上的元素是任意常数，其余元素都为 0 的 $n$ 阶矩阵，称为 $n$ 阶对角矩阵（简称对角阵），记作 $A$ ，即

对角矩阵有如下性质：

① 若 $A, B$ 为同阶对角矩阵，则 $kA, A+B, AB$ 仍为同阶对角矩阵；

② 若 $A$ 为对角矩阵，则 $A^T = A$

③ 若 $A$ 为对角矩阵，则 $|A| = \lambda_1 \lambda_2 \dots \lambda_n$

5) 单位矩阵——类似于"1"的存在：主对角线上的元素都为 1 的 $n$ 阶对角矩阵，称为 $n$ 阶单位矩阵（简称单位阵），记作 $E$ 。

注：单位矩阵的作用类似常数 1，如 $E_m A_{m\times n} = A_{m\times n} E_n = A_{m\times n}$，$A^0 = E$ 等

6) 数量矩阵：若对角矩阵主对角线上的元素相等，则称为数量矩阵。

数量矩阵有如下性质：

① 如果 $A, B$ 为同阶数量矩阵，则 $kA, A+B, AB$ 仍为同阶的数量矩阵；

② $A^T = A$

③ $A = aE$（ $a$ 为 $A$ 的主对角元）；

④ $AB = BA = aB$（ $A$ 为数量矩阵， $B$ 为同阶方阵）；

⑤ $|A| = a^n$

7) 对称矩阵：设 $A = (a_{ij})$ 是一个 $n$ 阶矩阵，如果 $a_{ij} = a_{ji} (i, j = 1, 2, \dots, n)$ ，即 $A^T = A$ ，则称 $A$ 为对称矩阵。

8) 反对称矩阵：设 $A = (a_{ij})$ 是一个 $n$ 阶矩阵，如果 $a_{ij} = -a_{ji} (i, j = 1, 2, \dots, n)$ ，即 $A^T = -A$ ，则称 $A$ 为反对称矩阵。

#### 反对称矩阵有如下性质

① 反对称矩阵的主对角元 $a_{ii}$ 全为零；

② 对于奇数阶的反对称矩阵 $A$ ，有 $|A| = 0$

注：任何一个 $n$ 阶矩阵 $A$ 都可以表示成一个对称矩阵与一个反对称矩阵的和，即

$$
A = \frac{1}{2}(A + A^T) + \frac{1}{2}(A - A^T)
$$

---

### 四、方阵的幂

#### 1. 矩阵可交换

定义： $A, B$ 为同阶方阵，若有 $AB = BA$ ，则称矩阵 $A$ 与 $B$ 可交换。

$A, B$ 可交换时，有以下等价命题成立：

$$
AB = BA \Leftrightarrow (A \pm B)^2 = A^2 \pm 2AB + B^2 \Leftrightarrow (A + B)(A - B) = A^2 - B^2
$$

$$
\Leftrightarrow (A + B)^n = \sum_{k=0}^n C_n^k A^{n-k} B^k
$$

#### 2. 方阵的幂

定义：设 $A$ 是 $n$ 阶矩阵，定义 $A^k = AA\dots A$ （ $k$ 个 $A$ 相乘），称 $A^k$ 为 $A$ 的 $k$ 次幂。特别地，若存在整数 $m$ ，使 $A^m = O$ ，称 $A$ 为幂零矩阵。规定 $A^0 = E$ 。

运算规律： ① $A^m A^n = A^{m+n} = A^n A^m$； ② $(A^m)^n = A^{mn}$（ $m, n$ 为正整数）。

注：1）只有方阵才有幂。

2）显然，方阵的幂是可交换的。

#### 2. 方阵的多项式

定义：设 $x$ 的 $k$ 次多项式 $f(x) = a_k x^k + a_{k-1} x^{k-1} + \dots + a_1 x + a_0$ ， $A$ 是 $n$ 阶矩阵，称

$$
f(A) = a_k A^k + a_{k-1} A^{k-1} + \dots + a_1 A + a_0 E_n
$$

为矩阵 $A$ 的一个 $k$ 次多项式

性质：

1）矩阵 $A$ 的两个多项式 $f(A)$ 和 $\phi(A)$ 总是可交换的。（因为 $A^k, A^l, E$ 都可交换）

2）矩阵 $A$ 的多项式可以像数的多项式一样相乘或因式分解。例如

$$
A^2 + 2A - 3E = (A + 3E)(A - E)， (A + E)(E - 2A) = -2A^2 - A + E
$$

注：若 $A = \begin{pmatrix}
\lambda_1 & & & \\
& \lambda_2 & & \\
& & \ddots & \\
& & & \lambda_n
\end{pmatrix}$ 为对角矩阵，则

$$
f(A) = a_0 E + a_1 A + \dots + a_m A^m = \begin{pmatrix}
f(\lambda_1) & & & \\
& f(\lambda_2) & & \\
& & \ddots & \\
& & & f(\lambda_n)
\end{pmatrix}
$$

### [矩阵有除法吗？]

### 五、矩阵的逆 $A^{-1}$

#### 1. 逆矩阵的定义

设 $A$ 是 $n$ 阶矩阵，如果存在 $n$ 阶矩阵 $B$ ，使得

$$
AB = BA = E
$$

则称 $A$ 为可逆矩阵（简称 $A$ 可逆)，记为 $A^{-1}$

注：1）可逆矩阵一定都是方阵

2）设 $A$ 是 $n$ 阶矩阵，若存在 $n$ 阶矩阵 $B$ ，使得 $AB = E$ ，则 $BA = E$ 。即只要有 $AB = E$ 或 $BA = E$ ，即可得出 $A, B$ 互为逆矩阵的结论， $A^{-1} = B, B^{-1} = A$

3）单位矩阵的逆矩阵是它本身。

#### 2. 逆矩阵的性质

1) 若 $A$ 可逆，则 $A^{-1}$ 唯一。

证：设 $AB_1 = B_1 A = E$， $AB_2 = B_2 A = E$ ，则 $B_1 = B_1 E = B_1 A B_2 = E B_2 = B_2$

2) $A$ 可逆的充要条件是 $|A| \neq 0$ ，此时 $A^{-1} = \frac{1}{|A|} A^*$

3) 若 $A$ 可逆，则 $A^T$ ， $A^{-1}$ 均可逆，且有 $(A^T)^{-1} = (A^{-1})^T$ ， $(A^{-1})^{-1} = A$

4) 若 $A$ 可逆，且 $k \neq 0$ ，则 $(kA)^{-1} = \frac{1}{k} A^{-1}$

5) 设 $A, B$ 为同阶可逆矩阵，则 $AB$ 也可逆，且 $(AB)^{-1} = B^{-1} A^{-1}$

推广： ① $(A_1 A_2 \dots A_s)^{-1} = A_s^{-1} A_{s-1}^{-1} \dots A_2^{-1} A_1^{-1}$； ② $A^{-k} \triangleq (A^k)^{-1} = (A^{-1})^k$

6) $|A^{-1}| = |A|^{-1}$

7) 如果 $A$ 是可逆矩阵，则 $A^*$ 也可逆，且 $(A^*)^{-1} = \frac{A}{|A|} = (A^{-1})^*$

注：若 $A, B$ 为同阶可逆矩阵，则 $A + B$ 不一定可逆；若 $A, B, A+B$ 为同阶可逆矩阵，也不一定有 $(A+B)^{-1} = A^{-1} + B^{-1}$ 成立。

---

### 六、伴随矩阵 $A^*$

#### 1. 伴随矩阵的定义

设 $A_{ij}$ 为方阵 $A = \begin{pmatrix}
a_{11} & a_{12} & \dots & a_{1 n} \\
a_{21} & a_{22} & \dots & a_{2 n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{n 1} & a_{n 2} & \dots & a_{nn}
\end{pmatrix}$ 的行列式 $|A|$ 中 $a_{ij}$ 的代数余子式，定义

$$
A^* = \begin{pmatrix}
A_{11} & A_{21} & \dots & A_{n1} \\
A_{12} & A_{22} & \dots & A_{n2} \\
\vdots & \vdots & \ddots & \vdots \\
A_{1n} & A_{2n} & \dots & A_{nn}
\end{pmatrix}
$$

为方阵 $A$ 的伴随矩阵，记作 $A^*$

注：1）为什么将 $A^*$ 定义为代数余子式转置？

若 $A^*$ 可逆，用反证法，假设 $A$ 不可逆，则 $A A^* = |A| E = O$ 。等式两端在右边乘 $(A^*)^{-1}$ ，得 $A A^* (A^*)^{-1} = O (A^*)^{-1}$ 即 $A = O$ 。此时 $A$ 的全部代数余子式 $A_{ij} = 0$ ，其伴随矩阵 $A^* = O$ ，与 $A^*$ 可逆矛盾。故 $A$ 可逆。

#### 3. 利用伴随矩阵求逆矩阵（低阶数值型矩阵求逆）

公式： $A^{-1} = \frac{A^*}{|A|}$

---

### 七、方阵行列式

#### 1. 方阵行列式的运算律

1) $|A^T| = |A|$；

2) $|\lambda A| = \lambda^n |A|$；

3) $|AB| = |A||B|$；

4) $|A^k| = |A|^k$；

5) $|A^{-1}| = |A|^{-1}$；

6) $|A^*| = |A|^{n-1}$；

注：1) 一般地， $|A \pm B| \neq |A| \pm |B|$

2) 若 $A = O$ ，则 $|A| = 0$ ，但 $|A| = 0$ 推不出 $A = O$

---

### 八、分块矩阵

1. 将矩阵 $A$ 用若干条纵线和横线分成许多个小矩阵，每一个小矩阵称为 $A$ 的子块，以子块为元素的形式上的矩阵称为分块矩阵。

2. 分块矩阵的运算规则与普通矩阵的运算规则类似。

3) 设两个矩阵行数、列数相同，采用相同的分块法，有

$$
\begin{pmatrix} A_{11} & A_{12} \\ A_{21} & A_{22} \end{pmatrix} + \begin{pmatrix} B_{11} & B_{12} \\ B_{21} & B_{22} \end{pmatrix} = \begin{pmatrix} A_{11}+B_{11} & A_{12}+B_{12} \\ A_{21}+B_{21} & A_{22}+B_{22} \end{pmatrix}
$$

2) 设有分块矩阵和常数 $k$ ，有

$$
k \begin{pmatrix} A_{11} & A_{12} \\ A_{21} & A_{22} \end{pmatrix} = \begin{pmatrix} kA_{11} & kA_{12} \\ kA_{21} & kA_{22} \end{pmatrix}
$$

3) 乘法：设两个分块矩阵的子块对应的列数和行数符合矩阵乘法的要求，则

$$
\begin{pmatrix} A_{11} & A_{12} \\ A_{21} & A_{22} \end{pmatrix} \begin{pmatrix} B_{11} & B_{12} \\ B_{21} & B_{22} \end{pmatrix} = \begin{pmatrix} A_{11}B_{11}+A_{12}B_{21} & A_{11}B_{12}+A_{12}B_{22} \\ A_{21}B_{11}+A_{22}B_{21} & A_{21}B_{12}+A_{22}B_{22} \end{pmatrix}
$$

4) 转置：

$$
\begin{pmatrix} A_{11} & A_{12} \\ A_{21} & A_{22} \end{pmatrix}^T = \begin{pmatrix} A_{11}^T & A_{21}^T \\ A_{12}^T & A_{22}^T \end{pmatrix}
$$

5) 分块三角矩阵的逆矩阵：

$$
\begin{pmatrix} A & O \\ C & B \end{pmatrix}^{-1} = \begin{pmatrix} A^{-1} & O \\ -B^{-1}CA^{-1} & B^{-1} \end{pmatrix}, \quad
\begin{pmatrix} A & C \\ O & B \end{pmatrix}^{-1} = \begin{pmatrix} A^{-1} & -A^{-1}CB^{-1} \\ O & B^{-1} \end{pmatrix}
$$

6) 分块(副)对角矩阵的逆矩阵（假设每个子块都可逆）：

$$
\begin{pmatrix} A & O \\ O & B \end{pmatrix}^{-1} = \begin{pmatrix} A^{-1} & O \\ O & B^{-1} \end{pmatrix}, \quad
\begin{pmatrix} O & A \\ B & O \end{pmatrix}^{-1} = \begin{pmatrix} O & B^{-1} \\ A^{-1} & O \end{pmatrix}
$$

7) 分块对角矩阵的幂：

$$
\begin{pmatrix} A & O \\ O & B \end{pmatrix}^k = \begin{pmatrix} A^k & O \\ O & B^k \end{pmatrix}
$$

注：分块副对角矩阵的幂无此规律。

8) 拉普拉斯公式：

① $\begin{vmatrix} A & O \\ * & B \end{vmatrix} = |A||B|$， $\begin{vmatrix} A & * \\ O & B \end{vmatrix} = |A||B|$

② $\begin{vmatrix} O & A \\ B & * \end{vmatrix} = (-1)^{mn} |A||B|$， $\begin{vmatrix} * & A \\ B & O \end{vmatrix} = (-1)^{mn} |A||B|$

③ $\begin{vmatrix} A_1 & & \\ & \ddots & \\ & & A_k \end{vmatrix} = |A_1||A_2|\dots|A_k|$， $|A_i| \neq 0 (i=1,2,\dots,k)$

（设 $A$ 为 $m$ 阶方阵， $B$ 为 $n$ 阶方阵， $A_i$ 为方阵）

注：设 $G = \begin{pmatrix} A & B \\ C & D \end{pmatrix}$ 为分块矩阵，且 $|G| \neq 0$ ，则注意以下不成立的等式

---

### 九、矩阵的初等变换

引入：消元法解线性方程组（方程组的同解变换）

#### 1. 初等变换的定义

对矩阵施行以下三种变换称为矩阵的初等变换

(1) 交换矩阵的两行（列），即 $r_i \leftrightarrow r_j$ 或 $c_i \leftrightarrow c_j$

(2) 以一个非零的数 $k$ 乘矩阵的某一行（列），即 $k r_i$ 或 $k c_i$ ， $k \neq 0$

(3) 将矩阵的某一行（列）乘以常数 $k$ 加到另一行（或列），即 $r_i + k r_j$ 或 $c_i + k c_j$

#### 2. 初等矩阵

1）定义：对单位矩阵 $E$ 作一次初等（行或列）变换所得的矩阵

2）三种初等矩阵（对应三种初等变换）：

$E_{ij}$ ：交换 $E$ 的 $i, j$ 两行（或列）所得到的矩阵

$E_i(k)$ ：用非零数 $k$ 乘 $E$ 的第 $i$ 行（或列）所得到的矩阵

$E_{ij}(k)$ ：把 $E$ 的第 $j$ 行的 $k$ 倍加到第 $i$ 行上（或把第 $i$ 列的 $k$ 倍加到第 $j$ 列上）所得到的矩阵

例如： $E_{12} = \begin{pmatrix} 0 & 1 & 0 \\ 1 & 0 & 0 \\ 0 & 0 & 1 \end{pmatrix}$， $E_3(-2) = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & -2 \end{pmatrix}$， $E_{21}(3) = \begin{pmatrix} 1 & 0 & 0 \\ 3 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix}$

3）定理：对矩阵 $A$ 作一次初等行（列）变换，相当于用一个相应的初等矩阵 $P$ 左（右）乘 $A$

( $\bullet \bullet \bullet$ ) 初等矩阵乘法可以"记录"矩阵的初等变换！

#### 4) 结论

① 初等矩阵均可逆，且其逆是同类型的初等矩阵，即

$$
E_{ij}^{-1} = E_{ij}, \quad E_i^{-1}(k) = E_i\left(\frac{1}{k}\right), \quad E_{ij}^{-1}(k) = E_{ij}(-k)
$$

例如： $E_{12}^{-1} = \begin{pmatrix} 0 & 1 & 0 \\ 1 & 0 & 0 \\ 0 & 0 & 1 \end{pmatrix}^{-1} = \begin{pmatrix} 0 & 1 & 0 \\ 1 & 0 & 0 \\ 0 & 0 & 1 \end{pmatrix} = E_{12}$

$$
E_3^{-1}(-2) = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & -2 \end{pmatrix}^{-1} = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & -\frac{1}{2} \end{pmatrix} = E_3\left(-\frac{1}{2}\right)
$$

$$
E_{21}^{-1}(3) = \begin{pmatrix} 1 & 0 & 0 \\ 3 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix}^{-1} = \begin{pmatrix} 1 & 0 & 0 \\ -3 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix} = E_{21}(-3)
$$

② $|E_{ij}| = -1$， $|E_i(k)| = k$， $|E_{ij}(k)| = 1$

#### 3. 几种初等变换下的特殊矩阵

1) 行阶梯形矩阵

定义：非零矩阵若满足下列条件：

① 所有零行在非零行的下面；

② 非零行的首非零元所在列在上一行（如果存在的话）的首非零元所在列的右面，

则称此矩阵为行阶梯形矩阵。

2) 行最简形矩阵

定义：行阶梯形矩阵若还满足下列条件：

① 各非零行的首非零元为 1；

② 首非零元所在列的其他元均为 0，

则称此行阶梯形矩阵为行最简形矩阵

3) 矩阵的等价标准形

特点是：

① 左上角是一个单位阵；

② 其余行列（如果有的话）元素全为 0

4) 定理：任一矩阵 $A_{m\times n}$ 总可经过初等行变换化为行阶梯形矩阵，再经过初等行变换化为行最简形矩阵，最后通过初等列变换化为标准形

$$
F = \begin{pmatrix} E_r & O \\ O & O \end{pmatrix}_{m \times n}
$$

---

### 十、利用初等变换求逆矩阵/解矩阵方程

#### 1. 利用初等变换求逆矩阵

$$
(A, E) \xrightarrow{\text{初等行变换}} (E, A^{-1})
$$

#### 2. 利用初等变换解矩阵方程

矩阵不能规定除法，乘法的逆运算是解矩阵方程（含有未知矩阵的等式）：

$$
(\mathrm{I}) \ AX = B, \qquad (\mathrm{II}) \ XA = B
$$

这里假定 $A$ 可逆，在此条件下，这两个方程的解都是存在并且唯一的，其中矩阵方程(I)的解为 $X = A^{-1}B$ ，(II)的解为 $X = BA^{-1}$ 。

用初等变换法解矩阵方程 $AX = B$ ， $XA = B$ 和 $AXB = C$

$$
(A, B) \xrightarrow{\text{初等行变换}} (E, X)
$$

---

### 十一、矩阵的等价

#### 1. 矩阵等价的定义

矩阵 $A_{m\times n}$ 经有限次初等变换化为 $B$ ，即存在一系列 $m$ 阶初等阵 $P_1, P_2, \dots, P_k$ 和一系列 $n$ 阶初等阵 $Q_1, Q_2, \dots, Q_l$ 使

$$
P_1 P_2 \dots P_k A Q_1 Q_2 \dots Q_l = B
$$

则称矩阵 $A$ 与 $B$ 等价，记作 $A \cong B$

注：若矩阵 $A_{m\times n}$ 经有限次初等行变换化为 $B$ ，则称矩阵 $A$ 与 $B$ 行等价；若矩阵 $A_{m\times n}$ 经有限次初等列变换化为 $B$ ，则称矩阵 $A$ 与 $B$ 列等价。

#### 2. 矩阵等价的等价命题

1) $A$ 经过有限次初等变换变成 $B$

2) 存在有限个初等阵 $P_1, \dots, P_s, Q_1, \dots, Q_t$ 使得 $P_s \dots P_1 A Q_1 \dots Q_t = B$

3) 存在可逆阵 $P, Q$ ，使得 $PAQ = B$

4) 同型矩阵 $A$ 与 $B$ 等价 $\Leftrightarrow r(A) = r(B)$

#### 推论

1) 可逆矩阵可经过有限次初等变换化为单位矩阵，即 $A$ 与 $E$ 等价。

2) 若矩阵 $B$ 可逆，则必存在有限个初等阵 $P_1, \dots, P_s$ ，使得 $B = P_1 \dots P_s$

#### 3. 矩阵等价的性质

1) 反身性： $A \cong A$

2) 对称性：若 $A \cong B$ ，则 $B \cong A$

3) 传递性：若 $A \cong B$ ， $B \cong C$ ，则 $A \cong C$

#### 4. 矩阵行等价的等价命题

1) $A$ 经过有限次初等行变换变成 $B$

2) 存在有限个初等阵 $P_1, P_2, \dots, P_s$ ，使得 $P_s \dots P_2 P_1 A = B$

3) 存在可逆阵 $P$ ，使得 $PA = B$

#### 5. 矩阵列等价的等价命题

1) $A$ 经过有限次初等列变换变成 $B$

2) 存在有限个初等阵 $Q_1, Q_2, \dots, Q_t$ ，使得 $A Q_1 Q_2 \dots Q_t = B$

3) 存在可逆阵 $Q$ ，使得 $AQ = B$

---

### 十二、矩阵的秩（最得力的解题小帮手！）

#### 1. 矩阵子式的概念

在矩阵 $A_{m\times n}$ 中，任取 $k$ 行和 $k$ 列（ $0 \leq k \leq m, 0 \leq k \leq n$ ），位于这些行列交叉处的 $k^2$ 个元素，不改变它们在 $A_{m\times n}$ 中所处的位置次序而得到的 $k$ 阶行列式，称为矩阵 $A_{m\times n}$ 的 $k$ 阶子式。

注：

1) 矩阵 $A$ 的任意一个元素都是 $A$ 的一个一阶子式。

2) $n$ 阶方阵 $A$ 的唯一 $n$ 阶子式是 $|A|$

#### 2. 矩阵的秩的概念

定义 1：矩阵 $A$ 的所有非零子式的最高阶数，称为矩阵 $A$ 的秩。记作 $r(A)$

定义 2：设在矩阵 $A$ 中有一个不为 0 的 $r$ 阶子式，且所有 $r+1$ 阶子式（如果存在的话）全为 0，则数 $r$ 称为矩阵 $A$ 的秩。

规定零矩阵的秩等于 0，故有 $A = O \Leftrightarrow r(A) = 0$

#### 易知

1) 矩阵 $A$ 中有一个 $s$ 阶子式不为 $0 \Leftrightarrow r(A) \geq s$

2) 矩阵 $A$ 中所有 $t$ 阶子式全为 $0 \Leftrightarrow r(A) < t$

#### 3. 求数量型矩阵的秩

定理：初等变换不改变矩阵的秩

方法：1) 定义法（最高阶子式法）

2) 初等变换法：可通过初等行变换化矩阵为行阶梯形，非零行的行数即为矩阵的秩。

进阶——含参数矩阵化行阶梯形、秩的讨论（在方程组和向量部分有大用！）

#### 【直观理解秩】

“有效行数”“有效方程个数”

$\begin{pmatrix} 1 & 1 \\ 2 & 2 \\ 3 & 3 \\ 4 & 4 \end{pmatrix}$ “1 个有效行”， $\begin{pmatrix} 1 & 1 \\ 1 & -1 \end{pmatrix}$ “2 个有效行”。 $\begin{cases} x + y = 0 \\ 2 x + 2 y = 0 \\ 3 x + 3 y = 0 \\ 4 x + 4 y = 0 \end{cases}$ “1 个有效方程”， $\begin{cases} x + y = 0 \\ x - y = 0 \end{cases}$ “2 个有效方程”

#### 4. 矩阵秩的重要结论

1) $r(A) = 0 \Leftrightarrow A = O$ ， $r(A) \geq 1 \Leftrightarrow A \neq O$

2) $0 \leq r(A_{m\times n}) \leq \min\{m, n\}$

3) $r(kA) = r(A)$（ $k \neq 0$）

4) $r(A) = r(A^T) = r(A^T A) = r(AA^T)$

5) $r(A_{m\times n}) + r(B_{n\times s}) - n \leq r(AB) \leq \min\{r(A), r(B)\}$

6) $r(A) - r(B) \leq r(A \pm B) \leq r(A) + r(B)$

7) $\max\{r(A), r(B)\} \leq r(A, B) \leq r(A) + r(B)$

8) 若 $A_{m\times n} B_{n\times s} = O$ ，则 $r(A) + r(B) \leq n$

9) 若 $P, Q$ 可逆，则 $r(PA) = r(AQ) = r(PAQ) = r(A)$

更一般地，若 $A$ 列满秩（即 $r(A_{m\times n}) = n$ ）则 $r(AB) = r(B)$ ，且有左消去律 $AB = O \Rightarrow B = O$ ， $AB = AC \Rightarrow B = C$。（同理， $A$ 行满秩时有右消去律）。

10) 矩阵 $A$ 和 $B$ 等价 $\Leftrightarrow r(A) = r(B)$

11) 伴随矩阵的秩

$$
r(A^*) = \begin{cases}
n, & \text{若 } r(A) = n \\
1, & \text{若 } r(A) = n-1 \\
0, & \text{若 } r(A) < n-1
\end{cases}
$$

12) 分块矩阵的秩

$$
r(A, B) \leq r(A) + r(B), \quad r\begin{pmatrix} A & O \\ O & B \end{pmatrix} = r(A) + r(B)
$$

13) $A$ 为 $n$ 阶满秩矩阵 $\Leftrightarrow r(A) = n \Leftrightarrow |A| \neq 0 \Leftrightarrow A$ 为可逆矩阵。

---

### 附录

性质 6【证明】对分块矩阵作初等变换得

得 $r(A + B) \leq r\begin{pmatrix} A & O \\ O & B \end{pmatrix} = r(A) + r(B)$ ，同理，

得 $r(A) \leq r\begin{pmatrix} A + B & O \\ O & B \end{pmatrix} = r(A + B) + r(B)$ ，得证。

性质 7【证明】 $A$ 的最高阶非零子式也是 $(A, B)$ 的非零子式

故 $r(A) \leq r(A, B)$ ，同理 $r(B) \leq r(A, B)$ 。又 $(A, B) \xrightarrow{c} (\tilde{A}, \tilde{B})$ ，其中 $\tilde{A}, \tilde{B}$ 为列最简形，故 $r(A, B) = r(\tilde{A}, \tilde{B}) \leq r(\tilde{A}) + r(\tilde{B}) = r(A) + r(B)$

性质 9【证明】由 $r(A_{m\times n}) = n$ ，存在 $m$ 阶可逆矩阵 $P$ 使 $PA = \begin{pmatrix} E_n \\ O \end{pmatrix}_{m\times n}$ ，而 $PAB_{n\times s} = \begin{pmatrix} E_n \\ O \end{pmatrix} B_{n\times s} = \begin{pmatrix} B \\ O \end{pmatrix}_{m\times s}$ ，故 $r(AB) = r(PAB) = r(B) = r(B)$

---

## 第三章 向量

### 考试要求

1. 理解 $n$ 维向量、向量的线性组合与线性表示的概念，掌握向量的加法和数乘运算法则。

2. 理解向量组线性相关、线性无关的概念，掌握向量组线性相关、线性无关的有关性质及判别法。

3. 理解向量组的极大线性无关组和向量组的秩的概念，会求向量组的极大线性无关组及秩。

4. 理解向量组等价的概念，理解矩阵的秩与其行（列）向量组的秩之间的关系。

5. 了解内积的概念，掌握线性无关向量组正交规范化的施密特（Schmidt）方法。了解正交矩阵的概念和性质。

6. 了解 $n$ 维向量空间、子空间、基底、维数、坐标等概念。了解基变换和坐标变换公式，会求过渡矩阵。了解规范正交基的概念以及它们的性质（数一）。

### 知识讲解

### 一、向量的概念

#### 1. 向量的定义

向量的定义：由 $n$ 个数 $a_1, a_2, \ldots, a_n$ 组成的有序数组，称为一个 $n$ 维向量。

若用一行表示，称为 $n$ 维行向量，即 $1\times n$ 矩阵，记作 $\pmb{a}^T = (a_1, a_2, \dots, a_n)$

若用一列表示，称为 $n$ 维列向量，即 $n\times 1$ 矩阵，记作 $\pmb{a} = (a_1, a_2, \dots, a_n)^T$

其中 $a_i$ 称为向量 $\pmb{a}$ 的第 $i$ 个分量。

注：考研中在没有指明时，都看作列向量。

向量组：由多个同型向量（维数相同且都为行向量或列向量）组成的集合称为向量组。

#### 2. 向量的运算

$\pmb{a} = (a_1, a_2, \dots, a_n)^T$， $\pmb{\beta} = (b_1, b_2, \dots, b_n)^T$

1) 向量相等：两个 $n$ 维向量相等当且仅当它们各对应分量都相等，即

$\pmb{a} = \pmb{\beta} \Leftrightarrow a_i = b_i (i = 1, 2, \dots, n)$

2) 零向量：所有分量全为零的向量称为零向量，记做 $\mathbf{0}$， $\pmb{a} = \mathbf{0} \Leftrightarrow a_i = 0 (i = 1, 2, \dots, n)$

3) 向量加法： $\pmb{a} \pm \pmb{\beta} = (a_1 \pm b_1, a_2 \pm b_2, \dots, a_n \pm b_n)^T$

4) 向量数乘： $k\pmb{a} = (k a_1, k a_2, \dots, k a_n)^T$

5) 向量内积： $\alpha^T \beta = (a_1, a_2, \dots, a_n) \begin{pmatrix} b_1 \\ b_2 \\ \vdots \\ b_n \end{pmatrix} = a_1 b_1 + a_2 b_2 + \dots + a_n b_n$

向量内积的性质：

① $(\alpha, \beta) = (\beta, \alpha)$

② $(\lambda \alpha, \beta) = \lambda (\alpha, \beta)$

③ $(\alpha + \beta, \chi) = (\alpha, \chi) + (\beta, \chi)$

④ 当 $\alpha = 0$ 时， $(\alpha, \alpha) = 0$；当 $\alpha \neq 0$ 时， $(\alpha, \alpha) > 0$

6) 向量正交：若 $\alpha^T \beta = 0$ ，称向量 $\alpha, \beta$ 正交。

向量正交的推论：

① $\alpha^T \alpha = 0 \Leftrightarrow a_1^2 + a_2^2 + \dots + a_n^2 = 0 \Leftrightarrow \alpha = 0$（ $\alpha$ 与自身正交当且仅当 $\alpha$ 是零向量）；

② 零向量与任何同型向量正交。

7) 向量的长度：令 $\|\alpha\| = \sqrt{(\alpha, \alpha)} = \sqrt{a_1^2 + a_2^2 + \dots + a_n^2}$ ， $\|\alpha\|$ 称为 $n$ 维向量 $\alpha$ 的长度

向量长度的性质：

① 非负性：当 $\alpha \neq 0$ 时， $\|\alpha\| > 0$；当 $\alpha = 0$ 时， $\|\alpha\| = 0$

② 齐次性： $\|\lambda \alpha\| = |\lambda| \|\alpha\|$

8) 单位化：当 $\|\alpha\| = 1$ 时， $\alpha$ 称为单位向量。若 $\beta \neq 0$ ，取 $\alpha = \frac{\beta}{\|\beta\|}$ ，则 $\alpha$ 是一个单位向量。由向量 $\beta$ 得到 $\alpha$ 的过程称为把向量 $\beta$ 单位化。

---

### 二、向量间的线性表示

#### 1. 线性组合

设 $\alpha_1, \alpha_2, \dots, \alpha_s$ 是一组 $n$ 维向量， $k_1, k_2, \dots, k_s$ 是一组常数，则称

$$
k_1 \alpha_1 + k_2 \alpha_2 + \ldots + k_s \alpha_s
$$

为 $\alpha_1, \alpha_2, \dots, \alpha_s$ 的一个线性组合。

#### 2. 向量组的线性表示

设有一组 $n$ 维向量 $\alpha_1, \alpha_2, \dots, \alpha_s$ ，以及向量 $\beta$ ，若存在一组常数 $k_1, k_2, \dots, k_s$ ，使

$$
k_1 \alpha_1 + k_2 \alpha_2 + \ldots + k_s \alpha_s = \beta
$$

则称 $\beta$ 可以由 $\alpha_1, \alpha_2, \dots, \alpha_s$ 线性表示，或称 $\beta$ 为 $\alpha_1, \alpha_2, \dots, \alpha_s$ 的一个线性组合。

注：1) 零向量可由任意一组向量线性表示；

2) 向量组 $\alpha_1, \alpha_2, \dots, \alpha_s$ 中的任一向量 $\alpha_j$（ $j = 1, 2, \dots, s$）都可由此向量组线性表示。

#### 3. 向量组线性表示的等价命题（紧密结合第四章线性方程组）

1) 向量 $\beta$ 可由向量组 $\alpha_1, \alpha_2, \dots, \alpha_s$ 线性表示且表示法唯一

存在且仅存在一组常数 $k_1, k_2, \dots, k_s$ 使 $k_1 \alpha_1 + k_2 \alpha_2 + \dots + k_s \alpha_s = \beta$

$\Leftrightarrow$ 非齐次线性方程组 $(\alpha_1, \alpha_2, \dots, \alpha_s) \begin{pmatrix} x_1 \\ x_2 \\ \vdots \\ x_s \end{pmatrix} = \beta$ 有唯一解

$\Leftrightarrow r(\alpha_1, \alpha_2, \dots, \alpha_s) = r(\alpha_1, \alpha_2, \dots, \alpha_s, \beta) = s$

2) 向量 $\beta$ 可由向量组 $\alpha_1, \alpha_2, \dots, \alpha_s$ 线性表示且表示法不唯一（无穷多种）

存在无穷多组常数 $k_1, k_2, \ldots, k_s$ 使 $k_1 \alpha_1 + k_2 \alpha_2 + \ldots + k_s \alpha_s = \beta$

$\Leftrightarrow$ 非齐次线性方程组 $(\alpha_1, \alpha_2, \dots, \alpha_s) \begin{pmatrix} x_1 \\ x_2 \\ \vdots \\ x_s \end{pmatrix} = \beta$ 有无穷多解

$\Leftrightarrow r(\alpha_1, \alpha_2, \dots, \alpha_s) = r(\alpha_1, \alpha_2, \dots, \alpha_s, \beta) < s$

3) 向量 $\beta$ 不可由向量组 $\alpha_1, \alpha_2, \dots, \alpha_s$ 线性表示

不存在一组常数 $k_1, k_2, \ldots, k_s$ 使 $k_1 \alpha_1 + k_2 \alpha_2 + \ldots + k_s \alpha_s = \beta$

$\Leftrightarrow$ 非齐次线性方程组 $(\alpha_1, \alpha_2, \dots, \alpha_s) \begin{pmatrix} x_1 \\ x_2 \\ \vdots \\ x_s \end{pmatrix} = \beta$ 无解

$\Leftrightarrow r(\alpha_1, \alpha_2, \dots, \alpha_s) < r(\alpha_1, \alpha_2, \dots, \alpha_s, \beta) \Leftrightarrow r(\alpha_1, \alpha_2, \dots, \alpha_s) + 1 = r(\alpha_1, \alpha_2, \dots, \alpha_s, \beta)$

4) 向量组 $\beta_1, \beta_2, \dots, \beta_s$ 可由向量组 $\alpha_1, \alpha_2, \dots, \alpha_m$ 线性表示

$\Leftrightarrow r(\alpha_1, \alpha_2, \dots, \alpha_m, \beta_1, \beta_2, \dots, \beta_s) = r(\alpha_1, \alpha_2, \dots, \alpha_m)$

$\Rightarrow r(\beta_1, \beta_2, \dots, \beta_s) \leq r(\alpha_1, \alpha_2, \dots, \alpha_m)$

注：

1) $r(\beta_1, \beta_2, \dots, \beta_s) \leq r(\alpha_1, \alpha_2, \dots, \alpha_m)$ 推不出向量组 $\beta_1, \beta_2, \dots, \beta_s$ 可由向量组 $\alpha_1, \alpha_2, \dots, \