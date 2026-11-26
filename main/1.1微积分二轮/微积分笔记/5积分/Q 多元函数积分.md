# Q 多元函数积分_第1页.png

## 多元函数积分——二重积分
### 概念（与一元函数积分对比）
#### 一元函数定积分（曲边梯形面积推导）
设函数$y=f(x)$，满足$x\in[a,b]$，对应曲边梯形函数示意图，曲边梯形面积按以下步骤求解：
1.  **分割**：将曲边梯形的面积任意分割为$n$份，对应区间分割示意图：在底边区间$[a,b]$上取分点$a=x_0, x_1, x_2, \dots, x_{k-1}, x_k, \dots, x_{n-1}, x_n=b$；在分割后的小区间中任取一段$\Delta x_k$，该小区间的长度满足：
$$\Delta x_k = x_k - x_{k-1}$$
2.  **近似**：对应小曲边梯形矩形近似示意图，在小区间$\Delta x_k$中任取一点$x=\varphi_k$，将$\Delta x_k$上变化的高度$y=f(x)$近似为定值$f(\varphi_k)$，则该段小曲边图形的面积就近似为矩形面积，这一小段的面积近似表示为$f(\varphi_k)\cdot \Delta x_k$。
3.  **求和**：将这些小段的近似面积相加，整个图形的近似面积为：
$$\sum_{k=1}^{n} f(\varphi_k)\cdot \Delta x_k$$
4.  **取极限**：记分割得到的所有小区间$\Delta x_k$中最长的区间长度为$\lambda$。

---

# Q 多元函数积分_第2页.png

设 $\lambda = \max\left\{\Delta x_k\right\},\ k\in[1,n]$

则误差趋于0的面积为
$$\lim_{\lambda \to 0} \sum_{k=1}^n f(\xi_k)\cdot \Delta x_k$$
若$\lambda \to 0$，则段数$n\to\infty$

若 $\lim_{\lambda \to 0} \sum_{k=1}^n f(\xi_k)\cdot \Delta x_k$ 存在，

则称$f(x)$在区间$[a,b]$上可积，

记
$$\int_a^b f(x)dx = \lim_{\lambda \to 0} \sum_{k=1}^n f(\xi_k)\cdot \Delta x_k$$

## 二元
$z=f(x,y)$

定义域为有界闭区域$D$

① 体积任意分割成$n$份

在其中任取一块$\Delta\sigma_k$

② 近似

在$\Delta\sigma_k$中任取一点$\begin{cases}x=\xi_k \\ y=\eta_k\end{cases}$，即点$(\xi_k,\eta_k)$。

将$\Delta\sigma_k$中变化的高度$z=f(x,y)$值近似为定值$f(\xi_k,\eta_k)$，则曲顶柱体体积就近似为了长方体体积，这一小块体积就近似表示为：
$$f(\xi_k,\eta_k)\cdot \Delta\sigma_k$$

---

# Q 多元函数积分_第3页.png

## ③ 求和
（曲顶柱体分割求和示意图）
将这些小块的近似体积相加，则整个图形的近似体积为
$$\sum_{k=1}^n f(\xi_k,\eta_k) \cdot \Delta\sigma_k$$

## ④ 取极限
让分割出来的所有小块$\Delta\sigma_k$中最大的那块设为$\lambda$，
设$\lambda = \max\left\{\Delta\sigma_k\right\},\ k\in[1,n]$
则误差趋于0的体积为
$$\lim_{\lambda \to 0} \sum_{k=1}^n f(\xi_k,\eta_k) \cdot \Delta\sigma_k$$
注：若$\lambda \to 0$，则分割的块数$n\to\infty$。

若$\lim\limits_{\lambda \to 0} \sum_{k=1}^n f(\xi_k,\eta_k) \cdot \Delta\sigma_k$存在，则称$f(x,y)$在区域$D$上可积。

## 二重积分的定义
记：
$$\iint_D f(x,y)\,d\sigma = \lim_{\lambda \to 0} \sum_{k=1}^n f(\xi_k,\eta_k) \cdot \Delta\sigma_k$$
该式表示二元函数$f(x,y)$在区域$D$上的二重积分。

### 相关概念
其中各部分名称如下：
- $f(x,y)$称为被积函数，
- $f(x,y)d\sigma$称为被积表达式，
- $d\sigma$称为面积元素，
- $x,y$称为积分变量，
- $D$称为积分区域，
- $\sum\limits_{k=1}^n f(\xi_k,\eta_k)\Delta\sigma_k$称为积分和。

