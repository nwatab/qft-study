### [定義] 張る空間（span）
$V$ を $\mathbb{C}$ 上のベクトル空間、$v_1, \dots, v_k \in V$ とする。

```math
\mathrm{span}\lbrace v_1, \dots, v_k \rbrace = \lbrace c_1 v_1 + \cdots + c_k v_k : c_1, \dots, c_k \in \mathbb{C} \rbrace
```

- 係数は $V$ と同じ体（ここでは $\mathbb{C}$）からとる。

### [定義] 群
- A1 : $\forall f, g \in G,\ fg \in G$
- A2 : $\forall f, g, h \in G,\ f(gh) = (fg)h$
- A3 : $\exists e \in G,\ \forall f \in G,\ ef = fe = f$
- A4 : $\forall f \in G,\ \exists f^{-1} \in G,\ ff^{-1} = f^{-1}f = e$

### [定義] 表現
$V$ をベクトル空間とする。$G$ の $V$ 上の表現とは、$G$ の元から $V$ 上の線形演算子への写像 $D$ で、次を満たすもの：

- B1 : $D(e) = 1$
- B2 : $\forall g_1, g_2 \in G,\ D(g_1)D(g_2) = D(g_1 g_2)$

（B1, B2：$D$ は群準同型）

### [定義] 同値な表現
$V$ 上の $G$ の表現 $D$ と $D'$ は、次を満たすとき同値であるといい、$D \simeq D'$ と書く。

```math
\exists S \in GL(V),\ \forall g \in G:\ D'(g) = S^{-1} D(g)\, S
```

- 全ての $g \in G$ に同じ $S$ を使う（基底の取り替えは1回）。
- $V$ 上の $D$ と $V'$ 上の $D'$ が同値であるには、可逆な線形写像 $S: V' \to V$ が必要で、それは $\dim V = \dim V'$ のときにしか存在しない。
  したがって、次元の異なる表現は同値にならない。

### [定義] 正則表現
- $\lbrace \lvert g\rangle : g \in G \rbrace$ は $V$ の正規直交基底。したがって $\dim V = \lvert G\rvert$
- $\forall g_1, g_2 \in G,\ D(g_2)\lvert g_1\rangle = \lvert g_2 g_1\rangle$

### [例] $Z_3$

群表（行 × 列）：

| $\cdot$ | $e$ | $a$ | $b$ |
|:-:|:-:|:-:|:-:|
| $e$ | $e$ | $a$ | $b$ |
| $a$ | $a$ | $b$ | $e$ |
| $b$ | $b$ | $e$ | $a$ |

$ab = ba = e$

#### 1次元表現

```math
D(e) = 1, \quad D(a) = e^{2\pi i/3}, \quad D(b) = e^{4\pi i/3}
```

#### 正則表現
基底 $(\lvert e\rangle, \lvert a\rangle, \lvert b\rangle)$ で：

```math
D(e) = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix}, \quad
D(a) = \begin{pmatrix} 0 & 0 & 1 \\ 1 & 0 & 0 \\ 0 & 1 & 0 \end{pmatrix}, \quad
D(b) = \begin{pmatrix} 0 & 1 & 0 \\ 0 & 0 & 1 \\ 1 & 0 & 0 \end{pmatrix}
```

### [定義] 不変部分空間
線形部分空間 $W \subseteq V$ は、次を満たすとき $G$ 不変であるという。

```math
\forall g \in G,\ \forall w \in W:\ D(g)w \in W
```

### [定義] 可約 / 既約
- **可約**：$\lbrace 0 \rbrace \neq W \neq V$ となる $G$ 不変部分空間 $W$ が存在する。
- **既約**：$V \neq \lbrace 0 \rbrace$ で、$G$ 不変部分空間は $\lbrace 0 \rbrace$ と $V$ だけである。

### [例] $D(g) = I_n$
任意の $G$、$V = \mathbb{C}^n$、全ての $g \in G$ で $D(g) = I_n$（$I_n I_n = I_n$ なので B1, B2 を満たす）。
- $n = 1$：既約。1次元の $V$ には $\lbrace 0 \rbrace$ と $V$ 以外の部分空間がないので、1次元の表現はすべて既約である。
- $n \geq 2$：可約。$W = \mathrm{span}\lbrace e_1 \rbrace$ は $\lbrace 0 \rbrace \neq W \neq V$ を満たし、$D(g)w = w \in W$。
- $n \geq 2$ のとき $I_1 \not\simeq I_n$（次元が違う）。

