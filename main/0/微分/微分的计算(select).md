#flashcards/微分/微分的计算



## 易错题


xxxx

**题目**

设函数 $f(x)=e^{x^2}-2x$，则 $\mathrm{d}f(x)=$　$\underline{\qquad\quad}$。
?
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
**这个容易把其看为$e^{x^2}=(e^{x})^2$ 事实上，$(e^{x})^2=e^{2x}$ **
<!--SR:!fsrs,2026-11-21T07:13:21.469Z,7,8.2956,1,2,1,0,0,2026-11-14T07:13:21.469Z,id=b2qcgs--> 

zzzz



## 基本求导公式




xxxx

**题目**

函数 $f(x)=\ln|x-1|$ 的导数是（　　）

- A. $f'(x)=\dfrac{1}{|x-1|}$
- B. $f'(x)=\dfrac{1}{x-1}$
- C. $f'(x)=\dfrac{1}{1-x}$
- D. 不存在
?
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
<!--SR:!fsrs,2026-11-26T04:39:24.101Z,8,8.2956,1,2,1,0,0,2026-11-18T04:39:24.101Z,id=ygovbm-->


zzzz





| 类别    | 公式                                                                                                                                                                                                                                                                                                                                                                                                     |
| :---- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 幂函数   | $\displaystyle (x^\alpha)'=\alpha x^{\alpha-1}$（$\alpha$ 为常数）<br>$\displaystyle  (x^{-1})'=-x^{-2}=-\frac{1}{x^2}$                                                                                                                                                                                                                                                                                     |
| 指数函数  | $\displaystyle (a^x)'=a^x\ln a\ (a>0,a\neq1)$<br>$\displaystyle (a^x)''=a^x(\ln a)^2$，$(e^x)'=e^x$<br>$\displaystyle (a^x)^{(n)}=a^x(\ln a)^n$，$(e^x)^{(n)}=e^x$                                                                                                                                                                                                                                       |
| 对数函数  | $\displaystyle (\log_a x)'=\frac{1}{x\ln a}\ (a>0,a\neq1)$<br>$\displaystyle (\ln x)'=\frac{1}{x}$<br>$\displaystyle (\ln(-x))'=\frac{1}{-x}\cdot(-1)=\frac{1}{x}$ <br>$\displaystyle \ln\vert x\vert=\begin{cases}\ln x,&x>0\\\ln(-x),&x<0\end{cases}$，$(\ln\vert x\vert)'=\dfrac{1}{x}\ (x\neq0)$，视绝对值而不见<br>$\displaystyle (\ln\vert u(x)\vert)'=\frac{1}{u(x)}\cdot u'(x) \ (u(x)\neq0)$，依旧视绝对值而不见 |
| 三角函数  | $\displaystyle (\sin x)'=\cos x$ <br>$\displaystyle (\cos x)'=-\sin x$ <br>$\displaystyle (\tan x)'=\sec^2x=\frac{1}{\cos^2x}=1+\tan^2x$ <br>$\displaystyle (\cot x)'=-\csc^2 x$ <br>$\displaystyle (\sec x)'=\sec x\tan x$ <br>$\displaystyle (\csc x)'=-\csc x\cot x$                                                                                                                                |
| 反三角函数 | $\displaystyle (\arcsin x)'=\frac{1}{\sqrt{1-x^2}}$<br>$\displaystyle (\arccos x)'=-\frac{1}{\sqrt{1-x^2}}$<br>$\displaystyle (\arctan x)'=\frac{1}{1+x^2}$<br>$\displaystyle (\operatorname{arccot} x)'=-\frac{1}{1+x^2}$                                                                                                                                                                             |
| 反双曲函数 | $\displaystyle \left[\ln\left(x+\sqrt{x^2+1}\right)\right]'=\frac{1}{\sqrt{x^2+1}}$<br>$\displaystyle \left[\ln\left(x+\sqrt{x^2-1}\right)\right]'=\frac{1}{\sqrt{x^2-1}}$                                                                                                                                                                                                                             |


## 四则运算



xxxx

**题目**

已知函数 $\varphi(x)$ 在点 $x=0$ 处可导，函数 $f(x)=(x-1)\varphi(x-1)$，则 $f'(1)=$（　　）

- A. $\varphi'(0)$
- B. $\varphi'(1)$
- C. $\varphi(0)$
- D. $\varphi(1)$
?
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

**另一解法：** 
$$
\begin{align*}
f'(1) &= \lim_{x \to 1} \frac{f(x)-f(1)}{x-1}\\[4pt]
&= \lim_{x \to 1} \frac{(x-1)\varphi(x-1) - 0}{x-1}\\[4pt]
&= \lim_{x \to 1} \varphi(x-1)\\[4pt]
&= \varphi(0)
\end{align*}
$$


**考点**：乘积求导（抽象函数，一点处）


```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-28T04:39:21.424Z,10,8.2956,1,2,1,0,0,2026-11-18T04:39:21.424Z,id=8e8lm4-->


zzzz



| 类别   | 公式                                                                                                                                                                                                                                                                                                 |
| :--- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 和差求导 | $\displaystyle [u(x)\pm v(x)]'=u'(x)\pm v'(x)$                                                                                                                                                                                                                                                     |
| 和差微分 | $\displaystyle d[u(x)\pm v(x)]=d[u(x)]\pm d[v(x)]$                                                                                                                                                                                                                                                 |
| 积的求导 | $\displaystyle [u(x)v(x)]'=u'(x)v(x)+u(x)v'(x)$<br><br><br>$\displaystyle [u(x)v(x)w(x)]'=u'(x)v(x)w(x)+u(x)v'(x)w(x)+u(x)v(x)w'(x)$<br><br><br>超过三个因子一般不要直接求导，另谋蹊径                                                                                                                                |
| 积的微分 | $\displaystyle d[u(x)v(x)]=u(x)d[v(x)]+d[u(x)]v(x)$                                                                                                                                                                                                                                                |
| 商的求导 | $\displaystyle \left[\frac{u(x)}{v(x)}\right]'=\frac{u'(x)v(x)-u(x)v'(x)}{[v(x)]^2},\quad v(x)\neq0$<br><br><br>$\displaystyle \left[\frac{u(x)}{v(x)}\right]'$ 可看成 $\displaystyle \left[u(x)\cdot\frac{1}{v(x)}\right]'$，是一个复合函数                                                                  |
| 商的微分 | $\displaystyle d\left[\frac{u(x)}{v(x)}\right]=\frac{v(x)d[u(x)]-u(x)d[v(x)]}{[v(x)]^2},\quad v(x)\neq0$                                                                                                                                                                                           |
| 记号说明 | $\displaystyle [u(x)v(x)]'=u'(x)v(x)+u(x)v'(x)$<br><br><br>$\displaystyle \frac{d[u(x)v(x)]}{dx}=\frac{d[u(x)]}{dx}\cdot v(x)+u(x)\cdot\frac{d[v(x)]}{dx}$<br><br><br>$\displaystyle \Rightarrow d[u(x)v(x)]=d[u(x)]\cdot v(x)+u(x)\cdot d[v(x)]$<br><br><br>即把“'”看作“$\dfrac{d}{dx}$”，（等号两边的dx抵消了） |

**注意区分符号：** 

$$
\begin{align*}
微分的平方: \quad &[D(\ )]^2 = \left( \frac{d(\ )}{dx} \right)^2 = \frac{d(\ )^2}{dx^2}\\[4pt]
二阶微分:\quad &\frac{d^2(\ )}{dx^2}=\frac{d\left( \frac{d(\ )}{dx} \right) }{dx}\\[4pt]
复合导:\quad &d(x^2)=2xdx\\[4pt]
\end{align*}
$$


## 几何意义




xxxx

**题目**

求曲线 $\begin{cases}x=e^t\cos t\\ y=e^t\sin t\end{cases}$ 在 $t=\dfrac{\pi}{2}$ 处的法线方程。
?
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
<!--SR:!fsrs,2026-11-24T04:39:05.201Z,6,8.2956,1,2,1,0,0,2026-11-18T04:39:05.201Z,id=z60f7t-->


zzzz



## 与导数的衔接



xxxx

**题目**

函数 $f(x)=e^{1-x}$，在点 $x=0.99$ 处的近似值为　$\underline{\qquad\quad}$。
?
````````col
```````col-md
flexGrow=20
===

**答案**：$1.01$

**解析**

> 用微分（线性近似）：$f(1)=1$，$f'(1)=-e^{1-x}\big|_{x=1}=-1$。
>
> $$f(0.99)\approx f(1)+f'(1)(0.99-1)=1+(-1)(-0.01)=1.01$$

**另一解法：** 

$0.99 + 0.01 = 1$
$$\lim_{x \to 1} e^{1-x} = 1$$
微分近似关系：
$$\Delta y \approx f'(x) \cdot \Delta x$$
对函数$f(x)=e^{1-x}$求导：
$$f'(x) = e^{1-x} \cdot (-1) = -e^{1-x}$$
代入$x=1$计算导数值：
$$f'(1) = -1$$
计算增量近似值：
$$
\begin{align*}
\Delta y &= f'(1) \cdot 0.01 \\
&= -0.01
\end{align*}
$$
最终近似计算：
$$1 - (-0.01) = 1.01$$









**考点**：微分的线性近似（一阶近似）


