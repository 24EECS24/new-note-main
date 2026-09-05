# B 函数极限题型总结_第1页.png

## 函数极限一般计算题页总结归纳
## 七种未定式的计算
未定：你来定，有可能存在，有可能不存在。

$\frac{0}{0}$、$\frac{\infty}{\infty}$、$0\cdot\infty$、$\infty-\infty$、$\infty^0$、$0^0$、$1^\infty$

这里的
- 1是以1作为标准实数的超实数
- 0是以0作为标准实数的超实数
- $\infty$是以$\infty$作为标准实数的超实数

## 题型
- 直接计算
- 反求参数
- 已知某一极限求另一极限
- 无穷小的比阶

要先化简，后计算。
直接用洛必达，或泰勒计算的话，可能会很复杂，甚至算不出来。

## 化简方法
- 提出极限不为0的因式（极限能求出的那种）
  因式：乘除型（四则运算那里有）
- 等价无穷小的合理代换（仅是$\times$）
- 恒等变形：
  提公因式
  拆项
  合并
  分子分母同除变量的最高次幂
  换元法，即，变量替换

要先判断出是七种类型的哪一种，再选择计算方法（洛必达，泰勒，夹逼准则）

---

# B 函数极限题型总结_第2页.png

(1) 待定型：$\frac{0}{0}$、$\frac{\infty}{\infty}$、$0\cdot\infty$【类1】
## 1.24
$$\lim_{x \to 0^+} \frac{(1+x)^{\frac{1}{x}} - e}{x} = \underline{\quad\quad}$$
当$x \to 0^+$时，$(1+x)^{\frac{1}{x}} \to e$，因此该极限为$\frac{0}{0}$型。
用到幂指函数恒等公式：
$$a^b = e^{b\ln a}$$
解：
$$
\begin{align*}
\text{原式} &= \lim_{x \to 0^+} \frac{e^{\frac{\ln(1+x)}{x}} - e}{x} \\
&= e \lim_{x \to 0^+} \frac{e^{\frac{\ln(1+x)}{x} - 1} - 1}{x}
\end{align*}
$$
由等价无穷小$e^x - 1 \sim x \ (x\to0)$，可得：当无穷小量$\square \to 0$时，$e^\square - 1 \sim \square$，因此：
$$
\text{原式} = e \lim_{x \to 0^+} \frac{\frac{\ln(1+x)}{x} - 1}{x}
$$
> 备注：心里要清楚，这里不是直接随意替换，依据是极限四则运算法则。
通分化简得：
$$
\text{原式} = e \lim_{x \to 0^+} \frac{\ln(1+x) - x}{x^2}
$$
---
### 法① 洛必达法则
$$
\begin{align*}
\text{原式} &= e \lim_{x \to 0^+} \frac{\frac{1}{1+x} - 1}{2x} \tag{第一次求导} \\
&= e \lim_{x \to 0^+} \frac{-\frac{1}{(1+x)^2}}{2} \tag{第二次求导}
\end{align*}
$$
> 旁注：$\left(\frac{1}{x}\right)' = -\frac{1}{x^2}$
计算得：
$$
\text{原式} = -\frac{1}{2}e
$$
---
### 法② 泰勒公式
泰勒公式一站直达：因为分母为2阶无穷小，因此分子展开到2阶即可，利用等价无穷小：
$$\ln(1+x) - x \sim -\frac{1}{2}x^2 \quad (x\to0)$$
因此：
$$
\begin{align*}
\text{原式} &= e \lim_{x \to 0^+} \frac{\ln(1+x) - x}{x^2} \\
&= e \lim_{x \to 0^+} \frac{-\frac{1}{2}x^2}{x^2}
\end{align*}
$$
> 备注：心里要清楚一点，本质上不是直接代换，是泰勒展开到对应阶数的结果。
计算得：
$$
\text{原式} = -\frac{1}{2}e
$$

---

# B 函数极限题型总结_第3页.png

## 记忆
$f(x)=(1+x)^{\frac{1}{x}}$在$x>0$时有以下性质：
- $f(x)$单调递减
  （附$f(x)=(1+x)^{\frac{1}{x}}$的函数示意图）
- $\lim\limits_{x \to 0^+} f(x) = e$
- $(1+x)^{\frac{1}{x}} - e \sim -\frac{e}{2}x \quad (x \to 0^+)$
- $\lim\limits_{x \to \infty} \left(1+\frac{1}{x}\right)^x = e$
  （附$\left(1+\frac{1}{x}\right)^x$的函数示意图）

