---

# A 函数极限的计算方法_第1页.png

## 极限的计算方法——极限的四则运算
若$\lim f(x)=A$，$\lim g(x)=B$，使用法则的前提：
只有$f(x), g(x)$的极限都存在时，才可拆分极限，使用以下运算规则。

- 线性组合运算法则：
$$
\lim\left[kf(x)\pm lg(x)\right] = k\cdot\lim f(x) \pm l\cdot\lim g(x) = kA\pm lB
$$
其中$k,l$为常数。

- 乘积运算法则：
$$
\lim\left[f(x)\cdot g(x)\right] = \lim f(x)\cdot \lim g(x) = A\cdot B
$$
特例：若$\lim f(x)$存在，$n$为正整数，则
$$
\lim\left[f(x)\right]^n = \left[\lim f(x)\right]^n
$$

- 商的运算法则：
$$
\lim \frac{f(x)}{g(x)} = \frac{\lim f(x)}{\lim g(x)} = \frac{A}{B} \quad (B\neq 0)
$$

即：当$f(x), g(x)$的极限都存在时，函数加减乘除的极限，等于各自极限的加减乘除。

---

## Caution（注意事项）
核心原则：不求极限，不去$\lim$；不去$\lim$，不求极限。

若写$\lim\limits_{x\to x_0} f(x) = \lim\limits_{x\to x_0} g(x)$，必须满足$f(x)=g(x)$，即$f(x)$到$g(x)$的变形是恒等变形。

### 典型错误示例
禁止提前对部分表达式单独取极限：
$$
\lim_{x\to 0} \frac{\frac{\sin x}{x} -1}{x^2} \neq \lim_{x\to 0} \frac{1-1}{x^2}
$$
错误原因：$\lim\limits_{x\to 0}\frac{\sin x}{x}=1$是极限运算的结果，但在极限过程中$\frac{\sin x}{x}\neq 1$，因此$\frac{\frac{\sin x}{x}-1}{x^2} \neq \frac{1-1}{x^2}$，不能提前将$\frac{\sin x}{x}$替换为1计算。

正确恒等变形（先通分再运算）：
$$
\lim_{x\to 0} \frac{\frac{\sin x}{x} -1}{x^2} = \lim_{x\to 0} \frac{\sin x - x}{x^3}
$$

---

# A 函数极限的计算方法_第2页.png

## ④ 构造满足$x_0$处导数匹配条件的多项式$g(x)$
要求$g(x)$在$x_0$处与$f(x)$的函数值、一至三阶导数值相等，即满足：
$$
\begin{cases}
f(x_0) = g(x_0) = a_0 \\
f'(x_0) = g'(x_0) = a_1 \\
f''(x_0) = g''(x_0) = a_2 \\
f'''(x_0) = g'''(x_0) = a_3
\end{cases}
$$

若仅构造到二次项：
$$g(x)=a_0+a_1(x-x_0)+\frac{a_2(x-x_0)^2}{2!}$$
此时$g'''(x)=0$，无法满足三阶导数匹配的要求。

由高阶求导规律：$(x^3)'''=3!$，$\left(\frac{x^3}{3!}\right)'''=1$，因此尝试添加三次项，最初构造的错误形式为：
$$g(x)=a_0+a_1(x-x_0)+\frac{a_2(x-x_0)^2}{2!}+\frac{a_3x^3}{3!} \tag{4.0 错误形式}$$
此时计算得$g'''(x)=a_3$，满足$g'''(x_0)=a_3$，但代入$x=x_0$可得：
$$g(x_0)=a_0+\frac{a_3x_0^3}{3!}\neq a_0$$
不满足函数值匹配的条件，因此将三次项修正为$(x-x_0)^3$，得到正确的三次多项式：
$$g(x)=a_0+a_1(x-x_0)+\frac{a_2(x-x_0)^2}{2!}+\frac{a_3(x-x_0)^3}{3!} \tag{4.1}$$

逐阶求导验证匹配性：
$$
\begin{aligned}
g'(x) &= a_1 + a_2(x-x_0)+\frac{a_3(x-x_0)^2}{2!} \\
g''(x) &= a_2 + a_3(x-x_0) \\
g'''(x) &= a_3
\end{aligned}
$$
该多项式在$x_0$处满足预设的函数值、各阶导数匹配条件。