```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-26T04:38:32.273Z,8,8.2956,1,2,1,0,0,2026-11-18T04:38:32.273Z,id=8ph67k-->


zzzz








# 一元微分


## 复合函数求导与微分形式不变性


xxxx

**题目**

求函数 $y=\sqrt{2-\cos x}$ 的导数。
?
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
<!--SR:!fsrs,2026-11-27T04:37:57.900Z,9,8.2956,1,2,1,0,0,2026-11-18T04:37:57.900Z,id=55ulcz-->


zzzz




xxxx

**题目**

设 $y=e^{x\cos x}$，$\mathrm{d}y=$　$\underline{\qquad\quad}$。
?
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
<!--SR:!fsrs,2026-11-28T04:38:52.096Z,10,8.2956,1,2,1,0,0,2026-11-18T04:38:52.096Z,id=a6242t-->


zzzz



xxxx

**题目**

设函数 $y=\arctan\sqrt{x}$，求 $\dfrac{dy}{dx}$ 及 $\dfrac{dy}{dx}\big|_{x=1}$。
?
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
<!--SR:!fsrs,2026-11-26T04:38:28.590Z,8,8.2956,1,2,1,0,0,2026-11-18T04:38:28.590Z,id=qv66f2-->


zzzz


xxxx

**题目**

设 $f(x)=\ln\sqrt{1+x}$，则 $f'(1)=$（　　）

- A. $2$
- B. $1$
- C. $\dfrac{1}{2}$
- D. $\dfrac{1}{4}$
?
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
<!--SR:!fsrs,2026-11-28T04:39:16.194Z,10,8.2956,1,2,1,0,0,2026-11-18T04:39:16.194Z,id=cwol9w-->


zzzz


xxxx

**题目**

已知函数 $y=e^{\sin 2x}+\arcsin\sqrt{x}$，求 $y'$。
?
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
<!--SR:!fsrs,2026-11-23T08:52:51.617Z,8,8.2956,1,2,1,0,0,2026-11-15T08:52:51.617Z,id=3b2lo8-->


zzzz



xxxx

**题目**

设二元函数 $z=(x-y)\sin(xy)$，求 $x\dfrac{\partial z}{\partial x}-y\dfrac{\partial z}{\partial y}$。
?
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
<!--SR:!fsrs,2026-11-22T04:10:07.794Z,5,7.49448566,3.58131923,2,3,0,0,2026-11-17T04:10:07.794Z,id=eujb5g-->


zzzz



xxxx

**题目**

已知 $y=(\sin x)^x-\arctan(2+x^2)$，求 $\dfrac{dy}{dx}$。
?
````````col
```````col-md
flexGrow=20
===

**答案**：$\dfrac{dy}{dx}=(\sin x)^x\big[\ln(\sin x)+x\cot x\big]-\dfrac{2x}{x^4+4x^2+5}$

**解析**

> 幂指部分先化为指数形式：$(\sin x)^x=e^{x\ln(\sin x)}$，由对数求导法：
>
> $$\frac{d}{dx}(\sin x)^x=e^{x\ln(\sin x)}\Big[\ln(\sin x)+x\cdot\frac{\cos x}{\sin x}\Big]=(\sin x)^x\Big[\ln(\sin x)+x\cot x\Big]$$
>
> 再对 $\arctan(2+x^2)$ 用复合函数求导：
>
> $$\frac{d}{dx}\arctan(2+x^2)=\frac{2x}{1+(2+x^2)^2}=\frac{2x}{x^4+4x^2+5}$$
>
> 两项相减：
>
> $$\frac{dy}{dx}=(\sin x)^x\Big[\ln(\sin x)+x\cot x\Big]-\frac{2x}{x^4+4x^2+5}$$

**考点**：幂指函数对数求导法 + 复合函数求导


```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-22T06:53:18.734Z,7,8.2956,1,2,1,0,0,2026-11-15T06:53:18.734Z,id=01kj2s-->


zzzz


xxxx

**题目**

设函数 $y=f^2(\cos x)$，其中 $f$ 可导，则 $y'=$（　　）

- A. $2f(\cos x)$
- B. $2f(\cos x)f'(\cos x)$
- C. $-2\sin x f(\cos x)f'(\cos x)$
- D. $2\sin x f(\cos x)f'(\cos x)$
?
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
<!--SR:!fsrs,2026-11-23T06:31:28.946Z,9,8.2956,1,2,1,0,0,2026-11-14T06:31:28.946Z,id=111n2n-->


zzzz


### 二阶导



xxxx

**题目**

设 $f(x)=(7x-6)^{\frac{8}{7}}+9x$，则 $f''(1)=$　$\underline{\qquad\quad}$。
?
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
<!--SR:!fsrs,2026-11-24T06:55:14.494Z,7,8.2956,1,2,1,0,0,2026-11-17T06:55:14.494Z,id=t5n721-->


zzzz


xxxx

**题目**

设函数 $f(x)=xe^{-x}+\sin x$，则 $f''(x)=$（　　）

- A. $(x+2)e^{-x}+\sin x$
- B. $(x+2)e^{-x}-\sin x$
- C. $(x-2)e^{-x}+\sin x$
- D. $(x-2)e^{-x}-\sin x$
?
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

**另一解法**

$$
\begin{align*}


&f'=e^{-x}-xe^{-x}+\cos x\\[6pt]

&三项分别再导：\\[6pt]

&(e^{-x})'=\underbrace{-e^{-x}}_{\text{链式：外层 }e^u,\ u=-x,\ u'=-1}\\[6pt]
&(-xe^{-x})'=-(xe^{-x})'=-\big[e^{-x}+x\,(-e^{-x})\big]=-e^{-x}+xe^{-x}\\[6pt]
&(\cos x)'=-\sin x\\[6pt]

&相加：\\[6pt]

&f''=-e^{-x}-e^{-x}+xe^{-x}-\sin x=(x-2)e^{-x}-\sin x\\[6pt]



\end{align*}
$$

**考点**：乘积与复合函数二阶导


```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-23T08:03:33.290Z,8,8.2956,1,2,1,0,0,2026-11-15T08:03:33.290Z,id=6b1o0u-->


zzzz




xxxx

**题目**

函数 $f(x)$ 二阶可导，且 $y=f(e^x)$，则 $y''=$（　　）

- A. $f''(e^x)$
- B. $f''(e^x)e^{2x}$
- C. $e^x f'(e^x)+e^{2x}f''(e^x)$
- D. $e^x f'(e^x)+e^x f''(e^x)$
?
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
<!--SR:!fsrs,2026-11-23T07:27:02.121Z,8,8.2956,1,2,1,0,0,2026-11-15T07:27:02.121Z,id=61gsya-->


zzzz


xxxx

**题目**

已知 $\displaystyle\int f(x)dx=\ln(x^2+2)+C$，则 $df(x)=$ $\underline{\qquad\qquad}$。
?
````````col
```````col-md
flexGrow=20
===

**答案**：$\dfrac{4-2x^2}{(x^2+2)^2}dx$

**解析**

> $f(x)=[\ln(x^2+2)]'=\frac{2x}{x^2+2}$，$f'(x)=\frac{2(x^2+2)-2x\cdot2x}{(x^2+2)^2}=\frac{4-2x^2}{(x^2+2)^2}$，故 $df(x)=\frac{4-2x^2}{(x^2+2)^2}dx$。

**考点**：由不定积分求 f 再微分

```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-24T07:14:49.002Z,10,8.2956,1,2,1,0,0,2026-11-14T07:14:49.002Z,id=edvc1u-->

zzzz





$$
\begin{align*}
&设u=g(x)在点处可导(泛指的点)，y=f(u)在点u=g(x)处可导，\\[4pt]
&则复合函数求导法则为：\\[4pt]

&\begin{array}{@{}c@{\qquad}c@{}}

\begin{aligned}
&求导顺序：(f\to g\to x)  \\[4pt]
&\left\{f[g(x)]\right\}' = f'[g(x)]\cdot g'(x) \\[4pt]
&\left\{f[v(g(x))]\right\}' = f'[v(g(x))] \cdot v'[g(x)] \cdot g'(x)\\[4pt]
&微分形式的不变性:\\[4pt]
&df(u) = f'(u)\cdot du\\[4pt]
\displaystyle d\{f[v(g(x))]\}&=f'[v(g(x))]\cdot d[v(g(x))]\\[4pt]
\displaystyle &=f'[v(g(x))]\cdot v'[g(x)]\cdot d[g(x)]\\[4pt]
\displaystyle &=f'[v(g(x))]\cdot v'[g(x)]\cdot g'(x)\,dx\\[4pt]
\end{aligned}
&
\begin{aligned}
&即把“'”看作“\dfrac{d}{dx}”\\[4pt]
&推导:\\[4pt]
&\frac{df[g(x)]}{dx} = \frac{df[g(x)]}{dg(x)} \cdot \frac{dg(x)}{dx}\\[4pt]
&\frac{df[g(x)]}{dx} = f'[g(x)] \cdot \frac{dg(x)}{dx}\\[4pt]
&df[g(x)]= f'[g(x)]dg(x)\\[4pt]
\end{aligned}

\end{array}\\[4pt]

\end{align*}

$$

## 分段函数求导
设
$$f(x)=
\begin{cases}
f_1(x), & x\geq x_0 \\
f_2(x), & x<x_0
\end{cases}
$$
其中，$f_1(x),f_2(x)$分别在$x>x_0,x<x_0$时可导，则：

`````col
````col-md
flexGrow=1
===

**①** 在分段点$x_0$处用导数定义求导：(因为断点处，导数可能不存在)
$$f'_+(x_0)=\lim_{x\to x_0^+}\frac{f_1(x)-f(x_0)}{x-x_0}$$
$$f'_-(x_0)=\lim_{x\to x_0^-}\frac{f_2(x)-f(x_0)}{x-x_0}$$
根据$f'_+(x_0)$是否等于$f'_-(x_0)$来判定$f'(x_0)$是否存在。

````

````col-md
flexGrow=1
===

**②** 在非分段点，用导数公式求导：
即
$x>x_0$时，$f'(x)=f'_1(x)$
$x<x_0$时，$f'(x)=f'_2(x)$




````
`````

## 含绝对值求导

**带绝对值的话，通过写成分段函数的形式去掉绝对值。** 


eg：函数 $y=|x e^{-x}|$，求 $y''$。
去绝对值，将函数写为分段形式：

$\displaystyle y=|x e^{-x}|=\begin{cases}x e^{-x}, & x\geq 0 \\-x e^{-x}, & x<0 \end{cases}$ 

`````col
````col-md
flexGrow=1
===

**①** 判断分段点$x=0$处的导数存在性：
左导数：
$$y'_-(0)=\lim_{x\to 0^-} \frac{y(x)-y(0)}{x-0}=\lim_{x\to 0^-} \frac{-x e^{-x} - 0}{x-0}=-1$$
右导数：
$$y'_+(0)=\lim_{x\to 0^+} \frac{y(x)-y(0)}{x-0}=\lim_{x\to 0^+} \frac{x e^{-x} - 0}{x-0}=1$$
因为 $y'_-(0)\neq y'_+(0)$，所以$y'(0)$不存在，因此$y''(0)$不存在。

````

````col-md
flexGrow=1
===

**②**分别在开区间内计算二阶导数：
当$x>0$时：
$$y'=e^{-x} + x e^{-x}\cdot (-1)=(1-x)e^{-x}$$
$$
\begin{align*}
y''&=-e^{-x} + (1-x)(-e^{-x})\\
&=(x-2)e^{-x}
\end{align*}
$$
当$x<0$时：
$$y'=-e^{-x} + (-x e^{-x})\cdot (-1)=(x-1)e^{-x}$$
$$y''=(2-x)e^{-x}$$



````
`````

