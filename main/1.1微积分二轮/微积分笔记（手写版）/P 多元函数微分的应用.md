---

# P 多元函数微分的应用_第1页.png

# 多元函数的应用
## 极值与最值
**概念**
- 极值：若存在点$(x_0,y_0)$的某个邻域，使得在该邻域内任意一点$(x,y)$，均有
$$f(x_0,y_0)\geq f(x,y) \quad \text{或} \quad f(x_0,y_0)\leq f(x,y)$$
成立，则称点$(x_0,y_0)$为$f(x,y)$的极大值点/极小值点，$f(x_0,y_0)$为$f(x,y)$的极大值/极小值。
- 最值：设点$(x_0,y_0)$为$f(x,y)$定义域内一点，若对于$f(x,y)$的定义域内任意一点$(x,y)$，均有
$$f(x_0,y_0)\geq f(x,y) \quad \text{或} \quad f(x_0,y_0)\leq f(x,y)$$
成立，则称$f(x_0,y_0)$为$f(x,y)$的最大值/最小值。

**理解**
- 极值：你在你周围的同学中，分最高
- 最值：你在你全班的同学中，分最高
- 就比如说：你的脸是一个三维面，脸上长了好几个小痘痘，每个小痘痘上都有一个极大值点，但整个脸上只有一个最大值点。

**例13.17**
问：二元函数$f(x,y)$在点$(x_0,y_0)$处取得极值，是一元函数$f(x,y_0)$和$f(x_0,y)$分别在$x_0$和$y_0$处取得极值的______条件

**分析**
二元函数$f(x,y)$的图像位于三维坐标系中，$z=f(x_0,y)$是该曲面上的曲线：
在$x=x_0$处插一个与$y$轴平行的截面，
在这个截面上，
该曲线对应二维坐标系中的一元函数$f(x_0,y)$，
其中，$z$随$y$的变化而变化，
在$y=y_0$时，
$z$取极值$f(x_0,y_0)$。

---

# P 多元函数微分的应用_第2页.png

## $z=f(x,y_0)$的图象
是在三维坐标系中的二元函数$f(x,y)$上，在$y=y_0$处插一个与$x$轴平行的截面。
在这个截面上
就是一个二维坐标系中的一元函数$f(x,y_0)$
其中，$z$随$x$的变化而变化
在$x=x_0$时，$z$取得极值$f(x_0,y_0)$
（具体图像见偏导数那里）

充分条件是显然的
因为在所有方向上，$f(x_0,y_0)$都为极值
那么，在$x$轴、$y$轴方向上依旧为极值
反过来看是不行的
因为只能确定在$x$轴、$y$轴方向上
$f(x_0,y_0)$为极值
不能确定在所有方向上
$f(x_0,y_0)$为极值

∴ 解：充分不必要

## 例13.18
设函数$f(x,y)$具有二阶连续偏导数
且在点$(x_0,y_0)$处取得极大值$f(x_0,y_0)$
记
$$a=\left.\frac{\partial^2 f}{\partial x^2}\right|_{(x_0,y_0)},\ b=\left.\frac{\partial^2 f}{\partial y^2}\right|_{(x_0,y_0)}$$
则$\underline{\qquad\qquad}$
A. $a>0,\ b>0$　　　　B. $a\geq0,\ b\geq0$
C. $a<0,\ b<0$　，　D. $a\leq0,\ b\leq0$

### 分析
随手举个简单的例子
看看能否秒出答案（排除法）
举例，$f(x,y)=-(x^2+y^2)$
$f''_{xx}=-2$，$a=\left.f''_{xx}\right|_{(0,0)}=-2$
$f''_{yy}=-2$，$b=\left.f''_{yy}\right|_{(0,0)}=-2$

---

# P 多元函数微分的应用_第3页.png

## 举例2
给定函数 $f(x,y) = -(x^4 + y^4)$，计算其二阶偏导数：
$$f_{xx}'' = -12x^2,\quad \left.f_{xx}''\right|_{(0,0)} = 0$$
$$f_{yy}'' = -12y^2,\quad \left.f_{yy}''\right|_{(0,0)} = 0$$
$\Rightarrow$ 选D

