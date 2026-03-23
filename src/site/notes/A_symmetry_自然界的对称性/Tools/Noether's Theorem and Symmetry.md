---
{"dg-publish":true,"permalink":"/A_symmetry_自然界的对称性/Tools/Noether's Theorem and Symmetry/","noteIcon":"default","created":"2025-10-23T14:36:45.381+08:00","updated":"2025-10-25T23:16:57.364+08:00"}
---


- refer to *Physics from Symmetry* by Jakob Schwichtenberg.

```table-of-contents
title: 
style: nestedList # TOC style (nestedList|nestedOrderedList|inlineFirstLevel)
minLevel: 0 # Include headings from the specified level
maxLevel: 0 # Include headings up to the specified level
includeLinks: true # Make headings clickable
hideWhenEmpty: false # Hide TOC if no headings are found
debugInConsole: false # Print debug info in Obsidian console
```
# 1 Halmilton 最小作用量原理
拉格朗日密度函数 $\mathcal{L}=L/V$ 是一个洛伦兹标量, 具有洛伦兹协变性, 即在所有惯性参考系中具有相同的形式. 作用量 $S$ 是一个泛函, 具有洛伦兹不变性, 即其极小值对应的路径 $q(t)$ 在所有惯性参考系中不变. 两者的关系如下:
$$
S[q(t)] = \int \mathcal{L}\left( q(t), \dot q(t), t \right) \,dt
$$
## 1.1 Fermat 原理
关于最小作用量的一个简单的例子就是 $fermat$ 原理, 即光沿着光程取极值的路径(测地线)传播:
$$
\min\ S 
= \min\ \int n\,ds 
= \min\ \int \frac{c}{v} \frac{ds}{dt} \,dt
=\min\  \int c\, dt
\ \ \propto\  \min\int dt
$$

# 2 Euler-Lagrange 方程
对于位形空间中固定的两个端点, $Euler-Lagrange$ 方程可以找到一条路径 $q(t)$, 使得作用量取得极值(极大 $or$ 极小), 推导步骤如下:

已知:
$$
S = \int_{t_1}^{t_2} \mathcal{L}\left( q, \dot q, t \right) \,dt
$$
对泛函进行微扰 $q(t) \to q(t) +\delta q(t)$ :
$$
S' = \int_{t_1}^{t_2} \mathcal{L}\left( q+\delta q,\ \dot q+\delta \dot q,\ t \right) \,dt 
= \int_{t_1}^{t_2} \left[ \frac{ \partial \mathcal{L} }{ \partial q }\delta q + \frac{ \partial \mathcal{L} }{ \partial \dot q }\delta \dot q \right] \,dt
$$
由于端点固定($\delta q(t_1)=\delta q(t_2)=0$)和变分原理 $\delta \dot q=\frac{ d }{ d t} \delta q$, 保留线性项:
$$
\begin{array}l
\delta S
&=\int_{t_1}^{t_2} \left[ \frac{ \partial \mathcal{L} }{ \partial q }\delta q + \frac{ \partial \mathcal{L} }{ \partial \dot q }\delta \dot q \right] \,dt
\\&=\int_{t_1}^{t_2} \left[\frac{ \partial \mathcal{L} }{ \partial q }\delta q \,dt + \frac{ \partial \mathcal{L} }{ \partial \dot q }d \delta q \right]
\\&=\int_{t_1}^{t_2} \frac{ \partial \mathcal{L} }{ \partial q }\delta q \,dt +
\left.\frac{ \partial \mathcal{L} }{ \partial \dot q }\delta q \right|_{t_1}^{t_2} - \int_{t_1}^{t_2} d\left( \frac{ \partial \mathcal{L} }{ \partial \dot q } \right) \delta q
\\&= \int_{t_1}^{t_2} \left[\frac{ \partial \mathcal{L} }{\partial q} -
 \frac{d}{dt}\left( \frac{ \partial \mathcal{L} }{ \partial \dot q } \right) \right]\delta q\, dt
 \\& = 0
 \end{array}
$$
根据端点选取的任意性, 得到粒子(质点)的 $Euler-Lagrange$ 方程:
$$
\frac{ \partial \mathcal{L} }{\partial q} -
 \frac{d}{dt}\left( \frac{ \partial \mathcal{L} }{ \partial \dot q } \right) =0