### [定義] 直和
$D_1$ を $V_1$ 上の表現、$D_2$ を $V_2$ 上の表現とする。
$D_1 \oplus D_2$ は、次で定まる $V_1 \oplus V_2$ 上の表現である。

```math
(D_1 \oplus D_2)(g) = \begin{pmatrix} D_1(g) & 0 \\ 0 & D_2(g) \end{pmatrix}
```

- $\dim (V_1 \oplus V_2) = \dim V_1 + \dim V_2$（積ではなく和。積になるのは $\otimes$）

### [定義] 完全可約
$D$ が既約表現の直和と同値であるとき、$D$ は完全可約であるという。

```math
\exists S,\ \forall g \in G:\ S^{-1} D(g)\, S = D_1(g) \oplus D_2(g) \oplus \cdots,\quad D_j \text{ は既約}
```

同値な言い換え（$V$ が有限次元のとき）：
任意の $G$ 不変部分空間 $W$ に対して、$V = W \oplus W'$ となる $G$ 不変部分空間 $W'$ が存在する。

- 注意：可約 $\not\Rightarrow$ 完全可約。
  反例：$G = (\mathbb{R}, +)$、$V = \mathbb{C}^2$、$D(x) = \begin{pmatrix} 1 & x \\ 0 & 1 \end{pmatrix}$。
  $W = \mathrm{span}\lbrace (1,0)^T \rbrace$ は不変。
  $\beta \neq 0$ である他の直線 $\mathrm{span}\lbrace (\alpha, \beta)^T \rbrace$ は不変でない：
  $x \neq 0$ のとき $D(x)(\alpha, \beta)^T = (\alpha + x\beta, \beta)^T \notin \mathrm{span}\lbrace (\alpha, \beta)^T \rbrace$。

### [定理] 有限群の表現は完全可約
- 証明：後で（TODO）

### [例] $Z_3$ の正則表現の分解
$D$：$Z_3$ の正則表現。

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

$D \simeq D_1 \oplus D_2 \oplus D_3$、$\ 3 = 1 + 1 + 1$（$D_j$ = $j$ 番目の対角成分。値は $(e, a, b)$ の順）
- $D_1$：自明表現 $(1, 1, 1)$
- $D_2$：上の1次元表現 $(1, \omega, \omega^2)$
- $D_3$：その複素共役 $(1, \omega^2, \omega)$
- 不変部分空間 = $S$ の各列が張る空間
- $Z_3$ は可換なので、ブロックは全て $1 \times 1$。

### [例] $Z_3$ の表現とその対角化
各 $D$ は $D(a)$ で決まる：$D(e) = I$、$D(b) = D(a)^2$。どの場合も $V = \mathbb{C}^n$（#9 も同じ）。
行列は標準基底 $(e_1, e_2, \dots)$ で書く（$k$ 列目 = $e_k$ の行き先）。

既約表現（$V = \mathbb{C}$。成分 $\lambda$ は写像 $z \mapsto \lambda z$ を表す）：

| 名前 | $e$ | $a$ | $b$ | 説明 |
|---|---|---|---|---|
| $D_1$ | $1$ | $1$ | $1$ | 自明表現 |
| $D_2$ | $1$ | $\omega$ | $\omega^2$ | $D_2(a)$：$z \mapsto \omega z$、$D_2(b)$：$z \mapsto \omega^2 z$ |
| $D_3$ | $1$ | $\omega^2$ | $\omega$ | $D_2$ の複素共役 |

部品の行列：

