# G 微分的概念和计算_第1页.png




## 微分的概念
之前我们用到函数在点$x_0$处的增量：
$$\Delta y = f(x_0+\Delta x) - f(x_0)$$

*$y=f(x)$在点$x=x_0$处的切线示意图，标注了函数增量$\Delta y$、切线对应的线性增量$A\cdot\Delta x$、自变量增量$\Delta x$，横坐标$x_0$、$x_0+\Delta x$，纵坐标$y_0$、$y_0+\Delta y$*

由图看到，若$f(x)$在点$x=x_0$处存在切线，我们将$\Delta y$设为：
$$\Delta y = A\cdot \Delta x + b$$
（$A$是与$\Delta x$无关的常数）

根据导数定义：
$$f'(x_0) = \lim_{\Delta x \to 0} \frac{\Delta y}{\Delta x} = \lim_{\Delta x \to 0} \frac{A\cdot \Delta x}{\Delta x} + \lim_{\Delta x \to 0} \frac{b}{\Delta x}$$

当$b$为$\Delta x$的高阶无穷小时，即$b=o(\Delta x) \ (\Delta x\to0)$时，可得：
$$f'(x_0)=A$$

用形式简单的“线性增量$A\cdot \Delta x$”去代替形式复杂的“真实增量$\Delta y$”，且其误差$\Delta y - A\Delta x$是$o(\Delta x)$。
这就是说，用“简单的量”代替了“复杂的量”，且产生的误差可以忽略不计，这就是可微的含义。

由定义知：若$\Delta y$可以写成
$$\Delta y = A\Delta x + o(\Delta x), \quad (A是与\Delta x无关的常数)$$
则称$f(x)$在点$x=x_0$处可微。

由前面知：若极限
$$\lim_{\Delta x \to 0} \frac{\Delta y}{\Delta x} = f'(x_0)$$
存在，则称$f(x)$在点$x=x_0$处可导。

$$
\because f'(x_0) = \lim_{\Delta x \to 0} \frac{\Delta y}{\Delta x} = \lim_{\Delta x \to 0} \frac{A\cdot \Delta x}{\Delta x} + \lim_{\Delta x \to 0} \frac{o(\Delta x)}{\Delta x} = A
$$

$$
\therefore f(x)在点x_0处可微 \iff f(x)在点x_0处可导
$$
两者是可以互推的：
- 可微必可导
- 可导必可微

若存在与$\Delta x$无关的常数$A$，使得
$$\Delta y = A\cdot \Delta x+o(\Delta x)$$
其中$o(\Delta x)$是$\Delta x \to 0$时比$\Delta x$更高阶的无穷小，则称$f(x)$在点$x_0$处可微，并把增量的主要部分$A\cdot \Delta x$称为**线性主部**，也叫作$f(x)$在点$x_0$处的微分。

微分记为：
$$
\left. dy \right|_{x=x_0} = A\cdot \Delta x = f'(x_0) dx
$$
同时规定自变量的微分：
$$
\left. dx \right|_{x=x_0} = \Delta x
$$

---

# G 微分的概念和计算_第2页.png

## 可微的判别
法1：$f'(x_0)$存在 $\iff f(x)$在点$x_0$处可微
法2：
① 写增量 $\Delta y = f(x_0+\Delta x) - f(x_0)$
② 写线性增量 $A\cdot\Delta x = f'(x_0)\cdot\Delta x$
③ 作极限 $\lim\limits_{\Delta x \to 0} \frac{\Delta y - A\cdot\Delta x}{\Delta x}$
$$\lim_{\Delta x \to 0} \frac{\Delta y - A\cdot\Delta x}{\Delta x} = 0 \iff \Delta y = A\cdot\Delta x + o(\Delta x)$$
若$\lim\limits_{\Delta x \to 0} \frac{\Delta y - A\Delta x}{\Delta x} = 0$，则可微
否则，不可微
## 例3.9
设函数$y=f(x)$在任意点$x$处的增量
$$\Delta y = \frac{y\Delta x}{x+\sqrt{x^2+y^2}} + o(\Delta x),\ 且f(0)=1$$
则$y=f(x)$在点$x=0$处的微分$dy = \underline{dx}$
由题知 $\left.\frac{y\Delta x}{x+\sqrt{x^2+y^2}} = dy\right|_{x=0}$
$\Delta x = \left.dx\right|_{x=0}$
$\Rightarrow \frac{y\,\mathrm{d}x}{x+\sqrt{x^2+y^2}} = \mathrm{d}y,\ \because f(0)=1$
$$\therefore \frac{\mathrm{d}y}{\mathrm{d}x} = \frac{y}{x+\sqrt{x^2+y^2}}$$
代入$x=0, y=f(0)=1$，得$f'(0) = \frac{1}{0+\sqrt{0+1^2}} = 1 = A$
$\because f'(0)=1=A$
$$\therefore \left.\mathrm{d}y\right|_{x=0} = A\cdot \mathrm{d}x = \mathrm{d}x$$

---

# G 微分的概念和计算_第3页.png

## 例3.10
设函数$f(u)$可导，且$y=f(x^2)$，当自变量$x$在$x=-1$处取得增量$\Delta x=-0.1$时，相应的函数增量$\Delta y$的线性主部为$0.1$，则$f'(1)=\underline{\frac{1}{2}}$。

解：由题知
$$\Delta y = A\cdot \Delta x + o(\Delta x)$$
$$A\cdot (-0.1) = 0.1$$
$$\Rightarrow A=-1$$

对复合函数$y=f[g(x)]$（其中$g(x)=x^2$），由链式求导法则：
$$
\begin{align*}
y'&=f'[g(x)]\cdot g'(x)\\
&=f'(x^2)\cdot 2x
\end{align*}
$$
因此函数在$x=-1$处的导数为：
$$y'(-1)=f'(1)\cdot (-2)$$
线性主部的系数$A$即为函数在该点的导数，因此：
$$A = f'(1)\cdot (-2) = -1$$
$$\Rightarrow f'(1)=\frac{1}{2}$$

## 3.9
设$f(x)$在$x=1$处可导，$\Delta f(1)$是$f(x)$在增量为$\Delta x$时的函数值增量，则
$$\lim_{\Delta x \to 0} \frac{\Delta f(1) - df(1)}{\Delta x} = \underline{\qquad}$$

