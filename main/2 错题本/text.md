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
\begin{tikzpicture}[x={(-0.866cm,-0.5cm)},y={(0.866cm,-0.5cm)},z={(0cm,1cm)},>=stealth]
\draw[->] (-2.2,0,0) -- (2.4,0,0) node[right]{$x$};  
\draw[->](0,0,0)--(0,3.5,0)node[right]{$y$};
\draw[->](0,0,-1.5)--(0,0,1.5)node[above]{$z$};
\foreach \xx in {-2,-1.5,...,2}{
  \draw[domain=0:3,samples=24,variable=\yy] plot (\xx,\yy,{2*(abs(\xx)/2)*(1-((\yy-1.5)/1.5)^2)});}
\foreach \yy in {0,0.5,...,3}{
  \draw (-2,\yy,{2*(1-((\yy-1.5)/1.5)^2)})--(0,\yy,0)--(2,\yy,{2*(1-((\yy-1.5)/1.5)^2)});}
\end{tikzpicture}
\end{document}
```

```tikz
\begin{document}
\begin{tikzpicture}[x={(-0.866cm,-0.5cm)},y={(0.866cm,-0.5cm)},z={(0cm,1cm)},>=stealth]  
% 修正坐标轴语法，调整范围覆盖正负x/z
\draw[->] (-2.2,0,0) -- (2.4,0,0) node[right]{$x$};  
\draw[->] (0,0,0) -- (0,4,0) node[right]{$y$};  
\draw[->] (0,0,-2.2) -- (0,0,2.4) node[above]{$z$};  
% 沿y方向抛物线族：去掉绝对值，x正负时z符号相反
\foreach \xx in {-2,-1.5,...,2}{  
  \draw[domain=0:3,samples=24,variable=\yy] plot (\xx,\yy,{\xx*(1-((\yy-1.5)/1.5)^2)});
}  
% 沿x方向直母线：x=-2处z改为负值，匹配曲面公式
\foreach \yy in {0,0.5,...,3}{  
  \draw (-2,\yy,{-2*(1-((\yy-1.5)/1.5)^2)})--(0,\yy,0)--(2,\yy,{2*(1-((\yy-1.5)/1.5)^2)});
}  
\end{tikzpicture}
\end{document}
```

```tikz
\begin{document}
\begin{tikzpicture}[x={(-0.866cm,-0.5cm)},y={(0.866cm,-0.5cm)},z={(0cm,1cm)},>=stealth,line join=round]  
% 坐标轴：只画正方向，原点处加虚线垂直线匹配示意图
\draw[->] (0,0,0) -- (-2.4,0,0) node[left]{$x$};  
\draw[->] (0,0,0) -- (0,3.2,0) node[right]{$y$};  
\draw[->] (0,0,0) -- (0,0,2.4) node[above]{$z$};
\draw[dashed, gray] (0,0,0) -- (0,0,-0.8); % z轴负方向短虚线

% ========== 曲面网格：固定y的直母线（沿x方向直线）+ 固定x的抛物线 ==========
% 曲面公式：z = -x·(1-((y-1.5)/1.5)^2)，x∈[-2,2],y∈[0,3]
% x∈[-2,0]为上凸面（z≥0），x∈[0,2]为下凹面（z≤0），x=0处交于y轴方向直线
\foreach \xx in {-2,-1.5,...,2}{  
  \draw[domain=0:3,samples=24,variable=\yy] plot (\xx,\yy,{-\xx*(1-((\yy-1.5)/1.5)^2)});
}
\foreach \yy in {0,0.5,...,3}{  
  \draw (-2,\yy,{2*(1-((\yy-1.5)/1.5)^2)})--(2,\yy,{-2*(1-((\yy-1.5)/1.5)^2)});
}
\end{tikzpicture}
\end{document}
```

```tikz
\begin{document}
\begin{tikzpicture}[x={(-0.866cm,-0.5cm)},y={(0.866cm,-0.5cm)},z={(0cm,1cm)},>=stealth]  
% 坐标轴适配凹凸双层面，保留x正方向可见原凸面位置已空
\draw[->] (-2.2,0,0) -- (2.4,0,0) node[right]{$x$};  
\draw[->] (0,0,0) -- (0,3.6,0) node[right]{$y$};  
\draw[->] (0,0,-2.2) -- (0,0,2.4) node[above]{$z$};  

