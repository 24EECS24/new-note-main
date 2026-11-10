#flashcards/函数/三要素   



$$
\begin{align*}
若\quad &D_{a} \to a(\ )\to R_{a}\quad(\text{第一层：内层})\\[4pt]
&D_{b} \to b(\ )\to R_{b}\quad(\text{第二层：外层})\\[4pt]
&D \to b\big[a(\ )\big]\to R\\[4pt]
则\quad &  \\[4pt]
&\left.\begin{matrix}
 D_{b}\xrightarrow[]{a^{-1}(\ )} \Box 
\\[4pt]
D_{a}\cap \Box =D
\end{matrix}\right\} D=D_{a}\cap a^{-1}(D_{b}) \\[4pt]
&\left.\begin{matrix}
 D\xrightarrow[]{a(\ )}R_{a}\cap D_{b}\xrightarrow[]{b(\ )}R
\\[4pt]
D_{a}\xrightarrow[]{a(\ )}R_{a}，R_{a}\cap D_{b}\xrightarrow[]{b(\ )}R
\end{matrix}\right\} R=b\big[a(D)\big]=b\big[R_{a}\cap D_{b}\big] \\[4pt]
\end{align*}
$$
求值域，本质是求最值
`````col
````col-md
flexGrow=1
===

$$
\begin{align*}
&无论是求定义域还是求值域\\[4pt]
&都是从各层定义域D_{a}，D_{b}入手\\[4pt]
&D_{a}与D_{b}往往都能直接得到\\[4pt]
\end{align*}
$$

````

````col-md
flexGrow=1
===

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
eg: \ &lnx \ ，\ x> 0   &&arcsinx\ ，\ x\in [-1,1] \\[4pt]                      
&\sqrt{x} \ ，\ x\ge 0  &&arctanx\ ，\ x\in R   \\[4pt]
&\frac{1}{x}  \ ，\ x\ne 0 \\[4pt]
\end{align*}
$$



````
`````

## 定义域

xxxx

函数 $f(x)=\dfrac{1}{\sqrt{4-x^2}}$ 的定义域是（　　）

- A. $[-2,2)$
- B. $(-2,2)$
- C. $(-2,2]$
- D. $[-2,2]$
?
**答案**：B

**解析**

> $4-x^2>0$，$|x|<2$，即 $(-2,2)$，选B。

**另一解法**：
>看到 $f(x)=\dfrac{1}{\sqrt{4-x^2}}$
>则，$4-x^2>0$，
>$-4+x^2<0$，小于0，取中间
>即 $(-2,2)$，选B。


**考点**：具体函数求定义域（根式被开方数为正）

zzzz


xxxx

**题目**

设函数 $f(x)$ 的定义域为 $[1,3]$，则函数 $f[\ln(1+x)]$ 的定义域为（　　）
?
**答案**：$[e-1,\,e^3-1]$

**解析**

> 令 $1\leq\ln(1+x)\leq3$，则 $e\leq1+x\leq e^3$，即 $e-1\leq x\leq e^3-1$。

**考点**：抽象/复合函数求定义域（由外层 $f$ 定义域反求内层 $x$ 的范围）
<!--SR:!fsrs,2026-11-18T05:56:03.327Z,8,8.2956,1,2,1,0,0,2026-11-10T05:56:03.327Z,id=ptxwbe-->

zzzz

xxxx

**题目**

已知函数 $f(x)=\begin{cases}x^2+3x, & x \geq 0 \\ 5+2x^3, & x < 0\end{cases}$，则 $f[f(-1)]=$（　　）
?
**答案**：$18$

**解析**

> $f(-1)=5+2(-1)^3=3$，$f[f(-1)]=f(3)=9+9=18$。

**考点**：分段函数嵌套求值（对应法则/复合函数，由内向外逐层代入）

zzzz

xxxx

**题目**

函数 $f(x)=\dfrac{7}{\sqrt{49-x^{2}}}+\lg(3x-6)$ 的定义域是（　　）

- A. $(-7,2)$
- B. $(2,7)$
- C. $(-7,7)$
- D. $(2,+\infty)$
?
**答案**：B

**解析**

> 由 $49-x^2>0$ 得 $-7<x<7$；由 $3x-6>0$ 得 $x>2$。取交集得定义域 $(2,7)$。

**考点**：具体函数求定义域（根式、对数各自约束后取交集）

zzzz

xxxx

**题目**

