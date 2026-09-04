---

# N 多元函数微分_第1页.png

## 多元函数的偏导数
## 邻域“相邻的区域”
设$P_0(x_0,y_0)$是$xOy$平面上的一个点，$\delta>0$，与点$P_0(x_0,y_0)$的距离小于$\delta$的点$P(x,y)$的全体称为点$P_0$的$\delta$邻域，记为$U(P_0,\delta)$：
$$
U(P_0,\delta) = \left\{ P \mid |PP_0| < \delta \right\}
$$
用坐标形式可表示为：
$$
U(P_0,\delta) = \left\{ (x,y) \mid \sqrt{(x-x_0)^2 + (y-y_0)^2} < \delta \right\}
$$
（示意图：平面直角坐标系下两点间距离示意图，标注了点$P_0(x_0,y_0)$、$P(x,y)$，坐标差$x-x_0$、$y-y_0$，以及两点间距离$\sqrt{(x-x_0)^2+(y-y_0)^2}$）

## 去心$\delta$邻域
点$P_0$的去心$\delta$邻域记为：
$$
\mathring{U}(P_0,\delta) = \left\{ P \mid 0 < |PP_0| < \delta \right\}
$$
特别地，若无需强调邻域半径$\delta$，可用$U(P_0)$表示$P_0$的某个邻域，去心邻域可记为$\mathring{U}(P_0)$。

## 邻域概念对比
- 一元函数中$x=x_0$的邻域：是数轴上以$x_0$为中心、向两边延伸$\delta$长度的开区域。
（示意图：数轴上的一元函数邻域示意图，标注了点$x_0-\delta$、$x_0$、$x_0+\delta$）
一元函数的去心邻域为邻域内抠去中心点$x_0$后的区域。

---

# N 多元函数微分_第2页.png

## 二元函数中点$P_0(x_0,y_0)$的邻域
为平面上的，以$P_0(x_0,y_0)$为圆心，
以$\delta$为半径所画圆的区域。
去心邻域为邻域内抠去点$P_0$后的区域。

## 二、极限
设函数$f(x,y)$在区域$D$上有定义，
$P_0\in D$或为区域$D$边界上的一点。
如果对于任意给定的$\varepsilon>0$，总有$\delta>0$，
当点$P(x,y)\in D$
且$0<|PP_0|=\sqrt{(x-x_0)^2+(y-y_0)^2}<\delta$时，
恒有$|f(x,y)-A|<\varepsilon$，
则称常数$A$为$(x,y)\to(x_0,y_0)$时
$f(x,y)$的极限。

记作：
$$\lim_{(x,y)\to(x_0,y_0)} f(x,y) = A$$
或
$$\lim_{\substack{x\to x_0\\y\to y_0}} f(x,y) = A$$

☆ compare
## 对比：一元函数极限
$$\lim_{x\to x_0} f(x) = A \quad \begin{cases}
f(x) = A + \alpha \\
当x\to x_0时 \\
\alpha 为无穷小量
\end{cases}$$
$$\exists\ \delta>0,\ 0<|x-x_0|<\delta \quad \vdots \quad x\to x_0$$
$$\forall\ \varepsilon>0,\ |f(x)-A|<\varepsilon \quad \vdots \quad f(x)\to A$$
$x\to x_0$的路径为两种：$\begin{cases} x\to x_0^+ \\ x\to x_0^- \end{cases}$

---

# N 多元函数微分_第3页.png

若$\lim\limits_{x \to x_0^+} f(x) \neq \lim\limits_{x \to x_0^-} f(x)$
则$\lim\limits_{x \to x_0} f(x)$不存在

## 二元函数极限，又名“二重极限”
$$\lim_{(x,y) \to (x_0,y_0)} f(x,y) = A \iff
\begin{cases}
f(x,y) = A + \alpha \\
\text{当}(x,y) \to (x_0,y_0)\text{时} \\
\alpha\text{为无穷小量}
\end{cases}$$

$\forall \varepsilon>0,\ \exists \delta>0$，当$0<|PP_0|=\sqrt{(x-x_0)^2+(y-y_0)^2} < \delta$时，有$|f(x,y)-A| < \varepsilon$

$(x,y)\to(x_0,y_0)$的路径有无穷种
例：
（平面直角坐标系示意图：展示沿多条不同曲线趋近于点$(x_0,y_0)$的路径）

当有2种及以上$(x,y)\to(x_0,y_0)$的路径，使$\lim\limits_{(x,y)\to(x_0,y_0)} f(x,y)$的值不相等，则$\lim\limits_{(x,y)\to(x_0,y_0)} f(x,y)$不存在。

## $(x,y)\to(x_0,y_0)$的路径
（平面直角坐标系示意图：绘制过点$(x_0,y_0)$的曲线$y=f(x)$，标注坐标轴、原点与点$(x_0,y_0)$）

不同的路径
指$y=f(x)$的不同关系式
$x=g(y)$的不同关系式

例：$(x,y)\to(0,0)$时
$y=x^3,\ x=2y$都过$(0,0)$点
$\therefore$
$x\to0,\ f(x)=x^3\to0$
$y\to0,\ g(y)=2y\to0$
为$(x,y)\to(0,0)$的两个不同路径

---

# N 多元函数微分_第4页.png

若
$$\lim_{\substack{x\to 0\\y=x^3}} f(x,x^3) \neq \lim_{\substack{y\to 0\\x=2y}} f(2y,y)$$
则
$$\lim_{\substack{x\to 0\\y\to 0}} f(x,y) \text{不存在}$$

## 注
除洛必达法则与单调有界准则外，可照搬一元函数求极限的方法来求二重极限。
e.g. 唯一性，局部有界性，局部保号性，脱帽法，运算规则，夹逼准则，等价替换等。
e.g. 当$(x,y)\to(0,0)$时，
$$e^{x^2+y^2}-1 \sim x^2+y^2$$

