---

# R 多元函数积分的计算_第1页.png

## 二重积分的计算
## 前言（直角坐标系）
在直角坐标系计算$\iint\limits_D f(x,y)\,d\sigma$时，可以变为累次积分：
$$\int_{a}^{b}\int_{\varphi_1(x)}^{\varphi_2(x)} f(x,y)\,dydx$$
或
$$\int_{c}^{d}\int_{\varphi_1(y)}^{\varphi_2(y)} f(x,y)\,dxdy$$
即累次积分。
二重积分的几何意义是求曲顶柱体体积，计算逻辑可通过切片法理解：
我们先把柱体切成一片一片的，每一片的厚度为$dx/dy$：
1.  求出每一片的横截面面积——（第一次积分）
2.  再把这些一片片的体积求出并累加——（第二次积分）
即可求出总体积。
且每次积分的计算规则都与一维定积分一致。
以下将以先积$x$后积$y$的顺序为例，即以累次积分
$$\int_{a}^{b}\int_{\varphi_1(y)}^{\varphi_2(y)} f(x,y)\,dxdy$$
为例进行说明：
### 细说
在$f(x,y)$的图像中，在$y=y_0$处，平行于$x$轴方向插一个截面，这个截面上对应的是一个一元函数。
（函数截面示意图：xOz平面直角坐标系，横轴为$x$轴，纵轴标注$z=f(x,y)$，原点为$O$；截面曲线与$x$轴交于$x=\varphi_1(y_0)$和$x=\varphi_2(y_0)$，两点间曲线与$x$轴围成的阴影区域为该位置的截面。）

---

# R 多元函数积分的计算_第2页.png

## Y型区域二重积分累次积分公式推导
则 $\int_{\varphi_1(y)}^{\varphi_2(y)} f(x,y)dx$ 为这一截面的面积
拿来无数个这样的截面
则，可以在所有$y$点处
平行于$x$轴方向插截面
则可以将曲顶柱体分成无数个
厚度为$dy$且平行于$x$轴的薄片
并以同样的方式算出
所有$y$点处薄片截面的面积
则可以得出一个自变量为$y$
因变量为薄片截面面积的函数
设这个函数为$A(y)$
$$A(y)=\int_{\varphi_1(y)}^{\varphi_2(y)} f(x,y)dx$$
发现，面积 $\int_{\varphi_1(y)}^{\varphi_2(y)} f(x,y)dx$ 乘厚度$dy$
即 $A(y)dy = \int_{\varphi_1(y)}^{\varphi_2(y)} f(x,y)dxdy$
正好为每一个薄片的体积
我们将这些薄片体积累加
得总体积：
$$\int_{a}^{b}\int_{\varphi_1(y)}^{\varphi_2(y)} f(x,y)dxdy,\quad y\in[a,b]$$
则，就成功推出
$$\iint_D f(x,y)d\sigma = \int_{a}^{b}\int_{\varphi_1(y)}^{\varphi_2(y)} f(x,y)dxdy$$
其中积分区域$D$为：
$$D=\begin{cases}
a\leq y\leq b \\
\varphi_1(y)\leq x\leq \varphi_2(y)
\end{cases}$$

---

# R 多元函数积分的计算_第3页.png

## 在直角坐标系下的计算方法
一般，积分区域$D$可以化为以下两种类型：
1.  **Y型区域**
    $$
    \begin{cases}
    a\leq y\leq b\\
    \varphi_1(y)\leq x\leq \varphi_2(y)
    \end{cases}
    $$
    （Y型积分区域$D$示意图）
    该类型为先对$x$积分、后对$y$积分，称为Y型，对应的累次积分公式为：
    $$
    \iint\limits_D f(x,y)\mathrm{d}\sigma = \int_a^b \int_{\varphi_1(y)}^{\varphi_2(y)} f(x,y)\mathrm{d}x\mathrm{d}y
    $$

2.  **X型区域**
    $$
    \begin{cases}
    a\leq x\leq b\\
    \varphi_1(x)\leq y\leq \varphi_2(x)
    \end{cases}
    $$
    （X型积分区域$D$示意图）
    该类型为先对$y$积分、后对$x$积分，称为X型，对应的累次积分公式为：
    $$
    \iint\limits_D f(x,y)\mathrm{d}\sigma = \int_a^b \int_{\varphi_1(x)}^{\varphi_2(x)} f(x,y)\mathrm{d}y\mathrm{d}x
    $$

## 注
- 与一重积分类似，积分累加方向为：竖直方向下$\to$上，水平方向左$\to$右。
- 定限规则：积分上限需大于等于下限，即上限$\geq$下限。
- 若出现上限$<$下限的情况，需要添加负号翻转上下限，得到符合定义的二重积分后再进行计算。

### 简算过程口诀
1.  后积先定限
2.  限内画条线（穿线方向：$\begin{cases}下\to上\\左\to右\end{cases}$）
3.  先交写下限
4.  后交写上限

---

# R 多元函数积分的计算_第4页.png

## 二重积分积分次序选择原则
- 若被积函数$f(x,y)$易于对$y$积分，或积分区域$D$为X型区域，则选择先对$y$积分、后对$x$积分的次序
- 若被积函数$f(x,y)$易于对$x$积分，或积分区域$D$为Y型区域，则选择先对$x$积分、后对$y$积分的次序

## 二重积分积分限确定要点
计算二重积分的关键是确定积分限：
1.  优先画出积分区域$D$的形状辅助判断
2.  若无法直接画出区域图形，则通过分析推导$D$关于$x,y$的不等式表示，进而确定积分上下限
3.  确定的积分限需要尽量简化积分运算，降低计算难度

## 例题：分段Y型区域的二重积分
（示意图：平面直角坐标系$xOy$中，积分区域为8字形连通区域，$y$轴标注刻度$a<c<b$，$y\in[c,b]$段区域右边界为$\varphi_1(y)$，$y\in[a,c]$段区域右边界为$\varphi_2(y)$，两曲线交于$y=c$处）

该区域无法用单一Y型不等式表示，需拆分为两部分：
$$
\begin{cases}
c\leq y\leq b \\
\varphi_2(y)\leq x\leq \varphi_1(y)
\end{cases}
$$
和
$$
\begin{cases}
a\leq y\leq c \\
\varphi_1(y)\leq x\leq \varphi_2(y)
\end{cases}
$$

对应二重积分化为分段累次积分：
$$
\iint_D f(x,y)d\sigma = \int_c^b \int_{\varphi_2(y)}^{\varphi_1(y)} f(x,y)dxdy + \int_a^c \int_{\varphi_1(y)}^{\varphi_2(y)} f(x,y)dxdy
$$