```math
C = \begin{pmatrix} 0 & -1 \\ 1 & -1 \end{pmatrix},\quad
C^2 = \begin{pmatrix} -1 & 1 \\ -1 & 0 \end{pmatrix},\quad
P = \begin{pmatrix} 0 & 0 & 1 \\ 1 & 0 & 0 \\ 0 & 1 & 0 \end{pmatrix},\quad
P^2 = \begin{pmatrix} 0 & 1 & 0 \\ 0 & 0 & 1 \\ 1 & 0 & 0 \end{pmatrix},\quad
R(\theta) = \begin{pmatrix} \cos\theta & -\sin\theta \\ \sin\theta & \cos\theta \end{pmatrix}
```

- $C$：$e_1 \mapsto e_2$、$e_2 \mapsto -e_1 - e_2$。$C^3 = I$。
- $P$：$e_1 \mapsto e_2 \mapsto e_3 \mapsto e_1$（正則表現）。
- $R(2\pi/3)$：$2\pi/3$ の回転。$\mathbb{C}^2$ に作用する。$R(2\pi/3)^2 = R(4\pi/3)$。
- $(\lambda)$：$1 \times 1$ のブロック $\lambda$。

| # | $V$ | $D(a)$ | $D(b)$ | 説明 |
|---|---|---|---|---|
| 1 | $\mathbb{C}^2$ | $C$ | $C^2$ | $e_1 \mapsto e_2$、$e_2 \mapsto -e_1 - e_2$ |
| 2 | $\mathbb{C}^2$ | $\omega C$ | $\omega^2 C^2$ | #1 を $\omega$ 倍 |
| 3 | $\mathbb{C}^2$ | $\omega^2 C$ | $\omega C^2$ | #1 を $\omega^2$ 倍 |
| 4 | $\mathbb{C}^3$ | $P$ | $P^2$ | $e_1, e_2, e_3$ の巡回置換（三角形の頂点） |
| 5 | $\mathbb{C}^3$ | $C \oplus (\omega)$ | $C^2 \oplus (\omega^2)$ | #1 と、$e_3 \mapsto \omega e_3$ |
| 6 | $\mathbb{C}^3$ | $\omega^2 C \oplus (1)$ | $\omega C^2 \oplus (1)$ | #3 と、$e_3 \mapsto e_3$ |
| 7 | $\mathbb{C}^4$ | $P \oplus (1)$ | $P^2 \oplus (1)$ | 三角形の頂点と、動かない中心 |
| 8 | $\mathbb{C}^6$ | $P \oplus P$ | $P^2 \oplus P^2$ | 2つの三角形を同時に回す |
| 9 | $\mathbb{C}^2$ | $R(2\pi/3)$ | $R(4\pi/3)$ | 平面の $2\pi/3$ 回転 |

対角化。どの場合も $S^{-1} D(e) S = I$。$S$ の列 = 全ての $D(g)$ に共通の固有ベクトル：

```math
S_C = \begin{pmatrix} 1 & 1 \\ -\omega & -\omega^2 \end{pmatrix},\quad
S_P = \begin{pmatrix} 1 & 1 & 1 \\ 1 & \omega^2 & \omega \\ 1 & \omega & \omega^2 \end{pmatrix},\quad
S_R = \begin{pmatrix} 1 & 1 \\ -i & i \end{pmatrix}
```

| # | $S$ | $S^{-1}D(a)S$ | $S^{-1}D(b)S$ | 分解 |
|---|---|---|---|---|
| 1 | $S_C$ | $\mathrm{diag}(\omega, \omega^2)$ | $\mathrm{diag}(\omega^2, \omega)$ | $D_2 \oplus D_3$ |
| 2 | $S_C$ | $\mathrm{diag}(\omega^2, 1)$ | $\mathrm{diag}(\omega, 1)$ | $D_3 \oplus D_1$ |
| 3 | $S_C$ | $\mathrm{diag}(1, \omega)$ | $\mathrm{diag}(1, \omega^2)$ | $D_1 \oplus D_2$ |
| 4 | $S_P$ | $\mathrm{diag}(1, \omega, \omega^2)$ | $\mathrm{diag}(1, \omega^2, \omega)$ | $D_1 \oplus D_2 \oplus D_3$ |
| 5 | $S_C \oplus (1)$ | $\mathrm{diag}(\omega, \omega^2, \omega)$ | $\mathrm{diag}(\omega^2, \omega, \omega^2)$ | $D_2 \oplus D_3 \oplus D_2$ |
| 6 | $S_C \oplus (1)$ | $\mathrm{diag}(1, \omega, 1)$ | $\mathrm{diag}(1, \omega^2, 1)$ | $D_1 \oplus D_2 \oplus D_1$ |
| 7 | $S_P \oplus (1)$ | $\mathrm{diag}(1, \omega, \omega^2, 1)$ | $\mathrm{diag}(1, \omega^2, \omega, 1)$ | $D_1 \oplus D_2 \oplus D_3 \oplus D_1$ |
| 8 | $S_P \oplus S_P$ | $\mathrm{diag}(1, \omega, \omega^2, 1, \omega, \omega^2)$ | $\mathrm{diag}(1, \omega^2, \omega, 1, \omega^2, \omega)$ | $(D_1 \oplus D_2 \oplus D_3)^{\oplus 2}$ |
| 9 | $S_R$ | $\mathrm{diag}(\omega, \omega^2)$ | $\mathrm{diag}(\omega^2, \omega)$ | $D_2 \oplus D_3$ |

