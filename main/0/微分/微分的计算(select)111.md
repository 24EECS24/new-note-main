---
title: "微分的计算真题归纳（2016—2026）"
aliases: ["微分的计算真题归纳", "微分的计算专题", "十一年真题微分的计算专题"]
tags:
  - 专升本/高等数学
  - 专题归纳/微分的计算
type: 专题归纳
---

# 十一年真题 · 微分的计算专题（2016—2026）

> 本文档以《5.微分的计算》（含速查版）界定的知识边界为**唯一准绳**，并参照《6.微分的应用》《12.变限积分求导》等相邻文件划定界限，从河南专升本《高等数学》2016—2026 共 11 套真题中，**逐年、逐题通读全卷（每卷 53 题，非正则筛选、非脚本、非子智能体），逐题理解后筛选并逐字核对**，只保留"动手求一个函数的导数/微分/高阶导/偏导/全微分"的运算题，共收录 **76 道**。
>
> **知识边界（两大板块）**：
> **一、一元微分计算**——基本求导公式（幂/指数/对数/三角/反三角/反双曲）；四则运算（和差/积/商的求导与微分）；复合函数求导与微分形式不变性；分段函数、含绝对值函数求导；反函数求导；隐函数求导；参数方程求导；对数求导法；幂指函数求导；高阶导数（归纳法、莱布尼茨公式、排列组合法）；泰勒展开式及唯一性。
> **二、二元微分学计算**——二元复合函数求导（偏导、全导、微分形式不变性、位置标记 $f_1'$、$f_2'$ 与复合结构）；二元隐函数求导（一元隐函数定理、二元隐函数定理，公式 $\dfrac{\partial z}{\partial x}=-\dfrac{F_x}{F_z}$ 等）。
>
> **收录口径（严格对齐文件）**：凡让你动手"求"一个函数的导数/微分/高阶导/偏导/全微分的运算题——含基本求导、四则与乘积/商求导、复合函数链式求导、求 $dy/df$（结果带 $dx$）、高阶导与高阶偏导、参数方程求导、隐函数求导（含求 $dz$）、幂指函数与对数求导法、多元复合链式偏导、微分的线性近似，以及"已知原函数（不定积分）求 $f(x)$"这类先积后导题，一律归入本专题。
>
> **不收录（相邻专题边界）**：
> ① 极值、单调性、凹凸、拐点、渐近线、最值/取值范围、函数图像及实际优化应用题 → 《6.微分的应用》；
> ② 变限积分求导（如 2022-16、2021-34）→ 《12.变限积分求导》；
> ③ 方向导数/梯度（含需梯度合成的方向导数）、切平面/法平面/空间曲线切线（空间几何）、微分方程、积分计算、中值定理与证明题，均不收；
> ④ 试卷明确归为"应用题"的 51、52 题不收录。
>
> **与导数专题的关系**：导数专题（34 道）只收"概念/定义/几何意义/可导性判断/关系"类；本专题收其全部"求导运算"。原《导数专题移出微分题号清单》的 44 道运算题已全部包含在本专题 76 道内；参数方程、隐函数、求 $dz$ 等本专题新增题不在 44 清单内，属正常，故本专题题量大于 44。
>
> **质检说明**：题面、选项、答案、解析均从对应年份题答源逐字照录；源文件内"答案存疑/机构分歧"标注一并保留；发现源文件笔误处加【订正】框说明。全部答案另经符号计算独立复算核对。格式：一个试卷=一级标题；一个题=二级标题；题号按真题原题号；按 2026→2016 倒序排列。返回 MOC：[[🏠首页-十年真题MOC]]。

---

## 各年题量矩阵

| 年份 | 收录题号 | 年合计 |
|---|---|---|
| 2026 | 7、8、31、36、43、48 | **6** |
| 2025 | 7、9、22、31、36、43、48 | **7** |
| 2024 | 7、9、31、37、43、48 | **6** |
| 2023 | 7、11、28、29、36、43、48 | **7** |
| 2022 | 6、9、20、29、37、42 | **6** |
| 2021 | 7、8、21、31、37、43、48 | **7** |
| 2020 | 11、15、19、24、34、38、42、48 | **8** |
| 2019 | 12、23、29、38、40、43 | **6** |
| 2018 | 8、9、34、42、50 | **5** |
| 2017 | 3、4、10、24、27、33、34、38、41、47、48、49 | **12** |
| 2016 | 9、24、34、37、42、46 | **6** |
| **合计** | — | **76** |

---

# 2026年河南专升本《高等数学》真题·微分的计算专题

> 本卷命中 6 道（第 7、8、31、36、43、48 题）。

## 第7题

xxxx

**题目**

设函数 $y=f^2(\cos x)$，其中 $f$ 可导，则 $y'=$（　　）

- A. $2f(\cos x)$
- B. $2f(\cos x)f'(\cos x)$
- C. $-2\sin x f(\cos x)f'(\cos x)$
- D. $2\sin x f(\cos x)f'(\cos x)$

````````col
```````col-md
flexGrow=20
===

**答案**：C

**解析**

> 由复合函数链式求导法则，外层为平方、中层为 $f$、内层为 $\cos x$：
>
> $$y'=2f(\cos x)\cdot f'(\cos x)\cdot(\cos x)'=-2\sin x\,f(\cos x)f'(\cos x)$$
>
> 选 C。

**考点**：复合函数链式求导（多层复合）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第8题

xxxx

**题目**

设参数方程 $\begin{cases}x=e^{-t}+\cos t\\ y=e^t+\sin t\end{cases}$，则 $\dfrac{dy}{dx}\bigg|_{t=0}=$（　　）

- A. $2$
- B. $-2$
- C. $1$
- D. $-1$

````````col
```````col-md
flexGrow=20
===

**答案**：B

**解析**

> 参数方程求导：
>
> $$\frac{dy}{dx}=\frac{dy/dt}{dx/dt}=\frac{e^t+\cos t}{-e^{-t}-\sin t}$$
>
> 代入 $t=0$：$\dfrac{1+1}{-1-0}=\dfrac{2}{-1}=-2$。选 B。

**考点**：参数方程求导（一点处）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第31题

xxxx

**题目**

设函数 $f(x)=e^{x^2}-2x$，则 $\mathrm{d}f(x)=$　$\underline{\qquad\quad}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$\big(2xe^{x^2}-2\big)\mathrm{d}x$

**解析**

> $$f'(x)=e^{x^2}\cdot 2x-2=2xe^{x^2}-2$$
>
> 故 $\mathrm{d}f(x)=\big(2xe^{x^2}-2\big)\mathrm{d}x$。

**考点**：复合函数求导与微分 $\mathrm{d}f=f'(x)\mathrm{d}x$


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第36题

xxxx

**题目**

设二元函数 $z=e^{x+y}-\ln(x+y)$，则 $\dfrac{\partial^2 z}{\partial x\partial y}\bigg|_{\substack{x=1\\y=0}}=$　$\underline{\qquad\quad}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$e+1$

**解析**

> 先对 $x$ 求偏导：
>
> $$\frac{\partial z}{\partial x}=e^{x+y}-\frac{1}{x+y}$$
>
> 再对 $y$ 求偏导：
>
> $$\frac{\partial^2 z}{\partial x\partial y}=e^{x+y}+\frac{1}{(x+y)^2}$$
>
> 代入 $(1,0)$：$e+1$。

**考点**：二元函数二阶混合偏导


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第43题

xxxx

**题目**

设函数 $y=(\sin x)^x$，求 $\dfrac{dy}{dx}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$\dfrac{dy}{dx}=(\sin x)^x\ln(\sin x)+x(\sin x)^{x-1}\cos x$

**解析**