### 推导③
由1.24得：
$$\lim_{x \to 0^+} \frac{(1+x)^{\frac{1}{x}} - e}{x} = -\frac{e}{2}$$
> 积累
> $x \to 0^+$时，$(1+x)^{\frac{1}{x}} - e \to 0^+$

$$\Rightarrow \lim_{x \to 0^+} \frac{(1+x)^{\frac{1}{x}} - e}{-\frac{e}{2}x} = 1$$
$$\Rightarrow (1+x)^{\frac{1}{x}} - e \sim -\frac{e}{2}x \quad (x \to 0^+)$$

---

## 1.25
求极限
$$I = \lim_{x \to \infty} \frac{a_n x^n + a_{n-1}x^{n-1} + \dots + a_1 x + a_0}{b_m x^m + b_{m-1}x^{m-1} + \dots + b_1 x + b_0}$$
其中$a_n(\neq 0), b_m(\neq 0)$为常数。

### 用到的方法、思想
- 代特殊值法/特例法：取特殊值$0,1,\infty$，考虑相等、相反数、倒数的特殊关系
- 找带头大哥：分子分母同除变量的最高次幂
  预备极限：
  $\lim\limits_{x \to \infty} \frac{1}{x} = 0$
  $\lim\limits_{x \to \infty} \left(\frac{1}{x} + x^2 + x^4\right) = \lim_{x \to \infty}\frac{1}{x} + \lim_{x \to \infty}x^2 + \lim_{x \to \infty}x^4$

### 解：若$m=n$
$$
\begin{align*}
I &= \lim_{x \to \infty} \frac{a_n + \frac{a_{n-1}}{x} + \dots + \frac{a_1}{x^{n-1}} + \frac{a_0}{x^n}}{b_m + \frac{b_{m-1}}{x} + \dots + \frac{b_1}{x^{m-1}} + \frac{b_0}{x^m}} \\
&= \frac{\lim\limits_{x \to \infty}\left(a_n + \frac{a_{n-1}}{x} + \dots + \frac{a_1}{x^{n-1}} + \frac{a_0}{x^n}\right)}{\lim\limits_{x \to \infty}\left(b_m + \frac{b_{m-1}}{x} + \dots + \frac{b_1}{x^{m-1}} + \frac{b_0}{x^m}\right)} \\
&= \frac{a_n}{b_m}
\end{align*}
$$

---

# B 函数极限题型总结_第4页.png

## x→∞时有理多项式分式的极限
若$n>m$：
$$
I = \lim_{x \to \infty} \frac{x^{n-m}\left(a_n x^m + a_{n-1}x^{m-1} + \dots + a_1 x^{m-n+1} + a_0 x^{m-n}\right)}{b_m x^m + b_{m-1}x^{m-1} + \dots + b_1 x + b_0}
$$
注：分子分母同除$x^m$，且$\lim_{x \to \infty} \frac{1}{x^u}=0 \ (u>0)$，低次项在$x \to \infty$时极限为0，因此：
$$
= \lim_{x \to \infty} x^{n-m} \cdot \frac{a_n}{b_m} = \infty
$$

若$n<m$：
$$
I = \lim_{x \to \infty} \frac{a_n x^n + a_{n-1}x^{n-1} + \dots + a_1 x + a_0}{x^{m-n}\left(b_m x^n + b_{m-1}x^{n-1} + \dots + b_1 x^{n-m+1} + b_0 x^{n-m}\right)}
$$
注：分子分母同除$x^n$，低次项在$x \to \infty$时极限为0，因此：
$$
= \lim_{x \to \infty} \frac{1}{x^{m-n}} \cdot \frac{a_n}{b_m} = 0
$$

可理解为：当$x \to \infty$时，多项式最高次项起主导作用，
$$a_n x^n \gg a_{n-1}x^{n-1} \gg \dots$$
$$b_m x^m \gg b_{m-1}x^{m-1} \gg \dots$$

综上，可得结论：
$$
\lim_{x \to \infty} \frac{a_n x^n + a_{n-1}x^{n-1} + \dots + a_1 x + a_0}{b_m x^m + b_{m-1}x^{m-1} + \dots + b_1 x + b_0}
=
\begin{cases}
\displaystyle \frac{a_n}{b_m}, & n=m \quad \text{分子与分母同阶} \\[6pt]
\infty, & n>m \quad \text{分子远大于分母} \\[6pt]
0, & n<m \quad \text{分子远小于分母}
\end{cases}
$$