解：$\Delta f(1)$为真实的函数增量，$df(1)$为线性增量。
$\because f(x)$在$x=1$处可导
$\therefore f(x)$在$x=1$处可微
因此$\left[\Delta f(1)-df(1)\right]$为$\Delta x$的高阶无穷小，故
$$\lim_{\Delta x \to 0} \frac{\Delta f(1) - df(1)}{\Delta x} = 0$$

---

# G 微分的概念和计算_第4页.png

# 一元微分学的计算
## 基本求导公式
$$(x^\alpha)'=\alpha x^{\alpha-1} \quad (\alpha\text{为常数})$$

$$(a^x)'=a^x \ln a \quad (a>0,a\neq1)$$

$$(a^x)''=a^x (\ln a)^2,\quad (e^x)'=e^x$$

$$(a^x)^{(n)}=a^x (\ln a)^n,\quad (e^x)^{(n)}=e^x$$

$$(\log_a x)'=\frac{1}{x\ln a} \quad (a>0,a\neq1)$$

$$(\ln x)'=\frac{1}{x}$$

$$(\ln(-x))'=\frac{1}{-x}\cdot(-1)=\frac{1}{x}$$

$$\ln|x|=\begin{cases}
\ln x & x>0 \\
\ln(-x) & x<0
\end{cases}$$

$(\ln|x|)'=\dfrac{1}{x} \ (x\neq0)$，$\ln|x|$求导，视绝对值而不见。

$$(\ln|u(x)|)'=\frac{1}{u(x)}\cdot u'(x) \quad (u(x)\neq0)$$

依旧是，视绝对值而不见。

$$(\sin x)'=\cos x,\quad (\arcsin x)'=\frac{1}{\sqrt{1-x^2}}$$

$$(\cos x)'=-\sin x,\quad (\arccos x)'=-\frac{1}{\sqrt{1-x^2}}$$

$$(\tan x)'=\sec^2 x,\quad (\arctan x)'=\frac{1}{1+x^2}$$

$$(\cot x)'=-\csc^2 x,\quad (\operatorname{arccot} x)'=-\frac{1}{1+x^2}$$

$$(\sec x)'=\sec x \tan x$$

$$(\csc x)'=-\csc x \cot x$$

$$\left[\ln\left(x+\sqrt{x^2+1}\right)\right]'=\frac{1}{\sqrt{x^2+1}}$$

$$\left[\ln\left(x+\sqrt{x^2-1}\right)\right]'=\frac{1}{\sqrt{x^2-1}}$$

---

# G 微分的概念和计算_第5页.png