> 幂指函数用对数求导法。两边取对数：
>
> $$\ln y=x\ln(\sin x)$$
>
> 两边对 $x$ 求导：
>
> $$\frac{1}{y}y'=\ln(\sin x)+x\cdot\frac{\cos x}{\sin x}$$
>
> $$y'=(\sin x)^x\Big[\ln(\sin x)+x\cot x\Big]$$
>
> 即 $\dfrac{dy}{dx}=(\sin x)^x\ln(\sin x)+x(\sin x)^{x-1}\cos x$。

**考点**：幂指函数对数求导法


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第48题

xxxx

**题目**

已知函数 $z=z(x,y)$ 由方程 $\sin x-xy^2+e^z-z=0$ 确定，求 $\mathrm{d}z$。

````````col
```````col-md
flexGrow=20
===

**答案**：$\mathrm{d}z=\dfrac{y^2-\cos x}{e^z-1}\mathrm{d}x+\dfrac{2xy}{e^z-1}\mathrm{d}y$

**解析**

> 令 $F(x,y,z)=\sin x-xy^2+e^z-z$，则
>
> $$F_x=\cos x-y^2,\qquad F_y=-2xy,\qquad F_z=e^z-1$$
>
> 由隐函数求导公式：
>
> $$\frac{\partial z}{\partial x}=-\frac{F_x}{F_z}=\frac{y^2-\cos x}{e^z-1},\qquad \frac{\partial z}{\partial y}=-\frac{F_y}{F_z}=\frac{2xy}{e^z-1}$$
>
> 故 $\mathrm{d}z=\dfrac{y^2-\cos x}{e^z-1}\mathrm{d}x+\dfrac{2xy}{e^z-1}\mathrm{d}y$。
> 【订正】源题答解析在已正确写出 $F_z=e^z-1$ 的情况下，后续公式误把分母写成 $e^z+1$，且 $\dfrac{\partial z}{\partial x}$ 的分子符号也写反（写成 $\dfrac{\cos x-y^2}{e^z+1}$）。按公式 $-F_x/F_z$ 复算，正确结果应为 $\dfrac{y^2-\cos x}{e^z-1}$，分母是 $e^z-1$，本专题已订正。

**考点**：隐函数求偏导公式 + 全微分


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
---
# 2025年河南专升本《高等数学》真题·微分的计算专题

> 本卷命中 7 道（第 7、9、22、31、36、43、48 题）。

## 第7题

xxxx

**题目**

函数 $f(x)$ 二阶可导，且 $y=f(e^x)$，则 $y''=$（　　）

- A. $f''(e^x)$
- B. $f''(e^x)e^{2x}$
- C. $e^x f'(e^x)+e^{2x}f''(e^x)$
- D. $e^x f'(e^x)+e^x f''(e^x)$

````````col
```````col-md
flexGrow=20
===

**答案**：C

**解析**

> 一阶：$y'=f'(e^x)\cdot e^x=e^x f'(e^x)$。
>
> 二阶（乘积 + 链式）：
>
> $$y''=e^x f'(e^x)+e^x\cdot f''(e^x)\cdot e^x=e^x f'(e^x)+e^{2x}f''(e^x)$$
>
> 选 C。

**考点**：抽象复合函数二阶导（链式 + 乘积）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第9题

xxxx

**题目**

函数 $y=\cos 2x$，则 $y^{(2025)}=$（　　）

- A. $2^{2025}\sin 2x$
- B. $2^{2025}\cos 2x$
- C. $-2^{2025}\cos 2x$
- D. $-2^{2025}\sin 2x$

````````col
```````col-md
flexGrow=20
===

**答案**：A

**解析**

> 由归纳公式：
>
> $$(\cos 2x)^{(n)}=2^n\cos\Big(2x+\frac{n\pi}{2}\Big)$$
>
> $2025\bmod 4=1$，故
>
> $$y^{(2025)}=2^{2025}\cos\Big(2x+\frac{2025\pi}{2}\Big)=2^{2025}\cos\Big(2x+\frac{\pi}{2}\Big)=2^{2025}\sin 2x$$
>
> 选 A。

**考点**：高阶导数（三角函数周期归纳）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第22题

xxxx

**题目**

已知函数 $x=x(y,z)$ 由 $2xz-2xy+\ln y=0$ 确定，则 $\dfrac{\partial x}{\partial z}=$（　　）

- A. $\dfrac{x}{z-y}$
- B. $\dfrac{y}{x-z}$
- C. $\dfrac{y}{z-x}$
- D. $\dfrac{x}{y-z}$

````````col
```````col-md
flexGrow=20
===

**答案**：D

**解析**

> 两边对 $z$ 求偏导（$x$ 是 $y,z$ 的函数）：
>
> $$2x+2z\frac{\partial x}{\partial z}-2y\frac{\partial x}{\partial z}=0$$
>
> 解得 $\dfrac{\partial x}{\partial z}=\dfrac{-2x}{2(z-y)}=\dfrac{x}{y-z}$。选 D。

**考点**：隐函数（$x$ 为因变量）求偏导


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第31题

xxxx

**题目**

设 $\int f(x)\mathrm{d}x=x^2+\ln(2x)+C$，则 $f(x)=$　$\underline{\qquad\quad}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$2x+\dfrac{1}{x}$

**解析**

> 对原函数（不定积分）两边求导，即得 $f(x)$：
>
> $$f(x)=\big(x^2+\ln(2x)+C\big)'=2x+\frac{1}{x}$$

**考点**：已知原函数求导得 $f(x)$（先积后导）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第36题

xxxx

**题目**

$f(x,y)=x^2+\tan\dfrac{xy}{x^2+y^2}$，则 $\dfrac{\partial f(x,y)}{\partial x}\bigg|_{(1,0)}=$　$\underline{\qquad\quad}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$2$

**解析**

> 由商的链式法则：
>
> $$f_x=2x+\sec^2\Big(\frac{xy}{x^2+y^2}\Big)\cdot\frac{y(x^2+y^2)-xy\cdot 2x}{(x^2+y^2)^2}$$
>
> 代入 $(1,0)$，第二项含因子 $y$ 而为 $0$，故 $f_x(1,0)=2$。

**考点**：复合函数偏导（一点处）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第43题

xxxx

**题目**

对于函数 $\begin{cases}x=(t+1)^3+1\\ y=\arcsin\sqrt{t}\end{cases}$，求 $\dfrac{dy}{dx}\bigg|_{t=\frac{1}{2}}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$\dfrac{4}{27}$

**解析**

> $$\frac{dx}{dt}=3(t+1)^2,\qquad \frac{dy}{dt}=\frac{1}{\sqrt{1-t}}\cdot\frac{1}{2\sqrt{t}}=\frac{1}{2\sqrt{t(1-t)}}$$
>
> $$\frac{dy}{dx}=\frac{dy/dt}{dx/dt}=\frac{1}{2\sqrt{t(1-t)}\cdot 3(t+1)^2}$$
>
> 代入 $t=\dfrac12$：
>
> $$\frac{dy}{dx}\bigg|_{t=1/2}=\frac{1}{2\cdot\frac12\cdot 3\cdot\frac94}=\frac{4}{27}$$

**考点**：参数方程求导（含反三角复合）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第48题

xxxx

**题目**

设二元函数 $z=(x-y)\sin(xy)$，求 $x\dfrac{\partial z}{\partial x}-y\dfrac{\partial z}{\partial y}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$(x+y)\sin(xy)$

**解析**

> $$\frac{\partial z}{\partial x}=\sin(xy)+(x-y)y\cos(xy)$$
>
> $$\frac{\partial z}{\partial y}=-\sin(xy)+(x-y)x\cos(xy)$$
>
> $$x\frac{\partial z}{\partial x}-y\frac{\partial z}{\partial y}=x\sin(xy)+xy(x-y)\cos(xy)+y\sin(xy)-xy(x-y)\cos(xy)$$
>
> $$=(x+y)\sin(xy)$$

