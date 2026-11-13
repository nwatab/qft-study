## 群と表現

### [定義] 群
- A1 : $`\forall f, g \in G,\ fg \in G`$
- A2 : $`\forall f, g, h \in G,\ f(gh) = (fg)h`$
- A3 : $`\exists e \in G,\ \forall f \in G,\ ef = fe = f`$
- A4 : $`\forall f \in G,\ \exists f^{-1} \in G,\ ff^{-1} = f^{-1}f = e`$

### [定義] 群準同型
$`G, H`$ を群とする。写像 $`\varphi: G \to H`$ が次を満たすとき、群準同型という。

```math
\forall g_1, g_2 \in G:\ \varphi(g_1 g_2) = \varphi(g_1)\, \varphi(g_2)
```

- 左辺の積は $`G`$ の積、右辺の積は $`H`$ の積。
- 単位元は単位元へ移る：$`\varphi(e_G) = \varphi(e_G e_G) = \varphi(e_G)\varphi(e_G)`$ の両辺に $`\varphi(e_G)^{-1}`$ を掛けて $`\varphi(e_G) = e_H`$。
- 逆元は逆元へ移る：$`\varphi(g)\varphi(g^{-1}) = \varphi(e_G) = e_H`$ より $`\varphi(g^{-1}) = \varphi(g)^{-1}`$。
- 全単射な群準同型を同型という。

### [定義] 一般線形群 $`GL(V)`$
$`V`$ をベクトル空間とする。$`V`$ 上の可逆な線形演算子全体を $`GL(V)`$ と書く。$`GL(V)`$ は合成について群になり、これを一般線形群という。

群であることを確かめる。$`A, B \in GL(V)`$ とする。
- A1：$`AB`$ は線形で、逆 $`B^{-1}A^{-1}`$ をもつ。
- A2：写像の合成は結合的。
- A3：恒等写像 $`1`$ は線形で可逆。
- A4：$`A^{-1}`$ は可逆（逆は $`A`$）で、線形でもある。$`x = A^{-1}u`$、$`y = A^{-1}w`$ とおくと $`A(\alpha x + \beta y) = \alpha u + \beta w`$ より $`A^{-1}(\alpha u + \beta w) = \alpha A^{-1}u + \beta A^{-1}w`$。

補足：
- $`V = ℂ^n`$ のとき、$`GL(n, ℂ) = \lbrace A \in ℂ^{n \times n} \mid \det A \neq 0 \rbrace`$。
- 和では閉じない（$`1 + (-1) = 0`$ は可逆でない）。群の演算は合成（積）だけ。

### [定義] 表現
$`V`$ をベクトル空間とする。$`G`$ の $`V`$ 上の表現とは、$`G`$ の元から $`V`$ 上の線形演算子への写像 $`D`$ で、次を満たすもの：

- B1 : $`D(e) = 1`$
- B2 : $`\forall g_1, g_2 \in G,\ D(g_1)D(g_2) = D(g_1 g_2)`$

B1, B2 より $`D(g)D(g^{-1}) = D(e) = 1`$ なので、$`D(g)`$ は可逆である。言い換えると、表現とは群準同型 $`D: G \to GL(V)`$ のことである。

正確には、表現は組 $`(V, D)`$ である。物理では $`D`$ だけを、数学では $`V`$ だけを指して「表現」と呼ぶことが多い。

### [定義] 同値な表現 $`\simeq`$
$`V`$ 上の $`G`$ の表現 $`D`$ と $`D'`$ は、次を満たすとき同値であるといい、$`D \simeq D'`$ と書く。

```math
\exists S \in GL(V),\ \forall g \in G:\ D'(g) = S^{-1} D(g)\, S
```

- 全ての $`g \in G`$ に同じ $`S`$ を使う（基底の取り替えは1回）。
- $`V`$ 上の $`D`$ と $`V'`$ 上の $`D'`$ が同値であるには、可逆な線形写像 $`S: V' \to V`$ が必要で、それは $`\dim V = \dim V'`$ のときにしか存在しない。
  したがって、次元の異なる表現は同値にならない。

### [定義] 正則表現
- $`\lbrace \lvert g\rangle \mid g \in G \rbrace`$ は $`V`$ の正規直交基底。したがって $`\dim V = \lvert G\rvert`$
- $`\forall g_1, g_2 \in G,\ D(g_2)\lvert g_1\rangle = \lvert g_2 g_1\rangle`$

### [例] $`Z_3`$

群表（行 × 列）：

| $`\cdot`$ | $`e`$ | $`a`$ | $`b`$ |
|:-:|:-:|:-:|:-:|
| $`e`$ | $`e`$ | $`a`$ | $`b`$ |
| $`a`$ | $`a`$ | $`b`$ | $`e`$ |
| $`b`$ | $`b`$ | $`e`$ | $`a`$ |

$`ab = ba = e`$

### [例] $`Z_3`$ の1次元表現

```math
D(e) = 1, \quad D(a) = e^{2\pi i/3}, \quad D(b) = e^{4\pi i/3}
```

### [例] $`Z_3`$ の正則表現
基底 $`(\lvert e\rangle, \lvert a\rangle, \lvert b\rangle)`$ で：

```math
D(e) = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix}, \quad
D(a) = \begin{pmatrix} 0 & 0 & 1 \\ 1 & 0 & 0 \\ 0 & 1 & 0 \end{pmatrix}, \quad
D(b) = \begin{pmatrix} 0 & 1 & 0 \\ 0 & 0 & 1 \\ 1 & 0 & 0 \end{pmatrix}
```

## 既約表現と完全可約性

### [記法] $`\mathrm{span}`$
$`V`$ を $`ℂ`$ 上のベクトル空間、$`v_1, \dots, v_k \in V`$ とする。$`v_1, \dots, v_k`$ の線形結合全体（$`v_1, \dots, v_k`$ が張る部分空間、線形包）を次のように書く。

```math
\mathrm{span}\lbrace v_1, \dots, v_k \rbrace = \lbrace c_1 v_1 + \cdots + c_k v_k \mid c_1, \dots, c_k \in ℂ \rbrace
```

- 係数は $`V`$ と同じ体（ここでは $`ℂ`$）からとる。

### [定義] 不変部分空間
線形部分空間 $`W \subseteq V`$ は、次を満たすとき $`G`$ 不変であるという。

```math
\forall g \in G,\ \forall w \in W:\ D(g)w \in W
```

### [定義] 可約 / 既約
- **可約**：$`\lbrace 0 \rbrace \neq W \neq V`$ となる $`G`$ 不変部分空間 $`W`$ が存在する。
- **既約**：$`V \neq \lbrace 0 \rbrace`$ で、$`G`$ 不変部分空間は $`\lbrace 0 \rbrace`$ と $`V`$ だけである。

### [例] $`D(g) = I_n`$
任意の $`G`$、$`V = ℂ^n`$、全ての $`g \in G`$ で $`D(g) = I_n`$（$`I_n I_n = I_n`$ なので B1, B2 を満たす）。
- $`n = 1`$：既約。1次元の $`V`$ には $`\lbrace 0 \rbrace`$ と $`V`$ 以外の部分空間がないので、1次元の表現はすべて既約である。
- $`n \geq 2`$：可約。$`W = \mathrm{span}\lbrace e_1 \rbrace`$ は $`\lbrace 0 \rbrace \neq W \neq V`$ を満たし、$`D(g)w = w \in W`$。
- $`n \geq 2`$ のとき $`I_1 \not\simeq I_n`$（次元が違う）。

### [定義] 直和 $`\oplus`$
$`D_1`$ を $`V_1`$ 上の表現、$`D_2`$ を $`V_2`$ 上の表現とする。
$`D_1 \oplus D_2`$ は、次で定まる $`V_1 \oplus V_2`$ 上の表現である。

```math
(D_1 \oplus D_2)(g) = \begin{pmatrix} D_1(g) & 0 \\ 0 & D_2(g) \end{pmatrix}
```

- $`\dim (V_1 \oplus V_2) = \dim V_1 + \dim V_2`$（積ではなく和。積になるのは下のテンソル積 $`\otimes`$）