## 四则运算
和差的导数：
$$[u(x)\pm v(x)]' = u'(x) \pm v'(x)$$
和差的微分：
$$d[u(x)\pm v(x)] = d[u(x)] \pm d[v(x)]$$
积的导数：
$$[u(x)v(x)]' = u'(x)v(x) + u(x)v'(x)$$
积的微分：
$$d[u(x)v(x)] = u(x)d[v(x)] + d[u(x)]v(x)$$
**注：**
$$[u(x)v(x)w(x)]' = u'(x)v(x)w(x) + u(x)v'(x)w(x) + u(x)v(x)w'(x)$$
如果遇到超过三个的式子，一般不要直接求导，而要另谋蹊径。
商的导数：
$$\left[\frac{u(x)}{v(x)}\right]' = \frac{u'(x)v(x) - u(x)v'(x)}{[v(x)]^2}, \quad v(x)\neq 0$$
$\left[\frac{u(x)}{v(x)}\right]'$可看成$\left[u(x)\cdot \frac{1}{v(x)}\right]'$，是一个复合函数。
$$
\begin{align*}
\left(u(x)\cdot \frac{1}{v(x)}\right)' &= u'(x)\cdot \frac{1}{v(x)} + u(x)\cdot \left(-\frac{1}{[v(x)]^2}\cdot v'(x)\right) \\
&= \frac{u'(x)v(x) - u(x)v'(x)}{[v(x)]^2}
\end{align*}
$$
商的微分：
$$d\left[\frac{u(x)}{v(x)}\right] = \frac{v(x)d[u(x)] - u(x)d[v(x)]}{[v(x)]^2}, \quad v(x)\neq 0$$
就是把“$'$”看作“$\frac{d}{dx}$”。
$$[u(x)v(x)]' = u'(x)v(x) + u(x)v'(x)$$
$$\frac{d[u(x)v(x)]}{dx} = \frac{d[u(x)]}{dx}\cdot v(x) + u(x)\cdot \frac{d[v(x)]}{dx}$$
$$\Rightarrow d[u(x)v(x)] = d[u(x)]\cdot v(x) + u(x)\cdot d[v(x)]$$

---

# G 微分的概念和计算_第6页.png

## 例4.1
设$f(x)=\left(\tan \frac{\pi x}{4}-1\right)\left(\tan \frac{\pi x^2}{4}-2\right)\cdots\left(\tan \frac{\pi x^{100}}{4}-100\right)$，则$f'(1)=\underline{\qquad}$

遇到新的情况时，我们要去寻找那些“经典形式”
当遇到新的形式时，我们要向经典形式上去转化
导数的乘积的经典形式就是两项相乘
我们要把这100项相乘，转化为两项相乘
发现，当$x=1$时，只有$\left(\tan \frac{\pi x}{4}-1\right)$为0

令$\left(\tan \frac{\pi x^2}{4}-2\right)\left(\tan \frac{\pi x^3}{4}-3\right)\cdots\left(\tan \frac{\pi x^{100}}{4}-100\right)=g(x)$
则$f(x)=\left(\tan \frac{\pi x}{4}-1\right)\cdot g(x)$
由乘积求导法则：
$$f'(x)=\sec^2 \frac{\pi x}{4}\cdot \frac{\pi}{4}\cdot g(x) + \left(\tan \frac{\pi x}{4}-1\right)\cdot g'(x)$$

代入$x=1$计算：
$$
\begin{aligned}
f'(1)&=\sec^2 \frac{\pi}{4}\cdot \frac{\pi}{4}\cdot g(1)\\
&=2\cdot \frac{\pi}{4}\cdot g(1)\\
&=\frac{\pi}{2}\cdot g(1)\\
&=\frac{\pi}{2}\cdot (-1)\cdot (-2)\cdots (-99)\\
&=-\frac{\pi}{2}\cdot 99!
\end{aligned}
$$

## 复合函数的导数与微分形式不变性
设$u=g(x)$在点$x$处可导（泛指的点），$y=f(u)$在点$u=g(x)$处可导，则复合函数求导法则为：
$$\left\{f[g(x)]\right\}' = f'[g(x)]\cdot g'(x) \quad (\text{求导顺序：}f\to g\to x)$$

导数的微商表示：
$$f'(x)=\frac{\mathrm{d}f(x)}{\mathrm{d}x}$$
$$f'[g(x)]=\frac{\mathrm{d}f[g(x)]}{\mathrm{d}g(x)}$$
$$\left\{f[g(x)]\right\}'=\frac{\mathrm{d}f[g(x)]}{\mathrm{d}x}$$

---

# G 微分的概念和计算_第7页.png

$$\frac{df[g(x)]}{dx} = \frac{df[g(x)]}{dg(x)} \cdot \frac{dg(x)}{dx}$$

$$
\begin{aligned}
df[g(x)] &= f'[g(x)]g'(x)dx \\
&= f'[g(x)]dg(x)
\end{aligned}
$$

## 微分形式的不变性
无论$u$是中间变量还是自变量，均成立：
$$df(u) = f'(u)\cdot du$$

## 多层复合求导扩展
$$\left\{f[v(g(x))]\right\}' = f'[v(g(x))] \cdot v'[g(x)] \cdot g'(x)$$

---

## 例4.2 $\left[\ln(x+\sqrt{x^2+1})\right]'$的证明
设$y=\ln(x+\sqrt{x^2+a^2}) \quad (a\neq 0)$，求$\left.y'\right|_{x=0}$。

复合层次分解：令$u=x+\sqrt{x^2+a^2}$，则$y=\ln u$；$u$由两部分构成：自变量项$x$，以及关于$x$的复合项$\sqrt{x^2+a^2}$。

解：
$$
\begin{aligned}
y' &= \frac{1}{x+\sqrt{x^2+a^2}} \cdot \left(1 + \frac{1}{2\sqrt{x^2+a^2}} \cdot 2x\right) \\
&= \frac{1}{x+\sqrt{x^2+a^2}} \cdot \frac{\sqrt{x^2+a^2} + x}{\sqrt{x^2+a^2}} \\
&= \frac{1}{\sqrt{x^2+a^2}}
\end{aligned}
$$

代入$x=0$计算得：
$$\left.y'\right|_{x=0} = \frac{1}{|a|}$$

---

# G 微分的概念和计算_第8页.png

## 例43
设函数
$$f(x)=\begin{cases}
\ln\sqrt{x}, & x\geq1 \\
2x-1, & x<1
\end{cases}$$
且$y=f[f(x)]$，则$\left.\frac{dy}{dx}\right|_{x=e} = \underline{\qquad}$

解：
$$
\begin{aligned}
\left.\frac{dy}{dx}\right|_{x=e} &= \left.\left\{f[f(x)]\right\}'\right|_{x=e} \\
&= \left.f'[f(x)]\cdot f'(x)\right|_{x=e} \\
&= f'[f(e)]\cdot f'(e)
\end{aligned}
$$
计算各点函数值与导数值：
$f(e)=\frac{1}{2}$
$f'[f(e)] = f'\left(\frac{1}{2}\right) = \left.(2x-1)'\right|_{x=\frac{1}{2}} = 2$
$f'(e) = \left.\left(\frac{1}{2}\ln x\right)'\right|_{x=e} = \left.\frac{1}{2x}\right|_{x=e} = \frac{1}{2e}$

因此：
$$f'[f(e)]\cdot f'(e) = 2\cdot \frac{1}{2e} = \frac{1}{e}$$

---

## 例44
设$y=e^{\sin(\ln x)}$，求$dy$及$\frac{dy}{dx}$

解：
### 法1（用导数）
根据复合函数链式求导法则：
$$\frac{dy}{dx} = \left[e^{\sin(\ln x)}\right]' = e^{\sin(\ln x)} \cdot \cos(\ln x) \cdot \frac{1}{x}$$
由微分与导数的关系$dy=y'dx$得：
$$dy = e^{\sin(\ln x)} \cdot \cos(\ln x) \cdot \frac{1}{x} \, dx$$

### 法2（用微分）
依据一阶微分形式不变性：$df(u)=f'(u)\cdot du$，逐层求微分：
$$d\left[e^{\sin(\ln x)}\right] = e^{\sin(\ln x)} \cdot d\left[\sin(\ln x)\right]$$
$$d\left[\sin(\ln x)\right] = \cos(\ln x) \cdot d(\ln x)$$
$$d(\ln x) = \frac{1}{x} \cdot dx$$
逐层回代得：
$$d\left[e^{\sin(\ln x)}\right] = e^{\sin(\ln x)} \cdot \cos(\ln x) \cdot \frac{1}{x} \, dx$$
即：
$$\frac{dy}{dx} = e^{\sin(\ln x)} \cdot \cos(\ln x) \cdot \frac{1}{x}, \quad dy = e^{\sin(\ln x)} \cdot \cos(\ln x) \cdot \frac{1}{x} \, dx$$

---

# G 微分的概念和计算_第9页.png

## 分段函数的导数
设
$$f(x)=
\begin{cases}
f_1(x), & x\geq x_0 \\
f_2(x), & x<x_0
\end{cases}
$$
其中，$f_1(x),f_2(x)$分别在$x>x_0,x<x_0$时可导，则：
① 在分段点$x_0$处用导数定义求导：
$$f'_+(x_0)=\lim_{x\to x_0^+}\frac{f_1(x)-f(x_0)}{x-x_0}$$
$$f'_-(x_0)=\lim_{x\to x_0^-}\frac{f_2(x)-f(x_0)}{x-x_0}$$
根据$f'_+(x_0)$是否等于$f'_-(x_0)$来判定$f'(x_0)$是否存在。
② 在非分段点，用导数公式求导：
即
$x>x_0$时，$f'(x)=f'_1(x)$
$x<x_0$时，$f'(x)=f'_2(x)$

## 例4.5
设$y=\ln|x|,x\neq0$，求$y'$
解：
$$y=\ln|x|=
\begin{cases}
\ln x, & x>0 \\
\ln(-x), & x<0
\end{cases}
$$
① $x>0 \implies (\ln x)'=\frac{1}{x}$
② $x<0 \implies (\ln(-x))'=\frac{1}{-x}\cdot(-1)=\frac{1}{x}$
$$y'=(\ln|x|)'=\frac{1}{x} \quad (x\neq0)$$

---

# G 微分的概念和计算_第10页.png

## 例4.6
设函数 $y=|x e^{-x}|$，求 $y''$。
带绝对值的话，通过写成分段函数的形式去掉绝对值。
解：
首先去绝对值，将函数写为分段形式：
$$y=|x e^{-x}|=
\begin{cases}
x e^{-x}, & x\geq 0 \\
-x e^{-x}, & x<0
\end{cases}$$
① 判断分段点$x=0$处的导数存在性：
左导数：
$$y'_-(0)=\lim_{x\to 0^-} \frac{y(x)-y(0)}{x-0}=\lim_{x\to 0^-} \frac{-x e^{-x} - 0}{x-0}=-1$$
右导数：
$$y'_+(0)=\lim_{x\to 0^+} \frac{y(x)-y(0)}{x-0}=\lim_{x\to 0^+} \frac{x e^{-x} - 0}{x-0}=1$$
因为 $y'_-(0)\neq y'_+(0)$，所以$y'(0)$不存在，因此$y''(0)$不存在。
② 分别在开区间内计算二阶导数：
当$x>0$时：
$$y'=e^{-x} + x e^{-x}\cdot (-1)=(1-x)e^{-x}$$
$$
\begin{align*}
y''&=-e^{-x} + (1-x)(-e^{-x})\\
&=(x-2)e^{-x}
\end{align*}
$$
当$x<0$时：
$$y'=-e^{-x} + (-x e^{-x})\cdot (-1)=(x-1)e^{-x}$$
$$y''=(2-x)e^{-x}$$
综上，函数的二阶导数为：
$$y''(x)=
\begin{cases}
(x-2)e^{-x}, & x>0 \\
(2-x)e^{-x}, & x<0
\end{cases}$$

---

# G 微分的概念和计算_第11页.png

## 反函数
设函数$y=f(x)$的定义域为$D$，值域为$R$。
如果对于每一个$y\in R$，必存在唯一的$x\in D$使得$y=f(x)$成立，则定义了一个新函数$x=f^{-1}(y)$，这个函数称为函数$y=f(x)$的反函数。
就是自变量与因变量换了一下位置。
自变量改行，当职因变量
因变量改行，当职自变量
即，两者换了一下职位
（映射关系示意图：$x$经映射$f$对应到$y$，$y$经逆映射$f^{-1}$对应回$x$，构成环形映射）
多层可逆映射关系：
$$像_1 \xrightleftharpoons[f^{-1}]{f} 像_2 \xrightleftharpoons[f^{-1}]{f} 像_3$$
只有单调且$f'(x)\neq0$，才能有反函数。
例：给出两组函数交换x、y轴（关于直线$y=x$对称）的示意图：
1.  上组：原函数为先增后减的非单调函数图像，及其交换坐标轴后的对称图像；
2.  下组：原函数为常函数图像，及其交换坐标轴后的对称图像。
一个$x$值对应2个或2个以上$y$值，不符合函数的定义。
先对微分、求导有一个进阶的理解，明确$\frac{d^2 y}{dx^2}$与$\frac{d^2 x}{dy^2}$的含义。

---

# G 微分的概念和计算_第12页.png

（函数与反函数互逆映射示意图：$x$经映射$f$得到$y$，$y$经逆映射$f^{-1}$得到$x$）
$$
\begin{aligned}
x &\to f(\ ) \to y \\
y &\to f^{-1}(\ ) \to x
\end{aligned}
$$

（微分算子与积分算子互逆映射示意图：函数$f$经微分算子$D$得到导函数$f'$，导函数$f'$经逆微分算子得到原函数$f$）
$$
\begin{aligned}
f &\to D(\ ) \to f' \\
f' &\to D^{-1}(\ ) \to f
\end{aligned}
$$

其实$D^{-1}(\ )$就是所谓的积分，满足$D^{-1}(\ )=\int(\ )$。
$D(\ )$是微分算子，其定义为：
$$D(\ ) = \frac{d(\ )}{dx}$$

逐次应用微分算子可得高阶导数：
$$f \to D(\ ) \to f' \to D(\ ) \to f''$$
二阶微分算子$D^2(\ )$是微分算子的复合，将$f$直接映射为二阶导$f''$：
$$f \to D^2(\ ) \to f''$$
二阶微分算子的定义为：
$$D^2(\ ) = D\left[D(\ )\right] = \frac{d^2(\ )}{dx^2}$$

### 另一种理解
设$y=x^3$，
则一阶微分：
$$dy = (3x^2)dx$$
二阶微分为一阶微分的微分：
$$d^2y = d(dy) = (6x dx)dx = 6x dx^2$$

## 反函数的导数
设$y=f(x)$为单调、可导函数，且$f'(x)\neq0$，
则存在反函数$x=f^{-1}(y)$，设$f^{-1}(\ )=\varphi(\ )$，即反函数为$x=\varphi(y)$。
由导数的微商表示：
$$f'(x) = \frac{dy}{dx}, \quad \varphi'(y) = \frac{dx}{dy}$$
根据微商的倒数关系：
$$\because \frac{dx}{dy} = \frac{1}{\frac{dy}{dx}}$$
因此反函数的一阶导数为：
$$\therefore \varphi'(y) = \frac{1}{f'(x)}$$