推广到无穷阶（泰勒级数形式）：
$$g(x)=a_0+a_1(x-x_0)+\frac{a_2(x-x_0)^2}{2!}+\dots+\frac{a_n(x-x_0)^n}{n!}+\frac{a_{n+k}(x-x_0)^{n+k}}{(n+k)!}+\dots$$
其中系数由$f(x)$在$x_0$处的各阶导数确定：
$$a_0=f(x_0),\ a_1=f'(x_0),\ a_2=f''(x_0),\dots$$

---

# A 函数极限的计算方法_第3页.png

这里，我们就找到了一个可以无限拟合$f(x)$的多项式函数$g(x)$：
$$\therefore g(x)=f(x_0)+f'(x_0)(x-x_0)+\frac{f''(x_0)(x-x_0)^2}{2!}+\dots+\frac{f^{(n)}(x_0)(x-x_0)^n}{n!}+\frac{f^{(n+k)}(x_0)(x-x_0)^{n+k}}{(n+k)!}+\dots\infty$$

---

# A 函数极限的计算方法_第4页.png

## 泰勒公式
可以用多项式函数模拟任何函数。
设$f(x)$在点$x=0$处$n$阶可导，则存在$x=0$的一个邻域，对于该邻域内的任何一点$x$，有：
$$f(x) = f(0) + f'(0)x + \frac{f''(0)x^2}{2!} + \dots + \frac{f^{(n)}(0)x^n}{n!} + o(x^n)$$
（越加越相近）
佩亚诺余项：后面剩的许多项不想写了，用佩亚诺余项表示。
$\alpha(x)$是$\beta(x)$的高阶无穷小，记：
$$\alpha(x) = o(\beta(x))$$
则$o(x^n)$指比$\frac{f^{(n)}(0)x^n}{n!}$更高阶的项们。

eg:
$$\sin x = \sin 0 + \left.(\sin x)'\right|_{x=0}\cdot x + \frac{\left.(\sin x)''\right|_{x=0}\cdot x^2}{2!} + \frac{\left.(\sin x)'''\right|_{x=0}\cdot x^3}{3!} + o(x^3)$$
化简：
$$\Rightarrow \sin x = x - \frac{1}{6}x^3 + o(x^3)$$

同理，可得如下重要函数的泰勒公式 主打一个提速：
$$\sin x = x - \frac{x^3}{3!} + o(x^3),\quad \cos x = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} + o(x^4)$$
$$\arcsin x = x + \frac{x^3}{3!} + o(x^3),\quad \tan x = x + \frac{x^3}{3} + o(x^3)$$
$$\arctan x = x - \frac{x^3}{3} + o(x^3),\quad \ln(1+x) = x - \frac{x^2}{2} + \frac{x^3}{3} + o(x^3)$$
$$e^x = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + o(x^3),\quad (1+x)^\alpha = 1 + \alpha x + \frac{\alpha(\alpha-1)x^2}{2!} + o(x^2)$$

背会$\longrightarrow$“一站直达”

---

# A 函数极限的计算方法_第5页.png

$\because \sin x = x - \frac{x^3}{3!} + o(x^3)$
$\therefore x - \sin x = \frac{1}{6}x^3 + o(x^3)$

$$
\lim_{x \to 0} \frac{x-\sin x}{\frac{1}{6}x^3} = \lim_{x \to 0} \frac{\frac{1}{6}x^3 + o(x^3)}{\frac{1}{6}x^3} = 1+0 = 1
$$
$\Longrightarrow x - \sin x \sim \frac{1}{6}x^3 \quad (x \to 0)$

广义化，让$x$换成$g(x)$，即$g(x) \to 0$：
$g(x) - \sin g(x) \sim \frac{1}{6}g^3(x)$