---

# R 多元函数积分的计算_第5页.png

## 例2
函数示意图：平面直角坐标系$xOy$，原点为$O$，$x$轴上从左到右依次标记点$a,c,b$；曲线$y=\varphi_1(x)$与$y=\varphi_2(x)$交于$x=c$处：在区间$[a,c]$上$\varphi_1(x)$位于$\varphi_2(x)$上方，在区间$[c,b]$上$\varphi_2(x)$位于$\varphi_1(x)$上方，两曲线与竖线$x=a,x=b$围成封闭积分区域$D$。
$D$可以表示为
$$\begin{cases} a\leq x\leq c \\ \varphi_2(x)\leq y\leq \varphi_1(x) \end{cases}$$
和
$$\begin{cases} c\leq x\leq b \\ \varphi_1(x)\leq y\leq \varphi_2(x) \end{cases}$$
$$\iint_D f(x,y)\,d\sigma = \int_a^c \int_{\varphi_2(x)}^{\varphi_1(x)} f(x,y)\,dy\,dx + \int_c^b \int_{\varphi_1(x)}^{\varphi_2(x)} f(x,y)\,dy\,dx$$
## 例14.6
当$x\to0^+$时，$f(x)=\int_{0}^{x^2} dy \int_{x}^{\sqrt{y}} \sin\frac{y}{t}\,dt$与$g(x)=ax^b$是等价无穷小量，求$ab$。
### 分析
我们之前说的二重积分是
$$\int_{0}^{x^2} dy \int_{x}^{\sqrt{y}} \sin\frac{y}{t}\,dt \quad \left( \begin{aligned} 先积t \\ 后积y \end{aligned} \right)$$
这里分出了变限积分（与一重一样）。
$$f(x)=\int_{0}^{x^2} dy \int_{x}^{\sqrt{y}} \sin\frac{y}{t}\,dt$$
$x\to0^+ \implies x>0$
则$x$是一个正数
$\implies y=x^2 \geq y=0$
$t=x$与$t=\sqrt{y}$谁大？

---

# R 多元函数积分的计算_第6页.png

## 交换积分次序计算累次积分
$t=\sqrt{y}$
$\Rightarrow y = t^2$
先交$t=\sqrt{y}$
后交$t=x$ $\Rightarrow$ $t=x \geq t=\sqrt{y}$
（附积分区域示意图：t为横轴、y为纵轴，曲线$y=t^2$与坐标轴、直线$t=x$围成阴影积分区域）

应调整为：
$$-\int_{0}^{x^2} dy \int_{\sqrt{y}}^{x} \sin\frac{y}{t} dt$$

$$\int_{0}^{x^2} dy \int_{\sqrt{y}}^{x} \sin\frac{y}{t} dt \quad \begin{cases} 0\leq y\leq x^2 \\ \sqrt{y}\leq t\leq x \end{cases}$$
才是实际的二重积分表达。

$\int \sin\frac{1}{x} dx$ 可积，
但，其原函数没有初等函数形式的表达。

之后，我们会讲，如何转为二重积分去解。
这里，我们不解。
交换积分次序，绕过去，
变成先积$y$后积$t$。

要先积$y$后积$t$，
后积先定限（先定$t$的限）：
$0\leq t\leq x$
再在限内画条线（定$y$的限）：
$0\leq y\leq t^2$
（附积分区域示意图：同上述t-y坐标系下的阴影积分区域）

$$\Rightarrow -\int_{0}^{x} dt \int_{0}^{t^2} \sin\frac{y}{t} dy \quad D\begin{cases}0\leq t\leq x \\ 0\leq y\leq t^2 \end{cases}$$

然后就是解两个一重积分。

---

# R 多元函数积分的计算_第7页.png

$$\int \sin\frac{y}{t} dy$$
$$= t\int \sin\frac{y}{t} \cdot \frac{1}{t} dy$$
$$= t\int \sin\frac{y}{t} \, d\left(\frac{y}{t}\right)$$
$$= -t\cos\frac{y}{t}$$

$$\int_0^{t^2} \sin\frac{y}{t} dy = -t(\cos t - 1)$$

解：
$$
\begin{align*}
\text{原式} &= -\int_0^{x^2} dy \int_{\sqrt{y}}^x \sin\frac{y}{t} dt \\
&= -\int_0^x dt \int_0^{t^2} \sin\frac{y}{t} dy \\
&= \int_0^x t(\cos t -1) dt
\end{align*}
$$

$$\lim_{x \to 0^+} \frac{f(x)}{g(x)} = 1$$
$$= \lim_{x \to 0^+} \frac{\int_0^x t(\cos t -1)dt}{a x^b} = 1$$
$$\overset{\text{洛}}{=} \lim_{x \to 0^+} \frac{x(\cos x -1)}{ab x^{b-1}} = 1$$
利用等价无穷小$\cos x -1 \sim -\frac{1}{2}x^2 \ (x\to0)$，得：
$$= \lim_{x \to 0^+} \frac{-\frac{1}{2}x^3}{ab x^{b-1}} = 1$$
$$
\Rightarrow \begin{cases}
ab = -\frac{1}{2} \\
b-1 = 3
\end{cases}
\Rightarrow \begin{cases}
a = -\frac{1}{8} \\
b = 4
\end{cases}
$$

## 例147
计算：
$$\int_0^1 dy \int_y^1 \arcsin\sqrt{4x-4x^2} dx$$

---

# R 多元函数积分的计算_第8页.png

## 分析
∵ 交换积分次序可得：
$$\int_{0}^{x} \arcsin\sqrt{4x-4x^2} \, dy$$
计算时将$x$看作常数，计算很简单：
$$= x\arcsin\sqrt{4x-4x^2}$$
∴ 先交换积分次序。
积分区域不同积分次序的范围：
- 先对$x$积分，后对$y$积分：$\begin{cases} 0\leq y\leq 1 \\ y\leq x\leq 1 \end{cases}$，附对应积分区域穿线示意图。
- 先对$y$积分，后对$x$积分：附对应积分区域穿线示意图。

后积先定限 $\Rightarrow 0\leq x\leq 1$
限内画条线 $\Rightarrow 0\leq y\leq x$
因此交换次序后的累次积分为：
$$\int_{0}^{1} dx \int_{0}^{x} \arcsin\sqrt{4x-4x^2} \, dy$$
计算内层对$y$的积分，可得：
$$= \int_{0}^{1} x\arcsin\sqrt{4x-4x^2} \, dx$$
最后求解该一重积分即可，在例9.15中已算过该积分，结果为$\frac{1}{2}$。