**考点**：偏导数计算（含乘积与链式）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
---
# 2024年河南专升本《高等数学》真题·微分的计算专题

> 本卷命中 6 道（第 7、9、31、37、43、48 题）。

## 第7题

xxxx

**题目**

设函数 $f(x)=xe^{-x}+\sin x$，则 $f''(x)=$（　　）

- A. $(x+2)e^{-x}+\sin x$
- B. $(x+2)e^{-x}-\sin x$
- C. $(x-2)e^{-x}+\sin x$
- D. $(x-2)e^{-x}-\sin x$

````````col
```````col-md
flexGrow=20
===

**答案**：D

**解析**

> 一阶：$f'(x)=e^{-x}-xe^{-x}+\cos x=(1-x)e^{-x}+\cos x$。
>
> 二阶：
>
> $$f''(x)=-e^{-x}-(1-x)e^{-x}-\sin x=(x-2)e^{-x}-\sin x$$
>
> 选 D。
> 【机构分歧】豫升/耶鲁选项字母印为 B，但其计算结果 $(x-2)e^{-x}-\sin x$ 对应选项 D，与库课一致，取 D。

**考点**：乘积与复合函数二阶导


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第9题

xxxx

**题目**

设函数 $y=y(x)$ 由参数方程 $\begin{cases}x=2\cos^3 t\\ y=2\sin^3 t\end{cases}$ 确定，则 $\dfrac{dy}{dx}\bigg|_{t=\frac{\pi}{4}}=$（　　）

- A. $1$
- B. $-1$
- C. $2$
- D. $-2$

````````col
```````col-md
flexGrow=20
===

**答案**：B

**解析**

> $$\frac{dy}{dx}=\frac{dy/dt}{dx/dt}=\frac{6\sin^2 t\cos t}{-6\cos^2 t\sin t}=-\tan t$$
>
> 代入 $t=\dfrac{\pi}{4}$ 得 $-1$。选 B。

**考点**：参数方程求导（星形线）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第31题

xxxx

**题目**

设函数 $y=f(x)$ 由方程 $x^2 y-e^y+3=y$ 所确定，则 $\dfrac{dy}{dx}=$　$\underline{\qquad\quad}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$\dfrac{2xy}{1-x^2+e^y}$

**解析**

> 两边对 $x$ 求导：
>
> $$2xy+x^2 y'-e^y y'=y'$$
>
> 整理得 $y'=\dfrac{2xy}{1-x^2+e^y}$。

**考点**：隐函数求导


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第37题

xxxx

**题目**

设 $z=xy e^{x^2+y^2}$，则 $\dfrac{\partial z}{\partial x}\bigg|_{\substack{x=0\\y=1}}=$　$\underline{\qquad\quad}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$e$

**解析**

> $$z_x=y e^{x^2+y^2}+xy\cdot 2x e^{x^2+y^2}=y e^{x^2+y^2}(1+2x^2)$$
>
> 代入 $(0,1)$ 得 $e$。

**考点**：偏导（乘积 + 链式，一点处）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第43题

xxxx

**题目**

已知函数 $y=e^{\sin 2x}+\arcsin\sqrt{x}$，求 $y'$。

````````col
```````col-md
flexGrow=20
===

**答案**：$y'=2e^{\sin 2x}\cos 2x+\dfrac{1}{2\sqrt{x(1-x)}}$

**解析**

> 由复合函数求导法则：
>
> $$y'=e^{\sin 2x}\cdot(\sin 2x)'+\frac{1}{\sqrt{1-(\sqrt{x})^2}}\cdot(\sqrt{x})'$$
>
> $$=e^{\sin 2x}\cdot 2\cos 2x+\frac{1}{\sqrt{1-x}}\cdot\frac{1}{2\sqrt{x}}$$
>
> $$=2e^{\sin 2x}\cos 2x+\frac{1}{2\sqrt{x(1-x)}}$$

**考点**：复合函数求导（指数 + 反三角）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第48题

xxxx

**题目**

已知函数 $z=f(x,y)$ 由方程 $x^2+e^{-y}+z=xyz$ 所确定，求 $\mathrm{d}z$。

````````col
```````col-md
flexGrow=20
===

**答案**：$\mathrm{d}z=\dfrac{yz-2x}{1-xy}\mathrm{d}x+\dfrac{xz+e^{-y}}{1-xy}\mathrm{d}y$

**解析**

> 方程两边全微分：
>
> $$2x\,\mathrm{d}x-e^{-y}\mathrm{d}y+\mathrm{d}z=yz\,\mathrm{d}x+xz\,\mathrm{d}y+xy\,\mathrm{d}z$$
>
> 整理得：
>
> $$(1-xy)\mathrm{d}z=(yz-2x)\mathrm{d}x+(xz+e^{-y})\mathrm{d}y$$
>
> 故 $\mathrm{d}z=\dfrac{yz-2x}{1-xy}\mathrm{d}x+\dfrac{xz+e^{-y}}{1-xy}\mathrm{d}y$。

**考点**：隐函数全微分（全微分形式不变性）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
---
# 2023年河南专升本《高等数学》真题·微分的计算专题

> 本卷命中 7 道（第 7、11、28、29、36、43、48 题）。

## 第7题

xxxx

**题目**

设函数 $y=f(x)$ 可导，且满足 $f'(x^3+2)=\dfrac{1}{x^3+6}$，则 $\mathrm{d}y=$（　　）

- A. $\dfrac{1}{x^3-4}\mathrm{d}x$
- B. $\dfrac{1}{x^3+6}\mathrm{d}x$
- C. $\dfrac{1}{x+4}\mathrm{d}x$
- D. $\dfrac{1}{x-4}\mathrm{d}x$

````````col
```````col-md
flexGrow=20
===

**答案**：C

**解析**

> 令 $t=x^3+2$，则 $x^3=t-2$，于是
>
> $$f'(t)=\frac{1}{t-2+6}=\frac{1}{t+4}$$
>
> 换回 $x$：$f'(x)=\dfrac{1}{x+4}$，故 $\mathrm{d}y=\dfrac{1}{x+4}\mathrm{d}x$。选 C。

**考点**：抽象函数求导与微分（换元还原自变量）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第11题

xxxx

**题目**

设 $y=e^{ax}+x^3$（$a>0$），则 $y'''(0)=$（　　）

- A. $6$
- B. $a^3+6$
- C. $a+6$
- D. $a^2+6$

````````col
```````col-md
flexGrow=20
===

**答案**：B

**解析**

