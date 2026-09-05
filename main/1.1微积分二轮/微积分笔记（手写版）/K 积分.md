# K 积分_第1页.png

# 不定积分
关系示意：$\int f(x)dx \leftarrow f(x) \rightarrow f'(x)$，附求导与不定积分互逆运算示意图，展示求导算子$\frac{d(\ )}{dx}$与不定积分算子$\int (\ )dx$的互逆性。

## 原函数与不定积分
如果一个函数$f(x)$在区间$I$上有定义，
如果存在一个可导函数$F(x)$，在区间$I$上每一点都满足$F'(x)=f(x)$成立，
就称$F(x)$为$f(x)$在区间$I$上的一个原函数。
记为：
$$\int f(x)dx = F(x) + C$$
该式叫做$f(x)$在区间$I$上的不定积分，满足：
$$F'(x)=f(x)$$
$$\left[F(x)+C\right]' = f(x)$$
其中$F(x)$为$f(x)$的一个原函数，$F(x)+C$为$f(x)$的全体原函数。

即：若$F'(x)=f(x),\ x\in I$成立，
则$\int f(x)dx$为$f(x)$的不定积分，
$\int f(x)dx$表示$f(x)$的全体原函数$F(x)+C$。

## 例8.1
设$0<x<1$，且$\int (1-x^2)f(x^2)dx = \arcsin x + C$，则$f(x)=$\underline{\qquad}

解：
由不定积分定义，对等式两边同时求导得：
$$\left[\arcsin x\right]' = (1-x^2)f(x^2)$$
计算左侧导数：
$$\frac{1}{\sqrt{1-x^2}} = (1-x^2)f(x^2)$$
整理得：
$$\Rightarrow f(x^2) = \frac{1}{(1-x^2)^{\frac{3}{2}}}$$
令$x^2 = t$，由$0<x<1$得$t\geq0$，代入得：
$$f(t) = \frac{1}{(1-t)^{\frac{3}{2}}},\quad t\geq0$$
将变量替换回$x$，得：
$$\Rightarrow f(x) = \frac{1}{(1-x)^{\frac{3}{2}}} = (1-x)^{-\frac{3}{2}}$$

---

# K 积分_第2页.png

## 原函数（不定积分）的存在定理
前面说，如果$\exists F'(x)=f(x),\ x\in I$成立，我们称$F(x)$是$f(x)$的原函数。
那么，什么样的$f(x)$一定会有原函数？什么样的$f(x)$可以有不定积分呢？
- 连续函数$f(x)$必有原函数$F(x)$。

那么，什么样的函数，没有原函数？什么样的函数，可能有原函数？
- 含有第一类间断点和无穷间断点的函数$f(x)$，在包含该间断点的区间内必没有原函数$F(x)$。
- 含有振荡间断点的函数$f(x)$，在包含该间断点的区间内可能有原函数$F(x)$。

若$F(x)$为可导函数，$F'(x)$会有什么样的性质？
- $f(x)$可导 $\implies$ $f(x)$必连续
- $f(x)$可导 $\nRightarrow$ $f'(x)$必连续
- $\implies$ 若$f'(x)$极限存在，则$f'(x)$必连续
- $\implies$ $f'(x)$有介值性
- $\implies$ 若$f'(x)\neq0$，则有$f'(x)$恒$>0$或恒$<0$
- $\implies$ $f'(x)$没有第一类间断点（可去、跳跃），没有无穷间断点
- $\implies$ $f'(x)$可能有振荡间断点

---

# K 积分_第3页.png

## 定积分
**前言**
当我们去求一个矩形面积时
$$
\begin{aligned}
S &= 底 \times 高 \\
&= (b-a)A
\end{aligned}
$$

那么，不规则图形的面积呢？
其高度$f(x)$是不断变化的。
$$S = (b-a) \times (?)$$

当我们把其分为许多小份时：
无论分多少实数份
其高度$f(x)$总是有一定的变化
$\Delta x$乘哪个高？
其误差总是存在的

但，若我把其分为超实数份？
即，$\Delta x \to 0$
那么，在实数系上，是没有误差的。
高度可以看作是不变的
即，当我们把其分为无穷份时
每一份可看作规则矩形
误差在实数系上为0

---

# K 积分_第4页.png

## 定义
若函数$f(x)$在区间$[a,b]$上有界
在$(a,b)$上任取$n-1$个分点$x_i\ (i=1,2,\dots,n-1)$
定义$x_0=a$和$x_n=b$，且$a=x_0<x_1<x_2<\dots<x_{n-1}<x_n=b$
记$\Delta x_k = x_k - x_{k-1},\quad k=1,2,\dots,n$。
并任取一点$\xi_k \in [x_{k-1},x_k]$
记$\lambda = \max\left\{\Delta x_k\right\},\ k\in[1,n]$
若当$\lambda \to 0$时，极限$\lim\limits_{\lambda \to 0} \sum_{k=1}^n f(\xi_k)\Delta x_k$存在，且与分点$x_i$及点$\xi_k$的取法无关，则称
函数$f(x)$在区间$[a,b]$上可积
记为：
$$\int_a^b f(x)dx = \lim_{\lambda \to 0} \sum_{k=1}^n f(\xi_k)\Delta x_k$$

其定义可分为4步：
① 分割
在其中任取一段$\Delta x_k$
$$\Delta x_k = x_k - x_{k-1}$$

② 近似
在$\Delta x_k$中任取一点$x=\xi_k$
这一小段面积近似为
$$S = f(\xi_k)\Delta x_k$$
（注：笔记中区间分割示意图、曲边梯形近似示意图未做符号转换，仅保留对应文字说明）

---

# K 积分_第5页.png

## ③ 求和
将这些小段的面积相加
则整个图形面积近似为
$$S = \sum_{k=1}^n f(\xi_k)\Delta x_k$$

## ④ 取极限
设$\lambda = \max\{\Delta x_k\},\ k\in[1,n]$
（让分割出来的所有小段中最长的那段设为$\lambda$）
则无误差的面积为
$$S = \lim_{\lambda \to 0} \sum_{k=1}^n f(\xi_k)\Delta x_k$$
（若最长的那一段为无穷小时，别的段只会更短，则$\Delta x \to 0,\ n\to\infty$）

若$\lim\limits_{\lambda \to 0} \sum_{k=1}^n f(\xi_k)\Delta x_k$存在，则称$f(x)$在区间$[a,b]$上可积，记为
$$\int_a^b f(x)dx = \lim_{\lambda \to 0} \sum_{k=1}^n f(\xi_k)\Delta x_k$$

