# L 积分的计算_第1页.png

## 一元函数积分学的计算方法
- $\cot x$：kāo，$\tan x$
- $\sec x$：sēi, yè, nà, x
- $\csc x$：kāo，$\sec x$
● 难点1：
$$(F(x))'=f(x)$$
由$F(x)$求$f(x)$很简单，
但由$f(x)$求$F(x)$很难。
● 难点2：
当$F(x)$不是一个初等函数时，
那么，有时基本的积分方法是不奏效的。
## 基本积分公式（10组公式，要熟记于心）
1.  
$$\int x^k \mathrm{d}x = \frac{1}{k+1}x^{k+1} + C,\quad k\neq -1$$
$$\int \frac{1}{x^2}\mathrm{d}x = -\frac{1}{x} + C$$
$$\int \frac{1}{\sqrt{x}}\mathrm{d}x = 2\sqrt{x} + C$$
2.  
$$\int \frac{1}{x}\mathrm{d}x = \ln|x| + C \quad \text{“视绝对值而不见”}$$
3.  
$$\int e^x \mathrm{d}x = e^x + C$$
$$\int a^x \mathrm{d}x = \frac{a^x}{\ln a} + C,\quad a>0,且a\neq1$$
4.  
$$\int \sin x \mathrm{d}x = -\cos x + C$$
$$\int \cos x \mathrm{d}x = \sin x + C$$

---

# L 积分的计算_第2页.png

## 三角函数类基本不定积分公式
$$\int \tan x \, dx = -\ln|\cos x| + C$$
注：“用凑微分法可推”
$$\int \cot x \, dx = \ln|\sin x| + C$$
$$\int \frac{dx}{\cos x} = \int \sec x \, dx = \ln|\sec x + \tan x| + C$$
$$\int \frac{dx}{\sin x} = \int \csc x \, dx = \ln|\csc x - \cot x| + C$$
$$\int \sec^2 x \, dx = \tan x + C$$
$$\int \csc^2 x \, dx = -\cot x + C$$
$$\int \sec x \tan x \, dx = \sec x + C$$
$$\int \csc x \cot x \, dx = -\csc x + C$$

## 5. 反正切型不定积分
$$\int \frac{1}{1+x^2} \, dx = \arctan x + C$$
$$\int \frac{1}{a^2+x^2} \, dx = \frac{1}{a}\arctan \frac{x}{a} + C \quad (a>0)$$
$$
\begin{align*}
\int \frac{1}{a^2+x^2} dx &= \frac{1}{a^2}\int \frac{1}{1+\left( \frac{x}{a} \right)^2} dx \\
&= \frac{1}{a}\int \frac{1}{1+\left( \frac{x}{a} \right)^2} \cdot \frac{1}{a} dx \\
&= \frac{1}{a}\int f\left[g(x)\right] g'(x) dx \\
&= \frac{1}{a}\int f[u] du
\end{align*}
$$

## 6. 反正弦型不定积分
$$\int \frac{1}{\sqrt{1-x^2}} \, dx = \arcsin x + C$$
$$\int \frac{1}{\sqrt{a^2-x^2}} \, dx = \arcsin \frac{x}{a} + C \quad (a>0)$$

---

# L 积分的计算_第3页.png

7.
$$\int \frac{1}{\sqrt{x^2+a^2}} \, dx = \ln\left(x+\sqrt{x^2+a^2}\right) + C \quad [\text{常见} \ a=1]$$
$$\int \frac{1}{\sqrt{x^2-a^2}} \, dx = \ln\left|x+\sqrt{x^2-a^2}\right| + C \quad [|x|>|a|]$$

8.
$$\int \frac{1}{x^2-a^2} \, dx = \frac{1}{2a}\ln\left|\frac{x-a}{x+a}\right| + C$$
$$\int \frac{1}{a^2-x^2} \, dx = \frac{1}{2a}\ln\left|\frac{x+a}{x-a}\right| + C$$

9.
$$\int \sqrt{a^2-x^2} \, dx = \frac{a^2}{2}\arcsin\frac{x}{a} + \frac{x}{2}\sqrt{a^2-x^2} + C \quad (a>|x|\geq0)$$

10.
$$\int \sin^2x \, dx = \frac{x}{2} - \frac{\sin2x}{4} + C$$
$$\sin^2x = \frac{1-\cos2x}{2}$$

$$\int \cos^2x \, dx = \frac{x}{2} + \frac{\sin2x}{4} + C$$
$$\cos^2x = \frac{1+\cos2x}{2}$$

$$\int \tan^2x \, dx = \tan x - x + C$$
$$\tan^2x = \sec^2x - 1$$

$$\int \cot^2x \, dx = -\cot x - x + C$$
$$\cot^2x = \csc^2x - 1$$

---

# L 积分的计算_第4页.png

## 不定积分的积分法
要用这些方法，把给的这些题目归到那10组基本积分公式上去。
## 凑微分法
（换元法的反过来）
由微分的定义：
$$f'(x) = \frac{\mathrm{d}f(x)}{\mathrm{d}x}$$
凑微分法的推导过程如下：
$$
\begin{alignat*}{2}
\int h(x)\mathrm{d}x &= \int f\left[g(x)\right]g'(x)\mathrm{d}x &\qquad f'\left[g(x)\right] &= \frac{\mathrm{d}f\left[g(x)\right]}{\mathrm{d}g(x)} \\
&= \int f\left[g(x)\right]\mathrm{d}\left[g(x)\right] &\qquad \left\{f\left[g(x)\right]\right\}' &= \frac{\mathrm{d}f\left[g(x)\right]}{\mathrm{d}x} \\
&= \int f(u)\mathrm{d}u \quad (\text{令 } g(x)=u)
\end{alignat*}
$$
注：当被积函数比较复杂时，拿出一部分放到$d$后面去，若能凑成$\int f(u)\mathrm{d}u$的形式则凑微分成功。
eg：
$$
\begin{align*}
\int \frac{\ln^5 x}{x}\mathrm{d}x &= \int \ln^5 x \cdot \frac{1}{x}\mathrm{d}x \\
&= \int \ln^5 x \mathrm{d}\ln x = \int (\ln x)^5 \mathrm{d}\ln x \\
&= \frac{\ln^6 x}{6} + C
\end{align*}
$$

---

# L 积分的计算_第5页.png

## 常用的凑微分公式
- 由于 $x\mathrm{d}x = \frac{1}{2}\mathrm{d}(x^2)$，
则
$$\int x f(x^2)\mathrm{d}x = \frac{1}{2}\int f(x^2)\mathrm{d}(x^2) = \frac{1}{2}\int f(u)\mathrm{d}u$$
- 由于 $\sqrt{x}\mathrm{d}x = \frac{2}{3}\mathrm{d}\left(x^{\frac{3}{2}}\right)$，
则
$$\int \sqrt{x} f\left(x^{\frac{3}{2}}\right)\mathrm{d}x = \frac{2}{3}\int f\left(x^{\frac{3}{2}}\right)\mathrm{d}\left(x^{\frac{3}{2}}\right)$$
- 由于 $\frac{1}{\sqrt{x}}\mathrm{d}x = 2\mathrm{d}(\sqrt{x})$，
则
$$\int \frac{f(\sqrt{x})}{\sqrt{x}}\mathrm{d}x = 2\int f(\sqrt{x})\mathrm{d}(\sqrt{x})$$
- 由于 $\frac{1}{x^2}\mathrm{d}x = \mathrm{d}\left(-\frac{1}{x}\right)$，
则
$$\int \frac{f\left(-\frac{1}{x}\right)}{x^2}\mathrm{d}x = \int f\left(-\frac{1}{x}\right)\mathrm{d}\left(-\frac{1}{x}\right)$$
- 由于当$x>0$时，$\frac{1}{x}\mathrm{d}x = \mathrm{d}(\ln x)$，
则
$$\int \frac{f(\ln x)}{x}\mathrm{d}x = \int f(\ln x)\mathrm{d}(\ln x)$$
- 由于 $e^x\mathrm{d}x = \mathrm{d}(e^x)$，
则
$$\int e^x f(e^x)\mathrm{d}x = \int f(e^x)\mathrm{d}(e^x)$$
- 由于 $a^x\mathrm{d}x = \frac{1}{\ln a}\mathrm{d}(a^x),\ a>0,a\neq1$，
则
$$\int a^x f(a^x)\mathrm{d}x = \frac{1}{\ln a}\int f(a^x)\mathrm{d}(a^x)$$
- 由于 $\sin x\mathrm{d}x = \mathrm{d}(-\cos x)$，
则
$$\int \sin x f(-\cos x)\mathrm{d}x = \int f(-\cos x)\mathrm{d}(-\cos x)$$
- 由于 $\cos x\mathrm{d}x = \mathrm{d}(\sin x)$，
则
$$\int \cos x f(\sin x)\mathrm{d}x = \int f(\sin x)\mathrm{d}(\sin x)$$

---

# L 积分的计算_第6页.png

## 常用凑微分公式
- 由于$\frac{1}{\cos^2 x}dx = \sec^2 x dx = d(\tan x)$，则
$$\int \frac{f(\tan x)}{\cos^2 x}dx = \int f(\tan x)d(\tan x)$$
- 由于$\frac{1}{\sin^2 x}dx = \csc^2 x dx = d(-\cot x)$，则
$$\int \frac{f(-\cot x)}{\sin^2 x}dx = \int f(-\cot x)d(-\cot x)$$
- 由于$\frac{1}{1+x^2}dx = d(\arctan x)$，则
$$\int \frac{f(\arctan x)}{1+x^2}dx = \int f(\arctan x)d(\arctan x)$$
- 由于$\frac{1}{\sqrt{1-x^2}}dx = d(\arcsin x)$，则
$$\int \frac{f(\arcsin x)}{\sqrt{1-x^2}}dx = \int f(\arcsin x)d(\arcsin x)$$

## 例9.1
求不定积分：
$$\int \frac{\sqrt{x}}{\sqrt{4-x^3}} dx$$
**思路**：将积分凑为$\int f[g(x)]g'(x)dx$的形式，找出内层函数$g(x)$与$g'(x)$。

解：
先对被积函数拆分变形：
$$\int \frac{\sqrt{x}}{\sqrt{4-x^3}} dx = \int \frac{1}{\sqrt{4-x^3}} \cdot \sqrt{x} dx$$
计算幂函数部分的积分：
$$\int \sqrt{x} dx = \frac{2}{3}x^{\frac{3}{2}}$$
因此$\sqrt{x}dx = \frac{2}{3}d\left(x^{\frac{3}{2}}\right)$，凑微分得：
$$\int \frac{\sqrt{x}}{\sqrt{4-x^3}} dx = \frac{2}{3}\int \frac{1}{\sqrt{2^2-\left(x^{\frac{3}{2}}\right)^2}} \cdot \left(x^{\frac{3}{2}}\right)' dx$$
利用基本积分公式：
$$\int \frac{1}{\sqrt{a^2-u^2}}du = \arcsin \frac{u}{a} + C \quad (a>0)$$
令$u=x^{\frac{3}{2}},a=2$，代入得最终结果：
$$\int \frac{\sqrt{x}}{\sqrt{4-x^3}} dx = \frac{2}{3}\arcsin \frac{x^{\frac{3}{2}}}{2} + C$$

---

# L 积分的计算_第7页.png

## 例9.2
求不定积分
$$\int e^{\frac{\sin\theta}{\cos\theta+\sin\theta}} \cdot \frac{1}{(\cos\theta+\sin\theta)^2} \, \mathrm{d}\theta$$
解：先将积分看成$\int f[g(x)]g'(x)\mathrm{d}x$的形式，找出$g(x)$与$g'(x)$：
若取$g(\theta) = \frac{\sin\theta}{\cos\theta+\sin\theta}$，对其求导：
$$
\begin{aligned}
\left( \frac{\sin\theta}{\cos\theta+\sin\theta} \right)' &= \frac{\cos\theta(\cos\theta+\sin\theta) - \sin\theta(-\sin\theta+\cos\theta)}{(\cos\theta+\sin\theta)^2} \\
&= \frac{1}{(\cos\theta+\sin\theta)^2}
\end{aligned}
$$
因此有$\frac{1}{(\cos\theta+\sin\theta)^2}\mathrm{d}\theta = \mathrm{d}\left( \frac{\sin\theta}{\cos\theta+\sin\theta} \right)$，代入原积分得：
$$
\begin{aligned}
\text{原式} &= \int e^{\frac{\sin\theta}{\cos\theta+\sin\theta}} \, \mathrm{d}\left( \frac{\sin\theta}{\cos\theta+\sin\theta} \right) \\
&\xlongequal{\text{令}u=\frac{\sin\theta}{\cos\theta+\sin\theta}} \int e^u \, \mathrm{d}u \\
&= e^u + C \\
&= e^{\frac{\sin\theta}{\cos\theta+\sin\theta}} + C
\end{aligned}
$$

