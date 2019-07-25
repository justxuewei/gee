# 基础知识

## 单位矩阵

- ${E}={E}^T$
- $|{E}|=1$
- 提公因式${A}-{AX}={A}({E}-{X})$
- $E^n=E$ <1000 线代19>

## 转置

- ${A}$和${B}$是$n$阶矩阵，${A}^T\pm{B}^T = ({A}\pm{B})^T $<1000题 线代15>
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

秩 [参见 `矩阵 > 秩 > 公式`]

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
- 逆
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
- $r(A)=r({A^T})=r(A^TA)=r(AA^T)$
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