这种排除法适合在考场上秒杀选择题，在其他题目中有需要时也可以使用，以此验证答案。

## 深入理解，简化视角
计算$a = \left.\frac{\partial^2 f}{\partial x^2}\right|_{(x_0,y_0)}$时，始终是对$x$求偏导，$y$一直被当作常数处理，因此：
$$a = \left.\frac{\partial^2 f(x,y)}{\partial x^2}\right|_{(x_0,y_0)} = \left.\frac{d^2 f(x,y_0)}{d x^2}\right|_{x=x_0}$$

上述思路相当于是例1317中的方法：
若$y$取固定值，即$y=y_0$，那么3维坐标系中的二元函数对$x$求偏导，就可以看作是2维坐标系中的一元函数对$x$求全导。

要注意的是：这里将变量$y$看作定量$y_0$，二元函数便可看作一元函数。
令$g(x) = f(x,y_0)$，则有：
$$\left.g''(x)\right|_{x=x_0} = \left.\frac{\partial^2 f(x,y)}{\partial x^2}\right|_{(x_0,y_0)}$$

因此我们完全可以用一元函数微分应用的知识来解此类题。
浅浅回顾一下之前的知识，会举出以下典例。

---

# P 多元函数微分的应用_第4页.png

## 无条件极值（极值的判别与寻找）
### 可疑点（compare）
#### 一元函数情形
$y=f(x)$在点$x=x_0$处满足$\begin{cases} 可导 \\ 取极值 \end{cases} \implies f'(x_0)=0$
$f'(x_0)=0 \implies y=f(x)$在$x=x_0$处的切线水平
**注**：导数不存在的点也可能是极值点
例：尖点情形，$y=\sqrt{x^2}=|x|$在点$x=0$处取极小值
注意：
- $f'(x_0)=0 \nRightarrow y=f(x)$在点$x=x_0$处取极值
- $f'(x_0)$不存在$\nRightarrow y=f(x)$在点$x=x_0$处取极值

---

#### 一元函数极大值示例
1.  推导过程：
$$f''(x)=-2 \implies f'(x)=-2x \implies f(x)=-x^2$$
对应3幅函数示意图：分别为$f''(x)$、$f'(x)$、$f(x)=-x^2$在$x_0$处的图像，$f(x)$在$x_0$处取极大值，$f''(x_0)=-2<0$。

2.  推导过程：
$$f''(x)=-12x^2 \implies f'(x)=-4x^3 \implies f(x)=-x^4$$
对应3幅函数示意图：分别为$f''(x)$、$f'(x)$、$f(x)=-x^4$在$x_0$处的图像，$f(x)$在$x_0$处取极大值，$f''(x_0)=0$。

---

#### 二元函数极值必要条件推导
则我们可以得出：
$\because f(x,y)$在点$(x_0,y_0)$处取得极大值
$\therefore$ 一元函数$g(x)=f(x,y_0)$在$x=x_0$处取得极大值
$$\therefore \left. g''(x) \right|_{x=x_0} = \left. \frac{\partial^2 f}{\partial x^2} \right|_{(x_0,y_0)} \le 0$$
同理可得：
$$b = \left. \frac{\partial^2 f}{\partial y^2} \right|_{(x_0,y_0)} \le 0$$

---

解：选D

---

# P 多元函数微分的应用_第5页.png

eg：
$f'(x)=3x^2$，$f(x)=x^3$
（此处有两个函数示意图：第一个为开口向上、顶点在原点的抛物线；第二个为$f(x)=x^3$的立方抛物线图像，过原点，在原点处与x轴相切）
只能说：满足以下条件的点为可疑点，即可能为极值点的点：
$$\begin{cases}
f'(x)=0\text{的点} \\
f'(x)\text{不存在的点}
\end{cases}$$

