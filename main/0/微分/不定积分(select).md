#flashcards/微分/不定积分




- $\cot x$：kāo，$\tan x$ 
- $\sec x$：sēi, yè, nà, x 
- $\csc x$：kāo，$\sec x$ 


# 概念


xxxx

**题目**

下列等式正确的是（　）

A. $\dfrac{d}{dx}\displaystyle\int f(x)\,dx=f(x)$

B. $d\!\left(\displaystyle\int f(x)\,dx\right)=f(x)$

C. $\dfrac{d}{dx}\displaystyle\int f'(x)\,dx=f(x)$

D. $\displaystyle\int f'(x)\,dx=f(x)$
?

````````col
```````col-md
flexGrow=20
===

**答案**：A

**解析**

> 逐项用积分—微分互逆关系判断：
>
> - A：$\left(\displaystyle\int f(x)\,dx\right)'=[F(x)+C]'=f(x)$，正确。
> - B：$d\!\left(\displaystyle\int f(x)\,dx\right)=d[F(x)+C]=f(x)\,dx$，选项右端少了微分因子 $dx$，错误。
> - C：$\left(\displaystyle\int f'(x)\,dx\right)'=[f(x)+C]'=f'(x)$，选项写成 $f(x)$，错误。
> - D：$\displaystyle\int f'(x)\,dx=f(x)+C$，选项少了任意常数 $C$，错误。
>
> 故选 A。

**考点**

积分与微分的互逆关系（微分 $dx$ 与任意常数 $C$ 的规范）
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-28T05:06:43.699Z,7,8.2956,1,2,1,0,0,2026-11-21T05:06:43.699Z,id=t2ft0j-->


zzzz



xxxx

**题目**

在 $[a,b]$ 内，$g'(x)=f'(x)$，则下列哪个正确（　）

A. $g(x)=f(x)$

B. $\left(\displaystyle\int g(x)\,dx\right)'=\left(\displaystyle\int f(x)\,dx\right)'$

C. $g(x)=f(x)-C$

D. $\displaystyle\int g(x)\,dx=\int f(x)\,dx$
?

````````col
```````col-md
flexGrow=20
===

**答案**：C

**解析**

> 由 $g'(x)=f'(x)$，得
> $$[g(x)-f(x)]'=0$$
> 故 $g(x)-f(x)$ 在区间内为常数，即 $g(x)=f(x)+C_{0}$，写成 $g(x)=f(x)-C$（$C$ 为任意常数），C 正确。
>
> - A：两函数相差一个常数，未必相等，错误。
> - B：$\left(\displaystyle\int g\,dx\right)'=g(x)$，$\left(\displaystyle\int f\,dx\right)'=f(x)$，而 $g$ 与 $f$ 未必相等，错误。
> - D：两个不定积分各自含任意常数，不能由 $g'=f'$ 直接断定其相等，错误。
>
> 故选 C。

**考点**

导数相同的两个函数相差常数（原函数之间的关系）
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-30T05:06:41.251Z,9,8.2956,1,2,1,0,0,2026-11-21T05:06:41.251Z,id=8l0bq8-->


zzzz




关系示意：$\int f(x)dx \leftarrow f(x) \rightarrow f'(x)$，

```tikz
\begin{document}
\usetikzlibrary{arrows.meta}
\begin{tikzpicture}[
    >={Stealth[length=2.2mm, width=5.2mm]},
    line cap=round, line join=round]
% f(x) -> d/dx
\draw[->, very thick] ({3.6*cos(154)},{2.7*sin(154)})
    arc(154:116:3.6 and 2.7);
% d/dx -> f'(x)
\draw[->, very thick] ({3.6*cos(64)},{2.7*sin(64)})
    arc(64:26:3.6 and 2.7);
% f'(x) -> ∫dx
\draw[->, very thick] ({3.6*cos(-26)},{2.7*sin(-26)})
    arc(-26:-64:3.6 and 2.7);
% ∫dx -> f(x)
\draw[->, very thick] ({3.6*cos(244)},{2.7*sin(244)})
    arc(244:206:3.6 and 2.7);
\node at (-3.6,0) [font=\fontsize{36}{42}\selectfont] {$f(x)$};
\node at ( 0,2.7) [font=\fontsize{36}{42}\selectfont]
    {$\displaystyle\frac{d(\;)}{dx}$};
\node at ( 3.6,0) [font=\fontsize{36}{42}\selectfont] {$f'(x)$};
\node at ( 0,-2.7)[font=\fontsize{36}{42}\selectfont]
    {$\displaystyle\int(\;)\,dx$};
\end{tikzpicture}
\end{document}
```

## 原函数与不定积分
如果一个函数$f(x)$在区间$I$上有定义，
如果存在一个可导函数$F(x)$，在区间$I$上每一点都满足$F'(x)=f(x)$成立，
就称$F(x)$为$f(x)$在区间$I$上的一个原函数。
记为：
$$\int f(x)dx = F(x) + C$$
该式叫做$f(x)$在区间$I$上的不定积分，满足：
$$F'(x)=f(x)$$
$$\left[F(x)+C\right]' = f(x)$$
其中$F(x)$为$f(x)$的一个原函数，$F(x)+C$为$f(x)$的全体原函数。

即：若$F'(x)=f(x),\ x\in I$成立，
则$\int f(x)dx$为$f(x)$的不定积分，
$\int f(x)dx$表示$f(x)$的全体原函数$F(x)+C$。


## 原函数（不定积分）的存在定理

- 连续函数$f(x)$必有原函数$F(x)$。


- 含有第一类间断点和无穷间断点的函数$f(x)$，在包含该间断点的区间内必没有原函数$F(x)$。
- 含有振荡间断点的函数$f(x)$，在包含该间断点的区间内可能有原函数$F(x)$。

若$F(x)$为可导函数，
$$
\begin{align*}

f(x)可导&\\[4pt]
&\implies f(x)必连续\\[4pt]
&\nRightarrow f'(x)必连续\\[4pt]
&\implies 若f'(x)极限存在，则f'(x)必连续\\[4pt]
&\implies f'(x)有介值性\\[4pt]
&\implies 若f'(x)\neq0，则有f'(x)恒>0或恒<0\\[4pt]
&\implies f'(x)没有第一类间断点（可去、跳跃），没有无穷间断点\\[4pt]
&\implies f'(x)可能有振荡间断点\\[4pt]

\end{align*}
$$





# 基本积分公式（10组公式）





xxxx

**题目**

求不定积分 $\displaystyle\int x\left[\sec^{2}x+\sin(2+x^{2})\right]dx$。
?

````````col
```````col-md
flexGrow=20
===

**答案**：$x\tan x+\ln|\cos x|-\dfrac{1}{2}\cos(2+x^{2})+C$

**解析**

> 拆成两个积分分别计算。
>
> 第一个用分部积分法，令 $u=x$，$dv=\sec^{2}x\,dx$，则 $du=dx$，$v=\tan x$：
> $$\int x\sec^{2}x\,dx=x\tan x-\int\tan x\,dx=x\tan x+\ln|\cos x|$$
> 第二个用凑微分法，注意 $d(2+x^{2})=2x\,dx$：
> $$\int x\sin(2+x^{2})\,dx=\frac12\int\sin(2+x^{2})\,d(2+x^{2})=-\frac12\cos(2+x^{2})$$
> 合并得
> $$x\tan x+\ln|\cos x|-\frac12\cos(2+x^{2})+C$$


**另一解法** 
$$
\begin{align*}
\text{原式} &= \int x \sec^2 x \, dx + \int x \sin(2+x^2) \, dx
\end{align*}
$$

对$\int x \sec^2 x \, dx$使用分部积分法，分部求导、积分关系如下：
$$
\begin{array}{c c c}
x &  & 1 \\
\sec^2 x &  & \tan x
\end{array}
$$

$$
\begin{align*}
\int x \sec^2 x \, dx &= x\tan x - \int \tan x \, dx \\[4pt]
&= x\tan x - \int \frac{\sin x}{\cos x} \, dx \\[4pt]
&= x\tan x + \int \frac{1}{\cos x} \, d(\cos x) \\[4pt]
&= x\tan x + \ln|\cos x| + C
\end{align*}
$$

对$\int x \sin(2+x^2) \, dx$使用凑微分法：
$$
\begin{align*}
\int x \sin(2+x^2) \, dx &= \dfrac{1}{2}\int \sin(2+x^2) \, d(x^2+2) \\[4pt]
&= -\dfrac{1}{2}\cos(x^2+2) + C
\end{align*}
$$

合并得最终结果：
$$
\begin{align*}
\text{原式} &= x\tan x + \ln|\cos x| - \dfrac{1}{2}\cos(x^2+2) + C
\end{align*}
$$






**考点**

分部积分法与凑微分法
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz




xxxx

**题目**

不定积分 $\displaystyle\int\left(\frac{3}{\sqrt{1-x^{2}}}-\sqrt{1-x}\right)dx=$
?

````````col
```````col-md
flexGrow=20
===

**答案**：$3\arcsin x+\dfrac{2}{3}(1-x)^{3/2}+C$

**解析**