### 二重积分存在的充分条件
若$f(x,y)$在有界闭区域$D$上连续，则二重积分$\displaystyle\iint_D f(x,y)\,d\sigma$一定存在。

---

# Q 多元函数积分_第4页.png

## 注（与一元一样）
如果$f(x,y)$是负的，柱体就在$xOy$面下方，二重积分的绝对值仍等于柱体的体积，但，二重积分的值是负的。

如果$f(x,y)$在$D$的若干部分区域上是正的，而在其他部分区域上是负的，那么$f(x,y)$在$D$上的二重积分就等于$xOy$面上方的柱体体积减去$xOy$面下方的柱体体积所得之差。

性质（与一元一样）

## 求区域面积
$$\iint\limits_D 1\cdot d\sigma = \iint\limits_D d\sigma = A \quad (A为D的面积)$$
相当于是$f(x,y)=1$，高为一定值1，则
体积 = 底面积 × 高 = 底面积

## 可积函数必有界
当$f(x,y)$在有界闭区域$D$上可积时，$f(x,y)$在$D$上必有界。

## 积分的线性性质
设$k_1,k_2$为常数，则
$$\iint\limits_D \left[k_1 f(x,y) \pm k_2 g(x,y)\right] d\sigma = k_1 \iint\limits_D f(x,y) d\sigma \pm k_2 \iint\limits_D g(x,y) d\sigma$$

---

# Q 多元函数积分_第5页.png

## 积分的可加性
设$f(x,y)$在有界闭区域$D$上可积，
且$D_1 \cup D_2 = D$，$D_1 \cap D_2 = \emptyset$，
则
$$\iint_D f(x,y)d\sigma = \iint_{D_1} f(x,y)d\sigma + \iint_{D_2} f(x,y)d\sigma$$

## 积分的保号性
当$f(x,y),g(x,y)$在有界闭区域$D$上可积时，
若在$D$上有$f(x,y) \leq g(x,y)$，
则有
$$\iint_D f(x,y)d\sigma \leq \iint_D g(x,y)d\sigma$$
特殊地有
$$\left| \iint_D f(x,y)d\sigma \right| \leq \iint_D |f(x,y)|d\sigma$$

## 二重积分的估值定理
设$M,m$分别是$f(x,y)$在有界闭区域$D$上的最大值和最小值，$A$为$D$的面积，
则有
$$mA \leq \iint_D f(x,y)d\sigma \leq MA$$
其中
$$\iint_D m\,d\sigma = mA,\quad \iint_D M\,d\sigma = MA$$

## 二重积分的中值定理（本质与一元一样）
设函数$f(x,y)$在有界闭区域$D$上连续，$A$为$D$的面积，
则在$D$上至少存在一点$(\xi,\eta)$，使得
$$\iint_D f(x,y)d\sigma = f(\xi,\eta) A,\quad (\xi,\eta)\in D$$
一元对应形式：
$$\int_a^b f(x)dx = f(\xi)(b-a),\quad \xi\in(a,b)$$

---

# Q 多元函数积分_第6页.png

## 例题
设$f(x,y)$具有二阶连续偏导数，
$$D_t = \{(x,y)\mid 0\leq x\leq t,\, 0\leq y\leq t\},$$
令$F(t) = \iint_{D_t} f_{xy}''(x,y)\,\mathrm{d}x\mathrm{d}y$，求$F_+'(0)$。

## 分析
当所求二重积分难以计算时，可考虑用二重积分中值定理处理。

## 解答
根据右导数定义：
$$
F_+'(0) = \lim_{t\to0^+} \frac{F(t)-F(0)}{t-0}
$$
注：当$t=0$时，积分区域面积$A=0$，对应二重积分值为$0$，即$F(0)=0$，因此：
$$
F_+'(0) = \lim_{t\to0^+} \frac{1}{t}\iint_{D_t} f_{xy}''(x,y)\,\mathrm{d}x\mathrm{d}y
$$
由二重积分中值定理，存在$(\xi,\eta)\in D_t$，使得：
$$\iint_{D_t} f_{xy}''(x,y)\,\mathrm{d}x\mathrm{d}y = f_{xy}''(\xi,\eta) \cdot t^2$$
注：积分区域$D_t$为正方形，底面积$A=t^2$。代入得：
$$
\begin{aligned}
F_+'(0) &= \lim_{t\to0^+} \frac{f_{xy}''(\xi,\eta)\cdot t^2}{t} \\
&= \lim_{t\to0^+} t\cdot f_{xy}''(\xi,\eta)
\end{aligned}
$$
当$t\to0$时，$x\to0,\, y\to0$，故$f_{xy}''(\xi,\eta)\to f_{xy}''(0,0)$，其中$f_{xy}''(0,0)$为一个常数，因此：
$$F_+'(0)=0$$

