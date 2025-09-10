---
{"dg-publish":true,"permalink":"/A_symmetry_自然界的对称性/Tools/Lie Group/","noteIcon":"","created":"2024-11-30T23:35:43.866+08:00","updated":"2025-09-10T13:11:30.945+08:00"}
---


# 1 $Group$ (群)
一个 $group$ (称 "$G$") 是一个集合，加上一个群乘法 “$\circ$”，且满足以下公理：
- *封闭性*。$\forall g_1, g_2 \in G,\ g_1\circ g_2 \in G$.
- *单位元（恒等变换）*。$\exists e\in G,\ s.t. \forall g \in G,\ g=e\circ g=g\circ e$.
- *逆元（逆变换）*。$\forall g\in G,\ \exists g^{-1}\in G,\ s.t.\ e=g^{-1}\circ g=g\circ g^{-1}$.
- *结合律*。$\forall g_1, g_2, g_3\in G,\ (g_1\circ g_2)\circ g_3=g_1\circ( g_2\circ g_3)$.

# 2 $2D\ Rotation$ (二维旋转群)
## 2.1 $O(2)$ 和 $SO(2)$
考虑让二维平面的向量长度不变的变换($G^TG=I$)：包括旋转和反演。或者严格讲是保持内积不变的变换。

将位于原点的向量 $\vec X = (x,y)^T$ 绕 $O$ 逆时针旋转角度 $\theta$ 后，方向变为 $\vec X'=(x',y')^T$，记 $\vec X'=R(\theta)\vec X$:
$$
R(\theta) = 
\begin{bmatrix} cos\theta & -sin\theta \\  sin\theta & cos\theta \end{bmatrix}
$$
注意，如果旋转的是坐标系，向量方向坐标的变化也表示为 $\vec X'=R(\theta)\vec X$ 的话，$R(\theta)$ 需要取逆。

关于 $x、y$ 轴的反演矩阵显然为：
$$
P_x = diag(-1,1),\ P_y = diag(1,-1)
$$
此时矩阵乘法可以作为群乘法的一种表示方式。  

> [!note]
> $O(2)$: 满足 $O^TO=I$  
> 
> $SO(2)$: 满足 $det(O)=1$ 的 $O(2)$群

"$O$"即"$orthogonal$"(正交), "$S$"即 $special$.

## 2.2 $U(1)$
> [!note]
>  $U(1)$: 单位复数构成的群, 或者说 $U^*U=I$，或者说 $U=e^{i\theta}$  

"$U$"即"$unitary$"(幺正,单位的,酉).

$U(1)$ 可以将二维平面的复数进行旋转，$e$ 指数上的 $\theta$ 就是上一节的二维实旋转的 $\theta$。即：
$$
1 = \begin{bmatrix} 1 & 0 \\  0 & 1 \end{bmatrix}
,\ i=e^{i \frac{\pi}{2}}=\begin{bmatrix} 0 & -1 \\  1 & 0 \end{bmatrix}, \ 
U(\theta) = \begin{bmatrix} cos\theta & -sin\theta \\  sin\theta & cos\theta \end{bmatrix}
$$
可见，任意复数对应的群元可以表示为矩阵形式：
$$
z=a+ib=\begin{bmatrix} a & -b \\  b & a \end{bmatrix}
$$
于是复数的旋转可以表示为：
$$
z' = U(\theta)z= \begin{bmatrix} cos\theta & -sin\theta \\  sin\theta & cos\theta \end{bmatrix}\begin{bmatrix} a & -b \\  b & a \end{bmatrix}
$$
## 2.3 $U(1)$ 和 $SO(2)$
只取第一列：
$$
\begin{bmatrix} a' \\ b' \end{bmatrix}= \begin{bmatrix} cos\theta & -sin\theta \\  sin\theta & cos\theta \end{bmatrix}\begin{bmatrix} a \\  b \end{bmatrix}
$$
其对应二维实旋转，当视为 $x,y\to a,b$.

```col
> [!info] 同构
> 如果映射 $\Pi: G \rightarrow G^{\prime}$ 一一映射, 并且满足: 
> $ \forall g_{1}, g_{2} \in G,\ \Pi\left(g_{1}\right) \circ\Pi\left(g_{2}\right)=\Pi\left(g_{1} \circ g_{2}\right) 
> $
> 则 $\Pi$ 就是同构映射, 并且称 $G, G^{\prime}$ 是同构的。
```

显然 $U(1),SO(2)$ 是同构的。

注意, 我们没有讨论 $SU(1)$, 因为 $det(U)=1$ 得到 :
$$
SU(1)={1}
$$
即 $SU(1)$ 只包含单位元，是一个平凡群。

# 3 $3 D\ Rotation$ (三维旋转群)
## 3.1 $O(3)$ 和 $SO(3)$
```col
> $O(3)$: 满足 $O^TO=I$
```
```col
> $SO(3)$: 满足 $det(O)=1$ 的 $O(3)$群
```
$SO(3)$ 群的基：
$$
R_x=\begin{pmatrix} 1 & &  \\ & cos\theta &  -sin\theta \\  & sin\theta & cos\theta \end{pmatrix},
R_y = \begin{pmatrix} cos\theta &  & {\color{red}+} sin\theta \\  & 1 &   \\ -sin\theta &  & cos\theta \end{pmatrix}.
R_z=\begin{pmatrix} cos\theta & -sin\theta &  \\ sin\theta & cos\theta &   \\  &  & 1 \end{pmatrix}.

$$
## 3.2 $SU(2)$ 和 四元数
定义三个虚数单位：
$$
\mathbf{i}^2=\mathbf{j}^2=\mathbf{k}^2=-1
$$
于是任意四元数 $q(quaternion)$ 可以表示为：
$$
q = a + b\mathbf{i} + c\mathbf{j} + d\mathbf{k}
$$
定义四元数之间的乘法：
$$
\mathbf{ijk}=-1
$$
这个定义和 $\mathbf{i}^2=\mathbf{j}^2=\mathbf{k}^2=-1$ 导致轮换性（注意轮换性和交换律不同），即：
$$
\mathbf{
ij}=\mathbf{k},\ \mathbf{jk}=\mathbf{i},\ \mathbf{ki}=\mathbf{j},\ \mathbf{jki}=-1,\cdots
$$

定义单位四元数满足：
$$
q^\dagger q=1
$$
四元数单位的复矩阵表述（也可以用四维实矩阵）：
$$
\begin{array}{ll}
\mathbf{1}=\left(\begin{array}{ll}
1 & 0 \\
0 & 1
\end{array}\right), \quad \mathbf{i}=\left(\begin{array}{cc}
0 & 1 \\
-1 & 0
\end{array}\right) \\
\mathbf{j}=\left(\begin{array}{ll}
0 & i \\
i & 0
\end{array}\right), \quad \mathbf{k}=\left(\begin{array}{cc}
i & 0 \\
0 & -i
\end{array}\right)
\end{array}
$$
不难验证上式满足四元数乘法。这样任意一个四元数都可用矩阵表示为：
$$
q=a \mathbf{1}+b \mathbf{i}+c \mathbf{j}+d \mathbf{k}=\left(\begin{array}{cc}
a+d i & b+c i \\
-b+c i & a-d i
\end{array}\right)
$$

由上式可见
$$
\operatorname{det}(q)=a^{2}+b^{2}+c^{2}+d^{2}=q^\dagger q=1
$$

单位四元数对应的 $2 \times 2$ 复数矩阵 $\mathcal{U}$ 满足：
$$
\mathcal{U}^{\dagger} \mathcal{U}=1, \ \operatorname{det}(\mathcal{U})=1
$$

>  $\mathcal{S U}(2)$： $\forall$ 单位四元数都唯一对应 $\mathcal{S U}(2)$ 群中的一个群元。