综上，函数的二阶导数为：
$$y''(x)=
\begin{cases}
(x-2)e^{-x}, & x>0 \\
(2-x)e^{-x}, & x<0
\end{cases}$$

## 反函数求导

**注**：某区间内严格单调 ⟹ 每个 y 只对应一个 x ⟹ 某区间内有反函数

设$y=f(x)$为单调、可导函数，且$f'(x)\neq0$，
则存在反函数$x=f^{-1}(y)$，设$f^{-1}(\ )=\varphi(\ )$，即反函数为$x=\varphi(y)$。

$\displaystyle f'(x) = \frac{dy}{dx}, \quad \varphi'(y) = \frac{dx}{dy}$ 

$\displaystyle \because \frac{dx}{dy} = \frac{1}{\frac{dy}{dx}}$ 
$\displaystyle \therefore \varphi'(y) = \frac{1}{f'(x)}$ 
### 二阶导



xxxx

**题目**

已知函数 $y=x\arctan x$，则 $y''=$　$\underline{\qquad\quad}$。
?
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
<!--SR:!fsrs,2026-11-28T04:36:39.755Z,10,8.2956,1,2,1,0,0,2026-11-18T04:36:39.755Z,id=l5irk8-->


zzzz






`````col
````col-md
flexGrow=1
===

$$\begin{align*}
&\varphi''(y) = -\frac{f''(x)}{\left[f'(x)\right]^3}\\[4pt]
&f''(x) = -\frac{\varphi''(y)}{\left[\varphi'(y)\right]^3}\\[4pt]
\end{align*}$$

````

````col-md
flexGrow=1
===

$$
\begin{align*}
\varphi''(y) &= \frac{d\left(\frac{dx}{dy}\right)}{dy} = \frac{d\left(\frac{1}{f'(x)}\right)}{dy} \\[4pt]
&= \frac{d\left(\frac{1}{f'(x)}\right)}{dx} \cdot \frac{dx}{dy}\\[4pt]
&= -\frac{1}{\left[f'(x)\right]^2} \cdot f''(x) \cdot \frac{1}{f'(x)}\\[4pt]
&= -\frac{f''(x)}{\left[f'(x)\right]^3}\\[4pt]
\end{align*}
$$



````
`````

## 隐函数求导



xxxx

**题目**

设 $y=f(x)$ 由方程 $y^2-3xy+x^3=1$ 确定，则 $y'=$（　　）

- A. $\dfrac{3x^2-3y}{2y-3x}$
- B. $\dfrac{3y-3x^2}{2y-3x}$
- C. $\dfrac{2y-3x}{3x^2-3y}$
- D. $\dfrac{3x-2y}{3x^2-3y}$
?
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
<!--SR:!fsrs,2026-11-24T04:36:32.554Z,6,8.2956,1,2,1,0,0,2026-11-18T04:36:32.554Z,id=n5ifj9-->


zzzz



xxxx

**题目**

设函数 $y=y(x)$ 是由方程 $\cos y=e^{2x+y}+x^3-y^2+3\pi$ 所确定的隐函数，求 $\dfrac{dy}{dx}$。
?
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


**另一解法** 
设 $z(x,y) = -\cos y + e^{2x+y} + x^3 - y^2 + 3\pi$。

$$dz = z_x' \cdot dx + z_y' \cdot dy$$

$$
\begin{align*}
z_x' &= 2e^{2x+y} + 3x^2 \\[4pt]
z_y' &= \sin y + e^{2x+y} - 2y
\end{align*}
$$

$$
\begin{align*}
dz &= 0 \\[4pt]
&= \left(2e^{2x+y} + 3x^2\right)dx + \left(\sin y + e^{2x+y} - 2y\right)dy
\end{align*}
$$

$$
\Rightarrow \frac{dy}{dx} = \frac{-\left(2e^{2x+y} + 3x^2\right)}{\sin y + e^{2x+y} - 2y}
$$




**考点**：隐函数求导（含复合）


```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-26T06:55:10.715Z,9,8.2956,1,2,1,0,0,2026-11-17T06:55:10.715Z,id=oabex3-->


zzzz


xxxx

**题目**

设函数 $y=f(x)$ 由方程 $x^2 y-e^y+3=y$ 所确定，则 $\dfrac{dy}{dx}=$　$\underline{\qquad\quad}$。
?
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
<!--SR:!fsrs,2026-11-24T08:52:55.684Z,9,8.2956,1,2,1,0,0,2026-11-15T08:52:55.684Z,id=ghraeg-->


zzzz



设函数$y=f(x)$是由方程$F(x,y)=0$确定的可导函数，求解步骤如下：
1.  将方程$F(x,y)=0$看作$F(x,f(x))=0$，即把$y$视为关于$x$的函数，求导时将$f(x)$作为中间变量。
2.  对方程$F(x,f(x))=0$两边对自变量$x$求导，得到关于$f'(x)$的方程。
3.  从求导后的方程中解出$f'(x)$。

## 参数方程求导


xxxx

**题目**

求参数方程 $\begin{cases}x=\dfrac12\cos^3 t\\ y=\dfrac12\sin^3 t\end{cases}$ 的导数 $\dfrac{dy}{dx}=$　$\underline{\qquad\quad}$。
?
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
<!--SR:!fsrs,2026-11-25T04:38:55.364Z,7,8.2956,1,2,1,0,0,2026-11-18T04:38:55.364Z,id=08quhd-->


zzzz


xxxx

**题目**

设曲线方程为 $\begin{cases}x=2\cos\theta+\sin 2\theta\\ y=2\sin\theta+\cos 2\theta\end{cases}$（$\theta$ 为参数），则 $\dfrac{dy}{dx}\bigg|_{\theta=0}=$　$\underline{\qquad\quad}$。
?
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
<!--SR:!fsrs,2026-11-28T04:39:07.950Z,10,8.2956,1,2,1,0,0,2026-11-18T04:39:07.950Z,id=nemo7z-->


zzzz



xxxx

**题目**

设函数 $y=y(x)$ 由参数方程 $\begin{cases}x=2\cos^3 t\\ y=2\sin^3 t\end{cases}$ 确定，则 $\dfrac{dy}{dx}\bigg|_{t=\frac{\pi}{4}}=$（　　）

- A. $1$
- B. $-1$
- C. $2$
- D. $-2$
?
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
<!--SR:!fsrs,2026-11-21T08:53:05.099Z,6,8.2956,1,2,1,0,0,2026-11-15T08:53:05.099Z,id=ttre0l-->


zzzz


xxxx

**题目**

对于函数 $y=\begin{cases}x=(t+1)^3+1\\ y=\arcsin\sqrt{t}\end{cases}$，求 $\dfrac{dy}{dx}\bigg|_{t=\frac{1}{2}}$。
?
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
<!--SR:!fsrs,2026-11-21T07:37:57.409Z,6,8.2956,1,2,1,0,0,2026-11-15T07:37:57.409Z,id=kyrcmd-->


zzzz




xxxx

**题目**

设参数方程 $\begin{cases}x=e^{-t}+\cos t\\ y=e^t+\sin t\end{cases}$，则 $\dfrac{dy}{dx}\bigg|_{t=0}=$（　　）

- A. $2$
- B. $-2$
- C. $1$
- D. $-1$
?
````````col
```````col-md
flexGrow=20
===

**答案**：B

**解析**

> 参数方程求导：
>
> $$\frac{dy}{dx}=\frac{\frac{dy}{dt}}{\frac{dx}{dt}}=\frac{e^t+\cos t}{-e^{-t}-\sin t}$$
>
> 代入 $t=0$：$\dfrac{1+1}{-1-0}=\dfrac{2}{-1}=-2$。选 B。

**考点**：参数方程求导（一点处）


```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-12-26T06:58:52.858Z,36,33.00890883,1,2,2,0,0,2026-11-20T06:58:52.858Z,id=186vyv-->


zzzz





设函数$y=y(x)$由参数方程$\begin{cases} x = g(t) \\ y = w(t) \end{cases}$确定，其中，$t$是参数，且$g(t),w(t)$均可导，$g'(t)\neq0$，

则：$\displaystyle y'=\frac{dy}{dx}=\frac{\frac{dy}{dt}}{\frac{dx}{dt}}=\frac{w'(t)}{g'(t)}$ 

### 二阶导



xxxx

**题目**

已知 $\begin{cases}x=2(t-\sin t)\\ y=2(1-\cos t)\end{cases}$，$0\leq t\leq 2\pi$，求 $\dfrac{d^2y}{dx^2}$。
?
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


**另一解法：** 


$dx = 2(1-\cos t)\cdot dt$
$dy = 2\sin t\cdot dt$

$$\frac{d^2 y}{dx^2} = \frac{d\left( \frac{dy}{dx} \right)}{dx}$$

$$\frac{dy}{dx} = \frac{\sin t}{1-\cos t}$$

$$
d\left( \frac{\sin t}{1-\cos t} \right) = \frac{\cos t(1-\cos t) - \sin t\cdot \sin t}{(1-\cos t)^2} \cdot dt
$$

$$
\frac{d^2 y}{dx^2} = \frac{d\left( \frac{\sin t}{1-\cos t} \right)}{2(1-\cos t)\cdot dt}
$$

$$
\begin{align*}
&= \frac{\cos t(1-\cos t) - \sin t\cdot \sin t}{2(1-\cos t)^3} \\[6pt]
&= \frac{\cos t - (\cos^2 t + \sin^2 t)}{2(1-\cos t)^3} \\[6pt]
&= \frac{-1}{2(1-\cos t)^2}
\end{align*}
$$






**考点**：参数方程二阶导（摆线）


```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-28T04:38:46.022Z,10,8.2956,1,2,1,0,0,2026-11-18T04:38:46.022Z,id=ad18p1-->


zzzz





xxxx

**题目**

设 $\begin{cases}x=\cos t\\ y=t\cos t-\sin t\end{cases}$（$t$ 为参数），则 $\dfrac{d^2y}{dx^2}\bigg|_{t=\pi/4}=$（　　）

- A. $-\sqrt{2}$
- B. $\sqrt{2}$
- C. $\dfrac{\sqrt{2}}{2}$
- D. $-\dfrac{\sqrt{2}}{2}$
?
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


