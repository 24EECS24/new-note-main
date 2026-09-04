---

# D 数列极限_第1页.png

## 数列的概念
对每个$n \in N_+$，如果按照某一法则，对应着一个确定的实数$x_n$，这些实数$x_n$按照下标$n$从小到大排成一个序列$\{x_n\}$，默认$n \to +\infty$，$n \in N_+$，即：
$$x_1,x_2,\dots,x_n,\dots$$
数列中每一个数叫项，第$n$项$x_n$为通项。
与函数不同的是，数列的点是离散的，相当于自变量为正整数的函数：
$$x_n = f(n),\quad n \in N_+$$

## 子列
从有无穷项的数列$\{a_n\}$中选取无穷项，并按原来的先后顺序组成新数列，称为$\{a_n\}$的子列。
例：从$\{a_n\}:a_1,a_2,a_3,\dots,a_n,\dots$中选取：
- 偶数项构成的子列：$\{a_{2n}\}:a_2,a_4,\dots,a_{2n},\dots$
- 奇数项构成的子列：$\{a_{2n-1}\}:a_1,a_3,\dots,a_{2n-1},\dots$

## 等差数列
首项为$a_1$，公差为$d$（$d \neq 0$），数列形式为：
$$a_1,\ a_1+d,\ a_1+2d,\ \dots,\ a_1+(n-1)d,\ \dots$$
通项公式：
$$a_n = a_1 + (n-1)d$$
前$n$项和公式：
$$S_n = \frac{n}{2}\left[2a_1+(n-1)d\right] = \frac{n}{2}(a_1+a_n)$$

## 等比数列
首项为$a_1$，公比为$r$（$r \neq 0$），数列形式为：
$$a_1,\ a_1r,\ a_1r^2,\ \dots,\ a_1r^{n-1},\ \dots$$
通项公式：
$$a_n = a_1 r^{n-1}$$
前$n$项和公式：
$$S_n=
\begin{cases}
na_1, & r=1 \\
\frac{a_1(1-r^n)}{1-r}, & r \neq 1
\end{cases}$$
若首项为1，则：
$$S_n = 1+r+r^2+\dots+r^{n-1} = \frac{1-r^n}{1-r}\quad (r \neq 1)$$

## 单调数列（$n \in N_+$）
1.  若$a_{n+1} \geq a_n$，则$\{a_n\}$单调不减
2.  若$a_{n+1} \leq a_n$，则$\{a_n\}$单调不增

---

# D 数列极限_第2页.png

## 有界数列
$n\in \mathbb{N}_+$
若存在正实数$M$，且$|a_n|\leq M$
则$\{a_n\}$为有界数列

其它证明有界的方法：放缩，求最值

## 一些数列的前n项和
$$\sum_{k=1}^n k = 1+2+3+\dots+n = \frac{n(n+1)}{2}$$
$$\sum_{k=1}^n k^2 = 1^2+2^2+3^2+\dots+n^2 = \frac{n(n+1)(2n+1)}{6}$$
$$\sum_{k=1}^n \frac{1}{k(k+1)} = \frac{1}{1\times2} + \frac{1}{2\times3} + \frac{1}{3\times4} + \dots + \frac{1}{n(n+1)} = \frac{n}{n+1}$$

## 裂项相消
$\frac{1}{1\times2}=1-\frac{1}{2},\quad \frac{1}{2\times3}=\frac{1}{2}-\frac{1}{3},\quad \frac{1}{3\times4}=\frac{1}{3}-\frac{1}{4},\dots$
$$
\begin{aligned}
\text{原式} &= 1-\frac{1}{2}+\frac{1}{2}-\frac{1}{3}+\frac{1}{3}-\frac{1}{4}+\dots+\frac{1}{n}-\frac{1}{n+1} \\
&= 1-\frac{1}{n+1} = \frac{n}{n+1}
\end{aligned}
$$