## 3.3 $SO(3)$ 和 $SU(2)$
将三维向量 $\vec{v}=(x, y, z)$ 定义为如下四元数：
$$
v \equiv x \mathbf{i}+y \mathbf{j}+z \mathbf{k}
$$
将旋转变换表示为（$U$ 为单位四元数）：
$$
v' = U^{-1}vU = U^\dagger v U
$$
例如绕 $z$ 轴旋转和任意三维向量的矩阵形式为：
$$\begin{array}{c}
U_z(\theta) = \mathbf{1}cos\theta + \mathbf{k}sin\theta = \begin{bmatrix} cos\theta+isin\theta &  \\   & cos\theta-isin\theta \end{bmatrix} = \begin{bmatrix} e^{i\theta} &  \\   & e^{-i\theta} \end{bmatrix},\\  \\
\vec v = v_x\mathbf{i}+v_y \mathbf{j}+v_z \mathbf{k} = \begin{bmatrix} iv_z & v_x+iv_y \\  -v_x+iv_y & -iv_z \end{bmatrix}
\end{array}
$$
注意，这导致的旋转角将是 $SO(3)$ 的两倍。
```col
> [!info] <font color="#ff0000">双覆盖</font>
>  $SU(2)$ 称为 $SO(3)$ 群的双覆盖，因为可以找到两个 $SU(2)$ 群元对应一个 $SO(3)$ 群元。这是因为 $SO(3)$ 的旋转角只有 $SU(2)$ 的一半，而旋转角有 $2\pi$ 的周期。
```

# 4 $Lie\ Algebra$ (李代数)
*Lie 代数研究连续对称性*
## 4.1 $Simple\ Definition$ (简要定义)
无限小变换根据 $Taylor$ 展开表示为：
$$
g(\epsilon) = 1+\epsilon X
$$
$X$ 称为生成元。对于有限旋转 $\theta=N\epsilon,\ N\to \infty$:
$$
R(\theta) = \left[ g\left( \frac{\theta}{N} \right) \right]^N = 
\\lim_{ N \to \infty } \left( 1+ \frac{\theta X}{N} \right)^N
= e^{\theta X}
$$
即有限旋转都可以由 $e$ 指数表示。

```col
> [!info] Lie 代数
>  群元是 $n \times n$ 矩阵 $Lie$群 $G$ 对应的的 $Lie$代数 $\mathfrak{g}$ 是满足如下条件的 $n \times n$ 矩阵 $X$ 的集合:
> $
> \mathrm{e}^{t \mathfrak{g}} \in G,\ t \in \mathbb{R}
> $
```

$Lie$ 群 $G$ 的乘法与 $Lie$ 代数 $\mathfrak{g}$ 结合法则由 $Baker-Campbell-Hausdorff$ 公式描述：
$$
\underset{\in G}{\underbrace{g} } \circ \underset{\in G}{\underbrace{h} } = e^X\circ e^Y
= exp\left\{ X+Y+ \frac{1}{2}[X,Y] + \frac{1}{12}[X,[X,Y]] - \frac{1}{12}[Y,[X,Y]]+ \cdots   \right\}
$$
"\[...\]" 表示对易子或者说 $Lie$ 括号。

注意，对于 $Lie$ 代数的生成元，对易子封闭，而群乘法不具有封闭性：$\forall X,Y\in \mathfrak{g},\ [X,Y]\in \mathfrak{g},\ X\circ Y \notin \mathbf{g}$. 这与 Lie 群不同。

## 4.2 $SO(3)$ 的生成元
根据 $SO(3)$ 群的定义：
$$
O^TO=I,\ det(O)=1
$$
以及任意群元 $O$ 对应的生成元 $J$：
$$
O=e^{\theta J}
$$
得到 $J$ 满足：
$$
J=-J^T,\ tr(J)=0
$$
第一个式子来自于 $O^TO=I$，并使用了 $[J^T,J]=0$（限制 $J\in$ 正规矩阵），第二个式子来自于 $det(O)=1$，并使用了 $det(e^A)=e^{tr(A)}$.

满足上式的三个线性无关的基是：
$$
J_x = \begin{pmatrix} 0 & 0 & 0 \\ 0 & 0 & -1 \\ 0 & 1 & 0 \end{pmatrix},\  
J_y = \begin{pmatrix} 0 & 0 & 1 \\ 0 & 0 & 0 \\ -1 & 0 & 0 \end{pmatrix},\
J_z = \begin{pmatrix} 0 & -1 & 0 \\ 1 & 0 & 0 \\ 0 & 0 & 0 \end{pmatrix}.
$$

显然，将 $SO(3)$ 的三个基取 $\theta\to0$ 留下一阶部分，再除以 $\theta$ 就是上式。

$J$ 满足对易关系：
$$
[J_i,J_j]=\epsilon_{ijk}J_k
$$
类似的，$SO(2)$ 的生成元是：
$$
J(SO(2))=\begin{pmatrix} 0 & -1 \\  1 & 0 \end{pmatrix}
$$
容易利用 $e^{\theta J},cos(\theta J),sin(\theta J)$ 的 $Taylor$ 展开，从而由上式得到 $SO(2)$ 群元的矩阵形式就是二维旋转矩阵。

将 $J$ 乘以 $i\hbar$，就得到量子力学里生成元 (厄米矩阵，本征值为实数)。此时对易条件变为：
$$
[J_i,J_j]=i\hbar\epsilon_{ijk}J_k
$$

## 4.3 $Abstract\ Definition$ (李代数的抽象定义)
```col
> [!info] Lie 代数
> $Lie$ 代数是一个向量空间 $\mathfrak{g}$， 并配备一个二元运算 $[...]$: $\mathfrak{g} \times \mathfrak{g} \rightarrow \mathfrak{g}$, [...] 满足如下公理:
> - 双线性:  $\forall a, b \in \mathbb{R},\ \forall X, Y, Z \in \mathfrak{g},\ [a X+b Y, Z]=a[X, Z]+   b[Y, Z],\ [Z, a X+b Y]=a[Z, X]+b[Z, Y]$;
> - 反交换律:  $\forall X, Y \in \mathfrak{g},\ [X, Y]=-[Y, X]$;
> - Jacobi 恒等式:  $\forall X, Y, Z \in \mathfrak{g},\ [X,[Y, Z]]+[Z,[X, Y]]+[Y,[Z, X]]=  0$.
```

对易子、$Poisson$ 括号满足上述二元运算的定义。

注意，以上抽象定义的 $Lie$ 代数完全不依赖于 $Lie$ 群。

## 4.4 $SU(2)$ 的生成元和群元
设 $SU(2)$ 的生成元 $J$ 满足 $U=e^{i \theta J}$，得到：
$$
J^\dagger=J,\ tr(J)=0
$$
满足这两个条件的基可以取为 $Pauli$ 矩阵：
$$
\sigma_x=\begin{pmatrix} 0 & 1 \\  1 & 0 \end{pmatrix},\
\sigma_y=\begin{pmatrix} 0 & -i \\  i & 0 \end{pmatrix},\
\sigma_z=\begin{pmatrix} 1 & 0 \\  0 & -1 \end{pmatrix},\
$$
令 $J_i=\frac{\hbar}{2}\sigma_i$，它也满足上述两个要求, 并且有对易条件：
$$
[J_i,J_j]=i\hbar\epsilon_{ijk}J_k
$$
这与 $SO(3)$ 一致。