### [定義] テンソル積 $`\otimes`$
$`V`$ の基底を $`e_1, \dots, e_m`$、$`W`$ の基底を $`f_1, \dots, f_n`$ とする。$`V \otimes W`$ は、全ての組 $`e_i \otimes f_j`$ を基底とするベクトル空間である。

- $`\dim (V \otimes W) = \dim V \cdot \dim W`$（和ではなく積）
- ベクトルのテンソル積は、各成分について線形に展開する：

```math
v = \sum_i a_i e_i,\quad w = \sum_j b_j f_j \quad\Rightarrow\quad v \otimes w = \sum_{i,j} a_i b_j\, e_i \otimes f_j
```

- 線形写像 $`A: V \to V`$、$`B: W \to W`$ のテンソル積 $`A \otimes B`$ は $`(A \otimes B)(v \otimes w) = Av \otimes Bw`$ で定まる。基底を $`e_1 \otimes f_1, \dots, e_1 \otimes f_n, e_2 \otimes f_1, \dots`$ の順に並べると、行列はクロネッカー積になる：

```math
A \otimes B = \begin{pmatrix} a_{11} B & \cdots & a_{1m} B \\ \vdots & \ddots & \vdots \\ a_{m1} B & \cdots & a_{mm} B \end{pmatrix}
```

- 定義から $`(A \otimes B)(C \otimes D) = AC \otimes BD`$。

$`D_1`$ を $`V_1`$ 上の表現、$`D_2`$ を $`V_2`$ 上の表現とする。$`D_1 \otimes D_2`$ は、次で定まる $`V_1 \otimes V_2`$ 上の表現である。

```math
(D_1 \otimes D_2)(g) = D_1(g) \otimes D_2(g)
```

- 表現であること：$`(D_1 \otimes D_2)(e) = I \otimes I = I`$、$`(D_1(g) \otimes D_2(g))(D_1(h) \otimes D_2(h)) = D_1(gh) \otimes D_2(gh)`$。
- 物理では、2つの系を合わせた系（例：2粒子）に対応する。物理の文献ではテンソル積表現を「直積表現（direct product representation）」と呼ぶこともある。

### [定義] 完全可約
$`D`$ が既約表現の直和と同値であるとき、$`D`$ は完全可約であるという。

```math
\exists S,\ \forall g \in G:\ S^{-1} D(g)\, S = D_1(g) \oplus D_2(g) \oplus \cdots,\quad D_j \text{ は既約}
```

同値な言い換え（$`V`$ が有限次元のとき）：
任意の $`G`$ 不変部分空間 $`W`$ に対して、$`V = W \oplus W'`$ となる $`G`$ 不変部分空間 $`W'`$ が存在する。

- 注意：可約 $`\not\Rightarrow`$ 完全可約。
  反例：$`G = (ℝ, +)`$、$`V = ℂ^2`$、$`D(x) = \begin{pmatrix} 1 & x \\ 0 & 1 \end{pmatrix}`$。
  $`W = \mathrm{span}\lbrace (1,0)^T \rbrace`$ は不変。
  $`\beta \neq 0`$ である他の直線 $`\mathrm{span}\lbrace (\alpha, \beta)^T \rbrace`$ は不変でない：
  $`x \neq 0`$ のとき $`D(x)(\alpha, \beta)^T = (\alpha + x\beta, \beta)^T \notin \mathrm{span}\lbrace (\alpha, \beta)^T \rbrace`$。

### [定理] 有限群の表現は完全可約
- 証明：後で（TODO）

### [例] $`Z_3`$ の正則表現の直和分解
$`D`$：$`Z_3`$ の正則表現。この節では、$`D_k`$ は $`Z_3`$ の既約表現 $`D_{k}`$ を表す（$`k = 1, 2, 3`$）。

```math
\omega = e^{2\pi i/3}, \quad
S = \frac{1}{3}\begin{pmatrix} 1 & 1 & 1 \\ 1 & \omega^2 & \omega \\ 1 & \omega & \omega^2 \end{pmatrix}
```

このとき

```math
S^{-1} D(e)\, S = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix}, \quad
S^{-1} D(a)\, S = \begin{pmatrix} 1 & 0 & 0 \\ 0 & \omega & 0 \\ 0 & 0 & \omega^2 \end{pmatrix}, \quad
S^{-1} D(b)\, S = \begin{pmatrix} 1 & 0 & 0 \\ 0 & \omega^2 & 0 \\ 0 & 0 & \omega \end{pmatrix}
```

$`D \simeq D_1 \oplus D_2 \oplus D_3`$、$`\ 3 = 1 + 1 + 1`$（$`D_j`$ = $`j`$ 番目の対角成分）
- $`D_1`$：自明表現。$`D_1(e) = D_1(a) = D_1(b) = 1`$
- $`D_2`$：上の1次元表現。$`D_2(e) = 1`$、$`D_2(a) = \omega`$、$`D_2(b) = \omega^2`$
- $`D_3`$：その複素共役。$`D_3(e) = 1`$、$`D_3(a) = \omega^2`$、$`D_3(b) = \omega`$
- 不変部分空間 = $`S`$ の各列が張る部分空間
- $`Z_3`$ は可換なので、ブロックは全て $`1 \times 1`$。

### [例] $`Z_3`$ の複数の表現とその対角化
この節では、$`D_k`$ は $`Z_3`$ の既約表現 $`D_{k}`$ を表す（$`k = 1, 2, 3`$）。
各 $`D`$ は $`D(a)`$ だけで決まる。なぜなら、$`D(e) = I`$、$`D(b) = D(a)^2`$で表現は確定するためである。
行列は標準基底 $`(e_1, e_2, \dots)`$ で書く（$`k`$ 列目 = $`e_k`$ の行き先）。

表1：巡回群 $`\mathbb{Z}_3=\{e,a,b\}`$（$`b=a^2`$）の既約表現。$`\omega=e^{2\pi i/3}`$。各成分 $`\lambda`$ は $`D_i(g)`$ であり、線形写像 $`z\mapsto\lambda z`$（$`V=\mathbb{C}`$）を表す。

| $`g`$ | $`D_1(g)`$ | $`D_2(g)`$ | $`D_3(g)`$ |
|:-:|:-:|:-:|:-:|
| $`e`$ | $`1`$ | $`1`$ | $`1`$ |
| $`a`$ | $`1`$ | $`\omega`$ | $`\omega^2`$ |
| $`b`$ | $`1`$ | $`\omega^2`$ | $`\omega`$ |

$`D_1`$ は自明表現、$`D_2`$ は $`D_2(a) = \omega`$ で定まる表現、$`D_3`$ は $`D_2`$ の複素共役。
表の行は群の元、列は表現に対応し、例えば $`a`$ 行 $`D_2`$ 列は $`D_2(a)=\omega`$ を意味する。いずれも1次元表現なので $`D_i(g)`$ は $`1\times 1`$ の正則行列、すなわちスカラー倍の写像であり、数と区別しにくいが、あくまで $`V`$ 上の作用である。

以下の表現で繰り返し用いる行列の定義：

```math
C = \begin{pmatrix} 0 & -1 \\ 1 & -1 \end{pmatrix},\quad
P = \begin{pmatrix} 0 & 0 & 1 \\ 1 & 0 & 0 \\ 0 & 1 & 0 \end{pmatrix},\quad
R(\theta) = \begin{pmatrix} \cos\theta & -\sin\theta \\ \sin\theta & \cos\theta \end{pmatrix}
```

それぞれ、以下の性質を満たす。

- $`C`$：$`Ce_1 = e_2`$、$`Ce_2 = -e_1 - e_2`$。$`C^3 = I`$。
- $`P`$：$`Pe_1 = e_2`$、$`Pe_2 = e_3`$、$`Pe_3 = e_1`$。$`P^3 = I`$。
- $`(\lambda)`$：$`\lambda`$ を成分に持つ $`1 \times 1`$ の行列。


表：可約表現の例

