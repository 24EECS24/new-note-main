#flashcards/微分/导数  

## 易看错

xxxx
**题目**

已知 $\lim\limits_{x \to 0}\dfrac{f(5x)-f(0)}{2x}=1$，求 $f'(0)=$（　　）

- A. $\dfrac{5}{2}$
- B. $\dfrac{2}{5}$
- C. $1$
- D. $5$
?
````````col
```````col-md
flexGrow=20
===

**答案**：B

**解析**

> $$\text{原式}=\dfrac{5}{2}\lim\limits_{x\to0}\dfrac{f(5x)-f(0)}{5x}=\dfrac{5}{2}f'(0)=1$$
>
> 故 $f'(0)=\dfrac{2}{5}$。

**考点**：导数定义（广义化形式）
误以为是$f'(0)=1$，求$\lim\limits_{x \to 0}\dfrac{f(5x)-f(0)}{2x}$


```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-22T08:22:11.206Z,10,8.2956,1,2,1,0,0,2026-11-12T08:22:11.206Z,id=0hd8ok-->
zzzz



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


xxxx
**题目**

设 $f(x)$ 在 $x=a$ 的某个邻域内有定义，若 $\lim\limits_{x\to a}\dfrac{f(x)-f(a)}{(x-a)^{3}}=6$，则在 $x=a$ 处（　　）

- A. $f(x)$ 导数存在且 $f'(a)\neq 0$
- B. $f(x)$ 导数不存在
- C. $f(x)$ 取得极小值
- D. $f(x)$ 不取极值
?
````````col
```````col-md
flexGrow=20
===

**答案**：D

**解析**

> $$\dfrac{f(x)-f(a)}{x-a}=6(x-a)^{2}\to 0$$
>
> 故 $f'(a)=0$。又 $f(x)-f(a)\sim 6(x-a)^{3}$ 
> $x<a：(x-a)^3<0$，所以 $f(x)-f(a)<0$
> $x>a：(x-a)^3>0$，所以 $f(x)-f(a)>0$
> 函数值从 “比 $f(a)$ 低” 变成 “比 $f(a)$ 高”
> 在 $a$ 两侧变号，故不取极值

**考点**：导数定义（由极限式判定导数）

```````

```````col-md
flexGrow=1
===





```````
````````
这一题看到一阶导=0，就容易选c
事实上，**$f'(a)=0$只是极值的必要条件，不是充分条件**
eg:
**水平拐点**：$f'$ 在该点两侧**同号**。
比如 $x^3 在 0 处，f'(0)=0$，
但 $f'=3x^2$在两侧都为正，函数始终递增，没有极值。
<!--SR:!fsrs,2026-11-13T06:54:09.775Z,0,0.212,6.4133,1,1,0,0,2026-11-13T06:53:09.775Z,id=24s2rb-->



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

关于二元函数 $z=f(x,y)$ 在点 $(x_0,y_0)$ 处，下列说法正确的是（　　）

- A. 可微则偏导数一定存在
- B. 连续一定可微
- C. 偏导数存在一定可微
- D. 偏导数存在一定连续
?
````````col
```````col-md
flexGrow=20
===

**答案**：A

**解析**

> 可微是偏导数存在的充分条件，选 A。

**考点**：二元函数可微与偏导数的关系

```````

```````col-md
flexGrow=1
===





```````
````````

zzzz



xxxx
**题目**

若函数 $y=f(x)$ 在 $(a,b)$ 内可导，下列结论正确的是（　　）

- A. 函数 $y=f(x)$ 在 $[a,b]$ 上连续
- B. 函数 $y=f(x)$ 在 $(a,b)$ 内可微
- C. 必有一点 $\xi\in(a,b)$，使 $f'(\xi)=0$ 成立
- D. 必有一点 $\xi\in(a,b)$，使 $f(b)-f(a)=f'(\xi)(b-a)$ 成立
?
````````col
```````col-md
flexGrow=20
===

**答案**：B

**解析**

> 可导即可微，故 B 正确。A、C、D 均缺少闭区间连续等条件。

**考点**：可导与可微的关系（可微 ⇔ 可导）

```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-18T08:22:00.824Z,6,8.2956,1,2,1,0,0,2026-11-12T08:22:00.824Z,id=kooefc-->
zzzz