$$
如果广义坐标为多个, 记为 $q_\alpha$, 得到方程组:
$$
\frac{ \partial \mathcal{L} }{\partial q_\alpha} -
 \frac{d}{dt}\left( \frac{ \partial \mathcal{L} }{ \partial \dot q_\alpha } \right) =0
$$
如果处理对象不是质点, 而是标量场 $\Phi(x^\mu)$, 对应拉氏函数 $\mathcal{L}(\Phi, \partial_\mu \Phi, x^\mu)$, 类似地:
$$
\frac{ \partial  }{ \partial x^\mu }\frac{ \partial \mathcal{L} }{ \partial (\partial_\mu \Phi) } - \frac{ \partial \mathcal{L} }{ \partial \Phi } = 0
$$
如果对象是四维矢量场 $A^\nu(x^\mu)$, 对应拉氏函数 $\mathcal{L}(A^\nu, \partial_\mu A^\nu, x^\mu)$, 只需将上式的 $\Phi$ 替换为 $A^\nu$:
$$
\frac{ \partial  }{ \partial x^\mu }\frac{ \partial \mathcal{L} }{ \partial (\partial_\mu A^\nu) } - \frac{ \partial \mathcal{L} }{ \partial A^\nu } = 0
$$
# 3 Nother 定理
诺特定理描述了系统在某种变换下的对称性, 即在这些变换下作用量的变分(或者说作用量的极值与其对应的系统演化路径)保持不变时, 可以找到一些守恒量.
## 3.1 自由粒子
### 3.1.1 守恒量的一般形式
拉格朗日量的非唯一性告诉我们, 如果拉氏量加上一个函数 $G(q,t)$ 对于时间的全导数 $\mathcal{L}\to\mathcal{L}+ \frac{dG}{dt}$ (此变化记作 $\Delta$), 将使得作用量不变:
$$
\Delta S = \int dt\, \Delta\mathcal{L} = \left.G(q(t),t)\right|_{t_1}^{t_2} = const.
$$
即变换前后, 作用量 $S$ 只相差一个常数项, 那么变分 $\delta S = \delta (S+\Delta S)$, 将得到相同的运动方程(欧拉-拉格朗日方程). 因此, 对于无限小变换 $q(t) \to q(t) +\delta q(t)$, 仍有 $\delta q(t_1)=\delta q(t_2)=0$ 和 $\delta \dot q=\frac{ d }{ d t} \delta q$。但是注意，
$$
\delta \mathcal{L} = \Delta \mathcal{L} = \frac{dG}{dt}
$$
即:
$$
\begin{array}l
\frac{ d G }{ d t}
&= \frac{ \partial \mathcal{L} }{ \partial q }\delta q + \frac{ \partial \mathcal{L} }{ \partial \dot q }\delta \dot q + \frac{ \partial \mathcal{L} }{ \partial t } \delta t
\\&= \frac{ d  }{ d t}\left( \frac{ \partial \mathcal{L} }{ \partial \dot q } \right) \delta q + \frac{ \partial \mathcal{L} }{ \partial \dot q }\delta \dot q  + \frac{ \partial \mathcal{L} }{ \partial t } \delta t
\\&= \frac{ d  }{ d t}\left( \frac{ \partial \mathcal{L} }{ \partial \dot q }  \delta q 
+ \int^t \frac{ \partial \mathcal{L} }{ \partial t } \delta t ~dt
\right)
\end{array}
$$
就能得到一个守恒量:
$$
J = \frac{ \partial \mathcal{L} }{ \partial \dot q }  \delta q - G + \int^t \frac{ \partial \mathcal{L} }{ \partial t } \delta t ~dt
$$
### 3.1.2 时空平移
#### 时间对称性 $\to$ 能量守恒
对于无限小时间平移 $t\to t+\epsilon$ 不变性, 对应于 $q(t) \to q(t+\epsilon)=q(t)+\dot q(t)\epsilon$,
$$
\delta \mathcal{L}(q(t),\ \dot q(t),\ t) 
= \left(
\frac{ \partial \mathcal{L} }{ \partial q }{\frac{ d q }{ d t}} 
+ \frac{ \partial \mathcal{L} }{ \partial \dot q }{\frac{ d \dot q }{ d t}}
+ \frac{ \partial \mathcal{L} }{ \partial t }
\right) \delta t
= \frac{ d \mathcal{L} }{ d t} \delta t
\\
= \frac{ \mathrm{d} \mathcal{L}\epsilon }{ \mathrm{d} x}
= \frac{ d G }{ d t}
$$
故可取 $G = \mathcal{\epsilon L}$，进一步地，若 $\mathcal{L}$ 不显含 $t$, 就得到哈密顿量 $\mathcal{H}$ 是守恒量:
$$
\frac{ \partial \mathcal{L} }{ \partial \dot q }  \delta q - \epsilon \mathcal L =const.
\quad\to\quad
\mathcal{H} \equiv \frac{ \partial \mathcal{L} }{ \partial \dot q }  \dot q - \mathcal L =const.
$$
而且从 $\mathcal{L}$ 到 $\mathcal{H}$ 的变换就是勒让德变换.

