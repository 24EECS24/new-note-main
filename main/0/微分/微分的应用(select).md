#flashcards/微分/微分的应用






# 一元函数微分学的应用

# 单调性与极值

$$
\begin{align*}

&\begin{cases}
f'(x) >0 ，f(x)单调增\\[4pt]
f'(x) <0 ，f(x)单调减\\[4pt]

f'(x) =0/不存在
\begin{cases}

\begin{aligned}
&f''(x_0) >0 \\[6pt]
&x=x_0为极小值点 \\[6pt]
\end{aligned}
\begin{cases}
(x_0-\delta, x_0)， f'(x) <0 \\[4pt]
x = x_0， f'(x) =0/不存在 \\[4pt]
(x_0, x_0+\delta)， f'(x) >0
\end{cases}\\[8pt]

\\[8pt]

\begin{aligned}
&f''(x_0) <0 \\[4pt]
&x=x_0为极大值点 \\[4pt]
\end{aligned}
\begin{cases}
(x_0-\delta, x_0)， f'(x) >0 \\[4pt]
x = x_0， f'(x) =0/不存在 \\[4pt]
(x_0, x_0+\delta)， f'(x) <0
\end{cases}\\[6pt]

\end{cases}\\[6pt]

\\[6pt]
\\[6pt]


\begin{aligned}
&n为偶数\\[6pt]
&f^{(n-1)}(x_0) =0\\[6pt]
&f^{(n)}(x_0)\ne  0 \\[6pt]
\end{aligned}
\begin{cases}
\begin{aligned}
&n为偶数\\[6pt]
&f^{(n)}(x_0)< 0 \\[6pt]
\end{aligned}
\Rightarrow 
\begin{aligned}
&f(x)在x=x_0处\\[6pt]
&为极大值 \\[6pt]
\end{aligned}

 \\[10pt]
 \\[10pt]

\begin{aligned}
&n为偶数\\[6pt]
&f^{(n)}(x_0)> 0 \\[6pt]
\end{aligned}
\Rightarrow 
\begin{aligned}
&f(x)在x=x_0处\\[6pt]
&为极小值 \\[6pt]
\end{aligned}
\end{cases}\\[8pt]

\end{cases}\\[6pt]

\end{align*}
$$

## 极值的定义


xxxx

**题目**

函数 $f(x)=|3-2x|$ 在 $x=$ ____ 处取得极小值。
?

````````col
```````col-md
flexGrow=20
===

**答案**：$\dfrac{3}{2}$

**解析**

> $$f(x)=|3-2x|=2\left|x-\frac{3}{2}\right|$$
> 当 $x<\dfrac32$ 时 $f(x)=3-2x$ 递减，当 $x>\dfrac32$ 时 $f(x)=2x-3$ 递增；$x=\dfrac32$ 处为尖点（不可导点），左减右增，由极值第一充分条件知 $f\left(\dfrac32\right)=0$ 为极小值（也是最小值）。
> 故 $f(x)$ 在 $x=\dfrac32$ 处取得极小值。

**考点**

绝对值函数在不可导点处的极值判定
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-30T04:09:42.211Z,10,8.2956,1,2,1,0,0,2026-11-20T04:09:42.211Z,id=239ix6-->


zzzz




对于函数$f(x)$，若存在点$x_0$的某个邻域，使得在该邻域内任意一点$x$均有
$$f(x)\leq f(x_0) \quad \text{或} \quad f(x)\geq f(x_0)$$
成立，则称点$x_0$为$f(x)$的极大值点或极小值点，$f(x_0)$为$f(x)$的极大值或极小值。

### 注
- 极值，是一个局部的概念。
- 极值点左右两侧的邻域有定义，间断点也是双侧邻域有定义的。
- 端点处，不讨论极值点和间断点。
- $\because f(x_0)$要不小于邻域内$f(x)$或不大于邻域内$f(x)$，$\therefore$ 常函数处处是极值。
- 间断点也可以是极值点，相关示例如下：

`````col
````col-md
flexGrow=1
===

1.  $$f(x)=\begin{cases}
1, & x=0 \\
|x|, & x\neq 0
\end{cases}$$
    $x=0$为$f(x)$的可去间断点，也是$f(x)$的极大值点。

````

````col-md
flexGrow=1
===

```tikz
\begin{document}
\begin{tikzpicture}[>=stealth,line cap=round,line join=round,scale=0.85]
\draw[->] (-2.4,0)--(2.4,0) node[right]{$x$};
\draw[->] (0,-0.4)--(0,2.0) node[above]{$y$};
\draw[thick,domain=-2:2,samples=40] plot(\x,{abs(\x)});
\draw[fill=white,thick] (0,0) circle (2.8pt);   % 原点开点
\fill (0,1) circle (2.8pt);                     % f(0)=1 闭点
\node[above right,font=\small] at (0,1){$f(0)=1$};
\end{tikzpicture}
\end{document}
```



````
`````


`````col
````col-md
flexGrow=1
===

2.  $$f(x)=\begin{cases}
1, & x>0 \\
-x, & x\leq 0
\end{cases}$$
    $x=0$是$f(x)$的跳跃间断点，也是$f(x)$的极小值点。

````

````col-md
flexGrow=1
===

```tikz
\begin{document}
\begin{tikzpicture}[>=stealth,line cap=round,line join=round,scale=0.85]
\draw[->] (-1.9,0)--(2.4,0) node[right]{$x$};
\draw[->] (0,-0.4)--(0,1.8) node[above]{$y$};
\draw[thick,domain=-1.5:0,samples=20] plot(\x,{-\x});  % 左段，含(0,0)
\draw[thick,domain=0:2,samples=20] plot(\x,{1});       % 右段 y=1
\fill (0,0) circle (2.8pt);                            % f(0)=0 闭点
\draw[fill=white,thick] (0,1) circle (2.8pt);          % (0,1) 开点
\node[below right,font=\small] at (0,0){$f(0)=0$};
\end{tikzpicture}
\end{document}
```



````
`````



`````col
````col-md
flexGrow=1
===

3.  $$f(x)=\begin{cases}
-1, & x=0 \\
\dfrac{1}{x^2}, & x\neq 0
\end{cases}$$
    $x=0$是$f(x)$的无穷间断点，也是$f(x)$的极小值点。

````

````col-md
flexGrow=1
===

```tikz
\begin{document}

\begin{tikzpicture}[>=stealth,line cap=round,line join=round,scale=0.85]
\clip (-2.6,-1.9) rectangle (2.6,4.1);
\draw[->] (-2.4,0)--(2.4,0) node[right]{$x$};
\draw[->] (0,-1.7)--(0,3.7) node[above]{$y$};
\draw[thick,domain=-2:-0.54,samples=40] plot(\x,{1/(\x*\x)});
\draw[thick,domain=0.54:2,samples=40] plot(\x,{1/(\x*\x)});
\fill (0,-1) circle (2.8pt);                           % f(0)=-1 闭点
\node[below right,font=\small] at (0,-1){$f(0)=-1$};
\end{tikzpicture}

\end{document}
```



````
`````


`````col
````col-md
flexGrow=1
===

4.  $$f(x)=\begin{cases}
2, & x=0 \\
\sin\dfrac{1}{x}, & x\neq 0
\end{cases}$$
    $x=0$是$f(x)$的振荡间断点，也是$f(x)$的极大值点。
````

````col-md
flexGrow=1
===

```tikz
\begin{document}

\begin{tikzpicture}[>=stealth,line cap=round,line join=round,scale=0.85]
\draw[->] (-2.4,0)--(2.4,0) node[right]{$x$};
\draw[->] (0,-1.5)--(0,2.7) node[above]{$y$};
\draw[thick,domain=-2:-0.16,samples=48] plot(\x,{sin((1/\x) r)});
\draw[thick,domain=-0.16:-0.04,samples=48] plot(\x,{sin((1/\x) r)});
\draw[thick,domain=0.04:0.16,samples=48] plot(\x,{sin((1/\x) r)});
\draw[thick,domain=0.16:2,samples=48] plot(\x,{sin((1/\x) r)});
\fill (0,2) circle (2.8pt);                            % f(0)=2 闭点
\node[above right,font=\small] at (0,2){$f(0)=2$};
\end{tikzpicture}

\end{document}
```



````
`````

## 单调性的判别



xxxx

**题目**

函数 $y=3x^4-4x^3$（　　）

A. 在 $(-\infty,1)$ 内单调递减　　B. 在 $(-\infty,0)$ 内单调递增　　C. 在 $(0,+\infty)$ 内单调递减　　D. 在 $(0,+\infty)$ 内单调递增
?

````````col
```````col-md
flexGrow=20
===

**答案**：A

**解析**

> $$y'=12x^3-12x^2=12x^2(x-1)$$
> 当 $x<1$ 且 $x\neq0$ 时，$12x^2>0$、$x-1<0$，故 $y'<0$（$x=0$ 处 $y'=0$，仅为孤立的驻点），$y$ 在 $(-\infty,1)$ 内单调递减，选 A。
> 当 $x>1$ 时 $y'>0$，故 D 的“$(0,+\infty)$ 内单调递增”不成立（$(0,1)$ 内是递减的）。

**考点**

单调区间的判别（驻点处导数为 0 不影响严格单调）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz


xxxx

**题目**

已知 $f(x)=2+x\mathrm{e}^{-x}$，则 $f(x)$ 的单调递减区间为 ____。
?

````````col
```````col-md
flexGrow=20
===

**答案**：$(1,+\infty)$

**解析**

> $$f'(x)=\mathrm{e}^{-x}-x\mathrm{e}^{-x}=(1-x)\mathrm{e}^{-x}$$
> 因 $\mathrm{e}^{-x}>0$，$f'(x)<0\iff1-x<0\iff x>1$。
> 故单调递减区间为 $(1,+\infty)$。

**考点**

单调区间的判别（导函数符号）
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-26T03:59:50.659Z,6,8.2956,1,2,1,0,0,2026-11-20T03:59:50.659Z,id=luzvh2-->


zzzz



设函数$y=f(x)$在$[a,b]$上连续，在$(a,b)$内可导。

严格单调（充要形式）

$$f\ \text{在}\ [a,b]\ \text{严格单调增加} \iff f'(x)\ge 0\ \text{于}\ (a,b)，且\ f'\ \text{不在任何长度大于 0 的子区间上恒等于}\ 0$$

$$f\ \text{在}\ [a,b]\ \text{严格单调减少} \iff f'(x)\le 0\ \text{于}\ (a,b)，且\ f'\ \text{不在任何长度大于 0 的子区间上恒等于}\ 0$$


**理解**：“$f'(x)不在任何长度大于 0 的子区间上恒等于 0$”

`````col
````col-md
flexGrow=2
===

例1：$f(x)=x^4$在$x=0$这一点的变化率

- $f'(0)=0$：$f(x)$ 在 x=0 这一个点的瞬时变化率为 0；
- 但 $f'(x)=4x^3$ 不恒为 0，在 0 两侧变号 
  即，f 的变化率在 0 附近是在变化的；
  
$$
\begin{align*}

&\begin{cases}
(0-\delta, 0)， f'(x) <0 \\[4pt]
x = 0， f'(x) =0 \\[4pt]
(0, 0+\delta)， f'(x) >0
\end{cases}\\[6pt]

\because &f{(x)}' 只在x=0这一点处为0，\\[6pt]
&即:f'(x)不在任何长度大于 0 的子区间上恒等于 0 \\[6pt]
\therefore& \\[6pt]
&在(0-\delta,0]上， f'(x) <0  \implies f(x)严格递减\\[6pt]
&在[0,0+\delta)上， f'(x) >0 \implies f(x)严格递增\\[6pt]

\end{align*}
$$

例2：
函数 $y=x^3$ 在 $(-\infty,+\infty)$ 上连续且可导，
且导函数 $y'=3x^2\geq0$，等号仅在 $x=0$ 处成立，
则函数 $y=x^3$ 在 $(-\infty,+\infty)$ 上严格单调增加。

$$

\begin{cases}
(0-\delta, 0)， f'(x) >0 \\[4pt]
x = 0， f'(x) =0 \\[4pt]
(0, 0+\delta)， f'(x) >0
\end{cases}

$$

````

````col-md
flexGrow=1
===

```tikz
\begin{document}

\begin{tikzpicture}[>=stealth,line cap=round,line join=round,scale=0.9]
\draw[->] (-2.0,0)--(2.0,0) node[right]{$x$};
\draw[->] (0,-0.5)--(0,5.8) node[above]{$y$};
\draw[thick,domain=-1.5:1.5,samples=48] plot(\x,{\x*\x*\x*\x});
\node[above right,font=\small] at (1.12,1.7){$y=x^4$};
\end{tikzpicture}

\end{document}
```