xxxx
**题目**

下列关于函数 $y=f(x)$ 在 $x_{0}$ 的命题中不正确的是（　　）

- A. 可导必连续
- B. 可微必可导
- C. 可导必可微
- D. 连续必可导
?
````````col
```````col-md
flexGrow=20
===

**答案**：D

**解析**

> 连续不一定可导（如 $|x|$ 在 $x=0$ 处），故选 D。

**考点**：可导、可微、连续的关系

```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-21T08:23:25.472Z,9,8.2956,1,2,1,0,0,2026-11-12T08:23:25.472Z,id=vhn1zr-->
zzzz


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
**题目**

函数 $f(x)$ 在 $x=a$ 处可导，则 $\lim\limits_{x\to 0}\dfrac{f(a+x)-f(a-x)}{x}=$（　　）

- A. $2f'(a)$
- B. $0$
- C. $f'(a)$
- D. $\dfrac{1}{2}f'(a)$
?
````````col
```````col-md
flexGrow=20
===

**答案**：A

**解析**

> $$\text{原式}=\lim\limits_{x\to 0}\dfrac{f(a+x)-f(a)}{x}+\lim\limits_{x\to 0}\dfrac{f(a-x)-f(a)}{-x}=f'(a)+f'(a)=2f'(a)$$

**考点**：导数定义（广义化形式）

```````

```````col-md
flexGrow=1
===





```````
````````

zzzz






xxxx
**题目**

设函数 $y=f(x)$ 在点 $x=1$ 处可导，且极限 $\lim\limits_{x \to 1}\dfrac{f(x)-f(1)}{x^{2}-1}=3$，则 $f'(1)=$（　　）

- A. $2$
- B. $3$
- C. $6$
- D. $12$
?
````````col
```````col-md
flexGrow=20
===

**答案**：C

**解析**

> $$\lim\limits_{x\to1}\dfrac{f(x)-f(1)}{(x-1)(x+1)}=\dfrac{f'(1)}{2}=3$$
>
> 故 $f'(1)=6$。

**考点**：导数定义（广义化形式）


```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-23T05:51:30.606Z,10,8.2956,1,2,1,0,0,2026-11-13T05:51:30.606Z,id=6n2fqr-->
zzzz

xxxx
**题目**

已知 $f'(0)=-2$，则极限 $\lim\limits_{x \to 0}\dfrac{f(-x)-f(0)}{\ln(1+3x)}=$　$\underline{\qquad\quad}$。
?
````````col
```````col-md
flexGrow=20
===

**答案**：$\dfrac{2}{3}$

**解析**

> $$\lim\limits_{x \to 0}\frac{f(-x)-f(0)}{\ln(1+3x)}=\lim\limits_{x \to 0}\frac{-f'(-x)}{3}=\frac{-f'(0)}{3}=\frac{2}{3}$$

**考点**：导数定义（广义化形式）

```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-18T08:21:49.592Z,6,8.2956,1,2,1,0,0,2026-11-12T08:21:49.592Z,id=ovh9zc-->

zzzz




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

函数 $f(x)=1-|x-1|$ 在点 $x=1$ 处（　　）

- A. 不连续
- B. 连续且可导
- C. 既不连续也不可导
- D. 连续但不可导
?
````````col
```````col-md
flexGrow=20
===

**答案**：D

**解析**

> $f(1)=1$，左极限 = 右极限 = 1，连续；但左导数 $=1$，右导数 $=-1$，不可导，选 D。

**考点**：绝对值函数在分段点的左右导数（可导性判断）

```````

```````col-md
flexGrow=1
===





```````
````````

zzzz


xxxx
**题目**

设 $f(x)=\begin{cases}x^2\sin\dfrac{1}{x},&x\neq 0\\ 0,&x=0\end{cases}$，则 $f(x)$ 在 $x=0$ 处（　　）

- A. 极限不存在
- B. 极限存在但不连续
- C. 连续但不可导
- D. 连续且可导
?
````````col
```````col-md
flexGrow=20
===

**答案**：D

**解析**

> $\lim\limits_{x\to 0}x^2\sin\dfrac{1}{x}=0=f(0)$，连续；
>
> $$f'(0)=\lim\limits_{x\to 0}\dfrac{x^2\sin(1/x)}{x}=\lim x\sin(1/x)=0$$
>
> 可导，选 D。

**考点**：分段函数在分段点的可导性（导数定义）

```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-20T06:52:50.508Z,7,8.2956,1,2,1,0,0,2026-11-13T06:52:50.508Z,id=foazkr-->