> $$y'=ae^{ax}+3x^2,\qquad y''=a^2e^{ax}+6x,\qquad y'''=a^3e^{ax}+6$$
>
> 故 $y'''(0)=a^3+6$。选 B。

**考点**：高阶导数（一点处）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第28题

xxxx

**题目**

设 $f(x)=(7x-6)^{\frac{8}{7}}+9x$，则 $f''(1)=$　$\underline{\qquad\quad}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$8$

**解析**

> $$f'(x)=8(7x-6)^{1/7}+9$$
>
> $$f''(x)=8(7x-6)^{-6/7}$$
>
> 代入 $x=1$：$f''(1)=8$。

**考点**：幂函数复合二阶导（一点处）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第29题

xxxx

**题目**

设参数方程 $\begin{cases}y=\sqrt{3}t^3+t\\ x=t^2-5\end{cases}$（$t$ 为参数），则 $\dfrac{dy}{dx}=$　$\underline{\qquad\quad}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$\dfrac{3\sqrt{3}\,t^2+1}{2t}$

**解析**

> $$\frac{dy}{dx}=\frac{dy/dt}{dx/dt}=\frac{3\sqrt{3}\,t^2+1}{2t}$$

**考点**：参数方程求导


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第36题

xxxx

**题目**

设函数 $z=2\sin x^2+e^{2y}-3xy^2$，则 $\mathrm{d}z=$　$\underline{\qquad\quad}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$(4x\cos x^2-3y^2)\mathrm{d}x+(2e^{2y}-6xy)\mathrm{d}y$

**解析**

> 分别求两个偏导：
>
> $$z_x=4x\cos x^2-3y^2,\qquad z_y=2e^{2y}-6xy$$
>
> 故 $\mathrm{d}z=(4x\cos x^2-3y^2)\mathrm{d}x+(2e^{2y}-6xy)\mathrm{d}y$。

**考点**：全微分计算（偏导合成）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第43题

xxxx

**题目**

设函数 $y=y(x)$ 是由方程 $\cos y=e^{2x+y}+x^3-y^2+3\pi$ 所确定的隐函数，求 $\dfrac{dy}{dx}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$\dfrac{dy}{dx}=\dfrac{2e^{2x+y}+3x^2}{2y-\sin y-e^{2x+y}}$

**解析**

> 两边对 $x$ 求导：
>
> $$-\sin y\cdot y'=e^{2x+y}(2+y')+3x^2-2y\cdot y'$$
>
> 整理得：
>
> $$y'(2y-\sin y-e^{2x+y})=2e^{2x+y}+3x^2$$
>
> $$\frac{dy}{dx}=\frac{2e^{2x+y}+3x^2}{2y-\sin y-e^{2x+y}}$$

**考点**：隐函数求导（含复合）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第48题

xxxx

**题目**

设 $z=u^2+\cos(xy+u)$，而 $u=x\ln y$，求 $\dfrac{\partial z}{\partial x}$ 和 $\dfrac{\partial z}{\partial y}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$\dfrac{\partial z}{\partial x}=2x(\ln y)^2-(y+\ln y)\sin(xy+x\ln y)$；$\dfrac{\partial z}{\partial y}=\dfrac{2x^2\ln y}{y}-x\Big(1+\dfrac{1}{y}\Big)\sin(xy+x\ln y)$

**解析**

> $\dfrac{\partial u}{\partial x}=\ln y$，$\dfrac{\partial u}{\partial y}=\dfrac{x}{y}$。
>
> $$\frac{\partial z}{\partial x}=2u\ln y-\sin(xy+u)(y+\ln y)=2x(\ln y)^2-(y+\ln y)\sin(xy+x\ln y)$$
>
> $$\frac{\partial z}{\partial y}=2u\cdot\frac{x}{y}-\sin(xy+u)\Big(x+\frac{x}{y}\Big)=\frac{2x^2\ln y}{y}-x\Big(1+\frac{1}{y}\Big)\sin(xy+x\ln y)$$

**考点**：多元复合函数链式求导（含中间变量）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
---
# 2022年河南专升本《高等数学》真题·微分的计算专题

> 本卷命中 6 道（第 6、9、20、29、37、42 题）。

## 第6题

xxxx

**题目**

设 $f(x)=\sqrt{2x}+\dfrac{1}{3}\cos 3x$，求 $f'(x)=$（　　）

- A. $\dfrac{1}{\sqrt{2x}}-\sin 3x$
- B. $\dfrac{1}{\sqrt{2x}}+\sin 3x$
- C. $-\dfrac{1}{\sqrt{2x}}-\sin 3x$
- D. $\dfrac{1}{\sqrt{2x}}-\dfrac{1}{3}\sin 3x$

````````col
```````col-md
flexGrow=20
===

**答案**：A

**解析**

> 分别求导：
>
> $$f'(x)=\frac{1}{\sqrt{2x}}-\sin 3x$$
>
> 选 A。

**考点**：基本求导（幂函数 + 三角）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第9题

xxxx

**题目**

已知 $\begin{cases}x=\cos t\\ y=t+\sin 2t\end{cases}$，求 $\dfrac{dy}{dx}\bigg|_{t=\frac{\pi}{2}}$（　　）

- A. $1$
- B. $2$
- C. $3$
- D. $4$

````````col
```````col-md
flexGrow=20
===

**答案**：A

**解析**

> $$\frac{dy}{dx}=\frac{1+2\cos 2t}{-\sin t}$$
>
> 代入 $t=\dfrac{\pi}{2}$：$\dfrac{1+2\cos\pi}{-1}=\dfrac{1-2}{-1}=1$。选 A。

**考点**：参数方程求导（一点处）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第20题

xxxx

**题目**

已知 $y=\arcsin(3x+1)$，则 $\mathrm{d}y=$（　　）

- A. $\dfrac{3\mathrm{d}x}{\sqrt{1-(3x+1)^2}}$
- B. $\dfrac{-3\mathrm{d}x}{\sqrt{1-(3x+1)^2}}$
- C. $\dfrac{3\mathrm{d}x}{\sqrt{1+(3x+1)^2}}$
- D. $\dfrac{-3\mathrm{d}x}{\sqrt{1+(3x+1)^2}}$

````````col
```````col-md
flexGrow=20
===

**答案**：A

**解析**

> 由反三角复合求导：
>
> $$y'=\frac{3}{\sqrt{1-(3x+1)^2}}$$
>
> 故 $\mathrm{d}y=\dfrac{3\mathrm{d}x}{\sqrt{1-(3x+1)^2}}$。选 A。

**考点**：反三角函数复合求导与微分


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第29题

xxxx

**题目**

已知函数 $f(x)=5^x$，则 $f^{(n)}(x)=$　$\underline{\qquad\quad}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$5^x(\ln 5)^n$

**解析**

> 指数函数逐次求导每次都乘一个 $\ln 5$，故 $n$ 阶导数为 $5^x(\ln 5)^n$。

**考点**：高阶导数（指数函数归纳）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第37题

xxxx

**题目**

已知 $u=5+e^{3x-yz}$，则 $\dfrac{\partial^2 u}{\partial x\partial y}=$　$\underline{\qquad\quad}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$-3z e^{3x-yz}$

**解析**

> 先对 $x$ 求偏导：$\dfrac{\partial u}{\partial x}=3e^{3x-yz}$。
>
> 再对 $y$ 求偏导：
>
> $$\frac{\partial^2 u}{\partial x\partial y}=3e^{3x-yz}\cdot(-z)=-3z e^{3x-yz}$$

**考点**：二阶混合偏导（指数复合）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第42题

xxxx

**题目**

若 $F(x,y,z)=\sin(x+3y-2z)=x+3y-2z$ 确定隐函数 $z=z(x,y)$，求 $\dfrac{\partial z}{\partial x}+\dfrac{\partial z}{\partial y}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$2$

**解析**

> 令 $G(x,y,z)=\sin(x+3y-2z)-(x+3y-2z)=0$，记 $u=x+3y-2z$，则
>
> $$G_x=\cos u-1,\qquad G_y=3\cos u-3,\qquad G_z=-2\cos u+2$$
>
> $$\frac{\partial z}{\partial x}=-\frac{G_x}{G_z}=\frac12,\qquad \frac{\partial z}{\partial y}=-\frac{G_y}{G_z}=\frac32$$
>
> 故 $\dfrac{\partial z}{\partial x}+\dfrac{\partial z}{\partial y}=\dfrac12+\dfrac32=2$。

**考点**：隐函数求偏导（公式法）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
---
# 2021年河南专升本《高等数学》真题·微分的计算专题

> 本卷命中 7 道（第 7、8、21、31、37、43、48 题）。

## 第7题

xxxx

**题目**

设函数 $f(x)=x^n+a_1x^{n-1}+a_2x^{n-2}+\cdots+a_n$，则 $f^{(n)}(x)=$（　　）

- A. $a_n$
- B. $n!$
- C. $0$
- D. $n!a_n$

````````col
```````col-md
flexGrow=20
===

**答案**：B

**解析**

> $n$ 次多项式求 $n$ 阶导数后，只剩最高次项 $x^n$ 的贡献，等于 $n!$；其余次数低于 $n$ 的项在 $n$ 阶导后均为 $0$。选 B。

**考点**：高阶导数（多项式 $n$ 阶导）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第8题

xxxx

**题目**

设 $f(x)=\ln\sqrt{1+x}$，则 $f'(1)=$（　　）

- A. $2$
- B. $1$
- C. $\dfrac{1}{2}$
- D. $\dfrac{1}{4}$

````````col
```````col-md
flexGrow=20
===

**答案**：D

**解析**

> $f(x)=\dfrac12\ln(1+x)$，故
>
> $$f'(x)=\frac{1}{2(1+x)}$$
>
> 代入 $x=1$：$f'(1)=\dfrac14$。选 D。

**考点**：复合函数求导（一点处）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第21题

xxxx

**题目**

设 $z=x^2-2xy-y^2$，则 $\dfrac{\partial^2 z}{\partial x\partial y}\bigg|_{(1,2)}=$（　　）

- A. $1$
- B. $2$
- C. $-2$
- D. $-1$

````````col
```````col-md
flexGrow=20
===

**答案**：C

**解析**

> $$z_x=2x-2y,\qquad z_{xy}=-2$$
>
> 与点无关，值为 $-2$。选 C。

**考点**：二阶混合偏导


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第31题

xxxx

**题目**

设曲线方程为 $\begin{cases}x=2\cos\theta+\sin 2\theta\\ y=2\sin\theta+\cos 2\theta\end{cases}$（$\theta$ 为参数），则 $\dfrac{dy}{dx}\bigg|_{\theta=0}=$　$\underline{\qquad\quad}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$1$

**解析**

> $$\frac{dy}{dx}=\frac{2\cos\theta-2\sin 2\theta}{-2\sin\theta+2\cos 2\theta}$$
>
> 代入 $\theta=0$：$\dfrac{2}{2}=1$。

**考点**：参数方程求导（一点处）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第37题

xxxx

**题目**

设二元函数 $z=2xy+y^2$，则 $\mathrm{d}z\big|_{(3,1)}=$　$\underline{\qquad\quad}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$2\mathrm{d}x+8\mathrm{d}y$

**解析**

> $$z_x=2y=2,\qquad z_y=2x+2y=8$$
>
> 故 $\mathrm{d}z\big|_{(3,1)}=2\mathrm{d}x+8\mathrm{d}y$。

**考点**：全微分（一点处）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第43题

xxxx

**题目**

设函数 $y=\arctan\sqrt{x}$，求 $\dfrac{dy}{dx}$ 及 $\dfrac{dy}{dx}\big|_{x=1}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$\dfrac{dy}{dx}=\dfrac{1}{2\sqrt{x}(1+x)}$；$\dfrac{dy}{dx}\big|_{x=1}=\dfrac14$

**解析**

> $$\frac{dy}{dx}=\frac{1}{1+(\sqrt{x})^2}\cdot\frac{1}{2\sqrt{x}}=\frac{1}{2\sqrt{x}(1+x)}$$
>
> 代入 $x=1$：$\dfrac{dy}{dx}\big|_{x=1}=\dfrac14$。

**考点**：复合函数求导（反三角）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第48题

xxxx

**题目**

设二元函数 $z=\dfrac{x^2}{3y}+\arcsin(xy)$，求 $xy\dfrac{\partial z}{\partial x}-y^2\dfrac{\partial z}{\partial y}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$x^2$

**解析**

> $$z_x=\frac{2x}{3y}+\frac{y}{\sqrt{1-x^2y^2}},\qquad z_y=-\frac{x^2}{3y^2}+\frac{x}{\sqrt{1-x^2y^2}}$$
>
> $$xy\,z_x-y^2z_y=\frac{2x^2}{3}+\frac{xy^2}{\sqrt{1-x^2y^2}}+\frac{x^2}{3}-\frac{xy^2}{\sqrt{1-x^2y^2}}=x^2$$

**考点**：偏导数计算（含反三角复合）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
---
# 2020年河南专升本《高等数学》真题·微分的计算专题

> 本卷命中 8 道（第 11、15、19、24、34、38、42、48 题）。本卷结构为选择 30 题、填空 10 题、计算 10 题、应用 2 题、证明 1 题。

## 第11题

xxxx

**题目**

设 $\begin{cases}x=\cos t\\ y=t\cos t-\sin t\end{cases}$（$t$ 为参数），则 $\dfrac{d^2y}{dx^2}\bigg|_{t=\pi/4}=$（　　）

- A. $-\sqrt{2}$
- B. $\sqrt{2}$
- C. $\dfrac{\sqrt{2}}{2}$
- D. $-\dfrac{\sqrt{2}}{2}$

````````col
```````col-md
flexGrow=20
===

**答案**：A

**解析**

> $$\frac{dy}{dt}=-t\sin t,\qquad \frac{dx}{dt}=-\sin t$$
>
> $$\frac{dy}{dx}=\frac{-t\sin t}{-\sin t}=t$$
>
> $$\frac{d^2y}{dx^2}=\frac{d(dy/dx)/dt}{dx/dt}=\frac{1}{-\sin t}=-\frac{1}{\sin t}$$
>
> 代入 $t=\dfrac{\pi}{4}$：$-\sqrt{2}$。选 A。

**考点**：参数方程二阶导


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第15题

xxxx

**题目**

设 $y=f(x)$ 由方程 $y^2-3xy+x^3=1$ 确定，则 $y'=$（　　）

- A. $\dfrac{3x^2-3y}{2y-3x}$
- B. $\dfrac{3y-3x^2}{2y-3x}$
- C. $\dfrac{2y-3x}{3x^2-3y}$
- D. $\dfrac{3x-2y}{3x^2-3y}$

````````col
```````col-md
flexGrow=20
===

**答案**：B

**解析**

> 两边对 $x$ 求导：
>
> $$2y\,y'-3(y+xy')+3x^2=0$$
>
> $$(2y-3x)y'=3y-3x^2$$
>
> 故 $y'=\dfrac{3y-3x^2}{2y-3x}$。选 B。

**考点**：隐函数求导


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第19题

xxxx

**题目**

设 $\int_0^x f(t)\mathrm{d}t=e^{2x}-1$，其中 $f(x)$ 为连续函数，则 $f^{(n)}(x)=$（　　）

- A. $2e^{2x}$
- B. $2^{n-1}e^{2x}$
- C. $2^n e^{2x}$
- D. $2^{n+1}e^{2x}$

````````col
```````col-md
flexGrow=20
===

**答案**：D

**解析**

> 两边对 $x$ 求导（微积分基本定理）：$f(x)=2e^{2x}$。
>
> 再求 $n$ 阶导：
>
> $$f^{(n)}(x)=2\cdot 2^n e^{2x}=2^{n+1}e^{2x}$$
>
> 选 D。

**考点**：基本定理求导 + 高阶导（指数函数）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第24题

xxxx

**题目**

设函数 $z=\sin(xy^2)$，则 $\dfrac{\partial^2 z}{\partial x^2}=$（　　）

- A. $y^4\cos(xy^2)$
- B. $-y^4\cos(xy^2)$
- C. $y^4\sin(xy^2)$
- D. $-y^4\sin(xy^2)$

````````col
```````col-md
flexGrow=20
===

**答案**：D

**解析**

> $$\frac{\partial z}{\partial x}=y^2\cos(xy^2)$$
>
> $$\frac{\partial^2 z}{\partial x^2}=y^2\big(-\sin(xy^2)\big)\cdot y^2=-y^4\sin(xy^2)$$
>
> 选 D。

**考点**：二阶偏导（三角复合）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第34题

xxxx

**题目**

设 $f(x)=x^3+3x\lim\limits_{x\to 2}f(x)$，且 $\lim\limits_{x\to 2}f(x)$ 存在，则 $f'(x)=$　$\underline{\qquad\quad}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$3x^2-\dfrac{24}{5}$

**解析**

> 设 $L=\lim\limits_{x\to 2}f(x)$，对等式两边取 $x\to 2$ 的极限：
>
> $$L=2^3+3\cdot 2\cdot L=8+6L$$
>
> 解得 $L=-\dfrac85$。于是
>
> $$f(x)=x^3-\frac{24}{5}x$$
>
> $$f'(x)=3x^2-\frac{24}{5}$$

**考点**：含极限常数的函数求导


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第38题

xxxx

**题目**

设 $z=\ln(x^2+y)$，则全微分 $\mathrm{d}z=$　$\underline{\qquad\quad}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$\dfrac{2x\,\mathrm{d}x+\mathrm{d}y}{x^2+y}$

**解析**

> $$\frac{\partial z}{\partial x}=\frac{2x}{x^2+y},\qquad \frac{\partial z}{\partial y}=\frac{1}{x^2+y}$$
>
> 故 $\mathrm{d}z=\dfrac{2x\,\mathrm{d}x+\mathrm{d}y}{x^2+y}$。

**考点**：全微分（对数复合）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第42题

xxxx

**题目**

求函数 $y=x^{\ln x}$ 的导数。

````````col
```````col-md
flexGrow=20
===

**答案**：$y'=x^{\ln x}\cdot\dfrac{2\ln x}{x}=2x^{\ln x-1}\ln x$

**解析**

> 取对数：$\ln y=(\ln x)^2$。
>
> 两边对 $x$ 求导：
>
> $$\frac{y'}{y}=\frac{2\ln x}{x}$$
>
> 故 $y'=x^{\ln x}\cdot\dfrac{2\ln x}{x}=2x^{\ln x-1}\ln x$。

**考点**：幂指函数对数求导法


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第48题

xxxx

**题目**

设函数 $z=z(x,y)$ 由方程 $x^2+y^3+3xyz^2+2z=1$ 所确定，求 $\dfrac{\partial z}{\partial x}$，$\dfrac{\partial z}{\partial y}$。（其中 $6xyz+2\neq 0$）

````````col
```````col-md
flexGrow=20
===

**答案**：$\dfrac{\partial z}{\partial x}=-\dfrac{2x+3yz^2}{6xyz+2}$；$\dfrac{\partial z}{\partial y}=-\dfrac{3y^2+3xz^2}{6xyz+2}$

**解析**

> 令 $F(x,y,z)=x^2+y^3+3xyz^2+2z-1$，则
>
> $$F_x=2x+3yz^2,\qquad F_y=3y^2+3xz^2,\qquad F_z=6xyz+2$$
>
> 由隐函数公式：
>
> $$\frac{\partial z}{\partial x}=-\frac{F_x}{F_z}=-\frac{2x+3yz^2}{6xyz+2},\qquad \frac{\partial z}{\partial y}=-\frac{F_y}{F_z}=-\frac{3y^2+3xz^2}{6xyz+2}$$

**考点**：隐函数求偏导（公式法）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
---
# 2019年河南专升本《高等数学》真题·微分的计算专题

> 本卷命中 6 道（第 12、23、29、38、40、43 题）。

## 第12题

xxxx

**题目**

已知 $y=xe^x$，求 $\mathrm{d}y=$（　　）

- A. $xe^x\mathrm{d}x$
- B. $e^x\mathrm{d}x$
- C. $(1+x)e^x\mathrm{d}x$
- D. $(x+e^x)\mathrm{d}x$

````````col
```````col-md
flexGrow=20
===

**答案**：C

**解析**

> 由乘积求导：
>
> $$y'=e^x+xe^x=(1+x)e^x$$
>
> 故 $\mathrm{d}y=(1+x)e^x\mathrm{d}x$。选 C。

**考点**：乘积求导与微分


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第23题

xxxx

**题目**

$z=x\ln(x+y)$，求 $\dfrac{\partial^2 z}{\partial x\partial y}=$（　　）

- A. $\dfrac{x}{(x+y)^2}$
- B. $\dfrac{y}{(x+y)^2}$
- C. $\dfrac{2x+y}{(x+y)^2}$
- D. $\dfrac{x+2y}{(x+y)^2}$

````````col
```````col-md
flexGrow=20
===

**答案**：B

**解析**

> 先对 $x$ 求偏导：
>
> $$\frac{\partial z}{\partial x}=\ln(x+y)+\frac{x}{x+y}$$
>
> 再对 $y$ 求偏导：
>
> $$\frac{\partial^2 z}{\partial x\partial y}=\frac{1}{x+y}-\frac{x}{(x+y)^2}=\frac{y}{(x+y)^2}$$
>
> 选 B。
> 【机构分歧】好老师键为 D，按 $\dfrac{\partial^2 z}{\partial x\partial y}=\dfrac{y}{(x+y)^2}$ 应为 B，本专题取 B。

**考点**：二阶混合偏导（含对数）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第29题

xxxx

**题目**

$y=2e^x-x^2+x+1$，$y^{(520)}=$（　　）

- A. $520e^x$
- B. $2e^x$
- C. $2e^{520x}$
- D. $0$

````````col
```````col-md
flexGrow=20
===

**答案**：B

**解析**

> $-x^2+x+1$ 的二阶及以上导数为 $0$；而 $(e^x)^{(n)}=e^x$。故
>
> $$y^{(520)}=2e^x$$
>
> 选 B。

**考点**：高阶导数（指数 + 多项式）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第38题

xxxx

**题目**

求出 $z=x^2+y^2$ 的全微分 $\mathrm{d}z=$　$\underline{\qquad\quad}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$2x\,\mathrm{d}x+2y\,\mathrm{d}y$

**解析**

> $$\frac{\partial z}{\partial x}=2x,\qquad \frac{\partial z}{\partial y}=2y$$
>
> 故 $\mathrm{d}z=2x\,\mathrm{d}x+2y\,\mathrm{d}y$。

**考点**：全微分（偏导合成）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第40题

xxxx

**题目**

求参数方程 $\begin{cases}x=\dfrac12\cos^3 t\\ y=\dfrac12\sin^3 t\end{cases}$ 的导数 $\dfrac{dy}{dx}=$　$\underline{\qquad\quad}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$-\tan t$

**解析**

> $$\frac{dy}{dx}=\frac{dy/dt}{dx/dt}=\frac{\dfrac32\sin^2 t\cos t}{-\dfrac32\cos^2 t\sin t}=-\tan t$$

**考点**：参数方程求导


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第43题

xxxx

**题目**

$xy+xyz=2x-4y$，$xy\neq 0$，求 $\dfrac{\partial z}{\partial x}$，$\dfrac{\partial z}{\partial y}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$\dfrac{\partial z}{\partial x}=\dfrac{4}{x^2}$；$\dfrac{\partial z}{\partial y}=-\dfrac{2}{y^2}$

**解析**

> 方程两边同除以 $xy$，得 $1+z=\dfrac{2}{y}-\dfrac{4}{x}$，即
>
> $$z=\frac{2}{y}-\frac{4}{x}-1$$
>
> 分别求偏导：
>
> $$\frac{\partial z}{\partial x}=\frac{4}{x^2},\qquad \frac{\partial z}{\partial y}=-\frac{2}{y^2}$$

**考点**：隐函数（先解出 $z$）求偏导


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
---
# 2018年河南专升本《高等数学》真题·微分的计算专题

> 本卷命中 5 道（第 8、9、34、42、50 题）。

## 第8题

xxxx

**题目**

已知 $y=x\ln x$，则 $y'''=$（　　）

