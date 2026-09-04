# 1 极限的定义2.0_第1页.png

## 邻域的基本概念
为了玩“极限”我们引入“邻域”。
若$\varphi>0$，左侧有数轴示意图，标注点$x_0-\varphi$、$x_0$、$x_0+\varphi$。
开区间$(x_0-\varphi, x_0+\varphi)$为$x_0$的**邻域**，是一个“开区间”，又叫“$x_0$的附近”。
右侧为单侧邻域内容，下方有数轴示意图，标注点$x_0-\varphi$、$x_0$、$x_0+\varphi$：
- 左邻域：集合表示为$\{x \mid x_0 - x < \varphi\}$，对应数轴上$x_0-\varphi$到$x_0$的区间。
- 右邻域：集合表示为$\{x \mid x - x_0 < \varphi\}$，对应数轴上$x_0$到$x_0+\varphi$的区间。
邻域记作：
$$U(x_0, \varphi) = \{x \mid x_0-\varphi < x < x_0+\varphi\} = \{x \mid |x - x_0| < \varphi\}$$
---
### 去心邻域
什么是去心邻域？去心邻域如何表示？
去心邻域不包含中心点$x_0$，即满足$x \neq x_0$，其集合表示为：
$$\mathring{U}(x_0, \varphi) = \{x \mid 0 < |x - x_0| < \varphi\}$$
---
### 思考问题
1.  这里的$\varphi$是个什么样的东西？
2.  极限是什么？

---

# 1 极限的定义2.0_第2页.png

## $x\to x_0$时函数极限的$\varepsilon$-$\delta$定义
- **前提**：若$f(x)$在$(x_0-\delta, x_0)\cup(x_0, x_0+\delta)$上有定义。
  （附去心邻域数轴示意图：数轴上标注$x_0-\delta$、$x_0$、$x_0+\delta$，$x_0$为空心点，去心邻域对应的两个开区间以弧线标注）
- 若存在常数$A$，对于任给$\varepsilon>0$，存在$\delta>0$满足：当$0<|x-x_0|<\delta$时，有$|f(x)-A|<\varepsilon$。
  上述定义与极限记法等价：
  $$
  \begin{cases}
  \forall \varepsilon>0 \\
  \exists \delta>0,\ \text{当 }0<|x-x_0|<\delta \text{ 时}, \\
  \text{有 }|f(x)-A|<\varepsilon
  \end{cases}
  \\
  \Updownarrow
  \\
  \lim_{x\to x_0} f(x) = A
  $$
- 则称$A$为$f(x)$当$x\to x_0$时的极限。
  说明：
  1.  $x$无限趋近于$x_0$，过程中满足$x\neq x_0$；
  2.  $f(x)$无限趋近于$A$，过程中满足$f(x)\neq A$；
  3.  由极限过程中$x\neq x_0$，可得$f(x)\neq A$。

---

# 1 极限的定义2.0_第3页.png

## 函数极限的$\boldsymbol{\varepsilon\text{-}\delta}$定义
$\forall \varepsilon>0,\exists\delta>0$，当$0<|x-x_0|<\delta$时，有$|f(x)-A|<\varepsilon$ $\iff$ $\lim\limits_{x\to x_0}f(x)=A$。

$\exists\delta>0$，有$x_0-\delta \to x_0 \gets x_0+\delta$，对应$0<|x-x_0|<\delta$时$|f(x)-A|<\varepsilon$；
$\forall \varepsilon>0$，有$A-\varepsilon \to A \gets A+\varepsilon$，对应$|f(x)-A|<\varepsilon$。

则$\lim\limits_{x\to x_0}f(x)=A$，即$x\to x_0$时，有$f(x)\to A$。

**函数极限几何意义示意图**：
纵向标注：$f(x)=A+\varepsilon$，与$f(x)=A$纵向间距为$\varepsilon$；$f(x)=A$（水平虚线）；$f(x)=A-\varepsilon$，与$f(x)=A$纵向间距为$\varepsilon$。
横向标注：$x=x_0-\delta$，与$x=x_0$横向间距为$\delta$；$x=x_0$（竖直虚线）；$x=x_0+\delta$，与$x=x_0$横向间距为$\delta$。

$\delta=?\quad A=?\quad x_0=?$

---

# 1 极限的定义2.0_第4页.png

