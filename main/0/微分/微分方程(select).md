#flashcards/微分/微分方程 




# 微分方程的概念



xxxx

**题目**

微分方程 $y'''-2x^{3}y'+x^{2}y=x\sin x$ 是（　）

A. 三阶线性微分方程

B. 三阶非线性微分方程

C. 四阶线性微分方程

D. 四阶非线性微分方程
?

````````col
```````col-md
flexGrow=20
===

**答案**：A

**解析**

> 方程中出现的最高阶导数是 $y'''$，故方程为三阶；方程中 $y'''$、$y'$、$y$ 都以一次幂出现，没有未知函数与导数相乘或导数的高次幂，关于未知函数及其各阶导数是线性的。因此该方程是三阶线性微分方程，选 A。

**考点**

微分方程的阶数与线性性判断
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz



xxxx

**题目**

下列方程中是一阶非齐次线性微分方程的是（　）

A. $y'+4y=xy^{2}$

B. $(y')^{2}-4y=\cos x$

C. $y'-x^{2}y=\sin x$

D. $(2x+y)dx+(x+y)dy=0$
?

````````col
```````col-md
flexGrow=20
===

**答案**：C

**解析**

> 一阶线性微分方程的标准形式为
> $$y'+P(x)y=Q(x)$$
> 要求 $y$ 与 $y'$ 都以一次幂出现，且右端 $Q(x)\ne 0$ 时为非齐次。
>
> - A 中出现 $y^{2}$，是伯努利方程，不是线性方程；
> - B 中出现 $(y')^{2}$，不是线性方程；
> - C 中 $y'$、$y$ 均为一次，右端 $\sin x\ne 0$，是一阶非齐次线性微分方程；
> - D 中含有 $y\,dy$、$y\,dx$ 等结构，是全微分方程，不是关于单个 $y'$ 的线性标准形式。
>
> 故选 C。

**考点**

一阶非齐次线性微分方程的识别
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz



xxxx

**题目**

关于微分方程 $y''+x^{2}y'-3xy=e^{x}$，下列结论正确的是（　）

①该方程是齐次微分方程　　②该方程是线性微分方程

③该方程是常系数微分方程　　④该方程是二阶微分方程

A. ①②　　B. ②④　　C. ①③④　　D. ②③④
?

````````col
```````col-md
flexGrow=20
===

**答案**：B

**解析**

> - ① 方程右端为 $e^{x}\ne 0$，是非齐次方程，不是齐次方程，①错；
> - ② 方程中 $y''$、$y'$、$y$ 都以一次幂出现，关于 $y$ 及其导数是线性的，②对；
> - ③ 方程中 $y'$ 的系数为 $x^{2}$、$y$ 的系数为 $-3x$，都含有自变量 $x$，不是常系数方程，③错；
> - ④ 方程中出现的最高阶导数为 $y''$，是二阶微分方程，④对。
>
> 故正确的是②④，选 B。

**考点**

微分方程的齐次性、线性性、常系数与阶数的综合判断
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz



xxxx

**题目**

下列方程为二阶线性微分方程的是（　）

A. $y''-4yy'+4y=3e^{x}$

B. $(y')^{2}+4x^{2}y=3\sin x$

C. $y''-4x^{3}y'+x^{4}y=0$

D. $y''+y'+4y^{2}=0$
?

````````col
```````col-md
flexGrow=20
===

**答案**：C

**解析**

> 线性微分方程要求未知函数 $y$ 及其各阶导数都以一次幂出现，且不出现 $y$ 与导数相乘、导数的高次幂等情形；阶数由方程中出现的最高阶导数决定。
>
> - A 中出现 $y\cdot y'$，关于 $y$ 不是线性的；
> - B 中出现 $(y')^{2}$，关于 $y'$ 不是线性的；
> - C 中 $y''$、$y'$、$y$ 均为一次，且最高阶为二阶，是二阶线性微分方程；
> - D 中出现 $y^{2}$，关于 $y$ 不是线性的。
>
> 故选 C。

**考点**

二阶线性微分方程的识别（线性性与阶数判断）
```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-29T07:55:21.151Z,9,8.2956,1,2,1,0,0,2026-11-20T07:55:21.151Z,id=alcmv2-->


zzzz








````col
```col-md
flexGrow=1
===
## 概念
$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&方程：含未知量的等式， \\[4pt]
&用来研究这个未知量 \\[4pt]
&若这个方程含有未知函数的导数/微分 \\[4pt]
&则研究的未知量是未知函数 \\[4pt]
&则，这个方程称为微分方程 \\[4pt]
&一般写为: \\[4pt]
&\qquad F\left [ x,y,y',\dots ,y^{(n)} \right ] =0 \\[4pt]
&或 \\[4pt]
&\qquad y^{(n)}=f\left [ x,y,y',\dots ,y^{(n-1)} \right ] \\[4pt]
\end{align*}
$$
## 常微分方程
未知函数为一元函数的微分方程
## 偏微分方程
未知函数为多元函数的微分方程
含的是未知函数的偏导数/偏微分
```

```col-md
flexGrow=1.2
===
## 线性微分方程
$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&形如 \\[4pt]
&f(x)=\\[4pt]
&a_n(x)y^{(n)}+a_{n-1}(x)y^{(n-1)}+\dots +a_1(x)y'+a_0(x)y \\[4pt]
&的微分方程称为n阶线性微分方程 \\[4pt]
&a_k(x)(k=0,1,2,\dots ,n) \\[4pt]
&都是关于自变量x的已知函数 \\[4pt]
&\because \quad 是n阶线性微分方程\\[4pt]
&\therefore \quad y^{(n)}的系数a_n(x)\ne 0  \\[4pt]
&\bullet \quad 若a_k(x)(k=0,1,2,\dots ,n)\in 常数，则  \\[4pt]
&\qquad 为n阶常系数线性微分方程  \\[4pt]
&\bullet \quad 若右端函数f(x)=0  \\[4pt]
&\qquad 则为n阶齐次线性微分方程  \\[4pt]
&\bullet \quad 若a_k(x)(k=0,1,2,\dots ,n)\in 常数  \\[4pt]
&\qquad 且右端函数f(x)=0时  \\[4pt]
&\qquad 则为n阶常系数齐次线性微分方程  \\[4pt]
&\bullet \quad 若右端函数f(x)\ne 0  \\[4pt]
&\qquad 则为n阶非齐次线性微分方程  \\[4pt]
\end{align*}
$$


```
````
## 线性代数补充知识

````col
```col-md
flexGrow=1
===
- [*] 
$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&若函数y_1(x)与函数y_2(x)  \\[4pt]
&满足\frac{y_1(x)}{y_2(x)}\ne 常数   \\[4pt]
&则，称y_1(x)与y_2(x)线性无关\\[4pt]
\end{align*}
$$


```

```col-md
flexGrow=1
===
- [*] 
$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&若\frac{y_1(x)}{y_2(x)}=常数  \\[4pt]
&则，称y_1(x)与y_2(x)线性相关\\[4pt]
\end{align*}
$$


```
````

````col
```col-md
flexGrow=1
===
## 微分方程的阶
$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&微分方程中未知函数的最高阶导数 \\[4pt]
&的阶数称为微分方程的阶 \\[4pt]
&eg：y'''-y'+6y=0 \\[4pt]
&\qquad 为三阶微分方程 \\[4pt]
&即，\because \quad 其为三阶微分方程\\[4pt]
&\qquad \: \therefore \quad 其中一定含有y'''  \\[4pt]
\end{align*}
$$
## 微分方程的解
$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&若将函数代入微分方程 \\[4pt]
&使方程成为恒等式\\[4pt]
&则，该函数为此微分方程的解 \\[4pt]
&微分方程解的图像称为积分曲线 \\[4pt]
\end{align*}
$$
## 初始条件与特解

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&通解:其含的不定常数是不定的数  \\[4pt]
&可能有多个解/无数个解   \\[4pt]
&题目给的初始条件，约束条件\\[4pt]
&把常数定下来  \\[4pt]
&则就得到一个确定的解\\[4pt]
&即为特解\\[4pt]
&通解是微分方程所有解的表达式  \\[4pt]
&特解是微分方程在初始条件下的具体解\\[4pt]
\end{align*}
$$

```

```col-md
flexGrow=1
===
## 微分方程的通解
$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&若微分方程的解中\\[4pt]
&含有的独立常数的个数\\[4pt]
&等于微分方程的阶数 \\[4pt]
&则，该解称为微分方程的通解 \\[4pt]
&独立常数指 \\[4pt]
&通解中的函数要非线性相关 \\[4pt]
&经过任何恒等变形都不能使 \\[4pt]
&常数个数减少 \\[4pt]
&{\color[RGB]{90,109,128} 常数也不一定是任意常数，见例15.4}  \\[4pt]
\end{align*}
$$

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
eg1:&  \\[4pt]
&y=C_1sinx+C_2\cdot 2sinx \\[4pt]
&y_1(x)=C_1sinx \\[4pt]
&y_2(x)=C_2\cdot 2sinx \\[4pt]
&\frac{y_1(x)}{y_2(x)}=常数，{\color[RGB]{90,109,128} 线性相关}  \\[4pt]
&\therefore \quad 原式可化为:\\[4pt]
&\ \ \qquad y=(2C_2+C_1)sinx=Csinx \\[4pt]
&实际是含有一个独立常数 \\[4pt]
&是一阶微分方程的通解 \\[4pt]
\end{align*}
$$

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
eg2:&  \\[4pt]
&y=(C_1+C_2x)e^x，\frac{C_1e^x}{C_2xe^x}\ne 常数  \\[4pt]
&\therefore \quad 含有二个独立常数\\[4pt]
&\therefore \quad 是二阶微分方程的通解\\[4pt]
\end{align*}
$$

```
````
- [*] 例15.2
设 $y=y(x)$ 是二阶常系数线性微分方程 $y''+py'+qy=e^{3x}$ 

满足初始条件 $y(0)=y'(0)=0$ 的特解，求 $\displaystyle \lim_{x \to 0} \frac{ln(1+x^2)}{y(x)}$ 
````col
```col-md
flexGrow=1
===
==分析：==
$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&因为他要的不是方程的解\\[4pt]
&所以，不必非要解方程\\[4pt]
&看看是否可以巧解，快解\\[4pt]
&\because \quad x \to 0时 \\[4pt]
&\qquad ln(1+x^2)\sim x^2\\[4pt]
&\therefore \quad \lim_{x \to 0} \frac{ln(1+x^2)}{y(x)}\\[4pt]
&\qquad =\lim_{x \to 0} \frac{x^2}{y(x)}\\[4pt]
&\because \quad y(0)=y'(0)=0 \\[4pt]
&\therefore \quad y''(0)+py'(0)+qy(0)=1\\[4pt]
&\Rightarrow \quad y''(0)=1\\[4pt]
&且\lim_{x \to 0}y(x)=\lim_{x \to 0}y'(x)=0\\[4pt]
&\therefore \quad \lim_{x \to 0} \frac{x^2}{y(x)}为\frac{0}{0}型，可用洛必达\\[4pt]
&\because \quad y(x)三阶可导且连续 \\[4pt]
&\therefore \quad \lim_{x \to 0} \frac{x^2}{y(x)}\\[4pt]
&\qquad =^洛\lim_{x \to 0} \frac{2x}{y'(x)}\\[4pt]
&\qquad =^洛\lim_{x \to 0} \frac{2}{y''(x)}\\[4pt]
&\because \quad y''(0)=1 \\[4pt]
&\therefore \quad \lim_{x \to 0} \frac{2}{y''(x)}=2\\[4pt]
\end{align*}
$$


```

```col-md
flexGrow=1
===
==解：==
$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&\because \quad y(0)=y'(0)=0 \\[4pt]
&\therefore \quad y''(0)+py'(0)+qy(0)=1\\[4pt]
&\qquad \Rightarrow \quad y''(0)=1\\[4pt]
&\therefore \quad \lim_{x \to 0} \frac{ln(1+x^2)}{y(x)}\\[4pt]
&\qquad =\lim_{x \to 0} \frac{x^2}{y(x)}\\[4pt]
&\qquad =\lim_{x \to 0} \frac{2x}{y'(x)}\\[4pt]
&\qquad =\lim_{x \to 0} \frac{2}{y''(x)}\\[4pt]
&\qquad =2\\[4pt]
\end{align*}
$$



```
````




# 一阶微分方程的求解



## 可分离变量型微分方程

可分离变量型指：方程 $F(x,y)=0$ 可表示为 $F(x,y)=f(x)\cdot g(y)=0$ 

### 直接可分离


xxxx

**题目**

微分方程 $(1+x)^{2}dy-y^{2}dx=0$ 满足 $y\big|_{x=0}=-\dfrac{2}{3}$ 的特解为　　　。
?

````````col
```````col-md
flexGrow=20
===

**答案**：$y=-\dfrac{2(1+x)}{3+5x}$

**解析**

> 这是可分离变量的微分方程。先移项：
> $$(1+x)^{2}dy=y^{2}dx$$
> 将变量分离（移项后右端为正号）：
> $$\frac{dy}{y^{2}}=\frac{dx}{(1+x)^{2}}$$
> 两边积分：
> $$-\frac{1}{y}=-\frac{1}{1+x}+C$$
> 代入初始条件 $y(0)=-\dfrac{2}{3}$：
> $$-\frac{1}{-2/3}=-\frac{1}{1+0}+C\;\Longrightarrow\;\frac{3}{2}=-1+C\;\Longrightarrow\;C=\frac{5}{2}$$
> 故
> $$-\frac{1}{y}=-\frac{1}{1+x}+\frac{5}{2}$$
> 两边取负并通分：
> $$\frac{1}{y}=\frac{1}{1+x}-\frac{5}{2}=\frac{2-5(1+x)}{2(1+x)}=\frac{-3-5x}{2(1+x)}$$
> 取倒数得
> $$y=-\frac{2(1+x)}{3+5x}$$
>
> **验证：**
>
> - 初始条件：当 $x=0$ 时，$y=-\dfrac{2}{3}$，与题给条件一致；
> - 微分方程：对 $y$ 求导可验证 $y'=\dfrac{y^{2}}{(1+x)^{2}}$ 成立。
>


**考点**

可分离变量微分方程的初值问题（初始条件定常数）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz








xxxx

**题目**

微分方程 $\dfrac{dy}{dx}=\dfrac{3x}{y\cos y^{2}}$ 的通解为（　）

A. $\sin y^{2}+3x^{2}+C=0$

B. $\sin y^{2}-3x^{2}+C=0$

C. $\sin y^{2}+3x^{2}=0$

D. $\sin y^{2}-3x^{2}=0$
?

````````col
```````col-md
flexGrow=20
===

**答案**：B

**解析**

> 这是可分离变量的微分方程。将含 $y$ 的项与含 $x$ 的项分置两边：
> $$y\cos y^{2}\,dy=3x\,dx$$
> 两边积分。左边注意到 $d(\sin y^{2})=2y\cos y^{2}\,dy$，故
> $$\frac{1}{2}\sin y^{2}=\frac{3}{2}x^{2}+C_{1}$$
> 两边乘 $2$ 并将常数合并记为 $C$：
> $$\sin y^{2}-3x^{2}+C=0$$
> 故选 B。

**考点**

可分离变量微分方程求通解
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz














$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
能写成&y'=f(x)g(y)形式的方程称为可分离变量型微分方程 \\[4pt]
解法为：& \\[4pt]
&\frac{dy}{dx}=f(x)g(y)\\[4pt]
&\Rightarrow \quad \frac{dy}{g(y)}=f(x)dx，g(y)\ne 0  \\[4pt]
&\Rightarrow \quad \int \frac{dy}{g(y)}=\int f(x)dx\\[4pt]
\end{align*}
$$

### 换元后可分离

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&是形如：\frac{dy}{dx} =f(ax+by+c)的方程\\[4pt]
&其中，常数a,b全都不为零 \\[4pt]
解法为：&\\[4pt]
\end{align*}
$$
````col
```col-md
flexGrow=1
===

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&令u=ax+by+c \quad {\color[RGB]{90,109,128} 换元}  \\[4pt]
&\frac{du}{dx}=a+\frac{dy}{dx}\cdot b \quad {\color[RGB]{90,109,128} u对x求导}  \\[4pt]
&\Rightarrow \ \frac{dy}{dx}=\left ( \frac{du}{dx}-a \right ) \cdot \frac{1}{b} \quad {\color[RGB]{90,109,128} 解出了\frac{dy}{dx}} \\[4pt]
&{\color[RGB]{90,109,128} 将\frac{dy}{dx}代入原式\frac{dy}{dx} =f(ax+by+c)中} \\[4pt]
&\Rightarrow \ \left ( \frac{du}{dx}-a \right ) \cdot \frac{1}{b}=f(u) \\[4pt]
\end{align*}
$$

```

```col-md
flexGrow=1
===

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&\Rightarrow \ \frac{du}{dx}-a=bf(u) \\[4pt]
&\frac{du}{dx}=bf(u)+a \quad {\color[RGB]{90,109,128} 分离变量}  \\[4pt]
&\frac{du}{bf(u)+a}=dx  \\[4pt]
&\int \frac{du}{bf(u)+a}=\int dx \quad {\color[RGB]{90,109,128} 两边同时积分}  \\[4pt]
\end{align*}
$$



```
````

## 齐次型微分方程

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&形如：\frac{dy}{dx} =\varphi (\frac{y}{x})的方程\\[4pt]
&叫作齐次型微分方程 \quad {\color[RGB]{90,109,128} y'随\frac{y}{x}的变化而变化} \\[4pt]
解法为：&\\[4pt]
\end{align*}
$$
````col
```col-md
flexGrow=1
===

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&令\frac{y}{x}=u \quad {\color[RGB]{90,109,128} y,u都是关于x的函数}  \\[4pt]
&y=xu \quad {\color[RGB]{90,109,128} 两边同时对x求导}  \\[4pt]
&\Rightarrow \ y'=(xu)' \Rightarrow \ \frac{dy}{dx}=u+x\frac{du}{dx}  \\[4pt]
&u+x\frac{du}{dx}=\varphi (u) \quad {\color[RGB]{90,109,128} 代入原式}  \\[4pt]
\end{align*}
$$

```

```col-md
flexGrow=1
===

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&\varphi (u)-u=\frac{xdu}{dx}   \\[4pt]
&\Rightarrow \ \frac{du}{\varphi (u)-u}=\frac{dx}{x} \quad {\color[RGB]{90,109,128} 分离变量}  \\[4pt]
&\int \frac{du}{\varphi (u)-u}=\int \frac{dx}{x} \quad {\color[RGB]{90,109,128} 两边同时积分}\\[4pt]
\end{align*}
$$



```
````

## 一阶线性微分方程（代公式）




xxxx

**题目**

求微分方程 $dy-(y+e^{x})dx=0$ 的通解　　　。
?

````````col
```````col-md
flexGrow=20
===

**答案**：$y=e^{x}(x+C)$

**解析**

> 将方程改写为一阶线性微分方程的标准形式：
> $$y'-y=e^{x}$$
> 其中 $p(x)=-1$，$q(x)=e^{x}$。由通解公式，积分因子为
> $$e^{\int p\,dx}=e^{\int-1\,dx}=e^{-x}$$
> 于是
> $$y=e^{x}\left(\int e^{x}\cdot e^{-x}\,dx+C\right)=e^{x}\left(\int 1\,dx+C\right)=e^{x}(x+C)$$
> 故通解为 $y=e^{x}(x+C)$。

**考点**

一阶线性非齐次微分方程的通解（积分因子法）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz



xxxx

**题目**

微分方程 $xy'-y-2x^{2}=0$ 的通解是（　）

A. $y=2x^{2}+Cx$

B. $y=-2x^{2}+Cx$

C. $y=2x^{2}+x+C$

D. $y=-2x^{2}+x+C$
?

````````col
```````col-md
flexGrow=20
===

**答案**：A

**解析**

> 将方程化为一阶线性微分方程的标准形式。两边除以 $x$（$x\ne 0$）：
> $$y'-\frac{1}{x}y=2x$$
> 其中 $p(x)=-\dfrac{1}{x}$，$q(x)=2x$。由一阶线性方程通解公式
> $$y=e^{-\int p\,dx}\left(\int q\,e^{\int p\,dx}\,dx+C\right)$$
> 计算得
> $$e^{\int p\,dx}=e^{\int-\frac{1}{x}dx}=e^{-\ln x}=\frac{1}{x},\qquad e^{-\int p\,dx}=x$$
> 于是
> $$y=x\left(\int 2x\cdot\frac{1}{x}\,dx+C\right)=x\left(\int 2\,dx+C\right)=x(2x+C)=2x^{2}+Cx$$
> 故选 A。

**考点**

一阶线性微分方程的通解公式（积分因子法）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz




$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&形如：y'+p(x)y=q(x)的方程\\[4pt]
&叫作一阶线性微分方程 \quad 其中，p(x),q(x)为已知的连续函数 \\[4pt]
其通解公式为：&\\[4pt]
&\displaystyle y=e^{-\int p(x)dx}\left [ \int e^{\int p(x)dx}\cdot q(x)dx+C \right ] \\[4pt]
&注：\\[4pt]
&\int p(x)dx取原函数时不加积分常数C\\[4pt]
\end{align*}
$$
### 通解公式的推导思路：
````col
```col-md
flexGrow=1
===
$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&(这里把p(x),q(x)简写为p,q)\\[4pt]
&把方程y'+py=q中的y解出来\\[4pt]
&的思想方法：\\[4pt]
&用乘积求导公式的逆用\\[4pt]
&(uv)'=u'v+uv'\\[4pt]
&\qquad\quad  y'\cdot 1+yp=q\\[4pt]
&其中，y'为u'，y为u\\[4pt]
&那么，1为v，(1)'=p吗？\\[4pt]
&可是，(1)'=0\ne p\\[4pt]
&(?)'=p\\[4pt]
&?=\int p\ dx\\[4pt]
&可是，\int p\ dx\ne 1\\[4pt]
&则，这也行不通\\[4pt]
&只有一个可能\\[4pt]
&y'旁边的v被提走了\\[4pt]
\end{align*}
$$


```

```col-md
flexGrow=1
===
$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&真相为\\[4pt]
&原本式子：vy'+vpy=qv\\[4pt]
&{\color[RGB]{90,109,128} v'=vp} \\[4pt]
&v(y'+py)=qv\\[4pt]
&\Rightarrow \ y'+py=q\\[4pt]
&且求导之后不仅含有自己，还会多乘一个p的\\[4pt]
&只有\left [ e^{a(x)} \right ] '=e^{a(x)}\cdot \left [ a(x) \right ] '\\[4pt]
&若\left [ a(x) \right ] '=p，则a(x)=\int p\ dx\\[4pt]
&则v=e^{\int p(x)\ dx}\\[4pt]
&就可以用乘积求导公式的逆用了\\[4pt]
\end{align*}
$$



```
````


### 推导
$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&y'+py=q\\[6pt]
&e^{\int p(x)\ dx}(y'+py)=q\cdot e^{\int p(x)\ dx}\\[6pt]
&y'\cdot e^{\int p(x)dx}+e^{\int p(x)dx}\cdot py=q\cdot e^{\int p(x)dx}\\[6pt]
&{\color[RGB]{90,109,128} \left ( e^{\int p(x)dx} \right ) '=e^{\int p(x)dx}\cdot p} \\[6pt]
&\Rightarrow \ \left (y\cdot e^{\int p(x)dx} \right ) '=q\cdot e^{\int p(x)dx}\\[6pt]
&{\color[RGB]{90,109,128} 两边同时积分} \\[6pt]
&y\cdot e^{\int p(x)dx}=\int e^{\int p(x)dx}\cdot q\ dx+C\\[6pt]
&\Rightarrow \ y=e^{-\int p\ dx}\cdot \left [ \int e^{\int p\ dx}\cdot q\ dx+C \right ]\\[6pt]
\end{align*}
$$



# 二阶常系数齐次线性微分方程
## 概念

形如：${y}'' +p{y}' +qy=0\ (p,q\in 常数)$ 的方程
## 其解的结构

若$y_{1}(x),y_{2}(x)$是${y}'' +p{y}' +qy=0$的两个特解，且$\displaystyle  \frac{y_{1}(x)}{y_{2}(x)}\ne c$(常数),则称$y_{1}(x)与y_{2}(x)$线性无关
则，$y(x)=c_{1} y_{1} (x)+c_{2} y_{2} (x)$是方程${y}'' +p{y}' +qy=0$的通解
## 通解的求法（思路）

````col
```col-md

$$
\begin{array}{l}
求\ y'' + p y' + q y = 0\ 的通解 \\[8pt]  % 逐行加固定间距，2.0等效12pt
只用找到\ y_1(x),y_2(x)，且\frac{y_1(x)}{y_2(x)}\ne c即可 \\[8pt]
什么样的函数满足这个方程呢？ \\[8pt]
设\ y(x)=e^{ax} \ (a\in 常数) \\[8pt]
将其代入方程 \\[8pt]
(e^{ax})'' =a^2 e^{ax}，(e^{ax})' =ae^{ax} \\[8pt]
\Rightarrow a^2 e^{ax}+p\cdot ae^{ax}+q\cdot e^{ax}=0 \\[8pt]
e^{ax}(a^2+pa+q)=0 \\[8pt]
\Rightarrow a^2+pa+q=0 \\[8pt]
我们称\ a^2+pa+q=0\ 为\\[8pt]
\ y'' + p y' + q y = 0\ 的特征方程 \\[8pt]
\because a^2+pa+q=0\ 为关于a的一元二次方程 \\[8pt]
\therefore 我们可以求出其两个实根a_1与a_2
\end{array}
$$
- [*] ==1.==若$p^{2}-4q>0$，则$a_{1} \ne a_{2}$
$$
\begin{array}{l}
则，\frac{e^{a_{1} x}}{e^{a_{2} x}} =e^{(a_{1}-a_{2})x}\ne c\\[8pt]
\Rightarrow通解为y(x)=c_{1} e^{a_{1} x}+c_{2} e^{a_{2} x}\\[8pt]
\end{array}
$$
- [*] ==2.==若$p^{2}-4q=0$，则$a_{1} = a_{2}=a$
$$
\begin{array}{l}
则，\frac{e^{a_{1} x}}{e^{a_{2} x}} =e^{(a_{1}-a_{2})x}= 1\\[8pt]
\Rightarrow e^{a_{1} x}与e^{a_{2} x}线性相关\\[8pt]
不能构成此方程的通解\\[8pt]
记住这个结论：\\[8pt]
xe^{ax}也是满足此方程的，且\frac{xe^{ax}}{e^{ax}} \ne c\\[8pt]
\Rightarrow通解为y(x)=c_{1} e^{a x}+c_{2} xe^{a x}=(c_{1}+c_{2}x)e^{a x}\\[8pt]
\end{array}
$$

```

```col-md

- [*] ==3.==若$p^{2}-4q<0$，则没有实根
用虚根     ${\color[RGB]{90,109,128} i^{2}=-1}$

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
a &=\frac{-p\pm \sqrt{p^{2}-4q} }{2} 
，
{\color[RGB]{90,109,128} \mathit{\left\{\begin{matrix} 
 \bigtriangleup = p^{2}-4q<0\\ 
-\bigtriangleup>0
\end{matrix}\right. } } \\[10pt]

&=\frac{-p\pm \sqrt{-\bigtriangleup \cdot i^{2} } }{2} \\[10pt]

&=\frac{-p\pm \sqrt{-\bigtriangleup}\cdot i }{2} \\[10pt]

&=\frac{-p}{2} \pm \frac{\sqrt{-\bigtriangleup } }{2} \cdot i\\[10pt]

&设\alpha = \frac{-p}{2} ，\beta=  \frac{\sqrt{-\bigtriangleup } }{2}\\[10pt]

&=\alpha \pm \beta i\\[10pt]

&\alpha \pm \beta i是特征方程的一对共轭复根\\[10pt]

&\Rightarrow通解为y(x)=e^{\alpha x} (c_{1}cos\beta x+c_{2}sin\beta x )\\[10pt]
\end{align*}
$$



```
````
## 通解的求法（总结）



xxxx

**题目**

微分方程 $y''+5y'-24y=0$ 的通解为　　　。
?

````````col
```````col-md
flexGrow=20
===

**答案**：$y=C_{1}e^{3x}+C_{2}e^{-8x}$

**解析**

> 特征方程为
> $$r^{2}+5r-24=0\;\Longrightarrow\;(r-3)(r+8)=0$$
> 特征根为 $r_{1}=3$，$r_{2}=-8$，是两个相异实根，故通解为
> $$y=C_{1}e^{3x}+C_{2}e^{-8x}$$

**考点**

二阶常系数齐次线性微分方程的特征根法
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz



xxxx

**题目**

求微分方程 $y''-10y'+26y=0$ 的通解。
?

````````col
```````col-md
flexGrow=20
===

**答案**：$y=e^{5x}(C_{1}\cos x+C_{2}\sin x)$

**解析**

> 特征方程为
> $$r^{2}-10r+26=0$$
> 解得特征根
> $$r=\frac{10\pm\sqrt{100-104}}{2}=\frac{10\pm 2i}{2}=5\pm i$$
> 这是一对共轭复根，其中 $\alpha=5$，$\beta=1$，故通解为
> $$y=e^{5x}(C_{1}\cos x+C_{2}\sin x)$$


**另一解法：** 
特征方程：$r^2 - 10r + 26 = 0$
$\Delta = 100 - 4 \times 26 < 0$ 
$$
\begin{align*}
r &= \frac{10 \pm \sqrt{-\Delta i^2} \, }{2} \\[6pt]
&= \frac{10}{2} \pm \frac{\sqrt{-\Delta}}{2} \, i \\[6pt]
&= 5 \pm \frac{\sqrt{4}}{2} \, i \\[6pt]
&= 5 \pm i
\end{align*}
$$
得到特征根的实部与虚部：$\alpha = 5,\ \beta = 1$
共轭复根情形下的微分方程通解：
$$
\begin{align*}
y &= e^{\alpha x}\left(C_1 \cos \beta x + C_2 \sin \beta x\right) \\[6pt]
&= e^{5x}\left(C_1 \cos x + C_2 \sin x\right)
\end{align*}
$$





**考点**

二阶常系数齐次线性微分方程的特征根法（共轭复根情形）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz




xxxx

**题目**

微分方程 $y''-3y'-4y=0$ 满足初始条件 $y|_{x=0}=0$，$y'|_{x=0}=-5$ 的特解。
?

````````col
```````col-md
flexGrow=20
===

**答案**：$y=-e^{4x}+e^{-x}$

**解析**

> 特征方程为
> $$r^{2}-3r-4=0\;\Longrightarrow\;(r-4)(r+1)=0$$
> 特征根为 $r_{1}=4$，$r_{2}=-1$，故通解为
> $$y=C_{1}e^{4x}+C_{2}e^{-x}$$
> 求导得
> $$y'=4C_{1}e^{4x}-C_{2}e^{-x}$$
> 代入初始条件：
> $$y(0)=C_{1}+C_{2}=0$$
> $$y'(0)=4C_{1}-C_{2}=-5$$
> 由第一式 $C_{2}=-C_{1}$，代入第二式：
> $$4C_{1}+C_{1}=-5\;\Longrightarrow\;C_{1}=-1,\quad C_{2}=1$$
> 故所求特解为
> $$y=-e^{4x}+e^{-x}$$

**考点**

二阶常系数齐次线性微分方程的初值问题
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz




对于${y}'' +p{y}' +qy=0$，
其对应的特征方程为$a^{2}+pa+q=0$
````col
```col-md

- [*]  ==1.==若$p^{2}-4q>0$，则$a_{1} \ne a_{2}$
$\Rightarrow$通解为$y(x)=c_{1} e^{a_{1} x}+c_{2} e^{a_{2} x}$
- [*] ==2.==若$p^{2}-4q=0$，则$a_{1} = a_{2}=a$
$\Rightarrow$通解为$y(x)=c_{1} e^{a x}+c_{2} xe^{a x}=(c_{1}+c_{2}x)e^{a x}$

```

```col-md

- [*] ==3.==若$p^{2}-4q<0$，则没有实根
$\alpha \pm \beta i$是特征方程的一对共轭复根
$\alpha =\frac{-p}{2} ，\beta=  \frac{\sqrt{-\bigtriangleup } }{2}$
$\Rightarrow$通解为$y(x)=e^{\alpha x} (c_{1}cos\beta x+c_{2}sin\beta x )$



```
````

````col
```col-md

## 例15.14
设函数$y=y(x)$是微分方程
${y}'' +{y}' -2y=0$的解，且在$x=0$处$y(0)$取得
极值3，求$y(x)$
==解：==
$$
\begin{array}{l}
方程的特征方程为r^{2}+r-2=0，\\[8pt]
且p^{2}-4q>0\\[8pt]
\Rightarrow r_{1}=-2，r_{2}=1\\[8pt]
\Rightarrow y(x)=c_{1} e^{-2 x}+c_{2} e^{x}\\[8pt]
\because 由题知y(0)=3\\[8pt]
\therefore c_{1}+c_{2}=3 \mathcal{\color[RGB]{90,109,128} 代入方程}\\[8pt]
\because 在可导点x=0处，y(x)取得极值\\[8pt]
\therefore 由费马定理\Rightarrow {y(0)}' =0\\[8pt]
\because {y(x)}' =-2c_{1} e^{-2 x}+c_{2} e^{x}\\[8pt]
\therefore -2c_{1}+c_{2}=0 \mathcal{\color[RGB]{90,109,128} 代入方程}\\[8pt]
\Rightarrow \left\{\begin{matrix}
  c_{1}+c_{2} =3  \\  
  -2c_{1}+c_{2} =0 
\end{matrix}\right. 
\ 解得
\left\{\begin{matrix} 
  c_{1} =1  \\  
  c_{2} =2 
\end{matrix}\right. 
\\[8pt]
\Rightarrow通解y(x)=e^{-2 x}+2e^{x}\\[8pt]
\end{array}
$$

```

```col-md

## 例15.15
设函数$y=f(x)$满足微分方程
${y}'' +2{y}' +5y=0$且$f(0)=1，{f}'(0) =-1$，
求$f(x)$
==解：==
$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&方程的特征方程为r^{2}+2r+5=0，\\[10pt]
&且p^{2}-4q<0\\[10pt]
r&=\frac{-2\pm \sqrt{16}\cdot i }{2} \\[10pt]
&=-1 \pm 2 i\\[10pt]
&\Rightarrow
\left\{\begin{matrix} 
  r_{1}=-1+ 2i \\  
  r_{2} =-1- 2i 
\end{matrix}\right. \\[10pt]
&\Rightarrow通解为y(x)=e^{-x} (c_{1}cos2x+c_{2}sin2x )\\[10pt]
&{y}' (x)=e^{-x}[ (2c_{2}-c_{1})cos2x-(2c_{1}+c_{2})sin2x ]\\[10pt]
&\because f(0)=1，{f}'(0) =-1\\[10pt]
&\therefore \ \Rightarrow
\left\{\begin{matrix} 
  c_{1} =1  \\  
  c_{2} =0 
\end{matrix}\right. \\[10pt]
&\Rightarrow f(x)=e^{-x}cos2x\\[10pt]
\end{align*}
$$



```
````
# 二阶常系数非齐次线性微分方程

## 概念

形如：${y}'' +p{y}' +qy=f(x)\ (p,q\in 常数)$ ，$f(x)$为已知的连续函数，叫做自由项
且$f(x)\ne 0$的方程
有时，我们称${y}'' +p{y}' +qy=0$是${y}'' +p{y}' +qy=f(x)$的导出方程
即，非齐次方程${y}'' +p{y}' +qy=f(x)$的导出方程是齐次方程
## 其通解的结构


xxxx

**题目**

若 $y_{1}=x^{2}-2x$、$y_{2}=x^{2}-2x+1$、$y_{3}=e^{-2x}+x^{2}-2x$ 是某二阶常系数非齐次线性微分方程的三个特解，则该微分方程的通解为（　）

A. $y=(C_{1}+C_{2}x)e^{-2x}+x^{2}-2x$

B. $y=C_{1}+C_{2}e^{-2x}+x^{2}-2x$

C. $y=(C_{1}+C_{2}x)e^{-2x}+e^{-2x}-1$

D. $y=C_{1}+C_{2}e^{-2x}+x^{2}-1$
?

````````col
```````col-md
flexGrow=20
===

**答案**：B

**解析**

> 非齐次线性方程任意两个特解之差，是其对应齐次方程的解。计算：
> $$y_{2}-y_{1}=1$$
> $$y_{3}-y_{1}=e^{-2x}$$
> 这两个函数 $1$ 与 $e^{-2x}$ 之比不是常数，线性无关，构成齐次方程的两个线性无关解，因此齐次通解为
> $$C_{1}\cdot 1+C_{2}e^{-2x}$$
> 再取任一非齐次特解（如 $y_{1}=x^{2}-2x$），得原方程通解
> $$y=C_{1}+C_{2}e^{-2x}+x^{2}-2x$$
> 故选 B。

**考点**

线性微分方程解的结构（由特解之差构造齐次通解）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz

非齐次线性方程任意两个特解之差，是其对应齐次方程的解
其(非齐次方程)的通解 = 其导出方程(齐次方程)的通解 + 其(非齐次方程)的一个特解
## 非齐次方程特解的性质
- [*] 若 $y_{1}(x)$是$y''+py'+qy=f_{1}(x)$的特解，$y_{2}(x)$是$y''+py'+qy=f_{2}(x)$的特解
    则，$y_{1}(x)+y_{2}(x)$是$y''+py'+qy=f_{1}(x)+f_{2}(x)$的特解
- [*] 设$y_{1}(x)，y_{2}(x)$都是${y}'' +p{y}' +qy=f(x)$的特解
    则，$y_{1}(x)-y_{2}(x)$是其对应的齐次方程(导出方程)的特解
## 求非齐次方程通解的方法





xxxx

**题目**

已知常系数线性微分方程为 $y''-ay'-by=5e^{-x}$，有特解 $y=-xe^{-x}$，求通解。
?

````````col
```````col-md
flexGrow=20
===

**答案**：$y=C_{1}e^{-x}+C_{2}e^{4x}-xe^{-x}$

**解析**

> 先由已知特解反求系数 $a,b$。对 $y=-xe^{-x}$ 求导：
> $$y'=-(e^{-x}-xe^{-x})=(x-1)e^{-x}$$
> $$y''=e^{-x}-(x-1)e^{-x}=(2-x)e^{-x}$$
> 代入原方程：
> $$(2-x)e^{-x}-a(x-1)e^{-x}+bxe^{-x}=5e^{-x}$$
> 两边除以 $e^{-x}$，整理关于 $x$ 的系数：
> $$x(-1-a+b)+(2+a)=5$$
> 比较系数得
> $$\begin{cases}-1-a+b=0\\[2pt] 2+a=5\end{cases}\;\Longrightarrow\;a=3,\quad b=4$$
> 于是原方程为
> $$y''-3y'-4y=5e^{-x}$$
> 其对应齐次方程的特征方程为
> $$r^{2}-3r-4=0\;\Longrightarrow\;(r+1)(r-4)=0$$
> 特征根为 $r_{1}=-1$，$r_{2}=4$，故齐次通解为
> $$Y=C_{1}e^{-x}+C_{2}e^{4x}$$
> 已知 $-xe^{-x}$ 是原方程的一个特解，因此所求通解为
> $$y=C_{1}e^{-x}+C_{2}e^{4x}-xe^{-x}$$


**另一解法：** 
由特解求出a,b
$y' = -e^{-x} + xe^{-x} = (-1+x)e^{-x}$
$y'' = e^{-x} - (-1+x)e^{-x} = (2-x)e^{-x}$

代入原方程：
$$
\begin{align*}
&e^{-x}(2-x) - a e^{-x}(-1+x) + b x e^{-x} = 5e^{-x}\\[4pt]
&e^{-x}\left[(2-x) - a(-1+x) + b x\right] = 5e^{-x}\\[4pt]
&2-x -a(-1+x) +b x = 5
\end{align*}
$$

代入特殊值求解系数：
- 令$x=1$，消去含$a$的项，得$2-1 +b =5$，解得$b=4$
- 令$x=0$，消去含$b$的项，得$2 +a =5$，解得$a=3$

得到原微分方程：
$$
y'' -3y' -4y = 5e^{-x}
$$

求解齐次方程通解：
特征方程：
$$
\begin{align*}
&r^2 -3r -4 = 0\\[4pt]
&因式分解\\[4pt]
&(r+1)(r-4)=0\\[4pt]
&\Rightarrow r_1=-1,\ r_2=4
\end{align*}
$$
因此齐次通解为
$$
Y(x) = C_1 e^{-x} + C_2 e^{4x}
$$

非齐次方程的通解为齐次通解加特解：
$$
y(x) = C_1 e^{-x} + C_2 e^{4x} - xe^{-x}
$$



**考点**

二阶常系数非齐次线性微分方程；由特解反求系数，再求通解
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz




$\because$ 非齐次方程的通解 = 其导出方程(齐次方程)的通解 + 其(非齐次方程)的一个特解
$\therefore$ 求通解的话，只用在求齐次方程通解的基础上再求一下非齐次方程的特解
重点在于求非齐次方程的特解，求非齐次方程特解的方法有一下两种：
- [*] 待定系数法
- [*] Haviside算子法( 由物理学家Haviside发明，可以用，但在数学上认为是不严谨)
    ( 仅用于快速计算或验证结果)
## 求非齐次方程的特解(用待定系数法)
对于${y}'' +p{y}' +qy=f(x)$，考试大纲要求会以下两种情况下的特解
设$p_{n}(x)，p_{m}(x)$分别为x的n次，m次多项式
### 情况1



xxxx

**题目**

用待定系数法求微分方程 $y''-3y'-4y=xe^{-x}$ 的特解时，其特解 $y^{*}$ 可设为（　）

A. $ax+b$

B. $(ax+b)e^{-x}$

C. $x(ax+b)e^{-x}$

D. $x^{2}(ax+b)e^{-x}$
?

````````col
```````col-md
flexGrow=20
===

**答案**：C

**解析**

> 先求对应齐次方程的特征方程：
> $$r^{2}-3r-4=0\;\Longrightarrow\;(r-4)(r+1)=0$$
> 特征根为 $r_{1}=4$，$r_{2}=-1$。
> 方程右端为 $xe^{-x}$，属于 $P_{n}(x)e^{\alpha x}$ 型，其中 $\alpha=-1$，$P_{n}(x)=x$ 为一次多项式。由于 $\alpha=-1$ 恰好是特征方程的**单根**，按待定系数法，特解应在多项式前乘一个 $x$：
> $$y^{*}=x(ax+b)e^{-x}$$
> 故选 C。

**考点**

二阶常系数非齐次方程待定系数法（$\alpha$ 为单根时特解乘 $x$）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz





当自由项 $f(x)=p_{n}(x )e^{\alpha x}$ 时，特解要设为 $y^{*} =e^{\alpha x} Q_{n} (x)x^{k}$ 
- [*] 对 $y^{*} =e^{\alpha x} Q_{n} (x)x^{k}$ 的详细说明

$$
\begin{align*}
e^{\alpha x} Q_{n} (x)x^{k}
\begin{cases}


&e^{\alpha x} :从自由项中照抄过来\\[10pt]

&Q_{n} (x):
\begin{cases}
p_{n}(x)是x的n次特殊多项式 \\[3pt] 
Q_{n}(x)是x的n次一般多项式 \\[3pt]
Q_{n}(x)=a_nx^n+a_{n-1}x^{n-1}+\dots+a_1x+a_0\\[3pt]
x的n次一般多项式就是x的n次的所有多项式\\[3pt]
x的n次特殊多项式，就是在x的n次一般多项式的基础上加一些限制的条件\\[3pt]
eg：
\begin{cases}
若p_{n}(x)=1，则Q_{n} (x)=a_0x^0=a_0\\[3pt]
若p_{n}(x)=x，则Q_{n} (x)=ax+b（a≠0）\\[3pt]
若p_{n}(x)=x^2，则Q_{n} (x)=ax²+bx+c（a≠0）\\[3pt]
若p_{n}(x)=x^3，则Q_{n} (x)=ax^3+bx^2+cx+d（a≠0）\\[3pt]
\end{cases}\\[10pt]
\end{cases}\\[10pt]

&k:
\begin{cases}
先算非齐次方程的导出方程的特征方程的根 r_1与r_2 \\[3pt]  
k就是\alpha 与r_1，r_2相等的个数\\[3pt]
找k的步骤：\\[3pt]
一看：看自由项中的\alpha 是什么\\[3pt]
二算：算非齐次方程的导出方程的特征方程的根 r_1与r_2\\[3pt]
三比较：
\begin{cases}
看自由项中的\alpha 与特征方程的根 r_1，r_2相等的个数\\[3pt]
若\alpha \ne r_1，\alpha \ne r_2，则k=0\\[3pt]
若\alpha = r_1或\alpha = r_2(r_1 \ne r_2)，则k=1\\[3pt]
若\alpha =r_1=r_2，则k=2\\[3pt]
\end{cases}\\[10pt]
\end{cases}\\[10pt]

\end{cases}\\[10pt]
\end{align*}
$$

````col
```col-md

- [*] ==例子==

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&y''-2y'+5y=1\cdot e^x\\[10pt]

&{\color[RGB]{90,109,128} 
自由项为1\cdot e^x
\begin{cases}
\alpha =1\\[3pt]
p_n(x)=1\\[3pt]
\end{cases}}\\[10pt]

&设特解为y^*=e^{\alpha x}Q_n(x)x^k\\[10pt]
\bullet&\quad e^x照抄\\[10pt]
\bullet&\quad p_n(x)=1，Q_n(x)=a_0x^0=a \\[10pt]
\bullet&\quad k=0
\begin{cases}
一看:\alpha =1\\[10pt]

二算
\begin{cases}
导出方程y''-2y'+5y=0 \\[3pt]
特征方程r^2-2r+5=0\\[3pt]
r_{1,2}=\frac{2\pm 4i}{2}=1\pm 2i\\[3pt]
r_1=1+2i，r_2=1-2i \\[3pt]
\end{cases}\\[10pt]

三比较:\\[10pt]
k=
\begin{cases}
\because \alpha \ne r_1 \ne r_2\\[3pt]
\therefore k=0\\[3pt]
\end{cases}\\[10pt]
\end{cases}\\[10pt]

&\quad  \Rightarrow 设y^*=ae^x\cdot x^0=ae^x\\[10pt]
\bullet&\quad 代入原方程\\[1pt]
&\quad \Rightarrow ae^x-2ae^x+5ae^x=e^x \\[8pt]
&\quad \Rightarrow 4a=1\\[8pt]
&\quad \Rightarrow a=\frac{1}{4} \\[8pt]
&\quad \Rightarrow 特解y^*=\frac{1}{4}e^x\\[8pt]
\bullet&\quad 导出方程的通解:\\[1pt]
&\quad y(x)=e^x (c_{1}cos2x+c_{2}sin2x )\\[10pt]
\bullet&\quad 非齐次方程的通解:\\[1pt]
&\quad y(x)=e^x (c_{1}cos2x+c_{2}sin2x )+\frac{1}{4}e^x
\end{align*}
$$

```

```col-md

- [*] ==情况1.用待定系数法求特解的总结==

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&y''+py'+qy=p_n(x)e^{\alpha x}\\[10pt]
&设特解为y=e^{\alpha x}Q_n(x)x^k\\[10pt]
\bullet&\quad e^{\alpha x}照抄\\[10pt]
\bullet&\quad p_n(x)写成Q_n(x) \\[10pt]
\bullet&\quad 求k
\begin{cases}
一看\alpha \\[10pt]

二算
\begin{cases}
非齐次方程的导出方程\\[3pt]
导出方程的特征方程\\[3pt]
解出r_1与r_2 \\[3pt]
\end{cases}\\[10pt]

三比较:\\[10pt]
k=
\begin{cases}
0，\alpha \ne r_1，\alpha \ne r_2\\[3pt]
1，\alpha = r_1或\alpha = r_2(r_1 \ne r_2)\\[3pt]
2，\alpha =r_1=r_2\\[3pt]
\end{cases}\\[10pt]
\end{cases}\\[10pt]

\bullet&\quad 将特解代入原方程可解出Q_n(x)的系数\\[1pt]
&\quad  \Rightarrow 特解\\[10pt]
\bullet&\quad 求出导出方程的通解\\[10pt]
\bullet&\quad 非齐次方程的通解\\[1pt]
&\quad =其导出方程的通解+其特解
\end{align*}
$$

```
````
### 情况2
当自由项 $f(x)=e^{\alpha x}[p_{m}(x )cos\beta x+p_{n}(x )sin\beta x]$ 时，
特解要设为 $y^{*} =e^{\alpha x}[Q_{l}^{(1)}(x)cos\beta x+Q_{l}^{(2)}(x)sin\beta x]x^{k}$ 
- [*] 对 $y^{*} =e^{\alpha x}[Q_{l}^{(1)}(x)cos\beta x+Q_{l}^{(2)}(x)sin\beta x]x^{k}$ 的详细说明

$$
\begin{align*} 
\begin{cases}


&e^{\alpha x} :从自由项中照抄过来\\[10pt]

&Q_{l}^{(1)}(x),Q_{l}^{(2)}(x):
\begin{cases}
l取m与n的最大值 \\[3pt] 
Q_{l}^{(1)}(x)与Q_{l}^{(2)}(x)是两个不同的x的l次一般多项式 \\[3pt]
eg：
\begin{cases}
若p_{0}(x)=2,p_{1}(x)=3x，则l取1\\[3pt]
\Rightarrow Q_{l}^{(1)}(x)=a_1x+b_1，Q_{l}^{(2)}(x)=a_2x+b_2\\[3pt]
\end{cases}\\[10pt]
\end{cases}\\[10pt]

&k:
\begin{cases}
一看：
\begin{cases}
看自由项中的\alpha ,\beta 是什么\\[3pt]
写出\alpha \pm \beta i\\[3pt]
\end{cases}\\[10pt]
二算：算非齐次方程的导出方程的特征方程的根 r_1与r_2\\[3pt]
三比较：
\begin{cases}
若\alpha \pm \beta i \ne r_1与r_2，则k=0\\[3pt]
若\alpha \pm \beta i = r_1与r_2，则k=1\\[3pt]
\end{cases}\\[10pt]
\end{cases}\\[10pt]



\end{cases}\\[10pt]
\end{align*}

$$

````col
```col-md

- [*] ==例子==

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&y''-2y'+5y=-e^xcos2x\\[10pt]
\bullet &\quad \because e^x是从自由项抄过来的\\[10pt]
        &\quad \therefore \alpha =1， e^{\alpha x}=e^x\\[1pt]
        &\quad（负号显然和e^{\alpha x}没关系） \\[10pt]
\bullet&\quad p_m(x)=-1，p_n(x)=0 \\[1pt]
\Rightarrow &\quad m是最高次0，则l=0 \\[1pt]
&\quad 设Q_{l}^{(1)}(x)=a_1，Q_{l}^{(2)}(x)=a_2  \\[10pt]
\bullet&\quad k=1
\begin{cases}
一看:\alpha \pm \beta i=1\pm 2i\\[10pt]

二算
\begin{cases}
导出方程y''-2y'+5y=0 \\[3pt]
特征方程r^2-2r+5=0\\[3pt]
r_{1,2}=\frac{2\pm 4i}{2}=1\pm 2i\\[3pt]
r_1=1+2i，r_2=1-2i \\[3pt]
\end{cases}\\[10pt]

三比较:\\[10pt]
k=
\begin{cases}
\because \alpha \pm \beta i=1\pm 2i\\[3pt]
\therefore k=1\\[3pt]
\end{cases}\\[10pt]
\end{cases}\\[10pt]

&\quad  \Rightarrow 设y^{*} =e^x(a_1cos2x+a_2sin2x)x^{1}\\[10pt]
\bullet&\quad 代入原方程\Rightarrow \\[1pt]
&\quad e^x(-4a_1sin2x+4a_2cos2x)=-e^xcos2x \\[8pt]
&\quad -4a_1sin2x+4a_2cos2x=0\cdot sin2x-1\cdot cos2x \\[8pt]

&\quad \Rightarrow  
\begin{cases}
-4a_1=0\\[3pt]
4a_2=-1\\[3pt]
\end{cases}
解得
\begin{cases}
a_1=0\\[3pt]
a_2=-\frac{1}{4} \\[3pt]
\end{cases}\\[10pt]

&\quad \Rightarrow 特解y^*=-\frac{1}{4}xe^xsin2x\\[8pt]
\bullet&\quad 导出方程的通解:\\[1pt]
&\quad y(x)=e^x (c_{1}cos2x+c_{2}sin2x )\\[10pt]
\bullet&\quad 非齐次方程的通解:\\[1pt]
&\quad y(x)=e^x (c_{1}cos2x+c_{2}sin2x )-\frac{1}{4}xe^xsin2x
\end{align*}
$$

```

```col-md

- [*] ==情况2.用待定系数法求特解的总结==

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&y''+py'+qy=e^{\alpha x}[p_{m}(x )cos\beta x+p_{n}(x )sin\beta x]\\[10pt]
&设特解为y^{*}=e^{\alpha x}[Q_{l}^{(1)}(x)cos\beta x+Q_{l}^{(2)}(x)sin\beta x]x^{k}\\[10pt]
\bullet&\quad e^{\alpha x}照抄\\[10pt]
\bullet&\quad 
\begin{cases}
l=max[m,n]\\[3pt]
p_{n}(x ),p_{m}(x )写成Q_{l}^{(1)}(x),Q_{l}^{(2)}(x)\\[3pt]
\end{cases}\\[10pt]
\bullet&\quad 求k
\begin{cases}
一看\alpha \pm \beta i\\[10pt]

二算
\begin{cases}
非齐次方程的导出方程\\[3pt]
导出方程的特征方程\\[3pt]
解出r_1与r_2 \\[3pt]
\end{cases}\\[10pt]

三比较:\\[10pt]
k=
\begin{cases}
0，\alpha \pm \beta i \ne r_{1,2}\\[3pt]
1，\alpha \pm \beta i = r_{1,2}\\[3pt]
\end{cases}\\[10pt]
\end{cases}\\[10pt]

\bullet&\quad 将特解代入原方程,将Q_{l}^{(1)}(x),Q_{l}^{(2)}(x)的系数定下来\\[1pt]
&\quad  \Rightarrow 特解\\[10pt]
\bullet&\quad 求出导出方程的通解\\[10pt]
\bullet&\quad 非齐次方程的通解\\[1pt]
&\quad =其导出方程的通解+其特解
\end{align*}
$$

```
````
## 求非齐次方程的特解(用Haviside 算子法)
用待定系数法写，用Haviside 算子法算——真写假算
(用于降低计算量，快速计算或验证计算结果)
### 前言
$\quad \qquad$由英国物理学家海威塞得在19世纪末提出，“D”由他引入，使得微分方程变为形式上的代数方程．许多数学家批评此方法不全面，不严谨．这让我又想起另一位物理学家，诺贝尔物理学奖得主费曼，他经常在积分号中求导，也被数学家批评不严谨甚至错误，但很多棘手的积分（甚至著名的积分，如 $\Gamma$ 函数）在他"荒唐"的方法下，却可轻易得到正确结果，这在第9讲有讲．
### 详解
````col
```col-md

$$
\begin{align*}
&引入D\\[8pt]

约定：&
\begin{cases}
D=\frac{d}{dx} ，Dy=\frac{dy}{dx} =y'\\[3pt]
D^2=\frac{d^2}{dx^2}，D^2y=\frac{d^2y}{dx^2} =y''\\[3pt]
\frac{1}{D} =\int dx，\frac{1}{D}y=\int ydx \ (c=0)\\[3pt]
\end{cases}\\[8pt]

则，&y''+py'+qy=f(x)\\[8pt]
可写成：&D^2y+pDy+qy=f(x)\\[8pt]
&(D^2+pD+q)y=f(x)\\[8pt]
\end{align*}
$$

```

```col-md

$$
\begin{align*}
\Rightarrow \\[8pt]
&D^2+pD+q=F(D)\\[1pt]
&(称F(D)为算子多项式)\\[8pt]
若是&求y，只用将F(D)除过去\\[8pt]
&y^*=\frac{f(x)}{F(D)} \\[8pt]
但，&F(D)除过去有以下情况与条件\\[8pt]
\end{align*}
$$



```
````
### 情况1
````col
```col-md

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&f(x)=ae^{\alpha x}型，(a\in 常数)\\[10pt]
&即y^{*}=\frac{1}{F(D)}ae^{\alpha x}\\[10pt]

\bullet&\quad 若F(D)|_{D=\alpha }\ne 0, \\[8pt]
\quad &\quad 则 y^{*}=\frac{1}{F(D)|_{D=\alpha }}ae^{\alpha x}(见eg_1) \\[10pt]

\bullet&\quad 若F(D)|_{D=\alpha }= 0,而 F'(D)|_{D=\alpha }\ne 0, \\[8pt]
\quad &\quad 则 y^{*}=x\cdot \frac{1}{F'(D)|_{D=\alpha }}ae^{\alpha x}(见eg_2) \\[10pt]

\bullet&\quad 若F(D)|_{D=\alpha }= 0， F'(D)|_{D=\alpha }= 0, \\[8pt]
\quad &\quad 而 F''(D)|_{D=\alpha }\ne 0, \\[8pt]
\quad &\quad 则 y^{*}=x^2\cdot \frac{1}{F''(D)|_{D=\alpha }}ae^{\alpha x}(见eg_3) \\[10pt]

\end{align*}
$$

```

```col-md

- [*] eg1：

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&y''+y'-2y=2,求y^{*}\\[8pt]
解：&\\[8pt]
&2=f(x)=2e^{0\cdot x}(\alpha =0) \\[8pt]
&F(D)=D^2+D-2 \\[8pt]
\because &\quad F(D)|_{D=0}=(D^2+D-2)|_{D=0}\ne 0 \\[8pt]
\therefore &\quad y^{*}=\frac{1}{F(D)|_{D=0}}\cdot 2 \\[8pt]
\quad &\qquad =\frac{1}{-2}\cdot 2  \\[8pt]
\quad &\qquad =-1 \\[8pt]
\end{align*}
$$

```
````
````col
```col-md

- [*] eg2：

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&y''+y'-2y=e^x,求y^{*}\\[8pt]
解：&\\[8pt]
&f(x)=e^x,(\alpha =1) \\[8pt]
&F(D)=D^2+D-2 \\[8pt]
\because &\quad F(D)|_{D=1}=(D^2+D-2)|_{D=1}=0 \\[8pt]
\quad &\quad F'(D)=2D+1，F'(D)|_{D=1}\ne 0   \\[8pt]
\therefore &\quad y^{*}=x\cdot \frac{1}{F'(D)|_{D=1}}\cdot e^x \\[8pt]
\quad &\qquad =\frac{1}{3}\cdot xe^x  \\[8pt]
\end{align*}
$$

```

```col-md

- [*] eg3：

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&y''-2y'+y=e^x,求y^{*}\\[8pt]
解：&\\[8pt]
&f(x)=e^x,(\alpha =1) \\[8pt]
&F(D)=D^2-2D+1 \\[8pt]
\because &\quad F(D)|_{D=1}=(D^2-2D+1)|_{D=1}=0 \\[4pt]
\quad &\quad F'(D)=2D-2，F'(D)|_{D=1}=0   \\[4pt]
\quad &\quad F''(D)=2，F''(D)|_{D=1}=2\ne 0   \\[4pt]
\therefore &\quad y^{*}=x^2\cdot \frac{1}{F''(D)|_{D=1}}\cdot e^x \\[8pt]
\quad &\qquad =\frac{1}{2}\cdot x^2e^x  \\[8pt]
\end{align*}
$$


```
````
### 情况2
````col
```col-md

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁

&f(x)=
\begin{cases}
cos\beta x\\[3pt]
或\\[3pt]
sin\beta x\\[3pt]
\end{cases}
型\\[8pt]

&即y^{*}=
\begin{cases}
\frac{1}{F(D)} \cdot cos\beta x\\[3pt]
或\\[3pt]
\frac{1}{F(D)} \cdot sin\beta x\\[3pt]
\end{cases}\\[8pt]

\bullet&\quad F(D)=D^2+q，(q\in 常数) \\[8pt]
\quad &\quad 若(D^2+q)|_{D=\beta i }\ne 0, \\[10pt]
\quad &\quad 则 y^{*}=
\begin{cases}
\frac{1}{(D^2+q)|_{D=\beta i }} \cdot cos\beta x\\[3pt]
或\\[3pt]
\frac{1}{(D^2+q)|_{D=\beta i }} \cdot sin\beta x\\[3pt]
\end{cases}
(i^2=-1)  \\[3pt]
\quad&\quad (见eg_4) \\[8pt]

\bullet&\quad F(D)=D^2+q，(q\in 常数) \\[8pt]
\quad &\quad 若(D^2+q)|_{D=\beta i }= 0, \\[10pt]
\quad &\quad 则 y^{*}=
\begin{cases}
x\cdot \frac{1}{(D^2+q)'} \cdot cos\beta x\\[3pt]
或\\[3pt]
x\cdot \frac{1}{(D^2+q)'} \cdot sin\beta x\\[3pt]
\end{cases}
(见eg_5)  \\[8pt]
\end{align*}
$$

```

```col-md

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
\bullet&\quad 若F(D)=D^2+pD+q，(p,q\in 常数) \\[8pt]
\quad &\quad 则F(D)|_{D^2=(\beta i)^2 } \ {\color[RGB]{90,109,128} (只代入D^2)} \\[1pt]
\quad &\qquad = pD+q-\beta^2 \\[10pt]
\quad &\quad 则 y^{*}=(\frac{1}{F(D)})|_{D^2=(\beta i)^2 } \cdot cos\beta x \\[6pt]
&\quad \qquad =(\frac{1}{pD+q-\beta^2})|_{D^2=(\beta i)^2 } \cdot cos\beta x \\[8pt]
&\quad \qquad {\color[RGB]{90,109,128} [上下同乘pD-(q-\beta^2)]}  \\[8pt]
&\quad \qquad =[\frac{pD-(q-\beta^2)}{p^2D^2-(q-\beta^2)^2}]|_{D^2=(\beta i)^2 } \cdot cos\beta x \\[8pt]
&\quad \qquad =\frac{pD-(q-\beta^2)}{-p^2\beta^2-(q-\beta^2)^2}\cdot cos\beta x{\color[RGB]{90,109,128} (D=\frac{d}{dx})}  \\[8pt]
&\quad \qquad (见eg_6)\\[8pt]
\quad &\quad y^{*}=(\frac{1}{F(D)})|_{D^2=(\beta i)^2 } \cdot sin\beta x同理 \\[6pt]
\end{align*}
$$



```
````

`````col
````col-md
- [*] eg4：
  
 $$
 \begin{align*}  % *号表示不自动加公式编号，更简洁
&y''-y=sinx,求y^{*}\\[8pt]
解：&\\[8pt]
&f(x)=sinx,(\beta =1) \\[8pt]
&F(D)=D^2-1 \\[8pt]
\because &\quad F(D)|_{D=i}=(D^2-1)|_{D=i}\ne 0 \\[4pt]
\therefore &\quad y^{*}=\frac{1}{(D^2-1)|_{D=i}}\cdot sinx \\[8pt]
\quad &\qquad =-\frac{1}{2}\cdot sinx  \\[8pt]
\end{align*}
 $$ 
  
```col-md
- [*] eg5：

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&y''+4y=sin2x,求y^{*}\\[8pt]
解：&\\[8pt]
&f(x)=sin2x,(\beta =2) \\[8pt]
&F(D)=D^2+4 \\[8pt]
\because &\quad F(D)|_{D=2i}=(D^2+4)|_{D=2i}= 0 \\[4pt]
\therefore &\quad y^{*}=x\cdot \frac{1}{(D^2+4)'}\cdot sin2x \\[8pt]
\quad &\qquad =x\cdot \frac{1}{2D}\cdot sin2x  \\[8pt]
\quad &\qquad =x\cdot \frac{1}{2}\cdot \frac{1}{D}sin2x {\color[RGB]{90,109,128} (\frac{1}{D} =\int dx)}  \\[8pt]
\quad &\qquad =\frac{x}{2}\cdot (-\frac{1}{2}\cdot cos2x)  \\[8pt]
\quad &\qquad =-\frac{x}{4}\cdot cos2x  \\[8pt]
\end{align*}
$$

```
````

````col-md
- [*] eg6：

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&y''-3y'+2y=-\frac{1}{2}cos2x,求y^{*}\\[8pt]
解：&\\[8pt]
&f(x)=-\frac{1}{2}cos2x,(\beta =2) \\[8pt]
&F(D)=D^2-3D+2 \\[8pt]
\because &\quad F(D)=D^2-3D+2 \\[4pt]
\therefore &\quad y^{*}=(\frac{1}{F(D)})|_{D^2=(2i)^2 } \cdot (-\frac{1}{2}cos2x) \\[8pt]
\quad &\qquad =(\frac{1}{D^2-3D+2})|_{D^2=(2i)^2 } \cdot (-\frac{1}{2}cos2x)  \\[8pt]
\quad &\qquad =(\frac{1}{-4-3D+2})|_{D^2=(2i)^2 } \cdot (-\frac{1}{2}cos2x)  \\[8pt]
\quad &\qquad =(\frac{1}{3D+2})|_{D^2=(2i)^2 } \cdot (\frac{1}{2}cos2x)  \\[8pt]
\quad &\qquad =[\frac{3D-2}{(3D+2)(3D-2)}]|_{D^2=(2i)^2 } \cdot (\frac{1}{2}cos2x)  \\[8pt]
\quad &\qquad =(\frac{3D-2}{9D^2-4})|_{D^2=(2i)^2 } \cdot (\frac{1}{2}cos2x)  \\[8pt]
\quad &\qquad =\frac{3D-2}{-40} \cdot \frac{1}{2}cos2x \\[8pt]
\quad &\qquad =-\frac{1}{80}(3D-2)cos2x \\[8pt]
\quad &\qquad =-\frac{1}{80}3Dcos2x+\frac{1}{40}cos2x {\color[RGB]{90,109,128} (D=\frac{d}{dx})} \\[8pt]
\quad &\qquad =\frac{1}{40}3sin2x+\frac{1}{40}cos2x {\color[RGB]{90,109,128} (cos2x)'=-2sin2x} \\[8pt]
\quad &\qquad =\frac{1}{40}(3sin2x+cos2x)\\[8pt]
\end{align*}
$$

````
`````

`````col
````col-md

### 情况3
$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&f(x)=x^k+a_1x^{k-1}+\dots +a_{k-1}x+a_k   型\\[10pt]
&即y^{*}=\frac{1}{F(D)}(x^k+a_1x^{k-1}+\dots +a_{k-1}x+a_k)\\[6pt]
\quad &\qquad =Q_k(D)(x^k+a_1x^{k-1}+\dots +a_{k-1}x+a_k)   \\[10pt]
\quad &\quad Q_k(D)是将\frac{1}{F(D)}展开为k次泰勒多项式   \\[11pt]

&常见的：
\begin{cases}
\frac{1}{1-x}的k次泰勒多项式为： \\[2pt]
1+x+x^2+\dots +x^k \\[10pt]
若是\frac{1}{1+x}=\frac{1}{1-(-x)}，则为： \\[3pt]
1+(-x)+(-x)^2+\dots +(-x)^k \\[10pt]
若是\frac{1}{-1+x}=\frac{1}{-(1-x)}，则为： \\[3pt]
-(1+x+x^2+\dots +x^k) \\[3pt]
\end{cases}\\[10pt]

\quad &\quad 见eg_7 \\[10pt]


\end{align*}
$$

```col-md

### 情况4
$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&f(x)=e^{\alpha x}\cdot v(x)型\\[8pt]
&即y^{*}=\frac{1}{F(D)}\cdot e^{\alpha x}\cdot v(x)\\[8pt]
\quad &\qquad = e^{\alpha x}\cdot \frac{1}{F(D+\alpha )}\cdot v(x)   \\[8pt]
&e^{\alpha x}不用管，\\[10pt]
&\frac{1}{F(D+\alpha )}\cdot v(x)回到之前的情况  \\[8pt]
&见eg_8，eg_9\\[8pt]
\end{align*}
$$

```
````

````col-md

- [*] eg7：
$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&y''+y'=x^2+1,求y^{*}\\[8pt]
解：&\\[8pt]
&f(x)=x^2+1,(k=2) \\[8pt]
&F(D)=D^2+D \\[8pt]
\because &\quad f(x)=x^2+1 \\[4pt]
\therefore &\quad y^{*}=\frac{1}{F(D)} \cdot f(x)  \\[8pt]
\quad &\qquad =\frac{1}{D^2+D} \cdot (x^2+1)  \\[8pt]
\quad &\qquad =\frac{1}{D} \cdot \frac{1}{1+D} \cdot (x^2+1)  \\[8pt]
\quad &\qquad  {\color[RGB]{90,109,128} \frac{1}{1+D} 的2次泰勒展开为：1-D+D^2}  \\[8pt]
\quad &\qquad =\frac{1}{D} \cdot (1-D+D^2) \cdot (x^2+1)  \\[8pt]
\quad &\qquad =(\frac{1}{D}-1+D) \cdot (x^2+1)   \\[8pt]
\quad &\qquad =\frac{1}{D}(x^2+1)-(x^2+1)+D(x^2+1)    \\[8pt]
\quad &\qquad \qquad {\color[RGB]{90,109,128} \frac{1}{D} =\int dx，  D=\frac{d}{dx}}   \\[8pt]
\quad &\qquad =\frac{1}{3}x^3-x^2+3x-1 \\[8pt]
\end{align*}
$$


````
`````
````col
```col-md

- [*] eg8：

$$
 \begin{align*}  % *号表示不自动加公式编号，更简洁
&y''+4y'+5y=e^{-2x}sinx,求y^{*}\\[8pt]
解：&\\[8pt]
&f(x)=e^{-2x}sinx,(\alpha =-2) \\[8pt]
&F(D)=D^2+4D+5 \\[8pt]
\because &\quad f(x)=e^{-2x}sinx \\[4pt]
\therefore &\quad y^{*}=\frac{1}{D^2+4D+5}\cdot e^{-2x}sinx \\[8pt]
\quad &\qquad =e^{-2x}\cdot \frac{1}{(D-2)^2+4(D-2)+5}sinx  \\[8pt]
\quad &\qquad =e^{-2x}\cdot \frac{1}{D^2+1}sinx  \\[8pt]
\quad & {\color[RGB]{90,109,128} \frac{1}{D^2+1}sinx回到情况2的第2个（\beta =1）}  \\[8pt]
\quad & {\color[RGB]{90,109,128} (D^2+1)|_{D=i}= 0}   \\[8pt]
\quad & {\color[RGB]{90,109,128} y^{*}=x\cdot \frac{1}{(D^2+1)'}\cdot sinx}  \\[8pt]
\quad &\qquad =e^{-2x}\cdot [x\cdot \frac{1}{(D^2+1)'}\cdot sinx]  \\[8pt]
\quad &\qquad =e^{-2x}\cdot x\frac{1}{2D}sinx  \\[8pt]
\quad &\qquad =\frac{1}{2}xe^{-2x}\cdot \frac{1}{D}sinx  \\[8pt]
\quad &\qquad =-\frac{1}{2}xe^{-2x}cosx  \\[8pt]
\end{align*}
$$

```

```col-md

- [*] eg9：


$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&y''-3y'+2y=2xe^{x},求y^{*}\\[8pt]
解：&\\[8pt]
&f(x)=2xe^{x},(\alpha =1) \\[8pt]
&F(D)=D^2-3D+2 \\[8pt]
\because &\quad f(x)=2xe^{x} \\[4pt]
\therefore &\quad y^{*}=\frac{1}{D^2-3D+2}\cdot 2xe^{x} \\[8pt]
\quad &\qquad =2e^{x}\cdot \frac{1}{(D+1)^2-3(D+1)+2}\cdot x  \\[8pt]
\quad &\qquad =2e^{x}\cdot \frac{1}{D^2-D}x  \\[8pt]
\quad & {\color[RGB]{90,109,128} \frac{1}{D^2-D}x回到情况3}  \\[8pt]
\quad & {\color[RGB]{90,109,128} y^{*}=\frac{1}{D}\cdot \frac{1}{D-1}x}  \\[8pt]
\quad & {\color[RGB]{90,109,128} \frac{1}{D-1}的1次泰勒展开为-1-D}  \\[8pt]
\quad & {\color[RGB]{90,109,128} y^{*}=\frac{1}{D}\cdot (-1-D)x}  \\[8pt]
\quad &\qquad =2e^{x}\cdot [\frac{1}{D}\cdot (-1-D)x]  \\[8pt]
\quad &\qquad =2e^{x}\cdot [(-\frac{1}{D}-1)x]  \\[8pt]
\quad &\qquad =2e^{x}\cdot [-\frac{1}{D}x-x]  \\[8pt]
\quad &\qquad =2e^{x}\cdot [-\frac{1}{2}x^2-x]  \\[8pt]
\quad &\qquad =-x(x+2)e^{x}  \\[8pt]
\end{align*}
$$



```
````
# n阶常系数齐次线性微分方程(n>2)
以下结论也可反推
齐次微分方程的特征方程的根
- [*] 若根为单根，即有且仅有一个实根r
    则通解中一定有  $ce^{rx}，(c\in 常数)$
- [*] 若根为2重根，即有且仅有两个实根  $r_{1}与r_{2}，且r_{1}=r_{2}=r$
    则通解中一定有  $(c_{1}+c_{2}x)e^{rx}$
- [*] 若根为k重根，即有且仅有k个实根, $r_{1}=r_{2}=\dots =r_{k}=r$
    则通解中一定有  $(c_{1}+c_{2}x+c_{3}x^2+\dots +c_{k}x^{k-1})e^{rx}$
- [*] 若根为单共轭复根，即有一对虚根  $r_{1,2}=\alpha \pm \beta i$
    则通解中一定有  $e^{\alpha x} (c_{1}cos\beta x+c_{2}sin\beta x )$
- [*] 若根为二重共轭复根，即有两对虚根  $r_{1,2}=r_{3,4}=\alpha \pm \beta i$
    则通解中一定有  $e^{\alpha x} (c_{1}cos\beta x+c_{2}sin\beta x +c_{3}xcos\beta x+c_{4}xsin\beta x)$