*易混记号注意：
注意区分一阶导的平方与二阶微分算子，避免记号错误：
$$[D(\ )]^2 = \left( \frac{d(\ )}{dx} \right)^2 = \frac{d(\ )^2}{dx^2} \neq \frac{d^2(\ )}{dx^2}$$
需注意：$dx^2$表示$(dx)^2$（自变量微分的平方），不要误写为$d^2x$（$x$的二阶微分，当$x$为自变量时$d^2x=0$，无意义），也不要与$d(x^2)=2xdx$混淆；同时不要将一阶导的平方与二阶导数混淆。

---

# G 微分的概念和计算_第13页.png

## 心得：从小到大，所学数学的变化
运算对象 $\quad$ 运算符
数 $\xrightarrow{\text{加减、乘除…}}$ 数
数组 $\xrightarrow{f(x)}$ 数组
函数 $\xrightarrow{D(f)}$ 函数

## 反函数的二阶导数
$$\varphi \to D(\ ) \to \varphi' \to D(\ ) \to \varphi''$$
$$\varphi(y) \to D(\ ) \to \frac{dx}{dy} \to D(\ ) \to \frac{d\left(\frac{dx}{dy}\right)}{dy}$$
$$\varphi''(y) = \frac{d\left(\frac{dx}{dy}\right)}{dy} = \frac{d\left(\frac{1}{f'(x)}\right)}{dy} = \frac{d\left(\frac{1}{f'(x)}\right)}{dx} \cdot \frac{dx}{dy}$$
$\frac{d\left(\frac{1}{f'(x)}\right)}{dx}$为以$x$为自变量的复合函数$w(x)=\frac{1}{f'(x)}$的导数，
则
$$w'(x) = -\frac{1}{\left[f'(x)\right]^2} \cdot f''(x)$$
$$\because \frac{dx}{dy} = \frac{1}{f'(x)}$$
$$\therefore \varphi''(y) = -\frac{1}{\left[f'(x)\right]^2} \cdot f''(x) \cdot \frac{1}{f'(x)}$$
$$= -\frac{f''(x)}{\left[f'(x)\right]^3}$$
则
$$\varphi''(y) = -\frac{f''(x)}{\left[f'(x)\right]^3}$$
$$f''(x) = -\frac{\varphi''(y)}{\left[\varphi'(y)\right]^3}$$

---

# G 微分的概念和计算_第14页.png

## 例4.7
当$x>0$时，设$y=f(x)=3x^2+e^x$有反函数$x=\varphi(y)$，则$\varphi''(3+e)=$____
$$\varphi''(y) = -\frac{f''(x)}{\left[f'(x)\right]^3} = -\frac{6+e^x}{(6x+e^x)^3}$$
其中，$y=3+e=3x^2+e^x$，则$x=1$。

当$x=1$时
$$\varphi''(y) = -\frac{6+e}{(6+e)^3} = -\frac{1}{(6+e)^2}$$

## 隐函数
$F(x,y)=0$，当$x$取某区间内的任一值时，总有满足该方程的唯一值$y$存在，则称$F(x,y)=0$在上述区间内确定了一个隐函数$y=y(x)$。

所谓隐函数，就是隐藏了$f()$其对应关系的样子的函数。

eg:
$y=6x$ $\longrightarrow$ $f(x)$为$6x$
写成隐函数：
$$\frac{y}{6} - x = 0$$
即$F(x,y)=0$。

eg:
$y=\sqrt{1-x^2}$ $\longrightarrow$ $f()$为$\sqrt{1-x^2}$
隐化：
$$x^2+y^2-1=0$$

eg:
$y=kx+b$
隐化：
$$ax+by+c=0$$

---

# G 微分的概念和计算_第15页.png

## 隐函数求导方法
设函数$y=f(x)$是由方程$F(x,y)=0$确定的可导函数，求解步骤如下：
1.  将方程$F(x,y)=0$看作$F(x,f(x))=0$，即把$y$视为关于$x$的函数，求导时将$f(x)$作为中间变量。
2.  对方程$F(x,f(x))=0$两边关于自变量$x$求导，得到关于$f'(x)$的方程。
3.  从求导后的方程中解出$f'(x)$。

### 例4
设函数$y=y(x)$由方程$y^3+xy^2+x^2y+6=0$确定，且$y'(1)=0$，求$y''(1)$的值。

解：将$y$看作关于$x$的函数$f(x)$，原方程写为：
$$f(x)^3 + x f(x)^2 + x^2 f(x) + 6 = 0$$
注：$f(x)^3$是复合函数，复合结构为$g[f(x)]$，其中外层函数$g(\cdot)\sim (\cdot)^3$，内层函数为$f(x)$。

对方程两边同时求一阶导数：
$$3f(x)^2 f'(x) + f(x)^2 + 2x f(x)f'(x) + 2x f(x) + x^2 f'(x) = 0$$

当$x=1$时，结合已知条件$f'(1)=0$，代入一阶导方程得：
$$f(1)^2 + 2f(1) = 0$$
解得$f(1)=0$或$f(1)=-2$。

由于将$f(1)=0$代入原方程得左边$=6\neq0$，与方程矛盾，因此舍去$f(1)=0$，得$f(1)=-2$。

对一阶导方程两边再次关于$x$求导（求二阶导）：
$$
\begin{aligned}
6f(x)[f'(x)]^2 + 3f(x)^2 f''(x) + 2f(x)f'(x) + 2\left(f(x)f'(x)+x[f'(x)]^2 +x f(x)f''(x)\right)\\
+ 2f(x) + 2x f'(x) + 2x f'(x) + x^2 f''(x) = 0
\end{aligned}
$$

将$x=1$、$f(1)=-2$、$f'(1)=0$代入二阶导方程：
$$12f''(1) -4f''(1) -4 + f''(1) = 0$$
整理得：
$$9f''(1) = 4$$
解得：
$$f''(1) = \frac{4}{9}$$

---

# G 微分的概念和计算_第16页.png

## 参数方程
(就是含有参数$t$的方程)

$y=f(x)$可以写成参数形式：
$$\begin{cases} x = f_1(t) \\ y = f_2(t) \end{cases}$$
$y$与$x$之间的对应关系由参数$t$联系。

eg：
$y=\frac{x^2}{4}$写成参数方程：
$$\begin{cases} x=2t \\ y=t^2 \end{cases}$$

## 由参数方程所确定的函数的导函数
设函数$y=y(x)$由参数方程$\begin{cases} x = g(t) \\ y = w(t) \end{cases}$确定，
其中，$t$是参数，且$g(t),w(t)$均可导，$g'(t)\neq0$，则：
$$y'=\frac{dy}{dx}=\frac{\frac{dy}{dt}}{\frac{dx}{dt}}=\frac{w'(t)}{g'(t)}$$

## 由参数方程确定的函数的二阶导数
设函数$y=y(x)$由参数方程$\begin{cases} x = g(t) \\ y = w(t) \end{cases}$确定，
其中，$t$是参数，且$g(t),w(t)$均二阶可导，$g'(t)\neq0$，则：
$$y''(x)=\frac{d^2 y}{dx^2} = \frac{d\left(\frac{dy}{dx}\right)}{dx} = \frac{\frac{d\left( \frac{w'(t)}{g'(t)} \right)}{dt}}{\frac{dx}{dt}}$$
代入$\frac{dx}{dt}=g'(t)$，得：
$$y''(x) = \frac{\frac{d\left( \frac{w'(t)}{g'(t)} \right)}{dt}}{g'(t)}$$
其中$\frac{d\left( \frac{w'(t)}{g'(t)} \right)}{dt}$表示对$\frac{w'(t)}{g'(t)}$关于$t$求导（即微分算子$D\left( \frac{w'(t)}{g'(t)} \right)$），由商的求导法则：
$$\left( \frac{w'(t)}{g'(t)} \right)' = \frac{w''(t)g'(t) - w'(t)g''(t)}{\left[g'(t)\right]^2}$$
代入后得到二阶导数公式：
$$y''(x) = \frac{w''(t)g'(t) - w'(t)g''(t)}{\left[g'(t)\right]^3}$$

此式也不用求导化简，将$\frac{dy}{dx}$即$\frac{w'(t)}{g'(t)}$看成关于$t$的函数。

---

# G 微分的概念和计算_第17页.png

设$\frac{w'(t)}{g'(t)}$为$\varphi(t)$，则
$$y''(x)=\frac{d^2 y}{dx^2} = \frac{d\left(\frac{dy}{dx}\right)}{dx} = \frac{\frac{d\varphi(t)}{dt}}{\frac{dx}{dt}} = \frac{\varphi'(t)}{g'(t)}$$
其中$\varphi'(t)=\left( \frac{w'(t)}{g'(t)} \right)'$

## 例4.9
设$y=y(x)$由参数方程$\begin{cases} x=\sin t \\ y=t\sin t + \cos t \end{cases}$确定，则$\left. \frac{d^2 y}{dx^2} \right|_{t=\frac{\pi}{4}} = \underline{\qquad\quad}.$

解：
求一阶导：
$$\frac{dy}{dx} = \frac{\frac{dy}{dt}}{\frac{dx}{dt}} = \frac{\sin t + t\cos t - \sin t}{\cos t} = t$$
求二阶导：
$$\frac{d^2 y}{dx^2} = \frac{d\left(\frac{dy}{dx}\right)}{dx} = \frac{\frac{dt}{dt}}{\frac{dx}{dt}} = \frac{1}{\cos t}$$
代入$t=\frac{\pi}{4}$得：
$$\Rightarrow \left. \frac{d^2 y}{dx^2} \right|_{t=\frac{\pi}{4}} = \sqrt{2}$$

## 对数求导法（应对多项式求导）
对于多项式相乘、相除、乘方的式子（为了求导的方便）：
一般先对等式两边同时取对数（前提是两边式子都$>0$），再求导。

设$y=f(x)$，$f(x)>0$，则：
等式两边取对数，即：
$$\ln y = \ln f(x)$$

对数可以实现以下运算转化：
$$\begin{cases}
乘 \to 加 \\
除 \to 减 \\
幂次 \to 倍数
\end{cases}$$

两边对自变量$x$求导：
注：求导时，将$y$看成关于$x$的函数$f(x)$，会涉及复合函数，即：
$$[\ln f(x)]' = \frac{1}{f(x)} \cdot f'(x)$$

---

# G 微分的概念和计算_第18页.png

## 例4.1
设函数$y=y(x)$由方程$x e^{f(y)} = e^y \ln2$确定，其中$f$具有二阶导数，且$f'\neq 1$，则$\frac{d^2 y}{dx^2} = \underline{\quad\quad}$

解：
在方程$x e^{f(y)} = e^y \ln2$中，
由$e^y>0$，$\ln2>0$ $\Rightarrow$ $x e^{f(y)}>0$，因此$x>0$。

对等式两边同时取对数：
$$\ln x + f(y)\ln e = y\ln e + \ln(\ln2)$$
化简得：
$$\ln x + f(y) = y + \ln(\ln2)$$

求导时按隐函数求导处理，将$y$看作关于$x$的函数（笔记中临时记$y=f(x)$），因此方程可写为：
$$\ln x + f[f(x)] = f(x) + \ln(\ln2)$$

对$x$求一阶导数：
① $$\frac{1}{x} + f'[f(x)]\cdot f'(x) = f'(x)$$

对$x$求二阶导数：
② $$-\frac{1}{x^2} + f''[f(x)]\cdot [f'(x)]^2 + f'[f(x)]f''(x) = f''(x)$$

由①式求解一阶导数：
$$f'(x) = \frac{-\frac{1}{x}}{f'[f(x)] - 1}$$

计算一阶导数的平方：
$$[f'(x)]^2 = \frac{\frac{1}{x^2}}{\left(f'[f(x)] - 1\right)^2}$$

由②式整理求解二阶导数，并将$[f'(x)]^2$代入化简：
$$
\begin{align*}
\frac{d^2 y}{dx^2}=f''(x) &= \frac{\frac{1}{x^2} - f''[f(x)]\cdot [f'(x)]^2}{f'[f(x)] - 1} \\
&= \frac{\left(f'[f(x)] - 1\right)^2 - f''[f(x)]}{x^2\left(f'[f(x)] - 1\right)^3}
\end{align*}
$$

## 幂指函数求导法
对于幂指函数$f(x)^{g(x)}$（满足$f(x)>0$，且$f(x)\neq1$），利用指数恒等式转换：
$$f(x)^{g(x)} = e^{g(x)\ln[f(x)]}$$

求导推导如下：
设$w(x) = g(x)\ln[f(x)]$，则
$$
\begin{align*}
\left[f(x)^{g(x)}\right]' &= \left[e^{g(x)\ln[f(x)]}\right]' \\
&= \left[e^{w(x)}\right]' \\
&= e^{w(x)} \cdot w'(x)
\end{align*}
$$

其中由乘积求导法则与复合函数求导法则：
$$w'(x) = g'(x)\cdot \ln[f(x)] + g(x)\cdot \frac{1}{f(x)} \cdot f'(x)$$

---

# G 微分的概念和计算_第19页.png

即
$$\left[f(x)^{g(x)}\right]' = f(x)^{g(x)}\left[g'(x)\ln f(x) + g(x)\cdot\frac{f'(x)}{f(x)}\right]$$

**例4.12**
求函数$y=x^x\ (x>0)$的导数。

解：
$x^x = e^{x\ln x}$
$$
\begin{align*}
y' &= \left(e^{x\ln x}\right)' \\
&= x^x\left(\ln x + 1\right) \quad (x>0)
\end{align*}
$$

**例4.13**
求函数$y=x^{\frac{1}{x}}\ (x>0)$的导数。

解：
$x^{\frac{1}{x}} = e^{\frac{1}{x}\ln x}$
$$
\begin{align*}
y' &= \left(e^{\frac{1}{x}\ln x}\right)' \\
&= x^{\frac{1}{x}}\left(-\frac{1}{x^2}\ln x + \frac{1}{x^2}\right) \\
&= x^{\frac{1}{x}} \cdot \frac{1-\ln x}{x^2} \quad (x>0)
\end{align*}
$$

## 高阶导数（求导的阶数≥2，一般为n阶）
求高阶导数主要有三种方法：
1.  **归纳法**：逐次求导，探索规律，得出通式。

常用的高阶导数（$n\in \mathbb{N}_+$）：
$$(e^{ax+b})^{(n)} = a^n e^{ax+b}$$
$$\left[\sin(ax+b)\right]^{(n)} = a^n \sin\left(ax+b + \frac{n\pi}{2}\right)$$
$$\left[\cos(ax+b)\right]^{(n)} = a^n \cos\left(ax+b + \frac{n\pi}{2}\right)$$
$$\left[\ln(ax+b)\right]^{(n)} = (-1)^{n-1}a^n \frac{(n-1)!}{(ax+b)^n}$$
$$\left(\frac{1}{ax+b}\right)^{(n)} = (-1)^n a^n \frac{n!}{(ax+b)^{n+1}}$$

遇到不常见的，向常见的去转化。

---

# G 微分的概念和计算_第20页.png

### 例4.15
设$y=\frac{1-x}{1+x}$，则$y^{(n)}(0) = \underline{\quad\quad}$
解：
$$y = \frac{1-x}{1+x} = \frac{-1-x+2}{1+x} = -1 + \frac{2}{1+x}$$
$$y^{(n)} = 2(-1)^n \frac{n!}{(1+x)^{n+1}}$$
$$y^{(n)}(0) = 2\cdot (-1)^n \cdot n!$$

### 例4.16
已知函数$f(x)$具有任意阶导数，且$f'(x) = [f(x)]^2$，其中$n\in \mathbb{N}_+$，则$f^{(n)}(x) = \underline{\quad\quad}$
解：
$$f'(x) = [f(x)]^2$$
$$f''(x) = 2f(x)\cdot f'(x) = 2[f(x)]^3$$
$$f'''(x) = 2\cdot 3 [f(x)]^2 \cdot f'(x) = 2\cdot 3\cdot [f(x)]^4$$
$$\Rightarrow f^{(n)}(x) = n!\, [f(x)]^{n+1}$$

## 莱布尼茨公式
设$u=u(x), v=v(x)$均$n$阶可导，则
$$(u\pm v)^{(n)} = u^{(n)} \pm v^{(n)}$$
$$
\begin{aligned}
(uv)^{(n)} &= \mathrm{C}_n^0 u^{(n)}v + \mathrm{C}_n^1 u^{(n-1)}v' + \mathrm{C}_n^2 u^{(n-2)}v'' + \dots \\
&\quad + \mathrm{C}_n^k u^{(n-k)}v^{(k)} + \dots + \mathrm{C}_n^{n-1} u'v^{(n-1)} + \mathrm{C}_n^n u v^{(n)} \\
&= \sum_{k=0}^n \mathrm{C}_n^k u^{(n-k)} v^{(k)}
\end{aligned}
$$
有时要莱布尼茨公式与归纳法中的通式结合着用。

### 补充：排列数与组合数
排列数：$\mathrm{A}_n^m = \underbrace{n(n-1)(n-2)\cdots(n-m+1)}_{m项相乘}$，例：$\mathrm{A}_6^3 = 6\times5\times4$
组合数：$\mathrm{C}_n^m = \frac{\mathrm{A}_n^m}{\mathrm{A}_m^m} = \frac{n(n-1)(n-2)\cdots(n-m+1)}{m!}$，例：$\mathrm{C}_6^3 = \frac{6\times5\times4}{3\times2\times1}$
规定$\mathrm{C}_n^0=1$：“不选择，也是一种选择”
性质：$\mathrm{C}_n^m = \mathrm{C}_n^{n-m}$
10个人送出6个人去比赛等价于10个人送出4个人不去比赛。

---

# G 微分的概念和计算_第21页.png

### 例4.17
设$f(x)=xe^x$，则$f^{(n)}(x)=\underline{\qquad}$
解：
$$
\begin{align*}
f^{(n)}(x)&=(xe^x)^{(n)}\\
&=\mathrm{C}_n^0 (e^x)^{(n)}x + \mathrm{C}_n^1 (e^x)^{(n-1)}x'\\
&=xe^x + ne^x\\
&=(n+x)e^x
\end{align*}
$$

## 泰勒展开式
任何一个任意阶可导的函数都可以写成：
在$x=x_0$点展开：
$$y=f(x)=\sum_{n=0}^{\infty} \frac{f^{(n)}(x_0)}{n!}(x-x_0)^n$$
在$x=0$处展开：
$$y=f(x)=\sum_{n=0}^{\infty} \frac{f^{(n)}(0)}{n!}x^n$$
我们的先辈们已经帮我们求出了一些常见的任意阶可导函数在$x=0$处的泰勒展开式，这些公式最好记住：
$$e^x=\sum_{n=0}^{\infty} \frac{x^n}{n!}=1+x+\frac{x^2}{2!}+\dots+\frac{x^n}{n!}+\dots,\quad -\infty<x<+\infty$$
$$\frac{1}{1+x}=\sum_{n=0}^{\infty} (-1)^n x^n=1-x+x^2-x^3+\dots+(-1)^n x^n+\dots,\quad -1<x<1$$
$$\frac{1}{1-x}=\sum_{n=0}^{\infty} x^n=1+x+x^2+x^3+\dots+x^n+\dots,\quad -1<x<1$$
$$\ln(1+x)=\sum_{n=1}^{\infty} (-1)^{n-1}\frac{x^n}{n}=x-\frac{x^2}{2}+\frac{x^3}{3}-\dots+(-1)^{n-1}\frac{x^n}{n}+\dots,\quad -1<x\leq1$$
$$
\begin{align*}
\sin x&=\sum_{n=0}^{\infty} (-1)^n \frac{x^{2n+1}}{(2n+1)!},\quad -\infty<x<+\infty\\
&=x-\frac{x^3}{3!}+\frac{x^5}{5!}-\frac{x^7}{7!}+\dots+(-1)^n \frac{x^{2n+1}}{(2n+1)!}+\dots
\end{align*}
$$
$$
\begin{align*}
\cos x&=\sum_{n=0}^{\infty} (-1)^n \frac{x^{2n}}{(2n)!},\quad -\infty<x<+\infty\\
&=1-\frac{x^2}{2!}+\frac{x^4}{4!}-\frac{x^6}{6!}+\dots+(-1)^n \frac{x^{2n}}{(2n)!}+\dots
\end{align*}
$$
$$(1+x)^\alpha=1+\alpha x+\frac{\alpha(\alpha-1)}{2!}x^2+\dots$$
$\tan x = x+\frac{1}{3}x^3+\dots$，$\arctan x = x-\frac{1}{3}x^3+\dots$
$\arcsin x = x+\frac{1}{6}x^3+\dots$

---

# G 微分的概念和计算_第22页.png

## 函数泰勒展开式的唯一性
无论$f(x)$在哪个点处展开，其泰勒展开式具有唯一性。
我们可以比较$f(x)$在$x=x_0$处展开和在$x=0$处展开的系数，来获得$f^{(n)}(x_0)$或$f^{(n)}(0)$。
即：背会展开式，由于展开式中包含了$f^{(n)}(x_0)$，所以可由展开式得出$f^{(n)}(x_0)$。

### 例4.18
设$f(x)=x^2\ln(1-x)$，则当$n\geq3$时，$f^{(n)}(0)=$____
解：
① 写出$f(x)$的麦克劳林展开式：
$$f(x)=\sum_{n=0}^{\infty} \frac{f^{(n)}(0)}{n!}x^n$$

② 利用已知的$\ln(1+u)$的幂级数展开式推导：
$$
\begin{align*}
f(x)&=x^2\cdot \ln\left[1+(-x)\right]\\
&=x^2\cdot \sum_{n=1}^{\infty} (-1)^{n-1}\cdot \frac{(-x)^n}{n}\\
&=x^2\cdot \sum_{n=1}^{\infty} \frac{(-1)^{n-1}\cdot (-1)^n x^n}{n}\\
&=x^2\sum_{n=1}^{\infty} (-1)^{2n-1}\cdot \frac{x^n}{n}\\
&=x^2\sum_{n=1}^{\infty} \frac{-x^n}{n}\\
&=-\sum_{n=1}^{\infty} \frac{x^{n+2}}{n}\\
&=-\sum_{n=0}^{\infty} \frac{x^{n+3}}{n+1}
\end{align*}
$$
对级数做指标换元（手写中记“设$n=n-3$时”为哑元替换表述，令新求和指标为原指标减3以对齐$x$的幂次），可得$\frac{x^{n+3}}{n+1} = \frac{1}{n-2}x^n$，换元后级数为：
$$f(x)=-\sum_{n=3}^{\infty} \frac{x^n}{n-2}$$

③ 根据泰勒展开式的唯一性，对比两边$x^n$（$n\geq3$）的系数：
$$\frac{f^{(n)}(0)}{n!} = -\frac{1}{n-2}$$
因此：
$$f^{(n)}(0) = -\frac{n!}{n-2}$$

---

#### 加强理解
将$\ln(1-x)$直接展开为幂级数：
$$f(x)=x^2\ln(1-x)=x^2\left(-x-\frac{x^2}{2}-\dots-\frac{x^{n-2}}{n-2}-\dots\right)$$
而$f(x)$的麦克劳林展开式形式为：
$$f(x)=f(0)+f'(0)x+\frac{f''(0)}{2!}x^2+\dots+\frac{f^{(n)}(0)}{n!}x^n+\dots$$
根据展开式的唯一性，对比等式两边$x^n$的系数，可得：
$$-\frac{1}{n-2} = \frac{f^{(n)}(0)}{n!} \implies f^{(n)}(0) = -\frac{n!}{n-2}$$

---

# G 微分的概念和计算_第23页.png

## 例419
设$f(x)=x^2 2^x$，则当$n\geq1$时，$f^{(n)}(0)=\underline{\qquad}$

## 法1 莱布尼茨公式
解：
$$f^{(n)}(x) = \left(x^2 2^x\right)^{(n)}$$
由莱布尼茨高阶求导公式展开：
$$= (2^x)^{(n)} x^2 + \mathrm{C}_n^1 (2^x)^{(n-1)} \cdot 2x + \mathrm{C}_n^2 (2^x)^{(n-2)} \cdot 2$$
代入$x=0$，前两项含因子$x$，取值为0，因此：
$$
\begin{aligned}
f^{(n)}(0) &= \left. \mathrm{C}_n^2 \cdot (2^x)^{(n-2)} \cdot 2 \right|_{x=0} \\
&= \left. \frac{n(n-1)}{2} \cdot 2^x \cdot (\ln 2)^{n-2} \cdot 2 \right|_{x=0} \\
&= n(n-1) (\ln 2)^{n-2}
\end{aligned}
$$

## 法2 泰勒公式
1.  将$f(x)$展开为麦克劳林级数：
$$
\begin{aligned}
f(x) &= x^2 2^x \\
&= x^2 e^{x\ln 2} \\
&= x^2 \sum_{n=0}^{\infty} \frac{(x\ln 2)^n}{n!} \\
&= \sum_{n=0}^{\infty} \frac{(\ln 2)^n}{n!} x^{n+2}
\end{aligned}
$$
2.  函数麦克劳林展开的标准形式为：
$$f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(0)}{n!} x^n$$
对上述级数做指标平移，令$k = n+2$（即$n=k-2$），对齐$x$的幂次：
$$f(x) = \sum_{k=2}^{\infty} \frac{(\ln 2)^{k-2}}{(k-2)!} x^k$$
将求和指标换回$n$，得：
$$f(x) = \sum_{n=2}^{\infty} \frac{(\ln 2)^{n-2}}{(n-2)!} x^n$$
3.  对比两个展开式中$x^n$项的系数：
$$\frac{f^{(n)}(0)}{n!} = \frac{(\ln 2)^{n-2}}{(n-2)!}$$
整理得：
$$f^{(n)}(0) = n(n-1) (\ln 2)^{n-2}$$