将其还原回 $Lie$ 群群元, 先定义旋转轴为单位向量 $\hat{n} = (n_x, n_y, n_z)$，旋转角度为 $\theta$，则群元可以写为：k
$$
U(\hat{n}, \theta) = e^{i \frac{\theta}{2} (\vec{n} \cdot \vec{\sigma})},
$$
其中 $\vec{n} \cdot \vec{\sigma} = n_x \sigma_x + n_y \sigma_y + n_z \sigma_z$。$Taylor$ 展开为：
$$
U(\hat{n}, \theta) = \cos\left(\frac{\theta}{2}\right) I + i \sin\left(\frac{\theta}{2}\right) (\vec{n} \cdot \vec{\sigma}).
$$
于是关于 $x, y, z$ 方向旋转的群元分别为：
$$
\begin{array}{l}
U_x(\theta_x) = \cos\left(\frac{\theta_x}{2}\right) I + i \sin\left(\frac{\theta_x}{2}\right) \sigma_x 
=\begin{pmatrix}
  \cos\left(\frac{\theta_x}{2}\right) & i \sin\left(\frac{\theta_x}{2}\right) \\
  i \sin\left(\frac{\theta_x}{2}\right) & \cos\left(\frac{\theta_x}{2}\right)
  \end{pmatrix}
\\
U_y(\theta_y) = \cos\left(\frac{\theta_y}{2}\right) I + i \sin\left(\frac{\theta_y}{2}\right) \sigma_y
=\begin{pmatrix}
  \cos\left(\frac{\theta_y}{2}\right) & \sin\left(\frac{\theta_y}{2}\right) \\
  -\sin\left(\frac{\theta_y}{2}\right) & \cos\left(\frac{\theta_y}{2}\right)
  \end{pmatrix} \\
U_z(\theta_z) = \cos\left(\frac{\theta_z}{2}\right) I + i \sin\left(\frac{\theta_z}{2}\right) \sigma_z 
=\begin{pmatrix}
  e^{i \frac{\theta_z}{2}} & 0 \\
  0 & e^{-i \frac{\theta_z}{2}}
  \end{pmatrix}
\end{array}
$$
根据下式( 3.2 节)可以得到任意三维向量 $\vec v$ 在 $SO(3)$ 的旋转 :
$$
v' = U^{-1}vU = U^\dagger v U
$$
$$
\vec v = v_x\mathbf{i}+v_y \mathbf{j}+v_z \mathbf{k} = \begin{bmatrix} iv_z & v_x+iv_y \\  -v_x+iv_y & -iv_z \end{bmatrix}
$$
## 4.5 李群的抽象定义
```col
> [!info] $Lie$ 群
> $Lie$ 群是一个群, 也是一个微分流形。这个流形满足如下条件:
> - 群乘法。诱导出的从流形到流形自身的映射必须是可微的。这称为相容性条件，它保证了群定义与流形定义的兼容。例如，群 $G$ 的任意群元 $a$ 诱导出了从 $G$ 到 $G$ 的映射：给定 $\forall b \in G  ，  c \equiv a \circ b \in G$ ，映射 $a: b\in G \rightarrow c\in G$ 必须是可微的。
> - 流形中的任意点都有相应的坐标, 可以用坐标的语言表示上述内容: $c=a b$ 对应的坐标必须是 $b$ 的坐标的可微函数。
```

```col
> [!info] 覆盖群
> 任一 $Lie$ 代数仅对应一个单连通 $Lie$ 群，该群称为覆盖群。（单连通： 流形上任意闭合曲线可以平滑地收缩为流形中的一点）
```

比如满足 $[J_i,J_j]=i\hbar\epsilon_{ijk}J_k$ 的 Lie 代数对应的覆盖群是 $SU(2)$，其流形是一个三维单位超球面 $S^3$（四维球面），是单连通的，而 $SO(3)$ 是单位超球面的一半，是 $SU(2)$ 的商空间，非单连通。

总结：

$$
\begin{array}{c}
S^1=U(1)\ \ \underset{同构}{\underbrace{\longleftrightarrow} }\ \ SO(2) \\
S^3=SU(2)\ \ \underset{覆盖}{\underbrace{\longrightarrow} }\ \ SO(3)
\end{array}
$$

# 5 表示论
```col
> [!info] 群的表示
>群 G 的一个表示 R 指的是从 *G* 到*某个向量空间 V 上的全体线性变换组成的集合*的映射：$R:\underset{\in G}{\underbrace{g} } \to R(g)$
```

$R(g)$表示某个矩阵变换，比如矩阵乘法。称 $R$ 为同态映射，当：
 - $R(e)=I$，恒等群元对应恒等变换。
 - $R(g^{-1})=R^{-1}(g)$，逆群元对应逆变换。
 - $R(g)\circ R(h)= R(g\circ h)$，变换的结合律。

例如，对于三维向量空间 $\mathbb{R}^3$，旋转矩阵是 $SO(3)$ 的一种表示，或者说是 $SO(3)$ 到 $\mathbb{R}^3$ 上全体旋转变换的同态映射。

下面给出一些定义，为下一节做铺垫：

```col
>[!info] 不变子空间 V'
> $
> \exists V'\subset V,\ s.t.\forall v\in V',g\in G,\ 满足\ R(g)v\in V'
> $
```
```col
>[!info] 子表示 R'
> $
> R(g)v=R'(g)v,\ \forall v\in V',g\in G
> $
```
```col
>[!info] <font color="#ff0000">不可约表示 R</font>
> R 不能分解为子表示，V 也不能分解成不变子空间
```
```col
> [!info] Casimir 元
> Casimir 元（记作 C）对任意生成元 $X$ 都有
> $
> [C, X]=0
>$
```
```col
> [!info] Schur 引理
> 给定一个不可约群表示 $R: \mathfrak{g} \rightarrow   G L(V)$，如果某个线性变换 $T: V \rightarrow V$（即 $T \in G L(V)$ ）与所有 $R(g), \forall g \in G$ 对易，则 $T$ 必为恒等变换的常数倍。其中 $G L(V)$ 表示向量空间 V 上所有线性变换的集合。
```

# 6 $SU(2)$ 的深入讨论
## 6.1 $SU(2)$ 的不可约表示
回顾 $4.4$ 节, 已经得到：

$$
\sigma_x=\begin{pmatrix} 0 & 1 \\  1 & 0 \end{pmatrix},\
\sigma_y=\begin{pmatrix} 0 & -i \\  i & 0 \end{pmatrix},\
\sigma_z=\begin{pmatrix} 1 & 0 \\  0 & -1 \end{pmatrix},\
J_i=\frac{\hbar}{2}\sigma_i，\ 
[J_i,J_j]=i\hbar\epsilon_{ijk}J_k.
$$
引入（升降算符）：
$$
J_{\pm}=\frac{1}{\sqrt 2}(J_1 \pm iJ_2)
$$
根据对易子性质得到:
$$
\begin{array}{c}
[J_3,J_{\pm}] = [J_3,\frac{1}{\sqrt 2}(J_1 \pm iJ_2)]
=[J_3,\frac{1}{\sqrt 2}J_1 ]+[J_3,\pm \frac{1}{\sqrt 2}iJ_2]
=\pm \hbar J_{\pm} \\ \\
[J_+,J_-] = \hbar J_3
\end{array}
$$

注意, $SO(3)$ 中将定义中的 $\sqrt 2$ 去掉, 即 $J_{\pm}=J_1 \pm iJ_2$, 第三式将变为 $[J_+,J_-] = 2\hbar J_3$ (多一个 $2$). 回顾 $SO(3)$ 的生成元以跟 $Pauli$ 矩阵做对比:
$$
J_x = i\hbar\begin{pmatrix} 0 & 0 & 0 \\ 0 & 0 & -1 \\ 0 & 1 & 0 \end{pmatrix},\  
J_y = i\hbar\begin{pmatrix} 0 & 0 & 1 \\ 0 & 0 & 0 \\ -1 & 0 & 0 \end{pmatrix},\
J_z = i\hbar\begin{pmatrix} 0 & -1 & 0 \\ 1 & 0 & 0 \\ 0 & 0 & 0 \end{pmatrix}.
$$

