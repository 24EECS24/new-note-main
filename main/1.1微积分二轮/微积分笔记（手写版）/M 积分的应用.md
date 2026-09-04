---

# M 积分的应用_第1页.png

## 积分的几何应用
“套公式，做计算”

## 一、用定积分表达和计算平面图形的面积
假设以下曲线都是连续的。
若用到反常积分，一般是收敛的。

三大体系的图形：
1.  直角坐标系下（直接算）
2.  参数方程系
    - 直接算（少）
    - 换元法
3.  极坐标系（直接算）

- 直角坐标系下的平面图形面积：
曲线$y=y_1(x)$与$y=y_2(x)$及$x=a$、$x=b$（$a<b$）所围成的平面图形的面积（直角坐标系）：
$$S=\int_{a}^{b} \left| y_1(x) - y_2(x) \right| dx$$
（对应函数示意图：两条曲线$y_1(x)$、$y_2(x)$在区间$[a,b]$内相交，以阴影标注二者围成的平面图形，标注了$x$轴、$y$轴，以及区间端点$a$、$b$）

- 参数方程坐标系下的面积计算：
见例10.2，可由直角坐标系过渡求解，即从直角坐标形式$y=f(x)$转换为参数方程形式
$$\begin{cases}
x = g(t) \\
y = w(t)
\end{cases}$$
的过程，其实就是换元的过程。

---

# M 积分的应用_第2页.png

## 参数方程形式的平面图形面积计算
$y=f(x) \xrightarrow{\text{令 }x=g(t)} y=f[g(t)]$
进一步写为参数方程形式：
$$
\begin{cases}
x = g(t) \\
y = f[g(t)] = w(t)
\end{cases}
$$
则对于用积分求面积，我们可以由直角坐标系过渡到参数方程坐标系，无非就是用定积分的换元法。

即，eg：题目给你参数方程：
$$
\begin{cases}
y = w(t) \\
x = g(t)
\end{cases}
$$
函数示意图：平面直角坐标系x轴上标注原点$O$、端点$a,b$；该参数方程对应的上凸曲线连接$(a,0)$与$(b,0)$，曲线与x轴围成的上半区域为阴影，要求该区域的面积。
让你求所围面积。

先设直角坐标系下曲线为$y=f(x)$，则面积为：
$$S = \int_{a}^{b} f(x) dx \quad \text{“虽然我们不知}f(x)\text{”}$$
相当于是做换元：令$x = g(t)$
当$x=a$时，对应参数$t=\alpha$，即$g(\alpha)=a$；当$x=b$时，对应参数$t=\beta$，即$g(\beta)=b$
微分替换：$dx = d\left[g(t)\right]$
被积函数替换：$f(x) = f\left[g(t)\right] = w(t)$

代入得：
$$\Rightarrow S = \int_{\alpha}^{\beta} w(t) \, d\left[g(t)\right]$$
则，已可解。

---

# M 积分的应用_第3页.png

## 极坐标系
O为极点，对应极坐标基本示意图：极点为$O$，极轴沿$x$轴正方向，标注点$P$、极径$r$、极角$\theta$。
极径$r=|OP|$，$r$的长度随$\theta$的变化而变化，即极坐标曲线方程为：
$$r=r(\theta)$$

曲线$r=r_1(\theta)$与$r=r_2(\theta)$及射线$\theta=\alpha$，$\theta=\beta\ (0<\beta-\alpha\leq2\pi)$所围成的曲边扇形的面积为：
$$S=\frac{1}{2}\int_{\alpha}^{\beta}\left|r_1^2(\theta)-r_2^2(\theta)\right|d\theta$$
对应两曲线围成区域示意图：标注$r_1(\theta),r_2(\theta),\theta=\alpha,\theta=\beta$，极点$O$，极轴$x$。