zzzz

xxxx
**题目**

$y=|\tan x|$ 在 $x=0$ 处（　　）

- A. 可导，不连续
- B. 可导，连续
- C. 不可导，连续
- D. 不可导，不连续
?
````````col
```````col-md
flexGrow=20
===

**答案**：C

**解析**

> $|\tan x|$ 在 $x=0$ 处连续，但左右导数分别为 $-1$ 和 $1$，故不可导。

**考点**：绝对值函数在分段点的左右导数（可导性判断）

```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-18T08:22:05.538Z,6,8.2956,1,2,1,0,0,2026-11-12T08:22:05.538Z,id=dmic8g-->

zzzz

xxxx
**题目**

函数 $f(x)=\sqrt[3]{x-1}+x$，在 $x=1$ 处（　　）

- A. 不可导，连续
- B. 不可导，不连续
- C. 可导，不连续
- D. 可导，连续
?
````````col
```````col-md
flexGrow=20
===

**答案**：A

**解析**

> $f(1)=\sqrt[3]{0}+1=1$，$\lim\limits_{x \to 1}f(x)=1=f(1)$，故连续；
>
> $$f'(1)=\lim\limits_{x \to 1}\frac{\sqrt[3]{x-1}+x-1}{x-1}=\lim\limits_{x \to 1}\frac{1}{\sqrt[3]{(x-1)^2}}+1=\infty$$
>
> 故不可导。

**考点**：一点可导性判断（连续但不可导）

```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-20T08:08:29.005Z,8,8.2956,1,2,1,0,0,2026-11-12T08:08:29.005Z,id=x1mdco-->

zzzz



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
<!--SR:!fsrs,2026-11-19T08:08:37.050Z,7,8.2956,1,2,1,0,0,2026-11-12T08:08:37.050Z,id=apxz20-->

zzzz




## 导数的几何意义

xxxx
**题目**

若曲线 $f(x)=1-x^3$ 与曲线 $g(x)=\ln x$ 在自变量 $x=x_0$ 时的切线相互垂直，则 $x_0$ 应为（　　）

- A. $\dfrac{1}{\sqrt[3]{3}}$
- B. $-\dfrac{1}{\sqrt[3]{3}}$
- C. $\dfrac{1}{3}$
- D. $-\dfrac{1}{3}$
?
````````col
```````col-md
flexGrow=20
===

**答案**：C

**解析**

> $f'(x_0)=-3x_0^2$，$g'(x_0)=\dfrac{1}{x_0}$，
>
> 垂直则 $f'(x_0)\cdot g'(x_0)=-1$，即
>
> $$-3x_0^2\cdot\dfrac{1}{x_0}=-3x_0=-1$$
>
> $x_0=\dfrac{1}{3}$，选 C。

**考点**：导数的几何意义（切线垂直、切线斜率）

```````

```````col-md
flexGrow=1
===





```````
````````
zzzz


xxxx
**题目**

曲线 $y=e^{1-x^2}$ 与直线 $x=-1$ 的交点为 $Q$，则曲线 $y=e^{1-x^2}$ 在点 $Q$ 处的切线方程式（　　）

- A. $2x-y-2=0$
- B. $2x+y-2=0$
- C. $2x+y+3=0$
- D. $2x-y+3=0$
?
````````col
```````col-md
flexGrow=20
===

**答案**：D

**解析**

> $Q(-1,1)$，$y'=-2xe^{1-x^2}$，$y'(-1)=2$，
>
> 切线 $y-1=2(x+1)$，即 $2x-y+3=0$，选 D。

**考点**：导数的几何意义（切线方程）

```````

```````col-md
flexGrow=1
===





```````
````````

zzzz

xxxx
**题目**

曲线 $y=\dfrac{1}{3}x^{3}+\dfrac{1}{2}x^{2}+6x+1$ 在点 $(0,1)$ 处的切线与 $x$ 轴的交点坐标为（　　）