```tikz
\begin{document}

\begin{tikzpicture}[>=stealth,line cap=round,line join=round,scale=0.9]
\draw[->] (-2.2,0)--(2.2,0) node[right]{$x$};
\draw[->] (0,-6.4)--(0,6.4) node[above]{$y$};
\draw[thick,domain=-1.8:1.8,samples=48] plot(\x,{\x*\x*\x});
\node[above right,font=\small] at (1.35,2.6){$y=x^3$};
\end{tikzpicture}
\end{document}
```

````
`````

## 极值的判别



xxxx

**题目**

函数 $y=4\mathrm{e}^{x}+\mathrm{e}^{-x}$ 的极值点坐标是 ____。
?

````````col
```````col-md
flexGrow=20
===

**答案**：$(-\ln2,\,4)$

**解析**

> $$y'=4\mathrm{e}^x-\mathrm{e}^{-x}$$
> 令 $y'=0$：$4\mathrm{e}^x=\mathrm{e}^{-x}$，即 $\mathrm{e}^{2x}=\dfrac14$，得 $x=-\ln2$。
> 又 $y''=4\mathrm{e}^x+\mathrm{e}^{-x}>0$ 恒成立，故 $x=-\ln2$ 处取极小值：
> $$y(-\ln2)=4\cdot\frac12+2=4$$
> 极值点坐标为 $(-\ln2,\,4)$。
>


**求解指数方程** $4e^x - e^{-x}=0$
$$
\begin{align*}
&4e^x - e^{-x} = 0\\[4pt]
&4e^x = e^{-x}\\[4pt]
&4 = e^{-2x}\\[4pt]
&\ln 4 = -2x\\[4pt]
&x = \frac{\ln 4}{-2}\\[4pt]
&\quad = \frac{2\ln 2}{-2}\\[4pt]
&x = -\ln 2
\end{align*}
$$



**考点**

极值点的计算（含指数方程求解）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz



### 必要条件

一阶可导点是极值点的必要条件：
设$f(x)$在$x=x_0$处可导，且在点$x_0$处取得极值，则必有 $f'(x_0)=0$。
即
$$
\begin{cases}
f'(x_0) \text{ 存在} \\
x_0\text{ 为极值点}
\end{cases}
\implies f'(x_0)=0
$$

注：事实上，若$x=x_0$为曲线$y=f(x)$的极值点，则只有以下两种情况：
1.  **驻点**：满足$f'(x_0)=0$，例：$y=x^2$在$(0,0)$处的情形
2.  **不可导点**：满足$f'(x_0)$不存在，例：$y=|x|$在$(0,0)$处的情形

### 判别极值的第一充分条件



xxxx

**题目**

设函数 $y=3x\cdot 3^{x}$ 在点 $x_{0}$ 处取得极小值，则 $x_{0}=$（　　）

A. $-\dfrac{1}{\ln 3}$　　B. $-\ln 3$　　C. $\dfrac{1}{\ln 3}$　　D. $\ln 3$
?

````````col
```````col-md
flexGrow=20
===

**答案**：A

**解析**

> $$y'=3\cdot3^x+3x\cdot3^x\ln3=3\cdot3^x(1+x\ln3)$$
> 令 $y'=0$，因 $3\cdot3^x>0$，得 $1+x\ln3=0$，即 $x=-\dfrac{1}{\ln3}$。
> 当 $x<-\dfrac1{\ln3}$ 时 $1+x\ln3<0$，$y'<0$；当 $x>-\dfrac1{\ln3}$ 时 $y'>0$。左减右增，故 $x_0=-\dfrac{1}{\ln3}$ 处取极小值，选 A。

**考点**

指数函数型极值点的计算（第一充分条件）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz




设$f(x)$在$x=x_0$处连续，（**分段函数时要注意**）
且在$x_0$的某去心邻域$\mathring{U}(x_0,\delta)\ (\delta>0)$内可导

$$
\begin{cases}
x\in (x_0-\delta，x_0)， f'(x) >0 \\
x\in (x_0，x_0+\delta)， f'(x) <0
\end{cases}
\implies f(x)在x=x_0处取得极大值
$$


$$
\begin{cases}
x\in (x_0-\delta，x_0)， f'(x) <0 \\
x\in (x_0，x_0+\delta)， f'(x) >0
\end{cases}
\implies f(x)在x=x_0处取得极小值
$$


$$
\begin{cases}
x\in (x_0-\delta，x_0)， \\
x\in (x_0，x_0+\delta)，
\end{cases}
f'(x)不变号 \implies 则点x_0不是极值点 
$$


### 判别极值的第二充分条件
设$f(x)$在$x=x_0$处二阶可导，
且$f'(x_0)=0$，$f''(x_0)\neq0$

`````col
````col-md
flexGrow=1
===

若$f''(x_0)<0$，
则$f(x)$在$x_0$处取得极大值
**即** 
$斜率f'(x_0)在x=x_0附近在减小$ 
$且斜率f'(x_0)在x=x_0处为0$ 
$$
则必然在
\begin{cases}
x\in (x_0-\delta，x_0)， f'(x) >0 \\
x\in (x_0，x_0+\delta)， f'(x) <0
\end{cases}
$$ 

````

````col-md
flexGrow=1
===

```tikz
\begin{document}

\begin{tikzpicture}[>=stealth,line cap=round,line join=round,scale=1.05]
\draw[->] (-2.4,0)--(2.6,0) node[right]{$x$};
\draw[->] (0,-2.2)--(0,2.7) node[above]{$y$};
\draw[thick,domain=-1.85:1.85,samples=60] plot(\x,{1.6-\x*\x});
\draw[dashed] (-0.85,1.6)--(0.85,1.6);
\fill (0,1.6) circle (2pt);
\node[above right,font=\small] at (0.1,1.62){$f'(x_0)=0$};
\draw[->] (-1.3,0)--(-0.7,1.2);
\node[above left,font=\small] at (-0.72,1.2){$f'(x)>0$};
\draw[->] (0.7,1.2)--(1.3,0);
\node[below right,font=\small] at (1.3,-0.02){$f'(x)<0$};
\node at (0,2.4){$f''(x_0)<0\;\Rightarrow\;\mathrm{Max}$};
\end{tikzpicture}

\end{document}
```



````
`````

`````col
````col-md
flexGrow=1
===

若$f''(x_0)>0$，
则$f(x)$在$x_0$处取得极小值
**即** 
$斜率f'(x_0)在x=x_0附近在增大$ 
$且斜率f'(x_0)在x=x_0处为0$ 
$$
则必然在
\begin{cases}
x\in (x_0-\delta，x_0)， f'(x) <0 \\
x\in (x_0，x_0+\delta)， f'(x) >0
\end{cases}
$$


````

````col-md
flexGrow=1
===

```tikz
\begin{document}

\begin{tikzpicture}[>=stealth,line cap=round,line join=round,scale=1.05]
\draw[->] (-2.4,0)--(2.6,0) node[right]{$x$};
\draw[->] (0,-2.5)--(0,2.3) node[above]{$y$};
\draw[thick,domain=-1.85:1.85,samples=60] plot(\x,{\x*\x-1.6});
\draw[dashed] (-0.85,-1.6)--(0.85,-1.6);
\fill (0,-1.6) circle (2pt);
\node[below right,font=\small] at (0.1,-1.7){$f'(x_0)=0$};
\draw[->] (-1.3,0)--(-0.7,-1.2);
\node[above left,font=\small] at (-1.3,0.05){$f'(x)<0$};
\draw[->] (0.7,-1.2)--(1.3,0);
\node[above right,font=\small] at (1.3,0.05){$f'(x)>0$};
\node at (0,1.95){$f''(x_0)>0\;\Rightarrow\;\mathrm{Min}$};
\end{tikzpicture}

\end{document}
```



````
`````


### 判别极值的第三充分条件
设$f(x)$在$x=x_0$处$n$阶可导，
且$f^{(m)}(x_0)=0 \quad (m=1,2,\dots,n-1)$，
$f^{(n)}(x_0) \neq 0 \quad (n\geq2)$。
- 当$n$为偶数，且$f^{(n)}(x_0)<0$时，$f(x)$在$x_0$处取得极大值。
- 当$n$为偶数，且$f^{(n)}(x_0)>0$时，$f(x)$在$x_0$处取得极小值。


# 凹凸性与拐点


$$
\begin{align*}

&\begin{cases}
f''(x) >0 ，f(x)为凹\\[4pt]
f''(x) <0 ，f(x)为凸\\[4pt]

f''(x) =0/不存在
\begin{cases}

\begin{aligned}
&f'''(x_0) >0 \\[6pt]
&x=x_0为拐点 \\[6pt]
\end{aligned}
\begin{cases}
(x_0-\delta, x_0)， f''(x) <0 \\[4pt]
x = x_0， f''(x) =0/不存在 \\[4pt]
(x_0, x_0+\delta)， f''(x) >0
\end{cases}\\[8pt]

\begin{aligned}
&f'''(x_0) <0 \\[6pt]
&x=x_0为拐点 \\[6pt]
\end{aligned}
\begin{cases}
(x_0-\delta, x_0)， f''(x) >0 \\[4pt]
x = x_0， f''(x) =0/不存在 \\[4pt]
(x_0, x_0+\delta)， f''(x) <0
\end{cases}\\[6pt]

\end{cases}\\[6pt]

\\[6pt]
\\[6pt]


\begin{cases}

\begin{aligned}
&n为奇数\\[6pt]
&f^{(n-1)}(x_0) =0\\[6pt]
&f^{(n)}(x_0)\ne  0 \\[6pt]
\end{aligned}
\Rightarrow 
\begin{aligned}
&f(x)在x=x_0处\\[6pt]
&为拐点 \\[6pt]
\end{aligned}
\end{cases}\\[8pt]

\end{cases}\\[6pt]

\end{align*}
$$

## 凹凸性的定义
**定义1**
设函数$f(x)$在区间$I$上连续，如果对$I$上任意不同两点$x_1,x_2$，恒有
$$f\left(\frac{x_1+x_2}{2}\right) < \frac{f(x_1)+f(x_2)}{2}$$
则称$y=f(x)$在$I$上的图形是凹的。
（凹函数示意图）

如果恒有
$$f\left(\frac{x_1+x_2}{2}\right) > \frac{f(x_1)+f(x_2)}{2}$$
则称$y=f(x)$在$I$上的图形是凸的。
（凸函数示意图）

**注**
事实上，当图形为凹（凸）时，可以将
$$f\left(\frac{1}{2}x_1+\frac{1}{2}x_2\right) \underset{(>)}{<} \frac{1}{2}f(x_1)+\frac{1}{2}f(x_2)$$
更一般地写为
$$f(ax_1+bx_2) \underset{(>)}{<} af(x_1)+bf(x_2)$$
其中，
$$
\begin{cases}
0<a<1\\
0<b<1\\
a+b=1
\end{cases}
$$

**定义2**
设$f(x)$在$[a,b]$上连续，在$(a,b)$内可导，若对$(a,b)$内的任意$x$及$x_0$（$x\neq x_0$）均有
$$f(x_0)+f'(x_0)(x-x_0) \underset{(>)}{<} f(x)$$
则称$f(x)$在$[a,b]$上的图形是凹（凸）的。


### 注
几何意义
曲线在$x=x_0$处的切线的表达式为
$$y-y_0 = k(x-x_0)$$
$$y = k(x-x_0)+y_0$$
$y=f(x_0)+f'(x_0)(x-x_0)$是曲线$y=f(x)$在点$(x_0,f(x_0))$处的切线方程，
因此，该式的几何意义为：
（附凹曲线切线示意图、凸曲线切线示意图）
若曲线$y=f(x)\ (a<x<b)$在任意点处的切线（除该点外）总在曲线的下方（上方），则该曲线是凹（凸）的。

## 拐点的定义
连续曲线的凹弧与凸弧的分界点称为该曲线的拐点。
- 拐点处，只需连续
- 判断拐点时，凹凸不分先后
- 拐点在曲线上，坐标写为$(x_0,f(x_0))$

## 判别凹凸性




xxxx

**题目**

求函数 $y=3x^4-4x^3+2$ 的凹凸区间和拐点。
?

````````col
```````col-md
flexGrow=20
===

**答案**：凹区间 $(-\infty,0)\cup\left(\dfrac23,+\infty\right)$，凸区间 $\left(0,\dfrac23\right)$，拐点 $(0,2)$ 和 $\left(\dfrac23,\dfrac{38}{27}\right)$

**解析**

> $$y'=12x^3-12x^2=12x^2(x-1),\qquad y''=36x^2-24x=12x(3x-2)$$
> 令 $y''=0$，得 $x=0$，$x=\dfrac23$。
> 逐段判号：
> - $x<0$：$12x<0$ 且 $3x-2<0$，$y''>0$，凹；
> - $0<x<\dfrac23$：$12x>0$ 且 $3x-2<0$，$y''<0$，凸；
> - $x>\dfrac23$：$y''>0$，凹。
>
> 凹区间为 $(-\infty,0)\cup\left(\dfrac23,+\infty\right)$，凸区间为 $\left(0,\dfrac23\right)$。
> $$y(0)=2,\qquad y\left(\frac23\right)=3\cdot\frac{16}{81}-4\cdot\frac{8}{27}+2=\frac{16}{27}-\frac{32}{27}+\frac{54}{27}=\frac{38}{27}$$
> 拐点为 $(0,2)$ 和 $\left(\dfrac23,\dfrac{38}{27}\right)$。