---

### 例题
$$
\lim_{x \to -\infty} \frac{\sqrt{4x^2+x-1} + x+1}{\sqrt{x^2+\sin x}}
$$
分析（$x \to -\infty$时忽略低阶无穷大，取主导项）：
- 分子根号项：$4x^2+x-1$以$4x^2$为主导，即$4x^2+x-1 \sim 4x^2$，故$\sqrt{4x^2+x-1} \sim |2x|$；$x \to -\infty$时$x<0$，$|2x|=-2x$，即该项主导项为$-2x$。
- 分子线性项：$x+1$的主导项为$x$。
- 分母：$x^2 \gg \sin x$，$x^2+\sin x$以$x^2$为主导，即$x^2+\sin x \sim x^2$，故$\sqrt{x^2+\sin x} \sim |x|$；$x<0$时$|x|=-x$，即分母主导项为$-x$。

---

# B 函数极限题型总结_第5页.png

$$\lim_{x \to -\infty} \frac{-2x + x}{-x} = 1$$

## 1.26 用极限定义函数的问题 分类讨论
设函数$f(x)=\lim\limits_{n \to \infty} \frac{x^2 + n x(1-x)\sin^2 \pi x}{1 + n \sin^2 \pi x}$，则$f(x)=$____

$n$为自然数
$n \to \infty$指$n \to +\infty$
$n$以某种速度无限扩大
（正负标注十字草稿示意图）

分类讨论前提：
当$x$为整数时：
$(1-x)\sin^2 \pi x = 0,\ n \sin \pi x = 0$

当$x$不为整数时：
$(1-x)\sin^2 \pi x \neq 0,\ n \sin \pi x \neq 0$

思考注记：$n \to +\infty$时，$\sin^2 \pi x \to 0$的速度远大于$n \to +\infty$的速度？？

$\Rightarrow$当$x$为整数时，$n \to +\infty$：
$$f(x) \to \frac{x^2 + 0}{1+0} \to x^2$$

当$x$不为整数，$n \to +\infty$：
$$f(x) \to \frac{n x(1-x)\sin^2 \pi x}{n \sin^2 \pi x} \to x(1-x)$$

$\Rightarrow$该函数为分段函数。

综上所述：
$$
f(x)=
\begin{cases}
x^2, & x为整数 \\
x(1-x), & x不为整数
\end{cases}
$$
（分段函数示意图：整数点处取$y=x^2$对应值，非整数区间为抛物线$y=x(1-x)$的部分，整数点处用虚线标注间断）

---

# B 函数极限题型总结_第6页.png

## 1.27 已知某一极限，去求另一极限
已知极限：
$$\lim_{x \to 0} \frac{\tan2x + x f(x)}{\sin x^3} = 0$$
求：
$$\lim_{x \to 0} \frac{2+f(x)}{x^2} = \underline{\quad\quad}$$

对已知极限做变形：
$$
\lim_{x \to 0} \frac{\tan2x + x f(x)}{\sin x^3} = \alpha \quad (\alpha \to 0)
$$
> 疑问：为什么乘除法时($\sin x^3$)可以替换，加减时($\tan2x$)不能替换？

当$x \to 0$时：
$$\lim_{x\to0}\frac{\sin x^3}{x^3} = 1$$
因此乘除法场景下可做等价无穷小替换：
$$
\lim_{x \to 0} \frac{\tan2x + x f(x)}{\sin x^3} \cdot \frac{\sin x^3}{x^3} = \lim_{x \to 0} \frac{\tan2x + x f(x)}{x^3}
$$

整理得到$f(x)$的表达式：
$$
\tan2x + x f(x) = \alpha x^3 \implies f(x) = \frac{x^3 \cdot \alpha - \tan2x}{x}
$$

代入待求极限计算：
$$
\begin{align*}
\lim_{x \to 0} \frac{2+f(x)}{x^2}
&= \lim_{x \to 0} \frac{2 + \frac{x^3 \alpha - \tan2x}{x}}{x^2} \\
&= \lim_{x \to 0} \frac{2x - \tan2x + x^3 \alpha}{x^3} \\
&= \lim_{x \to 0} \frac{2x - \tan2x}{x^3} + \lim_{x \to 0} \frac{x^3 \alpha}{x^3}
\end{align*}
$$
由题设已知极限为0，得$\alpha=0$，因此第二项极限值为0。

