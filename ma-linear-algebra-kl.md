# 基础知识

## 单位矩阵

- ${E}={E}^T$
- $|{E}|=1$
- 提公因式${A}-{AX}={A}({E}-{X})$
- $E^n=E$ <1000 线代19>

## 转置

- ${A}$和${B}$是$n$阶矩阵，${A}^T\pm{B}^T = ({A}\pm{B})^T $<1000题 线代15, 线代76>
- 假设$\alpha$和$\beta$都是<u>列向量</u>，$\alpha\beta^T$、$\beta\alpha^T$、$\alpha\alpha^T$都是矩阵（T在后面），$\alpha^T\beta$、$\beta^T\alpha$、$\alpha^T\alpha$都是数（T在前面）

# 行列式

## 求行列式

数值型

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

抽象型

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
- 矩阵的性质，适用于矩阵的每一列与$\alpha_1, \alpha_2,  \cdots, \alpha_n$有关，则可分解为$(\alpha_1, \alpha_2, \cdots, \alpha_n){C}$，其中${C}$是一个$n\times n$的矩阵 <1000题 线代13>
- 相似矩阵的行列式相同，即$P^{-1}AP=B\Rightarrow |A|=|B|$ <1000题 线代88>

## 代数余子式

- 对于具体型行列式，求代数余子式之和要想到求$A^*$，然后把$A^*$所有项求和即可。 <1000题 线代53>
- $tr(A^*)=A_{11}+A_{22}+\cdots+A_{nn}=\lambda_2\lambda_3\cdots\lambda_n+\lambda_1\lambda_3\cdots\lambda_n+\cdots+\lambda1\lambda_2\cdots\lambda_{n-1}$ [参见 `相似理论 > A的特征值和特征向量 > 特征值 `]

# 矩阵

## 基本运算

- 数乘 <1000题 线代21>
  $k A=A k=k\left[\begin{array}{cccc}{a_{11}} & {a_{12}} & {\cdots} & {a_{1 n}} \\ {a_{21}} & {a_{22}} & {\cdots} & {a_{2 n}} \\ {\vdots} & {\vdots} & {} & {\vdots} \\ {a_{m 1}} & {a_{m 2}} & {\cdots} & {a_{m n}}\end{array}\right]=\left[\begin{array}{cccc}{k a_{11}} & {k a_{12}} & {\cdots} & {k a_{1 n}} \\ {k a_{21}} & {k a_{22}} & {\cdots} & {k a_{2 n}} \\ {\vdots} & {\vdots} & {} & {\vdots} \\ {k a_{m 1}} & {k a_{m 2}} & {\cdots} & {k a_{m n}}\end{array}\right]$

## 求方阵的高阶幂（$A^n$）

- $r(A) = 1$型，若${A}={\alpha}{\beta}^T$，其中${\alpha}$和${\beta}$是n维非零<u>列向量</u>，则${A}^n = l^{n-1}{A}$，其中$l=\alpha^T\beta=\sum\limits_{i=1}^n a_{ii}$（迹） <1000题 线代34>
- 用归纳法，先求出$A^2, A^3, \cdots$，然后找规律 <1000题 线代27>
  - $ A^{2}=k A\Rightarrow A^{n}=k^{n-1} A$
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
- 若$A\sim\Lambda$，则$A^n = P^{-1}\Lambda^nP$

## 伴随、逆与初等阵

接下来的全部内容的矩阵必是方阵

### 伴随矩阵

定义

-  $A^{*}=\left[\begin{array}{cccc}{A_{11}} & {A_{21}} & {\cdots} & {A_{n 1}} \\ {A_{12}} & {A_{22}} & {\cdots} & {A_{n 2}} \\ {\vdots} & {\vdots} & {} & {\vdots} \\ {A_{1 n}} & {A_{2 n}} & {\cdots} & {A_{m}}\end{array}\right]$
-  ${A A}^{*}={A}^{*} {A}=|{A}|{E}$

公式

- ${A A}^{*}={A}^{*} {A}=|{A}|{E}$
- $\left|A^{*}\right|=|A|^{n-1}$ <1000题 线代50, 线代71>
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

秩 [参见 `矩阵 > 秩 > 公式`]

解题思路

- 若$a_{ij}=A_{ij}$，那么$A^T=A^*$ <1000题 线代29>
  - $|A|=1$
  - 矩阵$A$可逆且正交

### 可逆矩阵

定义

- $AB=E\Rightarrow A=B^{-1}$ <1000题 线代19, 线代21, 线代62, 线代64, 线代66（玩出花了）, 线代68>
- 等价说法：非奇异矩阵 = 可逆矩阵

性质

- $\left(A^{-1}\right)^{-1}=A$
- $(k A)^{-1}=\frac{1}{k} A^{-1}$
- $(A B)^{-1}=B^{-1} A^{-1}$
- $\left|A^{-1}\right|=|A|^{-1}$
- $\left(A^{T}\right)^{-1}=(A^{-1} )^{T}$

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

- 初等变换
  - 倍乘
  - 互换
  - 倍加
- 初等矩阵是由$E=\left(\begin{array}{ll}{1} & {0} & 0 \\ {0} & 1 & {0} \\ {0} & 0 & {1}\end{array}\right)$经过一次初等变换得到的矩阵
  - $E_i(k)$（倍乘初等阵），即第i行（列）乘k倍，如$E_2(k)=\left(\begin{array}{ll}{1} & {0} & 0 \\ {0} & k & {0} \\ {0} & 0 & {1}\end{array}\right)$
  - $E_{ij}$（互换初等阵），即互换第i行（列）与第j行（列），如$E_{12}=\left(\begin{array}{ll}{0} & {1} & 0 \\ {1} & 0 & {0} \\ {0} & 0 & {1}\end{array}\right)$
  - $E_{ij}(k)$（倍加初等阵），把第j行的k倍加到第i行，或者说把第i列的k倍加到第j列，如$E_{31}(k)=\left(\begin{array}{ll}{1} & {0} & 0 \\ {0} & 1 & {0} \\ {k} & 0 & {1}\end{array}\right)$