## 二重积分普通对称性
### 定义
（对应平面区域对称示意图：平面直角坐标系内关于y轴对称的积分区域，标注原点、x轴、y轴，对称点$(x,y)$与$(-x,y)$，以及两点处对应的面积元素$\mathrm{d}\sigma$）
设区域$D$关于$y$轴对称，取对称的两块小面积$\mathrm{d}\sigma$，对称点分别为$(x,y)$与$(-x,y)$，则对称点处的高分别为$f(x,y)$与$f(-x,y)$。
据定义，对称位置的两个“小竖条”的体积分别为$f(x,y)\mathrm{d}\sigma$与$f(-x,y)\mathrm{d}\sigma$。
因为$\mathrm{d}\sigma$一样，所以当$f(x,y)=f(-x,y)$时，$f(x,y)\mathrm{d}\sigma = f(-x,y)\mathrm{d}\sigma$，体积相同。
（对应空间曲顶柱体示意图：空间直角坐标系下的曲顶柱体示意图）

---

# Q 多元函数积分_第7页.png

此时，只需计算对称区域的一半，然后乘以2，即可得到整个积分值。

当$f(x,y) = -f(-x,y)$时，
$f(x,y)d\sigma = -f(-x,y)d\sigma$

【关于y轴对称的曲顶柱体函数示意图】

对称区域的体积正好相反，这样累加起来，积分值为0。

则，综上可得：
$$
\iint\limits_D f(x,y)dxdy =
\begin{cases}
2\iint\limits_{D_1} f(x,y)dxdy ,& f(x,y)=f(-x,y) \\
0 ,& f(x,y)=-f(-x,y)
\end{cases}
$$
其中，$D_1$为$D$关于$y$轴对称的半部分。

## 理解
本质是：
若两块体积，映射的一元函数部分
即$D$的面积相等/关于...对称
—— 底面积相等

且两块体积映射的一元函数$D$中，每一点处对应的$z=f(x,y)$相等
—— 高相等

则两块体积的值相等
—— 体积=底×高=$A$

若这两块的二重积分值：
同号 $\to$ 偶倍：$A+A=2A$
异号 $\to$ 奇零：$A-A=0$

## 对称情况的总结
$$\iint\limits_D f(x,y)d\sigma =$$

---

# Q 多元函数积分_第8页.png

## 积分区域$D$关于y轴（$x=0$）对称
（关于$x$为偶函数的曲面示意图）
当被积函数满足$f(x,y) = f(-x,y)$（即$f$关于$x$为偶函数），则
$$\iint_D f(x,y)\,d\sigma = 2\iint_{D_1} f(x,y)\,d\sigma$$

（关于$x$为奇函数的曲面示意图）
当被积函数满足$f(x,y) = -f(-x,y)$（即$f$关于$x$为奇函数），则
$$\iint_D f(x,y)\,d\sigma = 0$$

注：推广到$D$关于直线$x=a$对称
$$\iint_D f(x,y)\,d\sigma = 2\iint_{D_1} f(x,y)\,d\sigma,\quad f(x,y)=f(2a-x,y)$$
$$\iint_D f(x,y)\,d\sigma = 0,\quad f(x,y)=-f(2a-x,y)$$
其中，$D_1$为$D$关于$x=a$对称的半部分。

---

## 积分区域$D$关于x轴（$y=0$）对称
（关于$y$为偶函数的曲面示意图）
当被积函数满足$f(x,y) = f(x,-y)$（即$f$关于$y$为偶函数），则
$$\iint_D f(x,y)\,d\sigma = 2\iint_{D_1} f(x,y)\,d\sigma$$

（关于$y$为奇函数的曲面示意图）
当被积函数满足$f(x,y) = -f(x,-y)$（即$f$关于$y$为奇函数），则
$$\iint_D f(x,y)\,d\sigma = 0$$

注：推广到$D$关于直线$y=a$对称
$$\iint_D f(x,y)\,d\sigma = 2\iint_{D_1} f(x,y)\,d\sigma,\quad f(x,y)=f(x,2a-y)$$
$$\iint_D f(x,y)\,d\sigma = 0,\quad f(x,y)=-f(x,2a-y)$$
其中，$D_1$为$D$关于$y=a$对称的半部分。

