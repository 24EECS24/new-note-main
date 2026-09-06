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





```tikz
\begin{document}
\definecolor{gridgreen}{rgb}{0,0.39,0}
\begin{tikzpicture}[x=1cm,y=1cm,>=stealth,scale=1.5,
    x={(0.8cm,-0.32cm)}, y={(0.55cm,0.62cm)}, z={(0cm,1cm)}]
    % bounding box [-1,1]^2 x [-1,1], hidden edges dashed
    \draw[gray!25,line width=0.3pt,dashed] (-1,-1,-1) -- (1,-1,-1) -- (1,1,-1) -- (-1,1,-1) -- cycle;
    \draw[gray!35,line width=0.3pt] (-1,-1,1) -- (1,-1,1) -- (1,1,1) -- (-1,1,1) -- cycle;
    \draw[gray!35,line width=0.3pt] (1,-1,-1) -- (1,-1,1);
    \draw[gray!35,line width=0.3pt] (1,1,-1) -- (1,1,1);
    \draw[gray!35,line width=0.3pt] (-1,-1,-1) -- (-1,-1,1);
    \draw[gray!25,line width=0.3pt,dashed] (-1,1,-1) -- (-1,1,1);
    % domain D on z=0
    \draw[gray!55,dashed,line width=0.4pt] (-1,-1,0) -- (1,-1,0) -- (1,1,0) -- (-1,1,0) -- cycle;
    % surface z = 0.5*x*(2-y^2), sweep x with y fixed
    \foreach \y in {-1,-0.75,...,1} {
        \draw[gridgreen,line width=0.5pt,smooth,samples=15,domain=-1:1] plot (\x,\y,{0.5*\x*(2-\y*\y)});
    }
    % sweep y with x fixed -> variable=\y is mandatory
    \foreach \x in {-1,-0.75,...,1} {
        \draw[gridgreen,line width=0.5pt,smooth,samples=15,variable=\y,domain=-1:1] plot (\x,\y,{0.5*\x*(2-\y*\y)});
    }
    % surface outline edges
    \draw[gridgreen,line width=1pt,smooth,samples=30,domain=-1:1] plot (\x,-1,{0.5*\x});
    \draw[gridgreen,line width=1pt,smooth,samples=30,domain=-1:1] plot (\x,1,{0.5*\x});
    \draw[gridgreen,line width=1pt,smooth,samples=30,variable=\y,domain=-1:1] plot (1,\y,{1-0.5*\y*\y});
    \draw[gridgreen,line width=1pt,smooth,samples=30,variable=\y,domain=-1:1] plot (-1,\y,{-1+0.5*\y*\y});
    % zero line x=0
    \draw[line width=1pt,gray!80] (0,-1,0) -- (0,1,0);
    % axes
    \draw[->,black,line width=0.7pt] (0,0,0) -- (1.6,0,0) node[below right,font=\small] {$x$};
    \draw[->,black,line width=0.7pt] (0,-1.4,0) -- (0,1.65,0) node[above right,font=\small] {$y$};
    \draw[->,black,line width=0.7pt] (0,0,-1.3) -- (0,0,1.65) node[above,font=\small] {$z$};
    % labels
    \node[gridgreen,font=\small,fill=white,inner sep=1pt] at (1.12,-0.1,0.9) {$z>0$};
    \node[gridgreen,font=\small,fill=white,inner sep=1pt] at (-1.12,0.1,-0.9) {$z<0$};
    \node[font=\small] at (0,-1.35,2.0) {$f(x,y)=-f(-x,y)$};
\end{tikzpicture}
\end{document}
```