用到的等价无穷小（$x \to 0$）：
$$\tan x - x \sim \frac{1}{3}x^3, \quad x - \tan x \sim -\frac{1}{3}x^3$$
将$2x$视为整体，代入计算第一项：
$$
\begin{align*}
\lim_{x \to 0} \frac{2x - \tan2x}{x^3}
&= \lim_{x \to 0} \frac{-\frac{8}{3}x^3}{x^3} \\
&= -\frac{8}{3}
\end{align*}
$$

---

# B 函数极限题型总结_第7页.png

## 0·∞ 无穷小·无穷大
$0\cdot\infty$型未定式可转化为$\frac{0}{0}$或$\frac{\infty}{\infty}$型未定式，转化关系如下：
$$0\cdot\infty = \frac{0}{\frac{1}{\infty}} = \frac{\infty}{\frac{1}{0}} = \frac{0}{0} = \frac{\infty}{\infty}$$

例：求极限$\lim\limits_{x \to 0^+} x\ln x$，为$0\cdot\infty$型。
1.  第一种转化方式（将对数项取倒数下放为分母）：
$$= \lim_{x \to 0^+} \frac{x}{\frac{1}{\ln x}} \quad (\frac{0}{0}\text{型})$$
使用洛必达法则：
$$\xlongequal{\text{洛}} \lim_{x \to 0^+} \frac{1}{\frac{1}{-\ln^2 x} \cdot \frac{1}{x}} = \lim_{x \to 0^+} \left(-x\ln^2 x\right)$$
求导后形式更复杂，该方法不适用。

2.  第二种转化方式（将幂函数项取倒数下放为分母）：
$$= \lim_{x \to 0^+} \frac{\ln x}{\frac{1}{x}} \quad (\frac{\infty}{\infty}\text{型})$$
使用洛必达法则：
$$\xlongequal{\text{洛}} \lim_{x \to 0^+} \frac{\frac{1}{x}}{-\frac{1}{x^2}} = -\lim_{x \to 0^+} x = 0$$

## 总结
$0\cdot\infty$型未定式化分式的原则：
**设置分母有原则，简单因式才下放**
（原则目的：方便洛必达法则求导计算）
- 简单因式（适合下放为分母，即取倒数）：$x^\alpha$，$e^{\beta x}$，$\sin ax$
- 复杂因式（不适合下放为分母）：$\arcsin x$，$\arctan x$，$\ln x$，……

### 128 求极限$\lim\limits_{x \to 1^-} \ln x \ln(1-x)$，为$0\cdot\infty$型
解题思路：直接化成分式使用洛必达法则计算较繁琐，优先利用等价无穷小将复杂因式替换为简单因式。

等价无穷小回顾：
- 当$x \to 0$时，$\ln(1+x) \sim x$；
- 当$x \to 1$时，$\ln(1+(x-1)) \sim x-1$，即$\ln x \sim x-1 \ (x \to 1)$。

解：
$$
\begin{align*}
\text{原式} &= \lim_{x \to 1^-} \ln x \ln(1-x) \\
&= \lim_{x \to 1^-} (x-1)\ln(1-x)
\end{align*}
$$
令$1-x = t$，当$x \to 1^-$时，$t \to 0^+$。

定义域与趋近趋势分析：
- $\ln x$的定义域为$x>0$；
- $t \to 0^+$时$t>0$，$t \to 0^-$时$t<0$；
- 本题中$x \to 1^-$时，$x-1 \to 0^-$，$1-x \to 0^+$。

---

# B 函数极限题型总结_第8页.png

$$
\begin{aligned}
\text{原式} &= -\lim_{t \to 0^+} t\ln t \\
&= -\lim_{t \to 0^+} \frac{\ln t}{\frac{1}{t}} \\
&\xlongequal{\text{洛必达法则}} -\lim_{t \to 0^+} \frac{\frac{1}{t}}{-\frac{1}{t^2}} \\
&= \lim_{t \to 0^+} t \\
&= 0
\end{aligned}
$$