- A. $\left(-\dfrac{1}{6},0\right)$
- B. $(0,1)$
- C. $\left(\dfrac{1}{6},0\right)$
- D. $(-1,0)$
?
````````col
```````col-md
flexGrow=20
===

**答案**：A

**解析**

> $y'=x^{2}+x+6$，$x=0$ 处 $y'=6$，
> 切线方程:y=6x+b,代入(0,1)
>
> 切线 $y=6x+1$，令 $y=0$ 得 $x=-\dfrac{1}{6}$。

**考点**：导数的几何意义（切线方程）

```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-22T05:46:22.287Z,9,8.2956,1,2,1,0,0,2026-11-13T05:46:22.287Z,id=jv5vpp-->

zzzz

xxxx
**题目**

过曲线 $y=x\ln x$ 上 $M_{0}$ 点的切线平行于直线 $y=2x+1$，则切点 $M_{0}$ 的坐标是（　　）

- A. $(1,0)$
- B. $(e,0)$
- C. $(e,1)$
- D. $(e,e)$
?
````````col
```````col-md
flexGrow=20
===

**答案**：D

**解析**

> $y'=\ln x+1$，令 $=2$ 得 $\ln x=1$，$x=e$，$y=e\ln e=e$，切点 $(e,e)$。

**考点**：导数的几何意义（切线平行、切线斜率）

```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-21T05:53:41.974Z,8,8.2956,1,2,1,0,0,2026-11-13T05:53:41.974Z,id=044vn1-->

zzzz

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
<!--SR:!fsrs,2026-11-22T08:08:39.603Z,10,8.2956,1,2,1,0,0,2026-11-12T08:08:39.603Z,id=xcbwba-->

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

xxxx
**题目**

曲线 $y=\dfrac{x}{2\ln x}+1$ 在点 $\left(\mathrm{e}^{2},\dfrac{\mathrm{e}^{2}}{4}+1\right)$ 处的切线斜率为（　　）

- A. $-8$
- B. $-\dfrac{1}{8}$
- C. $\dfrac{1}{8}$
- D. $8$
?
````````col
```````col-md
flexGrow=20
===

**答案**：C

**解析**

> $$y'=\dfrac{2\ln x-2}{(2\ln x)^2}=\dfrac{\ln x-1}{2(\ln x)^2}$$
>
> 在 $x=\mathrm{e}^2$ 处，$k=\dfrac{2-1}{2\cdot4}=\dfrac{1}{8}$。

**考点**：导数的几何意义（切线斜率）

```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-22T08:21:53.854Z,10,8.2956,1,2,1,0,0,2026-11-12T08:21:53.854Z,id=a6uo8m-->
zzzz

### 与拉格朗日的联系

xxxx
**题目**

曲线 $y=\ln x$ 在点 $\underline{\qquad\quad}$ 处切线与连接曲线上两点 $(1,0)$，$(e,1)$ 的弦平行。
?
````````col
```````col-md
flexGrow=20
===

**答案**：$(e-1,\,\ln(e-1))$

**解析**

> 弦斜率 $=\dfrac{1-0}{e-1}=\dfrac{1}{e-1}$。
>
> $y'=\dfrac{1}{x}=\dfrac{1}{e-1}$，得 $x=e-1$。

**其实，这一题本质是拉格朗日**

**考点**：导数的几何意义（切线平行、切线斜率）

```````

```````col-md
flexGrow=1
===





```````
````````

zzzz


## 导数的性质

xxxx
**题目**

若 $f(x)$ 是可导的奇函数，且 $f'(2)=3$，则 $f'(-2)=$　$\underline{\qquad\quad}$。
?
````````col
```````col-md
flexGrow=20
===

**答案**：$3$

**解析**

> 奇函数的导数为偶函数，故 $f'(-2)=f'(2)=3$。

**考点**：导数的性质（奇偶函数的导数）


```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-21T06:49:28.823Z,8,8.2956,1,2,1,0,0,2026-11-13T06:49:28.823Z,id=t8gwpg-->
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
<!--SR:!fsrs,2026-11-18T08:08:33.703Z,6,8.2956,1,2,1,0,0,2026-11-12T08:08:33.703Z,id=43uu1n-->

zzzz