```tikz
\begin{document}
\definecolor{gridgreen}{rgb}{0,0.39,0}
\begin{tikzpicture}[x=1cm,y=1cm,>=stealth,scale=0.7]
% 左上 z=1-x^2-y^2
\begin{scope}[shift={(0,0)}, x={(-0.6cm,-0.3cm)}, y={(1cm,-0.2cm)}, z={(0cm,1cm)}]
    \draw[->] (0,0,0) -- (1.4,0,0) node[right,font=\small] {$x$};
    \draw[->] (0,0,0) -- (0,1.4,0) node[right,font=\small] {$y$};
    \draw[->] (0,0,0) -- (0,0,1.3) node[above,font=\small] {$z$};
    \foreach \y in {-1,-0.5,...,1} {
        \def\xmax{sqrt(1 - \y*\y)}
        \draw[gridgreen,smooth,samples=10,domain=-\xmax:\xmax]
            plot (\x, \y, {1 - \x*\x - \y*\y});
    }
    \foreach \x in {-1,-0.5,...,1} {
        \def\ymax{sqrt(1 - \x*\x)}
        \draw[gridgreen,smooth,samples=10,variable=\y,domain=-\ymax:\ymax]
            plot (\x, \y, {1 - \x*\x - \y*\y});
    }
    \node[below,font=\small] at (0,-1.6,0) {$f(x,y)=f(-x,y)$};
\end{scope}

% 右上
\begin{scope}[shift={(5,0)}, x={(-0.6cm,-0.3cm)}, y={(1cm,-0.2cm)}, z={(0cm,1cm)}]
    \draw[->] (0,0,0) -- (1.4,0,0) node[right,font=\small] {$x$};
    \draw[->] (0,0,0) -- (0,1.4,0) node[right,font=\small] {$y$};
    \draw[->] (0,0,0) -- (0,0,1.3) node[above,font=\small] {$z$};
    \foreach \y in {-1,-0.5,...,1} {
        \def\xmax{sqrt(1 - \y*\y)}
        \draw[gridgreen,smooth,samples=10,domain=-\xmax:\xmax]
            plot (\x, \y, {1 - \x*\x - \y*\y});
    }
    \foreach \x in {-1,-0.5,...,1} {
        \def\ymax{sqrt(1 - \x*\x)}
        \draw[gridgreen,smooth,samples=10,variable=\y,domain=-\ymax:\ymax]
            plot (\x, \y, {1 - \x*\x - \y*\y});
    }
    \node[below,font=\small] at (0,-1.6,0) {$f(x,y)=f(x,-y)$};
\end{scope}

% 左下 z=0.5x(2-y^2)
\begin{scope}[shift={(0,-5)}, x={(-0.6cm,-0.3cm)}, y={(1cm,-0.2cm)}, z={(0cm,1cm)}]
    \draw[->] (0,0,0) -- (1.4,0,0) node[right,font=\small] {$x$};
    \draw[->] (0,0,0) -- (0,1.4,0) node[right,font=\small] {$y$};
    \draw[->] (0,0,0) -- (0,0,1.3) node[above,font=\small] {$z$};
    \draw[->] (0,0,0) -- (0,0,-1.3);
    \draw[gridgreen] (-1,-1,0) -- (1,-1,0) -- (1,1,0) -- (-1,1,0) -- cycle;
    \draw[gridgreen] (-1,-1,-0.5) -- (-1,-1,0) -- (1,-1,0) -- (1,-1,0.5);
    \draw[gridgreen] (-1,1,-0.5) -- (-1,1,0) -- (1,1,0) -- (1,1,0.5);
    \foreach \y in {-1,-0.5,...,1} {
        \draw[gridgreen,smooth,samples=10,domain=-1:1]
            plot (\x, \y, {0.5*\x*(2 - \y*\y)});
    }
    \foreach \x in {-1,-0.5,...,1} {
        \draw[gridgreen,smooth,samples=10,variable=\y,domain=-1:1]
            plot (\x, \y, {0.5*\x*(2 - \y*\y)});
    }
    \node[below,font=\small] at (0,-1.6,0) {$f(x,y)=-f(-x,y)$};
\end{scope}

% 右下 z=0.5y(2-x^2)
\begin{scope}[shift={(5,-5)}, x={(-0.6cm,-0.3cm)}, y={(1cm,-0.2cm)}, z={(0cm,1cm)}]
    \draw[->] (0,0,0) -- (1.4,0,0) node[right,font=\small] {$x$};
    \draw[->] (0,0,0) -- (0,1.4,0) node[right,font=\small] {$y$};
    \draw[->] (0,0,0) -- (0,0,1.3) node[above,font=\small] {$z$};
    \draw[->] (0,0,0) -- (0,0,-1.3);
    \draw[gridgreen] (-1,-1,0) -- (1,-1,0) -- (1,1,0) -- (-1,1,0) -- cycle;
    \draw[gridgreen] (-1,-1,-0.5) -- (-1,-1,0) -- (-1,1,0) -- (-1,1,0.5);
    \draw[gridgreen] (1,-1,-0.5) -- (1,-1,0) -- (1,1,0) -- (1,1,0.5);
    \foreach \y in {-1,-0.5,...,1} {
        \draw[gridgreen,smooth,samples=10,domain=-1:1]
            plot (\x, \y, {0.5*\y*(2 - \x*\x)});
    }
    \foreach \x in {-1,-0.5,...,1} {
        \draw[gridgreen,smooth,samples=10,variable=\y,domain=-1:1]
            plot (\x, \y, {0.5*\y*(2 - \x*\x)});
    }
    \node[below,font=\small] at (0,-1.6,0) {$f(x,y)=-f(x,-y)$};
\end{scope}
\end{tikzpicture}
\end{document}
```