性质

- 行列式
  - $|E_{ij}|=-1$，是根据行列式互换行、列加负号的性质来的
  - $|E_i(k)|=k$
  - $|E_{ij}(k)|=1$
- 转置
  - $E_{ij}^T=E_{ij}$
  - $E_i(k)^T=E_i(k)$
  - $E_{ij}(k)^T=E_{ji}(k)$
- 逆 <1000题 线代58, 线代59>
  - $E_{ij}^{-1}=E_{ij}$
  - $E_i(k)^{-1}=E_i(\frac{1}{k})$
  - $E_{ij}(k)^{-1}=E_{ij}(-k)$
- 伴随，由公式$A^*=|A|A^{-1}$可以直接求出
  - $E_{ij}^*=-E_{ij}$
  - $E^*_i(k)=kE_i(\frac{1}{k})$
  - $E^*_{ij}(k)=E_{ij}(-k)$

左行右列定理

- 左行：如$E_{ij}A$就是将$A$做了第i行与第j行的交换
- 右列：如$AE_{31}(k)$就是将$A$的第三列乘k后加到第一列

应用

- 求$A^{-1}$ [参见`矩阵 > 伴随、逆与初等阵 > 可逆矩阵 > 求逆 > 具体型`]
- 研究$P_1^mAP_2^n=B$

## 矩阵方程

定义：求未知矩阵

化简

- 消公因式，如果C可逆，则$CA=CB$可以推出$A=B$
- 提公因式，$CA+CB=C(A+B)$
- 移项
- 常用公式
  - $A^*$的10大公式
  - $A^2-E=(A-E)(A+E)=(A+E)(A-E)$
  - $A^3-E=(A-E)(A^2+A+E)$
  - 穿脱原则
  - -1, *, T可以相互交换

求解

- 直接求逆
- 化方程组
- 待定元素法

## 秩

**定义**

- 矩阵中线性无关的向量个数
- 存在k阶子式（行列式）不为零，任意k+1阶子式（行列式）等于零
- 对于一个$n\times n$的矩阵，$r(A)=n$等价于$|A|\neq0$等价于矩阵A可逆

**公式**，在没有具体说明的时候，A是一个$m\times n$的矩阵，B是任意满足条件的矩阵

- $0\leq r(A) \leq \min\{m, n\}$，在不知道m和n的值的时候，$r(A)\leq m$和$r(A)\leq n$都是正确的
- $r(kA)=r(A)$
- 初等变换不改变秩的个数，若P和Q均为可逆矩阵，则$r(A)=r(PA)=r(AQ)=r(PAQ) ★
- 乘积的秩越乘越小$r(AB)\leq \min\{r(A), r(B)\}$，也即$r(AB)\leq r(A)$和$r(AB)\leq r(B)$都是正确的 ★
  - 推广：如果$r(AB)<r(A)$，则$B_{n\times n}$是不满秩矩阵，即$r(B)<n$。证明使用反证法，如果B是可逆矩阵（满秩），则$r(A)=r(AB)$。 ★★★
- $r(A+B)\leq r(A)+r(B)$ ★
- $r\left(\begin{array}{ll}{A} & {O} \\ {O} & {B}\end{array}\right)=r(A)+r(B)$
- $r(A)+r(B)\le r\left(\begin{array}{ll}{A} & {O} \\ {C} & {B}\end{array}\right)\le r(A)+r(B)+r(C)$
- $r(AB)\ge r(A)+r(B)-n$
  - 注：若$AB=O$，则$r(A)+r(B)\le n$ ★
- $r(A)=r({A^T})=r(A^TA)=r(AA^T)$ <1000题 线代134>
- 伴随的秩$r(A^*)$ （证明在9讲例题5.25） ★★★
  - $n, \quad r(A)=n$
  - $1,\quad r(A)=n-1$
  - $0,\quad r(A)<n-1$
- （二次型）设矩阵$A_{n\times n}$且$A^2=A$，则可以推出$r(A)+r(A-E)=n$或$r(A)+r(E-A)=n$ ★
- （相似理论）设矩阵$A_{n\times n}$且$A^2=E$，则可以推出$r(A+E)+r(A-E)=n$或$r(E+A)+r(E-A)=n$ ★
- （齐次方程组）设矩阵$A_{m\times n}$且$AX=O$可以推出$s=n-r(A)$，是<u>基础解析中所含向量的个数</u>等于<u>未知数个数</u>减去<u>秩</u> ★
- （相似对角化）若$A\sim \Lambda \Leftrightarrow n_i=n-r(\lambda_iE-A)$，其中$\lambda_i$是$n_i$的重根 ★
-  若$A\sim \Lambda \Rightarrow $$r(A)$等于非零特征值的个数 ★

**求秩**

- 化阶梯
- 用公式
- 定义法 <1000题 线代87>
- 对于抽象型矩阵可以利用初等变换（秩不变）化简后求 <1000题 线代96>

**结论**

- 任意矩阵A左乘列满秩或者右乘行满秩矩阵，不改变矩阵A的秩 <1000题 线代150>

## 等价、合同与相似