$\Longrightarrow$
## 一些差函数的等价无穷小
$x - \sin x \sim \frac{1}{6}x^3 \quad (x \to 0)$
$\arcsin x - x \sim \frac{1}{6}x^3 \quad (x \to 0)$
$\tan x - x \sim \frac{1}{3}x^3 \quad (x \to 0)$
$x - \arctan x \sim \frac{1}{3}x^3 \quad (x \to 0)$

以上结论都可做广义化。

## 高阶无穷小的运算
$\alpha(x)$是$\beta(x)$的高阶无穷小
记$\alpha(x) = o(\beta(x))$

$o(x^m)$是$x^m$的高阶无穷小
设$m,n$为正整数，则：
- $$o(x^m) \pm o(x^n) = o(x^l),\ l = \min[m,n]$$
  $l$为$m,n$中的最小值。
  无穷小次数越低，$x \to 0$时趋于0越慢，值就越大，$\therefore$ 大的说了算；加减法时，低阶吸收高阶。
  例：
  $o(x^2) - o(x^3) = o(x^2)$
  $o(x^2) - o(x^2) = o(x^2)$
  $o(x^2) + o(x^2) = o(x^2)$

- $$o(x^m) \cdot o(x^n) = o(x^{m+n})$$
  $$x^m \cdot o(x^n) = o(x^{m+n})$$
  相乘时，阶数累加。

- $$o(x^m) = o(kx^m) = k \cdot o(x^m),\ k \neq 0$$
  非零常数相乘不影响阶数。
  例：
  $o(x^2) = 2o(x^2)$

---

# A 函数极限的计算方法_第6页.png

## 泰勒公式展开原则
- $\boldsymbol{\frac{A}{B}}$型（分式型），适用**“上下同阶”原则**：
  若分母为$k$次方，则分子展开到$k$次方；
  若分子为$k$次方，则分母展开到$k$次方。

- $\boldsymbol{A-B}$型，适用**幂次最低原则**：
  该原则也适用于$A+B$型，转化方式为$A+B = A - (-B)$；
  规则：将$A,B$分别展开到它们的系数不相等的$x$的最低次幂为止。

---

**例题**：已知当$x \to 0$时，$\cos x - e^{-\frac{x^2}{2}}$与$ax^b$为等价无穷小，求$a,b$。

**解**：利用麦克劳林展开（$x=0$处的泰勒展开）计算：
可直接使用常用函数的麦克劳林展开式，其中$e^{-\frac{x^2}{2}}$可通过将$e^u$展开式中的$u$替换为$-\frac{x^2}{2}$得到。
1.  首先展开到0次幂（常数项）：
    $\cos x = 1$，$e^{-\frac{x^2}{2}}=1$，两者常数项系数相同，需继续展开。
2.  展开到$x^2$项：
    $$\cos x = 1 - \frac{1}{2}x^2$$
    $$e^{-\frac{x^2}{2}} = 1 - \frac{1}{2}x^2$$
    两者$x^2$项系数仍相同，继续展开。
3.  展开到$x^4$项，添加佩亚诺余项：
    $$\cos x = 1 - \frac{1}{2}x^2 + \frac{1}{24}x^4 + o(x^4)$$
    $$e^{-\frac{x^2}{2}} = 1 - \frac{1}{2}x^2 + \frac{1}{8}x^4 + o(x^4)$$
    此时$x^4$项系数已不相等，无需继续向更高次展开，用佩亚诺余项结尾即可。

计算两式的差，利用佩亚诺余项的运算性质$o(x^4) - o(x^4) = o(x^4)$：
$$
\begin{align*}
\cos x - e^{-\frac{x^2}{2}} &= \left(1 - \frac{1}{2}x^2 + \frac{1}{24}x^4 + o(x^4)\right) - \left(1 - \frac{1}{2}x^2 + \frac{1}{8}x^4 + o(x^4)\right) \\
&= -\frac{1}{12}x^4 + o(x^4)
\end{align*}
$$
根据等价无穷小的定义，可得：
$$\Rightarrow a = -\frac{1}{12},\quad b=4$$

---

# A 函数极限的计算方法_第7页.png