## 解答
$$
\begin{aligned}
\text{原式} &= \int_{0}^{1} dx \int_{0}^{x} \arcsin\sqrt{4x-4x^2} \, dy \\
&= \int_{0}^{1} x\arcsin\sqrt{4x-4x^2} \, dx \\
&= \frac{1}{2}
\end{aligned}
$$
见例9.15。

---

# R 多元函数积分的计算_第9页.png

## 前言（极坐标系）
若$\displaystyle\iint\limits_D f(x,y)\,d\sigma$的积分区域$D$可以表示为
$$D_0\begin{cases}
\alpha \leq \theta \leq \beta \\
r_1(\theta) \leq r \leq r_2(\theta)
\end{cases}$$

从极点$O$出发，作无数条射线，可以将满足
$$D\begin{cases}
\alpha \leq \theta \leq \beta \\
0 \leq r \leq r_2(\theta)
\end{cases}$$
的区域分割为无数个圆心角为$d\theta$、弧长近似为直线的小扇形。

分割得到的单个窄小扇形区域记为$D_1$，满足
$$D_1\begin{cases}
\alpha \leq \theta \leq \alpha+d\theta \\
0 \leq r \leq r_2(\alpha)
\end{cases}$$

再以极点为中心，作无数个同心圆，可以将满足
$$\begin{cases}
\alpha \leq \theta \leq \beta \\
r_1(\theta) \leq r \leq r_2(\theta)
\end{cases}$$
的区域分割为无数个近似矩形的小块。

---

# R 多元函数积分的计算_第10页.png

## 极坐标下二重积分的微元推导
（极坐标面积微元示意图）
取微元区域：
$$D_2\begin{cases}
\alpha\leq\theta\leq\alpha+d\theta\\
r_1(\alpha)\leq r\leq r_1(\alpha)+dr
\end{cases}$$

$\because d\theta\to0,\ dr\to0$
$\therefore$
$$l_1\to l_2$$
$$r_1(\alpha)\to r_1(\alpha)+dr$$
$$r_1(\alpha)\to r_1(\alpha+d\theta)=r$$

$\therefore l = r\theta = r d\theta$

面积近似为矩形面积：
$$
\begin{aligned}
dr\cdot l &= dr\cdot r d\theta\\
&= r\,dr\,d\theta
\end{aligned}
$$

则这一小块面积乘$f(r,\theta)$为其对应的体积：
$$f(r,\theta)\cdot r\,dr\,d\theta \quad (\text{为}D_2\text{对应的体积})$$

将这个小体积由$r_1(\alpha)$累加到$r_2(\alpha)$，可以得出区域
$$\begin{cases}
\alpha\leq\theta\leq\alpha+d\theta\\
r_1(\alpha)\leq r\leq r_2(\alpha)
\end{cases}$$
的体积为
$$\int_{r_1(\alpha)}^{r_2(\alpha)} f(r,\theta)\cdot r \,dr\,d\theta$$

若是从$r=0$累加到$r_2(\alpha)$，则体积为
$$\int_{0}^{r_2(\alpha)} f(r,\theta)\cdot r \,dr\,d\theta$$
对应区域
$$D_1\begin{cases}
\alpha\leq\theta\leq\alpha+d\theta\\
0\leq r\leq r_2(\alpha)
\end{cases}$$
（极点在$D_1$边上）

以同样的方法，可以求出所有极角$\theta$在$[\theta,\theta+d\theta]$之间区域的体积，记为$A(\theta)$。

---

# R 多元函数积分的计算_第11页.png

## 极坐标系下的计算方法
极角$\theta$处的角度微元对应的径向积分（极点在$D$外）：
$$A(\theta) = \int_{r_1(\theta)}^{r_2(\theta)} f(r,\theta) \cdot r \, dr d\theta$$
对应的微元区域$D$满足：
$$D\begin{cases}
\theta \leq \theta \leq \theta+d\theta \\
r_1(\theta) \leq r \leq r_2(\theta)
\end{cases}$$

特殊的有（极点在$D$上的情况）：
$$A(\theta) = \int_{0}^{r_2(\theta)} f(r,\theta) \cdot r \, dr d\theta$$
对应的微元区域$D_1$满足：
$$D_1\begin{cases}
\theta \leq \theta \leq \theta+d\theta \\
0 \leq r \leq r_2(\theta)
\end{cases}$$

将这些小体积由$\theta=\alpha$累加到$\theta=\beta$，可得出区域$D_0$上的体积，其中$D_0$满足：
$$D_0\begin{cases}
\alpha \leq \theta \leq \beta \\
r_1(\theta) \leq r \leq r_2(\theta)
\end{cases}$$
对应的二重累次积分为：
$$\int_{\alpha}^{\beta} \int_{r_1(\theta)}^{r_2(\theta)} f(r,\theta) \cdot r \, dr d\theta$$

特殊的有（围着极点$O$累加了一圈，即极点在$D$内部）：
$$\int_{0}^{2\pi} \int_{r_1(\theta)}^{r_2(\theta)} f(r,\theta) \cdot r \, dr d\theta$$
对应的区域$D$满足：
$$D\begin{cases}
0 \leq \theta \leq 2\pi \\
r_1(\theta) \leq r \leq r_2(\theta)
\end{cases}$$

## 与直角坐标系的联系
- 极坐标点示意图：标注极点$O$、极轴$\theta=0$、极坐标点$P(r,\theta)$、极径曲线$r=r(\theta)$。
- 直角坐标与极坐标对应示意图：标注平面直角坐标系$xOy$、原点$O$，点的横坐标分量$r\cos\theta$、纵坐标分量$r\sin\theta$、极径$r$、极角$\theta$。

极坐标转直角坐标公式：
$$\begin{cases}
x = r\cos\theta \\
y = r\sin\theta
\end{cases}$$

直角坐标下的极坐标关系式：
$$\begin{cases}
x^2 + y^2 = r^2 \\
\frac{y}{x} = \tan\theta \\
\frac{x}{y} = \cot\theta
\end{cases}$$

---

# R 多元函数积分的计算_第12页.png

## 计算方法
若是从直角坐标系转向极坐标系，则坐标变换为：
$$
\begin{cases}
x = r\cos\theta \\
y = r\sin\theta
\end{cases}
$$
一般积分区域$D$可化为以下四类极坐标形式：
①
$$
\begin{cases}
\alpha \leq \theta \leq \beta \\
r_1(\theta) \leq r \leq r_2(\theta)
\end{cases}
$$
（对应示意图：极点在积分区域外的极坐标扇形环域）
区域体积：
$$
\int_{\alpha}^{\beta} \int_{r_1(\theta)}^{r_2(\theta)} f(r\cos\theta, r\sin\theta) r \, dr d\theta
$$

