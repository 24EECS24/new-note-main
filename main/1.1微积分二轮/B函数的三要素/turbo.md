---
tags:
  - 微积分
  - 一元函数微分学
  - 反函数
  - 隐函数
  - 导数计算
aliases:
  - 反函数与隐函数求导
cssclass: null
---
# 📘 反函数与隐函数的求导

> [!info] 章节导航
> - **一、反函数**
>   - 1.1 反函数的定义
>   - 1.2 反函数的存在条件 ⚠️
>   - 1.3 反函数的几何意义
>   - 1.4 反函数的基本性质
>   - 1.5 微分算子与二阶微分（求导预备）
>   - 1.6 反函数的求导（核心考点）
>   - 1.7 基本初等函数的反函数求导（必背公式）
>   - 1.8 反函数典型例题
> - **二、隐函数**
>   - 2.1 显函数与隐函数
>   - 2.2 隐函数存在定理（了解）
>   - 2.3 隐函数求导方法（核心考点）
>   - 2.4 隐函数求导典型例题
>   - 2.5 对数求导法（隐函数思想的应用）⭐
>   - 2.6 由参数方程确定的函数的求导
> - **三、公式速查表 & 易错点总结**

> [!tip] 心得：从小到大，数学运算对象在升级
> | 运算对象 | 运算符 |
> |:-------:|:------|
> | 数      | $\xrightarrow{\text{加减、乘除…}}$ 数 |
> | 数组    | $\xrightarrow{f(x)}$ 数组 |
> | 函数    | $\xrightarrow{D(f)}$ 函数 |

---

# 一、反函数

## 1.1 反函数的定义

设函数 $y=f(x)$ 的定义域为 $D$，值域为 $R_f$（用 $R_f$ 避免与实数集 $\mathbb{R}$ 混淆）。

> [!important] 定义
> 如果对**每个** $y\in R_f$，都存在**唯一**的 $x\in D$ 使得 $y=f(x)$ 成立，则这个对应关系定义了一个新函数
> $$x = f^{-1}(y)$$
> 称为 $y=f(x)$ 的**反函数**。

**本质理解**：自变量与因变量"换职位"。
- 原映射：$x$（自变量）$\xrightarrow{f}$ $y$（因变量）
- 逆映射：$y$（自变量）$\xrightarrow{f^{-1}}$ $x$（因变量）

**互逆映射（环形还原）**：

```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[row sep=1.5em, column sep=3.0em]
x \arrow[rr, "f(\,)"] & & y \arrow[ld, "f^{-1}(\,)"'] \\
 & x \arrow[lu, "=" description, no head] &
\end{tikzcd}
\end{document}
```

还原性质：
$$f^{-1}\!\big[f(x)\big] = x,\qquad f\!\big[f^{-1}(y)\big] = y$$

> [!note] 多层可逆映射的复合
> $$像_1 \xrightleftharpoons[f^{-1}]{f} 像_2 \xrightleftharpoons[g^{-1}]{g} 像_3$$
> ⚠️ 复合逆的反序法则：$(g\circ f)^{-1} = f^{-1}\circ g^{-1}$，不同映射要用不同字母表示。

---

## 1.2 反函数的存在条件 ⚠️

> [!important] 反函数存在条件
> - **一般情况**：$f$ 是**双射**（一一对应），即每个 $y\in R_f$ 恰对应唯一 $x\in D$。
> - **连续函数（常考）**：在区间上 $f$ 存在反函数 $\iff$ $f$ **严格单调**（严格递增 或 严格递减）。

> [!warning] 两大误区（高频扣分点）
> 1. **必须说"严格单调"**。"单调"包括单调不减/不增，例如常函数 $y=C$ "单调不减"但没有反函数。
> 2. **$f'(x)\neq 0$ 不是反函数存在的条件**，它是反函数**可导**的条件（见 1.6 节）。
>    - 反例：$y=x^3$ 在 $\mathbb{R}$ 上严格递增，存在反函数 $x=\sqrt[3]{y}$，但 $f'(0)=0$（反函数在 $y=0$ 处不可导，表现为垂直切线）。

**几何判断法**：若函数图像与任意水平线至多交于一点（**水平线测试**），则存在反函数。

**没有反函数的典型**：
- **非单调函数**（如 $y=x^2$ 在 $\mathbb{R}$ 上）：一个 $y$ 对应多个 $x$，交换 $x,y$ 后变成"一个 $x$ 对应多个 $y$"，违反函数定义。
  - 但在 $[0,+\infty)$ 上 $y=x^2$ 严格递增，有反函数 $y=\sqrt{x}$；
  - 在 $(-\infty,0]$ 上严格递减，有反函数 $y=-\sqrt{x}$。
- **常函数** $y=C$：一个 $y$ 对应所有 $x$。

---

## 1.3 反函数的几何意义

--- start-multi-column: geo-meaning
```column-settings
number of columns: 2
largest column: left
border: off
```

