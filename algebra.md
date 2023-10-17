# 线性代数

## 结论

- 初等互换矩阵的转置和逆矩阵都是本身
- 特征值两两之积的和$\lambda_1 \lambda_2+\lambda_1 \lambda_3+\lambda_2 \lambda_3=A_{11}+A_{22}+A_{33}$

## 行列式

###  行列式的性质

- 行列式中某行（列）元素有公因子k,则k可提到行列式外面

- 是方的

- 行列式中某行（列）元素均是两个元素之和，则可拆成两个行列式之和，即
  $$
  \left[\begin{matrix}  
  a_{11} & a_{12}+a_{13} \\
  a_{21} & a_{22}+a_{23} \\ 
  \end{matrix}\right]=
  \left[\begin{matrix}  
  a_{11} & a_{12} \\
  a_{21} & a_{22} \\ 
  \end{matrix}\right]+\left[\begin{matrix}  
  a_{11} & a_{13} \\
  a_{21} & a_{23} \\ 
  \end{matrix}\right]
  $$
  
  $$
  [a_{11},a_{12}+a_{13}]=[a_{11},a_{12}]+[a_{11},a_{13}]
  $$
  
- 形如$[a_1-3a_2+2a_3,a_2-2a_3,2a_2+a_3]$形式的也可以列变换
  $$
  [a_1-3a_2+2a_3,a_2-2a_3,2a_3,2a_2+a_3]=[a_1-3a_2+2a_3,a_2-2a_3,2a_2+a_3-2(a_2-2a_3)]
  $$
  
- 代数余子式

  - 行列式的值等于行列式的某行(列)元素分别乘其相应的代数余子式后再求和，即

  $$
  |A|=a_{i1}A_{i2}+a_{i2}A_{i2}+...+a_{in}A_{in}=\sum^n_{j=1}a_{ij}A_{ij}(i=1,2,...,n)
  $$

  

  - 行列式的某行（列）元素分别乘另一行（列）元素的代数余子式后再求和，结果为零，即
    $$
    a_{i1}A_{k2}+a_{i2}A_{k2}+...+a_{in}A_{kn}=0,(i\not=k)
    $$

## 矩阵

###  矩阵的基本运算

- 矩阵乘法

$$
\left[\begin{matrix}  
1 & 1&0&0 \\
0 & 1&0&-1 \\ 
\end{matrix}\right]\left[\begin{matrix}  
0  \\
0  \\1\\0\\ 
\end{matrix}\right]=\left[\begin{matrix}  
0 \\
0  \\ 
\end{matrix}\right]\quad (2,4)(4,1)=(2,1)
$$

$$
A\left[\begin{matrix}  
1 &1 \\
0 &0 \\-1&1 
\end{matrix}\right]=\left[\begin{matrix}  
-1 &1\\
0  &0\\
1&1
\end{matrix}\right]\rightarrow  A\left[\begin{matrix}  
1 \\
0  \\-1 
\end{matrix}\right]=\left[\begin{matrix}  
-1 \\
0  \\
1
\end{matrix}\right]
$$



- 基本运算

​       $|kA|=k^n|A|$;$E^2=E$;$A=AE=EA$

- 初等矩阵
  - $E_{12} \quad E$的12行互换，$E_3(-2)\quad E$的第3行×-2,$E_{21}(3)\quad E$的第二行加上3倍的第一行(第一列加上3倍的第二列)
  - $E_{2}^3(k)=E_{2}(k^3)$
  - 初等矩阵的偶数次方等于$E$，奇数次方等于本身
  - 左行右列，一个矩阵左边×初等矩阵，行做初等矩阵的变换，右×，列做初等矩阵的变换

- 转置矩阵

​       将$m\times n$矩阵$A=(a_{ij})_{m\times n}$的行与列互换得到的$n\times m$矩阵，称为矩阵A的转置矩阵, 记为$A^T$，即
$$
\left[\begin{matrix}  
a_{11} & a_{21} \\
a_{12} & a_{22} \\ 
\end{matrix}\right]
$$
​       满足$(AB)^T=B^TA^T$;$(kA)^T=kA^T$;$(A^T)^T=A\quad ;A^T+B^T=(A+B)^T$

### 逆矩阵

- A可逆的充分必要条件是$|A|\not=0$.当$|A|\not=0$时,A可逆