注意, 在理论力学中我们知道:
$$
\frac{ d \mathcal{H} }{ d t}
\overset{poisson括号}{=} \frac{ \partial \mathcal{H} }{ \partial t } = -\frac{ \partial \mathcal{L} }{ \partial t }
$$
所以 "$\mathcal{H}$ 是守恒量" 与 "$\mathcal{H}$ 不显含 $t$", "$\mathcal{L}$ 不显含 $t$" 等价, 这与上述是一致的.

#### 空间对称性 $\to$ 动量守恒
对于无限小空间平移 $q_{\alpha}(t) \rightarrow q_{\alpha}(t)+\epsilon_{\alpha}$ 不变性, 取 $G=0$ ，于是得到广义动量 $p_\alpha$ 是守恒量:
$$
 \frac{\partial \mathcal{L}}{\partial \dot{q}_{\alpha}} \delta q_{\alpha} = const.
\quad\to\quad
p_\alpha \equiv  \frac{\partial \mathcal{L}}{\partial \dot{q}_{\alpha}} = const.
$$
当然, $\delta t=0$, 所以不必理睬 $\int^t \frac{ \partial \mathcal{L} }{ \partial t } \delta t ~dt$, 该项自动为 $0$.
### 3.1.3 旋转和 boost
#### 旋转对称性 $\to$ 角动量守恒
已知 $SO(3)$ 的生成元可以写作 $(J_i)_{jk} = -\epsilon_{ijk}$ , 于是欧氏空间无限小旋转可表述为 $q_i \to e^{\vec \theta \cdot \mathbf{J}_i}\cdot \vec q = \left[\ I+\theta_j (J_i)_{jk} \ \right]q_k = q_i - \epsilon_{ijk}\theta_j q_k =  q_i + \epsilon_{ijk}\theta_k q_j$, 取 $G=0$ ，可得到角动量 $J_{rot}$ 是守恒量:
$$
\frac{ \partial \mathcal{L} }{ \partial \dot q_i }\epsilon_{ijk}\theta_k q_j =\theta_k \epsilon_{ijk} q_j p_i = \vec \theta \cdot (\vec p \times \vec q) = const.
\quad\to\quad
J_{rot} = \vec q \times \vec p
$$
#### 推动对称性 $\to$ 质心运动定理
无限小 $boost$ 时, 洛伦兹变换退化为伽利略变换, 举个例子: 考虑 $x$ 方向的 $boost$,
$$
\begin{array}l
x = e^{\vec \phi \cdot \mathbf{K}}\cdot \vec x 
&= x + 
\begin{bmatrix} 0 & \phi & 0 & 0 \end{bmatrix}
\begin{bmatrix} 0 & 1 & 0 & 0 \\ 1 & 0 &  0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0  \end{bmatrix} 
\begin{bmatrix} t \\ x \\ 0 \\ 0  \end{bmatrix}
\\&= x + \phi t 
\approx x + \tanh \phi \cdot t
\\&= x + \beta t \ \ \left(\beta=\frac{v}{c} \right)
\end{array}
$$
或者也可以直接对洛伦兹变换的双曲旋转形式做一阶近似:
$$
\begin{bmatrix} ch\phi & sh\phi \\  sh\phi & ch\phi \end{bmatrix}
\approx
\begin{bmatrix} 1 & \phi \\  \phi & 1 \end{bmatrix}
\approx
\begin{bmatrix} 1 & v \\  v & 1 \end{bmatrix}
$$
或者也可以类似旋转对称性的讨论, 利用洛伦兹群对应的生成元 $K$, 可写作 $q_i \to q_i + \phi_j (K_i)_{jk} q_k$, 都将得到一致的结论: $q_\alpha \to q_\alpha + v_\alpha t$, 以及 $\dot q_\alpha \to \dot q_\alpha + v_\alpha$ 注意 $v_\alpha$ 是一个常值小量而不是变量 $\dot q_\alpha$. 考虑一维情形 $q \to q + v t$ 以及一个简单的多自由粒子的拉氏量:
$$
\mathcal{L} = \frac{1}{2} \sum_i m_i \dot q_i^2
$$
于是
$$
\delta \mathcal{L}(q(t),\ \dot q(t),\ t) 
= 
\frac{ \partial \mathcal{L} }{ \partial q } vt 
+ \frac{ \partial \mathcal{L} }{ \partial \dot q } v
= \sum_i m_i \dot q_i v
= \frac{ d G }{ d t}
$$
所以可以取 $G = \sum_i m_i q_i v$, 得到:
$$
\sum_i \frac{ \partial \mathcal{L} }{ \partial \dot q_i }  \delta q_i - \sum_i m_i q_i v
\equiv 
\sum_i \left( p_i vt - m_iq_i v \right) = const.
\quad\to\quad
q_c = \frac{{\sum_i m_iq_i}}{\sum_i m_i}= \frac{{\sum_i m_i \dot q_i t}}{\sum_i m_i}
$$
即初始时刻质心位于原点的质心运动方程.
## 3.2 自由场
### 3.2.1 场的内禀对称性
考虑矢量场 $A^\mu(x^\nu)$, 拉氏函数的形式为 $\mathcal{L}(A^\mu, \partial_\nu A^\mu)$ (不显含四维坐标是因为只考虑场的内禀对称性, 此时坐标变分 $\delta x^\mu=0$). 在场本身的无穷小变换 $A^\mu \to A'^\mu = A^\mu + \delta A^\mu$, 拉氏函数的不变性可以表述为:
$$
\begin{array}{l}
0 
= \delta \mathcal{L} 
&= \frac{ \partial \mathcal{L} }{ \partial A^\mu } \delta A^\mu + 
\frac{ \partial \mathcal{L} }{ \partial (\partial_\nu A^\mu) } \delta (\partial_\nu A^\mu)
\\&= \partial_\nu \left(\frac{ \partial \mathcal{L} }{ \partial (\partial_\nu A^\mu) }\right) \delta A^\mu +
\frac{ \partial \mathcal{L} }{ \partial (\partial_\nu A^\mu) }  \partial_\nu \delta A^\mu
\\&= \partial_\nu \left( \frac{ \partial \mathcal{L} }{ \partial (\partial_\nu A^\mu) }  \delta A^\mu \right)
\end{array}
$$
定义 $Nother$ 流 $J^\nu = \frac{ \partial \mathcal{L} }{ \partial (\partial_\nu A^\mu) }  \delta A^\mu$, 于是上式可以写作连续性方程:
$$
\partial_\nu J^\nu = 0
$$
记 $J^\nu=(J^0, \vec J \ )$, 于是
$$
\begin{array}c
\partial_t J^0 = -\nabla \cdot \vec J
\\ \downarrow \\
\partial_t \int J^0 ~d^3 x = - \int \nabla \cdot \vec J ~d^3 x = -\int \vec J \cdot d\vec S
\end{array}
$$
对全空间积分, 考虑到场不存在于无穷远处, 即无穷远处流的通量为 $0$, 将得到守恒量:
$$
\int J^0 ~d^3x = \int \frac{ \partial \mathcal{L} }{ \partial (\partial_t A^\mu) }  \delta A^\mu ~d^3x = const.
$$
如果场在自身的平移下保持不变(此时 $\delta A^\mu$ 退化为任意常数), 于是有正则动量(广义动量 $\Pi^\sigma = \int \frac{ \partial \mathcal{L} }{ \partial (\partial_\sigma \Phi) } ~d^3x$)的时间分量守恒:
$$
\Pi^t_\mu = \int \frac{ \partial \mathcal{L} }{ \partial (\partial_t A^\mu) } ~d^3x
$$
### 3.2.2 时空平移
#### 能动张量
考虑标量场 $\Phi(x^\mu)$, 拉氏函数的形式为 $\mathcal{L}(\Phi, \partial_\mu \Phi, x^\mu)$, 其中总变分 $\delta \Phi$ 由两部分组成：坐标变换引起的 $Lie$ 导数项和场的内禀变分 $\Psi$。其一般形式为：
$$
\delta \Phi = \Psi - \delta x^\mu~ \partial_\mu \Phi
$$
对于纯坐标变换, 内禀变分 $\Psi = 0$, 此时 $\delta \Phi = - \delta x^\mu~ \partial_\mu \Phi$; 对于纯内部对称性(如 $U(1)$ 规范变换), 坐标变换生成元 $\delta x^\mu = 0$ , 此时 $\delta \Phi = \Psi$. 负号来源于场移动方向与坐标变换 $\delta x^\mu$ 方向相反.