注：定积分的定义是由黎曼给出的，故这定积分又被称为黎曼积分。

## 定积分的精确定义
在原定义的①中
若把“将$[a,b]$任意分，分为$n$份”
改为“将$[a,b]$ $n$等分，等分为$n$份”

在原定义的②中
若把“在$\Delta x_k$中任取一点$x=\xi_k$”
改为“取$\Delta x_k$中的右端点$\xi_k = x_k$”

---

# K 积分_第6页.png

（上方为区间$[a,b]$的$n$等分数轴示意图，标注分点位置$a+\frac{b-a}{n}\cdot i$（$i=1,2,3$），标注小区间长度$\Delta x_k$）
则原来的
$$\Delta x_k = \frac{b-a}{n}$$
原来的
$$\xi_i = x_i = a + \frac{b-a}{n}\cdot i$$
则
$$S = \int_a^b f(x)dx = \lim_{n\to\infty} \sum_{i=1}^n f\left(a+\frac{b-a}{n}\cdot i\right)\frac{b-a}{n}$$
若式中的$a$取$0$，$b$取$1$，则
$$S = \int_0^1 f(x)dx = \lim_{n\to\infty} \sum_{i=1}^n f\left(\frac{i}{n}\right)\frac{1}{n}$$

## 几何意义
在$[a,b]$上：
① 若$f(x)\geq0$，定积分$\int_a^b f(x)dx$表示由曲线$y=f(x)$、直线$x=a$、直线$x=b$与$x$轴所围成的曲边梯形的面积。
（对应示意图：$x$轴上方的曲边梯形，旁注“曲边梯形”）
② 若$f(x)\leq0$，定积分$\int_a^b f(x)dx$表示由曲线$y=f(x)$、直线$x=a$、$x=b$与$x$轴所围成的曲边梯形面积的负值。
（对应示意图：跨$x$轴的曲边图形，$x$轴上下均有阴影区域）
③ 若$f(x)$既有正值又有负值，定积分$\int_a^b f(x)dx$表示$x$轴上方图形的面积减去$x$轴下方的图形面积。

---

# K 积分_第7页.png

## 定积分的值与字母无关
当定积分存在时，有
$$\int_{a}^{b} f(x) \, dx = \int_{a}^{b} f(t) \, dt = \int_{a}^{b} f(u) \, du$$
定积分的值只与被积函数及积分区间有关，而与积分变量的记法无关。

## 定积分的存在定理
定积分的存在性，也称一元函数的（常义）可积性，这里的“常义”指“区间有限，函数有界”，也有人称为黎曼可积性，与后面要谈到的“区间无穷，函数无界”的（反常）积分有所区别。

## 定积分存在的充分条件
- 若$f(x)$在$[a,b]$上连续，则$\int_{a}^{b} f(x) \, dx$存在。
- 若$f(x)$在$[a,b]$上单调，则$\int_{a}^{b} f(x) \, dx$存在（不在考纲内）。
- 若$f(x)$在$[a,b]$上有界，且只有有限个间断点，则$\int_{a}^{b} f(x) \, dx$存在（不能有无穷间断点）。

## 定积分存在的必要条件
可积函数必有界。
即，定积分$\int_{a}^{b} f(x) \, dx$存在$\implies f(x)$在$[a,b]$上必有界。

理解：当我们任意分割图形底边为若干小段时，若$f(x)$在区间$[a,b]$上无界，则至少存在一个小段$\Delta x$，在$\Delta x$上，$f(x)$可以任意大，于是一个“小竖条”的面积$f(x)\Delta x$便可以无穷大，这样整个曲边梯形的面积就是无穷大，极限就不存在了。

---

# K 积分_第8页.png

## 定积分的性质（假设以下积分均存在）
## 两个规定
- 当$b=a$时，$\int_{a}^{b} f(x)dx = 0$（底边长为0）
- 当$a>b$时，$\int_{a}^{b} f(x)dx = -\int_{b}^{a} f(x)dx$

## 性质1（求区间长度）
设$a<b$，$f(x)=1$，则
$$\int_{a}^{b} dx = b-a$$
（对应$f(x)=1$在区间$[a,b]$上积分的矩形面积几何意义示意图）

## 性质2（积分的线性性质）
设$k_1,k_2$为常数，则
$$\int_{a}^{b} \left[k_1 f(x) \pm k_2 g(x)\right] dx = k_1 \int_{a}^{b} f(x)dx \pm k_2 \int_{a}^{b} g(x)dx$$

## 性质3[积分的可加（拆）性]
无论$a,b,c$的大小如何，总有
$$\int_{a}^{b} f(x)dx = \int_{a}^{c} f(x)dx + \int_{c}^{b} f(x)dx$$

## 性质4（积分的保号性）
若在区间$[a,b]$上$f(x) \leq g(x)$，则
$$\int_{a}^{b} f(x)dx \leq \int_{a}^{b} g(x)dx$$

特殊地有
$$\left| \int_{a}^{b} f(x)dx \right| \leq \int_{a}^{b} |f(x)| dx$$

例：
（对应区间上变号函数的积分示意图，用于演示上述绝对值积分性质）

---

# K 积分_第9页.png

$$\left|\int_a^b f(x)\mathrm{d}x\right| = |5-3| = |2| = 2$$
$$\int_a^b |f(x)|\mathrm{d}x = |5| + |-3| = 5+3 = 8$$
$$8>2$$
注：事实上，设$f(x)$是$[a,b]$上非负的连续函数，只要$f(x)$不恒等于零，则必有
$$\int_a^b f(x)\mathrm{d}x > 0$$
在有些积分不等式的证明与定积分值的估计中，要求获得严格的不等式结果，便需要用到这个结论，证明见例87。
## 性质5（估值定理）
设$M,m$分别是$f(x)$在$[a,b]$上的最大值与最小值，$L$为区间$[a,b]$的长度，则有
$$mL \leq \int_a^b f(x)\mathrm{d}x \leq ML$$
$$mL = \int_a^b m\mathrm{d}x,\quad ML = \int_a^b M\mathrm{d}x$$
## 性质6（中值定理）
（右上角附函数示意图：$f(x)$在$[a,b]$上的连续函数例图，标注了函数值$f(ξ)$与横轴上$a,ξ,b$的位置）
设$f(x)$在区间$[a,b]$上连续，则在$[a,b]$上至少存在一点$ξ$，使得
$$\int_a^b f(x)\mathrm{d}x = f(ξ)(b-a),\quad ξ\in(a,b)$$
### 证明
∵连续函数必有原函数
∴令$F(x) = \int_a^x f(t)\mathrm{d}t$（变上限积分）
则对$F(x)$在$[a,b]$上用拉格朗日中值定理
$$\Rightarrow F(b) - F(a) = F'(ξ)(b-a)$$
$$\int_a^b f(t)\mathrm{d}t - \int_a^a f(t)\mathrm{d}t = F'(ξ)(b-a)$$
$$\Rightarrow \int_a^b f(x)\mathrm{d}x = f(ξ)(b-a)$$
$$ξ\in(a,b) \subset [a,b]$$