- 将直接函数写成 $y=f(x)$，反函数**习惯上**也写为 $y=f^{-1}(x)$（自变量仍用 $x$），则两者图像**关于直线 $y=x$ 对称**。
- $x=f^{-1}(y)$ 与 $y=f(x)$ 在同一坐标系下是**同一条曲线**；只有写成 $y=f^{-1}(x)$ 才是关于 $y=x$ 的对称图形。
- **切线斜率关系**：若 $f$ 在 $(a,b)$ 处切线斜率为 $k=f'(a)$，则反函数在对称点 $(b,a)$ 处切线斜率为 $1/k$（互为倒数），这正是反函数导数公式的几何意义。

--- end-column ---

```tikz
\usepackage{tikz}
\begin{document}
\begin{tikzpicture}[scale=1.0, >=stealth, domain=-0.3:2.5, samples=100]
  \draw[->] (-0.3,0) -- (3.0,0) node[right] {$x$};
  \draw[->] (0,-0.3) -- (0,3.0) node[above] {$y$};
  \draw[thick, red] plot (\x, {0.6*\x*\x+0.4}) node[above right, black, font=\small] {$y=f(x)$};
  \draw[thick, blue] plot ({0.6*\x*\x+0.4}, \x) node[below right, black, font=\small] {$y=f^{-1}(x)$};
  \draw[dashed, gray] (-0.3,-0.3) -- (3.0,3.0) node[midway, below right, black, font=\small] {$y=x$};
  \fill (0.8,0.784) circle (1.5pt) node[below left, font=\scriptsize] {$(a,b)$};
  \fill (0.784,0.8) circle (1.5pt) node[above right, font=\scriptsize] {$(b,a)$};
\end{tikzpicture}
\end{document}
```

--- end-multi-column

---

## 1.4 反函数的基本性质

| 性质 | 结论 |
|:----:|:-----|
| 定义域与值域互换 | $D_{f^{-1}} = R_f,\quad R_{f^{-1}} = D_f$ |
| 严格单调性一致 | $f$ 严格增 $\Rightarrow f^{-1}$ 严格增；$f$ 严格减 $\Rightarrow f^{-1}$ 严格减 |
| 奇偶性 | 奇函数若存在反函数，则 $f^{-1}$ 也是奇函数；偶函数一般不存在反函数 |
| 复合还原 | $f^{-1}[f(x)]=x\ (\forall x\in D)$；$f[f^{-1}(y)]=y\ (\forall y\in R_f)$ |
| 反函数的反函数 | $(f^{-1})^{-1} = f$ |

> [!note] 反函数连续性定理（补充）
> 若 $y=f(x)$ 在区间 $I$ 上**严格单调且连续**，则其反函数 $x=f^{-1}(y)$ 在对应区间上也**严格单调且连续**。
> 这是反函数可导性的前提——先连续，再谈可导。

---

## 1.5 微分算子与二阶微分（求导预备）

### 微分算子 $D$
将求导视为"吃进函数、吐出函数"的算子：
$$D(\,) = \frac{d(\,)}{dx}$$

- 一次作用：$f \xrightarrow{D} f'$
- 逐次复合得到高阶导：
  $$f \xrightarrow{D} f' \xrightarrow{D} f''$$
  $$D^2(\,) = D\big[D(\,)\big] = \frac{d^2(\,)}{dx^2}$$

**微分算子与逆算子关系图**：

```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[row sep=2.0em, column sep=3.5em]
f \arrow[rr, "D(\,)"] \arrow[rrdd, "D^2(\,)"'] & & f' \arrow[rr, "D(\,)"] \arrow[ld, "D^{-1}(\,)"'] & & f'' \arrow[ldd, "D^{-1}\circ D^{-1}"'] \\
 & f(+C) & & f'(+C) & \\
 & & f(+C_1+C_2) & &
\end{tikzcd}
\end{document}
```

### 逆微分算子（积分）
$$D^{-1}(\,) = \int(\,)\,dx$$

> [!warning] $D$ 与 $D^{-1}$ 不是严格互逆的
> - 先积后微：$\displaystyle D\!\left(D^{-1}f\right) = \frac{d}{dx}\!\int f(x)\,dx = f(x)$　✓ 完全还原
> - 先微后积：$\displaystyle D^{-1}\!\left(Df\right) = \int f'(x)\,dx = f(x)+C$　✗ 差一个常数 $C$
>
> 只有附加初始条件确定常数后才能严格还原。

### 二阶微分的理解（以 $y=x^3$ 为例）

- 一阶微分：$dy = 3x^2\,dx$
- 二阶微分（对一阶微分再取微分）：
  $$
  \begin{aligned}
  d^2y = d(dy) &= d(3x^2\cdot dx) \\
  &= d(3x^2)\cdot dx + 3x^2\cdot d(dx) \\
  &= 6x\,dx\cdot dx + 3x^2\cdot d^2x \\
  &= 6x\,dx^2 + 3x^2\,d^2x
  \end{aligned}
  $$

> [!note] 关于 $d^2x$ 的正确理解
> - 当 $x$ 是**自变量**时，$dx$ 是独立于 $x$ 的增量，$d(dx)=d^2x=0$（这是一个有意义的等式，**不是"无意义"**），此时 $d^2y=6x\,dx^2$。
> - 当 $x$ 不是自变量（例如参数方程 $x=x(t)$ 中 $t$ 才是自变量），$d^2x=x''(t)\,dt^2\neq 0$，上式 $d^2y=6x\,dx^2$ 不再成立。

### 易混记号辨析 ⚠️（高频考点）