| # | $`V`$ | $`D(e)`$ | $`D(a)`$ | $`D(b)`$ | 説明 |
|---|---|---|---|---|---|
| 1 | $`ℂ^2`$ | $`I`$ | $`C`$ | $`C^2`$ | $`Ce_1 = e_2`$、$`Ce_2 = -e_1 - e_2`$ |
| 2 | $`ℂ^2`$ | $`I`$ | $`\omega C`$ | $`\omega^2 C^2`$ | #1 を $`\omega`$ 倍 |
| 3 | $`ℂ^2`$ | $`I`$ | $`\omega^2 C`$ | $`\omega C^2`$ | #1 を $`\omega^2`$ 倍 |
| 4 | $`ℂ^3`$ | $`I`$ | $`P`$ | $`P^2`$ | $`e_1, e_2, e_3`$ の巡回置換（三角形の頂点） |
| 5 | $`ℂ^3`$ | $`I`$ | $`C \oplus (\omega)`$ | $`C^2 \oplus (\omega^2)`$ | #1 と、$`e_3 \mapsto \omega e_3`$ |
| 6 | $`ℂ^3`$ | $`I`$ | $`\omega^2 C \oplus (1)`$ | $`\omega C^2 \oplus (1)`$ | #3 と、$`e_3 \mapsto e_3`$ |
| 7 | $`ℂ^4`$ | $`I`$ | $`P \oplus (1)`$ | $`P^2 \oplus (1)`$ | 三角形の頂点と、動かない中心 |
| 8 | $`ℂ^6`$ | $`I`$ | $`P \oplus P`$ | $`P^2 \oplus P^2`$ | 2つの三角形を同時に回す |
| 9 | $`ℂ^2`$ | $`I`$ | $`R(2\pi/3)`$ | $`R(4\pi/3)`$ | 平面の $`2\pi/3`$ 回転 |

#9は、$`V=\mathbb{R}^2`$ なら既約である。

対角化について、 $`D(a)^3 = I`$ より、$`D(a)`$ の最小多項式は $`x^3 - 1 = (x-1)(x-\omega)(x-\omega^2)`$ を割り切る。重根を持たないので、$`D(a)`$ は $`ℂ`$ 上で対角化可能である。$`D(b) = D(a)^2`$ なので $`D(a)`$ の固有ベクトルは全ての $`D(g)`$ の共通固有ベクトルであり、それが張る1次元部分空間は不変部分空間になる。$`S`$ はその固有ベクトルを列に並べた行列：

表：上記の可約表現の規約分解
```math
S_C = \begin{pmatrix} 1 & 1 \\ -\omega & -\omega^2 \end{pmatrix},\quad
S_P = \begin{pmatrix} 1 & 1 & 1 \\ 1 & \omega^2 & \omega \\ 1 & \omega & \omega^2 \end{pmatrix},\quad
S_R = \begin{pmatrix} 1 & 1 \\ -i & i \end{pmatrix}
```

| # | $`S`$ | $`S^{-1}D(e)S`$ | $`S^{-1}D(a)S`$ | $`S^{-1}D(b)S`$ | 分解 |
|---|---|---|---|---|---|
| 1 | $`S_C`$ | $`I`$ | $`\mathrm{diag}(\omega, \omega^2)`$ | $`\mathrm{diag}(\omega^2, \omega)`$ | $`D_2 \oplus D_3`$ |
| 2 | $`S_C`$ | $`I`$ | $`\mathrm{diag}(\omega^2, 1)`$ | $`\mathrm{diag}(\omega, 1)`$ | $`D_3 \oplus D_1`$ |
| 3 | $`S_C`$ | $`I`$ | $`\mathrm{diag}(1, \omega)`$ | $`\mathrm{diag}(1, \omega^2)`$ | $`D_1 \oplus D_2`$ |
| 4 | $`S_P`$ | $`I`$ | $`\mathrm{diag}(1, \omega, \omega^2)`$ | $`\mathrm{diag}(1, \omega^2, \omega)`$ | $`D_1 \oplus D_2 \oplus D_3`$ |
| 5 | $`S_C \oplus (1)`$ | $`I`$ | $`\mathrm{diag}(\omega, \omega^2, \omega)`$ | $`\mathrm{diag}(\omega^2, \omega, \omega^2)`$ | $`D_2 \oplus D_3 \oplus D_2`$ |
| 6 | $`S_C \oplus (1)`$ | $`I`$ | $`\mathrm{diag}(1, \omega, 1)`$ | $`\mathrm{diag}(1, \omega^2, 1)`$ | $`D_1 \oplus D_2 \oplus D_1`$ |
| 7 | $`S_P \oplus (1)`$ | $`I`$ | $`\mathrm{diag}(1, \omega, \omega^2, 1)`$ | $`\mathrm{diag}(1, \omega^2, \omega, 1)`$ | $`D_1 \oplus D_2 \oplus D_3 \oplus D_1`$ |
| 8 | $`S_P \oplus S_P`$ | $`I`$ | $`\mathrm{diag}(1, \omega, \omega^2, 1, \omega, \omega^2)`$ | $`\mathrm{diag}(1, \omega^2, \omega, 1, \omega^2, \omega)`$ | $`(D_1 \oplus D_2 \oplus D_3)^{\oplus 2}`$ |
| 9 | $`S_R`$ | $`I`$ | $`\mathrm{diag}(\omega, \omega^2)`$ | $`\mathrm{diag}(\omega^2, \omega)`$ | $`D_2 \oplus D_3`$ |

1と9は、いずれも $`D_2 \oplus D_3`$ に分解されるが、同値である。実際、$`T=S_c S_R^{-1}`$ とおくと、$`T^{-1}CT=R(2 \pi / 3)`$ が成り立つ。

## $`S_3`$ の表現

### [例] $`S_3`$
$`S_3`$は、3つのモノの置換群であり、以下のような操作である。

```math
S_3 = \lbrace e, a_1, a_2, a_3, a_4, a_5 \rbrace, \quad
a_1 = (1,2,3),\ a_2 = (3,2,1),\ a_3 = (1,2),\ a_4 = (2,3),\ a_5 = (3,1)
```

- 記法：$`(i, j, k)`$ は、位置 $`i`$ の物を $`j`$ へ、$`j`$ の物を $`k`$ へ、$`k`$ の物を $`i`$ へ移す。$`(i, j)`$ は位置 $`i`$ と $`j`$ の物を入れ替える。
- 積：$`gh`$ = 先に $`h`$、次に $`g`$。



群表：
| $`\cdot`$ | $`e`$ | $`a_1`$ | $`a_2`$ | $`a_3`$ | $`a_4`$ | $`a_5`$ |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| $`e`$ | $`e`$ | $`a_1`$ | $`a_2`$ | $`a_3`$ | $`a_4`$ | $`a_5`$ |
| $`a_1`$ | $`a_1`$ | $`a_2`$ | $`e`$ | $`a_5`$ | $`a_3`$ | $`a_4`$ |
| $`a_2`$ | $`a_2`$ | $`e`$ | $`a_1`$ | $`a_4`$ | $`a_5`$ | $`a_3`$ |
| $`a_3`$ | $`a_3`$ | $`a_4`$ | $`a_5`$ | $`e`$ | $`a_1`$ | $`a_2`$ |
| $`a_4`$ | $`a_4`$ | $`a_5`$ | $`a_3`$ | $`a_2`$ | $`e`$ | $`a_1`$ |
| $`a_5`$ | $`a_5`$ | $`a_3`$ | $`a_4`$ | $`a_1`$ | $`a_2`$ | $`e`$ |

非可換群である。表は、行 × 列の順番で読む。

### [例] $`S_3`$ の $`\mathbb{C}^2`$ 上の表現

表現空間は $`V = \mathbb{C}^2`$、基底は標準基底 $`e_1, e_2`$。

三箇所の位置を、角度 $`30^\circ, 150^\circ, 270^\circ`$ にある正三角形の頂点 $`v_1, v_2, v_3`$ に対応させる。$`D(g)`$ は $`v_i \mapsto v_{g(i)}`$ となる回転または鏡映。

以下の3つのベクトル

```math
\begin{aligned}
v_1 &= \tfrac{\sqrt{3}}{2} e_1 + \tfrac{1}{2} e_2 \\
v_2 &= -\tfrac{\sqrt{3}}{2} e_1 + \tfrac{1}{2} e_2 \\
v_3 &= -e_2
\end{aligned}
```

をとる。正三角形の頂点であり、 $`v_1 + v_2 + v_3 = 0`$ を満たす。