---

# K 积分_第10页.png

## 知识小结
### $f(x)$是否有原函数
- 连续：存在（√）
- 间断：
  - 跳跃间断：不存在（×）
  - 可去间断：不存在（×）
  - 无穷间断：不存在（×）
  - 振荡间断：存在（√）
### $f(x)$是否有定积分（常义定积分，积分区间为$[a,b]$）
- 在$[a,b]$上连续：可积（√）
- 在$[a,b]$上有界且只有有限个间断点：可积（√）
- 在$[a,b]$上单调：可积（√）
- $[a,b]$为无限长度：不可积（×）（注：常义定积分要求积分区间为有限长度）
- $f(x)$无界：不可积（×）
## 例题
### 例8.3
判断下列函数$f(x)$在区间$[-1,2]$上的不定积分与定积分是否存在。
1.  
$$f(x)=\begin{cases}
2, & x>0 \\
1, & x=0 \\
-1, & x<0
\end{cases}$$
（函数示意图：分段函数，$x>0$时$f(x)=2$，$x=0$时$f(x)=1$，$x<0$时$f(x)=-1$，$x=0$为跳跃间断点）
$\because$ 有跳跃间断点
$\therefore$ 没有不定积分
$\because f(x)$在$[-1,2]$上有界
且在$[-1,2]$上只有有限个间断点
$\therefore$ 有定积分
2.  
$$f(x)=\begin{cases}
\frac{1}{x}, & x\neq0 \\
0, & x=0
\end{cases}$$
（函数示意图：反比例函数，$x>0$时图像位于第一象限单调递减，$x<0$时图像位于第三象限单调递增，$x=0$为间断点）

---

# K 积分_第11页.png

∵ 有无穷间断点
∴ 无不定积分
∵ 在$x \to 0$处，$f(x)$是无界的
∴ 无定积分

## 例84（对定积分的定义，即面积的考查）
设可导函数$y=f(x)$在$[0,+\infty)$上的值域是$[0,+\infty)$，$f(0)=0$，$f'(x)>0$，$x=\varphi(y)$是$y=f(x)$的反函数，记
$$I = \int_0^a f(x) dx + \int_0^b \varphi(y) dy$$
常数$a,b>0$。

求当$a < \varphi(b)$时，$I$与$ab$的大小关系。

解：
∵ $y=f(x)$在$[0,+\infty)$上的值域为$[0,+\infty)$
∴ 其图象在第一象限
∵ $f(0)=0$，$f'(x)>0$
∴ 可以大概猜出其图象

∵ $x=\varphi(y)$与$y=f(x)$为同一图象
（函数示意图：依次展示$\int_0^a f(x)dx$对应的曲线下面积、$\int_0^b \varphi(y)dy$对应的曲线左侧面积、$a<\varphi(b)$时两部分面积的合并区域、面积为$ab$的矩形参考区域）

∵ $a < \varphi(b)$
$\therefore I > ab$

---

# K 积分_第12页.png

## 例85（考查定积分所表示的面积）
$y=e^{-x}\sin x$ 在 $[0,+\infty)$ 上与$x$轴所围平面区域的面积写成如下表达式：
① $$\int_{0}^{+\infty} e^{-x}|\sin x| \, dx$$
② $$\left|\int_{0}^{+\infty} e^{-x}\sin x \, dx\right|$$
③ $$\lim_{n \to \infty} \sum_{k=0}^{n} \left| \int_{k\pi}^{(k+1)\pi} e^{-x}\sin x \, dx \right|$$
其中为正确表达式的是____

**解：**
（函数示意图：$y=\sin x$ 在$[0,+\infty)$上的正弦波形图像；$y=e^{-x}$ 在$[0,+\infty)$上单调递减趋于0的指数函数图像）

$e^{-x}\sin x$ 相当于在$\sin x$后面乘了一个随着$x$的改变，$y$不断变小的数，使$\sin x$图像的振幅不断变小。
（函数示意图：$y=e^{-x}\sin x$ 在$[0,+\infty)$上振幅不断衰减的振荡图像，标注了曲线与$x$轴围成的各段区域依次记为$A,B,C,D,\cdots$）

所围面积：$A+B+C+D+\cdots$
- $\displaystyle \int_{0}^{+\infty} e^{-x}\sin x \, dx$：$A-B+C-D+\cdots$
- $\displaystyle \int_{0}^{+\infty} e^{-x}|\sin x| \, dx$：$A+B+C+D+\cdots$，此处$e^{-x}>0$，$|e^{-x}\sin x|=e^{-x}|\sin x|$
- $\displaystyle \left|\int_{0}^{+\infty} e^{-x}\sin x \, dx\right|$：$\left|A-B+C-D+\cdots\right|$

---

# K 积分_第13页.png

$$\lim_{n \to \infty} \sum_{k=0}^n \left| \int_{k\pi}^{(k+1)\pi} e^{-x}\sin x dx \right| : |A|+|-B|+|C|+|-D|+\dots$$
∴ 为①③

## 例8.7（一个重要结论的证明）
设$f(x)$是$[a,b]$上非负的连续函数，且$f(x)$不恒等于零，证明：必有$\int_a^b f(x)dx > 0$

证明：由题意，至少$\exists x_0 \in (a,b)$使得$f(x_0)>0$
由$\lim_{x \to x_0} f(x) = f(x_0) > 0$
$\Rightarrow f(x) > 0,\ x \in (x_0-\delta, x_0+\delta)$
即$f(x) \geq \eta > 0$，$\eta>0$，$\eta$为常数
$$\Rightarrow \int_a^b f(x)dx \geq \int_{x_0-\delta}^{x_0+\delta} f(x)dx \geq \int_{x_0-\delta}^{x_0+\delta} \eta dx$$
$$\because \int_{x_0-\delta}^{x_0+\delta} \eta dx = 2\delta \eta > 0$$
$$\therefore \int_a^b f(x)dx > 0$$