## 函数极限概念相关疑问
- $\varphi = ?\quad A = ?\quad x_0 = ?$
关于$x$，这里无限趋近$A$、但又不等于$A$的数，已不属于实数范围了，$x$属于超实数。
$$\lim_{x \to x_0} f(x) = A$$
$f(x)$也属于超实数。
$f(x)$无限趋近于$A$，$f(x) \neq f(x_0)$。
$$\lim_{x \to x_0} f(x) = :$$
当$x$无限趋近于$x_0$，$x \neq x_0$时，
$f(x)$无限趋近于谁？$f(x) \neq$谁？
- 这里$\lim\limits_{x \to x_0} f(x) =$ <u>超实数</u>还是<u>实数</u>？
- $A = f(x_0)$吗？

---

# 1 极限的定义2.0_第5页.png

## 进一步理解
- 邻域上标注点$x_0-\delta$、$x_0$、$x_0+\delta$，邻域半径为$\delta$：
  $\delta$：某一值，某一距离。
- $\exists \delta$：$x$位于$x_0$的去心邻域内，$x$到$x_0$的距离趋近于0，$x$无限趋近于$x_0$；
  则有
  $\forall \varepsilon$：$f(x)$位于$A$的邻域内，邻域上标注点$A-\varepsilon$、$A$、$A+\varepsilon$，$f(x)$到$A$的距离趋近于0，$f(x)$无限趋近于$A$。
  上述直观过程等价于：
$$\lim_{x \to x_0} f(x) = A$$
- 极限思想示例：
$$\lim_{x \to 0} \frac{x-\sin x}{x^3} = \frac{(x-0) - (\sin x - 0)}{x^3} = \frac{1}{6} = \frac{x\text{到}\sin x\text{的距离}}{x^3\text{到}0\text{的距离}}$$
，极限思想！

---

# 1 极限的定义2.0_第6页.png

## 函数极限的超实数直观解释
$$\lim_{x \to x_0} f(x) = A$$
对应函数趋势示意图说明：
- 坐标系横轴为$x$轴，纵轴为$f(x)$轴，图中绘制函数曲线展示$x \to x_0$时$f(x) \to A$的趋势。
- 纵轴沿轴从下到上依次划分为：比$A$小的所有实数、以$A$为标准的超实数、点$A$、以$A$为标准的超实数、比$A$大的所有实数。
- 横轴沿轴从左到右依次划分为：比$x_0$小的所有实数、以$x_0$为标准的超实数、点$x_0$、以$x_0$为标准的超实数、比$x_0$大的所有实数。

### 极限示例
若
$$\lim_{x \to 0} \frac{x-\sin x}{x^3} = A$$
则对应数轴示意图说明：数轴以向右为正方向，标注有点$A$，展示$x \to 0$时$\frac{x-\sin x}{x^3}$的取值无限接近$A$。

---

# 1 极限的定义2.0_第7页.png

## 超实数的引入
为了让$\infty$在数轴上表示，引入**超实数**。
数系扩充路径：
$$\text{有理数}\xrightarrow{\sqrt{2}}\text{实数}\mathbb{R}\begin{cases}
\xrightarrow{\sqrt{-1}}\text{复数}\\
\xrightarrow{\infty}\text{超实数}
\end{cases}$$
任何实数边上都有无数个超实数。
超实数的分解：对任意超实数$x$，有
$$x = \operatorname{std}(x) + \underbrace{x - \operatorname{std}(x)}_{\text{无穷量}}$$
其中$\operatorname{std}(x)$为$x$对应的标准实数。

## 超实数解释函数极限示例
eg：
$$\lim_{x \to 2} f(x) = 3$$
- x轴示意图对应文字说明：超实数$x$无限趋近于实数$2$。
- 函数值轴示意图对应文字说明：超实数$f(x)$无限趋近于实数$3$。

---

# 1 极限的定义2.0_第8页.png

## 极限的概念与极限和无穷小的关系
> 本次回答了前面的问题：
> ① $\lim\limits_{x \to x_0} f(x) = A$（极限值为实数）
> ② $f(x_0) = A$
> ③ 即为无穷小量

（实数轴示意图：标注点$3$，左侧区域标注“任何比3小的实数”，右侧区域标注“任何比3大的实数”，3的邻域位置标注密集刻度）

3周围有许多以3为标准的超实数<u>≠3</u>，满足：
$$\text{任何比3小的实数} < \text{上述超实数} < \text{任何比3大的实数}$$

$f(2)=3 \implies 2 \to f(\quad) \to 3$，这是函数的对应关系。

