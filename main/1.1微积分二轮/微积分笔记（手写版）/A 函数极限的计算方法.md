# A 函数极限的计算方法_第1页.png

## 极限的计算方法一
## 极限的四则运算
若$\lim f(x)=A$，$\lim g(x)=B$，那么（前提）
只有$f(x), g(x)$的极限都存在了，才可拆，才可用这些运算规则。
$$\lim \left[k f(x) \pm l g(x)\right] = k\lim f(x) \pm l\lim g(x) = kA \pm lB$$
$k,l$为常数。
$$\lim \left[f(x)\cdot g(x)\right] = \lim f(x) \cdot \lim g(x) = A\cdot B$$
特：若$\lim f(x)$存在，$n$为正整数
则$\lim \left[f(x)\right]^n = \left[\lim f(x)\right]^n$
$$\lim \frac{f(x)}{g(x)} = \frac{\lim f(x)}{\lim g(x)} = \frac{A}{B} \quad (B\neq 0)$$
即：
当$f(x), g(x)$的极限都存在的时候
函数的加减乘除的极限
等于各自极限的加减乘除。

## Caution
不求极限，不去$\lim$
不去$\lim$，不求极限
$\lim\limits_{x \to x_0} f(x) = \lim\limits_{x \to x_0} g(x)$中，$f(x)=g(x)$
$f(x)\to g(x)$是恒等变形
$$\lim_{x \to 0} \frac{\frac{\sin x}{x} - 1}{x^2} \neq \lim_{x \to 0} \frac{1-1}{x^2}$$
$$\lim_{x \to 0} \frac{\frac{\sin x}{x} - 1}{x^2} = \lim_{x \to 0} \frac{\sin x - x}{x^3}$$
$\lim\limits_{x \to 0} \frac{\sin x}{x}=1$中，$\frac{\sin x}{x} \neq 1$
$$\frac{\frac{\sin x}{x} - 1}{x^2} \neq \frac{1-1}{x^2}$$
$$\lim_{x \to 0} \frac{\frac{\sin x}{x} - 1}{x^2} \neq \lim_{x \to 0} \frac{1-1}{x^2}$$

---

# A 函数极限的计算方法_第2页.png

eg:
$$\lim_{x \to 0} \frac{1-\cos x}{x^2} \neq \lim_{x \to 0} \frac{\frac{1}{2}x^2}{x^2}$$
$1-\cos x \sim \frac{1}{2}x^2$，$1-\cos x \neq \frac{1}{2}x^2$
$$\lim_{x \to 0} \frac{1-\cos x}{x^2}$$
$$\frac{1-\cos x}{x^2} \neq \frac{\frac{1}{2}x^2}{x^2}$$
$$= \lim_{x \to 0} \frac{\frac{1}{2}x^2}{x^2} \cdot \frac{1-\cos x}{\frac{1}{2}x^2}$$
$$\lim_{x \to 0} \frac{1-\cos x}{x^2} \neq \lim_{x \to 0} \frac{\frac{1}{2}x^2}{x^2}$$
$$= \lim_{x \to 0} \frac{\frac{1}{2}x^2}{x^2} \cdot \lim_{x \to 0} \frac{1-\cos x}{\frac{1}{2}x^2}$$

## Caution
只有$g(x), f(x)$的极限都存在（$\lim g(x)$与$\lim f(x)$是实数），
$$\lim [g(x)\pm f(x)] = \lim g(x) \pm \lim f(x)$$
才有意义，这相当于实数的四则运算。

如果
$g(x)$的极限存在，$f(x)$的极限不存在，$\lim [g(x)\pm f(x)]$一定不存在。
此时$\lim g(x) \pm \lim f(x)$无意义，
可直接得出$\lim [g(x)\pm f(x)]$不存在的结论。

如果
$g(x), f(x)$的极限都不存在，
即$\lim\limits_{x \to 0}f(x)$不存在，$\lim\limits_{x \to 0}g(x)$不存在，
但$[f(x)\pm g(x)]=3$，$\lim\limits_{x \to 0}3=3$存在。