## 两个重要的极限
$$\lim_{x \to 0} \frac{\sin x}{x} = 1,\quad \lim_{x \to \infty} \left(1+\frac{1}{x}\right)^x = e$$
扩义：$x$可为任一函数。
eg：$x$换成$\frac{1}{x}$
$$\lim_{\frac{1}{x} \to 0} \frac{\sin \frac{1}{x}}{\frac{1}{x}} = 1 \quad 即 \quad \lim_{x \to \infty} x\sin\frac{1}{x} = 1$$

$$\lim_{\frac{1}{x} \to \infty} \left(1+\frac{1}{\frac{1}{x}}\right)^{\frac{1}{x}} = e \quad 即 \quad \lim_{x \to 0} (1+x)^{\frac{1}{x}} = e$$

## 夹逼准则
先用，之后会开朗
夹：中间 逼：逼近
向中间逼近准则
若$f(x)$被夹在两个量之间：$h(x) \leq f(x) \leq g(x)$
这两个量的极限存在且相同：
$$\lim h(x)=A,\quad \lim g(x)=A$$
则，大喊一声，哪里跑
则$\lim f(x)$存在，且$\lim f(x) = A$。
极限逼近示意：
$$
\begin{aligned}
h(x) &\leq f(x) \leq g(x)\\
\downarrow &\quad \Downarrow \quad \downarrow\\
A &\Rightarrow A \Leftarrow A
\end{aligned}
$$
向中间逼近

---

# A 函数极限的计算方法_第8页.png

## 例题
eg:
$$\lim_{x \to 0} \frac{1-\cos x}{x^2} \neq \lim_{x \to 0} \frac{\frac{1}{2}x^2}{x^2}$$
$x \to 0$时$1-\cos x \sim \frac{1}{2}x^2$，但$1-\cos x \neq \frac{1}{2}x^2$，因此函数满足：
$$\frac{1-\cos x}{x^2} \neq \frac{\frac{1}{2}x^2}{x^2}$$
正确推导需依据极限乘法法则：
$$
\lim_{x \to 0} \frac{1-\cos x}{x^2} = \lim_{x \to 0} \left( \frac{\frac{1}{2}x^2}{x^2} \cdot \frac{1-\cos x}{\frac{1}{2}x^2} \right) = \lim_{x \to 0} \frac{\frac{1}{2}x^2}{x^2} \cdot \lim_{x \to 0} \frac{1-\cos x}{\frac{1}{2}x^2}
$$
## 注意（Caution）
只有当$f(x),g(x)$的极限都存在（$\lim g(x)$与$\lim f(x)$是实数）时，
$$\lim [g(x)\pm f(x)] = \lim g(x) \pm \lim f(x)$$
才有意义，这相当于实数的四则运算。
如果$g(x)$的极限存在，$f(x)$的极限不存在，则$\lim [g(x)\pm f(x)]$一定不存在。
此时$\lim g(x) \pm \lim f(x)$无意义，可直接得出$\lim [g(x)\pm f(x)]$不存在的结论。
如果$g(x),f(x)$的极限都不存在，即$\lim_{x \to 0} f(x)$不存在，$\lim_{x \to 0} g(x)$不存在，但$f(x)\pm g(x) = 3$（实常数），$\lim_{x \to 0} 3 = 3$存在。
则$\lim_{x \to 0} [f(x)\pm g(x)] = 3$，需直接写出结论，仅依据$\lim_{x \to 0} 3=3$计算；不能写成$\lim_{x \to 0} f(x) \pm \lim_{x \to 0} g(x) =3$，该式无意义。
若$\lim f(x) = A$，则
$$\lim [f(x)g(x)] = A \lim g(x)$$
同理，当$\lim f(x)=0$时，
$$\lim f(x)g(x)=0$$

---

# A 函数极限的计算方法_第9页.png

## 结论
若同一极限过程下$\lim \frac{f(x)}{g(x)}=A$，且$\lim g(x)=0$，则$\lim f(x)=0$。
**证明：**
由极限四则运算法则：
$$\lim \frac{f(x)}{g(x)} \cdot \lim g(x) = \lim \left( \frac{f(x)}{g(x)} \cdot g(x) \right) = \lim f(x)$$
代入已知条件得：
$$\lim f(x) = A\cdot 0 = 0$$