### [例] $S_3$
$S_3$：3つの物の置換群（対称群）。

```math
S_3 = \lbrace e, a_1, a_2, a_3, a_4, a_5 \rbrace, \quad
a_1 = (1,2,3),\ a_2 = (3,2,1),\ a_3 = (1,2),\ a_4 = (2,3),\ a_5 = (3,1)
```

- 記法：$(i, j, k)$ は、位置 $i$ の物を $j$ へ、$j$ の物を $k$ へ、$k$ の物を $i$ へ移す。$(i, j)$ は位置 $i$ と $j$ の物を入れ替える。
- 積：$gh$ = 先に $h$、次に $g$。

群表（行 × 列）：

| $\cdot$ | $e$ | $a_1$ | $a_2$ | $a_3$ | $a_4$ | $a_5$ |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| $e$ | $e$ | $a_1$ | $a_2$ | $a_3$ | $a_4$ | $a_5$ |
| $a_1$ | $a_1$ | $a_2$ | $e$ | $a_5$ | $a_3$ | $a_4$ |
| $a_2$ | $a_2$ | $e$ | $a_1$ | $a_4$ | $a_5$ | $a_3$ |
| $a_3$ | $a_3$ | $a_4$ | $a_5$ | $e$ | $a_1$ | $a_2$ |
| $a_4$ | $a_4$ | $a_5$ | $a_3$ | $a_2$ | $e$ | $a_1$ |
| $a_5$ | $a_5$ | $a_3$ | $a_4$ | $a_1$ | $a_2$ | $e$ |

#### 2次元表現
位置 1, 2, 3 = 角度 $30^\circ, 150^\circ, 270^\circ$ にある正三角形の頂点。
$D(g)$ = $g$ と同じように物を移す、平面の回転または鏡映。

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

- $D(a_1)$, $D(a_2)$：$\pm 120^\circ$ の回転。$D(a_3)$, $D(a_4)$, $D(a_5)$：動かない頂点を通る直線についての鏡映。

#### [主張] この2次元表現は既約
- 可約だとすると、完全可約性から $D \simeq D_1 \oplus D_2$（$D_1, D_2$ は1次元）となり、全ての $D(g)$ が可換になる。
- しかし $a_1 a_3 = a_5 \neq a_4 = a_3 a_1$ なので、$D(a_1) D(a_3) \neq D(a_3) D(a_1)$。
- 注意：$S_3$ にも1次元の既約表現はある（自明表現など）。非可換であることが意味するのは、既約表現が全て1次元とは限らないということ。

#### [例] $S_3$ の既約表現
同値を除いて、$S_3$ の既約表現はちょうど3つ：

| | $e$ | $a_1, a_2$ | $a_3, a_4, a_5$ | 次元 |
|:-:|:-:|:-:|:-:|:-:|
| 自明表現（trivial） | $1$ | $1$ | $1$ | 1 |
| 符号表現（sign） | $1$ | $1$ | $-1$ | 1 |
| 2次元表現（上のもの） | $I_2$ | 回転 | 鏡映 | 2 |

