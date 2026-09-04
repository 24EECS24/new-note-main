---

# E 夹逼准则与单调有界准则_第1页.png

## 夹逼准则（不等思想）
不用管等号
如果数列$\{x_n\}$、$\{y_n\}$及$\{c_n\}$满足下列条件：
1.  （夹）① 从某项起，即存在$n_0 \in \mathbf{N}_+$，当$n>n_0$时
    $$y_n \leq x_n \leq c_n,\quad n=1,2,3,\cdots$$
    $\left.\begin{array}{cc}
    \leq & < \\
    < & \leq \\
    < & <
    \end{array}\right\}$都行，不需要验证等号
2.  （逼）②
    $$\lim_{n \to \infty} y_n = a,\quad \lim_{n \to \infty} c_n = a$$

则$\{x_n\}$的极限存在/收敛，且$\lim\limits_{n \to \infty} x_n = a$。
$$\begin{matrix}
y_n & < & x_n & < & c_n \\
\downarrow & & \Downarrow & & \downarrow \\
a & \Rightarrow & a & \Leftarrow & a
\end{matrix}$$

注：放缩常用的方法

## 方法1 利用简单的放大、缩小
$$u_1+u_2+\cdots+u_n$$
$$\Downarrow$$
$$n\cdot u_{\text{min}} \leq u_1+u_2+\cdots+u_n \leq n\cdot u_{\text{max}}$$
（用于无穷项相加，$n \to \infty$）

### 例2.9
$$\lim_{n \to \infty} \left( \frac{1}{n^2+n+1} + \frac{2}{n^2+n+2} + \cdots + \frac{n}{n^2+n+n} \right) = \underline{\quad}$$
相当于是求通项为$\{a_i\} = \frac{i}{n^2+n+i}$的数列的前$n$项和。
∵分母越大，数越小
∴要让所有项的分母都为$n^2+n+n$，则加出来的为$\min$，即
$$f(n)_{\text{min}} = \frac{\frac{(1+n)n}{2}}{n^2+n+n}$$
同理，让所有项的分母都为$n^2+n+1$，然后加出来的为$\max$，即
$$f(n)_{\text{max}} = \frac{\frac{(1+n)n}{2}}{n^2+n+1}$$
$$\Rightarrow \frac{\frac{(1+n)n}{2}}{n^2+n+n} < \frac{1}{n^2+n+1} + \frac{2}{n^2+n+2} + \cdots + \frac{n}{n^2+n+n} < \frac{\frac{(1+n)n}{2}}{n^2+n+1}$$

---

# E 夹逼准则与单调有界准则_第2页.png

$$\lim_{n \to \infty} \frac{\frac{(1+n)n}{2}}{n^2+n+n} = \lim_{n \to \infty} \frac{n^2+n}{2n^2+4n} = \frac{1}{2}$$
$$\lim_{n \to \infty} \frac{\frac{(1+n)n}{2}}{n^2+n+1} = \lim_{n \to \infty} \frac{n^2+n}{2n^2+2n+2} = \frac{1}{2}$$

则对和式有放缩：
$$\frac{\frac{n(n+1)}{2}}{n^2+n+n} < \sum_{i=1}^n \frac{i}{n^2+n+i} < \frac{\frac{n(n+1)}{2}}{n^2+n+1}$$
不等式两端在$n\to\infty$时极限均为$\frac{1}{2}$，由夹逼准则可得：
$$\lim_{n\to\infty}\sum_{i=1}^n \frac{i}{n^2+n+i} = \frac{1}{2}$$

---

> 重点结论：当$u_1+u_2+u_3+\dots+u_n \geq 0$时，
> $$1\cdot u_{\text{max}} \leq u_1+u_2+\dots+u_n \leq n\cdot u_{\text{max}}$$
> 注：该放缩适用于有限项相加的情形。
> （手写标注疑问：此处$n$是否可取实数？解题疑问请记下来。）

---

## 例2.10
求极限：
$$\lim_{n \to \infty} \sqrt[n]{a_1^n + a_2^n + \dots + a_m^n}$$
其中$m$为给定实常数，$a_1^n,a_2^n,\dots,a_m^n$均为非负数。

