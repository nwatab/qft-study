### [Def] Group
- A1 : $\forall f, g \in G,\ fg \in G$
- A2 : $\forall f, g, h \in G,\ f(gh) = (fg)h$
- A3 : $\exists e \in G,\ \forall f \in G,\ ef = fe = f$
- A4 : $\forall f \in G,\ \exists f^{-1} \in G,\ ff^{-1} = f^{-1}f = e$

### [Def] Representation
A representation of $G$ is a mapping $D$ of the elements of $G$ onto a set of linear operators with the following properties:

- B1 : $D(e) = 1$
- B2 : $D(g_1)D(g_2) = D(g_1 g_2)$

### [Example] $Z_3$

Multiplication table (row × column):

| $\cdot$ | $e$ | $a$ | $b$ |
|:-:|:-:|:-:|:-:|
| $e$ | $e$ | $a$ | $b$ |
| $a$ | $a$ | $b$ | $e$ |
| $b$ | $b$ | $e$ | $a$ |

$ab = ba = e$

#### 1-dimensional representation

$$
D(e) = 1, \quad D(a) = e^{2\pi i/3}, \quad D(b) = e^{4\pi i/3}
$$

#### Regular representation

$$
D(e) = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix}, \quad
D(a) = \begin{pmatrix} 0 & 0 & 1 \\ 1 & 0 & 0 \\ 0 & 1 & 0 \end{pmatrix}, \quad
D(b) = \begin{pmatrix} 0 & 1 & 0 \\ 0 & 0 & 1 \\ 1 & 0 & 0 \end{pmatrix}
$$