% 沿y方向抛物线网格：凹面（下，z≤0）+ 平移后的凸面（上，z≥0）
% 凸面为原x>0部分沿x轴负向平移2单位，公式替换x→x+2，形状完全不变
\foreach \xx in {-2,-1.5,...,0}{  
  % 下方凹面
  \draw[domain=0:3,samples=24,variable=\yy] plot (\xx,\yy,{\xx*(1-((\yy-1.5)/1.5)^2)});
  % 上方平移后的凸面
  \draw[domain=0:3,samples=24,variable=\yy] plot (\xx,\yy,{(\xx+2)*(1-((\yy-1.5)/1.5)^2)});
}  

% 沿x方向直母线网格：凹面直边 + 凸面直边，两端y=0/y=3处两面自然贴合
\foreach \yy in {0,0.5,...,3}{  
  % 下方凹面直边：从左端点(-2,y,z_min)到原点侧(0,y,0)
  \draw (-2,\yy,{-2*(1-((\yy-1.5)/1.5)^2)})--(0,\yy,0);
  % 上方凸面直边：从左端点(-2,y,0)到右端点(0,y,z_max)
  \draw (-2,\yy,0)--(0,\yy,{2*(1-((\yy-1.5)/1.5)^2)});
}  
\end{tikzpicture}
\end{document}
```

```tikz
\begin{document}
\begin{tikzpicture}[x={(-0.866cm,-0.5cm)},y={(0.866cm,-0.5cm)},z={(0cm,1cm)},>=stealth]  
% 坐标轴保持原样式
\draw[->] (-2.2,0,0) -- (2.4,0,0) node[right]{$x$};  
\draw[->] (0,0,0) -- (0,3.6,0) node[right]{$y$};  
\draw[->] (0,0,-2.2) -- (0,0,2.4) node[above]{$z$};

% 凸面：原位置原形状完全不动，无任何修改
\foreach \xx in {-2,-1.5,...,0}{  
  \draw[domain=0:3,samples=24,variable=\yy] plot (\xx,\yy,{(\xx+2)*(1-((\yy-1.5)/1.5)^2)});  
}
\foreach \yy in {0,0.5,...,3}{  
  \draw (-2,\yy,0)--(0,\yy,{2*(1-((\yy-1.5)/1.5)^2)});
}  

% 凹面：仅删除虚线参数，改为实线，平移位置/形状完全不变
\foreach \xx in {0,0.5,...,2}{  
  \draw[domain=0:3,samples=24,variable=\yy] plot (\xx,\yy,{(\xx-2)*(1-((\yy-1.5)/1.5)^2)});
}
\foreach \yy in {0,0.5,...,3}{  
  \draw (0,\yy,{-2*(1-((\yy-1.5)/1.5)^2)})--(2,\yy,0);
}  
\end{tikzpicture}
\end{document}
```


```tikz
\begin{document}
\begin{tikzpicture}[x={(-0.6cm,-0.3cm)},y={(1cm,-0.2cm)},z={(0cm,1cm)},>=stealth,line cap=round,line join=round,scale=1]
\foreach \yy in {-1,-0.75,-0.5,-0.25,0,0.25,0.5,0.75,1}{\draw[gray!50] plot[samples=22,domain=-1:1] (\x,\yy,{(1.05)*(\x^2 - \yy^2)});}
\foreach \xx in {-1,-0.75,-0.5,-0.25,0,0.25,0.5,0.75,1}{\draw plot[samples=22,domain=-1:1,variable=\y] (\xx,\y,{(1.05)*(\xx^2 - \y^2)});}
\draw[->](-1.32,0,0)--(1.32,0,0)node[right]{$x$};
\draw[->](0,-1.32,0)--(0,1.32,0)node[right]{$y$};
\draw[->](0,0,-1.176)--(0,0,1.208)node[above]{$z$};
\end{tikzpicture}
\end{document}
```



```tikz
\begin{document}
\begin{tikzpicture}[x={(-0.866cm,-0.5cm)},y={(0.866cm,-0.5cm)},z={(0cm,1cm)},>=stealth]
% 坐标轴
\draw[->] (-3.2,0,0) -- (3.2,0,0) node[right]{$x$};
\draw[->] (0,-3.2,0) -- (0,3.2,0) node[right]{$y$};
\draw[->] (0,0,0) -- (0,0,2.2) node[above]{$z$};

