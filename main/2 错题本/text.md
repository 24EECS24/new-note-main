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
\usepackage{pgfplots}
\pgfplotsset{compat=1.15}
\usetikzlibrary{arrows,arrows.meta}

\definecolor{ffffff}{rgb}{1,1,1}
\begin{tikzpicture}[line cap=round,
line join=round,
>=triangle 45,
line width=0.5pt,
font=\fontsize{10pt}{12pt}\selectfont]
\begin{axis}[xtick={-5,-4,...,5},
ytick={-4,-3,...,4},
width=12cm,
height=9.213cm,
scale only axis=true,
xmajorgrids=false,
ymajorgrids=false,
xmin=-4.944357,
xmax=4.84178,
ymin=-3.67815,
ymax=3.83493,
axis lines=none,
axis line style={draw=none},
tick style={draw=none},
xticklabels={},
yticklabels={}]
\clip(-4.944357,-3.67815) rectangle (4.84178,3.83493);
\path[draw={rgb,255:red,255;green,255;blue,255},fill=none,line width=0.5pt,line cap=round,line join=round,draw opacity=0.2] (axis cs:-4.27,-4.27)
	-- (axis cs:4.73,4.73);
\path[draw={rgb,255:red,255;green,255;blue,255},fill=none,line width=0.5pt,line cap=round,line join=round,draw opacity=0.698039] (axis cs:-4.27,-4.27)
	-- (axis cs:4.73,4.73);

\draw[color=ffffff] (-3.75,-3.76) node {$f$};
\end{axis}
\end{tikzpicture}
```
