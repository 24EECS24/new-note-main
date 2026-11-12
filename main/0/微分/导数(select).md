#flashcards/微分/导数  

## 易看错
xxxx
 - [*] **题目**

设 $f(x)=\begin{cases}3x+2, & x \geq 1 \\ 2x^2-x+4, & x<1\end{cases}$，则在 $x=1$ 处（　　）

- A. 连续，可导
- B. 不连续，不可导
- C. 不连续，可导
- D. 连续，不可导
?
**答案**：A

**解析**

> $\lim\limits_{x\to1^-}f(x)=\lim\limits_{x\to1^-}(2x^2-x+4)=5$，$\lim\limits_{x\to1^+}f(x)=\lim\limits_{x\to1^+}(3x+2)=5$，$\lim\limits_{x\to1}f(x)=f(1)=5$，故 $f(x)$ 在 $x=1$ 处连续。$f'_-(1)=\lim\limits_{x\to1^-}\frac{2x^2-x+4-5}{x-1}=\lim\limits_{x\to1^-}\frac{(2x+1)(x-1)}{x-1}=3$，$f'_+(1)=\lim\limits_{x\to1^+}\frac{3x+2-5}{x-1}=3$，左右导数相等，故可导。选 A。

此题求导时易当成x趋向于0，从而选D
**考点**：分段函数连续性与可导性判断
<!--SR:!fsrs,2026-11-14T07:17:12.986Z,9,8.2956,1,2,1,0,0,2026-11-05T07:17:12.986Z,id=of28uh-->
zzzz


xxxx
 - [*] **题目**

已知 $f'(-3)=2$，则 $\lim\limits_{x \to -3}\dfrac{f(x)-f(-3)}{\sin(3+x)}=$（　　）

- A. $-2$
- B. $0$
- C. $2$
- D. 不存在
?
**答案**：c

**易忘的点**：

$\displaystyle \lim_{x\to-3}\frac{f(x)-f(-3)}{\sin(x+3)}=\lim_{x\to-3}\frac{f(x)-f(-3)}{x+3}=\lim_{x\to-3}\frac{f(x)-f(-3)}{x-(-3)}=f'(-3)=2$

这一题如果看不出$\displaystyle x+3=x-(-3)$的话，就容易想复杂

**考点**：导数定义
<!--SR:!fsrs,2026-11-19T05:01:18.667Z,9,10.56215632,3.58131923,2,3,0,0,2026-11-10T05:01:18.667Z,id=laje7g-->
zzzz

## 判别的总结

>$可微\Leftrightarrow 可导 \Rightarrow 连续 \Rightarrow 极限存在$ 
>
>$不可微\Leftrightarrow 不可导 \Leftarrow  不连续 \Leftarrow  极限不存在$ 
>
>即$A \to B \;\Longleftrightarrow\; (\neg) A \gets  (\neg) B$ (逆否命题)


>极限存在
>若，$\lim\limits_{x \to x_0^+} f(x) =\lim\limits_{x \to x_0^-} f(x)=A，(A为一确定的实数)$ 
>则，此极限存在

>连续
>若，$\displaystyle \lim_{x \to x_0^+} f(x) = \lim_{x \to x_0^-} f(x) = f(x_0)=A，(A为一确定的实数)$ 
>则称函数$f(x)$在点$x_0$处连续。

>可导
>若，$f'_-(x_0)$存在，$f'_+(x_0)$存在，且$f'_-(x_0)=f'_+(x_0)$ 
>则称函数$f(x)$在点$x_0$处可导。