当$\alpha>0$时，对$0\cdot\infty$型极限$\lim_{x \to 0^+} x^\alpha \ln x$，用洛必达法则计算：
$$
\begin{aligned}
\lim_{x \to 0^+} x^\alpha \ln x &= \lim_{x \to 0^+} \frac{\ln x}{x^{-\alpha}} = \lim_{x \to 0^+} \frac{x^{-1}}{-\alpha x^{-\alpha-1}} \\
&= -\frac{1}{\alpha}\lim_{x \to 0^+} x^\alpha = 0
\end{aligned}
$$

推广结论：对任意$\alpha>0,\beta>0$，有
$$\Rightarrow \lim_{x \to 0^+} x^\alpha (\ln x)^\beta = 0$$

对应之前总结的$n \to \infty$时无穷大的增长速度阶的比较：
当$n \to \infty$时，无穷大增长速度满足：
$$\ln^\alpha n \ll n^\beta \ll a^n \ll n! \ll n^n \quad (\alpha,\beta>0,a>1)$$
即幂函数$x^\alpha$的变化速度远快于对数函数的幂$(\ln x)^\alpha$的变化速度。

当$x \to 0^+$时，$\ln x$趋向$-\infty$（绝对值趋向$+\infty$）的速度相对于$x$趋向$0$的速度极慢：
$\ln x$的变化速度非常慢，以至于$x \to 0^+$时，对$x$的任意正次幂，哪怕是幂次极低、$x^\alpha$趋向$0$速度极慢的情况，$x^\alpha$都可以抵消掉$\ln x$趋向无穷的趋势，使得乘积为0。

## 例1.9 求极限$I = \lim_{x \to 0} x\left[\frac{10}{x}\right]$，其中$[\cdot]$为取整符号
求解思路：取整函数相关极限使用夹逼准则。

对任意实数$t$，取整函数满足不等式：
$$t - 1 < [t] \leq t$$
令$t = \frac{10}{x}$，代入得：
$$\frac{10}{x} - 1 < \left[\frac{10}{x}\right] \leq \frac{10}{x}$$

分左右极限讨论：
1.  当$x \to 0^+$时，$x>0$，不等式三边同乘正数$x$，不等号方向不变：
    $$x\left(\frac{10}{x} - 1\right) < x\left[\frac{10}{x}\right] \leq x\cdot \frac{10}{x}$$
    化简得：
    $$10 - x < x\left[\frac{10}{x}\right] \leq 10$$
    当$x \to 0^+$时，左边$10-x \to 10$，右边为常数10，由夹逼准则得：
    $$\lim_{x \to 0^+} x\left[\frac{10}{x}\right] = 10$$

2.  当$x \to 0^-$时，$x<0$，不等式三边同乘负数$x$，不等号方向反转：
    $$x\left(\frac{10}{x} - 1\right) > x\left[\frac{10}{x}\right] \geq x\cdot \frac{10}{x}$$
    化简得：
    $$10 - x > x\left[\frac{10}{x}\right] \geq 10$$
    当$x \to 0^-$时，左边$10-x \to 10$，右边为常数10，由夹逼准则得：
    $$\lim_{x \to 0^-} x\left[\frac{10}{x}\right] = 10$$

左右极限相等，因此$\Rightarrow I=10$。

---

# B 函数极限题型总结_第9页.png

## (2) $\boldsymbol{\infty-\infty}$型不定式极限
### 求解方法
$\infty-\infty$型为加减形式的不定式，核心是将其转化为$\frac{0}{0},\frac{\infty}{\infty},0\cdot\infty$型的乘除不定式，再选择方法求解：
1.  若表达式含有分母：直接通分即可转化为分式不定式，适用于$\frac{1}{\square}-\frac{1}{\square}$型的加减结构；使用洛必达法则求解较为基础常规，使用等价无穷小替换结合泰勒公式求解效率更高。
2.  若表达式不含分母：可提取公因式后构造分式分母，或作倒代换$t=\frac{1}{x}$，构造出分母后再通分转化。

---

