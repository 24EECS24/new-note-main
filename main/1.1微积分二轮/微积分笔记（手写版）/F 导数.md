---

# F 导数_第1页.png

## 一元函数微分学的概念
## 导数引例
（函数示意图：函数$x=f(t)$的整体图像，横轴为$t$，纵轴为$x$；图像从原点（对应$t=t_0=0$）出发单调上升至$t=t_1$处，随后水平延伸至$t=t_2$处，再单调下降至$t=t_3$处回到横轴。）

在区间$t_0\sim t_1$中：
$$\frac{f(t+\Delta t)-f(t)}{\Delta t}$$
为$x$关于$t$的平均变化率，也等于$x$关于$t$的瞬时变化率。

在区间$t_2\sim t_3$中：
$$\frac{f(t+\Delta t)-f(t)}{\Delta t}$$
为$x$关于$t$的平均变化率。

在区间$t_0\sim t_3$中：
$$\frac{f(t_3)-f(t_0)}{t_3} = \frac{0}{t_3}=0$$
$x$关于$t$在该区间的平均变化率为$0$，完全掩盖了$x$在$t_0\sim t_3$之间随时间$t$的实际变化情况。

由此可知：平均变化率是一个极其粗糙的概念。

在区间$t_2\sim t_3$中：
$$\frac{f(t+\Delta t)-f(t)}{\Delta t}$$
为$x$在$t\sim t+\Delta t$之间随时间$t$的平均变化率。

为了研究其间的瞬时变化率，令$\Delta t \to 0$，即$t+\Delta t$无限靠近$t$。
（局部函数示意图：$x=f(t)$的单调下降段局部图像，标注了位置$t$与$t+\Delta t$，表示$\Delta t \to 0$时$t+\Delta t$趋近于$t$。）

若极限$\lim\limits_{\Delta t \to 0} \frac{f(t+\Delta t)-f(t)}{\Delta t}$存在，
则称该极限值为$x$在$t$这一点处的瞬时变化率，不同数学家给出了不同记号：
- 拉格朗日记为$f'(t)$
- 莱布尼茨记为$\dfrac{df(t)}{dt}$，其中分子$df(t)$为$x$的微分，分母$dt$为$t$的微分
- 牛顿记为$\dot{f}(t)$

如今我们统一使用如下定义：
$$\lim_{\Delta t \to 0} \frac{f(t+\Delta t)-f(t)}{\Delta t} = f'(t) = \frac{df(t)}{dt}$$

---

# F 导数_第2页.png

极限是研究函数的变化趋势。
导数是建立在研究变化趋势之上的，研究变化的快慢：增、减、不变…
设$y=f(x)$定义在区间$I$上，让自变量在$x=x_0$处加一个增量$\Delta x$（可正可负），其中$x_0\in I$，$x_0+\Delta x\in I$。
则可得函数的增量$\Delta y = f(x_0+\Delta x)-f(x_0)$。
若函数增量$\Delta y$与自变量的增量$\Delta x$的比值在$\Delta x\to0$时的极限值存在，即$\lim\limits_{\Delta x \to 0} \frac{\Delta y}{\Delta x}$存在，则称函数$y=f(x)$在点$x_0$处可导，并称这个极限值为$y=f(x)$在点$x_0$处的导数，记作$f'(x_0)$。
$$f'(x_0)=\lim_{\Delta x \to 0} \frac{\Delta y}{\Delta x} = \lim_{\Delta x \to 0} \frac{f(x_0+\Delta x)-f(x_0)}{\Delta x}$$
即$f'(x_0)$为$f(x)$在$x_0$处的瞬时变化率。
在微积分中，瞬时变化率叫作变化率。

## 注
$$f'(x_0)=\lim_{\Delta x \to 0} \frac{f(x_0+\Delta x)-f(x_0)}{\Delta x}$$
增量广义化形式：
$$f'(x_0)=\lim_{\text{狗}\to0} \frac{f(x_0+\text{狗})-f(x_0)}{\text{狗}}$$
令$x_0+\Delta x = x$，可得导数的等价定义形式：
$$f'(x_0)=\lim_{x \to x_0} \frac{f(x)-f(x_0)}{x-x_0}$$

$$
\left.
\begin{aligned}
y=f(x)\text{在点}x_0\text{处可导}\\
y=f(x)\text{在点}x_0\text{处导数存在}\\
f'(x_0)\text{存在}
\end{aligned}
\right\}
\text{三种说法均一样}
$$

---

# F 导数_第3页.png

