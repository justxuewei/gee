# 高等数学基础知识

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

和差公式

- $\sin (\alpha \pm \beta)=\sin \alpha \cos \beta \pm \cos \alpha \sin \beta$ <1000题9.20>
- $\cos(\alpha \pm \beta)=\cos \alpha \cos \beta \mp \sin \alpha \sin \beta$ <1000题9.67>

## 经典不等式

经典不等式 *(2020 p111)*

1. $|ab| \leq \frac{a^2+b^2}{2}$，也可写做$2|ab|\leq a^2+b^2$ <1000题9.3>
2. $\left| {a \pm b} \right|$
3. $\left| {\left| a \right| - \left| b \right|} \right|$
4. $\left| {\int {f\left( x \right)dx} } \right|$
5. 平均值不等式大于等于谁？小于等于谁？
6. $\sin x \lt x$，在$x>0$区间上
7. $x\lt\tan x$，在$0<x<\frac{\pi}{2}$区间上
8. $\ln \left( {1 + {1 \over x}} \right)$与其他的大小关系，并证明，在什么区间上？
9. $x,\arcsin x,\arctan x$的关系在，什么区间上？
10. 对于任意的$x$有$e^x\geq x+1$
11. 对于$x>0$有$\ln x<x-1$

## 方程求根问题

- 高阶方程求根：试根法+除法 <1000题8.37>

## 因式分解公式

- $a^{3}+b^{3}=(a+b)\left(a^{2}-a b+b^{2}\right)$ <1000题9.41, 线代3, 线代19>
- $a^{3}-b^{3}=(a-b)\left(a^{2}+a b+b^{2}\right)$  <1000题 线代19>
- n是<u>正偶数</u>时，$a^{n}-b^{n}=(a+b)\left(a^{n-1}-a^{n-2} b+\dots+a b^{n-2}-b^{n-1}\right) $ <1000题 线代32>
- n是<u>正奇数</u>时，$a^{n}+b^{n}=(a+b)\left(a^{n-1}-a^{n-2} b+\cdots-a b^{n-2}+b^{n-1}\right)$
- $(a+b)^{n}=\sum\limits_{k=0}^{n} C_{n}^{k} a^{n-k} b^{k}$

## 奇偶性

- 奇函数x偶函数=奇函数

## 双阶乘

- $(2n-1)!! = 1\times3\times5\times\cdots\times(2n-1)$
- $(2n)!! = 2\times4\times6\times\cdots\times2n$

# 极限与连续

## 极限性质

$\lim _{n \rightarrow \infty} a_n = C$极限存在，则具有的性质有：

- 唯一性
- 有界性
- 保号性
- 脱帽法，$a_n=C+\alpha$，其中$\alpha\rightarrow0$

## 等价无穷小

$x \to 0$时，等价无穷小公式有：

- $x - \sin x$
- $\arcsin x - x$
- $\tan x - x$
- $x - \arctan x$ 
- $(1+x)^\alpha-1\sim\alpha x$ <1000题9.4(3)>
  - 拓展：$(1+x)^{\alpha(x)}-1\sim\alpha(x) x$，其中$\alpha(x)\rightarrow0$ <1000题1.31>

## 基本极限公式

- $\lim\limits_{x\rightarrow0^+} x^x=1$
- $\lim\limits_{x\rightarrow+\infty} x^{1\over x}=1$
- $\lim\limits_{x\rightarrow0^+} x\ln x=0$，意义在于$x$趋近于0的速度远大于$\ln x$趋近于负无穷的速度
  - 拓展：$\lim\limits_{x\rightarrow0^+} x^\alpha\ln x=0$，其中$\alpha>0$