## 应用
和的极限等于各极限的和。
$$\lim_{n\to\infty} \sum_{k=1}^n \frac{1}{k(k+1)} = \lim_{n\to\infty} \frac{n}{n+1} = 1$$
先算离它近的符号。

### 2.1
$$\lim_{n\to\infty} \left( \frac{1}{1\cdot2} + \frac{1}{2\cdot3} + \dots + \frac{1}{n(n+1)} \right)^n = \underline{\quad} \quad (n\in \mathbb{N}_+)$$
解：由于
$$
\begin{aligned}
\frac{1}{1\cdot2} + \frac{1}{2\cdot3} + \dots + \frac{1}{n(n+1)}
&= 1-\frac{1}{2}+\frac{1}{2}-\frac{1}{3}+\dots+\frac{1}{n}-\frac{1}{n+1} \\
&= 1-\frac{1}{n+1} = \frac{n}{n+1}
\end{aligned}
$$
$$\text{原式} = \lim_{n\to\infty} \left( \frac{n}{n+1} \right)^n$$

$n$为离散的，不是连续的。
设$x$为连续的。
此处配有离散变量与连续变量转化的示意图，对应转化关系：
$$x \xrightleftharpoons[\text{连续化}]{\text{离散化}} n$$

---

# D 数列极限_第3页.png

若$\lim_{x \to +\infty} f(x) = A$，则$\lim_{n \to +\infty} f(n) = A$。

计算$1^\infty$型极限$\lim_{x \to +\infty} \left( \frac{x}{x+1} \right)^x$，利用$1^\infty$型极限计算公式：
$$
\lim u^v \stackrel{1^\infty}{=} e^{\lim v(u-1)}
$$
计算过程：
$$
\lim_{x \to +\infty} \left( \frac{x}{x+1} \right)^x = e^{\lim_{x \to +\infty} x\left( \frac{x}{x+1} - 1 \right)} = e^{-1}
$$

## 例2.1
设$0 < x_1 < 3$，$x_{n+1} = \sqrt{x_n(3 - x_n)} \ (n=1,2,\cdots)$，证明数列$\{x_n\}$有界。

利用均值不等式：
$$
\frac{a+b}{2} \geq \sqrt{ab} \quad (a,b>0)
$$
推导得：
$$
x_{n+1} = \sqrt{x_n(3 - x_n)} \leq \frac{x_n + (3 - x_n)}{2} = \frac{3}{2}
$$
因此$\{x_n\}$有上界。

## 数列极限的定义
（默认$\begin{cases} n \to +\infty \\ n \in \mathbb{N}_+ \end{cases}$）
- 收敛：趋向一个确定的有限值。
- 发散：不趋向一个确定的有限值。

设$a$为常数，若$\lim_{n \to \infty} x_n = a$，即$\{x_n\}$收敛于$a$。
若不存在这样的常数$a$，则数列$\{x_n\}$是发散的。

### 与函数极限对比
函数在$x \to +\infty$时的极限定义：
$$
\lim_{x \to +\infty} f(x) = a \iff \forall \varepsilon > 0, \exists X > 0, 当x > X时, |f(x) - a| < \varepsilon
$$
数列在$n \to \infty$时的极限定义：
$$
\lim_{n \to \infty} x_n = a \iff \forall \varepsilon > 0, \exists N > 0, 当n > N时, |x_n - a| < \varepsilon
$$
两者本质是一样的，只是函数的极限过程是连续的，数列的极限过程是离散的。

### 无穷大与无穷小
- 无穷大不是数，是比任何数都大的量，是一个变量，属于超实数。
- 无穷小不是数，是比任何数都小的量，是一个变量，属于超实数。

---

# D 数列极限_第4页.png

## 数列收敛与其子列收敛的关系
若数列$\{a_n\}$收敛，则其任何子列$\{a_{n_k}\}$也收敛，且$\lim\limits_{k \to \infty} a_{n_k} = \lim\limits_{n \to \infty} a_n$，收敛到同一个数。