其升降含义是:
$$
J_3v=\lambda v \to J_3(J_{\pm}v)=(\lambda\pm1)(J_{\pm}v)
$$

有限维空间中, $J_3$ 的本征值 $m$ 具有最大/小值 $-j$ 和 $j$ ($j$ 为整数 or 半整数), 其对应的本征态矢量为 $v_{max}/v_{min}$ , 则:
$$
J_+v_{max} = J_-v_{min} = 0
$$

对应的 $2j+1$ 个本征态矢量张成了不变子空间 (或者称不可约表示空间), $J_{\pm}$ 为不可约表示.

若 $J_3$ 的本征值 $m$ 对应的本征态是 $| m \rangle$, 则:
$$
J_{\pm}|m\rangle = \frac{1}{\sqrt 2}\hbar\sqrt{j(j+1)-m(m+1)}\ |m+1\rangle
$$
对于 $SO(3)$, 需要将上式中的 $\sqrt 2$ 去掉.

## 6.2 $SU(2)$ 的 $Casimir$ 算符和群表示
$SU(2)$ 的 $Casimir$ 算符恰好是 $J^2=\sum_{i=1}^3 J_i^2$ : 
$$
[J^2, J_i] = 0
$$
根据 $J^2=\sum_{i=1}^3 J_i^2=J_+J_- + J_-J_+ + J_3^2$ :
$$
J^2 v= j(j+1)\hbar^2\  v
$$
## 6.3 $SU(2)$ 的 $2j+1$ 维不可约群表示
我们以 $2j+1$ 作为群表示的维数, 可以区分不同维数的群表示 :

$SU(2)$ 的一维群表示是单位变换 $1$, 对应的生成元是 $0$. ($p59$)

二维群表示是 $\frac{\hbar}{2}\sigma_i$ , 简要推导过程如下 : 可以看出 $J_3$ 的本征值是 $-\frac{1}{2}\hbar, \frac{1}{2}\hbar$ , 于是:
$$
J_3=\frac{\hbar}{2}\begin{pmatrix} 1 & 0 \\  0 & -1 \end{pmatrix}
$$
根据:
$$
J_{\pm}|m\rangle = \frac{1}{\sqrt 2}(J_1 \pm iJ_2)|m\rangle = \frac{1}{\sqrt 2}\hbar\sqrt{j(j+1)-m(m+1)}\ |m+1\rangle
$$
容易从 $|\pm j\rangle$ 之一递推求得 $J_{1,2} = \frac{\hbar}{2}\sigma_{1,2}$ .

三维群表示是类似的, 先根据 $J_3$ 的本征值是 $-\hbar,0, \hbar$ , 得到:
$$
J_3= \frac{1}{\sqrt 2} \begin{pmatrix} 1 & 0 & 0 \\ 0 & 0 &  0 \\ 0 & 0 & -1 \end{pmatrix}
$$
进一步可以递推得到:
$$
J_1 = \frac{1}{\sqrt 2}\begin{pmatrix} 0 & 1 & 0 \\ 1 & 0 &  1 \\ 0 & 1 & 0 \end{pmatrix},\ \ 
J_1 = \frac{1}{\sqrt 2}\begin{pmatrix} 0 & -i & 0 \\ i & 0 &  -i \\ 0 & i & 0 \end{pmatrix}
$$
# 7 $O(1,3)$: $Lorentz\ Group$ (洛伦兹群)
## 7.1 $Definition$
```col
> [!info] Lorentz 群 $\Lambda$
> 洛伦兹群的作用对象是四维 $Minkowski$ 空间, 并且保持其内积不变: $x^\mu \to x'^\mu = \Lambda^\mu_\nu x^\nu   \ \Rightarrow\     x'^\mu\eta_{\mu\nu}x'^{\nu}=x^\mu\eta_{\mu\nu}x^{\nu}$
```

上述定义等价于:
$$
\Lambda_{\mu}^{\sigma} \eta_{\sigma \rho} \Lambda_{\nu}^{\rho} = \eta_{\mu \nu}
$$

或者写成矩阵形式 :
$$
\Lambda^{T} \eta \Lambda = \eta
$$

对上式取行列式可得：
$$
\begin{aligned}
\operatorname{det}(\Lambda) \underbrace{\operatorname{det}(\eta)}_{=-1} \operatorname{det}(\Lambda)=\underbrace{\operatorname{det}(\eta)}_{=-1} 
& \rightarrow \operatorname{det}(\Lambda)^{2} = 1 \\
& \rightarrow \operatorname{det}(\Lambda) = \pm 1
\end{aligned}
$$

取度规的 $\mu=\nu=0$ 分量 :
$$
\begin{array}{l}
& \Lambda_{0}^{\sigma} \eta_{\sigma \rho} \Lambda_{0}^{\rho} = \underbrace{\eta_{00}}_{=1} \\
\to  & \Lambda_{0}^{\sigma} \eta_{\sigma \rho} \Lambda_{0}^{\rho}=\left(\Lambda_{0}^{0}\right)^{2}-\sum_{i\neq0}\left(\Lambda_{0}^{i}\right)^{2} = 1 \\
\to  & \Lambda_{0}^{0} = \pm \sqrt{1+\sum_{i\neq0}\left(\Lambda_{0}^{i}\right)^{2}}
\end{array}
$$

根据上述两个约束的正负可以把 $Lorentz$ 群分成 $4$ 个分支。不涉及坐标反演的两个分支满足 $\operatorname{det}(\Lambda)=+1$. 

```col
> [!info] $SO(1,3)^\uparrow$
> 满足 $\operatorname{det}(\Lambda) = 1$ 和 $\Lambda^0_0\geq 0$ 称为正规 $Lorentz$ 群 $SO(1,3)^\uparrow$.
```
引入宇称变换和时间反演变换 :
$$
\Lambda_P = diag(1,-1,-1,-1),\ \ \Lambda_T=diag(-1,1,1,1)
$$
于是 $O(1,3)$ 可以表示为四个分支的集合:
$$
O(1,3) = \{SO(1,3)^\uparrow,\ \Lambda_P SO(1,3)^\uparrow,\ \Lambda_T SO(1,3)^\uparrow,\ \Lambda_P \Lambda_T SO(1,3)^\uparrow \}
$$

## 7.2 $SO(1,3)^\uparrow$的生成元
考虑无穷小变换 : 
$$
\Lambda_\rho^\mu = \delta_\rho^\mu + \epsilon K_\rho^\mu
$$
使其满足 $\Lambda_{\mu}^{\sigma} \eta_{\sigma \rho} \Lambda_{\nu}^{\rho} = \eta_{\mu \nu}$, 显然意味着 $\operatorname{det}(\Lambda) = 1,\ \Lambda_{0}^{0} = \sqrt{1+\sum_{i\neq0}\left(\Lambda_{0}^{i}\right)^{2}}$, 即对应 $SO(1,3)^\uparrow$ .

