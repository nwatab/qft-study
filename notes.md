### [Def] Group
- A1 : $\forall f, g \in G,\ fg \in G$
- A2 : $\forall f, g, h \in G,\ f(gh) = (fg)h$
- A3 : $\exists e \in G,\ \forall f \in G,\ ef = fe = f$
- A4 : $\forall f \in G,\ \exists f^{-1} \in G,\ ff^{-1} = f^{-1}f = e$

### [Def] Representation
Let $V$ be a vector space. A representation of $G$ on $V$ is a mapping $D$
from the elements of $G$ to linear operators on $V$ with the following properties:

- B1 : $D(e) = 1$
- B2 : $\forall g_1, g_2 \in G,\ D(g_1)D(g_2) = D(g_1 g_2)$

(B1, B2: $D$ is a group homomorphism.)

### [Def] Regular representation
- $\lbrace \lvert g\rangle : g \in G \rbrace$ is an orthonormal basis of $V$, so $\dim V = \lvert G\rvert$
- $\forall g_1, g_2 \in G,\ D(g_2)\lvert g_1\rangle = \lvert g_2 g_1\rangle$

### [Example] $Z_3$

Multiplication table (row × column):

| $\cdot$ | $e$ | $a$ | $b$ |
|:-:|:-:|:-:|:-:|
| $e$ | $e$ | $a$ | $b$ |
| $a$ | $a$ | $b$ | $e$ |
| $b$ | $b$ | $e$ | $a$ |

$ab = ba = e$

#### 1-dimensional representation

```math
D(e) = 1, \quad D(a) = e^{2\pi i/3}, \quad D(b) = e^{4\pi i/3}
```

#### Regular representation
In the basis $(\lvert e\rangle, \lvert a\rangle, \lvert b\rangle)$:

```math
D(e) = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix}, \quad
D(a) = \begin{pmatrix} 0 & 0 & 1 \\ 1 & 0 & 0 \\ 0 & 1 & 0 \end{pmatrix}, \quad
D(b) = \begin{pmatrix} 0 & 1 & 0 \\ 0 & 0 & 1 \\ 1 & 0 & 0 \end{pmatrix}
```

### [Def] Invariant subspace
A linear subspace $W \subseteq V$ is $G$-invariant when

```math
\forall g \in G,\ \forall w \in W:\ D(g)w \in W
```

### [Def] Reducible / Irreducible
- **Reducible**: there exists a $G$-invariant subspace $W$ with $\lbrace 0 \rbrace \neq W \neq V$.
- **Irreducible**: $V \neq \lbrace 0 \rbrace$ and the only $G$-invariant subspaces are $\lbrace 0 \rbrace$ and $V$.