证明：弧度制下弧长$L=\angle c \cdot r$，圆面积为$\pi r^2$，对应小扇形分割示意图：标注$\theta=\alpha,\theta=\beta$，极径$r_1,r_2$，内角$\angle a,\angle b,\angle c$，弧长$l$，极点$O$，极轴$x$。
圆心角为$\angle c$的扇形面积为：
$$\text{扇形面积}=\frac{\angle c}{360^\circ}\cdot\pi r^2$$
将角度转换为弧度制（$360^\circ=2\pi$），推导得：
$$
\begin{align*}
\text{扇形面积}&=\frac{\angle c}{2\pi}\cdot\pi r^2\\
&=\frac{1}{2}\angle c \cdot r^2\\
&=\frac{1}{2}\angle c \cdot r \cdot r\\
&=\frac{1}{2} l r
\end{align*}
$$

记边界极径$r_1=r(\beta),\ r_2=r(\alpha)$，当$\angle c \to 0$时，即：$\angle c=\beta-\alpha=d\theta$时，有$\beta\approx\alpha$，$r_1\approx r_2$，$\angle a\approx\angle b\approx90^\circ$。
则扇形面积$\approx \frac{1}{2}\cdot底\cdot高$，即：
$$
\begin{align*}
&\approx\frac{1}{2}\cdot r_2 \cdot l\\
&=\frac{1}{2}\cdot r_2 \cdot r_2 \cdot d\theta\\
&=\frac{1}{2}r_2^2 d\theta
\end{align*}
$$
对应单曲边扇形示意图：标注$\theta=\alpha,\theta=\beta$，极径$r$，极点$O$，极轴$x$，阴影为积分区域。
则阴影面积为：
$$S=\frac{1}{2}\int_{\alpha}^{\beta}r^2(\theta)d\theta$$

**例10.1** 设$A_n$是曲线$y=x^n$与$y=x^{n+1}$（$n=1,2,3,\cdots$）所围的面积，则求：
$$\lim_{n\to\infty}\left(2\sum_{k=1}^{n}A_k\right)^n$$

---

# M 积分的应用_第4页.png

## 分析
先求出$A_n$，再由$A_n$求出$\lim\limits_{n \to \infty} \left(2\sum_{k=1}^n A_k\right)^n$。

## 解答
先找出$y=x^n$与$y=x^{n+1}$所围的面积，即先找交点：
$$x^{n+1}=x^n$$
$$x^{n+1}-x^n=0$$
$$x^n(x-1)=0$$
$$\Rightarrow x=0,\,x=1$$

发现在$x=0,x=1$处各有一个交点，因此所围区域在$x\in[0,1]$上；且在区间$x\in[0,1]$内，$x^{n+1}<x^n$，即$x^n - x^{n+1}\geq0$，因此：
$$
\begin{align*}
A_n&=\int_0^1 (x^n - x^{n+1})dx = \left.F_1(x)\right|_0^1 - \left.F_2(x)\right|_0^1 \\
&= \left.\frac{1}{n+1}x^{n+1}\right|_0^1 - \left.\frac{1}{n+2}x^{n+2}\right|_0^1 \\
&= \frac{1}{n+1} - \frac{1}{n+2}
\end{align*}
$$
即
$$A_n = \frac{1}{n+1} - \frac{1}{n+2}$$

接下来计算极限：
$$
\lim_{n \to \infty} \left(2\sum_{k=1}^n A_k\right)^n
= \lim_{n \to \infty} \left[2\sum_{k=1}^n \left( \frac{1}{k+1} - \frac{1}{k+2} \right) \right]^n
$$

这里要联想到未定式$\lim\limits_{n \to \infty}(1^\infty)$型，验证猜想：
对求和部分裂项可得：
$$
\sum_{k=1}^n \left( \frac{2}{k+1} - \frac{2}{k+2} \right)
= 1-\frac{2}{3}+\frac{2}{3}-\frac{2}{4}+\frac{2}{4}-\frac{2}{5}+\dots+\frac{2}{n+1}-\frac{2}{n+2}
$$

---

# M 积分的应用_第5页.png

当$x\to0$时，$\ln(1+x)\sim x$；
当$x-1\to0$时，$\ln[1+(x-1)]\sim x-1$，即$x\to1$时，$\ln x\sim x-1$。

