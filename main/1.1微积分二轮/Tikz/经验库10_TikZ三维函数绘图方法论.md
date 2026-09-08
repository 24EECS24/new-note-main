# 经验库10 — TikZ三维函数绘图方法论

## 1. 核心结论（已验证）
- 任意 $z=f(x,y)$ 的三维曲面图，本质是「采点+连线+循环」：图像是公式算出来的，不是照图描的。
- **斜投影三向量**是视角灵魂：`x={(-0.866cm,-0.5cm)}, y={(0.866cm,-0.5cm)}, z={(0cm,1cm)}`
  其中 0.866=cos30°，让 xy 平面倾斜、z 轴竖直 → 从斜上方俯视。
  屏幕位置 = X·x向量 + Y·y向量 + Z·z向量，TikZ 自动算，用户只写三维坐标。
- **画曲面靠两族正交截面线**：固定 x 扫 y 一族 + 固定 y 扫 x 一族，交叉成渔网才显立体。
- z 恒用原式代入（曲面定义就是 z=f(x,y)），与求导/积分无关（切片法只是"切片+描线"，非"切片+累加"）。

## 2. 万能模板
```latex
\begin{tikzpicture}[x={(-0.866cm,-0.5cm)},y={(0.866cm,-0.5cm)},z={(0cm,1cm)},>=stealth]
\draw[->] (xmin,0,0)--(xmax,0,0) node[right]{$x$};
\draw[->] (0,ymin,0)--(0,ymax,0) node[right]{$y$};
\draw[->] (0,0,zmin)--(0,0,zmax) node[above]{$z$};
\foreach \xx in {x1,x2,...,xN}{
  \draw[thin] plot[domain=ymin:ymax,samples=50,variable=\yy] (\xx,\yy,{f(\xx,\yy)});
}
\foreach \yy in {y1,y2,...,yN}{
  \draw[thin] plot[domain=xmin:xmax,samples=50,variable=\xx] (\xx,\yy,{f(\xx,\yy)});
}
\end{tikzpicture}
```

## 3. 数学式→TikZ表达式翻译规则
- 平方：`\xx*\xx`（**禁用 `\xx^2`**：pgfmath 中 `-1^2=-(1²)=-1`，负半轴畸变）
- 一般幂：`pow(\xx,n)`；指数：`exp(u)`；对数：`ln(u)`；开方：`sqrt(u)`；绝对值：`abs(u)`
- 三角：`sin(\xx r)` 必须带 `r`（弧度），否则按度算差 57 倍；反三角返回度，转弧度 `*pi/180`
- 乘号 `*` 不可省略；π 用 `pi`
- 坐标里的复杂公式**必须用花括号 `{}` 包住**：`(\xx,\yy,{公式})`

## 4. 高频排错
- 循环变量与 plot 自变量**不能重名**：外层 `\xx`，plot 用 `variable=\yy` 区分
- 变量名用纯字母（`\xa/\xb/\xx/\yy/\ra/\an`），禁用 `\def\x1\x2` 数字后缀（互相覆盖）
- 中文 node 文字致整图 broken image（TikZJax 无 CJK 字形），改英文/公式或 Mermaid
- samples 50 左右够用，勿上千；domain 避开奇点（1/x、ln、sin(1/x)）
- `\def` 复合算术宏不可靠，算式直接写进坐标 `{...}`

## 5. 四类三维图像模板速查（进阶）
- A 显函数 z=f(x,y)：两族截面线模板，改「函数式+domain+坐标轴+步长」四件套。
- B 参数曲面（球面/环面）：参数两族线，坐标三项全是参数函数；球面用经纬度 φ/θ，
  角度按"度"算故 `sin(\ph)` 不加 r。环面 (R+r·cos v)cos u 等。
- C 闭合曲面遮挡：纯TikZ线框无消隐，用「后层 gray!60 先画 + 前层实线后画」近似；
  前后判断：前半球 y≥0 即 θ∈[0,180]。
- D 隐函数：显化分片（z=±sqrt）用类型A；sqrt 内加 max(0,...) 防负值报错；或参数化回类型B。
- 出版级上色/真消隐：pgfplots `\addplot3[surf]`，但**TikZJax 不支持 pgfplots**，须本地LaTeX/Overleaf编译。

## 6. 交付物
完整 6 篇 Obsidian 教程（总览/核心原理/逐字符拆解/通用模板/排错/全类型模板手册，双链闭环）见：
`交付\TikZ三维函数绘图完全指南\`，直接复制进 Obsidian 库即可。