若同一极限过程下$\lim \frac{f(x)}{g(x)}=A\neq0$，且$\lim f(x)=0$，则$\lim g(x)=0$。
**证明：**
由极限四则运算法则：
$$\frac{\lim f(x)}{\lim \frac{f(x)}{g(x)}} = \lim \frac{f(x)}{\frac{f(x)}{g(x)}} = \lim g(x)$$
代入已知条件得：
$$\lim g(x) = \frac{0}{A} = 0$$

即：当$\lim \frac{f(x)}{g(x)}=A\neq0$时，$f(x)\to0$与$g(x)\to0$互为充要条件：若$f(x)\to0$则必有$g(x)\to0$，若$g(x)\to0$则必有$f(x)\to0$。
注：该性质对应：当两个函数商的极限为非零常数时，二者为同阶无穷小。

## 例1.21
设$\lim\limits_{x \to 0} \frac{\sin x}{e^x - a}(\cos x - b)=5$，则$b=\underline{\quad\quad}$。
解：
当$x\to0$时，$\sin x \to 0$，因此分子$\sin x (\cos x - b) \to 0$；
由于题设极限为非零常数5，因此分母必须满足$e^x - a \to 0$（否则极限为0，与题设矛盾）。
当$x\to0$时$e^x \to 1$，因此：
$$\lim_{x \to 0} (e^x - a) = \lim_{x \to 0}e^x - \lim_{x \to 0}a = 1 - a = 0$$
解得$a=1$。
当$x\to0$时，有等价无穷小$e^x -1 \sim \sin x$，因此$\lim\limits_{x\to0}\frac{\sin x}{e^x -1}=1$，代入原式可得：
$$\lim_{x \to 0} \frac{\sin x}{e^x -1} \cdot (\cos x - b) = \lim_{x \to 0} (\cos x - b) =5$$
计算极限：
$$\lim_{x \to 0}\cos x - \lim_{x \to 0}b = 1 - b =5$$
解得$b=-4$。

（右侧附$\cos x$函数示意图）

---

# A 函数极限的计算方法_第10页.png

## 0/0型未定式的直观推导（洛必达法则思想）
当 $\lim_{x \to x_0} f(x) = 0$，$\lim_{x \to x_0} g(x) = 0$ 时，
$$\lim_{x \to x_0} \frac{f(x)}{g(x)} = ?$$ 该如何计算？

给出具体例子：
$$
\begin{align*}
f(x) &= x^2 + 3x - 4 \\
g(x) &= \ln x
\end{align*}
$$
求 $\lim_{x \to 1} \frac{f(x)}{g(x)}$。

（函数示意图1：平面直角坐标系中绘制了开口向上的抛物线$f(x)$与对数曲线$g(x)=\ln x$，两曲线在$(1,0)$处相交，交点处标注了圆圈。）

对交点处的局部区域做无限放大：
> 类比：地球整体是球面（对应曲线），但在人站立的局部区域看起来是平面（对应直线），即脚下的地板是平直的。
> 对应到函数：交点附近的曲线被无限放大后会近似为直线（切线）。

（函数示意图2：$x=1$处局部放大后的示意图，以$(1,0)$为原点，标注了水平向右的自变量增量$dx$，以及两个函数近似得到的两条过原点的直线：更陡的直线对应$f(x)$，更平缓的对应$g(x)$，标注了竖直方向的增量$df$、$dy$。）

---

明显，当$dx \to 0$时，两个无穷小趋近于0的速度快慢取决于切线斜率：可以看出$dy$更快趋近于0，因此该推导仅适用于$f(x)\to0$、$g(x)\to0$的0/0型情况。

$dy \to 0$、$df \to 0$的速度差距可以由斜率的差距来表现：由于放大后曲线近似为直线，直线上各点斜率恒定等于该点切线斜率，因此：
$$
k_1 = \frac{df}{dx} = f'(1), \quad k_2 = \frac{dg}{dx} = g'(1)
$$
因此可以得到：
$$
\lim_{x \to 1} \frac{f(x)}{g(x)} = \frac{f'(1)}{g'(1)}$$
只需要求出$x=1$处两个函数的导数值即可计算极限。