**另一解法：** 
$$
\frac{d^2 y}{dx^2} = \frac{d\left( \frac{dy}{dx} \right)}{dx}
$$
$$
dx = -\sin t \cdot dt
$$
$$
dy = -t\sin t \cdot dt
$$
$$
\Rightarrow \frac{dy}{dx} = t
$$
$$
\begin{align*}
\frac{d^2 y}{dx^2} &= \frac{dt}{dx} \\[4pt]
&= \frac{dt}{-\sin t \cdot dt} \\[4pt]
&= -\frac{1}{\sin t}
\end{align*}
$$
$$
t=\frac{\pi}{4} \Rightarrow \frac{d^2 y}{dx^2} = -\sqrt{2}
$$





**考点**：参数方程二阶导


```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-28T04:39:18.666Z,10,8.2956,1,2,1,0,0,2026-11-18T04:39:18.666Z,id=ucf4ns-->




zzzz







设函数$y=y(x)$由参数方程$\begin{cases} x = g(t) \\ y = w(t) \end{cases}$确定，其中，$t$是参数，且$g(t),w(t)$均二阶可导，$g'(t)\neq0$，

则：$\displaystyle y''(x)=\frac{d^2 y}{dx^2}=\frac{d\left(\frac{dy}{dx}\right)}{dx}=\frac{d\left( \frac{w'(t)}{g'(t)}\right)}{dx}=\frac{\frac{d\left( \frac{w'(t)}{g'(t)} \right)}{dt}}{\frac{dx}{dt}}=\frac{\frac{d\left( \frac{w'(t)}{g'(t)} \right)}{dt}}{g'(t)}$ 
$$d\left( \frac{w'(t)}{g'(t)} \right) = \frac{w''(t)g'(t) - w'(t)g''(t)}{\left[g'(t)\right]^2}$$

$\displaystyle y''(x) = \frac{w''(t)g'(t) - w'(t)g''(t)}{\left[g'(t)\right]^3}$ 


若设$\frac{w'(t)}{g'(t)}$为$\varphi(t)$，
则
$\displaystyle y''(x)=\frac{d^2 y}{dx^2}=\frac{d\left(\frac{dy}{dx}\right)}{dx}=\frac{d\left( \frac{w'(t)}{g'(t)}\right)}{dx}=\frac{\frac{d\left( \frac{w'(t)}{g'(t)} \right)}{dt}}{\frac{dx}{dt}}=\frac{\frac{d\left( \frac{w'(t)}{g'(t)} \right)}{dt}}{g'(t)}= \frac{\frac{d\varphi(t)}{dt}}{g'(t)} = \frac{\varphi'(t)}{g'(t)}$ 

其中$\displaystyle \varphi'(t)=\left( \frac{w'(t)}{g'(t)} \right)'=d\left( \frac{w'(t)}{g'(t)} \right) = \frac{w''(t)g'(t) - w'(t)g''(t)}{\left[g'(t)\right]^2}$ 

## 多项式求导
### 对数求导法


xxxx

**题目**

求函数 $y=x^{\ln x}$ 的导数。
?
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

**另一解法：** 
$$
\begin{align*}
y &= e^{\ln x \cdot \ln x} \\[4pt]
&= e^{(\ln x)^2} \\[8pt]
y' &= e^{(\ln x)^2} \cdot 2\ln x \cdot \frac{1}{x} \\[8pt]
&= x^{\ln x} \cdot \frac{2\ln x}{x}
\end{align*}
$$





**考点**：幂指函数对数求导法


```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-24T04:36:48.862Z,6,8.2956,1,2,1,0,0,2026-11-18T04:36:48.862Z,id=b9an13-->




zzzz



对于多项式相乘、相除、乘方的式子（为了求导的方便）：
一般先对等式两边同时取对数（前提是两边式子都$>0$），再求导。

设$y=f(x)$，$f(x)>0$，则：
等式两边取对数，即：
$$\ln y = \ln f(x)$$

对数可以实现以下运算转化：
$$\begin{cases}
乘 \to 加 \\
除 \to 减 \\
幂次 \to 倍数
\end{cases}$$

两边对自变量$x$求导：
注：求导时，将$y$看成关于$x$的函数$f(x)$，会涉及复合函数，即：
$$[\ln f(x)]' = \frac{1}{f(x)} \cdot f'(x)$$


## 幂指函数求导法
对于幂指函数$f(x)^{g(x)}$（满足$f(x)>0$，且$f(x)\neq1$），利用指数恒等式转换：
$$f(x)^{g(x)} = e^{g(x)\ln[f(x)]}$$

求导推导如下：
设$w(x) = g(x)\ln[f(x)]$，则
$$\begin{align*}
\left[f(x)^{g(x)}\right]' &= \left[e^{g(x)\ln[f(x)]}\right]' \\[4pt]
&= \left[e^{w(x)}\right]'\\[4pt]
&= e^{w(x)} \cdot w'(x)  \\[4pt]
&= f(x)^{g(x)} \cdot  \left[g(x)\ln[f(x)]\right]'  \\[4pt]
w'(x) =\left[g(x)\ln[f(x)]\right]'&= g'(x)\cdot \ln[f(x)] + g(x)\cdot \frac{1}{f(x)} \cdot f'(x)
\end{align*}$$


