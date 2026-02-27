---
{"dg-publish":true,"permalink":"/A_symmetry_自然界的对称性/Applications/Electrodynamics/","noteIcon":"default","created":"2025-12-01T12:17:15.523+08:00","updated":"2025-10-17T15:06:01.367+08:00"}
---


# 1. $Proca$ $field$ 普罗卡场
## 1.1 $From\ Proca\ Equation \ to \ Maxwell's\ Equations$ 从普罗卡方程到麦克斯韦方程组
可跳转 [[A_symmetry_自然界的对称性/Applications/Quantum Field Theory - Field#3. Proca field 普罗卡场\|Quantum Field Theory#3. Proca field]]. 本文采取的度规是(+---).

$Proca$ 场是经典场论中描述有质量的矢量玻色子的重要模型, 其核心方程($Proca$ 方程)扩展了麦克斯韦方程组(即引入了质量项).

首先, 尝试构造满足洛伦兹不变性的拉格朗日密度函数(强约束), 注意到拉氏函数是标量函数, 因此其每一项都是 $Lorentz$ 标量. 可能的不超过二阶的洛伦兹标量包括:
$$
\partial^\mu A^\nu ~ \partial_\mu A_\nu, \ \ 
\partial^\mu A^\nu ~ \partial_\nu A_\mu, \ \ 
A^\mu A_\mu,\ \ 
\partial^\mu A_\mu.
$$
于是可以写出拉氏量的一般形式:
$$
\mathcal{L}(A^\mu) = \partial^\mu A^\nu ~ \partial_\mu A_\nu  +
C_1 ~ \partial^\mu A^\nu ~ \partial_\nu A_\mu  +
C_2 ~ A^\mu A_\mu  +
C_3 ~ \partial^\mu A_\mu
$$
根据欧拉-拉格朗日方程 $\frac{ \partial  }{ \partial x^\mu }\frac{ \partial \mathcal{L} }{ \partial (\partial_\mu A^\nu) } - \frac{ \partial \mathcal{L} }{ \partial A^\nu } = 0$ (可以发现 $\partial^\mu A_\mu$ 这一项对运动方程没有影响), 得到:
$$
C_2 A^\mu = \partial_\nu \partial^\nu A^\mu + C_1 \partial^\mu \partial_\nu A^\nu
$$
一般取常数满足:
$$
m^2A^\mu + \partial_\nu \left( \partial^\nu A^\mu - \partial^\mu A^\nu \right) = 0
$$
这被称为 $\color{red}proca$ <font color="#ff0000">方程</font>, 其中 $m$ 为粒子质量. 取 $F_{\mu\nu} = \partial_\mu A_\nu - \partial_\nu A_\mu$ 是场强张量, 于是对应的拉氏密度可以写作 $\mathcal{L} = -\frac{1}{4} F^{\mu\nu}F_{\mu\nu} + \frac{1}{2} m^2 A^\mu A_\mu$. 

由于电磁场由自旋为 $1$ 且静止质量为 $0$ 的光子产生, 所以由 $m=0$ 的 $proca$ 场描述, 此时就得到电磁场的拉氏量为 $\mathcal{L}_{em}=- \frac{1}{4\mu_0} F^{\alpha\beta}F_{\alpha\beta}$. 设 $A^\mu = \left( \frac{\phi}{c},~ \vec A \right)$, $proca$ 方程可以改写为
$$
\partial_\mu F^{\mu\nu} = 0
$$
$F^{\mu\nu}$ 又被称为电磁张量, 上式也等价于描述自由场的麦克斯韦方程组的其中两个:
$$
\begin{cases}
\nabla \cdot \vec E &= 0 \\
\nabla \times \vec B &= \frac{1}{c^2} \frac{ \partial \vec E }{ \partial t }
\end{cases}
$$
麦克斯韦方程组的另外两个方程, 实际上已经蕴含在电磁张量的定义$F_{\mu\nu} = \partial_\mu A_\nu - \partial_\nu A_\mu$当中. 由于 $F^{\mu\nu}$ 和 $\epsilon^{\mu\nu\rho\sigma}$ 均为反对称张量, 于是可以构造对偶张量 $\tilde F^{\mu\nu}=\frac{1}{2}\epsilon^{\mu\nu\rho\sigma}F_{\rho\sigma}$, 根据 $F^{\mu\nu} = \partial^\mu A^\nu - \partial^\nu A^\mu$ 得到:
$$
\partial_\mu \tilde F^{\mu\nu} = \epsilon^{\mu\nu\rho\sigma}(\partial_\mu\partial_\rho A_\sigma - \partial_\mu\partial_\sigma A_\rho )
$$
注意到
$$
\epsilon^{\mu\nu\rho\sigma}(\partial_\mu\partial_\rho A_\sigma - \partial_\mu\partial_\sigma A_\rho)
\overset{\rho\leftrightarrow\sigma}=
-\epsilon^{\mu\nu\sigma\rho}(\partial_\mu\partial_\sigma A_\rho - \partial_\mu\partial_\sigma A_\sigma)
\overset{\rho\sigma 是哑指标}=
-\epsilon^{\mu\nu\rho\sigma}(\partial_\mu\partial_\rho A_\sigma - \partial_\mu\partial_\sigma A_\rho)
$$
这意味着原表达式关于哑指标 $\rho\sigma$ 反对称相消, 因此
$$
\partial_\mu \tilde F^{\mu\nu} = 0
$$
上式对应剩下的两个麦克斯韦方程:
$$
\begin{cases}
\nabla \cdot \vec{B} = 0 \\
\nabla \times \vec{E} = -\frac{\partial \vec{B}}{\partial t}
\end{cases}
$$
当然, 如果考虑电荷的存在(非自由场), (参见 [[A_symmetry_自然界的对称性/Applications/Quantum Field Theory - Field#3.2 Field with charge/current 非自由场\|Quantum Field Theory#3.2 Field with charge]])引入质点 $m_i$ 和四维电流 $j^\mu$, 也有:  
$$
\begin{aligned} 
\mathcal{L}
&=
 -\sum_i \frac{m_i\delta(\vec x-\vec x_i)c^2}{\gamma}  - \frac{1}{4\mu_0 c} F^{\alpha\beta}F_{\alpha\beta} -\frac{{j^\mu A_\mu}}{c}
\end{aligned}
$$
这将为欧拉-拉格朗日方程引入新的项, 变成:  
$$
\frac{ \partial  }{ \partial x^\mu }\frac{ \partial \mathcal{L} }{ \partial (\partial_\mu A^\nu) } - \frac{ \partial \mathcal{L} }{ \partial A^\nu } = 0
\quad\to\quad
\partial_\mu F^{\mu\nu} = \mu_0 j^\mu
\quad\to\quad
\begin{cases}
\nabla \cdot \vec E = \frac{\rho}{\epsilon_0} \\
\nabla \times \vec B = \frac{1}{c^2} \frac{ \partial \vec E }{ \partial t } + \mu_0 \vec j
\end{cases}
$$
而另外一对方程对应着 $\partial_\mu \tilde F^{\mu\nu} = 0$, 与电荷无关, 所以依旧成立.
## 1.2 $Electromagnetic\ Field's\ U(1)\ Gauge\ Symmetry$ 电磁场的 U(1) 规范
$U(1)$ 规范对称性是指: 对电磁场的四维势 $A_\mu$ 做如下变换时, 物理观测结果 $\mathbf{E}$ 和 $\mathbf{B}$ 保持不变:
$$
A_\mu \to A_\mu + \partial_\mu f,
$$
其中 $f(x)$ 是任意标量函数. 这被称为电磁场的规范变换($Gauge~transformstion$), 该变换下场强张量 $F_{\mu\nu}$ 的变换为：
$$
F_{\mu\nu} \to \partial_\mu (A_\nu + \partial_\nu \lambda) - \partial_\nu (A_\mu + \partial_\mu \lambda) = \partial_\mu A_\nu - \partial_\nu A_\mu = F_{\mu\nu}.
$$
保持不变, 因此拉格朗日量 $\mathcal{L}_{\text{em}}$ 也不变.
# 2. $T^{\mu\nu}\ of\ Vacuum\ Free\ EMF$ 真空自由场的能动张量
电磁张量可以写作:
$$
F_{\mu\nu}= \partial_\mu A_\nu-\partial_\nu A_\mu
= \begin{bmatrix}   0 & \frac{E_x}{c} & \frac{E_y}{c} & \frac{E_z}{c}\\   -\frac{E_x}{c} & 0 & -B_z & B_y\\   -\frac{E_y}{c} & -\frac{E_z}{c} & 0 & -B_x \\    -B_y & B_z & B_x & 0 \end{bmatrix} 
\quad\longleftrightarrow\quad
\left\{
\begin{array}{l} F_{0i}=\frac{E_i}{c} \\ F_{ij}=-\epsilon_{ijk}B_k \end{array}
\right.
$$
于是拉氏量也可以显式地写为
$$
\mathcal{L} 
= -\frac{1}{4\mu_0}(\partial_\mu A_\nu-\partial_\nu A_\mu)(\partial^\mu A^\nu-\partial^\nu A^\mu)
= \frac{1}{2} \left( \epsilon_0 E^2 - \frac{B^2}{\mu_0} \right)
$$
根据 $T^{\mu\nu} = \frac{\partial \mathcal{L}}{\partial (\partial_\mu \Phi)} \partial^\nu \Phi - g^{\mu\nu} \mathcal{L}$ 和上式第一个等号, 可以计算得到
$$
T^{\mu\nu} = -\frac{1}{\mu_0}F^{\mu\lambda}\partial^\nu A_\lambda + \frac{1}{4\mu_0}g^{\mu\nu}F^{\alpha\beta}F_{\alpha\beta}
$$
遗憾的是, 这个形式并不对称, 因而不能让诺特流满足 $\partial_\nu (J^\nu)^{\mu\sigma} = 0$ (参见 [[A_symmetry_自然界的对称性/Tools/Noether's Theorem and Symmetry#诺特流\|Noether's Theorem and Symmetry]]), 需要对其加以修正.
# 3. $Symmetric\ correction$ 对称性修正
注意到 $\partial_\mu T^{\mu\nu}=0$, 而由于 $F^{\mu\lambda}$ 是反对称张量, 使得 $\partial_\lambda (F^{\mu\lambda} A^\nu)$ 恰好也满足 $\partial_\mu\partial_\lambda (F^{\mu\lambda} A^\nu)=0$.

于是可做修正 $T^{\mu\nu} \to T^{\mu\nu} + \frac{1}{\mu_0} \partial_\lambda (F^{\mu\lambda} A^\nu)$, 使得旧的 $T^{\mu\nu} = -\frac{1}{\mu_0}F^{\mu\lambda}\partial^\nu A_\lambda + \frac{1}{4\mu_0}g^{\mu\nu}F^{\alpha\beta}F_{\alpha\beta}$ 的第一项对称(进而 $T^{\mu\nu}$ 对称), 得到新的能动张量可以改写为:
$$
T^{\mu\nu} = \frac{1}{\mu_0} \left( F^{\mu\lambda}F_\lambda^{~\nu} + \frac{1}{4} g^{\mu\nu}F^{\alpha\beta}F_{\alpha\beta} \right)
$$
两项都是两个反对称张量的缩并, 结果自然对称(度规对称时). 在闵氏度规 $(+,-,-,-)$ 下展开得到具体形式:
$$
T^{\mu\nu} = \begin{bmatrix}   能量 & 能流\left( {动量}\cdot{c^2} \right)\\  能流 \left( {动量}\cdot{c^2} \right) & (电磁应力)_{3\times 3} \\   \end{bmatrix}
\quad\longleftrightarrow\quad
\left\{
\begin{array}{l} 
T^{00} = \frac{1}{2} \left( \epsilon_0 E^2 + \frac{B^2}{\mu_0} \right)
\\ 
T^{0i} = \frac{1}{c\mu_0} (\vec E \times \vec B )_i = \frac{1}{c}S_i = P_i c
\\
T^{ij} = \frac{1}{2} \left( \epsilon_0 E^2 - \frac{B^2}{\mu_0} \right) \delta^{ij} - \left( \epsilon_0 \vec E \vec E + \frac{\vec B\vec B}{\mu_0} \right)
\end{array}
\right.
$$
其中 $\vec S$ 是能流密度(波印廷矢量), $\vec P$ 是场的动量密度.
# 4. $Continuity\ equations$ 连续性方程
在非自由电磁场中, 由于场与粒子相互作用, 使得场的四维散度 $\partial_\mu T^{\mu\nu} \neq 0$, 利用有源 $maxwell$ 方程组
$$
\begin{aligned}
\nabla \times \vec E &= -\frac{ \partial \vec B }{ \partial t } \\
\nabla \cdot \epsilon  \vec E &= \rho \\
\nabla \times \frac{\vec B}{\mu} &= \vec j  + \frac{ \partial \epsilon \vec E }{ \partial t } \\
\nabla \cdot \vec B &= 0
\end{aligned}
$$
可以得到 $\partial_\mu T^{\mu\nu}$是:
$$
\begin{array}{l} 
\partial_\mu T^{\mu 0}
= \frac{1}{c} \frac{ \partial  }{ \partial t } E_{em} + \nabla \cdot \frac{1}{c}\vec{S}
 = - \frac{1}{c} \vec{j} \cdot \vec E = -\frac{1}{c}{f^0}
\\ 
\partial_\mu T^{\mu i} = \frac{ \partial  }{ \partial t }\vec{S} - \nabla \cdot \boldsymbol{T} = -\left( \vec j \times \vec B + \rho\vec{E} \right)_i = -f^i
\end{array}
$$
其中 $E_{em} = \frac{1}{2}(\epsilon_0 E^2 + \frac{B^2}{\mu_0})$ 为场的能量密度, $\boldsymbol{T}=-(T^{ij}) = -\frac{1}{2} \left( \epsilon_0 E^2 - \frac{B^2}{\mu_0} \right) \boldsymbol{I} + \left( \epsilon_0 \vec E \vec E + \frac{\vec B\vec B}{\mu_0} \right)$ 是 $maxwell$ 应力张量. $f^\mu = \left( \frac{1}{c} f^0, \vec f \right)$ 为四维洛伦兹力, 其时间部分 $f^0 = \vec j \cdot \vec E$ 是电磁场对粒子做的功(同时也是场的能量密度的损失速度), 空间部分 $\vec f = \vec j \times \vec B + \rho \vec E$ 是所谓的洛伦兹力(或者说场的动量密度损失).  

上述关系也可以写成更简洁的形式:  
$$
\partial_\mu T^{\mu\nu}_{E.M.field} = -F^{\nu}_{~~\mu} j^\mu
$$
四维洛伦兹力因此也可以记作:
$$
f^\mu = F^{\mu}_{~~\nu} j^\nu = m\delta(\vec x - \vec x_0)\frac{ d u^\mu }{ d t}
$$







