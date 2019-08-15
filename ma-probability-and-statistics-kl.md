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
  - $\int_{-\infty}^{+\infty}f(x)dx=1$
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
        - $F_{\max}(z) = [F(z)]^n$
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

定义：$\forall x > 0$，$\displaystyle P\{|X - EX| \ge \varepsilon \} \le \frac{DX}{\varepsilon^2}$

- 解释：指X距离均值的距离大于$\varepsilon$的概率应该小于$\displaystyle DX \over \varepsilon^2$

# 抽样分布

单正态总体分布 *(p161)*

- $\bar X$

- ${ {\sqrt n \left( {\overline X  - \mu } \right)} \over \sigma }$
- ${{\sqrt n \left( {\bar X - \mu } \right)} \over S}$
- ${n(\bar X-\mu)^2 \over S^2}$
- ${1 \over {{\sigma ^2}}}\sum\limits_{i = 1}^n {{{({X_i} - \bar X)}^2}} $
- ${1 \over {{\sigma ^2}}}\sum\limits_{i = 1}^n {{{({X_i} - \mu )}^2}} $