## 例13.1
判断
$$I_1 = \lim_{\substack{x\to 0\\y\to 0}} \frac{|xy|}{\sqrt{x^2+y^2}}, \quad I_2 = \lim_{\substack{x\to 0\\y\to 0}} \frac{x|y|}{x^2+y^2}$$
的存在与否。

### 分析
看到$|xy| \leq x^2+y^2$想到基本不等式
$$|ab| \leq \frac{a^2+b^2}{2}$$
看到可用不等式，可想到夹逼准则。

### 解 「先看$I_1$」
$$\because |ab| \leq \frac{a^2+b^2}{2}$$
$$\therefore |xy| \leq \frac{x^2+y^2}{2}$$

---

# N 多元函数微分_第5页.png

## 利用夹逼准则判断二元函数极限存在
$$\frac{|xy|}{\sqrt{x^2+y^2}} \leqslant \frac{\frac{x^2+y^2}{2}}{\sqrt{x^2+y^2}} = \frac{\sqrt{x^2+y^2}}{2}$$
$\because (x,y)\to(0,0)$时，
$$\frac{\sqrt{x^2+y^2}}{2} \to 0$$
且 $0\leqslant \frac{|xy|}{\sqrt{x^2+y^2}}$，考虑用夹逼准则。
$\therefore$ 当$(x,y)\to(0,0)$时：
$$0 \leqslant \frac{|xy|}{\sqrt{x^2+y^2}} \leqslant \frac{\frac{x^2+y^2}{2}}{\sqrt{x^2+y^2}} = \frac{\sqrt{x^2+y^2}}{2}$$
不等式两端在$(x,y)\to(0,0)$时极限均为$0$，由夹逼准则可得：
$\Rightarrow I_1$是存在的，且趋向于$0$。

## 利用路径法判断二元函数极限不存在
这类题，我们做题做多了，其是否存在，我们能感觉出来。
$I_2$上面为一次，下面为二次，大概率不存在，我们可以找不同的路径来找出其不存在的证据。
可以找$x\to0^+,x\to0^-$，$y=x$这两条路径。
（对应示意图：平面直角坐标系，标注原点$(0,0)$、$x$轴、$y$轴，绘制过原点的直线路径$y=x$）
则
$$I_2 = \lim\limits_{\substack{x\to0 \\ y=x}} \frac{x|x|}{2x^2} = \lim\limits_{\substack{x\to0 \\ y=x}} \frac{|x|}{2x}$$
发现有尖点。
$$\lim\limits_{\substack{x\to0^+ \\ y=x}} \frac{|x|}{2x} = \frac{1}{2} \neq \lim\limits_{\substack{x\to0^- \\ y=x}} \frac{|x|}{2x} = -\frac{1}{2}$$
$\Rightarrow I_2$不存在。

---

# N 多元函数微分_第6页.png

## 三、连续
点$x_1$与点$x_2$连续：$|x_1-x_2|\to0$。

若
$$\lim_{\substack{x\to x_0\\y\to y_0}} f(x,y) = f(x_0,y_0)$$
则称函数$f(x,y)$在点$(x_0,y_0)$处连续。

如果$f(x,y)$在区域$D$上每一点处都连续，则称$f(x,y)$在区域$D$上连续。

☆ compare
### 一元函数的连续
一元函数在点$x_0$处连续的充要条件为：
$$\lim_{x\to x_0} f(x) = f(x_0) = \lim_{x\to x_0^+} f(x) = \lim_{x\to x_0^-} f(x)$$
- 自变量角度直观：$x_0$点处连续，即$x_0$与其两边的$x_0^+$、$x_0^-$充分靠近，配自变量数轴示意图，数轴上标注$x_0^-$、$x_0$、$x_0^+$，箭头沿轴向右。
- 函数值角度直观：$f(x_0)$点处连续，即$f(x_0)$与其两边的$f(x_0^-)$、$f(x_0^+)$充分靠近，配函数值数轴示意图，数轴上标注$f(x_0^-)$、$f(x_0)$、$f(x_0^+)$，箭头沿轴向右。

若满足以下任意一条，则$x_0$为间断点：
① $\lim\limits_{x\to x_0^+} f(x) \neq f(x_0)$
② $\lim\limits_{x\to x_0^-} f(x) \neq f(x_0)$
③ $\lim\limits_{x\to x_0^+} f(x) \neq \lim\limits_{x\to x_0^-} f(x)$
④ $\lim\limits_{x\to x_0} f(x)$不存在

### 二元函数连续
二元函数在点$P_0(x_0,y_0)$处连续的定义为：
$$\lim_{(x,y)\to(x_0,y_0)} f(x,y) = f(x_0,y_0)$$
$P_0(x_0,y_0)$点处连续，即$P_0$与其周围的点$P(x,y)$充分靠近，配平面直角坐标系趋近示意图，标注原点$O$、$x$轴、$y$轴，展示平面上点趋近于$P_0(x_0,y_0)$。

---

# N 多元函数微分_第7页.png

（二元函数$z=f(x,y)$在点$(x_0,y_0)$处连续的曲面示意图，标注坐标轴$x,y,f(x,y)$与点$(x_0,y_0,f(x_0,y_0))$，展示连续点处曲面的形态）

$f(x_0,y_0)$这一点处连续，即$f(x_0,y_0)$与其周围的$f(x,y)$充分靠近。

若存在任意一种$(x,y)\to(x_0,y_0)$的路径，使
$$\lim_{\substack{x\to x_0\\y\to y_0}} f(x,y) \neq f(x_0,y_0) \text{ 或极限不存在}$$
则为间断点。

注：考纲中未要求讨论间断点。

## 例13.2
设
$$
f(x,y)=
\begin{cases}
\dfrac{\sqrt[3]{1-(x^2+y^2)} - 1}{e^{x^2+y^2} - 1}, & x^2+y^2 \neq 0 \\
a, & x^2+y^2 = 0
\end{cases}
$$
为连续函数，则$a=\underline{\qquad}$。

## 分析
$\because f(x,y)$为连续函数
$\therefore f(x,y)$在$(0,0)$处连续
$\because$ 当$x=0,y=0$时，
$$x^2+y^2=0$$
$\therefore$ 当$\substack{x\to0\\y\to0}$时，$f(x,y)\to a$