- A. $\dfrac{1}{x}$
- B. $\dfrac{1}{x^2}$
- C. $-\dfrac{1}{x}$
- D. $-\dfrac{1}{x^2}$

````````col
```````col-md
flexGrow=20
===

**答案**：D

**解析**

> $$y'=\ln x+1,\qquad y''=\frac{1}{x},\qquad y'''=-\frac{1}{x^2}$$
>
> 选 D。

**考点**：高阶导数（对数乘积）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第9题

xxxx

**题目**

已知二元函数 $z=(2y+1)^x$，则 $\dfrac{\partial z}{\partial y}=$（　　）

- A. $x(2y+1)^{x-1}$
- B. $2x(2y+1)^{x-1}$
- C. $(2y+1)^x\ln(2y+1)$
- D. $2(2y+1)^x\ln(2y+1)$

````````col
```````col-md
flexGrow=20
===

**答案**：B

**解析**

> 对 $y$ 求偏导（$x$ 视为常数，幂函数 + 链式）：
>
> $$\frac{\partial z}{\partial y}=x(2y+1)^{x-1}\cdot 2=2x(2y+1)^{x-1}$$
>
> 选 B。

**考点**：偏导数（幂函数复合）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第34题

xxxx

**题目**

已知函数 $y=x\sin x$，则 $\mathrm{d}y=$　$\underline{\qquad\quad}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$(\sin x+x\cos x)\mathrm{d}x$