解：设$a = \max\{a_1,a_2,\dots,a_m\}$，通俗来说，$a$是$a_1,a_2,\dots,a_m$中的最大项。

对被开方的和式做放缩：
$$\sqrt[n]{a^n} \leq \sqrt[n]{a_1^n+a_2^n+\dots+a_m^n} \leq \sqrt[n]{m\cdot a^n}$$
（手写标注：原手写此处误将系数写为$n$，自注疑问：求和共$m$项，不是乘$m$？？？ 标注该题此步解法存疑。）

---

# E 夹逼准则与单调有界准则_第3页.png

## 例2.10：n次和开n次方的极限题型
例2.10展开讲解一类极限题型：$\lim\limits_{n \to \infty} \sqrt[n]{\square^n + \triangle^n}$
此类题型的通用结论：
$$\lim_{n \to \infty} \sqrt[n]{\square^n + \triangle^n} = \max\left\{ \square, \triangle \right\}$$
---
### 例题1：负指数幂情形
当$0<a<b$时，计算$\lim\limits_{n \to \infty} \left( a^{-n} + b^{-n} \right)^{\frac{1}{n}}$
#### 推导过程（夹逼准则）：
由$0<a<b$可得$\frac{1}{a} > \frac{1}{b} > 0$，对两项和做放缩：
$$1\cdot a^{-n} < a^{-n} + b^{-n} < 2a^{-n}$$
对不等式三边同时开$n$次方：
$$\left(1\cdot a^{-n}\right)^{\frac{1}{n}} < \left(a^{-n} + b^{-n}\right)^{\frac{1}{n}} < \left(2 a^{-n}\right)^{\frac{1}{n}}$$
分别计算两侧在$n\to\infty$时的极限：
1.  左侧：$\left(a^{-n}\right)^{\frac{1}{n}} = \frac{1}{a}$，极限为$\frac{1}{a}$
2.  右侧：$\left(2 a^{-n}\right)^{\frac{1}{n}} = 2^{\frac{1}{n}} \cdot \frac{1}{a}$；当$n\to\infty$时$\frac{1}{n}\to0$，故$2^{\frac{1}{n}}\to1$，因此$2^{\frac{1}{n}}\cdot \frac{1}{a} \to \frac{1}{a}$，即右侧极限为$\frac{1}{a}$
由夹逼准则可得：
$$\lim_{n \to \infty} \left( a^{-n} + b^{-n} \right)^{\frac{1}{n}} = \frac{1}{a}$$
也可直接套用通用结论验证：因$\frac{1}{a}>\frac{1}{b}>0$，故$\max\left\{ \frac{1}{a}, \frac{1}{b} \right\} = \frac{1}{a}$，与推导结果一致。
---
### 例题2：三角函数变形
eg：变形2
当$0 \leq x \leq \frac{\pi}{2}$时，计算$\lim\limits_{n \to \infty} \sqrt[n]{\sin^n x + \cos^n x}$
根据通用结论，结果为$\max\left\{ \sin x, \cos x \right\}$。
（函数示意图：在$0\leq x\leq \frac{\pi}{2}$区间内绘制$\sin x$与$\cos x$的图像，两曲线交于$x=\frac{\pi}{4}$处，纵轴截距均为1，标注了原点$O$、交点横坐标$\frac{\pi}{4}$、区间右端点$\frac{\pi}{2}$）
结合区间内两函数的大小关系，可写为分段函数：
$$\max\left\{ \sin x, \cos x \right\} =
\begin{cases}
\cos x, & 0\leq x \leq \frac{\pi}{4} \\
\sin x, & \frac{\pi}{4}\leq x \leq \frac{\pi}{2}
\end{cases}$$

---

# E 夹逼准则与单调有界准则_第4页.png