代入 $\Lambda_{\mu}^{\sigma} \eta_{\sigma \rho} \Lambda_{\nu}^{\rho} = \eta_{\mu \nu}$ , 并忽略 $\epsilon^2$ 得到 :
$$
\begin{array}{c}
K_\rho^\mu \eta_{\mu\sigma} + \eta_{\rho\nu}K_\sigma^\nu = 0 \\ \\
{\small or}: \quad K^T\eta + \eta K = 0
\end{array}
$$
英文中常常称 $Lorentz$ 变换为 "**boost**", 先考虑关于 $x$ 轴的 $boost$, 即 $y'=y, z'=z$, 其生成元可以假设为 :
$$
K_x
= \begin{pmatrix} \underset{记作\ k_x}{\underbrace{\begin{pmatrix} a & b \\  c & d \end{pmatrix}} }  &  \\   & \begin{pmatrix} 0 & 0 \\  0 & 0 \end{pmatrix} \end{pmatrix}
$$
代入 $K^T\eta + \eta K = 0$ 得到 :
$$
K_x = \begin{pmatrix} 0 & 1 & 0 & 0 \\ 1 & 0 &  0 & 0\\ 0 & 0 & 0 & 0 \\  0 & 0 & 0 & 0 \end{pmatrix}
$$
类似的有 :
$$
K_y = \begin{pmatrix} 0 & 0 & 1 & 0 \\ 0 & 0 &  0 & 0\\ 1 & 0 & 0 & 0 \\  0 & 0 & 0 & 0 \end{pmatrix}, \quad
K_z = \begin{pmatrix} 0 & 0 & 0 & 1 \\ 0 & 0 &  0 & 0\\ 0 & 0 & 0 & 0 \\  1 & 0 & 0 & 0 \end{pmatrix}
$$
根据 $\Lambda_x = e^{\phi K_x}$ 可以得到 $Lie$ 群表示, 注意到 $k_x^2=I_{2\times 2}$ :
$$
 \begin{aligned}
\Lambda_{x}(\phi)  =\mathrm{e}^{\phi k_{x}}
&=\sum_{n=0}^{\infty} \frac{\phi^{n} k_{x}^{n}}{n!}=\sum_{n=0}^{\infty} \frac{\phi^{2 n}}{(2 n)!} \underbrace{k_{x}^{2 n}}_{=1}+\sum_{n=0}^{\infty} \frac{\phi^{2 n+1}}{(2 n+1)!} \underbrace{k_{x}^{2 n+1}}_{=k_{x}} \\
& =\left(\sum_{n=0}^{\infty} \frac{\phi^{2 n}}{(2 n)!}\right) I+\left(\sum_{n=0}^{\infty} \frac{\phi^{2 n+1}}{(2 n+1)!}\right) k_{x} \\ \\
& =\left(\begin{array}{cc}
\cosh (\phi) & 0 \\
0 & \cosh (\phi)
\end{array}\right)+\left(\begin{array}{cc}
0 & \sinh (\phi) \\
\sinh (\phi) & 0
\end{array}\right) \\ \\
& =\left(\begin{array}{cc}
\cosh (\phi) & \sinh (\phi) \\
\sinh (\phi) & \cosh (\phi)
\end{array}\right)
\end{aligned}
$$
即 :
$$
\Lambda_x(\phi) = \left(\begin{array}{cc}
\mathrm{ch} \phi & \mathrm{sh} \phi & &\\
\mathrm{sh} \phi & \mathrm{ch} \phi & & \\
& & 1 & \\
& & & 1
\end{array}\right)
$$
## 7.3 $O(1,3)$ 的生成元
从 $7.1$ 节已知 :
$$
\Lambda_P = diag(1,-1,-1,-1),\ \ \Lambda_T=diag(-1,1,1,1)
$$
$$
O(1,3) = \{SO(1,3)^\uparrow,\ \Lambda_P SO(1,3)^\uparrow,\ \Lambda_T SO(1,3)^\uparrow,\ \Lambda_P \Lambda_T SO(1,3)^\uparrow \}
$$
$\Lambda_P SO(1,3)^\uparrow$ 的生成元 $K_{i(P)},i=x/y/z$ 可由 $SO(1,3)^\uparrow$ 的生成元计算得到 :
$$
\Lambda_P SO(1,3)^\uparrow:\quad
K_{(P)}^{\alpha'\beta'} = (\Lambda_p)_{\ \ \alpha}^{\alpha'} K^{\alpha\beta}(\Lambda_p)_{\ \ \beta}^{\beta'} = \Lambda_pK(\Lambda_p)^T = {\color{red}-}K
$$
类似的 :
$$
\begin{array}{l} 
\Lambda_T SO(1,3)^\uparrow:\quad K_{(T)}^{\alpha'\beta'} = {\color{red}-}K
\\ 
\Lambda_P \Lambda_T SO(1,3)^\uparrow:\quad K_{(PT)}^{\alpha'\beta'} = K
\end{array}
$$
相比之下, 无论是宇称变换还是时间反演, $J_i$ 都不会改变.
## 7.4 $SO(1,3)^\uparrow$ 的 $Lie\ Algebra$
$SO(1,3)^\uparrow$ 的 $Lie$ 群元陈列如下 :
$$
J_x = \begin{pmatrix} 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0&-i \\ 0 & 0 & i & 0\end{pmatrix},\quad  
J_y = \begin{pmatrix} 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & i \\ 0 & 0 & 0& 0 \\ 0 & -i & 0 & 0\end{pmatrix},\quad
J_z = \begin{pmatrix} 0 & 0 & 0 & 0 \\ 0 & 0 & -i & 0 \\ 0 & i & 0& 0 \\ 0 & 0 & 0 & 0\end{pmatrix}
$$
$$
K_x = \begin{pmatrix} 0 & i & 0 & 0 \\ i & 0 &  0 & 0\\ 0 & 0 & 0 & 0 \\  0 & 0 & 0 & 0 \end{pmatrix}, \quad
K_y = \begin{pmatrix} 0 & 0 & i & 0 \\ 0 & 0 &  0 & 0\\ i & 0 & 0 & 0 \\  0 & 0 & 0 & 0 \end{pmatrix}, \quad
K_z = \begin{pmatrix} 0 & 0 & 0 & i \\ 0 & 0 &  0 & 0\\ 0 & 0 & 0 & 0 \\  i & 0 & 0 & 0 \end{pmatrix}
$$

注意上述六个矩阵都已乘以 $i$, $J$ 为厄密矩阵, 而 $K$ 为对称矩阵. 可以得到其 $Lie\ Algebra$ 是：
$$
[J_i,J_j]=i~\epsilon_{ijk}J_k,\quad [J_i,K_j]=i~\epsilon_{ijk}K_k, \quad [K_i,K_j]=-i~\epsilon_{ijk}J_k
$$
定义新的生成元 :
$$
N_i^\pm = \frac{1}{2} (J_i \pm \mathrm{i} K_i)
$$
带来的好处是对易运算得到封闭,  $N^+$ 和 $N^-$ 对应的正是 $SU(2)$ 的生成元:
$$
[N_i^\pm, N_j^\pm] = \mathrm{i}\epsilon_{ijk}N_k^\pm,\quad [N_i^\pm, N_j^\mp] = 0
$$
至此我们将 $SO(1,3)^\uparrow$ 拆成了两个 $SU(2)$ 的 $Lie\ Algebra$.

## 7.5 $SO(1,3)^\uparrow$ 的群表示
### 7.5.1 (1). $(0,0)$ 表示
所谓 $(0,0)$ 表示, 就是 $N^+$ 和 $N^-$ 都是 $1$ 维表示, 而这两者都是 $SU(2)$ 的生成元, 因此自然都是 $0$, 对应的 $Lie$ 群元是单位元 $e^0=1$, 作用对象是洛伦兹标量(1-分量).

### 7.5.2 (2). $\left( \frac{1}{2},0 \right)$ 表示
所谓 $\left( \frac{1}{2},0 \right)$ 表示, 就是 $N^+$ 是 $2$ 维表示, 而 $N^-$ 是 $1$ 维表示, 显然:
$$
N_i^+ = \frac{1}{2} (J_i + \mathrm{i} K_i) = \frac{\sigma_i}{2},
\quad N_i^- = \frac{1}{2} (J_i - \mathrm{i} K_i) = 0
$$
于是得到:
$$
J_i = \frac{1}{2}\sigma_i,
\quad K_i = -\frac{i}{2}\sigma_i
$$
求 $Lorentz$ 群元, 比如绕 $x$ 轴旋转 :
$$
R_x(\theta)
= e^{i \theta J_1}
= e^{i\theta  {\sigma_1}/2}
=\begin{pmatrix}
  \cos\left(\frac{\theta}{2}\right) & i \sin\left(\frac{\theta}{2}\right) \\
  i \sin\left(\frac{\theta}{2}\right) & \cos\left(\frac{\theta}{2}\right)
  \end{pmatrix}