## 例8.9（定积分比大小）
设$I_1 = \int_0^{\frac{\pi}{4}} \frac{\tan x}{x} dx,\ I_2 = \int_0^{\frac{\pi}{4}} \frac{x}{\tan x} dx$
比较$I_1,I_2,1$的大小关系

解：在$x \in (0,\frac{\pi}{4})$里
$0 < \sin x < x < \tan x$（常识）
$$\Rightarrow \frac{\tan x}{x} > \frac{x}{\tan x},\quad x \in \left(0,\frac{\pi}{4}\right)$$
$\Rightarrow I_1 > I_2$

在第2讲，第6个问题页的注(2)①中有说：在$x \in (0,\frac{\pi}{4})$里，$\frac{\tan x}{x} < \frac{4}{\pi}$
$$\Rightarrow I_1 < \int_0^{\frac{\pi}{4}} \frac{4}{\pi} dx$$
$$\Rightarrow 1 > I_1 > I_2$$

---

# K 积分_第14页.png

# 变限积分
## 前言
定积分示意图：纵轴为$f(t)$，横轴为$t$，阴影为区间$[a,b]$上的曲边梯形面积
定积分：
$$\int_{a}^{b} f(t) dt$$
变：改变，限：限制
变限积分就是在定积分的基础上，把定量$a,b$写成变量$x$，$x\in[a,b]$
变上限积分示意图：纵轴为$f(t)$，横轴为$t$，阴影为区间$[a,x]$上的曲边梯形面积
变上限积分：
$$\int_{a}^{x} f(t) dt$$
## 变限积分定义
当$x$在$[a,b]$上变动时，对应于每一个$x$值，积分$\int_{a}^{x} f(t) dt$都有一个确定的值，因此$\int_{a}^{x} f(t) dt$是一个关于$x$的函数
$$F(x) = \int_{a}^{x} f(t) dt,\quad x\in[a,b]$$
称函数$F(x)$为变上限积分，同理可以定义变下限积分和变上、下限积分
变限积分就是定积分的推广
## 性质
若函数$f(x)$在区间$I$上可积，则函数$F(x)=\int_{a}^{x} f(t) dt$在$I$上连续
函数性质的蕴含关系：
$$f(x)\text{可导} \implies \text{连续} \implies \text{可积} \implies \text{有界}$$

---

# K 积分_第15页.png

## 变限积分的连续性
证明：对任意$x, x+\Delta x \in I$，有：
$$\int_{x}^{x+\Delta x} f(t) dt$$
$$= \int_{a}^{x+\Delta x} f(t)dt - \int_{a}^{x} f(t)dt$$
$$= F(x+\Delta x) - F(x)$$
（对应函数示意图：以$t$为横轴、$f(t)$为纵轴的平面直角坐标系，轴上标注点$0,a,x,x+\Delta x$，阴影部分为区间$[a,x+\Delta x]$对应的曲边梯形，位置$x$处有竖直虚线标记）
由可积的必要条件（可积必有界）可知：
$\exists M>0$，使得在$I$上有$|f(t)| \leq M$。
所以由定积分的保号性知：
$$0 \leq |F(x+\Delta x) - F(x)| \leq M|\Delta x|$$
则
$$\lim_{\Delta x \to 0} |F(x+\Delta x) - F(x)| = 0$$
也可由夹逼准则推出。
即
$$\lim_{\Delta x \to 0} F(x+\Delta x) = F(x)$$
$\Rightarrow$ 对于变限积分$F(x)=\int_{a}^{x} f(t)dt$，只要它存在，就必然是连续的。

## 变上限积分求导定理（原函数存在定理）
函数$f(x)$在$I$上连续，
则函数
$$F(x) = \int_{a}^{x} f(t) dt$$
在$I$上可导，
且
$$F'(x) = f(x)$$
即：若$f(x)$连续，
$$\left( \int_{a}^{x} f(t) dt \right)' = f(x)$$
$$\int f(t) dt = \int_{a}^{x} f(t) dt + C$$

证明：
$$F'(x) = \lim_{\Delta x \to 0} \frac{F(x+\Delta x) - F(x)}{\Delta x}$$
若$x \in (a,b)$，取$\Delta x$使$x+\Delta x \in (a,b)$，则
$$\Delta F = F(x+\Delta x) - F(x)$$
$$= \int_{a}^{x+\Delta x} f(t)dt - \int_{a}^{x} f(t)dt$$
（对应函数示意图：以$t$为横轴、$f(t)$为纵轴的平面直角坐标系，轴上标注点$0,a,x,\Delta x,x+\Delta x$，网格阴影部分为区间$[x,x+\Delta x]$对应的曲边梯形，标注$\Delta F$）
$$= \int_{a}^{x} f(t)dt + \int_{x}^{x+\Delta x} f(t)dt - \int_{a}^{x} f(t)dt$$

---

# K 积分_第16页.png

## 连续函数下变上限积分求导推导
$$=\int_{x}^{x+\Delta x} f(t)dt$$
$$F'(x) = \lim_{\Delta x \to 0} \frac{\int_{x}^{x+\Delta x} f(t)dt}{\Delta x}$$
$\because f(x)$在$x\in[a,b]$上连续（用积分中值定理）
$\therefore \exists \xi$使
$$\int_{a}^{b}f(x)dx = f(\xi)(b-a),\quad \xi\in(a,b)$$
$$
\begin{align*}
\therefore F'(x) &= \lim_{\Delta x \to 0} \frac{f(\xi)\Delta x}{\Delta x} \\
&= \lim_{\Delta x \to 0} f(\xi),\quad \xi\in(x,x+\Delta x)
\end{align*}
$$
$\because \Delta x\to0$，$x+\Delta x\to x$
（数轴示意：$x<\xi<x+\Delta x$，当$\Delta x\to0$时，$x$、$x+\Delta x$均趋近于$x$）
$\therefore$由夹逼准则有$\xi \to x$
$\Rightarrow F'(x) = \lim_{\xi \to x} f(\xi)$，$\because f(x)$为连续函数
$$\therefore \lim_{\xi \to x} f(\xi) = f(x) = F'(x)$$

## 跳跃间断点情形
若$x=x_0\in I$是$f(x)$唯一的跳跃间断点
则$F(x)=\int_{a}^{x}f(t)dt$在$x=x_0$处不可导
且
$$
\begin{cases}
F'_-(x_0) = \lim_{x \to x_0^-} f(x) \neq f(x_0) \\
F'_+(x_0) = \lim_{x \to x_0^+} f(x) \neq f(x_0)
\end{cases}
$$
（$f(t)$函数示意图：横轴为$t$，标注$0,a,x_0,b$，$x_0$处为跳跃间断点，$[a,b]$上积分区域为阴影）