②
$$
\begin{cases}
\alpha \leq \theta \leq \beta \\
0 \leq r \leq r(\theta)
\end{cases}
$$
（对应示意图：极点在积分区域边界上的极坐标曲边扇形域）
区域体积：
$$
\int_{\alpha}^{\beta} \int_{0}^{r(\theta)} f(r\cos\theta, r\sin\theta) r \, dr d\theta
$$

③
$$
\begin{cases}
0 \leq \theta \leq 2\pi \\
r_1(\theta) \leq r \leq r_2(\theta)
\end{cases}
$$
（对应示意图：极点在区域内空心外侧的极坐标环形域）
区域体积：
$$
\int_{0}^{2\pi} \int_{r_1(\theta)}^{r_2(\theta)} f(r\cos\theta, r\sin\theta) r \, dr d\theta
$$

④
$$
\begin{cases}
0 \leq \theta \leq 2\pi \\
0 \leq r \leq r(\theta)
\end{cases}
$$
（对应示意图：极点在积分区域内部的极坐标实心域）
区域体积：
$$
\int_{0}^{2\pi} \int_{0}^{r(\theta)} f(r\cos\theta, r\sin\theta) r \, dr d\theta
$$

---

# R 多元函数积分的计算_第13页.png

## 注
极坐标系，一般用于解决：
1.  $D$为中心对称图形的情况
2.  $f(x,y)$中含有$x^2+y^2$的情况
    可以利用$x^2+y^2=r^2$
3.  $f(x,y)$中含有$\frac{y}{x}$或$\frac{x}{y}$的情况
    可以利用$\frac{y}{x}=\tan\theta$，$\frac{x}{y}=\cot\theta$

累次积分并不是两个一重积分相乘的形式，本质是内层积分与外层积分嵌套的形式。
二重积分化为两个一重积分乘积的形式要满足以下条件（极坐标系也同样，只是将$x,y$换成$r,\theta$）：

## 函数变量可分离
$$f(x,y) = g(x)\cdot h(y)$$
$g(x)$仅为$x$的函数
$h(y)$仅为$y$的函数
两者互不依赖

## 积分区域独立
$x$的积分限$[a,b]$与
$y$的积分限$[c,d]$
相互独立，
两者互不依赖

---

# R 多元函数积分的计算_第14页.png

## 理解
累次积分原定义是先积内层，后积外层。
如果对内层积分的时候，对外层积分无关；对外层积分的时候，对内层积分无关的话，则对积分次序也就无要求了，二重积分也就表示为两个一重积分乘积的形式。

## 条件的总结
函数变量可分离就是：
关于$x$的函数不含$y$，
关于$y$的函数不含$x$。

积分区域独立也就是：
$x$的积分限不含$y$，
$y$的积分限不含$x$。

$$
\begin{aligned}
eg_1:\ &\frac{3}{4}\int_{0}^{2\pi} \mathrm{d}\theta \int_{0}^{4\sqrt{2}} (x^2+y^2) r\mathrm{d}r \\
&= \frac{3}{4}\int_{0}^{2\pi} \mathrm{d}\theta \int_{0}^{4\sqrt{2}} r^2 \cdot r\mathrm{d}r \\
&= \frac{3}{4} \cdot 2\pi \int_{0}^{4\sqrt{2}} r^3 \mathrm{d}r
\end{aligned}
$$

$$
eg_2:\ f(x) = \iint_{D(x)} \ln(u^2+v^2) \mathrm{d}u\mathrm{d}v
$$
注：极坐标下$f(r,\theta) = 1\cdot g(r)$；积分过程中$0,\frac{\pi}{2},\frac{1}{2},x$相对于积分变量$r,\theta$为常量，其中$x$是与$r,\theta$无关的独立参数。
$$
\begin{aligned}
&= \int_{0}^{\frac{\pi}{2}} \int_{\frac{1}{2}}^{x} \ln r^2 \cdot r \mathrm{d}r\mathrm{d}\theta \\
&= 2\int_{0}^{\frac{\pi}{2}} \int_{\frac{1}{2}}^{x} \ln r \cdot r \mathrm{d}r\mathrm{d}\theta \\
&= 2\int_{0}^{\frac{\pi}{2}} \mathrm{d}\theta \int_{\frac{1}{2}}^{x} \ln r \cdot r \mathrm{d}r \\
&= \pi \int_{\frac{1}{2}}^{x} \ln r \cdot r \mathrm{d}r
\end{aligned}
$$

---

# R 多元函数积分的计算_第15页.png

## 例148
设区域$D=\left\{(x,y)\mid x^2+y^2\leqslant\sqrt{2}\right\}$，求$\iint\limits_D \left(x^2+\frac{y^2}{2}\right)dxdy$。

### 分析
发现被积函数与积分区域中含有$x^2+y^2$，可考虑转换为极坐标系，利用关系$x^2+y^2=r^2$计算。
观察区域$D=\left\{(x,y)\mid x^2+y^2\leqslant\sqrt{2}\right\}$：
- 该区域是中心对称型区域；
- 区域$D$中$x$与$y$互换位置后区域不变，即$D$关于直线$y=x$对称，因此可考虑利用轮换对称性简化计算。
（直角坐标系积分区域示意图：圆心在原点、半径为$\sqrt[4]{2}$的圆，标注x轴、y轴，圆与坐标轴的交点标注为$\sqrt[4]{2}$）

### 解答
根据轮换对称性，有：
$$\iint\limits_D \left(x^2+\frac{y^2}{2}\right)dxdy = \iint\limits_D \left(y^2+\frac{x^2}{2}\right)dydx$$
因此对原式做化简：
$$
\begin{align*}
\iint\limits_D \left(x^2+\frac{y^2}{2}\right)dxdy
&= \frac{1}{2}\iint\limits_D \left[\left(x^2+\frac{y^2}{2}\right)+\left(y^2+\frac{x^2}{2}\right)\right]d\sigma \\
&= \frac{1}{2}\cdot\frac{3}{2}\iint\limits_D (x^2+y^2)d\sigma
\end{align*}
$$
再转换为极坐标系，利用极坐标关系$x^2+y^2=r^2$确定积分限：
- 后积先定限：极角范围$0\leqslant\theta\leqslant2\pi$，区域半径$r=\sqrt[4]{2}$；
（极坐标系积分区域示意图：圆心在极点、半径为$\sqrt[4]{2}$的阴影圆，标注极轴$\theta=0$方向）
- 限内画条线：从极点向外作射线，得极径范围$0\leqslant r\leqslant\sqrt[4]{2}$。