## 解
利用等价无穷小：当$x\to0$时，$e^x -1 \sim x$，$(1+x)^\alpha -1 \sim \alpha x$。
$$
\begin{align*}
\lim_{\substack{x\to0\\y\to0}} \frac{\sqrt[3]{1-(x^2+y^2)} - 1}{e^{x^2+y^2} - 1}
&= \lim_{\substack{x\to0\\y\to0}} \frac{\dfrac{1}{3}\left[-(x^2+y^2)\right]}{x^2+y^2} \\
&= -\frac{1}{3}
\end{align*}
$$
故$a=-\dfrac{1}{3}$。

---

# N 多元函数微分_第8页.png

## 四、偏导数
$\partial$ 读法：“偏”，“round”
☆ Compare.
● 一元函数的导数
一元函数只有$x$轴方向上的变化率。
● 二元函数的偏导数
二元函数有无穷个方向的变化率。
偏导数“片面的导数/部分方向上的导数”，研究的是无穷方向中的某个方向上的变化率，本质与一元函数的导数差不多，只是要说明是求哪个方向上的变化率。

先求$x$轴方向上的变化率：
从中截一个与$x$轴平行方向的面$\alpha$，则可求出$x$轴方向上的变化率。
$$\lim_{\Delta x \to 0} \frac{f(x_0+\Delta x,y_0) - f(x_0,y_0)}{\Delta x}$$
称为函数$f(x,y)$在点$(x_0,y_0)$处对$x$轴方向的变化率。
记为$f_x'(x_0,y_0)$，$\left.\frac{\partial f}{\partial x}\right|_{\substack{x=x_0\\y=y_0}}$，$\frac{\partial f(x_0,y_0)}{\partial x}$。
若设$f(x,y)=z$，则可记为：$\left.\frac{\partial z}{\partial x}\right|_{\substack{x=x_0\\y=y_0}}$，$\left.z_x'\right|_{\substack{x=x_0\\y=y_0}}$。

---

# N 多元函数微分_第9页.png

（二元函数$z=f(x,y)$偏导数几何意义示意图）
从中截一个与y轴平行方向的面，则可求出y轴方向上的变化率。

$$\lim_{\Delta y \to 0} \frac{f(x_0,y_0+\Delta y)-f(x_0,y_0)}{\Delta y}$$

称为函数$f(x,y)$在点$(x_0,y_0)$处沿y轴方向上的变化率，
记为$f_y'(x_0,y_0)$，$\left.\frac{\partial f}{\partial y}\right|_{\begin{subarray}{l}x=x_0\\y=y_0\end{subarray}}$，$\frac{\partial f(x_0,y_0)}{\partial y}$。

若设$f(x,y)=z$，
则可记为：$\left.\frac{\partial z}{\partial y}\right|_{\begin{subarray}{l}x=x_0\\y=y_0\end{subarray}}$，$\left.z_y'\right|_{\begin{subarray}{l}x=x_0\\y=y_0\end{subarray}}$。

## 注：
- 若$z=f(x,y)$在点$(x_0,y_0)$处x轴、y轴方向上的偏导数都存在，则称函数$f(x,y)$在点$(x_0,y_0)$处有偏导数。
- 若$z=f(x,y)$在区域$D$上的每一点$(x,y)$处都有偏导数，则称函数$f(x,y)$在区域$D$上存在偏导函数。

偏导函数记作：$\frac{\partial z}{\partial x}$，$\frac{\partial z}{\partial y}$，$\frac{\partial f}{\partial x}$，$\frac{\partial f}{\partial y}$，$f_x'(x,y)$，$f_y'(x,y)$等。

无论是在x轴方向求导，还是在y轴方向上求导，都可以按对应规则计算，具体求导方法见例题页。

---

# N 多元函数微分_第10页.png

## 高阶偏导数
若函数$f(x,y)$的偏导数$f_x'(x,y)$和$f_y'(x,y)$仍存在偏导数，则
$f_x'(x,y)$和$f_y'(x,y)$的偏导数为函数$f(x,y)$的二阶偏导数。

第一次求导时，可以为$x$轴、$y$轴两个方向
第二次求导时，也可以为$x$、$y$轴两个方向
所以，二阶偏导数实际上有4个：

$$\frac{\partial^2 z}{\partial x^2} = \frac{\partial}{\partial x}\left( \frac{\partial z}{\partial x} \right) = f_{xx}''(x,y) = z_{xx}''$$
$$\frac{\partial^2 z}{\partial x\partial y} = \frac{\partial}{\partial y}\left( \frac{\partial z}{\partial x} \right) = f_{xy}''(x,y) = z_{xy}''$$
$$\frac{\partial^2 z}{\partial y^2} = \frac{\partial}{\partial y}\left( \frac{\partial z}{\partial y} \right) = f_{yy}''(x,y) = z_{yy}''$$
$$\frac{\partial^2 z}{\partial y\partial x} = \frac{\partial}{\partial x}\left( \frac{\partial z}{\partial y} \right) = f_{yx}''(x,y) = z_{yx}''$$

其中，称$f_{xy}''(x,y)$与$f_{yx}''(x,y)$为二阶混合偏导数。

**注**：若$\displaystyle \frac{\partial\left( \frac{\partial f}{\partial x} \right)}{\partial y}$与$\displaystyle \frac{\partial\left( \frac{\partial f}{\partial y} \right)}{\partial x}$在区域$D$内连续，则两者相等，与求导次序无关。
在大部分情况下，我们只用求两者之一即可。

**例13.3**
已知函数$f(x,y) = \ln\left( y + |x\sin y| \right)$，判断$\displaystyle \left. \frac{\partial f}{\partial x} \right|_{(0,1)}$与$\displaystyle \left. \frac{\partial f}{\partial y} \right|_{(0,1)}$的存在性。

