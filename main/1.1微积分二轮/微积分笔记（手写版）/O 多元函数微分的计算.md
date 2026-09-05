# O 多元函数微分的计算_第1页.png

## 多元函数微分法则
### 链式求导规则
难点是对标号的判别与理解。
设$z = f(u,v)$，$u = \varphi(x,y)$，$v = w(x,y)$，则复合函数为
$$z = f\left[\varphi(x,y), w(x,y)\right]$$
且偏导数满足：
$$\frac{\partial z}{\partial x} = \frac{\partial z}{\partial u} \cdot \frac{\partial u}{\partial x} + \frac{\partial z}{\partial v} \cdot \frac{\partial v}{\partial x}$$
$$\frac{\partial z}{\partial y} = \frac{\partial z}{\partial u} \cdot \frac{\partial u}{\partial y} + \frac{\partial z}{\partial v} \cdot \frac{\partial v}{\partial y}$$
#### 注
1.  设$z = f(u,v)$，$u = \varphi(t)$，$v = w(t)$，则复合函数为
    $$z = f\left[\varphi(t), w(t)\right]$$
    且全导数满足：
    $$\frac{\mathrm{d} z}{\mathrm{d} t} = \frac{\partial z}{\partial u} \cdot \frac{\mathrm{d} u}{\mathrm{d} t} + \frac{\partial z}{\partial v} \cdot \frac{\mathrm{d} v}{\mathrm{d} t}$$
2.  无论$z$对哪个变量求导，无论$z$已经求了几阶导，求导后的新函数仍然具有与原函数完全相同的复合结构。
---
### 与一元复合函数求导对比（compare）
一元情形：设$y = f(u)$，$u = \varphi(x)$，$y$对$x$求导的复合路径为$y \to u \to x$，求导公式为：
$$\frac{\mathrm{d} y}{\mathrm{d} x} = \frac{\mathrm{d} y}{\mathrm{d} u} \cdot \frac{\mathrm{d} u}{\mathrm{d} x}$$

---

# O 多元函数微分的计算_第2页.png

## 二元
$z = f(u,v),\ u = \varphi(x,y),\ v = w(x,y)$
### z对x轴方向求偏导
$$\frac{\partial z}{\partial x} = \frac{\partial z}{\partial u} \cdot \frac{\partial u}{\partial x} + \frac{\partial z}{\partial v} \cdot \frac{\partial v}{\partial x}$$
### z对y轴方向求偏导
$$\frac{\partial z}{\partial y} = \frac{\partial z}{\partial u} \cdot \frac{\partial u}{\partial y} + \frac{\partial z}{\partial v} \cdot \frac{\partial v}{\partial y}$$
## 注(1)
$z = f(u,v),\ u = \varphi(t),\ v = w(t)$
z对t求全导：
$$\frac{dz}{dt} = \frac{\partial z}{\partial u} \cdot \frac{du}{dt} + \frac{\partial z}{\partial v} \cdot \frac{dv}{dt}$$
当求导变量有多个，且只对其中一个求导时，是部分求导，是求偏导，例：$\frac{\partial z}{\partial u}$
当求导变量只有一个时，对其求导时，是全部求导，是求全导，例：$\frac{dz}{dt},\ \frac{du}{dt}$

---

# O 多元函数微分的计算_第3页.png

## (2) 复合函数偏导的记号含义
（复合函数结构示意：函数$f$包含两个中间变量，编号1的中间变量为$x^2 y$，编号2的中间变量为$xy^2$，两个中间变量均为自变量$x$的函数）
根据多元复合函数的链式求导法则，全导数为：
$$\frac{df}{dx} = \frac{\partial f}{\partial \text{口}} \cdot \frac{d\text{口}}{dx} + \frac{\partial f}{\partial \text{回}} \cdot \frac{d\text{回}}{dx}$$
对式中$\frac{\partial f}{\partial \text{口}}$的说明：
“口”在$\frac{\partial f}{\partial \text{口}}$中作为整体自变量存在，该偏导是对“口”这个整体求偏导，求解过程不体现“口$=x^2 y$”的具体表达式；无论“口”的表达式多么复杂，都不影响该偏导的形式。

