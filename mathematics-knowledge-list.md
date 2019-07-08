# 基础知识

## 数列基础

常见前$n$项和
- $\sum\limits_{k = 1}^n {k = 1 + 2 +  \cdots  + n} =\frac{n(n+1)}{2}$
- $\sum\limits_{k = 1}^n {\left( {2k - 1} \right) = 1 + 3 +  \cdots  + \left( {2n - 1} \right)} $
- $\sum\limits_{k = 1}^n {{k^2} = 1 + {2^2} +  \cdots  + {n^2}} $
- $\sum\limits_{k = 1}^n {{k^3} = 1 + {2^3} +  \cdots  + {n^3}} $
- $\sum\limits_{k = 1}^n {k\left( {k + 1} \right) = 1 \times 2 + 2 \times 3 +  \cdots  + n \times \left( {n + 1} \right)} $
- $\sum\limits_{k = 1}^n {{1 \over {k\left( {k + 1} \right)}} = {1 \over {1 \times 2}} + {1 \over {2 \times 3}} +  \cdots  + {1 \over {n \times \left( {n + 1} \right)}}} $

## 三角函数相关公式

常用三角函数

- $\sin 2x$
- $\cos 2x$
- $\sin^2 x$
- $\cos^2 x$
- $\tan 2x$
- $\cot 2x$
- $\sin {x \over 2}$
- $\cos {x \over 2}$
- $\tan {x \over 2}$
- $\cot {x \over 2}$

## 经典不等式

经典不等式 *(2020 p111)*

1. $2\left| {ab} \right|$
2. $\left| {a \pm b} \right|$
3. $\left| {\left| a \right| - \left| b \right|} \right|$
4. $\left| {\int {f\left( x \right)dx} } \right|$
5. 平均值不等式大于等于谁？小于等于谁？
6. $\tan x,\sin x,x$的关系，在什么区间上？
7. $x,\sin x$的关系，在什么区间上？
8. $\ln \left( {1 + {1 \over x}} \right)$与其他的大小关系，并证明，在什么区间上？
9. $x,\arcsin x,\arctan x$的关系在，什么区间上？
10. ${e^x}$与$x$的关系
11. $\ln x$与$x$的关系在，什么区间上？

## 其他

已知$A(x_1,y_1),B(x_2,y_2)$，则$\overrightarrow {AB} $的坐标$\left(x_{2}-x_{1}, y_{2}-y_{1}\right)$

# 一元函数微分学

## 函数极限计算公式

- ${1^\infty }$型公式 *(p41)*
- $\mathop {\lim }\limits_{x \to \infty } {\left( {1 + {1 \over x}} \right)^x}$

## 等价无穷小

$x \to 0$时，等价无穷小公式 *(p27)*

- $x - \sin x$
- $\arcsin x - x$
- $\tan x - x$
- $x - \arctan x$

## 级数经典放缩公式

- 当$n \to \infty $时，$\sum\limits_{i = 1}^n {{u_i}} $经典放缩公式 *(p36)*
- 当$n$是有限项时，$\sum\limits_{i = 1}^n {{u_i}} $经典放缩公式 *(p36)*

## ★泰勒公式

- 泰勒通用展开式 *(p89)*

- 常用展开式 *(p41)*
  - $\sin x$
  - $\cos x$
  - $\arcsin x$
  - $\tan x$
  - $\arctan x$
  - $\ln \left( {1 + x} \right)$
  - ${e^x}$
  - ${\left( {1 + x} \right)^\alpha }$

## ★导数公式

- 基本初等函数的导数公式 *(2020 p66)*
  - ${\left( {\arcsin x} \right)^\prime }$
  - ${\left( {\arccos x} \right)^\prime }$
  - ${\left( {\tan x} \right)^\prime }$
  - ${\left( {\cot x} \right)^\prime }$
  - ${\left( {\arctan x} \right)^\prime }$
  - ${\left( {{\mathop{\rm arccot}\nolimits} x} \right)^\prime }$
  - ${\left( {\sec x} \right)^\prime }$
  - ${\left( {\csc x} \right)^\prime }$
  - ${\left[ {\ln \left( {x + \sqrt {{x^2} + 1} } \right)} \right]^\prime }$
  - ${\left[ {\ln \left( {x + \sqrt {{x^2} - 1} } \right)} \right]^\prime }$
  
## ★常见一元函数n阶导数