**解：**
$$
\begin{aligned}
\left. \frac{\partial f}{\partial x} \right|_{(0,1)} &= \lim_{\Delta x \to 0} \frac{f(0+\Delta x,1) - f(0,1)}{\Delta x} \\
&= \lim_{\Delta x \to 0} \frac{\ln(1 + |\Delta x \sin 1|) - 0}{\Delta x} \quad (\Delta x \to 0 \text{ 时，} \Delta x \sin1 \to 0) \\
&= \lim_{\Delta x \to 0} \frac{|\Delta x| \sin1}{\Delta x} \quad (\text{利用等价无穷小：} \ln(1+x) \sim x,\, x\to0) \\
&= \sin1 \text{ 或 } -\sin1
\end{aligned}
$$

---

# N 多元函数微分_第11页.png

$\Rightarrow \left.\frac{\partial f}{\partial x}\right|_{(0,1)}$ 不存在

$$
\left.\frac{\partial f}{\partial y}\right|_{(0,1)} = \lim_{\Delta y \to 0} \frac{f(0,1+\Delta y)-f(0,1)}{\Delta y}
$$
$$
= \lim_{\Delta y \to 0} \frac{\ln(1+\Delta y)-0}{\Delta y}
$$
（$\Delta y \to 0$时，$\ln(1+\Delta y) \sim \Delta y$）
$$
= \lim_{\Delta y \to 0} \frac{\Delta y}{\Delta y} = 1
$$

## 例13.4 “积分变量只有一个$t$，比较简单”
设函数$f(t)$连续，
令 $F(x,y) = \int_{0}^{x-y} (x-y-t)f(t) \,\mathrm{d}t$，
求 $\displaystyle \frac{\partial F}{\partial x},\ \frac{\partial^2 F}{\partial x^2},\ \frac{\partial F}{\partial y},\ \frac{\partial^2 F}{\partial y^2}$。

## 分析
$x,y$为求导变量，$t$为积分变量。
积分时，$x,y$当常数看。
求导的话，因为我们求偏导数是只对$x$轴方向或$y$轴方向这一单方向的求导，与一元函数求导没区别，则求导规则也没区别。
- 若是在$x$轴方向求导，则可视$y$为常数；
- 若是在$y$轴方向求导，则可视$x$为常数。

例：若我们在$x$轴方向求导，则$y$视为常数，函数$\displaystyle x\int_{0}^{x-y} f(t)\,\mathrm{d}t$的求导规则为乘积求导法则：
$$
(f(x)\cdot g(x))' = f'(x)g(x) + f(x)g'(x)
$$
其中$f(x)=x$，$\displaystyle g(x)=\int_{0}^{x-y} f(t)\,\mathrm{d}t$。

---

# N 多元函数微分_第12页.png

## 二元变限积分的偏导数计算
函数$\int_0^{x-y} f(t)dt$求导规则依旧为：
视$y$为常数，公式与一元的一样，$t$换成$\beta(x),\alpha(x)$。

一元变限积分求导公式：
$$F(x)=\int_{\alpha(x)}^{\beta(x)} f(t)dt$$
$$F'(x)=f\left[\beta(x)\right]\beta'(x) - f\left[\alpha(x)\right]\alpha'(x)$$

待求偏导的二元函数：
$$F(x,y)$$
$$
\begin{aligned}
&= \int_0^{x-y} x f(t)dt - \int_0^{x-y} y f(t)dt - \int_0^{x-y} t f(t)dt \\
&= x\int_0^{x-y} f(t)dt - y\int_0^{x-y} f(t)dt - \int_0^{x-y} t f(t)dt
\end{aligned}
$$

解：
$$F(x,y)=x\int_0^{x-y} f(t)dt - y\int_0^{x-y} f(t)dt - \int_0^{x-y} t f(t)dt$$

计算$\int_0^{x-y} f(t)dt$对$x$的偏导（视$y$为常数）：
$$
\begin{aligned}
\frac{\partial}{\partial x}\left( \int_0^{x-y} f(t)dt \right)
&= f(x-y)\cdot \frac{\partial}{\partial x}(x-y) \\
&= f(x-y)
\end{aligned}
$$

计算$y\int_0^{x-y} f(t)dt$对$x$的偏导（$y$为常数）：
$$
\begin{aligned}
\frac{\partial}{\partial x}\left( y\int_0^{x-y} f(t)dt \right)
&= y f(x-y)
\end{aligned}
$$

计算$\int_0^{x-y} t f(t)dt$对$x$的偏导（$y$为常数）：
$$
\begin{aligned}
\frac{\partial}{\partial x}\left( \int_0^{x-y} t f(t)dt \right)
&= (x-y)f(x-y) \cdot \frac{\partial}{\partial x}(x-y) \\
&= (x-y)f(x-y)
\end{aligned}
$$

合并得到对$x$的偏导数：
$$
\begin{aligned}
\frac{\partial F}{\partial x}
&= \int_0^{x-y} f(t)dt + x f(x-y) - y f(x-y) - (x-y)f(x-y) \\
&= \int_0^{x-y} f(t)dt
\end{aligned}
$$

同理，视$x$为常数，计算对$y$的偏导数：
$$
\begin{aligned}
\frac{\partial F}{\partial y}
&= -x f(x-y) - \int_0^{x-y} f(t)dt + y f(x-y) + (x-y)f(x-y)
\end{aligned}
$$

---

# N 多元函数微分_第13页.png

$$= -\int_{0}^{x-y} f(t) dt$$

对$x$求二阶偏导（将$y$视为常数）：
$$
\begin{aligned}
\frac{\partial^2 F}{\partial x^2} &= \frac{\partial}{\partial x}\left( \int_{0}^{x-y} f(t) dt \right) \\
&= f(x-y)
\end{aligned}
$$

对$y$求二阶偏导（将$x$视为常数）：
$$
\begin{aligned}
\frac{\partial^2 F}{\partial y^2} &= \frac{\partial}{\partial y}\left( -\int_{0}^{x-y} f(t) dt \right) \\
&= -f(x-y)\cdot \frac{\partial}{\partial y}(x-y) \\
&= f(x-y)
\end{aligned}
$$