若“口”与“回”的表达式发生改变，例如：
$$
\begin{aligned}
\text{口} &= x^2 y + \sin x \\
\text{回} &= x y^2 + \ln x \cdot \cos x
\end{aligned}
$$
则$\frac{\partial f}{\partial \text{口}}$与$\frac{\partial f}{\partial \text{回}}$的表达式形式保持不变，发生改变的只有$\frac{d\text{口}}{dx}$与$\frac{d\text{回}}{dx}$；只有在计算$\frac{d\text{口}}{dx}$的过程中，才需要代入“口$=x^2 y + \sin x$”这类具体表达式。

$\therefore$可以直接将$\frac{\partial f}{\partial (x^2 y)}$标记为$f_1'$。
甚至可以采用如下标记方式：
（复合函数结构示意：函数$f$包含两个中间变量，标记为$x$的位置对应中间变量$x^2 y$，标记为$y$的位置对应中间变量$x y^2$，两个中间变量均为自变量$x$的函数）
将$\frac{\partial f}{\partial (x^2 y)}$记为$f_x'$，将$\frac{\partial f}{\partial (x y^2)}$记为$f_y'$。
需要明确：$f_x'$表示$f$对标记为$x$的中间变量位置求偏导。

---

# O 多元函数微分的计算_第4页.png

若 $z=f(u,v)$，$u=\varphi(x,y)$，$v=w(x,y)$，对应复合函数变量依赖关系示意图：$z$ 是 $u,v$ 的函数，$u,v$ 均为 $x,y$ 的函数。
我们一般表示：$u$ 为1或$x$，$v$ 为2或$y$。

$$z_u' = f_u'(u,v) = f_1'(u,v) = f_1' = z_1'$$
$$z_v' = f_v'(u,v) = f_2'(u,v) = f_2' = z_2'$$

$$
\begin{aligned}
z_x' &= z_u'\cdot u_x' + z_v'\cdot v_x' \\
&= f_1'\cdot u_x' + f_2'\cdot v_x'
\end{aligned}
$$

$$
\begin{aligned}
z_y' &= z_u'\cdot u_y' + z_v'\cdot v_y' \\
&= f_1'\cdot u_y' + f_2'\cdot v_y'
\end{aligned}
$$

$$z_{uu}'' = f_{11}'',\quad z_{uv}'' = f_{12}''$$

## (3)
对应复合函数变量依赖关系示意图：$z$ 是 $u,v$ 的函数，$u,v$ 均为 $x,y$ 的函数。
若为上述复合结构，则 $z_u'=f_1'$，对应相同的复合函数变量依赖关系示意图。

$z$，$f_1'$，$f_2'$，$f_3'$，$z_x'$，$z_x''$ 等等都为相同的复合结构。

## 例13.9
设 $z=f(e^x \sin y, x^2+y^2)$，其中$f$具有二阶连续偏导数，$f_1'(0,0)=1$，$f_2'(0,0)=-1$，求 $\dfrac{\partial^2 z}{\partial x \partial y}$。

---

# O 多元函数微分的计算_第5页.png

## 分析
$$\frac{\partial^2 z}{\partial x \partial y} = \frac{\partial}{\partial y}\left( \frac{\partial z}{\partial x} \right)$$
先对$x$求偏导，再对$y$求偏导。

复合结构：$z$有两个中间变量，1号中间变量为$e^x \sin y$，2号中间变量为$x^2+y^2$，两个中间变量均依赖自变量$x,y$。
$z$对$x$求偏导时，$y$视为常数，计算得一阶偏导：
$$\frac{\partial z}{\partial x} = f_1' \cdot e^x \sin y + f_2' \cdot 2x$$

之后再对$y$求偏导，此时$x$视为常数，展开偏导式：
$$
\begin{aligned}
\frac{\partial\left( \frac{\partial z}{\partial x} \right)}{\partial y} &= \frac{\partial\left[ f_1' \cdot e^x \sin y + f_2' \cdot 2x \right]}{\partial y} \\
&= \frac{\partial\left( f_1' \cdot e^x \sin y \right)}{\partial y} + \frac{\partial\left( f_2' \cdot 2x \right)}{\partial y}
\end{aligned}
$$

## 难点
难点在于求 $\frac{\partial(f_1')}{\partial y},\ \frac{\partial(f_2')}{\partial y}$。

$$\frac{\partial(f_1')}{\partial y} = \frac{\partial(z_u')}{\partial y}$$
由前面的注知：$f_1'$与$z$有相同的复合结构，$f_2'$与$z$也为相同的复合结构。