**另一解法：** 
$$y' = 12x^3 - 12x^2$$
$$y'' = 36x^2 - 24x$$
$$36x^2 - 24x = 0$$
$$3x^2 - 2x = 0$$
$$x(3x-2) = 0$$
$$x_1 = \frac{2}{3},\ x_2 = 0$$


当$x\in\left(0,\frac{2}{3}\right)$时，$y''<0$，为凸
当$x\in(-\infty,0)\cup\left(\frac{2}{3},+\infty\right)$时，$y''>0$，为凹


$y(0) = 2$，
$$
\begin{align*}
y\left(\frac{2}{3}\right) &= 3\cdot\frac{2^4}{3^4} - 4\cdot\frac{2^3}{3^3} + 2\\[6pt]
&= \frac{2^4(1-2)}{3^3} + \frac{2\cdot 3^3}{3^3}\\[6pt]
&= \frac{-16 + 54}{27}\\[6pt]
&= \frac{38}{27}
\end{align*}
$$








**考点**

凹凸区间与拐点（分段判号）
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-30T04:09:53.349Z,10,8.2956,1,2,1,0,0,2026-11-20T04:09:53.349Z,id=16ecny-->


zzzz




xxxx

**题目**

求曲线 $y=3+\ln(x^{2}+1)$ 的凹凸区间与拐点。
?

````````col
```````col-md
flexGrow=20
===

**答案**：凸区间 $(-\infty,-1)\cup(1,+\infty)$，凹区间 $(-1,1)$，拐点 $(-1,3+\ln2)$ 和 $(1,3+\ln2)$

**解析**

> $$y'=\frac{2x}{x^2+1},\qquad y''=\frac{2(1-x^2)}{(x^2+1)^2}$$
> 令 $y''=0$ 得 $1-x^2=0$，即 $x=\pm1$。
> 当 $x<-1$ 或 $x>1$ 时，$1-x^2<0$，$y''<0$，凸区间为 $(-\infty,-1)\cup(1,+\infty)$；
> 当 $-1<x<1$ 时 $y''>0$，凹区间为 $(-1,1)$。
> 在 $x=\pm1$ 两侧 $y''$ 变号，且 $y(\pm1)=3+\ln2$，故拐点为 $(-1,3+\ln2)$ 和 $(1,3+\ln2)$。


**另一解法：** 
$$
y'=\frac{2x}{x^2+1}
$$

$$
y''=\frac{2(x^2+1)-4x^2}{(x^2+1)^2}
$$

$\because (x^2+1)^2>0$

$\therefore$ 只用看 $2x^2+2-4x^2$

$$
-2x^2+2=0
$$

$$
-x^2+1=0
$$

当 $x\in(-1,1)$ 时，$y''>0$，为凹

当 $x\in(-\infty,-1)\cup(1,+\infty)$ 时，$y''<0$，为凸

$$
y(\pm1)=3+\ln2
$$

$\therefore$ 拐点为 $(-1,3+\ln2)$ 与 $(1,3+\ln2)$





**考点**

凹凸区间与拐点（偶函数，拐点成对出现）
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-30T04:05:58.994Z,10,8.2956,1,2,1,0,0,2026-11-20T04:05:58.994Z,id=fbpuvc-->


zzzz


xxxx

**题目**

曲线 $y=x^{3}(x-4)$ 在区间 $(-\infty,-4)$ 内的性质是（　　）

A. 单调减少，凸的　　B. 单调减少，凹的　　C. 单调增加，凸的　　D. 单调增加，凹的
?

````````col
```````col-md
flexGrow=20
===

**答案**：B

**解析**

> $$y=x^4-4x^3,\qquad y'=4x^3-12x^2=4x^2(x-3)$$
> 当 $x<-4$ 时，$4x^2>0$ 且 $x-3<0$，故 $y'<0$，单调减少。
> $$y''=12x^2-24x=12x(x-2)$$
> 当 $x<-4$ 时，$x<0$ 且 $x-2<0$，两负相乘 $y''>0$，图形为凹的。
> 故在 $(-\infty,-4)$ 内单调减少且为凹的，选 B。

**考点**

单调性与凹凸性的综合判别（一、二阶导符号）
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-27T04:09:47.548Z,7,8.2956,1,2,1,0,0,2026-11-20T04:09:47.548Z,id=dyktso-->


zzzz




xxxx

**题目**

求曲线 $y=3+\mathrm{e}^{\arctan x}$ 的凹凸区间与拐点。
?

````````col
```````col-md
flexGrow=20
===

**答案**：凹区间 $\left(-\infty,\dfrac12\right)$，凸区间 $\left(\dfrac12,+\infty\right)$，拐点 $\left(\dfrac12,\,3+\mathrm{e}^{\arctan\frac12}\right)$

**解析**

> $$y'=\frac{\mathrm{e}^{\arctan x}}{1+x^2}$$
> $$y''=\frac{\mathrm{e}^{\arctan x}\cdot\frac{1}{1+x^2}\cdot(1+x^2)-\mathrm{e}^{\arctan x}\cdot2x}{(1+x^2)^2}=\frac{\mathrm{e}^{\arctan x}(1-2x)}{(1+x^2)^2}$$
> 令 $y''=0$ 得 $1-2x=0$，即 $x=\dfrac12$。
> 当 $x<\dfrac12$ 时 $y''>0$，凹区间为 $\left(-\infty,\dfrac12\right)$；当 $x>\dfrac12$ 时 $y''<0$，凸区间为 $\left(\dfrac12,+\infty\right)$。
> $x=\dfrac12$ 处两侧变号，拐点为 $\left(\dfrac12,\,3+\mathrm{e}^{\arctan\frac12}\right)$。

**考点**

凹凸区间与拐点的计算（商式求导）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz




xxxx

**题目**

求曲线 $y=\dfrac{\mathrm{e}^{x}}{1+x}+3x-5$ 的凹凸区间。
?

````````col
```````col-md
flexGrow=20
===

**答案**：凹区间 $(-1,+\infty)$，凸区间 $(-\infty,-1)$，无拐点

**解析**

> 定义域 $x\neq-1$。
> $$y'=\frac{x\mathrm{e}^x}{(1+x)^2}+3,\qquad y''=\frac{\mathrm{e}^x(1+x^2)}{(1+x)^3}$$
> 因 $\mathrm{e}^x>0$ 且 $1+x^2>0$，$y''$ 的符号只取决于分母 $(1+x)^3$：
> 当 $x>-1$ 时 $y''>0$，凹区间为 $(-1,+\infty)$；
> 当 $x<-1$ 时 $y''<0$，凸区间为 $(-\infty,-1)$。
> $x=-1$ 处函数无定义，不构成拐点，故无拐点。

**考点**

凹凸区间的判定（二阶导符号，无定义点处无拐点）
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-29T04:00:24.055Z,9,8.2956,1,2,1,0,0,2026-11-20T04:00:24.055Z,id=r723tm-->


zzzz





设函数$f(x)$在区间$I$上二阶可导。
- 若在$I$上$f''(x)>0$，则$f(x)$在$I$上的图形是凹的
- 若在$I$上$f''(x)<0$，则$f(x)$在$I$上的图形是凸的

**理解性记忆** 
$\because f''(x)>0$，则$f'(x)$单调递增
则斜率是不断增大的
$\therefore$ 就形成了凹
凸的同理

**想象性记忆** 
将“凹”看成接水的，水越接越多，对应二阶导为正，即$f''(x)>0$。
将“凸”看成倒水的，水越倒越少，对应二阶导为负，即$f''(x)<0$。
## 拐点的判别



xxxx

**题目**

曲线 $y=\dfrac{x^{2}}{2}+4\ln x+\ln 7$ 的拐点为 ____。
?

````````col
```````col-md
flexGrow=20
===

**答案**：$(2,\,2+\ln 112)$

**解析**

> 定义域 $x>0$。
> $$y'=x+\frac{4}{x},\qquad y''=1-\frac{4}{x^2}$$
> 令 $y''=0$ 得 $x^2=4$，即 $x=2$（$x=-2$ 不在定义域内）。
> 当 $0<x<2$ 时 $y''<0$（凸），当 $x>2$ 时 $y''>0$（凹），两侧变号，故 $x=2$ 处为拐点。
> $$y(2)=\frac{4}{2}+4\ln2+\ln7=2+4\ln2+\ln7=2+\ln(16\times7)=2+\ln112$$
> 拐点为 $(2,\,2+\ln112)$。

**考点**

拐点坐标的计算（含对数化简）
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-26T04:01:05.484Z,6,8.2956,1,2,1,0,0,2026-11-20T04:01:05.484Z,id=ez2pfd-->


zzzz




### 必要条件
二阶可导点是拐点的必要条件


设$f''(x_0)$存在，且点$(x_0,f(x_0))$为曲线的拐点，则$f''(x_0)=0$。
即：
$$
\begin{cases}
f''(x_0) \text{ 存在} \\
\text{点}(x_0,f(x_0))\text{ 为拐点}
\end{cases}
\implies f''(x_0)=0
$$

**注**：事实上，若点$(x_0,f(x_0))$为曲线$y=f(x)$的拐点，则只有以下两种情况：
1.  $f''(x_0)=0$，如$y=x^3$在$(0,0)$处的情形（对应$y=x^3$的函数示意图）；
2.  $f''(x_0)$不存在，如$y=\sqrt[3]{x}$在$(0,0)$处的情形
其中，$y'=\frac{1}{3}x^{-\frac{2}{3}}$，$y''=-\frac{2}{9}x^{-\frac{5}{3}}$。
当$x>0$时，$y''<0$；当$x<0$时，$y''>0$。
故点$(0,0)$为曲线$y=\sqrt[3]{x}$的拐点，但在该点的导数不存在。
与极值点类比记忆

### 判别拐点的第一充分条件


xxxx

**题目**

曲线 $y=xe^{-x^2}$ 的拐点个数为（　　）

A. $0$　　B. $1$　　C. $2$　　D. $3$
?

````````col
```````col-md
flexGrow=20
===

**答案**：D（3 个）

**解析**

> 先求一、二阶导数：
> $$y'=e^{-x^2}-2x^2e^{-x^2}=e^{-x^2}(1-2x^2)$$
> $$y''=-2xe^{-x^2}(1-2x^2)-4xe^{-x^2}=2xe^{-x^2}(2x^2-3)$$
> 令 $y''=0$，因 $e^{-x^2}>0$，只需 $x=0$ 或 $2x^2-3=0$，解得三个可疑点 $x=0,\ \sqrt{\frac{3}{2}},\ -\sqrt{\frac{3}{2}}$。
> 逐点检查两侧 $y''$ 符号：$x=0$ 处，左侧（$x<0$）$2x<0$ 且 $2x^2-3<0$，两负相乘 $y''>0$；右侧（$x>0$ 且 $x<\sqrt{\frac32}$）$2x>0$ 而 $2x^2-3<0$，$y''<0$，变号，$(0,0)$ 为拐点。同理 $x=\pm\sqrt{\frac32}$ 处 $y''$ 亦左右异号，均为拐点。
> 故拐点共 3 个，选 D。

**另一解法** 
$$
\begin{align*}
y' &= e^{-x^2} + x\cdot e^{-x^2}\cdot (-2x) \\[4pt]
&= e^{-x^2}(1-2x^2) \\[8pt]
y'' &= -2x e^{-x^2}\cdot(1-2x^2) + e^{-x^2}\cdot (-4x) \\[4pt]
&= -2x e^{-x^2}(-2x^2 + 3)
\end{align*}
$$
要让$y''=0$：
- 要么$-2x^2 + 3 = 0$，
- 要么$-2x e^{-x^2} = 0$。
$-2x^2 + 3 = 0$有2个实根，
$-2x e^{-x^2} = 0$有一个实根$x=0$（因$e^{-x^2}>0$对任意实数$x$恒成立），
共3个$x$点使$y''=0$。



**考点**

拐点的判别（二阶导零点两侧变号）
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-26T07:04:19.249Z,8,8.2956,1,2,1,0,0,2026-11-18T07:04:19.249Z,id=nrhdl1-->


zzzz




设$f(x)$在$x=x_0$处连续，（**分段函数时要注意**）
且在$x_0$的某去心邻域$\mathring{U}(x_0,\delta)\ (\delta>0)$内二阶导数存在，

- 拐点判定（类比）：
  ① 在$x_0$点连续
  ② 左右$f''$变号
  $\implies (x_0,f(x_0))$点为拐点

  符号表示：
  