この表現は、準同型性 $`D(g)D(h) = D(gh)`$ を保つ。合同変換の合成は、頂点の置換の合成に対応するので成り立つ。

表：$`S_3`$ の $`ℂ^2`$ 上の表現

| $`g`$ | 置換 | 幾何 | $`D(g)`$ | $`D(g)v_1`$ | $`D(g)v_2`$ | $`D(g)v_3`$ |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| $`e`$ | 恒等 | 恒等 | $`\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}`$ | $`v_1`$ | $`v_2`$ | $`v_3`$ |
| $`a_1`$ | $`1\to2\to3\to1`$ | $`+120^\circ`$ 回転 | $`\begin{pmatrix} -\frac{1}{2} & -\frac{\sqrt{3}}{2} \\ \frac{\sqrt{3}}{2} & -\frac{1}{2} \end{pmatrix}`$ | $`v_2`$ | $`v_3`$ | $`v_1`$ |
| $`a_2`$ | $`3\to2\to1\to3`$ | $`-120^\circ`$ 回転 | $`\begin{pmatrix} -\frac{1}{2} & \frac{\sqrt{3}}{2} \\ -\frac{\sqrt{3}}{2} & -\frac{1}{2} \end{pmatrix}`$ | $`v_3`$ | $`v_1`$ | $`v_2`$ |
| $`a_3`$ | $`1\leftrightarrow2`$ | $`v_3`$ を通る直線で鏡映 | $`\begin{pmatrix} -1 & 0 \\ 0 & 1 \end{pmatrix}`$ | $`v_2`$ | $`v_1`$ | $`v_3`$ |
| $`a_4`$ | $`2\leftrightarrow3`$ | $`v_1`$ を通る直線で鏡映 | $`\begin{pmatrix} \frac{1}{2} & \frac{\sqrt{3}}{2} \\ \frac{\sqrt{3}}{2} & -\frac{1}{2} \end{pmatrix}`$ | $`v_1`$ | $`v_3`$ | $`v_2`$ |
| $`a_5`$ | $`3\leftrightarrow1`$ | $`v_2`$ を通る直線で鏡映 | $`\begin{pmatrix} \frac{1}{2} & -\frac{\sqrt{3}}{2} \\ -\frac{\sqrt{3}}{2} & -\frac{1}{2} \end{pmatrix}`$ | $`v_3`$ | $`v_2`$ | $`v_1`$ |


この2次元表現は既約である。
- もし、可約だとすると、完全可約性から $`D \simeq D_1 \oplus D_2`$（$`D_1, D_2`$ は1次元）となり、全ての $`D(g)`$ が可換になる。
- しかし $`a_1 a_3 = a_5 \neq a_4 = a_3 a_1`$ なので、$`D(a_1) D(a_3) \neq D(a_3) D(a_1)`$。

なお、注意が必要。$`S_3`$ にも1次元の既約表現はある（自明表現など）。非可換であることが意味するのは、既約表現が全て1次元とは限らないということである。

### [例] $`S_3`$ の3つの既約表現
同値を除いて、$`S_3`$ の既約表現はちょうど3つ。次元で名付け、同じ次元のものはプライムで区別する：$`\mathbf{1}`$（自明表現）、$`\mathbf{1}'`$（符号表現）、$`\mathbf{2}`$（標準表現、上の2次元表現）。表現行列は $`D_{\mathbf{1}}, D_{\mathbf{1}'}, D_{\mathbf{2}}`$ と書く。

| $`g`$ | $`\mathbf{1}`$（自明表現、1次元） | $`\mathbf{1}'`$（符号表現、1次元） | $`\mathbf{2}`$（標準表現、2次元） |
|:-:|:-:|:-:|:-:|
| $`e`$ | $`1`$ | $`1`$ | $`I_2`$ |
| $`a_1, a_2`$ | $`1`$ | $`1`$ | $`\pm 120^\circ`$ 回転の行列 |
| $`a_3, a_4, a_5`$ | $`1`$ | $`-1`$ | 鏡映の行列 |

$`\mathbf{2}`$ の各行列は [例] $`S_3`$ の $`\mathbb{C}^2`$ 上の表現 の表にある。

1次元の既約表現は $`\mathbf{1}`$ と $`\mathbf{1}'`$ に限る。

証明：$`D`$ を任意の1次元表現とする（1次元なので自動的に既約）。$`D(g)`$ は0でない数であり、数どうしは可換。以下で、
(i) $`D`$ は $`D_{\mathbf{1}}`$ か $`D_{\mathbf{1}'}`$ のどちらかに一致すること、(ii) その2つが実際に表現であること、を示す。

(i) 候補を絞る：
- $`e e = e`$ なので $`D(e)^2 = D(e)`$。$`D(e) \neq 0`$ なので $`D(e) = 1`$。
- $`a_3 a_4 = a_1`$、$`a_4 a_3 = a_2`$ なので、$`D(a_1) = D(a_3)D(a_4) = D(a_4)D(a_3) = D(a_2)`$。
- $`a_1 a_1 = a_2`$ なので $`D(a_1)^2 = D(a_2) = D(a_1)`$。$`D(a_1) \neq 0`$ なので $`D(a_1) = D(a_2) = 1`$。
- $`a_3 a_3 = e`$ なので $`D(a_3)^2 = 1`$、すなわち $`D(a_3) = \pm 1`$。
- $`a_1 a_3 = a_5`$、$`a_1 a_5 = a_4`$ なので $`D(a_5) = D(a_4) = D(a_3)`$。
- 以上より、$`D(a_3) = 1`$ なら $`D = D_{\mathbf{1}}`$、$`D(a_3) = -1`$ なら $`D = D_{\mathbf{1}'}`$。

(ii) 2つの候補が表現であること：
- $`\mathbf{1}`$：全ての値が $`1`$ なので、$`D(gh) = D(g)D(h)`$ は自明に成り立つ。
- $`\mathbf{1}'`$：$`H = \lbrace e, a_1, a_2 \rbrace`$、$`K = \lbrace a_3, a_4, a_5 \rbrace`$ とおく。群表より $`HH \subset H`$、$`HK \subset K`$、$`KH \subset K`$、$`KK \subset H`$ が成り立つ。これは値の積の規則 $`1 \cdot 1 = 1`$、$`1 \cdot (-1) = (-1) \cdot 1 = -1`$、$`(-1)(-1) = 1`$ と一致する。

3つの規約表現のうち、どの2つも同値でない：
- $`\mathbf{1} \not\simeq \mathbf{1}'`$：1次元では $`S^{-1} x S = x`$ なので、同値とは等しいことであり、2つは $`a_3`$ で値が違う。
- $`\mathbf{2}`$ はどちらとも同値でない：次元が違う。

他にはないこと：
- 既約表現について $`\sum_a n_a^2 = \lvert G \rvert`$（$`n_a`$ = 次元）。ここでは $`1^2 + 1^2 + 2^2 = 6 = \lvert S_3 \rvert`$ なので、他の既約表現が入る余地はない。この和の公式は、下の [定理] 既約表現の行列要素は完全正規直交系 の系として従う。

### [例] $`S_3`$ の表現とその規約分解
元・積・群表は上の [例] $`S_3`$ に従う。$`\mathbf{1}`$、$`\mathbf{1}'`$、$`\mathbf{2}`$ は $`S_3`$ の既約表現（上の [例] $`S_3`$ の既約表現）。どの場合も $`V = ℂ^n`$。行列は標準基底 $`(e_1, e_2, \dots)`$ で書く。

以下で使う記号と規約：
- $`D_{\mathbf{2}}(g)`$：$`\mathbf{2}`$ の行列（[例] $`S_3`$ の $`\mathbb{C}^2`$ 上の表現の表の $`D(g)`$ 列）。
- $`D_{\mathbf{1}'}(g)`$：$`e, a_1, a_2`$ で $`1`$、$`a_3, a_4, a_5`$ で $`-1`$。
- $`D_{\mathrm{perm}}(g)`$：$`3 \times 3`$ の置換行列。$`D_{\mathrm{perm}}(g)\, e_i = e_{g(i)}`$（$`e_i`$ = 頂点 $`i`$ にいる状態）。
- $`X = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}`$（2つの基底の入れ替え）。
- $`ℂ^4 = ℂ^2 \otimes ℂ^2`$ の基底の順序：$`e_1 \otimes e_1,\ e_1 \otimes e_2,\ e_2 \otimes e_1,\ e_2 \otimes e_2`$。