$$
\therefore \lim_{n\to\infty}\left(1-\frac{2}{n+2}\right)^n
= e^{\lim\limits_{n\to\infty}n\ln\left(1-\frac{2}{n+2}\right)} \quad \text{利用恒等式 }a^b=e^{b\ln a}
$$
$\because n\to\infty$时，$1-\frac{2}{n+2}\to1$，即$-\frac{2}{n+2}\to0$，
$\therefore \ln\left(1-\frac{2}{n+2}\right)\sim \left(1-\frac{2}{n+2}\right)-1$
$$
\begin{align*}
\therefore \quad &= e^{\lim\limits_{n\to\infty}n\cdot\left(\frac{-2}{n+2}\right)}\\
&= e^{-2}
\end{align*}
$$

## 例10.2 “参数方程坐标系”
求摆线$\begin{cases}x=a(t-\sin t)\\y=a(1-\cos t)\end{cases}\ (a>0)$的一拱与x轴所围平面图形的面积。

（函数示意图说明：平面直角坐标系中绘制摆线一拱，起点为原点$O$，终点为x轴上的$(2\pi a,0)$，拱高为$2a$；图侧标注摆线参数方程：
$$\begin{cases}
x=a(t-\sin t)\\
y=a(1-\cos t)
\end{cases}\quad (a>0)$$
）

**分析** 我们不用求$y=f(x)$。
这相当于是由直角坐标系的面积公式：
$$S=\int_a^b f(x)dx$$
令$x=a(t-\sin t)$，则$f(x)=f\left[a(t-\sin t)\right]=a(1-\cos t)$。

**解：** 对于直角坐标系，设$y=f(x)$，则
$$S=\int_0^{2\pi a} f(x)dx$$
虽然我们不知$f(x)$

---

# M 积分的应用_第6页.png

相当于是令 $x = a(t-\sin t)$
当$x=0$时，$0 = a(t-\sin t)$，得$t=0$；
当$x=2\pi a$时，$2\pi a = a(t-\sin t)$，得$t=2\pi$。

$$
\begin{align*}
dx &= d\left[a(t-\sin t)\right] \\
&= a(1-\cos t)dt
\end{align*}
$$

$f(x) = f\left[a(t-\sin t)\right] = a(1-\cos t)$

则
$$
\begin{align*}
\text{原式} &= \int_0^{2\pi} a(1-\cos t)\cdot a(1-\cos t)dt \\
&= a^2\int_0^{2\pi} (1-\cos t)^2 dt \quad \text{用华里士公式求解} \\
&= a^2\int_0^{2\pi} \left(1-2\cos t + \cos^2 t\right)dt \\
&= a^2\cdot 2\pi - 2a^2\int_0^{2\pi}\cos t dt + a^2\int_0^{2\pi}\cos^2 t dt \\
&= a^2\cdot 2\pi + a^2\int_0^{2\pi}\cos^2 t dt \quad \text{用华里士公式} \\
&= a^2\cdot 2\pi + a^2\cdot 4\cdot \frac{1}{2}\cdot \frac{\pi}{2} \\
&= 3\pi a^2
\end{align*}
$$

## 例10.3 求伯努利双纽线$r^2=a^2\cos2\theta$围成的面积
（函数示意图：平面直角坐标系下的伯努利双纽线，标注原点$O$、$x$轴，第一象限内标注极角$\beta=\frac{\pi}{4}$，图形关于x轴、y轴对称）

### 分析
伯努利双纽线四个对称部分面积相等，则我们只用求第一象限的面积，再乘4即可。

解：
$$
S = 4\cdot \frac{1}{2}\int_0^{\frac{\pi}{4}} a^2\cos2\theta \,d\theta
$$

---

# M 积分的应用_第7页.png

$$
\begin{aligned}
&= 2a^2 \cdot \frac{1}{2} \int_{0}^{\frac{\pi}{4}} \cos2\theta \,d\theta \\
&= a^2 \cdot \sin2\theta \bigg|_{0}^{\frac{\pi}{4}} \\
&= a^2
\end{aligned}
$$

## 二、用定积分表达和计算旋转体的体积
曲线$y=y(x)$与$x=a,x=b\ (a<b)$及$x$轴围成的曲边梯形绕$x$轴旋转一周所得旋转体体积
（对应示意图：区间$[a,b]$上以$y=y(x)$为曲边的曲边梯形示意图、该曲边梯形绕$x$轴旋转得到的旋转体示意图）
$$V_x = \int_{a}^{b} \pi y^2(x) \,dx$$

