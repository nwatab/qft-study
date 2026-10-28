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
- For $D$ on $V$ and $D'$ on $V'$, equivalence needs an invertible linear $S: V' \to V$, which exists only if $\dim V = \dim V'$.
  So representations of different dimensions are never equivalent.

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

### [Example] $D(g) = I_n$
Any $G$, $V = \mathbb{C}^n$, $D(g) = I_n$ for all $g \in G$ (B1, B2 hold since $I_n I_n = I_n$).
- $n = 1$: irreducible. A 1-dimensional $V$ has no subspaces other than $\lbrace 0 \rbrace$ and $V$, so every 1-dimensional representation is irreducible.
- $n \geq 2$: reducible. $W = \mathrm{span}\lbrace e_1 \rbrace$ satisfies $\lbrace 0 \rbrace \neq W \neq V$ and $D(g)w = w \in W$.
- $I_1 \not\simeq I_n$ for $n \geq 2$ (different dimensions).

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
$D$: regular representation of $Z_3$.

```math
\omega = e^{2\pi i/3}, \quad
S = \frac{1}{3}\begin{pmatrix} 1 & 1 & 1 \\ 1 & \omega^2 & \omega \\ 1 & \omega & \omega^2 \end{pmatrix}
```

Then

```math
S^{-1} D(e)\, S = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix}, \quad
S^{-1} D(a)\, S = \begin{pmatrix} 1 & 0 & 0 \\ 0 & \omega & 0 \\ 0 & 0 & \omega^2 \end{pmatrix}, \quad
S^{-1} D(b)\, S = \begin{pmatrix} 1 & 0 & 0 \\ 0 & \omega^2 & 0 \\ 0 & 0 & \omega \end{pmatrix}
```

$D \simeq D_1 \oplus D_2 \oplus D_3$, $\ 3 = 1 + 1 + 1$ ($D_j$ = $j$-th diagonal entry; values listed for $(e, a, b)$)
- $D_1$: trivial representation $(1, 1, 1)$
- $D_2$: the 1-dimensional representation above $(1, \omega, \omega^2)$
- $D_3$: its complex conjugate $(1, \omega^2, \omega)$
- Invariant subspaces = spans of the columns of $S$
- Every block is $1 \times 1$ because $Z_3$ is abelian.

### [Example] $S_3$
$S_3$: the permutation group (symmetric group) on three objects.

```math
S_3 = \lbrace e, a_1, a_2, a_3, a_4, a_5 \rbrace, \quad
a_1 = (1,2,3),\ a_2 = (3,2,1),\ a_3 = (1,2),\ a_4 = (2,3),\ a_5 = (3,1)
```

- Notation: $(i, j, k)$ moves the object at location $i$ to $j$, the object at $j$ to $k$, and the object at $k$ to $i$. $(i, j)$ swaps the objects at $i$ and $j$.
- Product: $gh$ = apply $h$ first, then $g$.

Multiplication table (row × column):

| $\cdot$ | $e$ | $a_1$ | $a_2$ | $a_3$ | $a_4$ | $a_5$ |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| $e$ | $e$ | $a_1$ | $a_2$ | $a_3$ | $a_4$ | $a_5$ |
| $a_1$ | $a_1$ | $a_2$ | $e$ | $a_5$ | $a_3$ | $a_4$ |
| $a_2$ | $a_2$ | $e$ | $a_1$ | $a_4$ | $a_5$ | $a_3$ |
| $a_3$ | $a_3$ | $a_4$ | $a_5$ | $e$ | $a_1$ | $a_2$ |
| $a_4$ | $a_4$ | $a_5$ | $a_3$ | $a_2$ | $e$ | $a_1$ |
| $a_5$ | $a_5$ | $a_3$ | $a_4$ | $a_1$ | $a_2$ | $e$ |

#### 2-dimensional representation
Locations 1, 2, 3 = vertices of an equilateral triangle at angles $30^\circ, 150^\circ, 270^\circ$.
$D(g)$ = rotation or reflection of the plane that moves the objects as $g$ does.

```math
D(e) = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}, \quad
D(a_1) = \begin{pmatrix} -\frac{1}{2} & -\frac{\sqrt{3}}{2} \\ \frac{\sqrt{3}}{2} & -\frac{1}{2} \end{pmatrix}, \quad
D(a_2) = \begin{pmatrix} -\frac{1}{2} & \frac{\sqrt{3}}{2} \\ -\frac{\sqrt{3}}{2} & -\frac{1}{2} \end{pmatrix}
```

```math
D(a_3) = \begin{pmatrix} -1 & 0 \\ 0 & 1 \end{pmatrix}, \quad
D(a_4) = \begin{pmatrix} \frac{1}{2} & \frac{\sqrt{3}}{2} \\ \frac{\sqrt{3}}{2} & -\frac{1}{2} \end{pmatrix}, \quad
D(a_5) = \begin{pmatrix} \frac{1}{2} & -\frac{\sqrt{3}}{2} \\ -\frac{\sqrt{3}}{2} & -\frac{1}{2} \end{pmatrix}
```

