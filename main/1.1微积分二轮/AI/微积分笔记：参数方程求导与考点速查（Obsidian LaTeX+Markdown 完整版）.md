---
tags:
  - 微积分
  - 一元函数微分学
  - 参数方程
  - 反函数
  - 隐函数
  - 考点总结
---

# 参数方程求导与考点速查

> [!tip] 章节导航
> 本文是「反函数与隐函数求导」系列第 3 篇。
> - [[微积分笔记：反函数求导（Obsidian LaTeX+Markdown 完整版）|第1篇：反函数]]
> - [[微积分笔记：隐函数与对数求导法（Obsidian LaTeX+Markdown 完整版）|第2篇：隐函数与对数求导法]]
> - [[微积分笔记：参数方程求导与考点速查（Obsidian LaTeX+Markdown 完整版）|第3篇：参数方程、速查表、易错总结]]

---

## 1. 参数方程确定的函数

设曲线由参数方程
$$
\begin{cases}
x=\varphi(t),\\
y=\psi(t)
\end{cases}
$$
给出。若 $x=\varphi(t)$ 有反函数 $t=\varphi^{-1}(x)$，则
$$y=\psi\big(\varphi^{-1}(x)\big),$$
即 $y$ 通过参数 $t$ 成为 $x$ 的函数。

因此，参数方程求导本质上是：
- 复合函数求导；
- 反函数求导。

---

## 2. 参数方程一阶导数

若 $\varphi'(t)\neq0$，则
$$
\boxed{\frac{dy}{dx}=\frac{dy/dt}{dx/dt}=\frac{\psi'(t)}{\varphi'(t)}}.
$$

推导：
$$\frac{dy}{dx}=\frac{dy}{dt}\cdot\frac{dt}{dx}
=\frac{dy}{dt}\cdot\frac{1}{dx/dt}
=\frac{\psi'(t)}{\varphi'(t)}.$$

> [!warning] 一阶导注意
> 参数方程一阶导不是简单地把 $y$ 对 $x$ 直接求，而是两个对 $t$ 导数的商。

---

## 3. 参数方程二阶导数

二阶导是高频易错点。设
$$\frac{dy}{dx}=\frac{\psi'(t)}{\varphi'(t)}.$$
要对 $x$ 求导，但表达式是关于 $t$ 的，因此必须再用链式法则乘 $\dfrac{dt}{dx}$：