**证明：**
（对应示意图：旋转体薄圆片微元示意图）
我们从中截取极薄一层，$|ab|\to0$，即$|ab|=dx$，则$y(a)=y(b)=$底面圆半径。
薄圆片体积满足 体积=底面积$\times$高：
- 底面积$=\pi r^2 = \pi y^2(a)$
- 高$=dx$
因此体积微元 $dV = \pi y^2(a) dx$
将所有微元累加（积分）后得到总体积：
$$V_x = \int_{a}^{b} \pi y^2(x) \,dx$$

曲线$y=y(x)$与$x=a,x=b\ (0\leq a<b)$及$x$轴围成的曲边梯形绕$y$轴旋转一周所得旋转体体积

---

# M 积分的应用_第8页.png

（平面直角坐标系中，区间$[a,b]$上曲线$y=y(x)$的函数示意图，标注了区间内宽度为$dx$的竖直阴影窄条）
$$V_y = 2\pi \int_a^b x|y(x)|dx$$

## 证明
我们依旧是从中截取极薄一圈
（平面直角坐标系中，区间$[a,b]$上截取的竖直窄条示意图，标注$y=y(x)$）
$|ab|\to0$，即$|ab|=dx$
则$y(a)=y(b)$，$|oa|=|ob|$
转一圈我们得到：
空心的圆柱体
（上述竖直窄条绕$y$轴旋转得到的空心薄圆柱体示意图）
我将$|ab|$那一面切开
然后展成直的，则
我们就得到一个长方体。

（薄圆柱体展开所得长方体示意图，标注底面边长$2\pi r$、侧边高度$y(b)$、厚度$dx$）
高度为$|y(b)|$
宽度为$dx$
长度为：半径为$r=b$的圆的周长$=2\pi r$
$=2\pi b$
体积为长×宽×高
$$= 2\pi b \cdot |y(b)| \cdot dx$$
则再累加后得体积
$$V_y = 2\pi \int_a^b x|y(x)|dx$$

## 小结
$$V_x = \pi \int_a^b \square^2 dx$$
$$V_y = 2\pi \int_a^b x\square dx$$

---

# M 积分的应用_第9页.png

## 平面曲线绕定直线旋转
设平面曲线$L: y=f(x),\ a\leq x\leq b$，且$f(x)$可导。
定直线$L_0: Ax+By+C=0$，且任意一条垂直于$L_0$的直线与$L$至多有一个交点。
（配图：平面直角坐标系$xOy$，x轴上标注$a,b$两点，曲线$L$位于$x\in[a,b]$区间上方，斜向定直线$L_0$位于曲线上方，过$x=a,x=b$分别作$L_0$的垂线连接曲线$L$与$L_0$）
则$L$与x轴围成的曲边梯形绕$L_0$旋转一周所得旋转体体积为
$$V=\frac{\pi}{(A^2+B^2)^{\frac{3}{2}}}\int_{a}^{b}\left[Ax+Bf(x)+C\right]^2\left|Af'(x)-B\right|dx$$

（配图：平面直角坐标系$xOy$，x轴标注原点$O$、$a,b$三点，曲线$L$位于x轴上方$x\in[a,b]$区间）
特别地，若考虑绕x轴旋转的情况，即取$L_0$为x轴位置，令$A=C=0,B\neq0$，则$L_0:y=0$（x轴），此时体积退化为圆盘法公式：
$$V=\pi\int_{a}^{b}f^2(x)dx$$