$$\lim_{x \to 2} f(x) = 3 \implies \begin{cases} 
\text{当} \ x \ \text{无限趋近于} \ 2 \ \text{时} \\
f(x) \ \text{无限趋近于} \ 3
\end{cases} \quad \text{这是极限的逻辑关系}.$$

eg：对于$\lim\limits_{x \to 2} f(x) = 3$：
- $f(x)$无限趋近于3，但$f(x) \neq 3$
- $x$无限趋近于2，但$x \neq 2$

$f(x)$就为3周围的超实数之一，$x$为2周围的许多超实数之一。

对$f(x)$做分解：
$$
\begin{aligned}
f(x) &= \operatorname{std}(f(x)) + f(x) - \operatorname{std}(f(x)) \\
&= 3 + \underbrace{f(x) - \operatorname{std}(f(x))}_{\text{无穷小量，对应} \ f(x) \to 3} \\
&= 3 + \underbrace{f(x) - 3}_{\text{$f(x)$与3之间的无穷小距离}}
\end{aligned}
$$

---

# 1 极限的定义2.0_第9页.png

## $x \to x_0$型函数极限分类对照表
| 自变量趋近方式 | $f(x) \to A$ | $f(x) \to \infty$ | $f(x) \to +\infty$ | $f(x) \to -\infty$ |
| --- | --- | --- | --- | --- |
| $x \to x_0$ |  |  |  |  |
| $x \to x_0^+$<br>（右极限） |  |  |  |  |
| $x \to x_0^-$<br>（左极限） |  |  |  |  |

---

# 1 极限的定义2.0_第10页.png

## 自变量趋于无穷时的函数极限分类
|          | $f(x)\to A$ | $f(x)\to \infty$ | $f(x)\to +\infty$ | $f(x)\to -\infty$ |
|----------|-------------|------------------|-------------------|-------------------|
| $x\to \infty$ |             |                  |                   |                   |
| $x\to +\infty$ |            |                  |                   |                   |
| $x\to -\infty$ |            |                  |                   |                   |

---

# 1 极限的定义2.0_第11页.png

## 函数极限的定义
### $x \to x_0$时的函数极限
1.  $f(x) \to A$：
    $\forall \varepsilon > 0,\ \exists \delta > 0$
    当$0 < |x - x_0| < \delta$时，
    有$|f(x) - A| < \varepsilon$。
2.  $f(x) \to \infty$：
    $\forall M > 0,\ \exists \delta > 0$
    当$0 < |x - x_0| < \delta$时，
    有$|f(x)| > M$。
3.  $f(x) \to +\infty$：
    $\forall M > 0,\ \exists \delta > 0$
    当$0 < |x - x_0| < \delta$时，
    有$f(x) > M$。
4.  $f(x) \to -\infty$：
    $\forall M > 0,\ \exists \delta > 0$
    当$0 < |x - x_0| < \delta$时，
    有$-M > f(x)$。
### $x \to x_0^+$（右极限）时的函数极限
1.  $f(x) \to A$：
    $\forall \varepsilon > 0,\ \exists \delta > 0$
    当$0 < x - x_0 < \delta$时，
    有$|f(x) - A| < \varepsilon$。
2.  $f(x) \to \infty$：
    $\forall M > 0,\ \exists \delta > 0$
    当$0 < x - x_0 < \delta$时，
    有$|f(x)| > M$。
3.  $f(x) \to +\infty$：
    $\forall M > 0,\ \exists \delta > 0$
    当$0 < x - x_0 < \delta$时，
    有$f(x) > M$。
4.  $f(x) \to -\infty$：
    $\forall M > 0,\ \exists \delta > 0$
    当$0 < x - x_0 < \delta$时，
    有$-M > f(x)$。

---

# 1 极限的定义2.0_第12页.png

## $x \to x_0^-$（左极限）相关定义
1.  左极限$\boldsymbol{\lim\limits_{x \to x_0^-} f(x) = A}$的$\varepsilon$-$\delta$定义：
$$\forall \varepsilon>0,\ \exists \delta>0$$
当$0 < x_0 - x < \delta$时，有
$$|f(x) - A| < \varepsilon$$

2.  $x \to x_0^-$时$f(x)$为无穷大的定义：
$$\forall M>0,\ \exists \delta>0$$
当$0 < x_0 - x < \delta$时，有
$$|f(x)| > M$$

3.  $x \to x_0^-$时$f(x)$为正无穷大的定义：
$$\forall M>0,\ \exists \delta>0$$
当$0 < x_0 - x < \delta$时，有
$$f(x) > M$$

