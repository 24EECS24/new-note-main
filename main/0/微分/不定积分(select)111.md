# 不定积分的计算真题归纳（2016—2026）

> 本文件收录 2016—2026 年河南专升本《高等数学》真题中**所有涉及不定积分计算知识点**的题目，共 **36 题**。题面均逐题对照官方试卷 PDF 核对，与原卷一致；解析逐题独立推导验证。按年份从 2026 倒序至 2016，**一个试卷一个一级标题，一题一个二级标题**，题号沿用真题题号。
>
> 收录范围：以 $\int f(x)\,dx$ 形式出现、无积分上下限、结果含任意常数 $C$，需用凑微分（第一类换元）、换元（第二类换元）、分部积分、有理函数部分分式等方法求原函数的题目。定积分（有上下限）、纯概念题（原函数与不定积分定义、积分与微分互逆）、微分方程等不收录。

# 2026年

## 第11题

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


zzzz

## 第12题

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

**考点**

由导数关系先求函数再计算不定积分
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


zzzz

## 第44题

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

**考点**

三角代换（第二类换元法）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz

# 2025年

## 第12题

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

**考点**

凑微分法（常数并入任意常数）
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

**考点**

分部积分法（结合凑微分）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz

## 第45题

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

**考点**

根式代换（第二类换元法）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz

# 2024年

## 第12题

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

**考点**

三角恒等变换求原函数
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz

## 第13题

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

**考点**

凑微分法（第一类换元法）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz

## 第32题

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

**考点**

凑微分法（结合恒等变形）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz

## 第45题

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

**考点**

分部积分法
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz

# 2023年

## 第13题

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

## 第31题

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

## 第45题

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

**考点**

分部积分法与凑微分法
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz

# 2022年

## 第13题

xxxx

**题目**

不定积分 $\displaystyle\int f'(7x)\,dx=$（　）

A. $f(x)+C$

B. $\dfrac{1}{7}f(7x)+C$

C. $7f(x)+C$

D. $7f(7x)+C$
?

````````col
```````col-md
flexGrow=20
===

**答案**：B

**解析**

> 用凑微分法，把 $dx$ 改写为 $\dfrac17 d(7x)$：
> $$\int f'(7x)\,dx=\frac17\int f'(7x)\,d(7x)=\frac17 f(7x)+C$$
> 故选 B。

**考点**

凑微分法（第一类换元法）
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

已知 $f(x)$ 的一个原函数是 $\ln x$，则 $\displaystyle\int xf'(x)\,dx=$
?

````````col
```````col-md
flexGrow=20
===

**答案**：$1-\ln x+C$

**解析**

> 由 $\ln x$ 是 $f(x)$ 的一个原函数，得
> $$f(x)=(\ln x)'=\frac1x$$
> 用分部积分法，令 $u=x$，$dv=f'(x)\,dx$，则 $v=f(x)$：
> $$\int xf'(x)\,dx=xf(x)-\int f(x)\,dx=x\cdot\frac1x-\ln x+C=1-\ln x+C$$

**考点**

分部积分法（结合原函数概念）
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

$\displaystyle\int\frac{3}{x^{2}-5x+6}\,dx=$ 
?

````````col
```````col-md
flexGrow=20
===

**答案**：$3\ln\left|\dfrac{x-3}{x-2}\right|+C$

**解析**

> 分母因式分解：$x^{2}-5x+6=(x-2)(x-3)$。作部分分式分解：
> $$\frac{3}{(x-2)(x-3)}=\frac{A}{x-2}+\frac{B}{x-3}$$
> 通分后比较分子 $A(x-3)+B(x-2)=3$。令 $x=2$ 得 $-A=3$，即 $A=-3$；令 $x=3$ 得 $B=3$。故
> $$\frac{3}{(x-2)(x-3)}=\frac{3}{x-3}-\frac{3}{x-2}$$
> 积分得
> $$3\ln|x-3|-3\ln|x-2|+C=3\ln\left|\frac{x-3}{x-2}\right|+C$$

**考点**

有理函数的部分分式积分
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

计算不定积分 $\displaystyle\int\left(\frac{3}{1+x^{2}}-\frac{2+\ln x}{x\ln x}\right)dx$。
?

````````col
```````col-md
flexGrow=20
===

**答案**：$3\arctan x-2\ln|\ln x|-\ln x+C$

**解析**

> 分项处理。第一项：
> $$\int\frac{3}{1+x^{2}}\,dx=3\arctan x$$
> 第二项拆分被积函数：
> $$\frac{2+\ln x}{x\ln x}=\frac{2}{x\ln x}+\frac{1}{x}$$
> 其中令 $u=\ln x$，$du=\dfrac1x dx$，有
> $$\int\frac{2}{x\ln x}\,dx=2\int\frac{du}{u}=2\ln|u|=2\ln|\ln x|$$
> $$\int\frac{1}{x}\,dx=\ln x$$
> 故
> $$\text{原式}=3\arctan x-2\ln|\ln x|-\ln x+C$$

