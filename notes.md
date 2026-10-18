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

### [Def] Equivalent representations
Representations $D$ and $D'$ of $G$ on $V$ are equivalent, written $D \simeq D'$, when

```math
\exists S \in GL(V),\ \forall g \in G:\ D'(g) = S^{-1} D(g)\, S
```

- The same $S$ is used for every $g \in G$ (a single change of basis).

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

### [Def] Direct sum
Let $D_1$ be a representation on $V_1$, and $D_2$ a representation on $V_2$.
$D_1 \oplus D_2$ is the representation on $V_1 \oplus V_2$ given by

```math
(D_1 \oplus D_2)(g) = \begin{pmatrix} D_1(g) & 0 \\ 0 & D_2(g) \end{pmatrix}
```

- $\dim (V_1 \oplus V_2) = \dim V_1 + \dim V_2$ (sum, not product; $\otimes$ gives the product)

### [Def] Completely reducible
$D$ is completely reducible when it is equivalent to a direct sum of irreducible representations:

```math
\exists S,\ \forall g \in G:\ S^{-1} D(g)\, S = D_1(g) \oplus D_2(g) \oplus \cdots,\quad D_j \text{ irreducible}
```

Equivalent form (for finite-dimensional $V$):
for every $G$-invariant subspace $W$, there exists a $G$-invariant subspace $W'$ with $V = W \oplus W'$.

- Remark: reducible $\not\Rightarrow$ completely reducible.
  Counterexample: $G = (\mathbb{R}, +)$, $V = \mathbb{C}^2$, $D(x) = \begin{pmatrix} 1 & x \\ 0 & 1 \end{pmatrix}$.
  $W = \mathrm{span}\lbrace (1,0)^T \rbrace$ is invariant.
  Any other line $\mathrm{span}\lbrace (\alpha, \beta)^T \rbrace$ with $\beta \neq 0$ is not invariant:
  for $x \neq 0$, $D(x)(\alpha, \beta)^T = (\alpha + x\beta, \beta)^T \notin \mathrm{span}\lbrace (\alpha, \beta)^T \rbrace$.

### [Thm] Representations of finite groups are completely reducible
- Proof: later (TODO)

### [Example] Decomposition of the regular representation of $Z_3$
$D$: regular representation of $Z_3$
```math
\omega = e^{2\pi i/3}, \quad
S = \frac{1}{3}\begin{pmatrix} 1 & 1 & 1 \\ 1 & \omega^2 & \omega \\ 1 & \omega & \omega^2 \end{pmatrix}
```



Hence

```math
  S^{-1} D(e)\, S = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix}, \quad
  S^{-1} D(a)\, S = \begin{pmatrix} 1 & 0 & 0 \\ 0 & \omega & 0 \\ 0 & 0 & \omega^2 \end{pmatrix}, \quad
  S^{-1} D(b)\, S = \begin{pmatrix} 1 & 0 & 0 \\ 0 & \omega^2 & 0 \\ 0 & 0 & \omega \end{pmatrix}
```

  $D \simeq D_1 \oplus D_2 \oplus D_3$, $\ 3 = 1 + 1 + 1$ ($D_j$ = $j$-th diagonal entry)
  - $D_1$: trivial representation $(1, 1, 1)$
  - $D_2$: the 1-dimensional representation above $(1, \omega, \omega^2)$
  - $D_3$: its complex conjugate $(1, \omega^2, \omega)$
- Invariant subspaces = spans of the columns of $S$
- Every block is $1 \times 1$ because $Z_3$ is abelian.