% 径向曲线（meridian curves），固定角度
\foreach \ang in {0,30,...,330}{
  \draw[domain=0:3,samples=40,variable=\r]
    plot ({\r*cos(\ang)}, {\r*sin(\ang)}, {5*\r*\r*exp(-\r*\r)});
}

% 等高圆环，固定半径
\foreach \r in {0.5,1,1.5,2,2.5}{
  \draw[domain=0:360,samples=40,variable=\t]
    plot ({\r*cos(\t)}, {\r*sin(\t)}, {5*\r*\r*exp(-\r*\r)});
}
\end{tikzpicture}
\end{document}
```



```tikz
\begin{document}
\begin{tikzpicture}[x={(-0.866cm,-0.5cm)},y={(0.866cm,-0.5cm)},z={(0cm,1cm)},>=stealth]
\draw[->] (-3.2,0,0)--(3.4,0,0) node[right]{$x$};
\draw[->] (0,-3.2,0)--(0,3.4,0) node[right]{$y$};
\draw[->] (0,0,0)--(0,0,2.3) node[above]{$z$};

% 沿x方向曲线族：x取定值，y扫过，z直接用原式
\foreach \xx in {-2.5,-2,...,2.5}{
  \draw[thin] plot[domain=-2.5:2.5,samples=50,variable=\yy]
    (\xx,\yy,{5*(\xx*\xx+\yy*\yy)*exp(-(\xx*\xx+\yy*\yy))});
}
% 沿y方向曲线族：y取定值，x扫过，z直接用原式
\foreach \yy in {-2.5,-2,...,2.5}{
  \draw[thin] plot[domain=-2.5:2.5,samples=50,variable=\xx]
    (\xx,\yy,{5*(\xx*\xx+\yy*\yy)*exp(-(\xx*\xx+\yy*\yy))});
}
\end{tikzpicture}
\end{document}
```




```tikz
\begin{document}
\begin{tikzpicture}[x={(-0.866cm,-0.5cm)},y={(0.866cm,-0.5cm)},z={(0cm,1cm)},>=stealth,line cap=round,line join=round,scale=3]
\foreach \yy in {-1,-0.75,-0.5,-0.25,0,0.25,0.5,0.75,1}{\draw[gray!50] plot[samples=22,domain=-1:1] (\x,\yy,{(1.05)*(\x*\x*\x*\yy*\yy*\yy)});}
\foreach \xx in {-1,-0.75,-0.5,-0.25,0,0.25,0.5,0.75,1}{\draw plot[samples=22,domain=-1:1,variable=\y] (\xx,\y,{(1.05)*(\xx*\xx*\xx*\y*\y*\y)});}
\draw[->](-1.32,0,0)--(1.32,0,0)node[right]{$x$};
\draw[->](0,-1.32,0)--(0,1.32,0)node[right]{$y$};
\draw[->](0,0,-1.176)--(0,0,1.208)node[above]{$z$};
\end{tikzpicture}
\end{document}
```
