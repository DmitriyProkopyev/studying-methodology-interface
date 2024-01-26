---
{"dg-publish":true,"permalink":"/homepage/","tags":["gardenEntry"]}
---

This is actually an obsidian note :)

> [!info] Description
> Mnemonic for quick computing of $3 \times 3$ matrix determinant

> [!abstract] Algorithm
> Given matrix $A$:
> $$
> A = \begin {bmatrix}
> a & b & c \\
> d & e & f \\
> g & h & i
> \end {bmatrix}
> $$
> Rewrite the first and second columns again for convenience. Then, highlight the full diagonals:
> $$
> \begin {bmatrix}
> \begin{array}{{ccc}|cc}
> \color {red} a & \color {orange} b & \color {yellow} c & a & b \\
> d & \color {red} e & \color {orange} f & \color {yellow} d & e \\
> g & h & \color {red} i & \color {orange} g & \color {yellow} h
> \end {array}
> \end {bmatrix}
> $$
> 
> $$
> \begin {bmatrix}
> \begin{array}{{ccc}|cc}
> a & b & \color {lightgreen} c & \color {cyan} a & \color {purple} b \\
> d & \color {lightgreen} e & \color {cyan} f & \color {purple} d & e \\
> \color {lightgreen} g & \color {cyan} h & \color {purple} i & g & h
> \end {array}
> \end {bmatrix}
> $$
> Calculate the sum of products of the *"downward"* diagonals:
> $$
> \color {red} {aei} + \color {orange} {bfg} + \color {yellow} cdh
> $$
> Then, calculate the sum of products of the *"upward"* diagonals:
> $$
> \color {lightgreen} {gec} + \color {cyan} {hfa} + \color {purple} idb
> $$
> The resulting determinant of $A$ is the difference of these sums
> $$
> det(A) = \color {red} {aei} + \color {orange} {bfg} + \color {yellow} cdh - \color {lightgreen} {gec} - \color {cyan} {hfa} - \color {purple} idb
> $$

> [!example]
> Let us calculate the determinant of $A^{3 \times 3}$:
> $$
> A = \begin {bmatrix}
> 3 & -7 & 1 \\
> 0 & -2 & 5 \\
> 0 & 9 & 8
> \end {bmatrix}
> $$
> Let us rewrite the first and second columns again for convenience and highlight the full diagonals:
> $$
> \begin {bmatrix}
> \begin{array}{{ccc}|cc}
> \color {red} 3 & \color {orange} -7 & \color {yellow} 1 & 3 & -7 \\
> 0 & \color {red} -2 & \color {orange} 5 & \color {yellow} 0 & -2 \\
> 0 & 9 & \color {red} 8 & \color {orange} 0 & \color {yellow} 9
> \end {array}
> \end {bmatrix}
> $$
> 
> $$
> \begin {bmatrix}
> \begin{array}{{ccc}|cc}
> 3 & -7 & \color {lightgreen} 1 & \color {cyan} 3 & \color {purple} -7 \\
> 0 & \color {lightgreen} -2 & \color {cyan} 5 & \color {purple} 0 & -2 \\
> \color {lightgreen} 0 & \color {cyan} 9 & \color {purple} 8 & 0 & 9
> \end {array}
> \end {bmatrix}
> $$
> $$
> det(A) = \color {red} {3 \cdot (-2) \cdot 8} + \color {orange} {0} + \color {yellow} 0 - \color {lightgreen} {0} - \color {cyan} {3 \cdot 5 \cdot 9} - \color {purple} 0 = \color {white} -48 - 135 = -183
> $$

___
### Derivation

$$
\begin {gather}
det \left( \begin {bmatrix}
a & b & c \\
d & e & f \\
g & h & i
\end {bmatrix} \right) = \\\\
a \cdot
det \left( \begin {bmatrix}
e & f \\
h & i
\end {bmatrix} \right) - b \cdot
det \left( \begin {bmatrix}
d & f \\
g & i
\end {bmatrix} \right) + c \cdot
det \left( \begin {bmatrix}
d & e \\
g & h
\end {bmatrix} \right) = \\\\
= a(ei - hf) - b(di - fg) + c(dh - eg) = \\\\
= aei - hfa - idb + bfg + cdh - gec = \\\\
= \color {red} {aei} + \color {orange} {bfg} + \color {yellow} cdh - \color {lightgreen} {gec} - \color {cyan} {hfa} - \color {purple} idb
\end {gather}
$$
[[Test 2\|Test 2]]