之前有说：若$f(x)$有跳跃间断点，那么$f(x)$是没有原函数的
所以
$$\int f(t)dt \neq \int_{a}^{x}f(t)dt + C$$
但，并不代表$\int_{a}^{x}f(t)dt$不存在
只是，$\int f(t)dt$不存在

## 可去间断点情形
若$x=x_0\in I$是$f(x)$唯一的可去间断点
则$F(x)=\int_{a}^{x}f(t)dt$
在$x=x_0$处可导
且
$$F'(x_0)=\lim_{x \to x_0}f(x) \neq f(x_0)$$
（$f(t)$函数示意图：横轴为$t$，标注$0,a,x_0,b$，$x_0$处为可去间断点（空心点），$[a,b]$上积分区域为阴影）

---

# K 积分_第17页.png

证明：∵ 若$f(x)$在$x=x_0$处为跳跃间断点
$$\therefore \lim_{x \to x_0^-} f(x) \neq \lim_{x \to x_0^+} f(x)$$
$$\because F'(x_0) = \lim_{x \to x_0} \frac{F(x)-F(x_0)}{x-x_0} \quad (\text{用洛必达})$$
$$= \lim_{x \to x_0} f(x)$$
$$\therefore F'_-(x_0) = \lim_{x \to x_0^-} f(x)$$
$$F'_+(x_0) = \lim_{x \to x_0^+} f(x)$$
$$\therefore F'_-(x_0) \neq F'_+(x_0)$$
∴ $F'(x_0)$不存在

(2) ∵ 若$f(x)$在$x=x_0$处为可去间断点
$$\therefore \lim_{x \to x_0^-} f(x) = \lim_{x \to x_0^+} f(x) \neq f(x_0)$$
$$\therefore F'_-(x_0) = F'_+(x_0)$$
∴ $F'(x_0)$存在

## 例8.11
设函数$y=f(x)$在区间$[-1,3]$上的图形给出，画出函数$F(x)=\int_0^x f(t)dt$的大概图形。

（附$y=f(x)$在$[-1,3]$上的函数示意图）

∵ $f(x)$在$x\in[a,b]$上有界
$x\in[a,b]$为有限区间
∴ $f(x)$在$x\in[a,b]$上可积
∴ 函数$F(x)=\int_a^x f(t)dt$在$[a,b]$上连续
$F(x)$在$x\in[a,b]$上无间断点
$$\because \int_0^0 f(t)dt = F(0) = 0$$

---

# K 积分_第18页.png

## 原函数$F(x)$的性质与图像
$\therefore F(x)$过原点
$\because f(x)$除在$x=0$，$x=2$处之外
$f(x)$为连续的
$\therefore$ 除$x=2$，$x=0$这俩点之外
$$F'(x) = f(x) = F(x)\text{的斜率}$$

$\therefore$ $F(x)$函数示意图：
横轴为$x$，标注刻度$-1,0,1,2,3$；纵轴为$F(x)$，标注刻度$-1$；图像过坐标原点，$x<0$时曲线位于第三象限，单调上升至原点；$0<x<2$时曲线先单调下降，在$x=1$处达到最低点（纵坐标约为$-1$），之后单调上升至点$(2,0)$；$x>2$时曲线先小幅上升，之后保持水平。

---

# K 积分_第19页.png

# 反常积分
## 引言
定积分$\to$常义积分：
$$
\begin{cases}
1.\ \text{积分区间有限} \\
2.\ \text{被积函数有界}
\end{cases}
$$
这是定积分存在的两个必要条件。
但是，人们后来发现，即使积分区间不是有限的，即使被积函数不是有界的，其所围出的曲边梯形的面积也有可能是存在的。
即：定积分的概念是不够用了，定义的范围需要扩大。
引入：反常积分$\to$广义积分
## 无穷区间上反常积分的概念与敛散性
**定义1** 设$F(x)$是$f(x)$在相应区间上的一个原函数：
$$
\int_{a}^{+\infty} f(x) \, dx = \lim_{x \to +\infty} F(x) - F(a)
$$
$$
\int_{-\infty}^{b} f(x) \, dx = F(b) - \lim_{x \to -\infty} F(x)
$$
若上述极限存在，则称反常积分收敛，否则称发散。

---

# K 积分_第20页.png

$$\int_{-\infty}^{+\infty} f(x)\mathrm{d}x = \int_{-\infty}^{x_0} f(x)\mathrm{d}x + \int_{x_0}^{+\infty} f(x)\mathrm{d}x$$
若右端两个积分都收敛，则称反常积分收敛，否则称发散。

## 无界函数的反常积分的概念与敛散性
定义2 设$F(x)$是$f(x)$在相应区间上的一个原函数，$x_0$为$f(x)$的瑕点。
瑕点：使$f(x)$在$x_0$的邻域内无界的点。
例：$\lim\limits_{x \to 0} \frac{1}{x} = \infty$，$x=0$为瑕点。
$\lim\limits_{x \to 0} \frac{1}{x}\sin\frac{1}{x}$为无界振荡，$x=0$为瑕点。

若$x=a$是唯一瑕点，则
$$\int_{a}^{b} f(x)\mathrm{d}x = F(b) - \lim_{x \to a^+} F(x)$$

若$x=b$是唯一瑕点，则
$$\int_{a}^{b} f(x)\mathrm{d}x = \lim_{x \to b^-} F(x) - F(a)$$

若上述极限存在，则称反常积分收敛，否则称发散。

若$x=c \in (a,b)$是唯一瑕点，则
$$\int_{a}^{b} f(x)\mathrm{d}x = \int_{a}^{c} f(x)\mathrm{d}x + \int_{c}^{b} f(x)\mathrm{d}x$$
若右端两个积分都收敛，则称反常积分收敛，否则称发散。

---

# K 积分_第21页.png

注：在反常积分中，一般把“$\infty$”和瑕点统称为奇点。
在判别积分敛散性时，一个积分中只能有一个奇点（判别前提），若出现两个及以上奇点，需拆分。

## 小结“加深理解”
先说结论：判断反常积分是收敛还是发散，本质上是一个比阶问题。

看$\int_{a}^{+\infty} f(x)dx$是否存在：
关键看$f(x)\to 0$的速度，即：看无穷小的阶数，
无穷小的阶数越高，$f(x)\to 0$的速度越快。