## eg:变形3
$$\lim_{n \to \infty} \sqrt[n]{1+|x|^{3n}} = \underline{\quad}$$
其中：
$\square = 1$，$\triangle = |x|^3$，推导得$|x|\cdot|x|\cdot|x| = |x^3| = |x|^3$。
函数示意图：$y=x^3$的图像，箭头指向变换后的$y=|x|^3$的图像；随后给出同一平面直角坐标系下$y=|x|^3$与$y=1$的图像。
推导得结果：
$$\text{结果} = \max\left\{\square, \triangle\right\}$$
写成分段函数形式：
$$
=
\begin{cases}
-x^3, & x < -1 \\
1, & |x| \leq 1 \\
x^3, & x > 1
\end{cases}
$$

## 方法2 利用重要不等式
- 设$a,b$为实数，则：
  ① $|a \pm b| \leq |a| + |b|$
  ② $||a| - |b|| \leq |a - b|$

可以将不等式①推广为$n$个实数的情形：
$$|a_1 \pm a_2 \pm \dots \pm a_n| \leq |a_1| + |a_2| + \dots + |a_n|$$

- 均值不等式：
  ① 二元情形（$a,b \geq 0$）：
  $$\sqrt{ab} \leq \frac{a+b}{2} \leq \sqrt{\frac{a^2+b^2}{2}}$$
  补充不等式：$|ab| \leq \frac{a^2 + b^2}{2}$
  应用举例：若$u_n > 0$，则
  $$\frac{u_n}{n} = u_n \cdot \frac{1}{n} \leq \frac{u_n^2 + \frac{1}{n^2}}{2}$$

  ② 三元情形（$a,b,c \geq 0$）：
  $$\sqrt[3]{abc} \leq \frac{a+b+c}{3} \leq \sqrt{\frac{a^2+b^2+c^2}{3}}$$

- 幂函数单调性不等式：
设$a > b \geq 0$，则
$$
\begin{cases}
a^m \geq b^m, & m>0 \\
a^m \leq b^m, & m<0
\end{cases}
$$

---

# E 夹逼准则与单调有界准则_第5页.png

若$0<a<x<b$，则
$$0<\frac{1}{b}<\frac{1}{x}<\frac{1}{a}$$
若同时满足$0<c<y<d$，则可推出
$$\frac{c}{b}<\frac{y}{x}<\frac{d}{a}$$

## 2.3 夹逼准则求极限
当$n\leq x <n+1$（$x\to+\infty$时$n\to\infty$，$n$为正整数）时，$2n\leq f(x)<2(n+1)$，求$\lim\limits_{x\to+\infty}\frac{f(x)}{x}$。

解：对不等式做放缩，由$n\leq x <n+1$可得$\frac{1}{n+1}<\frac{1}{x}\leq\frac{1}{n}$，结合$f(x)$的取值范围得：
$$\frac{2n}{n+1}<\frac{f(x)}{x}<\frac{2(n+1)}{n}$$
当$x\to+\infty$时$n\to\infty$：
- 左侧：$\frac{2n}{n+1}\approx\frac{2n}{n}=2$，因此$\lim\limits_{n\to\infty}\frac{2n}{n+1}=2$
- 右侧：$\frac{2(n+1)}{n}=\frac{2n+2}{n}\approx\frac{2n}{n}=2$，因此$\lim\limits_{n\to\infty}\frac{2(n+1)}{n}=2$

由夹逼准则，两侧极限均为2，因此：
$$\lim_{x\to+\infty}\frac{f(x)}{x}=2$$

## 常用三角与反三角函数不等式
1.  $$\sin x < x < \tan x,\quad 0<x<\frac{\pi}{2}$$
    对应函数示意图：绘制了原点附近$y=\sin x$、$y=x$、$y=\tan x$的图像。
2.  $$\sin x < x,\quad x>0$$
3.  当$0<x<\frac{\pi}{4}$时，$x<\tan x<\frac{4}{\pi}x$
    注：该结论可先行使用，证明见例6.9。
4.  当$0<x<\frac{\pi}{2}$时，$\sin x>\frac{2}{\pi}x$
    注：该结论可先行使用，证明见例6.19。
5.  $$\arctan x \leq x \leq \arcsin x,\quad 0\leq x\leq 1$$
    对应函数示意图：绘制了区间$[0,1]$上$y=\arcsin x$、$y=x$、$y=\arctan x$的图像。