## 多元函数极值
若$z=f(x,y)$在点$(x_0,y_0)$处满足：
$$\begin{cases}
\text{一阶偏导数存在} \\
\text{取极值}
\end{cases}$$
则必有：
$$f_x'(x_0,y_0)=0,\ f_y'(x_0,y_0)=0$$
且有如下推出关系：
$$\begin{cases}
f_x'(x_0,y_0)=0 \\
f_y'(x_0,y_0)=0
\end{cases} \Rightarrow \begin{matrix}
z=f(x,y)\text{在点}(x_0,y_0)\text{处} \\
\text{的切平面水平}
\end{matrix}$$

注：偏导数不存在的点也可能为极值点。
eg：圆锥的尖点，$z=\sqrt{x^2+y^2}$在点$(x_0,y_0)$处取极小值。
$$\begin{cases}
f_x'\text{不存在} \\
f_y'\text{不存在}
\end{cases} \nRightarrow z=f(x,y)\text{在点}(x_0,y_0)\text{处取极值}$$
$$\begin{cases}
f_x'(x_0,y_0)=0 \\
f_y'(x_0,y_0)=0
\end{cases} \nRightarrow z=f(x,y)\text{在点}(x_0,y_0)\text{处取极值}$$

eg：
- $f(x,y)=x^3+y^3$
- $f(x,y)=x^2-y^2$

只能说：
$$\begin{cases}
f_x'(x_0,y_0)=0 \\
f_y'(x_0,y_0)=0
\end{cases}\text{的点}(x_0,y_0)$$
$$\begin{cases}
f_x'\text{不存在} \\
f_y'\text{不存在}
\end{cases}\text{的点}(x_0,y_0)$$
为可疑点，即可能为极值点的点。

---

# P 多元函数微分的应用_第6页.png

## 判断可疑点是否为极值点（Δ判别法）
$$
\begin{cases}
f_{xx}''(x_0,y_0)=A \\
f_{xy}''(x_0,y_0)=B \\
f_{yy}''(x_0,y_0)=C
\end{cases}
\quad \Delta=AC-B^2
$$
若：
- $\Delta>0 \implies$ 极值，其中：
  $$
  \begin{cases}
  A<0 \ \text{或} \ C<0 \implies \text{极大值} \\
  A>0 \ \text{或} \ C>0 \implies \text{极小值}
  \end{cases}
  $$
- $\Delta<0 \implies$ 不是极值
- $\Delta=0 \implies$ 方法失效，另谋它法
### 理解
$$
\begin{aligned}
AC-B^2 &> 0 \\
\implies AC &> B^2
\end{aligned}
$$
$\because B^2\geq0$
$\therefore A$与$C$同号。
若$\Delta>0 \implies A$与$C$同号。
## 小结
找$z=f(x,y)$的极值点的思路：
- 找可能为极值点的可疑点：
  即满足
  $$\begin{cases}
  f_x'(x_0,y_0)=0 \\
  f_y'(x_0,y_0)=0
  \end{cases}$$
  的点，
  或满足
  $$\begin{cases}
  f_x' \text{不存在} \\
  f_y' \text{不存在}
  \end{cases}$$
  的点。
- 找确定为极值点的点：
  即满足$\Delta>0$的点。
因此极值点满足：
$$
\begin{cases}
f_x'=0 \ \text{或} \ f_x' \text{不存在} \\
f_y'=0 \ \text{或} \ f_y' \text{不存在} \\
\Delta>0
\end{cases}
$$

---

# P 多元函数微分的应用_第7页.png