则
$\lim\limits_{x \to 0}[f(x)\pm g(x)]=3$要直接写出结论，仅指$\lim\limits_{x \to 0}3=3$，
不能写成
$$\lim_{x \to 0}f(x) \pm \lim_{x \to 0}g(x) = 3$$
该式无意义。

若$\lim f(x)=A$，且$\lim g(x)$存在，则
$$\lim [f(x)g(x)] = A \lim g(x)$$

同理，
当$\lim f(x)=0$且$g(x)$在对应极限过程下局部有界时，
$$\lim f(x)g(x)=0$$

---

# A 函数极限的计算方法_第3页.png

## 结论
若$\lim \frac{f(x)}{g(x)}=A$，且$\lim g(x)=0$，则$\lim f(x)=0$。

证明：
$$
\lim \frac{f(x)}{g(x)} \cdot \lim g(x) = \lim \left( \frac{f(x)}{g(x)} \cdot g(x) \right) = \lim f(x) = A\cdot 0 = 0
$$

若$\lim \frac{f(x)}{g(x)}=A\neq 0$，且$\lim f(x)=0$，则$\lim g(x)=0$。

证明：
$$
\frac{\lim f(x)}{\lim \frac{f(x)}{g(x)}} = \lim \frac{f(x)}{\frac{f(x)}{g(x)}} = \lim g(x) = \frac{0}{A} = 0
$$

即：当$\lim \frac{f(x)}{g(x)}=A\neq 0$时，
- 若$f(x)\to 0$，则$g(x)\to 0$；
- 若$g(x)\to 0$，则$f(x)\to 0$。

相当于是商非零，同阶无穷小。

## 例1.21
设$\lim\limits_{x \to 0} \frac{\sin x}{e^x - a} (\cos x - b) = 5$，则$b = \underline{\quad\quad}$。

$x\to 0$时，$\sin x\to 0$
$\implies \sin x (\cos x - b)\to 0$，故$e^x - a \to 0$
$x\to0$时$e^x \to 1$
$$
\lim_{x\to 0} (e^x - a) = \lim_{x\to 0}e^x - \lim_{x\to 0}a = 1 - a = 0
$$
$\implies a=1$

$x\to0$时，$e^x -1 \sim \sin x$
$\implies \lim_{x\to 0} (\cos x - b) = 5$
$$
\lim_{x\to 0}\cos x - \lim_{x\to 0}b = 5
$$
$1 - b = 5$
$\implies b=-4$

（右下角为$\cos x$函数示意图）

---

# A 函数极限的计算方法_第4页.png

## 0/0型极限与洛必达法则几何引入
当$\lim\limits_{x \to x_0} f(x) = 0$，$\lim\limits_{x \to x_0} g(x) = 0$时，
$$\lim_{x \to x_0} \frac{f(x)}{g(x)} = ? \quad 这个怎么算？$$

给出算例：
$f(x) = x^2 + 3x - 4$
$g(x) = \ln x$
求$\lim\limits_{x \to 1} \frac{f(x)}{g(x)}$

函数整体示意图：平面直角坐标系$xOy$内绘制开口向上的抛物线$f(x)$与对数曲线$g(x)=\ln x$，二者在$x=1$处交于x轴，标注$x=1$位置。
图像旁注：当圈出的交点处被无限放大时，地球是圆的，曲线会变成直线，脚下的地板是直的。
局部放大示意图：以交点$x=1$为局部原点，横轴标注增量$dx$，绘制两曲线在该点的切线，标注对应$dx$下的函数增量$df$、$dy$，分别对应$f(x)$、$g(x)$。

明显，当$x \to 1$时，谁更快趋于0取决于斜率，$f(x)\to0$，可看出$dy$更快$\to0$，所以该方法仅适用于$g(x)\to0$、$f(x)\to0$的情况。

