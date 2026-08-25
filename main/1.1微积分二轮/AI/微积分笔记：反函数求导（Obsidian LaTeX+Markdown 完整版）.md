---
tags:
  - 微积分
  - 一元函数微分学
  - 反函数
  - 导数
---

# 反函数求导

> [!tip] 章节导航
> 本文是「反函数与隐函数求导」系列第 1 篇。
> - [[微积分笔记：反函数求导（Obsidian LaTeX+Markdown 完整版）|第1篇：反函数]]
> - [[微积分笔记：隐函数与对数求导法（Obsidian LaTeX+Markdown 完整版）|第2篇：隐函数与对数求导法]]
> - [[微积分笔记：参数方程求导与考点速查（Obsidian LaTeX+Markdown 完整版）|第3篇：参数方程、速查表、易错总结]]

---

## 1. 反函数的定义

设函数
$$y=f(x),\qquad x\in D$$
的定义域为 $D$，值域为 $R_f=f(D)$。

> [!important] 反函数定义
> 如果对于每一个 $y\in R_f$，都存在**唯一**的 $x\in D$ 使得
> $$y=f(x),$$
> 则这个对应关系定义了一个新函数
> $$x=f^{-1}(y),$$
> 称为 $y=f(x)$ 的反函数。

直观上说，反函数就是让自变量和因变量"交换职位"：

```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[row sep=1.8em, column sep=2.5em]
x \arrow[rr, "f"] &  & y \arrow[ld, "f^{-1}"'] \\
 & x &
\end{tikzcd}
\end{document}
```

因此反函数满足：
$$f^{-1}\big(f(x)\big)=x\quad (x\in D),$$
$$f\big(f^{-1}(y)\big)=y\quad (y\in R_f).$$

若习惯上仍把自变量记作 $x$，可把反函数写成
$$y=f^{-1}(x).$$

> [!warning] 记号提醒
> $f^{-1}(x)$ 表示反函数，不是 $\dfrac1{f(x)}$。

---

## 2. 反函数存在的条件

> [!important] 一般结论
> 函数存在反函数，当且仅当它是**双射**（一一对应）：每个函数值只对应一个自变量。

> [!important] 连续函数常用判定
> 若 $f$ 在区间 $I$ 上连续，则 $f$ 在该区间上存在反函数，当且仅当 $f$ 在该区间上**严格单调**。

> [!danger] 高频误区
> 1. 必须说"**严格单调**"，不能只说"单调"。常函数 $y=C$ 单调，但没有反函数。
> 2. $f'(x)\neq 0$ 不是反函数存在的条件，而是反函数**可导**的条件。

反例：
$$f(x)=x^3.$$
它在 $\mathbb R$ 上严格递增，所以有反函数
$$f^{-1}(x)=\sqrt[3]{x}.$$
但
$$f'(x)=3x^2,\qquad f'(0)=0,$$
因此反函数在对应点处不可导，图像表现为垂直切线。

没有反函数的典型情况：
- 非一一对应：如 $y=x^2$ 在 $\mathbb R$ 上，一个 $y=4$ 对应 $x=\pm2$；
- 常函数：$y=C$，一个函数值对应所有 $x$。

但局部限制区间后可能有反函数，例如：
$$y=x^2,\quad x\in[0,+\infty)\Longrightarrow y=\sqrt{x};$$
$$y=x^2,\quad x\in(-\infty,0]\Longrightarrow y=-\sqrt{x}.$$

---

## 3. 反函数的几何意义

若把直接函数写成 $y=f(x)$，反函数写成 $y=f^{-1}(x)$，则两者图像关于直线
$$y=x$$
对称。

```tikz
\usepackage{tikz}
\begin{document}
\begin{tikzpicture}[scale=1.0, >=stealth, domain=0:2.2, samples=80]
  \draw[->] (-0.3,0) -- (2.6,0) node[right] {$x$};
  \draw[->] (0,-0.3) -- (0,2.6) node[above] {$y$};
  \draw[dashed, gray] (-0.3,-0.3) -- (2.6,2.6) node[midway, below right] {$y=x$};
  \draw[thick, red] plot (\x, {0.4*\x*\x+0.25}) node[above right, black] {$y=f(x)$};
  \draw[thick, blue] plot ({0.4*\x*\x+0.25}, \x) node[below right, black] {$y=f^{-1}(x)$};
\end{tikzpicture}
\end{document}
```