- 基本公式

  - $(kA)^{-1}=\frac{1}{k}A^{-1}$

  - $(A+B)^{-1}\not =A^{-1}+B^{-1}$

  - $A^{-1}=\frac{1}{|A|}A^*$

  - $|A^{-1}|=|A|^{-1}$

  - $(AB)^{-1}=B^{-1}A^{-1}$

- 初等矩阵的逆矩阵

  $E_{12} \quad E$的12行互换，$E_3(-2)\quad E$的第3行×-2,$E_{21}(3)\quad E$的第二行加上3倍的第一行
  $$
  E_{12}^{-1}=\left[\begin{matrix}  
  0 & 1&0 \\
  1 & 0&0 \\
  0&0&1  \\
  \end{matrix}\right]^{-1}=\left[\begin{matrix}  
  0 & 1&0 \\
  1 & 0&0 \\
  0&0&1  \\
  \end{matrix}\right]=E_{12}
  $$

  $$
  E^{-1}_3(-2)=\left[\begin{matrix}  
  1 & 0&0 \\
  0 & 1&0 \\
  0&0&-2  \\
  \end{matrix}\right]^{-1}=\left[\begin{matrix}  
  1 & 0&0 \\
  0 & 1&0 \\
  0&0&-\frac{1}{2}  \\
  \end{matrix}\right]=E_3(-\frac{1}{2})
  $$

  $$
  E_{21}(3)=\left[\begin{matrix}  
  1 & 0&0 \\
  3 & 1&0 \\
  0&0&1  \\
  \end{matrix}\right]^{-1}=\left[\begin{matrix}  
  1 & 0&0 \\
  -3 & 1&0 \\
  0&0&1  \\
  \end{matrix}\right]=E_{21}(-3)
  $$

  





​       

### 伴随矩阵


- 将行列式的$n^2$个元素的代数余子式按如下形式排成的矩阵称为A的伴随矩阵，记作$A^*$

$$
\left[\begin{matrix}  
A_{11} & A_{21} \\
A_{12} & A_{22} \\ 
\end{matrix}\right]
$$

-  $(kA)^*=k^{n-1}A^*;|A^*|=|A|^{n-1};((A)^{*})^{-1}=((A)^{-1})^*$

-  $(A+B)^*\not =A^*+B^*$

- 求伴随矩阵$(A|E)$换成$(E|A^{-1})$

- 二阶矩阵的伴随矩阵

  主对调，副取反。

  具体来说就是主对角线元素（a11和a22）交换位置，副对角线上的元素（a12和a21）取其相反数
  $$
  \left[\begin{matrix}  
  a_{11} & a_{21} \\
  a_{12} & a_{22} \\ 
  \end{matrix}\right]^{*}=\left[\begin{matrix}  
  a_{22} & -a_{21} \\
  -a_{12} & a_{11} \\ 
  \end{matrix}\right]
  $$
  











### 分块矩阵

- A为m阶矩阵，B为n阶

$$
\left[\begin{matrix}  A & O \\O & B \\ \end{matrix}\right]=|A||B|
$$

$$
\left[\begin{matrix}  O	 & A \\B & O \\ \end{matrix}\right]=(-1)^{mn}|A||B|
$$

$$
 \left[\begin{matrix}  A & O \\O & B \\ \end{matrix}\right]^{-1}=\left[\begin{matrix}  A^{-1} & O \\O & B^{-1} \\ \end{matrix}\right]
$$


$$
\left[\begin{matrix}  O	 & A \\B & O \\ \end{matrix}\right]^{-1}=\left[\begin{matrix}  O & B^{-1} \\A^{-1} & O \\ \end{matrix}\right]
$$



### 矩阵方程

 设 $\boldsymbol{A}$ 为 $m \times n$ 矩阵, $\boldsymbol{B}$ 为 $m \times s$ 矩阵, 则矩阵方程 $\boldsymbol{A X}=\boldsymbol{B}$ 有解的充分必要条件为

