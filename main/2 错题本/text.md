`````col
````col-md
flexGrow=1
===

Column A

````

````col-md
flexGrow=1
===

Column B



````
`````

````col
```col-md

Column A

```

```col-md

Column B



```
````
`````col
````col-md
Column A
````

````col-md
Column B

```col-md
Column B
```

````
`````
`````col
````col-md
Column A
```col-md
Column B
```
````

````col-md
Column B

````
`````
````col
```col-md
flexGrow=2
===

Column A

```

```col-md
flexGrow=1
===

Column B



```
````






```tikz
\begin{document}
\begin{tikzpicture}[>=stealth,line cap=round,line join=round,
 x={(-0.88cm,-0.18cm)},y={(0.88cm,-0.18cm)},z={(0cm,1cm)},scale=1.0]
% 积分区域 x∈[-2,2], y∈[0,3], z∈[0,2]，无盖网格盒
% 曲面 z = 2*(|x|/2)*(1-((y-1.5)/1.5)^2)：x=0 是贴底谷线，x=±2 端面成拱
% --- 底面 z=0 方格 ---
\foreach \yy in {0,0.5,...,3}{\draw[gray,thin] (-2,\yy,0)--(2,\yy,0);}
\foreach \xx in {-2,-1.5,...,2}{\draw[gray,thin] (\xx,0,0)--(\xx,3,0);}
% --- 左前竖面 x=2 方格 ---
\foreach \yy in {0,0.5,...,3}{\draw[gray,thin] (2,\yy,0)--(2,\yy,2);}
\foreach \zz in {0,0.5,...,2}{\draw[gray,thin] (2,0,\zz)--(2,3,\zz);}
% --- 右前竖面 y=3 方格 ---
\foreach \xx in {-2,-1.5,...,2}{\draw[gray,thin] (\xx,3,0)--(\xx,3,2);}
\foreach \zz in {0,0.5,...,2}{\draw[gray,thin] (-2,3,\zz)--(2,3,\zz);}
% --- 后端面/远端棱边 ---
\draw[gray,thin] (-2,0,0)--(-2,0,2)--(2,0,2) (-2,0,2)--(-2,3,2)--(-2,3,0);
% --- 曲面：沿 x 的 V 形截面（在 x=0 谷线落底）---
\foreach \yy in {0,0.5,...,3}{
  \draw (-2,\yy,{2*(1-((\yy-1.5)/1.5)^2)})--(0,\yy,0)--(2,\yy,{2*(1-((\yy-1.5)/1.5)^2)});}
% --- 曲面：沿 y 的拱弧 ---
\foreach \xx in {-2,-1.5,...,2}{
  \draw[domain=0:3,samples=24,variable=\yy] plot (\xx,\yy,{2*(abs(\xx)/2)*(1-((\yy-1.5)/1.5)^2)});}
% --- 坐标轴 ---
\draw[->,thick] (-2.8,0,0)--(2.9,0,0) node at(3.2,0,0)[below]{$x$};
\draw[->,thick] (0,-0.8,0)--(0,3.8,0) node[right]{$y$};
\draw[->,thick] (0,0,0)--(0,0,2.7) node[above]{$z$};
\end{tikzpicture}
\end{document}
```



```tikz
\begin{document}
\begin{tikzpicture}[>=stealth,line cap=round,line join=round,
 x={(-0.88cm,-0.18cm)},y={(0.88cm,-0.18cm)},z={(0cm,1cm)},scale=1.0]
% 积分区域 x∈[-2,2], y∈[0,3], z∈[0,2]，无盖网格盒
% 曲面 z = 2*(|x|/2)*(1-((y-1.5)/1.5)^2)：x=0 是贴底谷线，x=±2 端面成拱
% --- 底面 z=0 方格 ---
\foreach \yy in {0,0.5,...,3}{\draw[gray,thin] (-2,\yy,0)--(2,\yy,0);}
\foreach \xx in {-2,-1.5,...,2}{\draw[gray,thin] (\xx,0,0)--(\xx,3,0);}
% --- 左前竖面 x=2 方格 ---
\foreach \yy in {0,0.5,...,3}{\draw[gray,thin] (2,\yy,0)--(2,\yy,2);}
\foreach \zz in {0,0.5,...,2}{\draw[gray,thin] (2,0,\zz)--(2,3,\zz);}
% --- 右前竖面 y=3 方格 ---
\foreach \xx in {-2,-1.5,...,2}{\draw[gray,thin] (\xx,3,0)--(\xx,3,2);}
\foreach \zz in {0,0.5,...,2}{\draw[gray,thin] (-2,3,\zz)--(2,3,\zz);}
% --- 后端面/远端棱边 ---
\draw[gray,thin] (-2,0,0)--(-2,0,2)--(2,0,2) (-2,0,2)--(-2,3,2)--(-2,3,0);
% --- 曲面：沿 x 的 V 形截面（在 x=0 谷线落底）---
\foreach \yy in {0,0.5,...,3}{
  \draw (-2,\yy,{2*(1-((\yy-1.5)/1.5)^2)})--(0,\yy,0)--(2,\yy,{2*(1-((\yy-1.5)/1.5)^2)});}
% --- 曲面：沿 y 的拱弧 ---
\foreach \xx in {-2,-1.5,...,2}{
  \draw[domain=0:3,samples=24,variable=\yy] plot (\xx,\yy,{2*(abs(\xx)/2)*(1-((\yy-1.5)/1.5)^2)});}
% --- 坐标轴 ---
\draw[->,thick] (-2.8,0,0)--(2.9,0,0) node at(3.2,0,0)[below]{$x$};
\draw[->,thick] (0,-0.8,0)--(0,3.8,0) node[right]{$y$};
\draw[->,thick] (0,0,0)--(0,0,2.7) node[above]{$z$};
\end{tikzpicture}
\end{document}
```

