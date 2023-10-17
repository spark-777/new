# 数列



形如$X_{n+2}=\frac{1}{2}(3X_{n+1}-X_n)$的3项数列递推式

把式子拆分为$X_{n+2},X_{n+1}$和$X_{n+1},X_n$

$X_{n+2}-X_{n+1}=\frac{1}{2}(X_{n+1}-X_n)$



单调有界准则



$a^x-1 \sim xlnx$



### 880

第一章 综合题 解答题

T8(2)，T9，T10，T12,T13,T14(2),T15,T16



### 一元函数微分学及其应用



$f(x)=(x^2+3x+2)|x^3-x|$不可导点为

1. 解出$f(x)=0$的根$x_1=-1,x_2=-2,x_3=0,x_3=1$
2. 分类根，$x_1,x_2$为非绝对值部分的根，$x_1,x_3,x_4$为绝对值部分的根
3. 不可导点为绝对值部分的根减去非绝对值部分和绝对值部分的根的并集，即$\{x_1,x_3,x_4\}-\{x_1,x_2\}\cap\{x_1,x_3,x_4\}$





渐近线



高阶导数

曲率

### 880

基础题T5,T11,T18,T19,T20

填空题T1，T2能否洛必达，T3,T6,T9,T13,T16，T18

解答题T1(2)，T8，T9，T10，T14

$2^{|sinx|}$求导时可化为$2^{\sqrt{sin^2x}}$









### 一元积分学

区间再现
$$
\int^b_af(x)dx=\int^b_af(a+b-x)dx
$$

$\int \sqrt{a^2-x^2}dx$

$\int\sqrt{x^2-a^2}dx$

$\int \sqrt {a^2+x^2}dx$

### 向量计算

设$\vec{a}$与$\vec{b}$是非零向量，$|\vec{b}|=2$($\vec{b}$表示$\vec{b}$的模)，$\vec{a}$与$\vec{b}$之间的夹角为$\frac{\pi}{3}$,求
$$
\lim\limits_{x\rightarrow 0}\frac{|\vec{a}+x\vec{b}|-|\vec{a}|}{x}=\lim\limits_{x\rightarrow 0}\frac{(|\vec{a}+x\vec{b}|-|\vec{a}|)(|\vec{a}+x\vec{b}|+|\vec{a}|)}{x(|\vec{a}+x\vec{b}|+|\vec{a}|)}
$$




### 万能公式

### 识别常用的二次曲面

- 单叶双曲面$\frac{x^2}{a^2}+\frac{y^2}{b^2}-\frac{z^2}{c^2}=1$
- 双叶双曲面$\frac{x^2}{a^2}+\frac{y^2}{b^2}-\frac{z^2}{c^2}=-1$
- 椭圆抛物面$\frac{x^2}{a^2}+\frac{y^2}{b^2}=cz$
- 双曲抛物面(马鞍面)$\frac{x^2}{a^2}-\frac{y^2}{b^2}=cz$






### 多元微分学


可微 ： $d_z|_{(0,0)}=dx+dy$

偏导数存在不能推出可微





### 重积分

$$
\int^\pi_{\frac{3}{4}\pi}d\theta \int^{2sin\theta}_0 \frac{1}{\sqrt{1-(\frac{r}{2})^2}}d(\frac{r}{2})=\int^\pi_{\frac{3}{4}\pi}  arcsin(\frac{r}{2})|^{2sin\theta}_0d\theta
$$

由于$arcsin\theta$值域在$[-\frac{\pi}{2},\frac{\pi}{2}]$

故
$$
\int^\pi_{\frac{3}{4}\pi}  arcsin(\frac{r}{2})|^{2sin\theta}_0d\theta\neq 
\int^\pi_{\frac{3}{4}\pi}  arcsin(\frac{2sin\theta}{2})d\theta
$$
$sin\theta = sin(\pi-\theta)$
$$
\int^\pi_{\frac{3}{4}\pi}  arcsin(\frac{r}{2})|^{2sin\theta}_0d\theta =\int^\pi_{\frac{3}{4}\pi}  arcsin(\frac{2sin(\pi -\theta)}{2})d\theta
$$

### 对称性

### 形心公式



### 转动惯量考不考

双纽线





### 微分方程

伯努利方程



### 单连通区域