$$
以及关于 $z$ 轴的 $boost$ :
$$
B_1(\phi) = e^{i\phi K_1} = e^{\phi \sigma_1/2}
=\begin{pmatrix}
  ch\left( \frac{\phi}{2} \right) & sh\left( \frac{\phi}{2} \right) \\
  sh\left( \frac{\phi}{2} \right) & ch\left( \frac{\phi}{2} \right)
  \end{pmatrix}
$$
### 7.5.3 (3). $\left( 0, \frac{1}{2} \right)$ 表示
类似的, 所谓 $\left(0, \frac{1}{2} \right)$ 表示, 就是 $N^+$ 是 $1$ 维表示, 而 $N^-$ 是 $2$ 维表示, 同样:
$$
N_i^+ = \frac{1}{2} (J_i + \mathrm{i} K_i) = 0 ,
\quad N_i^- = \frac{1}{2} (J_i - \mathrm{i} K_i) = \frac{\sigma_i}{2}
$$
得到:
$$
J_i = \frac{1}{2}\sigma_i,\quad K_i = \frac{i}{2}\sigma_i
$$
这里的 $K_i$ 与 $\left( \frac{1}{2},0 \right)$ 表示的结果相差一个负号, 隐含有宇称变换的意味.

### 7.5.4 (4). $Van\ der\ Waerden$ 符号
####  $Weyl$ 旋量
$\left( \frac{1}{2},0 \right)$ 表示所作用的 $2$ 分量对象称为左手旋量, $\left( 0, \frac{1}{2} \right)$ 表示所作用的 $2$ 分量对象称为右手旋量, 它们统称为 $Weyl$ 旋量 :
$$
\chi_L = \begin{pmatrix} (\chi_L)^1   \\  (\chi_L)^2\end{pmatrix}, \quad
\chi_R = \begin{pmatrix} (\chi_R)^1   \\  (\chi_R)^2\end{pmatrix}
$$
它们也可以用 $Van\ der\ Waerden$ 符号表示 :
$$
\chi_L = \chi_a, \quad
\chi_R = \chi^{\dot a}
$$
上标 $\dot a$ 上的点表示取复共轭. 用二阶 $Levi-Civita$ 符号定义旋量度规为 :
$$
\epsilon^{\alpha\beta} = \begin{pmatrix} 0 & 1 \\  -1 & 0 \end{pmatrix}
\quad\to\quad
\epsilon\epsilon = -I,\quad
\epsilon\sigma_i^*\epsilon = \sigma_i,\quad
(\epsilon^{ab})^{-1}=\epsilon_{ab} = \begin{pmatrix} 0 & -1 \\  1 & 0 \end{pmatrix}
$$
再定义一个新的旋量( 上角标 $*$ 表示复共轭 ) :
$$
\chi_L^C = \epsilon\chi_L^*
$$
在 $boost:\chi_L \to \chi_L' = e^{\vec \phi \cdot \vec \sigma/2}\chi_L$ 下, 看看这个新旋量的表现 :
$$
\begin{array}{l}
\chi_L^C \to {\chi'}_L^C
&= \epsilon(\chi_L')^* \\
&= \epsilon(e^{\vec \phi \cdot \vec \sigma/2}\chi_L)^* \\
&= \underset{e^{-\vec \phi \cdot \vec \sigma/2 }}{\underbrace{\epsilon e^{\vec \phi \cdot \vec \sigma^*/2 }(-\epsilon)} }\ 
\underset{\chi_L^C}{\underbrace{ (\epsilon)\chi_L^*} } \\
&= e^{-\vec \phi \cdot \vec \sigma/2 }\chi_L^C
\end{array}
$$
也就是说, $\chi_L^C$ 如同右手旋量一样变换, 这表明<font color="#ff0000">它是右手旋量</font>. 把其视为正常的右手旋量, 反过来定义一个<font color="#ff0000">新的左手旋量</font>为 :
$$
\chi_R^C = -\epsilon\chi_R^*
$$
显然旋量度规可以用作对 $Van\ der\ Waerden$ 符号升降指标的运算, 上述的定义的两个新的旋量就可以表示为 :
$$
\chi_L^C = \epsilon\chi_L^* \quad\to\quad \chi^{\dot a} = \epsilon^{ab}\chi_b^* = \epsilon^{ab}\chi_{\dot b} 
$$
$$
\chi_R^C = -\epsilon\chi_R^* \quad\to\quad 
\chi_b = (\epsilon^{ab})^{-1} (\chi^{\dot a})^* =\epsilon_{ab} \chi^{a}
$$
$\chi_L = \chi_a, \quad \chi_R = \chi^{\dot a}$ 的 $Lorentz$ 变换形式根据 $Weyl$ 旋量的定义是显然的, 
$$
\chi_a \to \chi_a' = \left( {e^{i\vec \theta\cdot \vec\sigma/2 + \vec \phi\cdot \vec\sigma/2}} \right)_a^b \ \chi_b
$$
$$
\chi^{\dot a} \to \chi'^{\dot a} = \left( {e^{i\vec \theta\cdot \vec\sigma/2 - \vec \phi\cdot \vec\sigma/2}} \right)_{\dot b}^{\dot a} \ \chi^{\dot b}
$$
而 $\chi_{\dot a},\ \ \chi^a$ 的 $Lorentz$ 变换形式可根据以上两式得到 :
$$
\chi_{\dot a} \to \chi_{\dot a}' = (\chi_{\dot a}' )^*
= \left[\left( {e^{i\vec \theta\cdot \vec\sigma/2 + \vec \phi\cdot \vec\sigma/2}} \right)_a^b\right]^* \ \chi_b^*
= \left( {e^{-i\vec \theta\cdot \vec\sigma^*/2 + \vec \phi\cdot \vec\sigma^*/2}} \right)_{\dot a}^{\dot b} \ \chi_{\dot b}
$$
$$
\chi^{a} \to \chi'^{a} = (\chi'^{\dot a})^*
= \left( {e^{-i\vec \theta\cdot \vec\sigma^*/2 - \vec \phi\cdot \vec\sigma^*/2}} \right)_{b}^{a} \ \chi^{b}
$$
注意到 $\sigma^\dagger_i = \sigma_i$, 则可以证明 $\chi^a\chi_a$ 是 $Lorentz$ 不变量 :
$$
(\chi^a)^T\chi_a \to 
(\chi'^a)^T\chi_a' =  (\chi^{b})^T \ 
\overset{\delta_b^c}{\overbrace{
\underset{\Large\left( {e^{-i\vec \theta\cdot \vec\sigma/2 - \vec \phi\cdot \vec\sigma/2}} \right)_{b}^{a}}{\underbrace{\left[\left( {e^{-i\vec \theta\cdot \vec\sigma^*/2 - \vec \phi\cdot \vec\sigma^*/2}} \right)_{b}^{a}\right]^T} } \ 
\left( {e^{i\vec \theta\cdot \vec\sigma/2 + \vec \phi\cdot \vec\sigma/2}} \right)_a^c 
}}\ 
\chi_c
= (\chi^c)^T \chi_c
$$
类似的, $\chi_{\dot a}$ 与 $\chi^{\dot a}$ 的结合也是 $Lorentz$ 不变量. 满足 :
$$
(\chi^a)^T\chi_a = \chi_a^T \epsilon^{ab} \chi_b
$$
也可以把 $Lorentz$ 变换的 $\left( \frac{1}{2}, 0 \right)$ 和 $\left( 0, \frac{1}{2} \right)$ 表示写作 :
$$
\Lambda_{\left( \frac{1}{2}, 0 \right)} = \Lambda_a^{\ \ b} = \left( {e^{(i\vec \theta + \vec \phi) \cdot \vec\sigma/2}} \right)_a^b\ \ ,\quad
\Lambda_{\left( 0, \frac{1}{2} \right)} = \Lambda_{\ \ \dot a}^{\dot b} = \left( {e^{(i\vec \theta - \vec \phi) \cdot \vec\sigma/2}} \right)_{b}^{a}
$$
它们分别对应于左手旋量和右手旋量的 $Lorentz$ 变换. 注意:

- 加上旋转变换后, $Lorentz$ 变换矩阵不再对称.
- 上述变换的作用量是 2-分量, 不是四维时空的 4-分量, 后者对应的 $\left( \frac{1}{2}, \frac{1}{2} \right)$ 表示可跳转至 [[#(5). $ left( frac{1}{2}, frac{1}{2} right)$ 表示与 $4-tendor$]].


#### 旋量与宇称
根据 $7.3$ 节, 在宇称变换下, $J_i\to J_i, K_i \to -K_i$, 而 :
$$
N_i^\pm = \frac{1}{2} (J_i \pm \mathrm{i} K_i)
$$
可见宇称变换下 $N_i^+ \leftrightarrow N_i^-$, 即 $\left( 0, \frac{1}{2} \right)$ 表示 $\leftrightarrow$ $\left( \frac{1}{2}, 0 \right)$ 表示, 左手旋量 $\leftrightarrow$ 右手旋量. 可见要获得一个物理体系在宇称变换下的表现, 需要同时有左手和右手旋量($Weyl$ 旋量). 定义 $\color{red}Dirac$ <font color="#ff0000">旋量</font>包含一个左手和一个右手旋量, 以及其在宇称变换下的表现 :
$$
\Psi = \begin{pmatrix} \chi_a \\  \xi^{\dot a}  \end{pmatrix}
\xleftrightarrow{\text {宇称变换 }}
\Psi^P = P\Psi = \begin{pmatrix} \xi^{\dot a} \\ \chi_a   \end{pmatrix},\ P=\begin{pmatrix} 0 & I \\  I & 0 \end{pmatrix}
$$
定义 $Majorana$ 旋量为一个左手旋量和与之对应的右手旋量的组合 :
$$
\Psi_M = \begin{pmatrix} \chi_a \\  \chi^{\dot a}  \end{pmatrix}
$$
注意这两个旋量不同于 $4-tensor$, $Dirac$ 旋量按照 $Loreatz$ 群的 $\left( \frac{1}{2}, 0 \right) \oplus \left( 0, \frac{1}{2} \right)$ 表示变换, 矩阵形式就是分块矩阵, 即 :
$$
\Psi \xrightarrow{\text { Lorentz 变换 }}
\Psi^{\prime}
=\binom{\chi'_{L}}{\xi'_{R}}
=\Lambda_{\left(\frac{1}{2}, 0\right) \oplus \left(0, \frac{1}{2}\right)} \Psi
=\left(\begin{array}{cc}
\Lambda_{\left(\frac{1}{2}, 0\right)} & 0 \\
0 & \Lambda_{\left(0, \frac{1}{2}\right)}
\end{array}\right)\binom{\chi_{L}}{\xi_{R}}
$$
####  $charge\ conjugation\ transformation$ (电荷共轭变换)
前面提到, $\chi_L^C$ 是右手旋量, $\chi_R^C$ 左手旋量, 上角标 $C$ 表示 $conjugation$ (共轭), 所以可以定义一个新的旋量 ${\Psi}^C$: 
$$
\Psi = \begin{pmatrix} \chi_L \\  \xi_R \end{pmatrix}
\xrightarrow{\text { charge\ conjugation 变换 }}
\Psi^C = \begin{pmatrix}  \xi_R^C \\ \chi_L^C  \end{pmatrix}
= \begin{pmatrix} \xi_L \\  \chi_R \end{pmatrix}
$$
$\Psi$ 和 $\Psi^C$ 是 $Dirac$ 旋量, 满足相同的 $Lorentz$ 变换关系.

### 7.5.5 (5). $\left( \frac{1}{2}, \frac{1}{2} \right)$ 表示与 $4-tendor$
所谓 $\left( \frac{1}{2}, \frac{1}{2} \right)$ 表示, 就是 $N^+$ 和 $N^-$ 都是 $2$ 维表示. 其作用的对象记作 $v_a^{\dot b}$, 每个指标在独立的 $SU(2)$ $Lie$ 代数下变换.

采用 $Van\ der\ Waerden$ 符号组成任意的<font color="#ff0000">厄密矩阵</font> $v_{a\dot b}$, 其可以在泡利矩阵和单位矩阵下展开:
$$
v_{a\dot b} \ \overset{\Delta}{=}\   \begin{pmatrix} 1 & 0 \\  0 & 1 \end{pmatrix}v_0 + \sum_{i=1}^3 v_i \sigma_i
= \begin{pmatrix} v_0+v_3 & v_1-iv_2 \\  v_1+iv_2 & v_0-v_3 \end{pmatrix}
$$
根据前面的旋量在 $Lorentz$ 变换下的表达式, 可以得到 $v_{a\dot b}$ 在 $Lorentz$ 变换下的形式:
$$
\begin{array}{rl}
v \to v^{\prime}=v_{a \dot{b}}^{\prime} & =\left(\mathrm{e}^{i \vec{\theta} \frac{\vec{\sigma}}{2}+\vec{\phi} \frac{\vec{\sigma}}{2}}\right)_{a}^{c} v_{c \dot{d}}\left(\left(\mathrm{e}^{-i \vec{\theta} \frac{\vec{\sigma}^{*}}{2}+\vec{\phi} \frac{\vec{\sigma}^{*}}{2}}\right)_{\dot{b}}^{\dot{d}}\right)^{T} \\
& =\left(\mathrm{e}^{i \vec{\theta} \frac{\vec{\sigma}}{2}+\vec{\phi} \frac{\vec{\sigma}}{2}}\right)_{a}^{c} v_{c \dot{d}}\left(\mathrm{e}^{-i \vec{\theta} \frac{\vec{\sigma}^{\dagger}}{2}+\vec{\phi} \frac{\vec{\sigma}^{\dagger}}{2}}\right)_{\dot{b}}^{\dot{d}} \\
{\sigma^{\dagger}=\sigma} \to &=\left(\mathrm{e}^{i \vec{\theta} \frac{\vec{\sigma}}{2}+\vec{\phi} \vec{\sigma}}\right)_{a}^{c} v_{c \dot{d}}\left(\mathrm{e}^{-i \vec{\theta} \vec{\sigma}+\vec{\phi} \vec{\sigma} \frac{\dot{\sigma}}{2}}\right)_{\dot{b}}^{\dot{d}}
\end{array}
$$
一个性质是, 厄密矩阵在 $Lorentz$ 变换后仍是厄米的, 反厄米也是如此, 即两者组成的集合都是不变子空间. 现在证明前者:
$$
\begin{array}{rl}
\left(\left(\mathrm{e}^{i \vec{\theta} \frac{\vec{\sigma}}{2}+\vec{\phi} \frac{\vec{\sigma}}{2}}\right)_{a}^{c} v_{c \dot{d}}\left(\mathrm{e}^{-i \vec{\theta} \frac{\vec{\sigma}}{2}+\vec{\phi} \frac{\vec{\sigma}}{2}}\right)_{\dot{b}}^{\dot{d}}\right)^{\dagger} 
&=\quad\left(\left(\mathrm{e}^{-i \vec{\theta} \frac{\vec{\sigma}}{2}+\vec{\phi} \frac{\vec{\sigma}}{2}}\right)_{\dot{b}}^{\dot{d}}\right)^{\dagger} v_{c \dot{d}}^{\dagger}\left(\left(\mathrm{e}^{i \vec{\theta} \frac{\vec{\sigma}}{2}+\vec{\phi} \frac{\vec{\sigma}}{2}}\right)_{a}^{c}\right)^{\dagger} \\
&=\quad\left(\mathrm{e}^{i \vec{\theta} \frac{\vec{\sigma}^{\dagger}}{2}+\vec{\phi} \frac{\vec{\sigma}^{\dagger}}{2}}\right)_{\dot{b}}^{\dot{d}} v^{\dagger} \dot{d}\left(\mathrm{e}^{-i \vec{\theta} \frac{\vec{\sigma}^{\dagger}}{2}+\vec{\phi}^{\vec{\sigma}^{\dagger}}}\right)_{a}^{c} \\
v_{c \dot{d}}^{\dagger}=v_{c \dot{d}} \to
&=\quad \left(\mathrm{e}^{i \vec{\theta} \frac{\vec{\sigma}}{2}+\vec{\phi} \frac{\vec{\sigma}}{2}}\right)_{\dot{b}}^{\dot{d}} v_{c \dot{d}}\left(\mathrm{e}^{-i \vec{\theta} \frac{\vec{\sigma}}{2}+\vec{\phi} \frac{\vec{\sigma}}{2}}\right)_{a}^{c}
\end{array}
$$
反厄米($v^\dagger=-v$)是类似的, 只是上面证明中多一个负号. 另外, $\left( \frac{1}{2}, \frac{1}{2} \right)$ 表示的作用对象正是 $4-tendor$ :
$$
v_{a\dot b} \ \overset{\Delta}{=}
\begin{pmatrix} v_0+v_3 & v_1-iv_2 \\  v_1+iv_2 & v_0-v_3 \end{pmatrix}
\overset{\Delta}{=}
(v_0, \vec v)^T
= (v_0, v_1, v_2, v_3)^T
$$
证明思路如下: 由上面得到的 $v_{a\dot b}$ 在 $Lorentz$ 变换下的形式, 取 **boost** 为 $x,y,z$ 方向, 可以验证, 结果与 $4-tendor$ 的 $Lorentz$ 变换形式一致.

# 8 $Poincaré \ Group$ (庞加莱群)
## 8.1 无限小平移变换
考虑一个简单的平移变换 :
$$
\Phi(\vec x)
\to
\Phi(\vec x + \vec \epsilon) = \Phi(\vec x) + \epsilon\vec \nabla\Phi(\vec x)
$$
其生成元就是动量算符, 加上虚数单位保证它是厄米的:
$$
P_i = (-\mathbf{i}\vec \nabla)_i = -\mathbf{i}\frac{ \partial  }{ \partial x_i }
$$
于是无限小平移变换写作:
$$
\Phi(\vec x)
\to
\Phi(\vec x + \vec \epsilon) = \Phi(\vec x) + i\epsilon P\Phi(\vec x)
$$
任意大小的平移就可以表示为 $Lie$ 群作用于函数空间 $\Phi(\vec x)$:
$$
\Phi(\vec x)
\to
\Phi(\vec x + \vec a) = e^{\mathbf{i}a^iP_i}\Phi(\vec x) = e^{a^i\partial_i} \Phi(\vec x)
$$
## 8.2 庞加莱群

洛伦兹群加上平移变换后, 就变成了的庞加莱群, 即: 
$$
Poincaré \ Group = Lorentz\ Group \ +\  Translation(平移) = rotation\ +\ boost\ +\ translation
$$
即对四维坐标 $x^\mu$ 的庞加莱变换可以写作 :
$$
x^\mu \to x'^\nu = 
\begin{pmatrix} \Lambda_{\ \ \mu}^\nu & a^\mu \\  0 & 1 \end{pmatrix}
\begin{pmatrix} x^\mu \\  1 \end{pmatrix}
\quad or \quad
x'^\nu = \Lambda_{\ \mu}^\nu x^\mu + a^\mu
$$
矩阵补上第二行只是为了保证变换矩阵是个方阵.

用 $J_{i}, K_{i}, P_{\mu}$ 表示的 $Lie$ 代数为 :
$$
\begin{aligned}
{\left[J_{i}, J_{j}\right] } & =i \epsilon_{i j k} J_{k} \\
{\left[J_{i}, K_{j}\right] } & =i \epsilon_{i j k} K_{k} \\
{\left[K_{i}, K_{j}\right] } & =-i \epsilon_{i j k} J_{k} \\
{\left[J_{i}, P_{j}\right] } & =i \epsilon_{i j k} P_{k} \\
{\left[J_{i}, P_{0}\right] } & =0 \\
{\left[K_{i}, P_{j}\right] } & =i \delta_{i j} P_{0} \\
{\left[K_{i}, P_{0}\right] } & =-i P_{i}
\end{aligned}
$$
定义 Poincaré 群 $M_{\mu \nu}$ 为 :
$$
\left\{\begin{array}l
J_{i}  =\frac{1}{2} \epsilon_{i j k} M_{j k} \\
K_{i}  =M_{0 i}
\end{array}\right.
\quad {\color{gray}or} \quad
M_{\mu \nu} = 
\begin{bmatrix} 
0 & K_1 & K_2 & K_3 \\
-K_1 & 0 &  J_3 & -J_2 \\
K_2 & -J_3 & 0 & J_1 \\
K_3 & J_2 & -J_1 & 0
\end{bmatrix}_{(4\times 4)\times (4\times 4)}
$$
于是用 $M_{\mu \nu}$ 表示的 $Poincaré\ Lie$ 代数关系为：
$$
\begin{aligned}
{\left[P_{\mu}, P_{\nu}\right] } & =0 \\
{\left[M_{\mu \nu}, P_{\rho}\right] } & =i\left(\eta_{\mu \rho} P_{\nu}-\eta_{\nu \rho} P_{\mu}\right)
\end{aligned}
$$
由定义式可得
$$
\left[M_{\mu \nu}, M_{\rho \sigma}\right]=i\left(\eta_{\mu \rho} M_{\nu \sigma}-\eta_{\mu \sigma} M_{\nu \rho}-\eta_{\nu \rho} M_{\mu \sigma}+\eta_{\nu \sigma} M_{\mu \rho}\right)
$$
如果在位置表象下写庞加莱群, 它是:  
$$
M_{\mu\nu}^{\infty} = \boldsymbol{i} (x_\mu \partial_\nu - x_\nu \partial_\mu)
$$
这也被称为 $Poincaré$ 群的无穷维表示, 和三维角动量算符 $\vec x\times\vec p$ 类似, 可以把它理解为四维的角动量算符.

$Poincaré$ 群有两个 $Casimir$ 算符, 第一个是：
$$
P_{\mu} P^{\mu}= m^{2}
$$

这个标量值记作 $m^{2}$, 它就是粒子质量.

第二个 $Casimir$ 算符为 $W_{\mu} W^{\mu}$ , 其中 $W^\mu$ 称为 $Pauli-Lubanski$ 四维向量 :
$$
W^{\mu}=\frac{1}{2} \epsilon^{\mu \nu \rho \sigma} P_{\nu} M_{\rho \sigma}
$$
它对应的标量值是自旋, 记作 $j = j_1+j_2$, 例如对于洛伦兹群, 其两个 $SU(2)\ Lie$ 代数对应 $j_1$ 和 $j_2$. 即庞加莱群用两个标量予以标记: $m$ (质量, 可取任意值), $j$ (自旋, 取整数或者半整数).
# 9 基本粒子
<font color="#ff0000">庞加莱群是描述所有基本粒子的数学工具.</font>