---

# E 夹逼准则与单调有界准则_第6页.png

## 常用不等式
1.  对任意实数$x$，成立$e^x \geqslant x+1$
    对应函数示意图：平面直角坐标系中绘制了$y=e^x$与$y=x+1$的函数图像。
2.  对$x>0$，成立$x-1 \geqslant \ln x$
    对应函数示意图：平面直角坐标系中绘制了$y=x-1$与$y=\ln x$的函数图像。
3.  对$x>0$，成立不等式组：
    $$\frac{1}{1+x} < \ln\left(1+\frac{1}{x}\right) < \frac{1}{x}$$
    $$\frac{x}{1+x} < \ln(1+x) < x$$
    备注：上述不等式可直接应用，相关证明将在拉格朗日中值定理部分给出。

## 数列收敛的证明方法
- 方法3：利用闭区间上连续函数必存在最大值、最小值的性质证明
- 方法4：利用压缩映射原理证明

### 2.8 证明方法4：压缩映射原理
**定理内容**：若对于数列$\{x_n\}$，存在常数$k\ (0<k<1)$，使得对任意正整数$n=1,2,3,\cdots$，满足
$$|x_{n+1} - a| \leqslant k|x_n - a|$$
则数列$\{x_n\}$收敛于$a$。

**证明过程**：
由递推条件$0 \leqslant |x_{n+1} - a| \leqslant k|x_n - a|$，对不等式逐次递推可得：
$$
\begin{align*}
0 \leqslant |x_{n+1} - a| &\leqslant k|x_n - a| \leqslant k^2|x_{n-1} - a| \\
&\leqslant k^3|x_{n-2} - a| \leqslant \cdots \leqslant k^n|x_1 - a|
\end{align*}
$$
当$n \to \infty$时，由于$k \in (0,1)$，因此$\lim_{n\to\infty}k^n = 0$，进而$\lim_{n\to\infty}k^n|x_1 - a| = 0$。
根据夹逼准则，对不等式
$$0 \leqslant |x_{n+1} - a| \leqslant k^n|x_1 - a|$$
两端同时取$n \to \infty$的极限，不等式两端极限均为0，因此
$$\lim_{n \to \infty} |x_{n+1} - a| = 0 \implies \lim_{n \to \infty} x_{n+1} = a$$
当$n \to \infty$时，$n$与$n+1$的极限趋势一致，因此$\lim_{n \to \infty} x_n = a$，即数列$\{x_n\}$收敛于$a$。

---

# E 夹逼准则与单调有界准则_第7页.png

## 2.7 对不等式的考察
设数列$\{x_n\}$满足$x_{n+1}=\ln x_n +1$，$x_n>0,\ n=1,2,3,\cdots$，则$\{x_n\}$（B）
A. 单调不减
B. 单调不增
C. 严格单增
D. 严格单减

当$x>0$时，成立不等式：
$$x-1\geq \ln x$$
即$x\geq \ln x +1$，等号当且仅当$x=1$时成立。
（函数示意图：平面直角坐标系中绘制了$y=x-1$与$y=\ln x$的图像，两曲线在$x=1$处相切）

由不等式对所有正实数成立，可得递推关系：
$$x_{n+1}=\ln x_n +1 \leq x_n$$
$\implies$ 对所有正整数$n$，$x_{n+1}\leq x_n$
$\implies \{x_n\}$单调不增

{注}
若$x_1=1$，则$\{x_n\}$为常数数列，每一项均为1，即$1,1,1,1,\cdots$，为不增不减数列。

---

## 2.11
设$a_n>0$，$\lim\limits_{n\to\infty}b_n=0$，且$e^{a_n}+a_n = e^{b_n}$，$n=1,2,\cdots$，求$\lim\limits_{n\to\infty}a_n$。