> [!note] 关键理解
> $x=f^{-1}(y)$ 与 $y=f(x)$ 在同一坐标系中是同一条曲线；只有写成 $y=f^{-1}(x)$ 后，才是关于 $y=x$ 对称的图像。

若原函数在点 $(a,b)$ 处切线斜率为 $f'(a)$，则反函数在对称点 $(b,a)$ 处切线斜率为
$$\frac{1}{f'(a)}.$$

---

## 4. 反函数的基本性质

| 性质 | 结论 |
|---|---|
| 定义域、值域互换 | $D_{f^{-1}}=R_f,\ R_{f^{-1}}=D_f$ |
| 单调性一致 | $f$ 严格增，则 $f^{-1}$ 严格增；$f$ 严格减，则 $f^{-1}$ 严格减 |
| 奇偶性 | 奇函数若有反函数，则反函数也是奇函数；偶函数通常没有反函数 |
| 复合还原 | $f^{-1}(f(x))=x,\ f(f^{-1}(y))=y$ |
| 反函数的反函数 | $(f^{-1})^{-1}=f$ |

多层可逆映射的复合也要注意反序：
$$(g\circ f)^{-1}=f^{-1}\circ g^{-1}.$$

---

## 5. 微分算子与易混记号

把求导看成作用在函数上的算子：
$$D(\;)=\frac{d(\;)}{dx}.$$

于是：
$$f\xrightarrow{D}f',$$
$$f'\xrightarrow{D}f'',$$
$$D^2(\;)=D\big(D(\;)\big)=\frac{d^2(\;)}{dx^2}.$$

逆微分算子对应积分：
$$D^{-1}(\;)=\int(\;)\,dx.$$

> [!warning] 微分与积分不是完全互逆
> $$D(D^{-1}f)=f,$$
> 但
> $$D^{-1}(Df)=f(x)+C.$$
> 先微后积会多出积分常数。

以 $y=x^3$ 为例：
$$dy=3x^2dx,$$
$$d^2y=d(dy)=6x\,dx^2+3x^2d^2x.$$
当 $x$ 是自变量时，$dx$ 与 $x$ 独立，所以 $d^2x=0$，从而
$$d^2y=6x\,dx^2.$$

> [!note] 关于 $d^2x$
> 当 $x$ 为自变量时 $d^2x=0$；但在参数方程中 $x=x(t)$，$t$ 才是自变量，此时 $d^2x=x''(t)dt^2$，并不为零。

---

## 6. 反函数一阶导数

> [!important] 反函数导数定理
> 设 $y=f(x)$ 在区间上严格单调、可导，并且 $f'(x)\neq0$，则其反函数 $x=\varphi(y)$ 可导，且
> $$\boxed{\varphi'(y)=\frac{dx}{dy}=\frac{1}{f'(x)}}.$$

从微商角度看：
$$\frac{dx}{dy}=\frac{1}{\frac{dy}{dx}}.$$

> [!warning] 变量对应是核心考点
> $\varphi'(y)$ 是对 $y$ 求导，右端 $f'(x)$ 是对 $x$ 求导，二者通过 $y=f(x)$ 联系。

例：若 $f(2)=4,\ f'(2)=3$，则
$$\varphi'(4)=\frac1{f'(2)}=\frac13.$$
注意代入反函数导数的自变量是 $y=4$，不是 $x=2$。

---

## 7. 反函数二阶导数

对
$$\varphi'(y)=\frac{1}{f'(x)}$$
再关于 $y$ 求导。由于右端是关于 $x$ 的表达式，而 $x$ 又是 $y$ 的函数，必须使用链式法则：

