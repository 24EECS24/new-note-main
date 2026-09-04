---

# I 中值定理_第1页.png

## 中值定理
- 符号$\xi$：读音标注kē, sè
- $\exists x$：至少有一个$x$

## 涉及函数的中值定理
设$f(x)$在$[a,b]$上连续，则有如下定理：

### 定理1（有界与最值定理）
一定有$m \leq f(x) \leq M$，其中$m,M$分别为$f(x)$在$[a,b]$上的最小值与最大值。
即：在闭区间上连续的函数，必有界，且必有最大值与最小值。
（函数示意图：闭区间上连续函数的最值示意，平面直角坐标系$xOy$中绘制$[a,b]$上的连续曲线，标注最大值线$y=M$、最小值线$y=m$，区间端点$a,b$）

### 定理2（介值定理）
介值：介于最小值与最大值之间的值。
内容：当$m \leq \mu \leq M$时，一定存在$\xi \in [a,b]$，使得$f(\xi)=\mu$。
通俗解释：如果存在一个实数$\mu$，$\mu$夹在$m$与$M$之间，则在$[a,b]$上至少存在一个$\xi$，使得$f(\xi)=\mu$，即$y=\mu$与$y=f(x)$至少有一个交点。

### 定理3（平均值定理）
在区间$(a,b)$内插入$n$个点，满足$a < x_1 < x_2 < \dots < x_n < b$，则在$[x_1,x_n]$内至少存在一点$\xi$，使得
$$f(\xi) = \frac{f(x_1)+f(x_2)+\dots +f(x_n)}{n}$$
（区间分点示意图：第一幅为线段表示区间$[a,b]$，标注端点$a,b$；第二幅为同区间线段，标注插入的分点$x_1,x_2,\dots,x_n$的位置）

#### 证明：
$\because f(x)$在闭区间上连续，
$\therefore$
$$
\begin{gathered}
m \leq f(x_1) \leq M \\
m \leq f(x_2) \leq M \\
\vdots \\
m \leq f(x_n) \leq M
\end{gathered}
$$

---

# I 中值定理_第2页.png

$\Rightarrow n\cdot m \leqslant f(x_1)+f(x_2)+\dots +f(x_n) \leqslant n\cdot M$
$\Rightarrow m \leqslant \frac{f(x_1)+f(x_2)+\dots +f(x_n)}{n} \leqslant M$
即
$$\frac{f(x_1)+f(x_2)+\dots +f(x_n)}{n} = \mu$$
$\Rightarrow \exists \xi$，使得
$$f(\xi) = \frac{f(x_1)+f(x_2)+\dots +f(x_n)}{n}$$
## 定理4（零点定理）
- 若$f(x)$在$[a,b]$上连续，当$f(a)\cdot f(b)<0$时，$\exists \xi \in (a,b)$，使得$f(\xi)=0$。
  （函数示意图：闭区间$[a,b]$上的连续曲线，两端点分处$x$轴两侧，与$x$轴相交）
  注：负数$<0<$正数
- 推广：若$f(x)$在$(a,b)$内连续，$\lim\limits_{x \to a^+} f(x) = \alpha$，$\lim\limits_{x \to b^-} f(x) = \beta$，且$\alpha\cdot\beta<0$，则$f(x)=0$在$(a,b)$内至少有一个根。这里的$a,b,\alpha,\beta$可以是有限数，也可以是无穷大。
（对应推广的两个函数示意图：
1.  开区间$(a,b)$上的连续曲线，$x\to a^+$时$f(x)\to\alpha<0$，$x\to b^-$时$f(x)\to\beta>0$，曲线与$x$轴相交；
2.  开区间$(a,b)$上的连续曲线，$x\to a^+$时$f(x)\to -\infty$，$x\to b^-$时$f(x)\to +\infty$，曲线与$x$轴相交）
取不到$\alpha$与$\beta$，不影响两端异号的事实。
## 例6.1
设函数$f(x)$在$[0,1]$上连续，且$f(1)=0$，$f\left(\frac{1}{2}\right)=1$，证明：存在$\eta \in \left(\frac{1}{2},1\right)$，使得$f(\eta)=\eta$。
证明：因为我们要用零点定理，即利用$f(x)>0$、$f(x)=0$、$f(x)<0$的异号性质找零点。
对$f(\eta)=\eta$移项，发现$f(\eta)-\eta=0$。
设$g(x)=f(x)-x$，问题就变为了：
证明$\exists \eta \in \left(\frac{1}{2},1\right)$，使得$g(\eta)=0$。