参见高数18讲2020版P64

  - ${\left( {{e^{ax + b}}} \right)^{(n)}}$
  - ${\left[ {\ln \left( {ax + b} \right)} \right]^{(n)}}$
  - ${\left[ {\sin \left( {ax + b} \right)} \right]^{(n)}}$
  - ${\left[ {\cos \left( {ax + b} \right)} \right]^{(n)}}$
  - ${\left( {{1 \over {ax + b}}} \right)^{(n)}}$

## 可导、连续的关系

一元函数 [答案在这](https://blog.csdn.net/tantiao666/article/details/80949734)

- 可导与连续的关系
- 可微和可导的关系
- 可微与连续的关系
- 可积与连续的关系
- 可积与可导的关系

- 函数可导，其导数一定连续吗（举例说明）？ *(真p42)* 

多元函数

- 函数偏导数连续、函数偏导数存在、函数可微和函数连续的关系

## 周期函数

- 函数$f(x)$是周期函数，那么它的导数必然是周期函数（用定义法证明）
- 函数$f(x)$是周期函数，它的原函数不一定是周期函数 <1000题8.14>

## 反函数

对于$x=x(y)$函数 <1000题8.25>

- $\frac{dy}{dx}={1\over{dx\over dy}}={1\over x'_y}$
- ${d^2y\over dx^2}={d\over dx}({1\over x'_y})={d\over dy}({1\over x'_y})\frac{dy}{dx}={0-x''_y\over x'^2_y} {1\over{dx\over dy}}=-{x''_y\over x'^3_y}$，这个地方极易想当然

## 几何应用

曲率相关

- 曲率公式$k=\frac{\left|y^{\prime \prime}\right|}{\left[1+\left(y^{\prime}\right)^{2}\right]^{\frac{3}{2}}}$

- 曲率半径$R=\frac{1}{k}=\frac{\left[1+\left(y^{\prime}\right)^{2}\right]^{\frac{3}{2}}}{\left|y^{\prime \prime}\right|}\left(y^{\prime \prime} \neq 0\right)$

- 曲率圆
  $$
  \begin{array}{c}{(X-\alpha)^{2}+(Y-\beta)^{2}=R^{2}} \\ 其中\quad{\alpha=x-\frac{y^{\prime}\left[1+\left(y^{\prime}\right)^{2}\right]}{y^{\prime \prime}}, \quad \beta=y+\frac{1+\left(y^{\prime}\right)^{2}}{y^{\prime \prime}}}\end{array}
$$

# 一元函数积分学

## 积分性质

- 积分可拆可加性
- 积分保号性
- $\int_\alpha ^\beta  {f(x)dx} >0$的条件是什么
- 估值定理
- 中值定理
- 周期性：若$f(x)$在$(-\infty,+\infty)$内连续，以$T$为周期
  - $\int_{a}^{a+T} f(x) \mathrm{d} x=\int_{0}^{T} f(x) \mathrm{d} x$（$a$为任意实数）<1000题8.14>
  - $\int_{0}^{x} f(t) \mathrm{d} t$以$T$为周期$\Leftrightarrow \int_{0}^{T} f(x) \mathrm{d} x=0$ <1000题8.14>
  - $\int f(x) \mathrm{d} x$（$f(x)$的全体原函数）周期为$T$$\Leftrightarrow \int_{0}^{T} f(x) \mathrm{d} x=0$

## ★一元不定积分

- $\int {\tan xdx} = \int \frac{\sin x}{\cos x} d x =-\ln |\cos x|+C =\ln |\sec x|+C$

- $\int {\cot xdx}= \int \frac{\cos x}{\sin x} d x=\ln |\sin x|+C=-\ln |\csc x|+C $

- $\int {\sec xdx} $ [What is the integral of sec(x)?](https://socratic.org/questions/what-is-the-integral-of-sec-x)

- $\int {\csc xdx} $ [How do you integrate cscx?](https://socratic.org/questions/how-do-you-integrate-cscx)

- $\int {{{\sec }^2}xdx} $

- $\int {{{\csc }^2}xdx} $

- $\int {\tan x\sec xdx} $ $\sec x + C$

- $\int {\cot x\csc xdx} $

- $\int {{{\sec }^3}xdx} $ [answer](https://socratic.org/questions/what-is-the-integral-of-sec-3-x)

- $\int {\ln xdx} $

- $\int {{1 \over {\sqrt {1 - {x^2}} }}dx} $

- $\int { - {1 \over {\sqrt {1 - {x^2}} }}dx} $

- $\int {{1 \over {\sqrt {1+{x^2}} }}dx}$
$$
\begin{align}
I&=\int \frac{1}{\sqrt{1+\tan ^{2} \theta}} \sec ^{2} \theta d \theta (令x=\tan\theta) \\
&=\int \frac{1}{\sqrt{\sec^2\theta}} \sec ^{2} \theta d \theta\\
&=\int \sec \theta d \theta\\
&=\ln |\sec \theta+\tan \theta|+C \\
&=\ln \left|x+\sqrt{1+x^{2}}\right|+C
\end{align}
$$

- $\int {{1 \over {\sqrt {{x^2} - 1} }}dx} $

- $\int \frac{1}{a^{2} x^{2}+b^{2}} d x=\frac{1}{a b} \int \frac{1}{\left(\frac{a}{b}\right)^{2} x^{2}+1} d\left(\frac{a}{b}\right) x=\frac{1}{a b} \arctan \left(\frac{a}{b} x\right)+C$

- $\int \frac{1}{x^{2}-a^{2}} d x=\int \frac{1}{(x-a)(x+a)} d x=\frac{1}{2 a} \int \frac{1}{x-a}-\frac{1}{x+a} d x=\frac{1}{2 a} \ln \left|\frac{x-a}{x+a}\right|+C$

- $\int \frac{1}{a^{2}-x^{2}} d x=\int \frac{1}{(a-x)(a+x)} d x=\frac{1}{2 a} \int \frac{1}{a-x}+\frac{1}{a+x} d x=\frac{1}{2 a} \ln \left|\frac{a+x}{a-x}\right|+C$

- $\int {{1 \over {\cos x + \sin x}}dx}=-\frac{1}{\sqrt{2}} \ln \left|\csc \left(x+\frac{\pi}{4}\right)+\cot \left(x+\frac{\pi}{4}\right)\right|+C$ <1000题5.39> 
$$
\begin{align}
I &= \int \frac{\frac{1}{\sqrt{2}}}{\sqrt{\frac{1}{2}} \cos x+\frac{1}{\sqrt{2}} \sin x} d x \\
&=\frac{1}{\sqrt{2}} \int \frac{1}{\sin \frac{\pi}{4} \cos x+\cos \frac{\pi}{4} \sin x} d x (和差化积公式)\\
&=\frac{1}{\sqrt{2}} \int \frac{1}{\sin \left(x+\frac{\pi}{4}\right)} d x \\
&=-\frac{1}{\sqrt{2}} \ln \left|\csc \left(x+\frac{\pi}{4}\right)+\cot \left(x+\frac{\pi}{4}\right)\right|+C
\end{align}
$$

- $\int \arctan x d x=x \arctan x-\frac{1}{2} \ln \left(1+x^{2}\right)+C$，思路是分部积分法 <1000题8.9>
  $$
  \begin{array}{l}
  {I=x \arctan x-\int \frac{x}{1+x^{2}} d x} \\ 
  {=x \arctan x-\frac{1}{2} \int \frac{2 x}{1+x^{2}} d x} \\
  {=x \arctan x-\frac{1}{2} \ln \left(1+x^{2}\right)+C}
  \end{array}
  $$

## ★一元定积分 

点火公式

- $\int_0^{{\pi  \over 2}} {{{\sin }^n}xdx} $或者$\int_0^{{\pi  \over 2}} {{{\cos }^n}xdx} $

点火公式升级版

- $\int_0^\pi  {{{\sin }^n}xdx = 2\int_0^{{\raise0.5ex\hbox{$\scriptstyle \pi $}
  \kern-0.1em/\kern-0.15em
  \lower0.25ex\hbox{$\scriptstyle 2$}}} {{{\sin }^n}xdx} } $ <1000题5.36>
- $\int_0^\pi  {{{\cos }^n}xdx} $
  - $n$为奇数时，结果为$0$
  - $n$为偶数时，结果为$2\int_0^{{\raise0.5ex\hbox{$\scriptstyle \pi $}
    \kern-0.1em/\kern-0.15em
    \lower0.25ex\hbox{$\scriptstyle 2$}}} {{{\cos }^n}xdx} $
- $\int_0^{2\pi } {{{\sin }^n}xdx = } \int_0^{2\pi } {{{\cos }^n}xdx} $
  - $n$为奇数时，结果为$0$
  - $n$为偶数时，结果为$4\int_0^{{\raise0.5ex\hbox{$\scriptstyle \pi $}
    \kern-0.1em/\kern-0.15em
    \lower0.25ex\hbox{$\scriptstyle 2$}}} {{{\sin }^n}xdx} $

其他

- $\int_0^a {\sqrt {{a^2} - {x^2}} dx = {1 \over 4}\pi {a^2}} $，考虑单位圆 <1000题5.17>

## 不定积分转变上限积分

- $\int f(x) \mathrm{d} x=\int_{x_{0}}^{x} f(t) \mathrm{d} t+C$ <1000题8.13, 8.14>

## 针对于概率论的积分

- 针对指数分布：$\int_{0}^{+\infty} x^{n} e^{-x} d x=n ! $
- 针对正态分布：$\int_{ - \infty }^{ + \infty } {{e^{ - {x^2}}}dx} = \sqrt{\pi}$

## 反常积分比阶

- $\int_1^{ + \infty } {{1 \over {{x^p}}}dx} $
- $\int_0^1 {{1 \over {{x^p}}}dx} $

# 多元函数微分学

## 全微分

- [如何理解](https://www.zhihu.com/question/272499712)
- 公式$du = {{\partial u} \over {\partial x}}dx + {{\partial u} \over {\partial y}}dy + {{\partial u} \over {\partial z}}dz$

## 隐函数

隐函数存在定理 *(p182)*

## 泰勒公式

$$f\left( {x,y} \right)$$在点$$\left( {{x_0},{y_0}} \right)$$处的二阶展开式公式 <1000题4.11>

# 二重积分

## 直角坐标转极坐标

$\int\!\!\!\int_D {f(x,y)d\sigma  = \int_{\theta_1} ^{\theta_2}  {d\theta \int_{r_1} ^{r_2}  {f(r\cos \theta ,r\sin \theta )rdr} } } $，千万不要忘了是$rdr$ <1000题5.1>

## 物理应用

- 形心公式$\bar x = {{\int\!\!\!\int\limits_D {xd\sigma } } \over {\int\!\!\!\int\limits_D {d\sigma } }}$, $\bar y = {{\int\!\!\!\int\limits_D {yd\sigma } } \over {\int\!\!\!\int\limits_D {d\sigma } }}$
- 质心(重心)公式$\bar x = {{\int\!\!\!\int\limits_D {x\rho \left( {x,y} \right)d\sigma } } \over {\int\!\!\!\int\limits_D {\rho \left( {x,y} \right)d\sigma } }}$,y同理，可以看出其区别在于密度$\rho \left( {x,y} \right)$是否是常数
- 半圆的质心为${4 \over {3\pi }}R$，详见1000题5.5视频35:00左右
- 已知薄片$D$密度为$\mu \left( {x,y} \right)$，其质量$M = \int\!\!\!\int\limits_D {\mu \left( {x,y} \right)d\sigma } $ <1000题5.46>

# 微分方程

- 基本方程求解
  - 变量可分离型 <1000题8.1>
  - 齐次微分方程 <1000题8.5>

    - 拓展1：如果不好直接做试试将函数看做 $x=x(y)$，即令$u = {x\over y}$ <1000题8.6>

    - 拓展2：用换元法化成变量可分离型 <1000题8.8>
  - 一阶线性微分方程$y=\mathrm{e}^{-\int \rho(x) d x}\left[\int e^{\int \rho(x) d x} \cdot q(x) d x+C\right]$  <1000题8.7>
    - 拓展1：如果不好直接做试试将函数看做 $x=x(y)$ <1000题8.11>
  - 伯努利方程$y^{\prime}+p(x) y=q(x) y^{n}(n \neq 0,1)$ <1000题8.16, 8.17>
    1. 恒等变形为$y^{-n} \cdot y^{\prime}+p(x) y^{1-n}=q(x)$
    2. 令$z=y^{1-n}$，得$\frac{\mathrm{d} z}{\mathrm{d} x}=(1-n) y^{-n} \frac{\mathrm{d} y}{\mathrm{d} x}$，则$\frac{1}{1-n} \frac{\mathrm{d} z}{\mathrm{d} x}+p(x) z=q(x)$
  - 二阶可降阶方程
    - $y^{\prime \prime}=f\left(x, y^{\prime}\right)$型：设$y^{\prime}=p(x)$，则$y^{\prime \prime}=p^{\prime}$ <1000题8.32>
    - $y^{\prime \prime}=f\left(y, y^{\prime}\right)$型：设$y^{\prime}=p(x)$，则$y^{\prime \prime}=p\frac{dp}{dy}$ <1000题8.33>
  - **二阶齐次式微分方程通解**，设方程为$y^{\prime \prime}+p y^{\prime}+q y=0$，则特征方程为$\lambda^{2}+p \lambda+q=0$
    - 若$p^{2}-4 q>0$，则设为$y=C_{1} \mathrm{e}^{\lambda_{1}x}+C_{2} \mathrm{e}^{\lambda_{2}x}$
    - 若$p^{2}-4 q=0$，则设为$y=\left(C_{1}+C_{2} x\right) \mathrm{e}^{\lambda x}$
    - 若$p^{2}-4 q<0$，设$\alpha \pm \beta i$是特征方程的复根，则设为$y=e^{a x}\left(C_{1} \cos \beta x+C_{2} \sin \beta x\right)$ <1000题8.38>
  - **二阶非齐次式微分方程特解**
    - 自由项$f(x)=P_{n}(x) e^{a x}$，特解设为$y^{*}=\mathrm{e}^{a x} Q_{n}(x) x^{k}$
      1. $\mathrm{e}^{a x}$照抄
      2. $Q_{n}(x)$为$n$次一般多项式，如二次多项式要设为$Ax^2+Bx+C$
      3. $k$取值分为三种
         - 当$ \alpha \neq \lambda_{1}, \alpha \neq \lambda_{2}$时，$k$取0 <1000题8.18>
         - 当$\alpha=\lambda_{1}$或$\alpha=\lambda_{2}$，$k$取1
         - 当$\alpha=\lambda_{1}=\lambda_{2}$，$k$取2，也就是首先$\lambda_1=\lambda_2$这个条件才有可能成立 <1000题8.19>
    - 自由项$f(x)=\mathrm{e}^{a r}\left[P_{m}(x) \cos \beta x+P_{n}(x) \sin \beta x\right]$，特解设为$y^{*}=e^{e x}\left[Q_{l}^{(1)}(x) \cos \beta x+Q_{l}^{(2)}(x) \sin \beta x\right] x^{k}$
      1. $\mathrm{e}^{a x}$照抄
      2. $l=\max \{m, n\}$，$Q_{l}^{(1)}(x), Q_{l}^{(2)}(x)$分别为两个不同的多项式
      3. $k$取值分为两种，特征根求法为$\lambda=\frac{-b\pm\sqrt{4ac-b^2}}{2a}$
         - 当$\alpha \pm \beta i$不是特征根时，其值为0，如果有实根则直接设为0即可 <1000题8.21>
         - 当$\alpha \pm \beta i$是特征根时，其值为1 <1000题8.20>
  - 二阶非齐次微分方程的通解 = 齐次通解 + 非齐次特解，也就是带$C_1$和$C_2$的解 <1000题8.29>
    还有一种题求非齐次微分方程的特解为带入初始条件求出$C_1$和$C_2$的解 <1000题8.25>
  - 高阶齐次微分方程的解 <1000题8.27>

- 利用线性方程解的理论求解，条件为:

  - 非齐次**线性方程**，只要含$y$的量是一次方程，无需关心$x$，如$y^{\prime \prime}+p(x) y^{\prime}+q(x) y=f(x)$，如$y^{\prime \prime}+p(x) y^{\prime2}+q(x) y=f(x)$则不是线性的了
  - 解相减后线性无关，即$\frac{y_{1}-y_{2}}{y_{2}-y_{3}} \neq k$

  那么齐次通解为$C_1(y_{1}-y_{2})+C_2(y_{2}-y_{3})$，非齐次通解为$C_1(y_{1}-y_{2})+C_2(y_{2}-y_{3})+y_1$

- 通过换元求解 <1000题8.37, 8.38>

- 根据解反求方程 

  - 常系数齐次方程，利用特征方程系数求解 <1000题8.26>
  - 非常系数方程利用通解和微分方程定义消除常数 <1000题8.28>

# 无穷级数

## 幂级数展开式

需要熟稔于心的幂级数展开式，要记住“展开式+收敛域” *(p244)*

- ${e^x}$
- ${1 \over {1 + x}}$
- ${1 \over {1 - x}}$
- $\ln \left( {1 + x} \right)$
- $\sin x$
- $\cos x$

## 常用无穷级数

比较判别法中比较常用的无穷级数 *(参见Notability讲义)*

- $\sum\limits_{n = 1}^\infty  {a{q^{n - 1}}} $
- $\sum\limits_{n = 1}^\infty  {{1 \over {{n^p}}}} $
- $\sum\limits_{n = 1}^\infty  {{{( - 1)}^n}{1 \over {{n^p}}}} $

## 概率论用到的无穷级数

- $\sum\limits_{k = 0}^\infty  {{1 \over {k!}}} =e$

# 空间解析几何


## 面积、体积、表面积公式以及曲线公式

面积、体积、表面积公式 

- 半径为$R$的球的体积$V={4\over3}\pi R^3$
- 半径为$R$的球的表面积$S=4\pi R^2$
- 椭圆${{{x^2}} \over {{a^2}}} + {{{y^2}} \over {{b^2}}} = 1$的面积公式 $S=\pi ab$
- 圆锥体积公式 
- 四面体体积公式 <1000题4.52>

椭圆 *(p307)*

- 椭圆方程
- 椭圆切线 ${{{x_0}x} \over {{a^2}}} + {{{y_0}y} \over {{b^2}}} = 1$

二次曲面 *(p307)*

- 椭球面${{{x^2}} \over {{a^2}}} + {{{y^2}} \over {{b^2}}} + {{{z^2}} \over {{c^2}}} = 1$

- 椭圆柱面${{{x^2}} \over {{a^2}}} + {{{y^2}} \over {{b^2}}} = {z^2}$
- 椭圆抛物面${{{x^2}} \over {{a^2}}} + {{{y^2}} \over {{b^2}}} = z$
- 旋转圆锥面$z = \sqrt {{x^2} + {y^2}} $

## 叉乘

-  几何意义 ![image-20190619110727916](http://res.niuxuewei.com/2019-06-19-030729.png)

- $\mathord{\buildrel{\lower3pt\hbox{$\scriptscriptstyle\rightharpoonup$}}\over 
   a}  \times \mathord{\buildrel{\lower3pt\hbox{$\scriptscriptstyle\rightharpoonup$}}\over 
   a}  = 0$
- $\mathord{\buildrel{\lower3pt\hbox{$\scriptscriptstyle\rightharpoonup$}}\over 
   a}  \times \mathord{\buildrel{\lower3pt\hbox{$\scriptscriptstyle\rightharpoonup$}}\over 
   b}  =  - \mathord{\buildrel{\lower3pt\hbox{$\scriptscriptstyle\rightharpoonup$}}\over 
   b}  \times \mathord{\buildrel{\lower3pt\hbox{$\scriptscriptstyle\rightharpoonup$}}\over 
   a} $  <1000题6.14>

## 平面与直线

平面方程 *(p304)*

- 已知平面法向量${\bf{n}} = \left( {A,B,C} \right)$，过点$\left( {{x_0},{y_0},{z_0}} \right)$，求平面方程
- 已知平面过不公线的三点$A\left( {{x_0},{y_0},{z_0}} \right)$，$B\left( {{x_1},{y_1},{z_1}} \right)$，$C\left( {{x_2},{y_2},{z_2}} \right)$，求平面方程
- 平面过$\left( {a,0,0} \right)$，$\left( {0,b,0} \right)$，$\left( {0,0,c} \right)$，求平面方程 [☢︎]

直线方程 *(p305)*

- 已知两个面，直线方程是什么？前提是什么？
- 已知直线的方向导数为$\tau  = \left( {l,m,n} \right)$，过点$\left( x_0,y_0,z_0 \right)$，求直线方程
- 已知直线的方向导数为$\tau  = \left( {l,m,n} \right)$，过点$\left( x_0,y_0,z_0 \right)$，已知参数$t$，求直线方程 [☢︎]
- 已知直线过两点$A\left( {{x_0},{y_0},{z_0}} \right)$，$B\left( {{x_1},{y_1},{z_1}} \right)$，求直线方程

点到直线（面）的距离

- 已知点$P\left( {{x_0},{y_0},{z_0}} \right)$，到平面$Ax+By+Cz+D=0$的距离为$d = {{\left| {A{x_0} + B{y_0} + C{z_0} + D} \right|} \over {\sqrt {{A^2} + {B^2} + {C^2}} }}$ <1000题6.28>
- [针对二维坐标系]已知点$P\left( {{x_0},{y_0}} \right)$，到直线$Ax+By+C=0$的距离为$d = {{\left| {A{x_0} + B{y_0} + C} \right|} \over {\sqrt {{A^2} + {B^2}} }}$
- [针对三维坐标系]已知点$P\left( {{x_0},{y_0},{z_0}} \right)$，在直线$L_1$中方向向量为$\mathord{\buildrel{\lower3pt\hbox{$\scriptscriptstyle\rightharpoonup$}}\over 
   s} $，其线上任一点$P_0$，$P$点到直线距离为$d = {{\left| {P{P_0} \times \mathord{\buildrel{\lower3pt\hbox{$\scriptscriptstyle\rightharpoonup$}}\over 
   s} } \right|} \over {\left| {\mathord{\buildrel{\lower3pt\hbox{$\scriptscriptstyle\rightharpoonup$}}\over 
   s} } \right|}}$ (原理参见叉乘的几何意义) <1000题6.8, 6.30>

## 空间曲线与曲面

- 空间曲线公式 *(p306)*
  - 一般式
  - 参数方程
- 空间曲面方程 *(p307)*

## 多元函数积分学的几何应用

- 空间曲线(参数方程)$\left\{ {\matrix{{x = \varphi (t)}  \cr {y = \psi (t)}  \cr {z = \omega (t)}  \cr } } \right.$并过$P_0\left(x_0,y_0,z_0 \right)$的切线和法平面 *(p308)*

- 空间曲面在点$P_0\left(x_0, y_0, z_0 \right)$处的法线和切平面 *(p309)*
  - 曲面方程为$F\left( {x,y,z} \right) = 0$ [☢︎]
  - 曲面方程为$z = f\left( {x,y} \right)$
- 空间曲面面积 *(p309)*
- 曲面全微分的几何意义 *(p309)*
- 法向量的方向余弦 *(p309)*

## 三重积分球坐标转化

- 三重积分$\mathop{\int\!\!\!\int\!\!\!\int}\limits_{\kern-5.5pt \Omega } 
   {f\left( {x,y,z} \right)dV} $角坐标系转极坐标 *(p328)*
  - $dx,dy,dz$
  - $x,y,z$

# 曲线、曲面积分

## 第二型曲线积分

- 第二型曲线积分与全微分问题结合 <1000题7.41, 7.45>
  - 观察法找原函数
  - 利用积分与路径无关，通过补一条折线求取
- 积分与路径无关$\Rightarrow$${{\partial Q} \over {\partial x}} = {{\partial Q} \over {\partial y}}$
- ${{\partial Q} \over {\partial x}} = {{\partial Q} \over {\partial y}}$与包含点的区域为单连通$\Rightarrow$积分与路径无关，根据与路径无关再找一个易解曲线解决问题 <1000题7.43>
- 第一型曲线积分与第二型曲线积分是可以相互转化的，其转化公式为$\int\limits_L {P\cos \alpha  + Q\cos \beta ds}  = \int\limits_L {Pdx + Qdy} $，其中$\cos\alpha$与$\cos\beta$为曲线$L$的切向量的方向余弦 <1000题7.47>

## 第二型曲面积分

- 化为二重积分
- 利用**高斯公式** <1000题7.50, 投影也要讲究±号7.53, 高斯公式反向使用7.56>
- 利用**转换公式**，将其投影至$XoY$面 <1000题7.51, 7.52>
  ![image-20190630121625205](http://res.niuxuewei.com/2019-06-30-041625.png)
  - [高数18讲2020版P377]与$z$轴夹角在$0$到$\pi\over2$时取正，其余取负
- 第二型曲面积分转换为第一型曲面积分，利用对称性解决（第二型不谈对称性）<1000题7.54>
- **斯托克斯公式**可以将**空间**第二型**曲线**积分转为第二型**曲面**积分 <1000题7.57>
  - 方向（右手法则）

## 场论

- 方向余弦：设${\mathbf  {v}}=v_{1}{\boldsymbol  {{\hat  {x}}}}+v_{2}{\boldsymbol  {{\hat  {y}}}}+v_{3}{\boldsymbol  {{\hat  {z}}}}\,$为一个三维空间向量，则
$$
\begin{aligned} \alpha &=\cos a=\frac{\mathbf{v} \cdot \hat{\boldsymbol{x}}}{\|\mathbf{v}\|} &=\frac{v_{1}}{\sqrt{v_{1}^{2}+v_{2}^{2}+v_{3}^{2}}} \\ \beta &=\cos b=\frac{\mathbf{v} \cdot \hat{\boldsymbol{y}}}{\|\mathbf{v}\|} &=\frac{v_{2}}{\sqrt{v_{1}^{2}+v_{2}^{2}+v_{3}^{2}}} \\ \gamma &=\cos c=\frac{\mathbf{v} \cdot \hat{\boldsymbol{z}}}{\|\mathbf{v}\|} &=\frac{v_{3}}{\sqrt{v_{1}^{2}+v_{2}^{2}+v_{3}^{2}}} \end{aligned}
$$

- 散度：$div\mathbf{F}={{\partial P} \over {\partial x}}+{{\partial Q} \over {\partial y}}+{{\partial R} \over {\partial z}}$，散度最后求出来是一个数 <1000题7.55>

- 梯度：${\displaystyle \nabla f={\begin{pmatrix}{\frac {\partial f}{\partial x}},{\frac {\partial f}{\partial y}},{\frac {\partial f}{\partial z}}\end{pmatrix}}={\frac {\partial f}{\partial x}}\mathbf {i} +{\frac {\partial f}{\partial y}}\mathbf {j} +{\frac {\partial f}{\partial z}}\mathbf {k} }$，梯度最后求出来是一个向量

  - 几何意义：梯度方向导数最大；相反方向导数最小；垂直方向（有两个）导数值为0 <1000题7.64>

- 旋度：向量场$\mathbf{A}=(A_x, A_y, A_z)$，${\displaystyle \mathbf {rot\,} \mathbf {A} ={\begin{vmatrix}\mathbf {i} &\mathbf {j} &\mathbf {k} \\{\frac {\partial }{\partial x}}&{\frac {\partial }{\partial y}}&{\frac {\partial }{\partial z}}\\A_{x}&A_{y}&A_{z}\end{vmatrix}}}$，同样也是一个向量 <1000题7.60>

- 方向导数：<1000题7.61>
![img](http://res.niuxuewei.com/2019-06-28-002942.png)

# 数学一、数学二专题内容

傅里叶级数

- 傅里叶级数收敛公式：在连续点收敛，在间断点收敛，在端点收敛 *(Notability中的讲义)*

# 行列式

- 余子式、代数余子式 *(p3)*
- 两列式的展开公式 *(p3)*
- 5种特殊矩阵的公式 *(p4)*

# 矩阵

## 秩的性质 

- $r(A+B)$
- $r(AB)$
- $AB = 0$
- $r(A)$与$r({A^T})$的关系
- 若A可相似对角化为$\Lambda$，则$r(A)$与$r(\Lambda)$的关系
- $r(A|B)$
- $r(A^*)$

## 特殊矩阵

- 正交矩阵 *(p78)*

## 伴随矩阵

- 伴随矩阵与原矩阵的关系 *(p38)*

# 概率分布

离散型  *(p32|[期望和方差参见这里](https://wenku.baidu.com/view/e8bfbef9910ef12d2af9e740.html))*

- 0-1分布
- 二项分布，实际意义
- 泊松分布，实际意义，期望和方差
- 几何分布，实际意义

连续型 *(p33)*

- 均匀分布
- 指数分布，期望和方差
- 正态分布，$\mu$的含义，对图像影响
- 标准正态分布

# 数字特征

E(X)的性质

- E(aX+b)
- E(X+Y)
- E(X)E(Y)

D(X)的性质

- D(X)与E(X)的关系
- D(aX+b)
- D(X±Y)

Cov(X,Y)的性质

- 定义
- Cov(X±Y,Z)
- Cov(X,X)

相关系数

- 定义
- 如果呈线性关系则ρ的值

正态分布

- 一维正态分布X如何化为标准正态分布

- 二维正态分布X,Y相互独立的充要条件 *(大全解p304)*
- 独立二维正态分布在相互独立时，$aX+bY$服从什么分布

X,Y独立可以推出什么？

- 相关系数
- Cov
- E
- D
- X，Y的线性关系

# 抽样分布

单正态总体分布 *(p161)*

- $\bar X$

- ${ {\sqrt n \left( {\overline X  - \mu } \right)} \over \sigma }$
- ${{\sqrt n \left( {\bar X - \mu } \right)} \over S}$
- ${n(\bar X-\mu)^2 \over S^2}$
- ${1 \over {{\sigma ^2}}}\sum\limits_{i = 1}^n {{{({X_i} - \bar X)}^2}} $
- ${1 \over {{\sigma ^2}}}\sum\limits_{i = 1}^n {{{({X_i} - \mu )}^2}} $