已知 $f(x)$ 的定义域为 $[1,e]$，则 $f(e^{x})$ 的定义域为（　　）

- A. $(0,1]$
- B. $[0,1]$
- C. $(0,1)$
- D. $[0,1)$
?
**答案**：B

**解析**

> 需 $1\le e^{x}\le e$，即 $0\le x\le 1$，为 $[0,1]$。

**考点**：复合函数求定义域（由外层 $f$ 定义域反求内层 $x$）

zzzz



## 值域


`````col
````col-md
flexGrow=1
===
**单调时：**
$$
\begin{align*}
&可直接把区间边界代入 \\[4pt]
&得到所求区间的边界 \\[4pt]
&若边界取不到（开区间）\\[4pt]
&就取极限\\[4pt]
&即：函数单调时\\[4pt]
&函数就没有极值点\\[4pt]
&最值就取在端点处\\[4pt]

\end{align*}
$$
````
````col-md
flexGrow=1
===
**不单调时：**
$$
\begin{align*}
&要多算一下 \\[4pt]
&极大值与极小值 \\[4pt]
\end{align*}
$$
````
`````

**例** 

$$
\begin{align*}
&\because \arctan x \text{ 在 } (0,1) \text{ 上单调} \\[4pt]
&\therefore \arctan x \text{ 的边界 } 0,1 \text{ 对应 } x \text{ 的边界 } 0,\ \tan 1 \\[4pt]
&\text{且边界取不到 } \Rightarrow x\in(0,\ \tan 1)
\end{align*}
$$


**这本质其实是求最值** 

1.  求出$f(x)$在$(a,b)$内的可疑点：
    - 驻点（导数为0的点）
    - 不可导点（导数不存在的点）
并求出这些可疑点处的函数值。
- 求出端点的函数值$f(a)$和$f(b)$ 

比较以上所求得的所有函数值：
  其中，最大者为$f(x)$在$[a,b]$上的最大值$M$，
  最小者为$f(x)$在$[a,b]$上的最小值$m$。

注：有时，这类问题也可记为“求连续函数$f(x)$在区间$[a,b]$上的值域$[m,M]$”。

（取不到端点时，对端点取极限）
- 求出$f(x)$在$(a,b)$内的可疑点$\begin{cases}驻点\\不可导点\end{cases}$，并求出这些可疑点处的函数值。
- 求出$(a,b)$两端点的单侧极限：
  若$a,b$为常数，则求$\lim\limits_{x \to a^+} f(x)$与$\lim\limits_{x \to b^-} f(x)$；
  若$\begin{cases}a为-\infty\\b为+\infty\end{cases}$，则求$\begin{cases}\lim\limits_{x \to -\infty} f(x)\\\lim\limits_{x \to +\infty} f(x)\end{cases}$。
- 比较所得结果，确定最值或取值范围。

注：
① 这类问题有时没有最大值、最小值。
② 求区间$(a,b]$或$[a,b)$内连续函数$f(x)$的最值或取值范围，只需在区间$(a,b)$内得到的结果基础上加上$f(b)$或$f(a)$的值即可。

xxxx

**题目**

函数 $f(x)=x-\sin^2 x$ 在区间 $[0,\frac{\pi}{2}]$ 上的最大值为（　　）
?
**答案**：$\dfrac{\pi}{2}-1$

**解析**

> $f'(x)=1-2\sin x\cos x=1-\sin 2x\geq0$，$f(x)$ 单调递增，最大值在右端点 $f(\frac{\pi}{2})=\frac{\pi}{2}-1$。

**考点**：闭区间上求最大值（求连续函数的值域；先判单调再代端点）

zzzz




## 对应关系

$$
\begin{align*}
&对于复合函数w(\ )=b\big[a(\ )\big]\\[4pt]
&给出w(\ )与a(\ )，求b(\ )\\[4pt]
\end{align*}
$$

`````col
````col-md
flexGrow=1
===
==法1==
$$
\begin{align*}
&由a(\ )求出a^{-1}(\ )\\[4pt]
&b(\ )=w\big[a^{-1}(\ )\big]=b\left [ a\left [ a^{-1}(\ ) \right ] \right ]  \\[4pt]
\end{align*}
$$
````
````col-md
flexGrow=1
===
==法2==
$$
\begin{align*}
&若a(\ )没有全局反函数，或a^{-1}(\ )不好求 \\[4pt]
&可用平方差，完全平方的逆运算等恒等变形\\[4pt]
&直接在w(\ )中凑出a(\ ) \\[4pt]
&使w(\ )=b\big[a(\ )\big]\\[4pt]
&\Rightarrow b() \\[4pt]
\end{align*}
$$
````
`````