---

# I 中值定理_第3页.png

$$g(1)=f(1)-1=-1<0$$
$$g\left(\frac{1}{2}\right)=f\left(\frac{1}{2}\right)-\frac{1}{2}=\frac{1}{2}>0$$
由零点定理$\Rightarrow \exists \eta \in \left(\frac{1}{2},1\right)$使$g(\eta)=0$
即 $f(\eta)=\eta$

## 例6.2
设函数$f(x)$在区间$[0,1]$上连续，且$f(1)>0$，且$\lim\limits_{x \to 0^+} \frac{f(x)}{x}<0$，证明：方程$f(x)=0$在区间$(0,1)$内至少存在一个实根。

证明：
$\because \lim\limits_{x \to 0^+} \frac{f(x)}{x}<0$
$\therefore$ 当$x \to 0^+$时，
$x>0$，
$\frac{f(x)}{x}<0$，
$\therefore f(x)<0$
又$\because f(1)>0$，
由零点定理$\Rightarrow$
$f(x)=0$在$(0,1)$内至少存在一个实根。

## 涉及导数（微分）的中值定理
### 定理5（费马定理）
设$f(x)$在点$x_0$处满足：
$$\begin{cases} ①\ 在x_0处可导 \\ ②\ 在x_0处取极值 \end{cases}$$
则$f'(x_0)=0$。

生活中的应用：当一个人跑到最远处时，他的速度为0；当一个人跑到最快时，他的加速度为0。

$f'(x)>0 \to f'(x_0)=0 \to f'(x)<0$

## 例6.3（导数的零点定理）
设$f(x)$在$[a,b]$上可导，证明当$f'_+(a)\cdot f'_-(b)<0$时，存在$\xi \in [a,b]$使得$f'(\xi)=0$。

---

# I 中值定理_第4页.png

## 函数的零点定理
$f(x)$在$[a,b]$上连续，且$f(a)\cdot f(b)<0$，则
$$\exists \xi\in(a,b),\quad f(\xi)=0$$

## 导数的零点定理
$f(x)$在$[a,b]$上可导，且$f'_+(a)\cdot f'_-(b)<0$，则
$$\exists \xi\in(a,b),\quad f'(\xi)=0$$

**证明：** 设$f'_+(a)>0$，$f'_-(b)<0$。
由右导数定义：
$$\lim_{x \to a^+} \frac{f(x)-f(a)}{x-a} > 0$$
根据极限的保号性，存在$\delta>0$，当$x \in (a,a+\delta)$时：
$x>a$，故$x-a>0$，因此
$$\frac{f(x)-f(a)}{x-a} > 0 \implies f(x) > f(a)$$

再由左导数定义：
$$\lim_{x \to b^-} \frac{f(x)-f(b)}{x-b} < 0$$
同理，当$x \in (b-\delta,b)$时：
$x<b$，故$x-b<0$，因此
$$f(x) > f(b)$$

由于$f(x)$在$[a,b]$上连续，根据闭区间上连续函数的最值定理，$f(x)$在$[a,b]$上存在最大值。结合$f(x)>f(a)$与$f(x)>f(b)$，可知$f(a),f(b)$均不是最大值，因此最大值点$\xi$必在开区间$(a,b)$内取得，即$\xi$为$f(x)$的极大值点。

由费马定理可得：
$$\exists \xi\in(a,b),\quad f'(\xi)=0$$

## 定理6（罗尔定理）
设$f(x)$满足以下条件：
$$
\begin{cases}
\text{① 在}[a,b]\text{上连续}, \\
\text{② 在}(a,b)\text{内可导}, \\
\text{③ }f(a)=f(b),
\end{cases}
$$
则存在$\xi\in(a,b)$，使得$f'(\xi)=0$。

## 推广的罗尔定理
（在$a,b$点的函数值可能取不到）
设$f(x)$满足以下条件：
$$
\begin{cases}
\text{① 在}(a,b)\text{内可导}, \\
\text{② }\lim_{x \to a^+}f(x) = \lim_{x \to b^-}f(x) = A,
\end{cases}
$$
则在$(a,b)$内至少存在一点$\xi$，使得$f'(\xi)=0$。