代入极坐标面积元素$d\sigma=rdrd\theta$，得累次积分：
$$\frac{3}{4}\int_{0}^{2\pi}d\theta\int_{0}^{\sqrt[4]{2}} (x^2+y^2) r dr$$
（替换提示：$x^2+y^2=r^2$）

---

# R 多元函数积分的计算_第16页.png

$$= \frac{3}{4} \cdot 2\pi \cdot \int_{0}^{\sqrt[4]{2}} r^3 dr$$
$$\int r^3 dr = \frac{r^4}{4}$$
$$\Rightarrow \int_{0}^{\sqrt[4]{2}} r^3 dr = \frac{1}{2}$$

解：
$$
\begin{aligned}
\text{原式} &= \frac{1}{2}\iint_D \left[ \left(x^2+\frac{y^2}{2}\right) + \left(y^2+\frac{x^2}{2}\right) \right] d\sigma \\
&= \frac{3}{4}\iint_D (x^2+y^2) d\sigma \\
&= \frac{3}{4}\int_{0}^{2\pi} d\theta \int_{0}^{\sqrt[4]{2}} (x^2+y^2) r dr \\
&= \frac{3}{4} \cdot 2\pi \cdot \int_{0}^{\sqrt[4]{2}} r^3 dr \\
&= \frac{3}{4} \cdot 2\pi \cdot \frac{1}{2} \\
&= \frac{3}{4}\pi
\end{aligned}
$$

## 例14.10
设$f(x) = \iint_{D(x)} \frac{v\ln\sqrt{u^2+v^2}}{u+v} dudv$，其中积分区域
$$D(x) = \left\{ (u,v) \mid \frac{1}{4} \leq u^2+v^2 \leq x^2,\ u>0,\ v>0 \right\}$$
求曲线$y(x) = \int_{1}^{x} f(t) dt\ (x>0)$的拐点。

### 分析
由14.4得：
$$
\begin{aligned}
f(x) &= \frac{1}{2}\iint_{D(x)} \ln\sqrt{u^2+v^2}\ dudv \\
&= \frac{1}{4}\iint_{D(x)} \ln(u^2+v^2) dudv
\end{aligned}
$$
被积函数中出现$u^2+v^2$，考虑用极坐标系。

---

# R 多元函数积分的计算_第17页.png

## 二重积分与变上限积分的拐点求解
∵ $u>0$，$v>0$
∴ 积分区域$D$在第一象限
（示意图：第一象限内的四分之一圆环积分区域，横轴为$u$轴，纵轴为$v$轴，内半径为$\frac{1}{2}$，外半径为$x$，阴影部分为积分区域）
∵ $u^2+v^2=r^2$
∴ 极径范围为$\frac{1}{2}\leq r\leq x$
将$D$化为极坐标系：
$$D=\begin{cases}
0\leq \theta \leq \frac{\pi}{2} \\
\frac{1}{2}\leq r \leq x
\end{cases}$$
其中直角坐标与极坐标满足关系$u^2+v^2=r^2$。

将二重积分转换为极坐标下的累次积分：
$$\text{原式}=\frac{1}{4}\int_{0}^{\frac{\pi}{2}}\int_{\frac{1}{2}}^{x} \ln r^2 \cdot r \, dr d\theta$$

发现题目要求的是$y(x)=\int_{1}^{x} f(t)dt$（$x>\frac{1}{2}$）的拐点，需要求解$y''(x)$。根据变上限积分求导法则：
$$y'(x)=f(x)\cdot x' - f(1)\cdot 1' = f(x)$$
因此$y''(x)=f'(x)$。

---

$$y''(x)=f'(x)$$
$f(x)$就是原式，我们可以直接对原式求导。

利用对数性质$\ln r^2=2\ln r$化简被积函数：
$$
\begin{align*}
\text{原式}&=\frac{1}{2}\int_{0}^{\frac{\pi}{2}}\int_{\frac{1}{2}}^{x} r\ln r \, dr d\theta \\
&=\frac{\pi}{4}\int_{\frac{1}{2}}^{x} r\ln r \, dr
\end{align*}
$$

对$x$求导得到二阶导数：
$$
\begin{align*}
y''(x)&=f'(x) \\
&=\frac{d}{dx}\left[ \frac{\pi}{4}\int_{\frac{1}{2}}^{x} r\ln r \, dr \right] \\
&=\frac{\pi}{4} x\ln x
\end{align*}
$$

最后根据二阶导数的符号变化求出拐点。

---

# R 多元函数积分的计算_第18页.png

解：由例14.4得
$$
f(x) = \frac{1}{2}\iint_{D(x)} \ln\sqrt{u^2+v^2} \,dudv
$$
$$
= \frac{1}{4}\iint_{D(x)} \ln(u^2+v^2) \,dudv
$$
$$
= \frac{1}{4}\int_{0}^{\frac{\pi}{2}} \int_{1}^{x} \ln r^2 \cdot r \,drd\theta
$$
$$
= \frac{1}{2}\int_{0}^{\frac{\pi}{2}} \int_{1}^{x} r\ln r \,drd\theta
$$
$$
= \frac{\pi}{4}\int_{1}^{x} r\ln r \,dr
$$

$$
y''(x)=f'(x)=\frac{\pi}{4}x\ln x
$$

令$y''(x)=0$
$$
\implies \frac{\pi}{4}x\ln x = 0
$$
解得$x=1$

$\because f(1)=0$

$\therefore$ 拐点为$(1,0)$

## 注
$$
\int \frac{e^x}{x}dx,\quad \int e^{ax^2+bx+c}dx \quad (a\neq0)
$$

$$
\int \frac{\sin x}{x}dx,\quad \int \sin x^2 dx,\quad \int \sin \frac{1}{x}dx
$$

$$
\int \frac{\cos x}{x}dx,\quad \int \cos x^2 dx,\quad \int \cos \frac{1}{x}dx
$$

$$
\int \frac{\tan x}{x}dx,\quad \int \tan x^2 dx
$$

$$
\int \frac{\ln(1+x)}{x}dx,\quad \int \frac{1}{\ln x}dx
$$

均没有初等函数形式的原函数
可考虑转为二重积分去求

---

# R 多元函数积分的计算_第19页.png

## 例14.1
计算 $\int_{0}^{+\infty} e^{-x^2} dx$

## 分析
当内层积分不依赖于外层积分，外层积分不依赖于内层积分时，二重积分可以表示为两个一重积分相乘，则我们可以将两个一重积分的乘积转为二重积分。

以 $\int_{a}^{b} f(x) dx$ 为例，一重积分有一个性质：
定积分的值只与被积函数及积分区间有关，与积分变量的记法无关，改变字母，积分值不变：
$$\int_{a}^{b} f(x) dx = \int_{a}^{b} f(t) dt = I$$