则$dy\to0$，$df\to0$的速度差距可由斜率的差距来表现。
因为放大后曲线近似为直线，各点斜率与切线斜率一致，
所以：
$$k_1 = \frac{df}{dx} = f'(1),\quad k_2 = \frac{dg}{dx} = g'(1)$$
$$\implies \lim_{x \to 1} \frac{f(x)}{g(x)} = \frac{f'(1)}{g'(1)}$$
即找$x=1$处的斜率即可计算极限。

由导函数在该点的连续性：
$$\lim_{x \to 1} f'(x) = f'(1),\quad \lim_{x \to 1} g'(x) = g'(1)$$
可得
$$\implies \lim_{x \to 1} \frac{f(x)}{g(x)} = \lim_{x \to 1} \frac{f'(x)}{g'(x)}$$
即对$f'(x)$、$g'(x)$分别求极限后再相除即可。

该方法可推广到高阶情形：
想比较速度（一阶导数）趋于0的大小，用加速度（二阶导数）的比；
想比较加速度趋于0的大小，用加速度的导数（三阶导数）的比；
……

---

# A 函数极限的计算方法_第5页.png

$\frac{1}{\text{无穷小}} = \infty$

$\Rightarrow$ 当$\lim\limits_{x \to x_0} f(x) = \infty$，$\lim\limits_{x \to x_0} g(x) = \infty$时，
$\lim\limits_{x \to x_0} \frac{f(x)}{g(x)} = ?$ 也能算。

证明：
$$\frac{f(x)}{g(x)} = \frac{\frac{1}{g(x)}}{\frac{1}{f(x)}}$$

$\lim\limits_{x \to x_0} f(x) = \infty$，$\lim\limits_{x \to x_0} \frac{1}{f(x)} = 0$

$\lim\limits_{x \to x_0} g(x) = \infty$，$\lim\limits_{x \to x_0} \frac{1}{g(x)} = 0$

$$\lim_{x \to x_0} \frac{f(x)}{g(x)} = \lim_{x \to x_0} \frac{\frac{1}{g(x)}}{\frac{1}{f(x)}} = \lim_{x \to x_0} \frac{f'(x)}{g'(x)} = \frac{f'(x_0)}{g'(x_0)}$$

## 洛必达法则
### 法则1
- 在$x \to x_0$（或$x \to \infty$）时，$f(x) \to 0$，$g(x) \to 0$；
- 在$x \to x_0$（或$x \to \infty$）时，$\lim f'(x)$存在，$\lim g'(x)$存在；
- 在$x \to x_0$（或$x \to \infty$）时，$\lim \frac{f'(x)}{g'(x)}$存在；

则在$x \to x_0$（或$x \to \infty$）时：
$$\lim \frac{f(x)}{g(x)} = \lim \frac{f'(x)}{g'(x)} = \lim \frac{f''(x)}{g''(x)}$$

### 法则2
- 在$x \to x_0$（或$x \to \infty$）时，$f(x) \to \infty$，$g(x) \to \infty$；
- 在$x \to x_0$（或$x \to \infty$）时，$\lim f'(x)$存在，$\lim g'(x)$存在且$\lim g'(x) \neq 0$；
- 在$x \to x_0$（或$x \to \infty$）时，$\lim \frac{f'(x)}{g'(x)}$存在；

则在$x \to x_0$（或$x \to \infty$）时：
$$\lim \frac{f(x)}{g(x)} = \lim \frac{f'(x)}{g'(x)} = \lim \frac{f''(x)}{g''(x)}$$

---

# A 函数极限的计算方法_第6页.png

## 双曲正弦函数
$y=\frac{e^x - e^{-x}}{2}$，是奇函数。

## 反双曲正弦函数
$y=\ln\left(x+\sqrt{1+x^2}\right)$
（函数示意图：过原点的奇函数曲线）
是奇函数，导数为：
$$y'=\frac{1}{\sqrt{1+x^2}}$$