## 例13.5
设函数$f(x,y)=\int_{0}^{xy} e^{-xt^2} dt$，求$f_x'(1,+\infty)$。

【分析】只有当被积函数里只有积分变量时，才可直接积分求导。所以，我们要把被积函数里的求导变量换走，用换元法。
由题知，这是在点$(1,+\infty)$处求$x$轴方向上的变化率。
∵ 是在点$(1,+\infty)$处求变化率
∴ $x>0, y>0$
用换元法时，求导变量$x$可看作常数。
∵ 若令$xt^2 = u$
则$t=\sqrt{\frac{u}{x}}$，不好算
∴ 令$\sqrt{x}\, t = u$

解：令$\sqrt{x}\, t = u$（换元时将$x,y$视为常数），则：
$$e^{-xt^2} = e^{-u^2}$$
$$t = \frac{u}{\sqrt{x}}$$
根据微分运算性质，常数因子可提出微分号（例如$3du = d(3u)$），得：
$$dt = d\left( \frac{u}{\sqrt{x}} \right) = \frac{1}{\sqrt{x}} du$$

更换积分上下限：
- 当$t=0$时，$u=\sqrt{x}\cdot t = 0$
- 当$t=xy$时，$u=\sqrt{x}\cdot t = x^{\frac{3}{2}} y$

---

# N 多元函数微分_第14页.png

$$原式=\frac{1}{\sqrt{x}}\int_{0}^{x^{\frac{3}{2}}y} e^{-u^2}du$$
是题目中已给出了$x_0$与$y_0$的值，且
我们是对$x$轴方向求导，$y,u$视为常数
则我们可以先把$y_0$值代上去，会简单些
当然，也可以先把$y$看作常数，
求出$x$轴方向上的导数后
再把$x_0=1,\,y_0=+\infty$代入
$$
\begin{align*}
f(x,+\infty)&=\lim_{y\to+\infty} f(x,y)\\
&=\frac{1}{\sqrt{x}}\int_{0}^{+\infty} e^{-u^2}du
\end{align*}
$$
之前反常积分处算过，之后二重积分也会讲
$$\int_{0}^{+\infty} e^{-x^2}dx=\frac{\sqrt{\pi}}{2}$$
即
$$f(x,+\infty)=\frac{\sqrt{\pi}}{2}\cdot\frac{1}{\sqrt{x}}$$
$$
\begin{align*}
f'_x(1,+\infty)&=\left.\frac{\sqrt{\pi}}{2}\cdot\left(\frac{1}{\sqrt{x}}\right)'\right|_{x=1}\\
&=\left.\frac{\sqrt{\pi}}{2}\cdot\left(-\frac{1}{2}\right)x^{-\frac{3}{2}}\right|_{x=1}\\
&=-\frac{\sqrt{\pi}}{4}
\end{align*}
$$

## 求不定积分
*Compare（对比）*
与一元相同点
$$f'(x)=\frac{df(x)}{dx}=\cos x$$
是在$x$轴方向上求导
$$f(x)=\int \cos x dx=\sin x + C$$
是在$x$轴方向上求原函数。

---

# N 多元函数微分_第15页.png

若是先在$y$轴方向上求导，那求原函数也要在$y$轴方向上，路径上要保持一致，与二元函数一样。

当然，在$x$轴方向上求积分时，$y$可视为常数；在$y$轴方向上求积分时，$x$可视为常数。

## 与一元不定积分的不同点
一元函数不定积分：
$$
\begin{align*}
f(x) &= \int \cos x \, dx \\
&= \sin x + C
\end{align*}
$$
其中$C$是任意常数。

二元函数在$x$轴方向上求不定积分（对$x$积分）：
$$
\begin{align*}
f(x,y) &= \int y\cos x \, dx \\
&= y\sin x + \varphi(y)
\end{align*}
$$

$\varphi(y)$是关于$y$的任意函数。
因为是在$x$轴方向上求原函数，可视$y$为常数，因此$+\varphi(y)$与一元情形的$+C$没有区别。

当然，如果是在$y$轴方向上求原函数，最后要$+\varphi(x)$。
至于$\varphi(\cdot)$是什么，后面会讲。

## 例13.6 二元函数求不定积分
设函数$f(x,y)$可微，$f(0,0)=0$，
$$\frac{\partial f}{\partial x} = -f(x,y),\quad \frac{\partial f}{\partial y} = e^{-x}\cos y,$$
求$f(x,y)$。

---

# N 多元函数微分_第16页.png

## 分析
可微，后面会讲
这里给出了$f_x'(x,y)$与$f_y'(x,y)$
让你求$f(x,y)$，相当于求原函数
题中是$f(x,y)$在$y$轴方向上求得
导函数$f_y'(x,y)=e^{-x}\cos y$
则，我们要在$y$轴方向上
对函数$e^{-x}\cos y$求不定积分
至于后面加的$\varphi(x)$
我们可以用$\frac{\partial f}{\partial x}=-f(x,y)$去解

## 解
$\because \frac{\partial f}{\partial y}=e^{-x}\cos y$
$$
\begin{aligned}
\therefore f(x,y)&=e^{-x}\int \cos y \, dy\\
&=e^{-x}\sin y + \varphi(x)
\end{aligned}
$$

$\because \frac{\partial f}{\partial x}=-f(x,y)$
$\therefore \frac{\partial}{\partial x}\left(e^{-x}\sin y + \varphi(x)\right) = -f(x,y)$
$-\sin y \cdot e^{-x} + \varphi'(x) = -f(x,y)$
$\because f(x,y)= e^{-x}\sin y + \varphi(x)$
$\therefore -\sin y \cdot e^{-x} + \varphi'(x) = -e^{-x}\sin y - \varphi(x)$
$\Rightarrow \varphi'(x) = -\varphi(x)$

这里由微分方程的知识（之后会讲）
可得$\varphi(x)=Ce^{-x}$（$C$为常数）

具体算法，这里可简单展示
$\varphi'(x)=-\varphi(x)$
$$\frac{d\varphi(x)}{dx}=-\varphi(x)$$