## 函数在一点可导的充要条件
### ① 单侧导数
- $f(x)$在点$x_0$处的左导数：
$$\lim_{\Delta x \to 0^-} \frac{f(x_0+\Delta x)-f(x_0)}{\Delta x} = f'_-(x_0)$$
- $f(x)$在点$x_0$处的右导数：
$$\lim_{\Delta x \to 0^+} \frac{f(x_0+\Delta x)-f(x_0)}{\Delta x} = f'_+(x_0)$$
### ② 可导的充要条件
$f'(x_0)$存在$\iff f'_-(x_0)$存在，$f'_+(x_0)$存在且$f'_-(x_0)=f'_+(x_0)$。
这一点与极限的存在性对应，因为本质上，导数的定义就是一个极限问题。
---
### 可导必连续
若$f(x)$在一点可导$\implies f(x)$在该点连续。
**证明：**
$$\lim_{\Delta x \to 0} \frac{f(x+\Delta x)-f(x)}{\Delta x} = a$$
$$\implies \lim_{\Delta x \to 0} \left[f(x+\Delta x)-f(x)\right] = \lim_{\Delta x \to 0} a\cdot \Delta x = 0$$
$$\implies \lim_{\Delta x \to 0} f(x+\Delta x) - \lim_{\Delta x \to 0} f(x) = 0$$
$$\implies f(x) = \lim_{\Delta x \to 0} f(x+\Delta x)$$
$\implies$ $f(x)$在该点连续。
> **注**：
> $f(x)$在$x=x_0$处可导$\implies f(x)$在$x=x_0$处连续
> $\nRightarrow f(x)$在$x=x_0$附近连续
> $\nRightarrow f(x)$在$x=x_0$附近可导
一个函数的连续、可导，都是点信息。
如果说$f(x)$在区间$I$上的所有点都可导，才可以说$f(x)$在区间$I$上可导。

---

# F 导数_第4页.png

## 例3.1
以下命题是否正确：若$f(x)$是可导的偶函数，则$f'(x)$是奇函数。
其中的$x$是泛指点，指$f(x)$定义域上任一点，需证明$f'(-x) = -f'(x)$。
由导数定义：
$$
f'(-x) = \lim_{\Delta x \to 0} \frac{f(-x+\Delta x) - f(-x)}{\Delta x}
$$
因$f(x)$是偶函数，满足$f(-x)=f(x)$，代入得：
$$
= \lim_{\Delta x \to 0} \frac{f(x-\Delta x) - f(x)}{\Delta x}
$$
对极限式做恒等变形，凑导数定义形式：
$$
= \lim_{-\Delta x \to 0} \frac{f(x+(-\Delta x)) - f(x)}{-\Delta x} \cdot (-1)
$$
注：变形依据为恒等式$a = a\cdot b\cdot \frac{1}{b}$，此处取$b=-1$，即$a = a\cdot (-1)\cdot (-1)$；当$\Delta x \to 0$时，$-\Delta x \to 0$，可按导数定义化简极限。
最终得：
$$
= -f'(x)
$$
结论：可导偶函数的导函数是奇函数，即**每求一次导，函数奇偶性互换**。

## 3.1
题目：设$f(x)=\ln(1-x)-\ln(1+x),\ -1<x<1$，则$f''(0)=\underline{\quad\quad}$
解：整理函数表达式：
$$f(x)=\ln\frac{1-x}{1+x}$$
易验证$f(x)$是奇函数；
根据“求导一次奇偶性互换”的结论：
1.  一阶导数$f'(x)$为偶函数；
2.  二阶导数$f''(x)$为奇函数；
奇函数在$x=0$处有定义时函数值为0，因此：
$$f''(0)=0$$
规律：只要是偶阶导函数就是奇函数，因此该函数任意偶数阶导数在0点的取值均为0，即：
$$f^{(6)}(0)=0$$

---

# F 导数_第5页.png

## 3.2
设$f(x)=\frac{1}{2^x +1},\ x\in\mathbb{R}$，则$f^{(4)}(0)=$____
由前面所讲内容可知$f(x)=\frac{1}{2^x +1}$不具有奇偶性，但$f(x)=\frac{1}{2^x +1}-\frac{1}{2}$为奇函数。
解：将$f(x)$拆分得：
$$f(x)=\underbrace{\frac{1}{2^x +1}-\frac{1}{2}}_{g(x)} + \frac{1}{2}$$
注：$\frac{1}{2}$为常数，求一次导数后即为0，在高阶导数中消失。
因此有：
$$f^{(4)}(x)=g^{(4)}(x)$$
$g(x)$为奇函数，根据奇偶函数导数的奇偶性规律，可得$g^{(4)}(x)$为奇函数。
由奇函数在$x=0$处的函数值为0，得：
$$g^{(4)}(0)=0 = f^{(4)}(0)$$
若$f(x)$是可导的、周期为$T$的周期函数，则$f'(x)$也是以$T$为周期的周期函数。
即：
$$f(x+T)=f(x)$$
证明$f'(x+T)=f'(x)$：
根据导数定义：
$$
\begin{align*}
f'(x+T)&=\lim_{\Delta x \to 0} \frac{f(x+T+\Delta x)-f(x+T)}{\Delta x}\\
&=\lim_{\Delta x \to 0} \frac{f(x+\Delta x)-f(x)}{\Delta x}\\
&=f'(x)
\end{align*}
$$
得证。
## 例32
设$f(x)$是二阶可导且以2为周期的奇函数，$f\left(\frac{1}{2}\right)>0$，$f'\left(\frac{1}{2}\right)>0$。记$M=f\left(-\frac{1}{2}\right)$，$N=f'\left(\frac{3}{2}\right)$，$K=f''(0)$，则$M,N,K$的大小顺序为____