4.  $x \to x_0^-$时$f(x)$为负无穷大的定义：
$$\forall M>0,\ \exists \delta>0$$
当$0 < x_0 - x < \delta$时，有
$$f(x) < -M$$

## $x \to \infty$相关极限定义
1.  极限$\boldsymbol{\lim\limits_{x \to \infty} f(x) = A}$的$\varepsilon$-$N$定义：
$$\forall \varepsilon>0,\ \exists N>0$$
当$|x| > N$时，有
$$|f(x) - A| < \varepsilon$$

2.  $x \to \infty$时$f(x)$为无穷大的定义：
$$\forall M>0,\ \exists N>0$$
当$|x| > N$时，有
$$|f(x)| > M$$

3.  $x \to \infty$时$f(x)$为正无穷大的定义：
$$\forall M>0,\ \exists N>0$$
当$|x| > N$时，有
$$f(x) > M$$

4.  $x \to \infty$时$f(x)$为负无穷大的定义：
$$\forall M>0,\ \exists N>0$$
当$|x| > N$时，有
$$f(x) < -M$$

---

# 1 极限的定义2.0_第13页.png

## 自变量趋于无穷时函数极限与无穷大的定义
### $x \to +\infty$
$$\forall \varepsilon>0,\ \exists N>0$$
当
$x>N$时
有
$$|f(x)-A|<\varepsilon$$
$$\forall M>0,\ \exists N>0$$
当
$x>N$时
有
$$|f(x)|>M$$
$$\forall M>0,\ \exists N>0$$
当
$x>N$时
有
$$f(x)>M$$
$$\forall M>0,\ \exists N>0$$
当
$x>N$时
有
$$-M > f(x)$$
### $x \to -\infty$
$$\forall \varepsilon>0,\ \exists N>0$$
当
$-N > x$时
有
$$|f(x)-A|<\varepsilon$$
$$\forall M>0,\ \exists N>0$$
当
$-N > x$时
有
$$|f(x)|>M$$
$$\forall M>0,\ \exists N>0$$
当
$-N > x$时
有
$$f(x)>M$$
$$\forall M>0,\ \exists N>0$$
当
$-N > x$时
有
$$-M > f(x)$$

---

# 1 极限的定义2.0_第14页.png

## $x \to x_0$时函数有限极限的$\varepsilon$-$\delta$定义
当$x \to x_0$时，$f(x) \to A$，其严格定义与直观语义对应如下：
- $\forall \varepsilon > 0,\ \exists \delta > 0$ —— 任给$\varepsilon>0$，存在$\delta>0$
- 当 $0<|x-x_0|<\delta$ 时 —— 当$x$无限趋近于$x_0$时
- 有 $|f(x)-A|<\varepsilon$ —— 有$f(x)$无限趋近于$A$

## $x \to x_0$时函数为无穷大量的定义
当$x \to x_0$时，$f(x) \to \infty$，其直观描述为：
存在$\delta>0$，当$x$无限趋近于$x_0$时，可推出：对$\forall M>0$，都有$|f(x)|>M$。
上述定义等价于标准极限记法：
$$\lim_{x \to x_0} f(x) = \infty = \mathrm{Std}(f(x))$$

---

# 1 极限的定义2.0_第15页.png

## 无穷大的概念与定义
$\infty$：无穷，为超实数，变化趋势为 $-\infty \xleftarrow{f(x)} \xrightarrow{} +\infty$
$x \to x_0$时$f(x)$为无穷大的M-δ定义：
$$
\left.
\begin{aligned}
&\forall M>0,\ \exists \delta>0\\
&\text{当 }0<|x-x_0|<\delta \text{ 时}\\
&\text{有 }|f(x)|>M
\end{aligned}
\right\}
$$
对应数轴示意图：标注$f(x)$、$\infty$、$f(x)$，相关性质：
- $|\infty| >$ 任何实数
- $|\infty| > |f(x)| >$ 任何实数
- $\Rightarrow$ 此时$|f(x)| >$ 任何实数
正无穷大（$f(x) \to +\infty$）：
$+\infty > f(x) >$ 所有正实数，对应数轴示意图：$f(x)$沿数轴箭头指向$+\infty$，表示$f(x)$趋向$+\infty$
负无穷大（$f(x) \to -\infty$）：
所有正实数 $> f(x) > -\infty$，对应数轴示意图：$f(x)$沿数轴箭头指向$-\infty$，表示$f(x)$趋向$-\infty$
## 单侧极限
右极限：
$x \to x_0^+$
$f(x) \to A$
对应数轴示意图：标注$x$与$x_0^+$，箭头指向$x_0^+$，表示$x$从右侧趋近于$x_0$的过程
左极限：
对应数轴示意图：标注$x_0^-$与$x$，箭头指向$x_0^-$，表示$x$从左侧趋近于$x_0$的过程（即$x \to x_0^-$）
## $x \to \infty$时的函数极限
$x \to \infty$
$f(x) \to A$
对应数轴示意图：数轴两端标注$-\infty$与$+\infty$，箭头分别指向$-\infty$和$+\infty$，标注$x$，表示$|x|$无限增大的过程
相关性质：
- $|\infty| > |x| >$ 任何实数
- $+\infty > x >$ 所有实数，对应$x \to +\infty$
- 所有实数 $> x > -\infty$，对应$x \to -\infty$，对应数轴示意图：$x$沿数轴箭头指向$-\infty$，表示$x$趋向$-\infty$