$$
\begin{cases}
x\in (x_0-\delta，x_0)， f''(x) >0 \\
x\in (x_0，x_0+\delta)， f''(x) <0
\end{cases}
\implies f(x)在x=x_0处取得拐点
$$


$$
\begin{cases}
x\in (x_0-\delta，x_0)， f''(x) <0 \\
x\in (x_0，x_0+\delta)， f''(x) >0
\end{cases}
\implies f(x)在x=x_0处取得拐点
$$


$$
\begin{cases}
x\in (x_0-\delta，x_0)， \\
x\in (x_0，x_0+\delta)，
\end{cases}
f''(x)不变号 \implies 则点x_0不是拐点 
$$




### 判别拐点的第二充分条件
设$f(x)$在$x=x_0$的某邻域内三阶可导，
且$f''(x_0)=0$，$f'''(x_0)\neq0$，
则点$(x_0,f(x_0))$为曲线的拐点。

**理解** 
证明：
若
$\displaystyle f'''(x_0)=\lim_{x \to x_0} \frac{f''(x)-f''(x_0)}{x-x_0} > 0$ 
则$\displaystyle \dfrac{f''(x)}{x-x_0}>0$。

### 判别拐点的第三充分条件


xxxx

**题目**

下列函数中拐点为 $(0,0)$ 的是（　　）

A. $y=x^5$　　B. $y=x^4$　　C. $y=x^{\frac{3}{2}}$　　D. $y=x^{\frac{2}{3}}$
?

````````col
```````col-md
flexGrow=20
===

**答案**：A

**解析**

> A：$y''=20x^3$，$y''(0)=0$，且 $x<0$ 时 $y''<0$、$x>0$ 时 $y''>0$，两侧变号，$(0,0)$ 为拐点。
> B：$y''=12x^2\geq0$，在 $x=0$ 两侧不变号，非拐点。
> C：定义域 $x\geq0$，$x=0$ 无左侧邻域，不构成拐点。
> D：$y''=-\dfrac{2}{9}x^{-\frac{4}{3}}<0$ 恒成立，两侧不变号，非拐点。
> 故选 A。

**考点**

拐点的判别（二阶导在点两侧变号）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz


设$f(x)$在$x_0$处$n$阶可导，
且$f^{(m)}(x_0)=0\ (m=2,3,\dots,n-1)$，
$$f^{(n)}(x_0)\neq0 \quad (n\geq3)$$
则当$n$为奇数时，
点$(x_0,f(x_0))$为曲线的拐点。

# 极值点与拐点的重要结论
（以下结论均可直接使用，不必证明）
- 曲线的可导点不可同时为极值点和拐点
- 曲线的不可导点可同时为极值点和拐点

eg.：
（函数示意图：平面直角坐标系中，$x_0$为尖点（不可导点），曲线在$[0,x_0]$段单调上升、上凸，在$[x_0,+\infty)$段单调下降、下凸，最终趋近于x轴正半轴）
$x_0$为不可导点，同时为极大值点、拐点。

**汇总** 

$$

\begin{align*}



&\begin{cases}
f'(x) >0 ，f(x)单调增\\[4pt]
f'(x) <0 ，f(x)单调减\\[4pt]

f'(x) =0/不存在
\begin{cases}

\begin{aligned}
&f''(x_0) >0 \\[6pt]
&x=x_0为极小值点 \\[6pt]
\end{aligned}
\begin{cases}
(x_0-\delta, x_0)， f'(x) <0 \\[4pt]
x = x_0， f'(x) =0/不存在 \\[4pt]
(x_0, x_0+\delta)， f'(x) >0
\end{cases}\\[8pt]

\\[8pt]

\begin{aligned}
&f''(x_0) <0 \\[4pt]
&x=x_0为极大值点 \\[4pt]
\end{aligned}
\begin{cases}
(x_0-\delta, x_0)， f'(x) >0 \\[4pt]
x = x_0， f'(x) =0/不存在 \\[4pt]
(x_0, x_0+\delta)， f'(x) <0
\end{cases}\\[6pt]

\end{cases}\\[6pt]

\\[6pt]
\\[6pt]


\begin{aligned}
&n为偶数\\[6pt]
&f^{(n-1)}(x_0) =0\\[6pt]
&f^{(n)}(x_0)\ne  0 \\[6pt]
\end{aligned}
\begin{cases}
\begin{aligned}
&n为偶数\\[6pt]
&f^{(n)}(x_0)< 0 \\[6pt]
\end{aligned}
\Rightarrow 
\begin{aligned}
&f(x)在x=x_0处\\[6pt]
&为极大值 \\[6pt]
\end{aligned}

 \\[10pt]
 \\[10pt]

\begin{aligned}
&n为偶数\\[6pt]
&f^{(n)}(x_0)> 0 \\[6pt]
\end{aligned}
\Rightarrow 
\begin{aligned}
&f(x)在x=x_0处\\[6pt]
&为极小值 \\[6pt]
\end{aligned}
\end{cases}\\[8pt]

\end{cases}\\[6pt]



&\\[8pt]
&\\[8pt]



&\begin{cases}
f''(x) >0 ，f(x)为凹\\[4pt]
f''(x) <0 ，f(x)为凸\\[4pt]

f''(x) =0/不存在
\begin{cases}

\begin{aligned}
&f'''(x_0) >0 \\[6pt]
&x=x_0为拐点 \\[6pt]
\end{aligned}
\begin{cases}
(x_0-\delta, x_0)， f''(x) <0 \\[4pt]
x = x_0， f''(x) =0/不存在 \\[4pt]
(x_0, x_0+\delta)， f''(x) >0
\end{cases}\\[8pt]

\begin{aligned}
&f'''(x_0) <0 \\[6pt]
&x=x_0为拐点 \\[6pt]
\end{aligned}
\begin{cases}
(x_0-\delta, x_0)， f''(x) >0 \\[4pt]
x = x_0， f''(x) =0/不存在 \\[4pt]
(x_0, x_0+\delta)， f''(x) <0
\end{cases}\\[6pt]

\end{cases}\\[6pt]

\\[6pt]
\\[6pt]


\begin{cases}

\begin{aligned}
&n为奇数\\[6pt]
&f^{(n-1)}(x_0) =0\\[6pt]
&f^{(n)}(x_0)\ne  0 \\[6pt]
\end{aligned}
\Rightarrow 
\begin{aligned}
&f(x)在x=x_0处\\[6pt]
&为拐点 \\[6pt]
\end{aligned}
\end{cases}\\[8pt]

\end{cases}\\[6pt]




\end{align*}

$$



# 渐近线
当曲线上的点远离原点时，这条曲线与某直线充分靠近，就称这条直线是曲线的渐近线。

## 注
寻找渐近线的顺序：
先找铅直渐近线
$\downarrow$
再找水平渐近线
$\downarrow$
斜渐近线


![[渐近线求解流程.svg|0]]

## 铅直渐近线



xxxx

**题目**

曲线 $y=3x^{2}(x-1)^{-\frac{2}{3}}+3$ 的垂直渐近线为（　　）

A. $x=1$　　B. $x=-1$　　C. $y=3$　　D. 无垂直渐近线
?

````````col
```````col-md
flexGrow=20
===

**答案**：A

**解析**

> 函数在 $x=1$ 处无定义，且
> $$\lim_{x\to1}3x^2(x-1)^{-\frac{2}{3}}=+\infty$$
> （负指数 $\frac23$ 次幂在 $x\to1$ 时趋于无穷大），故 $x=1$ 为垂直渐近线，选 A。
> 其余点处函数均有有限值，不再有其他铅直渐近线。

**另一解法** 
$$
原式=\frac{3x^2}{(x-1)^{\frac{2}{3}}}+3
$$
$x=1$处为无定义点，会使结果为$\infty$。


**考点**

铅直渐近线的判定（无定义点处极限为无穷）
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-29T03:58:14.627Z,9,8.2956,1,2,1,0,0,2026-11-20T03:58:14.627Z,id=f03llg-->



zzzz





xxxx

**题目**

曲线 $y=\dfrac{x^2+x-6}{2-3x+x^2}$ 的铅直渐近线为 ____。
?

````````col
```````col-md
flexGrow=20
===

**答案**：$x=1$

**解析**

> 分母 $2-3x+x^2=(x-1)(x-2)$，分子 $x^2+x-6=(x-2)(x+3)$，可约去 $x-2$，得 $y=\dfrac{x+3}{x-1}\;(x\neq2)$。
> 在 $x=1$ 处：$\lim\limits_{x\to1}\dfrac{x^2+x-6}{(x-1)(x-2)}=\infty$（分子趋于 $-4\neq0$），故 $x=1$ 为铅直渐近线。
> 在 $x=2$ 处：约分后 $\lim\limits_{x\to2}\dfrac{x+3}{x-1}=5$（有限值），$x=2$ 只是可去间断点，不是渐近线。

**另一解法**：找铅直渐近线
$\to$ 找无定义点、分段点、端点
分母为0是无定义点
$$
x^2-3x+2 = (x-2)(x-1)
$$
$x=2$时，分子也为0，可能为等价/同阶无穷小
$x=1$时，分子不为0
$$
\frac{C}{0}=\infty \quad (C \neq 0)
$$
$\Rightarrow x=1$为铅直渐近线




**考点**

铅直渐近线的判定
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-28T08:49:24.608Z,10,8.2956,1,2,1,0,0,2026-11-18T08:49:24.608Z,id=xbtgaj-->




zzzz



若$\lim\limits_{x \to x_0^+} f(x) = \infty$ 或 $\lim\limits_{x \to x_0^-} f(x) = \infty$，
则$x=x_0$为一条铅直渐近线。


注：此处的$x_0$可能是：
- 函数的无定义点
- 函数定义区间的端点
- 分段函数的分段点

## 水平渐近线





xxxx

**题目**

函数 $f(x)=\dfrac{3+4x-x^2}{1-3x+x^2}e^{-x^2}$ 的水平渐近线为 ____。
?

````````col
```````col-md
flexGrow=20
===

**答案**：$y=0$

**解析**

> $$\lim_{x\to\infty}f(x)=\lim_{x\to\infty}\frac{-x^2+4x+3}{x^2-3x+1}\cdot e^{-x^2}$$
> 有理分式分子分母同为二次，极限为 $-1$；而 $e^{-x^2}\to0$（$x\to\infty$）。
> $$(-1)\cdot0=0$$
> 故水平渐近线为 $y=0$。

**考点**

水平渐近线（无穷远极限为有限常数）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz



若$\lim\limits_{x \to +\infty} f(x) = y_1$，则$y=y_1$为一条水平渐近线；
若$\lim\limits_{x \to -\infty} f(x) = y_2$，则$y=y_2$为一条水平渐近线。

若$\lim\limits_{x \to +\infty} f(x) = \lim\limits_{x \to -\infty} f(x) = y_0$，
则$y=y_0$为一条水平渐近线。

## 斜渐近线

$y=f(x)$ 
若$\lim\limits_{x \to +\infty} \frac{f(x)}{x} = a_1 \ (a_1 \neq 0)$，$\lim\limits_{x \to +\infty} \left[f(x) - a_1 x\right] = b_1$，
则$y=a_1 x + b_1$是曲线$y=f(x)$的一条斜渐近线；

若$\lim\limits_{x \to -\infty} \frac{f(x)}{x} = a_2 \ (a_2 \neq 0)$，$\lim\limits_{x \to -\infty} \left[f(x) - a_2 x\right] = b_2$，
则$y=a_2 x + b_2$是曲线$y=f(x)$的一条斜渐近线。

若$\lim\limits_{x \to +\infty} \frac{f(x)}{x} = \lim\limits_{x \to -\infty} \frac{f(x)}{x} = a \ (a \neq 0)$，且
$$\lim_{x \to +\infty} \left[f(x) - a x\right] = \lim_{x \to -\infty} \left[f(x) - a x\right] = b$$
则$y=ax+b$是曲线$y=f(x)$的一条斜渐近线。

### 推导斜渐近线

设曲线$y_1=f(x)$，其斜渐近线为$y_2=ax+b$，
则，$y_1=f(x)与y_2=ax+b在x \to +\infty时无限靠近$ 可得：
$$\lim_{x \to +\infty} \left[f(x)-(ax+b)\right] = 0$$
### 求参数a 
$$\lim_{x \to +\infty} \frac{f(x)-(ax+b)}{x} = 0$$
$$\lim_{x \to +\infty} \left( \frac{f(x)}{x} - a \right) = 0$$
$$a = \lim_{x \to +\infty} \frac{f(x)}{x}$$
即：$y_1=f(x)的斜率与y_2=ax+b的斜率在x \to +\infty时无限接近$ 
### 求参数b
$$\lim_{x \to +\infty} \left[f(x)-ax -b\right] = 0$$
$$b = \lim_{x \to +\infty} \left[f(x)-ax\right]$$
### 发现
当$x \to +\infty$时，$f(x)$与$x$是同阶无穷大：
$f(x)$需要与$x$的一次方同阶；
若$f(x)$增长速度太快，则不会有斜渐近线。