**考点**

分项积分与凑微分法
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz

# 2021年

## 第12题

xxxx

**题目**

若 $F(x)$ 是 $f(x)$ 的一个原函数，则 $\displaystyle\int\frac{1}{x}f(\ln x)\,dx=$（　）

A. $F(\ln x)$

B. $F(\ln x)+C$

C. $xF(\ln x)+C$

D. $\dfrac{1}{x}F(\ln x)+C$
?

````````col
```````col-md
flexGrow=20
===

**答案**：B

**解析**

> 令 $u=\ln x$，则 $du=\dfrac1x dx$，于是
> $$\int\frac1x f(\ln x)\,dx=\int f(u)\,du=F(u)+C=F(\ln x)+C$$
> 故选 B。

**考点**

凑微分法（第一类换元法）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz

## 第32题

xxxx

**题目**

不定积分 $\displaystyle\int x\sin x\,dx=$
?

````````col
```````col-md
flexGrow=20
===

**答案**：$\sin x-x\cos x+C$

**解析**

> 用分部积分法，令 $u=x$，$dv=\sin x\,dx$，则 $du=dx$，$v=-\cos x$：
> $$\int x\sin x\,dx=-x\cos x+\int\cos x\,dx=-x\cos x+\sin x+C$$

**考点**

分部积分法
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz

## 第45题

xxxx

**题目**

计算不定积分 $\displaystyle\int\frac{1}{\sqrt[3]{x+1}+1}\,dx$。
?

````````col
```````col-md
flexGrow=20
===

**答案**：$\dfrac{3}{2}\sqrt[3]{(x+1)^{2}}-3\sqrt[3]{x+1}+3\ln\left|\sqrt[3]{x+1}+1\right|+C$

**解析**

> 令 $t=\sqrt[3]{x+1}$，则 $x=t^{3}-1$，$dx=3t^{2}dt$。于是
> $$\text{原式}=\int\frac{3t^{2}}{t+1}\,dt$$
> 由 $t^{2}=(t+1)(t-1)+1$，得
> $$\frac{t^{2}}{t+1}=t-1+\frac{1}{t+1}$$
> 故
> $$3\int\frac{t^{2}}{t+1}\,dt=3\int\left(t-1+\frac{1}{t+1}\right)dt=\frac32 t^{2}-3t+3\ln|t+1|+C$$
> 回代 $t=\sqrt[3]{x+1}$：
> $$\frac32\sqrt[3]{(x+1)^{2}}-3\sqrt[3]{x+1}+3\ln\left|\sqrt[3]{x+1}+1\right|+C$$

**考点**

根式代换（第二类换元法）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz

# 2020年

## 第18题

xxxx

**题目**

$\displaystyle\int\sin(1-2x)\,dx=$（　）

A. $\cos(1-2x)+C$

B. $-\cos(1-2x)+C$

C. $\dfrac{1}{2}\cos(1-2x)+C$

D. $-\dfrac{1}{2}\cos(1-2x)+C$
?

````````col
```````col-md
flexGrow=20
===

**答案**：C

**解析**

> 令 $u=1-2x$，则 $du=-2\,dx$，即 $dx=-\dfrac12 du$：
> $$\int\sin(1-2x)\,dx=-\frac12\int\sin u\,du=\frac12\cos u+C=\frac12\cos(1-2x)+C$$
> 故选 C。

**考点**

凑微分法（第一类换元法）
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

若 $\displaystyle\int f(x)\,dx=F(x)+C$，则 $\displaystyle\int f(\sin x)\cos x\,dx=$
?

````````col
```````col-md
flexGrow=20
===

**答案**：$F(\sin x)+C$

**解析**

> 令 $u=\sin x$，则 $du=\cos x\,dx$：
> $$\int f(\sin x)\cos x\,dx=\int f(u)\,du=F(u)+C=F(\sin x)+C$$

**考点**

凑微分法（第一类换元法）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz

## 第45题

xxxx

**题目**

计算不定积分 $\displaystyle\int\frac{1}{x(2x+1)}\,dx$。
?

````````col
```````col-md
flexGrow=20
===

**答案**：$\ln|x|-\ln|2x+1|+C$

**解析**

> 作部分分式分解：
> $$\frac{1}{x(2x+1)}=\frac{A}{x}+\frac{B}{2x+1}$$
> 通分后比较分子 $A(2x+1)+Bx=1$。令 $x=0$ 得 $A=1$；比较 $x$ 的系数 $2A+B=0$，得 $B=-2$。故
> $$\frac{1}{x(2x+1)}=\frac{1}{x}-\frac{2}{2x+1}$$
> 积分得
> $$\ln|x|-\ln|2x+1|+C$$