内禀分量 $\Psi$ 的具体形式取决于场 $\Phi$ 所服从的内部对称性群及其表示. 例如, 对于非阿贝尔规范对称性 $SU(N)$, 则 $\Psi$ 由群的生成元作用在场 $\Phi$ 上,
$$
\Psi^\alpha = T^\alpha \Phi
$$
其中, $T^\alpha$ 是规范群的生成元矩阵( 如 $SU(2)$ 的泡利矩阵 $\sigma^\alpha/2$ ). 此时场的变分为,
$$
\delta \Phi = \epsilon^a \cdot \Psi^a = \epsilon^a T^a \Phi
$$
或者用庞加莱群表示为,
$$
\delta \Phi = \epsilon^{\mu\nu} M_{\mu\nu} \Phi
$$
对应于规范变换 $\Phi \to e^{  \frac{\epsilon^{\mu\nu}}{2} M_{\mu\nu}}\Phi$. $\epsilon$ 为变换参数, 如旋转角度. 因此, 在时空平移 $x^\mu \to x'^\mu = x^\mu + \delta x^\mu$ 下(纯坐标变换), 标量场 $\Phi$ 的变换 $\delta \Phi$ 简化为,
$$
\delta \Phi = -\partial_\mu \Phi ~ \delta x^\mu
$$
注意, $\delta x^\mu$ 为常量, 于是拉氏函数的不变性可以表述为,
$$
\begin{array}{l}
0 
= \delta \mathcal{L} 
&= \frac{ \partial \mathcal{L} }{ \partial \Phi } \delta \Phi + 
\frac{ \partial \mathcal{L} }{ \partial (\partial_\nu \Phi) } \delta (\partial_\nu \Phi) + \partial_\mu \mathcal{L} ~\delta x^\mu
\\&= \partial_\nu \left(\frac{ \partial \mathcal{L} }{ \partial (\partial_\nu \Phi) }\delta\Phi \right) + \partial_\mu \mathcal{L} ~\delta x^\mu
\\&= - \left[ \partial_\nu \left(\frac{ \partial \mathcal{L} }{ \partial (\partial_\nu \Phi) } \partial_\mu{\Phi} ~\delta x^\mu \right) - \partial_\mu \mathcal{L} ~\delta x^\mu \right]
\\&= - \partial_\nu \left(  \frac{ \partial \mathcal{L} }{ \partial (\partial_\nu \Phi) } \partial_\mu{\Phi}  - \delta_\mu^\nu \mathcal{L}  \right) ~\delta x^\mu
\end{array}
$$
定义能动张量(混合指标形式) $T_\mu^\nu := \frac{ \partial \mathcal{L} }{ \partial (\partial_\nu \Phi) } \partial_\mu{\Phi}  - \delta_\mu^\nu \mathcal{L}$, 于是,
$$
\color {red} {\partial_\nu T_\mu^\nu = \partial_t T^0_\mu + \partial_i T^i_\mu = 0}
$$
通过利用度规升降指标, 以及 $\frac{\partial \mathcal{L}}{\partial (\partial^\mu \Phi)} = \frac{\partial \mathcal{L}}{\partial (\partial_\alpha \Phi)} \frac{\partial (\partial_\alpha \Phi)}{\partial (\partial^\mu \Phi)} = \frac{\partial \mathcal{L}}{\partial (\partial_\alpha \Phi)} g_{\alpha\mu}$, 容易得到逆变形式 $T^{\mu\nu} = \frac{\partial \mathcal{L}}{\partial (\partial_\mu \Phi)} \partial^\nu \Phi - g^{\mu\nu} \mathcal{L}$. 上式在无穷远处场为 $0$, 所以在全空间中积分可得到 $4$ 个守恒量:
$$
\begin{array}{c}
E = \int d^3x ~ T_0^0
\\ 
P_i = \int d^3x ~ T_i^0 
\end{array}
$$
### 3.2.3 旋转和 boost
#### 诺特流
在旋转和推动变换下, $x^\mu \to x'^\mu = x^\mu + \delta x^\mu$ 且 $\delta x^\mu = M^{\mu\sigma} x_\sigma$ 是常值, 参见上一节, 有:
$$
\begin{array}{cl}
0 
= \quad\delta \mathcal{L} 
&= - \partial_\nu \left(  \frac{ \partial \mathcal{L} }{ \partial (\partial_\nu \Phi) } \partial_\mu{\Phi}  - \delta_\mu^\nu \mathcal{L}  \right) ~\delta x^\mu
\\&= - \partial_\nu \left(  \frac{ \partial \mathcal{L} }{ \partial (\partial_\nu \Phi) } \partial_\mu{\Phi}  - \delta_\mu^\nu \mathcal{L}  \right) M^{\mu\sigma} x_\sigma
\\&= - \partial_\nu T_\mu^\nu ~ M^{\mu\sigma} x_\sigma
\\&= - \partial_\nu T^{\mu\nu} ~ M_{\mu\sigma} x^\sigma
\\ {\small\color{gray}{M_{\mu\sigma} = -M_{\sigma\mu}}} \to
&= -\frac{1}{2} \left( \partial_\nu T^{\mu\nu} ~ M_{\mu\sigma} x^\sigma - \partial_\nu T^{\sigma\nu} ~ M_{\mu\sigma} x^\mu \right)
\\&= -\frac{1}{2} \partial_\nu \left( T^{\mu\nu}  x^\sigma - T^{\sigma\nu} x^\mu \right) M_{\mu\sigma}
\end{array}
$$
定义 $Nother$ 流 $(J^\nu)^{\mu\sigma} = T^{\mu\nu}  x^\sigma - T^{\sigma\nu} x^\mu$, 上式可改写为,
$$
\partial_\nu (J^\nu)^{\mu\sigma} = 0
$$
或者
$$
\begin{array}{l} 
0 &=
\partial_\nu (T^{\mu\nu}  x^\sigma - T^{\sigma\nu} x^\mu)
\\
&= T^{\mu\sigma} + x^\sigma\partial_\nu T^{\mu\nu} - T^{\sigma\nu} - x^\mu \partial_\nu T^{\sigma\nu}
\\ 
&= T^{\mu\sigma} - T^{\sigma\nu}
\end{array}
$$
这意味着诺特流的四维散度为零, 等同于<font color="#ff0000">能动张量对称</font>.
#### 旋转对称性 $\to$ 场的角动量守恒
##### 轨道角动量
与时空平移不同, 对于 $\delta \Phi = \Psi - \delta x^\mu~ \partial_\mu \Phi$, 旋转将可能导致内禀变分 $\Psi$ 不为零(称为自旋).