> 分项积分。第一项用基本公式：
> $$3\int\frac{1}{\sqrt{1-x^{2}}}\,dx=3\arcsin x$$
> 第二项令 $u=1-x$，$du=-dx$：
> $$-\int\sqrt{1-x}\,dx=\int\sqrt{u}\,du=\frac{2}{3}u^{3/2}+C=\frac{2}{3}(1-x)^{3/2}+C$$
> 合并得
> $$3\arcsin x+\frac{2}{3}(1-x)^{3/2}+C$$

**考点**

基本积分公式与换元法
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz






xxxx

**题目**

已知 $f(x)=e^{x}$，则 $\displaystyle\int\left(\frac{f(\ln x)}{x^{2}}+1\right)dx=$（　）

A. $\ln|x|+x+C$

B. $-\ln|x|+x+C$

C. $\dfrac{1}{x}+x+C$

D. $-\dfrac{1}{x}+x+C$
?

````````col
```````col-md
flexGrow=20
===

**答案**：A

**解析**

> 由 $f(\ln x)=e^{\ln x}=x$，得
> $$\text{原式}=\int\left(\frac{x}{x^{2}}+1\right)dx=\int\left(\frac{1}{x}+1\right)dx=\ln|x|+x+C$$
> 故选 A。

**考点**

基本积分公式（对数与幂函数）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz




当$F(x)$不是一个初等函数时，
那么，有时基本的积分方法是不奏效的。


| 类别                         | 公式                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1. 幂函数                     | $\displaystyle \int x^k \mathrm{d}x = \frac{1}{k+1}x^{k+1} + C,\quad k\neq -1$<br><br>$\displaystyle \int \frac{1}{x^2}\mathrm{d}x = -\frac{1}{x} + C$<br><br>$\displaystyle \int \frac{1}{\sqrt{x}}\mathrm{d}x = 2\sqrt{x} + C$                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| 2. 对数函数                    | $\displaystyle \int \frac{1}{x}\mathrm{d}x = \ln\vert x\vert + C \quad \text{"视绝对值而不见"}$                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 3. 指数函数                    | $\displaystyle \int e^x \mathrm{d}x = e^x + C$<br><br>$\displaystyle \int a^x \mathrm{d}x = \frac{a^x}{\ln a} + C,\quad a>0,且a\neq1$                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| 4. 正弦余弦函数                  | $\displaystyle \int \sin x \mathrm{d}x = -\cos x + C$<br><br>$\displaystyle \int \cos x \mathrm{d}x = \sin x + C$                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 5. 三角函数类                   | $\displaystyle \int \tan x \, dx = -\ln\vert\cos x\vert + C$<br><br>注："用凑微分法可推"<br><br>$\displaystyle \int \cot x \, dx = \ln\vert\sin x\vert + C$<br><br>$\displaystyle \int \frac{dx}{\cos x} = \int \sec x \, dx = \ln\vert\sec x+\tan x\vert + C$<br><br>$\displaystyle \int \frac{dx}{\sin x} = \int \csc x \, dx = \ln\vert\csc x-\cot x\vert + C$<br><br>$\displaystyle \int \sec^2 x \, dx = \tan x + C$<br><br>$\displaystyle \int \csc^2 x \, dx = -\cot x + C$<br><br>$\displaystyle \int \sec x \tan x \, dx = \sec x + C$<br><br>$\displaystyle \int \csc x \cot x \, dx = -\csc x + C$                                                                                               |
| 6. 反三角函数                   | $\displaystyle \int \frac{1}{1+x^2} \, dx = \arctan x + C$<br><br>$\displaystyle \int \frac{1}{a^2+x^2} \, dx = \frac{1}{a}\arctan \frac{x}{a} + C \quad (a>0)$<br><br>推导：<br><br>$\displaystyle \int \frac{1}{a^2+x^2} dx = \frac{1}{a^2}\int \frac{1}{1+\left( \frac{x}{a} \right)^2} dx$<br><br>$\displaystyle = \frac{1}{a}\int \frac{1}{1+\left( \frac{x}{a} \right)^2} \cdot \frac{1}{a} dx$<br><br>$\displaystyle = \frac{1}{a}\int f\left[g(x)\right] g'(x) dx$<br><br>$\displaystyle = \frac{1}{a}\int f[u] du$<br><br>$\displaystyle \int \frac{1}{\sqrt{1-x^2}} \, dx = \arcsin x + C$<br><br>$\displaystyle \int \frac{1}{\sqrt{a^2-x^2}} \, dx = \arcsin \frac{x}{a} + C \quad (a>0)$ |
| 7. 含根号 $\sqrt{x^2\pm a^2}$ | $\displaystyle \int \frac{1}{\sqrt{x^2+a^2}} \, dx = \ln\left(x+\sqrt{x^2+a^2}\right) + C \quad [\text{常见} \ a=1]$<br><br>$\displaystyle \int \frac{1}{\sqrt{x^2-a^2}} \, dx = \ln\left\vert x+\sqrt{x^2-a^2}\right\vert + C \quad [\vert x\vert>\vert a\vert]$                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 8. 分母 $x^2-a^2$ 型分式        | $\displaystyle \int \frac{1}{x^2-a^2} \, dx = \frac{1}{2a}\ln\left\vert\frac{x-a}{x+a}\right\vert + C$<br><br>$\displaystyle \int \frac{1}{a^2-x^2} \, dx = \frac{1}{2a}\ln\left\vert\frac{x+a}{x-a}\right\vert + C$                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| 9. $\sqrt{a^2-x^2}$ 整体     | $\displaystyle \int \sqrt{a^2-x^2} \, dx = \frac{a^2}{2}\arcsin\frac{x}{a} + \frac{x}{2}\sqrt{a^2-x^2} + C \quad (a>\vert x\vert\geq0)$                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 10. 三角平方                   | $\displaystyle \int \sin^2x \, dx = \frac{x}{2} - \frac{\sin2x}{4} + C$<br><br>$\displaystyle \sin^2x = \frac{1-\cos2x}{2}$<br><br>$\displaystyle \int \cos^2x \, dx = \frac{x}{2} + \frac{\sin2x}{4} + C$<br><br>$\displaystyle \cos^2x = \frac{1+\cos2x}{2}$<br><br>$\displaystyle \int \tan^2x \, dx = \tan x - x + C$<br><br>$\displaystyle \tan^2x = \sec^2x - 1$<br><br>$\displaystyle \int \cot^2x \, dx = -\cot x - x + C$<br><br>$\displaystyle \cot^2x = \csc^2x - 1$                                                                                                                                                                                                                    |


# 不定积分的积分法

要用这些方法，把给的这些题目归到那10组基本积分公式上去。
# 凑微分法





xxxx

**题目**

已知函数 $f(x)=\tan x$，则 $\displaystyle\int\frac{f'(\sqrt{x})}{\sqrt{x}}\,dx=$（　）

A. $\tan\sqrt{x}+C$

B. $2\tan\sqrt{x}+C$

C. $\dfrac{1}{2}\tan\sqrt{x}+C$

D. $\dfrac{1}{4}\tan\sqrt{x}+C$
?

````````col
```````col-md
flexGrow=20
===

**答案**：B

**解析**

