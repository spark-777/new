

# 随机事件与概率

## 条件概率公式

- $P(B|A)=\frac{P(AB)}{p(A)}$

## 概率性质

- $P(A\cup B)=P(A)+P(B)-P(AB)$,$P(A\cup B \cup C)=P(A)+P(B)+P(C)-P(AB)-P(AC)-P(BC)+P(ABC)$

- 减法公式  $P(A-B)=P(A)-P(AB)=P(A\overline{B})$

- 德摩根率  $\overline{A\cup B}=\overline{A}\cap\overline{B},\overline{A\cap B}=\overline{A}\cup\overline{B},P(\overline A\quad \overline B\quad \overline C)=P(\overline A \cap\overline B\cap \overline C)=P(\overline{A\cup B \cup C})$

- 独立事件 即如果有若干个事件相互独立，则其中一部分事件的运算生成的事件与另一部分事件运算生成的事件仍然相互独立

## 全概率公式

- $$
  P(B)=\sum_{i=1}^n P\left(A_i\right) P\left(B \mid A_i\right)
  $$

## 贝叶斯

- $$
  P\left(A_j \mid B\right)=\frac{P\left(A_j B\right)}{P(B)}=\frac{P\left(A_j\right) P\left(B \mid A_j\right)}{\sum_{i=1}^n P\left(A_i\right) P\left(B \mid A_i\right)}, j=1,2, \cdots, n
  $$

## 用最值

当遇到与 $\max \{X, Y\}, \min \{X, Y\}$ 有关的事件时, 下面一些关系式是经常要用到的:

- $\{\max \{X, Y\} \leqslant a\}=\{X \leqslant a\} \cap\{Y \leqslant a\}$
-  $\{\max \{X, Y\}>a\}=\{X>a\} \cup\{Y>a\}$
- $\{\min \{X, Y\} \leqslant a\}=\{X \leqslant a\} \cup\{Y \leqslant a\}$
-  $\{\min \{X, Y\}>a\}=\{X>a\} \cap\{Y>a\}$
-  $\{\max \{X, Y\} \leqslant a\} \subseteq\{\min \{X, Y\} \leqslant a\}$
- $\{\min \{X, Y\}>a\} \subseteq\{\max \{X, Y\}>a\}$

# 一维随机变量及其分布

## 分布函数性质

- 非负性，单调不减
- $F(-\infty )\lim\limits_{x\rightarrow -\infty}F(x)=0,F(+\infty )\lim\limits_{x\rightarrow +\infty}F(x)=1$

- 右连续函数

- $F(x)=p(X<x)$

## 概率密度

- $P(a<x<b)=\int^b_af(x)dx=F(b)-F(a)$,$f(x)$为概率密度  $F(x)$，为分布函数
- $P(a<x)=\int_af(x)dx=-F(a)$,$f(x)$为概率密度  $F(x)$，为分布函数

## 常见的随机变量分布类型

### 离散型

- $X\sim p_i,$则$F(x)=\sum\limits_{x_i\leq x}p_i$(梯形函数)

- $0-1$   分布$B(1-p)$

- 二项分布

  - $$
    U_k=P\{X=k\}=C_n^k p^k(1-p)^{n-k},
    $$

- 几何分布

  - $P\{X=k\}=(1-p)^{k-1}p(k=1,2,..;0<p<1)$

