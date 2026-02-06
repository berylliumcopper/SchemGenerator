# SchemGenerator

这个项目旨在提供一种在 Minecraft 中使用由参数方程描述的曲面的方法。输入为函数 $(x, y, z) = (f_x(u, v), f_y(u, v), f_z(u, v))$ 以及参数 $u, v$ 的绘制范围（形式为 $u_1 ≤ u ≤ u_2，h_1(u) ≤ v ≤ h_2(u)$ ）。输出为 .schem 文件，可被 WorldEdit 等模组直接读取。

虽然可以直接使用 WorldEdit 本身来生成曲面（例如使用 `//g [pattern] -h [expression]`），但这种方式在某些情况下会失效：

- Minecraft 聊天消息的长度限制为 256 个字符，无法输入较为复杂的表达式。
- `//g [pattern] -h [expression]` 命令只能生成将选区分割为两部分的曲面（因为它是通过检测 `True` 与 `False` 区域的边界来生成的）。这对应于 $g(x, y, z) = 0$ 的曲面形式。然而，许多曲面更容易用参数方程的形式表示。

这些情况在我做 Minecraft 建筑的过程中经常遇到，因此我决定写一个程序，用参数形式的曲面表达式来生成 .schem 文件。

本项目基于 PolyForm Noncommercial License 1.0.0 许可证发布。

你可以在非商业用途下自由使用、修改和分享本软件。
禁止任何形式的商业用途，包括出售本软件或将其作为付费服务提供。

更新日志：

2026/02/06，版本 A.1：实现自相交曲面的生成。

This project aims to provide a way to use the curved surface described by parametric equations in minecraft. The input is the functions $(x,y,z)=(f_x(u,v),f_y(u,v),f_z(u,v))$ and the plot range of the parameters $u,v$, in the form of $u_1\leq u\leq u_2, h_1(u)\leq v\leq h_2(u)$. The output is the .schem file that can be directly read by mods like WorldEdit.

Although it is possible to generate curved surface with WorldEdit itself (using `//g [pattern] -h [expression]`), this approach breaks down in some cases:

- The length limit of Minecraft chat message is 256 characters, preventing the entry of complicated expressions.
- The `//g [pattern] -h [expression]` command can only generate the surfaces which seperate the selected zone into two parts (because it detects the border of the `True` and `False` regions). This corresponds to the surface form of $g(x,y,z)=0$. However, many surfaces are much easier to represent in the form of parametric equations.

These are situations I often encounter in minecraft buildings, so I decide to implement a program to generate the .schem files from parametric expressions of curved surfaces.

This project is licensed under the PolyForm Noncommercial License 1.0.0.

You are free to use, modify, and share this software for non-commercial purposes.
Commercial use, including selling the software or offering it as a paid service, is not permitted.

Update Log:

Feb 06 2026, version A.1: implement the generation of self-crossing surface