---

# N 多元函数微分_第17页.png

$$\frac{d\varphi(x)}{\varphi(x)} = -dx$$
$$\int \frac{1}{\varphi(x)} d\varphi(x) = -\int dx$$
$$\ln|\varphi(x)| = -x + C$$
$$\ln|\varphi(x)| = -x + \ln C$$
$$e^{\ln|\varphi(x)|} = e^{-x+\ln C}$$
$$|\varphi(x)| = C e^{-x}$$
$$\varphi(x) = \pm C e^{-x}$$
$$\varphi(x) = C e^{-x}$$
$$\Rightarrow \varphi(x) = C e^{-x} \quad (C为常数)$$

$$f(x,y) = e^{-x}\sin y + C e^{-x}$$

## 多元函数的全微分
### 回顾：一元函数微分
#### 定义
对于一个一元函数$y=f(x)$在点$x_0$处可微，是指，函数增量$\Delta y = f(x_0+\Delta x) - f(x_0)$可以表示为：
$$\Delta y = A\Delta x + o(\Delta x)$$
$A\Delta x$为$y=f(x)$在点$x_0$处的微分，记作：
$$
\begin{aligned}
dy &= A\cdot \Delta x \\
&= A dx
\end{aligned}
$$
其中$A = f'(x)$，则微分可表达为：
$$dy = f'(x)dx$$

---

# N 多元函数微分_第18页.png

## 核心思想
用简单的线性函数（直线），来逼近复杂的非线性函数（曲线）。

复杂增量 $\Delta y = f(x_0+\Delta x) - f(x_0)$
可被分解为两个部分：
- 一个与$\Delta x$成比例的线性部分
- 一个当$\Delta x \to 0$时，比$\Delta x$消失更快的部分

即
$$\Delta y = A\Delta x + o(\Delta x)$$

- $\Delta x$为点$x_0$与点$x=x_0+\Delta x$之间的距离
- $A\cdot\Delta x$ 是线性主部
- $o(\Delta x)$是高阶无穷小量

## 微分与导数的关系
$$\lim_{\Delta x \to 0} \frac{\Delta y}{\Delta x} = \lim_{\Delta x \to 0} \frac{A\Delta x + o(\Delta x)}{\Delta x} = A$$

由可导，可推出可微，也可反推：
$$\text{可微} \iff \text{可导}$$

导数反映了函数变化的速度；
微分反映了由一个微小增量$dx$所引起的具体变化量$dy$。

## 几何意义
在点$x_0$处，$x$轴方向上满足 $|\Delta y - dy| = o(\Delta x)$，为曲线增量$\Delta y$与切线增量$dy$之间的差距。
即，$dy$与真实变化量$\Delta y$之间差了一个无穷小量。

---

# N 多元函数微分_第19页.png

## 二元函数的全微分
**定义**
对于二元函数$z=f(x,y)$，在点$(x_0,y_0)$处可全微分是指：
函数的全增量（因为两个变量都有增量，则$\Delta z$为全增量）：
$$\Delta z = f(x_0+\Delta x,y_0+\Delta y) - f(x_0,y_0)$$
可表示为：
$$\Delta z = A\Delta x + B\Delta y + o(\rho)$$
$A\Delta x+B\Delta y$为$z=f(x,y)$在点$(x_0,y_0)$处的全微分，记作：
$$
\begin{aligned}
\mathrm{d}z &= A\Delta x + B\Delta y \\
&= A\mathrm{d}x + B\mathrm{d}y
\end{aligned}
$$
其中：
$A = f'_x(x,y)$
$B = f'_y(x,y)$

则全微分可表达为：
$$\mathrm{d}z = \frac{\partial z}{\partial x}\mathrm{d}x + \frac{\partial z}{\partial y}\mathrm{d}y$$

**核心思想**
用简单的线性函数（切平面），来逼近复杂的非线性函数（曲面）。

复杂全增量$\Delta z = f(x_0+\Delta x,y_0+\Delta y) - f(x_0,y_0)$可被分解为两个部分：
- 一个关于$\Delta x$和$\Delta y$的线性部分
- 一个当$\rho \to 0$时，比$\rho$消失更快的部分

即，
$$\Delta z = A\Delta x + B\Delta y + o(\rho)$$
- $\rho$为点$(x_0,y_0)$与$(x_0+\Delta x,y_0+\Delta y)$之间的距离
- $A\Delta x+B\Delta y$是线性主部
- $o(\rho)$是高阶无穷小量

---

# N 多元函数微分_第20页.png

二元函数增量示意图：标注点$(x_0,y_0)$、$(x_0+\Delta x,y_0)$、$(x_0,y_0+\Delta y)$、$(x_0+\Delta x,y_0+\Delta y)$，标记增量$\Delta x$、$\Delta y$，两点间距离$\rho=\sqrt{(\Delta x)^2+(\Delta y)^2}$。

## 全微分与偏导的关系
### x轴方向偏导推导
在x轴方向上求偏导：
因为沿x轴方向求偏导时y值固定，因此令$\Delta y=0$，此时$\rho=\sqrt{(\Delta x)^2+(\Delta y)^2}=|\Delta x|$，且$B\Delta y=0$。
$$
\begin{align*}
\lim_{\Delta x \to 0} \frac{\Delta z}{\Delta x} &= \lim_{\Delta x \to 0} \frac{\Delta z}{\Delta x} \\
&= \lim_{\Delta x \to 0} \frac{A\Delta x + o(|\Delta x|)}{\Delta x} \\
&= \lim_{\Delta x \to 0} \frac{A\Delta x}{\Delta x} + \lim_{\Delta x \to 0} \frac{o(|\Delta x|)}{\Delta x} \\
&= A
\end{align*}
$$

### y轴方向偏导推导
y轴方向上同理：
令$\Delta x=0$，此时$\rho=\sqrt{(\Delta x)^2+(\Delta y)^2}=|\Delta y|$，且$A\Delta x=0$。
$$
\begin{align*}
\lim_{\Delta y \to 0} \frac{\Delta z}{\Delta y} &= \lim_{\Delta y \to 0} \frac{B\Delta y + o(|\Delta y|)}{\Delta y} \\
&= B
\end{align*}
$$