## 综合找渐近线



xxxx

**题目**

$y=\dfrac{3x^{2}-5x}{(x-3)(x+7)}$ 的渐近线有几条（　　）

A. $1$　　B. $2$　　C. $3$　　D. $4$
?

````````col
```````col-md
flexGrow=20
===

**答案**：C

**解析**

> 分母零点 $x=3$ 与 $x=-7$ 处分子均不为 0，故有两条铅直渐近线 $x=3$ 和 $x=-7$。
> $$\lim_{x\to\infty}\frac{3x^2-5x}{(x-3)(x+7)}=\lim_{x\to\infty}\frac{3x^2-5x}{x^2+4x-21}=3$$
> 故有水平渐近线 $y=3$；同方向不再有斜渐近线。
> 共 $3$ 条，选 C。

**考点**

渐近线（铅直+水平）的判定
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz




xxxx

**题目**

曲线 $y=\dfrac{2x^2}{x^2-x-2}$ 的渐近线有 ____ 条。
?

````````col
```````col-md
flexGrow=20
===

**答案**：$3$ 条

**解析**

> 分母 $x^2-x-2=(x-2)(x+1)$，分子在 $x=2,-1$ 处均不为 0，故有两条铅直渐近线 $x=-1$ 与 $x=2$。
> $$\lim_{x\to\infty}\frac{2x^2}{x^2-x-2}=2$$
> 故有水平渐近线 $y=2$；有水平渐近线时同方向无斜渐近线。
> 共 $3$ 条。

**考点**

渐近线（铅直+水平）的判定
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-25T08:50:14.108Z,7,8.2956,1,2,1,0,0,2026-11-18T08:50:14.108Z,id=shx46y-->


zzzz






# 最值或取值范围 

函数单调 $\Rightarrow$ 最值取在定义域端点

最值不取在定义域端点$\iff$最值点取在极值点处 $\Rightarrow$  函数不单调

## 最值的定义 



xxxx

**题目**

$f(x)=\begin{cases}2-x,&0\le x<1\\2,&x=1\\-x+4,&1<x\le2\end{cases}$，则 $f(x)$ 在 $[0,2]$ 上（　　）

A. 无间断点　　B. 有最大值　　C. 有最小值　　D. 既无最大值又无最小值
?

````````col
```````col-md
flexGrow=20
===

**答案**：D

**解析**

> 在 $0\le x<1$ 段，$f(x)=2-x$，函数值落在 $(1,2]$；在 $1<x\le2$ 段，$f(x)=-x+4$，函数值落在 $[2,3)$；$f(1)=2$。
> $x=1$ 处左极限为 $1$、右极限为 $3$，为跳跃间断点（排除 A）。
> 整个函数的值域上确界为 $3$，但 $3$ 只在 $x\to1^+$ 时趋近而取不到；下确界为 $1$，同样取不到。故函数既无最大值又无最小值，选 D。

**考点**

闭区间上不连续函数的最值存在性
> 交叉收录：本题亦收入《连续与间断真题归纳(2016-2026)》（间断点/最值存在性口径）。

```````

```````col-md
flexGrow=1
===





```````
````````


zzzz


xxxx

**题目**

函数 $y=f(x)$，$x\in(a,b)$ 在 $x=x_0$ 处取得最大值，则必有（　　）

A. $f'(x_0)=0$　　B. $f''(x_0)=0$　　C. $f'(x_0)=0$ 且 $f''(x_0)<0$　　D. $f'(x_0)=0$ 或 $f'(x_0)$ 不存在
?

````````col
```````col-md
flexGrow=20
===

**答案**：D

**解析**

> $x_0$ 是开区间 $(a,b)$ 内部的最大值点，故 $x_0$ 必为极值点。极值点只有两种可能：驻点（$f'(x_0)=0$）或不可导点（$f'(x_0)$ 不存在），故选 D。
> A 不完整（漏掉不可导情形）；B、C 与最值无必然联系。

**考点**

极值点的必要条件（驻点或不可导点）
> 交叉收录：本题亦收入《中值定理与微分等式不等式真题归纳(2016-2026)》（费马定理/极值必要条件口径）。

```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-24T08:50:27.095Z,6,8.2956,1,2,1,0,0,2026-11-18T08:50:27.095Z,id=giba8k-->


zzzz


设$x_0$为$f(x)$定义域内一点，若对$f(x)$的定义域内任意一点$x$，均有$f(x) \leq f(x_0)$（或$f(x) \geq f(x_0)$）成立，则称$f(x_0)$为$f(x)$的最大值（或最小值）。
最值是一个整体的概念
极值是一个局部的概念
**注：极值与最值的关系**
例：$f(x)=e^x$，$x \in [0,+\infty)$，$x=0$为其最小值点，且没有最大值点。
（对应函数示意图）
因为$x=0$点为端点，所以$x=0$点不为极值点，因此：
最值点不一定为极值点。

例：$f(x)=3x-x^3$，有$f'(x)=3(1-x^2)$
$$f''(x) = -6x,\quad f'(\pm 1) = 0,\quad f''(1) = -6,\, f''(-1) = 6$$
$\Rightarrow f(1)=2$为极大值
$f(-1)=-2$为极小值
但$f(x)$在$(-\infty,+\infty)$内无最值
即：极值点并不一定是最值点
最值点并不一定是极值点
但是，下面这个结论是正确的：
如果$f(x)$在区间$I$上有最值点$x_0$，并且此最值点$x_0$不是区间$I$的端点，而是$I$内部的点，那么此$x_0$必是$f(x)$的一个极值点。

## 求开区间内连续函数的最值


xxxx

**题目**

函数 $f(x)=x-\sin^2 x$ 在区间 $[0,\frac{\pi}{2}]$ 上的最大值为 ____。
?

````````col
```````col-md
flexGrow=20
===

**答案**：$\dfrac{\pi}{2}-1$

**解析**

> $$f'(x)=1-2\sin x\cos x=1-\sin 2x$$
> 在 $[0,\frac{\pi}{2}]$ 上 $\sin 2x\in[0,1]$，故 $f'(x)=1-\sin 2x\geq0$ 恒成立（仅在 $x=\frac{\pi}{4}$ 处取 0），$f(x)$ 单调递增，最大值在右端点取得：
> $$f\left(\frac{\pi}{2}\right)=\frac{\pi}{2}-\sin^2\frac{\pi}{2}=\frac{\pi}{2}-1$$

**考点**

闭区间上连续函数的最值（单调性判最值）
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-27T08:49:19.475Z,9,8.2956,1,2,1,0,0,2026-11-18T08:49:19.475Z,id=ed5waz-->


zzzz




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


# 作函数图像（这是基本功）



xxxx

**题目**

设 $a<x<b$，$f'(x)<0$，$f''(x)<0$，在区间 $(a,b)$ 内，函数 $y=f(x)$ 的图形（　　）

A. 沿 $x$ 轴正向下降且为凹的　　B. 沿 $x$ 轴正向下降且为凸的　　C. 沿 $x$ 轴正向上升且为凹的　　D. 沿 $x$ 轴正向上升且为凸的
?

````````col
```````col-md
flexGrow=20
===

**答案**：B

**解析**

> $f'(x)<0$ 说明函数沿 $x$ 轴正向单调下降；$f''(x)<0$ 说明图形为凸的（斜率递减，曲线向下弯）。
> 故图形沿 $x$ 轴正向下降且为凸的，选 B。

**考点**

一、二阶导符号与图形形态的对应
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-30T04:00:04.206Z,10,8.2956,1,2,1,0,0,2026-11-20T04:00:04.206Z,id=0fcz0g-->


zzzz




- 函数$f(x)$作图的一般步骤
  1.  确定定义域、值域，考查函数是否有奇偶性、周期性，并用好图像变换。
  （注：图像变换相关内容后面马上说。）


## 用导数工具
- 一阶导数确定函数的单调区间、极值点
- 二阶导数确定曲线的凹凸区间、拐点

## 考查渐近线

## 作出函数图像

## 图像变换方式一般有三种
### 平移变换（左加右减，上加下减）
- 将函数$y=f(x)$的图像沿$x$轴向左平移$x_0$（$x_0>0$）个单位长度，得到函数$y=f(x+x_0)$的图像
- 将函数$y=f(x)$的图像沿$x$轴向右平移$x_0$（$x_0>0$）个单位长度，得到函数$y=f(x-x_0)$的图像
- 将函数$y=f(x)$的图像沿$y$轴向上平移$y_0$（$y_0>0$）个单位长度，得到函数$y=f(x)+y_0$的图像
- 将函数$y=f(x)$的图像沿$y$轴向下平移$y_0$（$y_0>0$）个单位长度，得到函数$y=f(x)-y_0$的图像

### 对称变换
- 将函数$y=f(x)$的图像关于$x$轴对称，得到函数$y=-f(x)$的图像
- 将函数$y=f(x)$的图像关于$y$轴对称，得到函数$y=f(-x)$的图像
- 将函数$y=f(x)$的图像关于原点对称，得到函数$y=-f(-x)$的图像


## 函数图像的常见变换作法
1.  反函数图像变换：将函数$y=f(x)$的图像关于直线$y=x$对称，得到函数$y=f^{-1}(x)$的图像，这其实就是$y=f(x)$的反函数的图像。
    对应函数示意图：展示$y=f(x)$、反函数$y=f^{-1}(x)$与对称轴$y=x$的位置关系
2.  $y=|f(x)|$的图像作法：保留函数$y=f(x)$在$x$轴及$x$轴上方的部分，把$x$轴下方的部分关于$x$轴对称到$x$轴上方，并去掉原来下方的部分，就得到函数$y=|f(x)|$的图像。
    对应函数示意图：$y=|f(x)|$的图像变换示意
3.  $y=f(|x|)$的图像作法：保留函数$y=f(x)$在$y$轴及$y$轴右侧的部分，去掉$y$轴左侧的部分，再将$y$轴右侧图像关于$y$轴对称到$y$轴左侧，就得到函数$y=f(|x|)$的图像。
    对应函数示意图：$y=f(|x|)$的图像变换示意

> 注：将$y=f(x)$移项可写为隐函数形式$F(x,y) = f(x) - y = 0$，下述对称性判定均基于该隐函数形式。

## 函数对称性的隐函数判定
1.  若$F(x,y) = F(-x,y)$，则$y=f(x)$关于$y$轴对称。
2.  若$F(x,y) = F(x,-y)$，则$y=f(x)$关于$x$轴对称。
3.  若$F(x,y) = F(-x,-y)$，则$y=f(x)$关于$(0,0)$点中心对称。
4.  若$F(x,y) = F(y,x)$，则$y=f(x)$关于直线$y=x$对称。
5.  若$F(x,y) = F(2T-x,y)$或$F(T+x,y) = F(T-x,y)$，则$y=f(x)$关于直线$x=T$对称（该结论是在$y=f(x)$关于$y$轴对称的基础上，进行左右平移得到的）。
6.  若$F(x,y) = F(x,2T-y)$或$F(x,T+y) = F(x,T-y)$，则$y=f(x)$关于直线$y=T$对称（该结论是在$y=f(x)$关于$x$轴对称的基础上，进行上下平移得到的：由原来的关于$y=0$对称，变为关于$y=T$对称）。
7.  若$F(a+x,y) = F(a-x,-y)$，则$y=f(x)$关于$(a,0)$点中心对称（该结论是在$y=f(x)$关于$(0,0)$点中心对称的基础上，进行左右平移得到的）。


## 伸缩变换（类似于上加下减，左加右减）
## 水平伸缩
$y=f(kx)\ (k>1)$的图像，可由$y=f(x)$的图像上每点的横坐标缩短到原来的$\frac{1}{k}$倍且纵坐标不变得到。
（水平伸缩函数示意图：虚线为$y=f(x)$，实线为$y=f(kx)\ (k>1)$）
$y=f(kx)\ (0<k<1)$的图像，可由$y=f(x)$的图像上的每点的横坐标伸长到原来的$\frac{1}{k}$倍，且纵坐标不变得到。
记法：
左加$\sim$
$$
\begin{cases}
y=f(kx)\ (k>1),\ k\uparrow \\
y=f\left(\frac{1}{k}x\right)\ (k>1),\ k\downarrow
\end{cases}
$$
图像被向左压窄
右减$\sim$
$$
\begin{cases}
y=f(kx)\ (k>1),\ k\downarrow \\
y=f\left(\frac{1}{k}x\right)\ (k>1),\ k\uparrow
\end{cases}
$$
图像被向右拉宽
## 垂直伸缩
$y=kf(x)\ (k>1)$的图像，可由$y=f(x)$的图像上每点的纵坐标伸长到原来的$k$倍且横坐标不变得到。
$y=kf(x)\ (0<k<1)$的图像，可由$y=f(x)$的图像上每点的纵坐标缩短到原来的$k$倍且横坐标不变得到。
（垂直伸缩函数示意图：虚线为$y=f(x)$，实线为$y=kf(x)\ (k>1)$）
记法：
上加$\sim$
$$
\begin{cases}
y=kf(x)\ (k>1),\ k\uparrow \\
y=\frac{1}{k}f(x)\ (k>1),\ k\downarrow
\end{cases}
$$
图像拉高
下减$\sim$
$$
\begin{cases}
y=kf(x)\ (k>1),\ k\downarrow \\
y=\frac{1}{k}f(x)\ (k>1),\ k\uparrow
\end{cases}
$$
图像拉低