表：$`S_3`$ の表現の例

| # | $`V`$ | $`D(g)`$ | 説明 |
|---|---|---|---|
| 1 | $`ℂ^2`$ | $`g = e, a_1, a_2`$ で $`I_2`$、$`g = a_3, a_4, a_5`$ で $`X`$ | 向き（左回り・右回り）の2状態。回転では変わらず、鏡映で入れ替わる |
| 2 | $`ℂ^3`$ | $`D_{\mathrm{perm}}(g)`$ | 三角形の頂点 |
| 3 | $`ℂ^3`$ | $`D_{\mathbf{1}'}(g)\, D_{\mathrm{perm}}(g)`$ | 三角形の頂点で、鏡映のときに符号が付く |
| 4 | $`ℂ^4`$ | $`D_{\mathbf{2}}(g) \otimes D_{\mathbf{2}}(g)`$ | $`\mathbf{2}`$ の2粒子（$`\mathbf{2} \otimes \mathbf{2}`$） |
| 5 | $`ℂ^6`$ | $`D(g)\lvert h\rangle = \lvert g h g^{-1}\rangle`$ | 基底 $`\lvert h\rangle`$（$`h \in S_3`$）への共役による作用 |
| 6 | $`ℂ^6`$ | $`D_{\mathrm{perm}}(g) \otimes I_2`$ | 三角形の頂点 × 2準位（基底 $`e_i \otimes f_n`$、$`n = 0, 1`$） |
| 7 | $`ℂ^6`$ | $`D(g)\lvert h\rangle = \lvert g h\rangle`$ | 正則表現 |

それぞれの規約分解を考える。$`S`$ は列ベクトルを横に並べた行列である。以下で用いるベクトル：

```math
\begin{aligned}
u_0 &= \tfrac{1}{\sqrt3}(e_1 + e_2 + e_3), \quad
u_1 = \tfrac{1}{\sqrt2}(e_1 - e_2), \quad
u_2 = \tfrac{1}{\sqrt6}(e_1 + e_2 - 2e_3) \\
w_{\mathbf{1}} &= \tfrac{1}{\sqrt6}\textstyle\sum_g \lvert g\rangle, \quad
w_{\mathbf{1}'} = \tfrac{1}{\sqrt6}\textstyle\sum_g D_{\mathbf{1}'}(g) \lvert g\rangle, \quad
w_{jk} = \tfrac{1}{\sqrt3}\textstyle\sum_g D_{\mathbf{2}}(g)_{jk} \lvert g\rangle
\end{aligned}
```

表：$`S_3`$ の表現の規約分解

| # | $`S`$ | $`S^{-1} D(g) S`$ | 分解 |
|---|---|---|---|
| 1 | $`\begin{pmatrix} e_1 + e_2 & e_1 - e_2 \end{pmatrix}`$ | $`1 \oplus D_{\mathbf{1}'}(g)`$ | $`\mathbf{1} \oplus \mathbf{1}'`$ |
| 2 | $`\begin{pmatrix} u_0 & u_1 & u_2 \end{pmatrix}`$ | $`1 \oplus D_{\mathbf{2}}(g)`$ | $`\mathbf{1} \oplus \mathbf{2}`$ |
| 3 | $`\begin{pmatrix} u_0 & u_2 & -u_1 \end{pmatrix}`$ | $`D_{\mathbf{1}'}(g) \oplus D_{\mathbf{2}}(g)`$ | $`\mathbf{1}' \oplus \mathbf{2}`$ |
| 4 | $`\begin{pmatrix} \frac{e_1 \otimes e_1 + e_2 \otimes e_2}{\sqrt2} & \frac{e_1 \otimes e_2 - e_2 \otimes e_1}{\sqrt2} & \frac{e_1 \otimes e_2 + e_2 \otimes e_1}{\sqrt2} & \frac{e_1 \otimes e_1 - e_2 \otimes e_2}{\sqrt2} \end{pmatrix}`$ | $`1 \oplus D_{\mathbf{1}'}(g) \oplus D_{\mathbf{2}}(g)`$ | $`\mathbf{1} \oplus \mathbf{1}' \oplus \mathbf{2}`$ |
| 5 | $`\begin{pmatrix} \lvert e\rangle & \frac{\lvert a_1\rangle + \lvert a_2\rangle}{\sqrt2} & \frac{\lvert a_1\rangle - \lvert a_2\rangle}{\sqrt2} & \frac{\lvert a_3\rangle + \lvert a_4\rangle + \lvert a_5\rangle}{\sqrt3} & \frac{\lvert a_4\rangle - \lvert a_5\rangle}{\sqrt2} & \frac{-2\lvert a_3\rangle + \lvert a_4\rangle + \lvert a_5\rangle}{\sqrt6} \end{pmatrix}`$ | $`1 \oplus 1 \oplus D_{\mathbf{1}'}(g) \oplus 1 \oplus D_{\mathbf{2}}(g)`$ | $`\mathbf{1} \oplus \mathbf{1} \oplus \mathbf{1} \oplus \mathbf{1}' \oplus \mathbf{2}`$ |
| 6 | $`\begin{pmatrix} u_0 \otimes f_0 & u_0 \otimes f_1 & u_1 \otimes f_0 & u_2 \otimes f_0 & u_1 \otimes f_1 & u_2 \otimes f_1 \end{pmatrix}`$ | $`1 \oplus 1 \oplus D_{\mathbf{2}}(g) \oplus D_{\mathbf{2}}(g)`$ | $`\mathbf{1} \oplus \mathbf{1} \oplus \mathbf{2} \oplus \mathbf{2}`$ |
| 7 | $`\begin{pmatrix} w_{\mathbf{1}} & w_{\mathbf{1}'} & w_{11} & w_{21} & w_{12} & w_{22} \end{pmatrix}`$ | $`1 \oplus D_{\mathbf{1}'}(g) \oplus D_{\mathbf{2}}(g) \oplus D_{\mathbf{2}}(g)`$ | $`\mathbf{1} \oplus \mathbf{1}' \oplus \mathbf{2} \oplus \mathbf{2}`$ |

表から読み取れること：
- #1：非可換群でも、1次元の既約表現だけでできていれば完全に対角になる。
- #2 と #3：不変部分空間は同じで、1次元の部分が $`\mathbf{1}`$ か $`\mathbf{1}'`$ かだけが違う。
- #4：$`\mathbf{2} \otimes \mathbf{2} = \mathbf{1} \oplus \mathbf{1}' \oplus \mathbf{2}`$。
- #5：共役類ごとに分かれる。$`\lbrace e \rbrace \to \mathbf{1}`$、$`\lbrace a_1, a_2 \rbrace \to \mathbf{1} \oplus \mathbf{1}'`$、$`\lbrace a_3, a_4, a_5 \rbrace \to \mathbf{1} \oplus \mathbf{2}`$。
- #7：各既約表現が、その次元と同じ回数だけ現れる（$`1 + 1 + 2 \cdot 2 = 6`$）。


## 部分群と剰余群

### [定義] 部分群
$`H \subseteq G`$ が $`G`$ の積について群になるとき、$`H`$ を $`G`$ の部分群という。

### [例] $`Z_3 \subset S_3`$
$`\lbrace e, a_1, a_2 \rbrace`$ は $`S_3`$ の部分群で、$`Z_3`$ と同型（$`a_1 \mapsto a`$、$`a_2 \mapsto b`$）。

### [定義] 右剰余類 $`Hg`$ / 左剰余類 $`gH`$
$`H`$ を $`G`$ の部分群、$`g \in G`$ とする。
- 右剰余類：$`Hg = \lbrace hg \mid h \in H \rbrace`$
- 左剰余類：$`gH = \lbrace gh \mid h \in H \rbrace`$

### [定義] 正規部分群 $`\trianglelefteq`$
$`G`$ の部分群 $`H`$ は、次を満たすとき正規部分群（不変部分群）であるといい、$`H \trianglelefteq G`$ と書く。