### 可微与可偏导的关系
$$\text{可全微分} \implies \text{可偏导，逆命题不成立}$$

### 概念说明
- 偏导数反映了函数在某一坐标轴方向上的变化速度
- 全微分反映了函数在所有方向上，由微小增量$dx$与$dy$所引起的具体变化量$dz$

---

# N 多元函数微分_第21页.png

## 几何意义
附曲面$\Sigma$在点$M$处的切平面、法向量$\vec{n}$与切向量$\vec{T}$的空间直角坐标系示意图。
其含义为：在$(x_0,y_0)$处的所有方向上满足$|\Delta z - \mathrm{d}z| = o(\rho)$，该式描述曲面全增量$\Delta z$与切平面全增量$\mathrm{d}z$之间的差距，即$\mathrm{d}z$与真实变化量$\Delta z$之间差了一个无穷小量。

## 可微的充分条件
$$
\left.
\begin{aligned}
&\text{若函数} \ z=f(x,y) \\
&\text{在点}(x_0,y_0)\text{处的} \\
&\text{偏导数存在且连续}
\end{aligned}
\right\}
\implies
\begin{aligned}
&\text{函数} \ z=f(x,y) \\
&\text{在点}(x_0,y_0)\text{处} \\
&\text{可微}
\end{aligned}
$$
逻辑关系：
$f_x'(x,y) \exists$，$f_y'(x,y) \exists$ $\bcancel{\iff}$ $\Delta z = \mathrm{d}z + o(\rho)$（可微）；
$f_x'(x,y) \exists$且连续，$f_y'(x,y) \exists$且连续 $\implies$ $\Delta z = \mathrm{d}z + o(\rho)$（可微）。

## 注：
### (1) 在区域$D$上
若$\mathrm{d}[f(x,y)] = 0$ 或 $\frac{\partial f}{\partial x} = \frac{\partial f}{\partial y} = 0$，
则$f(x,y) = C$（常数），$(x,y)\in D$。

### (2) 判别函数$z=f(x,y)$在点$(x_0,y_0)$处的偏导数是否连续，步骤如下
- 用定义法求$f_x'(x_0,y_0), f_y'(x_0,y_0)$
- 用公式法求$f_x'(x,y), f_y'(x,y)$
- 计算$\lim\limits_{\substack{x\to x_0 \\ y\to y_0}} f_x'(x,y)$，$\lim\limits_{\substack{x\to x_0 \\ y\to y_0}} f_y'(x,y)$
验证$\lim\limits_{(x,y)\to(x_0,y_0)} f_x'(x,y) = f_x'(x_0,y_0)$与$\lim\limits_{(x,y)\to(x_0,y_0)} f_y'(x,y) = f_y'(x_0,y_0)$是否成立。
若成立，则$z=f(x,y)$在点$(x_0,y_0)$处的偏导数是连续的。

---

# N 多元函数微分_第22页.png

## 概念对比（Compare）
### 一元函数
（概念关系示意图，展示可微、导数存在、连续、极限存在的推导关系）
- 可微 $\iff$ 导数存在（可导）
- 可微 $\implies$ 连续，连续 $\nRightarrow$ 可微
- 导数存在（可导）$\implies$ 连续，连续 $\nRightarrow$ 导数存在（可导）
- 连续 $\implies$ 极限存在，极限存在 $\nRightarrow$ 连续
- 导数存在（可导）$\implies$ 极限存在，极限存在 $\nRightarrow$ 导数存在（可导）

### 二元函数
（概念关系示意图，展示偏导数连续、可微、连续、偏导数存在、极限存在的推导关系）
- 偏导数连续 $\implies$ 可微，可微 $\nRightarrow$ 偏导数连续
- 可微 $\implies$ 连续，连续 $\nRightarrow$ 可微
- 可微 $\implies$ 偏导数存在，偏导数存在 $\nRightarrow$ 可微
- 连续 $\implies$ 极限存在，极限存在 $\nRightarrow$ 连续
- 连续与偏导数存在之间无必然推导关系，二者互相不能推出
- 偏导数存在与极限存在之间无必然推导关系，二者互相不能推出

## (3) 可微的判别步骤
判别函数$z=f(x,y)$在点$(x_0,y_0)$处是否可微，步骤如下：
1.  写出全增量
$$\Delta z = f(x_0+\Delta x, y_0+\Delta y) - f(x_0,y_0)$$
2.  写出线性增量$A\Delta x+B\Delta y$，其中$A=f_x'(x_0,y_0),\ B=f_y'(x_0,y_0)$
3.  计算极限
$$\lim_{\substack{\Delta x \to 0 \\ \Delta y \to 0}} \frac{\Delta z - (A\Delta x+B\Delta y)}{\sqrt{(\Delta x)^2+(\Delta y)^2}}$$
若极限等于$0$，则$z=f(x,y)$在点$(x_0,y_0)$处可微；否则，不可微。

## 例13.7
已知$(axy^3 - y^2\cos x)\mathrm{d}x + (1+by\sin x + 3x^2y^2)\mathrm{d}y$为某一函数$u(x,y)$的全微分，求$(a,b)$。
### 分析
$\because u(x,y)$可全微分，
$$\therefore \mathrm{d}u = \frac{\partial u}{\partial x}\mathrm{d}x + \frac{\partial u}{\partial y}\mathrm{d}y.$$

---

# N 多元函数微分_第23页.png

