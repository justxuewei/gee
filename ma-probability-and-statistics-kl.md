# 随机事件与概率

古典概型求概率

- 随机分配问题（放球问题），假设有N个盒子和n个小球，则
  - 每盒可以容纳任意多个球，那么不同的分法有$N^n$，也就是每个小球都有N种备选盒
  - 每盒仅可以容纳1个求，则不同的分法有$N(N-1)\cdots(N-n+1)$，也就是已经装球的盒子在下一次放球时就不考虑了。
    - 特殊情况：当$N=n$时，共有$N!$种分法

- 简单随机抽样问题（取球问题），假设有N个小球($\Omega$)取n次，则
  - 先后有放回的取n次，则抽法总数有$N^n$
  - 先后无放回额取n次，则抽法总数有$N(N-1)\cdots(N-n-1)$
  - 一次型任取n个（无先后顺序），则抽法总数有$C^n_N$

- 集合概型求概率
  
- 与形状、位置无关，关键是面积（在二维平面上讨论）
  
- 重要公式求概率
  - 用对立
    - $\overline{A\cup B} = \overline{A} \cap \overline{B}, \overline{AB} = \overline{A} \cup \overline{B}$
    - $P(A)=1-P(\overline{A})$
    
  - 用互斥
    
      - $A \cup B = A \cup \overline{A}B = B \cup \overline{B}A = \overline{A}B \cup AB \cup \overline{B}A$
      - $(A\cup B)(\overline A \cup B) = B$
      - $B_1, B_2, B_3$为完备事件组，则$A = AB_1 \cup AB_2 \cup AB_3$ （全概率思想）
      - $P(A\overline{B}) = P(A-B) = P(A) - P(AB)$
      - $P(A+B) = P(A) + P(B) - P(AB)$
    - $P(A+B+C)=P(A)+P(B)+P(C)-P(AB)-P(AC)-P(BC)+P(ABC)$
    - 若$A_1, A_2, \cdots, A_n$两两互斥，则$P(\bigcup\limits^n_{i=1}A_i) = \sum\limits^n_{i=1}P(A_i)$
    
  - 用独立
  
    > 这里讨论一下独立和互斥的关系：以抛硬币这个问题来说，抛一次抛出正面和反面这两个事件来看是互斥的，抛第二次与第一次结果无关来看又是独立的；从公式来看，互斥$P(AB)=0$，独立$P(AB)=P(A)P(B)$，即独立必不互斥，互斥必不独立。
  
    - $A_1, \cdots, A_n$相互独立，则$P(A_1\cdots A_n)=P(A_1)\cdots P(A_n)$
    - $A_1, \cdots, A_n$相互独立，则$P(\bigcup\limits^n_{i=1}A_i)=1-P(\bigcap\limits^n_{i=1}\overline{A_i}) = 1 - \prod\limits^n_{i=1} P(\overline A_i) = 1 - \prod\limits^n_{i=1} [1-P(A_i)]$
  
  - 用条件
  
    - $P(A|B) = \frac{P(AB)}{P(B)}$
    - $P(AB)=P(B)P(A|B) = P(A)P(B|A)$
    - $P(AB) = P(A) + P(B) - P(A+B) $
    - $P(AB) = P(A-\overline B) = P(A) - P(A\overline B)$
    - 知因求果$P(B) = \sum\limits^n_{i=1}P(A_i)P(B|A_i)$
    - 知果求因$P(A_i|B) = \frac{P(A_jB)}{P(B)}$
    
  - 用不等式
  
      - $0 \le P(A) \le 1$
      - 若$A\subset B$，则$P(A)\le P(B)$，常见的有$P(AB)\le P(A) \le P(A+B)$
  
  - 用最值
  
      - $\{\max(X, Y) \le a\} = \{X\le a\} \cap \{Y\le a\}$
      - $\{\max(X, Y) > a\} = \{X > a\} \cup \{Y > a\}$
      - $\{\min(X, Y) \le a\} = \{X\le a\} \cup \{Y\le a\}$
      - $\{\min(X, Y) > a\} = \{X > a\} \cap \{Y > a\}$
      - $\{\max(X, Y) \le a\} \subset \{\min(X, Y) \le a\}$
      - $\{\min(X, Y) > a\} \subset \{\max(X, Y) > a\}$
  
- 事件的独立性

  - $P(AB) = P(A)P(B)$
  - $A, B, \overline A, \overline B$任意两个不同字母的都相互独立
  - $A, B, C, D$相互独立，则任何运算也相互独立
  - A，B相互独立且$P(A) > 0$，则$P(B|A)=P(B)$
  - 若$0 < P(A) < 1$且A与B相互独立，$\Leftrightarrow P(B|A)=P(B | \overline A) = P(B)$，$\Leftrightarrow P(B|A) + P(\overline B|A) = 1$， $\Leftrightarrow P(B|A)+P(\overline B | \overline A) = 1$
  - 若$P(A) = 0$或$P(A) = 1$，则A与任意事件独立
  - 若$0 < P(A) < 1$且$0 < P(B) < 1$，且A与B互斥或存在包含关系，则必不可能独立。
    - 如果互斥，则$[P(AB)=0]\neq P(A)P(B)$

# 一维随机变量及其分布

## 判分布

分布函数

- 判别方式
  - 单调不减
  - 右连续，表现为"="总加在x的">"上，如$1 \le x < 2$
  - $F(-\infty)=0$
  - $F(+\infty)=1$
- 若$a, b$均大于0且$a+b=1$，$F_1(x)$与$F_2(x)$都是概率分布函数，则$F(x)=aF_1(x)+bF_2(x)$也是概率分布函数，证明过程套用上面的判别方式。
- 若$F_1(x)$与$F_2(x)$都是概率分布函数，则$F(x) = F_1(x)F_2(x)$也是概率分布函数
- 利用$F(-\infty)=0$和$F(+\infty)=1$反求系数 <1000题 概率49>
- 如果<u>连续型随机变量</u>$X$的概率密度$f(x)$是<u>偶函数</u>，则
  - $F(-a) = 1-F(a)$
  - $P\{|X|<a\} = 2F(a) - 1$
  - $P\{|X|>a\} = 2[1-F(a)]$

概率分布（离散型随机变量）

- 判别方式
  - $p_i\ge0$
  - $\sum\limits^n_{i=1}p_i=1$

概率密度（连续型随机变量）

- 判别方式
  - $f(x)\ge0$
  - $\displaystyle \int_{-\infty}^{+\infty}f(x)dx=1$
- 若$F_1(x)$与$F_2(x)$是概率分布函数，$f_1(x)$与$f_2(x)$是概率密度函数，则$F_1f_1+F_2f_2$也是概率密度函数，使用判别方式证明

## 求分布

一般型问题

- 给定X与Y的关系（如$Y=2X$）和$F_X(x)$，求$F_Y(y)$ <1000题 概率36, 概率37>
  - 分布函数法，利用$P\{Y\le y\}=P\{2X\le y\}$找到$F_X(x)$与$F_Y(y)$的关系
  - 公式法