解：对原式移项得：
$$e^{a_n}-e^{b_n}=-a_n<0$$
因此$e^{a_n}<e^{b_n}$，结合$y=e^x$的严格单调递增性，可得：
$$0<a_n<b_n$$
（函数示意图：平面直角坐标系中绘制了$y=e^x$的函数图像）
由夹逼准则，结合$\lim\limits_{n\to\infty}b_n=0$，可得：
$$\lim_{n\to\infty}a_n=0$$

---

# E 夹逼准则与单调有界准则_第8页.png

## 单调有界准则
单调有界数列必有极限。
即：若数列$\{x_n\}$单调增加（减少），且有上界（下界），则$\lim\limits_{n \to \infty} x_n$存在。

1.  单调递增且有上界：
    $$\underbrace{x_n \leq x_{n+1}}_{\text{单调递增}} \underbrace{\leq a}_{\text{有上界}} \implies \lim_{n \to \infty} x_n \exists$$
2.  单调递减且有下界：
    $$\underbrace{a \leq x_{n+1}}_{\text{有下界}} \underbrace{\leq x_n}_{\text{单调递减}} \implies \lim_{n \to \infty} x_n \exists$$

---

## 证明数列$\{x_n\}$单调性的方法
- 作差法与作商法：
  $$x_{n+1}-x_n \begin{cases}
  >0, & \text{单调递增} \\
  <0, & \text{单调递减}
  \end{cases}, \quad \frac{x_{n+1}}{x_n} \begin{cases}
  >1, & \text{单调递增} \\
  <1, & \text{单调递减}
  \end{cases}$$
- 利用数学归纳法（结合题目条件证明）
- 利用重要不等式（相关结论可参考夹逼准则部分）
- 若$x_n - x_{n-1}$与$x_{n-1} - x_{n-2}$同号，则数列$\{x_n\}$单调。
- 对于递推数列$x_{n+1}=f(x_n) \ (n=1,2,\dots)$，且$x_n$属于区间$I$：
  - 若对任意$x \in I$有$f'(x)>0$，则数列$\{x_n\}$单调，且：
    $$\begin{cases}
    \text{当}x_2 > x_1\text{时，数列}\{x_n\}\text{单调递增} \\
    \text{当}x_2 < x_1\text{时，数列}\{x_n\}\text{单调递减}
    \end{cases}$$
  - 若对任意$x \in I$有$f'(x)<0$，则数列$\{x_n\}$不单调。

证明见例2.13与例2.15。

---

# E 夹逼准则与单调有界准则_第9页.png

## 例2.12
设$0<x_1<3$，$x_{n+1}=\sqrt{x_n(3-x_n)} \quad (n=1,2,\cdots)$，证明数列$\{x_n\}$极限存在，并求此极限。

**解：**
由例2.1的结论，结合均值不等式$\sqrt{ab}\le \frac{a+b}{2}$，可知$\{x_n\}$有上界$\frac{3}{2}$，即：
$$0 < x_n \le \frac{3}{2},\quad n=2,3,4,\cdots$$

接下来证明数列单调性：数列已有上下界，采用作差法判断增减性：
$$
\begin{align*}
x_{n+1}-x_n &= \sqrt{x_n(3-x_n)} - x_n \\
&= \sqrt{x_n}\left(\sqrt{3-x_n} - \sqrt{x_n}\right)
\intertext{利用共轭根式有理化（注：$\sqrt{a}+\sqrt{b}$的共轭根式为$\sqrt{a}-\sqrt{b}$）：}
&= \sqrt{x_n} \cdot \frac{(\sqrt{3-x_n}-\sqrt{x_n})(\sqrt{3-x_n}+\sqrt{x_n})}{\sqrt{3-x_n}+\sqrt{x_n}} \\
&= \sqrt{x_n} \cdot \frac{3-2x_n}{\sqrt{3-x_n}+\sqrt{x_n}}
\end{align*}
$$
由$x_n \le \frac{3}{2}$，可得$3-2x_n \ge 0$，且$\sqrt{x_n}>0$，分母$\sqrt{3-x_n}+\sqrt{x_n}>0$，因此：
$$\sqrt{x_n} \cdot \frac{3-2x_n}{\sqrt{3-x_n}+\sqrt{x_n}} \ge 0$$
即$x_{n+1}\ge x_n$，$\{x_n\}$单调递增。