**解析**

> 由乘积求导：$y'=\sin x+x\cos x$，故
>
> $$\mathrm{d}y=(\sin x+x\cos x)\mathrm{d}x$$

**考点**：乘积求导与微分


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第42题

xxxx

**题目**

已知 $\begin{cases}x=2(t-\sin t)\\ y=2(1-\cos t)\end{cases}$，$0\leq t\leq 2\pi$，求 $\dfrac{d^2y}{dx^2}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$-\dfrac{1}{2(1-\cos t)^2}$

**解析**

> $$\frac{dx}{dt}=2(1-\cos t),\qquad \frac{dy}{dt}=2\sin t$$
>
> $$\frac{dy}{dx}=\frac{\sin t}{1-\cos t}$$
>
> $$\frac{d}{dt}\Big(\frac{dy}{dx}\Big)=\frac{\cos t(1-\cos t)-\sin^2 t}{(1-\cos t)^2}=-\frac{1}{1-\cos t}$$
>
> $$\frac{d^2y}{dx^2}=\frac{-1/(1-\cos t)}{2(1-\cos t)}=-\frac{1}{2(1-\cos t)^2}$$

**考点**：参数方程二阶导（摆线）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第50题

xxxx

**题目**

已知函数 $z=e^{xy}+\cos(x+y)$，求全微分 $\mathrm{d}z$。