```math
\forall g \in G:\ gH = Hg
```

同値な言い換え：

```math
\forall g \in G,\ \forall h \in H:\ g h g^{-1} \in H
```

### [定義] 剰余群 $`G/H`$
$`H \trianglelefteq G`$ のとき、剰余類の集合 $`G/H = \lbrace Hg \mid g \in G \rbrace`$ は、集合の積
$`AB = \lbrace ab \mid a \in A,\ b \in B \rbrace`$ について群になる：

```math
(Hg_1)(Hg_2) = H(g_1 H)g_2 = H(H g_1)g_2 = (HH)\,g_1 g_2 = H g_1 g_2
```

- 2つ目の等号で $`g_1 H = H g_1`$（正規性）を使う。
- $`HH = \lbrace h_1 h_2 \mid h_1, h_2 \in H \rbrace = H`$：
  - $`\subseteq`$：$`h_1, h_2 \in H \Rightarrow h_1 h_2 \in H`$（$`H`$ についての A1）。
  - $`\supseteq`$：$`e \in H`$ なので、全ての $`h \in H`$ は $`h = eh \in HH`$。
$`G/H`$ の群の公理（どれも $`(Hg_1)(Hg_2) = Hg_1g_2`$ から従う）：
- A1：$`(Hg_1)(Hg_2) = Hg_1g_2 \in G/H`$。
- A2：$`\big((Hg_1)(Hg_2)\big)(Hg_3) = H(g_1g_2)g_3 = Hg_1(g_2g_3) = (Hg_1)\big((Hg_2)(Hg_3)\big)`$（$`G`$ の A2 による）。
- A3：単位元は $`H = He`$。$`(He)(Hg) = Hg = (Hg)(He)`$ なので。
- A4：$`Hg`$ の逆元は $`Hg^{-1}`$。$`(Hg)(Hg^{-1}) = He = (Hg^{-1})(Hg)`$ なので。

### [例] $`S_3`$ の正規部分群
- TODO

## 指標

### [定義] トレース $`\mathrm{tr}`$
$`n \times n`$ 行列 $`A`$ のトレースを、対角成分の和で定める。

```math
\mathrm{tr}\, A = \sum_{i=1}^{n} A_{ii}
```

- $`\mathrm{tr}(AB) = \sum_{i,j} A_{ij} B_{ji} = \mathrm{tr}(BA)`$。
- したがって $`\mathrm{tr}(S^{-1} A S) = \mathrm{tr}(A S S^{-1}) = \mathrm{tr}\, A`$。トレースは基底の取り方によらないので、線形演算子 $`A: V \to V`$ のトレースとしても定まる。

### [定義] 指標 $`\chi`$
$`G`$ の表現 $`(V, D)`$ に対して、$`G`$ 上の関数

```math
\chi_D(g) = \mathrm{tr}\, D(g)
```

を $`D`$ の指標という。

性質：
1. $`\chi_D(e) = \mathrm{tr}\, 1 = \dim V`$。
2. 同値な表現は同じ指標をもつ：$`\chi_{D'}(g) = \mathrm{tr}(S^{-1} D(g) S) = \chi_D(g)`$。
3. 直和は和：$`\chi_{D_1 \oplus D_2} = \chi_{D_1} + \chi_{D_2}`$（ブロック対角行列のトレースは各ブロックのトレースの和）。

例：$`Z_3`$ の正則表現（上の [例] $`Z_3`$ の正則表現）では $`D(a), D(b)`$ の対角成分が全て $`0`$ なので、$`\chi = (3, 0, 0)`$（$`e, a, b`$ の順）。これは $`D_1 \oplus D_2 \oplus D_3`$ の指標 $`(1+1+1,\ 1+\omega+\omega^2,\ 1+\omega^2+\omega) = (3, 0, 0)`$ と一致する。

### [定理] 既約表現の指標の直交性
$`G`$ を有限群とする。$`G`$ 上の関数 $`\chi, \psi`$ に対して、内積を次で定める。

```math
\langle \chi, \psi \rangle = \frac{1}{\lvert G \rvert} \sum_{g \in G} \chi(g)^* \, \psi(g)
```

$`D_j, D_k`$ を既約表現とし、その指標を $`\chi_j, \chi_k`$ とする。このとき次が成り立つ。

```math
\langle \chi_j, \chi_k \rangle =
\begin{cases}
1 & (D_j \simeq D_k) \\
0 & (D_j \not\simeq D_k)
\end{cases}
```

- 証明：後で（TODO、Schur の補題を使う。Georgi 1章）。

### [例] $`Z_3`$ の指標の直交性
$`Z_3 = \lbrace e, a, a^2 \rbrace`$ の既約表現を再掲する（上の [例] $`Z_3`$ の複数の表現とその対角化 の表1）。$`\omega = e^{2\pi i/3}`$。

表：$`Z_3`$ の既約表現

| $`g`$ | $`D_1(g)`$ | $`D_2(g)`$ | $`D_3(g)`$ |
|:-:|:-:|:-:|:-:|
| $`e`$ | $`1`$ | $`1`$ | $`1`$ |
| $`a`$ | $`1`$ | $`\omega`$ | $`\omega^2`$ |
| $`a^2`$ | $`1`$ | $`\omega^2`$ | $`\omega`$ |

どれも1次元なので、$`D_k(g)`$ は $`1 \times 1`$ 行列であり、そのトレースは成分そのものである。したがって指標 $`\chi_k(g) = \mathrm{tr}\, D_k(g)`$ の表は、値としては上の表と同じになる。

表：$`Z_3`$ の指標

| $`g`$ | $`\chi_1(g)`$ | $`\chi_2(g)`$ | $`\chi_3(g)`$ |
|:-:|:-:|:-:|:-:|
| $`e`$ | $`1`$ | $`1`$ | $`1`$ |
| $`a`$ | $`1`$ | $`\omega`$ | $`\omega^2`$ |
| $`a^2`$ | $`1`$ | $`\omega^2`$ | $`\omega`$ |

計算で使う関係式：
- $`\omega^3 = 1`$ なので、$`\omega^* = \omega^{-1} = \omega^2`$、$`(\omega^2)^* = \omega`$、$`\lvert \omega \rvert = 1`$。
- $`(\omega - 1)(1 + \omega + \omega^2) = \omega^3 - 1 = 0`$ と $`\omega \neq 1`$ より、$`1 + \omega + \omega^2 = 0`$。

内積は、指標の表の2つの列について、各行の値の積（左側の指標は複素共役）を足し、$`\lvert G \rvert`$ で割ったものである。$`\lvert Z_3 \rvert = 3`$ とする。内積 $`\langle \chi_j, \chi_k \rangle`$ は $`3 \times 3 = 9`$ 通りある。そのうち6通りを直接計算する。

```math
\begin{aligned}
\langle \chi_1, \chi_1 \rangle &= \tfrac{1}{3}(1 + 1 + 1) = 1 \\
\langle \chi_2, \chi_2 \rangle &= \tfrac{1}{3}(1 + \omega^* \omega + (\omega^2)^* \omega^2) = \tfrac{1}{3}(1 + 1 + 1) = 1 \\
\langle \chi_3, \chi_3 \rangle &= \tfrac{1}{3}(1 + (\omega^2)^* \omega^2 + \omega^* \omega) = \tfrac{1}{3}(1 + 1 + 1) = 1 \\
\langle \chi_1, \chi_2 \rangle &= \tfrac{1}{3}(1 + \omega + \omega^2) = 0 \\
\langle \chi_1, \chi_3 \rangle &= \tfrac{1}{3}(1 + \omega^2 + \omega) = 0 \\
\langle \chi_2, \chi_3 \rangle &= \tfrac{1}{3}(1 + \omega^* \omega^2 + (\omega^2)^* \omega) = \tfrac{1}{3}(1 + \omega^2 \cdot \omega^2 + \omega \cdot \omega) = \tfrac{1}{3}(1 + \omega + \omega^2) = 0
\end{aligned}
```