例5.11 画出$y^2=(1-x^2)^3$的图像
解：①
$$
\begin{aligned}
\because F(-x,y)&=F(x,y)\\
F(x,-y)&=F(x,y)\\
F(-x,-y)&=F(x,y)
\end{aligned}
$$
$\therefore f(x)$关于$y$轴、$x$轴、原点对称
$\therefore$ 我们只用画出其第一象限的图像，再利用图像变换即可

则我们只用看第一象限，即$x\geq0,\ y\geq0$（不用加绝对值）
$$
\begin{aligned}
\implies y^2&=(1-x^2)^3\\
y&=(1-x^2)^{\frac{3}{2}}
\end{aligned}
$$
且$x=1$时$y=0$

②
$$y'=\frac{3}{2}\sqrt{1-x^2}\cdot(-2x)$$
令$y'=0$
解出$x=0$（驻点）
当$x=0$时，$y=1$

$$y''=3\cdot\frac{2x^2-1}{\sqrt{1-x^2}}$$
令$y''=0$
解出$x=\frac{\sqrt{2}}{2}$
当$x=\frac{\sqrt{2}}{2}$时，$y=\left(\frac{1}{2}\right)^{\frac{3}{2}}$
$\implies$ 拐点$\left(\frac{\sqrt{2}}{2}, \left(\frac{1}{2}\right)^{\frac{3}{2}}\right)$

在$x\in\left(0,\frac{\sqrt{2}}{2}\right)$时$y''<0$，图为凸的
在$x>\frac{\sqrt{2}}{2}$时$y''>0$，图为凹的

$\implies$ 大概图像（函数示意图）


## 例5.12
画出$y=x^x\ (x>0)$的图像
解：
① 定义域：$x\in(0,+\infty)$
恒等变形得：
$$y=x^x = e^{x\ln x}$$
② 求一阶导数：
$$y'=x^x(\ln x + 1)$$
令$y'=0$，解得$x=\frac{1}{e}$。
$\because \ln x$为增函数，
$\therefore$ 当$x\in(0,\frac{1}{e})$时，$y'<0$；
当$x\in(\frac{1}{e},+\infty)$时，$y'>0$。
$\therefore x=\frac{1}{e}$为唯一的极小值点。
求二阶导数：
$$y''=x^x(\ln x+1)^2 + x^{x-1} > 0$$
因此函数为凹函数。
③ 极限趋势分析：
$$\lim_{x\to0^+} x^x = e^{\lim_{x\to0^+} x\ln x}=1$$
$$\lim_{x\to+\infty} x^x = e^{\lim_{x\to+\infty} x\ln x}=+\infty$$
$$\lim_{x\to+\infty} \frac{x^x}{x}=\infty$$
说明$x\to+\infty$时$x^x$趋向无穷的速度太快。
函数示意图：极小值点位于$x=\frac{1}{e}$处，$x\to0^+$时函数值趋近于1（对应点为空心点），$(0,\frac{1}{e})$段递减，$(\frac{1}{e},+\infty)$段递增，曲线为凹形。

## 例5.13
画出$y=\frac{e^x}{x}$的图像
解：
① 定义域：$x\neq0$，即$x\in(-\infty,0)\cup(0,+\infty)$
② 求一阶导数：
$$y'=\frac{e^x(x-1)}{x^2}$$
令$y'=0$，得$x=1$（驻点）
（$y'$不存在的点：$x=0$）


当$x<1$时，$y'<0$
当$x>1$时，$y'>0$

$$y''=\frac{e^x(x^2-2x+2)}{x^3}=\frac{e^x\left[(x-1)^2+1\right]}{x^3}$$

当$x>0$时，$y''>0$
当$x<0$时，$y''<0$
（$y''$不存在的点：$x=0$）

③ 极限分析：
$$\lim_{x \to -\infty} \frac{e^x}{x}=0$$
在$x \to \infty$时，无穷大增长阶比较：$\ln^\alpha x \ll x^\beta \ll a^x \ll x^x$
$$\lim_{x \to 0^-} \frac{e^x}{x}=-\infty$$
$$\lim_{x \to 0^+} \frac{e^x}{x}=+\infty$$
$$\lim_{x \to +\infty} \frac{e^x}{x}=+\infty$$

$\Rightarrow$ 函数$y=\frac{e^x}{x}$的示意图：平面直角坐标系$xOy$中，$x>0$区间内曲线在$x=1$处取得极小值$e$，$x \to 0^+$时$y \to +\infty$，$x \to +\infty$时$y \to +\infty$，曲线为凹；$x<0$区间内$x \to -\infty$时$y \to 0$，$x \to 0^-$时$y \to -\infty$，曲线为凸。

## 参数方程作图的一般步骤
- 描点法
- 化为：
$$
\begin{cases}
\text{直角坐标方程} \\
\text{极坐标方程}
\end{cases}
$$

例：
参数方程为
$$
\begin{cases}
x=\sin t \\
y=\cos^3 t
\end{cases} \quad (0 \leq t \leq 2\pi)
$$
化为直角坐标方程为：
$$y^2=(1-x^2)^3$$



# 二元函数的应用
## 极值与最值的概念
### 极值
若存在点$(x_0,y_0)$的某个邻域，使得在该邻域内任意一点$(x,y)$，均有
$$f(x_0,y_0)\geq f(x,y) \quad \text{或} \quad f(x_0,y_0)\leq f(x,y)$$
成立，则称点$(x_0,y_0)$为$f(x,y)$的极大值点/极小值点，$f(x_0,y_0)$为$f(x,y)$的极大值/极小值。

### 最值
设点$(x_0,y_0)$为$f(x,y)$定义域内一点，若对于$f(x,y)$的定义域内任意一点$(x,y)$，均有
$$f(x_0,y_0)\geq f(x,y) \quad \text{或} \quad f(x_0,y_0)\leq f(x,y)$$
成立，则称$f(x_0,y_0)$为$f(x,y)$的最大值/最小值。

**理解**
- 极值：你在你周围的同学中，分最高
- 最值：你在你全班的同学中，分最高
- 就比如说：你的脸是一个三维面，脸上长了好几个小痘痘，每个小痘痘上都有一个极大值点，但整个脸上只有一个最大值点。


## 多元函数极值判别

### 结论 
二元函数$f(x,y)$在点$(x_0,y_0)$处取得极值，
是一元函数$f(x,y_0)$和$f(x_0,y)$分别在$x_0$和$y_0$处取得极值的*充分不必要条件*

**理解** 
二元函数$f(x,y)$的图像位于三维坐标系中，$z=f(x_0,y)$是该曲面上的曲线：
在$x=x_0$处插一个与$y$轴平行的截面，
在这个截面上，
该曲线对应二维坐标系中的一元函数$f(x_0,y)$，
其中，$z$随$y$的变化而变化，
在$y=y_0$时，
$z$取极值$f(x_0,y_0)$。
$z=f(x,y_0)$的图象
是在三维坐标系中的二元函数$f(x,y)$上，在$y=y_0$处插一个与$x$轴平行的截面。
在这个截面上
就是一个二维坐标系中的一元函数$f(x,y_0)$
其中，$z$随$x$的变化而变化
在$x=x_0$时，$z$取得极值$f(x_0,y_0)$ 

充分条件是显然的
因为在所有方向上，$f(x_0,y_0)$都为极值
那么，在$x$轴、$y$轴方向上依旧为极值
反过来看是不行的
因为只能确定在$x$轴、$y$轴方向上
$f(x_0,y_0)$为极值
不能确定在所有方向上
$f(x_0,y_0)$为极值

### 必要条件

若$z=f(x,y)$在点$(x_0,y_0)$处满足：

$$
\begin{cases}
\text{一阶偏导数存在} \\
\text{取极值}
\end{cases}
\implies f_x'(x_0,y_0)=0,\ f_y'(x_0,y_0)=0
$$

且有如下推出关系：
$$\begin{cases}
f_x'(x_0,y_0)=0 \\
f_y'(x_0,y_0)=0
\end{cases} \Rightarrow \begin{matrix}
z=f(x,y)\text{在点}(x_0,y_0)\text{处} \\
\text{的切平面水平}
\end{matrix}$$

**注**：偏导数不存在的点也可能为极值点。(这些为*可疑点*)
eg：圆锥的尖点，$z=\sqrt{x^2+y^2}$在点$(x_0,y_0)$处取极小值。
$$\begin{cases}
f_x'\text{不存在} \\
f_y'\text{不存在}
\end{cases} \nRightarrow z=f(x,y)\text{在点}(x_0,y_0)\text{处取极值}$$
$$\begin{cases}
f_x'(x_0,y_0)=0 \\
f_y'(x_0,y_0)=0
\end{cases} \nRightarrow z=f(x,y)\text{在点}(x_0,y_0)\text{处取极值}$$

eg：
- $f(x,y)=x^3+y^3$
- $f(x,y)=x^2-y^2$

只能说：
$$\begin{cases}
f_x'(x_0,y_0)=0 \\
f_y'(x_0,y_0)=0
\end{cases}\text{的点}(x_0,y_0)$$
$$\begin{cases}
f_x'\text{不存在} \\
f_y'\text{不存在}
\end{cases}\text{的点}(x_0,y_0)$$
为可疑点，即可能为极值点的点。


### 判断可疑点是否为极值点（Δ判别法）





xxxx

**题目**

若函数 $f(x,y)$ 在点 $(x_{0},y_{0})$ 处具有一阶与二阶偏导数且取极小值，则（　　）

A. $f_{x}(x_{0},y_{0})=f_{y}(x_{0},y_{0})=0$

B. 若 $(x_{0},y_{0})$ 是 $D$ 内唯一极值点，则必为最小值点

C. $f_{xx}(x_{0},y_{0})\cdot f_{yy}(x_{0},y_{0})-\left[f_{xy}(x_{0},y_{0})\right]^{2}>0$，且 $f_{xx}(x_{0},y_{0})>0$

D. $f_{xx}(x_{0},y_{0})\cdot f_{yy}(x_{0},y_{0})-\left[f_{xy}(x_{0},y_{0})\right]^{2}>0$，且 $f_{xx}(x_{0},y_{0})<0$
?

````````col
```````col-md
flexGrow=20
===

**答案**：C

**解析**

> 二元函数极值的第二充分条件：若在点 $(x_0,y_0)$ 处 $\Delta=AC-B^2>0$（其中 $A=f_{xx},\ B=f_{xy},\ C=f_{yy}$），则取极值；$\Delta>0$ 时 $A$ 与 $C$ 同号，$A>0$（或 $C>0$）对应极小值，$A<0$ 对应极大值。
> 故极小值应满足 $\Delta>0$ 且 $f_{xx}>0$，选 C。
> A 只是必要条件（驻点条件），不充分；B 中“唯一极值点必为最值点”在无界区域上不成立；D 是极大值的充分条件。

**考点**

二元函数极值的第二充分条件（Δ 判别法）
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-26T04:01:09.913Z,6,8.2956,1,2,1,0,0,2026-11-20T04:01:09.913Z,id=4f6udb-->


zzzz






xxxx

**题目**

已知二元函数 $f(x,y)=3y^{2}+6xy-x^{3}+5$，求极值点与极值。
?

````````col
```````col-md
flexGrow=20
===

**答案**：$(0,0)$ 为鞍点（非极值点）；$(-2,2)$ 为极小值点，极小值为 $1$

**解析**

> 求驻点：
> $$f_x=6y-3x^2=0,\qquad f_y=6y+6x=0$$
> 由 $f_y=0$ 得 $y=-x$，代入 $f_x=0$：$-6x-3x^2=0$，即 $x(x+2)=0$。
> 驻点为 $(0,0)$ 和 $(-2,2)$。
> 二阶偏导：$f_{xx}=-6x$，$f_{xy}=6$，$f_{yy}=6$。
> 在 $(0,0)$：$\Delta=f_{xx}f_{yy}-f_{xy}^2=0-36=-36<0$，为鞍点（非极值）。
> 在 $(-2,2)$：$f_{xx}=12$，$\Delta=12\times6-36=36>0$，且 $f_{xx}>0$，为极小值点。
> $$f(-2,2)=3\times4+6\times(-4)-(-8)+5=12-24+8+5=1$$
> 故极小值点为 $(-2,2)$，极小值为 $1$。

**考点**