根据导数的定义，结合$f(1)=0, g(1)=0$，因此：
$$
\lim_{x \to 1} \frac{f(x)}{x-1} = f'(1), \quad \lim_{x \to 1} \frac{g(x)}{x-1} = g'(1)
$$
两式相除消去共同的无穷小因子$x-1$，可得：
$$
\lim_{x \to 1} \frac{f(x)}{g(x)} = \lim_{x \to 1} \frac{f'(x)}{g'(x)}$$
即0/0型极限可以通过对分子、分母分别求导后，再取极限相除得到结果。

方法推广：
1.  若一阶导数求完后，$\lim_{x \to x_0}\frac{f'(x)}{g'(x)}$仍是0/0型（即一阶趋近速度相同），可以用二阶导数（对应“加速度”）的比值计算；
2.  若二阶导数仍为0/0型，可以继续用更高阶导数的比值计算，以此类推。

---

# A 函数极限的计算方法_第11页.png

## 洛必达法则
### 法则1
- 在$x \to x_0$（或$x \to \infty$）时，$\begin{cases} f(x) \to 0 \\ g(x) \to 0 \end{cases}$
- 在$x \to x_0$（或$x \to \infty$）时，$\lim f'(x)$存在，$\lim g'(x)$存在
- 在$x \to x_0$（或$x \to \infty$）时，$\lim \frac{f'(x)}{g'(x)}$存在

则在$x \to x_0$（或$x \to \infty$）时：
$$\lim \frac{f(x)}{g(x)} = \lim \frac{f'(x)}{g'(x)} = \lim \frac{f''(x)}{g''(x)}$$

$\frac{1}{无穷小} = \infty$

$\Rightarrow$ 当$\lim\limits_{x \to x_0} f(x) = \infty$，$\lim\limits_{x \to x_0} g(x) = \infty$时，
$\lim\limits_{x \to x_0} \frac{f(x)}{g(x)} = ?$ 也能算

证明：
$$\frac{f(x)}{g(x)} = \frac{\frac{1}{g(x)}}{\frac{1}{f(x)}}$$

$\lim\limits_{x \to x_0} f(x) = \infty$，$\lim\limits_{x \to x_0} \frac{1}{f(x)} = 0$
$\lim\limits_{x \to x_0} g(x) = \infty$，$\lim\limits_{x \to x_0} \frac{1}{g(x)} = 0$

$$\lim_{x \to x_0} \frac{f(x)}{g(x)} = \lim_{x \to x_0} \frac{\frac{1}{g(x)}}{\frac{1}{f(x)}} = \lim_{x \to x_0} \frac{f'(x)}{g'(x)} = \frac{f'(x_0)}{g'(x_0)}$$

### 法则2
- 在$x \to x_0$（或$x \to \infty$）时，$\begin{cases} f(x) \to \infty \\ g(x) \to \infty \end{cases}$
- 在$x \to x_0$（或$x \to \infty$）时，$\lim f'(x)$存在，$\lim g'(x)$存在且$\lim g'(x) \neq 0$
- 在$x \to x_0$（或$x \to \infty$）时，$\lim \frac{f'(x)}{g'(x)}$存在

则在$x \to x_0$（或$x \to \infty$）时：
$$\lim \frac{f(x)}{g(x)} = \lim \frac{f'(x)}{g'(x)} = \lim \frac{f''(x)}{g''(x)}$$

---

# A 函数极限的计算方法_第12页.png

## 双曲正弦与反双曲正弦函数
双曲正弦函数：$y=\frac{e^x - e^{-x}}{2}$，为奇函数。

反双曲正弦函数：$y=\ln\left(x+\sqrt{1+x^2}\right)$，为奇函数，其导数为：
$$y'=\frac{1}{\sqrt{1+x^2}}$$
（附反双曲正弦函数示意图：过原点的奇函数形态曲线）