### 推论
$$
\lim_{n \to \infty} a_n = a \Leftrightarrow
\begin{cases}
\lim\limits_{k \to \infty} a_{2k} = a \quad (\text{偶子列}) \\
\lim\limits_{k \to \infty} a_{2k-1} = a \quad (\text{奇子列}) \\
\{a_{2k}\} \cup \{a_{2k-1}\} = \{a_n\}
\end{cases}
$$

$$
\lim_{n \to \infty} a_n = a \Leftrightarrow
\begin{cases}
\lim\limits_{k \to \infty} a_{3k} = a \\
\lim\limits_{k \to \infty} a_{3k+1} = a \\
\lim\limits_{k \to \infty} a_{3k+2} = a \\
\{a_n\} = \{a_{3k}\} \cup \{a_{3k+1}\} \cup \{a_{3k+2}\}
\end{cases}
$$

## 例23
证明数列$\left\{n^{(-1)^n}\right\}$极限不存在。

解：数列$\left\{n^{(-1)^n}\right\}$的项依次为：$\displaystyle \frac{1}{1}, 2, \frac{1}{3}, 4, \frac{1}{5}, 6, \cdots$

偶项子列为$\{2n\}$，$\lim\limits_{n \to \infty} 2n = \infty$，该子列发散。
因为$\left\{n^{(-1)^n}\right\}$的子列$\{2n\}$不收敛，
故$\left\{n^{(-1)^n}\right\}$不收敛，即极限不存在。

但
该数列存在子列$\left\{\frac{1}{2n-1}\right\}$，对应项为$1, \frac{1}{3}, \frac{1}{5}, \cdots, \frac{1}{2n-1}, \cdots$，收敛于0，是收敛子列。
但由上述推导可知，原数列是发散的。

$\implies$ 一个数列的某个子列收敛 $\boldsymbol{\nRightarrow}$ 原数列收敛

$$
\left.
\begin{array}{l}
\text{原数列的任何子列收敛} \\
\text{且收敛到同一个数}
\end{array}
\right\}
\iff \text{原数列收敛}
$$

---

# D 数列极限_第5页.png

eg: 数列$\left\{(-1)^n\right\}: -1,1,-1,1,\dots,(-1)^n,\dots$
偶项子列$\left\{(-1)^{2k}\right\}:1,1,\dots,1,\dots$ 收敛于$1$
奇项子列$\left\{(-1)^{2k-1}\right\}:-1,-1,-1,\dots,-1,\dots$ 收敛于$-1$
$1 \neq -1$
$\implies$ 原数列极限不存在
即原数列发散

## 例2.2
证明：若$\lim\limits_{n \to \infty} a_n = A$，
则$\lim\limits_{n \to \infty} |a_n| = |A|$。

不能反过来用，
仅成立单向推导：
$$\lim_{n \to \infty} a_n = A \implies \lim_{n \to \infty} |a_n| = |A|$$

证：$\forall \varepsilon>0, \exists N>0$，$n>N$时：$|a_n - A|<\varepsilon$
$\implies ||a| - |b|| \leq |a - b|$
由于$||a_n| - |A|| \leq |a_n - A|$
$\implies \forall \varepsilon>0, \exists N>0$，$n>N$时：$||a_n| - |A|| < \varepsilon$
$\implies \lim_{n \to \infty} |a_n| = |A|$

若本题中$A=0$，
可以反过来用：
$\because ||a_n| - |A|| = ||a_n| - 0| = |a_n - 0|$
$$\lim_{n \to \infty} a_n = 0 \iff \lim_{n \to \infty} |a_n| = 0$$

由于$|a_n|\geq0$，若使用夹逼准则，便可省一半的力气，
只需证$|a_n|\leq 0$即可。