暂时不考虑内禀对称性. 类似地, 在无穷远处场为 $0$, 所以对诺特流在全空间中积分得到:
$$
Q^{\mu\sigma} 
= \int d^3x~ (J^0)^{\mu \sigma} 
= \int d^3x~ \left(T^{\mu 0}  x^\sigma - T^{\sigma 0} x^\mu\right)
$$
是守恒量. 对于转动不变性, 可选取指标 $i,j \in \{1,2,3\}$ 的部分(对应于庞加莱代数的旋转生成元 $M_{ij}$ ), 已知旋转生成元 $J_i= \frac{1}{2}\epsilon_{ijk}M_{jk}$, 相应的有场的轨道角动量 $\vec L_{orbit}$ 是守恒量:
$$
L_{orbit}^i 
= \frac{1}{2}\epsilon_{ijk} Q^{jk} 
= \frac{1}{2}\epsilon_{ijk} \int d^3x~ \left(T^{j 0}  x^k - T^{k 0} x^j \right)
=  \int  \epsilon_{ijk} T^{j0}  x^k ~d^3x
= \int d^3x~ (\vec x \times \vec p)^i
$$
在这里，如果加入带电粒子，就会有 $T^{\mu \nu} = T^{\mu \nu}_{field} + T^{\mu \nu}_{particles}$，其中  
$$
T^{\mu\nu}_{field} = \frac{\partial \mathcal{L}}{\partial (\partial_\mu \Phi)} \partial^\nu \Phi - g^{\mu\nu} \mathcal{L}
$$
是前面证明过的，而  
$$
T_{\text{particle}}^{\mu\nu} = \rho U^\mu U^\nu =  m \int d\tau~ \frac{dx^\mu}{d\tau} \frac{dx^\nu}{d\tau} \delta^{4}(x - x(\tau))
$$
现在，我们将这个连续的 $T_{\text{particle}}^{\mu\nu}$ 代入场论守恒荷公式 $Q^{\mu\sigma}$ 中：
$$
\begin{aligned} 
Q^{\mu\sigma}_{\text{particle}} &= \int d^3x~ \left(T_{\text{particle}}^{\mu 0} x^\sigma - T_{\text{particle}}^{\sigma 0} x^\mu\right)\\
&= \int d^3x~ \left[ \left( m \int d\tau~ \dot{x}^\mu \dot{x}^0 \delta^{4}(x - x(\tau)) \right) x^\sigma - \left( m \int d\tau~ \dot{x}^\sigma \dot{x}^0 \delta^{4}(x - x(\tau)) \right) x^\mu \right]
\end{aligned}
$$
由于积分变量 $\dot{ x}\left( =\frac{ \mathrm{d} x }{ \mathrm{d} \tau} \right)$， $x$ 和 $\tau$ 是独立的，我们可以交换积分顺序：
$$
Q^{\mu\sigma}_{\text{particle}} = m \int d\tau~ \dot{x}^0 \left[ \dot{x}^\mu \left(\int d^3x~ x^\sigma \delta^{3}(\mathbf{x} - \mathbf{x}(\tau))\right) - \dot{x}^\sigma \left(\int d^3x~ x^\mu \delta^{3}(\mathbf{x} - \mathbf{x}(\tau))\right) \right]
$$
得到
$$
Q^{\mu\sigma}_{\text{particle}} = m \left[ \dot{x}^\mu x^\sigma - \dot{x}^\sigma x^\mu \right]
$$
这个结果正是自由粒子在粒子理论中的轨道角动量部分。当然，我们一般考虑在电磁场中运动的带电粒子，这样 $T_{\text{particle}}^{\mu\nu}$ 就不只是包含 $m$ 项，还会多出一个因为与电磁场相互作用的含电荷 $e$ 的项，变成：  
$$
T_{\text{particle}}^{\mu\nu} = \int \mathrm{d}\tau ~ p^\mu \frac{dx^\nu}{d\tau} \delta^{4}(x - x(\tau))
$$
此处 $p^\mu = \frac{ \partial L }{ \partial \dot{x}_\mu }$ 为粒子的广义动量，代入一般的单个带电粒子在电磁场运动的拉氏量 ${L_{3D}}(\vec{x}, \vec{v}, t) = - \frac{mc^2}{\gamma(v)} - e \phi + e \vec{v} \cdot \vec{A}$，或者等价的：$L_{4D}(x^\mu, \dot{x}^\mu, \tau) = -mc \sqrt{\dot{x}^\mu \dot{x}_\mu} - e \dot{x}^\mu A_\mu(x^\mu)$，可以得到：  
$$
p^\mu = \frac{ \partial L_{4D} }{ \partial \dot{x}_\mu } = -m {\dot{x}^\mu} - e A^\mu
$$
前面所说的“多出一个因为与电磁场相互作用的含电荷 $e$ 的项”指的就是上式的第二项。上式也可以等价为：  
$$
\begin{aligned} 
E &= -cp^0 =  \gamma mc^2 + e\varphi  \\
\vec{p}&=\frac{ \partial L_{3D} }{ \partial \vec{v} } =  - (p^i) = \gamma m\vec{v} + e\vec{A}
\end{aligned}
$$
##### 自旋角动量
这里先插入一个题外话, 已知 $M_{\mu\nu}=x_\mu \partial_\nu - x_\mu \partial_\nu$ 是庞加莱群中旋转和 $boost$ 在无穷维表示下的生成元(当然不意外, $M$ 长得像个四维形式的角动量算符). 我们先说明一下旋转变换对应的变分: $\delta \Phi = \underbrace{\epsilon^{ij} S_{ij} \Phi}_{\text{自旋部分}} + \frac{\epsilon^{ij}}{2} \underbrace{(x_i \partial_j - x_j \partial_i)}_{\text{轨道部分}} \Phi$ (视为 $\delta x^\mu = 0$, 主动观点, 变换的是场) 与上面一直用的 $\delta \Phi = \underbrace{\Psi}_{自旋}  \underbrace{ -\delta x^i~ \partial_i \Phi}_{轨道} =  \epsilon^{ij} S_{ij} \Phi - \epsilon^{ij} x_j \partial_i \Phi$ ($\delta x^i = \epsilon^{ij}x_j$, 被动观点, 变换的是坐标系) 的等价性(前者的 $\frac{1}{2}$ 因子是由于庞加莱群的旋转子群是 $SO(3)$ 的双覆盖),  即在庞加莱对称性的框架下, 通过两种变分推导出的轨道角动量是同一个物理概念. 这点容易证明, 只需要注意到旋转参数 $\epsilon^{ij}反对称 \to \frac{\epsilon^{ij}}{2}(x_i \partial_j - x_j \partial_i)\Phi = - \epsilon^{ij} x_j \partial_i \Phi$, 即两者的轨道部分相同即可.