$f(x)$与$x$轴的靠近程度越大，$\int_{a}^{+\infty} f(x)dx$的面积值越易为有限值。
（对应无穷限反常积分几何意义示意图）

$\int_{a}^{b} f(x)dx$，其中$\lim\limits_{x \to a^+} f(x) = \infty$。
看$\int_{a}^{b} f(x)dx$是否存在：
关键看$f(x)\to\infty$的速度，即：看无穷大的阶数，
无穷大的阶数越低，$f(x)\to\infty$的速度越慢。

$f(x)$与$x=a$这条垂线的靠近程度越大。
（对应瑕积分几何意义示意图）

---

# K 积分_第22页.png

$\int_a^b f(x)dx$的面积值，极限为有限值。

## 敛散性的判别法
### 无穷区间
比的“大小”（函数值），“要会应用不等式”
Δ 比较判别法：设函数$f(x), g(x)$在区间$[a,+\infty)$上连续，并且$0\leq f(x)\leq g(x)\ (a\leq x<+\infty)$，则：“$f(x)$离$x$轴更近”
1.  当$\int_a^{+\infty}g(x)dx$收敛时，
$$\int_a^{+\infty}f(x)dx\text{收敛}$$
2.  当$\int_a^{+\infty}f(x)dx$发散时，
$$\int_a^{+\infty}g(x)dx\text{发散}$$

（函数示意图：平面直角坐标系$xOy$，原点为$O$；在$x\geq a$的区域内，$g(x)$与$f(x)$均为非负递减函数，$g(x)$图像位于$f(x)$上方，二者从$x=a$处出发向右延伸，逐渐趋近于$x$轴，分别标注有$g(x)$、$f(x)$）

Δ 比较判别法的极限形式 “$\frac{0}{0}$型”
比的“速度”（阶数，斜率）
设函数$f(x), g(x)$在区间$[a,+\infty)$上连续，且$f(x)\geq0$，$g(x)>0$，
$$\lim_{x\to+\infty}\frac{f(x)}{g(x)}=\lambda\quad(\text{有限或}\infty),\quad\text{为}\frac{0}{0}\text{型极限}$$
1.  当$\lambda\neq0$，且$\lambda\neq\infty$时，
$\int_a^{+\infty}f(x)dx$与$\int_a^{+\infty}g(x)dx$有相同的敛散性
2.  当$\lambda=0$时，若$\int_a^{+\infty}g(x)dx$收敛，
$\because f(x)$为$g(x)$的高阶无穷小
$\therefore \int_a^{+\infty}f(x)dx$也收敛
3.  当$\lambda=\infty$时，若$\int_a^{+\infty}g(x)dx$发散

---

# K 积分_第23页.png

∵ $g(x)$为$f(x)$的高阶无穷小
∴ $\int_{a}^{+\infty} f(x) \, dx$也发散

## 无界函数
### 比较判别法（不等式形式）
比的“大小”（函数值）
设$f(x), g(x)$在$(a,b]$上连续，瑕点同为$x=a$，并且$0 \leq f(x) \leq g(x) \ (a<x\leq b)$，则“$f(x)$离$x=a$更近”
1.  当$\int_{a}^{b} g(x) \, dx$收敛时，$\int_{a}^{b} f(x) \, dx$收敛
2.  当$\int_{a}^{b} f(x) \, dx$发散时，$\int_{a}^{b} g(x) \, dx$发散

附函数示意图：平面直角坐标系中，x轴标注原点$O$、点$a$、$b$，y轴为纵轴；区间$(a,b]$上$f(x),g(x)$均为单调递减正函数，$x\to a^+$时二者均趋向$+\infty$，$g(x)$图像始终位于$f(x)$上方，$x=b$处两函数值相等。

### 比较判别法的极限形式（$\frac{\infty}{\infty}$型）
比的“速度”（阶数，斜率）
设$f(x), g(x)$在$(a,b]$上连续，瑕点同为$x=a$，并且$f(x)\geq0, g(x)>0 \ (a<x\leq b)$，
$$\lim_{x \to a^+} \frac{f(x)}{g(x)} = \lambda \quad (\text{有限或}\infty)$$
则：
1.  当$\lambda \neq 0$，且$\lambda \neq \infty$时，$\int_{a}^{b} f(x) \, dx$和$\int_{a}^{b} g(x) \, dx$有相同敛散性
2.  当$\lambda = 0$时，若$\int_{a}^{b} g(x) \, dx$收敛
    ∵ $g(x)$为$f(x)$的高阶无穷大
    ∴ $\int_{a}^{b} f(x) \, dx$也收敛
3.  当$\lambda = \infty$时，若$\int_{a}^{b} g(x) \, dx$发散
    ∵ $f(x)$为$g(x)$的高阶无穷大
    ∴ $\int_{a}^{b} f(x) \, dx$也发散

---

# K 积分_第24页.png

$\therefore \int_a^b f(x)dx$也发散。

注：当你要作比较的时候，关键是比较对象要选的恰当。

## 两个重要结论
1.  瑕p积分$\int_0^1 \frac{1}{x^p}dx$的敛散性：
$$
\int_0^1 \frac{1}{x^p}dx
\begin{cases}
收敛, & 0<p<1\\
发散, & p\ge1
\end{cases}
$$
记法：$\int_0^1$的$p$越小越收敛。

2.  无穷限p积分$\int_1^{+\infty}\frac{1}{x^p}dx$的敛散性：
$$
\int_1^{+\infty} \frac{1}{x^p}dx
\begin{cases}
收敛, & p>1\\
发散, & 0<p\le1
\end{cases}
$$
记法：$\int_1^{+\infty}$的$p$越大越收敛。

## 3. 对1,2的扩展
eg：当$x\to0^+$时，$\sin x \sim x$，即$\lim\limits_{x\to0^+}\frac{\sin x}{x}=1$。

这意味着，在$x\to0^+$时，$\sin x$与$x$趋于0的“速度”是一样快的。

那么：
$$
\int_0^1 \frac{1}{\sin^p x}dx
\begin{cases}
收敛, & 0<p<1\\
发散, & p\ge1
\end{cases}
$$
$$
\int_0^1 \frac{1}{x^p}dx
\begin{cases}
收敛, & 0<p<1\\
发散, & p\ge1
\end{cases}
$$

两个是一样的。

事实上，凡是与$x$趋于0的“速度”一样的函数$f(x)$，均可如上讨论。

---

# K 积分_第25页.png

同理，eg：当$x \to +\infty$且$a>0$时，$ax+b$亦趋于$+\infty$，与$x$趋于$+\infty$的“速度”一样，即
$$\lim_{x \to +\infty} \frac{ax+b}{x} = a$$