二元函数极值（驻点 + Δ 判别法，鞍点排除）
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-30T04:09:35.002Z,10,8.2956,1,2,1,0,0,2026-11-20T04:09:35.002Z,id=7zp13u-->


zzzz



xxxx

**题目**

设 $f(x,y)=x^2+2y^2-2x+4y+3$，则点 $(1,-1)$（　　）

A. 是极大值点　　B. 是极小值点　　C. 不是驻点　　D. 是驻点但非极值点
?

````````col
```````col-md
flexGrow=20
===

**答案**：B

**解析**

> $$f_x=2x-2,\qquad f_y=4y+4$$
> 令 $f_x=f_y=0$，得驻点 $(1,-1)$，排除 C。
> 二阶偏导：$A=f_{xx}=2$，$B=f_{xy}=0$，$C=f_{yy}=4$。
> $$\Delta=AC-B^2=8=8>0$$
> $\Delta>0$ 且 $A=2>0$，由判别法知 $(1,-1)$ 为极小值点，选 B。

**考点**

二元函数极值的 Δ 判别法（$AC-B^2$）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz



xxxx

**题目**

若函数 $f(x,y)=e^x(ax-b+y^2)$ 在 $(1,0)$ 处取得极值 $-e$，则 $a,b=$（　　）

A. $a=-1,b=2$　　B. $a=-1,b=-2$　　C. $a=1,b=-2$　　D. $a=1,b=2$
?

````````col
```````col-md
flexGrow=20
===

**答案**：D

**解析**

> $f(1,0)=e(a-b)=-e$，则 $a-b=-1$。
> $$f'_x=e^x(ax-b+y^2)+ae^x=e^x(ax+a-b+y^2)$$
> 由极值必要条件 $f'_x(1,0)=e(2a-b)=0$，得 $2a-b=0$；又 $f'_y=2y\,e^x$，$f'_y(1,0)=0$ 自动成立。
> 联立 $\begin{cases}a-b=-1\\2a-b=0\end{cases}$，解得 $a=1,b=2$，选 D。
> 检验：$f''_{xx}=e^x(ax-b+y^2+2a)$，$f''_{xx}(1,0)=e(1-2+2)=e>0$；$f''_{xy}(1,0)=0$；$f''_{yy}(1,0)=2e$。$AC-B^2=2e^2>0$，故确为极小值，且 $f(1,0)=e(1-2)=-e$ 与题设吻合。
>


**考点**

二元函数极值的必要条件与充分条件（驻点 + $AC-B^2$ 判别）
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-24T08:49:14.127Z,6,8.2956,1,2,1,0,0,2026-11-18T08:49:14.127Z,id=gx7gwa-->


zzzz






$$
\begin{cases}
f_{xx}''(x_0,y_0)=A \\
f_{xy}''(x_0,y_0)=B \\
f_{yy}''(x_0,y_0)=C
\end{cases}
\quad \Delta=AC-B^2
$$
若：
- $\Delta>0 \implies$ 极值，其中：
  $$
  \begin{cases}
  A<0 \ \text{或} \ C<0 \implies \text{极大值} \\
  A>0 \ \text{或} \ C>0 \implies \text{极小值}
  \end{cases}
  $$
- $\Delta<0 \implies$ 不是极值
- $\Delta=0 \implies$ 方法失效，另谋它法
**理解** 
$$
\begin{aligned}
AC-B^2 &> 0 \\
\implies AC &> B^2
\end{aligned}
$$
$\because B^2\geq0$
$\therefore A$与$C$同号。
若$\Delta>0 \implies A$与$C$同号。
### 总结
找$z=f(x,y)$的极值点的思路：
- 找可能为极值点的可疑点：
  即满足
  $$\begin{cases}
  f_x'(x_0,y_0)=0 \\
  f_y'(x_0,y_0)=0
  \end{cases}$$
  的点，
  或满足
  $$\begin{cases}
  f_x' \text{不存在} \\
  f_y' \text{不存在}
  \end{cases}$$
  的点。
- 找确定为极值点的点：
  即满足$\Delta>0$的点。
因此极值点满足：
$$
\begin{cases}
f_x'=0 \ \text{或} \ f_x' \text{不存在} \\
f_y'=0 \ \text{或} \ f_y' \text{不存在} \\
\Delta>0
\end{cases}
$$

## 二元函数求最值

求二元函数$z = g(x,y)$的最值
### 一、求在某个路径上的最值




xxxx

**题目**

函数 $z=2x^{2}+3xy-4x-15$ 在条件 $2x-y=4$ 下的最小值为（　　）

A. $-23$　　B. $-17$　　C. $-15$　　D. $-11$
?

````````col
```````col-md
flexGrow=20
===

**答案**：A

**解析**

> 由条件 $2x-y=4$ 得 $y=2x-4$，代入目标函数化为一元函数：
> $$z=2x^2+3x(2x-4)-4x-15=8x^2-16x-15$$
> $$z'=16x-16=0\ \Rightarrow\ x=1$$
> 且 $z''=16>0$，为最小值点：
> $$z(1)=8-16-15=-23$$
> 或配方：$z=8(x-1)^2-23\geq-23$，当 $x=1$ 时取最小值 $-23$，选 A。

**考点**

条件极值（代入法化为一元函数求最值）
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-26T04:09:45.715Z,6,8.2956,1,2,1,0,0,2026-11-20T04:09:45.715Z,id=jzlwmn-->


zzzz




**1**.  路径为显函数$y=f(x)$ 
将路径代入二元函数，转化为一元函数求最值：
$$
\begin{align*}
z &= g(x,y) \\
&= g\left[x,f(x)\right] \\
&= w(x)
\end{align*}
$$
即求解一元函数$z=w(x)$的最值。
**2**.  路径为隐函数$F(x,y)=0$ 
若隐函数难以显化，或显化后表达式过于复杂，
可使用拉格朗日乘数法求解，无需解出显式$y=f(x)$。
> 代入法是在减少变量，拉格朗日乘数法是在增加变量。


引入变量$\lambda$，构造函数：
$$W(x,y,\lambda) = g(x,y) + \lambda F(x,y)$$
令：
$$
\begin{cases}
W'_x = g'_x + \lambda F'_x = 0 \\
W'_y = g'_y + \lambda F'_y = 0 \\
W'_\lambda = F(x,y) = 0
\end{cases}
$$
1. *用前两个方程消掉 $\lambda$* 
 $把 W'_x=0、W'_y=0 移项成 g'_x=-\lambda F'_x、g'_y=-\lambda F'_y，$ 
 $两式相除，\lambda 直接消失，得到x,y 的一个关系式$；
2. *把这个关系代回 $W'_\lambda=0$*，
 $解出具体的 (x,y)—— 候选点$；
 
比较这些点的函数值，得到最值点。

**注**：路径由两个或多个隐函数约束的情况
若路径由两个隐函数给出：
$$
\begin{cases}
F(x,y)=0 \\
G(x,y)=0
\end{cases}
$$
引入两个变量$\lambda,\mu$，构造函数：
$$W(x,y,\lambda,\mu) = g(x,y) + \lambda F(x,y) + \mu G(x,y)$$
列方程组并求解：
$$
\begin{cases}
W'_x = 0 \\
W'_y = 0 \\
W'_\lambda = 0 \\
W'_\mu = 0
\end{cases}
$$

同理
有$n$个约束就多加$n$个自变量，
自变量个数 $=$ 目标函数的自变量个数 $+$ 约束条件的个数，
自变量有$n$个就求$n$个一阶偏导数。

### 二、求在某区域$D$上的最值
**1**.  求区域$D$内部的最值点：
找出$D$内所有驻点(可疑点)，
即满足
$$g'_x(x,y)=0,且 g'_y(x,y)=0，或g'_x,g'_y不存在$$
的点，
比较这些点的函数值，得到内部的最值点。

**2**.  求区域$D$边界上的最值点：
$D$的边界是$xOy$平面上的一个函数
即：路径$F(x,y)=0$，
也就是求在这条路径上的最值，
按照「(一)求在某个路径上的最值」的方法计算即可。
**3**.  最后
再将内部的最值点的函数值与边界的最值点的函数值进行比较，
最终得到整个区域$D$上的最值。
**与一元函数求法 compare** 
- 根据$f'(x)$为0或不存在，求可疑点。
- 取端点为可疑点。
- 比较所有可疑点的函数值。

### 最远(近)点的垂线原理
“此原理可直接用”，用好此原理，可在多元最值问题上节约大量时间，提高效率。

- 如果$T$是光滑闭曲线，点$Q$是$T$外的一个点，点$P_1,P_2$分别是$T$上与$Q$的最远点与最近点，则直线$P_1Q,P_2Q$分别在点$P_1,P_2$处与$T$垂直，即$P_1Q,P_2Q$分别与点$P_1,P_2$处的切线垂直。
（函数示意图：点到光滑闭曲线的最远、最近点垂线示意图）

- 若光滑闭曲线$T_1,T_2$不相交，点$P_1,P_2$分别是它们之间的最远(近)点，则直线$P_1P_2$是$T_1,T_2$的公垂线，即$P_1P_2$同时垂直于$T_1,T_2$在这两个点处的切线。
（函数示意图：两条不相交光滑闭曲线的最远/最近点公垂线示意图）





# 应用大题




xxxx

**题目**

欲围成一个面积为 $150m^2$ 的矩形场地，所用材料的造价正面 $6$ 元$/m^2$，其余三面 $3$ 元$/m^2$，四面墙的高度相同。试问场地的长和宽各是多少米时，才能使所用的材料费用最低？
?

````````col
```````col-md
flexGrow=20
===

**答案**：正面长 10 米，侧面宽 15 米

**解析**

> 设正面长为 $x$（米），侧面宽为 $y$（米），墙高为 $h$。则 $xy=150$。
> 总造价 $C=6xh+3(xh+2yh)=9xh+6yh$。
> 代入 $y=\dfrac{150}{x}$：
> $$C(x)=h\left(9x+\frac{900}{x}\right)$$
> $$C'(x)=h\left(9-\frac{900}{x^2}\right)=0\ \Rightarrow\ x^2=100\ \Rightarrow\ x=10$$
> $$C''(x)=\frac{1800h}{x^3}>0$$
> 为极小值点。此时 $y=\dfrac{150}{10}=15$。
> 即正面长 10 米、侧面宽 15 米时费用最低。


**另一解法** 
$$ab=150$$

$$y = 6b + 2a\cdot 3 + 3b$$
换a更简单
$a=\dfrac{150}{b}$，
$$
\begin{align*}
y &= 9b + \frac{150\cdot 6}{b}\\[4pt]
y' &= 9 + 150\cdot6\cdot\left(-\frac{1}{b^2}\right)\\[4pt]
\text{令}\quad y' &= 0\\[4pt]
\frac{150\cdot 6}{b^2} &= 9\\[4pt]
\frac{50\cdot 2}{b^2} &= 1\\[4pt]
b_1 &= 10,\ b_2=-10\ (\text{舍})\\[4pt]
y'' &= 150\cdot 12 \cdot b^{-3} > 0\\[4pt]
&\implies b=10\text{为极小值点},\quad a = \frac{150}{10} = 15
\end{align*}
$$






**考点**

导数求实际问题的最小值（造价优化）
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-29T04:01:22.419Z,9,8.2956,1,2,1,0,0,2026-11-20T04:01:22.419Z,id=t12kn3-->


zzzz






xxxx

**题目**

某工厂生产计算器，若日产量为 $x$ 台的成本函数为 $C(x)=7500+50x-0.02x^2$，收入函数为 $R(x)=80x-0.03x^2$，且产销平衡，试确定日生产多少台计算器时，工厂的利润最大？
?

````````col
```````col-md
flexGrow=20
===

**答案**：日生产 1500 台时利润最大

**解析**

> 利润函数：
> $$L(x)=R(x)-C(x)=(80x-0.03x^2)-(7500+50x-0.02x^2)=30x-0.01x^2-7500$$
> $$L'(x)=30-0.02x=0\ \Rightarrow\ x=1500$$
> $$L''(x)=-0.02<0$$
> 故 $x=1500$ 为极大值点，即最大值点。

**考点**

导数求实际问题最大值（利润最大化）
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-27T04:09:38.177Z,7,8.2956,1,2,1,0,0,2026-11-20T04:09:38.177Z,id=zcz4hp-->


zzzz



xxxx

**题目**

已知血液浓度 $C$ 关于时间 $t$ 的函数为 $C(t)=0.30t+0.04t^{2}-0.0004t^{3}$，求时间 $t$ 为多少时血液浓度最大？（提示：$\sqrt{0.00784}\approx 0.0885$）
?

````````col
```````col-md
flexGrow=20
===

**答案**：$t\approx70.21$（秒）

**解析**