$$
\begin{cases}
\dfrac{\partial u}{\partial x} = axy^3 - y^2\cos x \\
\dfrac{\partial u}{\partial y} = 1 + by\sin x + 3x^2y^2
\end{cases}
$$
$\because$ 函数$axy^3 - y^2\cos x$与$1+by\sin x+3x^2y^2$是连续的
$\therefore \dfrac{\partial^2 u}{\partial x\partial y} = \dfrac{\partial^2 u}{\partial y\partial x}$，可解出$a$与$b$。
解：
$\because u(x,y)$可全微分
$$
\therefore du = \frac{\partial u}{\partial x}dx + \frac{\partial u}{\partial y}dy
$$
$$
\therefore \begin{cases}
\dfrac{\partial u}{\partial x} = axy^3 - y^2\cos x \\
\dfrac{\partial u}{\partial y} = 1 + by\sin x + 3x^2y^2
\end{cases}
$$
$$
\therefore \frac{\partial^2 u}{\partial x\partial y} = \frac{\partial}{\partial y}\left( \frac{\partial u}{\partial x} \right) = 3axy^2 - 2y\cos x
$$
$$
\frac{\partial^2 u}{\partial y\partial x} = \frac{\partial}{\partial x}\left( \frac{\partial u}{\partial y} \right) = by\cos x + 6xy^2
$$
$\because \dfrac{\partial^2 u}{\partial x\partial y} = \dfrac{\partial^2 u}{\partial y\partial x}$
$$
\therefore \begin{cases}
a=2 \\
b=-2
\end{cases}, \text{即}(a,b)=(2,-2)
$$
## 例13.8
设$z_1 = |xy|$，
$$
z_2 =
\begin{cases}
\dfrac{xy}{\sqrt{x^2+y^2}}, & (x,y)\neq(0,0) \\
0, & (x,y)=(0,0)
\end{cases}
$$
则判断$z_1,z_2$在点$(0,0)$处是否可微。

---

# N 多元函数微分_第24页.png

## 分析
只要$\Delta z = dz + o(\rho)$成立，则函数在该点可微；若该式不成立，则函数在该点不可微。

## 解
计算函数在$(0,0)$处的全增量：
$$\Delta z_1 = z_1(0+\Delta x,0+\Delta y) - z_1(0,0) = |\Delta x \Delta y|$$

写出全微分的定义形式：
$$dz_1 = z_{1x}'(0,0)\Delta x + z_{1y}'(0,0)\Delta y$$

计算$(0,0)$处对$x$的偏导数：
$$z_{1x}'(0,0) = \lim_{\Delta x \to 0} \frac{z_1(0+\Delta x,0) - z_1(0,0)}{\Delta x} = 0$$

计算$(0,0)$处对$y$的偏导数：
$$z_{1y}'(0,0) = \lim_{\Delta y \to 0} \frac{z_1(0,0+\Delta y) - z_1(0,0)}{\Delta y} = 0$$

因此$(0,0)$处的全微分为：
$$\Rightarrow dz_1 = 0$$

验证可微定义的极限条件：
$$
\lim_{\substack{\Delta x \to 0 \\ \Delta y \to 0}} \frac{\Delta z_1 - dz_1}{\sqrt{(\Delta x)^2 + (\Delta y)^2}}
= \lim_{\substack{\Delta x \to 0 \\ \Delta y \to 0}} \frac{|\Delta x \Delta y|}{\sqrt{(\Delta x)^2 + (\Delta y)^2}}
$$
放缩所用不等式：$|ab| \leq \frac{1}{2}(a^2+b^2)$，对分子做放缩：
$$
\lim_{\substack{\Delta x \to 0 \\ \Delta y \to 0}} \frac{|\Delta x \Delta y|}{\sqrt{(\Delta x)^2 + (\Delta y)^2}}
\leq \lim_{\substack{\Delta x \to 0 \\ \Delta y \to 0}} \frac{\frac{1}{2}\left[(\Delta x)^2 + (\Delta y)^2\right]}{\sqrt{(\Delta x)^2 + (\Delta y)^2}}
= \lim_{\substack{\Delta x \to 0 \\ \Delta y \to 0}} \frac{1}{2}\sqrt{(\Delta x)^2 + (\Delta y)^2}
= 0
$$

由夹逼准则：
$$
0 \leq \lim_{\substack{\Delta x \to 0 \\ \Delta y \to 0}} \frac{|\Delta x \Delta y|}{\sqrt{(\Delta x)^2 + (\Delta y)^2}}
\leq \lim_{\substack{\Delta x \to 0 \\ \Delta y \to 0}} \frac{1}{2}\sqrt{(\Delta x)^2 + (\Delta y)^2}
$$
不等式两端极限均为0，因此：
$$
\Rightarrow \lim_{\substack{\Delta x \to 0 \\ \Delta y \to 0}} \frac{\Delta z_1 - dz_1}{\sqrt{(\Delta x)^2 + (\Delta y)^2}} = 0
$$

则$z_1$在$(0,0)$点可微。

---

# N 多元函数微分_第25页.png

## 二元函数$Z_2$在$(0,0)$点的可微性判定
$$\Delta Z_2 = \frac{\Delta x |\Delta y|}{\sqrt{(\Delta x)^2 + (\Delta y)^2}}$$
$$\mathrm{d}Z_2 = Z'_{2x}(0,0)\Delta x + Z'_{2y}(0,0)\Delta y$$
$$Z'_{2x}(0,0) = \lim_{\Delta x \to 0} \frac{Z_2(0+\Delta x,0) - Z_2(0,0)}{\Delta x} = 0$$
$$Z'_{2y}(0,0) = \lim_{\Delta y \to 0} \frac{Z_2(0,0+\Delta y) - Z_2(0,0)}{\Delta y} = 0$$
$$\Rightarrow \mathrm{d}Z_2 = 0$$
$$\lim_{\substack{\Delta x \to 0 \\ \Delta y \to 0}} \frac{\Delta Z_2 - \mathrm{d}Z_2}{\sqrt{(\Delta x)^2 + (\Delta y)^2}}$$
$$= \lim_{\substack{\Delta x \to 0 \\ \Delta y \to 0}} \frac{\Delta x |\Delta y|}{(\Delta x)^2 + (\Delta y)^2}$$
在例13.1有说过，此极限不存在。
不存在
$$\Rightarrow \mathrm{d}Z_2 \text{不存在}$$
即$Z_2$在$(0,0)$点不可微。