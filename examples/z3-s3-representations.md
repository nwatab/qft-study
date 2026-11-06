# Representations of $Z_3$ and $S_3$: examples

All entries were checked numerically: each $D$ satisfies the group table, and $S^{-1} D(g) S$ has the shown form for every $g$.
Matrices are in the basis $e$ (column $k$ = image of $e_k$).

## $Z_3 = \lbrace e, a, a^2 \rbrace$

$\omega = e^{2\pi i/3}$. Irreducible representations: $D_k(a) = \omega^k$ ($k = 0, 1, 2$). $D(e) = I$, $D(a^2) = D(a)^2$.

### Representations

| # | $V$ | $[D(e)]_e$ | $[D(a)]_e$ | $[D(a^2)]_e$ |
|---|---|---|---|---|
| 1 | $\mathbb{C}^2$ | $I_2$ | $\left(\begin{smallmatrix}0&-1\\1&-1\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}-1&1\\-1&0\end{smallmatrix}\right)$ |
| 2 | $\mathbb{C}^2$ | $I_2$ | $\left(\begin{smallmatrix}0&-\omega\\\omega&-\omega\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}-\omega^2&\omega^2\\-\omega^2&0\end{smallmatrix}\right)$ |
| 3 | $\mathbb{C}^2$ | $I_2$ | $\left(\begin{smallmatrix}0&-\omega^2\\\omega^2&-\omega^2\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}-\omega&\omega\\-\omega&0\end{smallmatrix}\right)$ |
| 4 | $\mathbb{C}^3$ | $I_3$ | $\left(\begin{smallmatrix}0&0&1\\1&0&0\\0&1&0\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}0&1&0\\0&0&1\\1&0&0\end{smallmatrix}\right)$ |
| 5 | $\mathbb{C}^3$ | $I_3$ | $\left(\begin{smallmatrix}0&-1&0\\1&-1&0\\0&0&\omega\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}-1&1&0\\-1&0&0\\0&0&\omega^2\end{smallmatrix}\right)$ |
| 6 | $\mathbb{C}^3$ | $I_3$ | $\left(\begin{smallmatrix}0&-\omega^2&0\\\omega^2&-\omega^2&0\\0&0&1\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}-\omega&\omega&0\\-\omega&0&0\\0&0&1\end{smallmatrix}\right)$ |
| 7 | $\mathbb{C}^4$ | $I_4$ | $\left(\begin{smallmatrix}0&0&1&0\\1&0&0&0\\0&1&0&0\\0&0&0&1\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}0&1&0&0\\0&0&1&0\\1&0&0&0\\0&0&0&1\end{smallmatrix}\right)$ |
| 8 | $\mathbb{C}^6$ | $I_6$ | $\left(\begin{smallmatrix}0&0&1&0&0&0\\1&0&0&0&0&0\\0&1&0&0&0&0\\0&0&0&0&0&1\\0&0&0&1&0&0\\0&0&0&0&1&0\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}0&1&0&0&0&0\\0&0&1&0&0&0\\1&0&0&0&0&0\\0&0&0&0&1&0\\0&0&0&0&0&1\\0&0&0&1&0&0\end{smallmatrix}\right)$ |
| 9 | $\mathbb{C}^2$ | $I_2$ | $\left(\begin{smallmatrix}-\tfrac12&-\tfrac{\sqrt3}{2}\\\tfrac{\sqrt3}{2}&-\tfrac12\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}-\tfrac12&\tfrac{\sqrt3}{2}\\-\tfrac{\sqrt3}{2}&-\tfrac12\end{smallmatrix}\right)$ |

### Diagonalization (columns of $S$ = common eigenvectors)