设D是一区域，若属于D内任一简单闭曲线的内部都属于D，则称D为单连通区域，单连通区域也可以这样描述：D内任一封闭曲线所围成的区域内只含有D中的点。更通俗地说，单连通区域是没有“洞”的区域。

注意**单连通区域上**能找到全微分，那么才能说明积分为0，而如果挖去原点，这个区域就不是单连通的了（定义可以去查）微分形式的积分和路径是否有关，这件事本身就反映了整个空间（比如这里的平面挖去原点）的一些性质，这方面在数学里有深刻的内容。





### my conclusion

- f(x)求导后周期性不变

- 极值点为x=1

- 极值是f(a)=b为极大值

  



### Conclusions to remember

- 曲率

- $$
  k=\frac{|y^{\prime\prime}|}{[1+(y^\prime)^2]^{\frac{3}{2}}}
  $$

- 基本求导公式$(arctanx)^\prime=\frac{1}{x^2+1}$

- $$
  \frac{d^2y}{dx^2}=\frac{d}{dx}(\frac{dy}{dx})
  $$

  

- 周期函数的积分

- $$
  \int^{2a+\phi}_\phi f(x)dx=\int^{2a}_0f(x)dx=\int^{a}_{-a}f(x)dx
  $$

  

- 弧长，质心-形心

- $$
  \int\frac{1}{sinx}dx=\int\frac{1}{2tan\frac{x}{2}cos^2\frac{x}{2}}dx=\int\frac{dtan\frac{x}{2}}{2tan\frac{x}{2}}=\frac{1}{2}lntan\frac{x}{2}+C\\
  or\\
  \int\frac{1}{sinx}dx=\int cscxdx=-\int-\frac{cscxcotx+csc^2x}{cotx+cscx}dx=-\int\frac{d(cotx+cscx)}{cotx+cscx}=-ln(cotx+cscx)+C
  $$

- $$
  \int\frac{1}{\sqrt{1+x^2}}dx
  $$

- $$
  \int\frac{1}{\sqrt{x^2\pm 1}}dx
  $$

- 

- 

- 高斯积分

- $$
  \int^\infty_0e^{-x^2}dx=\frac{\sqrt{\pi}}{2}
  $$

- 弧长，旋转体体积

- 周期函数所有原函数为周期函数$\Leftrightarrow$ $\int^T_0f(x)dx=0$

- 一阶偏导数连续$\Rightarrow$可微

- 可微$\Rightarrow$两个偏导数存在

- 驻点，一阶导数为零

- 

$$
\sum\limits^n_{i=1}k^2=\frac{n(n+1)(2n+1)}{6}
$$

黎曼积分


- 实对称矩阵不同特征向量正交



(1) $\bar{X} \sim N\left(\mu, \frac{\sigma^2}{n}\right)$, 即 
$$
\frac{\bar{X}-\mu}{\frac{\sigma}{\sqrt{n}}}=\frac{\sqrt{n}(\bar{X}-\mu)}{\sigma} \sim N(0,1)
$$

$$
\frac{1}{\sigma^2} \sum_{i=1}^n\left(X_i-\mu\right)^2 \sim \chi^2(n)
$$

$$
\frac{(n-1) S^2}{\sigma^2}=\sum_{i=1}^n\left(\frac{X_i-\bar{X}}{\sigma}\right)^2 \sim \chi^2(n-1)(\mu
$$



(3) $\frac{(n-1) S^2}{\sigma^2}=\sum_{i=1}^n\left(\frac{X_i-\bar{X}}{\sigma}\right)^2 \sim \chi^2(n-1)(\mu$ 末知时, 在 (2) 中用 $\bar{X}$ 替代 $\mu)$;
$$
\frac{\sqrt{n}(\bar{X}-\mu)}{S} \sim t(n-1)
$$


(4) $\bar{X}$ 与 $S^2$ 相互独立, $\frac{\sqrt{n}(\bar{X}-\mu)}{S} \sim t(n-1)$ ( $\sigma$ 末知时, 在 (1) 中用 $S$ 替代 $\left.\sigma\right)$. 进一步有 $\frac{n(\bar{X}-\mu)^2}{S^2} \sim F(1, n-1)$.

泰勒公式


梯度

散度

旋度
狄利克雷

级数求和

球面坐标系