此结论对函数亦成立。
若$\lim\limits_{x \to x_0} f(x) = A$，则$\implies \lim\limits_{x \to x_0} |f(x)| = |A|$
$$\lim_{x \to x_0} f(x) = 0 \iff \lim_{x \to x_0} |f(x)| = 0$$

## 例2.4
设
$$x_n = \begin{cases}
\dfrac{n^2 + \sqrt{n}}{n}, & n为正奇数 \\
\dfrac{1}{n}, & n为正偶数
\end{cases}$$
则当$n \to \infty$时，变量$x_n$为$\underline{\quad\quad}$。

解：$\lim\limits_{n \to \infty} x_{2n} = \lim\limits_{n \to \infty} \frac{1}{2n} = 0$
$$\lim_{n \to \infty} x_{2n-1} = \lim_{n \to \infty} \frac{(2n-1)^2 + \sqrt{2n-1}}{2n-1} = \lim_{n \to \infty} \frac{(2n-1)^2}{2n-1} = \infty$$

---

# D 数列极限_第6页.png

注：$x_n$为无界变量，但不是无穷大量
（包含0点）
## 收敛数列的性质（类比函数）
### 唯一性
给出数列$\{x_n\}$，若$\lim\limits_{n \to \infty} x_n = a$，则$a$是唯一的。
### 有界性
若数列$\{x_n\}$极限存在，则数列$\{x_n\}$有界。
### 保号性
#### 脱帽情形
如果数列的极限值存在且大于$b$，设$\lim\limits_{n \to \infty} x_n = a > b$，则存在$N>0$，当$n>N$时，数列的所有项都满足$x_n > b$。
#### 带帽情形
若数列$\{x_n\}$从某一项起有$x_n \geqslant b$，且$\lim\limits_{n \to +\infty} x_n = a$，则$a \geqslant b$；$b$为任意实数，常考$b=0$的情形。
##### 方法总结
- 带帽法：
$$x_n \genfrac{}{}{0}{}{\geqslant}{\leqslant} a \implies \lim_{n \to \infty} x_n \genfrac{}{}{0}{}{\geqslant}{\leqslant} a$$
- 脱帽法：
$$\lim_{n \to \infty} x_n \genfrac{}{}{0}{}{>}{<} a \implies x_n \genfrac{}{}{0}{}{>}{<} a$$
##### 示例
1.  $\lim\limits_{n \to \infty} x_n > 1 \implies n$足够大时$x_n > 1$
2.  $x_n > -1 \implies \lim\limits_{n \to \infty} x_n \geqslant -1$
3.  $x_n = \frac{1}{n} > 0,\ n=1,2,3,\dots$，$\lim\limits_{n \to \infty} x_n = 0$

---

# D 数列极限_第7页.png

## 例2.5 保号性判断数列最值
已知 $a_n=1-\frac{(-1)^n}{n}\ (n=1,2,\cdots)$（用保号性），求$\{a_n\}$有没有最值。
### 分析
写出数列前几项：
$$a_1=2,\ a_2=\frac{1}{2},\ a_3=\frac{4}{3},\ a_4=\frac{3}{4},\cdots$$
数列不是单调的。
取个极限看看：
$$\lim_{n\to\infty}a_n=1$$
$n\to\infty$时$a_n$要无限趋近于1，大胆猜一下。
（函数示意图：数列$\{a_n\}$围绕水平直线$y=1$震荡，逐渐趋近于$y=1$；纵轴标注刻度2与$\frac{1}{2}$，旁注数列项$2,\frac{1}{2},\frac{4}{3},\cdots$）
### 解答
$$\lim_{n\to\infty}a_n=1$$
由保号性可知，存在正整数$N$，当$n>N$时，所有$a_n$都无限靠近1，满足：
$$\frac{1}{2} < \text{无限靠近1的数} < 2$$
故
$$\lim_{n\to\infty}(a_n - a_1) = \lim_{n\to\infty}a_n - 2 <0$$
$\Rightarrow \exists N_1>0$，当$n>N_1$时：
$$a_n - a_1 <0 \Rightarrow a_n < a_1$$
$$\lim_{n\to\infty}(a_n - a_2) = \lim_{n\to\infty}a_n - \frac{1}{2} >0$$
$\Rightarrow \exists N_2>0$，当$n>N_2$时：
$$a_n - a_2>0 \Rightarrow a_n>a_2$$
取$N=\max\{N_1,N_2\}$，当$n>N$时，$a_n$均不能是最值。
即$\{a_n\}$既有最大值，也有最小值。
> 莱布尼兹说过：最值是比较出来的。
> 这里用保号性说明了$n>N$后的项没有资格参与比较，故前有限项中必有最大值、最小值。