1次元のものは自明表現と符号表現に限る。$D$ を1次元とする（数は可換）。
- $a_3 a_4 = a_1$、$a_4 a_3 = a_2$ なので、$D(a_1) = D(a_3)D(a_4) = D(a_4)D(a_3) = D(a_2)$。
- $a_1 a_1 = a_2$ なので $D(a_1)^2 = D(a_2) = D(a_1)$。$D(a_1) \neq 0$ なので $D(a_1) = D(a_2) = 1$。
- $a_3 a_3 = e$ なので $D(a_3) = \pm 1$。
- $a_1 a_3 = a_5$、$a_1 a_5 = a_4$ なので $D(a_5) = D(a_4) = D(a_3)$。
- 符号表現が表現であること：群表より、$a_3, a_4, a_5$ のうち2つの積は $\lbrace e, a_1, a_2 \rbrace$ に入り、そのうち1つと $e, a_1, a_2$ のどれかとの積は $\lbrace a_3, a_4, a_5 \rbrace$ に入る。

どの2つも同値でない：
- 自明表現 $\not\simeq$ 符号表現：1次元では $S^{-1} x S = x$ なので、同値とは等しいことであり、2つは $a_3$ で値が違う。
- 2次元表現はどちらとも同値でない：次元が違う。

他にはない：
- 既約表現について $\sum_a n_a^2 = \lvert G \rvert$（$n_a$ = 次元）。ここでは $1^2 + 1^2 + 2^2 = 6 = \lvert S_3 \rvert$ なので、他の既約表現が入る余地はない。この和の公式の証明：後で（TODO、Georgi 1.12）。

### [定義] 部分群
$H \subseteq G$ が $G$ の積について群になるとき、$H$ を $G$ の部分群という。

### [例] $Z_3 \subset S_3$
$\lbrace e, a_1, a_2 \rbrace$ は $S_3$ の部分群で、$Z_3$ と同型（$a_1 \mapsto a$、$a_2 \mapsto b$）。

### [定義] 右剰余類 / 左剰余類
$H$ を $G$ の部分群、$g \in G$ とする。
- 右剰余類：$Hg = \lbrace hg : h \in H \rbrace$
- 左剰余類：$gH = \lbrace gh : h \in H \rbrace$

### [定義] 正規部分群
$G$ の部分群 $H$ は、次を満たすとき正規部分群（不変部分群）であるといい、$H \trianglelefteq G$ と書く。

```math
\forall g \in G:\ gH = Hg
```

同値な言い換え：

```math
\forall g \in G,\ \forall h \in H:\ g h g^{-1} \in H
```

### [定義] 剰余群
$H \trianglelefteq G$ のとき、剰余類の集合 $G/H = \lbrace Hg : g \in G \rbrace$ は、集合の積
$AB = \lbrace ab : a \in A,\ b \in B \rbrace$ について群になる：

```math
(Hg_1)(Hg_2) = H(g_1 H)g_2 = H(H g_1)g_2 = (HH)\,g_1 g_2 = H g_1 g_2
```

- 2つ目の等号で $g_1 H = H g_1$（正規性）を使う。
- $HH = \lbrace h_1 h_2 : h_1, h_2 \in H \rbrace = H$：
  - $\subseteq$：$h_1, h_2 \in H \Rightarrow h_1 h_2 \in H$（$H$ についての A1）。
  - $\supseteq$：$e \in H$ なので、全ての $h \in H$ は $h = eh \in HH$。
$G/H$ の群の公理（どれも $(Hg_1)(Hg_2) = Hg_1g_2$ から従う）：
- A1：$(Hg_1)(Hg_2) = Hg_1g_2 \in G/H$。
- A2：$\big((Hg_1)(Hg_2)\big)(Hg_3) = H(g_1g_2)g_3 = Hg_1(g_2g_3) = (Hg_1)\big((Hg_2)(Hg_3)\big)$（$G$ の A2 による）。
- A3：単位元は $H = He$。$(He)(Hg) = Hg = (Hg)(He)$ なので。
- A4：$Hg$ の逆元は $Hg^{-1}$。$(Hg)(Hg^{-1}) = He = (Hg^{-1})(Hg)$ なので。

### [例] $S_3$ の正規部分群
- TODO