则就得到了两个积分变量不同、积分值相同的积分：
$$
\begin{align*}
I_2 &= \int_{a}^{b} f(x) dx \cdot \int_{a}^{b} f(t) dt \\
&= \iint\limits_D f(x,t) \, dxdt
\end{align*}
$$
且 $f(x,t) = f(x)\cdot f(t)$，积分区域$D$满足：
$$D\begin{cases}
a\leq x\leq b \\
a\leq t\leq b
\end{cases}$$

---

# R 多元函数积分的计算_第20页.png

## 二重积分法计算泊松反常积分
我们也可以将$t$换成$y$：
$$I_2 = \int_a^b f(x)dx \cdot \int_a^b f(y)dy = \iint_D f(x,y)dxdy$$

$\int_0^{+\infty} e^{-x^2}dx$可以这样算：
$\because e^{-(x^2+y^2)} = e^{-x^2}\cdot e^{-y^2}$，函数变量可分离，且积分区域独立，
$$
\therefore \iint_D e^{-(x^2+y^2)}dxdy = \int_0^{+\infty} e^{-x^2}dx \cdot \int_0^{+\infty} e^{-y^2}dy
$$
可算出$\iint_D e^{-(x^2+y^2)}dxdy$，其中积分区域$D$在直角坐标系下为：
$$
D\begin{cases}
0\leq x < +\infty \\
0\leq y < +\infty
\end{cases}
$$

被积函数含$-(x^2+y^2)$，考虑转极坐标系：
$$
D\begin{cases}
0\leq x < +\infty \\
0\leq y < +\infty
\end{cases}
$$
（直角坐标视角第一象限无界积分区域示意图：标注$x,y$坐标轴，$r\to+\infty$）

（极坐标视角第一象限积分区域示意图：标注$\theta=0$、$\theta=\frac{\pi}{2}$、$r\to+\infty$，阴影标识积分范围）
极坐标系下积分区域$D$为：
$$
D\begin{cases}
0\leq \theta \leq \frac{\pi}{2} \\
0\leq r < +\infty
\end{cases}
$$

计算积分：
$$
\begin{align*}
\text{原式} &= \int_0^{\frac{\pi}{2}} d\theta \int_0^{+\infty} e^{-r^2}\cdot r dr \\
&= \frac{1}{2}\int_0^{\frac{\pi}{2}} d\theta \int_0^{+\infty} e^{-r^2} dr^2
\end{align*}
$$

计算原函数：
$$\int e^{-r^2} dr^2 = -e^{-r^2}$$

计算内层反常积分：
$$\int_0^{+\infty} e^{-r^2} dr^2 = \left. -e^{-r^2} \right|_0^{+\infty} = 0 + 1 = 1$$

---

# R 多元函数积分的计算_第21页.png

## 泊松积分（高斯积分）计算
解：设
$$I = \int_{0}^{+\infty} e^{-x^2} dx = \int_{0}^{+\infty} e^{-y^2} dy$$
由指数运算性质：
$$\because e^{-(x^2+y^2)} = e^{-x^2} \cdot e^{-y^2}$$
因此$I^2$可表示为第一象限区域$D: x\geq0, y\geq0$上的二重积分：
$$
\begin{aligned}
I^2 &= \iint_D e^{-(x^2+y^2)} \, dxdy \\
&= \int_{0}^{+\infty} e^{-x^2} dx \cdot \int_{0}^{+\infty} e^{-y^2} dy
\end{aligned}
$$
转换为极坐标计算，由极坐标变换关系$x^2+y^2=r^2$，面积元素$dxdy = r\,dr d\theta$，第一象限对应积分范围$\theta\in[0,\frac{\pi}{2}], r\in[0,+\infty)$，因此：
$$
\begin{aligned}
I^2 &= \int_{0}^{\frac{\pi}{2}} d\theta \int_{0}^{+\infty} e^{-r^2} \cdot r \, dr \\
&= \frac{1}{2}\int_{0}^{\frac{\pi}{2}} d\theta \int_{0}^{+\infty} e^{-r^2} \, dr^2
\end{aligned}
$$
由于$\int_{0}^{+\infty} e^{-r^2} dr^2$是收敛的，且积分结果与$\theta$无关，因此该二重积分可分离为两个一重积分相乘的形式；换元$u=r^2$可得$\int_{0}^{+\infty} e^{-r^2} dr^2 = \int_{0}^{+\infty} e^{-u} du = 1$，因此：
$$
\begin{aligned}
I^2 &= \frac{1}{2} \cdot \int_{0}^{\frac{\pi}{2}} d\theta \cdot \int_{0}^{+\infty} e^{-r^2} dr^2 \\
&= \frac{1}{2} \cdot \frac{\pi}{2} \cdot 1 \\
&= \frac{\pi}{4}
\end{aligned}
$$
根据积分的保号性，被积函数满足$e^{-x^2}>0$，因此：
$$\because e^{-x^2} > 0 \implies I = \int_{0}^{+\infty} e^{-x^2} dx > 0$$
对$I^2$开平方取正根得：
$$
\begin{aligned}
I &= \sqrt{I^2} \\
&= \frac{\sqrt{\pi}}{2}
\end{aligned}
$$

---

# R 多元函数积分的计算_第22页.png

## 注
一个结论
$$\int_{-\infty}^{+\infty} e^{-x^2} \, dx = \sqrt{\pi}$$
### 推导：
由例14.11得
$$\int_{0}^{+\infty} e^{-x^2} \, dx = \frac{\sqrt{\pi}}{2}$$
$\because f(x)=e^{-x^2}$为连续的偶函数
$$
\begin{aligned}
\therefore \int_{-\infty}^{+\infty} e^{-x^2} \, dx &= 2\int_{0}^{+\infty} e^{-x^2} \, dx \\
&= 2\cdot \frac{\sqrt{\pi}}{2} \\
&= \sqrt{\pi}
\end{aligned}
$$

## 极坐标系与直角坐标系的互相转化
- 要用好$\begin{cases} x=r\cos\theta \\ y=r\sin\theta \end{cases}$这个转化关系
- 要画出区域$D$的边界图形，做好上、下限的转化

### 例14.14
求
$$\int_{0}^{1} dx \int_{1-x}^{\sqrt{1-x^2}} \frac{x+y}{x^2+y^2} \, dy$$

#### 分析
发现，交换积分次序也不会变得简单，且含有$x^2+y^2$，则考虑转极坐标系。

---

# R 多元函数积分的计算_第23页.png

