
# C 函数的连续与间断_第1页.png

$$e^x = 1 + x + \frac{1}{2}x^2 + o(x^2)$$
~ 泰勒公式，其中标注的$1+x+\frac{1}{2}x^2$为2次泰勒多项式。

## 函数的连续与间断的判别/判定问题
本质上是函数极限计算的问题。
$\lim\limits_{x \to x_0^+} f(x)$ 与 $\lim\limits_{x \to x_0^-} f(x)$ 的存在与否与$f(x_0)$无关，这是因为单侧极限描述的是$f(x_0)$这一点周围的函数值变化趋势。

## 连续的定义
设函数$f(x)$在点$x_0$的某一个邻域内有定义，若满足
$$\lim_{x \to x_0^+} f(x) = \lim_{x \to x_0^-} f(x) = f(x_0)$$
则称函数$f(x)$在点$x_0$处连续，上述结论也是函数在点$x_0$处连续的充要条件：
$$\lim_{x \to x_0^+} f(x) = \lim_{x \to x_0^-} f(x) = f(x_0) \iff f(x)在点x_0处连续$$

## 连续函数的运算法则
- 若$f(x)$与$g(x)$都在点$x=x_0$处连续，则$f(x)\pm g(x)$与$f(x)g(x)$在点$x=x_0$处都连续；当$g(x_0)\neq 0$时，$\frac{f(x)}{g(x)}$在点$x=x_0$处也连续。
- 若$u=\varphi(x)$在点$x=x_0$处连续，$u_0=\varphi(x_0)$，且$y=f(u)$在点$u=u_0$处连续，则复合函数$y=f[\varphi(x)]$在点$x=x_0$处连续。
- 若$y=f(x)$在区间$I_x$上单调且连续，则其反函数$x=\varphi(y)$在对应的值域区间$I_y=\{y\mid y=f(x), x\in I_x\}$上连续，且与原函数有相同的单调性。
- （局部保号性）若$f(x)$在点$x=x_0$处连续，且$f(x_0)>0$（或$f(x_0)<0$），则存在$\delta>0$，使得当$|x-x_0|<\delta$（即在$x_0$附近）时，$f(x)>0$（或$f(x)<0$）。
  （对应$x_0$的$\delta$邻域示意图，标注邻域端点$x_0-\delta$、$x_0$、$x_0+\delta$）

---

# C 函数的连续与间断_第2页.png

## 间断点的定义与分类
前提：以下设函数$f(x)$在$x_0$的某去心邻域内（即$f(x_0)$的附近）有定义。

## 第一类间断点
- 可去间断点/可补间断点
若$\lim\limits_{x \to x_0} f(x) = A \neq f(x_0)$（$f(x_0)$甚至可以无定义），则$x=x_0$为可去间断点/可补间断点。
即$\lim\limits_{x \to x_0^+} f(x)$与$\lim\limits_{x \to x_0^-} f(x)$存在且相等，但不等于$f(x_0)$。

- 跳跃间断点
若$\lim\limits_{x \to x_0^-} f(x)$与$\lim\limits_{x \to x_0^+} f(x)$都存在，但$\lim\limits_{x \to x_0^-} f(x) \neq \lim\limits_{x \to x_0^+} f(x)$，不管$f(x_0)$是否有定义、取值如何，则$x=x_0$为跳跃间断点。

## 第二类间断点
- 无穷间断点
若$\lim\limits_{x \to x_0} f(x) = \infty$，或$\lim\limits_{x \to x_0^+} f(x) = \infty$，或$\lim\limits_{x \to x_0^-} f(x) = \infty$，则$x=x_0$为无穷间断点。
即这一点的左右两侧至少有一个极限值为$\infty$即可。
例：$y=\frac{1}{x}$的$x=0$点。

- 振荡间断点
若$\lim\limits_{x \to x_0} f(x)$振荡不存在，则$x=x_0$为振荡间断点。
即在该点的去心邻域内，函数呈现振荡状态。
例：$y=\sin\frac{1}{x}$在点$x=0$处没有定义，当$x \to 0$时，函数值在$-1$与$1$之间振荡取值，值不唯一，极限不存在，故点$x=0$为$y=\sin\frac{1}{x}$的振荡间断点。

---

# C 函数的连续与间断_第3页.png

## 例1.36
$$
f(x)=
\begin{cases}
(\cos x)^{x^{-2}}, & x\neq 0 \\
a, & x=0
\end{cases}
$$
在$x=0$处连续，则$a=\underline{\qquad}$