| # | $S$ | $S^{-1}D(e)S$ | $S^{-1}D(a)S$ | $S^{-1}D(a^2)S$ | Decomposition |
|---|---|---|---|---|---|
| 1 | $\left(\begin{smallmatrix}1&1\\-\omega&-\omega^2\end{smallmatrix}\right)$ | $I_2$ | $\mathrm{diag}(\omega, \omega^2)$ | $\mathrm{diag}(\omega^2, \omega)$ | $D_1\oplus D_2$ |
| 2 | $\left(\begin{smallmatrix}1&1\\-\omega&-\omega^2\end{smallmatrix}\right)$ | $I_2$ | $\mathrm{diag}(\omega^2, 1)$ | $\mathrm{diag}(\omega, 1)$ | $D_2\oplus D_0$ |
| 3 | $\left(\begin{smallmatrix}1&1\\-\omega&-\omega^2\end{smallmatrix}\right)$ | $I_2$ | $\mathrm{diag}(1, \omega)$ | $\mathrm{diag}(1, \omega^2)$ | $D_0\oplus D_1$ |
| 4 | $\left(\begin{smallmatrix}1&1&1\\1&\omega^2&\omega\\1&\omega&\omega^2\end{smallmatrix}\right)$ | $I_3$ | $\mathrm{diag}(1, \omega, \omega^2)$ | $\mathrm{diag}(1, \omega^2, \omega)$ | $D_0\oplus D_1\oplus D_2$ |
| 5 | $\left(\begin{smallmatrix}1&1&0\\-\omega&-\omega^2&0\\0&0&1\end{smallmatrix}\right)$ | $I_3$ | $\mathrm{diag}(\omega, \omega^2, \omega)$ | $\mathrm{diag}(\omega^2, \omega, \omega^2)$ | $D_1\oplus D_2\oplus D_1$ |
| 6 | $\left(\begin{smallmatrix}1&1&0\\-\omega&-\omega^2&0\\0&0&1\end{smallmatrix}\right)$ | $I_3$ | $\mathrm{diag}(1, \omega, 1)$ | $\mathrm{diag}(1, \omega^2, 1)$ | $D_0\oplus D_1\oplus D_0$ |
| 7 | $\left(\begin{smallmatrix}1&1&1&0\\1&\omega^2&\omega&0\\1&\omega&\omega^2&0\\0&0&0&1\end{smallmatrix}\right)$ | $I_4$ | $\mathrm{diag}(1, \omega, \omega^2, 1)$ | $\mathrm{diag}(1, \omega^2, \omega, 1)$ | $D_0\oplus D_1\oplus D_2\oplus D_0$ |
| 8 | $\left(\begin{smallmatrix}1&1&1&0&0&0\\1&\omega^2&\omega&0&0&0\\1&\omega&\omega^2&0&0&0\\0&0&0&1&1&1\\0&0&0&1&\omega^2&\omega\\0&0&0&1&\omega&\omega^2\end{smallmatrix}\right)$ | $I_6$ | $\mathrm{diag}(1, \omega, \omega^2, 1, \omega, \omega^2)$ | $\mathrm{diag}(1, \omega^2, \omega, 1, \omega^2, \omega)$ | $D_0\oplus D_1\oplus D_2\oplus D_0\oplus D_1\oplus D_2$ |
| 9 | $\left(\begin{smallmatrix}1&1\\-i&i\end{smallmatrix}\right)$ | $I_2$ | $\mathrm{diag}(\omega, \omega^2)$ | $\mathrm{diag}(\omega^2, \omega)$ | $D_1\oplus D_2$ |


## $S_3$