> 令 $u=\sqrt{x}$，则 $du=\dfrac{1}{2\sqrt{x}}dx$，即 $\dfrac{1}{\sqrt{x}}dx=2\,du$。于是
> $$\int\frac{f'(\sqrt{x})}{\sqrt{x}}\,dx=2\int f'(u)\,du=2f(u)+C=2\tan u+C=2\tan\sqrt{x}+C$$
> 故选 B。

**另一解法：** 
令 $t=\sqrt{x}$，则
$$x = t^2$$
$$dx = 2t\,dt$$
代入积分计算：
$$
\begin{align*}
\int \frac{f'(\sqrt{x})}{\sqrt{x}}dx
&= \int \frac{f'(t)\cdot 2t}{t}dt \\[6pt]
&= 2\int f'(t)dt \\[6pt]
&= 2f(t) + C \\[6pt]
&= 2\tan(\sqrt{x}) + C
\end{align*}
$$




**考点**

凑微分法（第一类换元法）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz







xxxx

**题目**

已知函数 $f(x)=2\sin x\cos x$，则 $f(x)$ 的一个原函数是（　）

A. $\dfrac{1}{2}\sin 2x$

B. $\dfrac{1}{2}\cos 2x$

C. $1-\sin^{2}x$

D. $1-\cos^{2}x$
?

````````col
```````col-md
flexGrow=20
===

**答案**：D

**解析**

> 先化简 $f(x)=2\sin x\cos x=\sin 2x$，求不定积分：
> $$\int 2\sin x\cos x\,dx=\int\sin 2x\,dx=-\frac12\cos 2x+C$$
> 由 $\cos 2x=1-2\sin^{2}x$，得 $-\dfrac12\cos 2x=\sin^{2}x-\dfrac12$，常数并入 $C$ 后一个原函数为 $\sin^{2}x$。又 $\sin^{2}x=1-\cos^{2}x$，故选 D。


**另一解法：** 
$$
\begin{align*}
&\int 2\sin x \cos x \, dx \\[4pt]
&= 2\int \sin x \, d(\sin x) \\[4pt]
&= 2\cdot \frac{1}{2}\sin^2 x + C \\[4pt]
&= \sin^2 x + C \\[4pt]
&= 1-\cos^2 x + C
\end{align*}
$$



**考点**

三角恒等变换求原函数
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz







xxxx

**题目**

已知 $f(x)=-2x$，则 $\displaystyle\int\frac{f(\tan x)}{\sin^{2}x-1}\,dx=$（　）

A. $\tan^{2}x+C$

B. $-\tan^{2}x+C$

C. $\cot^{2}x+C$

D. $-\cot^{2}x+C$
?

````````col
```````col-md
flexGrow=20
===

**答案**：A

**解析**

> 代入 $f(\tan x)=-2\tan x$，并利用 $\sin^{2}x-1=-\cos^{2}x$：
> $$\text{原式}=\int\frac{-2\tan x}{-\cos^{2}x}\,dx=2\int\frac{\tan x}{\cos^{2}x}\,dx=2\int\frac{\sin x}{\cos^{3}x}\,dx$$
> 令 $u=\cos x$，$du=-\sin x\,dx$：
> $$2\int\frac{\sin x}{\cos^{3}x}\,dx=-2\int\frac{du}{u^{3}}=\frac{1}{u^{2}}+C=\sec^{2}x+C$$
> 由于 $\sec^{2}x=\tan^{2}x+1$，常数 $1$ 并入任意常数 $C$，故结果可写为 $\tan^{2}x+C$。选 A。


**另一解法：** 
$$
\begin{align*}
\text{原式} &= \int \frac{-2 \tan x}{\sin^2 x - 1} \, dx \\[4pt]
&= \int \frac{-2 \tan x}{-\cos^2 x} \, dx \\[4pt]
&= 2 \int \frac{\tan x}{\cos^2 x} \, dx
\end{align*}
$$
这里，可以敏锐地察觉到
$$\tan'x = \sec^2 x = \frac{1}{\cos^2 x}$$
$$
\begin{align*}
&= 2 \int \tan x \cdot \tan'x \, dx \\[4pt]
&= 2 \int \tan x \, d(\tan x) \\[4pt]
&= 2 \cdot \frac{1}{2} \tan^2 x + C \\[4pt]
&= \tan^2 x + C
\end{align*}
$$




**考点**

凑微分法（常数并入任意常数）
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-29T08:27:04.870Z,8,8.2956,1,2,1,0,0,2026-11-21T08:27:04.870Z,id=rkqav9-->


zzzz









xxxx

**题目**

$\displaystyle\int\frac{x-2}{x^{2}-4x+2}\,dx=$
?

````````col
```````col-md
flexGrow=20
===

**答案**：$\dfrac{1}{2}\ln|x^{2}-4x+2|+C$

**解析**

> 观察到分母的导数为
> $$(x^{2}-4x+2)'=2x-4=2(x-2)$$
> 即 $(x-2)\,dx=\dfrac12 d(x^{2}-4x+2)$。用凑微分法：
> $$\int\frac{x-2}{x^{2}-4x+2}\,dx=\frac12\int\frac{2x-4}{x^{2}-4x+2}\,dx=\frac12\int\frac{d(x^{2}-4x+2)}{x^{2}-4x+2}$$
> $$=\frac12\ln|x^{2}-4x+2|+C$$

**考点**

凑微分法（第一类换元法）
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-12-01T08:27:10.136Z,10,8.2956,1,2,1,0,0,2026-11-21T08:27:10.136Z,id=j81jb0-->


zzzz




xxxx

**题目**

若 $f'(x-1)=2x^{2}-4x+1$，且 $f(0)=0$，则 $\displaystyle\int f(x)\,dx=$（　）

A. $2x^{2}-1+C$

B. $\dfrac{2}{3}x^{3}-x+C$

C. $\dfrac{2}{3}x^{3}-\dfrac{1}{2}x^{2}+C$

D. $\dfrac{1}{6}x^{4}-\dfrac{1}{2}x^{2}+C$
?

````````col
```````col-md
flexGrow=20
===

**答案**：D

**解析**

> 令 $t=x-1$，即 $x=t+1$，代入已知条件：
> $$f'(t)=2(t+1)^{2}-4(t+1)+1=2(t^{2}+2t+1)-4t-4+1=2t^{2}-1$$
> 故 $f'(x)=2x^{2}-1$，积分得
> $$f(x)=\int(2x^{2}-1)\,dx=\frac{2}{3}x^{3}-x+C_{1}$$
> 由 $f(0)=0$ 得 $C_{1}=0$，即 $f(x)=\dfrac{2}{3}x^{3}-x$。再对 $f(x)$ 求不定积分：
> $$\int f(x)\,dx=\int\left(\frac{2}{3}x^{3}-x\right)dx=\frac{2}{3}\cdot\frac{x^{4}}{4}-\frac{x^{2}}{2}+C=\frac{1}{6}x^{4}-\frac{1}{2}x^{2}+C$$
> 故选 D。




**另一解法** 

$$f'(x) = 2(x+1)^2 - 4(x+1) + 1$$
$$
\begin{align*}
\int f'(x)\,\mathrm{d}x &= \int 2(x+1)^2\,\mathrm{d}(x+1) - \int 4(x+1)\,\mathrm{d}(x+1) + \int 1\,\mathrm{d}(x+1) \\
&= \frac{2}{3}(x+1)^3 - 2(x+1)^2 + (x+1) + C
\end{align*}
$$
**另一解法** 
$$
\begin{align*}
f'(x) &= 2(x+1)^2 - 4(x+1) + 1 \\
&= 2x^2 - 1
\end{align*}
$$
$$
\begin{align*}
f(x) = \int f'(x)\,\mathrm{d}x &= \int (2x^2 - 1)\,\mathrm{d}x \\
&= \frac{2}{3}x^3 - x + C
\end{align*}
$$
代入$x=0$，由$f(0)=0$得$C=0$，因此：
$$f(x) = \frac{2}{3}x^3 - x$$ 
$$
\begin{align*}
\int f(x)\,\mathrm{d}x &= \int \left( \frac{2}{3}x^3 - x \right)\mathrm{d}x \\
&= \frac{1}{6}x^4 - \frac{1}{2}x^2 + C
\end{align*}
$$







**考点**

由导数关系先求函数再计算不定积分
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-29T06:07:19.158Z,8,8.2956,1,2,1,0,0,2026-11-21T06:07:19.158Z,id=01oi03-->


zzzz








凑微分法的推导过程如下：

`````col
````col-md
flexGrow=1
===

$$
\begin{align*}
\because \quad &\int g(x)dx = G(x)+C \\[4pt]
\therefore \quad &g(x) = \frac{d\left ( G(x)+C \right ) }{dx}  \\[4pt]
&g(x)dx = d\left ( G(x)+C \right )  \\[4pt]
\because \quad &d\left ( G(x)+C \right )=dG(x) \\[4pt]
\therefore \quad &g(x)dx = dG(x) \\[4pt]
即&\\[4pt]
\Rightarrow 若&\int g(x)dx = G(x)+C\\[4pt]
则&g(x)dx = d\left ( G(x)+C \right )  \\[4pt]
&g(x)dx = dG(x) \\[4pt]
\end{align*}
$$

````

````col-md
flexGrow=1.6
===

$$
\begin{align*}
h(x)& =f\left[g(x)\right]g'(x)  \\[4pt]
\int h(x)\mathrm{d}x &= \int f\left[g(x)\right]g'(x)\mathrm{d}x  \\[4pt]
&= \int f\left[g(x)\right]\mathrm{d}\left[g(x)\right]  \\[4pt]
&令  g(x)=u  \\[4pt]
&= \int f(u)\mathrm{d}u \\[4pt]
&= F(u)+C \\[4pt]
回代u=g(x)并验证：& \\[4pt]
&= F\left [ g(x) \right ] +C \\[4pt]
&=\int h(x)\mathrm{d}x  \\[4pt]
\end{align*}
$$



````
`````

注：当被积函数比较复杂时，拿出一部分放到$d$后面去，若能凑成$\int f(u)\mathrm{d}u$的形式则凑微分成功。
eg：
$$
\begin{align*}
\int \frac{\ln^5 x}{x}\mathrm{d}x &= \int \ln^5 x \cdot \frac{1}{x}\mathrm{d}x \\
&= \int \ln^5 x \mathrm{d}\ln x = \int (\ln x)^5 \mathrm{d}\ln x \\
&= \frac{\ln^6 x}{6} + C
\end{align*}
$$

## 常用的凑微分公式

| 类别        | 凑微分                                                                                                                                                                                                                                                                                                                         | 换元积分                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| --------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **幂函数**   | $\displaystyle x\mathrm{d}x = \frac{1}{2}\mathrm{d}(x^2)$<br><br>$\displaystyle \sqrt{x}\mathrm{d}x = \frac{2}{3}\mathrm{d}\left(x^{\frac{3}{2}}\right)$<br><br>$\displaystyle \frac{1}{\sqrt{x}}\mathrm{d}x = 2\mathrm{d}(\sqrt{x})$<br><br>$\displaystyle \frac{1}{x^2}\mathrm{d}x = \mathrm{d}\left(-\frac{1}{x}\right)$ | $\displaystyle \int x f(x^2)\mathrm{d}x = \frac{1}{2}\int f(x^2)\mathrm{d}(x^2) = \frac{1}{2}\int f(u)\mathrm{d}u$<br><br>$\displaystyle \int \sqrt{x} f\left(x^{\frac{3}{2}}\right)\mathrm{d}x = \frac{2}{3}\int f\left(x^{\frac{3}{2}}\right)\mathrm{d}\left(x^{\frac{3}{2}}\right)$<br><br>$\displaystyle \int \frac{f(\sqrt{x})}{\sqrt{x}}\mathrm{d}x = 2\int f(\sqrt{x})\mathrm{d}(\sqrt{x})$<br><br>$\displaystyle \int \frac{f\left(-\frac{1}{x}\right)}{x^2}\mathrm{d}x = \int f\left(-\frac{1}{x}\right)\mathrm{d}\left(-\frac{1}{x}\right)$ |
| **对数函数**  | 当$x>0$时，$\displaystyle \frac{1}{x}\mathrm{d}x = \mathrm{d}(\ln x)$                                                                                                                                                                                                                                                          | $\displaystyle \int \frac{f(\ln x)}{x}\mathrm{d}x = \int f(\ln x)\mathrm{d}(\ln x)$                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **指数函数**  | $\displaystyle e^x\mathrm{d}x = \mathrm{d}(e^x)$<br><br>$\displaystyle a^x\mathrm{d}x = \frac{1}{\ln a}\mathrm{d}(a^x),\ a>0,a\neq1$                                                                                                                                                                                        | $\displaystyle \int e^x f(e^x)\mathrm{d}x = \int f(e^x)\mathrm{d}(e^x)$<br><br>$\displaystyle \int a^x f(a^x)\mathrm{d}x = \frac{1}{\ln a}\int f(a^x)\mathrm{d}(a^x)$                                                                                                                                                                                                                                                                                                                                                                                 |
| **三角函数**  | $\displaystyle \sin x\mathrm{d}x = \mathrm{d}(-\cos x)$<br><br>$\displaystyle \cos x\mathrm{d}x = \mathrm{d}(\sin x)$<br><br>$\displaystyle \frac{1}{\cos^2 x}dx = \sec^2 x dx = d(\tan x)$<br><br>$\displaystyle \frac{1}{\sin^2 x}dx = \csc^2 x dx = d(-\cot x)$                                                          | $\displaystyle \int \sin x f(-\cos x)\mathrm{d}x = \int f(-\cos x)\mathrm{d}(-\cos x)$<br><br>$\displaystyle \int \cos x f(\sin x)\mathrm{d}x = \int f(\sin x)\mathrm{d}(\sin x)$<br><br>$\displaystyle \int \frac{f(\tan x)}{\cos^2 x}dx = \int f(\tan x)d(\tan x)$<br><br>$\displaystyle \int \frac{f(-\cot x)}{\sin^2 x}dx = \int f(-\cot x)d(-\cot x)$                                                                                                                                                                                            |
| **反三角函数** | $\displaystyle \frac{1}{1+x^2}dx = d(\arctan x)$<br><br>$\displaystyle \frac{1}{\sqrt{1-x^2}}dx = d(\arcsin x)$                                                                                                                                                                                                             | $\displaystyle \int \frac{f(\arctan x)}{1+x^2}dx = \int f(\arctan x)d(\arctan x)$<br><br>$\displaystyle \int \frac{f(\arcsin x)}{\sqrt{1-x^2}}dx = \int f(\arcsin x)d(\arcsin x)$                                                                                                                                                                                                                                                                                                                                                                     |


# 换元法（凑微分法反过来）



xxxx

**题目**

不定积分 $\displaystyle\int\frac{1}{e^{3x}+e^{-3x}}\,dx=$
?

````````col
```````col-md
flexGrow=20
===

**答案**：$\dfrac{1}{3}\arctan e^{3x}+C$

**解析**

> 分子分母同乘 $e^{3x}$：
> $$\frac{1}{e^{3x}+e^{-3x}}=\frac{e^{3x}}{e^{6x}+1}$$
> 令 $u=e^{3x}$，则 $du=3e^{3x}dx$，即 $e^{3x}dx=\dfrac13 du$：
> $$\int\frac{e^{3x}}{e^{6x}+1}\,dx=\frac13\int\frac{1}{u^{2}+1}\,du=\frac13\arctan u+C=\frac13\arctan e^{3x}+C$$

**另一解法：** 
设 $e^{3x}=t$，则：
$$
e^{-3x} = t^{-1}
$$
$$
3x = \ln t
$$
$$
x = \frac{\ln t}{3}
$$
$$
dx = \frac{1}{3t} dt
$$

$$
\begin{align*}
\text{原式} &= \int \frac{1}{t + t^{-1}} \cdot \frac{1}{3t} \, dt \\[6pt]
&= \frac{1}{3}\int \frac{1}{t^2 + 1} \, dt \\[6pt]
&= \frac{1}{3}\arctan t + C
\end{align*}
$$

代回 $e^{3x}=t$，得：
$$
\text{原式} = \frac{1}{3}\arctan\left(e^{3x}\right) + C
$$




**考点**

凑微分法（结合恒等变形）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz









换元法推导步骤：
$$
\begin{align*}
h(x)& =f\left[g(x)\right]g'(x)  \\[4pt]
&令 \ x=g(u)\\[4pt]
\int f(x) \, \mathrm{d}x &= \int f[g(u)] \, \mathrm{d}[g(u)]  \\[4pt]
&= \int f[g(u)] g'(u) \, \mathrm{d}u \\[4pt]
&令 \ f[g(u)]g'(u) = h(u) \\[4pt]
&= \int h(u) \, \mathrm{d}u  \\[4pt]
&= H(u) + C \\[4pt]
回代，令u=g^{-1}(x)&并验证：\\[4pt]

&= H\left[g^{-1}(x)\right] + C \\[4pt]
&= \int f(x) \, \mathrm{d}x  \\[4pt]
\end{align*}

$$

**理解：** 
当遇到$f(x)$比较复杂时（有根号或分母复杂），
$\displaystyle e.g. f(x)=\sqrt{e^x+1}、\sqrt{\frac{2x+1}{x+1}}、\frac{1}{\sqrt{e^{2x}+1}}$
引入新的自变量$u$，让其变为简单的$h(u)$（无根号或分母简单）。

当被积函数不容易积分（比如含有根式或反三角函数）时，可以通过换元的方法从$d$后面拿出一部分放到前面来，就成为
$$\int f[g(u)]g'(u)du$$ 
的形式，若$f[g(u)]g'(u)$容易积分，则换元成功。
$x=g(u)$必须是单调可导函数（满足单调才能有反函数），且不要忘记，计算结束后用反函数$u=g^{-1}(x)$回代。

## 三角函数代换




xxxx

**题目**

计算 $\displaystyle\int\frac{1}{(x^{2}+x^{4})\sqrt{1+x^{2}}}\,dx$。
?

````````col
```````col-md
flexGrow=20
===

**答案**：$-\dfrac{\sqrt{1+x^{2}}}{x}-\dfrac{x}{\sqrt{1+x^{2}}}+C$

**解析**

> 被积函数含 $\sqrt{1+x^{2}}$，作三角代换，令 $x=\tan t$，则 $dx=\sec^{2}t\,dt$，$\sqrt{1+x^{2}}=\sec t$，且
> $$x^{2}+x^{4}=\tan^{2}t(1+\tan^{2}t)=\tan^{2}t\sec^{2}t$$
> 于是
> $$\text{原式}=\int\frac{\sec^{2}t}{\tan^{2}t\sec^{2}t\cdot\sec t}\,dt=\int\frac{1}{\tan^{2}t\sec t}\,dt=\int\frac{\cos^{3}t}{\sin^{2}t}\,dt$$
> 注意 $\cos t\,dt=d(\sin t)$，且 $\cos^{2}t=1-\sin^{2}t$，令 $u=\sin t$：
> $$\int\frac{\cos^{3}t}{\sin^{2}t}\,dt=\int\frac{1-\sin^{2}t}{\sin^{2}t}\,d(\sin t)=\int\left(\frac{1}{u^{2}}-1\right)du=-\frac{1}{u}-u+C$$
> 由 $\tan t=x$ 有 $\sin t=\dfrac{x}{\sqrt{1+x^{2}}}$，回代得
> $$-\frac{\sqrt{1+x^{2}}}{x}-\frac{x}{\sqrt{1+x^{2}}}+C$$


**另一解法** 
求解不定积分$\displaystyle \int \frac{1}{(x^2+x^4)\sqrt{1+x^2}} \, dx$，看到$\sqrt{1+x^2}$，令$x=\tan t$，推导过程如下：
$$
\begin{align*}
\text{原式} &= \int \frac{1}{(\tan^2 t + \tan^4 t)\cdot \sqrt{1+\tan^2 t}} \, d(\tan t) \\[4pt]
&= \int \frac{1}{\tan^2 t(1+\tan^2 t)\cdot \sec t} \, d(\tan t) \\[4pt]
&= \int \frac{\sec^2 t}{\tan^2 t \cdot \sec^2 t \cdot \sec t} \, dt \\[4pt]
&= \int \frac{1}{\tan^2 t \cdot \sec t} \, dt \\[4pt]
&= \int \frac{\cos^3 t}{\sin^2 t} \, dt \\[4pt]
&= \int \frac{\cos^2 t}{\sin^2 t} \, d(\sin t) \\[4pt]
&= \int \frac{1-\sin^2 t}{\sin^2 t} \, d(\sin t) \\[4pt]
&= \int \left( \frac{1}{\sin^2 t} - 1 \right) d(\sin t) \\[4pt]
&= \int \frac{1}{\sin^2 t} d(\sin t) - \int 1 \, d(\sin t) \\[4pt]
&= -\frac{1}{\sin t} - \sin t + C
\end{align*}
$$
代回$x=\tan t$：
由$\displaystyle \tan t =x= \frac{对}{临} =\frac{x}{1}$
可得斜边长为$\sqrt{1+x^2}$，
因此$\displaystyle \sin t = \frac{对}{斜}= \frac{x}{\sqrt{1+x^2}}$，

$$
\text{原式} = -\frac{\sqrt{1+x^2}}{x} - \frac{x}{\sqrt{1+x^2}} + C
$$







**考点**

三角代换（第二类换元法）
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-12-01T08:26:57.917Z,10,8.2956,1,2,1,0,0,2026-11-21T08:26:57.917Z,id=7hxoao-->


zzzz




当被积函数含有如下根式时，可作三角函数代换，这里$a>0$：

`````col
````col-md
flexGrow=1
===

- 对于根式$\sqrt{a^2-x^2}$：令$x=a\sin t$，
- 其中$|t|<\frac{\pi}{2}$，（因为在这个区间函数单调）

````

````col-md
flexGrow=1
===

```tikz
\begin{document}

\begin{tikzpicture}[scale=1.1]
\draw[->] (-2.3,0) -- (2.3,0) node[right] {$t$};
\draw[->] (0,-1.6) -- (0,1.6) node[above] {$x$};
\draw[thick,blue,domain=-1.55:1.55,samples=100] plot (\x,{sin(\x r)});
\fill (0,0) circle[radius=1.5pt];
\fill (-1.57,-1) circle[radius=1.5pt];
\fill (1.57,1) circle[radius=1.5pt];
\node[font=\tiny,below left] at (-1.57,0) {$-\frac{\pi}{2}$};
\node[font=\tiny,below right] at (1.57,0) {$\frac{\pi}{2}$};
\node[font=\tiny,left] at (0,1) {$a$};
\node[font=\tiny,left] at (0,-1) {$-a$};
\node[blue,above right,font=\small] at (0.6,0.5) {$x=a\sin t$};
\end{tikzpicture}
\end{document}
```



````
`````

`````col
````col-md
flexGrow=1
===

- 对于根式$\sqrt{a^2+x^2}$：令$x=a\tan t$，
- 其中$|t|<\frac{\pi}{2}$，

````

````col-md
flexGrow=1
===

```tikz
\begin{document}
\begin{tikzpicture}[scale=1.1]
\clip (-2.3,-2.2) rectangle (2.3,2.4);
\draw[->] (-2.3,0) -- (2.3,0) node[right] {$t$};
\draw[->] (0,-2.2) -- (0,2.4) node[above] {$x$};
\draw[dashed,gray] (-1.57,-2.2) -- (-1.57,2.4);
\draw[dashed,gray] (1.57,-2.2) -- (1.57,2.4);
\draw[thick,blue,domain=-1.2:1.2,samples=100] plot (\x,{tan(\x r)});
\fill (0,0) circle[radius=1.5pt];
\node[font=\tiny,below left] at (-1.57,0) {$-\frac{\pi}{2}$};
\node[font=\tiny,below right] at (1.57,0) {$\frac{\pi}{2}$};
\node[blue,above right,font=\small] at (0.4,1.2) {$x=a\tan t$};
\end{tikzpicture}
\end{document}
```



````
`````

`````col
````col-md
flexGrow=1
===

- 对于根式$\sqrt{x^2-a^2}$：令$x=a\sec t$，
- $t$的取值范围为
  $$
  \begin{cases}
  若x>0,则0<t<\frac{\pi}{2} \\
  若x<0,则\frac{\pi}{2}<t<\pi
  \end{cases}
  $$

````

````col-md
flexGrow=1
===

```tikz
\begin{document}
\begin{tikzpicture}[scale=1.1]
\clip (-0.5,-2.6) rectangle (3.9,2.8);
\draw[->] (-0.5,0) -- (3.9,0) node[right] {$t$};
\draw[->] (0,-2.6) -- (0,2.8) node[above] {$x$};
\draw[dashed,gray] (1.57,-2.6) -- (1.57,2.8);
\draw[thick,blue,domain=0:1.2,samples=100] plot (\x,{1/cos(\x r)});
\draw[thick,blue,domain=1.95:3.14,samples=100] plot (\x,{1/cos(\x r)});
\fill (0,1) circle[radius=1.5pt];
\fill (3.14,-1) circle[radius=1.5pt];
\node[font=\tiny,below left] at (0,0) {$0$};
\node[font=\tiny,below left] at (1.57,0) {$\frac{\pi}{2}$};
\node[font=\tiny,below right] at (3.14,0) {$\pi$};
\node[font=\tiny,left] at (0,1) {$a$};
\node[font=\tiny,left] at (0,-1) {$-a$};
\node[blue,above right,font=\small] at (0.2,1.5) {$x=a\sec t$};
\end{tikzpicture}
\end{document}
```



````
`````

# 恒等变形后作三角函数代换
当被积函数含有根式$\sqrt{ax^2+bx+c}$时，可先通过配方恒等变形为以下三种形式之一，再作三角函数代换求解积分：
$$\sqrt{\varphi^2(x)+k^2},\quad \sqrt{\varphi^2(x)-k^2},\quad \sqrt{k^2-\varphi^2(x)}$$

## 根式代换（举重若轻）



xxxx

**题目**

求不定积分 $\displaystyle\int\frac{e^{x}}{1+\sqrt{2e^{x}+1}}\,dx$。
?

````````col
```````col-md
flexGrow=20
===

**答案**：$\sqrt{2e^{x}+1}-\ln\big(1+\sqrt{2e^{x}+1}\big)+C$

**解析**

> 令 $t=\sqrt{2e^{x}+1}$，则 $t^{2}=2e^{x}+1$，即 $e^{x}=\dfrac{t^{2}-1}{2}$。两边微分得 $2t\,dt=2e^{x}dx$，即 $e^{x}dx=t\,dt$。于是
> $$\text{原式}=\int\frac{t}{1+t}\,dt=\int\left(1-\frac{1}{1+t}\right)dt=t-\ln|1+t|+C$$
> 回代 $t=\sqrt{2e^{x}+1}$：
> $$\sqrt{2e^{x}+1}-\ln\big(1+\sqrt{2e^{x}+1}\big)+C$$


**另一解法** 
对于含$\sqrt{2e^x+1}$的不定积分，该根式不适合三角代换，直接处理较为困难，
直接设 $t = \sqrt{2e^x + 1}$，
$$e^x = \frac{t^2 - 1}{2}$$
$$x = \ln\left( \frac{t^2 - 1}{2} \right)$$
$$
\begin{align*}
dx &= d\left[ \ln\left( \frac{t^2 - 1}{2} \right) \right] \\[4pt]
&= \frac{2t}{t^2 - 1} \, dt
\end{align*}
$$

$$
\begin{align*}
\text{原式} &= \int \frac{\frac{t^2 - 1}{2}}{1 + t} \cdot \frac{2t}{t^2 - 1} \, dt \\[4pt]
&= \int \frac{t}{1 + t} \, dt \\[4pt]
&= \int \frac{t + 1 - 1}{t + 1} \, dt \\[4pt]
&= \int 1 \, dt - \int \frac{1}{t + 1} \, d(t+1) \\[4pt]
&= t - \ln|t + 1| + C
\end{align*}
$$
回代$t = \sqrt{2e^x + 1}$，
$$\text{原式} = \sqrt{2e^x + 1} - \ln\left(1 + \sqrt{2e^x + 1}\right) + C$$





**考点**

根式代换（第二类换元法）
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-12-02T03:02:46.609Z,10,8.2956,1,2,1,0,0,2026-11-22T03:02:46.609Z,id=908u4t-->


zzzz



当被积函数含有根式

$\displaystyle \sqrt[n]{ax+b}，\sqrt{\frac{ax+b}{cx+d}}，\sqrt{ae^{bx}+c}$时

（因为很难通过根号内换元的办法凑出平方，就没法用三角函数代换等方法把根号去掉）
直接令根式为$t$，e.g. 令$\sqrt[n]{ax+b}=t$

若表达式里既含有$\sqrt[n]{ax+b}$，也含有$\sqrt[m]{ax+b}$的函数，
则取$m,n$的最小公倍数$k$
令$\sqrt[k]{ax+b}=t$

##  倒代换
当被积函数分母的幂次比分子高两次及两次以上时，作倒代换，令$x=\frac{1}{t}$

##  复杂函数直接代换
当被积函数中含有$a^x$，$e^x$，$\ln x$，$\arcsin x$，$\arctan x$时
直接令复杂函数等于$t$

若$\ln x$，$\arcsin x$，$\arctan x$与$P_n(x)$或$\displaystyle e^{ax}$作乘法时，优先考虑分部积分法

$P_n(x)$为$x$的$n$次多项式


# 分部积分法


xxxx

**题目**

$f(x)$ 的一个原函数为 $x\arcsin x$，则 $\displaystyle\int xf'(x)\,dx=$（　）

A. $x\arcsin x+C$

B. $\dfrac{x^{2}}{\sqrt{1-x^{2}}}+C$

C. $\dfrac{x}{\sqrt{1-x^{2}}}+\arcsin x+C$

D. $\dfrac{x^{2}}{\sqrt{1-x^{2}}}-x\arcsin x+C$
?

````````col
```````col-md
flexGrow=20
===

**答案**：B

**解析**

> 由 $x\arcsin x$ 是 $f(x)$ 的一个原函数，对其求导得
> $$f(x)=(x\arcsin x)'=\arcsin x+\frac{x}{\sqrt{1-x^{2}}}$$
> 对目标积分用分部积分法，令 $u=x$，$dv=f'(x)\,dx$，则 $du=dx$，$v=f(x)$：
> $$\int xf'(x)\,dx=xf(x)-\int f(x)\,dx$$
> 又因为 $\displaystyle\int f(x)\,dx=x\arcsin x+C$，代入得
> $$xf(x)-x\arcsin x+C=x\left(\arcsin x+\frac{x}{\sqrt{1-x^{2}}}\right)-x\arcsin x+C=\frac{x^{2}}{\sqrt{1-x^{2}}}+C$$
> 故选 B。

**考点**

分部积分法（结合原函数概念）
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-28T06:07:08.021Z,7,8.2956,1,2,1,0,0,2026-11-21T06:07:08.021Z,id=xhfwt4-->


zzzz



（$u,v$一般是不同类型的函数）
$$\int u\mathrm{d}v = uv - \int v\mathrm{d}u$$

$$
\begin{align*}
推导:& \\[4pt]
&(uv)' = u'v + uv'\\[4pt]
两边对x积分：& \\[4pt]
&\int (uv)'\mathrm{d}x = \int u'v\mathrm{d}x + \int uv'\mathrm{d}x \\[4pt]
&\frac{\mathrm{d}(\quad)}{\mathrm{d}x}与\int (\quad)\mathrm{d}x互为逆运算，因此：& \\[4pt]
&uv = \int v\mathrm{d}u + \int u\mathrm{d}v \\[4pt]
移项得:& \\[4pt]
&\implies \int u\mathrm{d}v = uv - \int v\mathrm{d}u \\[4pt]
\end{align*}
$$

这个方法主要适用于求$\displaystyle \int u\mathrm{d}v$比较难，而$\displaystyle \int v\mathrm{d}u$比较简单的情形。

### 注1：
$$
\begin{align*}
&v' = \frac{\mathrm{d}v}{\mathrm{d}x} = \frac{\mathrm{d}(v+c)}{\mathrm{d}x}\\[4pt]
\int uv'\mathrm{d}x &= \int u\mathrm{d}v  \\[4pt]
&= \int u\mathrm{d}(v+c) \\[4pt]
\end{align*}
$$

### 注2：
$[P_n(x)\text{为}x\text{的}n\text{次多项式}]$ 
积分后会“简单”些的函数宜取作$v$，微分后会“简单”些的函数宜取作$u$。

按**反、对、幂、指、三**的顺序选取$u,v$，对应代表函数依次为

$$\displaystyle
\begin{array}{c}
\arcsin x\quad \ln x\quad x^{2}\quad e^{x}\quad \sin x \\[4pt]
\xleftarrow{\quad U\quad 越易求导\quad}
反\quad对\quad幂\quad指\quad三
\xrightarrow{\quad V\quad 越易积分\quad}
\end{array}$$
分部积分转化关系：
$$
\begin{align*}
\int u\mathrm{d}v &=uv - \int v\mathrm{d}u\\[4pt]
& =uv - \int vu'\mathrm{d}x\\[4pt]
\end{align*}
$$
排在顺序左侧的函数宜选作$u$，用来求导；排在顺序右侧的函数宜选作$v$，用来积分。
- 当被积函数为$P_n(x)e^{kx}$、$P_n(x)\sin ax$、$P_n(x)\cos ax$等形式时，选取$u=P_n(x)$；
- 当被积函数为$e^{ax}\sin bx$、$e^{ax}\cos bx$等形式时，$u$选哪一个都行。


**eg:** 
当被积函数为$P_n(x)\ln x$，$P_n(x)\arcsin x$，$P_n(x)\arctan x$等形式时：
选$u=\ln x$，$u=\arcsin x$，$u=\arctan x$。

例：计算$\int \ln(1+x^2)\,\mathrm{d}x$
$$
\begin{aligned}
\int \ln(1+x^2)\,\mathrm{d}x &= \int \ln(1+x^2)\cdot 1\,\mathrm{d}x \\
&= \int \ln(1+x^2)\cdot (x)'\,\mathrm{d}x \\
&= x\ln(1+x^2) - \int x\,\mathrm{d}\left[\ln(1+x^2)\right] \\
&= x\ln(1+x^2) - \int x\cdot \frac{2x}{1+x^2}\,\mathrm{d}x \\
&= x\ln(1+x^2) - 2\int \frac{x^2}{1+x^2}\,\mathrm{d}x \\
&= x\ln(1+x^2) - 2\int \frac{x^2+1-1}{1+x^2}\,\mathrm{d}x \\
&= x\ln(1+x^2) - 2\left(\int \mathrm{d}x - \int \frac{1}{1+x^2}\,\mathrm{d}x\right) \\
&= x\ln(1+x^2) - 2x + 2\arctan x + C
\end{aligned}
$$


## 表格法 




xxxx

**题目**

求不定积分 $\displaystyle\int(x+2024)\ln x\,dx$。
?

````````col
```````col-md
flexGrow=20
===

**答案**：$\left(\dfrac{1}{2}x^{2}+2024x\right)\ln x-\dfrac{1}{4}x^{2}-2024x+C$

**解析**

> 用分部积分法，令 $u=\ln x$，$dv=(x+2024)\,dx$，则 $du=\dfrac{1}{x}dx$，$v=\dfrac{x^{2}}{2}+2024x$：
> $$\int(x+2024)\ln x\,dx=\left(\frac{x^{2}}{2}+2024x\right)\ln x-\int\left(\frac{x^{2}}{2}+2024x\right)\frac{1}{x}\,dx$$
> $$=\left(\frac{x^{2}}{2}+2024x\right)\ln x-\int\left(\frac{x}{2}+2024\right)dx$$
> $$=\left(\frac{x^{2}}{2}+2024x\right)\ln x-\frac{x^{2}}{4}-2024x+C$$


**另一解法：** 
使用分部积分法（竖式列表法）计算不定积分，选取$u=\ln x$，$dv=(x+2024)dx$：
对$u$求导得$u'=\frac{1}{x}$，对应符号$+$；对$dv$积分得$v=\frac{1}{2}x^2+2024x$，对应符号$-$。

$$
\begin{align*}
\text{原式}&=\left(\frac{1}{2}x^2+2024x\right)\ln x - \int \frac{\frac{1}{2}x^2+2024x}{x}\,dx + C\\[6pt]
&=\left(\frac{1}{2}x^2+2024x\right)\ln x - \int \left(\frac{1}{2}x + 2024\right)dx + C\\[6pt]
&=\left(\frac{1}{2}x^2+2024x\right)\ln x - \frac{1}{4}x^2 - 2024x + C
\end{align*}
$$





**考点**

分部积分法
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz




计算$\displaystyle \int x^3 e^x\,\mathrm{d}x$ 要用多次分部积分，很麻烦

该方法适用于计算$\displaystyle \int P_n(x)e^{kx}\mathrm{d}x$、$\displaystyle \int P_n(x)\sin ax \mathrm{d}x$、$\displaystyle \int P_n(x)\cos bx \mathrm{d}x$类型的不定积分，
其中$\displaystyle P_n(x)$为$n$次多项式。

计算$\displaystyle \int uv^{(4)}\mathrm{d}x$ 可通过表格快速计算，表格结构如下：


```tikz


\begin{document}

\begin{tikzpicture}[
  lab/.style={font=\Large},
  arr/.style={<->, thin}
]
  % 网格（foreach 整数计数：6 列 x=0..10.8；2 行 y=0,1.8,3.6）
  \foreach \i in {0,1,...,6}      {\draw[thin] (\i*1.8,0) -- (\i*1.8,3.6);}
  \foreach \y in {0,1.8,3.6}      {\draw[thin] (0,\y) -- (10.8,\y);}
  % 第 1 列：行标签（被表格包含）
  \node[lab] at (0.9,2.7) {$\displaystyle \frac{du}{dx}$};
  \node[lab] at (0.9,0.9) {$\displaystyle \int v^{(4)} \,dx$};
  % 上排文字（第 2-6 列，中心 y=2.7）
  \node[lab] at (2.7,2.7) {$u$};
  \node[lab] at (4.5,2.7) {$u'$};
  \node[lab] at (6.3,2.7) {$u''$};
  \node[lab] at (8.1,2.7) {$u^{(3)}$};
  \node[lab] at (9.9,2.7) {$u^{(4)}$};
  % 下排文字（中心 y=0.9）
  \node[lab] at (2.7,0.9) {$v^{(4)}$};
  \node[lab] at (4.5,0.9) {$v^{(3)}$};
  \node[lab] at (6.3,0.9) {$v''$};
  \node[lab] at (8.1,0.9) {$v'$};
  \node[lab] at (9.9,0.9) {$v$};
  % 斜向错位箭头：u→v⁽³⁾, u'→v'', u''→v', u⁽³⁾→v（跨列线 3.6,5.4,7.2,9.0；行标签列与 u 列之间无箭头）
  \draw[arr] (3.05,2.05) -- (4.15,1.55);
  \draw[arr] (4.85,2.05) -- (5.95,1.55);
  \draw[arr] (6.65,2.05) -- (7.75,1.55);
  \draw[arr] (8.45,2.05) -- (9.55,1.55);
  % 第 6 列竖向箭头（u⁽⁴⁾↔v，跨中横线）
  \draw[arr] (9.9,2.05) -- (9.9,1.55);
  % 符号：列线与中横线交点右上方，⊕⊖⊕⊖⊕ 相间
  \node[lab] at (3.78,2.10) {$\oplus$};
  \node[lab] at (5.58,2.10) {$\ominus$};
  \node[lab] at (7.38,2.10) {$\oplus$};
  \node[lab] at (9.18,2.10) {$\ominus$};
  \node[lab] at (10.20,2.10) {$\oplus$};
\end{tikzpicture}



\end{document}
```

$$
\int uv^{(4)}\mathrm{d}x = uv^{(3)} - u'v'' + u''v' -u^{(3)}v + \int u^{(4)}v\mathrm{d}x
$$

计算规则：以$u$作为起点，按左上、右下错位相乘，各项符号“+”“-”交替出现，

最后剩余项为$\displaystyle \int u^{(4)}v\mathrm{d}x$。多项式求导多次后可导为 $0$，若$\displaystyle u^{(4)}=0$ 

则剩余积分项$\displaystyle \displaystyle \int u^{(4)}v\mathrm{d}x=\int 0\cdot v\mathrm{d}x=0$ 自动消失，结果就是有限项和，无需反复套分部积分。

## 循环型分部积分


计算$\displaystyle \int  \sin  (\arctan x)\,\mathrm{d}e^{ \arctan x}，令t = \arctan x，原式=\displaystyle\int  \sin  t\,\mathrm{d}e^{t}$，
使用分部积分法计算时发现，对该积分无论使用多少次分部积分，结果始终是两个不同类型函数乘积的形式。

```tikz


\begin{document}

\begin{tikzpicture}[
  lab/.style={font=\Large},
  arr/.style={<->, thin}
]
  % 网格（foreach 整数计数：4 列列宽 2.0 x=0,2,...,8；2 行 y=0,1.8,3.6）
  \foreach \i in {0,1,...,4}      {\draw[thin] (\i*2.0,0) -- (\i*2.0,3.6);}
  \foreach \y in {0,1.8,3.6}      {\draw[thin] (0,\y) -- (8.0,\y);}
  % 第 1 列：行标签（被表格包含）
  \node[lab] at (1.0,2.7) {$\displaystyle \frac{du}{dt}$};
  \node[lab] at (1.0,0.9) {$\displaystyle \int v\,dt$};
  % 上排（sin t 求导 2 次，中心 y=2.7）
  \node[lab] at (3.0,2.7) {$\sin t$};
  \node[lab] at (5.0,2.7) {$\cos t$};
  \node[lab] at (7.0,2.7) {$-\sin t$};
  % 下排（e^t 逐次积分，中心 y=0.9）
  \node[lab] at (3.0,0.9) {$e^t$};
  \node[lab] at (5.0,0.9) {$e^t$};
  \node[lab] at (7.0,0.9) {$e^t$};
  % 斜向错位箭头：sin t→e^t, cos t→e^t（跨列线 4,6；行标签列与 sin t 列之间无箭头）
  \draw[arr] (3.45,2.05) -- (4.55,1.55);
  \draw[arr] (5.45,2.05) -- (6.55,1.55);
  % 第 3 列竖向箭头（-sin t↔e^t，跨中横线；∫(-sin t)e^t dt = -I 循环出现）
  \draw[arr] (7.0,2.05) -- (7.0,1.55);
  % 符号：列线与中横线交点右上方，⊕⊖⊕ 相间
  \node[lab] at (4.18,2.10) {$\oplus$};
  \node[lab] at (6.18,2.10) {$\ominus$};
  \node[lab] at (7.28,2.10) {$\oplus$};
\end{tikzpicture}





\end{document}
```


计算过程中$\displaystyle \int \sin t \cdot e^t \, dt$会重复出现，因此可以通过建立方程的方式求解该积分：
$$\int \sin t \, e^t \, dt = e^t\sin t - e^t\cos t - \int \sin t \, e^t \, dt$$
设$\displaystyle I = \int \sin t \, e^t \, dt$，代入上式得：
$$I = e^t(\sin t - \cos t) - I$$
移项整理：
$$2I = e^t(\sin t - \cos t)$$
因此：
$$I = \frac{e^t(\sin t - \cos t)}{2} + C$$
即
$$\int \sin t \, e^t \, dt = \frac{1}{2}e^t(\sin t - \cos t) + C$$
回代$\displaystyle t = \arctan x，即 \tan t=\frac{x}{1}$，

```tikz


\begin{document}

\begin{tikzpicture}[
  lab/.style={font=\Large}
]
  % 三条边
  \draw[thin] (0,0) -- (4,0);       % 底边（邻边 1）
  \draw[thin] (4,0) -- (4,2.5);     % 竖边（对边 x）
  \draw[thin] (0,0) -- (4,2.5);     % 斜边 √(1+x²)
  % 直角标记（右下角 B）
  \draw[thin] (3.6,0) -- (3.6,0.4) -- (4,0.4);
  % 角 t 弧线（左下角 A）
  \draw[thin] (0.6,0) arc (0:32.005:0.6);
  % 标注
  \node[lab] at (2,-0.3) {$1$};
  \node[lab] at (4.4,1.25) {$x$};
  \node[lab] at (1.80,1.75) {$\sqrt{1+x^2}$};
  \node[lab] at (0.9,0.35) {$t$};
\end{tikzpicture}




\end{document}
```

可得$\displaystyle \sin t = \frac{x}{\sqrt{1+x^2}}$，$\displaystyle \cos t = \frac{1}{\sqrt{1+x^2}}$，代入得原积分结果：
$$
\begin{align*}
\text{原式} &= \frac{1}{2}e^{\arctan x}\left( \frac{x}{\sqrt{1+x^2}} - \frac{1}{\sqrt{1+x^2}} \right) \\
&= \frac{1}{2}e^{\arctan x} \cdot \frac{x-1}{\sqrt{1+x^2}} + C
\end{align*}
$$


# 特殊函数的不定积分




xxxx

**题目**

$\displaystyle\int x\ln(1+x^{2})\,dx=$
?

````````col
```````col-md
flexGrow=20
===

**答案**：$\dfrac{1}{2}\big[(x^{2}+1)\ln(x^{2}+1)-x^{2}\big]+C$

**解析**

> 用分部积分法，令 $u=\ln(1+x^{2})$，$dv=x\,dx$，则 $du=\dfrac{2x}{1+x^{2}}dx$，$v=\dfrac{x^{2}}{2}$：
> $$\int x\ln(1+x^{2})\,dx=\frac{x^{2}}{2}\ln(1+x^{2})-\int\frac{x^{2}}{2}\cdot\frac{2x}{1+x^{2}}\,dx=\frac{x^{2}}{2}\ln(1+x^{2})-\int\frac{x^{3}}{1+x^{2}}\,dx$$
> 对后一项作变形，$x^{3}=x(1+x^{2})-x$，故
> $$\frac{x^{3}}{1+x^{2}}=x-\frac{x}{1+x^{2}}$$
> $$\int\frac{x^{3}}{1+x^{2}}\,dx=\int x\,dx-\int\frac{x}{1+x^{2}}\,dx=\frac{x^{2}}{2}-\frac12\ln(1+x^{2})$$
> 代回整理：
> $$\text{原式}=\frac{x^{2}}{2}\ln(1+x^{2})-\frac{x^{2}}{2}+\frac12\ln(1+x^{2})+C=\frac12\big[(x^{2}+1)\ln(1+x^{2})-x^{2}\big]+C$$


**另一解法**：
用分部积分的表格法计算不定积分，
选取$u=\ln(1+x^2)$求导，$v'=x$积分，
- 求导列：$\ln(1+x^2) \to \frac{2x}{1+x^2}$
- 积分列：$x \to \frac{1}{2}x^2$

$$
\begin{align*}
\text{原式} &= \frac{1}{2}x^2\ln(1+x^2) - \int \frac{1}{2}x^2 \cdot \frac{2x}{1+x^2} \, dx \\[6pt]
&= \frac{1}{2}x^2\ln(1+x^2) - \int \frac{x^3}{1+x^2} \, dx
\end{align*}
$$

对被积函数$\frac{x^3}{1+x^2}$做代数拆分，结合凑微分计算积分：
$$
\begin{align*}
\int \frac{x^3}{1+x^2} dx &= \int \frac{x^3 + x - x}{1+x^2} dx \\[6pt]
&= \int \frac{x(1+x^2) - x}{1+x^2} dx \\[6pt]
&= \int x \, dx - \int \frac{x}{1+x^2} dx \\[6pt]
&= \frac{1}{2}x^2 - \int \frac{x}{1+x^2} dx + C
\end{align*}
$$

利用$(1+x^2)'=2x$凑微分计算剩余积分项：
$$
\begin{align*}
\because (1+x^2)' &= 2x, \\
\therefore \int \frac{x}{1+x^2} dx &= \frac{1}{2}\int \frac{2x}{1+x^2} dx \\[6pt]
&= \frac{1}{2}\int \frac{1}{1+x^2} d(x^2) \\[6pt]
&= \frac{1}{2}\int \frac{1}{1+x^2} d(x^2+1) \\[6pt]
&= \frac{1}{2}\ln(1+x^2) + C
\end{align*}
$$

化简得到最终结果：
$$
\begin{align*}
\text{原式} &= \frac{1}{2}x^2\ln(1+x^2) - \frac{1}{2}x^2 + \frac{1}{2}\ln(1+x^2) + C \\[6pt]
&= \frac{1}{2}\left[(x^2+1)\ln(1+x^2) - x^2\right] + C
\end{align*}
$$







**考点**

分部积分法（结合凑微分）
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-12-01T08:26:52.098Z,10,8.2956,1,2,1,0,0,2026-11-21T08:26:52.098Z,id=amdz82-->


zzzz













有理函数的积分
所谓有理函数，就是形如$\frac{P_n(x)}{Q_m(x)}$的函数，其中：
$\displaystyle P_n(x)$为$x$的$n$次多项式。
$Q_m(x)$为$x$的$m$次多项式。
- 当$n<m$时，$\displaystyle \frac{P_n(x)}{Q_m(x)}$为真分式。
- 当$n\geq m$时，$\displaystyle \frac{P_n(x)}{Q_m(x)}$为假分式。

## 假分式的分解
假分式 = 多项式 + 真分式

### 通过+1-1的变形方式
例1：化简$\displaystyle \frac{x^2}{x+1}$  
$$
\begin{aligned}
\frac{x^2}{x+1}&=\frac{x^2-1+1}{x+1}\\
&=\frac{x^2-1}{x+1}+\frac{1}{x+1}\\
&=x-1+\frac{1}{x+1}
\end{aligned}
$$

例2：化简$\displaystyle \frac{x}{x-1}$ 
$$
\begin{aligned}
\frac{x}{x-1}&=\frac{x-1+1}{x-1}\\
&=1+\frac{1}{x-1}
\end{aligned}
$$



## 真分式=最简式之和

**最简式有4种** 
### 1~2
若$Q_m(x)$因式分解后出现了$\displaystyle (ax+b)$，
那么$\displaystyle \frac{P_n(x)}{Q_m(x)}$就会因式分解出
$$\frac{A}{ax+b}$$ 若$Q_m(x)$因式分解出了$(ax+b)^2$，
那么$\displaystyle \frac{P_n(x)}{Q_m(x)}$就会因式分解出
$$\frac{A_1}{ax+b} + \frac{A_2}{(ax+b)^2}$$
若$Q_m(x)$因式分解出$(ax+b)^k$，
那么$\displaystyle \frac{P_n(x)}{Q_m(x)}$就会因式分解出
$$\frac{A_1}{ax+b} + \frac{A_2}{(ax+b)^2} + \dots + \frac{A_k}{(ax+b)^k},\quad k>0,k\neq1$$

### 3~4
若$Q_m(x)$因式分解出了$(px^2+qx+r)$，
那么，$\displaystyle \frac{P_n(x)}{Q_m(x)}$中就会分解出
$$\frac{Ax+B}{px^2+qx+r}$$
若$Q_m(x)$中出现了$(px^2+qx+r)^2$，
那么，$\displaystyle \frac{P_n(x)}{Q_m(x)}$中就会分解出
$$\frac{A_1x+B_1}{px^2+qx+r} + \frac{A_2x+B_2}{(px^2+qx+r)^2}$$

若$Q_m(x)$中出现了$(px^2+qx+r)^k$，
那么，$\displaystyle \frac{P_n(x)}{Q_m(x)}$就会因式分解出
$$\frac{A_1x+B_1}{px^2+qx+r} + \frac{A_2x+B_2}{(px^2+qx+r)^2} + \dots + \frac{A_kx+B_k}{(px^2+qx+r)^k} \quad (q^2-4pr<0)$$
---
∵ 当$px^2+qx+r$在分母上时，分母不能为0
且当$q^2-4pr<0$时，$y=px^2+qx+r$无实根
即$y=px^2+qx+r$与x轴无交点，函数值恒正或恒负
y的取值就不会为0
∴ 要规定该形式满足条件$q^2-4pr<0$ 


## 求最简式的不定积分
**1** 
$\displaystyle \star \int \frac{A}{ax+b} dx$，方法：凑微分，把分子凑为分母的导数。
例：计算$\displaystyle \int \frac{3}{2x+1} dx$，其中$(2x+1)'=2$ 
$$
\begin{align*}
\int \frac{3}{2x+1} dx &= \frac{3}{2}\int \frac{2}{2x+1} dx \\
&= \frac{3}{2}\int \frac{1}{2x+1} d(2x+1) \quad \text{凑微分} \\
&= \frac{3}{2}\ln|2x+1| + C
\end{align*}
$$
**2** 
$\displaystyle \star \int \frac{A}{(ax+b)^k} dx$ 
例：计算$\displaystyle \int \frac{3}{(2x-1)^2} dx$，其中$(2x-1)'=2$ 
$$
\begin{align*}
\int \frac{3}{(2x-1)^2} dx &= \frac{3}{2}\int \frac{2}{(2x-1)^2} dx \\
&= \frac{3}{2}\int \frac{1}{(2x-1)^2} d(2x-1) \\
&= -\frac{3}{2} \cdot \frac{1}{2x-1} + C
\end{align*}
$$
**3** 
$\displaystyle \star \int \frac{Ax+B}{px^2+qx+r} dx \quad (q^2-4pr < 0)$ 
方法：凑微分，构造$\displaystyle \int f[g(x)]\cdot g'(x)dx$的形式，把分子凑为分母的导数。
例：计算$\displaystyle \int \frac{3x-2}{x^2+1} dx$，其中$(x^2+1)'=2x = g'(x)$
$$
\int \frac{3x-2}{x^2+1} dx = \int \frac{3x}{x^2+1} dx - \int \frac{2}{x^2+1} dx
$$

k=1时可直接通过凑微分、基本积分公式求解：
$$
\begin{aligned}
&= \frac{3}{2}\int \frac{2x}{x^2+1} \, dx - 2\int \frac{1}{x^2+1} \, dx \\
&= \frac{3}{2}\int \frac{1}{x^2+1} \, d(x^2+1) - 2\int \frac{1}{x^2+1} \, dx \\
&= \frac{3}{2}\ln|x^2+1| - 2\arctan x + C
\end{aligned}
$$

★ 当分母为判别式小于0的二次不可约因式的k次幂时，对应部分分式的一般形式为：
$$\frac{Ax+B}{(px^2+qx+r)^k} \quad (q^2-4pr<0)$$

分部积分可造出方程，这里我们用分部积分法造出递推式。

e.g. $\displaystyle \int \frac{1}{(1+x^2)^2} \, dx$

$\because k=2$
$\therefore$ 设$\displaystyle I_2 = \int \frac{1}{(1+x^2)^2} \, dx$，$I_2$不好解
则$\displaystyle I_1 = \int \frac{1}{1+x^2} \, dx$，$I_1$好解

由导数公式：
$$\left(\frac{1}{u}\right)' = -\frac{1}{u^2}$$

则用分部积分可以由$I_1$推$I_2$：
$$
\begin{aligned}
\int \frac{1}{1+x^2} \, dx &= \frac{x}{1+x^2} - \int x \, d\left(\frac{1}{1+x^2}\right) \quad \text{分部积分} \\
&= \frac{x}{1+x^2} + \int x\cdot \frac{2x}{(1+x^2)^2} \, dx \\
&= \frac{x}{1+x^2} + 2\int \frac{x^2+1-1}{(1+x^2)^2} \, dx
\end{aligned}
$$

$$= \frac{x}{1+x^2} + 2\int \frac{1}{x^2+1} dx - 2\int \frac{1}{(1+x^2)^2} dx$$

$$I_1 = \frac{x}{1+x^2} + 2I_1 - 2I_2$$

$$I_2 = \frac{x}{2(1+x^2)} + \frac{1}{2}I_1$$

$$
\begin{aligned}
\int \frac{1}{(1+x^2)^2} dx &= \frac{x}{2(1+x^2)} + \frac{1}{2}\int \frac{1}{1+x^2} dx \\
&= \frac{x}{2(1+x^2)} + \frac{1}{2}\arctan x + C
\end{aligned}
$$

若是题目给的是$n$次方，则一样是可以找到$I_n$与$I_{n-1}$的关系。








# 二元函数求不定积分

一元函数不定积分：
$$
\begin{align*}
f(x) &= \int \cos x \, dx \\
&= \sin x + C
\end{align*}
$$
其中$C$是任意常数。

二元函数在$x$轴方向上求不定积分（对$x$积分）：
$$
\begin{align*}
f(x,y) &= \int y\cos x \, dx \\
&= y\sin x + \varphi(y)
\end{align*}
$$

$\varphi(y)$是关于$y$的任意函数。
因为是在$x$轴方向上求原函数，可视$y$为常数，因此$+\varphi(y)$与一元情形的$+C$没有区别。

当然，如果是在$y$轴方向上求原函数，最后要$+\varphi(x)$。
至于$\varphi(\cdot)$是什么，后面会讲。


## 注 
若是先在$y$轴方向上求导，那求原函数也要在$y$轴方向上，路径上要保持一致，与二元函数一样。

当然，在$x$轴方向上求积分时，$y$可视为常数；在$y$轴方向上求积分时，$x$可视为常数。