## 1.22  $x \to 0$时的等价无穷小
### (1) $\ln\left(x+\sqrt{1+x^2}\right) \sim x$
推导：
当$x \to 0$时，$\lim\limits_{x \to 0} \ln\left(x+\sqrt{1+x^2}\right)=0$，$\lim\limits_{x \to 0} x=0$，该极限为$\frac{0}{0}$型，使用洛必达法则计算：
对分子分母分别求导：
$$\left[\ln\left(x+\sqrt{1+x^2}\right)\right]' = \frac{1}{\sqrt{1+x^2}}$$
$$(x)' = 1$$
因此：
$$\lim_{x \to 0} \frac{\ln\left(x+\sqrt{1+x^2}\right)}{x} = \lim_{x \to 0} \frac{\frac{1}{\sqrt{1+x^2}}}{1} = 1$$
$\Rightarrow$ 结论：当$x \to 0$时，$\ln\left(x+\sqrt{1+x^2}\right) \sim x$。

### (2) $1-(\cos x)^a \sim \frac{1}{2}a x^2 \quad (a \neq 0)$
推导：
当$x \to 0$时，该极限为$\frac{0}{0}$型，使用洛必达法则计算：
对分子分母分别求导：
$$\left[1-(\cos x)^a\right]' = -a (\cos x)^{a-1} \cdot (-\sin x)$$
$$\left[\frac{1}{2}a x^2\right]' = a x$$
由洛必达法则：
$$\lim_{x \to 0} \frac{1-(\cos x)^a}{\frac{1}{2}a x^2} = \lim_{x \to 0} \frac{-a (\cos x)^{a-1} \cdot (-\sin x)}{a x} = 1$$
（化简利用$x \to 0$时$\sin x \sim x$约去无穷小因子，且$\lim\limits_{x\to0}(\cos x)^{a-1}=1$）
$\Rightarrow$ 结论：当$x \to 0$时，$1-(\cos x)^a \sim \frac{1}{2}a x^2 \quad (a \neq 0)$。

#### 例子
取$a=\frac{1}{2}$代入结论，可得：
$$1-\sqrt{\cos x} \sim \frac{1}{4}x^2$$

---

# A 函数极限的计算方法_第13页.png

## 1.23 无穷大大小比较
设$f(x)=\ln^{10}x$，$g(x)=x$，$h(x)=e^{\frac{x}{10}}$，则当$x$充分大时，试比较三者的大小。
$\frac{\infty}{\infty}$型，用洛必达法则。
$$\lim_{x \to +\infty} \frac{x}{\ln^{10}x} \xlongequal{\text{洛}} \lim_{x \to +\infty} \frac{1}{10\ln^{9}x \cdot \frac{1}{x}} \xlongequal{\text{化简}} \lim_{x \to +\infty} \frac{x}{10\ln^{9}x}$$
$$\xlongequal{\text{洛}} \lim_{x \to +\infty} \frac{x}{10\cdot9\ln^{8}x} \xlongequal{\text{洛}} \dots \xlongequal{\text{洛}} \lim_{x \to +\infty} \frac{x}{10\cdot9\cdot8\cdots2\cdot1\cdot \ln x}$$
$$\xlongequal{\text{洛}} \frac{1}{10!} \cdot \lim_{x \to +\infty} \frac{1}{\frac{1}{x}} = +\infty$$
$\implies x \gg \ln^{10}x$（远远大于）
$$\lim_{x \to +\infty} \frac{e^{\frac{x}{10}}}{x} \xlongequal{\text{洛}} \lim_{x \to +\infty} \frac{e^{\frac{x}{10}} \cdot \frac{1}{10}}{1} = +\infty$$
（复合函数求导：$(e^u)' = e^u \cdot u'$）
$\implies e^{\alpha x} \gg x^\beta \quad (\alpha,\beta>0)$
---
### 常用结论
结论：当$x \to +\infty$时，（考试直接用）有
$$\ln^\alpha x \ll x^\beta \ll a^x \quad (\alpha,\beta>0,\ a>1)$$
提速记忆：对数函数、幂函数、指数函数，增长速度依次递增。
当$n \to \infty$时，有
$$\ln^\alpha n \ll n^\beta \ll a^n \ll n! \ll n^n \quad (\alpha,\beta>0,\ a>1)$$

---

# A 函数极限的计算方法_第14页.png