## 直角坐标系下绘制积分区域
画出区域$D$：
$$
D:
\begin{cases}
0\leq x\leq 1\\
1-x\leq y\leq \sqrt{1-x^2}
\end{cases}
$$
1.  绘制边界$y=1-x$，即$y=-x+1$，范围为$0\leq x\leq 1$，对应直角坐标系直线段示意图。
2.  绘制边界$y=\sqrt{1-x^2}$：
    两边平方得$y^2=1-x^2$，整理为$x^2+y^2=1$，是半径$r=1$的单位圆，该边界为单位圆在第一象限的圆弧段，对应直角坐标系圆弧示意图。

则可画出完整积分区域$D$：
$$
D:
\begin{cases}
0\leq x\leq 1\\
1-x\leq y\leq \sqrt{1-x^2}
\end{cases}
$$
区域为第一象限内直线$y=1-x$上方、单位圆弧下方的部分，附直角坐标系下积分区域阴影示意图。

## 极坐标系下表示积分区域$D$
极坐标定限遵循口诀：后积先定限，限内画条线，先交写下限，后交写上限。
1.  先确定后积分变量$\theta$的范围：$0\leq\theta\leq\frac{\pi}{2}$。
2.  利用极坐标变换公式：
    $\because x=r\cos\theta,\ y=r\sin\theta$
    代入直线边界$y=-x+1$：
    $$r\sin\theta = -r\cos\theta +1$$
    整理得$r$的下限：
    $$r = \frac{1}{\sin\theta+\cos\theta}$$
3.  射线后交单位圆边界，因此$r$的上限为$r=1$。

最终极坐标系下积分区域$D$为：
$$
D:
\begin{cases}
0\leq\theta\leq\frac{\pi}{2}\\[6pt]
\dfrac{1}{\sin\theta+\cos\theta}\leq r\leq 1
\end{cases}
$$
附极坐标系下积分区域阴影示意图。

---

# R 多元函数积分的计算_第24页.png

解：
$$
原式 = \int_{0}^{\frac{\pi}{2}} d\theta \int_{\frac{1}{\sin\theta+\cos\theta}}^{1} \frac{r(\sin\theta+\cos\theta)}{r^2} \cdot r dr
$$

$$
= \int_{0}^{\frac{\pi}{2}} d\theta \int_{\frac{1}{\sin\theta+\cos\theta}}^{1} (\sin\theta+\cos\theta) dr
$$

对$r$积分时，$\theta$当常数看
$$
= \int_{0}^{\frac{\pi}{2}} (\sin\theta+\cos\theta)\cdot\left(1 - \frac{1}{\sin\theta+\cos\theta}\right) d\theta
$$

$$
= \int_{0}^{\frac{\pi}{2}} (\sin\theta+\cos\theta - 1) d\theta
$$

$$
= 2 - \frac{\pi}{2}
$$

---

# R 多元函数积分的计算_第25页.png

## 换元法
## 定积分的换元法
$\int_{a}^{b} f(x)dx$ 不好算
令 $x=\varphi(t)$，积分变量由$x\to t$
换元要三换：
- $f(x) \to f[\varphi(t)]$
- $\int_{a}^{b} \to \int_{\alpha}^{\beta}$
- $dx \to \varphi'(t)dt$
换元公式：
$$\int_{a}^{b} f(x)dx = \int_{\alpha}^{\beta} f[\varphi(t)]\varphi'(t)dt$$
前提：$x=\varphi(t)$单调，存在一阶连续导数
## 二重积分的换元法
$$\iint_{D_{xy}} f(x,y)dxdy$$ 不好算
令 $\begin{cases} x=x(u,v) \\ y=y(u,v) \end{cases}$，积分变量由$\begin{pmatrix}x\\y\end{pmatrix}\to\begin{pmatrix}u\\v\end{pmatrix}$
换元要三换：
- $f(x,y) \to f[x(u,v),y(u,v)]$
- $\iint_{D_{xy}} \to \iint_{D_{uv}}$
- $dxdy \to \left|\frac{\partial(x,y)}{\partial(u,v)}\right|dudv$

---

# R 多元函数积分的计算_第26页.png

$\left|\frac{\partial(x,y)}{\partial(u,v)}\right|$为雅可比行列式的绝对值，其中雅可比行列式定义为：
$$\frac{\partial(x,y)}{\partial(u,v)} = \begin{vmatrix}
\frac{\partial x}{\partial u} & \frac{\partial x}{\partial v} \\
\frac{\partial y}{\partial u} & \frac{\partial y}{\partial v}
\end{vmatrix}$$

二阶行列式的计算规则为：
$$\begin{vmatrix}a&b\\c&d\end{vmatrix}=ad-bc$$

因此雅可比行列式可展开为：
$$\begin{vmatrix}
\frac{\partial x}{\partial u} & \frac{\partial x}{\partial v} \\
\frac{\partial y}{\partial u} & \frac{\partial y}{\partial v}
\end{vmatrix} = \frac{\partial x}{\partial u}\cdot\frac{\partial y}{\partial v} - \frac{\partial x}{\partial v}\cdot\frac{\partial y}{\partial u}$$

二重积分换元法的使用前提：
$x=x(u,v),\ y=y(u,v)$存在一阶连续偏导数，且
$$\frac{\partial(x,y)}{\partial(u,v)} = \begin{vmatrix}
\frac{\partial x}{\partial u} & \frac{\partial x}{\partial v} \\
\frac{\partial y}{\partial u} & \frac{\partial y}{\partial v}
\end{vmatrix} \neq 0$$

满足上述条件时，二重积分换元公式为：
$$
\iint_{D_{xy}} f(x,y) \, dxdy = \iint_{D_{uv}} f\left[x(u,v),y(u,v)\right] \left|\frac{\partial(x,y)}{\partial(u,v)}\right| \, dudv
$$

## 直角坐标系转极坐标系
直角坐标系转极坐标实际上就是换元的过程。
直角坐标系下的二重积分$\iint_{D_{xy}} f(x,y)dxdy$不好算，因此做换元：
令
$$
\begin{cases}
x = r\cos\theta \\
y = r\sin\theta
\end{cases}
$$
积分变量由$\begin{pmatrix}x\\y\end{pmatrix}$变换为$\begin{pmatrix}r\\\theta\end{pmatrix}$。

---

# R 多元函数积分的计算_第27页.png

## 二重积分极坐标换元法
换元要三换：
- 被积函数替换：$f(x,y) \to f(r\cos\theta, r\sin\theta)$
- 积分区域替换：直角坐标积分区域$D_{xy}$替换为极坐标积分区域$D_{r\theta}$
- 面积元素替换：$dxdy \to \left|\frac{\partial(x,y)}{\partial(r,\theta)}\right| drd\theta$