$$
\begin{align*}
&对于复合函数w(\ )=c\big[b\big[a(\ )\big]\big]\\[4pt]
&给出w(\ )、a(\ )、b(\ )，求c(\ )\\[4pt]
\end{align*}
$$

`````col
````col-md
flexGrow=1
===
==法1 反函数剥离法==
$$
\begin{align*}
&若a、b均为一一对应函数，存在单值反函数\\[4pt]
&连续两次反函数代入，逐层向内剥离\\[4pt]
&先剥离第二层b，再剥离第一层a\\[4pt]
&本质：c\big(b\big(a\big(a^{-1}\big(b^{-1}(t)\big)\big)\big)\big) = c(t)\\[4pt]
\end{align*}
$$
````
````col-md
flexGrow=1
===
$$
\begin{align*}
&由b(\ )求b^{-1}(\ )，由a(\ )求a^{-1}(\ )\\[4pt]
&c(\ )=w\big[a^{-1}\big[b^{-1}(\ )\big]\big] \\[4pt]
&= c\left[ b\left[ a\left[ a^{-1}\left[ b^{-1}(\ ) \right] \right] \right] \right] \\[4pt]
\end{align*}
$$
````
`````

`````col
````col-md
flexGrow=1
===
==法2 逐层配凑法==
$$
\begin{align*}
&若内层无全局反函数，或反函数不好求 \\[4pt]
&利用恒等变形，逐层构造内层整体\\[4pt]
&先在w(\ )中凑出b(\ )的整体形式\\[4pt]
&再进一步凑出a(\ )的整体形式\\[4pt]
&\Rightarrow c(\ ) \\[4pt]
\end{align*}
$$
````
````col-md
flexGrow=1
===
$$
\begin{align*}
&将w(\ )恒等变形，逐层匹配内层结构\\[4pt]
&使w(\ )=c\big[b\big[a(\ )\big]\big]\\[4pt]
&直接还原最外层c(\ )的对应法则 \\[4pt]
\end{align*}
$$
````
`````

xxxx

**题目**

$f(x+1)=2x+3$，求 $f[f(x)-3]=$（　　）
?
**答案**：$4x-3$

**解析**

> $f(x+1)=2(x+1)+1$，故 $f(x)=2x+1$。$f(x)-3=2x-2$，$f(2x-2)=2(2x-2)+1=4x-3$。

**考点**：由复合式求函数表达式并复合求值（对应法则）

zzzz



xxxx

**题目**

若 $f(x)=\ln x$，$f[g(x)]=2x$，则 $g(x)=$（　　）
?
**答案**：$e^{2x}$

**解析**

> $f[g(x)]=\ln g(x)=2x，e^{\ln g(x)}=e^{2x}=g(x)$，故 $g(x)=e^{2x}$。

**考点**：复合函数对应关系反求内层函数（对应法则）

zzzz

## 反函数

xxxx

**题目**

已知 $f(x+1)=x^2+2$，则 $f(\cos x)=$（　　）
?
**答案**：$\cos^2 x-2\cos x+3$

**解析**

> 令 $u=x+1$，$x=u-1$，$f(u)=(u-1)^2+2=u^2-2u+3$，代入 $u=\cos x$ 即得。

**考点**：由复合式求函数表达式并代入复合（对应法则）

zzzz



xxxx

**题目**

已知 $f(x)=e^x$ 且 $f[\varphi(x)]=1+2x\,(x>0)$，则 $\varphi(x)=$（　　）
?
**答案**：$\ln(1+2x)$

**解析**

> $e^{\varphi(x)}=1+2x$，
> $\ln e^{\varphi(x)}=\ln(1+2x)=\varphi(x)$，
> 故 $\varphi(x)=\ln(1+2x)$。

**考点**：复合函数对应关系反求内层函数（对应法则）


zzzz


xxxx

**题目**

