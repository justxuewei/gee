#                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         基础知识

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

## 代数余子式

- 对于具体型行列式，求代数余子式之和要想到求$A^*$，然后把$A^*$所有项求和即可。 <1000题 线代53>

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

定义

- 矩阵中线性无关的向量个数
- 存在k阶子式（行列式）不为零，任意k+1阶子式（行列式）等于零
- 对于一个$n\times n$的矩阵，$r(A)=n$等价于$|A|\neq0$等价于矩阵A可逆

公式，在没有具体说明的时候，A是一个$m\times n$的矩阵，B是任意满足条件的矩阵

- $0\leq r(A) \leq \min\{m, n\}$
- $r(kA)=r(A)$
- ★初等变换不改变秩的个数，若P和Q均为可逆矩阵，则$r(A)=r(PA)=r(AQ)=r(PAQ)
- ★乘积的秩越乘越小$r(AB)\leq \min\{r(A), r(B)\}$
  - ★★★推广：如果$r(AB)<r(A)$，则$B_{n\times n}$是不满秩矩阵，即$r(B)<n$。证明使用反证法，如果B是可逆矩阵（满秩），则$r(A)=r(AB)$。
- ★$r(A+B)\leq r(A)+r(B)$
- $r\left(\begin{array}{ll}{A} & {O} \\ {O} & {B}\end{array}\right)=r(A)+r(B)$
- $r(A)+r(B)\le r\left(\begin{array}{ll}{A} & {O} \\ {C} & {B}\end{array}\right)\le r(A)+r(B)=r(C)$
- $r(AB)\ge r(A)+r(B)-n$
  - ★注：若$AB=O$，则$r(A)+r(B)\le n$
- $r(A)=r({A^T})=r(A^TA)=r(AA^T)$ <1000题 线代134>
- ★★★伴随的秩$r(A^*)$ （证明在9讲例题5.25）
  - $n, \quad r(A)=n$
  - $1,\quad r(A)=n-1$
  - $0,\quad r(A)<n-1$
- ★（二次型）设矩阵$A_{n\times n}$且$A^2=A$，则可以推出$r(A)+r(A-E)=n$或$r(A)+r(E-A)=n$
- ★（相似理论）设矩阵$A_{n\times n}$且$A^2=E$，则可以推出$r(A+E)+r(A-E)=n$或$r(E+A)+r(E-A)=n$
- ★（齐次方程组）设矩阵$A_{m\times n}$且$AX=O$可以推出$s=n-r(A)$，是<u>基础解析中所含向量的个数</u>等于<u>未知数个数</u>减去<u>秩</u>
- ★（相似对角化）若$A\sim \Lambda \Leftrightarrow n_i=n-r(\lambda_iE-A)$，其中$\lambda_i$是$n_i$的重根
-  ★若$A\sim \Lambda \Rightarrow $$r(A)$等于非零特征值的个数

考法

- 化阶梯
- 用公式

## 特殊矩阵

正交矩阵

- 性质：正交矩阵是指${A}^T{A}={E} \Leftrightarrow {A}^T={A}^{-1}$（这个等价是在A可逆的前提下的），其性质有
  - 特征值全部为$1$或$-1$ <1000题 线代15, 线代16>
- 正交矩阵与T、-1和\*的关系：如果A是正交阵，则$A^T$、$A^{-1}$和$A^{*}$都是正交矩阵

实对称矩阵

- 实对称矩阵与T、-1和\*的关系：如果A是正交阵，则$A^T$、$A^{-1}$和$A^{*}$都是实对称矩阵

## 等价、合同与相似

矩阵等价 [[ref](https://blog.csdn.net/abraham_li/article/details/50058123)]

- 定义：对同型矩阵A、B，存在可逆阵P和Q，使得$B=PAQ$
- 充要条件：A与B的秩相同

矩阵合同

- 定义：对同型方阵A、B，存在可逆阵P使得$B=P^{T} A P$

矩阵相似

- 定义：对同型方阵A、B，存在可逆阵P，使得$B=P^{-1} A P$

关系：等价（只有秩相同）–>合同（秩和正负惯性指数相同）–>相似（秩，正负惯性指数，特征值均相同）

# 线性方程组

## ★具体型

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

- 相互带入法，$AX=0$的解满足$BX=0$，同样的$BX=0$的解也满足$AX=0$
- $r(A)=r(B)$且单方满足（例如只需证明$AX=0$的解满足$BX=0$，而不需证明$BX=0$的解也满足$AX=0$，相反同理）
- ★$r(A)=r(B)=r\left(\begin{array}{l}{A} \\ {B}\end{array}\right)$

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

- 情况1：$r(\alpha_1, \alpha_2, \alpha_3)=3$，显然有$r(\alpha_1, \alpha_2, \alpha_3, \alpha_4)=3$，这个时候方程组有唯一解，其几何意义为这三个向量不共线
  <img height="150" src="http://res.niuxuewei.com/2019-07-28-055433.png"/>
- 情况2：$r\left({\alpha}_{1}, {\alpha}_{2}, {\alpha}_{3}\right)=2$，也即$r\left({\beta}, {\beta}_{2}, {\beta}_{3}\right)=2$
  - 情况2.1：$r\left({\alpha}_{1}, {\alpha}_{2}, {\alpha}_{3}, {\alpha}_{4}\right)=2$，方程有无穷多解（解是一条线）
    - $r\left(\gamma_{1}, \gamma_{2}, \gamma_{3}\right)=2$且$\gamma_{1}, \gamma_{2}, \gamma_{3}$中有两个是线性相关的，其几何意义为两个向量共线（对应的平面重合），一个不共线
      <img height="150" src="http://res.niuxuewei.com/2019-07-28-060536.png"/>
    - $r\left(\gamma_{1}, \gamma_{2}, \gamma_{3}\right)=2$且$\gamma_{1}, \gamma_{2}, \gamma_{3}$互不共线
      <img height="150" src="http://res.niuxuewei.com/2019-07-28-060920.png"/>
  - 情况2.2：$r\left({\alpha}_{1}, {\alpha}_{2}, {\alpha}_{3}, {\alpha}_{4}\right)=2$，方程无解
    - 情况2.2.1：$\beta_1, \beta_2, \beta_3$有两个共线
      <img height="150" src="http://res.niuxuewei.com/2019-07-28-061120.png"/>
    - 情况2.2.2：$\beta_1, \beta_2, \beta_3$互不共线
      <img height="150" src="http://res.niuxuewei.com/2019-07-28-061309.png"/>
- 情况3：$r\left({\alpha}_{1}, {\alpha}_{2}, {\alpha}_{3}\right)=1$，也即$r\left({\beta}, {\beta}_{2}, {\beta}_{3}\right)=1$
  - 情况3.1：$r\left({\alpha}_{1}, {\alpha}_{2}, {\alpha}_{3}, {\alpha}_{4}\right)=1$，那么有无穷多解（解是一个面），三个面重合
    <img height="150" src="http://res.niuxuewei.com/2019-07-28-062605.png"/>
  - 情况3.2：$r\left({\alpha}_{1}, {\alpha}_{2}, {\alpha}_{3}, {\alpha}_{4}\right)=2$，此时方程组无解
    - 情况3.2.1：$\gamma_{1}, \gamma_{2}, \gamma_{3}$有两个向量线性相关
<img height="150" src="http://res.niuxuewei.com/2019-07-28-063531.png"/>
    - 情况3.2.2：$\gamma_{1}, \gamma_{2}, \gamma_{3}$任意两个线性无关
      <img height="150" src="http://res.niuxuewei.com/2019-07-28-063647.png"/>