离散型  *(p32|[期望和方差参见这里](https://wenku.baidu.com/view/e8bfbef9910ef12d2af9e740.html))*

- 0-1分布$X \sim B(1, p)$
- 二项分布$X \sim B(n, p)$
  - 期望：$np$
  - 方差：$npq$
  - 二项分布与0-1分布的关系：如果$X_i\sim B(1, p)$，即$X_i$服从0-1分布，并且<u>相互独立</u>，则$Y_n = \sum^n\limits_{i=1}X_i \sim B(n, p)$
  - 求二项分布的三种方法
    - 当$n$不太大时直接计算，即$P\{X = k\} = C^k_n p^k (1-p)^{n-k}$
    - 当$n$较大且$p$较小时（$n > 10, p < 0.1$）利用泊松分布近似，即$\displaystyle P\{X = k\} \approx \frac{\lambda^k}{k!}e^{-\lambda} $
    - 当$n$较大且$p$不太大且<u>求一个范围</u>时利用中心极限定理近似，即$\displaystyle P\{a < X < b\} \approx \Phi(\frac{a - EX}{\sqrt{DY}}) - \Phi(\frac{b - EX}{\sqrt{DY}}) = \Phi(\frac{a - np}{\sqrt{np(1-p)}}) - \Phi(\frac{b - np}{\sqrt{np(1-p)}})$ <1000题 概率142>
- 泊松分布$X \sim P(\lambda)$
  - 定义：$P\{X=k\} = \frac{\lambda^{k}}{k!} e^{-\lambda}(k=0, 1, \cdots;\lambda>0)$
    - 如果给定$P\{X\le 1\} = P\{X = 0\} + P\{X = 1\}$，因为k只能取0及以上
  - 期望：$\lambda$
  - 方差：$\lambda$
- 几何分布
  - 实际意义：前k-1次皆失败，第k次成功的概率
  - 定义：$P\{X = k\} = (1-p)^{k-1}p$
  - 期望：$\displaystyle 1\over p$
  - 方差：$\displaystyle 1-p \over p^2$ <证明 1000题 概率115>
- 超几何分布
  - 定义：$\displaystyle P(X=k)=\frac{C_{M}^{k} C_{N-M}^{n-k}}{C_{N}^{n}}$
  - 实际意义：从有限N个物件（其中包含M个指定种类的物件）中抽出n个物件，成功抽出该指定种类的物件的次数（不放回）
  - 期望：$n\frac{M}{N}$

连续型

- 均匀分布$X\sim U(a, b)$
  - 定义：
    - 概率密度函数：$X\sim f(x)=\left\{\begin{array}{l}{\frac{1}{b-a}, a\le x < b} \\ {0, else}\end{array}\right.$，图3-2-1
    - 分布函数：$F(x)=\left\{\begin{array}{l}{0, x < a \\ \frac{x-a}{b-a}, a\le x < b \\ 1, x \ge b}\end{array}\right.$， 图3-2-2 
  - 期望：$\displaystyle \frac{a+b}{2}$
  - 方程：$\displaystyle \frac{(b-a)^2}{12}$
- 指数分布$X\sim E(\lambda)$
  - 定义：下面的$\lambda>0$
    - 概率密度函数：$X\sim f(x)=\left\{\begin{array}{l}{\lambda e^{-\lambda x}, x>0} \\ {0, x \leq 0}\end{array}\right.$，图3-2-3
    - 分布函数：$F(x)=\left\{\begin{array}{l}{1-e^{-\lambda x}, x\ge0} \\ {0, x < 0}\end{array}\right.$，图3-2-4
  - 期望： $1\over\lambda$
  - 方差：$1\over\lambda^2$
  - 无记忆性：$P\{X\ge t+s|X\ge t\} = P\{X\ge s\}$
- 正态分布$X\sim N(\mu, \sigma^2)$
  - 定义：$\displaystyle X \sim f(x)=\frac{1}{\sqrt{2 \pi} \sigma} e^{-\frac{(x-\mu)^{2}}{2 \sigma^{2}}} (-\infty<x<+\infty, \sigma>0)$，下图3-2-5
  - 期望：$\mu$
  - 方差：$\sigma^2$
  - 性质
    - $\frac{X-\mu}{\sigma}\sim0$，将任意正态分布化为标准正态分布
    - $F(x)=P\{X\le x\}=\Phi(\frac{x-\mu}{\sigma})$ 
      - 比较两个不同的正态分布概率 <1000题 概率35>
    - $P\{a \le X\le b\}=\Phi(\frac{b-\mu}{\sigma})-\Phi(\frac{a-\mu}{\sigma})$
      - 特殊情况1：$P\{\mu-\sigma \le X\le \mu+\sigma\}=\Phi(1)-\Phi(-1)=2\Phi(1)-1$
      - 特殊情况2：$P\{\mu-k\sigma \le X\le \mu+k\sigma\}=\Phi(k)-\Phi(-k)=2\Phi(k)-1$
- 标准正态分布

<img height="200" src="http://res.niuxuewei.com/2019-08-09-021646.png" /><img height="200" src="http://res.niuxuewei.com/2019-08-08-122213.png" /><img height="200" src="http://res.niuxuewei.com/2019-08-08-034245.png" />

## 用分布

若$X \sim F(x)$，则

- 

## 求函数分布

(连) $\rightarrow$ (连)

- 分布函数法 <1000题 概率123(分段函数+全集分解思想)>

# 多维随机变量

## 判分布

有界性

- $F(-\infty, y)=F(x,-\infty)=F(-\infty,-\infty)=0$
- $F(+\infty,+\infty)=1$

充要条件

- 离散型：$(X, Y) \sim p_{ij}$
  - $p_{ij} \ge 0$
  - $\displaystyle \sum\limits_{j}\sum\limits_{i} p_{ij} = 1$
- 连续型：$(X, Y) \sim f(x, y)$
  - $f(x, y) \ge 0$
  - $\displaystyle \int_{-\infty}^{+\infty}\int_{-\infty}^{+\infty} f(x, y) dxdy = 1$

## 求分布

求联合分布

- 求$F(x, y)$，将各个点延伸出上、右线，然后用一个方形卡点
  - $(X, Y) \sim p_{ij}$，则$F(x, y) = P\{X \le x, Y \le y\} = \sum\limits_{i=1}\sum\limits_{j=1}p_{ij}$
  - $(X, Y) \sim f(x, y)$，则$F(x, y) = P\{X \le x, Y \le y\} = \int^x_{-\infty}du\int^y_{-\infty} f(u, v)dv$ （注意符号变号问题）
- 求$p_{ij}$
- 求$f(x,y)$
  - 二维均匀分布$f(x, y)=\left\{\begin{array}{l}{\frac{1}{S_{D}}, \quad (x, y) \in D} \\ {0, \quad else}\end{array}\right.$，其中$S_D$为D的面积
  - 二维正态分布，记为$(X, Y) \sim N(\mu_1, \mu_2; \sigma^2_1, \sigma^2_2; \rho)$
    - 条件概率密度和边缘概率密度均为正态分布 <1000题 概率82>
    - 若$(X_1, X_2) \sim N(\mu_1, \mu_2; \sigma^2_1, \sigma^2_2; \rho)$，则$X_1\sim(\mu_1, \sigma^2_1), X_2\sim(\mu_2, \sigma^2_2)$
    - 若$X_1\sim(\mu_1, \sigma^2_1), X_2\sim(\mu_2, \sigma^2_2)$且$X_1X_2$<u>相互独立</u>，则$(X_1, X_2) \sim N(\mu_1, \mu_2; \sigma^2_1, \sigma^2_2; \rho)$
    - 若$(X_1, X_2) \sim N(\mu_1, \mu_2; \sigma^2_1, \sigma^2_2; \rho)$，则$k_1X_1+k_2X_2\sim(k_1\mu_1+k_2\mu_2, \sigma^2_1+\sigma^2_2)$，即二维降为一维 <1000题 概率89>
    - 若$(X_1, X_2) \sim N(\mu_1, \mu_2; \sigma^2_1, \sigma^2_2; \rho)$，设$Y_{1}=a_{1} X_{1}+a_{2} X_{2}, Y_{2}=b_{1} X_{1}+b_{2} X_{2}$，且$\left|\begin{array}{ll}{a_1} & {a_2} \\ {b_1} & {b_2}\end{array}\right| \ne 0$，即$a_1, a_2$与$b_1, b_2$不成比例，则$(Y_1, Y_2) \sim N$
    - 若$(X_1, X_2) \sim N(\mu_1, \mu_2; \sigma^2_1, \sigma^2_2; \rho)$，则$X_1, X_2$相互独立

求边缘分布

- $F_X(x) = P\{X \le x, Y \le +\infty\} = F(x, +\infty)$，同理$F_Y(y) = F(+\infty, y)$
- 边缘概率分布
  - $p_{i .}=\sum\limits_{j} p_{i j}$
  - $p_{ . j}=\sum\limits_{i} p_{i j}$
- 边缘概率密度 <1000题 概率62>
  - $\displaystyle f_{X}(x)=\int_{-\infty}^{+\infty} f(x, y) d y$
  - $\displaystyle f_{Y}(y)=\int_{-\infty}^{+\infty} f(x, y) d x$
- 边缘分布函数 $P\{a\le X\le b \} = \int^a_b f_{X}(x) dx$ <1000题 概率64>

求条件概率

- 离散型
  - $\displaystyle P\left\{Y=y_{j} | X=x_{i}\right\}=\frac{P\left\{X=x_{i}, Y=y_{j}\right\}}{P\left\{X=x_{i}\right\}}=\frac{p_{i j}}{p_{i.}}$
  - $\displaystyle P\left\{X=x_{i} | Y=y_{j}\right\}=\frac{P\left\{X=x_{i}, Y=y_{j}\right\}}{P\left\{Y=y_{i}\right\}} = \frac{p_{ij}}{p_{.j}}$
- 连续型
  - $\displaystyle f_{Y | X}(y | x)=\frac{f(x, y)}{f_{X}(x)}$, $\displaystyle \int_{-\infty}^{+\infty}f_{Y | X}(y | x) dy = 1$
  - $\displaystyle f_{X | Y}(x | y)=\frac{f(x, y)}{f_{Y}(y)}$, $\displaystyle \int_{-\infty}^{+\infty}f_{X | Y}(x | y) dx = 1$ <1000题 概率82>
- 拓展：
  - 求联合：联合 = 条件 x 边缘

判独立

- $F(x, y)=F_{X}(x) \cdot F_{Y}(y), \forall x, y$
- $p_{i j}=p_{\cdot i} p_{\cdot j}, \forall i, j$
- $f(x, y)=f_{X}(x) f_{Y}(y), \forall x, y$

## 求函数分布

多维 $\rightarrow$ 一维

- (离, 离) $\rightarrow$ (离)
  - 分布函数法
  - 公式法，前提是随机变量<u>相互独立</u>，设$X \sim p_k, Y \sim q_k$
    - $Z=X+Y$，则$P\{Z=k\}$
      $ = P\{X=0\} P\{Y=k\}+P\{X=1\} P\{Y=k-1\}+\cdots+P\{X=k\} P\{Y=0\}$
      $=p_0q_k+\cdots+p_kq_0$
    - $Z = \max\{X, Y\}$，则
      $\begin{aligned}P\{Z=k\}=& P\{\max \{X, Y\}=k\}=P\{X=k, Y=k\}+\cdots +P\{X=k, Y=0\}\\ &+P\{X=k-1, Y=k\}+P\{X=k-2, Y=k\}+\cdots +P\{X=0, Y=k\} \\=& p_{k} q_{k}+p_{k} q_{k+1}+\cdots+p_{k} q_{l}+p_{k+1} q_{k}+p_{k+2} q_{k}+\cdots+p_{l} q_{k}, \quad k= 0,1,2, \cdots, l \end{aligned}$
    - $Z = \min\{X, Y\}$且$0\le X,Y \le l$，则
      $\begin{aligned}P\{Z=k\}=& P\{X=k, Y=k\}+P\{X=k, Y=k+1\}+\cdots+P\{X=k, Y=l\}+\\ & P\{X=k+1, Y=k\}+P\{X=k+2, Y=k\}+\cdots+P\{X=l, Y=k\} \\=& p_{k} q_{k}+p_{k} q_{k+1}+\cdots+p_{k} q_{l}+p_{k+1} q_{k}+p_{k+2} q_{k}+\cdots+p_{l} q_{k}, \quad k= 0,1,2, \cdots, l \end{aligned}$
  - 最值函数法
    - $Z = \max\{X_1, X_2, \cdots, X_n\}$，则$P(Z = k) = P(Z \le k) - P(Z \le k-1)$，其意义是最大值小于等于$k$的概率减去最大值小于等于$k-1$的概率，这样最大值只能是$k$ <1000题 概率177>
- (连, 连) $\rightarrow$ (连)
  - 分布函数法：若$(X, Y) \sim f(x, y), Z=g(X, Y)$，则
    - $\displaystyle F_{z}(z)=P\{g(X, Y) \leqslant z\}$
    - 求$z$的定义域
    - 解出$F_{z}(z)$
      - $\displaystyle \iint\limits_{g(x, y) \leqslant z} f(x, y) d x d y$
      - 全集分解（适用于带绝对值的）<1000题 概率79 >
    - $f_Z(z) = F_Z^{\prime}(z)$
  - 卷积公式法
    - $Z = X + Y$且$X, Y$独立 <1000题 概率74, 概率75>
      - $\displaystyle f_{z}(z)=\int_{-\infty}^{+\infty} f(x, z-x) d x = \int_{-\infty}^{+\infty} f_{X}(x) f_{Y}(z-x) d x$
      - $\displaystyle f_{z}(z)=\int_{-\infty}^{+\infty} f(z-y, y) d y = \int_{-\infty}^{+\infty} f_{X}(z-y) f_{Y}(y) d y$
      - 证明详见《张宇强化21三、04求函数分布02（多维随机变量）》00:13:01
    - $Z = X - Y$且$X, Y$独立
      - $\displaystyle f_{z}(z)=\int_{-\infty}^{+\infty} f(x, x-z) d x = \int_{-\infty}^{+\infty} f_{X}(x) f_{Y}(x-z) d x$
      - $\displaystyle f_{z}(z)=\int_{-\infty}^{+\infty} f(y+z, y) d y = \int_{-\infty}^{+\infty} f_{X}(y+z) f_{Y}(y) d y$
    - $Z=XY$且$X, Y$独立
      - $\displaystyle f_{z}(z)=\int_{-\infty}^{+\infty} \frac{1}{|x|} f\left(x, \frac{z}{x}\right) d x = \int_{-\infty}^{+\infty} \frac{1}{|x|} f_X\left(x\right)f_Y\left(\frac{z}{x}\right) d x$
      - $\displaystyle f_{z}(z)=\int_{-\infty}^{+\infty} \frac{1}{|y|} f\left(\frac{z}{y}, y\right) d x = \int_{-\infty}^{+\infty} \frac{1}{|y|} f_X\left(\frac{z}{y}\right)f_Y\left(y\right) d x$
    - $Z=\frac{X}{Y}$且$X, Y$独立，这里一定可以确定$Y\ne0$
      - $\displaystyle f_{z}(z)=\int_{-\infty}^{+\infty} |y| f\left(yz, y\right) d x = \int_{-\infty}^{+\infty} |y| f_X\left(yz\right)f_Y\left(y\right) d x$
  - 最值函数法
    - max分布，即$Z = \max\{X, Y\}$
      - $F_{\max}(z) = F(\max\{X, Y\} \le z) = F(X \le z, Y \le z) = F(z, z)$
      - 若$XY$独立，则$F_{\max}(z) = F_X(z)F_Y(z)$
      - 拓展到n个随机变量，则$F_{\max}(z) = F_{X_1}(z)F_{X_2}(z) \cdots F_{X_n}(z)$
      - 若n个变量iid，则
        - $F_{\max}(z) = [F(z)]^n$ <1000题 概率171>
        - $f_{\max}(z) = n[F(z)]^{n-1}f(z)$
    - min分布，则$Z = \min\{X, Y\}$
      - $F_{\min}(z) = F(\min\{X, Y\} \le z) = F(\{X \le z\} \cup \{Y \le z\}) = F_X(z) + F_Y(z) - F(z, z)$
      - 若$XY$独立，则$F_{\min}(z) = F_X(z) + F_Y(z) - F_X(z)F_Y(z) = 1 - [1 - F_X(z)][1 - F_Y(z)]$
      - 拓展到n个随机变量，则$F_{\min}(z) = 1 - [1 - F_{X_1}(z)][1 - F_{X_2}(z)]\cdots[1 - F_{X_n}(z)]$
      - 若n个变量iid，则
        - $F_{\min}(z) = 1 - [1 - F(z)]^n$
        - $f_{\min}(z) = n[1 - F(z)]^{n-1}f(z)$
- (连, 离) $\rightarrow$ (连)
  - 若$XY$相互独立，则利用全集分解思想分解 <1000题 概率60m, 概率83>
  - 若$XY$不独立，则用分布函数法

多维 $\rightarrow$ 多维

- (离, 离) $\rightarrow$ (离, 离)：$(X, Y)\sim p_{ij}$，$U=g(X, Y), V=h(X, Y) \Rightarrow (U, V)\sim q_{ij}$ <1000题 概率59>
  - 主要是找到U, V全部可能的取值然后画表

# 数字特征

## E(X)

> 已知概率密度或概率分布的时候用公式法，当其未知是尽量考虑公式法等。

X

- 离散型$X \sim p_{i} \Rightarrow E X=\sum\limits_{i} x_{i} p_{i}$
- 连续型$\displaystyle X \sim f(x) \Rightarrow E X=\int_{-\infty}^{+\infty} x f(x) \mathrm{d} x$

g(X)，这里只是X变为g(X)，但是g(X)对应的概率$p_i$没有变

- $X \sim p_{i}, Y=g(X) \Rightarrow E Y=\sum\limits_{i} g\left(x_{i}\right) p_{i}$
- $\displaystyle X \sim f(x), Y=g(X) \Rightarrow E Y=\int_{-\infty}^{+\infty} g(x) f(x) \mathrm{d} x$

g(X, Y)，同上

- $(X, Y) \sim p_{i j}, Z=g(X, Y) \Rightarrow E Z=\sum\limits_{i} \sum\limits_{j} g\left(x_{i}, y_{j}\right) p_{i j}$
- $\displaystyle (X, Y) \sim f(x, y), Z=g(X, Y) \Rightarrow E Z=\int_{-\infty}^{+\infty} \int_{-\infty}^{+\infty} g(x, y) f(x, y) d x d y$

最值，若$X_i$<u>独立同分布</u>于$F(x)$，其概率密度为$f(x)$，记$Y=\min\{X_1, X_2, \cdots, X_n\}, Z=\max\{X_1, X_2, \cdots, X_n\}$

- $\displaystyle F_Y(y) = 1-[1-F(y)]^{n}, f_Y(y) = n[1-F(y)]^{n-1}f(y)\Rightarrow E Y=\int_{-\infty}^{+\infty} y f_{Y}(y) \mathrm{d} y$
- $\displaystyle F_{Z}(z)=[F(z)]^{n}, f_{Z}(z)=n[F(z)]^{n-1} f(z) \Rightarrow E Z=\int_{-\infty}^{+\infty} z f_{Z}(z) \mathrm{d} z$

分解

- 若$X=X_{1}+X_{2}+\cdots+X_{n}$，则$E X=E X_{1}+E X_{2}+\cdots+E X_{n}$

性质

- $E a=a, E(E X)=E X$
- $E(a X+b Y)=a E X+b E Y, E\left(\sum\limits_{i=1}^{n} a_{i} X_{i}\right)=\sum\limits_{i=1}^{n} a_{i} E X_{i}$
- 若$XY$相互独立，则$E(X Y)=E X E Y$

## D(X)

定义

- $DX = E[(X - EX)^2]$

定义法

- $X \sim p_{i} \Rightarrow D X=E\left[(X-E X)^{2}\right]=\sum\limits_{i}\left(x_{i}-E X\right)^{2} p_{i}$
- $\displaystyle X \sim f(x) \Rightarrow D X=E\left[(X-E X)^{2}\right]=\int_{-\infty}^{+\infty}(x-E X)^{2} f(x) \mathrm{d} x$

公式法

- $D X=E\left(X^{2}\right)-(E X)^{2}$
  - 证明：$DX = E[(X - EX)^2] = E[X^2 - 2XEX + (EX)^2] = E[X^2]-2(EX)^2 + (EX)^2 =E\left(X^{2}\right)-(E X)^{2} $
  - 求$E(X^2)$，公式为$E(X^2) = DX + (EX)^2$

最值，条件同$EX$最值条件

- $\displaystyle E Y=\int_{-\infty}^{+\infty} y f_{Y}(y) \mathrm{d} y, E (Y^2)=\int_{-\infty}^{+\infty} y^2 f_{Y}(y) \mathrm{d} y \Rightarrow DY = E(Y^2) - (EY)^2$
- $\displaystyle E Z=\int_{-\infty}^{+\infty} z f_{Z}(z) \mathrm{d} z, E (Z^2)=\int_{-\infty}^{+\infty} z^2 f_{Z}(z) \mathrm{d} z\Rightarrow DZ = E(Z^2) - (EZ)^2$

统计量法

- 在有正态分布出现的时候，可以考虑借助$\chi^2$分布等手段 <1000题 概率174>

分解

- 若$X=X_{1}+X_{2}+\cdots+X_{n}$，则$D X=D X_{1}+D X_{2}+\cdots+D X_{n}+2 \sum\limits_{1 \leqslant i<j \leqslant n} \operatorname{Cov}\left(X_{i}, X_{j}\right)$
- 若$X_i(i = 1, 2, \cdots, n)$相互独立，则$D X=D X_{1}+D X_{2}+\cdots+D X_{n}$

性质

- $DX \ge 0$
  - $E(X^2) \ge (EX)^2$
    - 证明：$E(X^2) = DX + (EX)^2 \ge (EX)^2$
- $Dc = 0$，这里的c为常数
  - 理解：常数无波动
  - $DX = 0$可以理解为X几乎处处为某个常数a
- $D(a X+b)=a^{2} D X$
- $D(X \pm Y)=D X+D Y \pm 2 \operatorname{Cov}(X, Y)$
  - 这里一定注意，若XY相互独立，则$D(X-Y) = DX + DY$
- 若XY相互独立，则
  - $D(a X+b Y)=a^{2} D X+b^{2} D Y$
  - $D(X Y)=D X \cdot D Y+D X(E Y)^{2} + D Y(E X)^{2} \ge DX\cdot D Y$
    - 证明：
      - XY相互独立，则$X^2Y^2$也相互独立
      - $E(XY)=EXEY$
      - $E(X^2Y^2)=E(X^2)E(Y^2)$
      - $D(XY) = E(X^2Y^2) - [E(XY)]^2 = E(X^2)E(Y^2) - (EX)^2(EY)^2$
        $= \left[D X+(E X)^{2}\right]\left[D Y+(E Y)^{2}\right] - (EX)^2(EY)^2 $
        $= D X \cdot D Y+D X(E Y)^{2} + D Y(E X)^{2}$
- 对于任意常数c，有$DX = E[(X-EX)^2] \le E[(X-c)^2]$ <1000题 概率117>
  - 证明：式子展开把c看做自变量，然后求最值点即可得到在$c=EX$点取得最小值

## Cov(X, Y)

意义

- $Cov(X, Y)>0$时，$X, Y$正相关，即两者有同时增加或者减少的倾向
- $Cov(X, Y)<0$时，$X, Y$负相关，即两者有反向增加或者减少的倾向
- $Cov(X, Y)=0$时，$X, Y$不相关

定义

- $Cov(X, Y) = E[(X - EX)(Y - EY)]$

定义法

- $\sum\limits_{i}\sum\limits_{j}(x_i - EX)(y_i - EY) p_{ij}$
- $\displaystyle \int^{+\infty}_{-\infty} \int^{+\infty}_{-\infty} (x - EX)(y - EY) f(x, y) dxdy$

公式法

- $Cov(X, Y) = E(XY) - EXEY$

性质

- $Cov(X, Y) = Cov(Y, X)$
- $Cov(aX, bY) = abCov(X, Y)$
- $Cov(X+Y,Z) = Cov(X, Z) + Cov(Y, Z)$

与独立的关系

- 独立必不相关
  - 证明：$Cov(X, Y) = E(XY) - EXEY = 0$
  - 逆否命题：相关必不独立
- 不相关不一定独立
  - 协方差只能决定是否有正、负相关性（线性相关性），但是除此之外还有可能有别的相关性（非线性相关），因此不能靠不相关判定是否独立，如下图所示![image-20190814101103089](http://res.niuxuewei.com/2019-08-14-021104.png)

## ρ

意义

- $\rho > 0$：正相关，且$\rho = 1$时，称为完全正相关
- $\rho < 0$：负相关，且$\rho = -1$时，称为完全负相关
- $\rho = 0$：不相关

定义

- $\displaystyle \rho_{XY} = \frac{Cov(X, Y)}{\sqrt{DX}\sqrt{DY}}$

性质

- $|\rho_{XY}| \le 1$
- $\rho_{XY} = 1 \Leftrightarrow P\{Y = aX + b\} = 1(a>0)$
- $\rho_{XY} = -1 \Leftrightarrow P\{Y = aX + b\} = 1(a<0)$
- 五个充要条件
  - $\rho_{XY} = 0$
  - $Cov(X, Y) = 0$
  - $E(XY) = EX\cdot EY$
  - $D(X+Y) = DX + DY$
  - $D(X-Y) = DX + DY$
- $X, Y$独立 $\Rightarrow \rho_{XY} = 0$
- 若$(X, Y) \sim N$，则$X, Y$独立  $\Leftrightarrow \rho_{XY} = 0$

## 独立性与相关性判别

套路

- 判别$Cov(X, Y) = E(XY) - EX\cdot EY$
  - 如果$Cov(X, Y) \neq 0$，则可以推出X, Y相关，则必不独立
  - 如果$Cov(X, Y) = 0$，只能说明不相关，但是是否独立需要做进一步判别
    - 分布判别
      - $F(x, y) = F_X(x) \cdot F_Y(y)$
      - $f(x, y) = f_X(x) \cdot f_Y(y)$
      - $P\{X = x_i, Y = y_i\} = P\{X = x_i\} \cdot P\{Y = y_i\}$
    - 反证法
    - 如果$(X, Y) \sim N$，则不相关$\Leftrightarrow$ 独立
    - X, Y服从0-1分布，则不相关$\Leftrightarrow$ 独立

## 切比雪夫不等式

定义：$\forall x > 0$，$\displaystyle P\{|X - EX| \ge \varepsilon \} \le \frac{DX}{\varepsilon^2}$或$\displaystyle P\{|X-E X|<\varepsilon\} \geqslant 1-\frac{D X}{\varepsilon^{2}}$

- 解释：指X距离均值的距离大于$\varepsilon$的概率应该小于$\displaystyle DX \over \varepsilon^2$

# 大数定律与中心极限定理

## 依概率收敛

- 设随机变量$X$与随机变量序列$\{X_n\}$，对于$\forall \varepsilon > 0$，有$\lim \limits_{n \rightarrow \infty} P\left\{\left|X_{n}-X\right|<\varepsilon\right\}=1$，则称随机变量序列$\{X_n\}$依概率收敛于随机变量$X$，记为$X_{n} \stackrel{P}{\longrightarrow} X(n \rightarrow \infty)$ <1000题 概率136>
  - 随机变量$X$可以被常数$a$代替
- 证明依概率收敛
  - 若给定$\{X_n\}$的概率密度或概率分布可以使用定义法，最后通过夹逼准则来求 <1000题 概率136, 概率171>
  - 当给定$EX = X$（或$\displaystyle \lim_{n\rightarrow\infty} EX = X$）和$DX$时，考虑使用切比雪夫不等式，最后通过夹逼准则来求 <1000题 概率137, 概率179>
  - 大数定律

## 大数定律

- 都在讲一个问题，即$\displaystyle \frac{1}{n} \sum_{i=1}^{n} X_{i} \stackrel{P}{\longrightarrow} E\left(\frac{1}{n} \sum_{i=1}^{n} X_{i}\right)$，区别就是<u>条件不同</u>
  - $\displaystyle \frac{1}{n} \sum_{i=1}^{n} X_{i} = \overline{X}$讲的是频率，即实际的实验测试值，如抛硬币10次3次正面7次反面，不是理想化的数值
  - $\displaystyle E\left(\frac{1}{n} \sum_{i=1}^{n} X_{i}\right) = \mu$讲的是数学期望，是理想的值，如抛硬币正面的期望就是$\displaystyle {1\over2}$
  - 这个公式本质上反映的就是在测试数据量极大的情况下，频率会无限逼近于期望
- 条件不同
  - 切比雪夫大数定律的条件更一般，要求1️⃣$\{X_n\}$相互独立、2️⃣全部$D_i$有相同的上界
  - 辛钦大数定律限制稍多，要求1️⃣$\{X_n\}$相互独立、2️⃣同分布、3️⃣期望存在

## 中心极限定理

> 中心极限定理就是在符合条件的情况下将任意分布的随机变量转化为正态分布，甚至标准正态分布。

列维-林德伯格定理

- 条件
  - $X_i$独立同分布
  - $EX_i = \mu$存在，即$X_i$的期望存在
  - $DX_i = \sigma^2$存在，即$X_i$的方差存在
- 那么$\lim\limits_{n\rightarrow\infty} \sum\limits^n_{i=1}X_i \sim N(n\mu, n\sigma^2)$，可将其化为标准正态分布为$\displaystyle \lim\limits_{n\rightarrow\infty} \sum\limits^n_{i=1} \frac{X_i - n\mu}{\sqrt{n}\sigma} \sim N(0, 1)$
- $\displaystyle P\left\{a<\sum\limits_{i=1}^{n} X_{i}<b\right\} \approx \Phi\left(\frac{b-n \mu}{\sqrt{n} \sigma}\right)-\Phi\left(\frac{a-n \mu}{\sqrt{n} \sigma}\right)$

# 数理统计

> 概率论是从总体出发推测某事件发生的概率，而数理统计是概率论的逆向方式，通过部分（抽样样本）推测总体，这是因为在现实世界中很难抽取总体样本，比如统计学校学生身高总是有人要请假的，因此数理统计是一个通过简单随机抽取的样本来推测总体的学科。

## 统计量的数字特征及分布

样本具有随机性与确定性

- 随机性：比如说，从该大学的女生中抽取一位，但是具体抽出来哪一位是随机的。因此用大写字母$X_{i}, i=1,2, \cdots, n$表示，表示某一次从总体中随机抽取一个个体，这是一个随机变量。
- 确定性：而某一次抽取的具体女生又是确定的，因此用小写字母$x_{i}, i=1,2, \cdots, n$表示某一次样本的具体值，这是确定的

统计量

- 定义：完全由样本($X_i$)所决定的量叫作统计量
- 常用统计量
  - 样本均值 $\displaystyle \overline{X}=\frac{1}{n} \sum\limits_{i=1}^{n} X_{i}$
    - $E(\overline X) = E(X)$
    - $\displaystyle D(\overline X) = \frac{D(X)}{n}$
  - 样本方差 $\displaystyle S^{2}=\frac{1}{n-1} \sum_{i=1}^{n}\left(X_{i}-\overline{X}\right)^{2}=\frac{1}{n-1}\left(\sum_{i=1}^{n} X_{i}^{2}-n \overline{X}^{2}\right)$
    - $X_i$服从标准正态分布时，$D(S^2)$可以利用$\displaystyle \frac{(n-1)S^2}{\sigma^2} \sim \chi^2(n-1)$求出 <1000题 概率149>
    - 利用无偏性$E(S^2) = DX$ <1000题 概率156>

统计量的四大分布

- 正态分布
- $\chi^2$分布
  - 条件
    - 相互独立
    - 服从标准正态分布，即$X_i \sim N(0, 1)$
  - 定义：如果$\displaystyle X = \sum^n_{i=1}X_i^2$，则称$X$服从自由度为n的$\chi^2$分布
  - 性质
    - 若$X_1 \sim \chi^2(n_1), X_2 \sim \chi^2(n_2)$且$X_1, X_2$相互独立，则$X_1+X_2 \sim \chi^2(n_1 + n_2)$
    - 若$X \sim \chi^2(n)$，则$EX = n, DX = 2n$
- t分布
  - 条件
    - $X \sim N(0, 1)$且$Y \sim \chi^2(n)$
    - 相互独立
  - 定义：$\displaystyle t = \frac{X}{\sqrt{Y/n}}$服从自由度为n的t分布
    - 因为X是服从标准正态分布的，而Y是服从卡方分布的，从结构上来说Y是X的n项平方和，所以为了确保比值的公平和有意义，通常除以n并开根号，这样分母也就与标准正态分布同级了。
- F分布
  - 条件
    - $X \sim \chi^2(n_1)$且$Y \sim \chi^2(n_2)$
    - 相互独立
  - 定义：$\displaystyle F = \frac{X / n_1}{Y / n_2}$服从自由度为$(n_1, n_2)$的F分布
    - 同t分布，为了要保证比值的公平性，所以要各自除以各自的自由度
  - 性质 <1000题 概率148>
    - $\displaystyle \frac{1}{F} \sim F(n_2, n_1)$，相当于分子分母互换位置
    - $\displaystyle F_{1-\alpha}(n_1, n_2) = \frac{1}{F_\alpha(n_2, n_1)}$

单正态总体分布

- $\displaystyle \overline X \sim N(\mu, \frac{\sigma^2}{n})$
  - 证明：$X_i \sim N(\mu, \sigma^2)$，则$\displaystyle \sum^n_{i=1}X_i \sim N(n\mu, n\sigma^2)$，则$\displaystyle \overline X = \frac{1}{n} \sum^n_{i=1}X_i \sim N(\mu, \frac{\sigma^2}{n})$
  - 化为标准正态分布：$\displaystyle \frac{\overline X - \mu}{\sigma / \sqrt{n}} = \frac{\sqrt{n}(\overline X - \mu)}{\sigma} \sim N(0, 1)$
- $\displaystyle {1 \over {{\sigma ^2}}}\sum\limits_{i = 1}^n {{{({X_i} - \mu )}^2}} \sim \chi^2(n)$
  - 证明：因为$X_i \sim N(\mu, \sigma^2)$，所以$\displaystyle \frac{X_i - \mu}{\sigma} \sim N(0, 1)$，进而$\displaystyle \sum^n_{i=1}\frac{(X_i - \mu)^2}{\sigma^2} \sim \chi^2(n)$
- $\displaystyle \frac{1}{\sigma^2} \sum^n_{i=1}(X_i - \overline X)^2 = \frac{(n-1)S^2}{\sigma^2} \sim \chi^2(n-1)$
  - 证明过程略
  - 适用于$\mu$未知$\sigma$已知的情况，这里用$\overline X$代替
- $\displaystyle \frac{\overline X - \mu}{S / \sqrt{n}} \sim t(n-1)$
  - 证明：因为$\displaystyle \frac{\overline X - \mu}{\sigma / \sqrt{n}} \sim N(0, 1)$且$\displaystyle \frac{(n-1)S^2}{\sigma^2} \sim \chi^2(n-1)$，则根据t分布定义，$\displaystyle \frac{\frac{\overline X - \mu}{\sigma / \sqrt{n}}}{\sqrt{\frac{(n-1)S^2}{\sigma^2 / (n-1)}}} = \frac{\overline X - \mu}{S / \sqrt{n}} = \frac{\sqrt{n}(\overline X - \mu)}{S} \sim t(n-1)$
  - 适用于求$\overline X$分布过程中$\sigma$未知的情况，这里用$S$代替
- $\displaystyle \frac{(\overline X - \mu)^2}{S^2 / n} \sim F(1, n-1)$
  - 证明：因为$\displaystyle \frac{\overline X - \mu}{\sigma / \sqrt{n}} \sim N(0, 1)$，则$\displaystyle \left(\frac{\overline X - \mu}{\sigma / \sqrt{n}}\right)^2 \sim \chi^2(1)$，进而$\displaystyle \frac{\left(\frac{\overline X - \mu}{\sigma / \sqrt{n}}\right)^2}{\frac{(n-1)S^2}{\sigma^2}} = \frac{(\overline X - \mu)^2}{S^2 / n} = \frac{n(\overline X - \mu)^2}{S^2} \sim F(1, n-1)$ 

## 参数估计

参数估计是在已知分布的背景下求未知参数（参数通常是$\mu$或$\sigma^2$），如已知X服从泊松分布，但不知道参数$\lambda$，因此需要利用现有样本估计参数$\lambda$（在泊松分布下$\lambda = EX = \mu$）

另外$\displaystyle E\overline X = \frac{1}{n} \sum^n_{i=1}EX_i$，这个与$EX$无直接关系。

### 点估计

> 估计值与估计量在结构上是一样的，但是估计量需要小写$x$，如$x_i$，相反估计量需要大写，如$X_i$

矩估计

- 一个参数
  - 一阶矩：$\overline X = EX$
  - 二阶矩：$\displaystyle \frac{1}{n}\sum^n_{i=1}X_i^2 = E(X^2) $ <1000题 概率168(利用无穷级数解题)>
- 二个参数
  - 一阶矩+二阶矩

最大似然估计

- 最大似然函数
  - 离散型
    $\displaystyle L\left(x_{1}, x_{2}, \cdots, x_{n} ; \theta\right)=\prod_{i=1}^{n} f\left(x_{i} ; \theta\right) = P\left(X=X_{1}\right) P\left(X=X_{2}\right) \cdots P\left(X=X_{n}\right)$
    可以将$(X_1, \cdots, X_n)$看做一个联合概率分布，而实验与实验间都是<u>独立同分布</u>的，因此可以通过相乘求得联合概率分布。
    - 例如抛硬币每次抛10次，做了两次实验，一次得到6次正面，一次得到5次正面，在$p$不知道的情况下我们可以写出概率分布如下所示$\displaystyle P(X=6) P(X=5)=\left(\begin{array}{c}{10} \\ {6}\end{array}\right) p^{6}(1-p)^{4} \cdot\left(\begin{array}{c}{10} \\ {5}\end{array}\right) p^{5}(1-p)^{5}$这样就求出一个关于$p$的函数，求导后即可获得$p$的最大似然估计值
  - 连续型与离散型类似，只不过$P(X=x_i)$换为了$f(x_i)$，然后相乘即可，其最大似然函数为
    $\displaystyle L\left(x_{1}, x_{2}, \cdots, x_{n} ; \theta\right)=\prod_{i=1}^{n} f\left(x_{i} ; \theta\right) = f(x_1)f(x_2)\cdots f(x_n)$
- 取对数求导即可
  - 对于双参数问题，即$\mu, \sigma^2$均不知道的情况下，在取对数之前的步骤是完全一致的，但是求导改为求偏导（分别对$\mu$和$\sigma^2$求偏导），然后分别求出最大值即可 <1000题 概率161>
  - 不通过求导直接确定最大值 <1000题 概率177>

估计量优劣判定

- 一致性（相合性）：$\displaystyle \lim _{n \rightarrow \infty} P(|\hat{\theta}-\theta|<\epsilon)=1$ <1000题 概率171>
- 无偏性：在一致性的基础上，$E(\hat{\theta})=\theta $ <1000题 概率172>
  - 其实$E(\hat{\theta})$是一个与样本有直接关系的量（也就是掺杂着$X_i$的量），而$\theta$是被预测的量。这两个值相等意味着我的估计与原有式子理论上是一致的。比如$\displaystyle \frac{1}{n-1} \sum_{i=1}^{n}\left(X_{i}-\overline{X}\right)^{2}, \quad \frac{1}{n} \sum_{i=1}^{n}\left(X_{i}-\overline{X}\right)^{2}$都是方差一致估计量，但是前者更好，因为满足无偏性。
- 有效性：在无偏性的基础上，$D\hat{\theta}_{1} \le D\hat{\theta}_{2}$，即$\hat{\theta}_{1}$相对波动较小，因此更有效

### 区间估计

#### 原理

[推荐阅读[马同学的概率教程](https://www.matongxue.com/lessons/766)]“以点估点”的方法是不可取的，就以$\mu$与$\overline X$的关系而言，$\overline X$的结果很难等于$\mu$，也就是随便一次的样本均值很难等于总体均值，所以我们以每次$\overline X$为中心扩展一个区域，那么相对来说在这个区域上更容易包含$\mu$这个点，如下图所示：

<img src="http://res.niuxuewei.com/2019-08-21-022152.png" width="500"/>

置信区间为95%说明，有100个$\overline X$我可以很有把握的说有95个区域包含了$\mu$，那么这个区间长度应该如何定夺？其实很简单，在前面我们说过如果总体服从正态分布，则$\displaystyle \overline X \sim N(\mu, \frac{\sigma^2}{n})$，可以看到$\overline X$的期望与总体的期望一致（这是这个方法能够起效的核心），也就是可以利用$\overline X$的分布来确定区域。

<img src="http://res.niuxuewei.com/2019-08-21-023055.png" width="400"/>

如上图所示，紫色的区间即为$\overline X$的概率密度函数，绿色的点为实际$\overline X$的样本，紫色的阴影对应的宽度($\overline \mu - \underline \mu$)可以作为置信区间的宽度，这样我就有理由相信以$\overline \mu - \underline \mu$为宽度的区间就是我们要找的95%置信水平的置信区间 。

#### 结论

- $\sigma^2$已知，估$\mu$：利用$\displaystyle Z= \frac{\overline X - \mu}{\sigma / \sqrt n} \sim N(0, 1)$，那么我们要求出$\displaystyle P\left(-z_{\alpha / 2}<Z<z_{\alpha / 2}\right) = 1-\alpha$，最终移项后我们可以得到$\displaystyle P\left(\overline{X}-\frac{\sigma}{\sqrt{n}} z_{\alpha / 2}<\mu<\overline{X}+\frac{\sigma}{\sqrt{n}} z_{\alpha / 2}\right)=1-\alpha$，最终我们获得的区间为$\displaystyle \left(\overline{X} \pm \frac{\sigma}{\sqrt{n}} z_{\alpha / 2}\right)$

<img src="http://res.niuxuewei.com/2019-08-21-024029.png" width="500"/> 

- $\sigma^2$未知，估$\mu$：利用$\displaystyle T = \frac{\overline X - \mu}{S / \sqrt n} \sim t(n-1)$，那么通过与上面一样的移项后，可以获得的区间为$\displaystyle \left(\overline{X} \pm \frac{S}{\sqrt{n}} t_{\alpha / 2}(n-1)\right)$
<img src="http://res.niuxuewei.com/2019-08-21-024851.png" width="500"/>

## 假设检验

### 原理

[推荐阅读[马同学的概率教程](https://www.matongxue.com/lessons/733)]假设检验是需要先画出一个随机变量的概率分布，假设是正态分布，设$H_0: \mu \le \mu_0$（$\mu_0$是已知数），为了方便说明可以假设$\mu = \mu_0$，如下图（已经将其标准化）：

<img src="http://res.niuxuewei.com/2019-08-21-055010.png" width="500"/>

可以看到当样本取值在蓝色阴影区域的时候，这件事情的发生已经变成一个小概率事件了，因此就称为拒绝域，当一次实验的样本落入该区域时我们就可以拒绝$H_0$假设，而接受备择假设。但该拒绝域只拒绝了$\mu = \mu_0$，还有$\mu < \mu_0$需要检验，但是$\mu$减少之后整个分布左移动，$\mu = \mu_0$得到的拒绝域仍然成立，如下图所示。

<img src="http://res.niuxuewei.com/2019-08-21-060242.png" width="500"/>

不管怎么说拒绝域一直都是上方蓝色区域。

以上单边检测，双边检测与单边检测类似，只是$H_0: \mu = \mu_0$，他是在说这样一个事情，比如考试怎么证明一个人会不会，那肯定是看考试成绩，单边检测是说这个人考100分时可以拒绝原假设认为这个人学习很好，而双边检测则是说这个人考0分也是学习很好（需要完美避开全部正确答案），所以双边检测的拒绝域是分布在两边的，如下图所示。

<img src="http://res.niuxuewei.com/2019-08-21-060712.png" width="500"/>

假设检验与置信区间有着某种冥冥之间的关系：如果置信区间的置信水平为$1-\alpha$，而拒绝域的显著性水平为$\alpha$，则置信区间以外就是拒绝域。

![image-20190821141101671](http://res.niuxuewei.com/2019-08-21-061102.png)

### 正态总体下的假设检验

期望假设检验

- $\sigma^2$已知时
  - 单边检验，假设为$H_0: \mu \leq \mu_0, H_1: \mu > \mu_0$
    - 将$\displaystyle \overline X \sim N(\mu_0, \frac{\sigma^2}{n})$其转换为标准正态分布$\displaystyle Z=\frac{\overline{X}-\mu_{0}}{\sigma / \sqrt{n}} \sim N(0,1)$
    - 画出概率密度分布图，蓝色区域为拒绝域(Fig. 1)
    - 拒绝域为$Z > z_\alpha$，因此$\displaystyle \overline X > \mu_0 + \frac{\sigma}{\sqrt n}z_\alpha$
  - 单边检验，假设为$H_0: \mu \geq \mu_0, H_1: \mu < \mu_0$
    - 将$\displaystyle \overline X \sim N(\mu_0, \frac{\sigma^2}{n})$其转换为标准正态分布$\displaystyle Z=\frac{\overline{X}-\mu_{0}}{\sigma / \sqrt{n}} \sim N(0,1)$
    - 画出概率密度分布图，蓝色区域为拒绝域(与Fig. 1情况相反)
    - 拒绝域为$Z < -z_\alpha$，因此$\displaystyle \overline X < \mu_0 - \frac{\sigma}{\sqrt n}z_\alpha$
  - 双边检验，假设为$H_0: \mu = \mu_0, H_1: \mu \neq \mu_0$
    - 将$\displaystyle \overline X \sim N(\mu_0, \frac{\sigma^2}{n})$其转换为标准正态分布$\displaystyle Z=\frac{\overline{X}-\mu_{0}}{\sigma / \sqrt{n}} \sim N(0,1)$
    - 画出概率密度分布图，蓝色区域为拒绝域(Fig. 2)
    - 拒绝域为$Z \leq -z_{\alpha / 2} \cup Z \geq z_{\alpha / 2}$，则$\displaystyle \overline X \leq \mu_0 - \frac{\sigma}{\sqrt n} z_{\alpha / 2} \cup \overline X \geq \mu_0 + \frac{\sigma}{\sqrt n} z_{\alpha / 2}$

<div style="text-align:center">
    <div style="float: left">
      <img src="http://res.niuxuewei.com/2019-08-21-063816.png" height="200">
      <br>
      <p style="text-align:center; width: 100%">Fig. 1</p>
    </div>
    <div style="float: left">
      <img src="http://res.niuxuewei.com/2019-08-21-063458.png" height="200">
      <br>
      <p style="text-align:center; width: 100%">Fig. 2</p>
    </div>
    <div style="clear:both"></div>
</div>

- $\sigma^2$未知时
  - 单边检验，假设为$H_0: \mu \leq \mu_0, H_1: \mu > \mu_0$
    - 将$\displaystyle \overline X \sim N(\mu_0, \frac{\sigma^2}{n})$其转换为$t(n-1)$分布$\displaystyle T = \frac{\overline X - \mu_0}{S / \sqrt n}$
    - 画出概率密度分布图，蓝色区域为拒绝域(Fig. 3)
    - 拒绝域为$T \geq t_{\alpha}(n-1)$，则$\displaystyle \overline X \geq \mu_0 + \frac{S}{\sqrt n} t_{\alpha}(n-1)$
  - 单边检验，假设为$H_0: \mu \geq \mu_0, H_1: \mu < \mu_0$
    - 将$\displaystyle \overline X \sim N(\mu_0, \frac{\sigma^2}{n})$其转换为$t(n-1)$分布$\displaystyle T = \frac{\overline X - \mu_0}{S / \sqrt n}$
    - 画出概率密度分布图，蓝色区域为拒绝域(与Fig. 3情况相反)
    - 拒绝域为$T \leq -t_{\alpha}(n-1)$，则$\displaystyle \overline X \leq \mu_0 - \frac{S}{\sqrt n} t_{\alpha}(n-1)$
  - 双边检验，假设为$H_0: \mu = \mu_0, H_1: \mu \neq \mu_0$
    - 将$\displaystyle \overline X \sim N(\mu_0, \frac{\sigma^2}{n})$其转换为$t(n-1)$分布$\displaystyle T = \frac{\overline X - \mu_0}{S / \sqrt n}$
    - 画出概率密度分布图，蓝色区域为拒绝域(Fig. 4)
    - 拒绝域为$T \leq -t_{\alpha / 2}(n-1) \cup T \geq -t_{\alpha / 2}(n-1)$，则$\displaystyle \overline X \leq \mu_0 - \frac{S}{\sqrt n}t_{\alpha / 2}(n-1) \cup \overline X \geq \mu_0 + \frac{S}{\sqrt n}t_{\alpha / 2}(n-1)$

<div style="text-align:center">
    <div style="float: left">
      <img src="http://res.niuxuewei.com/2019-08-21-064225.png" height="200">
      <br>
      <p style="text-align:center; width: 100%">Fig. 3</p>
    </div>
    <div style="float: left">
      <img src="http://res.niuxuewei.com/2019-08-21-064427.png" height="200">
      <br>
      <p style="text-align:center; width: 100%">Fig. 4</p>
    </div>
    <div style="clear:both"></div>
</div>