其中区间$(a,b)$可以是有限区间，也可以是无穷区间；
$A$可以是有限数，也可以是无穷大。

---

# I 中值定理_第5页.png

注：常用的逆运算

## 乘积求导公式$(uv)'=u'v+uv'$的逆用
$$\left[f(x)f(x)\right]'=\left[f^2(x)\right]'=2f(x)f'(x)$$
见到$f(x)f'(x)$，令$g(x)=f^2(x)$

$$\left[f(x)f'(x)\right]'=\left[f'(x)\right]^2 + f(x)f''(x)$$
见到$\left[f'(x)\right]^2 + f(x)f''(x)$，令$g(x)=f(x)f'(x)$

$$
\begin{aligned}
\left[f(x)e^{\varphi(x)}\right]'
&= f'(x)e^{\varphi(x)} + f(x)e^{\varphi(x)}\cdot \varphi'(x)\\
&= \left[f'(x)+f(x)\varphi'(x)\right]e^{\varphi(x)}
\end{aligned}
$$
见到$f'(x)+f(x)\varphi'(x)$，令$g(x)=f(x)e^{\varphi(x)}$

eg: 见到$f'(x)+f(x)$，令$g(x)=f(x)e^x$
见到$f'(x)-f(x)$，令$g(x)=f(x)e^{-x}$
见到$f'(x)-2f(x)$，令$g(x)=f(x)e^{-2x}$

## 商的求导公式$\left(\frac{u}{v}\right)'=\frac{u'v-uv'}{v^2}$的逆用
$$\left[\frac{f(x)}{x}\right]' = \frac{f'(x)x - f(x)}{x^2}$$
见到$f'(x)x-f(x)$，$x\neq0$，令$g(x)=\frac{f(x)}{x}$

$$\left[\frac{f'(x)}{f(x)}\right]' = \frac{f''(x)f(x)-\left[f'(x)\right]^2}{f^2(x)}$$
见到$f''(x)f(x)-\left[f'(x)\right]^2$，$f(x)\neq0$
令$g(x)=\frac{f'(x)}{f(x)}$

$$\left[\ln f(x)\right]' = \frac{f'(x)}{f(x)}$$
故
$$\left[\ln f(x)\right]'' = \left[\frac{f'(x)}{f(x)}\right]' = \frac{f''(x)f(x)-\left[f'(x)\right]^2}{f^2(x)}$$
见到$f''(x)f(x)-\left[f'(x)\right]^2$，$f(x)>0$
令$g(x)=\ln f(x)$

二阶导是涉及到凹凸性的。

---

# I 中值定理_第6页.png

## 广义化
将$f(x)$看成$\square$
见到$\square'+\square$，令$g(x)=\square e^x$
见到$\square'-\square$，令$g(x)=\square e^{-x}$

eg：当你见到$f'''(x)-f'(x)$时
$$
\begin{align*}
f'''(x)-f'(x)&=f'''(x)-f''(x)+f''(x)-f'(x)\\
&=[f''(x)-f'(x)]'+[f''(x)-f'(x)]
\end{align*}
$$
则令$g(x)=[f''(x)-f'(x)]e^x$

eg：当你见到$f''(x)-f(x)$时
$$
\begin{align*}
f''(x)-f(x)&=[f''(x)+f'(x)]-[f'(x)+f(x)]\\
&=[f'(x)+f(x)]'-[f'(x)+f(x)]
\end{align*}
$$
则令$g(x)=[f'(x)+f(x)]e^{-x}$

## 例6.4
设$f(x)$在$[0,3]$上连续，在$(0,3)$内可导，且$f(0)+f(1)+f(2)=3$，$f(3)=1$，证明：
必存在$\xi\in(0,3)$，使得$f'(\xi)=0$。

证明：由平均值定理，
$$\exists \eta\in[0,2],\ f(\eta)=\frac{f(0)+f(1)+f(2)}{3}=1$$
$\because f(\eta)=1,\ f(3)=1$
由罗尔定理$\Rightarrow \exists \xi\in(\eta,3)\subset(0,3)$，使得$f'(\xi)=0$。

## 罗尔定理的扩展
（适用场景：证明$\exists \xi$使得$f''(\xi)=0$）
要找出函数值相等的三个不同点：
$$f(a)=f(b)=f(c)$$
若$a<b<c$，对应x轴上从左到右依次为$a,b,c$三点。

---

# I 中值定理_第7页.png

则分别在$[a,b]$，$[b,c]$上使用罗尔定理
有$f'(\xi_1)=f'(\xi_2)=0$
$\xi_1 \in (a,b),\ \xi_2 \in (b,c)$
再由$f'(\xi_1)=f'(\xi_2)$在$[\xi_1,\xi_2]$上使用罗尔定理
$\Rightarrow \exists \xi \in (\xi_1,\xi_2)$使得$f''(\xi)=0$

## 定理7（拉格朗日中值定理）
设$f(x)$满足
$$
\begin{cases}
①\text{在}[a,b]\text{上连续} \\
②\text{在}(a,b)\text{内可导}
\end{cases}
$$
则存在$\xi \in (a,b)$使得
$$f(b)-f(a)=f'(\xi)(b-a)$$
或$f(a)-f(b)=f'(\xi)(a-b)$
或写成
$$f'(\xi)=\frac{f(b)-f(a)}{b-a}$$

注：见到$f(a)-f(b)$或$f$与$f'$的关系时
一般想到用拉格朗日中值定理

作用：用导数值来控制函数值的增减
$$f(b)-f(a)=f'(\xi)(b-a)$$
$(b-a)$是一个固定的值.
$f'(\xi)$的大小，就控制了$[f(b)-f(a)]$的大小
$f'(\xi)$大，则$[f(b)-f(a)]$大
$f'(\xi)=0$，则$[f(b)-f(a)]=0$

例6.8
若$f(x)$在$(a,b)$内可导，且$f'(x)$有界
证明：$f(x)$在$(a,b)$内有界

---

# I 中值定理_第8页.png

## 解题技巧：见到$f$与$f'$，想到拉格朗日中值定理
证明：$\because f(x)$在$(a,b)$内可导
$\therefore f(x)$在$(a,b)$内连续
在$(a,b)$内任取一固定点$x_0$。
任取一泛指点为$x$，对应区间示意图：数轴上从左到右依次标注点$a,\ x,\ x_0,\ b$
则$f(x)$满足：
$$
\begin{cases}
在[x,x_0]上连续 \\
在(x,x_0)内可导
\end{cases}
$$
由拉格朗日中值定理可得：
$$f(x)-f(x_0)=f'(\xi)(x-x_0)$$
$\because f'(x)$有界
$\therefore \exists K>0,\ |f'(x)|\leq K,\ \forall x\in(a,b)$
$\therefore f(x)=f(x_0)+f'(\xi)(x-x_0)$
$$|f(x)|=\left|f(x_0)+f'(\xi)(x-x_0)\right|$$
由三角不等式：
$$\left|f(x_0)+f'(\xi)(x-x_0)\right|\leq |f(x_0)|+|f'(\xi)|\cdot |x-x_0|$$
$$\Rightarrow |f(x)|\leq |f(x_0)|+K(b-a)$$
$\therefore f(x)$在$(a,b)$内有界

## 例6.9
设$f(x)$在$[0,1]$上连续，在$(0,1)$内可导，$f(0)=0$，且$f(x)$在$[0,1]$上不恒等于零，证明：存在$\xi\in(0,1)$，使得$f(\xi)f'(\xi)>0$。

证明：根据导数逆运算构造辅助函数
令$g(x)=\frac{1}{2}f^2(x)$，要证$g'(\xi)>0$。
由$g(0)=0$，且$f(x)$不恒为零，故$\exists a\in(0,1]$，使$f(a)\neq0$，因此：
$$g(a)=\frac{1}{2}f^2(a)>0$$
在$[0,a]$上对$g(x)$应用拉格朗日中值定理：
$$\frac{g(a)-g(0)}{a-0}=g'(\xi)$$
$\because g(a)>0,\ g(0)=0,\ a>0$
$$\therefore g'(\xi)=f(\xi)f'(\xi)>0$$

---

# I 中值定理_第9页.png

## 注例
证明：$\exists \xi \in \left(0,\frac{\pi}{2}\right)$，使得$x\cos\xi = \sin x$。
### 正推（分析法）：
将待证式变型：
$$\cos\xi = \frac{\sin x}{x}$$
对比拉格朗日中值公式在左端点函数值为0时的形式$\frac{f(b)}{b}$，凑出拉格朗日中值定理的标准结构$\frac{f(b)-f(a)}{b-a}$：
$$\cos\xi = \frac{\sin x - \sin 0}{x - 0}$$
由拉格朗日中值定理可得：
$$\sin x = \cos\xi \cdot x,\quad \xi\in\left(0,\frac{\pi}{2}\right)$$
### 综合证明：
$\because \sin x$满足：
$$\begin{cases}
在\left[0,\frac{\pi}{2}\right]上连续 \\
在\left(0,\frac{\pi}{2}\right)上可导
\end{cases}$$
$\therefore \exists \xi\in\left(0,\frac{\pi}{2}\right)$，使得
$$\sin x - \sin 0 = (\sin\xi)'(x-0)$$
化简得：
$$\sin x = \cos\xi \cdot x$$
即$\exists \xi\in\left(0,\frac{\pi}{2}\right)$，使得$x\cos\xi = \sin x$。
---
## 定理8（柯西中值定理）
注：该定理考查形式往往是一个具体函数搭配一个抽象函数。
设$f(x),g(x)$满足以下条件：
$$\begin{cases}
①\ 在[a,b]上连续 \\
②\ 在(a,b)内可导 \\
③\ \forall x\in(a,b),g'(x)\neq0
\end{cases}$$
则存在$\xi\in(a,b)$，使得
$$\frac{f(b)-f(a)}{g(b)-g(a)}=\frac{f'(\xi)}{g'(\xi)}$$
---
## 三大定理的联系
罗尔定理几何意义示意图：平面直角坐标系横轴为$x$轴，纵轴为$y$轴，标注区间端点$a,b$及内点$\xi$；函数在$[a,b]$上两端点等高，$\xi$处为极大值点，标注$f'(\xi)=0$，对应罗尔定理的几何意义。
示意图下方有竖直向下箭头，代表定理从特殊到一般的推广方向。

---

# I 中值定理_第10页.png

直角坐标系$xOy$下函数$y=f(x)$示意图：标注端点$(a,f(a))$、$(b,f(b))$，区间$(a,b)$内点$\xi$处的切线平行于两端点连线，对应拉格朗日中值公式：
$$f'(\xi)=\frac{f(b)-f(a)}{b-a}$$
旁注：拉格朗日
将直角坐标系下的函数表达式写成参数方程：
参数方程$\begin{cases}x=g(t)\\y=f(t)\end{cases}$对应的曲线示意图（横轴为$g(t)$，纵轴为$f(t)$）：标注端点$(g(a),f(a))$、$(g(b),f(b))$，区间$(a,b)$内参数$\xi$对应点处的切线斜率为$K=\frac{f(b)-f(a)}{g(b)-g(a)}$。
由参数方程求导法则推导柯西中值公式：
$$K=\left.\frac{dy}{dx}\right|_{\xi}=\left.\frac{\frac{dy}{dt}}{\frac{dx}{dt}}\right|_{\xi}=\frac{f'(\xi)}{g'(\xi)}=\frac{f(b)-f(a)}{g(b)-g(a)}$$
## 例6.11
设$f(x)$在$[a,b]$上连续，在$(a,b)$内可导，$0<a<b$。
证明：至少存在一点$\xi\in(a,b)$，使得
$$f(b)-f(a)=\xi\left(\ln\frac{b}{a}\right)f'(\xi)$$
$\because$ 待证结论可变形为：
$$f(b)-f(a)=\xi\left(\ln b - \ln a\right)f'(\xi)$$
整理得：
$$\frac{f(b)-f(a)}{\ln b - \ln a}=\frac{f'(\xi)}{\frac{1}{\xi}}, \quad (\ln x)'=\frac{1}{x}$$
（推）
$\therefore$ 证明：
$\because f(x),\ln x$满足：
$$
\begin{cases}
在[a,b]上连续\\
在(a,b)内可导\\
(\ln x)'\neq 0
\end{cases}
$$
则由柯西中值定理$\Rightarrow$
$\exists \xi\in(a,b)$，使得：
$$\frac{f(b)-f(a)}{\ln b - \ln a}=\frac{f'(\xi)}{(\ln \xi)'}$$
即
$$f(b)-f(a)=\xi\ln\frac{b}{a}f'(\xi)$$
（证）

---

# I 中值定理_第11页.png

## 定理9（泰勒公式）

### 带拉格朗日余项的n阶泰勒公式
（此公式适用于区间$[a,b]$，常在证明时使用，如：证明不等式、中值等式等）

设$f(x)$在点$x_0$的某个区间邻域内$n+1$阶导数存在，则：
$$
f(x) = f(x_0) + f'(x_0)(x-x_0) + \dots + \frac{1}{n!}f^{(n)}(x_0)(x-x_0)^n + \frac{f^{(n+1)}(\xi)}{(n+1)!}(x-x_0)^{n+1}
$$
其中，$\xi$介于$x$与$x_0$之间。

---

### 带佩亚诺余项的n阶泰勒公式
（此公式仅适用于点$x=x_0$及其邻域，常用于研究点$x=x_0$处的局部结论，如：求极限、判定无穷小的阶数、判定极值等）

设$f(x)$在点$x_0$处$n$阶可导，则存在$x_0$的一个局部邻域，对于该邻域内的任意点$x$有：
$$
f(x) = f(x_0) + f'(x_0)(x-x_0) + \dots + \frac{1}{n!}f^{(n)}(x_0)(x-x_0)^n + o\left((x-x_0)^n\right)
$$

---

# I 中值定理_第12页.png

## 麦克劳林公式
注1：当$x_0=0$时的泰勒公式称为麦克劳林公式。
带拉格朗日余项的麦克劳林公式：
$$f(x) = f(0) + f'(0)x + \frac{f''(0)}{2!}x^2 + \dots + \frac{f^{(n)}(0)}{n!}x^n + \frac{f^{(n+1)}(\xi)}{(n+1)!}x^{n+1}$$
（其中，$\xi$介于$0$和$x$之间）
带佩亚诺余项的麦克劳林公式：
$$f(x) = f(0) + f'(0)x + \frac{f''(0)}{2!}x^2 + \dots + \frac{f^{(n)}(0)}{n!}x^n + o(x^n)$$
注2：n个重要的函数的麦克劳林展开式
- $$e^x = 1 + x + \frac{1}{2!}x^2 + \dots + \frac{1}{n!}x^n + o(x^n)$$
- $$\sin x = x - \frac{x^3}{3!} + \dots + (-1)^n \frac{x^{2n+1}}{(2n+1)!} + o(x^{2n+1})$$
- $$\cos x = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \dots + (-1)^n \frac{x^{2n}}{(2n)!} + o(x^{2n})$$
- $$\frac{1}{1-x} = 1 + x + x^2 + \dots + x^n + o(x^n)$$
- $$\frac{1}{1+x} = 1 - x + x^2 - \dots + (-1)^n x^n + o(x^n)$$
- $$\ln(1+x) = x - \frac{x^2}{2} + \frac{x^3}{3} - \dots + (-1)^{n-1} \frac{x^n}{n} + o(x^n)$$
- $$(1+x)^\alpha = 1 + \alpha x + \frac{\alpha(\alpha-1)}{2!}x^2 + \dots + \frac{\alpha(\alpha-1)\cdots(\alpha-n+1)}{n!}x^n + o(x^n)$$

---

# I 中值定理_第13页.png

## 例6.13
设函数$f(x)$在区间$[-1,1]$上具有三阶连续导数，且$f(-1)=0$，$f(1)=1$，$f'(0)=0$，证明：
在区间$(-1,1)$内至少存在一点$\xi$，使$f'''(\xi)=3$。

一般遇到$f$与$f^{(n)}(n\geq2)$的关系，考虑泰勒公式或麦克劳林公式。
带拉格朗日余项的泰勒公式为：
$$f(x)=f(x_0)+f'(x_0)(x-x_0)+\frac{f''(x_0)}{2!}(x-x_0)^2+\frac{f'''(\xi)}{3!}(x-x_0)^3$$
取$x_0=0$，此时$\xi$位于$0$与$x$之间，分别代入$x=-1,1$：
① 代入$x=-1$：
$$0 = f(-1) = f(0)+f'(0)\cdot(-1)+\frac{f''(0)}{2!}+\frac{f'''(\xi_1)}{3!}(-1)^3$$
其中$\xi_1\in(-1,0)$。
② 代入$x=1$：
$$1 = f(1) = f(0)+f'(0)\cdot1+\frac{f''(0)}{2!}+\frac{f'''(\xi_2)}{3!}\cdot1^3$$
其中$\xi_2\in(0,1)$。

$$②-①:\ 1 = \frac{1}{6}\left[f'''(\xi_1)+f'''(\xi_2)\right]$$
$$\implies f'''(\xi_1)+f'''(\xi_2)=6$$

以下用介值定理：
$\because f(x)$在$[-1,1]$上三阶导数连续，即$f'''(x)$在闭区间上连续，设$m,M$分别为$f'''(x)$在$[-1,1]$上的最小值和最大值，则：
$$m \leq f'''(x) \leq M$$
因此：
$$m \leq f'''(\xi_1) \leq M$$
$$m \leq f'''(\xi_2) \leq M$$
两式相加得：
$$2m \leq f'''(\xi_1)+f'''(\xi_2) \leq 2M$$
两边除以2得：
$$m \leq \frac{f'''(\xi_1)+f'''(\xi_2)}{2} \leq M$$
代入$f'''(\xi_1)+f'''(\xi_2)=6$，即$m\leq 3\leq M$，由闭区间连续函数的介值定理：
$$\implies \exists \xi\in[\xi_1,\xi_2]\subset[-1,1]$$
使$f'''(\xi)=3$。

---

# I 中值定理_第14页.png

## 牛顿插值法
设直线$f(x)$中，$y_1=f(x_1),\ y_2=f(x_2)$，我们知道了两个点的函数值，用中学的知识，写出$f(x)$的直线方程：
$$\frac{y-y_1}{x-x_1} = \frac{y_2-y_1}{x_2-x_1}$$
$$\Rightarrow f(x) = \frac{y_2-y_1}{x_2-x_1}(x-x_1) + y_1$$

用牛顿插值法写$f(x)$，其实就是换了个角度，和前面推导泰勒公式的思想相似。
要设出一个$f(x)$，使其满足
$$\begin{cases}
y_1 = f(x_1) \\
y_2 = f(x_2)
\end{cases}$$

① 先让$f(x)$满足$y_1=f(x_1)$
$$\Rightarrow f(x) = y_1$$

② 再让$f(x)$满足
$$\begin{cases}
y_1 = f(x_1) \\
y_2 = f(x_2)
\end{cases}$$

设方程：
$$f(x) = y_1 + a(x-x_1)$$
代入条件得：
$$y_2 = y_1 + a(x_2-x_1) \quad (\text{让}f(x)=y_2,\ x=x_2\text{解出}a)$$
解得：
$$a = \frac{y_2-y_1}{x_2-x_1}$$
$$\Rightarrow f(x) = y_1 + \frac{y_2-y_1}{x_2-x_1}(x-x_1)$$

③ 若还有$y_3$，则让$f(x)$满足
$$\begin{cases}
y_1 = f(x_1) \\
y_2 = f(x_2) \\
y_3 = f(x_3)
\end{cases}$$

---

# I 中值定理_第15页.png

## 牛顿插值多项式构造
设方程：
$$f(x) = y_1 + \frac{y_2-y_1}{x_2-x_1}(x-x_1) + b(x-x_1)(x-x_2)$$
令$x=x_3$时$f(x_3)=y_3$，解出$b$：
$$y_3 = y_1 + \frac{y_2-y_1}{x_2-x_1}(x_3-x_1) + b(x_3-x_1)(x_3-x_2)$$
解出$b$。
④ 若还有$y_4=f(x_4)$，则继续增设项，解出$c$；
无限循环下去。
给出$f(x)$的点越多，得出的方程就越接近$f(x)$。

* 公式的推导逻辑和泰勒公式很像：
两者都是用来拟合函数的，即用多项式去拟合一个函数$f(x)$，只是牛顿插值法用的是离散的点。

## 方法扩展：牛顿插值与泰勒公式联合
### 例6.9（以多项式来替代$f(x)$）
设函数$f(x)$在$[0,1]$上二阶可导，$f(0)=f(1)=0$，
当$x\in[0,1]$时，$f(x)$的最小值为$-1$，证明：
$$\exists \xi \in (0,1),\ \text{使得}\ f''(\xi)\geqslant 8$$

[分析]：发现这类题的规律：
例6.13的条件：$f(-1)=0,\ f(1)=1,\ f'(0)=0$
这一题的条件：$f(0)=0,\ f(1)=0,\ f(x_0)=-1$
再任举一例子：$f(0)=0,\ f(1)=1,\ \int_0^1 f(x)dx=\frac{2}{3}$

解决这类问题，我们可以用牛顿插值法与泰勒公式联合。
核心思想：泰勒公式与牛顿插值法的推导逻辑方法。

---

# I 中值定理_第16页.png

## 牛顿插值结合罗尔定理证明
证明：用牛顿插值法拟合$f(x)$，要求插值结果满足$f(0)=0$，$f(1)=0$，$f(x_0)=-1$，对应三个插值节点的函数值$f(x_1)=y_1$，$f(x_2)=y_2$，$f(x_3)=y_3$。
设二次插值多项式形式为：
$$f(x) = y_1 + \frac{y_2 - y_1}{x_2 - x_1}(x - x_1) + b(x - x_1)(x - x_2)$$
代入$x_1=0,y_1=0$，$x_2=1,y_2=0$与$f(x_0)=-1$：
$$f(x_0) = -1 = 0 + \frac{0-0}{1-0}(x_0 - 0) + b(x_0 - 0)(x_0 - 1)$$
化简得：
$$-1 = b x_0 (x_0 - 1)$$
解得系数：
$$b = \frac{1}{x_0(1 - x_0)}$$
因此得到插值多项式：
$$f(x) = \frac{1}{x_0(1 - x_0)} x(x-1)$$
因为该式仅满足了$f(x)$在3个节点处的取值，因此这个插值得到的$f(x)$与真实的$f(x)$之间存在误差。
构造误差辅助函数：
令
$$F(x) = f(x) - \frac{1}{x_0(1 - x_0)} x(x-1)$$
$F(x)$就是插值近似存在的误差项。
计算$F(x)$在三个节点处的函数值：
$$F(0) = f(0) - 0 = 0$$
$$F(1) = f(1) - 0 = 0$$
$$F(x_0) = -1 - (-1) = 0$$
两次应用罗尔定理：
（零点分布示意图：展示$F(x)$的三个零点$0,x_0,1$，以及各阶导函数零点的位置关系）
因为$F(0) = F(x_0) = 0$，$F(1) = F(x_0) = 0$，所以：
- $\exists \xi_1 \in (0, x_0)$，使得$F'(\xi_1) = 0$；
- $\exists \xi_2 \in (x_0, 1)$，使得$F'(\xi_2) = 0$。
又因为$F'(\xi_1) = F'(\xi_2) = 0$，所以：
$$\exists \xi \in (\xi_1, \xi_2),\ \text{使得}\ F''(\xi) = 0$$

---

# I 中值定理_第17页.png

## 证明推导
$$F''(x) = f''(x) - \frac{2}{x_0(1-x_0)}$$
$$\Rightarrow F''(\xi) = f''(\xi) - \frac{2}{x_0(1-x_0)} = 0$$
$$f''(\xi) = \frac{2}{x_0(1-x_0)}$$
$\because x_0 \in (0,1)$
$\therefore 1-x_0 \in (0,1)$
由基本不等式$\sqrt{ab} \leq \frac{a+b}{2}$，可得：
$$x_0(1-x_0) \leq \frac{1}{4}$$
$$\Rightarrow \frac{1}{x_0(1-x_0)} \geq 4$$
$$\frac{2}{x_0(1-x_0)} \geq 8$$
$$\Rightarrow \exists \xi \in (0,1), 使f''(\xi) \geq 8$$

## 定理关联示意图
以$f(x)$为核心的定理联系如下：
1.  向左上连接变上限积分$\int_a^x f(t)dt$，对应定理：拉格朗日中值定理
2.  向左下连接定积分$\int_a^b f(x)dx$，对应内容：定积分/积分中值定理
3.  向右依次连接一阶导数$f'(x)$、$n$阶导数$f^{(n)}(x) \ (n\geq2)$
4.  经弧形箭头向右上连接$n$阶导数$f^{(n)}(x) \ (n\geq2)$，对应定理：泰勒公式