当$ax+b>0$时，$\int_{1}^{+\infty} \frac{1}{(ax+b)^p} \mathrm{d}x$ 亦满足
$$
\begin{cases}
\text{收敛}, & p>1 \\
\text{发散}, & p \leq 1
\end{cases}
$$

凡是与$x$趋于$+\infty$的“速度”一样的函数$f(x)$，均可满足以上结论。

## 例8.15
设$a>b>0$，反常积分
$$\int_{0}^{+\infty} \frac{1}{x^a + x^b} \mathrm{d}x$$
收敛，求$a$与$b$的取值范围。

### 分析
$\because \int_{0}^{+\infty}$中有两个奇点：$+\infty$、$0$
$\therefore$要拆开，拆成$\int_{0}^{1} + \int_{1}^{+\infty}$，两个分开看。

### 解
先看$\int_{0}^{1} \frac{1}{x^a + x^b} \mathrm{d}x$

$\because \frac{1}{x^a + x^b}$很复杂，$\therefore$我们要找与其趋向速度一致的来把其替换掉。

$\because a>b>0$
$\therefore x \to 0$时，$x^a \ll x^b$
$\therefore$当$x \to 0$时，$x^a + x^b \approx x^b$

比较速度

---

# K 积分_第26页.png

## 比较速度
$$\lim_{x \to 0^+} \frac{\frac{1}{x^a + x^b}}{\frac{1}{x^b}} = \lim_{x \to 0^+} \frac{x^b}{x^a + x^b} = 1$$
$\therefore \int_0^1 \frac{1}{x^a + x^b} \mathrm{d}x$ 与 $\int_0^1 \frac{1}{x^b} \mathrm{d}x$ 敛散性一致。
$$\because \int_0^1 \frac{1}{x^b} \mathrm{d}x \begin{cases}
\text{收敛}, & 0<b<1 \\
\text{发散}, & b\geq1
\end{cases}$$
$\therefore$ 当$b<1$时，$\int_0^1 \frac{1}{x^b} \mathrm{d}x$收敛，即$\int_0^1 \frac{1}{x^a + x^b} \mathrm{d}x$收敛。
再看$\int_1^{+\infty} \frac{1}{x^a + x^b} \mathrm{d}x$：
$\because a>b>0$
$\therefore x \to +\infty$时，$x^a \gg x^b$
$\therefore$ 当$x \to +\infty$时，$x^a + x^b \approx x^a$。
$$\lim_{x \to +\infty} \frac{\frac{1}{x^a + x^b}}{\frac{1}{x^a}} = \lim_{x \to +\infty} \frac{x^a}{x^a + x^b} = 1$$
$\therefore \int_1^{+\infty} \frac{1}{x^a + x^b} \mathrm{d}x$ 与 $\int_1^{+\infty} \frac{1}{x^a} \mathrm{d}x$ 敛散性一致。
$$\because \int_1^{+\infty} \frac{1}{x^a} \mathrm{d}x \begin{cases}
\text{收敛}, & a>1 \\
\text{发散}, & a\leq1
\end{cases}$$
$\therefore$ 当$a>1$时，$\int_1^{+\infty} \frac{1}{x^a} \mathrm{d}x$收敛，即$\int_1^{+\infty} \frac{1}{x^a + x^b} \mathrm{d}x$收敛。

---

# K 积分_第27页.png

当$\int_{0}^{1} \frac{1}{x^a + x^b} \, dx$与$\int_{1}^{+\infty} \frac{1}{x^a + x^b} \, dx$收敛时，$\int_{0}^{+\infty} \frac{1}{x^a + x^b} \, dx$收敛，即$a>1$且$b<1$。

## 例8.16
若反常积分$\int_{1}^{+\infty} \left( e^{-\cos \frac{1}{x}} - e^{-1} \right) x^k \, dx$收敛，则$k$的取值范围是$\underline{\qquad}$

**分析**：找一个在$x \to +\infty$时，与被积函数趋向速度相同的简单式来替换掉这个复杂式，最好将$\int_{1}^{+\infty} \left(e^{-\cos \frac{1}{x}} - e^{-1}\right)x^k \, dx$换成$\int_{1}^{+\infty} \frac{1}{x^p} \, dx$，然后用结论秒杀。

**解**：
对被积函数做恒等变形：
$$\text{原式} = \int_{1}^{+\infty} e^{-1}\left( e^{1-\cos \frac{1}{x}} - 1 \right) x^k \, dx$$

当$x \to +\infty$时，$1-\cos \frac{1}{x} \to 0$，有等价关系：
$$e^{1-\cos \frac{1}{x}} - 1 \sim 1-\cos \frac{1}{x}$$
$$1-\cos \frac{1}{x} \sim \frac{1}{2}\left( \frac{1}{x} \right)^2$$
$$e^{-1} \cdot \frac{1}{2} \cdot \frac{1}{x^2} \sim \frac{1}{x^2}$$

由反常积分比较判别法的极限形式：
$$\lim_{x \to +\infty} \frac{e^{-1}\left( e^{1-\cos \frac{1}{x}} - 1 \right) x^k}{\frac{1}{x^2} \cdot x^k} = \text{常数} \neq 0$$

即$\int_{1}^{+\infty} e^{-1}\left( e^{1-\cos \frac{1}{x}} - 1 \right) x^k \, dx$与$\int_{1}^{+\infty} \frac{1}{x^2} \cdot x^k \, dx$敛散性一致。

化简得：
$$\int_{1}^{+\infty} \frac{1}{x^2} \cdot x^k \, dx = \int_{1}^{+\infty} \frac{1}{x^{2-k}} \, dx$$

---

# K 积分_第28页.png

当$2-k>1$时，收敛
即$k<1$

## 例8.18 “一个重要结论”
已知$\alpha>0$，判别反常积分$\int_{0}^{1} \frac{\ln x}{x^\alpha} dx$的敛散性。

【分析】由$\int_{0}^{1} \frac{1}{x^\alpha} dx$换成了$\int_{0}^{1} \frac{\ln x}{x^\alpha} dx$，已知p型瑕积分的敛散性结论：
$$\int_{0}^{1} \frac{1}{x^\alpha} dx
\begin{cases}
收敛，&0<\alpha<1\\
发散，&\alpha\geq1
\end{cases}$$

比较一下

解：
计算$x \to 0^+$时的极限，为$\frac{\infty}{\infty}$型：
$$\lim_{x \to 0^+} \frac{\frac{\ln x}{x^\alpha}}{\frac{1}{x^\alpha}} = +\infty$$

