# I10.png

（拉格朗日中值定理几何示意图）
$$f'(\xi)=\frac{f(b)-f(a)}{b-a}$$
拉格朗日

将直角坐标系表达式写成参数方程：
（参数方程形式的中值定理几何示意图）
$$k=\frac{f(b)-f(a)}{g(b)-g(a)}$$
对应的参数方程为：
$$\begin{cases}
x=g(t)\\
y=f(t)
\end{cases}$$
由参数方程求导，$\xi$处切线斜率满足：
$$K=\left.\frac{dy}{dx}\right|_{\xi}=\left.\frac{\frac{dy}{dt}}{\frac{dx}{dt}}\right|_{\xi}=\frac{f'(\xi)}{g'(\xi)}=\frac{f(b)-f(a)}{g(b)-g(a)}$$

---

## 例6.11
设$f(x)$在$[a,b]$上连续，在$(a,b)$内可导，$0<a<b$。
证明：至少存在一点$\xi\in(a,b)$，使得
$$f(b)-f(a)=\xi\ln\frac{b}{a}f'(\xi)$$

$$\because f(b)-f(a)=\xi\left[\ln b - \ln a\right]f'(\xi)$$
$$\frac{f(b)-f(a)}{\ln b - \ln a}=\frac{f'(\xi)}{\frac{1}{\xi}}$$
其中$[\ln x]'=\frac{1}{x}$。

∴证明：
$\because f(x), \ln x$满足：
$$\begin{cases}
在[a,b]上连续\\
在(a,b)内可导\\
[\ln x]'\neq0
\end{cases}$$

则由柯西中值定理可得：
$\exists \xi\in(a,b)$，使得
$$\frac{f(b)-f(a)}{\ln b - \ln a}=\frac{f'(\xi)}{[\ln\xi]'}$$
即
$$f(b)-f(a)=\xi\ln\frac{b}{a}f'(\xi)$$