根据单调有界收敛定理，$\lim\limits_{n\to\infty}x_n$存在。当$n\to\infty$时，$x_n$与$x_{n+1}$趋于同一极限值，对递推式两边同时取极限，得到一元二次方程：
$$x = \sqrt{x(3-x)}$$
求解得$x=\frac{3}{2}$或$x=0$。

由于$\{x_n\}$单调递增、有上界，且满足$0<x_n\le \frac{3}{2}$，因此极限为0的解不符合数列性质，舍去。
（附：数列单调递增趋近于上界$\frac{3}{2}$的趋势示意图）

因此数列极限为：
$$\lim_{n\to\infty}x_n = \frac{3}{2}$$

---

# E 夹逼准则与单调有界准则_第10页.png

## 迭代法逼近极限（超越方程，这是动态的函数值）
例2.13的精华

$y_2 = x$，即$g(x_n)=x_n$；$y_1 = f(x_n) = x_{n+1}$
（单调递增迭代蛛网示意图，迭代序列演化：$x_1 \to x_2 \to x_3 \to x_4 \to \dots \to a$）
$$
\begin{align*}
f(x_1) &= y_1 = x_2 \\
x_2 &= y_2 = x_2 \\
f(x_2) &= y_1 = x_3 \\
x_3 &= y_2 = x_3 \\
f(x_3) &= y_1 = x_4 \\
x_4 &= y_2 = x_4 \\
f(x_4) &= y_1 = x_5 \\
&\vdots \\
\lim_{n \to \infty} x_n &= a
\end{align*}
$$
$x_1<x_2$，单增

$y_2 = y(x_n) = x_n$；$y_1 = f(x_n) = x_{n+1}$
（单调递减迭代蛛网示意图，迭代序列演化：$x_1 \gets x_2 \gets x_3 \gets \dots \gets a$）
$$
\begin{align*}
f(x_1) &= y_1 = x_2 \\
x_2 &= y_2 = x_2 \\
f(x_2) &= y_1 = x_3 \\
x_3 &= y_2 = x_3 \\
f(x_3) &= y_1 = x_4 \\
x_4 &= y_2 = x_4 \\
f(x_4) &= y_1 = x_5 \\
&\vdots \\
\lim_{n \to \infty} x_n &= a
\end{align*}
$$
$x_1>x_2$，单减

---

# E 夹逼准则与单调有界准则_第11页.png

## 2.11
设 $c=2\ln(1+b)$，$b>a>0$，
且 $a$ 是方程 $x-2\ln(1+x)=0$ 的唯一解，
证明 $c>a$。

$$
\begin{aligned}
c &= 2\ln(1+b) \\
a &= 2\ln(1+a) \\
f(x) &= 2\ln(1+x)
\end{aligned}
$$
（函数示意图：平面直角坐标系中过原点、单调递增的$\ln x$曲线）

$f(x)$ 严格单调递增，
$\because b>a>0$，
$\therefore 2\ln(1+b) > 2\ln(1+a)$，
$\therefore c > a$。

## 2.12
设单调递减数列 $\{x_n\}$ 满足
$$x_{n+1}=2\ln(1+x_n),\ n=1,2,3,\cdots,\quad x_1>a>0$$
且 $a$ 是方程 $x-2\ln(1+x)=0$ 的唯一解，
证明 $\{x_n\}$ 收敛。

由$a$是方程的解，可得：
$$a=2\ln(1+a)$$
数列递推关系为：
$$x_{n+1}=2\ln(1+x_n)$$

$\because x_1>a>0$，且$f(x)=2\ln(1+x)$严格单调递增，
$\therefore$ 由数学归纳法可得 $x_{n+1} > a$；
结合数列单调递减的条件，有 $x_n > x_{n+1} > a$，即 $\{x_n\}$ 有下界$a$。

$\because \{x_n\}$ 单调递减且有下界，
$\therefore$ 根据单调有界收敛定理，$\lim\limits_{n\to\infty} x_n$ 存在，即 $\{x_n\}$ 收敛。