## 1.22 $x\to0$时的等价无穷小
### (1) $\ln\left(x+\sqrt{1+x^2}\right) \sim x$
当$x\to0$时，$\ln\left(x+\sqrt{1+x^2}\right)\sim x$。
$\lim_{x\to0} \ln\left(x+\sqrt{1+x^2}\right)=0$，$\lim_{x\to0} x=0$，为$\frac{0}{0}$型。
求导得：
$$\left[\ln\left(x+\sqrt{1+x^2}\right)\right]' = \frac{1}{\sqrt{1+x^2}}$$
$$(x)' = 1$$
由洛必达法则：
$$\lim_{x\to0} \frac{\ln\left(x+\sqrt{1+x^2}\right)}{x} = \lim_{x\to0} \frac{\frac{1}{\sqrt{1+x^2}}}{1} = 1$$
$\Rightarrow$ 结论：$\ln\left(x+\sqrt{1+x^2}\right) \sim x \quad (x\to0)$

### (2) $1-(\cos x)^a \sim \frac{1}{2}a x^2 \quad (a\neq0)$
当$x\to0$时，$1-(\cos x)^a\sim \frac{1}{2}a x^2,\ a\neq0$。
此为$\frac{0}{0}$型。
求导得：
$$\left[1-(\cos x)^a\right]' = -a(\cos x)^{a-1}\cdot(-\sin x)$$
$$\left[\frac{1}{2}a x^2\right]' = a x$$
由洛必达法则：
$$\lim_{x\to0} \frac{1-(\cos x)^a}{\frac{1}{2}a x^2} = \lim_{x\to0} \frac{-a(\cos x)^{a-1}\cdot(-\sin x)}{a x} = 1$$
（约分化简）
$\Rightarrow$ 结论：$1-(\cos x)^a \sim \frac{1}{2}a x^2 \quad (a\neq0,\ x\to0)$

例：
$1-\sqrt{\cos x} \sim \frac{1}{4}x^2$

---

# A 函数极限的计算方法_第7页.png

## 1.23 无穷大阶的比较例题
设$f(x)=\ln^{10}x$，$g(x)=x$，$h(x)=e^{\frac{x}{10}}$，则当$x$充分大时，比较三者的大小。
本题为$\frac{\infty}{\infty}$型极限，使用洛必达法则求解：
1.  比较$x$与$\ln^{10}x$的阶：
$$
\begin{align*}
\lim_{x \to +\infty} \frac{x}{\ln^{10}x} &\xlongequal{\text{洛必达}} \lim_{x \to +\infty} \frac{1}{10\ln^{9}x \cdot \frac{1}{x}} \xlongequal{\text{化简}} \lim_{x \to +\infty} \frac{x}{10\ln^{9}x} \\
&\xlongequal{\text{洛必达}} \lim_{x \to +\infty} \frac{x}{10\cdot9\ln^{8}x} \xlongequal{\text{洛必达}} \dots \xlongequal{\text{洛必达}} \lim_{x \to +\infty} \frac{x}{10! \cdot \ln x} \\
&\xlongequal{\text{洛必达}} \frac{1}{10!} \cdot \lim_{x \to +\infty} x = +\infty
\end{align*}
$$
可得：$x \gg \ln^{10}x$（即$x$远远大于$\ln^{10}x$，$x$是比$\ln^{10}x$高阶的无穷大）。
2.  比较$e^{\frac{x}{10}}$与$x$的阶：
$$
\lim_{x \to +\infty} \frac{e^{\frac{x}{10}}}{x} \xlongequal{\text{洛必达}} \lim_{x \to +\infty} \frac{e^{\frac{x}{10}} \cdot \frac{1}{10}}{1} = +\infty
$$
注：此处使用复合函数链式求导法则：$(e^u)' = e^u \cdot u'$。
推广可得一般结论：$e^{\alpha x} \gg x^\beta \quad (\alpha,\beta>0)$，即正指数指数函数是比任意正次幂函数高阶的无穷大。
## 无穷大增速比较常用结论
结论：当$x \to +\infty$时（考试可直接使用）：
$$\ln^\alpha x \ll x^\beta \ll a^x \quad (\alpha,\beta>0,\ a>1)$$
提速（增速从慢到快）：对数函数 $\ll$ 幂函数 $\ll$ 指数函数
当$n \to \infty$（数列情形）时：
$$\ln^\alpha n \ll n^\beta \ll a^n \ll n! \ll n^n \quad (\alpha,\beta>0,\ a>1)$$