## 例10.5
求曲线$y=e^{-\frac{x}{2}}\sqrt{\sin x}$在$[0,2\pi]$部分与x轴围成的平面图形绕x轴旋转一周所成旋转体体积。
**分析** 由根式定义，$\sqrt{\sin x}$要求$\sin x\geq0$，因此$x$的有效定义域为$[0,\pi]$，$[\pi,2\pi]$区间上函数无定义，对应部分不存在体积。
**解：**
$$
\begin{align*}
V_x&=\int_{0}^{\pi}\pi\cdot\left(e^{-\frac{x}{2}}\sqrt{\sin x}\right)^2dx\\
&=\pi\int_{0}^{\pi}e^{-x}\sin xdx \quad \text{（该积分计算过程见例9.5）}\\
&=\pi\cdot\left.\frac{-1}{2}e^{-x}(\sin x+\cos x)\right|_{0}^{\pi}\\
&=\frac{1}{2}\pi\left(1+e^{-\pi}\right)
\end{align*}
$$

---

# M 积分的应用_第10页.png

## 例10.6
求曲线 $y=\frac{x}{\sqrt{1+x^2}},\ x>0$ 与 $y=\frac{1}{2}$、$y=\frac{\sqrt{3}}{2}$ 及$y$轴所围图形绕$x$轴旋转一周所得旋转体的体积。

## 分析
（函数示意图：第一象限平面直角坐标系，标注原点$O$、$x$轴、$y$轴，绘制曲线$y=f(x)$，以水平虚线标注$y=\frac{1}{2}$、$y=\frac{\sqrt{3}}{2}$的位置）
此题的旋转方式对应左图，我们将左图按逆时针旋转$90^\circ$，将原$x$轴看作$y$轴，原$y$轴看作$x$轴，问题就转化为与绕$y$轴旋转体积同形式的问题，因此需要先求$y=f(x)$的反函数。

## 解答
推导$y=f(x)$的反函数：
由 $y^2=\frac{x^2}{1+x^2},\ x>0$，
两边同乘$1+x^2$得：
$$x^2 = y^2(1+x^2)$$
展开并移项整理：
$$x^2 = y^2 + y^2x^2$$
$$x^2(1-y^2) = y^2$$
$$x^2 = \frac{y^2}{1-y^2}$$
因为$x>0$，开方得：
$$x = \frac{y}{\sqrt{1-y^2}}$$
由$x>0$，分母$\sqrt{1-y^2}>0$，可得$0<y<1$，即反函数为：
$$x = \frac{y}{\sqrt{1-y^2}},\quad 0<y<1$$

根据柱壳法，绕$y$轴旋转的体积公式为：
$$V_y = 2\pi \int_a^b x f(x)dx$$
经坐标系旋转变换后，原问题绕$x$轴旋转的体积为：
$$V_x = 2\pi \int_{\frac{1}{2}}^{\frac{\sqrt{3}}{2}} y f^{-1}(y) dy$$
代入反函数表达式得：
$$V_x = 2\pi \int_{\frac{1}{2}}^{\frac{\sqrt{3}}{2}} y\cdot \frac{y}{\sqrt{1-y^2}} dy$$

---

# M 积分的应用_第11页.png

$$=2\pi\int_{\frac{1}{2}}^{\frac{\sqrt{3}}{2}} \frac{y^2}{\sqrt{1-y^2}} dy \quad \text{三角代换.}$$
令$y=\sin t$，
换限：
- 当$y=\frac{1}{2}$时，$\sin t=\frac{1}{2}$，得$t=\frac{\pi}{6}$；
- 当$y=\frac{\sqrt{3}}{2}$时，$\sin t=\frac{\sqrt{3}}{2}$，得$t=\frac{\pi}{3}$。

计算微分：
$$dy = d\sin t = \cos t dt$$

化简被积函数：
$$\frac{y^2}{\sqrt{1-y^2}} = \frac{\sin^2 t}{\sqrt{1-\sin^2 t}} = \frac{\sin^2 t}{\cos t}$$

代入换元计算：
$$
\begin{align*}
\text{原式} &= 2\pi\int_{\frac{\pi}{6}}^{\frac{\pi}{3}} \frac{\sin^2 t}{\cos t} \cdot \cos t dt \\
&= 2\pi\int_{\frac{\pi}{6}}^{\frac{\pi}{3}} \sin^2 t dt \\
&= 2\pi\int_{\frac{\pi}{6}}^{\frac{\pi}{3}} \frac{1-\cos 2t}{2} dt
\end{align*}
$$
其中利用三角恒等式$\sin^2 t = \frac{1-\cos 2t}{2}$化简，继续计算定积分：
$$= \frac{\pi^2}{6} - \frac{\pi}{2}\sin2t \bigg|_{\frac{\pi}{6}}^{\frac{\pi}{3}}$$
备注：区间正好为$\sin x$一个周期，一眼为0（代入上下限后$\sin\frac{2\pi}{3}=\sin\frac{\pi}{3}=\frac{\sqrt{3}}{2}$，正弦项差值为0）。