````````col
```````col-md
flexGrow=20
===

**答案**：$\mathrm{d}z=\big[ye^{xy}-\sin(x+y)\big]\mathrm{d}x+\big[xe^{xy}-\sin(x+y)\big]\mathrm{d}y$

**解析**

> $$\frac{\partial z}{\partial x}=ye^{xy}-\sin(x+y),\qquad \frac{\partial z}{\partial y}=xe^{xy}-\sin(x+y)$$
>
> 故 $\mathrm{d}z=\big[ye^{xy}-\sin(x+y)\big]\mathrm{d}x+\big[xe^{xy}-\sin(x+y)\big]\mathrm{d}y$。

**考点**：全微分计算（指数 + 三角复合）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
---
# 2017年河南专升本《高等数学》真题·微分的计算专题

> 本卷命中 12 道（第 3、4、10、24、27、33、34、38、41、47、48、49 题），是十一年中命中最多的一年。

## 第3题

xxxx

**题目**

设函数 $y=\cos 5x-\sin 3x$，则 $y'=$（　　）

- A. $-5\sin 5x-3\cos 3x$
- B. $5\cos 5x+3\sin 3x$
- C. $\cos 5x-\sin 3x$
- D. $\cos 5x+\sin 3x$

````````col
```````col-md
flexGrow=20
===

**答案**：A

**解析**

> 由链式求导：
>
> $$y'=-5\sin 5x-3\cos 3x$$
>
> 选 A。

**考点**：基本求导（三角复合）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第4题

xxxx

**题目**

设 $z=6x^3y^2$，则 $\dfrac{\partial z}{\partial y}=$（　　）

- A. $18x^2y^2$
- B. $12x^3y$
- C. $18x^3y^2$
- D. $6x^2y^2$

````````col
```````col-md
flexGrow=20
===

**答案**：B

**解析**

> 对 $y$ 求偏导（$x$ 视为常数）：
>
> $$\frac{\partial z}{\partial y}=6x^3\cdot 2y=12x^3y$$
>
> 选 B。

**考点**：偏导数（幂函数）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第10题

xxxx

**题目**

二元函数 $z=2x^2+xy^3$，则 $\dfrac{\partial^2 z}{\partial x\partial y}=$（　　）

- A. $4x$
- B. $2y$
- C. $3y^2$
- D. $3x^2$

````````col
```````col-md
flexGrow=20
===

**答案**：C

**解析**

> $$\frac{\partial z}{\partial x}=4x+y^3$$
>
> $$\frac{\partial^2 z}{\partial x\partial y}=3y^2$$
>
> 选 C。

**考点**：二阶混合偏导


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第24题

xxxx

**题目**

函数 $f(x)=\ln|x-1|$ 的导数是（　　）

- A. $f'(x)=\dfrac{1}{|x-1|}$
- B. $f'(x)=\dfrac{1}{x-1}$
- C. $f'(x)=\dfrac{1}{1-x}$
- D. 不存在

````````col
```````col-md
flexGrow=20
===

**答案**：B

**解析**

> 由公式 $(\ln|u|)'=\dfrac{u'}{u}$，取 $u=x-1$：
>
> $$f'(x)=\frac{1}{x-1}$$
>
> 选 B。

**考点**：含绝对值对数函数求导


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第27题

xxxx

**题目**

设 $f(x)=x\cos x$，则 $f'\Big(\dfrac{\pi}{2}\Big)=$（　　）

- A. $\dfrac12$
- B. $1$
- C. $-\dfrac{\pi}{2}$
- D. $2\pi$

````````col
```````col-md
flexGrow=20
===

**答案**：C

**解析**

> 由乘积求导：
>
> $$f'(x)=\cos x-x\sin x$$
>
> 代入 $x=\dfrac{\pi}{2}$：$f'\Big(\dfrac{\pi}{2}\Big)=0-\dfrac{\pi}{2}=-\dfrac{\pi}{2}$。选 C。

**考点**：乘积求导（一点处）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第33题

xxxx

**题目**

已知函数 $y=x\arctan x$，则 $y''=$　$\underline{\qquad\quad}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$\dfrac{2}{(1+x^2)^2}$

**解析**

> $$y'=\arctan x+\frac{x}{1+x^2}$$
>
> $$y''=\frac{1}{1+x^2}+\frac{1-x^2}{(1+x^2)^2}=\frac{2}{(1+x^2)^2}$$

**考点**：二阶导（反三角乘积）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第34题

xxxx

**题目**

设 $y=\sin^3(2x+1)$，$y'=$　$\underline{\qquad\quad}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$6\sin^2(2x+1)\cos(2x+1)$

**解析**

> 多层链式求导：
>
> $$y'=3\sin^2(2x+1)\cdot\cos(2x+1)\cdot 2=6\sin^2(2x+1)\cos(2x+1)$$

**考点**：复合函数链式求导（多层）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第38题

xxxx

**题目**

设 $y=e^{x\cos x}$，$\mathrm{d}y=$　$\underline{\qquad\quad}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$(\cos x-x\sin x)e^{x\cos x}\mathrm{d}x$

**解析**

> $$y'=e^{x\cos x}\cdot(\cos x-x\sin x)$$
>
> 故 $\mathrm{d}y=(\cos x-x\sin x)e^{x\cos x}\mathrm{d}x$。

**考点**：复合函数求导与微分（指数 + 乘积）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第41题

