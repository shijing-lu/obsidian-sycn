
#### 1. D 为 X 型区域
设积分区域 $D$ 可以表示为 $\{(x, y) \mid a \leq x \leq b, \varphi_1(x) \leq y \leq \varphi_2(x)\}$，则
$$
\iint_D f(x, y) d\sigma = \int_a^b \left[ \int_{\varphi_1(x)}^{\varphi_2(x)} f(x, y) dy \right] dx
$$
这也称为**先对 $y$，后对 $x$ 的二次积分**，也常记作
$$
\iint_D f(x, y) d\sigma = \int_a^b dx \int_{\varphi_1(x)}^{\varphi_2(x)} f(x, y) dy
$$

#### 2. D 为 Y 型区域
设积分区域 $D$ 可以表示为 $\{(x, y) \mid c \leq y \leq d, \psi_1(y) \leq x \leq \psi_2(y)\}$，则
$$
\iint_D f(x, y) d\sigma = \int_c^d dy \int_{\psi_1(y)}^{\psi_2(y)} f(x, y) dx
$$
**注**：若 $D$ 为其他类型的区域，可作辅助线将 $D$ 划分为若干不相交的 $X$ 型和 $Y$ 型区域，利用二重积分可加性将 $D$ 上的二重积分转化为各子区域上二重积分之和。