Elements and $D_{\mathrm{perm}}(g) \lvert v_i \rangle = \lvert v_{g(i)} \rangle$ follow the conventions in `notes.md`.
Irreducible representations: $\mathrm{triv}$, $\mathrm{sign}$, $\mathrm{2D}$ (the matrices of #1).

### Representations (dimension $\le 4$)

| # | $V$ | Content | $e$ | $a_1$ | $a_2$ | $a_3$ | $a_4$ | $a_5$ |
|---|---|---|---|---|---|---|---|---|
| 1 | $\mathbb{C}^2$ | $\mathrm{2D}$ itself (irreducible) | $\left(\begin{smallmatrix}1&0\\0&1\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}-\tfrac12&-\tfrac{\sqrt3}{2}\\\tfrac{\sqrt3}{2}&-\tfrac12\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}-\tfrac12&\tfrac{\sqrt3}{2}\\-\tfrac{\sqrt3}{2}&-\tfrac12\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}-1&0\\0&1\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}\tfrac12&\tfrac{\sqrt3}{2}\\\tfrac{\sqrt3}{2}&-\tfrac12\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}\tfrac12&-\tfrac{\sqrt3}{2}\\-\tfrac{\sqrt3}{2}&-\tfrac12\end{smallmatrix}\right)$ |
| 2 | $\mathbb{C}^2$ | two orientations (counterclockwise / clockwise) | $\left(\begin{smallmatrix}1&0\\0&1\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}1&0\\0&1\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}1&0\\0&1\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}0&1\\1&0\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}0&1\\1&0\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}0&1\\1&0\end{smallmatrix}\right)$ |
| 3 | $\mathbb{C}^3$ | triangle vertices $D_{\mathrm{perm}}$ | $\left(\begin{smallmatrix}1&0&0\\0&1&0\\0&0&1\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}0&0&1\\1&0&0\\0&1&0\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}0&1&0\\0&0&1\\1&0&0\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}0&1&0\\1&0&0\\0&0&1\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}1&0&0\\0&0&1\\0&1&0\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}0&0&1\\0&1&0\\1&0&0\end{smallmatrix}\right)$ |
| 4 | $\mathbb{C}^3$ | $\mathrm{sign}(g)\,D_{\mathrm{perm}}(g)$ | $\left(\begin{smallmatrix}1&0&0\\0&1&0\\0&0&1\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}0&0&1\\1&0&0\\0&1&0\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}0&1&0\\0&0&1\\1&0&0\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}0&-1&0\\-1&0&0\\0&0&-1\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}-1&0&0\\0&0&-1\\0&-1&0\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}0&0&-1\\0&-1&0\\-1&0&0\end{smallmatrix}\right)$ |
| 5 | $\mathbb{C}^4$ | $\mathrm{2D}\otimes\mathrm{2D}$ (two particles) | $\left(\begin{smallmatrix}1&0&0&0\\0&1&0&0\\0&0&1&0\\0&0&0&1\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}\tfrac14&\tfrac{\sqrt3}{4}&\tfrac{\sqrt3}{4}&\tfrac34\\-\tfrac{\sqrt3}{4}&\tfrac14&-\tfrac34&\tfrac{\sqrt3}{4}\\-\tfrac{\sqrt3}{4}&-\tfrac34&\tfrac14&\tfrac{\sqrt3}{4}\\\tfrac34&-\tfrac{\sqrt3}{4}&-\tfrac{\sqrt3}{4}&\tfrac14\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}\tfrac14&-\tfrac{\sqrt3}{4}&-\tfrac{\sqrt3}{4}&\tfrac34\\\tfrac{\sqrt3}{4}&\tfrac14&-\tfrac34&-\tfrac{\sqrt3}{4}\\\tfrac{\sqrt3}{4}&-\tfrac34&\tfrac14&-\tfrac{\sqrt3}{4}\\\tfrac34&\tfrac{\sqrt3}{4}&\tfrac{\sqrt3}{4}&\tfrac14\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}1&0&0&0\\0&-1&0&0\\0&0&-1&0\\0&0&0&1\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}\tfrac14&\tfrac{\sqrt3}{4}&\tfrac{\sqrt3}{4}&\tfrac34\\\tfrac{\sqrt3}{4}&-\tfrac14&\tfrac34&-\tfrac{\sqrt3}{4}\\\tfrac{\sqrt3}{4}&\tfrac34&-\tfrac14&-\tfrac{\sqrt3}{4}\\\tfrac34&-\tfrac{\sqrt3}{4}&-\tfrac{\sqrt3}{4}&\tfrac14\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}\tfrac14&-\tfrac{\sqrt3}{4}&-\tfrac{\sqrt3}{4}&\tfrac34\\-\tfrac{\sqrt3}{4}&-\tfrac14&\tfrac34&\tfrac{\sqrt3}{4}\\-\tfrac{\sqrt3}{4}&\tfrac34&-\tfrac14&\tfrac{\sqrt3}{4}\\\tfrac34&\tfrac{\sqrt3}{4}&\tfrac{\sqrt3}{4}&\tfrac14\end{smallmatrix}\right)$ |