即
$$\left[f(x)^{g(x)}\right]' = f(x)^{g(x)}\left[g'(x)\ln f(x) + g(x)\cdot\frac{f'(x)}{f(x)}\right]$$

## 求高阶导（求导的阶数≥2，一般为n阶）



xxxx

**题目**

已知 $y=x\ln x$，则 $y'''=$（　　）

- A. $\dfrac{1}{x}$
- B. $\dfrac{1}{x^2}$
- C. $-\dfrac{1}{x}$
- D. $-\dfrac{1}{x^2}$
?
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
<!--SR:!fsrs,2026-11-28T04:38:14.562Z,10,8.2956,1,2,1,0,0,2026-11-18T04:38:14.562Z,id=s2f2ft-->


zzzz



xxxx

**题目**

$y=2e^x-x^2+x+1$，$y^{(520)}=$（　　）

- A. $520e^x$
- B. $2e^x$
- C. $2e^{520x}$
- D. $0$
?
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
<!--SR:!fsrs,2026-11-26T04:39:27.304Z,8,8.2956,1,2,1,0,0,2026-11-18T04:39:27.304Z,id=oz4l4x-->


zzzz



xxxx

**题目**

设函数 $f(x)=x^n+a_1x^{n-1}+a_2x^{n-2}+\cdots+a_n$，则 $f^{(n)}(x)=$（　　）

- A. $a_n$
- B. $n!$
- C. $0$
- D. $n!a_n$
?
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
<!--SR:!fsrs,2026-11-25T04:38:21.670Z,7,8.2956,1,2,1,0,0,2026-11-18T04:38:21.670Z,id=tlff1f-->


zzzz



xxxx

**题目**

已知函数 $f(x)=5^x$，则 $f^{(n)}(x)=$　$\underline{\qquad\quad}$。
?
````````col
```````col-md
flexGrow=20
===

**答案**：$5^x(\ln 5)^n$

**解析**

> 指数函数逐次求导每次都乘一个 $\ln 5$，故 $n$ 阶导数为 $5^x(\ln 5)^n$。

**考点**：高阶导数（指数函数归纳）
$$
\begin{align*}
\left(a^x\right)' &= \left(e^{x\ln a}\right)' \\[4pt]
&= e^{x\ln a} \cdot \ln a \\[4pt]
&= a^x \ln a
\end{align*}
$$



```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-26T06:55:16.404Z,9,8.2956,1,2,1,0,0,2026-11-17T06:55:16.404Z,id=i1s73c-->


zzzz





xxxx

**题目**

设 $y=e^{ax}+x^3$（$a>0$），则 $y'''(0)=$（　　）

- A. $6$
- B. $a^3+6$
- C. $a+6$
- D. $a^2+6$
?
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
<!--SR:!fsrs,2026-11-26T06:54:44.598Z,9,8.2956,1,2,1,0,0,2026-11-17T06:54:44.598Z,id=2xjdz0-->


zzzz





xxxx

**题目**

函数 $y=\cos 2x$，则 $y^{(2025)}=$（　　）

- A. $2^{2025}\sin 2x$
- B. $2^{2025}\cos 2x$
- C. $-2^{2025}\cos 2x$
- D. $-2^{2025}\sin 2x$
?
````````col
```````col-md
flexGrow=20
===

**答案**：D

**解析**

$$
\begin{align*}


&\mathrm dF=F_x\,\mathrm dx+F_y\,\mathrm dy+F_z\,\mathrm dz\\[6pt]



&\begin{aligned}
y&=\cos 2x\\
y'&=-2\sin 2x\\
y''&=-2^2\cos 2x\\
y'''&=2^3\sin 2x\\
y^{(4)}&=2^4\cos 2x
\end{aligned}\\[6pt]
&第四阶回到\cos 2x，所以每 4 阶循环一次，且每循环一次系数多乘 2^4。\\[6pt]

&定位 2025 落在哪一位\\[6pt]

&2025=4\times506+1\\[6pt]

&余 1，也就是 2025 阶和**一阶同款**（都是 \sin 2x、前面带负号），只是系数变成：\\[6pt]

&y^{(2025)}=2^{2025}\times(-1)\sin 2x=-2^{2025}\sin 2x\\[6pt]



\end{align*}
$$

> 选 A。

**考点**：高阶导数（三角函数周期归纳）


```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-24T07:27:22.536Z,9,8.2956,1,2,1,0,0,2026-11-15T07:27:22.536Z,id=g6kbve-->


zzzz




求高阶导数主要有三种方法：
1.  **归纳法**：逐次求导，探索规律，得出通式。

常用的高阶导数（$n\in \mathbb{N}_+$）：
$$(e^{ax+b})^{(n)} = a^n e^{ax+b}$$
$$\left[\sin(ax+b)\right]^{(n)} = a^n \sin\left(ax+b + \frac{n\pi}{2}\right)$$
$$\left[\cos(ax+b)\right]^{(n)} = a^n \cos\left(ax+b + \frac{n\pi}{2}\right)$$
$$\left[\ln(ax+b)\right]^{(n)} = (-1)^{n-1}a^n \frac{(n-1)!}{(ax+b)^n}$$
$$\left(\frac{1}{ax+b}\right)^{(n)} = (-1)^n a^n \frac{n!}{(ax+b)^{n+1}}$$

遇到不常见的，向常见的去转化。


### 莱布尼茨公式
设$u=u(x), v=v(x)$均$n$阶可导，则
$$(u\pm v)^{(n)} = u^{(n)} \pm v^{(n)}$$
$$
\begin{aligned}
(uv)^{(n)} &= \mathrm{C}_n^0 u^{(n)}v + \mathrm{C}_n^1 u^{(n-1)}v' + \mathrm{C}_n^2 u^{(n-2)}v'' + \dots \\
&\quad + \mathrm{C}_n^k u^{(n-k)}v^{(k)} + \dots + \mathrm{C}_n^{n-1} u'v^{(n-1)} + \mathrm{C}_n^n u v^{(n)} \\
&= \sum_{k=0}^n \mathrm{C}_n^k u^{(n-k)} v^{(k)}
\end{aligned}
$$
有时要莱布尼茨公式与归纳法中的通式结合着用。

### 补充：排列数与组合数
排列数：$\mathrm{A}_n^m = \underbrace{n(n-1)(n-2)\cdots(n-m+1)}_{m项相乘}$，例：$\mathrm{A}_6^3 = 6\times5\times4$
组合数：$\mathrm{C}_n^m = \frac{\mathrm{A}_n^m}{\mathrm{A}_m^m} = \frac{n(n-1)(n-2)\cdots(n-m+1)}{m!}$，例：$\mathrm{C}_6^3 = \frac{6\times5\times4}{3\times2\times1}$
规定$\mathrm{C}_n^0=1$：“不选择，也是一种选择”
性质：$\mathrm{C}_n^m = \mathrm{C}_n^{n-m}$
10个人送出6个人去比赛等价于10个人送出4个人不去比赛。

## 泰勒展开式
任何一个任意阶可导的函数都可以写成：
在$x=x_0$点展开：
$$y=f(x)=\sum_{n=0}^{\infty} \frac{f^{(n)}(x_0)}{n!}(x-x_0)^n$$
在$x=0$处展开：
$$y=f(x)=\sum_{n=0}^{\infty} \frac{f^{(n)}(0)}{n!}x^n$$
我们的先辈们已经帮我们求出了一些常见的任意阶可导函数在$x=0$处的泰勒展开式，这些公式最好记住：
$$e^x=\sum_{n=0}^{\infty} \frac{x^n}{n!}=1+x+\frac{x^2}{2!}+\dots+\frac{x^n}{n!}+\dots,\quad -\infty<x<+\infty$$
$$\frac{1}{1+x}=\sum_{n=0}^{\infty} (-1)^n x^n=1-x+x^2-x^3+\dots+(-1)^n x^n+\dots,\quad -1<x<1$$
$$\frac{1}{1-x}=\sum_{n=0}^{\infty} x^n=1+x+x^2+x^3+\dots+x^n+\dots,\quad -1<x<1$$
$$\ln(1+x)=\sum_{n=1}^{\infty} (-1)^{n-1}\frac{x^n}{n}=x-\frac{x^2}{2}+\frac{x^3}{3}-\dots+(-1)^{n-1}\frac{x^n}{n}+\dots,\quad -1<x\leq1$$
$$
\begin{align*}
\sin x&=\sum_{n=0}^{\infty} (-1)^n \frac{x^{2n+1}}{(2n+1)!},\quad -\infty<x<+\infty\\
&=x-\frac{x^3}{3!}+\frac{x^5}{5!}-\frac{x^7}{7!}+\dots+(-1)^n \frac{x^{2n+1}}{(2n+1)!}+\dots
\end{align*}
$$
$$
\begin{align*}
\cos x&=\sum_{n=0}^{\infty} (-1)^n \frac{x^{2n}}{(2n)!},\quad -\infty<x<+\infty\\
&=1-\frac{x^2}{2!}+\frac{x^4}{4!}-\frac{x^6}{6!}+\dots+(-1)^n \frac{x^{2n}}{(2n)!}+\dots
\end{align*}
$$
$$(1+x)^\alpha=1+\alpha x+\frac{\alpha(\alpha-1)}{2!}x^2+\dots$$
$\tan x = x+\frac{1}{3}x^3+\dots$，$\arctan x = x-\frac{1}{3}x^3+\dots$
$\arcsin x = x+\frac{1}{6}x^3+\dots$

### 函数泰勒展开式的唯一性
无论$f(x)$在哪个点处展开，其泰勒展开式具有唯一性。
我们可以比较$f(x)$在$x=x_0$处展开和在$x=0$处展开的系数，来获得$f^{(n)}(x_0)$或$f^{(n)}(0)$。
即：背会展开式，由于展开式中包含了$f^{(n)}(x_0)$，所以可由展开式得出$f^{(n)}(x_0)$。


eg：
将$\ln(1-x)$直接展开为幂级数：
$$f(x)=x^2\ln(1-x)=x^2\left(-x-\frac{x^2}{2}-\dots-\frac{x^{n-2}}{n-2}-\dots\right)$$
而$f(x)$的麦克劳林展开式形式为：
$$f(x)=f(0)+f'(0)x+\frac{f''(0)}{2!}x^2+\dots+\frac{f^{(n)}(0)}{n!}x^n+\dots$$
根据展开式的唯一性，对比等式两边$x^n$的系数，可得：
$$-\frac{1}{n-2} = \frac{f^{(n)}(0)}{n!} \implies f^{(n)}(0) = -\frac{n!}{n-2}$$


# 二元微分学的计算

## 二元复合函数求导


 - [*] **例13.9**
设 $z = f(e^x \sin y, x^2+y^2)$，其中$f$具有二阶连续偏导数，$f_1'(0,0)=1$，$f_2'(0,0)=-1$，求 $\dfrac{\partial^2 z}{\partial x \partial y}$。


分析
混合偏导$\frac{\partial^2 z}{\partial x \partial y}$的求解顺序：先对$x$求偏导，再对$y$求偏导，即
$$\frac{\partial^2 z}{\partial x \partial y} = \frac{\partial}{\partial y}\left( \frac{\partial z}{\partial x} \right)$$
以复合函数$z=f\left(e^x \sin y, x^2+y^2\right)$为例：
图1：复合函数$z$的变量依赖关系：$z$以$u=e^x \sin y$（第1个中间变量）、$v=x^2+y^2$（第2个中间变量）为中间变量，$u,v$均为自变量$x,y$的二元函数；对$x$求偏导时将$y$视为常数。
```tikz
\begin{document}
\begin{tikzpicture}[>=stealth,node distance=1.5cm, font=\small]
    \node (z) at (0,0) {$z$};
    \node[draw, rectangle] (u) at (-1.5,-1.5) {$e^x \sin y$};
    \node[draw, rectangle] (v) at (1.5,-1.5) {$x^2+y^2$};
    \node (x) at (-2,-3) {$x$};
    \node (y) at (2,-3) {$y$};
    \node at (-1.8,-0.8) {$1$};
    \node at (1.8,-0.8) {$2$};
    \draw[->] (z) -- (u);
    \draw[->] (z) -- (v);
    \draw[->] (u) -- (x);
    \draw[->] (u) -- (y);
    \draw[->] (v) -- (x);
    \draw[->] (v) -- (y);
\end{tikzpicture}
\end{document}
```
第一步：对$x$求一阶偏导（$y$视为常数），由链式法则得：
$$\frac{\partial z}{\partial x} = f_1' \cdot e^x \sin y + f_2' \cdot 2x$$
第二步：对$y$求偏导（此时$x$视为常数），先拆分求导项：
$$
\begin{align*}
\frac{\partial}{\partial y}\left( \frac{\partial z}{\partial x} \right) &= \frac{\partial}{\partial y}\left[ f_1' \cdot e^x \sin y + f_2' \cdot 2x \right] \\[4pt]
&= \frac{\partial \left(f_1' \cdot e^x \sin y\right)}{\partial y} + \frac{\partial \left(f_2' \cdot 2x\right)}{\partial y}
\end{align*}
$$





### 求偏导


xxxx

**题目**

已知二元函数 $z=(2y+1)^x$，则 $\dfrac{\partial z}{\partial y}=$（　　）

- A. $x(2y+1)^{x-1}$
- B. $2x(2y+1)^{x-1}$
- C. $(2y+1)^x\ln(2y+1)$
- D. $2(2y+1)^x\ln(2y+1)$
?
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
<!--SR:!fsrs,2026-11-24T04:38:36.341Z,6,8.2956,1,2,1,0,0,2026-11-18T04:38:36.341Z,id=t9i1ia-->


zzzz



xxxx

**题目**

设 $z=xy e^{x^2+y^2}$，则 $\dfrac{\partial z}{\partial x}\bigg|_{\substack{x=0\\y=1}}=$　$\underline{\qquad\quad}$。
?
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
<!--SR:!fsrs,2026-11-25T08:52:47.000Z,10,8.2956,1,2,1,0,0,2026-11-15T08:52:47.000Z,id=ipw94u-->


zzzz


xxxx

**题目**

$f(x,y)=x^2+\tan\dfrac{xy}{x^2+y^2}$，则 $\dfrac{\partial f(x,y)}{\partial x}\bigg|_{(1,0)}=$　$\underline{\qquad\quad}$。
?
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
<!--SR:!fsrs,2026-11-21T07:32:31.777Z,6,8.2956,1,2,1,0,0,2026-11-15T07:32:31.777Z,id=65tpxk-->


zzzz


求偏导是要求各自变量相互独立的，**为了求偏导，就算不独立也要假设独立**。因为求偏导是令其他增量为0，若不独立，则会牵扯到要偏导的那个方向的增量，会使这个方向的增量也为0，这样偏导也就无从谈起了

设 $z = f(u,v)$，$u = \varphi(x,y)$，$v = w(x,y)$，
则 $z = f\left[\varphi(x,y), w(x,y)\right]$，

**z对x的偏导数** 

`````col
````col-md
flexGrow=1
===


求偏导路径为$z \to u \to x$、$z \to v \to x$，
y为求偏导时固定的另一自变量

````

````col-md
flexGrow=1
===

```tikz
\begin{document}
\begin{tikzpicture}[>=stealth,scale=1.2,font=\small]
    \node at (0,0) {$z$};
    \node at (1,0.5) {$u$};
    \node at (1,-0.5) {$v$};
    \node at (2,0.5) {$x$};
    \node at (2,-0.8) {$y$};
    \draw[->] (0.2,0.1) -- (0.8,0.4);
    \draw[->] (0.2,-0.1) -- (0.8,-0.4);
    \draw[->] (1.2,0.5) -- (1.8,0.5);
    \draw[->] (1.2,-0.4) -- (1.8,0.4);
\end{tikzpicture}
\end{document}
```



````
`````

偏导计算公式：
$$
\frac{\partial z}{\partial x} = \frac{\partial z}{\partial u} \cdot \frac{\partial u}{\partial x} + \frac{\partial z}{\partial v} \cdot \frac{\partial v}{\partial x}
$$


**z对y的偏导数** 

`````col
````col-md
flexGrow=1
===

求导路径为$z \to u \to y$、$z \to v \to y$，
x为求偏导时固定的另一自变量

````

````col-md
flexGrow=1
===

```tikz
\begin{document}
\begin{tikzpicture}[>=stealth,scale=1.2,font=\small]
    \node at (0,0) {$z$};
    \node at (1,0.5) {$u$};
    \node at (1,-0.5) {$v$};
    \node at (2,-0.5) {$y$};
    \node at (2,0.8) {$x$};
    \draw[->] (0.2,0.1) -- (0.8,0.4);
    \draw[->] (0.2,-0.1) -- (0.8,-0.4);
    \draw[->] (1.2,0.4) -- (1.8,-0.4);
    \draw[->] (1.2,-0.5) -- (1.8,-0.5);
\end{tikzpicture}
\end{document}
```



````
`````

偏导计算公式：
$$
\frac{\partial z}{\partial y} = \frac{\partial z}{\partial u} \cdot \frac{\partial u}{\partial y} + \frac{\partial z}{\partial v} \cdot \frac{\partial v}{\partial y}
$$

### 求全导

- [*] 设 $f(u,v)=z$，$u=\varphi(t)$，$v=w(t)$，
则 $z = f\left[\varphi(t), w(t)\right]$，

`````col
````col-md
flexGrow=1
===


求导路径为$z \to u \to t$、$z \to v \to t$

````

````col-md
flexGrow=1
===

```tikz
\begin{document}
\begin{tikzpicture}[>=stealth,scale=1.2,font=\small]
    \node at (0,0) {$z$};
    \node at (1,0.5) {$u$};
    \node at (1,-0.5) {$v$};
    \node at (2,0) {$t$};
    \draw[->] (0.2,0.1) -- (0.8,0.4);
    \draw[->] (0.2,-0.1) -- (0.8,-0.4);
    \draw[->] (1.2,0.4) -- (1.8,0.1);
    \draw[->] (1.2,-0.4) -- (1.8,-0.1);
\end{tikzpicture}
\end{document}
```



````
`````

全导数计算公式：
$$
\frac{dz}{dt} = \frac{\partial z}{\partial u} \cdot \frac{du}{dt} + \frac{\partial z}{\partial v} \cdot \frac{dv}{dt}
$$


- [*] 设 $f(y,x)=z$，$y=g(x)$ 
则 $z = f\left[g(x)， x\right]$，

`````col
````col-md
flexGrow=1
===

$$
\begin{align*}
dz 
&= \frac{\partial z}{\partial x}dx + \frac{\partial z}{\partial y}dy \\[4pt]
&= \frac{\partial z}{\partial x}dx + \frac{\partial z}{\partial y} \frac{dy}{dx}dx \\[4pt]
\end{align*}
$$

````

````col-md
flexGrow=1
===


$$
\begin{align*}
&dy = \frac{dy}{dx}dx \\[4pt]
&dx = \frac{dx}{dx}dx \\[4pt]
\end{align*}
$$


````
`````

### 微分形式不变性 

设 $z = f(u,v)$，$u = u(x,y)$，$v = v(x,y)$。
如果 $f(u,v)$，$u(x,y)$，$v(x,y)$ 分别有连续偏导数，
则复合函数 $z = f(u,v)$ 在 $(x,y)$ 处的全微分可表示为
$$\mathrm{d}z = \frac{\partial z}{\partial u}\mathrm{d}u + \frac{\partial z}{\partial v}\mathrm{d}v$$
无论 $u,v$ 是自变量还是中间变量，上式都成立。

无论$z$对哪个变量求导，无论$z$已经求了几阶导，求导后的新函数，仍然具有与原函数完全相同的复合结构。


$$
\begin{align*}
&设 z = f(u,v)，u = \varphi(x,y)，v = w(x,y)，y=g(x) \\[4pt]
&则 z = f\left[\varphi(x,y), w(x,y)\right]=f\left[\varphi(x,g(x)), w(x,g(x))\right]  \\[4pt]
& \\[4pt]

&dz = \frac{\partial z}{\partial u} du + \frac{\partial z}{\partial v} dv \\[4pt]
&du = \frac{\partial u}{\partial x} dx + \frac{\partial u}{\partial y} dy \\[4pt]
&dv = \frac{\partial v}{\partial x} dx + \frac{\partial v}{\partial y} dy \\[4pt]
&dy = \frac{dy}{dx} dx \\[4pt]
&dx = \frac{dx}{dx}dx \\[4pt]

扩展&\\[4pt]

&若 F = f(u,v)，其中u = u(x,y,z)，v = v(x,y,z)，z = \varphi(x,y)，y = g(x) \\[4pt]
&则 \\[4pt]

&dF = \frac{\partial F}{\partial u} du + \frac{\partial F}{\partial v} dv \\[4pt]
&du = \frac{\partial u}{\partial x} dx + \frac{\partial u}{\partial y} dy + \frac{\partial u}{\partial z} dz \\[4pt]
&dv = \frac{\partial v}{\partial x} dx + \frac{\partial v}{\partial y} dy + \frac{\partial v}{\partial z} dz \\[4pt]
&dz = \frac{\partial z}{\partial x} dx + \frac{\partial z}{\partial y} dy \\[4pt]
&dy = \frac{dy}{dx} dx \\[4pt]
&dx = \frac{dx}{dx}dx \\[4pt]



\end{align*}
$$

该复合结构为多层链式依赖，直接通过链式法则求偏导需要梳理所有依赖路径，计算繁琐；利用一阶全微分形式不变性，可无需提前梳理路径，直接逐层写出微分：
后续只需代入$\mathrm{d}z$、$\mathrm{d}y$的微分表达式，整理即可得到最终结果。

### 对位置的标记规则



`````col
````col-md
flexGrow=1
===

若 $z = f(u,v)$，$u = \varphi(x,y)$，$v = w(x,y)$

```tikz
\begin{document}
\definecolor{curveblue}{rgb}{0.2,0.3,0.8}
\begin{tikzpicture}[>=stealth,scale=1.2,font=\small]
    % Nodes for variables
    \node (z) at (0,0) {$z$};
    \node[draw,rectangle,minimum size=0.5cm] (u) at (1.5,0.8) {$u$};
    \node[draw,rectangle,minimum size=0.5cm] (v) at (1.5,-0.8) {$v$};
    \node (x) at (3,1.2) {$x$};
    \node (y) at (3,-1.2) {$y$};
    % Index labels for intermediate variables
    \node at (1.0,1.1) {$1$};
    \node at (1.0,-1.1) {$2$};
    % Arrows for dependency
    \draw[->,curveblue] (z) -- (u);
    \draw[->,curveblue] (z) -- (v);
    \draw[->,curveblue] (u) -- (x);
    \draw[->,curveblue] (u) -- (y);
    \draw[->,curveblue] (v) -- (x);
    \draw[->,curveblue] (v) -- (y);
\end{tikzpicture}
\end{document}
```
我们一般称：
- $u$为1类（第1个中间变量）
- $v$为2类（第2个中间变量）

偏导数记号约定：
$$
\begin{align*}
z_u' &= f_u'(u,v) = f_1'(u,v) = f_1' = z_1' \\
z_v' &= f_v'(u,v) = f_2'(u,v) = f_2' = z_2'
\end{align*}
$$

一阶偏导链式法则：
$$
\begin{align*}
z_x' &= z_u' \cdot u_x' + z_v' \cdot v_x' \\
&= f_1' \cdot u_x' + f_2' \cdot v_x' \\[6pt]
z_y' &= z_u' \cdot u_y' + z_v' \cdot v_y' \\
&= f_1' \cdot u_y' + f_2' \cdot v_y'
\end{align*}
$$

二阶偏导记号：
$$
z_{uu}'' = f_{11}'',\quad z_{uv}'' = f_{12}''
$$

````

````col-md
flexGrow=1
===

**注** 

若 $z = f(u,v)$，$u = \varphi(x,y)$，$v = w(x,y)$
复合函数变量依赖关系图，
```tikz
\begin{document}
\definecolor{curveblue}{rgb}{0.2,0.3,0.8}
\begin{tikzpicture}[>=stealth,scale=1.2,font=\small]
    % Nodes for variables
    \node (z) at (0,0) {$z$};
    \node[draw,rectangle,minimum size=0.5cm] (u) at (1.5,0.8) {$u$};
    \node[draw,rectangle,minimum size=0.5cm] (v) at (1.5,-0.8) {$v$};
    \node (x) at (3,1.2) {$x$};
    \node (y) at (3,-1.2) {$y$};
    % Index labels for intermediate variables
    \node at (1.0,1.1) {$x$};
    \node at (1.0,-1.1) {$y$};
    % Arrows for dependency
    \draw[->,curveblue] (z) -- (u);
    \draw[->,curveblue] (z) -- (v);
    \draw[->,curveblue] (u) -- (x);
    \draw[->,curveblue] (u) -- (y);
    \draw[->,curveblue] (v) -- (x);
    \draw[->,curveblue] (v) -- (y);
\end{tikzpicture}
\end{document}
```

偏导数记号约定：
$$
\begin{align*}
z_u' &= f_u'(u,v) = f_x'(u,v) = f_x' = z_x' \\
z_v' &= f_v'(u,v) = f_y'(u,v) = f_y' = z_y'
\end{align*}
$$

$f_x'$为$f$对标$x$的中间变量位置求偏导，并非对自变量$x$求偏导。




````
`````

### 二阶偏导



xxxx

**题目**

$z=x\ln(x+y)$，求 $\dfrac{\partial^2 z}{\partial x\partial y}=$（　　）

- A. $\dfrac{x}{(x+y)^2}$
- B. $\dfrac{y}{(x+y)^2}$
- C. $\dfrac{2x+y}{(x+y)^2}$
- D. $\dfrac{x+2y}{(x+y)^2}$
?
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
<!--SR:!fsrs,2026-11-25T04:39:02.138Z,7,8.2956,1,2,1,0,0,2026-11-18T04:39:02.138Z,id=zeat47-->


zzzz


xxxx

**题目**

设 $z=x^2-2xy-y^2$，则 $\dfrac{\partial^2 z}{\partial x\partial y}\bigg|_{(1,2)}=$（　　）

- A. $1$
- B. $2$
- C. $-2$
- D. $-1$
?
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
<!--SR:!fsrs,2026-11-28T04:38:58.802Z,10,8.2956,1,2,1,0,0,2026-11-18T04:38:58.802Z,id=bdp1k0-->


zzzz


xxxx

**题目**

已知 $u=5+e^{3x-yz}$，则 $\dfrac{\partial^2 u}{\partial x\partial y}=$　$\underline{\qquad\quad}$。
?
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
<!--SR:!fsrs,2026-11-24T06:54:39.298Z,7,8.2956,1,2,1,0,0,2026-11-17T06:54:39.298Z,id=qvalbg-->


zzzz



xxxx

**题目**

设 $z=e^{x+y}-\ln(x+y)$，则 $\dfrac{\partial^2 z}{\partial x\partial y}\bigg|_{(1,0)}=$　$\underline{\qquad\quad}$。
?
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
<!--SR:!fsrs,2026-11-21T05:35:51.557Z,6,8.2956,1,2,1,0,0,2026-11-15T05:35:51.557Z,id=2ai8tn-->


zzzz





*二元导函数与其原函数的复合结构相同* 

**eg：** 
若

```tikz
\begin{document}
\definecolor{curveblue}{rgb}{0.2,0.3,0.8}
\begin{tikzpicture}[>=stealth,scale=1.2,font=\small]
    \node (z) at (0,0) {$z$};
    \node (u) at (1.5,0.8) {$u$};
    \node (v) at (1.5,-0.8) {$v$};
    \node (x) at (3,1.2) {$x$};
    \node (y) at (3,-1.2) {$y$};
    \draw[->,curveblue] (z) -- (u);
    \draw[->,curveblue] (z) -- (v);
    \draw[->,curveblue] (u) -- (x);
    \draw[->,curveblue] (u) -- (y);
    \draw[->,curveblue] (v) -- (x);
    \draw[->,curveblue] (v) -- (y);
\end{tikzpicture}
\end{document}
```
则 $z_u' = f_1'，z_v' = f_2'$ 

一阶偏导$f_1'$（即$z_u'$）与原函数$z$具有完全相同的复合结构；
同理$f_2'$（即$z_v'$）也与$z$具有相同的复合结构，仍以$u,v$为中间变量、$x,y$为自变量。

`````col
````col-md
flexGrow=1
===

```tikz
\begin{document}
\begin{tikzpicture}[>=stealth,node distance=1.5cm, font=\small]
    \node (f1) at (0,0) {$f_1'$};
    \node (u) at (-1.2,-1.2) {$u$};
    \node (v) at (1.2,-1.2) {$v$};
    \node (x) at (-1.8,-2.4) {$x$};
    \node (y) at (1.8,-2.4) {$y$};
    \draw[->] (f1) -- (u);
    \draw[->] (f1) -- (v);
    \draw[->] (u) -- (x);
    \draw[->] (u) -- (y);
    \draw[->] (v) -- (x);
    \draw[->] (v) -- (y);
\end{tikzpicture}
\end{document}
```

````

````col-md
flexGrow=1
===

```tikz
\begin{document}
\begin{tikzpicture}[>=stealth,node distance=1.5cm, font=\small]
    \node (f2) at (0,0) {$f_2'$};
    \node (u) at (-1.2,-1.2) {$u$};
    \node (v) at (1.2,-1.2) {$v$};
    \node (x) at (-1.8,-2.4) {$x$};
    \node (y) at (1.8,-2.4) {$y$};
    \node at (-1.5,-0.6) {$1$};
    \node at (1.5,-0.6) {$2$};
    \draw[->] (f2) -- (u);
    \draw[->] (f2) -- (v);
    \draw[->] (u) -- (x);
    \draw[->] (u) -- (y);
    \draw[->] (v) -- (x);
    \draw[->] (v) -- (y);
\end{tikzpicture}
\end{document}
```



````
`````




二阶偏导记号约定：$z_{vu}'' = f_{21}'' = (z_v')_u'$，表示先对第2个中间变量$v$求偏导，再对第1个中间变量$u$求偏导。
根据链式法则，$f_2'$对$y$的偏导为：
$$\frac{\partial (f_2')}{\partial y} = f_{21}'' \cdot \frac{\partial u}{\partial y} + f_{22}'' \cdot \frac{\partial v}{\partial y}$$
$z,\ f_1',\ f_2',\ f_3',\ z_x',\ z_x''$ 等等，都为相同的复合结构。

___


若函数$f(x,y)$的偏导数$f_x'(x,y)$和$f_y'(x,y)$仍存在偏导数，则
$f_x'(x,y)$和$f_y'(x,y)$的偏导数为函数$f(x,y)$的二阶偏导数。

第一次求导时，可以为$x$轴、$y$轴两个方向
第二次求导时，也可以为$x$、$y$轴两个方向
所以，二阶偏导数实际上有4个：

$$\frac{\partial^2 z}{\partial x^2} = \frac{\partial}{\partial x}\left( \frac{\partial z}{\partial x} \right) = f_{xx}''(x,y) = z_{xx}''$$
$$\frac{\partial^2 z}{\partial x\partial y} = \frac{\partial}{\partial y}\left( \frac{\partial z}{\partial x} \right) = f_{xy}''(x,y) = z_{xy}''$$
$$\frac{\partial^2 z}{\partial y^2} = \frac{\partial}{\partial y}\left( \frac{\partial z}{\partial y} \right) = f_{yy}''(x,y) = z_{yy}''$$
$$\frac{\partial^2 z}{\partial y\partial x} = \frac{\partial}{\partial x}\left( \frac{\partial z}{\partial y} \right) = f_{yx}''(x,y) = z_{yx}''$$

其中，称$f_{xy}''(x,y)$与$f_{yx}''(x,y)$为二阶混合偏导数。

**注**：若$\displaystyle \frac{\partial\left( \frac{\partial f}{\partial x} \right)}{\partial y}$与$\displaystyle \frac{\partial\left( \frac{\partial f}{\partial y} \right)}{\partial x}$在区域$D$内连续，则两者相等，与求导次序无关。
在大部分情况下，我们只用求两者之一即可。


## 二元隐函数求导(推论)



### 公式法


xxxx

**题目**

已知函数 $z=f(x,y)$ 由方程 $xz-yz-x+y=0$ 所确定，求全微分 $\mathrm{d}z$。
?
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
<!--SR:!fsrs,2026-11-28T04:38:05.240Z,10,8.2956,1,2,1,0,0,2026-11-18T04:38:05.240Z,id=pjgbqf-->


zzzz



xxxx

**题目**

设函数 $y=y(x)$ 由方程 $\ln(x^2+y)=x^3y+\sin x$ 确定，求 $\dfrac{dy}{dx}\bigg|_{x=0}$。
?
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

**另一解法：** 

$$F(x,y) = -\ln(x^2+y) + x^3 y + \sin x$$

$$\frac{dy}{dx} = -\frac{F_x'}{F_y'}$$

$$
\begin{align*}
F_x' &= -\frac{2x}{x^2+y} + 3x^2 y + \cos x \\[6pt]
F_y' &= -\frac{1}{x^2+y} + x^3
\end{align*}
$$

$$\ln y = 0 \implies  y=1$$

$$F_x'\big|_{(0,1)} = 1,\quad F_y'\big|_{(0,1)} = -1$$

$$\frac{dy}{dx}\bigg|_{x=0} = 1$$








**考点**：隐函数求导（一点处）


```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-26T04:39:13.446Z,8,8.2956,1,2,1,0,0,2026-11-18T04:39:13.446Z,id=36o0q8-->


zzzz



xxxx

**题目**

$xy+xyz=2x-4y$，$xy\neq 0$，求 $\dfrac{\partial z}{\partial x}$，$\dfrac{\partial z}{\partial y}$。
?
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


**另一解法：** 

$$xy + xyz - 2x + 4y = 0$$

$$
\frac{\partial z}{\partial x} = -\frac{F_x}{F_z}, \quad \frac{\partial z}{\partial y} = -\frac{F_y}{F_z}
$$

$$
\begin{align*}
F_x' &= y + yz - 2 \\
F_y' &= x + xz + 4 \\
F_z' &= xy
\end{align*}
$$

$$
\frac{\partial z}{\partial x} = -\frac{y + yz - 2}{xy}, \quad \frac{\partial z}{\partial y} = -\frac{x + xz + 4}{xy}
$$






**考点**：隐函数（先解出 $z$）求偏导


```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-25T04:38:40.438Z,7,8.2956,1,2,1,0,0,2026-11-18T04:38:40.438Z,id=q5btf6-->


zzzz


xxxx

**题目**

设函数 $z=z(x,y)$ 由方程 $x^2+y^3+3xyz^2+2z=1$ 所确定，求 $\dfrac{\partial z}{\partial x}$，$\dfrac{\partial z}{\partial y}$。（其中 $6xyz+2\neq 0$）
?
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
<!--SR:!fsrs,2026-11-26T04:39:10.748Z,8,8.2956,1,2,1,0,0,2026-11-18T04:39:10.748Z,id=vtzwwb-->


zzzz




xxxx



**题目**

若 $F(x,y,z)=\sin(x+3y-2z)=x+3y-2z$ 确定隐函数 $z=z(x,y)$，求 $\dfrac{\partial z}{\partial x}+\dfrac{\partial z}{\partial y}$。
?
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

**公式法是变三项**
1，降一级或升一级
2，取倒数
3，取相反数
<!--SR:!fsrs,2026-11-25T06:55:04.451Z,8,8.2956,1,2,1,0,0,2026-11-17T06:55:04.451Z,id=ohl7ti-->


zzzz




### 偏导


xxxx

**题目**

设二元函数 $z=\dfrac{x^2}{3y}+\arcsin(xy)$，求 $xy\dfrac{\partial z}{\partial x}-y^2\dfrac{\partial z}{\partial y}$。
?
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
<!--SR:!fsrs,2026-11-28T04:36:56.100Z,10,8.2956,1,2,1,0,0,2026-11-18T04:36:56.100Z,id=okzjwh-->


zzzz


xxxx

**题目**

已知函数 $x=x(y,z)$ 由 $2xz-2xy+\ln y=0$ 确定，则 $\dfrac{\partial x}{\partial z}=$（　　）

- A. $\dfrac{x}{z-y}$
- B. $\dfrac{y}{x-z}$
- C. $\dfrac{y}{z-x}$
- D. $\dfrac{x}{y-z}$
?
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
<!--SR:!fsrs,2026-11-24T07:27:26.614Z,9,8.2956,1,2,1,0,0,2026-11-15T07:27:26.614Z,id=c0y2vb-->


zzzz



### 全导



xxxx

**题目**

设函数 $z=2\sin x^2+e^{2y}-3xy^2$，则 $\mathrm{d}z=$　$\underline{\qquad\quad}$。
?
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
<!--SR:!fsrs,2026-11-23T06:55:23.734Z,6,8.2956,1,2,1,0,0,2026-11-17T06:55:23.734Z,id=13b0a4-->


zzzz


xxxx

**题目**

已知函数 $z=f(x,y)$ 由方程 $x^2+e^{-y}+z=xyz$ 所确定，求 $\mathrm{d}z$。
?
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

**另一解法**

求偏导是要求各自变量相互独立的，**为了求偏导，就算不独立也要假设独立**。因为求偏导是令其他增量为0，若不独立，则会牵扯到要偏导的那个方向的增量，会使这个方向的增量也为0，这样偏导也就无从谈起了


$$
\begin{align*}
&\displaystyle F = x^2 + e^{-y} + z - xyz = 0\\[6pt]
&\displaystyle \mathrm{d}F = F_x\,\mathrm{d}x + F_y\,\mathrm{d}y + F_z\,\mathrm{d}z\\[6pt]
&\displaystyle F_x = 2x - yz,\quad F_y = -e^{-y} - xz,\quad F_z = 1 - xy\\[6pt]
&\displaystyle \mathrm{d}F = (2x-yz)\,\mathrm{d}x + (-e^{-y}-xz)\,\mathrm{d}y + (1-xy)\,\mathrm{d}z = 0\\[6pt]
&\displaystyle (1-xy)\,\mathrm{d}z = (yz-2x)\,\mathrm{d}x + (xz+e^{-y})\,\mathrm{d}y\\[6pt]
&\displaystyle \mathrm{d}z = \frac{yz-2x}{1-xy}\,\mathrm{d}x + \frac{xz+e^{-y}}{1-xy}\,\mathrm{d}y\\[6pt]
\end{align*}
$$

**考点**：隐函数全微分（全微分形式不变性）


```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-25T08:52:59.966Z,10,8.2956,1,2,1,0,0,2026-11-15T08:52:59.966Z,id=ibs7y9-->


zzzz



xxxx

**题目**

已知函数 $z=z(x,y)$ 由方程 $\sin x-xy^2+e^z-z=0$ 确定，求 $\mathrm{d}z$。
?
````````col
```````col-md
flexGrow=20
===

**答案**：$\mathrm{d}z=\dfrac{y^2-\cos x}{e^z-1}\mathrm{d}x+\dfrac{2xy}{e^z-1}\mathrm{d}y$

**解析**


> 令 $F(x,y,z)=\sin x-xy^2+e^z-z$，则
>$\mathrm dF=F_x\,\mathrm dx+F_y\,\mathrm dy+F_z\,\mathrm dz$
> $$F_x=\cos x-y^2,\qquad F_y=-2xy,\qquad F_z=e^z-1$$
>
> 由隐函数求导公式：
>
> $$\frac{\partial z}{\partial x}=-\frac{F_x}{F_z}=\frac{y^2-\cos x}{e^z-1},\qquad \frac{\partial z}{\partial y}=-\frac{F_y}{F_z}=\frac{2xy}{e^z-1}$$
>
> 故 $\mathrm{d}z=\dfrac{y^2-\cos x}{e^z-1}\mathrm{d}x+\dfrac{2xy}{e^z-1}\mathrm{d}y$。
> 【订正】源题答解析在已正确写出 $F_z=e^z-1$ 的情况下，后续公式误把分母写成 $e^z+1$，且 $\dfrac{\partial z}{\partial x}$ 的分子符号也写反（写成 $\dfrac{\cos x-y^2}{e^z+1}$）。按公式 $-F_x/F_z$ 复算，正确结果应为 $\dfrac{y^2-\cos x}{e^z-1}$，分母是 $e^z-1$，本专题已订正。

**另一解法**

$$
\begin{align*}


&\mathrm dF=F_x\,\mathrm dx+F_y\,\mathrm dy+F_z\,\mathrm dz\\[6pt]

&第一步：算三个偏导\\[6pt]

&F=\sin x-xy^2+e^z-z\\[6pt]

&F_x=\cos x-y^2,\qquad F_y=-2xy,\qquad F_z=e^z-1\\[6pt]

&第二步：代入全微分\\[6pt]

&\mathrm dF=(\cos x-y^2)\mathrm dx-2xy\,\mathrm dy+(e^z-1)\mathrm dz\\[6pt]

&因为方程是 F=0，所以 \mathrm dF=0：\\[6pt]

&(\cos x-y^2)\mathrm dx-2xy\,\mathrm dy+(e^z-1)\mathrm dz=0\\[6pt]

&第三步：解出 dz\\[6pt]

&(e^z-1)\mathrm dz=(y^2-\cos x)\mathrm dx+2xy\,\mathrm dy\\[6pt]

&\boxed{\mathrm dz=\frac{y^2-\cos x}{e^z-1}\,\mathrm dx+\frac{2xy}{e^z-1}\,\mathrm dy}\\[6pt]



\end{align*}
$$







**考点**：隐函数求偏导公式 + 全微分


```````

```````col-md
flexGrow=1
===





```````
````````
<!--SR:!fsrs,2026-11-21T06:53:12.383Z,6,8.2956,1,2,1,0,0,2026-11-15T06:53:12.383Z,id=i7b39u-->

zzzz




**(隐函数存在定理)** 
### 定理1


**公式法是变三项** 
1，降一级或升一级
2，取倒数
3，取相反数

若对于由方程$F(x,y)=0$在点$(x_0,y_0)$处所确定的隐函数$y=f(x)$，

则当$F_y'(x,y)\neq0$时，有$\displaystyle  \frac{dy}{dx} = -\frac{F_x'(x,y)}{F_y'(x,y)}$ 


**推导**（链式法则）

$$
\begin{align*}
&F= F(x,f(x))=0 两边对 x 求导：\\[4pt]
&\left. \frac{dF}{dx} \right|_{y=f(x)}=0 \\[4pt]
&\frac{\frac{\partial F}{\partial x}\mathrm{d}x + \frac{\partial F}{\partial y}\mathrm{d}y}{dx}=0 \\[4pt]
& \displaystyle F_x' + F_y'\cdot\frac{dy}{dx} = 0   \\[4pt]
\Longrightarrow\;& \frac{dy}{dx}=-\frac{F_x'}{F_y'}\\[4pt]
\because \;& 若F_y'=0，则两边就不能除F_y'了，此推导也就无法进行\\[4pt]
\therefore  \;& 当F_y'=0时，此公式失效 \\[4pt]
\end{align*}
$$



**注意**：

当，$\displaystyle F_y'=0$(此公式失效)时

我们要把隐函数$\displaystyle F= F(x,f(x))=0$显化为$\displaystyle y=f(x)$ 
进而判断函数$\displaystyle y=f(x)$ 是否存在

`````col
````col-md
flexGrow=1
===

$$
\begin{align*}
&合法的函数：\\[4pt]
&\displaystyle 一个y对应一个或多个x\\[4pt]
&eg1:y=x\\[4pt]
&eg2: y=0
\begin{cases}
x=任意值时 \\[4pt]
y只取0 \\[4pt]
\end{cases}\\[4pt]
\end{align*}
$$


````

````col-md
flexGrow=1.5
===


$$
\begin{align*}
&不存在的函数：\\[4pt]
&一个x对应多个y\\[4pt]

&eg1:y=\pm x
\begin{cases}
x=1时 \\[4pt]
有y=+1和y=-1 \\[4pt]
\end{cases}\\[4pt]

&eg2: x=0
\begin{cases}
x=0时 \\[4pt]
y可以是任意值，有无穷个y \\[4pt]
\end{cases}\\[4pt]

\end{align*}
$$



````
`````



### 定理2

若对于由方程$F(x,y,z)=0$，在点$(x_0,y_0,z_0)$处确定的隐函数$z=z(x,y)$，

则当$F_z'\neq0$时，有$\displaystyle  \frac{\partial z}{\partial x}=-\frac{F_x'}{F_z'},\quad \frac{\partial z}{\partial y}=-\frac{F_y'}{F_z'}$ 


**推导**（链式法则）
$$
\begin{align*}

&\begin{array}{@{}c@{\qquad}c@{}}

\begin{aligned}
&F=F(x,y,z(x,y))=0 \\[4pt]
&两边对 x 求偏导(y 看作常数):\\[4pt]
&\left. \frac{\partial F}{\partial x} \right|_{y=常数,\, z=z(x,y)}=0 \\[4pt]
&\frac{\frac{\partial F}{\partial x}dx + \frac{\partial F}{\partial y}dy + \frac{\partial F}{\partial z}dz}{dx}=0 \\[4pt]
&y 看作常数 \Rightarrow dy=0: \\[4pt]
& \displaystyle F_x' + F_z'\cdot\frac{\partial z}{\partial x} = 0   \\[4pt]
&\Longrightarrow\; \frac{\partial z}{\partial x}=-\frac{F_x'}{F_z'}\\[8pt]
\end{aligned}
&
\begin{aligned}
&F=F(x,y,z(x,y))=0 \\[4pt]
&两边对 y 求偏导(x 看作常数):\\[4pt]
&\left. \frac{\partial F}{\partial y} \right|_{x=常数,\, z=z(x,y)}=0 \\[4pt]
&\frac{\frac{\partial F}{\partial x}dx + \frac{\partial F}{\partial y}dy + \frac{\partial F}{\partial z}dz}{dy}=0 \\[4pt]
&x 看作常数 \Rightarrow dx=0: \\[4pt]
& \displaystyle F_y' + F_z'\cdot\frac{\partial z}{\partial y} = 0   \\[4pt]
&\Longrightarrow\; \frac{\partial z}{\partial y}=-\frac{F_y'}{F_z'}\\[8pt]
\end{aligned}

\end{array}\\[4pt]

\because \;& 若F_z'=0，则两边就不能除F_z'了，此推导也就无法进行\\[4pt]
\therefore  \;& 当F_z'=0时，此公式失效 \\[4pt]

\end{align*}
$$

**注意**：

当，$\displaystyle F_z'=0$（此公式失效）时

我们要把隐函数 $\displaystyle F(x,y,z)=0$ 显化为 $\displaystyle z=z(x,y)$
进而判断函数 $\displaystyle z=z(x,y)$ 是否存在





