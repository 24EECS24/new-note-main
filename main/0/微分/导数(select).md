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

## 导数的基本形式

xxxx

 - [*] **【题目】** 


$设函数f(x)可导，且满足条件\lim_{x \to 0}\frac{f(1)-f(1-x)}{2x}=1，则求 f'(1)$ 


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

 - [*] **【题目】** 

已知$f'(1)=2$,则$\lim\limits_{x \to 0}\frac{x}{f(1-x)-f(1+3x)}=\underline{\qquad\qquad}$。

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

## 导数的广义化形式
 - [*] **【题目】** 
当 $x \to 0$ 时，$f(x)-1$ 是比 $\sin x$ 高阶的无穷小，且 $f(0)=1$，则下列选项正确的是（==C==）

- A. $f'(0)=1$
- B. $\lim\limits_{x \to 0}f(x)=0$
- C. $f'(0)=0$
- D. $\lim\limits_{x \to 0}\sin f(x)=0$

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
 - [*] **【题目】** 

设 $f(0)=0$,$f'(0)=-1$,则 $\lim\limits_{x \to 0}\dfrac{f(3x)}{x}=\underline{\quad\quad}$。

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

## 导数的几何意义


 - [*] **【题目】** 

$y=a(x-1)^2+x\cos x$ 在 $(0,a)$ 处的切线斜率为 $-4$，则常数 $a=$ $\underline{\qquad\qquad}$。

**答案**：$\dfrac{5}{2}$

**解析**

> $y'=2a(x-1)+\cos x-x\sin x$，$k_{\text{切}}=y'|_{x=0}=-2a+1=-4$，解得 $a=\frac{5}{2}$。

**考点**：导数的几何意义（切线斜率）