## 函数差异与逐阶比较的直观逻辑
- 函数与函数不同的原因就是：在自变量相同的变化下，因变量变化不同，而斜率是变化不同的原因。
- 洛必达用$f(x)$与$g(x)$在$x_0$上的斜率的差距，来表现出$f(x),g(x)$趋近于$f(x_0),g(x_0)$的快慢差距：
  即$f(x_0)=g(x_0)$，且$f'(x_0) \neq g'(x_0)$；
  若$f'(x_0)=g'(x_0)$，则$f''(x_0) \neq g''(x_0)$，则比较$g''(x_0)$与$f''(x_0)$。
- 若两者在$x_0$上的斜率相同，即$f'(x_0)=g'(x_0)$，则两个函数在数值上就更相近；
  同样，若两者在$x_0$上的斜率的斜率也相同，则两个函数在数值上就更加相近。

今想让两个函数无限相近，则需要满足：
$$
\begin{aligned}
f(x_0) &= g(x_0) \\
f'(x_0) &= g'(x_0) \\
f''(x_0) &= g''(x_0) \\
&\vdots \\
f^{(+\infty)}(x_0) &= g^{(+\infty)}(x_0)
\end{aligned}
\quad \bigg\downarrow \text{两函数越来越相近}
$$

## 函数拟合的条件与分步思路
若想找一个$g(x)$无限拟合于$f(x)$的话，只用让$g(x)$满足：
① $f(x_0) = g(x_0) = a_0$
② $f'(x_0) = g'(x_0) = a_1$
③ $f''(x_0) = g''(x_0) = a_2$
④ $f'''(x_0) = g'''(x_0) = a_3$
$\vdots$
$\infty$. $f^{(\infty)}(x_0) = g^{(\infty)}(x_0) = a_\infty$

直接找的话，这是一个很抽象的问题。那，我们先不看②、③、④…，先看①，先满足①，再在①的基础上，再看②。
就将一个复杂的问题分割成一个个的小问题。

---

# A 函数极限的计算方法_第15页.png

## 点$x_0$处泰勒近似多项式构造
① 找$g(x)$满足$f(x_0)=g(x_0)=a_0$
设$g(x)=a_0$ \tag{1.0}
则$g(x_0)=a_0$

② 找$g(x)$满足
$$\begin{cases}
f(x_0)=g(x_0)=a_0 \\
f'(x_0)=g'(x_0)=a_1
\end{cases}$$
$\because g(x)=a_0$时，$g'(x)=0$，
又$(x)'=1!$，
$\therefore$ 设$g(x)=a_0+a_1 x$ \tag{2.0}
则$g'(x)=a_1$，$g'(x_0)=a_1$
$\because g(x_0)=a_0+a_1 x_0 \neq a_0$
$\therefore g(x)=a_0+a_1(x-x_0)$ \tag{2.1}
即$g(x)=a_0+a_1 x - a_1 x_0$
则$g'(x)=a_1$，$g(x_0)=a_0$

③ 找$g(x)$满足
$$\begin{cases}
f(x_0)=g(x_0)=a_0 \\
f'(x_0)=g'(x_0)=a_1 \\
f''(x_0)=g''(x_0)=a_2
\end{cases}$$
$\because g(x)=a_0+a_1(x-x_0)$时，$g''(x)=0$，
又$(x^2)''=2!$，$\left(\frac{x^2}{2!}\right)''=1$，
$\therefore$ 设$g(x)=a_0+a_1(x-x_0)+\frac{a_2 x^2}{2!}$ \tag{3.0}
则$g''(x)=a_2$，$g''(x_0)=a_2$
$\because g(x_0)=a_0+\frac{a_2 x_0^2}{2!} \neq a_0$
$\therefore g(x)=a_0+a_1(x-x_0)+\frac{a_2(x-x_0)^2}{2!}$ \tag{3.1}
即
$$g(x)=a_0+a_1 x - a_1 x_0 + \frac{a_2 x^2 - 2a_2 x x_0 + a_2 x_0^2}{2!}$$
则$g(x_0)=a_0$，$g'(x_0)=a_1$，$g''(x_0)=a_2$