### 例1.30（有分母情形）
计算极限：
$$\lim_{x \to 0} \left( \frac{1}{\ln(1+x)} - \frac{1}{x} \right)$$
解：
先通分转化为$\frac{0}{0}$型：
$$
\begin{align*}
\lim_{x \to 0} \left( \frac{1}{\ln(1+x)} - \frac{1}{x} \right) &= \lim_{x \to 0} \frac{x - \ln(1+x)}{x \cdot \ln(1+x)}
\end{align*}
$$
利用等价无穷小：$x\to0$时$\ln(1+x) \sim x$，对分母作替换；代入$\ln(1+x)$的泰勒展开$\ln(1+x) = x - \frac{x^2}{2} + \frac{x^3}{3} + o(x^3)$：
$$
\begin{align*}
&= \lim_{x \to 0} \frac{x - \left( x - \frac{x^2}{2} + o(x^2) \right)}{x^2} \\
&= \lim_{x \to 0} \frac{\frac{1}{2}x^2 + o(x^2)}{x^2} \\
&= \frac{1}{2}
\end{align*}
$$

---

### 例1.13
计算极限：
$$\lim_{x \to 0} \left( \frac{1}{x} - \frac{1}{\sin x} \right)$$
解：
通分转化为$\frac{0}{0}$型：
$$
\begin{align*}
\lim_{x \to 0} \left( \frac{1}{x} - \frac{1}{\sin x} \right) &= \lim_{x \to 0} \frac{\sin x - x}{x \sin x}
\end{align*}
$$
利用等价无穷小：$x\to0$时$\sin x \sim x$，对分母作替换；代入$\sin x$的泰勒展开$\sin x = x - \frac{x^3}{3!} + o(x^3)$：
$$
\begin{align*}
&= \lim_{x \to 0} \frac{\left( x - \frac{x^3}{6} + o(x^3) \right) - x}{x^2} \\
&= \lim_{x \to 0} \frac{-\frac{1}{6}x^3 + o(x^3)}{x^2} \\
&= 0
\end{align*}
$$
注：该结果本质是分子为$x$的3阶无穷小，分母为$x$的2阶无穷小，高阶无穷小与低阶无穷小的比值极限为0。

---

### 例1.14
计算极限：
$$\lim_{x \to 0} \left( \frac{1}{x} - \frac{1}{\ln(x+\sqrt{1+x^2})} \right)$$
注：本题用到前置结论：$\left[\ln(x+\sqrt{1+x^2})\right]' = \frac{1}{\sqrt{1+x^2}}$。
解：
通分转化为$\frac{0}{0}$型：
$$
\begin{align*}
\lim_{x \to 0} \left( \frac{1}{x} - \frac{1}{\ln(x+\sqrt{1+x^2})} \right) &= \lim_{x \to 0} \frac{\ln(x+\sqrt{1+x^2}) - x}{x \cdot \ln(x+\sqrt{1+x^2})}
\end{align*}
$$
利用等价无穷小：$x\to0$时$\ln(x+\sqrt{1+x^2}) \sim x$，因此分母$x \cdot \ln(x+\sqrt{1+x^2}) \sim x^2$；对分子分母使用洛必达法则求导，结合等价无穷小替换分母（$x\to0$时分母求导后$\ln(x+\sqrt{1+x^2}) + \frac{x}{\sqrt{1+x^2}} \sim 2x$）：
$$
\begin{align*}
&= \lim_{x \to 0} \frac{\frac{1}{\sqrt{1+x^2}} - 1}{2x}
\end{align*}
$$
利用等价无穷小$(1+u)^\alpha -1 \sim \alpha u \ (u\to0)$，令$u=x^2,\alpha=-\frac{1}{2}$，则$\frac{1}{\sqrt{1+x^2}} -1 = (1+x^2)^{-1/2} -1 \sim -\frac{1}{2}x^2$，代入得：
$$
\begin{align*}
&= \lim_{x \to 0} \frac{-\frac{1}{2}x^2}{2x} \\
&= \lim_{x \to 0} \left( -\frac{1}{4}x \right) \\
&= 0
\end{align*}
$$

---

# B 函数极限题型总结_第10页.png