---

# D 数列极限_第8页.png

## 数列极限四则运算规则
设$\lim_{n \to \infty} x_n = a$，$\lim_{n \to \infty} y_n = b$，则：
- $$\lim_{n \to \infty} (x_n \pm y_n) = a \pm b$$
- $$\lim_{n \to \infty} x_n y_n = ab$$
- 若$b \neq 0$，则$$\lim_{n \to \infty} \frac{x_n}{y_n} = \frac{a}{b}$$

四则运算规则可以推广至有限个数列的情形。

若$\lim_{n \to \infty} x_n$与$\lim_{n \to \infty} y_n$不存在，那么即使$\lim_{n \to \infty} (x_n \pm y_n) = a$有结果，也不能写成$\lim_{n \to \infty} x_n \pm \lim_{n \to \infty} y_n = a$，因为$\lim_{n \to \infty} x_n$与$\lim_{n \to \infty} y_n$不存在。

## 例2-6
设$\lim_{n \to \infty} (a_n + b_n) = 1$，$\lim_{n \to \infty} (a_n - b_n) = 3$，则$\{a_n\}$与$\{b_n\}$的极限是否存在？

因为我们不知道$\lim_{n \to \infty} a_n$与$\lim_{n \to \infty} b_n$是否存在，但$\lim_{n \to \infty} (a_n + b_n)$与$\lim_{n \to \infty} (a_n - b_n)$存在。

那么，令$u_n = a_n + b_n$，$v_n = a_n - b_n$，则：
$$
\begin{aligned}
\lim_{n \to \infty} (u_n + v_n) &= \lim_{n \to \infty} u_n + \lim_{n \to \infty} v_n \\
&= 2\lim_{n \to \infty} a_n = 1 + 3 = 4 \\
\Rightarrow \lim_{n \to \infty} a_n &= 2，极限存在
\end{aligned}
$$

$$
\begin{aligned}
\lim_{n \to \infty} (u_n - v_n) &= \lim_{n \to \infty} u_n - \lim_{n \to \infty} v_n \\
&= 2\lim_{n \to \infty} b_n = 1 - 3 = -2 \\
\Rightarrow \lim_{n \to \infty} b_n &= -1，极限存在
\end{aligned}
$$

---

# D 数列极限_第9页.png

## 海涅定理（归结原则）
联系数列与函数的桥梁，可实现数列极限与函数极限的互相转化。

### 定理前提
设$f(x)$在$x_0$的去心邻域$\mathring{U}(x_0, \delta)$内有定义，即无需考虑$f(x_0)$是否有定义，仅需考虑$x_0$点附近的函数定义情况。

### 定理核心内容
$\lim\limits_{x \to x_0} f(x) = A$存在的充要条件是：对$\mathring{U}(x_0, \delta)$内所有以$x_0$为极限的数列$\{x_n\}$，对应的函数值数列$\{f(x_n)\}$的极限都存在，且相等，等于$A$。

### 两类极限过程对应
- 连续极限过程：$x \to x_0$（函数极限）
- 离散极限过程：$n \to \infty$（数列极限）