---

# 1 极限的定义2.0_第16页.png

在不同场合
$$
\begin{cases}
在不同场景理解\\
做不同的题理解
\end{cases}
$$

## 极限的定义题

1.9 已知$\lim\limits_{x \to 0} \frac{f(x)}{x}$存在，且函数$f(x)=\ln(1+x)+2x$，$\lim\limits_{x \to 0} \frac{f(x)}{\sin x}$，则$\lim\limits_{x \to 0} \frac{f(x)}{x}=$\underline{\qquad}。

∵题上说“$\lim\limits_{x \to 0} \frac{f(x)}{x}$存在”
∴有$\lim\limits_{x \to 0} \frac{f(x)}{x} = \mathrm{std}\left( \frac{f(x)}{x} \right)$

（极限趋近示意图：示意$x \to 0$时，$\frac{f(x)}{x}$从两侧趋近于作为定值的极限值）

---

# 1 极限的定义2.0_第17页.png

解：
$$\frac{f(x)}{x} = \frac{\ln(1+x)}{x} + 2\lim_{x \to 0} \frac{f(x)}{\sin x}$$
建立方程（这里的$\frac{f(x)}{x}$为实数）
（这里的$\frac{f(x)}{\sin x}$为超实数）

$$\frac{f(x)}{x} = \frac{\ln(1+x)}{x} + 2\lim_{x \to 0} \left( \frac{f(x)}{x} \cdot \frac{x}{\sin x} \right)$$
“后面会讲”
$$\lim_{x \to 0} \frac{\sin x}{x} = 1 = std\left( \frac{\sin x}{x} \right)$$

$$\frac{f(x)}{x} = \frac{\ln(1+x)}{x} + 2\lim_{x \to 0} \frac{f(x)}{x} \cdot \frac{x}{\sin x}$$
$$\lim_{x \to 0} std\left( \frac{f(x)}{x} \right) = std\left( \frac{f(x)}{x} \right)$$
因为$std\left( \frac{f(x)}{x} \right)$是实数。
又对任意实数$A$，有$A = std(A) + A - std(A) = A + A - A = A$，即实数的标准部分为其自身。

$$\frac{f(x)}{x} = \frac{\ln(1+x)}{x} + 2\ std\left( \frac{f(x)}{x} \right)$$
$$\Rightarrow \lim_{x \to 0} \frac{f(x)}{x} = \lim_{x \to 0} \frac{\ln(1+x)}{x} + 2\ std\left( \frac{f(x)}{x} \right)$$
$$\Rightarrow std\left( \frac{f(x)}{x} \right) = \lim_{x \to 0} \frac{\ln(1+x)}{x} + 2std\left( \frac{f(x)}{x} \right)$$

（数轴示意图：标注0点位置，说明$\lim\limits_{x\to0}\frac{\ln(1+x)}{x}$为0点附近的极限，$std\left( \frac{\ln(1+x)}{x} \right)=1$，旁注“为啥是在0旁边？”，注释“之后讲”）

代入$\lim\limits_{x\to0}\frac{\ln(1+x)}{x}=1$：
$$std\left( \frac{f(x)}{x} \right) = 1 + 2std\left( \frac{f(x)}{x} \right)$$
$$\Rightarrow std\left( \frac{f(x)}{x} \right) = -1 = \lim_{x \to 0} \frac{f(x)}{x}$$

---