残りの3つは、順序を入れ替えると複素共役になることから決まる。内積の定義で各項の複素共役をとると $`\chi_k(g)^* \chi_j(g) = \big(\chi_j(g)^* \chi_k(g)\big)^*`$ なので、$`\langle \chi_k, \chi_j \rangle = \langle \chi_j, \chi_k \rangle^*`$。例えば $`\langle \chi_2, \chi_1 \rangle = \langle \chi_1, \chi_2 \rangle^* = 0^* = 0`$。まとめると：

表：$`Z_3`$ の指標の内積 $`\langle \chi_j, \chi_k \rangle`$

| | $`\chi_1`$ | $`\chi_2`$ | $`\chi_3`$ |
|:-:|:-:|:-:|:-:|
| $`\chi_1`$ | $`1`$ | $`0`$ | $`0`$ |
| $`\chi_2`$ | $`0`$ | $`1`$ | $`0`$ |
| $`\chi_3`$ | $`0`$ | $`0`$ | $`1`$ |

3つの既約表現はどの2つも同値でないので、定理のとおり異なる指標どうしの内積は $`0`$、同じ指標どうしは $`1`$ になっている。

### [例] $`S_3`$ の指標の直交性
$`S_3`$ の既約表現を再掲する（上の [例] $`S_3`$ の3つの既約表現。$`D_{\mathbf{2}}`$ の行列は [例] $`S_3`$ の $`\mathbb{C}^2`$ 上の表現 の表から）。

表：$`S_3`$ の既約表現

| $`g`$ | $`D_{\mathbf{1}}(g)`$ | $`D_{\mathbf{1}'}(g)`$ | $`D_{\mathbf{2}}(g)`$ |
|:-:|:-:|:-:|:-:|
| $`e`$ | $`1`$ | $`1`$ | $`\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}`$ |
| $`a_1`$ | $`1`$ | $`1`$ | $`\begin{pmatrix} -\frac{1}{2} & -\frac{\sqrt{3}}{2} \\ \frac{\sqrt{3}}{2} & -\frac{1}{2} \end{pmatrix}`$ |
| $`a_2`$ | $`1`$ | $`1`$ | $`\begin{pmatrix} -\frac{1}{2} & \frac{\sqrt{3}}{2} \\ -\frac{\sqrt{3}}{2} & -\frac{1}{2} \end{pmatrix}`$ |
| $`a_3`$ | $`1`$ | $`-1`$ | $`\begin{pmatrix} -1 & 0 \\ 0 & 1 \end{pmatrix}`$ |
| $`a_4`$ | $`1`$ | $`-1`$ | $`\begin{pmatrix} \frac{1}{2} & \frac{\sqrt{3}}{2} \\ \frac{\sqrt{3}}{2} & -\frac{1}{2} \end{pmatrix}`$ |
| $`a_5`$ | $`1`$ | $`-1`$ | $`\begin{pmatrix} \frac{1}{2} & -\frac{\sqrt{3}}{2} \\ -\frac{\sqrt{3}}{2} & -\frac{1}{2} \end{pmatrix}`$ |

$`D_{\mathbf{2}}`$ の指標は、行列の対角成分の和から求まる：$`e`$ で $`1 + 1 = 2`$、$`a_1, a_2`$ で $`-\tfrac12 - \tfrac12 = -1`$、$`a_3`$ で $`-1 + 1 = 0`$、$`a_4, a_5`$ で $`\tfrac12 - \tfrac12 = 0`$。

表：$`S_3`$ の指標

| $`g`$ | $`\chi_{\mathbf{1}}(g)`$ | $`\chi_{\mathbf{1}'}(g)`$ | $`\chi_{\mathbf{2}}(g)`$ |
|:-:|:-:|:-:|:-:|
| $`e`$ | $`1`$ | $`1`$ | $`2`$ |
| $`a_1`$ | $`1`$ | $`1`$ | $`-1`$ |
| $`a_2`$ | $`1`$ | $`1`$ | $`-1`$ |
| $`a_3`$ | $`1`$ | $`-1`$ | $`0`$ |
| $`a_4`$ | $`1`$ | $`-1`$ | $`0`$ |
| $`a_5`$ | $`1`$ | $`-1`$ | $`0`$ |

$`\lvert S_3 \rvert = 6`$ とする。内積は $`3 \times 3 = 9`$ 通りある。指標は全て実数なので複素共役は値を変えず、順序を入れ替えても内積は同じ。したがって6通りを直接計算すれば足りる。

```math
\begin{aligned}
\langle \chi_{\mathbf{1}}, \chi_{\mathbf{1}} \rangle &= \tfrac{1}{6}(1 + 1 + 1 + 1 + 1 + 1) = 1 \\
\langle \chi_{\mathbf{1}'}, \chi_{\mathbf{1}'} \rangle &= \tfrac{1}{6}(1 + 1 + 1 + 1 + 1 + 1) = 1 \\
\langle \chi_{\mathbf{2}}, \chi_{\mathbf{2}} \rangle &= \tfrac{1}{6}(4 + 1 + 1 + 0 + 0 + 0) = 1 \\
\langle \chi_{\mathbf{1}}, \chi_{\mathbf{1}'} \rangle &= \tfrac{1}{6}(1 + 1 + 1 - 1 - 1 - 1) = 0 \\
\langle \chi_{\mathbf{1}}, \chi_{\mathbf{2}} \rangle &= \tfrac{1}{6}(2 - 1 - 1 + 0 + 0 + 0) = 0 \\
\langle \chi_{\mathbf{1}'}, \chi_{\mathbf{2}} \rangle &= \tfrac{1}{6}(2 - 1 - 1 + 0 + 0 + 0) = 0
\end{aligned}
```

$`Z_3`$ と同じく、内積の表は単位行列になり、3つの既約表現の指標は直交している。

## 群上の関数の展開

### [定理] 既約表現の行列要素は完全正規直交系
$`G`$ を有限群とし、$`N = \lvert G \rvert`$ とする。

$`G`$ 上の関数 $`f: G \to ℂ`$ は、$`N`$ 個の値 $`f(g)`$ の組なので、全体は $`N`$ 次元のベクトル空間になる。$`f`$ は正則表現の空間のベクトル $`\sum_g f(g) \lvert g\rangle`$ と1対1に対応する。この式は標準基底 $`\lvert g\rangle`$ での展開であり、係数は値 $`f(g)`$ をそのまま読めばよい。

$`D_a`$ を $`G`$ のユニタリな（$`D_a(g)^\dagger = D_a(g)^{-1}`$ を満たす）既約表現とし、$`n_a`$ をその次元とする。同値でない既約表現を全てとる。行列要素 $`[D_a(g)]_{jk}`$ は、$`a, j, k`$ を固定すると $`G`$ 上の関数になる。このとき次が成り立つ（Georgi Theorem 1.5）。

```math
\left\lbrace \sqrt{n_a}\, [D_a(g)]_{jk} \;\middle|\; a,\ 1 \le j, k \le n_a \right\rbrace
```

は、内積 $`\langle \cdot, \cdot \rangle`$（[定理] 既約表現の指標の直交性 で定めたもの）について、$`G`$ 上の関数の正規直交基底である。


- 正規直交：異なる関数どうしの内積は $`0`$、同じ関数どうしは $`1`$。
- 完全：$`G`$ 上の任意の関数 $`f`$ が、これらの線形結合で書ける。係数は内積で求まる：基底を $`\phi_1, \phi_2, \dots`$ とすると $`f = \sum_m \langle \phi_m, f \rangle\, \phi_m`$。
- 正則表現の空間の内積（$`1/N`$ を付けない $`\sum_g`$）で正規直交にするには、$`\sqrt{n_a / N}`$ 倍にする。
- 証明：後で（TODO、Georgi 1章）。

系：基底の本数は空間の次元 $`N`$ に等しい。表現 $`a`$ からは $`n_a^2`$ 本の関数が出るので、

```math
N = \sum_a n_a^2
```

### [例] $`Z_3`$ 上の関数の展開
$`Z_3`$ の既約表現は全て1次元なので、行列要素は指標そのもの。$`n_a = 1`$ なので、基底は $`\chi_1, \chi_2, \chi_3`$（[例] $`Z_3`$ の指標の直交性 の指標の表の3つの列）。本数は $`3 = 1^2 + 1^2 + 1^2`$。