注：涉及数列下标$n$时，默认满足
$$\begin{cases}
n \in \mathbb{N}_+ \\
n \to +\infty
\end{cases}$$

---

将连续极限过程$x \to x_0$离散为点列极限过程$x_n \to x_0$：
$x_n$是以$x_0$为极限的数列，即$\lim\limits_{n \to \infty} x_n = x_0$。
满足该条件的数列$\{x_n\}$有无穷多个，例如：
1.  等差（算术级）趋近数列：满足$\frac{1}{x_n - x_0} = n+2$，即$x_n = x_0 + \frac{1}{n+2}$
    对应示意图：横轴为$n$，纵轴为$x_n$，$x_n$随$n$增大逐步趋近于水平直线$x=x_0$。
2.  等比（指数级）趋近数列：满足$x_n - x_0 = \left(\frac{1}{4}\right)^n$，即$x_n = x_0 + \frac{1}{4^n}$
    对应示意图：横轴为$n$，纵轴为$x_n$，$x_n$随$n$增大快速趋近于水平直线$x=x_0$。

### 归结原则严格表述
$$\lim_{x \to x_0} f(x) = A \iff \text{对所有满足} \lim_{n \to \infty} x_n = x_0 \text{的数列} \{x_n\}，都有\lim_{n \to \infty} f(x_n) = A$$
注：定理要求所有以$x_0$为极限的数列$\{x_n\}$对应的$\{f(x_n)\}$极限都存在，且极限值彼此相等，均等于$A$。

---

# D 数列极限_第10页.png

## 连续与离散
- 若$x\to0$，取$\{x_n\}=\frac{1}{n}$
  即若$\lim\limits_{x\to0}f(x)=A$，则$\lim\limits_{n\to\infty}f\left(\frac{1}{n}\right)=A$。
  $x\to0,\ x_n\to0$
  $\Downarrow$
  $f(x)\to A,\ f(x_n)\to A$
- 若$x\to+\infty$，取$\{x_n\}=n$
  即若$\lim\limits_{x\to+\infty}f(x)=A$，则$\lim\limits_{n\to\infty}f(n)=A$。
  $x\to+\infty,\ x_n\to+\infty$
  $\Downarrow$
  $f(x)\to A,\ f(x_n)\to A$
- 若$x_n\to a$且$x_n\neq a$时
  若$\lim\limits_{x\to a}f(x)=A$，则$\lim\limits_{n\to\infty}f(x_n)=A$。
  $x\to a,\ x_n\to a$
  $\Downarrow$
  $f(x)\to A,\ f(x_n)\to A$
### 例2.7
当$x\to0$时，$\frac{1}{x}\sin\frac{1}{x}$是$\underline{\quad\quad}$
**分析** 计算$\lim\limits_{x\to0}\frac{1}{x}\sin\frac{1}{x}$
只用找两个离散的$x_n$，看看极限值是否相等：
若$\lim\limits_{x_{n1}\to0}f(x_{n1})=A=\lim\limits_{x_{n2}\to0}f(x_{n2})$，那么大概率$\lim\limits_{x\to0}f(x)=A$。
若$\lim\limits_{x_{n1}\to0}f(x_{n1})\neq\lim\limits_{x_{n2}\to0}f(x_{n2})$，那么$\lim\limits_{x\to0}f(x)$不存在。
**解：**
① 取$x_n=\frac{1}{n\pi}\to0$
$$\lim_{x_n\to0}f(x_n)=\lim_{x_n\to0} n\pi \sin(n\pi)=0$$
② 取$x_n=\frac{1}{(2n+\frac{1}{2})\pi}\to0$
$$\lim_{x_n\to0}f(x_n)=\lim_{x_n\to0} \left(2n+\frac{1}{2}\right)\pi\cdot\sin\left[\left(2n+\frac{1}{2}\right)\pi\right]=+\infty$$
综上，一个为0，一个为$+\infty$ $\Rightarrow$ $\lim\limits_{x\to0}\frac{1}{x}\sin\frac{1}{x}$不存在/无界
## $f(x)$在$x=x_0$处连续
$$\Leftrightarrow \lim_{x\to x_0^+}f(x)=\lim_{x\to x_0^-}f(x)=f(x_0)$$
等价于
$$\Leftrightarrow \lim_{\Delta x\to0}\left[f(x_0+\Delta x)-f(x_0)\right]=0$$
$$\Leftrightarrow \lim_{\Delta x\to0}\Delta f(x)=0$$
即当在$x_0$这一点处有一个增量$\Delta x$时，$\Delta x\to0$，其函数增量$\Delta f(x)$的极限值也为0，$(x_0,f(x_0))$与$(x_0+\Delta x,f(x_0)+\Delta f(x))$这两点间的距离为无穷小。