## 例1.31 $\infty-\infty$型（无分母情形）
求极限：
$$\lim_{x \to +\infty}\left[x^2\left(e^{\frac{1}{x}}-1\right)-x\right]$$
解：
$$
\begin{align*}
\text{原式}&=\lim_{x \to +\infty} x\left[x\left(e^{\frac{1}{x}}-1\right)-1\right]\\
&=\lim_{x \to +\infty} \frac{x\left(e^{\frac{1}{x}}-1\right)-1}{\frac{1}{x}}
\end{align*}
$$
令$x=\frac{1}{t}$，当$x\to+\infty$时$t\to0^+$，变量替换得：
$$
\begin{align*}
&=\lim_{t \to 0^+} \frac{\frac{1}{t}\left(e^t -1\right)-1}{t}\\
&=\lim_{t \to 0^+} \frac{e^t -1 -t}{t^2}
\end{align*}
$$
利用$t\to0$时的泰勒展开公式：
$$e^t = 1 + t + \frac{t^2}{2!} + o(t^2)$$
即$e^t -1 -t = \frac{t^2}{2!} + o(t^2)$，满足等价无穷小关系$e^t -1 -t \sim \frac{t^2}{2!}\ (t\to0)$，代入得：
$$
\begin{align*}
&=\lim_{t \to 0^+} \frac{\frac{1}{2!}t^2 + o(t^2)}{t^2}\\
&=\frac{1}{2}
\end{align*}
$$

## 例1.15 $\infty-\infty$型极限（等价无穷小的应用）
注：等价无穷小的使用对此类问题十分重要
求极限：
$$\lim_{x \to 1} \left( \frac{x}{x-1} - \frac{1}{\ln x} \right) \quad (\infty-\infty\text{型})$$
解：先通分转化为$\frac{0}{0}$型极限：
$$
\begin{align*}
\text{原式}&=\lim_{x \to 1} \frac{x\ln x -x +1}{(x-1)\ln x}
\end{align*}
$$
当$x\to1$时$x-1\to0$，由等价无穷小基本公式$\ln(1+u)\sim u\ (u\to0)$，令$u=x-1$可得$\ln x = \ln(1+(x-1)) \sim x-1$，对分母的乘除因子做等价无穷小替换：
$$
\begin{align*}
&=\lim_{x \to 1} \frac{x\ln x -x +1}{(x-1)^2}
\end{align*}
$$
应用洛必达法则求导：
$$
\begin{align*}
&\xlongequal{\text{洛必达法则}} \lim_{x \to 1} \frac{\ln x + 1 - 1}{2(x-1)}\\
&=\lim_{x \to 1} \frac{\ln x}{2(x-1)}
\end{align*}
$$
再次使用等价无穷小$\ln x \sim x-1\ (x\to1)$替换：
$$
\begin{align*}
&=\lim_{x \to 1} \frac{x-1}{2(x-1)}\\
&=\frac{1}{2}
\end{align*}
$$

---

# B 函数极限题型总结_第11页.png

## $\boldsymbol{\infty^0}$、$\boldsymbol{0^0}$型幂指函数极限
“$\infty^0$”“$0^0$”型未定式属于幂指函数$u(x)^{v(x)}$的极限类型。
计算方法：利用指数对数恒等式
$$a^b = e^{b\ln a}$$
将幂指函数转化为指数形式，通过计算指数部分的极限得到原极限。
### 例32
求极限 $\lim\limits_{x \to +\infty} \left(x+\sqrt{1+x^2}\right)^{\frac{1}{x}}$，该极限为$\infty^0$型未定式。
计算过程：
$$
\begin{align*}
\lim_{x \to +\infty} \left(x+\sqrt{1+x^2}\right)^{\frac{1}{x}} &= \lim_{x \to +\infty} e^{\frac{1}{x}\ln\left(x+\sqrt{1+x^2}\right)} \\
&= e^{\lim\limits_{x \to +\infty} \frac{\ln\left(x+\sqrt{1+x^2}\right)}{x}}
\end{align*}
$$
指数部分为$\frac{\infty}{\infty}$型未定式，使用洛必达法则计算：
对数部分求导结果为：
$$\left[\ln\left(x+\sqrt{1+x^2}\right)\right]' = \frac{1}{\sqrt{1+x^2}}$$
因此指数部分极限：
$$
\lim_{x \to +\infty} \frac{\ln\left(x+\sqrt{1+x^2}\right)}{x} = \lim_{x \to +\infty} \frac{\frac{1}{\sqrt{1+x^2}}}{1} = 0
$$
原极限结果：
$$
\lim_{x \to +\infty} \left(x+\sqrt{1+x^2}\right)^{\frac{1}{x}} = e^0 = 1
$$
## $\boldsymbol{1^\infty}$型幂指函数极限
“$1^\infty$”型未定式是**无限趋向于1的数的无穷大次幂**。
通用计算方法：利用指数对数恒等式
$$\lim a^b = e^{\lim b\ln a}$$
简化技巧：当$a \to 1$时，有等价无穷小$\ln a \sim a-1$，因此公式可简化为：
$$\lim_{\substack{a \to 1 \\ b \to \infty}} a^b = e^{\lim\limits_{\substack{a \to 1 \\ b \to \infty}} b(a-1)}$$
注：$1^\infty$型未定式对应$a^b$满足$\begin{cases} b \to \infty \\ a \to 1 \end{cases}$。
### 例33
利用上述简化公式$\lim\limits_{\substack{a \to 1 \\ b \to \infty}} a^b = e^{\lim\limits_{\substack{a \to 1 \\ b \to \infty}} b(a-1)}$，求极限：
$$\lim_{x \to 0} \left( \frac{e^x + e^{2x} + e^{3x}}{3} \right)^{\frac{e}{x}}$$
类型判断（$x \to 0$时）：
1.  $e^x \to 1$，$e^{2x} \to 1$，$e^{3x} \to 1$
2.  因此底数$\frac{e^x + e^{2x} + e^{3x}}{3} \to \frac{1+1+1}{3} = 1$
3.  指数$\frac{e}{x} \to \infty$
因此该极限为$1^\infty$型未定式，可使用上述简化公式计算。