类似上面诺特流导出的方式, 由 $\delta \Phi = \epsilon^{ij} (x_i \partial_j - x_j \partial_i) \Phi + \epsilon^{ij} S_{ij} \Phi$ 导出的守恒流为,
$$
J^\mu = \frac{\partial \mathcal{L}}{\partial (\partial_\mu \Phi)} \epsilon^{ij} \left( x_i \partial_j - x_j \partial_i \right) \Phi + \frac{\partial \mathcal{L}}{\partial (\partial_\mu \Phi)} \epsilon^{ij} S_{ij} \Phi
$$
自旋角动量流对应第二项, 可以直接写出:
$$
(J^\mu)^{ij}_{\text{spin}} = \frac{\partial \mathcal{L}}{\partial (\partial_\mu \Phi)}  S^{ij} \Phi
$$
积分得到自旋角动量:
$$
L^i_{spin} = \frac{1}{2}\epsilon_{ijk} \int d^3x~ \frac{\partial \mathcal{L}}{\partial (\partial_0 \Phi)}  S^{jk} \Phi
$$
最终将有场的总角动量 $L = L_{orbit}+L_{spin}$ 守恒.
#### 推动对称性
从轨道角动量一节已经得到反对称张量 $Q^{\mu\sigma} = \int d^3 x~ (J^0)^{\mu \sigma} = \int d^3 x~ \left(T^{\mu 0}  x^\sigma - T^{\sigma 0} x^\mu\right)$ 为守恒量, 并且在轨道角动量中借用了其空间分量, 同样有时间分量守恒:
$$
Q^{0i} = \int d^3 x~ (J^0)^{0 i} = \int d^3 x~ \left(T^{0 0}  x^i - T^{i 0} x^0\right)
$$
即:
$$
\begin{aligned}
0 = \frac{ \partial Q^{0i} }{ \partial t } 
&= \frac{ \partial Q^{0i} }{ \partial x^0 }
\\&= \frac{ \partial  }{ \partial t }\int d^3x~  T^{00}x^i - t {\int d^3x~ \frac{ \partial T^{i0} }{ \partial t }}  - \underset{\large =P^i = const.}{\underbrace{\int d^3x~ T^{i0}}}\\
\quad\Longrightarrow\quad
	\frac{ \partial E_c }{ \partial t } &=  t P^i = const.
\end{aligned}
$$
对应的是能量中心 $E_c=\int d^3x~  T^{00}x^i$ 以匀速运动. 这与之前的 $boost$ 不变量 $q_c = \frac {{\sum_i m_iq_i}} {\sum_i m_i}= \frac {{\sum_i m_i \dot q_i t}} {\sum_i m_i}$ 不同, $q_c$ 守恒是对多粒子系统的非相对性描述(因为推导所用的是非相对性拉氏量 $\mathcal{L} = \frac{1}{2} \sum_i m_i \dot q_i^2$ , 而不是相对性拉氏量 $\mathcal{L} = \frac{1}{2} \sum_i \gamma_i(\dot {q_i}) m_i \dot q_i^2$), 而 $E_c$ 守恒是狭义相对论当中的描述, 此时能量中心和质心已经通过 $E=\gamma m_0c^2$ 构建了紧密的联系.