且称：
$$z_{vu}'' = f_{21}'' = (z_v')_u'$$

即：
$$\frac{\partial(f_2')}{\partial y} = f_{21}'' \cdot \frac{\partial u}{\partial y} + f_{22}'' \cdot \frac{\partial v}{\partial y}$$

例：
求$\frac{\partial(f_1')}{\partial x}$
（对应复合结构示意图：该例中$f_1'$的复合结构与$z$一致，两个中间变量均依赖自变量$x,y$）

---

# O 多元函数微分的计算_第6页.png

$$
= f_{11}''\cdot \frac{\partial u}{\partial x} + f_{12}''\cdot \frac{\partial v}{\partial x}
$$
$$
= f_{11}''\cdot e^x \sin y + f_{12}''\cdot 2x
$$

解：
先求$z$对$x$的一阶偏导数：
$$
\frac{\partial z}{\partial x} = f_1'\cdot e^x \sin y + f_2'\cdot 2x
$$
再对$y$求偏导，计算混合二阶偏导数$\frac{\partial^2 z}{\partial x \partial y}$：
$$
\frac{\partial\left( \frac{\partial z}{\partial x} \right)}{\partial y} = \frac{\partial\left( f_1' e^x \sin y \right)}{\partial y} + \frac{\partial\left( f_2' \cdot 2x \right)}{\partial y}
$$
由乘积求导法则展开：
$$
= \frac{\partial(f_1')}{\partial y}\cdot e^x \sin y + f_1'\cdot e^x \cos y + 2x\cdot \frac{\partial(f_2')}{\partial y}
$$
对$f_1',f_2'$应用复合函数链式法则求偏导：
$$
\begin{aligned}
={}& \left( f_{11}''\cdot e^x \cos y + f_{12}''\cdot 2y \right)e^x \sin y + f_1'\cdot e^x \cos y \\
&+ 2x\cdot \left( f_{21}''\cdot e^x \cos y + f_{22}''\cdot 2y \right)
\end{aligned}
$$

$\because$ 将$(0,0)$点代入，可得：
$$e^x\sin y=0,\quad 2x=0,\quad e^x\cos y=1$$
且已知该点处一阶偏导值：
$$f_1'(0,0)=1,\quad f_2'(0,0)=-1$$
$\therefore$ 二阶混合偏导在$(0,0)$处的值为：
$$
\left. \frac{\partial^2 z}{\partial x \partial y} \right|_{(0,0)} = f_1'(0,0) = 1
$$

## 例13.10
设函数$f(x,e^x) = x + e^x$，
且$\left. f_x'(x,y) \right|_{y=e^x} = 1+2e^x$，
求$\left. f_y'(x,y) \right|_{y=e^x}$。

**分析** 通常情况下，我们为了方便，按中间变量顺序标记偏导。该复合函数的变量依赖关系为：$f$的第一个中间变量为$x$，第二个中间变量为$e^x$，两个中间变量均最终依赖自变量$x$。由全导数的链式法则：
$$
\begin{aligned}
\frac{df}{dx} &= f_1'\cdot \frac{dx}{dx} + f_2'\cdot \frac{d(e^x)}{dx} \\
&= f_1'\cdot 1 + f_2'\cdot e^x
\end{aligned}
$$

---

# O 多元函数微分的计算_第7页.png

## 复合函数偏导记号说明
此题标记的方式略有不同：
复合函数变量依赖示意图：二元函数$f$分为两个支路，分别指向自变量位置$x$（支路标注$x$）和$e^x$（支路标注$y$），两个支路最终汇合到$x$，即复合为关于$x$的一元函数，对应链式求导公式：
$$
\begin{align*}
\frac{df}{dx} &= f_x'\cdot \frac{dx}{dx} + f_y'\cdot \frac{d(e^x)}{dx} \\
&= f_x'\cdot 1 + f_y'\cdot e^x
\end{align*}
$$

则，题目中的
$$\left. f_x'(x,y) \right|_{y=e^x} = f_x'(x,e^x) = f_x'$$
是指$f$对标记为$x$的位置求偏导，与$f_1'$是一样的。

让你求的$\left. f_y'(x,y) \right|_{y=e^x}$
$$= f_y'(x,e^x) = f_y'$$
与$f_2'$是一样的。

## 例题求解
解：
$\because f(x,e^x) = x + e^x$
$\therefore \frac{df}{dx} = 1 + e^x$

$\because$ 根据链式法则：
$$
\begin{align*}
\frac{df}{dx} &= f_x'\cdot \frac{dx}{dx} + f_y'\cdot \frac{d(e^x)}{dx} \\
&= f_x'\cdot 1 + f_y'\cdot e^x = 1+e^x
\end{align*}
$$
且$f_x' = 1+2e^x$
$\therefore$
$$1+2e^x + f_y'\cdot e^x = 1+e^x$$
$$\Rightarrow f_y' = -1$$

---

# O 多元函数微分的计算_第8页.png

## 全微分形式不变性
设 $z = f(u,v)$，$u = u(x,y)$，$v = v(x,y)$。
如果 $f(u,v)$，$u(x,y)$，$v(x,y)$ 分别有连续偏导数，
则复合函数 $z = f(u,v)$ 在 $(x,y)$ 处的全微分可表示为
$$dz = \frac{\partial z}{\partial u}du + \frac{\partial z}{\partial v}dv$$
无论 $u,v$ 是自变量还是中间变量，上式都成立。

*Compare*

### 一元函数微分形式不变性的证明
设 $y = y(u)$，$u = u(x)$。
则 $dy = \frac{dy}{dx}\cdot dx$，$\because y\to u\to x$
$$\therefore \frac{dy}{dx} = \frac{dy}{du}\cdot \frac{du}{dx}$$
$$
\begin{aligned}
\therefore dy &= \left( \frac{dy}{du}\cdot \frac{du}{dx} \right) dx \\
&= \frac{dy}{du}\cdot du
\end{aligned}
$$
$$\Rightarrow dy = \frac{dy}{du}du$$

### 二元函数微分形式不变性的证明
设 $z = z(u,v)$，$u = u(x,y)$，$v = v(x,y)$。
则
$$dz = \frac{\partial z}{\partial x}dx + \frac{\partial z}{\partial y}dy.$$
$\because$ 复合函数变量依赖关系示意图：$z$ 依赖中间变量 $u,v$，$u,v$ 均同时依赖自变量 $x,y$。

---

# O 多元函数微分的计算_第9页.png

## 一阶全微分形式不变性推导
对复合函数$z=f(u,v)$，其中$u=u(x,y), v=v(x,y)$，由多元复合函数偏导链式法则：
$$\frac{\partial z}{\partial x} = \frac{\partial z}{\partial u}\cdot\frac{\partial u}{\partial x} + \frac{\partial z}{\partial v}\cdot\frac{\partial v}{\partial x}$$
$$\frac{\partial z}{\partial y} = \frac{\partial z}{\partial u}\cdot\frac{\partial u}{\partial y} + \frac{\partial z}{\partial v}\cdot\frac{\partial v}{\partial y}$$

写出全微分并整理公因子：
$$
\begin{aligned}
\therefore \mathrm{d}z &= \left( \frac{\partial z}{\partial u}\frac{\partial u}{\partial x} + \frac{\partial z}{\partial v}\frac{\partial v}{\partial x} \right)\mathrm{d}x + \left( \frac{\partial z}{\partial u}\frac{\partial u}{\partial y} + \frac{\partial z}{\partial v}\frac{\partial v}{\partial y} \right)\mathrm{d}y \\
&= \frac{\partial z}{\partial u}\left( \frac{\partial u}{\partial x}\mathrm{d}x + \frac{\partial u}{\partial y}\mathrm{d}y \right) + \frac{\partial z}{\partial v}\left( \frac{\partial v}{\partial x}\mathrm{d}x + \frac{\partial v}{\partial y}\mathrm{d}y \right)
\end{aligned}
$$

由中间变量的全微分定义：
$\because u=u(x,y),\quad \mathrm{d}u = \frac{\partial u}{\partial x}\mathrm{d}x + \frac{\partial u}{\partial y}\mathrm{d}y$
$v=v(x,y),\quad \mathrm{d}v = \frac{\partial v}{\partial x}\mathrm{d}x + \frac{\partial v}{\partial y}\mathrm{d}y$

代入后得到结论：
$$\therefore \implies \mathrm{d}z = \frac{\partial z}{\partial u}\mathrm{d}u + \frac{\partial z}{\partial v}\mathrm{d}v$$

## 性质意义
当你计算一阶全微分时，可以像对待自变量一样对待中间变量，就极大地简化了计算的复杂度。

## 应用举例：多元复合函数求微分
给定多层复合函数的变量依赖关系：
$F=F(u,v)$，其中
$$
\begin{cases}
u=u(x,y,z), & z=z(x,y) \\
v=v(x,y,z), & y=y(x)
\end{cases}
$$

（复合函数链式结构示意图）
链式结构很复杂，用形式不变性无脑直接写。

逐层写出微分表达式：
$$\mathrm{d}F = \frac{\partial F}{\partial u}\mathrm{d}u + \frac{\partial F}{\partial v}\mathrm{d}v$$
$$\mathrm{d}u = \frac{\partial u}{\partial x}\mathrm{d}x + \frac{\partial u}{\partial y}\mathrm{d}y + \frac{\partial u}{\partial z}\mathrm{d}z$$
$$\mathrm{d}v = \frac{\partial v}{\partial x}\mathrm{d}x + \frac{\partial v}{\partial y}\mathrm{d}y + \frac{\partial v}{\partial z}\mathrm{d}z$$

---

# O 多元函数微分的计算_第10页.png

$$dz = \frac{\partial z}{\partial x}dx + \frac{\partial z}{\partial y}dy$$
$$dy = \frac{dy}{dx}dx$$
$$dx = \frac{dx}{dx}dx$$

## 例13.12
若函数$z=z(x,y)$由方程
$$e^{x+2y+3z} + xyz = 1$$
确定，求$\left.dz\right|_{(0,0)}$。

### 分析
用全微分形式不变性去解。

解：
$$\because \begin{cases}
x=0 \\
y=0 \\
e^{x+2y+3z} + xyz - 1 = 0
\end{cases}$$
$\implies z=0$
$\therefore \left.z=z(x,y)\right|_{(0,0)} = 0$

对式子微分，得出$dz$：
令$u = u(x,y,z) = x+2y+3z$，
$v = v(x,y,z) = xyz$，
$F = F(u,v) = e^u + v - 1 = 0$。

$\because dF = \frac{\partial F}{\partial u}du + \frac{\partial F}{\partial v}dv$
$\therefore$
$$
\begin{aligned}
dF &= \frac{\partial(e^u)}{\partial u}du + \frac{\partial v}{\partial v}dv \\
&= e^u du + dv = 0
\end{aligned}
$$

---

# O 多元函数微分的计算_第11页.png

$\because du = \frac{\partial u}{\partial x}dx + \frac{\partial u}{\partial y}dy + \frac{\partial u}{\partial z}dz$
$dv = \frac{\partial v}{\partial x}dx + \frac{\partial v}{\partial y}dy + \frac{\partial v}{\partial z}dz$
$\therefore du = dx + 2dy + 3dz$
$dv = yzdx + xzdy + xydz$
$\Rightarrow e^{(x+2y+3z)}\cdot (dx+2dy+3dz) + yzdx + xzdy + xydz = 0$
代入$x=0,y=0,z=0$：
$\Rightarrow dx + 2dy + 3dz = 0$
整理得：
$$dz = -\frac{1}{3}dx - \frac{2}{3}dy$$

## 隐函数存在定理
### 定理1
对于由方程$F(x,y)=0$在点$(x_0,y_0)$处所确定的隐函数$y=f(x)$，当$F_y'(x,y)\neq 0$时，有
$$\frac{dy}{dx} = -\frac{F_x'(x,y)}{F_y'(x,y)}$$

#### 理解
由隐函数存在定理知：
若$F(x,y)=0$在点$(x_0,y_0)$处可以确定$y=y(x)$，则有
$$\frac{dy}{dx} = -\frac{F_x'}{F_y'}$$
若在点$(x_0,y_0)$处$F_y'=0$，$F_x'\neq 0$，则在点$(x_0,y_0)$处$\frac{dy}{dx}=\infty$。

> 函数示意图：平面直角坐标系$xOy$，曲线在$x=x_0$处存在垂直于$x$轴的切线，$x=x_0$对应多个$y$值。

发现，出现了一个$x=x_0$值对应多个$y$值的情况，就不符合函数定义了，在点$(x_0,y_0)$处，就确定不了$y=y(x)$。

---

# O 多元函数微分的计算_第12页.png

## 隐函数存在的特殊情形（$F_y'=0$的情况）
若在点$(x_0,y_0)$处，$F_y'\neq0$，$F_x'=0$，
则在点$(x_0,y_0)$处$\frac{dy}{dx}$为实数，是有斜率的，
在点$(x_0,y_0)$处能确定一个函数$y=y(x)$。

若在点$(x_0,y_0)$处，按极限来看，当$\substack{x\to x_0 \\ y\to y_0}$时，
$$F_y'\to0,\quad F_x'\to0$$
则$\frac{dy}{dx}$有三种可能的结果：$\infty$、实数、$0$，
则在点$(x_0,y_0)$处，
可能确定一个函数$y=y(x)$，
也可能不能确定一个函数。

例：$F(x,y)=(y-x)^2=0$
在点$(0,0)$处，
确定一函数$y=x$。

但$F_y'=2(y-x)$，
$$\left.F_y'\right|_{(0,0)}=0$$
因为$F_x'=-2(y-x)$，
$$\left.F_x'\right|_{(0,0)}=0$$

$$\frac{dy}{dx}=-\frac{F_x'}{F_y'}=\frac{2(y-x)}{2(y-x)}$$

$$\lim_{\substack{x\to0 \\ y\to0}} \frac{2(y-x)}{2(y-x)}=1 = \left.\frac{dy}{dx}\right|_{(0,0)}$$

则在$\left.F_y'\right|_{(0,0)}=0$时，
在$(0,0)$点处，也可确定一函数$y=x$。

例：$F(x,y)=x^3-xy=0$
在点$(0,0)$处，
确定一函数$y=x^2$。

---

# O 多元函数微分的计算_第13页.png

但 $F_y'=-x$
$$\left.F_y'\right|_{(0,0)}=0$$

证明：
$F_x'=3x^2-y$
$$\left.F_x'\right|_{(0,0)}=0$$
$$\frac{dy}{dx}=-\frac{F_x'}{F_y'}=\frac{3x^2-y}{x}$$

$\because y=x^2$
$$\therefore \lim\limits_{\substack{x\to0\\y\to0}} \frac{dy}{dx} = \lim\limits_{\substack{x\to0\\y\to0}} \frac{3x^2-y}{x} \xlongequal{\text{代入}y=x^2}$$
$$= \lim\limits_{\substack{x\to0\\y\to0}} \frac{2x^2}{x}=0$$

则在点$(0,0)$处可确定 $y=x^2$

## 定理1的证明：
$\because y=f(x)$
$\therefore F(x,y)=F(x,f(x))=0$
即$F(x,y)=0$，旁附复合函数链式法则示意图：函数$F$包含两个中间变量，编号1对应$x$，编号2对应$y$，两个中间变量最终均指向自变量$x$。

两边同时对$x$求导
$\Rightarrow$
$$F_1'\cdot 1 + F_2'\cdot \frac{dy}{dx}=0$$
$$\frac{dy}{dx}=-\frac{F_1'}{F_2'} \quad \text{且} \ F_2'\neq0$$

## 定理2
对于由方程$F(x,y,z)=0$，在点$(x_0,y_0,z_0)$处确定的隐函数$z=z(x,y)$，当$F_z'\neq0$时，有
$$\frac{\partial z}{\partial x}=-\frac{F_x'}{F_z'}, \quad \frac{\partial z}{\partial y}=-\frac{F_y'}{F_z'}$$

---

# O 多元函数微分的计算_第14页.png

## 定理2的证明
$F(x,y,z)=0$
两边同时对$x$求偏导，
$y$看作常数：
$$F_1'\cdot 1 + F_3'\cdot \frac{\partial z}{\partial x} = 0$$
$$\Rightarrow \frac{\partial z}{\partial x} = -\frac{F_1'}{F_3'}, \quad 且 \ F_3'\neq 0$$

$F(x,y,z)=0$
两边同时对$y$求偏导，
$x$看作常数：
$$F_2'\cdot 1 + F_3'\cdot \frac{\partial z}{\partial y} = 0$$
$$\Rightarrow \frac{\partial z}{\partial y} = -\frac{F_2'}{F_3'}, \quad 且 \ F_3'\neq 0$$

## 例13.13
设有三元方程$xy - z\ln y + e^{xz} = 1$，
根据隐函数存在定理，
存在点$(0,1,1)$的一个邻域，
写出在此邻域内
该方程能确定的隐函数。
### 分析
由隐函数存在定理知：
若$\frac{\partial z}{\partial x} = -\frac{F_x'}{F_z'}$ 或 $\frac{\partial z}{\partial y} = -\frac{F_y'}{F_z'}$，
则在点$(x_0,y_0,z_0)$处就确定了
$z=z(x,y)$这个隐函数存在，
要求$F_z'\neq 0$。
若在点$(x_0,y_0,z_0)$处，$F_z'=0$，
则就不能确定$z=z(x,y)$。
∴ 你就看导数是否为0就行。

---

# O 多元函数微分的计算_第15页.png

解：令 $F(x,y,z)=xy - z\ln y + e^{xz} -1 = 0$
至于 $x=x(y,z)$，$y=y(x,z)$，$z=z(x,y)$，哪个可以确定？
计算偏导数：
$$F_x' = y + z e^{xz} \implies F_x'|_{(0,1,1)} = 2 \neq 0$$
$$F_y' = x - \frac{z}{y} \implies F_y'|_{(0,1,1)} = -1 \neq 0$$
$$F_z' = -\ln y + x e^{xz} \implies F_z'|_{(0,1,1)} = 0$$
则在点$(0,1,1)$处可以确定隐函数：
$$x=x(y,z)$$
$$y=y(x,z)$$

## 例13.14
“全面且真正的隐函数存在定理的描述”

设$F(x,y)$在点$(x_0,y_0)$处的某邻域内，有连续的偏导数，且$F(x_0,y_0)=0$。
问：$F_y'(x_0,y_0)\neq0$是$F(x,y)=0$在$(x_0,y_0)$处的某邻域内能确定一个连续函数$y=y(x)$且满足$y_0=y(x_0)$，并有连续导数的______条件。

分析：根据前面的隐函数存在定理知，这个正着推是成立的，即为充分条件。
根据前面的“理解”知：
- $F_y'\neq0$，可以确定$y=y(x)$
- $F_y'=0$，也可以确定$y=y(x)$

即，若$y=y(x)$确定，则$F_y'=0$或$F_y'\neq0$。

$\because$
$A\Rightarrow B$，其中$A$为$F_y'\neq0$，$B$为$y=y(x)$确定；
$A\nLeftarrow B$。

---

# O 多元函数微分的计算_第16页.png

$\therefore \Rightarrow$
$y=y(x)$确定 $\not\Rightarrow F_y'\neq0$
$y=y(x)$确定 $\Leftarrow F_y'\neq0$

解：为充分不必要条件。

## 例13.15
若函数$z=z(x,y)$
由方程$e^{x+2y+3z}+xyz=1$确定
求$\left.dz\right|_{(0,0)}$

### 分析
（隐函数变量依赖关系示意图）
用公式法：
$$dz = \frac{\partial z}{\partial x}dx + \frac{\partial z}{\partial y}dy$$
$$\frac{\partial z}{\partial x} = -\frac{F_x'}{F_z'}$$
$$\frac{\partial z}{\partial y} = -\frac{F_y'}{F_z'}$$

### 注意
要求出$F_x',F_y',F_z'$
$F$对$z$求导时，$x,y$当常数看
$F$对$x$求导时，$y,z$当常数看

解：
令$F(x,y,z)=e^{x+2y+3z}+xyz-1=0$
$$
\begin{align*}
\frac{\partial z}{\partial y} &= -\frac{F_y'}{F_z'} \\
&= -\frac{2e^{x+2y+3z} + xz}{3e^{x+2y+3z} + xy}
\end{align*}
$$
$$
\begin{align*}
\frac{\partial z}{\partial x} &= -\frac{F_x'}{F_z'} \\
&= -\frac{e^{x+2y+3z} + yz}{3e^{x+2y+3z} + xy}
\end{align*}
$$

---

# O 多元函数微分的计算_第17页.png

$$
\begin{cases}
x=0\\
y=0\\
e^{x+2y+3z} + xyz -1 = 0
\end{cases}
$$
代入解得$z=0$，因此$\left.z(x,y)\right|_{(0,0)} = 0$。

将$x=0,y=0,z=0$代入计算$\frac{\partial z}{\partial x}$与$\frac{\partial z}{\partial y}$，得：
$$\left.\frac{\partial z}{\partial x}\right|_{(0,0)} = -\frac{1}{3},\quad \left.\frac{\partial z}{\partial y}\right|_{(0,0)} = -\frac{2}{3}$$

由全微分公式：
$$dz = \frac{\partial z}{\partial x}dx + \frac{\partial z}{\partial y}dy$$
因此$(0,0)$处的全微分为：
$$\left.dz\right|_{(0,0)} = -\frac{1}{3}dx - \frac{2}{3}dy$$

## 例13.16
设函数$z=z(x,y)$由方程
$$F\left(x+\frac{z}{y},\, y+\frac{z}{x}\right)=0$$
所确定，其中$F$具有连续偏导数，且$xF_1'+yF_2'\neq 0$，求$x\frac{\partial z}{\partial x} + y\frac{\partial z}{\partial y}$。

## 分析
例13.15是两层复合函数：
- 第一层：$F=F(x,y,z)$
- 第二层：$z=z(x,y)$
（两层复合函数变量依赖关系示意图）

这一题是多了一层，为三层复合函数：
- 第一层：$F=F(u,v)$
- 第二层：$u=u(x,y,z),\ v=v(x,y,z)$，其中$u=x+\frac{z}{y},\ v=y+\frac{z}{x}$
- 第三层：$z=z(x,y)$
（三层复合函数变量依赖关系示意图）

---

# O 多元函数微分的计算_第18页.png

## 隐函数偏导计算例题
与例13.15同类型。
我们令 $G(x,y,z) = F\left(x+zy^{-1}, y+zx^{-1}\right)$
解：令 $G(x,y,z) = F\left(x+\frac{z}{y}, y+\frac{z}{x}\right)$
根据隐函数求导法则，若方程$G(x,y,z)=0$确定隐函数$z=z(x,y)$，则有$\frac{\partial z}{\partial x} = -\frac{G_x'}{G_z'}$，$\frac{\partial z}{\partial y} = -\frac{G_y'}{G_z'}$。
（附复合函数变量依赖示意图：$F$包含两个中间变量位置1、2，分别与$x,y,z$存在复合关系）
对$x$求偏导时，对$F$中标记$x$的位置求导，将$y,z$视为常数；对标记$z$的位置求导同理，计算得：
$$
\frac{\partial z}{\partial x} = -\frac{G_x'}{G_z'} = -\frac{F_1'\cdot 1 + F_2'\cdot\left(-\frac{z}{x^2}\right)}{F_1'\cdot \frac{1}{y} + F_2'\cdot \frac{1}{x}}
$$
对$y$求偏导时，对$F$中标记$y$的位置求导，将$x,z$视为常数；对标记$z$的位置求导同理，计算得：
$$
\frac{\partial z}{\partial y} = -\frac{G_y'}{G_z'} = -\frac{F_1'\cdot\left(-\frac{z}{y^2}\right) + F_2'\cdot 1}{F_1'\cdot \frac{1}{y} + F_2'\cdot \frac{1}{x}}
$$
计算$x\frac{\partial z}{\partial x} + y\frac{\partial z}{\partial y}$：
$$
\begin{aligned}
x\frac{\partial z}{\partial x} + y\frac{\partial z}{\partial y}
&= -\frac{x F_1' - F_2'\cdot \frac{z}{x}}{F_1'\cdot \frac{1}{y} + F_2'\cdot \frac{1}{x}} - \frac{-F_1'\cdot \frac{z}{y} + y F_2'}{F_1'\cdot \frac{1}{y} + F_2'\cdot \frac{1}{x}} \\
&= \frac{\left(\frac{z}{y} - x\right)F_1' + \left(\frac{z}{x} - y\right)F_2'}{F_1'\cdot \frac{1}{y} + F_2'\cdot \frac{1}{x}} \quad \text{上下同乘 } xy \\
&= \frac{(xz - x^2 y)F_1' + (yz - xy^2)F_2'}{x F_1' + y F_2'} \\
&= \frac{x(z-xy)F_1' + y(z-xy)F_2'}{x F_1' + y F_2'} \\
&= \frac{(z-xy)\left(x F_1' + y F_2'\right)}{x F_1' + y F_2'} \\
&= z - xy
\end{aligned}
$$