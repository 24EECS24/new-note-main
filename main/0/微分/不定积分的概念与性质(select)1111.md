# 不定积分的概念与性质真题归纳（2016—2026）

> 本文件收录 2016—2026 年河南专升本《高等数学》真题中**所有涉及不定积分的概念与性质知识点**的纯概念题，共 **3 题**。题面均逐题对照官方试卷 PDF 核对，与原卷一致；答案逐题独立推导验证。按年份从 2026 倒序至 2016，**一个试卷一个一级标题，一题一个二级标题**，题号沿用真题题号。
>
> 收录范围：靠原函数与不定积分概念、积分—微分互逆关系即可判断，不需要凑微分/换元/分部等积分方法的题目；需用积分方法求原函数的运算题归入《不定积分的计算》。

# 2021年

## 第13题

xxxx

**题目**

下列等式正确的是（　）

A. $\dfrac{d}{dx}\displaystyle\int f(x)\,dx=f(x)$

B. $d\!\left(\displaystyle\int f(x)\,dx\right)=f(x)$

C. $\dfrac{d}{dx}\displaystyle\int f'(x)\,dx=f(x)$

D. $\displaystyle\int f'(x)\,dx=f(x)$
?

````````col
```````col-md
flexGrow=20
===

**答案**：A

**解析**

> 逐项用积分—微分互逆关系判断：
>
> - A：$\left(\displaystyle\int f(x)\,dx\right)'=[F(x)+C]'=f(x)$，正确。
> - B：$d\!\left(\displaystyle\int f(x)\,dx\right)=d[F(x)+C]=f(x)\,dx$，选项右端少了微分因子 $dx$，错误。
> - C：$\left(\displaystyle\int f'(x)\,dx\right)'=[f(x)+C]'=f'(x)$，选项写成 $f(x)$，错误。
> - D：$\displaystyle\int f'(x)\,dx=f(x)+C$，选项少了任意常数 $C$，错误。
>
> 故选 A。

**考点**

积分与微分的互逆关系（微分 $dx$ 与任意常数 $C$ 的规范）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz

# 2019年

## 第16题

xxxx

**题目**

在 $[a,b]$ 内，$g'(x)=f'(x)$，则下列哪个正确（　）

A. $g(x)=f(x)$

B. $\left(\displaystyle\int g(x)\,dx\right)'=\left(\displaystyle\int f(x)\,dx\right)'$

C. $g(x)=f(x)-C$

D. $\displaystyle\int g(x)\,dx=\int f(x)\,dx$
?

````````col
```````col-md
flexGrow=20
===

**答案**：C

**解析**

> 由 $g'(x)=f'(x)$，得
> $$[g(x)-f(x)]'=0$$
> 故 $g(x)-f(x)$ 在区间内为常数，即 $g(x)=f(x)+C_{0}$，写成 $g(x)=f(x)-C$（$C$ 为任意常数），C 正确。
>
> - A：两函数相差一个常数，未必相等，错误。
> - B：$\left(\displaystyle\int g\,dx\right)'=g(x)$，$\left(\displaystyle\int f\,dx\right)'=f(x)$，而 $g$ 与 $f$ 未必相等，错误。
> - D：两个不定积分各自含任意常数，不能由 $g'=f'$ 直接断定其相等，错误。
>
> 故选 C。

**考点**

导数相同的两个函数相差常数（原函数之间的关系）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz

# 2018年

## 第11题

xxxx

**题目**

下列等式正确的是（　）

A. $d\displaystyle\int df(x)=f'(x)+C$

B. $d\displaystyle\int df(x)=f(x)+C$

C. $\displaystyle\int f'(x)\,dx=f(x)+C$

D. $\dfrac{d}{dx}\displaystyle\int df(x)=f(x)$
?

````````col
```````col-md
flexGrow=20
===

**答案**：C

**解析**

> 先化简 $\displaystyle\int df(x)=\int f'(x)\,dx=f(x)+C$。
>
> - A、B：$d\displaystyle\int df(x)=d[f(x)+C]=df(x)=f'(x)\,dx$，结果是一个含 $dx$ 的微分；A、B 右端既无 $dx$ 又带 $+C$，均错误。
> - C：$\displaystyle\int f'(x)\,dx=f(x)+C$，正确。
> - D：$\left(\displaystyle\int df(x)\right)'=[f(x)+C]'=f'(x)$，选项写成 $f(x)$，错误。
>
> 故选 C。

**考点**

积分与微分的互逆关系（微分与不定积分的规范形式）
```````

```````col-md
flexGrow=1
===





```````
````````


zzzz

> （注：部分内容由豆包 AI 生成）