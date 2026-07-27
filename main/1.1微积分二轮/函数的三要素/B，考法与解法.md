# 复合函数
## 二层复合
### 定义域与值域

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
若\quad &D_{g} \to g(\ )\to R_{g}\\[4pt]
&D_{f} \to f(\ )\to R_{f}\\[4pt]
&D \to f[g(\ )]\to R\\[4pt]
则\quad &  \\[4pt]
&\left.\begin{matrix}
 D_{f}\xrightarrow[]{g^{-1}(\ )} \Box 
\\[4pt]
D_{g}\cap \Box =D
\end{matrix}\right\} D=D_{g}\cap g^{-1}(D_{f}) \\[4pt]

&\left.\begin{matrix}
 D\xrightarrow[]{g(\ )}R_{g}\cap D_{f}\xrightarrow[]{f(\ )}R
\\[4pt]
D_{g}\xrightarrow[]{g(\ )}R_{g}，R_{g}\cap D_{f}\xrightarrow[]{f(\ )}R
\end{matrix}\right\} R=f[g(D)]=f[R_{g}\cap D_{f}] \\[4pt]

\end{align*}
$$

`````col
````col-md
flexGrow=1
===

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&无论是求定义域还是求值域\\[4pt]
&都是从各层定义域D_{g}，D_{f}入手\\[4pt]
&D_{g}与D_{f}往往都能得到\\[4pt]
\end{align*}
$$

````

````col-md
flexGrow=1
===

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
eg: \ &lnx \ ，\ x> 0   &&arcsinx\ ，\ x\in [-1,1] \\[4pt]                      
&\sqrt{x} \ ，\ x\ge 0  &&arctanx\ ，\ x\in R   \\[4pt]
&\frac{1}{x}  \ ，\ x\ne 0 \\[4pt]
\end{align*}
$$



````
`````
- [*] 求定义域
`````col
````col-md
flexGrow=1
===

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&先找出D_{g}与D_{f}\\[4pt]
&由D_{f}作为第一层的输出域\\[4pt]
&反求出有效输入域\Box \\[4pt]
&再将D_{g}\cap \Box =D\\[4pt]
\end{align*}
$$

````

````col-md
flexGrow=1
===

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&\to D_{g}，D_{f}\\[4pt]
&D_{f}\xrightarrow[]{g^{-1}(\ )} \Box \\[4pt]
&D=D_{g}\cap \Box \\[4pt]
\end{align*}
$$



````
`````
- [*] 求值域
 ==基初法：==
`````col
````col-md
flexGrow=1
===

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&先求出定义域D\\[4pt]
&由D作为第一层的输入域\\[4pt]
&求出第二层的有效输入域R_{g}\cap D_{f} \\[4pt]
&再由R_{g}\cap D_{f}为第二层的输入域\\[4pt]
&求出输出域R\\[4pt]
\end{align*}
$$

````

````col-md
flexGrow=1
===

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&\to D_{g}，D_{f}\\[4pt]
&D_{f}\xrightarrow[]{g^{-1}(\ )} \Box \\[4pt]
&D_{g}\cap \Box =D \\[4pt]
&\to D\\[4pt]
&D\xrightarrow[]{g(\ )}R_{g}\cap D_{f}\\[4pt]
&R_{g}\cap D_{f}\xrightarrow[]{f(\ )}R\\[4pt]
\end{align*}
$$



````
`````
==进阶法：==
`````col
````col-md
flexGrow=1
===

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&先找出D_{g}与D_{f}\\[4pt]
&由D_{g}作为第一层的输入域\\[4pt]
&求出第一层的输出域R_{g} \\[4pt]
&与D_{f}取交集得出第二层的有效输入域R_{g}\cap D_{f} \\[4pt]
&再由R_{g}\cap D_{f}为第二层的输入域\\[4pt]
&求出输出域R\\[4pt]
\end{align*}
$$

````

````col-md
flexGrow=1
===

$$
\begin{align*}  % *号表示不自动加公式编号，更简洁
&\to D_{g}，D_{f}\\[4pt]
&D_{g}\xrightarrow[]{g(\ )}R_{g}\\[4pt]
&R_{g}\cap D_{f}\\[4pt]
&R_{g}\cap D_{f}\xrightarrow[]{f(\ )}R\\[4pt]
\end{align*}
$$



````
`````
### 对应关系