> $$C'(t)=0.30+0.08t-0.0012t^2$$
> 令 $C'(t)=0$，即 $0.0012t^2-0.08t-0.30=0$：
> $$t=\frac{0.08\pm\sqrt{0.08^2+4\times0.0012\times0.30}}{2\times0.0012}=\frac{0.08\pm\sqrt{0.00784}}{0.0024}$$
> 由 $\sqrt{0.00784}\approx0.0885$，得正根
> $$t=\frac{0.08+0.0885}{0.0024}\approx70.21\ \text{（秒）}$$
> （负根 $t\approx-3.54$ 舍去。）此时 $C(t)$ 取得最大值。

看到$\sqrt{0.00784}\approx 0.0885$）就要想到这一题一定有猫腻
又看到这题十字相乘凑不了
**又要用$\frac{-b\pm\sqrt{b^2-4ac}}{2a}$，就想到这个肯定是给$\sqrt{-b\pm4ac}$这个根号用的**




**考点**

导数求实际问题的最大值（医学模型）
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-30T04:07:07.661Z,10,8.2956,1,2,1,0,0,2026-11-20T04:07:07.661Z,id=fy483s-->


zzzz



xxxx

**题目**

已知抛物线 $y=1-x^{2}$ 与 $x$ 轴交于 $A$、$B$ 两点，以 $AB$ 为下底的等腰梯形 $ABCD$ 内接于该抛物线，试问当 $C$ 点的纵坐标为多少时，等腰梯形的面积达到最大？
?

````````col
```````col-md
flexGrow=20
===

**答案**：$C$ 点纵坐标为 $\dfrac{8}{9}$ 时面积最大

**解析**

> 令 $y=0$ 得 $x=\pm1$，即 $A=(-1,0)$，$B=(1,0)$，下底 $AB=2$。
> 设 $C=(x,1-x^2)$（$0<x<1$），由对称性 $D=(-x,1-x^2)$，上底 $CD=2x$，高为 $1-x^2$。
> 面积：
> $$S(x)=\frac{2+2x}{2}(1-x^2)=(1+x)(1-x^2),\quad 0<x<1$$
> $$S'(x)=1-2x-3x^2=(1+x)(1-3x)$$
> 令 $S'(x)=0$，得 $x=\dfrac13$（$x=-1$ 舍去）。在 $0<x<\dfrac13$ 时 $S'>0$，$\dfrac13<x<1$ 时 $S'<0$，故 $x=\dfrac13$ 处面积最大。
> 此时 $C$ 点纵坐标 $y=1-\dfrac19=\dfrac89$。

**考点**

导数求几何最值（内接图形面积最大）
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-27T04:01:02.339Z,7,8.2956,1,2,1,0,0,2026-11-20T04:01:02.339Z,id=qebztv-->


zzzz



xxxx

**题目**

一房地产公司有 $60$ 套公寓要出租，当月租金定为 $3000$ 元时，公寓会全部租出去，当月租金每增加 $200$ 元时，就会多一套公寓租不出去，而租出去的公寓每月需花费 $200$ 元的维修费。试问租金定为多少可获得最大收入？最大收入是多少？
?

````````col
```````col-md
flexGrow=20
===

**答案**：租金定为 $7600$ 元，最大收入 $273800$ 元

**解析**

> 设租金增加 $x$ 个 $200$ 元，则：
> 租金 $=3000+200x$，租出套数 $=60-x$，每套净收入 $=3000+200x-200=2800+200x$。
> 总收入：
> $$R(x)=(60-x)(2800+200x)=168000+9200x-200x^2$$
> $$R'(x)=9200-400x=0\ \Rightarrow\ x=23$$
> 且 $R''(x)=-400<0$，为最大值点。
> 租金定为 $3000+200\times23=7600$ 元。
> 最大收入：
> $$R(23)=(60-23)(2800+4600)=37\times7400=273800\text{ 元}$$


**另一解法：** 
$\text{收入} = \text{租金} \times \text{房子个数} - \text{维修费} \times \text{房子个数}$ 
因为
租金+$200x$时，
房子个数就$-x$，
所以
$$
\begin{align*}
y&=(3000+200x)\cdot(60-x)-200\cdot(60-x)\\[4pt]
&=(60-x)\cdot(3000+200x-200)\\[4pt]
\end{align*}
$$

$$
\begin{align*}
y'&=(-1)\cdot(2800+200x)+(60-x)\cdot200\\[4pt]
\text{令}y'=0,\quad 0&=-2800-200x+(60-x)\cdot200\\[4pt]
\text{等式两边同除以200化简：}\quad 0&=-14 -x +60 -x\\[4pt]
2x&=60-14\\[4pt]
x&=30-7=23
\end{align*}
$$

$$
y''=-200-200=-400<0
$$
因此$x=23$为极大值点，
$$
(60-23)\cdot(3000+200\times23-200)=273800
$$






**考点**

导数求实际问题最大值（收入函数）
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-30T04:00:58.058Z,10,8.2956,1,2,1,0,0,2026-11-20T04:00:58.058Z,id=qw8kkn-->


zzzz






xxxx

**题目**

某产品生产 $x$ 件的总成本为 $C(x)=\dfrac{2}{3}x^3-22x^2+8x+3500$，每一件产品价格是 $P=30-\dfrac{x}{2}$，求产品产量为多少件时才能获得最大利润？
?

````````col
```````col-md
flexGrow=20
===

**答案**：产量为 $22$ 件时利润最大

**解析**

> 利润函数（产销平衡，收入 $=xP$）：
> $$L(x)=xP-C(x)=x\left(30-\frac{x}{2}\right)-\left(\frac{2}{3}x^3-22x^2+8x+3500\right)$$
> $$=-\frac{2}{3}x^3+\frac{43}{2}x^2+22x-3500\quad(x>0)$$
> 求导：
> $$L'(x)=-2x^2+43x+22=-(2x+1)(x-22)$$
> 令 $L'(x)=0$，得唯一正驻点 $x=22$。
> $$L''(x)=-4x+43,\qquad L''(22)=-88+43=-45<0$$
> 故 $x=22$ 为极大值点，即最大值点。

**另一解法** 

利润=收入-成本
$$y = x\cdot p - G(x)$$
$$
\begin{align*}
y'&= 30 - \frac{x}{2} + x\cdot\left(-\frac{1}{2}\right) - \left(2x^2 -44x +8\right)\\[4pt]
&= 30 - \frac{1}{2}x - \frac{1}{2}x -2x^2 +44x -8\\[4pt]
&= -2x^2 +43x +22\\[4pt]
&= (-2x -1)(x -22)
\end{align*}
$$
令$y'=0$，解得$x_1=-\frac{1}{2}$（舍去），$x_2=22$。
$$y'' = -4x +43$$
$$y''(22) = -4\times22 +43 = -45 < 0$$
$\Rightarrow x=22$为最大值点。





**考点**

导数求实际问题最大值（利润函数）
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-30T04:01:08.259Z,10,8.2956,1,2,1,0,0,2026-11-20T04:01:08.259Z,id=lcq51d-->


zzzz



xxxx

**题目**

将长为 $4m$ 的铁丝剪成两段，一段围成正方形，余下的围成圆周，如何选择边长与半径，可使两个图形的面积之和为最小。
?

````````col
```````col-md
flexGrow=20
===

**答案**：正方形边长 $\dfrac{4}{\pi+4}\,m$，圆半径 $\dfrac{2}{\pi+4}\,m$

**解析**

> 设正方形边长为 $x$，圆半径为 $r$，则 $4x+2\pi r=4$，即 $2x+\pi r=2$，得 $r=\dfrac{2-2x}{\pi}$。
> 面积之和：
> $$A=x^2+\pi r^2=x^2+\pi\left(\frac{2-2x}{\pi}\right)^2=x^2+\frac{4(1-x)^2}{\pi}$$
> 求导：
> $$A'=2x-\frac{8(1-x)}{\pi}=0\ \Rightarrow\ 2\pi x-8+8x=0\ \Rightarrow\ x=\frac{4}{\pi+4}$$
> $$r=\frac{2-2\cdot\frac{4}{\pi+4}}{\pi}=\frac{2}{\pi+4}$$
> 此时 $A''=2+\dfrac{8}{\pi}>0$，故为极小值点；由实际问题可知即为最小值点。

**另一解法** 
$$
\begin{align*}
&4=4a+2\pi r \implies r=\frac{2(1-a)}{\pi}\\[4pt]
&y=a^2+\pi r^2\\[4pt]
&=a^2+\pi\cdot\frac{2(1-a)}{\pi}\cdot\frac{2(1-a)}{\pi}\\[4pt]
&=a^2+\frac{2(1-a)\cdot2(1-a)}{\pi}\\[4pt]
&y=a^2+\frac{(2-2a)^2}{\pi}\\[4pt]
&y'=2a+\frac{1}{\pi}\cdot2(2-2a)\cdot(-2)\\[4pt]
&=2a+\frac{-4(2-2a)}{\pi}\\[4pt]
&\text{当}\ \frac{4(2-2a)}{\pi}=2a\ \text{时，}\ y'=0\\[4pt]
&8(1-a)=2\pi a\\[4pt]
&\frac{2\pi}{8}a +a -1=0\\[4pt]
&a\left(\frac{2\pi}{8}+1\right)=1\\[4pt]
&a=\frac{4}{4+\pi},\quad r=\frac{2(1-a)}{\pi}=\frac{2}{4+\pi}\\[4pt]
&y''=2+\frac{8}{\pi}>0 \implies \text{为极小值点}
\end{align*}
$$




**考点**

导数求实际问题的最小值（条件化为一元函数）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz



xxxx

**题目**

假设货车以 $x\,km/h$ 的速度匀速行驶 $280km$，按照交通惯例规定，货车行驶速度 $x\,km/h$ 需满足 $60\leq x\leq100$，已知柴油价格 $7$ 元$/L$，货车耗油速率为 $\left(5+\dfrac{x^2}{560}\right)L/h$，司机工资每小时 $45$ 元。问：使总行驶成本最低的行驶速度是多少？在此速度下行驶全程的总费用是多少？
?

````````col
```````col-md
flexGrow=20
===

**答案**：最经济速度 $80\,km/h$，总费用 $560$ 元

**解析**

> 行驶时间为 $\dfrac{280}{x}$ 小时，总费用
> $$L(x)=\left[7\times\left(5+\frac{x^2}{560}\right)+45\right]\times\frac{280}{x}=\left(80+\frac{x^2}{80}\right)\times\frac{280}{x}=\frac{22400}{x}+\frac{7x}{2}$$
> $$L'(x)=-\frac{22400}{x^2}+\frac{7}{2}$$
> 令 $L'(x)=0$，得 $x^2=6400$，$x=80$（$-80$ 舍去）。
> 因 $60\leq x\leq100$，比较端点与驻点：
> $$L(60)=\frac{22400}{60}+\frac{7\times60}{2}\approx583.3,\quad L(80)=280+280=560,\quad L(100)=224+350=574$$
> $560<574<583.3$，故最经济速度为 $80\,km/h$，最小总费用为 $560$ 元。

**另一解法**：运输成本最低问题
问以怎样的速度行驶，成本最低。
成本 = 油钱 + 司机的工费
$$
\begin{align*}
\text{成本} &= 7 \cdot \left[ \frac{280}{x} \cdot \left(5 + \frac{x^2}{560}\right) \right] + \frac{280}{x} \cdot 45 \\[4pt]
y &= 7 \cdot \frac{280}{x} \cdot \left(5 + \frac{x^2}{560}\right) + \frac{280}{x} \cdot 45 \\[4pt]
&= \frac{280 \cdot 7 \cdot 5}{x} + \frac{280 \cdot 7 \cdot x}{560} + \frac{280 \cdot 45}{x} \\[4pt]
&= \frac{280(35 + 45)}{x} + \frac{7}{2}x \\[4pt]
&= \frac{22400}{x} + \frac{7}{2}x
\end{align*}
$$

$$
\begin{align*}
&y' = -\frac{22400}{x^2} + \frac{7}{2}\\[4pt]
&\text{令 } y'=0\\[4pt]
&\frac{22400}{x^2} = \frac{7}{2}\\[4pt]
&\frac{1}{x^2} = \frac{7}{2} \cdot \frac{1}{22400}\\[4pt]
&\frac{1}{x^2} = \frac{1}{6400}\\[4pt]
&\Rightarrow x_1=80,\ x_2=-80\ (\text{舍去})\\[4pt]
&y(60) = \frac{22400}{60} + \frac{7}{2} \cdot 60 \approx 373 + 210 = 583\\[4pt]
&y(80) = \frac{22400}{80} + \frac{7}{2} \cdot 80 = 280 + 280 = 560\\[4pt]
&y(100) = \frac{22400}{100} + \frac{7}{2} \cdot 100 = 224 + 350 = 574\\[4pt]
&\Rightarrow \text{在}x=80\text{处取得最小值}560\text{元}
\end{align*}
$$



**考点**

导数求实际问题的最小值（闭区间端点比较）
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-27T08:50:01.504Z,9,8.2956,1,2,1,0,0,2026-11-18T08:50:01.504Z,id=tzlvy9-->


zzzz