**考点**

有理函数的部分分式积分
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz

# 2019年

## 第17题

xxxx

**题目**

计算不定积分 $\displaystyle\int\frac{1}{1-2x}\,dx=$（　）

A. $\dfrac{1}{2}\ln|1-2x|+C$

B. $\dfrac{1}{2}\ln(1-2x)+C$

C. $-\dfrac{1}{2}\ln|1-2x|+C$

D. $-\dfrac{1}{2}\ln(1-2x)+C$
?

````````col
```````col-md
flexGrow=20
===

**答案**：C

**解析**

> 令 $u=1-2x$，则 $du=-2\,dx$，即 $dx=-\dfrac12 du$：
> $$\int\frac{1}{1-2x}\,dx=-\frac12\int\frac{1}{u}\,du=-\frac12\ln|u|+C=-\frac12\ln|1-2x|+C$$
> 故选 C。

**考点**

凑微分法（第一类换元法）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz

## 第35题

xxxx

**题目**

计算不定积分 $\displaystyle\int\frac{x}{\sqrt{1+x^{2}}}\,dx=$
?

````````col
```````col-md
flexGrow=20
===

**答案**：$\sqrt{1+x^{2}}+C$

**解析**

> 令 $u=1+x^{2}$，则 $du=2x\,dx$，即 $x\,dx=\dfrac12 du$：
> $$\int\frac{x}{\sqrt{1+x^{2}}}\,dx=\frac12\int u^{-1/2}\,du=u^{1/2}+C=\sqrt{1+x^{2}}+C$$

**考点**

凑微分法（第一类换元法）
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

$\displaystyle\int x\cos x\,dx=$
?

````````col
```````col-md
flexGrow=20
===

**答案**：$x\sin x+\cos x+C$

**解析**

> 用分部积分法，令 $u=x$，$dv=\cos x\,dx$，则 $du=dx$，$v=\sin x$：
> $$\int x\cos x\,dx=x\sin x-\int\sin x\,dx=x\sin x+\cos x+C$$

**考点**

分部积分法
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz

# 2018年

## 第12题

xxxx

**题目**

已知 $\displaystyle\int f(x)\,dx=x^{3}+C$，则 $\displaystyle\int x\,f(1-x^{2})\,dx=$（　）

A. $(1-x^{2})^{3}+C$

B. $\dfrac{1}{2}(1-x^{2})^{3}$

C. $\dfrac{1}{2}(1-x^{2})^{3}+C$

D. $-\dfrac{1}{2}(1-x^{2})^{3}+C$
?

````````col
```````col-md
flexGrow=20
===

**答案**：D

**解析**

> 令 $u=1-x^{2}$，则 $du=-2x\,dx$，即 $x\,dx=-\dfrac12 du$：
> $$\int x\,f(1-x^{2})\,dx=-\frac12\int f(u)\,du=-\frac12 u^{3}+C=-\frac12(1-x^{2})^{3}+C$$
> 故选 D。

**考点**

凑微分法（第一类换元法）
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

不定积分 $\displaystyle\int\frac{1}{x^{2}}\,dx=$
?

````````col
```````col-md
flexGrow=20
===

**答案**：$-\dfrac{1}{x}+C$

**解析**

> 用幂函数积分公式 $\displaystyle\int x^{k}dx=\frac{x^{k+1}}{k+1}+C$，取 $k=-2$：
> $$\int\frac{1}{x^{2}}\,dx=\int x^{-2}\,dx=\frac{x^{-1}}{-1}+C=-\frac1x+C$$

**考点**

基本积分公式（幂函数）
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

求不定积分 $\displaystyle\int x\sqrt{x-1}\,dx$。
?

````````col
```````col-md
flexGrow=20
===

**答案**：$\dfrac{2}{5}(x-1)^{5/2}+\dfrac{2}{3}(x-1)^{3/2}+C$

**解析**

> 令 $t=\sqrt{x-1}$，则 $x=t^{2}+1$，$dx=2t\,dt$：
> $$\int x\sqrt{x-1}\,dx=\int(t^{2}+1)\,t\cdot 2t\,dt=2\int(t^{4}+t^{2})\,dt$$
> $$=2\left(\frac{t^{5}}{5}+\frac{t^{3}}{3}\right)+C$$
> 回代 $t=\sqrt{x-1}$：
> $$\frac{2}{5}(x-1)^{\frac{5}{2}}+\frac{2}{3}(x-1)^{\frac{3}{2}}+C$$

**考点**

根式代换（第二类换元法）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz

# 2017年

## 第15题

xxxx

**题目**