---

# A 函数极限的计算方法_第8页.png

## 函数差异与无限逼近的原理
- 函数与函数不同的原因就是：在自变量相同的变化下，因变量变化不同，而斜率是变化不同的原因。
- 洛必达用$f(\ \ )$与$g(\ \ )$在$x_0$上的斜率的差距，来表现出$f(x),g(x)$趋近于$f(x_0),g(x_0)$的快慢差距：
  即$f(x_0)=g(x_0)$，且$f'(x_0)\neq g'(x_0)$；
  若$f'(x_0)=g'(x_0)$，则$f''(x_0)\neq g''(x_0)$，则比较$g''(x_0)$与$f''(x_0)$。
- 若两者在$x_0$上的斜率相同，$f'(x_0)=g'(x_0)$，则两个函数在数值上就更相近；
  同样，若两者在$x_0$上的斜率的斜率也相同，则两个函数在数值上就更加相近。
- 想让两个函数无限相近，则需要满足：
$$
\begin{aligned}
f(x_0) &= g(x_0) \\
f'(x_0) &= g'(x_0) \\
f''(x_0) &= g''(x_0) \\
&\quad \vdots \\
f^{(\infty)}(x_0) &= g^{(\infty)}(x_0)
\end{aligned}
\quad \text{两函数越来越相近}
$$

## 函数拟合的构造思路
若想找一个$g(x)$无限拟合于$f(x)$的话，只用让$g(x)$满足：
1.  $f(x_0) = g(x_0) = a_0$
2.  $f'(x_0) = g'(x_0) = a_1$
3.  $f''(x_0) = g''(x_0) = a_2$
4.  $f'''(x_0) = g'''(x_0) = a_3$
    $\vdots$
$\infty$. $f^{(\infty)}(x_0) = g^{(\infty)}(x_0) = a_\infty$

直接找的话，这是一个很抽象的问题。那，我们先不看②、③、④、…，先看①，先满足①，再在①的基础上，再看②，就将一个复杂的问题分割成一个个的小问题。

---

# A 函数极限的计算方法_第9页.png

## $x=x_0$处泰勒多项式构造推导
① 找$g(x)$满足：
$$\begin{cases} f(x_0)=g(x_0)=a_0 \end{cases}$$
设$g(x)=a_0 \quad 1.0$
则$g(x_0)=a_0$

② 找$g(x)$满足：
$$\begin{cases} f(x_0)=g(x_0)=a_0 \\ f'(x_0)=g'(x_0)=a_1 \end{cases}$$
$\because g(x)=a_0$，
$g'(x)=0$，
$(x)'=1!$，
$\therefore$ 设$g(x)=a_0+a_1 x \quad 2.0$
则$g'(x)=a_1$，
$g'(x_0)=a_1$，
$\because g(x_0)=a_0+a_1 x_0 \neq a_0$，
$\therefore g(x)=a_0+a_1(x-x_0) \quad 2.1$
即$g(x)=a_0+a_1 x -a_1 x_0$
则$g'(x)=a_1$，
$g(x_0)=a_0$