$$
r(\boldsymbol{A})=r\left(\left[\begin{array}{l:l}
\boldsymbol{A} & \boldsymbol{B}
\end{array}\right]) \right.
$$
将 $\boldsymbol{X}, \boldsymbol{B}$ 按列分块: $\boldsymbol{X}=\left[\boldsymbol{x}_{1}, \boldsymbol{x}_{2}, \cdots, \boldsymbol{x}_{s}\right], \boldsymbol{B}=\left[\boldsymbol{\beta}_{1}, \boldsymbol{\beta}_{2}, \cdots, \boldsymbol{\beta}_{s}\right]$.
$$
\boldsymbol{A X}=\boldsymbol{B} \text { 有解 } \Leftrightarrow \boldsymbol{A}\left[\boldsymbol{x}_{1}, \boldsymbol{x}_{2}, \cdots, \boldsymbol{x}_{s}\right]=\left[\boldsymbol{\beta}_{1}, \boldsymbol{\beta}_{2}, \cdots, \boldsymbol{\beta}_{s}\right] \text { 有解 }
$$
$\Leftrightarrow \boldsymbol{A} \boldsymbol{x}_{i}=\boldsymbol{\beta}_{i}(i=1,2, \cdots, s)$ 有解
$\Leftrightarrow r(\boldsymbol{A})=r\left(\left[\begin{array}{l:l}\boldsymbol{A} & \boldsymbol{\beta}_{i}\end{array}\right]\right)(i=1,2, \cdots, s)$
$\stackrel{\text { (*) }}{\Leftrightarrow} r(\boldsymbol{A})=r\left(\left[\begin{array}{l:l}\boldsymbol{A} & \left.\left.\boldsymbol{\beta}_{1}, \boldsymbol{\beta}_{2}, \cdots, \boldsymbol{\beta}_{s}\right]\right)\end{array}\right.\right.$
$\Leftrightarrow r(\boldsymbol{A})=r\left(\left[\begin{array}{l:l}\boldsymbol{A} & \boldsymbol{B}\end{array}\right]\right) .$
其中, $($ * ) 处的理解: 从左至右是显然的, 从右至左的思路如下:
$$
\left\{\begin{array}{l}
r(\boldsymbol{A})=r\left(\left[\boldsymbol{A}: \boldsymbol{\beta}_{1}, \boldsymbol{\beta}_{2}, \cdots, \boldsymbol{\beta}_{s}\right]\right), \\
r(\boldsymbol{A}) \leqslant r\left(\left[\boldsymbol{A}: \boldsymbol{\beta}_{i}\right]\right) \leqslant r\left(\left[\boldsymbol{A}: \boldsymbol{\beta}_{1}, \boldsymbol{\beta}_{2}, \cdots, \boldsymbol{\beta}_{s}\right]\right)
\end{array} \Rightarrow r(\boldsymbol{A})=r\left(\left[\boldsymbol{A}: \boldsymbol{\beta}_{i}\right]\right)(i=1,2, \cdots, s) .\right.
$$


### 几个重要矩阵

- 对称矩阵

  满足条件$A^T=A$的矩阵A称为对称矩阵,$A^T=A\Leftrightarrow a_{ij}=a_{ji}$

  
  
  
  
  
  
  
  
## 向量组

### 线性相关的判断

- 向量组所含向量的个数大于向量的维数，一定线性相关

### 等价向量组

- 向量组$I,II$等价的充要条件：$r(I)=r(II)=r(I|II)$

- 等价向量组等秩
- 向量组和它的极大线性无关组是等价向量组

### 过渡矩阵

求基$[a_1,a_2,a_3]$到基$[b_1,b_2,b_3]$的过渡矩阵
$$
[b_1,b_2,b_3]=[a_1,a_2,a_3]P
$$

$$
P=[a_1,a_2,a_3]^{-1}[b_1,b_2,b_3]
$$

$$
(A,B)\rightarrow(E,P)
$$

把A初等行变换为E

  

## 矩阵的秩

- 初等变换不改变矩阵的秩，矩阵×可逆矩阵可以看成矩阵做初等变换，秩不变
- $A_{m\times n}B_{n\times s}=O$,$r(A)+r(B)\leq n$ 
- 可逆矩阵满秩
- $0 \leqslant r\left(\boldsymbol{A}_{m \times n}\right) \leqslant \min \{m, n\}$
- $r(k \boldsymbol{A})=r(\boldsymbol{A})(k \neq 0)$
- $r(\boldsymbol{A})=r(\boldsymbol{P A})=r(\boldsymbol{A} Q)=r(\boldsymbol{P A} Q)$
- $r(\boldsymbol{A B}) \leqslant \min \{r(\boldsymbol{A}), r(\boldsymbol{B})\}$
- $ r(\boldsymbol{A}+\boldsymbol{B}) \leqslant r([\boldsymbol{A}, \boldsymbol{B}]) \leqslant r(\boldsymbol{A})+r(\boldsymbol{B}) $
- $r\left(\left[\begin{array}{ll}
  \boldsymbol{A} & \boldsymbol{O} \\
  \boldsymbol{O} & \boldsymbol{B}
  \end{array}\right]\right)=r(\boldsymbol{A})+r(\boldsymbol{B})$
- $r(\boldsymbol{A})+r(\boldsymbol{B}) \leqslant r\left(\left[\begin{array}{ll}
  \boldsymbol{A} & \boldsymbol{O} \\
  \boldsymbol{C} & \boldsymbol{B}
  \end{array}\right]\right) \leqslant r(\boldsymbol{A})+r(\boldsymbol{B})+r(\boldsymbol{C})$
- $r(\boldsymbol{A B}) \geqslant r(\boldsymbol{A})+r(\boldsymbol{B})-n$
- $r(\boldsymbol{A})=r\left(\boldsymbol{A}^{\mathrm{T}}\right)=r\left(\boldsymbol{A} \boldsymbol{A}^{\mathrm{T}}\right)=r\left(\boldsymbol{A}^{\mathrm{T}} \boldsymbol{A}\right)$
- $ r\left(\boldsymbol{A}{ }^{*}\right)= \begin{cases}n, \quad r(\boldsymbol{A})=n \\
  1, \quad r(\boldsymbol{A})=n-1 \\
  0, \quad r(\boldsymbol{A})<n-1\end{cases}$

- 若 $\boldsymbol{A}^{2}=\boldsymbol{A}$, 则 $r(\boldsymbol{A})+r(\boldsymbol{A}-\boldsymbol{E})=n$
-  若 $\boldsymbol{A}^{2}=\boldsymbol{E}$, 则 $r(\boldsymbol{A}+\boldsymbol{E})+r(\boldsymbol{A}-\boldsymbol{E})=n$
-  $\boldsymbol{A x}=\mathbf{0}$ 的基础解系所含向量的个数 $s=n-r(\boldsymbol{A})$
- 若 $\boldsymbol{A} \sim \boldsymbol{\Lambda}$, 则 $n_{i}=n-r\left(\lambda_{i} \boldsymbol{E}-\boldsymbol{A}\right)$, 其中 $\lambda_{i}$ 是 $n_{i}$ 重特征根
- 若 $\boldsymbol{A} \sim \boldsymbol{\Lambda}$, 则 $r(\boldsymbol{A})$ 等于非零特征值的个数, 重根按重数算



## 线性方程组

### 克拉默法则

- （推荐）使用条件

  - $Ax=b,A$为方阵,$|A|\not=0$
  - b与A某列成比例

- 使用方法
  $$
  x_j=\frac{D_j}{D}(D=|A|,D_j为A第j列换为b)
  $$

- 例如
  $$
  \left\{ 
      \begin{array}{lc}
          x_1+x_2-x_3=1  \\
          2x_1+3x_2+x_3=2 \\
          4x_1+9x_2-x_3=4\\
      \end{array}
  \right.
  $$

  $$
  x_2=\frac{D_2}{D}=\frac{\left[\begin{matrix}  
  1 & 1&-1 \\
  2 & 3&1 \\
  4&9&-1  \\
  \end{matrix}\right]}{\left[\begin{matrix}  
  1 & 1&-1 \\
  2 & 2&1 \\
  4&4&-1  \\
  \end{matrix}\right]}
  $$


### 方程组有解的条件

- $Ax=0$,总有解，至少有零解

- $A_{m\times n}x=0$
  $$
  \left\{ 
      \begin{array}{lc}
          r(A)=n&只有零解  \\
          r(A)<n&无穷多解 \\
      \end{array}
  \right.
  $$
  
- $A_{m\times n}x=b$

$$
\left\{ 
    \begin{array}{lc}
         r(A,b)\not=r(A)&无解\\
        r(A,b)=r(A)=n&唯一解  \\
        r(A,b)=r(A)=r<n&无穷多解 \\
    \end{array}
\right.
$$

### 解的结构

- 齐次解+特解 = 非齐解
- $AB=0\Rightarrow B$的列都是$Ax=0$的解



## 特征值与特征向量

### 基本概念

- $(\lambda E-A)\xi=0$
- $\xi\not=0$

###  特征值的性质

- $\prod\limits_{i=1}^n\lambda_i=|A|$
- $\sum\limits_{i=1}^n\lambda_i=\sum\limits_{i=1}^na_{ii}=tr(A)(矩阵的迹)$
- 若矩阵r=1，其中一个特征值为主对角元素之和，其余的为0
- 特征值两两之积的和$\lambda_1 \lambda_2+\lambda_1 \lambda_3+\lambda_2 \lambda_3=A_{11}+A_{22}+A_{33}$
- 矩阵A的非0特征值对应的$A^*$特征值就一定是0,0特征值对应的$A^*$特征值不是0

### A以及与A有关的常用矩阵的特征值和特征向量


$$
\begin{matrix}
\hline
矩阵 & A&kA  &A^k &f(A)&   A^{-1}&    A^*    &P^{-1}AP&A^T&A-aE\\
\hline
特征值 & \lambda&k\lambda    &\lambda^k&f(\lambda)&\frac{1}{\lambda} &\frac{|A|}{\lambda}&\lambda&\lambda&\lambda-a\\
\hline
对应的特征向量&\xi&\xi&\xi&\xi&\xi&\xi&P^{-1}\xi&需计算  \\
\hline
\lambda=0 时不能使用
\end{matrix}
$$



$$
f(x)为多项式，若矩阵A满足f(A)=0,\lambda 是A的任一特征值，则入满足f(\lambda)=0
$$



### 特征向量

- $AP=PB  \rightarrow A,B$特征值相等

- 若A为实对称矩阵

  - 当$\lambda_1 \not=\lambda_2 \Rightarrow \xi_1 \perp\xi_2$

  - 当$\lambda_1 =\lambda_2 \Rightarrow \xi_1 \perp\xi_2 \quad or\quad  \xi_1 ,\xi_2$线性无关

- $A(\beta_1,\beta_2,\beta_3)=-2(\beta_1,\beta_2,\beta_3)\rightarrow A\beta_i=-2\beta_i\rightarrow \lambda=-2,\xi=(\beta_1,\beta_2,\beta_3)$的极大无关组

- k重特征值入至多只有k个线性无关的特征向量

- 若$\xi_1,\xi_2$是A的属于不同特征值$\lambda_1,\lambda_2$的特征向量，则$\xi_1,\xi_2$线性无关

- 对于不同的特征值，其对应的特征向量之和，如$\xi_1+\xi_2$等不再是A的特征向量(接上条)

- 若$\xi_1,\xi_2$是A的属于同一特征值$\lambda$的特征向量，则$k_1\xi_1+k_2\xi_2$仍是A的属于特征值$\lambda$的特征向量（常考其中一个系数（如k2）等于0的情形）

- 若3阶矩阵A的每行元素和为3

  - $$
    A {\left(\begin{matrix}  
    1  \\
    1  \\
    1 \\
    \end{matrix}\right)}={\left(\begin{matrix}  
    3  \\
    3  \\
    3 \\
    \end{matrix}\right)}=3{\left(\begin{matrix}  
    1  \\
    1  \\
    1 \\
    \end{matrix}\right)}
    $$

  - 有一个特征值$\lambda =3$,特征向量为$[1,1,1]^T$





### 矩阵的相似对角化

- $P^{-1}AP=\Lambda$

- 对角矩阵P可以是由特征向量组成
- P由特征向量组成

- 实对称必可相似对角化

- n阶矩阵A相似于对角矩阵$\leftrightarrow$A有n个线性无关的特征向量（每个k重特征值都有k个线性无关的特征向量）
- n阶矩阵A有n个不同的特征值$\rightarrow$A相似与对角矩阵
- A为实对称矩阵$\rightarrow$A相似于对角矩阵
- 线性无关的特征向量的个数=n-r

## 二次型

### 定义

- $f(x)=x^TAx$
- 实对称矩阵A为二次型$f(x)$的矩阵

- 二次型中矩阵转为对称矩阵$b_{ij}=\frac{a_{ij}+a_{ji}}{2}$
- 二次型$f(x)$的秩为A的秩
- 二次型标准型 $\lambda_1 y_1^2+\lambda_2 y_2^2+\lambda_3 y_3^2 \quad \lambda$为特征值



### 实对称矩阵合同的判断

- 实对称矩阵必可以合同

- 定义法：$A,B$合同$\Leftrightarrow$存在可逆矩阵$C,C^T AC=B$
- $A,B$合同$\Leftrightarrow$正负惯性指数相同
- 传递性，A合同于C，C合同于B，A合同于B
- $A,B$相似$\Leftrightarrow$存在可逆矩阵$C,C^{-1} AC=B$
- 同阶实对称矩阵A，B相似必合同
- 若A，B相似，满足以下4条
  - $r(A)=r(B)$
  - $|A|=|B|$
  - $tr(A)=tr(B)$
  - A,B特征值相同
- 已知A，B，$C^TAC=B$,求C
  - 设$C=E_1E_2...E_n$
  - $C^TAC=(E_1E_2...E_n)^TA(E_1E_2...E_n)=B$
  - $E_n...E_2E_1AE_1E_2..E_n=B$
  - $[A|E] \rightarrow [B|C^T]$（初等行变换，行变换一次要对A矩阵做对应的列变换）
  - $[\frac{A}{E}]\rightarrow [\frac{B}{C}]$（初等列变换，列变换一次就要对A做对应的行变换）






### 合同变换，二次型的合同标准形、规范形

- A，B为n阶**实对称**矩阵，$C^T AC=B$,则A，B合同

- 合同矩阵的**秩**相同

- 规范性的系数为$(-1,1,0)$,当特征值为0时为0，大于0时为1，小于0时为-1

- 若二次型的秩为r，则r=p+q,p(为正项特征值个数)称为正惯性指数q称为负惯性指数

- 两个二次型（或实对称矩阵）合同的充要条件是有相同的正、负惯性指数，或有相同的秩

- 配方法

  - $x_1^2-x_2^2+2 a x_1 x_3+4 x_2 x_3=(x_1+a x_3)^2-(x_2-2 x_3)^2+(4-a^2)x^3$负惯性指数为1
$$
x^2_1+2 x_2^2+4 x_3^2-2 x_1 x_2+4 x_1 x_3+6 x_2 x_3=x_1^2-2 x_1(x_2-2x_3)^2+(x_2-2x_3)^2+x_2^2+10x_2x_3
$$

$$
=[x_1-(x_2-2x_3)]^2+(x_2^2+10x_2x_3+25x_3^2)-25x_3^2
$$

$$
=(x_1-x_2+2x_3)^2+(x_2+5x_3)^2-25x_3^2 (惯性指数为1，1，-1)
$$

### 用配方法将二次型化为规范性

化二次型$f(x_1,x_2,x_3)=x_1^2+2 x_1 x_2+2 x_1 x_3-x_2^2-2 x_2 x_3-x_3^2$为标准型，并写出所作的可逆线性变换
$$
f(x_1,x_2,x_3)=(x_1+x_2+x_3)^2-2(x_2+x_3)^2
$$

$$
\left\{ 
    \begin{array}{lc}
        y_1=x_1+x_2+x_3  \\
        y_2=x_2+x_3 \\
        y_3=x_3
    \end{array}
\right.即\left\{ 
    \begin{array}{lc}
        x_1=y_1-y_2  \\
        x_2=y_2-y_3 \\
        x_3=y_3
    \end{array}
\right.
$$



把二次型化为标准型$f(x_1,x_2,x_3) \overset{\text{x=Cy}}{=\!=\!=}y_1^2-2y^2_2$
$$
C=\left[\begin{matrix}  
1 & -1&0 \\
0 & 1&-1 \\
0&0&1  \\
\end{matrix}\right]
$$
C为**变换矩阵**，因$|C|=1\not =0$,故所作变换为可逆线性变换

### 用正交变换将二次型化为规范性

利用正交变换$x=Qy$,把二次型$f(x_1,x_2,x_3)=x_1^2+x_2^2+2x_3^2+2x_1x_2$化为标准形

二次型矩阵为A
$$
A=\left[\begin{matrix}  
1 & 1&0 \\
1 & 1&0 \\
0&0&2  \\
\end{matrix}\right]
$$


特征值为0，2，2，特征向量为$[1,-1,0]^T,[1,1,0]^T,[0,0,1]^T$

由于特征向量已两两正交，只需单位化
$$
\eta_1=[\frac{\sqrt{2}}{2},-\frac{\sqrt{2}}{2},0]^T,\eta_2=[\frac{\sqrt{2}}{2},\frac{\sqrt{2}}{2},0]^T,\eta_3=[0,0,1]^T
$$

$$
Q=\left[\begin{matrix}  
\frac{\sqrt{2}}{2}&\frac{\sqrt{2}}{2}&0 \\
-\frac{\sqrt{2}}{2}&\frac{\sqrt{2}}{2}&0  \\
0&0&1  \\
\end{matrix}\right]
$$

标准型为$f=2y_2^2+2y_3^2$，系数为特征值

### 正定二次型及其判别

- $n$ 元二次型 $f=\boldsymbol{x}^{\mathrm{T}} \boldsymbol{A} \boldsymbol{x}$ 正定 (充要条件)
  - $\Leftrightarrow$ 对任意 $\boldsymbol{x} \neq \boldsymbol{0}$, 有 $\boldsymbol{x}^{\mathrm{T}} \boldsymbol{A} \boldsymbol{x}>0$ (定义)
  - $\Leftrightarrow f$ 的正惯性指数 $p=n$
  - $\Leftrightarrow$ 存在可逆矩阵 $\boldsymbol{D}$, 使 $\boldsymbol{A}=\boldsymbol{D}^{\mathrm{T}} \boldsymbol{D}$
  - $\Leftrightarrow \boldsymbol{A} \simeq \boldsymbol{E}$
  - $\Leftrightarrow \boldsymbol{A}$ 的特征值 $\lambda_i>0(i=1,2, \cdots, n)$
  - $\Leftrightarrow \boldsymbol{A}$ 的全部顺序主子式均大于 0 

- 必要条件
  - $a_{ij}>0$
  - |A|>0

## 相似理论

### A的相似对角化$(A \sim \Lambda)$

- 充要条件
  - $A$有n个线性无关的特征向量$\Leftrightarrow A\sim\Lambda$
  - $n_i=n-r(\lambda_iE-A)\Leftrightarrow A\sim \Lambda(n_i$为$\lambda_i$重根数）
- 充分条件
  - A为实对称矩阵
  - A有n个互异的特征值
  - $A^2=A$
  - $A^2=E$
  - $r(A)=1 \quad and \quad tr(A)\not=0 $
- 必要条件
  - $A\sim\Lambda\Rightarrow r(A)=$非零特征值的个数（重根按重数算）
- 否定条件
  - $A\not=O,A^k=O (k为大于1的整数)\Rightarrow A$不可相似对角化
  - A的特征值全为k但$A\not=kE\Rightarrow A$不可相似对角化

### 矩阵的相似

- A,B为n阶方阵

- $P^{-1}AP=B$（P可以是由特征向量组成）
- 性质,若AB相似
  - $|A|=|B|$
  - $r(A)=r(B)$
  - $tr(A)=tr(B)$
  - $| \lambda E-A|=|\lambda E-B|$
  - A，B具有相同的特征值
  - $A^T,B^T$相似
  - $A^*,B^*$相似（A可逆）
  - $A^{-1},B^{-1}$相似（A可逆）
- $A\sim \Lambda,B\sim \Lambda\Rightarrow A\sim B$

### 实对称矩阵与正交矩阵

- 若A为实对称矩阵
  - n阶实对称矩阵A有n个特征值的话（含重根），若r(A)<n，则有n-r(A)个零特征值
  - 特征值均为实数，特征向量均为实向量
  - 当$\lambda_1 \not=\lambda_2 \Rightarrow \xi_1 \perp\xi_2$
  - 当$\lambda_1 =\lambda_2 \Rightarrow \xi_1 \perp\xi_2 \quad or\quad  \xi_1 ,\xi_2$线性无关
  - 必可用正交矩阵相似对角化（即存在正交矩阵P,使$P^{-1}AP=P^TAP=\Lambda$）
- 若A为正交矩阵
  - $A^TA=E\Leftrightarrow A^{-1}=A^T$
  - $\Leftrightarrow A$由规范正交基组成
  - $\Leftrightarrow A^{-1}$是正交矩阵
  - $\Leftrightarrow A^*$是正交矩阵
  - $\Leftrightarrow -A$是正交矩阵

- 若A，B为同阶正交矩阵，则AB为正交矩阵（A+B不一定）