## 换元法（凑微分法反过来）
换元法推导步骤：
$$
\begin{aligned}
\int f(x) \, \mathrm{d}x &= \int f[g(u)] \, \mathrm{d}[g(u)] \quad \text{令} \ x=g(u) \\
&= \int f[g(u)] g'(u) \, \mathrm{d}u \\
&= \int h(u) \, \mathrm{d}u \quad \text{令} \ f[g(u)]g'(u) = h(u) \\
&= H(u) + C \quad \text{求出积分}
\end{aligned}
$$
回代，令$u=g^{-1}(x)$并验证：
$$
\begin{aligned}
&= H\left[g^{-1}(x)\right] + C \\
&= \int f(x) \, \mathrm{d}x
\end{aligned}
$$

---

# L 积分的计算_第8页.png

## 常用的换元法
理解：当遇到$f(x)$比较复杂时（有根号或分母复杂），
e.g. $f(x)=\sqrt{e^x+1}$、$\sqrt{\frac{2x+1}{x+1}}$、$\frac{1}{\sqrt{e^{2x}+1}}$
引入新的自变量$u$，让其变为简单的$h(u)$（无根号或分母简单）。

注：
1.  当被积函数不容易积分（比如含有根式或反三角函数）时，可以通过换元的方法从$d$后面拿出一部分放到前面来，就成为
    $$\int f[g(u)]g'(u)du$$
    的形式，若$f[g(u)]g'(u)$容易积分，则换元成功。
2.  $x=g(u)$必须是单调可导函数（只有单调才能有反函数），且不要忘记，计算结束后用反函数$u=g^{-1}(x)$回代。

### 1. 三角函数代换
当被积函数含有如下根式时，可作三角函数代换，这里$a>0$：
- 对于根式$\sqrt{a^2-x^2}$：令$x=a\sin t$，其中$|t|<\frac{\pi}{2}$，附$x=a\sin t$的函数示意图。
- 对于根式$\sqrt{a^2+x^2}$：令$x=a\tan t$，其中$|t|<\frac{\pi}{2}$，附$x=a\tan t$的函数示意图。
- 对于根式$\sqrt{x^2-a^2}$：令$x=a\sec t$，$t$的取值范围为
  $$
  \begin{cases}
  若x>0,则0<t<\frac{\pi}{2} \\
  若x<0,则\frac{\pi}{2}<t<\pi
  \end{cases}
  $$
  附$x=a\sec t$的函数示意图。

---

# L 积分的计算_第9页.png

## 例题：计算$\int \sqrt{a^2-x^2}\, dx$
使用三角换元法，令$x=a\sin t$，限定$|t|<\frac{\pi}{2}$，推导过程如下：
$$
\begin{align*}
\int \sqrt{a^2-x^2}\, dx &= \int \sqrt{a^2-(a\sin t)^2}\, d(a\sin t) \\
&= \int \sqrt{a^2(1-\sin^2 t)}\, d(a\sin t) \\
&= \int \sqrt{a^2\cos^2 t}\, d(a\sin t) \\
&= \int a\cos t \cdot a\cos t\, dt \\
&= a^2\int \cos^2 t\, dt \quad \text{（该积分属于第10组基本积分公式）} \\
&= a^2\left( \frac{t}{2} + \frac{\sin2t}{4} \right) + C
\end{align*}
$$
### 回代
由反函数定义：若$y=\sin x = f(x)$，则$x=f^{-1}(y)=\arcsin y$。
此处$\frac{x}{a}=\sin t$（将$\frac{x}{a}$整体看作$y$），因此将$t=\arcsin \frac{x}{a}$回代：
利用三角恒等式$\sin2t=2\sin t\cos t$，结合辅助直角三角形（斜边为$a$，角$t$对边为$x$，邻边为$\sqrt{a^2-x^2}$），可得$\sin t=\frac{x}{a}$，$\cos t=\frac{\sqrt{a^2-x^2}}{a}$，代入得：
$$
\begin{align*}
\text{原式}&=a^2\left( \frac{1}{2}\arcsin \frac{x}{a} + \frac{2\sin t\cos t}{4} \right) + C \\
&=a^2\left( \frac{1}{2}\arcsin \frac{x}{a} + \frac{1}{2}\cdot \frac{x}{a}\cdot \frac{\sqrt{a^2-x^2}}{a} \right) + C \\
&= \frac{a^2}{2}\arcsin \frac{x}{a} + \frac{1}{2}x\sqrt{a^2-x^2} + C
\end{align*}
$$
注：$\int \sqrt{a^2-x^2}\, dx$ 属于第9组基本积分公式。
## 2. ⚠️ 恒等变形后作三角函数代换
当被积函数含有根式$\sqrt{ax^2+bx+c}$时，可先通过配方恒等变形为以下三种形式之一，再作三角函数代换求解积分：
$$\sqrt{\varphi^2(x)+k^2},\quad \sqrt{\varphi^2(x)-k^2},\quad \sqrt{k^2-\varphi^2(x)}$$

---

# L 积分的计算_第10页.png

## 3. 根式代换（举重若轻）
当被积函数含有根式
$\sqrt[n]{ax+b}$，$\sqrt{\frac{ax+b}{cx+d}}$，$\sqrt{ae^{bx}+c}$时

（因为很难通过根号内换元的办法凑出平方，就没法用三角函数代换等方法把根号去掉）
直接令根式为$t$，e.g. 令$\sqrt[n]{ax+b}=t$

若表达式里既含有$\sqrt[n]{ax+b}$，也含有$\sqrt[m]{ax+b}$的函数，
则取$m,n$的最小公倍数$k$
令$\sqrt[k]{ax+b}=t$

## 4. 倒代换
当被积函数分母的幂次比分子高两次及两次以上时，作倒代换，令$x=\frac{1}{t}$

## 5. 复杂函数直接代换
当被积函数中含有$a^x$，$e^x$，$\ln x$，$\arcsin x$，$\arctan x$时
直接令复杂函数等于$t$

若$\ln x$，$\arcsin x$，$\arctan x$与$P_n(x)$或$e^{ax}$作乘法时，优先考虑分部积分法

[$P_n(x)$为$x$的$n$次多项式]

---

# L 积分的计算_第11页.png

## 分部积分法（$u,v$一般是不同类型的函数）
$$\int u\mathrm{d}v = uv - \int v\mathrm{d}u$$
推导：
$$(uv)' = u'v + uv'$$
两边对$x$积分：
$$\int (uv)'\mathrm{d}x = \int u'v\mathrm{d}x + \int uv'\mathrm{d}x$$
改写为微分形式：
$$\int \frac{\mathrm{d}(uv)}{\mathrm{d}x}\mathrm{d}x = \int \frac{\mathrm{d}u}{\mathrm{d}x}v\mathrm{d}x + \int u\frac{\mathrm{d}v}{\mathrm{d}x}\mathrm{d}x$$
$\frac{\mathrm{d}(\quad)}{\mathrm{d}x}$与$\int (\quad)\mathrm{d}x$互为逆运算，因此：
$$uv = \int v\mathrm{d}u + \int u\mathrm{d}v$$
移项得：
$$\implies \int u\mathrm{d}v = uv - \int v\mathrm{d}u$$
这个方法主要适用于求$\int u\mathrm{d}v$比较难，而$\int v\mathrm{d}u$比较简单的情形。

注1：
$$
\begin{align*}
\int uv'\mathrm{d}x &= \int u\mathrm{d}v \\
&= \int u\mathrm{d}(v+c)
\end{align*}
$$
即 $v' = \frac{\mathrm{d}v}{\mathrm{d}x} = \frac{\mathrm{d}(v+c)}{\mathrm{d}x}$。

注2：$[P_n(x)\text{为}x\text{的}n\text{次多项式}]$
积分后会“简单”些的函数宜取作$v$，微分后会“简单”些的函数宜取作$u$。

按**反、对、幂、指、三**的顺序选取$u,v$，对应代表函数依次为$\arcsin x$、$\ln x$、$x^2$、$e^x$、$\sin x$：
$$\xleftarrow{\quad U\quad \text{越不易积分}\quad} \text{反}\quad\text{对}\quad\text{幂}\quad\text{指}\quad\text{三} \xrightarrow{\quad V\quad \text{越易积分}\quad}$$
分部积分转化关系：
$$\int u\mathrm{d}v \longrightarrow \int v\mathrm{d}u = \int vu'\mathrm{d}x$$
排在顺序左侧的函数宜选作$u$，用来求导；排在顺序右侧的函数宜选作$v$，用来积分。
- 当被积函数为$P_n(x)e^{kx}$、$P_n(x)\sin ax$、$P_n(x)\cos ax$等形式时，选取$u=P_n(x)$；
- 当被积函数为$e^{ax}\sin bx$、$e^{ax}\cos bx$等形式时，$u$选哪一个都行。

---

# L 积分的计算_第12页.png

## 分部积分法u的选取规则（对数、反三角函数类）
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

## 多次分部积分示例（多项式乘指数函数）
再例：计算$\int x^3 e^x\,\mathrm{d}x$
分部积分公式：
$$\int u\,\mathrm{d}v = uv - \int v\,\mathrm{d}u = uv - \int v u'\,\mathrm{d}x$$
第一次分部选取$u=x^3$，$v=e^x$：
$$
\begin{aligned}
\int x^3 e^x\,\mathrm{d}x &= \int x^3\,\mathrm{d}e^x \\
&= x^3 e^x - \int e^x\,\mathrm{d}(x^3) \\
&= x^3 e^x - \int e^x\cdot 3x^2\,\mathrm{d}x \\
&= x^3 e^x - 3\int x^2\,\mathrm{d}e^x
\end{aligned}
$$
又来一次分部积分，满足$\int uv'\,\mathrm{d}x=\int u\,\mathrm{d}v$，选取$u=x^2$，$v=e^x$：
$$
\begin{aligned}
&= x^3 e^x - 3\left(x^2 e^x - \int e^x\,\mathrm{d}(x^2)\right) \\
&= x^3 e^x - 3\left(x^2 e^x - \int e^x\cdot 2x\,\mathrm{d}x\right) \\
&= x^3 e^x - 3\left(x^2 e^x - 2\int x\,\mathrm{d}e^x\right)
\end{aligned}
$$
还可再来一次分部积分，选取$u=x$，$v=e^x$：
$$
\begin{aligned}
&= x^3 e^x - 3\left[x^2 e^x - 2\left(x e^x - \int e^x\,\mathrm{d}x\right)\right] \\
&= x^3 e^x - 3\left(x^2 e^x - 2x e^x + 2e^x\right) + C \\
&= x^3 e^x - 3x^2 e^x + 6x e^x - 6e^x + C
\end{aligned}
$$

这样写，要用多次分部积分，很麻烦。

$\therefore \quad \downarrow$

---

# L 积分的计算_第13页.png

## 分部积分法的推广公式
该公式适用于计算$\int P_n(x)e^{kx}\mathrm{d}x$、$\int P_n(x)\sin ax \mathrm{d}x$、$\int P_n(x)\cos bx \mathrm{d}x$类型的不定积分，其中$P_n(x)$为$n$次多项式。

设函数$u=u(x)$与$v=v(x)$具有直到第$(n+1)$阶的连续导数，根据分部积分公式：
$$
\begin{aligned}
\int uv'\mathrm{d}x &= \int u\mathrm{d}v = uv - \int v\mathrm{d}u \\
&= uv - \int u'v\mathrm{d}x
\end{aligned}
$$

逐次应用分部积分可得推广公式：
$$
\begin{aligned}
\int uv^{(n+1)}\mathrm{d}x &= uv^{(n)} - u'v^{(n-1)} + u''v^{(n-2)} - \dots \\
&\quad + (-1)^n u^{(n)}v + (-1)^{n+1}\int u^{(n+1)}v\mathrm{d}x
\end{aligned}
$$