③ 找$g(x)$满足：
$$\begin{cases} f(x_0)=g(x_0)=a_0 \\ f'(x_0)=g'(x_0)=a_1 \\ f''(x_0)=g''(x_0)=a_2 \end{cases}$$
$\because g(x)=a_0+a_1(x-x_0)$，
$g''(x)=0$，
$(x^2)''=2!$，$\left(\frac{x^2}{2!}\right)''=1$，
$\therefore$ 设$g(x)=a_0+a_1(x-x_0)+\frac{a_2 x^2}{2!} \quad 3.0$
则$g''(x)=a_2$，
$g''(x_0)=a_2$，
$\because g(x_0)=a_0+\frac{a_2 x_0^2}{2!} \neq a_0$，
$\therefore g(x)=a_0+a_1(x-x_0)+\frac{a_2(x-x_0)^2}{2!} \quad 3.1$
即
$$g(x)=a_0+a_1 x -a_1 x_0 + \frac{a_2 x^2 - 2a_2 x x_0 +a_2 x_0^2}{2!}$$
则$g(x_0)=a_0$，
$g'(x_0)=a_1$，
$g''(x_0)=a_2$

---

# A 函数极限的计算方法_第10页.png

## ④ 找$g(x)$
要求$g(x)$在$x=x_0$处满足：
$$
\begin{cases}
f(x_0)=g(x_0)=a_0 \\
f'(x_0)=g'(x_0)=a_1 \\
f''(x_0)=g''(x_0)=a_2 \\
f'''(x_0)=g'''(x_0)=a_3
\end{cases}
$$
$\because g(x)=a_0+a_1(x-x_0)+\frac{a_2(x-x_0)^2}{2!}$
此时$g'''(x)=0$
由高阶导数公式：$(x^3)'''=3!,\ \left(\frac{x^3}{3!}\right)'''=1$
$\therefore$ 最初尝试设$g(x)=a_0+a_1(x-x_0)+\frac{a_2(x-x_0)^2}{2!}+\frac{a_3 x^3}{3!}$
则$g'''(x)=a_3$，满足$g'''(x_0)=a_3$
$\because g(x_0)=a_0+\frac{a_3 x_0^3}{3!}\neq a_0$，不满足函数值匹配条件
$\therefore$ 修正构造为：
$$g(x)=a_0+a_1(x-x_0)+\frac{a_2(x-x_0)^2}{2!}+\frac{a_3(x-x_0)^3}{3!}$$
逐阶求导验证：
$g'(x)=0 + a_1 + a_2(x-x_0)+\frac{a_3(x-x_0)^2}{2!}$
$g''(x)=0 + 0 + a_2 + a_3(x-x_0)$
$g'''(x)=0 + 0 + 0 + a_3$
推广到无穷阶一般形式：
$$g(x)=a_0+a_1(x-x_0)+\frac{a_2(x-x_0)^2}{2!}+\dots+\frac{a_n(x-x_0)^n}{n!}+\frac{a_{n+k}(x-x_0)^{n+k}}{(n+k)!}+\dots$$
其中系数满足：
$a_0=f(x_0),\ a_1=f'(x_0),\ a_2=f''(x_0),\dots$

---

# A 函数极限的计算方法_第11页.png

这里，我们就找到了一个可以无限拟合$f(x)$的多项式函数$g(x)$：
$$
g(x) = f(x_0) + f'(x_0)(x-x_0) + \frac{f''(x_0)(x-x_0)^2}{2!} + \dots + \frac{f^{(n)}(x_0)(x-x_0)^n}{n!} + \frac{f^{(n+k)}(x_0)(x-x_0)^{n+k}}{(n+k)!} + \dots^\infty
$$

---

# A 函数极限的计算方法_第12页.png

## 泰勒公式
可以用多项式函数模拟任何函数。

设$f(x)$在点$x=0$处$n$阶可导，则存在$x=0$的一个邻域，对于该邻域内的任何一点$x$，有
$$f(x)=f(0)+f'(0)x+\frac{f''(0)x^2}{2!}+\dots+\frac{f^{(n)}(0)x^n}{n!}+\underbrace{o(x^n)}_{\text{佩亚诺余项}}$$
（越加越相近）