---

# D 数列极限_第11页.png

## 问题（要对归结原则有一个好的理解）
若$f(x)$在$x=x_0$处连续，是否能推出：
$\exists \delta>0$，当$|x-x_0|<\delta$时，$f(x)$连续（$\delta$对应$x_0$的邻域范围）。
即：$f(x)$在$x=x_0$这一点连续，那么$f(x)$在$x_0$这一点的邻域内是否是连续的？
> 邻域示意图：x轴上标注邻域端点$x_0-\delta$、$x_0$、$x_0+\delta$，标注邻域内点与$x_0$的差满足$x_0-(x_0\pm\delta)=\Delta x$。
---
**证：**
引入狄利克雷函数：
$$
D(x)=\begin{cases}
1, & x\in 有理数 \\
0, & x\in 无理数
\end{cases}
$$
构造函数：
$$
f(x)=x^2 D(x)=\begin{cases}
x^2, & x\in 有理数 \\
0, & x\in 无理数
\end{cases}
$$
因为$0\in$有理数，所以$f(0)=0$，计算$\lim_{x\to 0} f(x)$：
### 法1
因为$f(0)=0$，因此：
$$
\lim_{\Delta x\to 0} \left[f(0+\Delta x)-f(0)\right] = \lim_{\Delta x\to 0} (\Delta x)^2 D(\Delta x) = 0
$$
其中$(\Delta x)^2$是$\Delta x\to0$时的无穷小，$D(\Delta x)$是有界函数，根据无穷小与有界函数的乘积仍为无穷小，可得：
$$
\Rightarrow \lim_{x\to 0} f(x) = f(0)
$$
> 拓展补充：二元函数仅在原点连续的反例
> $$
> f(x,y)=\begin{cases}
> xy, & xy\neq 0 \\
> x, & x=0 \\
> y, & y=0
> \end{cases}
> $$
> 满足$|f(x,y)|\leq |xy|+|x|+|y|$。
### 法2
对于上述一元函数$f(x)$，当$x$为有理数时$|f(x)|=x^2$，当$x$为无理数时$|f(x)|=0$，因此有夹逼不等式：
$$0\leq |f(x)| \leq x^2$$
当$x\to0$时$x^2\to0$，由夹逼准则，不等式两边极限均为0，因此：
$$\lim_{x\to 0} |f(x)| = 0 \Rightarrow \lim_{x\to 0} f(x) = 0 = f(0)$$

---

# D 数列极限_第12页.png