因此积分结果为：
$$=\frac{\pi^2}{6}$$

## 例10.7
过坐标原点，作曲线$y=e^x$的切线，该切线与曲线$y=e^x$以及x轴围成的向x轴负向无限伸展的平面图形记为D。
求：
(1) D的面积$A$
(2) D绕直线$x=1$旋转一周所得旋转体的体积

---

# M 积分的应用_第12页.png

## 分析
（函数示意图：平面直角坐标系$xOy$中绘制指数函数$y=e^x$、过原点的切线$L$，切点标注为$P(x_0,y_0)$）
先求出点$P(x_0,y_0)$与直线$L$，再求面积、体积。

## 解
设$P(x_0,y_0)$。
$\because$ 直线$L$与曲线$y=e^x$共点$P$，
$\therefore y_0 = e^{x_0}$。
$\because$ 直线$L$斜率为$\left.(e^x)'\right|_{x=x_0} = e^{x_0}$，
$\therefore$ 设$L: y-y_0 = e^{x_0}(x-x_0)$。
$\because y_0 = e^{x_0}$，且直线$L$过原点$(0,0)$，即$y(0)=0$，
代入得：
$$0 - e^{x_0} = e^{x_0}(-x_0) \implies x_0=1$$

$\therefore y_0 = e^{x_0} = e$，
切线$L$的方程：
$$y-e = e(x-1)$$
化简得：
$$y=ex$$
即切点为$P(1,e)$。

## (1) 分析
$\because$ 算面积时，$(-\infty,0]$与$[0,1]$区间上的面积因所围函数不同，要分开算，很麻烦。
$\therefore$ 将图像转$90^\circ$后，将$x$轴当$y$轴，$y$轴当$x$轴，取反函数也可计算，且不用分开算。

---

# M 积分的应用_第13页.png

解：
（函数示意图：平面直角坐标系，纵轴为$x$轴，横轴为$y$轴，绘制曲线$y=e^x$、直线$L:y=ex$，标注原点$O$及$y=e$处的两曲线交点）

$L$的反函数：$x=\frac{y}{e}$
$y=e^x$的反函数：$x=\ln y$
其中$y\in(0,+\infty)$

则平面图形面积为：
$$A = \int_{0}^{e} \left( \frac{y}{e} - \ln y \right) dy$$

计算不定积分：
$$\int \frac{y}{e} dy = \frac{1}{e} \cdot \frac{y^2}{2} + C$$
$$
\begin{align*}
\int \ln y dy &= y\ln y - \int y\cdot \frac{1}{y} dy \\
&= y\ln y - y + C
\end{align*}
$$

代入定积分计算：
$$A = \left. \frac{1}{e}\cdot \frac{y^2}{2} \right|_{0}^{e} - \left. (y\ln y - y) \right|_{0}^{e}$$
注：$y$无法取到$0$，下限通过极限$\lim\limits_{y\to 0^+} x(y)$计算。

计算得：
$$
\begin{align*}
A&= \frac{e}{2} - (0 - 0) \\
&= \frac{e}{2}
\end{align*}
$$

## (2) 旋转体体积计算
### 分析
所求体积为$y=e^x$绕$x=1$旋转所得旋转体体积，减去$y=ex$绕$x=1$旋转所得旋转体体积。

解：
$\because$ 旋转轴$L_0: x=1$
$\therefore$ 将其写为直线一般式$Ax+By+C=0$，对应系数为：
$$
\begin{cases}
A=1 \\
B=0 \\
C=-1
\end{cases}
$$
其中边界曲线为$L_1: y=e^x$，$L_2: y=ex$。