后面剩的许多项不想写了，用佩亚诺余项表示。
若$\alpha(x)$是$\beta(x)$的高阶无穷小，
记：$\alpha(x) = o(\beta(x))$
则$o(x^n)$指的是比$\frac{f^{(n)}(0)x^n}{n!}$更高阶的项。

eg:
$$\sin x = \sin 0 + \left.(\sin x)'\right|_{x=0}\cdot x + \frac{\left.(\sin x)''\right|_{x=0}\cdot x^2}{2!} + \frac{\left.(\sin x)'''\right|_{x=0}\cdot x^3}{3!} + o(x^3)$$
化简：
$$\Rightarrow \sin x = x - \frac{1}{6}x^3 + o(x^3)$$

同理，可得如下重要函数的泰勒公式，主打一个提速：
$$\sin x = x - \frac{x^3}{3!} + o(x^3),\quad \cos x = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} + o(x^4)$$
$$\arcsin x = x + \frac{x^3}{3!} + o(x^3),\quad \tan x = x + \frac{x^3}{3} + o(x^3)$$
$$\arctan x = x - \frac{x^3}{3} + o(x^3),\quad \ln(1+x) = x - \frac{x^2}{2} + \frac{x^3}{3} + o(x^3)$$
$$e^x = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + o(x^3),\quad (1+x)^\alpha = 1 + \alpha x + \frac{\alpha(\alpha-1)x^2}{2!} + o(x^2)$$

背会$\boldsymbol{\longrightarrow}$ “一站直达”

---

# A 函数极限的计算方法_第13页.png

$\because \sin x = x - \frac{x^3}{3!} + o(x^3)$

$\therefore x - \sin x = \frac{1}{6}x^3 + o(x^3)$

$$\lim_{x \to 0} \frac{x-\sin x}{\frac{1}{6}x^3} = \lim_{x \to 0} \frac{\frac{1}{6}x^3 + o(x^3)}{\frac{1}{6}x^3}$$

$= 1 + 0 = 1$

$\implies x-\sin x \sim \frac{1}{6}x^3 \quad (x \to 0)$

广义化，将$x$替换为$g(x)$，其中满足$g(x) \to 0$，可得：
$g(x) - \sin g(x) \sim \frac{1}{6}g^3(x)$

### 一些差函数的等价无穷小
$$
\begin{align*}
x - \sin x &\sim \frac{1}{6}x^3 \quad (x \to 0) \\
\arcsin x - x &\sim \frac{1}{6}x^3 \quad (x \to 0) \\
\tan x - x &\sim \frac{1}{3}x^3 \quad (x \to 0) \\
x - \arctan x &\sim \frac{1}{3}x^3 \quad (x \to 0)
\end{align*}
$$

以上等价无穷小结论均可做广义化。

## 高阶无穷小的运算
若$\alpha(x)$是$\beta(x)$的高阶无穷小，记为
$$\alpha(x) = o(\beta(x))$$
其中$o(x^m)$表示$x^m$的高阶无穷小。

设$m,n$为正整数，则高阶无穷小（$o$记号）满足以下运算规则：
- **加减法规则**
  $$o(x^m) \pm o(x^n) = o(x^l),\quad l = \min[m,n]$$
  其中$l$为$m,n$中的最小值。
  说明：$x \to 0$时，无穷小的次数越低，趋于0的速度越慢，取值相对越大，加减法运算中低阶无穷小会吸收高阶无穷小（低阶主导）。
  示例：
  $$
  \begin{align*}
  o(x^2) - o(x^3) &= o(x^2) \\
  o(x^2) - o(x^2) &= o(x^2) \\
  o(x^2) + o(x^2) &= o(x^2)
  \end{align*}
  $$

- **乘法规则**
  $$
  \begin{align*}
  o(x^m) \cdot o(x^n) &= o(x^{m+n}) \\
  x^m \cdot o(x^n) &= o(x^{m+n})
  \end{align*}
  $$
  说明：无穷小相乘时，阶数累加。