但，若取$x_0 \neq 0$
取有理数数列$x_n$，$\lim\limits_{x_n \to x_0} x_n^2 = x_0^2 \neq 0$
取无理数数列$x_n$，$\lim\limits_{x_n \to x_0} 0 = 0$
由归结原则，
$$\lim_{x \to x_0} f(x) = A \iff \text{任给数列 } x_n, \text{ 满足 } x_n \to x_0 \ (x_n \neq x_0), \text{ 都有 } \lim_{x_n \to x_0} f(x_n) = A.$$
一个是0，一个不是0 $\implies \lim\limits_{x \to x_0} f(x)$不存在
$\implies$ 不连续
$\implies$ 综上所述是不连续
即$f(x)$在$x=x_0$这一点处连续，那么，$f(x)$在$x=x_0$这一点的附近是不连续的。
所谓连续，不是几何意义上的两点相连不断开，
而是：自变量$x_0$增加$\Delta x$，变为$x_0+\Delta x$，$\Delta x \to 0$，
而因变量$f(x_0)$增加$\Delta f(x)$，变为$f(x_0)+\Delta f(x)$，$\Delta f(x) \to 0$，
两点之间的距离是一个无穷小量，则这两点连续，
即点$(x_0,f(x_0))$与点$(x_0+\Delta x, f(x_0)+\Delta f(x))$两点之间的距离是无穷小量，极限为0，两点间的距离是动态的，两点在无限靠近。
$x=x_0$，这一点和它旁边的这些点是无限靠近的：
$$\underbrace{x=x_0}_{f(x_0)}, \quad \underbrace{\text{旁边的这些点}}_{\lim_{x \to x_0^-} f(x) \text{ 与 } \lim_{x \to x_0^+} f(x)}$$
∵
$$\lim_{x \to x_0} \left[ \underbrace{f(x)}_{\lim\limits_{x \to x_0} f(x)} - f(x_0) \right] = 0$$
∴
$$\lim_{x \to x_0^+} f(x) = f(x_0) = \lim_{x \to x_0^-} f(x)$$
称函数$f(x)$在点$x_0$处连续。

## 例2.8
求$\lim\limits_{n \to \infty} \sqrt[n]{\left( \cos \frac{1}{\sqrt{n}} \right)^{n^2}}$
解：
$$
\begin{align*}
\lim_{x \to +\infty} \sqrt[x]{\left( \cos \frac{1}{\sqrt{x}} \right)^{x^2}}
&= \lim_{x \to +\infty} \left( \cos \frac{1}{\sqrt{x}} \right)^x
\end{align*}
$$

---

# D 数列极限_第13页.png

当$x \to +\infty$时：
$$
\left.
\begin{array}{l}
\displaystyle \frac{1}{\sqrt{x}} \to 0 \\
\displaystyle \cos\frac{1}{\sqrt{x}} \to 1
\end{array}
\right\} \Rightarrow 1^\infty \text{型极限}
$$

计算过程：
$$
\begin{align*}
\text{原式} &= e^{\lim\limits_{x \to +\infty} x\left(\cos\frac{1}{\sqrt{x}} - 1\right)} \\
&= e^{\lim\limits_{x \to +\infty} x\cdot\left(-\frac{1}{2}\cdot\frac{1}{x}\right)} \\
&= e^{-\frac{1}{2}}
\end{align*}
$$
其中用到等价无穷小：
$1-\cos t \sim \frac{1}{2}t^2 \ (t\to0)$，即$\cos t - 1 \sim -\frac{1}{2}t^2 \ (t\to0)$。

由归结原则知，原式$=e^{-\frac{1}{2}}$。

## 2.2
当$n \to \infty$时，$\left(1+\frac{1}{n}\right)^n - e$与$\frac{a}{n}$是等价无穷小量，则$a = \underline{\quad\quad}$

在极限的题型总结中的例1.24有得出结论：
$$(1+x)^{\frac{1}{x}} - e \sim -\frac{e}{2}x \quad (x \to 0^+)$$

解答：
当$x \to 0^+$时，$\frac{1}{x} \to +\infty$，令$x=\frac{1}{n}$，则$n \to +\infty$。
由归结原则可得：
$$\left(1+\frac{1}{n}\right)^n - e \sim -\frac{e}{2} \cdot \frac{1}{n} \quad (n \to +\infty)$$
因此$a = -\frac{e}{2}$。