---

# B 函数极限题型总结_第12页.png

计算极限$\lim\limits_{x \to 0} \left( \frac{e^x + e^{2x} + e^{3x}}{3} \right)^{\frac{e}{x}}$：
$$
\begin{align*}
\text{原式} &= e^{\lim\limits_{x \to 0} \frac{e}{x} \left( \frac{e^x + e^{2x} + e^{3x}}{3} - 1 \right)} \\
&= e^{\lim\limits_{x \to 0} \frac{e}{x} \cdot \frac{e^x - 1 + e^{2x} - 1 + e^{3x} - 1}{3}} \\
&= e^{\lim\limits_{x \to 0} \frac{e}{x} \left( \frac{e^x - 1}{3} + \frac{e^{2x} - 1}{3} + \frac{e^{3x} - 1}{3} \right)} \\
&= e^{\lim\limits_{x \to 0} \frac{e}{x} \cdot \frac{6x}{3}} \\
&= e^{2e}
\end{align*}
$$

## 1.16 不是未定式的幂指函数
幂指函数恒等变形公式：
$$a^b = e^{b \ln a}$$

例题：计算极限$\lim\limits_{x \to 0} \frac{(1+x)^x - 1}{1-\cos x}$
当$x \to 0$时，用到以下等价无穷小：
- $e^u - 1 \sim u \quad (u \to 0)$
- $1 - \cos x \sim \frac{1}{2}x^2$
- $\ln(1+x) \sim x$

计算过程：
$$
\begin{align*}
\text{原式} &= \lim_{x \to 0} \frac{e^{x\ln(1+x)} - 1}{1-\cos x} \\
&= \lim_{x \to 0} \frac{x\ln(1+x)}{\frac{1}{2}x^2} \\
&= \lim_{x \to 0} \frac{x \cdot x}{\frac{1}{2}x^2} \\
&= 2
\end{align*}
$$

## （5）泰勒公式，一站直达
### 例134
设当$x \to 0$时，$e^x - (ax^2 + bx + 1)$是比$x^2$高阶的无穷小，求$a,b$的值。

根据高阶无穷小的定义，有：
$$\lim_{x \to 0} \frac{e^x - (ax^2 + bx + 1)}{x^2} = 0$$

> 上下同阶原则：将函数展开到与分母相同的阶数，此处展开到$x^2$阶即可。$e^x$的麦克劳林展开式为：
> $$e^x = 1 + x + \frac{x^2}{2} + o(x^2)$$

将展开式代入极限式，整理得：
$$
\lim_{x \to 0} \frac{(1-b)x + \left( \frac{1}{2} - a \right)x^2 + o(x^2)}{x^2} = 0
$$

要使该极限为0，分子作为无穷小的阶数必须高于分母$x^2$，即分子不能包含低阶项（$x$项）和同阶项（$x^2$项），仅保留高阶无穷小$o(x^2)$，因此低阶、同阶项的系数必须全部为0：
$$
\begin{cases}
1 - b = 0 \\
\frac{1}{2} - a = 0
\end{cases}
$$

解得$b=1$，$a=\frac{1}{2}$，此时$\lim\limits_{x \to 0} \frac{o(x^2)}{x^2} = 0$，满足高阶无穷小的要求。