$\cos\dfrac{\pi}{2}x$ 的一个原函数是（　）

A. $\dfrac{\pi}{2}\sin\dfrac{\pi}{2}x$

B. $\dfrac{2}{\pi}\sin\dfrac{\pi}{2}x$

C. $\dfrac{\pi}{2}\sin\dfrac{2}{\pi}x$

D. $\dfrac{\pi}{2}\sin\dfrac{1}{2}x$
?

````````col
```````col-md
flexGrow=20
===

**答案**：B

**解析**

> 用凑微分法：
> $$\int\cos\frac{\pi}{2}x\,dx=\frac{2}{\pi}\int\cos\frac{\pi}{2}x\,d\left(\frac{\pi}{2}x\right)=\frac{2}{\pi}\sin\frac{\pi}{2}x+C$$
> 故一个原函数为 $\dfrac{2}{\pi}\sin\dfrac{\pi}{2}x$，选 B。

**考点**

凑微分法（第一类换元法）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz

## 第35题

xxxx

**题目**

不定积分 $\displaystyle\int e^{2x}\cos 3x\,dx=$
?

````````col
```````col-md
flexGrow=20
===

**答案**：$\dfrac{2}{13}e^{2x}\cos 3x+\dfrac{3}{13}e^{2x}\sin 3x+C$

**解析**

> 这是循环型分部积分，令 $I=\displaystyle\int e^{2x}\cos 3x\,dx$。
>
> 第一次分部，令 $u=\cos 3x$，$dv=e^{2x}dx$，则 $v=\dfrac12 e^{2x}$：
> $$I=\frac12 e^{2x}\cos 3x+\frac32\int e^{2x}\sin 3x\,dx$$
> 第二次分部，令 $u=\sin 3x$，$dv=e^{2x}dx$：
> $$\int e^{2x}\sin 3x\,dx=\frac12 e^{2x}\sin 3x-\frac32 I$$
> 代回：
> $$I=\frac12 e^{2x}\cos 3x+\frac32\left(\frac12 e^{2x}\sin 3x-\frac32 I\right)=\frac12 e^{2x}\cos 3x+\frac34 e^{2x}\sin 3x-\frac94 I$$
> 移项得 $\dfrac{13}{4}I=\dfrac12 e^{2x}\cos 3x+\dfrac34 e^{2x}\sin 3x$，故
> $$I=\frac{2}{13}e^{2x}\cos 3x+\frac{3}{13}e^{2x}\sin 3x+C$$

**考点**

循环型分部积分法
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz

## 第44题

xxxx

**题目**

计算不定积分 $\displaystyle\int\cos^{2}\frac{x}{2}\,dx$。
?

````````col
```````col-md
flexGrow=20
===

**答案**：$\dfrac{x}{2}+\dfrac{1}{2}\sin x+C$

**解析**

> 用半角公式 $\cos^{2}\dfrac{x}{2}=\dfrac{1+\cos x}{2}$：
> $$\int\cos^{2}\frac{x}{2}\,dx=\frac12\int(1+\cos x)\,dx=\frac{x}{2}+\frac12\sin x+C$$

**考点**

三角恒等变换求不定积分
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz

# 2016年

## 第16题

xxxx

**题目**

已知 $F(x)$ 是 $f(x)$ 的一个原函数，则不定积分 $\displaystyle\int f(x-1)\,dx=$（　）

A. $F(x-1)+C$

B. $F(x)+C$

C. $-F(x-1)+C$

D. $-F(x)+C$
?

````````col
```````col-md
flexGrow=20
===

**答案**：A

**解析**

> 令 $u=x-1$，则 $du=dx$：
> $$\int f(x-1)\,dx=\int f(u)\,du=F(u)+C=F(x-1)+C$$
> 故选 A。

**考点**

凑微分法（第一类换元法）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz

## 第35题

xxxx

**题目**

不定积分 $\displaystyle\int\sin(x+1)\,dx=$
?

````````col
```````col-md
flexGrow=20
===

**答案**：$-\cos(x+1)+C$

**解析**

> 用凑微分法：
> $$\int\sin(x+1)\,dx=\int\sin(x+1)\,d(x+1)=-\cos(x+1)+C$$

**考点**

凑微分法（第一类换元法）
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

计算不定积分 $\displaystyle\int\frac{2\ln x-1}{x}\,dx$。
?

````````col
```````col-md
flexGrow=20
===

**答案**：$\ln^{2}x-\ln x+C$

**解析**

> 令 $u=\ln x$，则 $du=\dfrac1x dx$：
> $$\int\frac{2\ln x-1}{x}\,dx=\int(2u-1)\,du=u^{2}-u+C=\ln^{2}x-\ln x+C$$

**考点**

凑微分法（第一类换元法）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz

> （注：部分内容由豆包 AI 生成）