- $D(a_1)$, $D(a_2)$: rotations by $\pm 120^\circ$. $D(a_3)$, $D(a_4)$, $D(a_5)$: reflections across the line through the fixed vertex.

#### [Claim] This 2-dimensional representation is irreducible
- If it were reducible, then by complete reducibility $D \simeq D_1 \oplus D_2$ with $D_1, D_2$ 1-dimensional, so all $D(g)$ would commute.
- But $a_1 a_3 = a_5 \neq a_4 = a_3 a_1$, so $D(a_1) D(a_3) \neq D(a_3) D(a_1)$.
- Remark: $S_3$ also has 1-dimensional irreducible representations (e.g. the trivial one). What non-abelian means is that not every irreducible representation is 1-dimensional.

#### [Example] The irreducible representations of $S_3$
Up to equivalence, $S_3$ has exactly 3 irreducible representations:

| | $e$ | $a_1, a_2$ | $a_3, a_4, a_5$ | dim |
|:-:|:-:|:-:|:-:|:-:|
| trivial | $1$ | $1$ | $1$ | 1 |
| sign | $1$ | $1$ | $-1$ | 1 |
| 2-dimensional (above) | $I_2$ | rotations | reflections | 2 |

1-dimensional ones are exactly trivial and sign. Let $D$ be 1-dimensional; numbers commute.
- $a_3 a_4 = a_1$, $a_4 a_3 = a_2$, so $D(a_1) = D(a_3)D(a_4) = D(a_4)D(a_3) = D(a_2)$.
- $a_1 a_1 = a_2$, so $D(a_1)^2 = D(a_2) = D(a_1)$, and $D(a_1) \neq 0$, so $D(a_1) = D(a_2) = 1$.
- $a_3 a_3 = e$, so $D(a_3) = \pm 1$.
- $a_1 a_3 = a_5$ and $a_1 a_5 = a_4$, so $D(a_5) = D(a_4) = D(a_3)$.
- Sign is a representation: by the table, a product of two of $a_3, a_4, a_5$ lies in $\lbrace e, a_1, a_2 \rbrace$, and a product of one of them with one of $e, a_1, a_2$ lies in $\lbrace a_3, a_4, a_5 \rbrace$.

Pairwise inequivalent:
- trivial $\not\simeq$ sign: in 1 dimension $S^{-1} x S = x$, so equivalent means equal, and they differ at $a_3$.
- 2-dimensional $\not\simeq$ either: different dimensions.

No others:
- $\sum_a n_a^2 = \lvert G \rvert$ over the irreducible representations ($n_a$ = dimension). Here $1^2 + 1^2 + 2^2 = 6 = \lvert S_3 \rvert$, so there is no room for another. Proof of the sum rule: later (TODO, Georgi 1.12).

### [Def] Subgroup
$H \subseteq G$ is a subgroup of $G$ when $H$ is a group under the multiplication of $G$.

### [Example] $Z_3 \subset S_3$
$\lbrace e, a_1, a_2 \rbrace$ is a subgroup of $S_3$, isomorphic to $Z_3$ ($a_1 \mapsto a$, $a_2 \mapsto b$).

### [Def] Right coset / Left coset
Let $H$ be a subgroup of $G$ and $g \in G$.
- Right coset: $Hg = \lbrace hg : h \in H \rbrace$
- Left coset: $gH = \lbrace gh : h \in H \rbrace$

### [Def] Normal subgroup
A subgroup $H$ of $G$ is normal (invariant), written $H \trianglelefteq G$, when

```math
\forall g \in G:\ gH = Hg
```

Equivalent form:

```math
\forall g \in G,\ \forall h \in H:\ g h g^{-1} \in H
```

### [Def] Factor group
If $H \trianglelefteq G$, the set of cosets $G/H = \lbrace Hg : g \in G \rbrace$ is a group under the product of sets
$AB = \lbrace ab : a \in A,\ b \in B \rbrace$:

```math
(Hg_1)(Hg_2) = H(g_1 H)g_2 = H(H g_1)g_2 = (HH)\,g_1 g_2 = H g_1 g_2
```

- The second equality uses $g_1 H = H g_1$ (normality).
- $HH = \lbrace h_1 h_2 : h_1, h_2 \in H \rbrace = H$:
  - $\subseteq$: $h_1, h_2 \in H \Rightarrow h_1 h_2 \in H$ (A1 for $H$).
  - $\supseteq$: $e \in H$, so every $h \in H$ is $h = eh \in HH$.
Group axioms for $G/H$ (all from $(Hg_1)(Hg_2) = Hg_1g_2$):
- A1: $(Hg_1)(Hg_2) = Hg_1g_2 \in G/H$.
- A2: $\big((Hg_1)(Hg_2)\big)(Hg_3) = H(g_1g_2)g_3 = Hg_1(g_2g_3) = (Hg_1)\big((Hg_2)(Hg_3)\big)$, by A2 in $G$.
- A3: the identity is $H = He$, since $(He)(Hg) = Hg = (Hg)(He)$.
- A4: the inverse of $Hg$ is $Hg^{-1}$, since $(Hg)(Hg^{-1}) = He = (Hg^{-1})(Hg)$.

### [Example] Normal subgroups of $S_3$
- TODO