- **数乘规则**
  $$o(x^m) = o(kx^m) = k \cdot o(x^m),\quad k \neq 0$$
  说明：与非零常数相乘不影响无穷小的阶数。
  示例：$o(x^2) = 2o(x^2)$

---

# A 函数极限的计算方法_第14页.png

## 泰勒公式展开原则
- $\boldsymbol{\frac{A}{B}}$型，适用“上下同阶”原则
  若分母为$k$次方，那分子就展到$k$次方；
  若分子为$k$次方，那分母就展到$k$次方。
- $\boldsymbol{A-B}$型，适用“幂次最低”原则
  $A+B$型可转化为$A+B = A-(-B)$，适用该原则；
  即：将$A,B$分别展开到它们的系数不相等的$x$的最低次幂为止。

**例**：已知当$x\to0$时，$\cos x - e^{-\frac{x^2}{2}}$与$ax^b$为等价无穷小，求$a,b$。
**解**：
利用泰勒展开，两个函数都可使用已记忆的展开式，其中$e^{-\frac{x^2}{2}}$将$e^x$展开式中的$x$替换为$-\frac{x^2}{2}$即可。
1.  初次展开到常数项：
    $$\cos x = 1,\quad e^{-\frac{x^2}{2}}=1$$
    系数相同，继续展开。
2.  展开到$x^2$项：
    $$\cos x = 1-\frac{1}{2}x^2,\quad e^{-\frac{x^2}{2}}=1-\frac{1}{2}x^2$$
    系数相同，继续展开。
3.  展开到$x^4$项，用佩亚诺余项结尾，不再展开更高次项：
    $$\cos x = 1-\frac{1}{2}x^2 + \frac{1}{24}x^4 + o(x^4)$$
    $$e^{-\frac{x^2}{2}} = 1-\frac{1}{2}x^2 + \frac{1}{8}x^4 + o(x^4)$$

两式作差，由佩亚诺余项性质$o(x^4)-o(x^4)=o(x^4)$，得：
$$\cos x - e^{-\frac{x^2}{2}} = -\frac{1}{12}x^4 + o(x^4)$$
因此$\boldsymbol{a=-\frac{1}{12},\ b=4}$。

---

# A 函数极限的计算方法_第15页.png

## 两个重要的极限
$$\lim_{x \to 0} \frac{\sin x}{x} = 1,\quad \lim_{x \to \infty} \left(1+\frac{1}{x}\right)^x = e$$
广义化：公式中的$x$可为任一函数。
例：将$x$替换为$\frac{1}{x}$：
- 对第一个重要极限：
$$\lim_{\frac{1}{x} \to 0} \frac{\sin \frac{1}{x}}{\frac{1}{x}} = 1 \quad \text{即} \quad \underline{\lim_{x \to \infty} x\sin \frac{1}{x} = 1}$$
- 对第二个重要极限：
$$\lim_{\frac{1}{x} \to \infty} \left(1+\frac{1}{\frac{1}{x}}\right)^{\frac{1}{x}} = e \quad \text{即} \quad \underline{\lim_{x \to 0} (1+x)^{\frac{1}{x}} = e}$$

## 夹逼准则
学习提示：先用，之后会开朗
含义解释：夹：取中间函数；逼：向中间逼近，即向中间逼近准则。
准则条件：
若$f(x)$被夹在两个量之间，满足：
$$h(x) \leq f(x) \leq g(x)$$
且这两个量的极限存在且相同：
$$\lim h(x) = A,\quad \lim g(x) = A$$
记忆口诀：则，大喊一声，哪里跑
准则结论：$\lim f(x)$存在，且$\lim f(x) = A$。
逼近过程示意：
$$
\begin{matrix}
h(x) &\leq &f(x) &\leq &g(x)\\
\downarrow & &\Downarrow & &\downarrow\\
A &\Rightarrow &A &\Leftarrow &A
\end{matrix}
$$
核心逻辑：向中间逼近。