- 超几何分布

  - $$
    P\{X=k\}=\frac{\mathrm{C}_{\mathrm{M}}^k \mathrm{C}_{N-M}^{n-k}}{\mathrm{C}_N^n}(\max \{0, n-N+M\} \leqslant k \leqslant \min \{M, n\}\\
    M,N,n为正整数andM<=N,n<=N,k为整数
    $$
- 泊松分布

  - $P\{X=k\}=\frac{\lambda^k}{k!}e^{-k}(k=0,1,...;\lambda>0)$


### 连续型

- $X\sim f(x),$则$F(x)=\int^x_{-\infty}f(t)dt$
- 均匀分布

- 指数分布

  - $$
    f(x)=\left\{\begin{array}{ll}
    \lambda \mathrm{e}^{-\lambda x}, & x \geqslant 0, \\
    0, & \text { 其他 }
    \end{array}(\lambda>0), F(x)=\left\{\begin{array}{ll}
    1-\mathrm{e}^{-\lambda x}, & x \geqslant 0, \\
    0, & x<0
    \end{array}(\lambda>0),\right.\right.
    $$

  - 无记忆性$\rightarrow P\{X \ge t+s|X\ge t\}=P\{X\ge s\}$

- 正态分布
  
  - $F(x)=P\{X\leq x \}=\Phi(\frac{x-\mu}{\sigma})$
  - $\Phi(-x)=1-\Phi(x)$
  - $X\sim N(\mu,\sigma^2)\rightarrow \frac{X-\mu}{\sigma}\sim N(0,1)$
  - $F(x)=P(X\le x)=\Phi(\frac{x-\mu}{\sigma})$
  
  - $aX+b\sim N(a\mu+b,a^2\sigma^2)(a\not =0)$
  
  - $X\sim N(\mu_1,\sigma_1^2),Y\sim N(\mu_2,\sigma^2_2)$且$X,Y$独立可得
  - $X+Y\sim N(\mu_1+\mu_2,\sigma_1^2+\sigma_2^2),X-Y\sim N(\mu_1-\mu_2,\sigma_1^2+\sigma_2^2)$
  


### 混合型分布

- $F(x)=P\{X\leq x\}$

## 常用分布的期望和方差

$$
\begin{array}{c|l|l|l}
{分布}&{分布列p_k或概率密度f(x)}&{期望}&{方差}\\
\hline
{0-1分布}&P \{X=k\}=p^k(1-p)^{1-k},k=0,1,...&{p}&{p(1-p)}\\
\hline
{二项分布B(n,p)}&{P\{X=k\}=C^k_np^k(1-p)^{n-k},k=0,1,...}&{np}&{np(1-p)}\\
\hline
{泊松P(\lambda)}&{P\{X=k\}=\frac{\lambda^k}{k!}e^{-\lambda},k=0,1,...}&{\lambda}&{\lambda}\\
\hline
{几何分布G(p)}&{P\{X=k\}=(1-p)^{k-1}p,k=1,2,...}&{\frac{1}{p}}&{\frac{1-p}{p^2}}\\
\hline
{正态分布N(\mu,\sigma^2)}&{f(x)=
\frac{1}{\sqrt{2 \pi} \sigma} \mathrm{e}^{-\frac{1}{2}\left(\frac{x-\mu}{\sigma}\right)^2}
}&{\mu}&{\sigma^2}\\
\hline
{均匀分布U(a,b)}&{f(x)=\frac{1}{b-a},a<x<b}&{\frac{a+b}{2}}&{\frac{(b-a)^2}{12}}\\
\hline
指数分布E(\lambda)&f(x)=\lambda e^{-\lambda x},x>0&\frac{1}{\lambda}&\frac{1}{\lambda^2}
\end{array}
$$

## 用分布$X\sim F(x)$
- $P(X\le a)=F(a)$
- $P(X<a)=F(a-0)$
- $P(X=a)=P(X\le a)-P(X<a)$
- $P(a<X<b)=P(X<b)-P(X\le a)$
- $P(a\le X\le b)=P(X\le b)-P(X<a)$

# 多维随机变量及分布

### 联合概率密度

若X，Y互相独立，X和Y的联合概率密度为$f(x,y)=f_X(x)f_Y(y)$



### 边缘分布

- $F_X(x)=F(x,+\infty),F_Y(y)=F(+\infty,y)$
- $f_X(x)=\int^{+\infty}_{-\infty}f(x,y)dy,f_Y(y)=\int^{+\infty}_{-\infty}f(x,y)dx$

### 二维均匀分布

称（X,Y）在平面有界区域D上服从均匀分布，如果（X,Y）的概率密度为

$S_D$为区域D的面积
$$
f(x,y)=\left\{ 
    \begin{array}{lc}
        \frac{1}{S_D}&(x,y)\in D  \\
        0&其他 \\
    \end{array}
\right.
$$

### 正态分布

如果 $(X, Y)$ 的概率密度为

$$
f(x, y)=\frac{1}{2 \pi \sigma_1 \sigma_2 \sqrt{1-\rho^2}} \exp \left\{-\frac{1}{2\left(1-\rho^2\right)}\left[\left(\frac{x-\mu_1}{\sigma_1}\right)^2-2 \rho\left(\frac{x-\mu_1}{\sigma_1}\right)\left(\frac{y-\mu_2}{\sigma_2}\right)+\left(\frac{y-\mu_2}{\sigma_2}\right)^2\right]\right\},
$$
其中 $\mu_1 \in \mathbf{R}, \mu_2 \in \mathbf{R}, \sigma_1>0, \sigma_2>0,-1<\rho<1$, 则称 $(X, Y)$ 服从参数为 $\mu_1, \mu_2, \sigma_1^2, \sigma_2^2, \rho$ 的二维正态分布, 记 为 $(X, Y) \sim N\left(\mu_1, \mu_2 ; \sigma_1^2, \sigma_2^2 ; \rho\right)$

- $\rho$为X与Y的相关系数,独立则$\rho =0$

- $$
  \rho=\frac{Cov(X,Y)}{\sqrt{DX}\sqrt{DY}}=\frac{Cov(X,Y)}{\sigma_1 \sigma_2}
  $$

  

【注】有下面 6 条重要结论

- 若 $\left(X_1, X_2\right) \sim N\left(\mu_1, \mu_2 ; \sigma_1^2, \sigma_2^2 ; \rho\right)$, 则

$$
X_1 \sim N\left(\mu_1, \sigma_1^2\right), X_2 \sim N\left(\mu_2, \sigma_2^2\right) .
$$
- 若 $X_1 \sim N\left(\mu_1, \sigma_1^2\right), X_2 \sim N\left(\mu_2, \sigma_2^2\right)$ 且 $X_1, X_2$ 相互独立, 则

$$
\left(X_1, X_2\right) \sim N\left(\mu_1, \mu_2 ; \sigma_1^2, \sigma_2^2 ; 0\right) \text {. }
$$
- $\left(X_1, X_2\right) \sim N \Rightarrow k_1 X_1+k_2 X_2 \sim N\left(k_1, k_2\right.$ 是不全为 0 的常数) 

- $$
  \begin{aligned}
  &\left(X_1, X_2\right) \sim N, Y_1=a_1 X_1+a_2 X_2, Y_2=b_1 X_1+b_2 X_2, \text { 且 } \\
  &\qquad \mid \begin{array}\\
  a_1 & a_2 \\
  b_1 & b_2
  \end{array} \mid \neq 0 \Rightarrow\left(Y_1, Y_2\right) \sim N .
  \end{aligned}
  $$

  

-  $\left(X_1, X_2\right) \sim N$, 则 $X_1, X_2$ 相互独立 $\Leftrightarrow X_1, X_2$ 不相关
  以上 5 条可推广至有限个随机变量的情形
-  $(X, Y) \sim N$, 则 $f_{X \mid Y}(x \mid y) \sim N, f_{Y \mid X}(y \mid x) \sim N$ (二维正态分布的条件分布仍是正态分布)

### 条件概率密度

- $\int^{+\infty}_{-\infty}f_{X|Y}(x|y)dx=1,\int^{+\infty}_{-\infty}f_{Y|X}(y|x)dx=1$

## 卷积公式

### 和的分布

- 设 $(X, Y) \sim f(x, y)$, 则 $Z=X+Y$ 的概率密度为

  

- $$
  \begin{aligned}
  f_Z(z) &=\int_{-\infty}^{+\infty} f(x, z-x) \mathrm{d} x=\int_{-\infty}^{+\infty} f(z-y, y) \mathrm{d} y \\
  & \stackrel{\text { 独立 }}{=} \int_{-\infty}^{+\infty} f_X(x) f_Y(z-x) \mathrm{d} x=\int_{-\infty}^{+\infty} f_X(z-y) f_Y(y) \mathrm{d} y .
  \end{aligned}
  $$

### 差的分布

- 设 $(X, Y) \sim f(x, y)$, 则 $Z=X-Y$ 的概率密度为

- $$
  \begin{aligned}
  f_Z(z) &=\int_{-\infty}^{+\infty} f(x, x-z) \mathrm{d} x=\int_{-\infty}^{+\infty} f(y+z, y) \mathrm{d} y \\
  & \stackrel{\text { 独立 }}{=} \int_{-\infty}^{+\infty} f_X(x) f_Y(x-z) \mathrm{d} x=\int_{-\infty}^{+\infty} f_X(y+z) f_Y(y) \mathrm{d} y .
  \end{aligned}
  $$

### 积的分布

- 设 $(X, Y) \sim f(x, y)$, 则 $Z=X Y$ 的概率密度为

- $$
  \begin{aligned}
  f_Z(z) &=\int_{-\infty}^{+\infty} \frac{1}{|x|} f\left(x, \frac{z}{x}\right) \mathrm{d} x=\int_{-\infty}^{+\infty} \frac{1}{|y|} f\left(\frac{z}{y}, y\right) \mathrm{d} y \\
  & \stackrel{\text { 独立 }}{=} \int_{-\infty}^{+\infty} \frac{1}{|x|} f_X(x) f_Y\left(\frac{z}{x}\right) \mathrm{d} x=\int_{-\infty}^{+\infty} \frac{1}{|y|} f_X\left(\frac{z}{y}\right) f_Y(y) \mathrm{d} y .
  \end{aligned}
  $$

### 商的分布

- 设 $(X, Y) \sim f(x, y)$, 则 $Z=\frac{X}{Y}$ 的概率密度为

- $$
  f_z(z)=\int^{+\infty}_{-\infty}|y|f(yz,y)dy \overset{独立}{=}\int^{+\infty}_{-\infty}|y|f_X(yz)f_Y(y)dy
  $$

### 总

- 【注】 $(1)(*)$ 处来自如下公式. 设 $(X, Y) \sim f(x, y)$, 则 $Z=a X+b Y(a b \neq 0)$ 的概率密度为
  $$
  f_Z(z)=\frac{1}{|a|} \int_{-\infty}^{+\infty} f\left(\frac{z-b y}{a}, y\right) \mathrm{d} y=\frac{1}{|b|} \int_{-\infty}^{+\infty} f\left(x, \frac{z-a x}{b}\right) \mathrm{d} x .
  $$
  进一步地, 若 $X, Y$ 相互独立, 且 $X \sim f_X(x), Y \sim f_Y(y)$, 则
  $$
  f_Z(z)=\frac{1}{|a|} \int_{-\infty}^{+\infty} f_X\left(\frac{z-b y}{a}\right) f_Y(y) \mathrm{d} y=\frac{1}{|b|} \int_{-\infty}^{+\infty} f_X(x) f_Y\left(\frac{z-a x}{b}\right) \mathrm{d} x .
  $$
  这些公式依然符合我们所讲的“口诀”:“积谁不换谁,换完求偏导”.
  如 $f_Z(z)=\frac{1}{|a|} \int_{-\infty}^{+\infty} f\left(\frac{z-b y}{a}, y\right) \mathrm{d} y$ 中.
  先用第一句: “积谁不换谁”. 对 $y$ 积分, 则不换 $y$, 写成 $f(\square, y)$, 换 $x=\frac{z-b y}{a}$, 为 $f\left(\frac{z-b y}{a}, y\right)$.
  再用第二句: “换完求偏导”. $\frac{\partial\left(\frac{z-b y}{a}\right)}{\partial z}=\frac{1}{a}$, 因概率密度非负, 要加绝对值, 即为 $\frac{1}{|a|}$. 这样便记 住了公式.

### 最值函数的分布

- $\max \{X, Y\}$ 分布.
  设 $(X, Y) \sim F(x, y)$, 则 $Z=\max \{X, Y\}$ 的分布函数为

$$
F_{\max }(z)=P\{\max \{X, Y\} \leqslant z\}=P\{X \leqslant z, Y \leqslant z\}=F(z, z) .
$$
当 $X$ 与 $Y$ 独立时, $\quad F_{\max }(z)=F_X(z) \cdot F_Y(z)$.

- $\min \{X, Y\}$ 分布.
  设 $(X, Y) \sim F(x, y)$, 则 $Z=\min \{X, Y\}$ 的分布函数为

$$
\begin{aligned}
F_{\min }(z) &=P\{\min \{X, Y\} \leqslant z\}=P\{\{X \leqslant z\} \cup\{Y \leqslant z\}\} \\
&=P\{X \leqslant z\}+P\{Y \leqslant z\}-P\{X \leqslant z, Y \leqslant z\} \\
&=F_X(z)+F_Y(z)-F(z, z) .
\end{aligned}
$$
当 $X$ 与 $Y$ 独立时,
$$
F_{\min }(z)=F_X(z)+F_Y(z)-F_X(z) F_Y(z)=1-\left[1-F_X(z)\right]\left[1-F_Y(z)\right] .
$$
推广到 $n$ 个相互独立的随机变量 $X_1, X_2, \cdots, X_n$ 的情况, 即
$$
\begin{gathered}
F_{\max }(z)=F_{X_1}(z) F_{X_2}(z) \cdots F_{X_n}(z), \\
F_{\min }(z)=1-\left[1-F_{X_1}(z)\right]\left[1-F_{X_2}(z)\right] \cdots\left[1-F_{X_n}(z)\right] .
\end{gathered}
$$
特别地, 当 $X_i(i=1,2, \cdots, n)$ 相互独立且有相同的分布函数 $F(x)$ 与概率密度 $f(x)$ 时,
$$
\begin{gathered}
F_{\max }(z)=[F(z)]^n, f_{\max }(z)=n[F(z)]^{n-1} f(z) . \\
F_{\min }(z)=1-[1-F(z)]^n, f_{\min }(z)=n[1-F(z)]^{n-1} f(z) .
\end{gathered}
$$
这些结果在数理统计部分极为重要.



# 随机变量的数字特征

## 数学期望

- $E(aX+c)=aEX+c$

- $E(X \pm Y)=EX\pm EY$

- 若X是连续型随机变量，$EX=\int^{+\infty}_{-\infty}xf(x)dx$
- $E(g(x))=\int^{+\infty}_{-\infty}g(x)f(x)dx$
- 两个边缘概率密度数学期望为0，本身数学期望也为0

## 方差

- $D(aX+b)=a^2DX$
- $D(X\pm Y)=DY+DX\pm 2Cov(X,Y)$

- $DX=E[(X-EX)^2]=E(X^2)-E(X)^2$



### $\Gamma $函数 

- $$
  \Gamma (\alpha)=\int^{+\infty}_0x^{\alpha-1}e^{-x}dx\overset{x=t^2}{=}2\int^{+\infty}_0t^{2\alpha-1}e^{-t^2}dt
  $$

- $\Gamma (\alpha+1)=\alpha \Gamma(\alpha)$

- $\Gamma(\alpha+1)=\alpha!$

## 协方差

- $Cov(X,Y)=E[(X-EX)(Y-EY)]=E(XY)-E(X)E(Y)$

- $Cov(aX,Y)=aCov(X,Y)$

- $Cov(X,X)=DX$
- $Cov(X_1+X_2,Y)=Cov(X_1,Y)+Cov(X_2,Y)$

### 相关系数

- 独立一定相关系数为0，相关系数为0不一定独立

- $\rho _{xy}=\frac{Cov(X,Y)}{\sqrt{DX}\sqrt{DY}}\quad, \rho=0$(不相关)
- $\rho _{xy}=1\Leftrightarrow P\{Y=aX+b\}=1(a>0)$
- $\rho _{xy}=-1\Leftrightarrow P\{Y=aX+b\}=1(a<0)$
- 二维正态分布和二维二项分布，当$\rho =0$时，X与Y互相独立

### 切比雪夫 

- $P\{|X-EX|\ge \epsilon\}\leq \frac{DX}{\epsilon^2}$
- $P\{|X-EX|< \epsilon\}\ge 1-\frac{DX}{\epsilon^2}$



## 大数定律

### 依概率收敛

设随机变量 $X$ 与随机变量序列 $\left\{X_n\right\}(n=1,2,3, \cdots)$, 如果对任意的 $\varepsilon>0$, 有
$$
\lim _{n \rightarrow \infty} P\left\{\left|X_n-X\right| \geqslant \varepsilon\right\}=0 \text { 或 } \lim _{n \rightarrow \infty} P\left\{\left|X_n-X\right|<\varepsilon\right\}=1,
$$
则称随机变量序列 $\left\{X_n\right\}$ 依概率收敛于随机变量 $X$, 记为
$$
\lim _{n \rightarrow \infty} X_n=X(P) \text { 或 } X_n \stackrel{P}{\longrightarrow} X(n \rightarrow \infty) \text {. }
$$

### 大数定律

- 切比雪夫大数定律
  假设 $\left\{X_n\right\}(n=1,2, \cdots)$ 是①相互独立的随机变量序列, 如果②方差 $D X_i(i \geqslant 1)$ 存在且一致有上界, 即存在常数 $C$, 使 $D X_i \leqslant C$ 对一切 $i \geqslant 1$ 均成立,则 $\left\{X_n\right\}$ 服从大数定律:

$$
\frac{1}{n} \sum_{i=1}^E X_i \stackrel{P}{\longrightarrow} \frac{1}{n} \sum_{i=1}^n E X_i .
$$
- 伯努利大数定律
  假设 $\mu_n$ 是 $n$ 重伯努利试验中事件 $A$ 发生的次数, 在每次试醶中事件 $A$ 发生的概率为 $p(0<p<1)$, 则 $\frac{\mu_n}{n} \stackrel{P}{\longrightarrow} p$, 即对任意 $\varepsilon>0$, 有

$$
\lim _{n \rightarrow \infty} P\left\{\left|\frac{\mu_n}{n}-p\right|<\varepsilon\right\}=1 .
$$
- 辛钦大数定律(常考)
  假设 $\left\{X_n\right\}(n=1,2, \cdots)$ 是①独立②同分布的随机变量序列, 如果③数学期望 $E X_i=\mu(i=1,2, \cdots)$ 存在, 则 $\frac{1}{n} \sum\limits_{i=1}^n X_i \stackrel{P}{\longrightarrow} \mu$, 即对任意 $\varepsilon>0$, 有

$$
\lim _{n \rightarrow \infty} P\left\{\left|\frac{1}{n} \sum_{i=1}^n X_i-\mu\right|<\varepsilon\right\}=1 .
$$
- 考结论
  概率依均值收敛到期望(均值回归)

$$
\frac{1}{n} \sum_{i=1}^n X_i \stackrel{P}{\longrightarrow} E\left(\frac{1}{n} \sum_{i=1}^n X_i\right) .
$$

### 中心极限定理

不论 
$$
X_i \stackrel{ii d}{\sim} F\left(\mu, \sigma^2\right), \mu=E X_i, \sigma^2=D X_i \Rightarrow 
\sum_{i=1}^n X_i \stackrel{n+\infty}{\sim} N\left(n \mu, n \sigma^2\right)\sim N\left(n \mu, n \sigma^2\right) \Rightarrow \frac{\sum\limits_{i=1}^n X_i-n \mu{ }}{\sqrt{n}\sigma}\stackrel{n+\infty}{\sim} N(0,1)
$$
即   
$$
\lim _{n \rightarrow \infty} P\left\{\frac{\sum\limits_{i=1}^n X_i-n \mu}{\sqrt{n} \sigma} \leqslant x\right\}=\Phi(x)
$$









# 数理统计

## 统计量

- 不含未知参数
- 样本k阶原点矩$A_k=\frac{1}{n}\sum\limits^n_{i=1}X_i^k(k=1,2,...)$
- 样本k阶中心矩$A_k=\frac{1}{n}\sum\limits^n_{i=1}(X_i-\overline{X})^k(k=2,3,...)$

## 三大分布

- $\chi^2$分布
  - $X = X_1^2+X_2^2+X_3^2+...+X^2_n$,且$X_i独立同分布于N(0,1)$,则$X  \sim \chi^2(n)$,自由度为n
  - 若$X_1 \sim \chi^2(n_1),X_2\sim \chi^2(n_2);则X_1+X_2\sim \chi^2(n_1+n_2)$
  - 若$X \sim \chi^2(n);E(X)=n,D(X)=2n$
- $t$分布
  - $X\sim N(0,1),Y\sim \chi^2(n);\frac{X}{\sqrt{\frac{Y}{n}}}\sim t(n)$
  - $t\sim t(n),Et=0$
  - $t_{1-a}n=-t_an$
- F分布
  - $X\sim \chi^2(n_1),Y\sim \chi^2(n_2),F=\frac{\frac{X}{n_1}}{\frac{Y}{n_2}}=\frac{X/n_1}{Y/n_2}\sim F(n_1,n_2)$
  - $F\sim F(n_1,n_2);\frac{1}{F} \sim F(n_2,n_1)$
  - $F_{1-\alpha}(n_1,n_2)=\frac{1}{F_\alpha(n_2,n_1)}$

###  正态总体条件下的常用结论

$X_i$独立同分布于$N(\mu,\sigma^2)$

- $\overline{X}\sim N(\mu,\frac{\sigma^2}{n})即$$\frac{\overline{X}-\mu}{\sigma/\sqrt{n}}\sim N(0,1)$
- $\sum\limits_{i=1}^n(\frac{X_i-\mu}{\sigma})^2\sim \chi^2(n)$
- $\frac{n(\overline{X}-\mu)^2}{S^2} \sim F(1, n-1)$
- $\sum\limits_{i=1}^{n}(\frac{X_i-\overline{X}}{\sigma})^2=\frac{(n-1)S^2}{\sigma^2}\sim \chi^2(n-1)$
- $S^2$与$\overline{X}$独立,$\frac{\overline{X}-\mu}{S/\sqrt{n}}\sim t(n-1)$



## ？

- $X\sim N(\mu,\sigma^2)$，$\overline{X}\sim N(\mu,\frac{\sigma^2}{n})$
- $P=(|\overline{X}-\mu|<\Delta)=1-\alpha\quad \alpha$显著性水平(一般取0.025，0.05，0.01),$1-\alpha$,置信度
- 平均值减去期望应该小于一个很小的数$\Delta$

- $P(|\frac{\overline{X}-\mu}{\sigma/\sqrt{n}}|<\frac{\Delta}{\sigma/\sqrt{n}}=1-\alpha)$

- $Z=\frac{\overline{X}-\mu}{\sigma/\sqrt{n}}$,$Z\sim N(0,1)$
- $P(|Z|<\frac{\Delta}{\sigma/\sqrt{n}}=1-\alpha)$

- $\frac{\Delta}{\sigma/\sqrt{n}}=Z_{\frac{\alpha}{2}}$,$\Delta =Z_{\frac{\alpha}{2}}\frac{\sigma}{\sqrt{n}}$



## 矩估计法

- $\overline{X}=EX$

### 最大似然估计

- 写出似然函数

  - 若总体X是连续型随机变量，其概率密度为$f(x;\theta),\theta \in I$,则样本的似然函数为

  - $$
    L(\theta)=L(x_1,x_2,...,x_n;\theta)=\prod^n_{i=1}f(x_i;\theta)
    $$

  - 求函数最大时的$\theta$

### 区间估计

设置信水平为 $1-\alpha$.

- $\sigma^2$ 已知,估

$$
\mu \Rightarrow\overline{X}-\frac{\sigma}{\sqrt{n}} z_{\frac{a}{2}}<\overline{X}<   \overline{X}+\frac{\sigma}{\sqrt{n}} z_{\frac{a}{2}}
$$

-  $\sigma^2$ 末知, 估 

$$
\mu \Rightarrow\overline{X}-\frac{S}{\sqrt{n}} t_{\frac{a}{2}}(n-1)<\overline{X}<   \overline{X}+\frac{S}{\sqrt{n}} t_{\frac{a}{2}}(n-1)
$$

- 单侧置信区间$\frac{a}{2}$改为$a$