>可微
>若，$\displaystyle \lim\limits_{\Delta x \to 0} \frac{\Delta y - f'(x_0)\cdot\Delta x}{\Delta x}=0，\Delta y = f(x_0+\Delta x) - f(x_0)$  
>即，$\displaystyle \Delta y - dy=o(\Delta x)$  
>则称函数$f(x)$在点$x_0$处可微。


xxxx

**题目**

设函数 $f(x)=\begin{cases}3x+2, & x \geq 1 \\ 2x^2-x+4, & x<1\end{cases}$，则在 $x=1$ 处（　　）

- A. 连续，可导
- B. 不连续，不可导
- C. 不连续，可导
- D. 连续，不可导
?
````````col
```````col-md
flexGrow=20
===

**答案**：A

**解析**

> $\lim\limits_{x\to1^-}f(x)=\lim\limits_{x\to1^-}(2x^2-x+4)=5$，$\lim\limits_{x\to1^+}f(x)=\lim\limits_{x\to1^+}(3x+2)=5$，$\lim\limits_{x\to1}f(x)=f(1)=5$，故 $f(x)$ 在 $x=1$ 处连续。
>
> $f'_-(1)=\lim\limits_{x\to1^-}\frac{2x^2-x+4-5}{x-1}=\lim\limits_{x\to1^-}\frac{(2x+1)(x-1)}{x-1}=3$，
>
> $f'_+(1)=\lim\limits_{x\to1^+}\frac{3x+2-5}{x-1}=3$，
>
> 左右导数相等，故可导。选 A。

**考点**：分段函数在分段点的连续性与左右导数（可导充要条件）

```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-19T07:16:59.170Z,7,8.2956,1,2,1,0,0,2026-11-12T07:16:59.170Z,id=3d0qk9-->

zzzz





## 导数的基本形式

xxxx

 - [*] **【题目】**


设函数$f(x)$可导，且满足条件$\displaystyle \lim_{x \to 0}\frac{f(1)-f(1-x)}{2x}=1，则求 f'(1)$


 ?
````````col
```````col-md
flexGrow=20
===

`````col
````col-md
flexGrow=1
===

$$
\begin{align*}
&解法一:\\[6pt]
&根据导数的定义，\\[6pt]
&f'(x_0) = \lim\limits_{\Delta x \to 0}\frac{f(x_0+\Delta x)-f(x_0)}{\Delta x}\\[6pt]
&=\lim\limits_{x \to x_0}\frac{f(x)-f(x_0)}{x - x_0}\\[6pt]
&令 x_0=1，则f'(1) = \lim\limits_{\Delta x \to 0}\frac{f(1+\Delta x)-f(1)}{\Delta x}\\[6pt]
&即，\Delta x \to 0时，\frac{f(1+\Delta x)-f(1)}{\Delta x} \to f'(1) \\[6pt]
&原式=\lim_{x \to 0}\frac{f(1-x)-f(1)}{-2x}=1  \\[6pt]
&\!\! \qquad =\frac{1}{2} \lim_{x \to 0}\frac{f(1-x)-f(1)}{-x}=1 \\[6pt]
&\!\! \qquad \therefore \ x \to 0时，\frac{f(1-x)-f(1)}{-x} \to 2\\[6pt]
&\!\! \qquad \because \ \lim_{x \to 0}\frac{x}{-x}=常数，\\[6pt]
&\!\! \qquad 即，x \to 0时，x与-x同阶无穷小 \\[6pt]
&\!\! \qquad \therefore \ -x \to 0时，\frac{f(1-x)-f(1)}{-x} \to 2\\[6pt]
& \!\! \qquad =\frac{1}{2} \lim_{-x \to 0}\frac{f(1-x)-f(1)}{-x}=1  \\[6pt]
& \Rightarrow \ \lim_{-x \to 0}\frac{f(1-x)-f(1)}{-x}=f'(1)=2 \\[6pt]
\end{align*}
$$

````

````col-md
flexGrow=1
===

$$
\begin{aligned}
&解法二:\\[6pt]
\because f'(1) &= \lim_{h \to 0} \frac{f(1+h)-f(1)}{h} \\[4pt]
& = \lim_{h \to 1} \frac{f(h)-f(1)}{h-1} \\[4pt]
&= \lim_{x \to 0} \frac{f(1-x)-f(1)}{-x} \\[4pt]
\therefore 原式 &= \lim_{x \to 0} \frac{-\left[f(1-x)-f(1)\right]}{2x} \\[4pt]
& = \lim_{x \to 0} \frac{f(1-x)-f(1)}{-2x} \\[4pt]
\Rightarrow f'(1) &= \lim_{x \to 0} \frac{f(1-x)-f(1)}{-x} \\[4pt]
& = 2 \lim_{x \to 0} \frac{f(1-x)-f(1)}{-2x} \\[4pt]
& = 2 \times 1 \\[4pt]
& = 2 \\[4pt]
\end{aligned}
$$



````
`````
**另一个思路** 
用导数的广义形式写
$$
f'(1) = \lim_{x \to 1} \frac{f(x)-f(1)}{x-1}
$$
**只要当$\lim 下面的 x \to a$时，式子里的$w(x) \to x_0$ 则，极限值就不变** 
通过换元来靠

思路1：看到分子很像，往上转化
要往 $\lim_{x \to 0} \frac{f(1)-f(1-x)}{2x}$ 上靠
则，让 $x换为w(x)=1-x$ 
且 $w(x) \to 1$ 
则 $x \to 0$ 

思路2：看到$\lim 下面是 x \to 0$ 
且 $w(x) \to 1$ 
看到分子很像，往上转化
则，让 $x换为w(x)=1-x$ 

$$
\begin{align*}
f'(1) &= \lim_{x \to 1} \frac{f(x)-f(1)}{x-1}= \lim_{x \to 0} \frac{f(1-x)-f(1)}{(1-x)-1} \\[6pt]
&= \lim_{x \to 0} \frac{f(1)-f(1-x)}{x}
\end{align*}
$$
即
$$\lim_{x \to 0} \frac{f(1)-f(1-x)}{2x} = \frac{1}{2}f'(1)$$




```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-19T05:57:14.333Z,7,8.2956,1,2,1,0,0,2026-11-12T05:57:14.333Z,id=hrvccy-->

zzzz

xxxx

 - [*] **【题目】**

设 $f'(x_0)=A$,则 $\lim\limits_{\Delta x \to 0}\dfrac{f(x_0+2\Delta x)-f(x_0-3\Delta x)}{\Delta x}=\underline{\quad\quad}$。
?
````````col
```````col-md
flexGrow=20
===

**【解析】**

【答案】$5A$
【解】
$$
\begin{aligned}
&\lim_{\Delta x \to 0} \frac{f(x_0 + 2\Delta x) - f(x_0 - 3\Delta x)}{\Delta x} \\[4pt]
&= \lim_{\Delta x \to 0} \frac{f(x_0 + 2\Delta x) - f(x_0) + f(x_0) - f(x_0 - 3\Delta x)}{\Delta x} \\[4pt]
&= \lim_{\Delta x \to 0} \frac{f(x_0 + 2\Delta x) - f(x_0)}{\Delta x} - \lim_{\Delta x \to 0} \frac{f(x_0 - 3\Delta x) - f(x_0)}{\Delta x} \\[4pt]
&= 2\lim_{\Delta x \to 0} \frac{f(x_0 + 2\Delta x) - f(x_0)}{2\Delta x} + 3\lim_{\Delta x \to 0} \frac{f(x_0 - 3\Delta x) - f(x_0)}{-3\Delta x} \\[4pt]
&= 2f'(x_0) + 3f'(x_0) \\[4pt]
 &= 5A.
\end{aligned}
$$


```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-20T05:53:50.607Z,8,8.2956,1,2,1,0,0,2026-11-12T05:53:50.607Z,id=elo88x-->

zzzz

xxxx

 - [*] **【题目】**

已知$f'(1)=2$,则$\lim\limits_{x \to 0}\frac{x}{f(1-x)-f(1+3x)}=\underline{\qquad\qquad}$。
?
````````col
```````col-md
flexGrow=20
===

**【解析】**

【答案】$-\dfrac{1}{8}$
【解】

$$
\begin{aligned}
\because &f'(1) = \lim_{x \to 0} \frac{f(1+x)-f(1)}{x} \\[4pt]
\therefore &\lim_{x \to 0} \frac{f(1-x)-f(1+3x)}{x} \\[4pt]
&= \lim_{x \to 0} \frac{f(1-x)-f(1)}{x} + \lim_{x \to 0} \frac{f(1)-f(1+3x)}{x} \\[4pt]
&= -\lim_{x \to 0} \frac{f(1-x)-f(1)}{-x} + (-3)\cdot\lim_{x \to 0} \frac{f(1+3x)-f(1)}{3x} \\[4pt]
&= -f'(1) -3f'(1) \\[4pt]
&= -4f'(1) \\[4pt]
&= -8.\\[4pt]
\therefore &\lim_{x \to 0} \frac{x}{f(1-x)-f(1+3x)} \\[4pt]
&= -\frac{1}{8}.
\end{aligned}
$$


```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-19T06:02:40.648Z,7,8.2956,1,2,1,0,0,2026-11-12T06:02:40.648Z,id=1t9sps-->

zzzz
## 导数的广义化形式

xxxx
 - [*] **【题目】**
当 $x \to 0$ 时，$f(x)-1$ 是比 $\sin x$ 高阶的无穷小，且 $f(0)=1$，则下列选项正确的是（）

- A. $f'(0)=1$
- B. $\lim\limits_{x \to 0}f(x)=0$
- C. $f'(0)=0$
- D. $\lim\limits_{x \to 0}\sin f(x)=0$
?
````````col
```````col-md
flexGrow=20
===

==C==
$$
\begin{align*}

f'(0) &= \lim_{x \to x_0} \frac{f(x)-f(x_0)}{x-x_0} \\[4pt]
&= \lim_{x \to 0} \frac{f(x)-f(0)}{x-0} \\[4pt]
&= \lim_{x \to 0} \frac{f(x)-1}{x} \\[4pt]
&= \lim_{x \to 0} \frac{f(x)-1}{\sin x} \\[4pt]
&\because f(x)-1是\sin x的高阶无穷小\\[4pt]
&\therefore f'(0) = \lim_{x \to 0} \frac{f(x)-1}{\sin x} = 0
\end{align*}
$$


```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-20T06:11:47.082Z,8,8.2956,1,2,1,0,0,2026-11-12T06:11:47.082Z,id=63y3vk-->

zzzz

xxxx

 - [*] **【题目】**

设 $f(0)=0$,$f'(0)=-1$,则 $\lim\limits_{x \to 0}\dfrac{f(3x)}{x}=\underline{\quad\quad}$。
?
````````col
```````col-md
flexGrow=20
===

**【解析】**

【答案】$-3$
【解】
`````col
````col-md
flexGrow=1
===

$$
\begin{aligned}
解法一：&\\[4pt]
&\lim_{x \to 0} \frac{f(3x)}{x} \\[4pt]
&= 3\lim_{x \to 0} \frac{f(3x)}{3x} \\[4pt]
&= 3\lim_{x \to 0} \frac{f(3x) - f(0)}{3x - 0} \\[4pt]
&= 3f'(0) \\[4pt]
&= -3.\\[4pt]
\end{aligned}
$$

````

````col-md
flexGrow=1
===

$$
\begin{align*}
解法二：&\\[4pt]
\because f'(0) &= \lim_{x \to 0} \frac{f(x) - f(0)}{x - 0} \\[4pt]
&= \lim_{x \to 0} \frac{f(3x) - f(0)}{3x - 0} \\[4pt]
&= \lim_{x \to 0} \frac{f(3x)}{3x} = -1\\[4pt]
\therefore& \lim_{x \to 0} \frac{f(3x)}{x} \\[4pt]
&= 3\lim_{x \to 0} \frac{f(3x)}{3x} \\[4pt]
&= -3
\end{align*}
$$



````
`````


```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-18T06:14:27.411Z,6,8.2956,1,2,1,0,0,2026-11-12T06:14:27.411Z,id=kk4wzm-->
zzzz

## 函数在一点可导的充要条件

xxxx

**题目**

已知 $f(x)=\begin{cases}\sin ax+2a-1, & x \geq 0 \\ \ln(1+bx)+3b, & x<0\end{cases}$ 在 $x=0$ 处可导，求参数 $a,b$ 的值。
?
````````col
```````col-md
flexGrow=20
===

**答案**：$a=-1,\ b=-1$

**解析**

> 可导必连续。$f(0)=2a-1$，$\lim\limits_{x\to0^+}f(x)=\lim\limits_{x\to0^+}[\ln(1+bx)+3b]=3b$，故 $2a-1=3b$。
>
> 右导数：$f'_+(0)=\lim\limits_{x\to0^+}\frac{\sin ax+2a-1-(2a-1)}{x}=\lim\limits_{x\to0^+}\frac{\sin ax}{x}=a$。
>
> 左导数：$f'_-(0)=\lim\limits_{x\to0^-}\frac{\ln(1+bx)+3b-(2a-1)}{x}=\lim\limits_{x\to0^-}\frac{\ln(1+bx)}{x}=b$。
>
> 可导要求 $a=b$。联立 $\begin{cases}2a-1=3b \\ a=b\end{cases}$，解得 $2a-1=3a$，$a=-1$，$b=-1$。

**考点**：分段函数在分段点的连续性与左右导数（可导充要条件）

```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-20T07:17:03.908Z,8,8.2956,1,2,1,0,0,2026-11-12T07:17:03.908Z,id=toqxa4-->


zzzz
## 带绝对值因式的函数求导
先把绝对值打开，写成分段函数：
$$
F(x)=
\begin{cases}
-f(x)(x-a), & x<a \\
0, & x=a \\
f(x)(x-a), & x>a
\end{cases}
$$

###  一个结论

设$f(x)$在$x=a$处连续
$f(a)=0$$\iff$ $F(x)=f(x)|x-a|$在$x=a$处可导

$|x-a|$在$x=a$处不可导，要让乘积$y=f(x)|x-a|$在$x=a$处可导，需要$f(x)$抵消$|x-a|$在该点的不可导性，“拯救”该点的可导性。




xxxx

**题目**

函数 $y=(x^2-x+2)|x-3|$ 的不可导点的个数（　　）

- A. $0$
- B. $1$
- C. $2$
- D. $3$
?
````````col
```````col-md
flexGrow=20
===

**答案**：B

**解析**

> $x=3$ 为 $|x-3|$ 的不可导点。令 $g(x)=x^2-x+2$，$g(3)=8\neq0$，故 $x=3$ 处 $y$ 不可导；其余点均为多项式可导区间内点，故不可导点个数为1。

**考点**：带绝对值因式函数的可导性（$f(a)\neq0$ 时 $f(x)|x-a|$ 在 $a$ 点不可导）

```````

```````col-md
flexGrow=1
===





```````
````````

zzzz




## 导数的几何意义

xxxx
**题目**

曲线 $y=e^{-2x}\cos 3x$ 在点 $(0,1)$ 处的切线方程为　$\underline{\qquad\quad}$。
?
````````col
```````col-md
flexGrow=20
===

**答案**：$y=-2x+1$

**解析**

> $y'=-2e^{-2x}\cos 3x-3e^{-2x}\sin 3x$，$y'(0)=-2$，
>
> 切线方程 $y-1=-2x$，即 $y=-2x+1$。

**考点**：导数的几何意义（切线方程）

```````

```````col-md
flexGrow=1
===





```````
````````

zzzz

xxxx
 - [*] **【题目】**

$y=a(x-1)^2+x\cos x$ 在 $(0,a)$ 处的切线斜率为 $-4$，则常数 $a=$ $\underline{\qquad\qquad}$。
?
````````col
```````col-md
flexGrow=20
===

**答案**：$\dfrac{5}{2}$

**解析**

> $y'=2a(x-1)+\cos x-x\sin x$，$k_{\text{切}}=y'|_{x=0}=-2a+1=-4$，解得 $a=\frac{5}{2}$。

**考点**：导数的几何意义（切线斜率）

```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-18T07:16:53.890Z,6,8.2956,1,2,1,0,0,2026-11-12T07:16:53.890Z,id=516fqr-->

zzzz

## 二元函数求导



### 方向导

xxxx
**题目**

函数 $f(x,y,z)=xy+yz^2-x$ 在点 $(2,-1,1)$ 处沿 $x$ 轴正方向的方向导数为（　　）

- A. $-2$
- B. $-7$
- C. $2$
- D. $7$
?
````````col
```````col-md
flexGrow=20
===

**答案**：A

**解析**

> 沿 $x$ 轴正方向的方向导数即 $\dfrac{\partial f}{\partial x}\big|_{(2,-1,1)}=y-1=-1-1=-2$。

**考点**：沿坐标轴方向的方向导数（即一阶偏导数）

```````

```````col-md
flexGrow=1
===





```````
````````

zzzz