- $\lim\limits _{x \rightarrow \infty} \sqrt[n]{a}=1$（其中$a$为任意常数）
- $\lim\limits _{x \rightarrow \infty} \sqrt[n]{n}=1$
- $\lim\limits_{n\rightarrow\infty} (1+\frac{1}{n})^n=e$ <1000题9.8>
  - 拓展：$\lim\limits_{n\rightarrow\infty} (1+\frac{x}{n})^n=e^x$，对其证明[在这](https://math.stackexchange.com/questions/882741/limit-of-1-x-nn-when-n-tends-to-infinity)

- ${1^\infty }$型公式 $\lim u^v=e^{\lim (u-1)v}$

## 数列极限

解题技巧

- 递推式是单调的，使用单调有界准则
- 递推式不是单调的，使用先斩后奏 <1000题1.77, 9.54>
  1. 求极限并舍去不符合要求的点
  2. $|x_{n+1}-A|=|f(x_n)-g(A)|$经过计算可以获得一个递推式$|x_{n+1}-A|<k|x_n-A|<\cdots<k^n|x_1-A|$，其中$0<k<1$
  3. 当$n\rightarrow\infty$时，$0 \leq |x_{n}-A|< 0$，所以我们有理由相信$x_n$的极限为$A$

# 一元函数微分学

## 性质

奇偶性

- 奇函数求导变偶函数，偶函数求导变奇函数

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
- 函数$f(x)$是周期函数，它的原函数不一定是周期函数 [参见`一元函数积分学 > 积分性质 > 周期性 `] <1000题8.14>

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
- 周期性：若$f(x)$在$(-\infty,+\infty)$内连续，以$T$为周期 <1000题3.2>
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

- $\int \frac{1}{a^{2} x^{2}+b^{2}} d x=\frac{1}{a b} \int \frac{1}{\left(\frac{a}{b}\right)^{2} x^{2}+1} d\left(\frac{a}{b}\right) x=\frac{1}{a b} \arctan \left(\frac{a}{b} x\right)+C$ <1000题9.41>

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

## 变上限积分

- 不定积分转变上限积分：$\int f(x) \mathrm{d} x=\int_{x_{0}}^{x} f(t) \mathrm{d} t+C$ <1000题8.13, 8.14>
- 变上限积分的等价代换：$\int_{0}^{f(x)} g(t) \mathrm{d} t$在$f(x)\rightarrow 0$时，可以将$f(x)$和$g(t)$同时做等价代换 <1000题9.1>
- **以0为下限的变上限积分**，奇偶性与被积函数相反，如$f(t)$为奇函数，则$\int_0^xf(t)dt$为偶函数 <1000题9.41>

## 针对于概率论的积分

- 针对指数分布：$\int_{0}^{+\infty} x^{n} e^{-x} d x=n ! $
- 针对正态分布：$\int_{ - \infty }^{ + \infty } {{e^{ - {x^2}}}dx} = \sqrt{\pi}$

## 反常积分比阶

- $\int_1^{ + \infty } {{1 \over {{x^p}}}dx} $
- $\int_0^1 {{1 \over {{x^p}}}dx} $

## 解题技巧

- 分部积分法
- 换元
- 凑微分法
- 有理函数积分法 <1000题9.41>

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

# 三重积分

## 对称性

- 普通对称性
- 轮转对称性

## 三重积分球坐标转化

三重积分$\mathop{\int\!\!\!\int\!\!\!\int}\limits_{\kern-5.5pt \Omega } 
{f\left( {x,y,z} \right)dV} $角坐标系转球坐标

- $dx,dy,dz$
- $x,y,z$

# 曲线、曲面积分

## 第二型曲线积分

- 积分与路径无关$\Rightarrow$${{\partial Q} \over {\partial x}} = {{\partial Q} \over {\partial y}}$
- ${{\partial Q} \over {\partial x}} = {{\partial Q} \over {\partial y}}$与包含点的区域为单连通$\Rightarrow$积分与路径无关，根据与路径无关再找一个易解曲线解决问题 <1000题7.43>
- 第一型曲线积分与第二型曲线积分是可以相互转化的，其转化公式为$\int\limits_L {P\cos \alpha  + Q\cos \beta ds}  = \int\limits_L {Pdx + Qdy} $，其中$\cos\alpha$与$\cos\beta$为曲线$L$的切向量的方向余弦 <1000题7.47>

## 第二型曲面积分

- 化为二重积分
- 利用**高斯公式** <1000题7.50, 投影也要讲究±号7.53, 高斯公式反向使用7.56>
- 利用**转换公式**，以投影至$XoY$面为例，其转换公式为$\iint_{\Sigma} Pd y d z+Qd z d x+Rd x d y=\iint_{\Sigma} [P(-z^{\prime}_x) +Q(-z^{\prime}_y) +R]d x d y$ <1000题7.51, 7.52>
  - 需要注意正负号，与$z$轴夹角在$0$到$\pi\over2$时取正，其余取负[高数18讲2020版P377]
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

# 微分方程

## 基本方程求解

- 变量可分离型 <1000题8.1>

- 齐次微分方程 <1000题8.5>
  - 拓展1：如果不好直接做试试将函数看做 $x=x(y)$，即令$u = {x\over y}$ <1000题8.6>

  - 拓展2：用换元法化成变量可分离型 <1000题8.8>

- 一阶线性微分方程：最终解得形式为$y=\mathrm{e}^{-\int p(x) d x}\left[\int e^{\int p(x) d x} \cdot q(x) d x+C\right]$  <1000题8.7>
  - 拓展1：如果不好直接做试试将函数看做 $x=x(y)$ <1000题8.11>
  - 注：若这里的$\int p(x) d x=\ln|\varphi(x)|$，那么可以不加绝对值变为$\ln\varphi(x)$

- 伯努利方程：$y^{\prime}+p(x) y=q(x) y^{n}(n \neq 0,1)$ ，其结题步骤为：<1000题8.16, 8.17>
  1. 恒等变形为$y^{-n} \cdot y^{\prime}+p(x) y^{1-n}=q(x)$
  2. 令$z=y^{1-n}$，得$\frac{\mathrm{d} z}{\mathrm{d} x}=(1-n) y^{-n} \frac{\mathrm{d} y}{\mathrm{d} x}$，则$\frac{1}{1-n} \frac{\mathrm{d} z}{\mathrm{d} x}+p(x) z=q(x)$

- 二阶可降阶方程，其类型有：
  - $y^{\prime \prime}=f\left(x, y^{\prime}\right)$型：设$y^{\prime}=p(x)$，则$y^{\prime \prime}=p^{\prime}$ <1000题8.32>
  - $y^{\prime \prime}=f\left(y, y^{\prime}\right)$型：设$y^{\prime}=p(x)$，则$y^{\prime \prime}=p\frac{dp}{dy}$ <1000题8.33>

- 二阶齐次式微分方程通解：设方程为$y^{\prime \prime}+p y^{\prime}+q y=0$，则特征方程为$\lambda^{2}+p \lambda+q=0$
  - 若$p^{2}-4 q>0$，则设为$y=C_{1} \mathrm{e}^{\lambda_{1}x}+C_{2} \mathrm{e}^{\lambda_{2}x}$
  - 若$p^{2}-4 q=0$，则设为$y=\left(C_{1}+C_{2} x\right) \mathrm{e}^{\lambda x}$
  - 若$p^{2}-4 q<0$，设$\alpha \pm \beta i$是特征方程的复根，则设为$y=e^{a x}\left(C_{1} \cos \beta x+C_{2} \sin \beta x\right)$ <1000题8.38>

- 二阶非齐次式微分方程特解
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

- 二阶非齐次微分方程的解 
  - 二阶非齐次微分方程的**通解** = 齐次通解 + 非齐次特解，也就是带$C_1$和$C_2$的解 <1000题8.29>
  - 还有一种题求非齐次微分方程的**特解**为带入初始条件求出$C_1$和$C_2$的解 <1000题8.25>

- 高阶齐次微分方程的解 
  - 类比二阶齐次方程 <1000题8.27, 8.37>

## 利用线性方程解的理论求解

条件为:

- 非齐次**线性方程**，只要含$y$的量是一次方程，无需关心$x$，如$y^{\prime \prime}+p(x) y^{\prime}+q(x) y=f(x)$，如$y^{\prime \prime}+p(x) y^{\prime2}+q(x) y=f(x)$则不是线性的了
- 解相减后线性无关，即$\frac{y_{1}-y_{2}}{y_{2}-y_{3}} \neq k$

那么齐次通解为$C_1(y_{1}-y_{2})+C_2(y_{2}-y_{3})$，非齐次通解为$C_1(y_{1}-y_{2})+C_2(y_{2}-y_{3})+y_1$

## 通过换元求解 

换元基本上是题目告知了如何换 <1000题8.37, 8.38>

## 根据解反求方程 

- 常系数齐次方程，利用特征方程系数求解 <1000题8.26>
- 非常系数方程利用通解和微分方程定义消除常数 <1000题8.28>

## 全微分问题

一般格式为$Pdx+Qdy=0$，其步骤为: <1000题7.41, 7.45, 8.35>

1. 验证是否是全微分方程，方法有：
   - 当$P$和$Q$给定具体的式子时，使用$\frac{\partial P}{\partial y}=\frac{\partial Q}{\partial x}$ <1000题8.35>
   - 当$P$和$Q$是抽象的时，可以考虑使用第二型曲线积分的积分与路径无关 <1000题7.41>
2. 求解找出原函数
   - 观察法 [不推荐]
   - 折线法$u(x, y)=\int_{(0,0)}^{(x, y)} P(x, y) \mathrm{d} x+Q(x, y) \mathrm{d} y=\int_{0}^{x} P(x, 0) \mathrm{d} x+\int_{0}^{y} Q(x, y) \mathrm{d} y$

## 欧拉方程

形如$x^{2} \frac{d^{2} y}{d x^{2}}+p x \frac{d y}{d x}+q y=f(x)$，其中$p$和$q$为常数 <1000题8.36, 8.37>

- $x>0$时，令$x=\mathrm{e}^{t}$
- $x<0$时，令$x=-\mathrm{e}^{t}$

# 无穷级数

## 常数项级数

通项中仅含有$n$吗，其写法为$\sum\limits_{n=1}^{\infty} u_{n}$。

### 性质

下列性质适用于**任意常数项级数**：

- 线性性质
- 无穷级数改变**任意有限项**，敛散性不会改变
- 若$S = \sum\limits_{n=1}^{\infty} u_{n}$收敛，则$\lim\limits _{n \rightarrow \infty} u_{n}=0$
  - 此性质是级数收敛的**必要条件**：也就是仅有$\lim \limits_{n \rightarrow \infty} u_{n}=0$这个条件时，不能说明级数收敛一定收敛
  - 但是反过来说，如果$\lim \limits_{n \rightarrow \infty} u_{n}\neq0$，那么必发散 ✅
- 夹逼准则：若$w_n<u_n<v_n$且$\sum\limits_{n=1}^{\infty} w_{n}$和$\sum\limits_{n=1}^{\infty} v_{n}$均收敛，则$\sum\limits_{n=1}^{\infty} u_{n}$也收敛

### 比阶问题

- 拆开级数，将含有合适的次方项保留，剩余项用$o(x^a)$表示即可 <1000题9.1>

### 常用常数项级数

比较判别法中比较常用的无穷级数，可以直接判定敛散性

- 等比级数：$\sum\limits_{n = 1}^\infty  {a{q^{n - 1}}} $ [证明参见2020·18讲P254]
  - 若$|q|\geq1$，则发散
  - 若$|q|\lt1$，则收敛，其和为$\frac{a}{1-q}$
- P级数：$\sum\limits_{n = 1}^\infty  {{1 \over {{n^p}}}} $，是一种特殊的正向级数 [证明参见2020·18讲P256]
  - 若$p>1$，则收敛
  - 若$p\leq1$，则发散
- $\sum\limits_{n=1}^{\infty} x_{n+1}-x_n$收敛$\Leftrightarrow$$\lim\limits_{n\rightarrow+\infty} x_n$存在，因为$S_n=x_{n+1}-x_1$

### 级数敛散性判别方法

收敛类型

- 绝对收敛：若$\sum\limits_{n=1}^{\infty} |u_{n}|$（通项加入绝对值）收敛，称之为绝对值收敛
- 条件收敛：若$\sum\limits_{n=1}^{\infty} u_{n}$收敛，$\sum\limits_{n=1}^{\infty} |u_{n}|$发散，则成为条件收敛

#### 正项级数

正项级数是指$u_n > 0$，那么同样的$S > 0$且$\{S_n\}$是单调递增的。

解题技巧

- 正向级数是可以使用等价无穷小替换的<1000题9.4③提公因子法>，尤其要注意含有$1\over n$的方程，同样的在使用完“比值判别法”或“根值判别法”之后也可以使用基本极限公式将极限计算出来。[参见`极限与连续 > 基本极限公式`] <1000题9.8, 9.14>
- 当通项为定积分的情况下，一般要使用放缩法把被积式化为一个简单的式子后再进行积分，最后利用比较判别法作出判断 <1000题9.5, 9.6>
  - $\sin ax$放缩为$ax$
- 利用无穷级数收敛定义反求数列极限 <1000题9.8>

方法

- 比较判别法[难点]，其核心思想是利用放缩法放缩为常用常数项级数后，再利用“小发散则大发散，大收敛则小收敛”原则进行判别，主要的放缩手段有：
  - 利用函数连续的有界性 <1000题9.2②>
  - 利用常用不等式进行放缩 <1000题9.3, 9.5, 9.6>
  - 基本不等式：去除部分分母使其变大 <1000题9.5>
- 比值判别法，适用于通项含有阶乘的级数 <1000题9.11>
- 根值判别法，适用于通项中含有$n$次方的级数 <1000题9.4(1)>

#### 交错级数

结题技巧

- 有的时候$(-1)^{n-1}$可以被$\cos n\pi$代替，当$n$取0, 1, 2, …时与其效果完全一致 <1000题9.16>
- $\sin n\pi$永远为0 <1000题9.20>

方法

- 判别绝对收敛
  - 利用等价无穷小代换 <1000题9.18, 9.19>
  - 利用放缩法 <1000题9.17>

- 莱布尼兹判别法 <1000题9.16>

  - 利用夹逼准则确定极限$\lim\limits_{n\rightarrow\infty} u^n$ <1000题9.17>
  - 误区1：$u_n$不单调减则级数发散 ❎（不单调减什么也说明不了）
- 不好直接用莱布尼兹判别法的，先考虑化简、拆项和加括号
  - 三角函数 <1000题9.20>
  - 泰勒展开式 <1000题9.21>
  - 有理化 <1000题9.22>
  - 加括号有一个注意点 <1000题9.23>
    - 如果原级数收敛，加上括号也收敛
    - 如果加上括号收敛，不能推出原级数收敛，除非加上条件$\lim\limits_{n\rightarrow\infty} u^n=0$

### 求和问题

- 利用等比数列，如果收敛（$|q|<1$），那么其和为$\frac{首项}{1-公比}$ <1000题9.44>
- 将常数项级数转为幂级数：补一个$x^{n-1}$或$x^n$或$x^{n+1}$使之变为一个幂级数，然后利用上面方法求出和函数，带入合适的$x$值即可 <1000题9.51>
- 利用傅里叶级数 <1000题9.68, 9.69, 9.70>

## 幂级数

### 阿贝尔定理

结论

- 收敛半径：假定$\sum\limits_{n = 1}^\infty  a_n(x-p)^n $，则其中心为于$x=p$，设$\lim \limits_{n \rightarrow \infty}\left|\frac{a_{n+1}}{a_{n}}\right|=\rho$，则收敛半径$R$为：

$$
R=\left\{\begin{array}{ll}{\frac{1}{\rho},} & {\rho \neq 0} \\ {+\infty,} & {\rho=0} \\ {0,} & {\rho=+\infty}\end{array}\right.
$$

- 如果给定幂级数不是连续的，如$\sum\limits_{n = 1}^\infty  a_n(x-p)^{\alpha n+\beta} $，那么求半径的时候需要注意$R=\sqrt{\frac{1}{\rho}}$当$\rho\neq0$时 <1000题9.32>

解题技巧

- 一般$a_n$是抽象的，但给定中心和某点的敛散性，推测另外一点的敛散性 <1000题9.29>
  - 收敛域内绝对收敛
  - 收敛域端点上不确定（代入$x$转化为常数项级数检查敛散性）
  - 收敛域外部必发散
- 幂级数是具体的（即给定$a_n$）求收敛域
  - 求收敛半径
  - 求端点的敛散性

### 幂级数展开求和问题

展开公式

- ${e^x}=\sum\limits_{n=0}^{\infty} \frac{x^{n}}{n !}=1+x+\frac{x^{2}}{2 !}+\cdots+\frac{x^{n}}{n !}+\cdots,-\infty<x<+\infty$
- ${1 \over {1 + x}}=\sum\limits_{n=0}^{\infty}(-1)^{n} x^{n}=1-x+x^{2}-x^{3}+\cdots+(-1)^{n} x^{n}+\cdots,-1<x<1$
- ${1 \over {1 - x}}=\sum\limits_{n=0}^{\infty} x^{n}=1+x+x^{2}+\cdots+x^{n}+\cdots,-1<x<1$
- $\ln \left( {1 + x} \right)=\sum\limits_{n=1}^{\infty}(-1)^{n-1} \frac{x^{n}}{n}=x-\frac{x^{2}}{2}+\frac{x^{3}}{3}-\frac{x^{4}}{4}+\cdots+(-1)^{n-1} \frac{x^{n}}{n}+\cdots,-1<x \leqslant 1$
- $\sin x=\sum\limits_{n=0}^{\infty}(-1)^{n} \frac{x^{2 n+1}}{(2 n+1) !} {=x-\frac{x^{3}}{3 !}+\frac{x^{5}}{5 !}-\frac{x^{7}}{7 !}+\cdots+(-1)^{n} \frac{x^{2 n+1}}{(2 n+1) !}+\cdots,-\infty<x<+\infty}$
- $\cos x=\sum\limits_{n=0}^{\infty}(-1)^{n} \frac{x^{2 n}}{(2 n) !}=1-\frac{x^{2}}{2 !}+\frac{x^{4}}{4 !}-\frac{x^{6}}{6 !}+\cdots+(-1)^{n} \frac{x^{2 n}}{(2 n) !}+\cdots,-\infty<x<+\infty$
注意
  - 角标开始于0还是1
  - 每个式子的收敛域
  - 这里的$x$是广义化的，如果需要也可改为$\frac{x}{2}$等，同样的收敛域也需要有相应的变化 <1000题9.36>
  - 角标+1时对应累加式$n$需要-1：$\sum\limits_{n=0}^{\infty}u_nx^n=\sum\limits_{n=1}^{\infty}u_{n-1}x^{n-1}$ 

解题技巧：不管是展开还是求和归根结底还是要回到幂级数那6种常用的展开公式上去。

- 展开问题：给定$f(x)$，求其幂级数$\sum\limits^\infty_{n=0}a_nx^n$
  - 当需要求在$x-a$点的展开式时，可以通过换元$t=x-a$转换为在$t$点展开 <1000题9.34>
    - 需要在最后将$t$转换$x$
    - 收敛域也需要同时转换
  - $f(x)$变形为标准的幂级数展开式
    - 恒等变形 <1000题9.36, 9.39>
    - 先积后导 <1000题9.38>
    - 先导后积 <1000题9.40>
      - 考虑常数$C$的取值问题，一般是$S(0)$，因为$S(x)-S(0) = \int_0^xf(t)dt$
      - 最后积分需要验证端点是否收敛
  - 与泰勒公式结合，若$f(x)=\sum\limits_{n=0}^{\infty}a_nx^n$，则$a_n=\frac{f^{(n)}(x)}{n!}$

- 求和问题：给定幂级数$\sum\limits^\infty_{n=0}a_nx^n$，求和函数$f(x)$
  - 如果通项是$u_n=\frac{1}{a_{n+1}}-\frac{1}{a_n}$，那么求$\sum\limits_{n=0}^{\infty}u_n$就可以全部写开，用加减抵消的方法来求和 <1000题9.43>
  - 先导后积 <1000题9.50>
  - 先积后导 <1000题9.49>

## 傅里叶级数

- 傅里叶级数展开式：任何连续或有有限个一类间断点的周期函数可以在$[l, -l]$展开为$f(x) \sim S(x) = \frac{a_0}{2} + \sum \limits_{n=1}^{\infty} a_n\cos  \frac{n\pi}{l}x+b_n\sin \frac{n\pi}{l}x$，其中：
  - $a_n = \frac{1}{l}\int^l_{-l} f(x)\cos \frac{n\pi}{l} x dx$
  - $b_n = \frac{1}{l}\int^l_{-l} f(x)\sin  \frac{n\pi}{l}x dx$

- 狄利克雷收敛定理
$$
  S(x)=
\left\{
  \begin{array}{l}
  {f(x)},\quad x为连续点 \\ 
  {\frac{f(x-0)+f(x+0)}{2},\quad x为间断点} \\ 
  {\frac{f(-\pi+0)+f(\pi-0)}{2},\quad x为端点}
  \end{array}
  \right.
$$

- 正弦级数$f(x)$是奇函数，因为正弦级数只有$b_n \sin \frac{n\pi}{l}x$，这是因为$a_n = \frac{1}{l}\int^l_{-l} f(x)\cos \frac{n\pi}{l} x dx$，奇函数$f(x)$x偶函数$\cos \frac{n\pi}{l} x$为奇函数，所以$a_n$为0，所以为正弦函数
- 余弦函数同理，利用积分的奇偶性可以算出$b_n=0$，这样展开式就只有$a_n\cos  \frac{n\pi}{l}x$了

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

椭圆

- 椭圆方程
- 椭圆切线 ${{{x_0}x} \over {{a^2}}} + {{{y_0}y} \over {{b^2}}} = 1$

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

点到直线（面）的距离

- 已知点$P\left( {{x_0},{y_0},{z_0}} \right)$，到平面$Ax+By+Cz+D=0$的距离为$d = {{\left| {A{x_0} + B{y_0} + C{z_0} + D} \right|} \over {\sqrt {{A^2} + {B^2} + {C^2}} }}$ <1000题6.28>
- [针对二维坐标系]已知点$P\left( {{x_0},{y_0}} \right)$，到直线$Ax+By+C=0$的距离为$d = {{\left| {A{x_0} + B{y_0} + C} \right|} \over {\sqrt {{A^2} + {B^2}} }}$
- [针对三维坐标系]已知点$P\left( {{x_0},{y_0},{z_0}} \right)$，在直线$L_1$中方向向量为$\mathord{\buildrel{\lower3pt\hbox{$\scriptscriptstyle\rightharpoonup$}}\over 
   s} $，其线上任一点$P_0$，$P$点到直线距离为$d = {{\left| {P{P_0} \times \mathord{\buildrel{\lower3pt\hbox{$\scriptscriptstyle\rightharpoonup$}}\over 
   s} } \right|} \over {\left| {\mathord{\buildrel{\lower3pt\hbox{$\scriptscriptstyle\rightharpoonup$}}\over 
   s} } \right|}}$ (原理参见叉乘的几何意义) <1000题6.8, 6.30>

线

- 已知$A(x_1,y_1),B(x_2,y_2)$，则$\overrightarrow {AB} $的坐标$\left(x_{2}-x_{1}, y_{2}-y_{1}\right)$

# 线性代数基础知识

## 单位矩阵

- $\boldsymbol{E}=\boldsymbol{E}^T$
- $|\boldsymbol{E}|=1$
- 提公因式$\boldsymbol{A}-\boldsymbol{AX}=\boldsymbol{A}(\boldsymbol{E}-\boldsymbol{X})$
- $E^n=E$ <1000 线代19>

## 转置

- $\boldsymbol{A}$和$\boldsymbol{B}$是$n$阶矩阵，$\boldsymbol{A}^T\pm\boldsymbol{B}^T = (\boldsymbol{A}\pm\boldsymbol{B})^T $<1000题 线代15>
- 假设$\alpha$和$\beta$都是<u>列向量</u>，$\alpha\beta^T$、$\beta\alpha^T$、$\alpha\alpha^T$都是矩阵（T在后面），$\alpha^T\beta$、$\beta^T\alpha$、$\alpha^T\alpha$都是数（T在前面）

# 行列式

数值型行列式

- 性质

  - 提公因式 <1000题 线代1> 
    $\left|\begin{array}{cccc}{a_{11}} & {a_{12}} & {\cdots} & {a_{1 n}} \\ {\vdots} & {\vdots} & {} & {\vdots} \\ {k a_{i 1}} & {k a_{i 2}} & {\cdots} & {k a_{i n}} \\ {\vdots} & {\vdots} & {} & {\vdots} \\ {a_{n 1}} & {a_{n 2}} & {\cdots} & {a_{m}}\end{array}\right|=k\left|\begin{array}{cccc}{a_{11}} & {a_{12}} & {\cdots} & {a_{1 n}} \\ {\vdots} & {\vdots} & {} & {\vdots} \\ {a_{i 1}} & {a_{i 2}} & {\cdots} & {a_{i n}} \\ {\vdots} & {\vdots} & {} & {\vdots} \\ {a_{n 1}} & {a_{n 2}} & {\cdots} & {a_{m}}\end{array}\right|$
    - 推广：$|k A|=k^{n}|A|$
  - 行列交换加负号 <1000题 线代2, 线代9>
- 展开公式，适用于行列式的某一行只有1-2个数不是0 <1000题 线代5>
- 加边法 
$$\left|\begin{array}{cccc}{a_{11}} & {a_{12}} & {\cdots} & {a_{1 n}} \\ {\vdots} & {\vdots} & {} & {\vdots} \\ {a_{i 1}} & {a_{i 2}} & {\cdots} & {a_{i n}} \\ {\vdots} & {\vdots} & {} & {\vdots} \\ {a_{n 1}} & {a_{n 2}} & {\cdots} & {a_{m}}\end{array}\right| = \left|\begin{array}{cccc} {1} & {*} & {*} & {\cdots} & {*} \\ {0} &  {a_{11}} & {a_{12}} & {\cdots} & {a_{1 n}} \\ {\vdots} & {\vdots} & {\vdots} & {} & {\vdots} \\ {0} & {a_{i 1}} & {a_{i 2}} & {\cdots} & {a_{i n}} \\ {\vdots} & {\vdots} & {\vdots} & {} & {\vdots} \\ {0} & {a_{n 1}} & {a_{n 2}} & {\cdots} & {a_{m}}\end{array}\right|=\left|\begin{array}{cccc} {1} & {0} & {0} & {\cdots} & {0} \\ {*} &  {a_{11}} & {a_{12}} & {\cdots} & {a_{1 n}} \\ {\vdots} & {\vdots} & {\vdots} & {} & {\vdots} \\ {*} & {a_{i 1}} & {a_{i 2}} & {\cdots} & {a_{i n}} \\ {\vdots} & {\vdots} & {\vdots} & {} & {\vdots} \\ {*} & {a_{n 1}} & {a_{n 2}} & {\cdots} & {a_{m}}\end{array}\right|$$

- 递推式
  
  - 三对角型行列式 <1000题 线代7, 线代10, 线代11>
  
- 重要行列式

  - 主对角线行列式 
    $\left|\begin{array}{rrrr}{a_{11}} & {a_{12}} & {\cdots} & {a_{1 n}} \\ {0} & {a_{22}} & {\cdots} & {a_{2 n}} \\ {\vdots} & {\vdots} & {} & {\vdots} \\ {0} & {0} & {\cdots} & {a_{nn}}\end{array}\right|=\left|\begin{array}{cccc}{a_{11}} & {0} & {\cdots} & {0} \\ {a_{21}} & {a_{22}} & {\cdots} & {0} \\ {\vdots} & {\vdots} & {} & {\vdots} \\ {a_{n 1}} & {a_{n 2}} & {\cdots} & {a_{nn}}\end{array}\right|=\left|\begin{array}{cccc}{a_{11}} & {0} & {\cdots} & {0} \\ {0} & {a_{22}} & {\cdots} & {0} \\ {\vdots} & {\vdots} & {} & {\vdots} \\ {0} & {0} & {\cdots} & {a_{nn}}\end{array}\right|=\prod\limits_{i=1}^{n} a_{ii}$
  - 副对角线行列式
    $\left|\begin{array}{ccccc}{a_{11}} & {a_{12}} & {\cdots} & {a_{1, n-1}} & {a_{1 n}} \\ {a_{21}} & {a_{22}} & {\cdots} & {a_{2, n-1}} & {0} \\ {\vdots} & {\vdots} & {} & {\vdots} & {\vdots} \\ {a_{n 1}} & {0} & {\cdots} & {0} & {0}\end{array}\right|=\left|\begin{array}{cccc}{0} & {\cdots} & {0} & {a_{1 n}} \\ {0} & {\cdots} & {a_{2, n-1}} & {a_{2 n}} \\ {\vdots} & {} & {\vdots} & {\vdots} \\ {a_{n 1}} & {\cdots} & {a_{n, n-1}} & {a_{m}}\end{array}\right|=\left|\begin{array}{cccc}{0} & {\cdots} & {0} & {a_{1 n}} \\ {0} & {\cdots} & {a_{2, n-1}} & {0} \\ {\vdots} & {} & {\vdots} & {\vdots} \\ {a_{n 1}} & {\cdots} & {0} & {0}\end{array}\right|=(-1)^{\frac{n(n-1)}{2}} a_{1 n} a_{2, n-1} \cdots a_{n 1}$
  - 拉普拉斯行列式，也分主对角和副对角线：
    - 主对角线$\left|\begin{array}{ll}{A} & {O} \\ {O} & {B}\end{array}\right|=\left|\begin{array}{ll}{A} & {C} \\ {O} & {B}\end{array}\right|=\left|\begin{array}{ll}{A} & {O} \\ {C} & {B}\end{array}\right|=|A||B|$ <1000题 线代2>
	  - 副对角线$\left|\begin{array}{ll}{O} & {A} \\ {B} & {O}\end{array}\right|=\left|\begin{array}{ll}{C} & {A} \\ {B} & {O}\end{array}\right|=\left|\begin{array}{ll}{O} & {A} \\ {B} & {C}\end{array}\right|=(-1)^{m n}|A||B|$
	- 范德蒙德行列式，其规律是$n\times n$行列式最高次数为$n-1$，如果是$(n+1)\times(n+1)$行列式则最高次数为$n$才能满足 <1000题 线代9>
	$\left|\begin{array}{cccc}{1} & {1} & {\cdots} & {1} \\ {x_{1}} & {x_{2}} & {\cdots} & {x_{n}} \\ {x_{1}^{2}} & {x_{2}^{2}} & {\cdots} & {x_{n}^{2}} \\ {\vdots} & {\vdots} & {} & {\vdots} \\ {x_{1}^{n-1}} & {x_{2}^{n-1}} & {\cdots} & {x_{n}^{n-1}}\end{array}\right|=\prod\limits_{1 \leqslant i<j \leqslant n}\left(x_{j}-x_{i}\right)$
	- 经常使用的行列式1
	  $\left|\begin{array}{cccccc} {a} & {b} & {b} & {\cdots} & {b} & {b} \\ {b} & {a} & {b} & {\cdots} & {b} & {b} \\ {b} & {b} & {a} & {\cdots} & {b} & {b} \\ {\vdots} & {\vdots} & {\vdots} & {} & {\vdots} & {\vdots} \\ {b} & {b} & {b} & {\cdots} & {a} & {b} \\  {b} & {b} & {b} & {\cdots} & {b} & {a} \end{array}\right|= [a+(n-1)b](a-b)^{n-1}$
	- 爪型转三角型 <1000题 线代6>

抽象型行列式

- 性质
  - $\left|A^{T}\right|=|A|$
  - $|A B|=|A||B|$
  - $\left|A^{*}\right|=|A|^{n-1}$
  - 若$A$是$n$阶可逆矩阵，则$\left|A^{-1}\right|=|A|^{-1}$
  - 若$\lambda_{1}, \lambda_{2}, \cdots, \lambda_{n}$是矩阵$A$的特征值，则$|A|=\lambda_{1} \lambda_{2} \cdots \lambda_{n}$
  - 若矩阵$A$与矩阵$B$相似，则$|A|=|B|$
    - $P^{-1}AP=B \Rightarrow |P^{-1}AP|=|B|$
    - $|A B|=|A||B|$，$|P^{-1}||A||P|=|B|$
    - 由$|P^{-1}||P|=1$可以推出$|A|=|B|$
- 矩阵的性质，适用于矩阵的每一列与$\alpha_1, \alpha_2,  \cdots, \alpha_n$有关，则可分解为$(\alpha_1, \alpha_2, \cdots, \alpha_n)\boldsymbol{C}$，其中$\boldsymbol{C}$是一个$n\times n$的矩阵 <1000题 线代13>

# 矩阵

## 基本运算

- 数乘 <1000题 线代21>
  $k A=A k=k\left[\begin{array}{cccc}{a_{11}} & {a_{12}} & {\cdots} & {a_{1 n}} \\ {a_{21}} & {a_{22}} & {\cdots} & {a_{2 n}} \\ {\vdots} & {\vdots} & {} & {\vdots} \\ {a_{m 1}} & {a_{m 2}} & {\cdots} & {a_{m n}}\end{array}\right]=\left[\begin{array}{cccc}{k a_{11}} & {k a_{12}} & {\cdots} & {k a_{1 n}} \\ {k a_{21}} & {k a_{22}} & {\cdots} & {k a_{2 n}} \\ {\vdots} & {\vdots} & {} & {\vdots} \\ {k a_{m 1}} & {k a_{m 2}} & {\cdots} & {k a_{m n}}\end{array}\right]$

## 求$\boldsymbol{A}^n$(方阵的幂)

- $r(A) = 1$型，若${A}={\alpha}{\beta}^T$，其中${\alpha}$和${\beta}$是n维非零<u>列向量</u>，则${A}^n = l^{n-1}{A}$，其中$l=\alpha^T\beta=\sum\limits_{i=1}^n a_{ii}$（迹） <1000题 线代34>
- 用归纳法，先求出$A^2, A^3, \cdots$，然后找规律 <1000题 线代27>
  - $ A^{2}=k A\Rightarrow A^{n}=k^{n-1} A$
  - $A^{2}=k E$
    - $A^{2 n}=(k E)^{n}=k^{n} E$
    - $A^{2 n+1}=k^{n} A$
  - $A=\left[\begin{array}{lll}{0} & {a} & {c} \\ {0} & {0} & {b} \\ {0} & {0} & {0}\end{array}\right]$型，则$A^{2}=\left[\begin{array}{ccc}{0} & {0} & {a b} \\ {0} & {0} & {0} \\ {0} & {0} & {0}\end{array}\right]$，$A^{3}=A^{4}=\cdots=A^{n}=0$
  - $A=\left[\begin{array}{lll}{0} & {a} & {b} & c \\ {0} & {0} & {d} & f \\ {0} & {0} & {0} & e \\ 0 & 0 & 0 & 0 \end{array}\right]$型，则$A^3 = \left[\begin{array}{lll}{0} & {0} & {0} & {ade} \\ {0} & {0} & {0} & 0 \\ {0} & {0} & {0} & 0 \\ 0 & 0 & 0 & 0 \end{array}\right]$，$A^4=A^5=\cdots=A^n=0$
- $A^n = (B + C)^n$，使用展开式的前提是$BC=CB$ [参见`高等数学基础知识 > 因式分解公式`]
  - $B=E$
  - $BC=CB=0$
- 相似，若$P^{-1} A P=\Lambda$，则$P^{-1} A^{n} P=\Lambda^{n}$，则$A^{n}=P\Lambda^{n}P^{-1}$
- 初等行变换，即$P_1^mAP_2^n$（左行右列）
- 分块矩阵，$\left[\begin{array}{ll}{A} & {0} \\ {0} & {B}\end{array}\right]^{n}=\left[\begin{array}{ll}{A^{n}} & {0} \\ {0} & {B^{n}}\end{array}\right]$ <1000题 线代40>

## 伴随、逆与初等阵

接下来的全部内容的矩阵必是方阵

### 伴随矩阵

定义

-  $A^{*}=\left[\begin{array}{cccc}{A_{11}} & {A_{21}} & {\cdots} & {A_{n 1}} \\ {A_{12}} & {A_{22}} & {\cdots} & {A_{n 2}} \\ {\vdots} & {\vdots} & {} & {\vdots} \\ {A_{1 n}} & {A_{2 n}} & {\cdots} & {A_{m}}\end{array}\right]$
-  ${A A}^{*}={A}^{*} {A}=|{A}|{E}$

公式

- ${A A}^{*}={A}^{*} {A}=|{A}|{E}$
- $\left|A^{*}\right|=|A|^{n-1}$
  - 推导过程：$|AA^*|=\left|\left|A\right|E\right|=|A|^n \Rightarrow |A||A^*|=|A|^n \Rightarrow |A^*|=|A|^{n-1}$
- $\left(A^{T}\right)^{*}=\left(A^{*}\right)^{T}$
  - $\left(A^{-1}\right)^{*}=\left(A^{*}\right)^{-1}$
  - $\left(A^{T}\right)^{-1}=(A^{-1} ){T}$
- $(k A)^{*}=k^{n-1} A^{*}$
  - $|k A|=k^{n}|A|$
  - $(k A)^{T}=k A^{T}$
  - $(k A)^{-1}=\frac{1}{k} A^{-1}$
- $A^{-1} =\frac{1}{|A|}A^{*}$
- $ A^{*}=|A|A^{-1}$
- $\left(A^{-1}\right)^{*}=\left(A^{*}\right)^{-1}$
- $\left(A^{*}\right)^{*}=|A|^{n-2} A$
- $|\left(A^{*}\right)^{*}|=|A|^{(n-1)^2}$
- $(A B )^{*}=B^{*} A^{*}$
  - $(A B )^{T}=B^{T} A^{T}$
  - $(A B )^{-1}=B^{-1} A^{-1}$

秩 (TODO: 待补充)

解题思路

- 若$a_{ij}=A_{ij}$，那么$A^T=A^*$ <1000题 线代29>
  - $|A|=1$
  - 矩阵$A$可逆且正交

### 可逆矩阵

定义

- $AB=E\Rightarrow A=B^{-1}$ <1000题 线代19, 线代21>
- 等价说法：非奇异矩阵 = 可逆矩阵

性质

- $\left(A^{-1}\right)^{-1}=A$
- $(k A)^{-1}=\frac{1}{k} A^{-1}$
- $(A B)^{-1}=B^{-1} A^{-1}$
- $\left|A^{-1}\right|=|A|^{-1}$
- $\left(A^{T}\right)^{-1}=(A^{-1} ){T}$

求逆

- 具体型
  - 利用伴随矩阵，即$A^{-1}=\frac{1}{|A|} A^{*}$
  - 初等变换法，即$(A|E)=(E|A^{-1})$
- 抽象型
  - 定义
  - $A=BC$且$B$和$C$都可逆，则$A^{-1}=C^{-1}B^{-1}$

分块矩阵

- 加法
- 数乘
- 乘法
- $\left[\begin{array}{ll}{A} & {0} \\ {0} & {B}\end{array}\right]^{n}=\left[\begin{array}{ll}{A^{n}} & {0} \\ {0} & {B^{n}}\end{array}\right]$
- 求逆
  - 主对角线直接求逆，左边乘上同行的，右边乘上同列的，最后加一个负号
    - $\left[\begin{array}{ll}{B} & {O} \\ {D} & {C}\end{array}\right]^{-1}=\left[\begin{array}{ll}{B^{-1}} & {O} \\ {-C^{-1}DB^{-1}} & {C^{-1}}\end{array}\right]$
    - $\left[\begin{array}{ll}{B} & {D} \\ {O} & {C}\end{array}\right]^{-1}=\left[\begin{array}{ll}{B^{-1}} & {-B^{-1}DC^{-1}} \\ {O} & {C^{-1}}\end{array}\right]$
  - 副对角线换位置求逆，$O$和$D$也换位置后，左边乘上同行的，右边乘上同列的，最后加一个负号
    - $\left[\begin{array}{ll}{O} & {B} \\ {C} & {D}\end{array}\right]^{-1}=\left[\begin{array}{ll}{-C^{-1}DB^{-1}} & {C^{-1}} \\ {B^{-1}} & {O}\end{array}\right]$
    - $\left[\begin{array}{ll}{D} & {B} \\ {C} & {O}\end{array}\right]^{-1}=\left[\begin{array}{ll}{O} & {C^{-1}} \\ {B^{-1}} & {-B^{-1}DC^{-1}}\end{array}\right]$

解题技

- 证明矩阵是否可逆
  - 利用行列式，如果$|A|\neq0$，那么矩阵$A$可逆 <1000题 线代29>
  - 秩等于行数
  - 行向量(或列向量)是线性无关组
  - 齐次线性方程组$AX=0$仅有零解
  - 非齐次线性方程组$AX=b$有唯一解
  - 可以经过初等行变换化为单位矩阵，即该矩阵等价于n阶单位矩阵
  - 特征值全部非0 <1000题 线代34>
- 求$(A+B)^{-1}$没有直接可以用的性质，要借助单位矩阵$E$来将其化为相乘后，在使用可逆的性质求解 <1000题 线代18>

### 初等阵

定义

性质

- 转置
- 逆
- 伴随

左行右列定理

应用

## 矩阵方程

定义

化简

求解

- 直接求解
- 化方程组
- 待定元素法

## 秩

定义

公式

- $r(A+B)$
- $r(AB)$
- $AB = 0$
- $r(A)$与$r({A^T})$的关系
- 若A可相似对角化为$\Lambda$，则$r(A)$与$r(\Lambda)$的关系
- $r(A|B)$
- $r(A^*)$

考法

- 化阶梯
- 用公式

## 特殊矩阵

- 正交矩阵是指$\boldsymbol{A}^T\boldsymbol{A}=\boldsymbol{E} \Leftrightarrow \boldsymbol{A}^T=\boldsymbol{A}^{-1}$，其性质有
  - 特征值全部为$1$或$-1$ <1000题 线代15, 线代16>

## 等价、合同与相似

矩阵等价 [(ref)](https://blog.csdn.net/abraham_li/article/details/50058123)

- 定义：对同型矩阵A、B，存在可逆阵P和Q，使得$B=PAQ$
- 充要条件：A与B的秩相同

矩阵合同

- 定义：对同型方阵A、B，存在可逆阵P使得$B=P^{T} A P$

矩阵相似

- 定义：对同型方阵A、B，存在可逆阵P，使得$B=P^{-1} A P$

关系：等价（只有秩相同）–>合同（秩和正负惯性指数相同）–>相似（秩，正负惯性指数，特征值均相同）

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