## 例13.19
函数$z=z(x,y)$由方程
$$(x^2+y^2)z + \ln z + 2(x+y+1)=0$$
确定，求$z(x,y)$的极值。
## 分析
先求$z$的一阶偏导：
采用隐函数求导法，直接对方程两边求偏导，即可得到$z$的一阶偏导。
对$x$求一阶偏导的注意要点：
- 将$y$视为常数
- 将$z$视为关于$x,y$的函数$z(x,y)$
- 遵循求导法则计算，例如乘积求导法则：$[xf(x)]' = (x)'f(x) + x[f(x)]'$
- 整理后即可解出$\frac{\partial z}{\partial x}$
对$y$求一阶偏导的方法同理。
求出$\frac{\partial z}{\partial x}$与$\frac{\partial z}{\partial y}$后，寻找可疑极值点：
令
$$\begin{cases}
\displaystyle \frac{\partial z}{\partial x}=0 \\
\displaystyle \frac{\partial z}{\partial y}=0
\end{cases}$$
解出对应的$x,y$。
找出可疑点后，使用$\Delta$判别法进一步判别该点是否为极值点。
> 注：将$\begin{cases}
\displaystyle \frac{\partial z}{\partial x}=0 \\
\displaystyle \frac{\partial z}{\partial y}=0
\end{cases}$代入求导后的方程，可简化计算过程。
## 解
对方程两边分别求关于$x$和$y$的一阶偏导：
求关于$x$的偏导（$y$视为常数，$z$视为$x,y$的函数），得：
$$2xz + (x^2+y^2)\frac{\partial z}{\partial x} + \frac{1}{z}\cdot\frac{\partial z}{\partial x} + 2 = 0 \tag{1}$$
同理，求关于$y$的偏导（$x$视为常数，$z$视为$x,y$的函数），得：
$$2yz + (x^2+y^2)\frac{\partial z}{\partial y} + \frac{1}{z}\cdot\frac{\partial z}{\partial y} + 2 = 0 \tag{2}$$
令一阶偏导为0，即
$$\begin{cases}
\displaystyle \frac{\partial z}{\partial x}=0 \\
\displaystyle \frac{\partial z}{\partial y}=0
\end{cases}$$
将其代入(1)(2)，可得：
$$\begin{cases}
2xz + 2 = 0 \\
2yz + 2 = 0
\end{cases} \implies \begin{cases}
x=-\dfrac{1}{z} \\
y=-\dfrac{1}{z}
\end{cases}$$

---

# P 多元函数微分的应用_第8页.png

## 二元隐函数极值求解
将$\begin{cases}x=-\dfrac{1}{2}\\[6pt]y=-\dfrac{1}{2}\end{cases}$代入原式
$$\implies \ln z - \frac{2}{z} + 2 = 0$$

这是一个超越方程，可用“观察法”与“试错法”

可直接看出$z=1$

解得$z=1 \implies \begin{cases}x=-1\\y=-1\end{cases}$，即可疑点$(-1,-1)$