---

# Q 多元函数积分_第9页.png

## 二重积分对称性：积分区域关于原点对称
（附对应二元函数曲面示意图2张）
若积分区域$D$关于原点对称：
- 若被积函数满足$f(x,y)=f(-x,-y)$，则
$$\iint_D f(x,y)d\sigma = 2\iint_{D_1} f(x,y)d\sigma$$
- 若被积函数满足$f(x,y)=-f(-x,-y)$，则
$$\iint_D f(x,y)d\sigma = 0$$
其中，$D_1$是$D$关于原点对称的半部分。

## 二重积分对称性：积分区域关于$y=x$对称
（附二元函数曲面示意图1张、平面区域关于$y=x$对称的示意图1张）
若积分区域$D$关于直线$y=x$对称：
- 若被积函数满足$f(x,y)=f(y,x)$，则
$$\iint_D f(x,y)d\sigma = 2\iint_{D_1} f(x,y)d\sigma$$
- 若被积函数满足$f(x,y)=-f(y,x)$，则
$$\iint_D f(x,y)d\sigma = 0$$
其中，$D_1$是$D$关于$y=x$对称的半部分。

## 例143
设$J_i = \iint_{D_i} \sqrt[3]{x-y} \, dxdy \quad (i=1,2,3)$，
其中各积分区域为：
$$
\begin{aligned}
D_1 &= \{(x,y) \mid 0\leq x\leq1,\, 0\leq y\leq1\} \\
D_2 &= \{(x,y) \mid 0\leq x\leq1,\, 0\leq y\leq\sqrt{x}\} \\
D_3 &= \{(x,y) \mid 0\leq x\leq1,\, x^2\leq y\leq1\}
\end{aligned}
$$
求$J_1,J_2,J_3$的大小关系。

解：
$\because \sqrt[3]{x-y} = -\sqrt[3]{y-x}$
$\therefore f(x,y)=\sqrt[3]{x-y}$关于$y=x$对称，即曲顶柱体的“高”关于$y=x$对称，且为“奇零”型。

- 分析$J_1$：
  积分区域“底”为$D_1$：$D_1$是$x\in[0,1]$上，由$y=0,y=1$所围的区域。
  （附$D_1$关于$y=x$对称的平面区域示意图1张）
  该区域的“底面积”关于$y=x$对称，结合被积函数的奇零性质，可得
  $$\Rightarrow J_1 = 0$$

---

# Q 多元函数积分_第10页.png

## “底”为$D_2$
（函数示意图：平面直角坐标系$xOy$，绘制曲线$y=\sqrt{x}$与直线$y=x$，二者交于$(1,1)$）
$D_2$为在$x\in[0,1]$上$y=0,y=\sqrt{x}$所围区域，发现“底面积”不关于$y=x$对称。
但是，$D_1$是关于$y=x$对称的区域，我们可以补上去，补对称区域做对比，发现可以在不对称区域中找出部分对称的区域：这部分关于$y=x$对称，且$f(x,y)$符合“奇零”性质，因此只需计算剩余区域，即$a$区。
（函数示意图：平面直角坐标系$xOy$，绘制直线$y=x$，阴影标注对称区域，剩余区域标注为$a$区，标注$a$区内点$(x,y)$）
$a$区内满足$x>y$，将$a$区的点$(x,y)$代入$f(x,y)$：
$$\Rightarrow \sqrt[3]{x-y} > 0$$
由二重积分的保号性：
$$\Rightarrow J_2 = \iint_{D_2} \sqrt[3]{x-y} \,d\sigma > 0$$

## “底”为$D_3$
（函数示意图：平面直角坐标系$xOy$，绘制曲线$y=x^2$、直线$y=1$与直线$y=x$，$y=x$与$y=1$交于$(1,1)$）
$D_3$为在$x\in[0,1]$上$y=x^2,y=1$所围区域，与$D_2$的分析做法一致，利用$f(x,y)$关于$y=x$的对称性分析。
在不对称的部分中，找出$D_3$关于$y=x$对称的部分，发现$b$区满足$y>x$，将$b$区的点$(x,y)$代入$f(x,y)$：
（函数示意图：平面直角坐标系$xOy$，绘制直线$y=x$，阴影标注$b$区）
$$\Rightarrow \sqrt[3]{x-y} < 0$$
由二重积分的保号性：
$$\Rightarrow J_3 = \iint_{D_3} \sqrt[3]{x-y} \,d\sigma < 0$$
$$\Rightarrow J_2 > J_1 > J_3$$