$\Rightarrow x\to0^+$时，
两者趋向$x=0$的速度：$\frac{\ln x}{x^\alpha} \gg \frac{1}{x^\alpha}$，
$\frac{1}{x^\alpha}$离$x=0$更近。

若$\alpha\geq1$：
则$\int_{0}^{1} \frac{1}{x^\alpha} dx$发散，
$\because \frac{\ln x}{x^\alpha}$为$\frac{1}{x^\alpha}$的高阶无穷大，
$\therefore \int_{0}^{1} \frac{\ln x}{x^\alpha} dx$也必发散。

若$0<\alpha<1$：
则$\int_{0}^{1} \frac{1}{x^\alpha} dx$收敛，
之前说过一个式子：
$$\because \lim_{x \to 0^+} x^\alpha \ln x = 0 \quad (\forall \alpha>0)$$

---

# K 积分_第29页.png

## 先说结论
∵ 对于$\ln x$与幂函数$x^\alpha$，
无论$x \to +\infty$，还是$x \to 0^+$，
两者趋向速度均满足$\ln x \ll x^\alpha$，$\ln x$的趋向速度比$x^\alpha$慢得多。
∴ 【结论】
$$\int_0^1 \frac{\ln x}{x^\alpha} \, dx \begin{cases}
收敛, & 0<\alpha<1 \\
发散, & \alpha \geq 1
\end{cases}$$
即：∵ $\ln x$趋向速度比$x^\alpha$慢得多，
∴ $\left(\frac{1}{x}\right)^\alpha$乘个$\ln x$，
对$\int_0^1 \frac{1}{x^\alpha} \, dx$原来的敛散性
无影响。
> “蚊子叮大象，不痛不痒”

## 例8.19 “一个重要结论”
已知$\alpha>0$，判断反常积分
$\int_1^{+\infty} \frac{\ln x}{x^\alpha} \, dx$的敛散性。

【分析】由$\int_1^{+\infty} \frac{1}{x^\alpha} \, dx$换成了$\int_1^{+\infty} \frac{\ln x}{x^\alpha} \, dx$，已知p积分的敛散性结论：
$$\int_1^{+\infty} \frac{1}{x^\alpha} \, dx \begin{cases}
收敛, & \alpha>1 \\
发散, & 0<\alpha \leq 1
\end{cases}$$
根据例8.18很容易得出结论。

解：
$$\lim_{x \to +\infty} \frac{\frac{\ln x}{x^\alpha}}{\frac{1}{x^\alpha}} = +\infty \quad \text{“}\frac{0}{0}\text{”型}$$

---

# K 积分_第30页.png

对于$\ln x$与幂函数$x^\alpha$：
无论$x\to+\infty$，还是$x\to0^+$，两者趋向速度均满足$\ln x \ll x^\alpha$，即$x^\alpha \ln x$趋向结果与$x^\alpha$趋向结果一致。

$\Rightarrow$ 当$x\to+\infty$时：
两者趋向$y=0$的速度满足$\frac{\ln x}{x^\alpha} \ll \frac{1}{x^\alpha}$，即$\frac{1}{x^\alpha}$离$y=0$更近。
若$0<\alpha\leq1$：
则$\int_{1}^{+\infty}\frac{1}{x^\alpha}\mathrm{d}x$发散，
$\because \frac{1}{x^\alpha}$为$\frac{\ln x}{x^\alpha}$的高阶无穷小，
$\therefore \int_{1}^{+\infty}\frac{\ln x}{x^\alpha}\mathrm{d}x$也必发散。

若$\alpha>1$：
则$\int_{1}^{+\infty}\frac{1}{x^\alpha}\mathrm{d}x$收敛，
$\because$ 对$\forall \alpha>0$，有：
$$\lim_{x\to+\infty} x^\alpha \ln x = +\infty$$
$$\lim_{x\to+\infty} x^{-\alpha}\ln x = 0$$

## 结论
$$\therefore \int_{1}^{+\infty}\frac{\ln x}{x^\alpha}\mathrm{d}x
\begin{cases}
\text{收敛}, & \alpha>1 \\
\text{发散}, & 0<\alpha\leq1
\end{cases}$$
即：$\int_{1}^{+\infty}\frac{1}{x^\alpha}\mathrm{d}x$与$\int_{1}^{+\infty}\frac{\ln x}{x^\alpha}\mathrm{d}x$的敛散性一致。

---

# K 积分_第31页.png

## 知识小结 “宏观”
对于反常积分敛散性的判别方法：
- 比较
  1.  比函数值：$f(x) > g(x)$
  2.  比趋向速度：“$\frac{0}{0}$”“$\frac{\infty}{\infty}$”
  3.  结论：
      $$\int_0^1 \frac{1}{x^p}dx,\quad \int_0^1 \frac{\ln x}{x^p}dx$$
      $$\int_1^{+\infty} \frac{1}{x^p}dx,\quad \int_1^{+\infty} \frac{\ln x}{x^p}dx$$
- “速度为同一级别”
  $\because f(x)$与$\frac{1}{x^p}$趋向速度一致
  例：
  $$\lim_{x\to0^+} \frac{f(x)}{\frac{1}{x^p}} = \text{非零常数}$$
  $\therefore \int_0^1 \frac{1}{x^p}dx$与$\int_0^1 f(x)dx$敛散性一致。
- “自行车撞大卡车，不痛不痒”
  $\because$ 趋向速度 $\ln x \ll x^p$
  即：
  $$\lim_{x\to0^+} x^\alpha \ln x = 0 \quad (\forall \alpha>0)$$
  $$\lim_{x\to+\infty} x^\alpha \ln x = +\infty \quad (\forall \alpha>0)$$
  $\therefore \ln x \cdot x^p$与$x^p$极限趋向结果一致，积分敛散性一致。

---

# K 积分_第32页.png

## 注：
当$f(x)$为偶函数
且$\int_{0}^{+\infty} f(x)\mathrm{d}x$收敛时，
有$$\int_{-\infty}^{+\infty} f(x)\mathrm{d}x = 2\int_{0}^{+\infty} f(x)\mathrm{d}x$$

当$f(x)$为奇函数
且$\int_{0}^{+\infty} f(x)\mathrm{d}x$收敛时
有$$\int_{-\infty}^{+\infty} f(x)\mathrm{d}x = 0$$

“这里并不是说$+\infty$与$-\infty$互为相反数”
“更不是说$\int_{-\infty}^{+\infty}$是对称区间”
关键是因为反常积分的收敛