$`a`$ でだけ $`1`$ の関数 $`f = (f(e), f(a), f(b)) = (0, 1, 0)`$ を展開する。係数は $`c_k = \langle \chi_k, f \rangle = \tfrac13 \sum_g \chi_k(g)^* f(g) = \tfrac13 \chi_k(a)^*`$ なので、

```math
c_1 = \tfrac13, \quad c_2 = \tfrac13 \omega^* = \tfrac13 \omega^2, \quad c_3 = \tfrac13 (\omega^2)^* = \tfrac13 \omega
```

確かめ：$`c_1 \chi_1 + c_2 \chi_2 + c_3 \chi_3`$ の各成分は

```math
\begin{aligned}
e:&\quad \tfrac13 (1 + \omega^2 + \omega) = 0 \\
a:&\quad \tfrac13 (1 + \omega^2 \cdot \omega + \omega \cdot \omega^2) = \tfrac13 (1 + 1 + 1) = 1 \\
b:&\quad \tfrac13 (1 + \omega^2 \cdot \omega^2 + \omega \cdot \omega) = \tfrac13 (1 + \omega + \omega^2) = 0
\end{aligned}
```

で、$`f = (0, 1, 0)`$ に戻る。

正則表現との関係：[例] $`Z_3`$ の正則表現の直和分解 の $`S`$ の第 $`k`$ 列は $`\tfrac13 (\chi_k(e)^*, \chi_k(a)^*, \chi_k(b)^*)`$ である。正則表現を対角化する基底は、この基底（の複素共役）になっている。

### [例] $`S_3`$ 上の関数の基底
$`N = 6 = 1^2 + 1^2 + 2^2`$。$`\mathbf{1}`$ と $`\mathbf{1}'`$ から1本ずつ、$`\mathbf{2}`$ から $`2^2 = 4`$ 本（成分 $`(1,1), (1,2), (2,1), (2,2)`$）、計6本。

表：$`S_3`$ の既約表現の行列要素（$`D_{\mathbf{2}}`$ は [例] $`S_3`$ の指標の直交性 の表から）

| $`g`$ | $`D_{\mathbf{1}}`$ | $`D_{\mathbf{1}'}`$ | $`[D_{\mathbf{2}}]_{11}`$ | $`[D_{\mathbf{2}}]_{12}`$ | $`[D_{\mathbf{2}}]_{21}`$ | $`[D_{\mathbf{2}}]_{22}`$ |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| $`e`$ | $`1`$ | $`1`$ | $`1`$ | $`0`$ | $`0`$ | $`1`$ |
| $`a_1`$ | $`1`$ | $`1`$ | $`-\frac12`$ | $`-\frac{\sqrt3}{2}`$ | $`\frac{\sqrt3}{2}`$ | $`-\frac12`$ |
| $`a_2`$ | $`1`$ | $`1`$ | $`-\frac12`$ | $`\frac{\sqrt3}{2}`$ | $`-\frac{\sqrt3}{2}`$ | $`-\frac12`$ |
| $`a_3`$ | $`1`$ | $`-1`$ | $`-1`$ | $`0`$ | $`0`$ | $`1`$ |
| $`a_4`$ | $`1`$ | $`-1`$ | $`\frac12`$ | $`\frac{\sqrt3}{2}`$ | $`\frac{\sqrt3}{2}`$ | $`-\frac12`$ |
| $`a_5`$ | $`1`$ | $`-1`$ | $`\frac12`$ | $`-\frac{\sqrt3}{2}`$ | $`-\frac{\sqrt3}{2}`$ | $`-\frac12`$ |

値は全て実数なので、内積で複素共役は値を変えない。いくつか計算する（$`\lvert S_3 \rvert = 6`$）。

```math
\begin{aligned}
\langle [D_{\mathbf{2}}]_{11}, [D_{\mathbf{2}}]_{11} \rangle &= \tfrac16 \left(1 + \tfrac14 + \tfrac14 + 1 + \tfrac14 + \tfrac14\right) = \tfrac12 \\
\langle [D_{\mathbf{2}}]_{11}, [D_{\mathbf{2}}]_{22} \rangle &= \tfrac16 \left(1 + \tfrac14 + \tfrac14 - 1 - \tfrac14 - \tfrac14\right) = 0 \\
\langle [D_{\mathbf{2}}]_{12}, [D_{\mathbf{2}}]_{21} \rangle &= \tfrac16 \left(0 - \tfrac34 - \tfrac34 + 0 + \tfrac34 + \tfrac34\right) = 0 \\
\langle D_{\mathbf{1}'}, [D_{\mathbf{2}}]_{11} \rangle &= \tfrac16 \left(1 - \tfrac12 - \tfrac12 + 1 - \tfrac12 - \tfrac12\right) = 0
\end{aligned}
```

1つ目より、$`\mathbf{2}`$ の行列要素は $`\sqrt{n_a} = \sqrt2`$ 倍して長さ $`1`$ になる。6本の関数（$`\mathbf{2}`$ の成分は $`\sqrt2`$ 倍）の内積は、全ての組で単位行列になる（残りの組は Python での数値計算で確認）。

[例] $`S_3`$ の表現とその規約分解 の #7（正則表現）で使ったベクトル $`w_{\mathbf{1}}, w_{\mathbf{1}'}, w_{jk}`$ は、この6本の関数を $`\sum_g f(g) \lvert g\rangle`$ でベクトルにし、$`\sqrt{n_a / N}`$ で正規化したもの（$`w_{jk}`$ の係数 $`\tfrac{1}{\sqrt3} = \sqrt{2/6}`$）。

### [例] $`Z_N`$ とフーリエ変換
Georgi 1章の例（式 1.75〜1.77）。

$`Z_N`$ の元を $`a_j`$（$`j = 0, 1, \dots, N-1`$、$`a_0 = e`$）とし、積を次で定める。

```math
a_j a_k = a_{(j+k) \bmod N}
```

既約表現は次の $`N`$ 個で、全て1次元（$`n = 0, 1, \dots, N-1`$）。

```math
D_n(a_j) = e^{2\pi i n j / N}
```

- 表現であること：$`D_n(a_j) D_n(a_k) = e^{2\pi i n (j+k)/N}`$。$`e^{2\pi i n N/N} = 1`$ なので、$`j + k`$ を $`N`$ で割った余りに置き換えても値は同じで、$`D_n(a_{(j+k) \bmod N})`$ に等しい。
- 本数：$`N = \sum_n 1^2`$ で、[定理] 既約表現の行列要素は完全正規直交系 の系と合う。
- $`N = 3`$ では $`e^{2\pi i/3} = \omega`$、$`a_1 = a`$、$`a_2 = b`$ で、$`D_0, D_1, D_2`$ がこのノートの $`D_1, D_2, D_3`$ にあたる（添字が1つずれる）。

指標の直交性は次の形になる（Georgi 式 1.77）。

```math
\langle D_{n'}, D_n \rangle = \frac{1}{N} \sum_{j=0}^{N-1} e^{-2\pi i n' j / N}\, e^{2\pi i n j / N} = \delta_{n' n}
```

直接の確かめ：$`r = e^{2\pi i (n - n')/N}`$ とおくと、和は $`1 + r + \cdots + r^{N-1}`$。
- $`n = n'`$：$`r = 1`$ なので和は $`N`$、$`N`$ で割って $`1`$。
- $`n \neq n'`$：$`r^N = 1`$、$`r \neq 1`$ なので、和は $`\frac{r^N - 1}{r - 1} = 0`$（$`N = 3`$ では $`1 + \omega + \omega^2 = 0`$）。

$`Z_N`$ 上の関数の展開は、離散フーリエ変換そのものである。

```math
f(a_j) = \sum_{n=0}^{N-1} c_n\, e^{2\pi i n j / N}, \qquad
c_n = \langle D_n, f \rangle = \frac{1}{N} \sum_{j=0}^{N-1} e^{-2\pi i n j / N} f(a_j)
```

- Georgi は式 1.77 を「フーリエ級数の基本関係」と呼んでいる。$`N`$ 点上の関数なので、正確には離散フーリエ変換にあたる。
- 円周上の周期関数のフーリエ級数 $`f(\theta) = \sum_n c_n e^{i n \theta}`$ は、有限群ではない連続な群 $`U(1)`$ で同じことをしたものにあたる。