$$
\begin{aligned}
\frac{d^2y}{dx^2}
&=\frac{d}{dx}\left(\frac{dy}{dx}\right)\\
&=\frac{d}{dt}\left(\frac{\psi'(t)}{\varphi'(t)}\right)\cdot\frac{dt}{dx}\\
&=\frac{\psi''(t)\varphi'(t)-\psi'(t)\varphi''(t)}{[\varphi'(t)]^2}\cdot\frac{1}{\varphi'(t)}\\
&=\boxed{\frac{\psi''(t)\varphi'(t)-\psi'(t)\varphi''(t)}{[\varphi'(t)]^3}}.
\end{aligned}
$$

也常记作：
$$\boxed{\frac{d^2y}{dx^2}=\frac{y_t''x_t'-y_t'x_t''}{(x_t')^3}}.$$

> [!danger] 三大高频错误
> 1. 错写成 $\dfrac{\psi''(t)}{\varphi''(t)}$；
> 2. 对 $t$ 求完商的导数后忘记乘 $\dfrac{dt}{dx}=\dfrac1{\varphi'(t)}$；
> 3. 分母写成平方而不是三次方。

---

## 4. 参数方程典型例题

### 例1：椭圆参数方程

设
$$
\begin{cases}
x=a\cos t,\\
y=b\sin t,
\end{cases}
$$
求 $\dfrac{dy}{dx}$ 和 $\dfrac{d^2y}{dx^2}$。

解：
$$x_t'=-a\sin t,\qquad y_t'=b\cos t,$$
$$x_t''=-a\cos t,\qquad y_t''=-b\sin t.$$

一阶导：
$$\frac{dy}{dx}=\frac{b\cos t}{-a\sin t}=\boxed{-\frac ba\cot t}.$$

二阶导：
$$
\begin{aligned}
\frac{d^2y}{dx^2}
&=\frac{(-b\sin t)(-a\sin t)-(b\cos t)(-a\cos t)}{(-a\sin t)^3}\\
&=\frac{ab(\sin^2t+\cos^2t)}{-a^3\sin^3t}\\
&=\boxed{-\frac{b}{a^2\sin^3t}}.
\end{aligned}
$$

---

### 例2：参数方程切线问题

设曲线由
$$
\begin{cases}
x=\sin t,\\
y=\cos 2t
\end{cases}
$$
确定，求 $t=\dfrac{\pi}{4}$ 对应点处的切线方程。

解：当 $t=\dfrac{\pi}{4}$ 时，
$$x=\sin\frac{\pi}{4}=\frac{\sqrt2}{2},$$
$$y=\cos\frac{\pi}{2}=0.$$
所以切点为
$$\left(\frac{\sqrt2}{2},0\right).$$

又
$$x_t'=\cos t,\qquad y_t'=-2\sin2t.$$
因此
$$
\frac{dy}{dx}\bigg|_{t=\pi/4}
=\frac{-2\sin(\pi/2)}{\cos(\pi/4)}
=\frac{-2}{\sqrt2/2}
=-2\sqrt2.
$$

切线方程为
$$y-0=-2\sqrt2\left(x-\frac{\sqrt2}{2}\right),$$
即
$$\boxed{y=-2\sqrt2x+2}.$$

---

## 5. 反函数核心公式速查

| 知识点 | 公式/结论 |
|---|---|
| 反函数定义 | $x=f^{-1}(y)\Longleftrightarrow y=f(x)$ |
| 复合还原 | $f^{-1}(f(x))=x,\ f(f^{-1}(y))=y$ |
| 连续函数有反函数 | 严格单调 |
| 反函数可导条件 | 严格单调、可导且 $f'(x)\neq0$ |
| 反函数一阶导 | $\varphi'(y)=\dfrac1{f'(x)}$ |
| 反函数二阶导 | $\varphi''(y)=-\dfrac{f''(x)}{[f'(x)]^3}$ |
| 对数函数导数 | $(\ln x)'=\dfrac1x$ |
| 一般对数导数 | $(\log_ax)'=\dfrac1{x\ln a}$ |
| 反正弦导数 | $(\arcsin x)'=\dfrac1{\sqrt{1-x^2}}$ |
| 反余弦导数 | $(\arccos x)'=-\dfrac1{\sqrt{1-x^2}}$ |
| 反正切导数 | $(\arctan x)'=\dfrac1{1+x^2}$ |
| 反余切导数 | $(\operatorname{arccot}x)'=-\dfrac1{1+x^2}$ |

---

## 6. 隐函数与参数方程速查

| 知识点 | 公式/方法 |
|---|---|
| 隐函数 | $F(x,y)=0$ 确定 $y=y(x)$ |
| 隐函数定理公式 | $y'=-\dfrac{F_x}{F_y}$ |
| 隐函数求导步骤 | 视 $y$ 为 $x$ 的函数 → 两边求导 → 解出 $y'$ |
| 幂指函数 | $(u^v)'=u^v\left(v'\ln u+\dfrac vu u'\right)$ |
| 参数方程一阶导 | $\dfrac{dy}{dx}=\dfrac{y_t'}{x_t'}$ |
| 参数方程二阶导 | $\dfrac{d^2y}{dx^2}=\dfrac{y_t''x_t'-y_t'x_t''}{(x_t')^3}$ |

---

## 7. 易错点总清单

> [!danger] 反函数部分
> 1. "单调函数有反函数"应改为"严格单调函数有反函数"。
> 2. $f'(x)\neq0$ 是可导条件，不是反函数存在条件。
> 3. $\varphi'(y_0)$ 要代入对应的 $y_0$，不是直接代入 $x$。
> 4. 反函数二阶导有负号，分母是三次方。
> 5. $dx^2=(dx)^2$，不是 $d^2x$。
> 6. $(f')^2\neq f''$。

> [!danger] 隐函数部分
> 1. 对含 $y$ 项求导必须乘 $y'$。
> 2. 公式 $y'=-F_x/F_y$ 不要漏负号。
> 3. 求二阶导时，$y'$ 仍然是 $x$ 的函数。
> 4. 多值方程不一定整体确定一个函数，要注意取值范围。
> 5. 对数求导后要乘回原函数 $y$。

> [!danger] 参数方程部分
> 1. 二阶导绝对不能写成 $y_t''/x_t''$。
> 2. 二阶导要乘 $dt/dx=1/x_t'$。
> 3. 分母是 $(x_t')^3$。
> 4. 求切线时要先求切点，再求斜率。

---

## 8. 章节关系图

```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[row sep=2.2em, column sep=1.8em]
& \text{一元函数求导} \arrow[ld] \arrow[d] \arrow[rd] & \\
\text{显函数求导} & \text{反函数求导} \arrow[d] \arrow[rdd, bend right=20] & \text{隐函数求导} \arrow[d] \\
& \varphi'(y)=\frac1{f'(x)} & \text{对数求导法} \\
& \varphi''(y)=-\frac{f''(x)}{[f'(x)]^3} & \text{参数方程求导} \arrow[d] \\
& & \frac{d^2y}{dx^2}=\frac{y_t''x_t'-y_t'x_t''}{(x_t')^3}
\end{tikzcd}
\end{document}
```

> [!tip] 图中箭头说明
> - 反函数求导向下推导出一阶导、二阶导公式；
> - 隐函数求导向下延伸出对数求导法；
> - 反函数求导向右下的弯箭头表示：参数方程求导本质上也依赖反函数求导（$t=\varphi^{-1}(x)$）。

---

## 9. Obsidian 使用说明

- 数学公式使用标准 LaTeX，Obsidian 原生支持。
- `> [!important]`、`> [!warning]`、`> [!danger]` 等使用 Obsidian Callouts。
- ```` ```tikz ```` 代码块需要安装并启用 **TikZJax** 插件后渲染。
- 多栏布局使用 **Multi-Column Markdown** 插件语法。
- 三篇笔记互相用 `[[ ]]` 链接，可直接点击跳转。
- 若不需要 TikZ 图，可删除对应代码块，不影响文字与公式内容。

---

## 10. 最终复习建议

1. 先掌握反函数一阶导、二阶导推导，而不是死记公式。
2. 做隐函数题时，每一步都问自己："这里谁是谁的函数？"
3. 参数方程二阶导一定要单独练熟，这是最容易丢分的点。
4. 对数求导法重点掌握幂指函数和复杂乘除式。
5. 做题后尽量代入原方程检验，避免舍根或计算错误。