计算极坐标变换的雅可比行列式：
$$
\frac{\partial(x,y)}{\partial(r,\theta)} = \begin{vmatrix}
\frac{\partial x}{\partial r} & \frac{\partial x}{\partial \theta} \\
\frac{\partial y}{\partial r} & \frac{\partial y}{\partial \theta}
\end{vmatrix}
$$
由极坐标变换关系$x=r\cos\theta$，$y=r\sin\theta$，计算偏导数：
$\because x=r\cos\theta$
$\therefore \frac{\partial x}{\partial r} = \cos\theta,\quad \frac{\partial x}{\partial \theta} = -r\sin\theta$
$\because y=r\sin\theta$
$\therefore \frac{\partial y}{\partial r} = \sin\theta,\quad \frac{\partial y}{\partial \theta} = r\cos\theta$

代入行列式展开计算：
$$
\frac{\partial(x,y)}{\partial(r,\theta)} = \begin{vmatrix}
\cos\theta & -r\sin\theta \\
\sin\theta & r\cos\theta
\end{vmatrix}
$$
$$
\begin{align*}
\frac{\partial(x,y)}{\partial(r,\theta)} &= r\cos^2\theta + r\sin^2\theta \\
&= r\left(\cos^2\theta + \sin^2\theta\right) \\
&= r
\end{align*}
$$
推导使用三角恒等式$\cos^2\theta + \sin^2\theta = 1$。

由此得到极坐标下二重积分换元公式：
$$
\iint_{D_{xy}} f(x,y) dxdy = \iint_{D_{r\theta}} f(r\cos\theta, r\sin\theta) \cdot r \, drd\theta
$$

## 例1415
计算二重积分$\displaystyle \iint_D e^{\frac{y}{x+y}} d\sigma$，其中积分区域$D$满足：
$$
D: \begin{cases}
0\leq y\leq 1 \\
0\leq x\leq 1-y
\end{cases}
$$

### 分析
这一题我们使用换元法求解，直接计算$\displaystyle \iint_D e^{\frac{y}{x+y}} d\sigma$不好算。
对积分变量做换元，令
$$
\begin{cases}
x+y = u \\
y = v
\end{cases}
$$
即完成变量变换$\begin{pmatrix}x\\y\end{pmatrix} \to \begin{pmatrix}u\\v\end{pmatrix}$。

---

# R 多元函数积分的计算_第28页.png

## 二重积分换元法
换元要三换：
1.  被积函数替换：$e^{\frac{y}{x+y}} \to e^{\frac{v}{u}}$
2.  积分区域替换：$\iint_{D_{xy}} \to \iint_{D_{uv}}$
3.  面积元素替换：$dxdy \to \left| \frac{\partial(x,y)}{\partial(u,v)} \right| dudv$

原积分区域$D_{xy}$满足：
$$D_{xy} = \begin{cases}
0\leq y\leq 1 \\
0\leq x\leq 1-y
\end{cases}$$
其中边界$x=1-y$即$y=-x+1$，区域$D$由
$$\begin{cases}
y=-x+1 \\
y=0 \\
x=0
\end{cases}$$
三条直线围成，对应$xy$平面第一象限内的三角形阴影区域（函数示意图）。

取换元关系：
$\because x+y=u,\ y=v$
$\therefore$ 区域边界对应变换为：
- $y=-x+1 \implies u=1$
- $y=0 \implies v=0$
- $x=0 \implies u=v$

则$D_{uv}$由
$$\begin{cases}
u=1 \\
v=0 \\
u=v
\end{cases}$$
三条直线围成，对应$uv$平面（横轴为$v$，纵轴为$u$）第一象限内的三角形阴影区域（函数示意图）。

积分次序选择：先积$v$后积$u$更简单。
定限口诀：后积先定限，限内画条线，最终得到$D_{uv}$的积分限：
$$D_{uv} = \begin{cases}
0\leq u\leq 1 \\
0\leq v\leq u
\end{cases}$$
对应该积分限的$uv$平面区域示意图（函数示意图）。

---

# R 多元函数积分的计算_第29页.png

## 二重积分换元法计算
解：令
$$
\begin{cases}
x + y = u \\
y = v
\end{cases}
$$
即$x = u-v$，$y = v$。

计算雅可比行列式：
$$
\frac{\partial(x,y)}{\partial(u,v)} = \begin{vmatrix}
\frac{\partial x}{\partial u} & \frac{\partial x}{\partial v} \\
\frac{\partial y}{\partial u} & \frac{\partial y}{\partial v}
\end{vmatrix}
$$
计算偏导数：
$\because x = u-v$，$\therefore \frac{\partial x}{\partial u} = 1$，$\frac{\partial x}{\partial v} = -1$
$\because y = v$，$\therefore \frac{\partial y}{\partial u} = 0$，$\frac{\partial y}{\partial v} = 1$

代入得：
$$
\frac{\partial(x,y)}{\partial(u,v)} = \begin{vmatrix}
1 & -1 \\
0 & 1
\end{vmatrix} = 1
$$
因此面积元素满足 $dxdy = dudv$。

则被积函数转换为：
$$e^{\frac{y}{x+y}} = e^{\frac{v}{u}}$$

积分区域转换为：
$$
D = \begin{cases}
0\leq y\leq 1 \\
0\leq x\leq 1-y
\end{cases} = \begin{cases}
0\leq u\leq 1 \\
0\leq v\leq u
\end{cases}
$$

由二重积分换元公式：
$$
\iint_D f(x,y) \, dxdy = \iint_D e^{\frac{v}{u}} \, dudv = \int_{0}^{1} du \int_{0}^{u} e^{\frac{v}{u}} \, dv
$$

因此原二重积分计算过程为：
$$
\begin{aligned}
\iint_D e^{\frac{y}{x+y}} \, d\sigma &= \int_{0}^{1} du \int_{0}^{u} e^{\frac{v}{u}} \, dv \\
&= \int_{0}^{1} u \int_{0}^{u} e^{\frac{v}{u}} \, d\left( \frac{v}{u} \right) du
\end{aligned}
$$

---

# R 多元函数积分的计算_第30页.png

$$= \int_{0}^{1} \left. u\cdot e^{\frac{v}{u}} \right|_{v=0}^{v=u} du$$
$\int e^x dx = e^x$

$$= \int_{0}^{1} u(e-1) du$$
$\int x dx = \frac{1}{2}x^2$

$$= (e-1)\cdot \left. \frac{1}{2}u^2 \right|_{u=0}^{u=1}$$

$$= \frac{1}{2}(e-1)$$