矩阵等价 [[ref](https://blog.csdn.net/abraham_li/article/details/50058123)]

- 定义：对同型矩阵A、B，存在可逆阵P和Q，使得$B=PAQ$
- 充要条件：A与B的秩相同 <1000题 线代228>

矩阵合同

- 定义：对同型方阵A、B，存在可逆阵P使得$B=P^{T} A P$

矩阵相似

- 定义：对同型方阵A、B，存在可逆阵P，使得$B=P^{-1} A P$

关系：等价（只有秩相同）–>合同（秩和正负惯性指数相同）–>相似（秩，正负惯性指数，特征值均相同）

# 线性方程组

## 具体型 ★

**解含参数的线性方程组**（参考马同学线性代数）

- 齐次线性方程组$AX=0$
  1. 利用初等行变换将其化为阶梯型矩阵（注意：这里不能进行列变换；爪型需要回归原始<闭关修炼 例2.3.1>）
  2. 求基础解系含向量的个数$s=n-r(A)$，其中基础解系为$\xi_{1}, \xi_{2}, \cdots, \xi_{s}$
  3. 利用基础解析线性无关的特性对其进行赋值
  4. 利用系数进行求解得到全部基础解系
  5. 通解为$k_{1} \xi_{1}+k_{2} \xi_{2}+\cdots+k_{s} \xi_{s}$
- 非齐次线性方程组$AX=\beta$
  1. 将$(A|\beta)$利用初等行变换化为阶梯型矩阵（注意：这里不能进行列变换）
  2. 求基础解系含向量的个数$s=n-r(A)$，其中基础解系为$
  3. 利用基础解析线性无关的特性对其进行赋值
  4. 利用系数进行求解得到全部基础解系
  5. 求一个非齐次特解$\eta=\left[\begin{array}{l} x & 0 & \cdots & 0  \end{array}\right]^T$
  6. 通解$k_{1} \xi_{1}+k_{2} \xi_{2}+\cdots+k_{s} \xi_{s}+\eta$
- 对**方形**（方程个数=未知数个数）的方程组（$AX=\beta$）可用克拉默法则求解，即 <1000题 线代137>
  - 若$|A|\ne 0 \Rightarrow AX=\beta$有唯一解$x_i = \frac{|A_i|}{|A|}$，其中$A_i$是吧矩阵A中的第i列换为$\beta$
  - 若$|A|= 0 \Rightarrow AX=\beta$有非唯一解
- 变体：含参的向量之间的关系

**公共解** <闭关修炼 2.3.5>

A的解部分是B的解，相似的B的解部分是A的解。

- 方程组${A}_{m \times n} {x}={0}$和${B}_{m \times n} {x}={0}$联立变为$\left[\begin{array}{l}{A} \\ {B}\end{array}\right] x=0$，对于非齐次方程组也是同理，本质是方程组的联立；
- 已知$A_{m \times n} x=0$的通解$k_{1} \xi_{1}+k_{2} \xi_{2}+\cdots+k_s\xi_s$，带入到${B}_{m \times n} {x}={0}$，求出$k_i(i=1, 2, \cdots, s)$，再代回$A_{m \times n} x=0$的通解，即公共解（仅齐次）；
- 已知$A_{m \times n} x=0$的基础解系$\xi_{1}, \xi_{2}, \cdots, \xi_{s}$和${B}_{m \times n} {x}={0}$的基础解系$\eta_1, \eta_2, \cdots, \eta_t$，则y公共解为$\gamma =  k_{1} \xi_{1}+k_{2} \xi_{2}+\cdots+k \xi_{s} - (l_{1} \boldsymbol{\eta}_{1}+l_{2} \boldsymbol{\eta}_{2}+\cdots+l_{t}\eta_t)=0$，即解$\xi_{1}+k_{2} \xi_{2}+\cdots+k \xi_{s}=l_{1} \boldsymbol{\eta}_{1}+l_{2} \boldsymbol{\eta}_{2}+\cdots+l_{t}\eta_t$，求出$k_i$或者$l_j$，即可求出公共解$\gamma$（仅齐次）。

**同解**

A的解完全是B的解，A可以被B线性表示

- 相互带入法，$AX=0$的解满足$BX=0$，同样的$BX=0$的解也满足$AX=0 $  <1000题 线代145>
  - A的非齐次式的特解代入B的非齐次式，如果有点求不出来，则再将A的齐次式通解的一个代入B的齐次式中
- $r(A)=r(B)$且单方满足（例如只需证明$AX=0$的解满足$BX=0$，而不需证明$BX=0$的解也满足$AX=0$，相反同理）
- ★$r(A)=r(B)=r\left(\begin{array}{l}{A} \\ {B}\end{array}\right)$

- 结论
  - $A^nX=0$与$A^{n+1}X=0$是同解 <1000题 线代148>
  - $AX=0$与$A^TAX=0$是同解 <1000题 线代149>

## 抽象型

解的判定

- 齐次方程组必有零解
- 列满秩、列不满秩解得个数
- 方程组是否有解
- 注：
  - $AX=0$只有非零解（或有无穷解），$AX=b$可能有解也可能无解
  - $AX=b$有唯一解，$AX=0$只有零解
  - $AX=b$有无穷解，$AX=0$也有无穷解
  - 若A行满秩，则$AX=b$一定有解

基础解系

- 是否是基础解系（三要素） <1000题 线代133>
  - 是解（基础解系的加减法不影响是不是解）
  - 线性无关（通过行列式判断）
  - $s=n-r(A)$
- 用基础解系表示解，反过来说就是基础解系是否可以线性表示解
  - 验证给定解是否是基础解系
  - 建立矩阵$B=\left(\begin{array}{l} \xi_1 & \xi_2 & \cdots & \xi_s & | & \alpha_1 & \alpha_2 & \cdots & \alpha_n  \end{array}\right)$并进行初等行变换
  - 看哪一个给定的解可以通过基础解系线性表示

解的结构 <1000题 线代112>

- 齐次线性方程组：$k_{1} \xi_{1}+k_{2} \xi_{2}+\cdots+k_{s} \xi_{s}$ 
- 非齐次线性方程组：$k_{1} \xi_{1}+k_{2} \xi_{2}+\cdots+k_{s} \xi_{s}+\eta$（齐次式通解+非齐次式特解）<闭关修炼 2.3.12>

解与系数的关系

对于齐次线性方程组，有解${\beta}=\left[b_{1}, b_{2}, \cdots, b_{n}\right]^{\mathrm{T}}$

- $a_{i 1} b_{1}+a_{i 2} b_{2}+\cdots+a_{i n} b_{n}=0$，也就是系数与解点乘为0
  - 角色互换，已知解反求系数，${{\beta}^{\mathrm{T}}\alpha}_{i}^{\mathrm{T}}=0  $ <闭关修炼 2.3.14>
  - $\alpha_i\perp\beta$  <闭关修炼 2.3.13>

用方程组讨论秩 <闭关修炼 2.3.15, **2.3.16**; 1000题 线代132>

- 对于任意$A_{m\times n}$可以推出$AX=0$与$A^TAX=0$是同解

## 方程组的几何意义

对于齐次线性方程组$\left\{\begin{array}{l}{a_{1} x+b_{1} y+c_{1} z=d_{1}} \\ {a_{2} x+b_{2} y+c_{2} z=d_{2}} \\ {a_{3} x+b_{3} y+c_{3} z=d_{3}}\end{array}\right.$，设${\alpha}_{1}=\left[\begin{array}{l}{a_{1}} \\ {a_{2}} \\ {a_{3}}\end{array}\right], {\alpha}_{2}=\left[\begin{array}{l}{b_{1}} \\ {b_{2}} \\ {b_{3}}\end{array}\right], {\alpha}_{3}=\left[\begin{array}{l}{c_{1}} \\ {c_{2}} \\ {c_{3}}\end{array}\right], {\alpha}_{4}=\left[\begin{array}{l}{d_{1}} \\ {d_{2}} \\ {d_{3}}\end{array}\right]$，系数矩阵的3个行向量为${\beta}_{1}=\left[a_{1}, b_{1}, c_{1}\right], {\beta}_{2}=\left[a_{2}, b_{2}, c_{2}\right], {\beta}_{3}=\left[a_{3}, b_{3}, c_{3}\right]$，增广矩阵的3个行向量为$\gamma_{1}=\left[a_{1}, b_{1}, c_{1}, d_{1}\right], \gamma_{2}=\left[a_{2}, b_{2}, c_{2}, d_{2}\right], \gamma_{3}=\left[a_{3}, b_{3}, c_{3}, d_{3}\right]$

- 情况1：$r(\alpha_1, \alpha_2, \alpha_3)=3$，显然有$r(\alpha_1, \alpha_2, \alpha_3, \alpha_4)=3$，这个时候方程组有唯一解，其几何意义为这三个向量不共线（图2-3-1）
- 情况2：$r\left({\alpha}_{1}, {\alpha}_{2}, {\alpha}_{3}\right)=2$，也即$r\left({\beta}, {\beta}_{2}, {\beta}_{3}\right)=2$
  - 情况2.1：$r\left({\alpha}_{1}, {\alpha}_{2}, {\alpha}_{3}, {\alpha}_{4}\right)=2$，方程有无穷多解（解是一条线）
    - $r\left(\gamma_{1}, \gamma_{2}, \gamma_{3}\right)=2$且$\gamma_{1}, \gamma_{2}, \gamma_{3}$中有两个是线性相关的，其几何意义为两个向量共线（对应的平面重合），一个不共线（图2-3-2）
    - $r\left(\gamma_{1}, \gamma_{2}, \gamma_{3}\right)=2$且$\gamma_{1}, \gamma_{2}, \gamma_{3}$互不共线（图2-3-3）
  
  - 情况2.2：$r\left({\alpha}_{1}, {\alpha}_{2}, {\alpha}_{3}, {\alpha}_{4}\right)=2$，方程无解
    - 情况2.2.1：$\beta_1, \beta_2, \beta_3$有两个共线（图2-3-4）
    - 情况2.2.2：$\beta_1, \beta_2, \beta_3$互不共线（图2-3-5）
- 情况3：$r\left({\alpha}_{1}, {\alpha}_{2}, {\alpha}_{3}\right)=1$，也即$r\left({\beta}, {\beta}_{2}, {\beta}_{3}\right)=1$
  - 情况3.1：$r\left({\alpha}_{1}, {\alpha}_{2}, {\alpha}_{3}, {\alpha}_{4}\right)=1$，那么有无穷多解（解是一个面），三个面重合（图2-3-6）
  - 情况3.2：$r\left({\alpha}_{1}, {\alpha}_{2}, {\alpha}_{3}, {\alpha}_{4}\right)=2$，此时方程组无解
    - 情况3.2.1：$\gamma_{1}, \gamma_{2}, \gamma_{3}$有两个向量线性相关（图2-3-7）
  - 情况3.2.2：$\gamma_{1}, \gamma_{2}, \gamma_{3}$任意两个线性无关（图2-3-8）

<img height="150" src="http://res.niuxuewei.com/2019-07-28-055433.png"/><img height="150" src="http://res.niuxuewei.com/2019-07-28-060536.png"/><img height="150" src="http://res.niuxuewei.com/2019-07-28-060920.png"/><img height="150" src="http://res.niuxuewei.com/2019-07-28-061120.png"/><img height="150" src="http://res.niuxuewei.com/2019-07-28-061309.png"/><img height="150" src="http://res.niuxuewei.com/2019-07-28-062605.png"/><img height="150" src="http://res.niuxuewei.com/2019-07-28-063531.png"/><img height="150" src="http://res.niuxuewei.com/2019-07-28-063647.png"/>

# 向量组

## 具体型

**$\beta$与$\alpha_1, \cdots, \alpha_n $ （非齐次方程组）**

- 建立方程组$\left[{\alpha}_{1}, {\alpha}_{2}, \cdots, {\alpha}_{n}\right]\left[\begin{array}{c}{x_{1}} \\ {x_{2}} \\ {\vdots} \\ {x_{n}}\end{array}\right]=\boldsymbol{\beta}$
- 解方程
- 结果
  - $r(A)<r(A|\beta)$说明向量组不能表示$\beta$（方程组无解）
  - $r(A)=r(A|\beta)=n$说明向量组可以唯一的表示$\beta$（方程组有唯一解）
  - $r(A)=r(A|\beta)<n$说明A有无穷多种表示方法（方程组无穷解）

**$\alpha_1, \cdots, \alpha_n $ （齐次方程组）**

- 线性无关与线性无关定义
  - 线性无关：仅在$k_1=k_2=\cdots=k_n=0$的情况下$k_1\alpha_1+\cdots+k_n\alpha_n=0$成立，则成为线性无关$\Leftrightarrow$$AX=0$只有零解
  - 线性相关：存在$k_i\neq0$的情况下似的$k_1\alpha_1+\cdots+k_n\alpha_n=0$成立，则该向量方程组线性相关$\Leftrightarrow$$AX=0$有非零解
- 向量个数(方程组的列数)与向量维度(方程组的行数)的关系
  - 向量个数>向量维度，则向量组必线性相关
  - 向量个数=向量维度（方形，可以用行列式）
    - 若$|\alpha_1  \cdots \alpha_n|= 0$，则线性相关
    - 若$|\alpha_1  \cdots \alpha_n|\neq 0$，则线性无关
  - 向量个数<向量维度，化台阶
- 若线性无关
  - 加任意分量仍然无关，假设$\alpha_1, \alpha_2, \alpha_3$线性无关，则$\left[\begin{array}{c} \alpha_1 \\ a \end{array}\right], \left[\begin{array}{c} \alpha_2 \\ b \end{array}\right], \left[\begin{array}{c} \alpha_3 \\ c \end{array}\right]$也是线性无关的
  - 减向量个数，如$\alpha_1, \alpha_2$也线性无关
- 若线性相关
  - 减任意分量仍然相关，如$\left[\begin{array}{c} 1 \\ 2 \end{array}\right], \left[\begin{array}{c} 2 \\ 4 \end{array}\right]$是线性相关的，则$\left[\begin{array}{c} 1 \end{array}\right], \left[\begin{array}{c} 2 \end{array}\right]$仍然是线性相关的
  - 加向量个数

**求极大线性无关组**

- 构造矩阵A
- 初等行变换化台阶
- 每个阶梯上随便选一个<u>列向量</u>即可

## 抽象型

已知某些向量关系，研究另一些向量

- 定义法证明线性无关

  - 步骤
    1. 写出$k_1\alpha_1+\cdots+k_n\alpha_n=0$
    2. 证明$k_1=k_2=\cdots=k_n=0$

  - 可以用的方法有
    - 左右两边同乘一个矩阵或者重组 <闭关修炼 2.4.7>
    - 转化为齐次方程组（$\left[{\alpha}_{1}, {\alpha}_{2}, \cdots, {\alpha}_{n}\right]X=0$，把$k_i$看做方程组的解）只有零解
    - 与特征值、基础解系和正定综合 <1000题 线代91(略), 线代92(略), 线代187>

- 用秩 <闭关修炼 2.4.9>

  - 新向量组是原向量组的线性组合 <1000题 线代86, 线代87>
  - 利用秩的公式 <1000题 线代90, 线代101>

## 向量组等价

- 定义：$\left\{{\alpha}_{1}, {\alpha}_{2}, \cdots, {\alpha}_{s}\right\}$与$\left\{{\beta}_{1}, {\beta}_{2}, \cdots, {\beta}_{t}\right\}$可以互相表出，与方程组同解一样的
- 判定方法
  - 三秩相同$r(\alpha)=r(\beta)=r(\alpha|\beta)$
  - $r(\alpha)=r(\beta)$且可单方表出
- 矩阵等价于向量组等价不一样：矩阵A等价于矩阵B，在$r(A)=r(B)$的条件下即可满足

## 向量空间

概念：${\alpha}=a_{1} {\xi}_{1}+a_{2} {\xi}_{2}+\cdots+a_{n} {\xi}_{n}$，其中$\xi_i$为基（方程组未知量），$a_i$为坐标（是非齐次方程组的唯一解，那么$\left[{\xi}_{1}, {\xi}_{2}, \cdots, {\xi}_{n}\right]$是满秩的，即都是线性无关的）。

过渡矩阵：$\left[{\eta}_{1}, {\eta}_{2}, \cdots, {\eta}_{n}\right]=\left[{\xi}_{1}, {\xi}_{2}, \cdots, \xi_{n}\right] {C}$，$C$称为$\xi_i$到$\eta_i$的过渡矩阵 <1000题 线代105>

- 注意C的位置是在$\left[{\xi}_{1}, {\xi}_{2}, \cdots, \xi_{n}\right] $的后面

坐标变换：${\alpha}=\left[{\xi}_{1}, {\xi}_{2}, \cdots, {\xi}_{n}\right] {x}=\left[{\eta}_{1}, {y}_{2}, \cdots, {y}_{n}\right] {y}\Leftrightarrow \left[{\xi}_{1}, {\xi}_{2}, \cdots, {\xi}_{n}\right] {x} = \left[{\xi}_{1}, {\xi}_{2}, \cdots, {\xi}_{n}\right] Cy$，则$x=Cy$叫坐标变换。

# 相似理论

这里的矩阵均为方阵

## 特征值和特征向量

定义：$A\xi=\lambda\xi(\xi\ne0)$，其中$\lambda$称为特征值，$\xi$称为特征向量

**特征值**

- $(\lambda E-A)\xi=0$有解，即$\lambda E-A$不满秩，即$|\lambda E-A|=0$
  - $\lambda_0$是特征值 $\Leftrightarrow$ $|\lambda_0 E-A|=0$
  - $\lambda_0$不是特征值 $\Leftrightarrow$ $|\lambda_0 E-A|\neq0$（矩阵可逆、满秩）
  - 拓展：$|aA+bE|=0$ $\Leftrightarrow$ $\lambda = -\frac{b}{a}$
- 特征值与行列式的关系：$|A|=\lambda_1\lambda_2\cdots\lambda_n$ <1000题 线代162>
- 特征值与迹的关系：$tr(A)=a_{11}+\cdots+a_{nn}=\lambda_1+\cdots+\lambda_n$
- 公式，假设矩阵A的特征值为$\lambda$，特征向量为$\xi$
  - $f(A)$的特征值为$f(\lambda)$，特征向量为$\xi$ ★
    - 具体情况1：$kA$的特征值为$k\lambda$
    - 具体情况2：$A^k$的特征值为$\lambda^k$
      - $A^k$的特征向量未必是$A$的特征向量 <1000题 线代171>
    - 特殊情况：$f(A)=O$则$f(\lambda)=0$
  - $A^{-1}$的特征值为$\frac{1}{\lambda}(\lambda\ne0)$，特征向量为$\xi $ <1000题 线代180> ★
    - 证明过程：$A\xi=\lambda\xi \Rightarrow A^{-1}A\xi = \lambda A^{-1}\xi \Rightarrow A^{-1}\xi=\frac{1}{\lambda}\xi$
  - $A^*$的特征值为$\frac{|A|}{\lambda}(\lambda\ne0)$，特征向量为$\xi$ ★★★
    - 证明过程：$A^*A\xi = \lambda A^*\xi  \Rightarrow |A|\xi = \lambda A^*\xi \Rightarrow A^*\xi = \frac{|A|}{\lambda}\xi$
    - $A^*$的特征向量未必是$A$的特征向量 <1000题 线代171>
  - $P^{-1}AP$的特征值为$\lambda$，特征向量为$P^{-1}\xi$
    - 证明过程：$(P^{-1}AP)(P^{-1}\xi) = \lambda (P^{-1}\xi)$
  - $A$与$A^T$的特征值相同，特征向量完全不同，需要另行计算
    - 证明特征值相同：$|\lambda E - A|=|(\lambda E - A)^T|（行列式性质）=|\lambda E-A^T| = 0$
- 伴随矩阵特征值与矩阵特征值的关系：设$\lambda_1, \lambda_2, \lambda_3$是矩阵A的特征值，则$\lambda_1^*=\frac{|A|}{\lambda_1}=\frac{\lambda_1\lambda_2\lambda_3}{\lambda_1}=\lambda_2\lambda_3$，同理可以得到$\lambda_2^*=\lambda_1\lambda_3$和$\lambda_3^*=\lambda_1\lambda_2$，即$A_{11}+A_{22}+A_{33}=\lambda_2\lambda_3+\lambda_1\lambda_3+\lambda_1\lambda_2$
- $A+E$的特征值为$\lambda_1+1, \cdots, \lambda_n+1$，其中$\lambda_i(i=1, \cdots, n)$为A的特征值 <1000题 线代162>
- $AB$与$BA$有相同的特征值（不是一样的特征值） <1000题 线代185>

**特征向量**

- 特征向量 $\Leftrightarrow$ $(\lambda_0E-A)X=0$的非零解
- 重要结论 ★★★
  - k重特征值($\lambda$)至多有k个无关的特征向量($\xi$)，比如求出3个特征值，最多三个无关的特征向量
  - $\xi_1 \rightarrow \lambda_1, \xi_2 \rightarrow \lambda_2$且$\lambda_1\ne\lambda_2$，可以推出$\xi_1$与$\xi_2$线性无关
    - 如果矩阵A是实对称矩阵，则$\xi_1$与$\xi_2$正交
  - $\xi_1 \rightarrow \lambda, \xi_2 \rightarrow \lambda$，在$k_1$与$k_2$不全为0的情况下，可以推出$k_1\xi_1+k_2\xi_2 \rightarrow \lambda$ ★
    - 例如，$\xi$是特征向量，则$-\xi$也是特征向量
  - $\xi_1 \rightarrow \lambda_1, \xi_2 \rightarrow \lambda_2$且$\lambda_1\ne\lambda_2$，在$k_1$与$k_2$不全为0的情况下，可以推出$k_1\xi_1+k_2\xi_2$不是任何特征值的特征向量 ★
- 遇到求$A^n\beta$，先将$\beta$用特征向量表示出来，然后再利用特征值性质$A^n$的特征值为$\lambda^n$求解 <1000题 线代193>
- $A=\alpha\beta^T$，即$r(A)=1$的矩阵，在$\alpha\ne0$和$\beta\ne0$的情况下，$\lambda_1=tr(A)$对应的特征向量为$\alpha$，其余的特征向量为$\left[\begin{array}{c}{b_2} \\ {-b_1} \\ 0 \\  {\vdots} \\ {0}\end{array}\right], \left[\begin{array}{c}{b_3} \\ {0} \\ -b_1 \\  {\vdots} \\ {0}\end{array}\right], \cdots, \left[\begin{array}{c}{b_n} \\ {0}\\  {\vdots} \\ {0} \\ -b_1 \end{array}\right]$ <1000题 线代205>

**特征值和特征向量综合**

- 已知$A\sim B$、B的具体型以及A的特征值和特征向量，反求A <1000题 线代191>
  - 利用已知构造$P$，然后利用$P^{-1}AP=B$反求A

**矩阵方程**

- $AB=0 \Rightarrow A[\beta_1, \beta_2, \cdots, \beta_n]=[0\beta_1, 0\beta_2, \cdots, 0\beta_n]$，所以每一个$\beta_i$均为特征值0对应的特征向量
- $AB=C; C = [\lambda_1\beta_1, \lambda_2\beta_2, \cdots, \lambda_n\beta_n] \Rightarrow A[\beta_1, \beta_2, \cdots, \beta_n] = [\lambda_1\beta_1, \lambda_2\beta_2, \cdots, \lambda_n\beta_n] $，所以$\beta_i$是A的属于$\lambda_i$的特征向量
- $AP=PB$且P可逆，则可以推出$P^{-1}AP=B$，则可以推出$A\sim B$，则$\lambda_A=\lambda_B $ ★
- 若A的每行元素之和为k，则$A\left[\begin{array}{c}{1} \\ {1} \\ {\vdots} \\ {1}\end{array}\right]=k\left[\begin{array}{c}{1} \\ {1} \\ {\vdots} \\ {1}\end{array}\right]$，即k是A的一个特征值

**秩**

- $r(A)=1$，则$\lambda_1= \cdots = \lambda_{n-1}=0$，$\lambda_n=tr(A)$，其特征向量全部线性无关，必定可以相似对角化，其证明如下
  - $A=\alpha\beta^T \Rightarrow A^2=\beta^T\alpha A = aA$，其中$a = tr(A)$，进一步化简为$A^2-aA=0$
  - 由特征值公式可知$A^2-aA=0$的特征值为$\lambda^2-a\lambda=0$，可以推出$\lambda=0$或$\lambda=a$
  - 又因为$tr(A)=\lambda_1+\cdots+\lambda_n$，所以$\lambda_1= \cdots = \lambda_{n-1}=0$，$\lambda_n=tr(A)$
  - 将特征值0带入特征值定义，即$(0E-A)X=0$，$0E-A$的秩为1，则基础解系的无关向量有$s=n-1$个，即$\xi_1, \cdots, \xi_{n-1}$都线性无关
  - 有因为$\lambda_n\ne\lambda_i(i=1, 2, \cdots, n-1)$，所以有特征向量的重要结论可知，特征向量全部线性无关
  - $P=[\xi_1, \xi_2, \cdots, \xi_n]$是线性无关的，也即P是可逆的，$P^{-1}AP=\Lambda$，即$A\sim\Lambda$

## 向量对角化 ★

### A与对角阵的相似($A\sim\Lambda$)

**充要条件**

- A有n个无关特征向量 $\Leftrightarrow$ $A\sim\Lambda$
  - 设$P=[\xi_1, \xi_2, \cdots, \xi_n]$，其中P的秩为n（$\xi_i$线性无关），则$P^{-1}AP=\Lambda$
- $n_i = n-r(\lambda_iE-A)$，其中$\lambda_i$是$n_i$的重根 $\Leftrightarrow$ $A\sim\Lambda$
  - 证明：根据特征向量的重要结论可知，特征值不同时特征向量必不同，但是反过来如果特征值（重根）相同，那么还需要进一步证明其对应的特征向量是否线性无关，证明的手法就是利用$(\lambda_iE-A)X=0$，如果基础解析的个数正好是相同特征值的个数，那么我们就有理由相信A有n个无关的特征向量，进而可以推出$A\sim\Lambda$ [参见 `相似理论 > 特征值和特征向量 > 秩 > 证明`]

**充分条件**

- A是实对称矩阵 $\Rightarrow$ $A\sim\Lambda$ <1000题 线代174>
- A有n个不同的特征值 $\Rightarrow$ $A\sim\Lambda$
  - 因为A有n个不同的特征值必可以推出A有n个无关特征向量
- $A^2=A$  $\Rightarrow$ $A\sim\Lambda$ <1000题 线代203>
- $A^2=E$  $\Rightarrow$ $A\sim\Lambda$
- $r(A)=1$且$tr(A)\neq0$  $\Rightarrow$ $A\sim\Lambda$

**必要条件**

- $A\sim\Lambda$ $\Rightarrow$ $r(A)$等于非零特征值个数

**否定条件**

- A的特征值全部为k且$A\neq kE$ $\Rightarrow$ $A\nsim \Lambda$
- $A\neq0, A^k=0$，其中k为大于1的整数 $\Rightarrow$ $A\nsim \Lambda$

### A与B的相似($A\sim B$)

定义：$P^{-1}AP=B$

**四个性质**

$A\sim B$的必要条件

- $|A| = |B|$
- $r(A)=r(B)$
- $tr(A)=tr(B)$
- $\lambda_A=\lambda_B$

可用于求参数、否定

**重要结论** <1000题 线代196> ★

- $A\sim B \Rightarrow A^T\sim B^T, A^{-1}\sim B^{-1}, A^*\sim B^*$
- $A\sim B \Rightarrow A^n\sim B^n, f(A)\sim f(B)$ <1000题 线代158>
  - 更特殊的：$A\sim \Lambda \Rightarrow A^n\sim \Lambda^n, f(A)\sim f(\Lambda)$ ★★★
- $A\sim B , B\sim\Lambda \Rightarrow A\sim\Lambda$
  - 根究定义可知$P^{-1}AP=B, Q^{-1}BQ=\Lambda$
  - 将$P^{-1}AP=B$带入$Q^{-1}BQ=\Lambda$可得$Q^{-1}P^{-1}APQ=\Lambda$，也即$(PQ)^{-1}APQ=\Lambda$
  - 令$C=PQ$，则$C^{-1}AC=\Lambda$
- $A\sim\Lambda, B\sim\Lambda \Rightarrow A\sim B$
  - 根究定义可知$P^{-1}AP=\Lambda, Q^{-1}BQ=\Lambda$
  - $P^{-1}AP = Q^{-1}BQ \Rightarrow QP^{-1}APQ^{-1}=B \Rightarrow (PQ^{-1})^{-1}A(PQ^{-1})=B$
  - 令$C=PQ^{-1}$，则$C^{-1}AC=B$

## 实对称矩阵与正交阵

**正交矩阵**

- 正交矩阵是指${A}^T{A}={E}$，其充要条件为
  - $ {A}^T={A}^{-1}$
  - A是由规范正交基组成，规范指的是单位向量，正交指的是任意向量两两垂直
  - $A^{-1}$也是正交矩阵
  - $A^*$也是正交矩阵
  - $A^T$也是正交矩阵
  - $-A$也是正交矩阵
  - 特征值全部为$1$或$-1$ <1000题 线代15, 线代16>
    - 证明：设A的特征值为$\lambda$，则$A^{-1}$的特征值为$\frac{1}{\lambda}$，又因为$A^T=A^{-1}$且$A$的特征值与$A^T$相同（特征向量不同），所以$\lambda=\frac{1}{\lambda}$，因此特征值全部为$1$或$-1$
- 若P和Q为同阶正交矩阵，则$PQ$也是正交矩阵，$P+Q$则不一定是
  - 所以问$P^{-1}Q$、$-P^*Q$是不是正交阵，要会识别

**实对称矩阵**

- 若$\lambda_1\ne\lambda_2$，则$\xi_1\perp\xi_2$ [参见 `相似理论 > 特征值和特征向量 > 特征向量`] <1000题 线代191>
- 若A为实对称矩阵，则必可以用一个正交矩阵P，使得$P^{-1}AP=\Lambda$

# 二次型

前提：矩阵A为实对称矩阵

实对称矩阵性质

- $A^TA=A^2$

## 配方法

**含平方项**

- 配方，假设会得到$f=(ax_1+bx_2+cx_3)^2+(dx_2+ex_3)^2$
- 换元，令$y_1=ax_1+bx_2+cx_3$，$y_2=dx_2+ex_3$
- 反解，求出$y_i\rightarrow x_i$的变换矩阵$C_1$
- 化为标准型
- 再次换元（以下步骤为求规范型，其特征是前面的系数要么为+1要么为-1）
- 反解，求出$z_i \rightarrow y_i$变换矩阵$C_2$
- 化为规范型，从普通的化为规范型的矩阵是$C=C_1C_2$

**不含平方项**

- 不含平方项要创造平方项，即可以通过平方差公式来进行 <闭关修炼 2.6.3>

**常用场合**

- 求正惯性指数p、负惯性指数q
  - 补充：正惯性指数指的是正系数的个数（也即正特征值的个数），负惯性指数指的是负系数的个数（也即负特征值的个数），另外$p+q=r(A)$，其意义是非零特征值的个数是该矩阵的秩 <1000题 线代226>
- 判断A的正定型
  - 补充：所谓的正定型是指矩阵的系数只能为正，不能为零或负数

**矩阵语言**

- 实对称矩阵A，必存在可逆矩阵C，使得$C^TAC=\Lambda$

## 正交变换法

**基本步骤**

对于$f=x^TAx$

- 求A的特征值$\lambda_1, \lambda_2, \cdots, \lambda_n$
- 求特征值对应的特征向量$\xi_1, \xi_2, \cdots, \xi_n$
- 将$\xi_1, \xi_2, \cdots, \xi_n$正交化、单位化为$\eta_1, \eta_2, \cdots, \eta_n$
  - 正交化使用施密特正交法：对于任给的$\alpha_1, \alpha_2$，则$\beta_1=\alpha_1$，则$\beta_2=\alpha_2-\frac{(\alpha_2, \beta_1)}{(\beta_1, \beta_1)}\beta_1$，其原理是将$\alpha_2$投影到$\beta_1$上去，然后用$\alpha_2-投影向量$，即可得到两个正交向量
  - 单位化
- 令$Q=(\eta_1, \eta_2, \cdots, \eta_n)$，可得$Q^{-1}AQ=Q^TAQ=\Lambda$
- 令$x=Qy$，则$f=x^TAx=(Qy)^TAx=y^T(Q^TAQ)y=y^T\Lambda y $ （化到这一步是标准型）
- 如果要求化为规范型，请参考`二次型 > 配方法 > 含平方项`

**考法**

- 对于方阵A，使其$P^TAP=\Lambda$，求$P $(前提是A是实对称矩阵)

- A通过P转到B，但是B不是标准型 <1000题 线代225>

- 反求参数

- 反求A

- 最值问题
  - 条件
    - 是二次型问题，设$f=x^TAx=y^TQ^TAQy$
    - A的特征值$\lambda_1\le\lambda_2\le\cdots\le\lambda_n$
  - 结论
    - $\lambda_1x^Tx \le x^Tx \le \lambda_nx^Tx$，这里$x^Tx=x_1^2+x_2^2+\cdots+x_n^2$
    - 若$x^Tx=1$，则$f_{max}=\lambda_n$，$f_{min}=\lambda_1$

- 几何应用

  | $\lambda_1, \lambda_2, \lambda_3$的符号 | $f(x_1, x_2, x_3)=1$ |
  | :-------------------------------------: | :------------------: |
  |                   3正                   |    椭球面（左1）     |
  |                 2正1负                  |  单叶双曲面（左2）   |
  |                 1正2负                  |  双叶双曲面（左3）   |
|                 2正1零                  |   椭圆柱面（右2）    |
  |                1正1负1零                |   双曲柱面（右1）    |

  <img height="150" src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d2/Ellipsoid_cut_by_plane.gif/440px-Ellipsoid_cut_by_plane.gif"/><img height="150" src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/7f/HyperboloidOfOneSheet.png/300px-HyperboloidOfOneSheet.png"/><img height="150" src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/91/HyperboloidOfTwoSheets.png/300px-HyperboloidOfTwoSheets.png"/><img height="150" src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e1/Cylinder_geometry.svg/324px-Cylinder_geometry.svg.png"/><img height="150" src="http://res.niuxuewei.com/2019-08-02-040048.png"/>

  注：
  
  - 这里$f(x_1, x_2, x_3)=2$也可以

## 实对称矩阵合同

- 前提：实对称矩阵
- A与B合同 $\Leftrightarrow$ 存在可逆矩阵C，使得$C^TAC=B$ $\Rightarrow$ $p_A=p_B, q_A=q_B$，即A正惯性指数等于B，A的负惯性指数等于B
- 与相似的联系：相似必合同，因为相似要求特征值要相同
- 考法：
  - 告知A和B，求C，使得$C^TAC=B$ <闭关修炼 2.6.15>
    - 结题技巧：利用二次型化为标准型，来求出C
  - A合同于B，B合同于C，则A合同于C
    - 证明方法：$P^TAP=B, Q^TBQ=C \Rightarrow (PQ)^TA(PQ)=C$

## 正定二次型

**前提**

- A是实对称矩阵，即$A=A^T$

**充要条件**

$f=x^TAx$正定

- $\Leftrightarrow$ $\forall x\ne0, f>0$
- $\Leftrightarrow$ $p=n$，即系数全整（p是正惯性指数）
- $\Leftrightarrow$ A的特征值全部大于0
- $\Leftrightarrow$ $A=D^TD$，其中D是一个可逆矩阵 <闭关修炼 2.6.20>
- $\Leftrightarrow$ A合同于E <闭关修炼 2.6.20>
- $\Leftrightarrow$ A的顺序主子式全部大于0 <闭关修炼 2.6.18>

**必要条件**

- $a_{ii}>0$，A中的主对角线元素大于0
- $|A|>0$，因为A的顺序主子式全部大于0

**重要结论** ★

- 如果A正定，则以下矩阵全部正定
  - $kA$
  - $A^{-1}$
  - $A^*$
  - $A^m$，m为正整数
  - $C^TAC$，C为可逆矩阵
- A和B正定，则下列全部正定
  - $A+B$
  - $\left[\begin{array}{ll}{A} & {O} \\ {O} & {B}\end{array}\right]$
- A和B正定且AB=BA，则AB正定
- A正定且A是正交矩阵，则A=E