---

# Q 多元函数积分_第11页.png

## 轮换对称性
### 引言
发现：
$$\iint_{D_1} (2x^2+3y^2)\mathrm{d}x\mathrm{d}y = \iint_{D_2} (2y^2+3x^2)\mathrm{d}y\mathrm{d}x$$
其中，$D_1: \frac{x^2}{4}+\frac{y^2}{3}\leq1$，$D_2: \frac{y^2}{4}+\frac{x^2}{3}\leq1$
是x,y互换后，积分值不变

深入观察发现
x,y互换
与物体的体积大小不构成任何影响
因为，底面积不变，只是关于$y=x$对称
高也不变
则体积不变

### 定义
在直角坐标系下
若把$x$与$y$对调后
区域$D$不变或关于$y=x$对称
则
$$\iint_D f(x,y)\mathrm{d}\sigma = \iint_D f(y,x)\mathrm{d}\sigma$$

### 意义
若$\iint_D f(x,y)\mathrm{d}\sigma$很难算
但$f(x,y)+f(y,x)$很简单时
则
$$
\begin{aligned}
\iint_D f(x,y)\mathrm{d}\sigma &= \frac{1}{2}\iint_D \left[f(x,y)+f(y,x)\right]\mathrm{d}\sigma
\end{aligned}
$$

---

# Q 多元函数积分_第12页.png

## 与保号性结合的结论
在直角坐标系中
若 $f(x,y)+f(y,x)\geqslant a$，则
$$
\begin{aligned}
\iint\limits_D f(x,y)\mathrm{d}\sigma &= \iint\limits_D f(y,x)\mathrm{d}\sigma \\
&= \frac{1}{2}\iint\limits_D \left[f(x,y)+f(y,x)\right]\mathrm{d}x\mathrm{d}y \\
&\geqslant \frac{1}{2}\iint\limits_D a \,\mathrm{d}x\mathrm{d}y = \frac{a}{2}\cdot S_D
\end{aligned}
$$

例：计算 $\iint\limits_D \frac{a\sqrt{f(x)}+b\sqrt{f(y)}}{\sqrt{f(x)}+\sqrt{f(y)}}\mathrm{d}\sigma$，如果直接计算很麻烦。
$$
\because \frac{a\sqrt{f(x)}+b\sqrt{f(y)}}{\sqrt{f(x)}+\sqrt{f(y)}} + \frac{a\sqrt{f(y)}+b\sqrt{f(x)}}{\sqrt{f(y)}+\sqrt{f(x)}} = a+b
$$
$$
\therefore 原式 = \frac{1}{2}\iint\limits_D (a+b)\mathrm{d}\sigma = \frac{1}{2}(a+b)\cdot S_D
$$

## 理解
普通对称中的$\begin{cases} D关于y=x对称 \\ 且f(x,y)关于y=x对称 \end{cases}$的情形，与这里的轮换对称性的区别与联系：
虽然都是$D$关于$y=x$对称，
但普通对称考查的是$f(x,y)$与$f(y,x)$相等还是相反；
轮换对称性考查的是$f(x,y)+f(y,x)$是否变得简单。

事实上，当$f(x,y)=-f(y,x)$时，二者是一回事。

### 例14.4
设$f(x)=\iint\limits_{D(x)} \frac{v\ln\sqrt{u^2+v^2}}{u+v}\mathrm{d}u\mathrm{d}v$，
其中$D(x)=\left\{(u,v)\mid \frac{1}{4}\leqslant u^2+v^2\leqslant x^2\right\}$，
求$f(x)$。

---

# Q 多元函数积分_第13页.png

解：
u,v互换，D不变
先考虑用普通对称性
$g(u,v)=\frac{v\ln\sqrt{u^2+v^2}}{u+v}$
$g(v,u)=\frac{u\ln\sqrt{v^2+u^2}}{v+u}$
发现，$g(u,v)$与$g(v,u)$既不相同，也不相反
则，考虑用轮换对称
$$g(u,v)+g(v,u)=\ln\sqrt{u^2+v^2}$$
成功化简了计算
即，
$$原式=\frac{1}{2}\iint\limits_{D(xy)} \ln\sqrt{u^2+v^2}\,\mathrm{d}u\mathrm{d}v$$
（等计算方法学完，再回来解此题）