xxxx

**题目**

求函数 $z=x^2y^2+e^{xy}$ 在点 $(1,1)$ 处的全微分。

````````col
```````col-md
flexGrow=20
===

**答案**：$\mathrm{d}z\big|_{(1,1)}=(2+e)\mathrm{d}x+(2+e)\mathrm{d}y=(2+e)(\mathrm{d}x+\mathrm{d}y)$

**解析**

> $$z_x=2xy^2+ye^{xy},\qquad z_y=2x^2y+xe^{xy}$$
>
> 在 $(1,1)$ 处：$z_x=2+e$，$z_y=2+e$。
>
> 故 $\mathrm{d}z\big|_{(1,1)}=(2+e)(\mathrm{d}x+\mathrm{d}y)$。

**考点**：全微分（一点处）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第47题

xxxx

**题目**

设函数 $y=y(x)$ 由方程 $\ln(x^2+y)=x^3y+\sin x$ 确定，求 $\dfrac{dy}{dx}\bigg|_{x=0}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$1$

**解析**

> 当 $x=0$ 时，$\ln y=0$，故 $y=1$。
>
> 方程两边对 $x$ 求导：
>
> $$\frac{2x+y'}{x^2+y}=3x^2y+x^3y'+\cos x$$
>
> 代入 $(0,1)$：$\dfrac{y'}{1}=1$，故 $y'\big|_{x=0}=1$。

**考点**：隐函数求导（一点处）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第48题

xxxx

**题目**

求曲线 $\begin{cases}x=e^t\cos t\\ y=e^t\sin t\end{cases}$ 在 $t=\dfrac{\pi}{2}$ 处的法线方程。

````````col
```````col-md
flexGrow=20
===

**答案**：$y=x+e^{\pi/2}$

**解析**

> 当 $t=\dfrac{\pi}{2}$ 时，$x=0$，$y=e^{\pi/2}$。
>
> $$\frac{dx}{dt}=e^t(\cos t-\sin t),\qquad \frac{dy}{dt}=e^t(\sin t+\cos t)$$
>
> 在 $t=\dfrac{\pi}{2}$ 处：$\dfrac{dx}{dt}=-e^{\pi/2}$，$\dfrac{dy}{dt}=e^{\pi/2}$，故 $\dfrac{dy}{dx}=-1$。
>
> 法线斜率为 $1$，法线方程：$y-e^{\pi/2}=x$，即 $y=x+e^{\pi/2}$。

**考点**：参数方程求导 + 平面曲线法线


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第49题

xxxx

**题目**

设 $y=x^{\sin x}$（$x>0$），求 $y'$。

````````col
```````col-md
flexGrow=20
===

**答案**：$y'=x^{\sin x}\Big(\cos x\ln x+\dfrac{\sin x}{x}\Big)$

**解析**

> 两边取对数：$\ln y=\sin x\ln x$。
>
> 两边对 $x$ 求导：
>
> $$\frac{y'}{y}=\cos x\ln x+\frac{\sin x}{x}$$
>
> 故 $y'=x^{\sin x}\Big(\cos x\ln x+\dfrac{\sin x}{x}\Big)$。

**考点**：幂指函数对数求导法


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
---
# 2016年河南专升本《高等数学》真题·微分的计算专题

> 本卷命中 6 道（第 9、24、34、37、42、46 题）。

## 第9题

xxxx

**题目**

已知函数 $\varphi(x)$ 在点 $x=0$ 处可导，函数 $f(x)=(x-1)\varphi(x-1)$，则 $f'(1)=$（　　）

- A. $\varphi'(0)$
- B. $\varphi'(1)$
- C. $\varphi(0)$
- D. $\varphi(1)$

````````col
```````col-md
flexGrow=20
===

**答案**：C

**解析**

> 由乘积求导：
>
> $$f'(x)=\varphi(x-1)+(x-1)\varphi'(x-1)$$
>
> 代入 $x=1$：$f'(1)=\varphi(0)+0=\varphi(0)$。选 C。

**考点**：乘积求导（抽象函数，一点处）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第24题

xxxx

**题目**

设二元函数 $z=x^3+xy^2+y^3$，则 $\dfrac{\partial^2 z}{\partial x\partial y}=$（　　）

- A. $3y^2$
- B. $3x^2$
- C. $2y$
- D. $2x$

````````col
```````col-md
flexGrow=20
===

**答案**：C

**解析**

> $$\frac{\partial z}{\partial x}=3x^2+y^2$$
>
> $$\frac{\partial^2 z}{\partial x\partial y}=2y$$
>
> 选 C。

**考点**：二阶混合偏导


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第34题

xxxx

**题目**

函数 $f(x)=e^{1-x}$，在点 $x=0.99$ 处的近似值为　$\underline{\qquad\quad}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$1.01$

**解析**

> 用微分（线性近似）：$f(1)=1$，$f'(1)=-e^{1-x}\big|_{x=1}=-1$。
>
> $$f(0.99)\approx f(1)+f'(1)(0.99-1)=1+(-1)(-0.01)=1.01$$

**考点**：微分的线性近似（一阶近似）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第37题

xxxx

**题目**

函数 $z=xy-x^2-y^2$ 在点 $(0,1)$ 处的全微分 $\mathrm{d}z\big|_{(0,1)}=$　$\underline{\qquad\quad}$。

````````col
```````col-md
flexGrow=20
===

**答案**：$\mathrm{d}x-2\mathrm{d}y$

**解析**

> $$z_x=y-2x,\qquad z_y=x-2y$$
>
> 在 $(0,1)$ 处：$z_x=1$，$z_y=-2$。
>
> 故 $\mathrm{d}z\big|_{(0,1)}=\mathrm{d}x-2\mathrm{d}y$。

**考点**：全微分（一点处）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第42题

xxxx

**题目**

求函数 $y=\sqrt{2-\cos x}$ 的导数。

````````col
```````col-md
flexGrow=20
===

**答案**：$y'=\dfrac{\sin x}{2\sqrt{2-\cos x}}$

**解析**

> $y=(2-\cos x)^{1/2}$，由复合函数链式求导：
>
> $$y'=\frac{1}{2\sqrt{2-\cos x}}\cdot(2-\cos x)'=\frac{\sin x}{2\sqrt{2-\cos x}}$$

**考点**：复合函数链式求导


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
## 第46题

xxxx

**题目**

已知函数 $z=f(x,y)$ 由方程 $xz-yz-x+y=0$ 所确定，求全微分 $\mathrm{d}z$。

````````col
```````col-md
flexGrow=20
===

**答案**：$\mathrm{d}z=\dfrac{1-z}{x-y}\mathrm{d}x+\dfrac{z-1}{x-y}\mathrm{d}y$

**解析**

> 令 $F(x,y,z)=xz-yz-x+y$，则
>
> $$F_x=z-1,\qquad F_y=1-z,\qquad F_z=x-y$$
>
> 由隐函数公式：
>
> $$\frac{\partial z}{\partial x}=-\frac{F_x}{F_z}=\frac{1-z}{x-y},\qquad \frac{\partial z}{\partial y}=-\frac{F_y}{F_z}=\frac{z-1}{x-y}$$
>
> 故 $\mathrm{d}z=\dfrac{1-z}{x-y}\mathrm{d}x+\dfrac{z-1}{x-y}\mathrm{d}y$。

**考点**：隐函数求导 + 全微分（公式法）


```````

```````col-md
flexGrow=1
===





```````
````````


zzzz
---
> 全文完。本专题共收录 2016—2026 十一年真题 **76 道**，全部题面、选项、答案逐字照录并经符号计算独立复算；源文件笔误（2026-48）已加【订正】，机构分歧（2024-7、2019-23）已保留标注。返回 MOC：[[🏠首页-十年真题MOC]]
> （注：部分内容由豆包 AI 生成）