| 记号 | 含义 | 注意 |
|:----:|:-----|:-----|
| $\left(\dfrac{dy}{dx}\right)^2 = (f')^2$ | 一阶导的平方 | **≠** $f''$；规范写法为 $\left(\dfrac{d(\,)}{dx}\right)^2$，不要写成 $\dfrac{d(\,)^2}{dx^2}$（易与二阶导混淆） |
| $\dfrac{d^2y}{dx^2} = f''$ | 二阶导 | 不是一阶导的平方 |
| $dx^2$ | $(dx)^2$，自变量微分的平方 | **≠** $d^2x$，**≠** $d(x^2)$ |
| $d^2x$ | $x$ 的二阶微分 | $x$ 为自变量时 $=0$；参数方程中 $\neq 0$ |
| $d(x^2)$ | 对 $x^2$ 取微分 | $d(x^2)=2x\,dx$ |

---

## 1.6 反函数的求导（核心考点）

### 一阶导数公式

> [!important] 反函数导数定理
> 设 $y=f(x)$ 在区间 $I$ 上**严格单调、可导**，且 $f'(x)\neq 0$，则其反函数 $x=\varphi(y)$ 在对应区间上可导，且：
> $$\boxed{\;\varphi'(y) = \frac{dx}{dy} = \frac{1}{\dfrac{dy}{dx}} = \frac{1}{f'(x)}\;}$$

**推导**：从微商视角看，导数就是微分之商，$dx/dy$ 与 $dy/dx$ 互为倒数。

> [!tip] 几何意义
> 原函数切线斜率 $f'(x)$ 与反函数切线斜率 $\varphi'(y)$ 互为倒数（关于 $y=x$ 对称的两条直线斜率互为倒数）。

> [!warning] 使用时注意变量对应
> $\varphi'(y)$ 是对 $y$ 求导，右边 $f'(x)$ 是对 $x$ 求导，$x$ 与 $y$ 必须通过 $y=f(x)$ 关联！
> 例如：$f(2)=4$，$f'(2)=3$，则 $\varphi'(4)=1/f'(2)=1/3$——代入的是 $y=4$（反函数自变量），不是 $x=2$。

### 二阶导数公式

在相同条件下，对一阶导公式再关于 $y$ 求导（**链式法则是关键**）：