# 1 极限的定义2.0_第18页.png

已知$\lim\limits_{x \to 0} \frac{f(x)}{x^2}$存在，且函数
$$f(x) = \frac{x-\sin x}{x} + x^2 \lim_{x \to 0} \frac{f(x)}{1-\cos x}$$
则$\lim\limits_{x \to 0} \frac{f(x)}{x^2} = \underline{\quad\quad}$。

## 解答
解：记$\lim\limits_{x \to 0} \frac{f(x)}{x^2} = \mathop{\mathrm{std}}\left( \frac{f(x)}{x^2} \right) = A$，其中$\mathop{\mathrm{std}}$为书写者自用的定值记号，代表对应极限的常数值。

将$f(x)$的表达式两边同时除以$x^2$，可得：
$$\frac{f(x)}{x^2} = \frac{x-\sin x}{x^3} + \lim_{x \to 0} \frac{f(x)}{1-\cos x}$$

对极限$\lim\limits_{x \to 0} \frac{f(x)}{1-\cos x}$做恒等变形：
$$\lim_{x \to 0} \frac{f(x)}{1-\cos x} = \lim_{x \to 0} \left( \frac{f(x)}{x^2} \cdot \frac{x^2}{1-\cos x} \right)$$

计算得：
$$\lim_{x \to 0} \frac{x^2}{1-\cos x} = 2$$

> 旁注：后续通过建立方程求解，此处用到极限结论：
> $$\lim_{x \to 0} \frac{1-\cos x}{\frac{1}{2}x^2} = 1$$
> 该知识点后续会讲解。
> 即$\mathop{\mathrm{std}}\left( \frac{1-\cos x}{\frac{1}{2}x^2} \right) = 1$，书写者个人理解为：在极限$\lim\limits_{x \to 0} \frac{1-\cos x}{\frac{1}{2}x^2}$中，$\frac{1-\cos x}{\frac{1}{2}x^2}$是1周围的超实数。

---

# 1 极限的定义2.0_第19页.png

## 极限等式求解
$$\Rightarrow \frac{f(x)}{x^2} = \frac{x-\sin x}{x^3} + 2A$$
记$A = \lim_{x\to0}\frac{f(x)}{x^2}$，两边同时取$x\to0$的极限：
$$A = \lim_{x\to0}\frac{x-\sin x}{x^3} + 2A$$
计算右侧极限（划去错误的极限书写方式）：
$$\lim_{x\to0}\frac{x-\sin x}{x^3} = \mathrm{Std}\left(\frac{x-\sin x}{x^3}\right) = \frac{1}{6}$$
批注：[之后展开]，<泰勒公式>（手写“开朗”为连笔笔误，“秦朝公式”为形近笔误）
（数轴示意图：以0为原点，标注0点位置，示意0点两侧的邻域区间）
红色批注疑问：<为啥是在0周围？>
移项求解得：
$$\Rightarrow A = -\frac{1}{6}$$

---

# 1 极限的定义2.0_第20页.png

## 函数极限的直观演示
$$\lim_{x \to x_0} f(x) = 3$$
以下演示$x \to x_0$时，$f(x)$趋近于3的过程：
1.  初始状态：纵轴为$f(x)$轴，标注刻度3、4，函数值初始位于4附近；随着$x$向$x_0$趋近，$f(x)$开始向3冲去、靠近。
2.  第一逼近阶段：以$f(x)=3$为基准线，此时$f(x)$与3的距离为$0.03$，对应说明：快到了，还差$0.03$。
3.  第二逼近阶段：以$f(x)=3$为基准线，此时$f(x)$与3的距离缩小为$0.0003$（即$\frac{3}{10000}$），对应说明：快到了，还差$0.0003$。
4.  极限状态：以$f(x)=3$为基准线，此时$f(x)$与3的距离为无穷小量（直观表示为$\frac{1}{+\infty}$，即距离趋近于0），对应说明：马上到了，还差无穷小的距离。

---

# 1 极限的定义2.0_第21页.png

## 超实数系中点3的无穷小邻域
点$3$的无穷小邻域简化示意图：邻域尺度为$\frac{1}{+\infty}$，箭头指向邻域内点$x$，邻域包含圈注强调的点$3$。
点$3$的无穷小邻域放大示意图：邻域尺度为$\frac{1}{+\infty}$，邻域内对点$x$的说明如下：
这里是超实数系
是离$3$很近的地方
你离$3$的距离是$\frac{1}{+\infty}$