平面曲线$y=f(x)$绕直线$Ax+By+C=0$旋转的旋转体体积公式为：
$$V = \frac{\pi}{(A^2+B^2)^{\frac{3}{2}}} \int_{a}^{b} \left[ Ax+Bf(x)+C \right]^2 \left| Af'(x)-B \right| dx$$

---

# M 积分的应用_第14页.png

$$V_1 = \pi \int_{-\infty}^{1} (x-1)^2 e^x dx$$
$$V_2 = \pi \int_{0}^{1} (x-1)^2 e \, dx$$
$$
\begin{align*}
V &= V_1 - V_2 \\
&= \frac{5\pi}{3}e
\end{align*}
$$

## 3. 用定积分表达和计算函数的平均值
“理解去积分中值定理那里”
设$x\in[a,b]$，函数$y=f(x)$在$[a,b]$上的平均值为
$$\bar{y} = \frac{1}{b-a}\int_{a}^{b} f(x) dx$$

## 例10.9 “定积分周期性结论的升华”
设$f(x)$连续，且$f(x+2)-f(x)=x$，$\int_{0}^{2} f(x) dx = 0$，求$f(x)$在$x\in[1,3]$上的平均值。

分析：由公式得
$$
\begin{align*}
\bar{y} &= \frac{1}{3-1}\int_{1}^{3} f(x) dx \\
&= \frac{1}{2}\int_{1}^{3} f(x) dx
\end{align*}
$$
看到$\int_{0}^{2} f(x) dx = 0$，让你求$\int_{1}^{3} f(x) dx$，很容易联想到周期函数性质。

---

# M 积分的应用_第15页.png

## 变限积分求导公式应用
$$\int_{a}^{a+T} f(t)dt = \int_{0}^{T} f(t)dt$$
由$\int_{0}^{2} f(t)dt$求出$\int_{1}^{3} f(t)dt$
但，这一题显然不是周期函数
但，我们可以在此性质上升华
设出$F(x) = \int_{x}^{x+2} f(t)dt$，且
已知，当$x=0$时，$F(0)=0$
我们要求的是$F(1)$
求$F(x)$要有逆推意识
看到$f(x+2)-f(x)$，要联想到变限积分求导公式：
$$\left( \int_{\alpha(x)}^{\beta(x)} f(t)dt \right)' = f\left(\beta(x)\right)\beta'(x) - f\left(\alpha(x)\right)\alpha'(x)$$
即
$$F'(x) = \frac{d}{dx}\left[ \int_{\alpha(x)}^{\beta(x)} f(t)dt \right]$$
$$= f\left(\beta(x)\right)\beta'(x) - f\left(\alpha(x)\right)\alpha'(x)$$
因此可得
$$
\begin{align*}
F'(x) &= \frac{d}{dx}\left[ \int_{x}^{x+2} f(t)dt \right] \\
&= f(x+2) - f(x) \\
&= x
\end{align*}
$$
则$\Rightarrow F(x) = \frac{x^2}{2} + C$
$\because F(0)=0$
$\therefore \Rightarrow C=0$
即$F(x) = \frac{x^2}{2}$
此题已可解

---

# M 积分的应用_第16页.png

## 函数在区间上的平均值计算（变限积分求导应用）
解：
$$
\bar{y} = \frac{1}{3-1}\int_{1}^{3} f(x) dx = \frac{1}{2}\int_{1}^{3} f(x) dx
$$
设
$$
F(x) = \int_{x}^{x+2} f(t) dt
$$
则
$$
F(0) = \int_{0}^{2} f(t) dt = 0
$$
$$
\begin{aligned}
\because f(x+2)-f(x)
&= \left( \int_{x}^{x+2} f(t) dt \right)' \\
&= F'(x) \\
&= x
\end{aligned}
$$
$$
\therefore F(x) = \int x \, dx = \frac{x^2}{2} + C
$$
$\because F(0) = 0$
$$
\therefore C=0,\ F(x) = \frac{x^2}{2}
$$
$$
\because F(1) = \int_{1}^{3} f(x) dx
$$
$$
\begin{aligned}
\therefore \bar{y} &= \frac{1}{2} \cdot F(1) \\
&= \frac{1}{4}
\end{aligned}
$$