解：由函数在$x=0$处连续的定义，有
$$\lim_{x\to 0} (\cos x)^{x^{-2}} = a = \lim_{x\to 0} (\cos x)^{\frac{1}{x^2}}$$
利用$1^\infty$型极限公式：$\lim\limits_{a\to 1} a^b = e^{\lim\limits_{a\to 1} b(a-1)}$，
$$
\begin{align*}
\text{原式}&= e^{\lim\limits_{x\to 0} \frac{\cos x - 1}{x^2}} \\
&= e^{-\frac{1}{2}}
\end{align*}
$$
故$a=e^{-\frac{1}{2}}$

## 例1.37
求函数
$$f(x)=\frac{e^{\frac{1}{x-1}} \ln(1+x)}{(e^x -1)(x-2)}$$
的第二类间断点的个数为$\underline{\qquad}$。

首先找出所有无定义点/间断点：
- 因子$e^x -1$对应无定义点$x=0$
- 因子$x-2$对应无定义点$x=2$
- 因子$e^{\frac{1}{x-1}}$对应无定义点$x=1$
- 因子$\ln(1+x)$对应无定义点$x=-1$

逐个分析间断点类型：
1.  对于$x=1$：
$\lim\limits_{x\to 1^+} f(x)=\infty$（例1.15已计算过），因此$x=1$为第二类间断点。

2.  对于$x=0$：
$x\to 0$时，利用等价无穷小化简：
此时$1+x>0$，故$\ln|1+x|=\ln(1+x)\sim x$；
$e^x -1\sim x$；
$x-2\sim -2$；
$e^{\frac{1}{x-1}}\to \frac{1}{e}$。

因此
$$
\lim_{x\to 0} f(x) = \lim_{x\to 0} \frac{e^{\frac{1}{x-1}} \ln(1+x)}{(e^x -1)(x-2)} = -\frac{1}{2e}
$$
可推得极限存在，故$\lim\limits_{x\to 0^+} f(x)$与$\lim\limits_{x\to 0^-} f(x)$存在且相等，而$f(0)$无定义，因此$x=0$是可去间断点。

---

# C 函数的连续与间断_第4页.png

## 例1.10 间断点分析
$x \to 2$时：
$x-2 \to 0$
$e^x - 1,\ e^{\frac{1}{x-1}},\ \ln(1+x)$都趋向同一常数
$\frac{1}{x-2} \cdot 常数 \to \infty$
$\Rightarrow \lim\limits_{x \to 2} f(x) = \infty$
则$x=2$为第二类间断点。

$x \to -1$时：
$1+x \to 0$
$\ln(1+x) \to \infty$
$e^{\frac{1}{x-1}},\ e^x - 1,\ x-2$都趋向同一常数
$\Rightarrow 原式 = \lim\limits_{x \to -1} \frac{\ln(1+x)}{1} \cdot 常数 = \infty$
$\Rightarrow x=-1$是第二类间断点。

## 1.20 可去间断点个数问题
$$f(x) = \frac{|x|^x - 1}{x(x+1)\ln|x|}$$
的可去间断点个数为：

解：$f(x)$的无定义点（间断点）为$0,-1,1$。
1.  **分析$x=-1$处**：
    $\lim\limits_{x \to -1} f(x) = \infty$（在例1.10有算），为第二类无穷间断点。
2.  **分析$x=0$处**：
    当$x \to 0$时，$\ln|x|$的阶远低于$x$的负幂次阶，故$x\ln|x| \to 0$；由等价无穷小$e^t - 1 \sim t\ (t \to 0)$，得：
    $$\lim_{x \to 0} f(x) = \lim_{x \to 0} \frac{e^{x\ln|x|} - 1}{x(x+1)\ln|x|} = \lim_{x \to 0} \frac{x\ln|x|}{x\ln|x| \cdot (x+1)} = 1$$
    即$\lim\limits_{x \to 0^+} f(x) = \lim\limits_{x \to 0^-} f(x) = 1$，且$x=0$处无定义，故$x=0$为可去间断点。
3.  **分析$x=1$处**：
    与上述推导同理，$x \to 1$时$x\ln|x| \to 0$，因此：
    $$\lim_{x \to 1} f(x) = \lim_{x \to 1} \frac{e^{x\ln|x|} - 1}{x(x+1)\ln|x|} = \lim_{x \to 1} \frac{x\ln|x|}{x(x+1)\ln|x|} = \frac{1}{2}$$
    且$x=1$处无定义，故$x=1$为可去间断点。

---

# C 函数的连续与间断_第5页.png

## 例138与例126连动
设函数
$$f(x)=\lim_{n \to \infty} \frac{x^2 + n x(1-x)\sin^2 \pi x}{1 + n\sin^2 \pi x}$$
则$f(x)$的间断点种类。

在例1.26中已求得：
$$
f(x)=
\begin{cases}
x^2, & x=0,\pm1,\pm2,\cdots \\
x(1-x), & x\text{取其他值}
\end{cases}
$$

图象为：

$\Rightarrow$ 只有可去间断点，
即只有第一类间断点。