$$
\begin{aligned}
\varphi''(y)
&=\frac{d}{dy}\left(\frac1{f'(x)}\right)\\
&=\frac{d}{dx}\left(\frac1{f'(x)}\right)\cdot\frac{dx}{dy}\\
&=-\frac{f''(x)}{[f'(x)]^2}\cdot\frac1{f'(x)}\\
&=\boxed{-\frac{f''(x)}{[f'(x)]^3}}.
\end{aligned}
$$

对称地，
$$f''(x)=-\frac{\varphi''(y)}{[\varphi'(y)]^3}.$$

> [!danger] 二阶导公式易错点
> - 有**负号**；
> - 分母是 $[f'(x)]^3$，不是平方；
> - 链式法则中的 $\dfrac{dx}{dy}=\dfrac1{f'(x)}$ 不能漏。

---

## 8. 基本初等函数的反函数导数

### 8.1 对数函数

设 $y=e^x$，其反函数为 $x=\ln y$。因为
$$f'(x)=e^x=y,$$
所以
$$\boxed{(\ln x)'=\frac1x}.$$

一般地，由 $(a^x)'=a^x\ln a$，得
$$\boxed{(\log_a x)'=\frac1{x\ln a}}.$$

### 8.2 反正弦函数

设
$$y=\sin x,\qquad x\in\left[-\frac{\pi}{2},\frac{\pi}{2}\right],$$
其反函数为 $x=\arcsin y$。由于该区间内 $\cos x\ge0$，
$$f'(x)=\cos x=\sqrt{1-\sin^2x}=\sqrt{1-y^2}.$$
因此
$$\boxed{(\arcsin x)'=\frac1{\sqrt{1-x^2}}}.$$

### 8.3 反余弦函数

设
$$y=\cos x,\qquad x\in[0,\pi],$$
其反函数为 $x=\arccos y$。由于该区间内 $\sin x\ge0$，
$$f'(x)=-\sin x=-\sqrt{1-y^2}.$$
因此
$$\boxed{(\arccos x)'=-\frac1{\sqrt{1-x^2}}}.$$

### 8.4 反正切函数

设
$$y=\tan x,\qquad x\in\left(-\frac{\pi}{2},\frac{\pi}{2}\right),$$
其反函数为 $x=\arctan y$。因为
$$f'(x)=\sec^2x=1+\tan^2x=1+y^2,$$
所以
$$\boxed{(\arctan x)'=\frac1{1+x^2}}.$$

### 8.5 反余切函数

$$\boxed{(\operatorname{arccot}x)'=-\frac1{1+x^2}}.$$

> [!tip] 反三角函数导数口诀
> - "正"字头：$\arcsin,\arctan$，导数无负号；
> - "余"字头：$\arccos,\operatorname{arccot}$，导数有负号；
> - $\arcsin,\arccos$ 分母带根号；
> - $\arctan,\operatorname{arccot}$ 分母为 $1+x^2$。

---

## 9. 典型例题

--- start-multi-column: inverse-examples
```column-settings
Number of Columns: 2
Largest Column: left
```

### 例1：反函数二阶导

当 $x>0$ 时，设
$$y=f(x)=3x^2+e^x$$
有反函数 $x=\varphi(y)$，求 $\varphi''(3+e)$。

解：
$$f'(x)=6x+e^x,\qquad f''(x)=6+e^x.$$
当 $x>0$ 时，$f'(x)>0$，所以 $f$ 严格递增。由
$$3x^2+e^x=3+e$$
得 $x=1$。因此
$$
\begin{aligned}
\varphi''(3+e)
&=-\frac{f''(1)}{[f'(1)]^3}\\
&=-\frac{6+e}{(6+e)^3}\\
&=\boxed{-\frac1{(6+e)^2}}.
\end{aligned}
$$

--- end-column ---

### 例2：反函数一阶导

设 $y=f(x)$ 的反函数为 $x=\varphi(y)$，且
$$f(2)=4,\qquad f'(2)=3.$$
求 $\varphi'(4)$。

解：$y=4$ 对应 $x=2$，所以
$$\varphi'(4)=\frac1{f'(2)}=\boxed{\frac13}.$$

### 例3：反函数与复合函数

设 $y=f(x)$ 可导且 $f'(x)\neq0$，反函数为 $x=\varphi(y)$，求
$$\frac{d}{dx}\varphi[f(x)],\qquad \frac{d}{dy}f[\varphi(y)].$$

解：由反函数性质，
$$\varphi[f(x)]=x,\qquad f[\varphi(y)]=y,$$
所以
$$\frac{d}{dx}\varphi[f(x)]=1,\qquad \frac{d}{dy}f[\varphi(y)]=1.$$

--- end-multi-column

---

## 10. 本篇小结

- 反函数存在的关键是一一对应；连续函数情形下常用"严格单调"判断。
- $f'(x)\neq0$ 是反函数可导条件，不是反函数存在条件。
- 反函数图像与原函数关于 $y=x$ 对称。
- 反函数一阶导：
  $$\varphi'(y)=\frac1{f'(x)}.$$
- 反函数二阶导：
  $$\varphi''(y)=-\frac{f''(x)}{[f'(x)]^3}.$$
- 反三角函数导数必须熟记，尤其注意正负号和根号。

下一篇：[[微积分笔记：隐函数与对数求导法（Obsidian LaTeX+Markdown 完整版）|隐函数与对数求导法]]。