函数 $y=1+2\tan 5x\,\left(|x|<\dfrac{\pi}{10}\right)$ 的反函数是（　　）
?
`````col
````col-md
flexGrow=10
===

**答案**：$y=\dfrac{1}{5}\arctan\dfrac{x-1}{2}$

**解析**

> 由 $2\tan5x=y-1$ 得 $\tan5x=\dfrac{y-1}{2}$，$x=\dfrac{1}{5}\arctan\dfrac{y-1}{2}$，交换变量得反函数。

**另一解法**：

$$
\begin{align*}
&x = 1 + 2\tan(5y) \\[4pt]
&x - 1 = 2\tan(5y) \\[4pt]
&\frac{x-1}{2} = \tan(5y) \\[4pt]
&\arctan\left( \frac{x-1}{2} \right) = 5y \\[4pt]
&y = \frac{1}{5}\arctan\left( \frac{x-1}{2} \right)
\end{align*}
$$

**考点**：求反函数（对应法则的逆，定义域与值域互换）

````

````col-md
flexGrow=1
===





````
`````

zzzz

xxxx

**题目**

已知 $f(x)=\sqrt{x^{3}+2}$，则 $f^{-1}(2)=$（　　）
?
`````col
````col-md
flexGrow=20
===

**答案**：$\sqrt[3]{2}$

**解析**

> 令 $\sqrt{x^3+2}=2$，$x^3=2$，$x=\sqrt[3]{2}$。


**另一解法**：
$$
\begin{align*}
&x = \sqrt{y^3 + 2}\\[4pt]
&x^2 = y^3 + 2\\[4pt]
&x^2 - 2 = y^3\\[4pt]
&y = \sqrt[3]{x^2 - 2}\\[4pt]
&y(2) = \sqrt[3]{2}
\end{align*}
$$

**考点**：反函数求值（对应法则；解方程 $f(x)=2$ 即得 $f^{-1}(2)$）

````

````col-md
flexGrow=1
===





````
`````


zzzz

xxxx

**题目**

已知 $f(1+x)=\arctan x$，$f[\varphi(x)]=x-2$，则 $\varphi(x+2)=$（　　）
?
`````col
````col-md
flexGrow=20
===

**答案**：$1+\tan x$

**解析**

> $f(u)=\arctan(u-1)$。$\arctan(\varphi(x)-1)=x-2$，故 $\varphi(x)-1=\tan(x-2)$，$\varphi(x)=1+\tan(x-2)$，$\varphi(x+2)=1+\tan x$。

**另一解法**：

求解路径：$f(x) \to \varphi(x) \to \varphi(x+2)$

换元推导$f(x)$解析式：
令$1+x = t$，则$x = t-1$，代入得：
$$f(t) = \arctan(t-1)$$
将变量替换为$x$，得到：
$$f(x) = \arctan(x-1)$$

结合复合函数关系求解$\varphi(x)$：
$$
\begin{align*}
f\left[\varphi(x)\right] &= \arctan\left[\varphi(x)-1\right] = x-2 \\
\varphi(x) - 1 &= \tan(x-2) \\
\varphi(x) &= \tan(x-2) + 1
\end{align*}
$$

做变量替换$x \mapsto x+2$，得到目标式：
$$\varphi(x+2) = \tan x + 1$$


**考点**：复合函数对应关系反求内层函数（对应法则）

````

````col-md
flexGrow=1
===





````
`````

zzzz

xxxx

**题目**

已知函数 $f(x+1)=2x+1$，则 $f^{-1}(x-5)=$（　　）

- A. $2x-9$
- B. $2x-11$
- C. $\dfrac{x}{2}-3$
- D. $\dfrac{x}{2}-2$
?
`````col
````col-md
flexGrow=20
===

**答案**：D

**解析**

> $f(x+1)=2(x+1)-1$，故 $f(x)=2x-1$，$f^{-1}(x)=\dfrac{x+1}{2}$，于是 $f^{-1}(x-5)=\dfrac{x-4}{2}=\dfrac{x}{2}-2$。

**另一解法**：

变换流程：$f(x) \to f^{-1}(x) \to f^{-1}(x-5)$
换元推导：
令$x+1 = t$，则$x = t-1$
$$f(t) = 2(t-1) + 1$$
化简得到原函数：
$$f(x) = 2x - 1$$
求反函数：
令$x = 2y - 1$，解得$y = \frac{x+1}{2}$，因此
$$f^{-1}(x) = \frac{x+1}{2}$$
计算平移后的反函数：
$$
\begin{align*}
f^{-1}(x-5) &= \frac{x-5+1}{2} \\[4pt]
&= \frac{x}{2} - 2
\end{align*}
$$

**考点**：由复合式求函数表达式并求反函数（对应法则）

````

````col-md
flexGrow=1
===





````
`````

zzzz




