---

# F 导数_第6页.png

解：
$M = f\left(-\frac{1}{2}\right) = -f\left(\frac{1}{2}\right) < 0$
$N = f'\left(\frac{3}{2}\right) = \underbrace{f'\left(\frac{3}{2} - 2\right)}_{\text{周期性}} = \underbrace{f'\left(-\frac{1}{2}\right) = f'\left(\frac{1}{2}\right)}_{f(x)\text{奇}\Rightarrow f'(x)\text{偶}} > 0$
$k = f''(0) = 0$（$f''(x)$为奇函数）
$\Rightarrow N > k > M$

## 判断题
判断对错：若$f(x)$是可导的有界函数，则$f'(x)$是有界函数。
举个反例：$f(x) = \sqrt{x},\ x \in (0,1]$
函数示意图：$y=\sqrt{x}$
当$x \to 0^+$时，该函数的切线是一条竖直的线，导数值即切线斜率是无穷大，即变化率是无穷大，因此$f'(x)$是无界的。
但$f(x) \in (0,1]$是有界的。
$\Rightarrow$ 该命题是错误的。

## 例3.3
设$f(x)$在$x=0$的某邻域内有定义，并且$|f(x)| \leq 1-\cos x$，则$f(x)$在$x=0$处（C）
A. 极限存在但不连续
B. 连续但不可导
C. 可导且$f'(0)=0$
D. 可导且$f'(0) \neq 0$

---

# F 导数_第7页.png

解：已知 $0<|f(x)|\leqslant 1-\cos x$
当$x\to0$时，对不等式各项取极限，由夹逼准则：
$$\lim_{x\to 0}0 \leqslant \lim_{x\to 0}|f(x)| \leqslant \lim_{x\to 0}(1-\cos x)$$
不等式左右两侧极限均为0，因此：
$$\lim_{x\to 0}|f(x)|=0 \iff \lim_{x\to 0}f(x)=0 \quad (\text{前面有讲})$$
$\because f(x)$在$x=0$附近有定义，$\therefore f(0)$存在；代入$x=0$得：
$1-\cos 0 = 0$
因此$x=0$时，$|f(0)|\leqslant 1-\cos 0 = 0$
可得$f(0)=0$
因此$\lim_{x\to 0}f(x)=f(0)$
即$f(x)$在$x=0$处连续。

求$f'(0)$：
令$0+\Delta x = x$，由导数定义：
$$f'(0)=\lim_{x\to 0}\frac{f(x)-f(0)}{x-0}=\lim_{x\to 0}\frac{f(x)}{x}$$
由$|f(x)|\leqslant 1-\cos x$，不等式两边同时除以$|x|$得：
$$\frac{|f(x)|}{|x|}\leqslant \frac{1-\cos x}{|x|}$$
即
$$0\leqslant \frac{|f(x)|}{|x|}\leqslant \frac{1-\cos x}{|x|}$$
当$x\to0$时，利用等价无穷小：$x\to0$时$1-\cos x \sim \frac{1}{2}x^2$，因此
$$\frac{\frac{1}{2}x^2}{|x|}\to 0$$
由夹逼准则：
$$\lim_{x\to 0}\frac{|f(x)|}{|x|}=0 \iff \lim_{x\to 0}\frac{f(x)}{x}=f'(0)$$
因此$f'(0)=0$

## 乘积求导法则
两函数乘积的求导法则：
$$(u\cdot v)'=u'v+uv'$$
趣味记忆口诀：（要打都打，这样才公平；你一把掌，我一把掌）

同理，三个函数乘积的求导法则：
$$(u_1\cdot u_2\cdot u_3)'=u_1'u_2u_3 + u_1u_2'u_3 + u_1u_2u_3'$$

---

# F 导数_第8页.png

## 例3.4
设函数$f(x)=(e^x - 1)(e^{2x} - 2)\cdots(e^{nx} - n)$，其中$n$为正整数，则$f'(0)=$\underline{\qquad}
解：当$x=0$时，只有因子$(e^x - 1)=0$，其余因子均非0。
令$g(x)=(e^{2x} - 2)(e^{3x} - 3)\cdots(e^{nx} - n)$，
则$f(x)=(e^x - 1)g(x)$。
由乘积求导法则：
$$
\begin{align*}
f'(x)&=(e^x - 1)'g(x)+(e^x - 1)g'(x)\\
&=e^x\cdot g(x)+(e^x - 1)g'(x)
\end{align*}
$$
代入$x=0$计算导数值：
$$
\begin{align*}
f'(0)&=e^0\cdot g(0)+(e^0 - 1)g'(0)\\
&=g(0)+0\cdot g'(0)\\
&=g(0)\\
&=(-1)\cdot(-2)\cdot(-3)\cdot\cdots\cdot(-(n-1))\\
&=(-1)^{n-1}\cdot (n-1)!
\end{align*}
$$

## 例3.5 一个重要的结论
设$f(x)$在$x=a$处连续，$F(x)=f(x)|x-a|$，则$f(a)=0$是$F(x)$在$x=a$处可导的**充要条件**。
### 分析
由乘积求导法则：
$$F'(x)=\left(f(x)|x-a|\right)'=f'(x)|x-a|+f(x)\cdot |x-a|'$$
基础函数可导性对比：
1.  $y=x$在$x=0$处可导，斜率为1，对应过原点、斜率为1的直线示意图。
2.  $y=|x|$在$x=0$处不可导，因为左导数$f'_-(0)\neq$右导数$f'_+(0)$，斜率不相等，对应顶点在原点的V形折线示意图。

本题思路：这一题讨论$F(x)$在$x=a$处的可导性，$|x-a|$在$x=a$（即$t=x-a=0$）处不可导，要让乘积$y=f(x)|x-a|$在$x=a$处可导，需要$f(x)$抵消$|x-a|$在该点的不可导性，“拯救”该点的可导性。

---

# F 导数_第9页.png

## 带绝对值因式的函数可导性推导
解：先把绝对值打开，写成分段函数：
$$
F(x)=
\begin{cases}
-f(x)(x-a), & x<a \\
0, & x=a \\
f(x)(x-a), & x>a
\end{cases}
$$
（附绝对值函数示意图：顶点在原点的V型折线，对应$y=|x|$的图像形态）

当$x<a$时，计算$x=a$处的左导数：
$$F'_-(a)=\lim_{x \to a^-} \frac{-f(x)(x-a)-0}{x-a}=-f(a)$$

当$x>a$时，计算$x=a$处的右导数：
$$F'_+(a)=\lim_{x \to a^+} \frac{f(x)(x-a)-0}{x-a}=f(a)$$

则当$-f(a)=f(a)$时，$F(x)$在$x=a$处可导，$F'(a)$存在。
$\Rightarrow$ 当$f(a)=0$时，满足$-f(a)=f(a)$，$F'(a)$存在，该条件为充要条件。

$\Rightarrow$ 推广结论：当$y=|x-x_0|$在$x=x_0$处不可导时，若乘以因式$f(x)$，其中
$$f(x) \text{满足}
\begin{cases}
\text{在}x=x_0\text{处连续} \\
f(x_0)=0
\end{cases}$$
则$F(x)=f(x)|x-x_0|$在$x=x_0$处可导。

## 例3.6(1)
题目：$f(x)=(x^2-1)|x^3+x^2-2x-2|$的不可导点的个数为$\underline{\qquad}$

解：把绝对值内的多项式因式分解，拆分绝对值：
$$
\begin{align*}
f(x)&=(x^2-1)\left|x^3+x^2-2x-2\right|\\
&=(x^2-1)\left|x^2(x+1)-2(x+1)\right|\\
&=(x^2-1)\left|(x^2-2)(x+1)\right|\\
&=(x^2-1)|x+1|\cdot |x+\sqrt{2}|\cdot |x-\sqrt{2}|\\
&=(x-1)(x+1)|x+1|\cdot |x+\sqrt{2}|\cdot |x-\sqrt{2}|
\end{align*}
$$

若没有因式$(x-1)(x+1)$，则$f(x)$在$x=-1$、$x=-\sqrt{2}$、$x=\sqrt{2}$处均不可导；但乘以因式$(x-1)(x+1)$后，$x=-1$处对应因式$(x+1)$在该点连续且取值为0，因此该点可导。

因此$f(x)$的不可导点为$x=-\sqrt{2}$、$x=\sqrt{2}$，共2处。

---

# F 导数_第10页.png

## 例3.6(2)
求$f(x)=(x^2-1)|x^3-2x^2-x+2|$的不可导点个数$\underline{\qquad}$
解：
$$
\begin{align*}
f(x)&=(x^2-1)\left|x^2(x-2)-(x-2)\right|\\
&=(x^2-1)\left|(x^2-1)(x-2)\right|\\
&=(x^2-1)\left|(x-1)(x+1)(x-2)\right|\\
&=(x-1)(x+1)|x-1||x+1||x-2|
\end{align*}
$$
若没有$(x-1)(x+1)$的话，不可导点为$x=1$，$x=-1$，$x=2$
但乘了$(x-1)(x+1)$之后，$f(x)$的不可导点为$x=2$，共一处。

## 例3.6(3)
$$f(x)=(x^2-1)\left|x^3+3x^2-2x-6\right|$$
解：
$$
\begin{align*}
f(x)&=(x^2-1)\left|x^2(x+3)-2(x+3)\right|\\
&=(x^2-1)\left|(x^2-2)(x+3)\right|\\
&=(x+1)(x-1)|x+\sqrt{2}||x-\sqrt{2}||x+3|
\end{align*}
$$
若没有$(x^2-1)$的话，不可导点为$x=\sqrt{2}$，$x=-\sqrt{2}$，$x=-3$
乘了$(x^2-1)$之后，不可导点仍为$x=\sqrt{2}$，$x=-\sqrt{2}$，$x=-3$，共3处。

## 3.3
设$f(x)$在$x=0$处可导，$f\left(\frac{1}{n}\right)=\frac{2}{n}$，$n=1,2,\dots$，则$f'(0)=\underline{\qquad}$
### 解法1
$$
\begin{align*}
f\left(\frac{1}{n}\right)&=\frac{2}{n}\\
\implies f(x)&=2x\\
f'(x)&=2\\
\implies f'(0)&=2
\end{align*}
$$

### 解法2
$\because f(x)$在$x=0$处可导
$\therefore \lim\limits_{x\to 0}f(x)=f(0)$
由归结原则：
$$\lim_{\frac{1}{n}\to 0^+}f\left(\frac{1}{n}\right)=0 \implies f(0)=0$$
由导数定义：
$$f'(0)=\lim_{x\to 0}\frac{f(x)-f(0)}{x-0}=\lim_{x\to 0}\frac{f(x)}{x}$$
由归结原则：
$$
\lim_{\frac{1}{n}\to 0^+}\frac{f\left(\frac{1}{n}\right)}{\frac{1}{n}}=\lim_{\frac{1}{n}\to 0^+} n\cdot \frac{2}{n}=2
$$

---

# F 导数_第11页.png

## 3.4
设$f(x)$在$x=0$处可导，$f(0)=f'(0)=\sqrt{2}$，则
$$\lim_{x \to 0} \frac{f^2(x)-2}{x} = \underline{\qquad}$$
解：
$$
\begin{aligned}
\text{原式} &= \lim_{x \to 0} \frac{f(x)-\sqrt{2}}{x} \cdot \frac{f(x)+\sqrt{2}}{1} \\
&= \lim_{x \to 0} \frac{f(x)-f(0)}{x-0} \cdot \frac{f(x)+\sqrt{2}}{1} \\
&= \lim_{x \to 0} \frac{f(x)-f(0)}{x-0} \cdot \lim_{x \to 0} \frac{f(x)+\sqrt{2}}{1} \\
&= f'(0) \cdot (\sqrt{2}+\sqrt{2}) \\
&= 4
\end{aligned}
$$

## 3.5
设$f(x)=\frac{1}{n^2}$，其中$\frac{1}{n^2+1} < x \leq \frac{1}{n^2},\ n=1,2,3,\cdots$，且$f(0)=0$，则$f'_+(0)=\underline{\qquad}$。
解：
根据右导数定义：
$$f'_+(0) = \lim_{x \to 0^+} \frac{f(x)-f(0)}{x-0} = \lim_{x \to 0^+} \frac{f(x)}{x}$$
当$\frac{1}{n^2+1} < x \leq \frac{1}{n^2}$时，$f(x)=\frac{1}{n^2}$，对区间不等式取倒数得：
$$n^2 \leq \frac{1}{x} < n^2+1$$
对$\frac{f(x)}{x}$做放缩：
$$\frac{\frac{1}{n^2}}{\frac{1}{n^2}} \leq \frac{f(x)}{x} \leq \frac{\frac{1}{n^2}}{\frac{1}{n^2+1}}$$
即
$$1 \leq \frac{f(x)}{x} \leq \frac{n^2+1}{n^2}$$
当$x \to 0^+$时对应$n \to \infty$，此时$\lim\limits_{n \to \infty}\frac{n^2+1}{n^2}=1$，由夹逼准则可得：
$$\lim_{x \to 0^+} \frac{f(x)}{x} = 1$$
即$f'_+(0)=1$。

---

# F 导数_第12页.png

## 3.6
设可导函数$f(x)>0$，则
$$\lim_{n \to \infty} n\cdot \ln \frac{f(\frac{1}{n})}{f(0)} = \underline{\quad\quad}$$
旁注：对数运算性质 $\ln\frac{A}{B}=\ln A - \ln B$。
解：
$$
\begin{align*}
\text{原式}&=\lim_{n \to \infty} n\cdot \left(\ln f\left(\frac{1}{n}\right) - \ln f(0)\right) \\
&=\lim_{n \to \infty} \frac{\ln f\left(\frac{1}{n}\right) - \ln f(0)}{\frac{1}{n} - 0} \\
&=\lim_{\frac{1}{n} \to 0^+} \frac{\ln f\left(\frac{1}{n}\right) - \ln f(0)}{\frac{1}{n} - 0}
\end{align*}
$$
旁注：$\because f(x)$为可导函数，$\ln(x)$处处可导，$\therefore \ln f(x)$也为可导。
由归结原则：
$$
\begin{align*}
\lim_{x \to 0^+} \frac{\ln f(x) - \ln f(0)}{x-0} &= \left.(\ln f(x))'\right|_{x=0} \\
&= \left.\frac{f'(x)}{f(x)}\right|_{x=0} \\
&= \frac{f'(0)}{f(0)}
\end{align*}
$$

## 3.7 绝对值也可求导
设函数$f(x)$可导，$|f(x)|$在$x=0$处不可导，则（  ）
A. $f(0)=0$，$f'(0)=0$
B. $f(0)=0$，$f'(0)\neq0$
C. $f(0)\neq0$，$f'(0)=0$
D. $f(0)\neq0$，$f'(0)\neq0$

解：
$|f(x)|=\sqrt{f^2(x)}$，当$f(x)\neq0$时，由复合函数求导法则：
$$
\begin{align*}
(|f(x)|)'&=\left(\sqrt{f^2(x)}\right)' = \frac{1}{2\sqrt{f^2(x)}} \cdot 2f(x)\cdot f'(x) \\
&= \frac{f(x)f'(x)}{\sqrt{f^2(x)}} = \frac{f(x)\cdot f'(x)}{|f(x)|},\quad f(x)\neq0
\end{align*}
$$
$\because |f(x)|$在$x=0$处不可导，且$|f(x)|$在上述导数的分母上
$\therefore$ 当$f(0)=0$时，分母为0，则不可导。
记$g(x)=|f(x)|$，则其在$x=0$处的右导数为：
$$g'_+(0)=\lim_{x \to 0^+} \frac{g(x)-g(0)}{x-0}$$

---

# F 导数_第13页.png

## |f(x)|在x=0处的可导性推导
设$g(x)=|f(x)|$，$f(x)$在$x=0$处可导，推导$g(x)$在$x=0$处的左右导数：
计算右导数$g'_+(0)$：
$$
\begin{align*}
g'_+(0)&=\lim_{x \to 0^+} \frac{|f(x)|-|f(0)|}{x} \\
&=\lim_{x \to 0^+} \frac{|f(x)|}{x} \quad (x\to0^+ \text{ 时 }x>0, f(0)=0) \\
&=\lim_{x \to 0^+} \left|\frac{f(x)}{x}\right| \\
&=\left|\lim_{x \to 0^+} \frac{f(x)}{x}\right| = \left|f'_+(0)\right| = \lim_{x \to 0^+}\left|\frac{f(x)-f(0)}{x-0}\right|
\end{align*}
$$
之前有学过极限性质：
$$\lim_{x \to x_0} f(x)=A \implies \lim_{x \to x_0} |f(x)|=|A|$$
计算左导数$g'_-(0)$：
$$
\begin{align*}
g'_-(0)&=\lim_{x \to 0^-} \frac{g(x)-g(0)}{x-0} \\
&=\lim_{x \to 0^-} \frac{|f(x)|}{x} \quad (x\to0^- \text{ 时 }x<0, f(0)=0) \\
&=-\lim_{x \to 0^-} \frac{|f(x)|}{|x|} \\
&=-\lim_{x \to 0^-} \left|\frac{f(x)-f(0)}{x-0}\right| \\
&=-|f'_-(0)|
\end{align*}
$$
由$f(x)$在$x=0$处可导，故$f'_+(0)=f'_-(0)=f'(0)$，因此$g'_+(0)=|f'(0)|$，$g'_-(0)=-|f'(0)|$：
- 若$f'(0)=0$，则$|f'(0)|=-|f'(0)|$，即$g'_+(0)=g'_-(0)$，此时$|f(x)|$在$x=0$处可导。
- 若题目要求$|f(x)|$在$x=0$处不可导，则当$f'(0)\neq0$时，$|f'(0)|\neq -|f'(0)|$，即$g'_+(0)\neq g'_-(0)$，此时不可导。
### 法2 举例验证
取$f(x)=x$，则：
$$|f(x)|=|x|$$
$$f(0)=0$$
$$f'(0)=1\neq0$$
即该例子满足$f(0)=0$且$f'(0)\neq0$，对应$|f(x)|$在$x=0$处不可导的情形。

---

# F 导数_第14页.png

## 导数的几何意义
函数$y=f(x)$在点$x_0$处的导数值$f'(x_0)$就是曲线$y=f(x)$在点$(x_0,y_0)$处切线的斜率$k$，即
$$k = f'(x_0)$$

于是曲线$y=f(x)$在点$(x_0,y_0)$处的切线方程为
$$y - y_0 = f'(x_0)(x - x_0)$$
（附曲线$y=f(x)$的切线示意图：标注曲线$y=f(x)$、切点$(x_0,y_0)$）

物理上，做曲线运动的物体在某一点处的瞬时速度方向为这一点处的切线方向。

---

### 例
研究①$y=f(x)=|x|$、②$y=f(x)=x^{\frac{1}{3}}$在$x=0$处的切线。

#### ① 对$y=f(x)=|x|$的分析：
从$x=0$出发，取增量$\Delta x$，有
$$\Delta y = f(0+\Delta x) - f(0) = |\Delta x|$$

当$\Delta x>0$时，$\Delta y = \Delta x$，则
$$f'_+(0) = \lim_{\Delta x \to 0^+} \frac{\Delta y}{\Delta x} = 1$$
记为$k_+$。

当$\Delta x<0$时，$\Delta y = -\Delta x$，则
$$f'_-(0) = \lim_{\Delta x \to 0^-} \frac{\Delta y}{\Delta x} = -1$$
记为$k_-$。

$f'_-(0) \neq f'_+(0)$，则$f'(0)$不存在，即$y=f(x)=|x|$在$x=0$处不可导，也就没有切线。
（附$y=|x|$的函数示意图：标注$x$轴、$y$轴，原点处标注尖点）

---

# F 导数_第15页.png

## 无穷导数示例（②）
对于函数$y=f(x)=x^{\frac{1}{3}}$，分析其在$x=0$处的可导性与切线：
计算函数增量与自变量增量的比值：
$$\frac{\Delta y}{\Delta x} = \frac{f(0+\Delta x)-f(0)}{\Delta x} = \frac{(\Delta x)^{\frac{1}{3}}}{\Delta x} = \frac{1}{(\Delta x)^{\frac{2}{3}}}$$
当$\Delta x>0$时，右导数为：
$$f'_+(0) = \lim_{\Delta x \to 0^+} \frac{1}{(\Delta x)^{\frac{2}{3}}} = +\infty$$
当$\Delta x<0$时，左导数为：
$$f'_-(0) = \lim_{\Delta x \to 0^-} \frac{1}{(\Delta x)^{\frac{2}{3}}} = +\infty$$
因此$f'_+(0)=f'_-(0)=+\infty$，$y=f(x)=x^{\frac{1}{3}}$在$x=0$处的切线是竖直的，其斜率（变化率）为无穷大。
这种情况称为**无穷导数**：此时形式上记$f'(0)=\infty$，但$\infty$不是实数，因此函数在该点导数不存在。
结论：函数在该点存在竖直切线，但在此处不可导。
> 注：$f'(x_0)$存在$\overset{\Rightarrow}{\nLeftarrow}$切线存在，即可导一定存在切线，但存在切线不一定可导（如竖直切线对应无穷导数，此时导数不存在）。

## 3.8 切线方程求解
设函数$f(x)$连续，$\lim_{x \to 1} \frac{f(x)-1}{\ln x} = 2$，则曲线$y=f(x)$在点$x=1$处的切线方程为$\underline{\quad\quad}$。

解：
切线方程的点斜式为$y - f(1) = f'(1)(x-1)$，因此需要先求解$f(1)$与$f'(1)$。

1.  求$f(1)$：
    因为$f(x)$连续，故$f(1)=\lim_{x \to 1}f(x)$，对极限变形计算：
    $$
    \begin{align*}
    f(1) &= \lim_{x \to 1} f(x) \\
    &= \lim_{x \to 1} \left[(f(x)-1) + 1\right] \\
    &= \lim_{x \to 1} \left( \frac{f(x)-1}{\ln x} \cdot \ln x \right) + 1 \\
    &= \lim_{x \to 1}\frac{f(x)-1}{\ln x} \cdot \lim_{x \to 1}\ln x + 1 \\
    &= 2 \cdot 0 + 1 \\
    &= 1
    \end{align*}
    $$

2.  求$f'(1)$：
    根据导数的定义：
    $$
    \begin{align*}
    f'(1) &= \lim_{x \to 1} \frac{f(x)-f(1)}{x-1} \\
    &= \lim_{x \to 1} \frac{f(x)-1}{\ln x} \cdot \frac{\ln x}{x-1} \\
    &= \lim_{x \to 1}\frac{f(x)-1}{\ln x} \cdot \lim_{x \to 1}\frac{\ln x}{x-1}
    \end{align*}
    $$
    当$x \to 1$时，由等价无穷小$\ln x \sim x-1$，可得$\lim_{x \to 1}\frac{\ln x}{x-1}=1$，因此：
    $$f'(1) = 2 \cdot 1 = 2$$

3.  确定切线方程：
    将$f(1)=1$、$f'(1)=2$代入点斜式，得：
    $$y-1=2(x-1)$$
    整理为斜截式：
    $$y=2x-1$$

---

# F 导数_第16页.png

## 高阶导数（变化率的变化率）
$x$随$t$的变化率为$v$，
$v$随$t$的变化率为$a$，
$a$随$t$的变化率为…
⋮
函数$f(x)$在点$x_0$处的二阶导数为：
函数$f(x)$在点$x_0$处的一阶导数在点$x_0$处的变化率
$$f''(x_0) = \lim_{\Delta x \to 0} \frac{f'(x_0+\Delta x) - f'(x_0)}{\Delta x}$$
$$= \lim_{x \to x_0} \frac{f'(x) - f'(x_0)}{x - x_0}$$
函数$f(x)$在点$x_0$处的$n$阶导数为（$n>2, n\in \mathbb{Z}$）：
函数$f(x)$在点$x_0$处的$(n-1)$阶导数在点$x_0$处的变化率
$$f^{(n)}(x_0) = \lim_{\Delta x \to 0} \frac{f^{(n-1)}(x_0+\Delta x) - f^{(n-1)}(x_0)}{\Delta x}$$
$$= \lim_{x \to x_0} \frac{f^{(n-1)}(x) - f^{(n-1)}(x_0)}{x - x_0}$$
一阶到$n$阶的导数写法：
$f', f'', f''', f^{(4)}, f^{(5)}, \dots, f^{(n)}$
### 结论
如果$f(x)$在点$x_0$处有二阶导数，
则$f(x)$在点$x_0$的某邻域内有一阶导数，
且$f'(x)$在点$x_0$处连续。
#### 证明：
设$f''(x_0) = \lim_{x \to x_0} \frac{f'(x) - f'(x_0)}{x - x_0} = a$，则
$$f''(x_0) = \frac{\lim\limits_{x \to x_0} \left[f'(x) - f'(x_0)\right]}{\lim\limits_{x \to x_0} (x - x_0)}$$
$$
\begin{aligned}
\lim_{x \to x_0} \left[f'(x) - f'(x_0)\right] &= f''(x_0) \cdot \lim_{x \to x_0} (x - x_0) \\
&= f''(x_0) \cdot 0 \\
&= 0
\end{aligned}
$$

---

# F 导数_第17页.png

$\implies x \to x_0$
$$\lim_{x \to x_0} f'(x) = \lim_{x \to x_0} f'(x_0)$$
$$\lim_{x \to x_0} f'(x) = f'(x_0)$$
$\implies f'(x)$在点$x_0$处连续
与之前的函数连续照应
$f'(x_0) \exists \implies f(x)$在$x_0$附近有定义，且$f(x)$在点$x_0$处连续

$f^{(n)}(x_0) \exists \implies f^{(n-1)}(x)$在点$x_0$的附近有定义
且$f^{(n-1)}(x)$在点$x_0$处连续

## 例3.8
设$f(x)$在$x=x_0$处二阶可导，且$f'(x_0)=0$，$f''(x_0) \neq 0$，证明：
1.  若$f''(x_0)<0$，则$f(x)$在$x_0$处取得极大值
2.  若$f''(x_0)>0$，则$f(x)$在$x_0$处取得极小值

(1)
解：
$$
\begin{aligned}
f''(x_0) &= \lim_{x \to x_0} \frac{f'(x) - f'(x_0)}{x - x_0} < 0 \\
&= \lim_{x \to x_0} \frac{f'(x)}{x - x_0} < 0
\end{aligned}
$$
由局部保号性$\implies$
$$\frac{f'(x)}{x-x_0} < 0$$
$\implies$
- 当$x \in (x_0-\delta, x_0)$，$x < x_0$时，$f'(x) > 0$
- 当$x \in (x_0, x_0+\delta)$，$x > x_0$时，$f'(x) < 0$
（附邻域符号数轴示意图：标注$x_0-\delta$、$x_0$、$x_0+\delta$，标记两侧区间导数符号）
$\implies f(x)$在$x_0$处取极大值

(2) 与(1)同理