$$
\begin{aligned}
\varphi''(y) &= \frac{d}{dy}\left(\frac{dx}{dy}\right) = \frac{d}{dy}\left(\frac{1}{f'(x)}\right) \\
&= \frac{d}{dx}\left(\frac{1}{f'(x)}\right)\cdot \frac{dx}{dy} \quad\text{（链式法则！先对 $x$ 求导，再乘 $dx/dy$）}\\
&= -\frac{f''(x)}{\left[f'(x)\right]^2}\cdot \frac{1}{f'(x)} \\
&= \boxed{\;-\frac{f''(x)}{\left[f'(x)\right]^3}\;}
\end{aligned}
$$

**对称公式**（互换 $f$ 与 $\varphi$）：
$$f''(x) = -\frac{\varphi''(y)}{\left[\varphi'(y)\right]^3}$$

> [!tip] 记忆口诀
> - 公式带**负号**：反映原函数与反函数凹凸性反转（例如 $f$ 严格增且凸，则 $f^{-1}$ 严格增且凹）。
> - 分母是 $f'(x)$ 的**三次方**，不是平方！
> - 链式法则那步乘 $\frac{dx}{dy}=\frac{1}{f'(x)}$ 是关键，千万别漏。

---

## 1.7 基本初等函数的反函数求导（必背公式）

反函数求导最直接的应用——推导对数函数、反三角函数的导数公式。

> [!note] 反三角函数的定义域与主值区间（必背）
> | 函数 | 定义域 | 主值区间 | 单调性 | 奇偶性 |
> |:----:|:------:|:--------:|:------:|:------:|
> | $\arcsin x$ | $[-1,1]$ | $\left[-\dfrac{\pi}{2},\dfrac{\pi}{2}\right]$ | 严格递增 | 奇函数 |
> | $\arccos x$ | $[-1,1]$ | $[0,\pi]$ | 严格递减 | 非奇非偶 |
> | $\arctan x$ | $(-\infty,+\infty)$ | $\left(-\dfrac{\pi}{2},\dfrac{\pi}{2}\right)$ | 严格递增 | 奇函数 |
> | $\operatorname{arccot} x$ | $(-\infty,+\infty)$ | $(0,\pi)$ | 严格递减 | 非奇非偶 |

--- start-multi-column: inverse-derivs
```column-settings
number of columns: 2
largest column: left
border: off
```

### （1）对数函数（指数函数的反函数）

$y=e^x$ 的反函数为 $x=\ln y$，$f'(x)=e^x=y$，故
$$\boxed{\;(\ln x)' = \frac{1}{x}\;}$$
一般情形 $(a^x)'=a^x\ln a$，其反函数 $x=\log_a y$：
$$\boxed{\;(\log_a x)' = \frac{1}{x\ln a}\;}$$

### （2）反正弦函数

$y=\sin x\ \left(x\in\left[-\frac{\pi}{2},\frac{\pi}{2}\right]\right)$，反函数 $x=\arcsin y$。
$f'(x)=\cos x = \sqrt{1-\sin^2 x}=\sqrt{1-y^2}$（$x\in[-\pi/2,\pi/2]$ 时 $\cos x\geq 0$），故
$$\boxed{\;(\arcsin x)' = \frac{1}{\sqrt{1-x^2}}\;}$$

### （3）反余弦函数

$y=\cos x\ (x\in[0,\pi])$，反函数 $x=\arccos y$。
$f'(x)=-\sin x=-\sqrt{1-y^2}$（$x\in[0,\pi]$ 时 $\sin x\geq 0$），故
$$\boxed{\;(\arccos x)' = -\frac{1}{\sqrt{1-x^2}}\;}$$

--- end-column ---

### （4）反正切函数

$y=\tan x\ \left(x\in\left(-\frac{\pi}{2},\frac{\pi}{2}\right)\right)$，反函数 $x=\arctan y$。
$f'(x)=\sec^2 x = 1+\tan^2 x = 1+y^2$，故
$$\boxed{\;(\arctan x)' = \frac{1}{1+x^2}\;}$$

### （5）反余切函数

$$\boxed{\;(\operatorname{arccot} x)' = -\frac{1}{1+x^2}\;}$$

> [!tip] 反三角函数导数口诀
> - "正"字头（$\arcsin,\arctan$）导数无负号；"余"字头（$\arccos,\operatorname{arccot}$）导数有负号。
> - $\arcsin/\arccos$ 分母带根号 $\sqrt{1-x^2}$，$\arctan/\operatorname{arccot}$ 分母为 $1+x^2$（无根号）。

--- end-multi-column

---

## 1.8 反函数典型例题

### 【例1】反函数二阶导（教材例4.7）

> 当 $x>0$ 时，$y=f(x)=3x^2+e^x$ 有反函数 $x=\varphi(y)$，求 $\varphi''(3+e)$。

**解**：
1. $f'(x)=6x+e^x$，$f''(x)=6+e^x$。
2. 解方程 $3x^2+e^x=3+e$：因 $x>0$ 时 $f'(x)=6x+e^x>0$，$f$ 严格递增，故有唯一解 $x=1$。
3. 代入二阶导公式：
$$\varphi''(3+e)=-\frac{f''(1)}{\left[f'(1)\right]^3}=-\frac{6+e}{(6+e)^3}=\boxed{-\frac{1}{(6+e)^2}}$$

### 【例2】反函数一阶导（变量对应考点）

> 设 $y=f(x)$ 的反函数为 $x=\varphi(y)$，已知 $f(2)=4$，$f'(2)=3$，求 $\varphi'(4)$。

**解**：$y=4$ 对应 $x=2$，故
$$\varphi'(4)=\frac{1}{f'(2)}=\boxed{\frac{1}{3}}$$
⚠️ 注意代入的是 $y=4$（反函数自变量），不是 $x=2$。

### 【例3】反函数与复合函数结合

> 设 $y=f(x)$ 可导且 $f'(x)\neq 0$，$x=\varphi(y)$ 为反函数，求 $\dfrac{d}{dx}\varphi[f(x)]$ 和 $\dfrac{d}{dy}f[\varphi(y)]$。

**解**：由还原性质 $\varphi[f(x)]\equiv x$，$f[\varphi(y)]\equiv y$，故
$$\frac{d}{dx}\varphi[f(x)]=1,\qquad \frac{d}{dy}f[\varphi(y)]=1$$

### 【例4】反函数在某点的切线方程

> 设 $y=f(x)=x^3+3x+1$，求其反函数 $x=\varphi(y)$ 在 $y=5$ 处的切线方程（写成 $y=f^{-1}(x)$ 的形式）。

**解**：
1. $f(1)=1+3+1=5$，故对应点 $x=1$。
2. $f'(x)=3x^2+3$，$f'(1)=6$，故 $\varphi'(5)=1/6$。
3. 反函数 $y=f^{-1}(x)$ 过点 $(5,1)$，切线斜率 $1/6$，切线方程：
$$y-1=\frac{1}{6}(x-5)\quad\Longleftrightarrow\quad \boxed{y=\frac{1}{6}x+\frac{1}{6}}$$

---

# 二、隐函数

## 2.1 显函数与隐函数

- **显函数**：$y=f(x)$，直接写出因变量 $y$ 关于自变量 $x$ 的表达式（对应关系 $f$ 一目了然）。
- **隐函数**：由方程 $F(x,y)=0$ 所确定的函数 $y=y(x)$。对应关系 $f$ 隐藏在方程中，不一定能（或没必要）解出 $y=f(x)$ 的显式表达式。

> [!important] 隐函数定义
> 设 $F(x,y)$ 在某区域上有定义，若对区间 $I$ 内的每个 $x$，都存在**唯一**的 $y$ 满足 $F(x,y)=0$，则称 $F(x,y)=0$ 在区间 $I$ 上确定了一个隐函数 $y=y(x)$。
>
> 所谓"隐"，就是"隐藏了 $f(\,)$ 具体对应关系"。

**显化/隐化示例**：

| 显函数 | 隐函数形式 |
|:------|:----------|
| $y=6x$ | $\dfrac{y}{6}-x=0$ |
| $y=\sqrt{1-x^2}$ | $x^2+y^2-1=0$（⚠️ 整个单位圆 $x^2+y^2=1$ 本身多值，需附加 $y\geq 0$ 才确定 $y=\sqrt{1-x^2}$；$y\leq 0$ 对应 $y=-\sqrt{1-x^2}$）|
| $y=kx+b$ | $ax+by+c=0$ |
| $y=x^x$（幂指函数） | $\ln y=x\ln x$（隐化处理，见对数求导法）|

> [!warning] 注意
> - 并非所有方程 $F(x,y)=0$ 都能确定隐函数（如 $x^2+y^2+1=0$ 无实解）。
> - 并非所有隐函数都能显化（如开普勒方程 $y-x-\varepsilon\sin y=0$），这正是隐函数求导法的价值——**不需要解出显式表达式也能求导**。

---

## 2.2 隐函数存在定理（了解）

> [!note] 一元隐函数存在定理
> 设 $F(x,y)$ 在点 $P_0(x_0,y_0)$ 的某邻域内具有**连续偏导数**（偏导数是多元微积分概念，此处只需知道这是一个光滑性条件），且
> $$F(x_0,y_0)=0,\qquad F_y(x_0,y_0)\neq 0$$
> 则方程 $F(x,y)=0$ 在点 $(x_0,y_0)$ 的某邻域内**唯一确定**一个具有连续导数的函数 $y=y(x)$，满足 $y_0=y(x_0)$，且
> $$\frac{dy}{dx} = -\frac{F_x}{F_y}$$
> 其中 $F_x=\dfrac{\partial F}{\partial x}$，$F_y=\dfrac{\partial F}{\partial y}$ 是 $F$ 分别对 $x$、$y$ 的偏导数。

> [!tip] 考点提醒
> - $F_y\neq 0$ 是隐函数存在且可导的关键条件（类比反函数求导中 $f'(x)\neq 0$）。
> - 公式中有**负号**：$y'=-F_x/F_y$，千万别丢！

---

## 2.3 隐函数求导方法（核心考点）

> [!important] 隐函数求导三步法
> 设 $y=y(x)$ 由 $F(x,y)=0$ 确定且可导：
> 1. **视 $y$ 为 $x$ 的函数**：将方程理解为 $F(x,y(x))\equiv 0$，$y$ 是中间变量，遇到含 $y$ 的项必须用链式法则。
> 2. **两边对 $x$ 求导**：逐次求导；凡遇到 $y$ 的函数（如 $y^3,e^y,\sin y,\ln y$），先对 $y$ 求导再乘 $y'$（链式法则）。
> 3. **解出 $y'$**：求导后得到关于 $y'$ 的一次方程，整理解出 $y'$，结果中**允许保留 $y$**。

**求二阶导 $y''$**：对一阶导得到的等式**两边再次对 $x$ 求导**，注意此时 $y$ 和 $y'$ 都是 $x$ 的函数，凡遇到 $y'$ 也要用链式法则乘 $y''$；最后将一阶已求得的 $y'$ 代入化简，并尽量利用原方程化简结果。

---

## 2.4 隐函数求导典型例题

### 【例1】基础一阶导+二阶导（原笔记例4）

> 设函数 $y=y(x)$ 由方程 $y^3+xy^2+x^2y+6=0$ 确定，且 $y'(1)=0$，求 $y''(1)$ 的值。

**解**：将 $y$ 看作关于 $x$ 的函数 $f(x)$，原方程写为：
$$f(x)^3 + x f(x)^2 + x^2 f(x) + 6 = 0$$
（注意：$f(x)^3$ 是复合函数，外层 $g(u)=u^3$，内层 $u=f(x)$。）

**第一步：求一阶导**
$$3f(x)^2 f'(x) + f(x)^2 + 2x f(x)f'(x) + 2x f(x) + x^2 f'(x) = 0$$
当 $x=1$ 时，由 $f'(1)=0$，代入得：
$$f(1)^2 + 2f(1) = 0 \implies f(1)=0 \text{ 或 } f(1)=-2$$
代入原方程检验：$f(1)=0$ 时左边 $=6\neq 0$，矛盾，舍去；故 $\boldsymbol{f(1)=-2}$。

**第二步：求二阶导**
对一阶导方程两边再对 $x$ 求导：
$$
\begin{aligned}
6f(x)[f'(x)]^2 + 3f(x)^2 f''(x) + 2f(x)f'(x) + 2\Big(f(x)f'(x)+x[f'(x)]^2+x f(x)f''(x)\Big)\\
+ 2f(x) + 2x f'(x) + 2x f'(x) + x^2 f''(x) = 0
\end{aligned}
$$

**第三步：代入求值**
将 $x=1$、$f(1)=-2$、$f'(1)=0$ 代入：
$$0 + 12f''(1) + 0 + 2\big(0+0-2f''(1)\big) -4 + 0 + 0 + f''(1) = 0$$
$$12f''(1)-4f''(1)-4+f''(1)=0 \implies 9f''(1)=4 \implies \boldsymbol{f''(1)=\dfrac{4}{9}}$$

---

### 【例2】两种方法对比（直接求导 vs 隐函数定理）

> 求由方程 $e^y+xy-e=0$ 所确定的隐函数的导数 $y'$。

--- start-multi-column: example2-cols
```column-settings
number of columns: 2
largest column: left
border: off
```

**方法一：直接求导法**

两边对 $x$ 求导：
$$e^y\cdot y' + y + x\cdot y' = 0$$
解得：
$$y' = -\frac{y}{x+e^y}\quad (x+e^y\neq 0)$$

--- end-column ---

**方法二：隐函数定理公式**

令 $F(x,y)=e^y+xy-e$，则
$F_x=y$，$F_y=e^y+x$，故
$$y'=-\frac{F_x}{F_y}=-\frac{y}{x+e^y}$$

结果一致 ✓

--- end-multi-column

> [!tip] 验证
> $x=0$ 时，由原方程 $e^y=e$ 得 $y=1$，故 $y'(0)=-1/(0+e)=-1/e$。

---

### 【例3】隐函数二阶导（含化简技巧）

> 设方程 $x^2+y^2=1$ 确定 $y=y(x)$（$y>0$），求 $y''$。

**解**：
一阶导：$2x+2yy'=0 \implies y'=-\dfrac{x}{y}$
二阶导（对 $y'=-x/y$ 用商的求导法则）：
$$y'' = -\frac{1\cdot y - x\cdot y'}{y^2} = -\frac{y - x\cdot\left(-\frac{x}{y}\right)}{y^2} = -\frac{y^2+x^2}{y^3} = \boxed{-\frac{1}{y^3}}$$
（最后一步用原方程 $x^2+y^2=1$ 化简，非常关键！）

---

## 2.5 对数求导法（隐函数思想的应用）⭐

> [!important] 适用场景
> 1. **幂指函数**：$y=u(x)^{v(x)}$（底数和指数都含 $x$）；
> 2. **连乘/连除/开方**：多个因式乘除、乘方开方的复杂函数。

**方法**：对 $y=f(x)$ 两边**取自然对数**，利用对数性质 $\ln(ab)=\ln a+\ln b$、$\ln(a/b)=\ln a-\ln b$、$\ln a^b=b\ln a$ 将乘除化为加减、幂化为乘法，再用隐函数求导法两边对 $x$ 求导。

### 【例4】幂指函数求导

> 求 $y=x^{\sin x}\ (x>0)$ 的导数。

**解**：取对数：
$$\ln y = \sin x\cdot \ln x$$
两边对 $x$ 求导（左边 $\ln y$ 是 $y$ 的函数，需链式法则）：
$$\frac{1}{y}\cdot y' = \cos x\cdot \ln x + \sin x\cdot \frac{1}{x}$$
故
$$\boxed{y' = x^{\sin x}\left(\cos x\ln x + \frac{\sin x}{x}\right)}$$

### 【例5】多因式连乘连除

> 求 $y=\sqrt{\dfrac{(x-1)(x-2)}{(x-3)(x-4)}}\ (x>4)$ 的导数。

**解**：取对数：
$$\ln y = \frac{1}{2}\big[\ln(x-1)+\ln(x-2)-\ln(x-3)-\ln(x-4)\big]$$
对 $x$ 求导：
$$\frac{y'}{y} = \frac{1}{2}\left(\frac{1}{x-1}+\frac{1}{x-2}-\frac{1}{x-3}-\frac{1}{x-4}\right)$$
故
$$\boxed{y' = \frac{1}{2}\sqrt{\frac{(x-1)(x-2)}{(x-3)(x-4)}}\left(\frac{1}{x-1}+\frac{1}{x-2}-\frac{1}{x-3}-\frac{1}{x-4}\right)}$$

> [!tip] 幂指函数通用公式
> 对 $y=u^v$（$u>0$），由对数求导可推得：
> $$(u^v)' = u^v\left(v'\ln u + \frac{v}{u}u'\right)$$
> 记忆：幂指函数导数 = 当作幂函数求导 + 当作指数函数求导（两项之和）：
> $$(u^v)' = v\,u^{v-1}\cdot u' + u^v\ln u\cdot v'$$

---

## 2.6 由参数方程确定的函数的求导（相关考点）

参数方程形式：
$$\begin{cases}x=\varphi(t)\\y=\psi(t)\end{cases}$$
若 $x=\varphi(t)$ 有反函数 $t=\varphi^{-1}(x)$，则 $y$ 通过 $t$ 成为 $x$ 的复合函数：$y=\psi[\varphi^{-1}(x)]$。

### 一阶导公式（链式法则 + 反函数求导）
$$\boxed{\;\frac{dy}{dx} = \frac{dy/dt}{dx/dt} = \frac{\psi'(t)}{\varphi'(t)}\quad(\varphi'(t)\neq 0)\;}$$

**推导思路**：$y$ 通过 $t$ 成为 $x$ 的复合函数 $y=\psi[\varphi^{-1}(x)]$，由链式法则和反函数求导：
$$\frac{dy}{dx} = \frac{dy}{dt}\cdot\frac{dt}{dx} = \frac{dy}{dt}\cdot\frac{1}{\frac{dx}{dt}} = \frac{\psi'(t)}{\varphi'(t)}$$

### 二阶导公式（⚠️ 高频易错）

对 $dy/dx$ 再关于 $x$ 求导，注意 $t$ 是中间变量，必须用链式法则再乘 $dt/dx$：

$$
\begin{aligned}
\frac{d^2y}{dx^2} &= \frac{d}{dx}\left(\frac{dy}{dx}\right) = \frac{d}{dt}\left(\frac{\psi'(t)}{\varphi'(t)}\right)\cdot\frac{dt}{dx} \\
&= \frac{\psi''(t)\varphi'(t)-\psi'(t)\varphi''(t)}{\left[\varphi'(t)\right]^2}\cdot\frac{1}{\varphi'(t)} \\
&= \boxed{\;\frac{d^2y}{dx^2} = \frac{\psi''(t)\varphi'(t)-\psi'(t)\varphi''(t)}{\left[\varphi'(t)\right]^3}\;}
\end{aligned}
$$

> [!danger] 高频错误（千万不要犯！）
> 1. 二阶导 **不是** $\dfrac{\psi''(t)}{\varphi''(t)}$ —— 这是没有依据的。
> 2. 二阶导 **不是** 对 $t$ 求完 $\dfrac{d}{dt}\!\left(\dfrac{\psi'}{\varphi'}\right)$ 就结束了，**必须**再乘 $\dfrac{dt}{dx}=\dfrac{1}{\varphi'(t)}$。
> 3. 分母是 $\left[\varphi'(t)\right]^3$（三次方），和反函数二阶导公式的分母三次方规律一致。

### 【例6】椭圆参数方程求导

> 设 $\begin{cases}x=a\cos t\\y=b\sin t\end{cases}$，求 $\dfrac{dy}{dx}$ 和 $\dfrac{d^2y}{dx^2}$。

**解**：
$x'_t=-a\sin t$，$y'_t=b\cos t$，$x''_t=-a\cos t$，$y''_t=-b\sin t$。

一阶导：
$$\frac{dy}{dx} = \frac{y'_t}{x'_t} = \frac{b\cos t}{-a\sin t} = \boxed{-\frac{b}{a}\cot t}$$

二阶导：
$$
\begin{aligned}
\frac{d^2y}{dx^2} &= \frac{y''_t x'_t - y'_t x''_t}{(x'_t)^3} \\
&= \frac{(-b\sin t)(-a\sin t)-(b\cos t)(-a\cos t)}{(-a\sin t)^3} \\
&= \frac{ab(\sin^2 t+\cos^2 t)}{-a^3\sin^3 t} = \boxed{-\frac{b}{a^2\sin^3 t}}
\end{aligned}
$$

### 【例7】参数方程求切线方程（真题类型）

> 设曲线由参数方程 $\begin{cases}x=\sin t\\y=\cos 2t\end{cases}$ 确定，求 $t=\dfrac{\pi}{4}$ 对应点处的切线方程。

**解**：
$t=\dfrac{\pi}{4}$ 时，$x=\sin\dfrac{\pi}{4}=\dfrac{\sqrt{2}}{2}$，$y=\cos\dfrac{\pi}{2}=0$，对应点 $\left(\dfrac{\sqrt{2}}{2},0\right)$。
$x'_t=\cos t$，$y'_t=-2\sin 2t$，故
$$\frac{dy}{dx}\bigg|_{t=\pi/4} = \frac{-2\sin(\pi/2)}{\cos(\pi/4)} = \frac{-2}{\sqrt{2}/2} = -2\sqrt{2}$$
切线方程：
$$y-0=-2\sqrt{2}\!\left(x-\frac{\sqrt{2}}{2}\right)\quad\Longleftrightarrow\quad \boxed{y=-2\sqrt{2}\,x+2}$$

---

# 三、公式速查表 & 易错点总结

## 3.1 反函数核心公式速查

| 公式 | 说明 |
|:-----|:-----|
| $f^{-1}[f(x)]=x,\quad f[f^{-1}(y)]=y$ | 复合还原性质 |
| 连续函数 $f$ 有反函数 $\iff$ $f$ **严格**单调 | 存在条件（注意"严格"）|
| $f$ 严格单调可导且 $f'(x)\neq 0$ $\Rightarrow$ $f^{-1}$ 可导 | 可导条件（$f'\neq 0$ 不是存在条件）|
| $\varphi'(y)=\dfrac{1}{f'(x)}$ | 一阶导（互为倒数，变量对应）|
| $\varphi''(y)=-\dfrac{f''(x)}{\left[f'(x)\right]^3}$ | 二阶导（负号 + 三次方）|
| $(\ln x)'=\dfrac{1}{x}$ | 对数函数（$e^x$ 的反函数）|
| $(\log_a x)'=\dfrac{1}{x\ln a}$ | 一般对数 |
| $(\arcsin x)'=\dfrac{1}{\sqrt{1-x^2}}$ | 反正弦 |
| $(\arccos x)'=-\dfrac{1}{\sqrt{1-x^2}}$ | 反余弦（负号）|
| $(\arctan x)'=\dfrac{1}{1+x^2}$ | 反正切 |
| $(\operatorname{arccot}x)'=-\dfrac{1}{1+x^2}$ | 反余切（负号）|

## 3.2 隐函数 & 参数方程核心公式速查

| 公式/方法 | 说明 |
|:----------|:-----|
| $F(x,y)=0\Rightarrow y=y(x)$ | 隐函数定义（一个 $x$ 对应唯一 $y$）|
| $y'=-\dfrac{F_x}{F_y}$ | 隐函数定理公式（注意**负号**）|
| 隐函数求导三步法 | 视 $y$ 为 $x$ 的函数 → 两边求导 → 解出 $y'$ |
| 对数求导法 | 适用：幂指函数 $u^v$、连乘连除开方 |
| $(u^v)'=u^v\left(v'\ln u+\dfrac{v}{u}u'\right)$ | 幂指函数导数（两项之和）|
| $\dfrac{dy}{dx}=\dfrac{y'_t}{x'_t}$ | 参数方程一阶导 |
| $\dfrac{d^2y}{dx^2}=\dfrac{y''_t x'_t - y'_t x''_t}{(x'_t)^3}$ | 参数方程二阶导（分母三次方，记得乘 $1/x'_t$）|

---

## 3.3 易错点汇总（考前必看）

> [!danger] 反函数部分易错点
> 1. ❌ "单调函数有反函数" → ✅ 必须是**严格**单调（常函数单调但无反函数）。
> 2. ❌ "$f'(x)\neq 0$ 才有反函数" → ✅ $f'(x)\neq 0$ 是反函数**可导**的条件，不是存在条件（反例 $y=x^3$）。
> 3. ❌ $f^{-1}(x) = \dfrac{1}{f(x)}$ → ✅ $f^{-1}$ 表示逆映射，**不是**倒数！$f^{-1}(x) \neq \dfrac{1}{f(x)}$。
> 4. ❌ $d^2x$ "无意义" → ✅ 当 $x$ 为自变量时 $d^2x=0$（有意义的等式）；参数方程中 $d^2x\neq 0$。
> 5. ❌ $(f')^2=f''$ → ✅ 一阶导的平方 ≠ 二阶导；$\dfrac{d(\,)^2}{dx^2}$ 是不规范写法，应为 $\left(\dfrac{d(\,)}{dx}\right)^2$。
> 6. ❌ 反函数二阶导分母写平方 → ✅ 分母是 $[f'(x)]^3$（三次方），且带负号。
> 7. ❌ $\varphi'(y_0)$ 时代入 $x$ 的值 → ✅ 必须先由 $y_0=f(x_0)$ 找到对应的 $x_0$，再代入 $1/f'(x_0)$。

> [!danger] 隐函数部分易错点
> 8. ❌ 对 $y^3$ 关于 $x$ 求导得 $3y^2$ → ✅ 应得 $3y^2 y'$（链式法则，$y$ 是 $x$ 的函数！）。
> 9. ❌ 隐函数定理公式忘记负号 → ✅ $y'=-F_x/F_y$，负号别丢！
> 10. ❌ 求二阶导时代完值才想起 $y'$ 也是 $x$ 的函数 → ✅ 对含 $y'$ 的项求导会出现 $y''$。
> 11. ❌ 单位圆 $x^2+y^2=1$ 整体视为一个隐函数 → ✅ 需附加 $y\geq 0$ 或 $y\leq 0$ 才确定唯一函数。
> 12. ❌ "结果里怎么还有 $y$，是不是算错了？" → ✅ 隐函数求导结果中保留 $y$ 是**正常现象**，不需要（也往往不能）全部换成 $x$。
> 13. ❌ 对数求导后忘记把结果乘回 $y$ → ✅ 得到 $y'/y=\cdots$ 后，$y'=y\cdot(\cdots)$。

> [!danger] 参数方程部分易错点
> 14. ❌ 二阶导直接用 $y''_t/x''_t$ → ✅ 必须用公式 $\dfrac{y''_t x'_t - y'_t x''_t}{(x'_t)^3}$。
> 15. ❌ 对 $t$ 求导后忘了乘 $dt/dx=1/x'_t$ → ✅ 这是最常见的丢分原因。
> 16. ❌ 分母写成二次方 → ✅ 分母是三次方 $(x'_t)^3$。

---

## 3.4 章节关系图

```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[row sep=2.2em, column sep=2.0em]
& \text{一元函数求导} \arrow[ld] \arrow[d] \arrow[rd] & \\
\text{显函数求导（已学）} & \text{反函数求导} \arrow[d] & \text{隐函数求导} \arrow[ld] \arrow[rd] \\
& \begin{matrix}
\varphi'(y)=\dfrac{1}{f'(x)}\\[6pt]
\varphi''(y)=-\dfrac{f''(x)}{[f'(x)]^3}
\end{matrix} & \text{对数求导法} & \text{参数方程求导} \arrow[d] \\
& & & \begin{matrix}
y'_x=\dfrac{y'_t}{x'_t}\\[6pt]
y''_x=\dfrac{y''_t x'_t-y'_t x''_t}{(x'_t)^3}
\end{matrix}
\end{tikzcd}
\end{document}
```

> [!success] 学习建议
> - **会推导**比**死记硬背**更重要——反函数二阶导、参数方程二阶导都应能独立推出。
> - **变量关系**是核心：反函数求导注意 $x,y$ 对应关系；隐函数/参数方程求导时刻牢记"谁是谁的函数"，不滥用链式法则就不会错。
> - **做完检验**：求完导后代入原方程验证（如例4中舍去 $f(1)=0$），是避免计算错误的好习惯。