### Representations (dimension 6)

| # | $V$ | Content | $D(g)$ on the basis |
|---|---|---|---|
| 6 | $\mathbb{C}^6$, basis $\lvert h \rangle$, $h \in S_3$ | conjugation | $D(g) \lvert h \rangle = \lvert g h g^{-1} \rangle$ |
| 7 | $\mathbb{C}^6$, basis $\lvert v_i \rangle \otimes \lvert s \rangle$, $\lvert v_i \rangle \otimes \lvert p \rangle$ | vertices $\times$ two levels | $D(g) = D_{\mathrm{perm}}(g) \otimes I_2$ |
| 8 | $\mathbb{C}^6$, basis $\lvert h \rangle$, $h \in S_3$ | regular | $D(g) \lvert h \rangle = \lvert g h \rangle$ |

### Block diagonalization ($S^{-1} D(g) S$ as a direct sum of blocks)

| # | $S$ | $e$ | $a_1$ | $a_2$ | $a_3$ | $a_4$ | $a_5$ | Decomposition |
|---|---|---|---|---|---|---|---|---|
| 1 | $\left(\begin{smallmatrix}1&0\\0&1\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}1&0\\0&1\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}-\tfrac12&-\tfrac{\sqrt3}{2}\\\tfrac{\sqrt3}{2}&-\tfrac12\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}-\tfrac12&\tfrac{\sqrt3}{2}\\-\tfrac{\sqrt3}{2}&-\tfrac12\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}-1&0\\0&1\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}\tfrac12&\tfrac{\sqrt3}{2}\\\tfrac{\sqrt3}{2}&-\tfrac12\end{smallmatrix}\right)$ | $\left(\begin{smallmatrix}\tfrac12&-\tfrac{\sqrt3}{2}\\-\tfrac{\sqrt3}{2}&-\tfrac12\end{smallmatrix}\right)$ | $\mathrm{2D}$ |
| 2 | $\left(\begin{smallmatrix}1&1\\1&-1\end{smallmatrix}\right)$ | $1\oplus 1$ | $1\oplus 1$ | $1\oplus 1$ | $1\oplus (-1)$ | $1\oplus (-1)$ | $1\oplus (-1)$ | $\mathrm{triv}\oplus\mathrm{sign}$ |
| 3 | $\left(\begin{smallmatrix}\tfrac{1}{\sqrt3}&\tfrac{1}{\sqrt2}&\tfrac{1}{\sqrt6}\\\tfrac{1}{\sqrt3}&-\tfrac{1}{\sqrt2}&\tfrac{1}{\sqrt6}\\\tfrac{1}{\sqrt3}&0&-\tfrac{2}{\sqrt6}\end{smallmatrix}\right)$ | $1\oplus \left(\begin{smallmatrix}1&0\\0&1\end{smallmatrix}\right)$ | $1\oplus \left(\begin{smallmatrix}-\tfrac12&-\tfrac{\sqrt3}{2}\\\tfrac{\sqrt3}{2}&-\tfrac12\end{smallmatrix}\right)$ | $1\oplus \left(\begin{smallmatrix}-\tfrac12&\tfrac{\sqrt3}{2}\\-\tfrac{\sqrt3}{2}&-\tfrac12\end{smallmatrix}\right)$ | $1\oplus \left(\begin{smallmatrix}-1&0\\0&1\end{smallmatrix}\right)$ | $1\oplus \left(\begin{smallmatrix}\tfrac12&\tfrac{\sqrt3}{2}\\\tfrac{\sqrt3}{2}&-\tfrac12\end{smallmatrix}\right)$ | $1\oplus \left(\begin{smallmatrix}\tfrac12&-\tfrac{\sqrt3}{2}\\-\tfrac{\sqrt3}{2}&-\tfrac12\end{smallmatrix}\right)$ | $\mathrm{triv}\oplus \mathrm{2D}$ |
| 4 | $\left(\begin{smallmatrix}\tfrac{1}{\sqrt3}&\tfrac{1}{\sqrt6}&-\tfrac{1}{\sqrt2}\\\tfrac{1}{\sqrt3}&\tfrac{1}{\sqrt6}&\tfrac{1}{\sqrt2}\\\tfrac{1}{\sqrt3}&-\tfrac{2}{\sqrt6}&0\end{smallmatrix}\right)$ | $1\oplus \left(\begin{smallmatrix}1&0\\0&1\end{smallmatrix}\right)$ | $1\oplus \left(\begin{smallmatrix}-\tfrac12&-\tfrac{\sqrt3}{2}\\\tfrac{\sqrt3}{2}&-\tfrac12\end{smallmatrix}\right)$ | $1\oplus \left(\begin{smallmatrix}-\tfrac12&\tfrac{\sqrt3}{2}\\-\tfrac{\sqrt3}{2}&-\tfrac12\end{smallmatrix}\right)$ | $(-1)\oplus \left(\begin{smallmatrix}-1&0\\0&1\end{smallmatrix}\right)$ | $(-1)\oplus \left(\begin{smallmatrix}\tfrac12&\tfrac{\sqrt3}{2}\\\tfrac{\sqrt3}{2}&-\tfrac12\end{smallmatrix}\right)$ | $(-1)\oplus \left(\begin{smallmatrix}\tfrac12&-\tfrac{\sqrt3}{2}\\-\tfrac{\sqrt3}{2}&-\tfrac12\end{smallmatrix}\right)$ | $\mathrm{sign}\oplus \mathrm{2D}$ |
| 5 | $\left(\begin{smallmatrix}\tfrac{1}{\sqrt2}&0&0&\tfrac{1}{\sqrt2}\\0&\tfrac{1}{\sqrt2}&\tfrac{1}{\sqrt2}&0\\0&-\tfrac{1}{\sqrt2}&\tfrac{1}{\sqrt2}&0\\\tfrac{1}{\sqrt2}&0&0&-\tfrac{1}{\sqrt2}\end{smallmatrix}\right)$ | $1\oplus 1\oplus \left(\begin{smallmatrix}1&0\\0&1\end{smallmatrix}\right)$ | $1\oplus 1\oplus \left(\begin{smallmatrix}-\tfrac12&-\tfrac{\sqrt3}{2}\\\tfrac{\sqrt3}{2}&-\tfrac12\end{smallmatrix}\right)$ | $1\oplus 1\oplus \left(\begin{smallmatrix}-\tfrac12&\tfrac{\sqrt3}{2}\\-\tfrac{\sqrt3}{2}&-\tfrac12\end{smallmatrix}\right)$ | $1\oplus (-1)\oplus \left(\begin{smallmatrix}-1&0\\0&1\end{smallmatrix}\right)$ | $1\oplus (-1)\oplus \left(\begin{smallmatrix}\tfrac12&\tfrac{\sqrt3}{2}\\\tfrac{\sqrt3}{2}&-\tfrac12\end{smallmatrix}\right)$ | $1\oplus (-1)\oplus \left(\begin{smallmatrix}\tfrac12&-\tfrac{\sqrt3}{2}\\-\tfrac{\sqrt3}{2}&-\tfrac12\end{smallmatrix}\right)$ | $\mathrm{triv}\oplus\mathrm{sign}\oplus \mathrm{2D}$ |
| 6 | $\lvert e\rangle$, $\tfrac{\lvert a_1\rangle+\lvert a_2\rangle}{\sqrt2}$, $\tfrac{\lvert a_1\rangle-\lvert a_2\rangle}{\sqrt2}$, $\tfrac{\lvert a_3\rangle+\lvert a_4\rangle+\lvert a_5\rangle}{\sqrt3}$, $\tfrac{\lvert a_4\rangle-\lvert a_5\rangle}{\sqrt2}$, $\tfrac{-2\lvert a_3\rangle+\lvert a_4\rangle+\lvert a_5\rangle}{\sqrt6}$ | $1\oplus 1\oplus 1\oplus 1\oplus \mathrm{2D}(e)$ | $1\oplus 1\oplus 1\oplus 1\oplus \mathrm{2D}(a_1)$ | $1\oplus 1\oplus 1\oplus 1\oplus \mathrm{2D}(a_2)$ | $1\oplus 1\oplus (-1)\oplus 1\oplus \mathrm{2D}(a_3)$ | $1\oplus 1\oplus (-1)\oplus 1\oplus \mathrm{2D}(a_4)$ | $1\oplus 1\oplus (-1)\oplus 1\oplus \mathrm{2D}(a_5)$ | $3\,\mathrm{triv}\oplus\mathrm{sign}\oplus\mathrm{2D}$ |
| 7 | $u_0\otimes\lvert s\rangle$, $u_0\otimes\lvert p\rangle$, $u_1\otimes\lvert s\rangle$, $u_2\otimes\lvert s\rangle$, $u_1\otimes\lvert p\rangle$, $u_2\otimes\lvert p\rangle$ ($u_i$: columns of $S$ in #3) | $1\oplus 1\oplus \mathrm{2D}(e)\oplus \mathrm{2D}(e)$ | $1\oplus 1\oplus \mathrm{2D}(a_1)\oplus \mathrm{2D}(a_1)$ | $1\oplus 1\oplus \mathrm{2D}(a_2)\oplus \mathrm{2D}(a_2)$ | $1\oplus 1\oplus \mathrm{2D}(a_3)\oplus \mathrm{2D}(a_3)$ | $1\oplus 1\oplus \mathrm{2D}(a_4)\oplus \mathrm{2D}(a_4)$ | $1\oplus 1\oplus \mathrm{2D}(a_5)\oplus \mathrm{2D}(a_5)$ | $2\,\mathrm{triv}\oplus 2\cdot\mathrm{2D}$ |
| 8 | $\tfrac{1}{\sqrt6}\sum_g\lvert g\rangle$, $\tfrac{1}{\sqrt6}\sum_g\mathrm{sign}(g)\lvert g\rangle$, $\tfrac{1}{\sqrt3}\sum_g \mathrm{2D}(g)_{jk}\lvert g\rangle$ (in the order $(j,k)=(1,1),(2,1),(1,2),(2,2)$) | $1\oplus 1\oplus \mathrm{2D}(e)\oplus \mathrm{2D}(e)$ | $1\oplus 1\oplus \mathrm{2D}(a_1)\oplus \mathrm{2D}(a_1)$ | $1\oplus 1\oplus \mathrm{2D}(a_2)\oplus \mathrm{2D}(a_2)$ | $1\oplus (-1)\oplus \mathrm{2D}(a_3)\oplus \mathrm{2D}(a_3)$ | $1\oplus (-1)\oplus \mathrm{2D}(a_4)\oplus \mathrm{2D}(a_4)$ | $1\oplus (-1)\oplus \mathrm{2D}(a_5)\oplus \mathrm{2D}(a_5)$ | $\mathrm{triv}\oplus\mathrm{sign}\oplus 2\cdot\mathrm{2D}$ |