①式对$x$求偏导
$\implies$③
$$2z+2x\cdot z_x'+2x\cdot z_x'+(x^2+y^2)z_{xx}''+\left(-\frac{1}{z^2}\right)\cdot(z_x')^2+\frac{1}{z}\cdot z_{xx}''=0$$

①式对$y$求偏导
$\implies$④
$$2x\cdot z_y'+2y\cdot z_x'+(x^2+y^2)\cdot z_{xy}''+\left(-\frac{1}{z^2}\right)\cdot z_y'\cdot z_x'+\frac{1}{z}\cdot z_{xy}''=0$$

②式对$y$求偏导
$\implies$⑤
$$2z+2y\cdot z_y'+2y\cdot z_y'+(x^2+y^2)z_{yy}''+\left(-\frac{1}{z^2}\right)\cdot(z_y')^2+\frac{1}{z}\cdot z_{yy}''=0$$

将$\begin{cases}\dfrac{\partial z}{\partial x}=0\\[6pt]\dfrac{\partial z}{\partial y}=0\end{cases}$代入得
$$
\begin{cases}
2z+(x^2+y^2)z_{xx}''+\dfrac{1}{z}\cdot z_{xx}''=0 & \text{⑥}\\[6pt]
(x^2+y^2)\cdot z_{xy}''+\dfrac{1}{z}\cdot z_{xy}''=0 & \text{⑦}\\[6pt]
2z+(x^2+y^2)\cdot z_{yy}''+\dfrac{1}{z}\cdot z_{yy}''=0 & \text{⑧}
\end{cases}
$$

$\because x=-1,y=-1$时$z=1$

$\therefore$将$\begin{cases}x=-1\\y=-1\\z=1\end{cases}$代入⑥⑦⑧$\implies \Delta=\dfrac{4}{9}>0$

$\because x=-1<0,y=-1<0$

$\therefore z(-1,-1)$为极大值

---

# P 多元函数微分的应用_第9页.png

## 条件最值与拉格朗日乘数法
（最值的判别与寻找）

求目标函数 $u = f(x,y,z)$ 在约束条件
$$\begin{cases}
\varphi(x,y,z) = 0 \\
w(x,y,z) = 0
\end{cases}$$
下的最值。

① 构造辅助函数
$$F(x,y,z,\lambda,\mu) = f(x,y,z) + \lambda \varphi(x,y,z) + \mu w(x,y,z)$$

② 令
$$\begin{cases}
F'_x = f'_x + \lambda \varphi'_x + \mu w'_x = 0 \\
F'_y = f'_y + \lambda \varphi'_y + \mu w'_y = 0 \\
F'_z = f'_z + \lambda \varphi'_z + \mu w'_z = 0 \\
F'_\lambda = \varphi(x,y,z) = 0 \\
F'_\mu = w(x,y,z) = 0
\end{cases}$$

③ 解方程组，得出可能为最值点的点
将这些点代入 $f(x,y,z)$，
最小的为最小值，
最大的为最大值。

💡 理解
构造辅助函数时，
有$n$个约束就多加$n$个自变量，
自变量个数 $=$ 目标函数的自变量个数 $+$ 约束条件的个数，
自变量有$n$个就求$n$个一阶偏导数。

💡 注：若从约束条件
$$\begin{cases}
\varphi(x,y,z) = 0 \\
w(x,y,z) = 0
\end{cases}$$
中可解出 $z = z(x,y)$，则将其代入 $f(x,y,z)$，得 $f[x,y,z(x,y)]$，就转化为了无条件最值问题。

---

# P 多元函数微分的应用_第10页.png

## 有界闭区域上连续函数的最值问题
### 理论依据——最大最小值定理
在有界闭区域$D$上的多元连续函数，在区域$D$上，一定有最小值和最大值。
### 求法
- 根据$f_x',f_y'$为0或不存在，求出区域$D$内部的所有可疑点。
- 用拉格朗日乘数法或代入法，求出区域$D$边界上的所有可疑点。
- 比较以上所有可疑点的函数值大小，取其最小者为最小值，最大者为最大值。
### 与一元函数求法 compare
- 根据$f'(x)$为0或不存在，求可疑点。
- 取端点为可疑点。
- 比较所有可疑点的函数值。
### 例13.22
已知函数$z = f(x,y) = x^2 - y^2 + 2$，求$f(x,y)$在椭圆域$D = \left\{(x,y)\mid x^2 + \frac{y^2}{4} \leq 1\right\}$上的最大值和最小值。
#### 分析
∵ 给出了$z=x^2-y^2+2$
∴ 可求出区域$D$内部的可疑点：
即满足$\begin{cases} f_x'=0 \\ f_y'=0 \end{cases}$的点，或$\begin{cases} f_x'不存在 \\ f_y'不存在 \end{cases}$的点。
求区域$D$边界上的可疑点：
∵ 由题可知$D = \left\{(x,y)\mid x^2 + \frac{y^2}{4} \leq 1\right\}$

---

# P 多元函数微分的应用_第11页.png

## 拉格朗日乘数法求椭圆域上二元函数的最值
$\therefore$ 区域$D$为一个椭圆轮廓的区域
则我们要求的是椭圆轮廓上的点，若这点满足椭圆方程，则就是在这个椭圆轮廓上，这就是一个约束。
即求目标函数 $z = x^2 - y^2 + 2$ 在约束条件$\varphi = x^2 + \frac{y^2}{4} - 1 = 0$下的最值，很明显用拉格朗日乘数法求解。

**解：**
在$D$内的可疑点：
$$\frac{\partial z}{\partial x} = 2x,\quad \frac{\partial z}{\partial y} = -2y$$
令
$$
\begin{cases}
\displaystyle \frac{\partial z}{\partial x} = 0 \\[6pt]
\displaystyle \frac{\partial z}{\partial y} = 0
\end{cases}
$$
解得$x=0,\,y=0$，即$(0,0)$点，且偏导数没有无定义点。

在$D$上的可疑点：
构造拉格朗日函数
$$F(x,y,\lambda) = x^2 - y^2 + 2 + \lambda\left(x^2 + \frac{y^2}{4} - 1\right)$$
列偏导为零的方程组：
$$
\begin{cases}
F_x' = 2x + 2\lambda x = 0 \\[6pt]
F_y' = -2y + \frac{\lambda}{2} y = 0 \\[6pt]
F_\lambda' = x^2 + \frac{y^2}{4} - 1 = 0
\end{cases}
$$
解得
$$
\begin{cases} x=0 \\ y=2 \end{cases},\quad
\begin{cases} x=0 \\ y=-2 \end{cases},\quad
\begin{cases} x=1 \\ y=0 \end{cases},\quad
\begin{cases} x=-1 \\ y=0 \end{cases}
$$
即找到4个解，共4个可疑点：$(0,2),\,(0,-2),\,(1,0),\,(-1,0)$。

将这4个可疑点包括$(0,0)$代入$z = x^2 - y^2 + 2$中，得最大值为$3$，最小值为$-2$。

---

# P 多元函数微分的应用_第12页.png

## 最远(近)点的垂线原理
“此原理可直接用”，用好此原理，可在多元最值问题上节约大量时间，提高效率。

- 如果$T$是光滑闭曲线，点$Q$是$T$外的一个点，点$P_1,P_2$分别是$T$上与$Q$的最远点与最近点，则直线$P_1Q,P_2Q$分别在点$P_1,P_2$处与$T$垂直，即$P_1Q,P_2Q$分别与点$P_1,P_2$处的切线垂直。
（函数示意图：点到光滑闭曲线的最远、最近点垂线示意图）

- 若光滑闭曲线$T_1,T_2$不相交，点$P_1,P_2$分别是它们之间的最远(近)点，则直线$P_1P_2$是$T_1,T_2$的公垂线，即$P_1P_2$同时垂直于$T_1,T_2$在这两个点处的切线。
（函数示意图：两条不相交光滑闭曲线的最远/最近点公垂线示意图）

## 例13.21
求曲线$x^2+4y^2=4$上到直线$2x+3y-6=0$的距离最近点。

### 分析
∵ 题中给的是隐函数，
∴ 我们可以用隐函数存在定理，求出$\frac{dy}{dx}$，即斜率；
则我们可以用最远(近)点的垂线原理去将两个斜率建立关系，便可求出最近点的坐标。
（函数示意图：直线与曲线最近点的公垂线示意图）

### 解：
设
$$F_1(x,y)=2x+3y-6$$
$$F_2(x,y)=x^2+4y^2-4$$

---

# P 多元函数微分的应用_第13页.png

$$\frac{dy_1}{dx} = -\frac{F_{1x}'}{F_{1y}'} = -\frac{2}{3}$$

$$\frac{dy_2}{dx} = -\frac{F_{2x}'}{F_{2y}'} = -\frac{2x}{8y}$$

$\because P_1,P_2$分别是$T_1$与$T_2$之间最近点

$\therefore$ 直线$P_1P_2$是$T_1,T_2$的公垂线

$\therefore P_1,P_2$处的切线斜率相等

$\therefore$ 令
$$-\frac{2}{3} = -\frac{2x}{8y}$$

$$\Rightarrow x = \frac{8y}{3}$$

将$x=\frac{8y}{3}$代入$x^2+4y^2=4$中

$$\Rightarrow \begin{cases} x_1 = \frac{8}{5} \\ y_1 = \frac{3}{5} \end{cases}, \begin{cases} x_2 = -\frac{8}{5} \\ y_2 = -\frac{3}{5} \end{cases}$$