### 推导（n=3时的公式）
证明：对$\int uv^{(4)}\mathrm{d}x$逐次应用分部积分法：
$$
\int uv^{(4)}\mathrm{d}x = \int u\mathrm{d}\left[v^{(3)}\right] = uv^{(3)} - \int u'v^{(3)}\mathrm{d}x
$$
$$
\int u'v^{(3)}\mathrm{d}x = \int u'\mathrm{d}\left[v''\right] = u'v'' - \int u''v''\mathrm{d}x
$$
$$
\int u''v''\mathrm{d}x = \int u''\mathrm{d}\left[v'\right] = u''v' - \int u^{(3)}v'\mathrm{d}x
$$
$$
\int u^{(3)}v'\mathrm{d}x = \int u^{(3)}\mathrm{d}v = u^{(3)}v - \int u^{(4)}v\mathrm{d}x
$$

联立以上式子得：
$$
\int uv^{(4)}\mathrm{d}x = uv^{(3)} - u'v'' + u''v' - u^{(3)}v + \int u^{(4)}v\mathrm{d}x
$$

### 表格记法
上述公式可通过表格快速计算，表格结构如下：
| $u$的各阶导数 | $u$ | $u'$ | $u''$ | $u^{(3)}$ | $u^{(4)}$ |
| :---: | :---: | :---: | :---: | :---: | :---: |
| $v^{(4)}$的各阶原函数 | $v^{(4)}$ | $v^{(3)}$ | $v''$ | $v'$ | $v$ |

计算规则：以$u$作为起点，按左上、右下错位相乘，各项符号“+”“-”交替出现，最后剩余项为$\int u^{(4)}v\mathrm{d}x$。

### 例题
计算$\int x^3 e^x \mathrm{d}x$：
选取$u=x^3$，$\mathrm{d}v=e^x\mathrm{d}x$，列表计算$u$的各阶导数与$v$的各阶原函数：
| $u$的各阶导数 | $x^3$ | $3x^2$ | $6x$ | $6$ | $0$ |
| :---: | :---: | :---: | :---: | :---: | :---: |
| $v$的各阶原函数 | $e^x$ | $e^x$ | $e^x$ | $e^x$ | $e^x$ |

按照表格规则计算得：
$$
\begin{aligned}
\int x^3 e^x \mathrm{d}x &= x^3 e^x - 3x^2 e^x + 6x e^x - 6e^x + \int 0\cdot e^x \mathrm{d}x \\
&= x^3 e^x - 3x^2 e^x + 6x e^x - 6e^x + C
\end{aligned}
$$

---

# L 积分的计算_第14页.png

以下是综合性的不定积分例题：
综合求解方法包含：
$$
\begin{cases}
\text{恒等变形（诱导公式等，加一下、减一下的技巧等）}\\
\text{凑微分法}\\
\text{换元法}\\
\text{分部积分法}
\end{cases}
$$

注：以下例题解法不唯一

## 例9.4
求不定积分
$$\int \frac{x e^x}{\sqrt{e^x -1}} \, dx$$

【分析】分母很复杂且带有根号，像个$\triangle$，看上去很稳固，$\int \triangle dx$一般没有$\int \triangledown dx$好写。

解：令$\sqrt{e^x -1}=t$（换元法），
则$e^x = 1+t^2$，
可得$x = \ln(1+t^2)$。

$$
\begin{align*}
\text{原式} &= \int \frac{\ln(1+t^2) \cdot (1+t^2)}{t} \, d\left[\ln(1+t^2)\right] \\
&= \int \frac{\ln(1+t^2)(1+t^2)}{t} \cdot \frac{2t}{1+t^2} \, dt \\
&= 2\int \ln(1+t^2) \, dt \quad \text{（变简单了）}
\end{align*}
$$
被积函数为不同类型函数乘积的形式，考虑用分部积分法：
$$
\begin{align*}
&= 2\left[ t\ln(1+t^2) - \int t \, d\left[\ln(1+t^2)\right] \right] \\
&= 2\left[ t\ln(1+t^2) - \int t \cdot \frac{2t}{1+t^2} \, dt \right]
\end{align*}
$$

---

# L 积分的计算_第15页.png

$$
\begin{align*}
&=2\left[ t\ln(1+t^2) - 2\int \frac{t^2+1-1}{1+t^2} dt \right] \\
&=2\left[ t\ln(1+t^2) - 2\int dt + 2\int \frac{1}{1+t^2} dt \right] \\
&= 2t\ln(1+t^2) -4t +4\arctan t + C
\end{align*}
$$
回带 $t=\sqrt{e^x -1}$ 验证，由$1+t^2=e^x$得$\ln(1+t^2)=x$，代入得：
$$
=2\left( x\sqrt{e^x -1} - 2\sqrt{e^x -1} + 2\arctan\sqrt{e^x -1} \right) + C
$$
即
$$
\int \frac{x e^x}{\sqrt{e^x -1}} dx = 2\left( x\sqrt{e^x -1} - 2\sqrt{e^x -1} + 2\arctan\sqrt{e^x -1} \right) + C
$$

## 例9.5
求不定积分
$$
\int \frac{x e^{\arctan x}}{(1+x^2)^{\frac{3}{2}}} dx
$$

**分析** 发现分母为$\sqrt{(1+x^2)^3}=(1+x^2)^{\frac{3}{2}}$，为$\sqrt{a^2+x^2}$的形式，考虑用三角函数代换。

**解：** 令$x=\tan t$（换元法），
则$t=\arctan x$，
$$dx = (\tan t)' dt = \sec^2 t dt$$
代入原式化简：
$$
\begin{align*}
\text{原式} &= \int \frac{\tan t \cdot e^t}{\sec^3 t} \cdot \sec^2 t dt \\
&= \int \frac{\tan t \cdot e^t}{\sec t} dt \quad \text{变简单了} \\
&= \int e^t \sin t dt
\end{align*}
$$
其中三角恒等式：
$\sec t = \frac{1}{\cos t}$，$\tan t = \frac{\sin t}{\cos t}$。

---

# L 积分的计算_第16页.png

## 分部积分法（循环型积分求解）
被积函数为不同类型函数乘积的形式，考虑使用分部积分法。
但计算时发现，对该积分无论使用多少次分部积分，结果始终是两个不同类型函数乘积的形式。
（分部积分表格法示意：对$\sin t$逐次求导，结果依次为$\cos t, -\sin t, -\cos t, \sin t, \cdots$，对应交错符号为$+,-,+,\cdots$；对$e^t$逐次积分，结果始终为$e^t,e^t,e^t,\cdots$）
计算过程中$\int \sin t \cdot e^t \, dt$会重复出现，因此可以通过建立方程的方式求解该积分：
$$\int \sin t \, e^t \, dt = e^t\sin t - e^t\cos t - \int \sin t \, e^t \, dt$$
设$I = \int \sin t \, e^t \, dt$，代入上式得：
$$I = e^t(\sin t - \cos t) - I$$
移项整理：
$$2I = e^t(\sin t - \cos t)$$
因此：
$$I = \frac{e^t(\sin t - \cos t)}{2} + C$$
即
$$\int \sin t \, e^t \, dt = \frac{1}{2}e^t(\sin t - \cos t) + C$$
回代$t = \arctan x$，结合直角三角形辅助示意图（角$t$的邻边为$1$，对边为$x$，斜边为$\sqrt{1+x^2}$），可得$\sin t = \frac{x}{\sqrt{1+x^2}}$，$\cos t = \frac{1}{\sqrt{1+x^2}}$，代入得原积分结果：
$$
\begin{align*}
\text{原式} &= \frac{1}{2}e^{\arctan x}\left( \frac{x}{\sqrt{1+x^2}} - \frac{1}{\sqrt{1+x^2}} \right) \\
&= \frac{1}{2}e^{\arctan x} \cdot \frac{x-1}{\sqrt{1+x^2}} + C
\end{align*}
$$
## 例9.6
（一道难题，是一道好且有意思的题）
设$f(\ln x) = \frac{\ln(1+x)}{x}$，计算$\int f(x) \, dx$。
【分析】题目给出的是复合函数，需要先求出$f(x)$的表达式，再计算积分。

---

# L 积分的计算_第17页.png

## 不定积分求解
解：令$\ln x = t$
则$x=e^t$，$f(t)= \frac{\ln(1+e^t)}{e^t}$

$$
\begin{align*}
\int f(x)dx &= \int \frac{\ln(1+e^x)}{e^x}dx \\
&= \int \ln(1+e^x)\cdot e^{-x} dx
\end{align*}
$$

为对数函数与指数函数乘积的形式，考虑用分部积分法。

$u = \ln(1+e^x)$，$v = e^{-x}$

要找$\int u \, dv = \int \ln(1+e^x) \, d e^{-x}$

想把$e^{-x}$放到$d$后面，即$d e^{-x}$

$\because -e^{-x}dx = d e^{-x}$

$\therefore$要添个负号，再乘个负号

即$(-1)\cdot (-e^{-x}dx)$

$$
\begin{align*}
\int f(x)dx &= \int \ln(1+e^x)\cdot (-1)\cdot (-e^{-x})dx \\
&= -\int \ln(1+e^x) \, d e^{-x} \\
&= -e^{-x}\ln(1+e^x) + \int e^{-x}\cdot \frac{e^x}{1+e^x} dx \quad \text{已可凑微分}\\
&= -e^{-x}\ln(1+e^x) + \int \frac{1}{1+e^x} dx \\
&= -e^{-x}\ln(1+e^x) + \int \frac{1+e^x - e^x}{1+e^x} dx
\end{align*}
$$

---

# L 积分的计算_第18页.png

这里要有一个意识和注意点
$$\int \frac{e^x}{1+e^x}dx = \int \frac{1}{1+e^x}de^x = \int \frac{1}{1+e^x}d(e^x+1) = \ln(1+e^x)$$
$\because e^x dx = de^x$，这是一个积分的过程
$\therefore e^x dx = d(e^x + c)$，$c$可为任意常数
即 $e^x = \frac{de^x}{dx}$，$e^x = \frac{d(e^x + c)}{dx}$
$$= -\ln(1+e^x)e^{-x} + \int dx - \int \frac{e^x}{1+e^x}dx$$
$$= -\ln(1+e^x)e^{-x} + x - \ln(1+e^x) + C$$

## 例9.7
计算 $\int e^{2x}(\tan x + 1)^2 dx$

**[分析]** 因为式子比较复杂，且正好有三角公式：
$$(\tan x + 1)^2 = \tan^2 x + 2\tan x + 1$$
$$\tan^2 x + 1 = \sec^2 x,\quad (\tan x)' = \sec^2 x$$
则试着化简：

解：
$$
\begin{align*}
\text{原式} &= \int e^{2x}(\tan^2 x + 2\tan x + 1)dx \\
&= \int e^{2x}\cdot \sec^2 x dx + 2\int e^{2x}\tan x dx
\end{align*}
$$
为两个不同函数乘积的形式，考虑用分部积分：
$$
\begin{align*}
&= \int e^{2x}d(\tan x) + 2\int e^{2x}\tan x dx \\
&= e^{2x}\tan x - \int \tan x d(e^{2x}) + 2\int e^{2x}\tan x dx
\end{align*}
$$

---

# L 积分的计算_第19页.png

$$= e^{2x}\tan x - 2\int \tan x \, e^{2x} \, dx + 2\int e^{2x}\tan x \, dx$$
$$= e^{2x}\tan x + C$$

## 特殊函数的不定积分
对不定积分的基本积分法的应用

## 有理函数的积分
所谓有理函数，就是形如$\frac{P_n(x)}{Q_m(x)}$的函数，其中：
- $P_n(x)$为$x$的$n$次多项式
- $Q_m(x)$为$x$的$m$次多项式

有理函数$\frac{P_n(x)}{Q_m(x)}$可分为两类：
- 真分式：满足$n<m$，即$\frac{P_n(x)}{Q_m(x)} \ (n<m)$
- 假分式：满足$n\geq m$，即$\frac{P_n(x)}{Q_m(x)} \ (n\geq m)$

假分式 = 多项式 + 真分式
例：
$$\frac{x^2}{x+1} = \frac{x^2-1+1}{x+1} = x-1 + \frac{1}{x+1}$$
所以我们主要研究真分式，即
$$\int \frac{P_n(x)}{Q_m(x)} \, dx \quad (n<m)$$

## 求解步骤
思想：真分式是一定可以表示成若干最简式之和。
① 若$Q_m(x)$在实数域内可因式分解，则因式分解后把$\frac{P_n(x)}{Q_m(x)}$拆成若干项最简有理分式之和。

---

# L 积分的计算_第20页.png

## 最简有理分式有4种
$$\frac{A}{ax+b}$$
若$Q_m(x)$因式分解后出现了$(ax+b)$，那么$\frac{P_n(x)}{Q_m(x)}$就会因式分解出$\frac{A}{ax+b}$。

$$\frac{A_1}{ax+b} + \frac{A_2}{(ax+b)^2} + \dots + \frac{A_k}{(ax+b)^k},\quad k>0,k\neq1$$
若$Q_m(x)$因式分解出$(ax+b)^2$，那么$\frac{P_n(x)}{Q_m(x)}$就会因式分解出$\frac{A_1}{ax+b} + \frac{A_2}{(ax+b)^2}$。
若$Q_m(x)$因式分解出$(ax+b)^k$，那么$\frac{P_n(x)}{Q_m(x)}$就会因式分解出
$$\frac{A_1}{ax+b} + \frac{A_2}{(ax+b)^2} + \dots + \frac{A_k}{(ax+b)^k},\quad k>0,k\neq1$$

$$\frac{Ax+B}{px^2+qx+r}\quad (q^2-4pr<0)$$
其中$q^2-4pr<0$是为了不让分母为0。
若$Q_m(x)$因式分解出了$(px^2+qx+r)$，那么$\frac{P_n(x)}{Q_m(x)}$就会因式分解出$\frac{Ax+B}{px^2+qx+r}$。

$$\frac{A_1x+B_1}{px^2+qx+r} + \frac{A_2x+B_2}{(px^2+qx+r)^2} + \dots + \frac{A_kx+B_k}{(px^2+qx+r)^k}\quad (q^2-4pr<0)$$
若$Q_m(x)$中出现了$(px^2+qx+r)^2$，那么$\frac{P_n(x)}{Q_m(x)}$中就会出现$\frac{A_1x+B_1}{px^2+qx+r} + \frac{A_2x+B_2}{(px^2+qx+r)^2}$。
若$Q_m(x)$中出现了$(px^2+qx+r)^k$，那么$\frac{P_n(x)}{Q_m(x)}$就会因式分解出
$$\frac{A_1x+B_1}{px^2+qx+r} + \frac{A_2x+B_2}{(px^2+qx+r)^2} + \dots + \frac{A_kx+B_k}{(px^2+qx+r)^k}\quad (q^2-4pr<0)$$

---

# L 积分的计算_第21页.png

## ② 求最简式的不定积分
$\star \int \frac{A}{ax+b} dx$，方法：凑微分，把分子凑为分母的导数。
例：计算$\int \frac{3}{2x+1} dx$，其中$(2x+1)'=2$
$$
\begin{align*}
\int \frac{3}{2x+1} dx &= \frac{3}{2}\int \frac{2}{2x+1} dx \\
&= \frac{3}{2}\int \frac{1}{2x+1} d(2x+1) \quad \text{凑微分} \\
&= \frac{3}{2}\ln|2x+1| + C
\end{align*}
$$
$\star \int \frac{A}{(ax+b)^k} dx$
例：计算$\int \frac{3}{(2x-1)^2} dx$，其中$(2x-1)'=2$
$$
\begin{align*}
\int \frac{3}{(2x-1)^2} dx &= \frac{3}{2}\int \frac{2}{(2x-1)^2} dx \\
&= \frac{3}{2}\int \frac{1}{(2x-1)^2} d(2x-1) \\
&= -\frac{3}{2} \cdot \frac{1}{2x-1} + C
\end{align*}
$$
$\star \int \frac{Ax+B}{px^2+qx+r} dx \quad (q^2-4pr < 0)$
方法：凑微分，构造$\int f[g(x)]\cdot g'(x)dx$的形式，把分子凑为分母的导数。
例：计算$\int \frac{3x-2}{x^2+1} dx$，其中$(x^2+1)'=2x = g'(x)$
$$
\int \frac{3x-2}{x^2+1} dx = \int \frac{3x}{x^2+1} dx - \int \frac{2}{x^2+1} dx
$$

---

# L 积分的计算_第22页.png

## 二次不可约因式幂次的不定积分
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

在例9.5中有说过，分部积分可造出方程，这里我们用分部积分法造出递推式。

e.g. $\displaystyle \int \frac{1}{(1+x^2)^2} \, dx$

$\because k=2$
$\therefore$ 设$I_2 = \int \frac{1}{(1+x^2)^2} \, dx$，$I_2$不好解
则$I_1 = \int \frac{1}{1+x^2} \, dx$，$I_1$好解

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

---

# L 积分的计算_第23页.png

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

## 例9.8
求$\int \frac{4x^2-6x-1}{(x+1)(2x-1)^2} dx$

**分析**：这是一个真分式
我们直接把其分解为最简式
然后对最简式求积分

看到$Q_m(x)$中出现了$(x+1)$与$(2x-1)^2$，则$\frac{P_n(x)}{Q_m(x)}$一定可以分解为：
$$\frac{A}{x+1} + \frac{B}{2x-1} + \frac{C}{(2x-1)^2} = \frac{4x^2-6x-1}{(x+1)(2x-1)^2}$$

$$4x^2-6x-1 = A(2x-1)^2 + B(2x-1)(x+1) + C(x+1)$$

两种解法。

---

# L 积分的计算_第24页.png

## 解法①：直接硬算
$$=(2A+B)2x^2-(4A-B-C)x+A-B+C$$
$$\Rightarrow \begin{cases}
2A+B=2 \\
4A-B-C=6 \\
A-B+C=-1
\end{cases}$$
解出
$$\begin{cases}
A=1 \\
B=0 \\
C=-2
\end{cases}$$

## 解法②：恒等式赋值法
因为是恒等式，$x$可以代任何值，我们可以代入$x$值，把$A,B,C$这3个量中的2个消去。
若令$x=\frac{1}{2}$，则只剩$C$：
$$-3 = C\cdot \frac{3}{2},\quad C=-2$$
若令$x=-1$，则$B,C$消去：
$$9=9A,\quad A=1$$
带$x^2$的项很好找，等号左边为$4x^2$，右边为$4Ax^2+2Bx^2$，则：
$$4x^2=4Ax^2+2Bx^2$$
将$A=1$代入，解出$B=0$
$$\Rightarrow A=1,\,B=0,\,C=-2$$

解：
$$
\begin{align*}
\text{原式} &= \int \frac{1}{x+1}\,\mathrm{d}x + \int \frac{-2}{(2x-1)^2}\,\mathrm{d}x \\
&= \int \frac{1}{x+1}\,\mathrm{d}(x+1) - \int \frac{1}{(2x-1)^2}\,\mathrm{d}(2x-1) \\
&= \ln|x+1| + \frac{1}{2x-1} + C
\end{align*}
$$

## 例9.9
求 $\displaystyle\int \frac{x}{x^2+x-1}\,\mathrm{d}x$

【分析】先化为最简式，再对最简式求不定积分。

---

# L 积分的计算_第25页.png

解：
$$
\begin{align*}
\text{原式}&=\int \frac{x}{x^2(x-1)+x-1}\,dx\\
&=\int \frac{x}{(x^2+1)(x-1)}\,dx
\end{align*}
$$

此时一定有：
$$\frac{A}{x-1} + \frac{Bx+C}{x^2+1} = \frac{x}{(x^2+1)(x-1)}$$
通分后两边分子恒等：
$$x = A(x^2+1) + (Bx+C)(x-1)$$

求解系数：
- 若令$x=1$，则$B,C$消去：
  $1=2A\ ,\ A=\frac{1}{2}$
- 若令$x=0$，$B$消去，且已知$A=\frac{1}{2}$：
  $0 = A - C\ ,\ C=\frac{1}{2}$
- 带$x^2$的项很好找，且最后我们是不要$x^2$项的，即$x^2$的系数为$0$；
  带$x^2$的项有$Ax^2,\ Bx^2$，因此：
  $0 = A + B \implies B=-\frac{1}{2}$

最终得$A=\frac{1}{2}\ ,\ B=-\frac{1}{2}\ ,\ C=\frac{1}{2}$。

将系数代入拆分并计算积分：
$$
\begin{align*}
&=\int \frac{\frac{1}{2}}{x-1}\,dx + \int \frac{-\frac{1}{2}x+\frac{1}{2}}{x^2+1}\,dx\\
&=\frac{1}{2}\int \frac{1}{x-1}\,dx - \frac{1}{2}\int \frac{x-1}{x^2+1}\,dx \quad \left( (x^2+1)'=2x \right)\\
&=\frac{1}{2}\int \frac{1}{x-1}\,d(x-1) - \frac{1}{4}\int \frac{2x}{x^2+1}\,dx + \frac{1}{2}\int \frac{1}{x^2+1}\,dx\\
&=\frac{1}{2}\int \frac{1}{x-1}\,d(x-1) - \frac{1}{4}\int \frac{1}{x^2+1}\,d(x^2+1) + \frac{1}{2}\int \frac{1}{x^2+1}\,dx\\
&=\frac{1}{2}\ln|x-1| - \frac{1}{4}\ln(x^2+1) + \frac{1}{2}\arctan x + C
\end{align*}
$$

## 例9.10
求不定积分：
$$\int \frac{2x+3}{x^2-x+1}\,dx$$

---

# L 积分的计算_第26页.png

## 分析
被积式为$\frac{Ax+B}{px^2+qx+r}$的形式，
且二次分母的判别式满足$q^2-4pr = 1-4<0$，
分母多项式$Q_m(x)$在实数域内没法再分解，
因此该式已是最简积分形式，可直接计算积分。

计算用到的基本积分公式：
$$\int \frac{1}{x^2+a^2} \, dx = \frac{1}{a}\arctan\frac{x}{a} + C$$

## 解答
注：分母求导得$(x^2-x+1)' = 2x-1$，将分子拆分为分母导数与常数之和，拆分积分计算：
$$
\begin{align*}
\text{原式} &= \int \frac{2x-1+4}{x^2-x+1} \, dx \\
&= \int \frac{2x-1}{x^2-x+1} \, dx + 4\int \frac{1}{x^2-x+1} \, dx \\
&= \int \frac{2x-1}{x^2-x+1} \, dx + 4\int \frac{1}{\left(x-\frac{1}{2}\right)^2 + \frac{3}{4}} \, dx \\
&= \int \frac{1}{x^2-x+1} \, d(x^2-x+1) + 4\int \frac{1}{\left(x-\frac{1}{2}\right)^2 + \left(\frac{\sqrt{3}}{2}\right)^2} \, d\left(x-\frac{1}{2}\right) \\
&= \ln|x^2-x+1| + 4\cdot \frac{2\sqrt{3}}{3}\arctan\frac{x-\frac{1}{2}}{\frac{\sqrt{3}}{2}} + C
\end{align*}
$$

---

# L 积分的计算_第27页.png

## 定积分的积分法
虽然，从概念上来说，不定积分与定积分是完全不一样的，但从计算上来说，两者的关系是紧密的。

## 牛顿——莱布尼茨公式，及其推广
设函数$F(x)$是连续函数$f(x)$在$[a,b]$上的一个原函数，则
$$\int_{a}^{b} f(x) \, dx = F(x)\bigg|_{a}^{b} = F(b) - F(a)$$
$$\int f(x) \, dx = F(x) + C$$

证明：
∵ 闭区间上的连续函数必有原函数
∴ 设$G(x) = \int f(t) \, dt = \int_{a}^{x} f(t) \, dt,\quad x\in[a,b]$

则$G(a) = 0$
$$G(b) = \int_{a}^{b} f(t) \, dt = G(b) - G(a)$$

∵ $F(x)$为$f(x)$的一个原函数
∴ $F(x) = \int f(t) \, dt$，即$F'(x) = f(x)$

∴ $F(x) - G(x) = C$
即$G(x) = F(x) + C$

$$
\begin{aligned}
\therefore \int_{a}^{b} f(t) \, dt &= G(b) - G(a) \\
&= \left[F(b) + C\right] - \left[F(a) + C\right] \\
&= F(b) - F(a)
\end{aligned}
$$

---

# L 积分的计算_第28页.png

## 注：牛顿-莱布尼茨公式推广
(1) 若$f(x)$在$x\in[a,b]$上有原函数$F(x)$，则
$$\int_a^b f(x)dx = F(b) - F(a)$$
(2) 若$f(x)$在$[a,b]$上分段有原函数，$x=c$为断点：
如$[a,c)$上有原函数$F_1(x)$，$(c,b]$上有原函数$F_2(x)$，则
$$
\begin{align*}
\int_a^b f(x)dx &= \int_a^c f(x)dx + \int_c^b f(x)dx \\
&= F_1(c-0) - F_1(a) + F_2(b) - F_2(c+0)
\end{align*}
$$
$\because x=c$点取不到，$\therefore$ 取$x\to c$时$F(x)$的极限值：
- $F_1(c-0)$为$F_1(x)\to F_1(c)$的左极限值
- $F_2(c+0)$为$F_2(x)\to F_2(c)$的右极限值
见习题页9.10。
- 若$F_1(c-0), F_2(c+0)$存在，则$\int_a^b f(x)dx$收敛，即$\int_a^b f(x)dx$存在；
- 若$F_1(c-0), F_2(c+0)$至少有一个不存在，则$\int_a^b f(x)dx$发散，即$\int_a^b f(x)dx$不存在。
## 例9.11
设$f\left(x+\frac{1}{x}\right)=\frac{x+x^3}{x^4+1}$，则$\int_{2}^{2\sqrt{2}} f(x)dx = \underline{\quad\quad}$
【分析】求出$f(x) \longrightarrow F(x) \longrightarrow \int_{2}^{2\sqrt{2}} f(x)dx$
解：
$$
\begin{align*}
f\left(x+\frac{1}{x}\right) &= \frac{\frac{x+x^3}{x^2}}{\frac{1+x^4}{x^2}} = \frac{x+\frac{1}{x}}{x^2+\frac{1}{x^2}} \\
&= \frac{x+\frac{1}{x}}{\left(x+\frac{1}{x}\right)^2 - 2\cdot x\cdot \frac{1}{x}}
\end{align*}
$$
（利用完全平方公式：$(a+b)^2=a^2+b^2+2ab$）

---

# L 积分的计算_第29页.png

令$t = x+\frac{1}{x}$，即$f(x)=\frac{x}{x^2-2}$

$$
\begin{align*}
F(x)&=\int f(x)dx=\int \frac{x}{x^2-2}dx\\
&=\frac{1}{2}\int \frac{2x}{x^2-2}dx \quad (x^2-2)'=2x\\
&=\frac{1}{2}\int \frac{1}{x^2-2}d(x^2-2)\\
&=\frac{1}{2}\ln(x^2-2)
\end{align*}
$$

$$
\begin{align*}
\int_{2}^{2\sqrt{2}} f(x)dx &= F(2\sqrt{2}) - F(2)\\
&=\frac{1}{2}\ln6 - \frac{1}{2}\ln2\\
&=\frac{1}{2}\ln3
\end{align*}
$$

## 例9.10
求定积分$\int_{0}^{\frac{3\pi}{4}} \frac{1}{1+\cos^2 x}dx$

**分析**：求解路径为$f(x)\to \int f(x)dx \to \int_{0}^{\frac{3\pi}{4}}f(x)dx$

解：先求原函数$F(x)=\int \frac{1}{1+\cos^2 x}dx$
$$
\begin{align*}
F(x)&=\int \frac{1}{1+\cos^2 x}dx\\
&=\int \frac{1}{1+\frac{1}{\sec^2 x}}dx \quad \cos x=\frac{1}{\sec x}\\
&=\int \frac{\sec^2 x}{\sec^2 x +1}dx \quad \begin{aligned}
\sec^2 x&=\tan^2 x+1\\
\sec^2 x&=(\tan x)'
\end{aligned}\\
&=\int \frac{(\tan x)'}{\tan^2 x +2}\\
&=\int \frac{1}{\tan^2 x + (\sqrt{2})^2}d(\tan x) \quad \text{参考积分公式 } \int \frac{1}{a^2+x^2}dx\\
&=\frac{1}{\sqrt{2}}\arctan \frac{\tan x}{\sqrt{2}} + C = \frac{1}{a}\arctan\frac{x}{a}+C \quad (a>0)
\end{align*}
$$

---

# L 积分的计算_第30页.png

## 牛顿-莱布尼茨公式应用易错点
### 错误计算过程
$$\int_{0}^{\frac{3\pi}{4}} \frac{1}{1+\cos^2 x} dx = F\left(\frac{3\pi}{4}\right) - F(0)$$
$$= \frac{1}{\sqrt{2}} \arctan \frac{-1}{\sqrt{2}} < 0$$
$$\because \int_{0}^{\frac{3\pi}{4}} \frac{1}{1+\cos^2 x} dx > 0$$
∴ 不符题意，结果是错的

### 错误根源分析
$\because F(x)$要在$x\in\left[0,\frac{3\pi}{4}\right]$上处处可导
才能有$F'(x)=f(x),\ x\in\left[0,\frac{3\pi}{4}\right]$
才称$F(x)$为$f(x)$在$x\in\left[0,\frac{3\pi}{4}\right]$上的原函数
但$F(x)$在$x=\frac{\pi}{2}$处为一个无意义的断点，为一个不可导点
$\therefore F(x)=\frac{1}{\sqrt{2}}\arctan \frac{\tan x}{\sqrt{2}}$并不是
$f(x)=\frac{1}{1+\cos^2 x}$在$x\in\left[0,\frac{3\pi}{4}\right]$上的原函数

### 正确求解过程
把$\left[0,\frac{3\pi}{4}\right]$拆成$\left[0,\frac{\pi}{2}\right) \cup \left(\frac{\pi}{2},\frac{3\pi}{4}\right]$
则$F(x)$为$f(x)$在$x\in\left[0,\frac{\pi}{2}\right) \cup \left(\frac{\pi}{2},\frac{3\pi}{4}\right]$上的原函数
$$
\begin{aligned}
\int_{0}^{\frac{3\pi}{4}} \frac{1}{1+\cos^2 x} dx
&= \int_{0}^{\frac{\pi}{2}} \frac{1}{1+\cos^2 x} dx + \int_{\frac{\pi}{2}}^{\frac{3\pi}{4}} \frac{1}{1+\cos^2 x} dx \\
&= \left[\lim_{x \to (\frac{\pi}{2})^-} F(x) - F(0)\right] + \left[F\left(\frac{3\pi}{4}\right) - \lim_{x \to (\frac{\pi}{2})^+} F(x)\right] \\
&= \frac{1}{\sqrt{2}} \cdot \frac{\pi}{2} - 0 + \frac{1}{\sqrt{2}} \arctan \frac{-1}{\sqrt{2}} - \frac{1}{\sqrt{2}} \cdot \left(-\frac{\pi}{2}\right) \\
&= \frac{\pi}{\sqrt{2}} - \frac{1}{\sqrt{2}} \arctan \frac{1}{\sqrt{2}}
\end{aligned}
$$

---

# L 积分的计算_第31页.png

## 例13
已知$\frac{1}{1+e^{\frac{1}{x}}}$是$f(x)$的一个原函数，则$f(x)$在$[-1,1]$上的平均值为$\underline{\qquad}$
### 分析
由原函数的定义：
$$\left( \frac{1}{1+e^{\frac{1}{x}}} \right)' = f(x)$$
$\because \frac{1}{1+e^{\frac{1}{x}}}$在$x=0$处不可导，$\therefore$ 默认$x \neq 0$。
函数在区间$[a,b]$上的平均值定义为：
$$\bar{f} = \frac{\int_{a}^{b} f(x) dx}{b-a}$$
对本题区间$[-1,1]$，即：
$$\bar{f} = \frac{\int_{-1}^{1} f(x) dx}{1-(-1)}$$
可知$\bar{f}=f(\xi),\ \xi \in (-1,1)$。
$\because$ 若$f(x)$连续，则由积分中值定理：
$$\exists \xi \in (a,b),\text{使} \int_{a}^{b} f(x) dx = f(\xi)(b-a)$$
因此：
$$f(\xi) = \frac{\int_{a}^{b} f(x) dx}{b-a} = \frac{\int_{-1}^{1} f(x) dx}{1-(-1)} = \bar{f}$$
### 解答
解：
$$
\begin{align*}
\bar{f} &= \frac{\int_{-1}^{1} f(x) dx}{1-(-1)} = \frac{1}{2}\int_{-1}^{1} f(x) dx \\
&= \frac{1}{2}\int_{-1}^{1} \left( \frac{1}{1+e^{\frac{1}{x}}} \right)' dx
\end{align*}
$$
$\because F(x)=\frac{1}{1+e^{\frac{1}{x}}}$在$x=0$处不可导，
$\therefore$ 拆分积分计算：
$$
\begin{align*}
\bar{f} &= \frac{1}{2}\int_{-1}^{0} \left( \frac{1}{1+e^{\frac{1}{x}}} \right)' dx + \frac{1}{2}\int_{0}^{1} \left( \frac{1}{1+e^{\frac{1}{x}}} \right)' dx \\
&= \frac{1}{2}\left[ \lim_{x \to 0^-} F(x) - F(-1) \right] + \frac{1}{2}\left[ F(1) - \lim_{x \to 0^+} F(x) \right] \\
&= \frac{1}{2}\left(1 - \frac{1}{1+e^{-1}}\right) + \frac{1}{2}\left( \frac{1}{1+e} - 0 \right) \\
&= \frac{1}{e+1}
\end{align*}
$$

---

# L 积分的计算_第32页.png

由牛顿-莱布尼茨公式，结合不定积分的计算方法，我们就可以把不定积分的换元积分法和分部积分法继承过来。

## 定积分的换元积分法
设$f(x)$在$[a,b]$上连续，函数$x=g(t)$满足：
① $g(\alpha)=a$，$g(\beta)=b$；
② $x=g(t)$在$t\in[\alpha,\beta]$（或$t\in[\beta,\alpha]$）上有连续的导数，且其值域为$x\in[a,b]$。

则有定积分换元公式：
$$
\begin{aligned}
\int_a^b f(x) \, \mathrm{d}x
&= \int_{\alpha}^{\beta} f[g(t)] \, \mathrm{d}[g(t)] \\
&= \int_{\alpha}^{\beta} f[g(t)] g'(t) \, \mathrm{d}t
\end{aligned}
$$

对积分$\int_a^b f(x) \, \mathrm{d}x$，令$x=g(t)$，这时自变量由$x$换成了$t$，积分上下限也会对应改变：
- 对原下限$x=a$，代入换元式得$a=g(t)$，解出对应的$t=\alpha$作为新的积分下限；
- 对原上限$x=b$，代入换元式得$b=g(t)$，解出对应的$t=\beta$作为新的积分上限。

（配有两幅函数示意图：分别为横轴$x$、纵轴$f(x)$的函数图像，横轴$t$、纵轴$f[g(t)]g'(t)$的函数图像）

## 定积分的分部积分法
要求$u'(x), v'(x)$在$[a,b]$上连续。

分部积分公式推导：
$$
\begin{aligned}
\int_a^b u(x) \, \mathrm{d}[v(x)]
&= \int_a^b u(x) v'(x) \, \mathrm{d}x \\
&= \left. u(x)v(x) \right|_a^b - \int_a^b v(x) u'(x) \, \mathrm{d}x \\
&= \left. u(x)v(x) \right|_a^b - \int_a^b v(x) \, \mathrm{d}[u(x)]
\end{aligned}
$$

> 注：在计算定积分时，下面这些结论是很有用的。

---

# L 积分的计算_第33页.png

## 对称区间连续偶函数定积分性质
设$f(x)$为连续的偶函数，则
$$\int_{-a}^{a} f(x) \, \mathrm{d}x = 2\int_{0}^{a} f(x) \, \mathrm{d}x$$
（对应偶函数积分几何意义示意图，记忆口诀：偶倍）

## 对称区间连续奇函数定积分性质
设$f(x)$为连续的奇函数，则
$$\int_{-a}^{a} f(x) \, \mathrm{d}x = 0$$
（对应奇函数积分几何意义示意图，记忆口诀：奇零）

## 连续周期函数定积分性质
设$f(x)$是以$T$为周期的连续函数，则对任意的实数$a$，都有
$$\int_{a}^{a+T} f(x) \, \mathrm{d}x = \int_{0}^{T} f(x) \, \mathrm{d}x$$
（对应周期函数积分几何意义示意图，示例取周期$T=2$）

代入$a=1, T=2$得：
$$\int_{1}^{1+2} f(x) \, \mathrm{d}x = \int_{0}^{2} f(x) \, \mathrm{d}x = \int_{2}^{4} f(x) \, \mathrm{d}x$$

即在长度为一个周期的区间上的定积分，与该区间的起点位置无关。
证明见例9.16。

---

# L 积分的计算_第34页.png

## (4) 区间再现公式
设$f(x)$为连续函数，则
$$\int_{a}^{b} f(x) dx = \int_{a}^{b} f(a+b-x) dx$$

**证明：**
考虑定积分
$$\int_{a}^{b} f(x) dx$$
做换元$x=a+b-t$：
- 当$x=a$时，代入得$a=a+b-t$，解得$t=b$；
- 当$x=b$时，代入得$b=a+b-t$，解得$t=a$；
- 微分关系：$dx=-dt$，且$f(x)=f(a+b-t)$。

将换元关系代入积分：
$$
\begin{align*}
\int_{a}^{b} f(x) dx &= \int_{b}^{a} f(a+b-t) (-dt) \\
&= \int_{a}^{b} f(a+b-t) dt \\
&= \int_{a}^{b} f(a+b-x) dx
\end{align*}
$$

### 适用场景
用于$f(x)$形式复杂，但构造的$g(x)=f(x)+f(a+b-x)$形式简单的情形，此时有：
$$\int_{a}^{b} f(x) dx = \frac{1}{2}\int_{a}^{b} g(x) dx$$

### 例题
计算定积分：
$$\int_{0}^{\frac{\pi}{4}} \ln(1+\tan x) dx$$

由区间再现公式：
$$\int_{0}^{\frac{\pi}{4}} \ln(1+\tan x) dx = \int_{0}^{\frac{\pi}{4}} \ln\left[1+\tan\left(\frac{\pi}{4}-x\right)\right] dx$$
由正切差角公式：
$$\tan\left(\frac{\pi}{4}-x\right) = \frac{\tan\frac{\pi}{4}-\tan x}{1+\tan\frac{\pi}{4}\tan x} = \frac{1-\tan x}{1+\tan x}$$
代回被积函数化简：
$$
\begin{align*}
\int_{0}^{\frac{\pi}{4}} \ln(1+\tan x) dx &= \int_{0}^{\frac{\pi}{4}} \ln\left(1+\frac{1-\tan x}{1+\tan x}\right) dx \\
&= \int_{0}^{\frac{\pi}{4}} \ln\left( \frac{2}{1+\tan x} \right) dx
\end{align*}
$$

---

# L 积分的计算_第35页.png

$$= \int_{0}^{\frac{\pi}{4}} \left[ \ln2 - \ln(1+\tan x) \right] dx$$

$$\int_{a}^{b} f(x) dx = \frac{1}{2} \int_{a}^{b} \left[ f(x) + f(a+b-x) \right] dx$$

$$\Rightarrow \int_{0}^{\frac{\pi}{4}} \ln(1+\tan x) dx$$
$$
\begin{aligned}
&= \frac{1}{2} \int_{0}^{\frac{\pi}{4}} \left[ \ln(1+\tan x) + \ln2 - \ln(1+\tan x) \right] dx \\
&= \frac{1}{2} \int_{0}^{\frac{\pi}{4}} \ln2 \, dx \\
&= \frac{1}{2} \cdot \ln2 \cdot \frac{\pi}{4} \\
&= \frac{\pi}{8} \ln2
\end{aligned}
$$

## 华里士公式
(5), (6), (7)叫华里士公式，可快速计算某些特殊的定积分。

(5)
$$\int_{0}^{\frac{\pi}{2}} \sin^n x dx = \int_{0}^{\frac{\pi}{2}} \cos^n x dx$$
$$
=
\begin{cases}
\displaystyle \frac{n-1}{n} \cdot \frac{n-3}{n-2} \cdot \dots \cdot \frac{2}{3} \cdot 1, & n为大于1的奇数 \\[6pt]
\displaystyle \frac{n-1}{n} \cdot \frac{n-3}{n-2} \cdot \dots \cdot \frac{1}{2} \cdot \frac{\pi}{2}, & n为正偶数
\end{cases}
$$

eg:
$$\int_{0}^{\frac{\pi}{2}} \sin^{10} x dx = \frac{9}{10} \cdot \frac{7}{8} \cdot \frac{5}{6} \cdot \frac{3}{4} \cdot \frac{1}{2} \cdot \frac{\pi}{2}$$

$$\int_{0}^{\frac{\pi}{2}} \sin^{9} x dx = \frac{8}{9} \cdot \frac{6}{7} \cdot \frac{4}{5} \cdot \frac{2}{3}$$

$$\int_{0}^{\frac{\pi}{2}} \sin^2 x \cos^2 x dx$$
$$= \int_{0}^{\frac{\pi}{2}} \sin^2 x (1-\sin^2 x) dx$$

---

# L 积分的计算_第36页.png

$$
\begin{aligned}
&= \int_{0}^{\frac{\pi}{2}} \sin^2 x \, dx - \int_{0}^{\frac{\pi}{2}} \sin^4 x \, dx \\
&= \frac{1}{2} \cdot \frac{\pi}{2} - \frac{3}{4} \cdot \frac{1}{2} \cdot \frac{\pi}{2} \\
&= \frac{1}{4} \cdot \frac{\pi}{4} \\
&= \frac{\pi}{16}
\end{aligned}
$$

## (6) 区间$[0,\pi]$上的三角函数幂积分公式
$$
\int_{0}^{\pi} \sin^n x \, dx =
\begin{cases}
2 \cdot \frac{n-1}{n} \cdot \frac{n-3}{n-2} \cdot \cdots \cdot \frac{2}{3} \cdot 1, & n\text{为大于1的奇数} \\
2 \cdot \frac{n-1}{n} \cdot \frac{n-3}{n-2} \cdot \cdots \cdot \frac{1}{2} \cdot \frac{\pi}{2}, & n\text{为正偶数}
\end{cases}
$$

$$
\int_{0}^{\pi} \cos^n x \, dx =
\begin{cases}
0, & n\text{为正奇数} \\
2 \cdot \frac{n-1}{n} \cdot \frac{n-3}{n-2} \cdot \cdots \cdot \frac{1}{2} \cdot \frac{\pi}{2}, & n\text{为正偶数}
\end{cases}
$$

## (7) 区间$[0,2\pi]$上的三角函数幂积分公式
$$
\int_{0}^{2\pi} \cos^n x \, dx = \int_{0}^{2\pi} \sin^n x \, dx =
\begin{cases}
0, & n\text{为正奇数} \\
4 \cdot \frac{n-1}{n} \cdot \frac{n-3}{n-2} \cdot \cdots \cdot \frac{1}{2} \cdot \frac{\pi}{2}, & n\text{为正偶数}
\end{cases}
$$

## 例9.13 计算定积分$\int_{-1}^{1} x^2 \sqrt{1-x^2} \, dx$
$\because x^2\sqrt{1-x^2}$为偶函数，
$$
\therefore \int_{-1}^{1} x^2 \sqrt{1-x^2} \, dx = 2\int_{0}^{1} x^2 \sqrt{1-x^2} \, dx
$$

见到$\sqrt{1-x^2}$为$\sqrt{a^2-x^2}$的形式，考虑用换元法：
令$x = \sin t$，则$dx = \cos t \, dt$。

变换积分上下限：
当$x=1$时，$\sin t = 1$，得$t = \frac{\pi}{2}$；
当$x=0$时，$\sin t = 0$，得$t = 0$。

---

# L 积分的计算_第37页.png

$$= 2\int_{0}^{\frac{\pi}{2}} \sin^2 t \sqrt{1-\sin^2 t} \cdot \cos t \, dt$$
利用$1-\sin^2 t = \cos^2 t$化简得：
$$= 2\int_{0}^{\frac{\pi}{2}} \sin^2 t \cos^2 t \, dt$$
考虑使用华里士公式计算，展开被积函数：
$$= 2\int_{0}^{\frac{\pi}{2}} \sin^2 t (1-\sin^2 t) \, dt$$
拆分为两个定积分：
$$= 2\int_{0}^{\frac{\pi}{2}} \sin^2 t \, dt - 2\int_{0}^{\frac{\pi}{2}} \sin^4 t \, dt$$
代入华里士公式计算：
$$= 2\left( \frac{1}{2} \cdot \frac{\pi}{2} - \frac{3}{4} \cdot \frac{1}{2} \cdot \frac{\pi}{2} \right)$$
$$= \frac{\pi}{8}$$
「注」从原则上讲，作变换$x=\sin t$后，因为$\sin t$为周期函数，所以可合理地变换上下限：当$x=0$时，可取$t=0,\pm\pi,\pm2\pi,\cdots$；当$x=1$时，可取$t=\frac{\pi}{2},\frac{\pi}{2}\pm2\pi,\cdots$。上下限有多种组合，可满足华里士定理的使用条件。
被积函数中$\sqrt{1-x^2} = \sqrt{1-\sin^2 t} = |\cos t|$。
尽量不要出现绝对值，因为有时去绝对值很麻烦。
## 例9.14
$$\int_{0}^{1} \arcsin\sqrt{1-x^2} \, dx = \underline{\qquad}$$
### 解法1：
【分析】因为被积函数含有$\sqrt{a^2-x^2}$形式的$\sqrt{1-x^2}$，因此考虑使用换元法。
可令$x=\sin t$去掉根号：
$$\sqrt{1-x^2} = \sqrt{1-\sin^2 t} = \cos t$$
原式$= \arcsin \cos t$。
但若令$x=\cos t$，也可以去掉根号：
$$\sqrt{1-x^2} = \sqrt{1-\cos^2 t} = \sin t$$
原式$= \arcsin \sin t$，这样正好可以抵消反函数。

---

# L 积分的计算_第38页.png

## 解法1（三角换元+分部积分法）
解：令$x=\cos t$
则$dx = -\sin t \, dt$，化简根式：
$$\sqrt{1-\cos^2 t} = \sqrt{\sin^2 t} = \sin t$$
确定换元积分限：
- 当$x=1$时，$\cos t=1$，对应$t=0$
- 当$x=0$时，$\cos t=0$，对应$t=\frac{\pi}{2}$

代入定积分换元：
$$
\begin{align*}
\text{原式} &= \int_{\frac{\pi}{2}}^{0} \arcsin(\sin t) \cdot (-\sin t) dt \\
&= \int_{0}^{\frac{\pi}{2}} t\sin t \, dt
\end{align*}
$$
被积函数为两个函数乘积的形式，考虑使用分部积分法：选取$t$作为求导项，$\sin t$作为积分项，分部积分对应关系如下：
1.  求导列：$t$一阶求导得$1$，二阶求导得$0$
2.  积分列：$\sin t$一阶积分得$-\cos t$，二阶积分得$-\sin t$

计算分部积分结果：
$$
\begin{align*}
\int_{0}^{\frac{\pi}{2}} t\sin t \, dt &= -t\cos t\bigg|_0^{\frac{\pi}{2}} + \sin t\bigg|_0^{\frac{\pi}{2}} + \int_{0}^{\frac{\pi}{2}} 0\cdot(-\sin t)dt \\
&= 1
\end{align*}
$$

## 解法2（分部积分+凑微分法）
【分析】选取$\arcsin\sqrt{1-x^2}$作为求导项，$1$作为积分项。
对$\arcsin\sqrt{1-x^2}$求导得：
$$\frac{1}{\sqrt{1-(1-x^2)}} \cdot \frac{-2x}{2\sqrt{1-x^2}}$$
对$1$积分得$x$。

解：代入分部积分公式：
$$
\begin{align*}
\text{原式} &= x\arcsin\sqrt{1-x^2}\bigg|_0^1 - \int_{0}^{1} x\cdot \frac{1}{\sqrt{1-(1-x^2)}} \cdot \frac{-2x}{2\sqrt{1-x^2}} dx \\
&= \int_{0}^{1} \frac{x}{\sqrt{1-x^2}} dx
\end{align*}
$$
该积分可考虑用凑微分法计算。

---

# L 积分的计算_第39页.png

$$
\begin{align*}
&= -\frac{1}{2}\int_{0}^{1} \frac{-2x}{\sqrt{1-x^2}} \, dx \\
&= -\frac{1}{2}\int_{0}^{1} \frac{1}{\sqrt{1-x^2}} \, d(-x^2+1) = -\frac{1}{2}F(x)\big|_{0}^{1} \\
&= -\frac{1}{2} \cdot 2\sqrt{1-x^2}\big|_{0}^{1} \\
&= 1
\end{align*}
$$

## 例9.15
计算定积分：
$$\int_{0}^{1} x \arcsin\sqrt{4x-4x^2} \, dx$$

**分析**：见到$\sqrt{ax^2+bx+c}$的形式，考虑将其凑成$\sqrt{k^2+\varphi^2(x)}$、$\sqrt{k^2-\varphi^2(x)}$或$\sqrt{\varphi^2(x)-k^2}$的形式，再使用换元法求解。

解：先对根号内的二次式配方变形：
$$
\begin{align*}
\text{原式} &= \int_{0}^{1} x\arcsin\sqrt{1-(-4x+4x^2+1)} \, dx \\
&= \int_{0}^{1} x\arcsin\sqrt{1^2-(1-2x)^2} \, dx
\end{align*}
$$
该式的根号部分为$\sqrt{a^2-x^2}$的形式，后续既可以参照例9.14的思路求解，也可以按如下换元方法计算：

令 $1-2x = t$，则：
$$x = \frac{1-t}{2}, \quad dx = -\frac{1}{2}dt$$
更换积分上下限：
- 当$x=1$时，代入$x=\frac{1-t}{2}$得$1=\frac{1-t}{2}$，解得$t=-1$；
- 当$x=0$时，代入$x=\frac{1-t}{2}$得$0=\frac{1-t}{2}$，解得$t=1$。

将换元关系代入原积分，整理得：
$$
\begin{align*}
&= \int_{1}^{-1} \frac{1-t}{2} \cdot \arcsin\sqrt{1-t^2} \cdot \left(-\frac{1}{2}\right) dt \\
&= \frac{1}{4}\int_{-1}^{1} (1-t)\arcsin\sqrt{1-t^2} \, dt
\end{align*}
$$

---

# L 积分的计算_第40页.png

展开，拆开
$$=\frac{1}{4}\int_{-1}^{1} \arcsin\sqrt{1-t^2}\,dt + \frac{1}{4}\int_{-1}^{1} (-t)\arcsin\sqrt{1-t^2}\,dt$$
∵ 都是对称区间
且$f_1(t)=\arcsin\sqrt{1-t^2}$为偶函数
$f_2(t)=(-t)\arcsin\sqrt{1-t^2}$为奇函数
$$\therefore = 2\cdot \frac{1}{4}\int_{0}^{1} \arcsin\sqrt{1-t^2}\,dt + 0$$
$$= \frac{1}{2}\int_{0}^{1} \arcsin\sqrt{1-t^2}\,dt$$
发现这与例9.14的一模一样（只乘了个$\frac{1}{2}$）
∴ 由例9.14得
$$=\frac{1}{2}$$

## 例9.16（一个结论的证明）
【分析】由积分的可拆性
$$\Rightarrow \int_{a}^{a+T} f(x)\,dx = \int_{a}^{0} f(x)\,dx + \int_{0}^{T} f(x)\,dx + \int_{T}^{a+T} f(x)\,dx$$
若证出 $\int_{a}^{0} f(x)\,dx + \int_{T}^{a+T} f(x)\,dx = 0$
则得证 $\int_{a}^{a+T} f(x)\,dx = \int_{0}^{T} f(x)\,dx$

解：$\int_{T}^{a+T} f(x)\,dx$
想让图像在$x$轴上向左平移$\Delta x = T$
令$x_1 = x - T$
则$x = x_1 + T$
$a+T = x_1 + T,\ x_1 = a$
$T = x_1 + T,\ x_1 = 0$
$$= \int_{0}^{a} f(x_1+T)\,dx_1$$

---

# L 积分的计算_第41页.png

## 周期函数的积分性质
$\because f(x)$是以$T$为周期的连续函数
$\therefore f(x_1+T)=f(x_1)$
$$
\begin{align*}
\int_{T}^{a+T} f(x_1)\mathrm{d}x_1 &= \int_{0}^{a}f(x_1)\mathrm{d}x_1 \\
&= \int_{0}^{a}f(x)\mathrm{d}x \\
&= -\int_{a}^{0}f(x)\mathrm{d}x
\end{align*}
$$
即
$$\int_{T}^{a+T}f(x)\mathrm{d}x = -\int_{a}^{0}f(x)\mathrm{d}x$$
则
$$\int_{a}^{a+T}f(x)\mathrm{d}x = \int_{0}^{T}f(x)\mathrm{d}x$$

## 例9.18 一个结论的证明
方法：换元法，也可以建立方程求解。
设$f(x)$在$[0,1]$上连续，证明：
$$\int_{0}^{\pi}xf(\sin x)\mathrm{d}x = \frac{\pi}{2}\int_{0}^{\pi}f(\sin x)\mathrm{d}x$$
并计算：
$$\int_{0}^{\pi}x\sin^9 x \mathrm{d}x$$

**分析**：积分区间为$[0,\pi]$，被积函数含有$\sin x$，可通过区间再现法利用诱导公式推导。

证明：
$$
\begin{align*}
\int_{0}^{\pi}xf(\sin x)\mathrm{d}x &= \int_{0}^{\pi}(\pi-x)f\left[\sin(\pi-x)\right]\mathrm{d}x \\
&= \int_{0}^{\pi}(\pi-x)f(\sin x)\mathrm{d}x \\
&= \int_{0}^{\pi}\pi f(\sin x)\mathrm{d}x - \int_{0}^{\pi}xf(\sin x)\mathrm{d}x
\end{align*}
$$
发现上述等式构成关于所求积分的方程，因此：
$$
\begin{align*}
\Rightarrow 2\int_{0}^{\pi}xf(\sin x)\mathrm{d}x &= \int_{0}^{\pi}\pi f(\sin x)\mathrm{d}x \\
\Rightarrow \int_{0}^{\pi}xf(\sin x)\mathrm{d}x &= \frac{\pi}{2}\int_{0}^{\pi}f(\sin x)\mathrm{d}x
\end{align*}
$$

---

# L 积分的计算_第42页.png

则
$$\int_0^\pi x\sin^9 x \, dx$$
$$= \frac{\pi}{2}\int_0^\pi \sin^9 x \, dx \quad \text{用点火公式}$$
$$= \frac{\pi}{2} \cdot 2 \cdot \frac{8}{9} \cdot \frac{6}{7} \cdot \frac{4}{5} \cdot \frac{2}{3}$$
$$= \frac{128}{315}\pi$$

## 变限积分的计算
### 变限积分求导公式
设$F(x)=\int_{\alpha(x)}^{\beta(x)} f(t)dt$，其中$f(x)$在$[a,b]$上连续，可导函数$\alpha(x)$和$\beta(x)$的值域在$[a,b]$上，则在函数$\alpha(x)$和$\beta(x)$的公共定义域上有
$$
\begin{aligned}
F'(x) &= \frac{d}{dx}\left[ \int_{\alpha(x)}^{\beta(x)} f(t)dt \right] \\
&= f\left(\beta(x)\right)\beta'(x) - f\left(\alpha(x)\right)\alpha'(x)
\end{aligned}
$$

**注：** 我们称，公式中的
- $x$为求导变量
- $t$为积分变量

不求导时，求导变量$x$看作常数；不积分时，积分变量$t$看作常数。

当被积函数$f(\ )$中只含“积分变量”$t$时，才能用求导公式；若被积函数$f(\ )$中有“求导变量”$x$时，必须通过恒等变形（例如：变量代换等方法），将其移出被积函数，才能使用变限积分求导公式。

**例：**
$$
\begin{aligned}
\left( \int_{x^2}^{\sin^2 x} f(t^2)dt \right)'
&= f(\sin^4 x)\cdot (\sin^2 x)' - f(x^4)\cdot (x^2)'
\end{aligned}
$$

---

# L 积分的计算_第43页.png

## 例9.20 变限积分曲线的法线方程
曲线 $y=\int_{0}^{\sin x} e^{t^2} dt$ 在点 $(0,0)$ 处的法线方程为$\underline{\qquad\quad}$。

**分析** $y$ 在 $(0,0)$ 点处的导数$y'$为曲线在该点切线的斜率，法线的斜率为切线斜率的负倒数。

解：
$$
\begin{align*}
y'&=\left( \int_{0}^{\sin x} e^{t^2} dt \right)'\\
&=e^{\sin^2 x} \cdot \cos x
\end{align*}
$$
$\Rightarrow y'(0)=e^{0}\cdot\cos0=1\cdot1=1$

$y$在$(0,0)$处法线斜率为$1$的负倒数，即$-1$。
$\Rightarrow$ 法线方程：$y-0 = -1\cdot(x-0)$
$\Rightarrow y=-x$

## 例9.22 对换元法的深刻理解
设函数$f(x)$可导，且$f(x) < -2x f'(x)$，则曲线 $F(x)=\int_{0}^{x} t f(x^2-t^2) dt$ 在$x=0$处为极值点还是拐点？

**分析** 因为需要对$F(x)$求导，所以被积函数中不能含有$x$，需要用换元法将被积函数中的$x$换掉；换元过程暂不对$x$求导，此时$x$可看作常数。

**思路** 先令$x^2-t^2=u$（$x$为常数），使用定积分的换元积分法，将积分变量$t$替换为$u$：
- 积分变量由$t$替换为$u=x^2-t^2$
- 积分上限：当$t=x$时，替换为$u=x^2-x^2=0$

---

# L 积分的计算_第44页.png

## 变上限积分换元求导
下限由$t=0$换成了$x^2-0=x^2$，即：
- $t=x$时，$u=0$；
- $t=0$时，$u=x^2$。

先正着思路走：
$\because$ 对积分变量$t$积分时$x$可看作常数，
$\therefore$ 令$x^2-t^2=u$，两边同时微分，得：
$$-2t\mathrm{d}t = \mathrm{d}u$$
发现只要凑出$-2t\mathrm{d}t$即可换元成功，因此只用再逆着这个思路往回走，即：
$$
\begin{align*}
-2t\mathrm{d}t &= \mathrm{d}(-t^2) \\
&= \mathrm{d}(-t^2+x^2)
\end{align*}
$$

解：
$$
\begin{align*}
\int_{0}^{x} t f(x^2-t^2)\mathrm{d}t
&= -\frac{1}{2}\int_{0}^{x} -2t f(x^2-t^2)\mathrm{d}t \\
&= -\frac{1}{2}\int_{0}^{x} f(x^2-t^2)\mathrm{d}(-t^2+x^2)
\end{align*}
$$

令$x^2-t^2=u$，则换限为：
- $t=x$时，$u=0$；
- $t=0$时，$u=x^2$。

代入换元后得：
$$
\begin{align*}
&= -\frac{1}{2}\int_{x^2}^{0} f(u)\mathrm{d}u \\
&= \frac{1}{2}\int_{0}^{x^2} f(u)\mathrm{d}u \quad \text{“已可求导”}
\end{align*}
$$

对$x$求一阶导数：
$$
\begin{align*}
F'(x) &= \frac{1}{2}f(x^2)\cdot 2x - \frac{1}{2}f(0)\cdot 0 \\
&= x f(x^2)
\end{align*}
$$
注：若一阶导数无法作出判断，可再次求导。

---

# L 积分的计算_第45页.png

$$
\begin{align*}
F''(x) &= f(x^2) + x f'(x^2) \cdot 2x \\
&= f(x^2) + 2x^2 f'(x^2)
\end{align*}
$$
与题上给的“$f(x) < -2x f'(x)$”很相像
$\because f(x) < -2x f'(x)$
$\therefore f(x) + 2x f'(x) < 0$
当$x=0$时
$\Rightarrow f(0) < 0$
$\because$ 当$x=0$时
$F(0)=0,\ F'(0)=0$
$F''(0) = f(0) < 0$
$\therefore F(x)$在$x=0$处为极大值点。

## 重要结论
(1) $f(x)$为可积的奇函数
$$
\Rightarrow
\begin{cases}
\displaystyle \int_{0}^{x} f(t) \, \mathrm{d}t \text{ 为偶函数} \\[6pt]
\displaystyle \int_{a}^{x} f(t) \, \mathrm{d}t \text{ 为偶函数} \quad (a\neq 0)
\end{cases}
$$
$f(x)$为奇函数 $\Rightarrow f'(x)$为偶函数
$f(x)$为奇函数 $\Rightarrow \displaystyle \int_{a}^{x} f(t) \, \mathrm{d}t$ 为偶函数

注：若$f(x)$为连续的奇函数，则$f(x)$的全体原函数都为偶函数。

---

# L 积分的计算_第46页.png

(2) $f(x)$为可积的偶函数
$$\Rightarrow \begin{cases}
\displaystyle \int_{0}^{x} f(t)\mathrm{d}t \text{ 为奇函数} \\
\displaystyle \int_{a}^{x} f(t)\mathrm{d}t \quad (a\neq 0)
\end{cases}$$
若$\displaystyle \int_{a}^{x} f(t)\mathrm{d}t = \int_{0}^{x} f(t)\mathrm{d}t$，为奇函数
若$\displaystyle \int_{a}^{x} f(t)\mathrm{d}t \neq \int_{0}^{x} f(t)\mathrm{d}t$，为非奇非偶。

$f(x)$偶 $\implies f'(x)$奇
$f(x)$偶 $\implies \displaystyle \int_{0}^{x} f(t)\mathrm{d}t$奇

注：若$f(x)$为连续的偶函数，则$f(x)$的全体原函数中，只有$\displaystyle \int_{0}^{x} f(t)\mathrm{d}t$是奇函数。

(3) $f(x)$是可积的且是以$T$为周期的周期函数，则
$$\int_{0}^{x} f(t)\mathrm{d}t \text{ 是以}T\text{为周期的周期函数} \iff \int_{0}^{T} f(x)\mathrm{d}x=0$$

$f(x)$是以$T$为周期的周期函数
$\implies f'(x)$是以$T$为周期的周期函数

$$\left. \begin{array}{l}
f(x)\text{以}T\text{为周期} \\
\displaystyle \int_{0}^{T} f(x)\mathrm{d}x=0
\end{array} \right\} \implies \int_{0}^{x} f(t)\mathrm{d}t \text{ 以}T\text{为周期}$$

## 例9.24
设奇函数$f(x)$在$(-\infty,+\infty)$上具有连续导数，判断以下函数的奇偶性：
(1) $\displaystyle \int_{0}^{x} \left[ \cos f(t) + f'(t) \right] \mathrm{d}t$

---

# L 积分的计算_第47页.png

(2)  判断积分$\int_{0}^{x} \left[\cos f(t) + f'(t)\right] dt$的奇偶性：
(1)  $\because f(t)$为奇函数，由复合函数奇偶性规律：*内偶则偶，内奇同外*，
$\therefore \cos\left[f(t)\right]$为偶函数，
$\therefore \int_{0}^{x} \cos\left[f(t)\right] dt$为奇函数。
$\because f'(t)$为偶函数（可导奇函数的导函数为偶函数），
$\therefore \int_{0}^{x} f'(t) dt$为奇函数，
$\therefore \int_{0}^{x} \left[\cos f(t) + f'(t)\right] dt$为奇函数（*奇+奇=奇*），即
$$\int_{0}^{x} \left[\cos f(t) + f'(t)\right] dt = \int_{0}^{x} \cos\left[f(t)\right] dt + \int_{0}^{x} f'(t) dt$$
为奇函数。
(2)  与(1)推导类似（*奇+偶=非奇非偶*）：
$\int_{0}^{x} \cos\left[f(t)\right] dt$为奇函数，
$\int_{0}^{x} f(t) dt$为偶函数，
因此$\int_{0}^{x} \left[\cos f(t) + f(t)\right] dt$为非奇非偶函数。
## 例9.25
设$f(x)$连续，且是以$T$为周期的周期函数，$F(x) = \int_{a}^{x} f(t) dt$，且当$\int_{0}^{T} f(x) dx = 0$时，$F(x)$以$T$为周期。
证明：先证$\varphi(x) = F(x) - \frac{\int_{0}^{T} f(x) dx}{T} x$以$T$为周期。
**分析**：设$\varphi(x) = F(x) - \frac{\int_{0}^{T} f(x) dx}{T} x$，
- 法1：证明$\varphi(x+T) = \dots = \varphi(x)$；
- 法2：证明$\varphi(x+T) - \varphi(x) = \dots = 0$。
这里我们采用法2。

---

# L 积分的计算_第48页.png

证明：
$$
\begin{aligned}
&F(x+T) - \frac{\int_0^T f(x)\mathrm{d}x}{T}(x+T) - F(x) + \frac{\int_0^T f(x)\mathrm{d}x}{T}x\\
&\text{其中}\quad F(x)=\int_a^x f(t)\mathrm{d}t\\
=& \int_a^{x+T} f(t)\mathrm{d}t - \frac{\int_0^T f(x)\mathrm{d}x}{T}(x+T) + \frac{\int_0^T f(x)\mathrm{d}x}{T}x - \int_a^x f(t)\mathrm{d}t\\
=& \int_a^{x+T} f(t)\mathrm{d}t - \int_a^x f(t)\mathrm{d}t - \int_0^T f(x)\mathrm{d}x
\end{aligned}
$$
注：上面的$\int_0^T f(x)\mathrm{d}x$是一个固定的常数，因为整体是一个定积分值。
由定积分区间可加性：
$$\because \int_a^{x+T} f(t)\mathrm{d}t = \int_a^x f(t)\mathrm{d}t + \int_x^{x+T} f(t)\mathrm{d}t$$
$$\therefore 原式= \int_x^{x+T} f(t)\mathrm{d}t - \int_0^T f(t)\mathrm{d}t$$
$\because f(x)$为周期函数，
$$\therefore \int_x^{x+T} f(t)\mathrm{d}t = \int_0^T f(t)\mathrm{d}t$$
$$\therefore 原式=0$$

## 反常积分的计算
在计算反常积分时
1.  注意识别奇点（端点，内部点）：$+\infty,-\infty$，瑕点
2.  往往是在收敛的条件下进行计算的。

---

# L 积分的计算_第49页.png

## 例9.26
$$\int_{\frac{1}{2}}^{\frac{3}{2}} \frac{\mathrm{d}x}{\sqrt{|x-x^2|}} = \underline{\qquad\qquad}$$
## 分析
先找奇点
大眼一看，$x=1$为一个无定义点
$$\lim_{x \to 1} \frac{1}{\sqrt{|x-x^2|}} = \infty$$
即，$x=1$为一个无穷间断点
这是一个无界函数的反常积分
因为奇点在积分区间中间
则先拆，且可顺便去绝对值
再由“公式在反常积分定义那”
$$\int_{a}^{b} f(x)\mathrm{d}x = F(b) - \lim_{x \to a^+} F(x) \quad a\text{为奇点}$$
$$\int_{a}^{b} f(x)\mathrm{d}x = \lim_{x \to b^-} F(x) - F(a) \quad b\text{为奇点}$$
求出结果
## 解：
$$\because \lim_{x \to 1} \frac{1}{\sqrt{|x-x^2|}} = \infty$$
$$\therefore 原式 = \int_{\frac{1}{2}}^{1} \frac{1}{\sqrt{x-x^2}} \mathrm{d}x + \int_{1}^{\frac{3}{2}} \frac{1}{\sqrt{x^2 - x}} \mathrm{d}x$$
$$
\begin{align*}
\because x - x^2 &= -(x^2 - x) \\
&= -\left[x^2 - x + \left(\frac{1}{2}\right)^2 - \left(\frac{1}{2}\right)^2\right] \\
&= -\left[\left(x-\frac{1}{2}\right)^2 - \left(\frac{1}{2}\right)^2\right] \\
&= \left(\frac{1}{2}\right)^2 - \left(x-\frac{1}{2}\right)^2
\end{align*}
$$
且
$$\int \frac{1}{\sqrt{a^2 - u^2}} \mathrm{d}u = \arcsin\frac{u}{a} + C$$
$$\therefore \int \frac{1}{\sqrt{x-x^2}} \mathrm{d}x$$

---

# L 积分的计算_第50页.png

$$
=\int \frac{1}{\sqrt{\left(\frac{1}{2}\right)^2 - \left(x-\frac{1}{2}\right)^2}} d\left(x-\frac{1}{2}\right)
$$

$$
= \arcsin \frac{x-\frac{1}{2}}{\frac{1}{2}} + C
$$

$\arcsin 1 = ?$，即 $1 = \sin ?$，得 $? = \frac{\pi}{2}$

$$
\lim_{x \to 1^-} \arcsin \frac{x-\frac{1}{2}}{\frac{1}{2}} = \frac{\pi}{2}
$$

$$
\int_{\frac{1}{2}}^{1} \frac{1}{\sqrt{x-x^2}} dx = \lim_{x \to 1^-} F(x) - F\left(\frac{1}{2}\right)
$$

$$
= \lim_{x \to 1^-} \arcsin \frac{x-\frac{1}{2}}{\frac{1}{2}} - \arcsin \frac{\frac{1}{2}-\frac{1}{2}}{\frac{1}{2}}
$$

$$
= \frac{\pi}{2}
$$

同理，对$x^2-x$配方：
$$
x^2 - x = \left(x-\frac{1}{2}\right)^2 - \left(\frac{1}{2}\right)^2
$$

且有积分公式：
$$
\int \frac{1}{\sqrt{u^2 - a^2}} du = \ln\left(u + \sqrt{u^2 - a^2}\right) + C
$$

$$
\int \frac{1}{\sqrt{x^2 - x}} dx
$$

$$
= \int \frac{1}{\sqrt{\left(x-\frac{1}{2}\right)^2 - \left(\frac{1}{2}\right)^2}} d\left(x-\frac{1}{2}\right)
$$

$$
= \ln\left(x-\frac{1}{2} + \sqrt{\left(x-\frac{1}{2}\right)^2 - \left(\frac{1}{2}\right)^2}\right) + C
$$

$$
\lim_{x \to 1^+} \ln\left(x-\frac{1}{2} + \sqrt{\left(x-\frac{1}{2}\right)^2 - \left(\frac{1}{2}\right)^2}\right) = \ln\left(\frac{1}{2}\right)
$$

$$
\int_{1}^{\frac{3}{2}} \frac{1}{\sqrt{x^2 - x}} dx = F\left(\frac{3}{2}\right) - \lim_{x \to 1^+} F(x)
$$

---

# L 积分的计算_第51页.png

$$
= \ln\left(\frac{3}{2}-\frac{1}{2}+\sqrt{\left(\frac{3}{2}-\frac{1}{2}\right)^2-\left(\frac{1}{2}\right)^2}\right) - \ln\frac{1}{2}
$$
$$
= \ln(2+\sqrt{3})
$$
则
$$
原式 = \left.\arcsin\frac{x-\frac{1}{2}}{\frac{1}{2}}\right|_{\frac{1}{2}}^{1} + \left.\ln\left(x-\frac{1}{2}+\sqrt{\left(x-\frac{1}{2}\right)^2-\left(\frac{1}{2}\right)^2}\right)\right|_{1}^{\frac{3}{2}}
$$
$$
= \frac{\pi}{2} + \ln(2+\sqrt{3})
$$

## 例9.27 “用换元法换成了定积分”
求$$\int_{3}^{+\infty} \frac{dx}{(x-1)^4\sqrt{x^2-2x}}$$
**分析** 该积分为无穷区间的反常积分，由反常积分计算公式：
$$\int_{a}^{+\infty} f(x)dx = \lim_{x \to +\infty} F(x) - F(a)$$
$$\int_{-\infty}^{b} f(x)dx = F(b) - \lim_{x \to -\infty} F(x)$$
通过求原函数代入公式得到结果。

解：先化简被积函数，由$x^2-2x=(x-1)^2-1$，得
$$
原式 = \int_{3}^{+\infty} \frac{dx}{(x-1)^4\sqrt{(x-1)^2 - 1^2}}
$$
用换元法求原函数$F(x)$：
令$x-1 = \sec t$，利用三角恒等式$\sec^2 t = \tan^2 t + 1$，
则$dx = d(\sec t + 1) = \sec t \tan t \, dt$，其中$\sec t = \frac{1}{\cos t}$，导数满足$(\sec t)' = \sec t \tan t$。

更换积分上下限：
- 当$x=3$时，$\sec t +1 = 3$，即$\sec t=2$，得$t=\frac{\pi}{3}$，此时$\cos t = \frac{1}{2}$；
- 当$x \to +\infty$时，$\sec t +1 \to +\infty$，即$\sec t \to +\infty$，得$t \to \frac{\pi}{2}^-$，此时$\cos t \to 0^+$。

代入换元关系得：
$$
\begin{align*}
原式 &= \int_{\frac{\pi}{3}}^{\frac{\pi}{2}} \frac{\sec t \cdot \tan t}{\sec^4 t \cdot \tan t} \, dt \\
&= \int_{\frac{\pi}{3}}^{\frac{\pi}{2}} \frac{1}{\sec^3 t} \, dt
\end{align*}
$$

---

# L 积分的计算_第52页.png

$$=\int_{\frac{\pi}{3}}^{\frac{\pi}{2}} \cos^3 x dx$$
利用三角恒等式：$\cos^2 x = 1-\sin^2 x$，变形被积函数得：
$$=\int_{\frac{\pi}{3}}^{\frac{\pi}{2}} (1-\sin^2 x)\cos x dx$$
凑微分换元：
$$=\int_{\frac{\pi}{3}}^{\frac{\pi}{2}} (1-\sin^2 x)d\sin x = F\left(\frac{\pi}{2}\right) - F\left(\frac{\pi}{3}\right)$$
由牛顿-莱布尼茨公式代入原函数计算：
$$=\left. \left( \sin x - \frac{1}{3}\sin^3 x \right) \right|_{\frac{\pi}{3}}^{\frac{\pi}{2}}$$
$$=\frac{2}{3} - \frac{3\sqrt{3}}{8}$$

注：一个收敛的反常积分，是可以化为一个定积分，当然一个定积分也可以化为一个收敛的反常积分。

## 伽马函数$\Gamma(\alpha)$
“用于秒杀反常积分”
“这里先浅学，深入以后再说”

定义：
$$\Gamma(\alpha) = \int_{0}^{+\infty} x^{\alpha-1} e^{-x} dx$$

递推性质：
$$\Gamma(\alpha+1) = \alpha \cdot \Gamma(\alpha)$$
即对正整数$n$有：
$$\Gamma(n+1) = n!$$
“先不写推导，记住公式即可”

eg：计算$\int_{0}^{+\infty} x^3 e^{-x} dx$
$$
\begin{align*}
\int_{0}^{+\infty} x^3 e^{-x} dx &= \Gamma(3+1) \\
&= 3! \\
&= 6
\end{align*}
$$

---

# L 积分的计算_第53页.png

## 外加一题
$$\int_{0}^{+\infty} e^{-\frac{x}{a}} dx \quad (a\text{为常数且}a>0)$$
推导过程：
$$
\begin{aligned}
\int_{0}^{+\infty} e^{-\frac{x}{a}} dx &= -a\int_{0}^{+\infty} \frac{-1}{a} \cdot e^{-\frac{x}{a}} dx \\
&= -a\int_{0}^{+\infty} e^{-\frac{x}{a}} d\left(-\frac{x}{a}\right) \\
&= -a\cdot\left( \lim_{x \to +\infty} e^{-\frac{x}{a}} - e^{-\frac{0}{a}} \right) \\
&= -a\cdot(-1) \\
&= a
\end{aligned}
$$