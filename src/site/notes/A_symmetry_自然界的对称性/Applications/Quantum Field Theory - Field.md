---
{"dg-publish":true,"permalink":"/A_symmetry_自然界的对称性/Applications/Quantum Field Theory - Field/","noteIcon":"default","created":"2025-12-01T13:39:20.973+08:00","updated":"2025-11-18T22:30:07.227+08:00"}
---


- refer to *Quantum Field Theory* by Franz Mandl, Graham Shaw.

```table-of-contents
title: 
style: nestedList # TOC style (nestedList|nestedOrderedList|inlineFirstLevel)
minLevel: 0 # Include headings from the specified level
maxLevel: 0 # Include headings up to the specified level
includeLinks: true # Make headings clickable
hideWhenEmpty: false # Hide TOC if no headings are found
debugInConsole: false # Print debug info in Obsidian console
```

# 1 Quantum Mechanics 量子力学
## 1.1 Operator 算符
考虑到算符是厄米的 , 根据前面对称性操作和守恒量的讨论, 容易找到对应关系:
$$
\begin{array}{rccl} 
\color{blue}{对称性操作} \quad\longleftrightarrow\quad &\color{blue}{算符在位置表象下的表示}& \quad\longleftrightarrow\quad &\color{blue}{算符}
\\
空间平移 \quad\longleftrightarrow\quad &-\boldsymbol{i}\partial_i& \quad\longleftrightarrow\quad &动量\ \hat p_i
\\ 
时间平移 \quad\longleftrightarrow\quad &-\boldsymbol{i}\partial_t& \quad\longleftrightarrow\quad &能量\ \hat E
\\
转动(轨道) \quad\longleftrightarrow\quad & \epsilon_{ijk}x^i\partial^j& \quad\longleftrightarrow\quad &轨道角动量 \ \hat L_i
\\
转动(自转) \quad\longleftrightarrow\quad & S_i &  \quad\longleftrightarrow\quad &自旋角动量\ \hat S_i
\end{array}
$$

关于自旋并没有给出详细的算符表示, 因为粒子的自旋不同, 导致 $S_i$ 的表示不唯一. 比如电子自旋为 $\frac{1}{2}$, 对应的是泡利矩阵 $S_i =  \frac{\hbar}{2} \sigma_i$ ; 光子自旋为 $1$, 对应的是 $SO(3)$ 的生成元乘以 $\boldsymbol{i}\hbar$, 等等.

上面的说法仅是一种直觉, 结果也跟量力一致. 其中的厄米性来自于: 算符对应的可观测量必须是实数,  厄米算符的特征值正好满足这一点.
# 2 Quantum Field Theory 量子场论
## 2.1 Klein-Gordon field 克莱恩-戈登场
对于自旋为 $0$ 的粒子(比如 $Higgs$ 玻色子)的标量场, 使用 $Lorentz$ 群的 $(0,0)$ 表示描述其变换, 可以尝试用两种方式得到这种场的运动方程($Euler-Lagrange$ 方程), 或者说场的演化方程.
### 2.1.1 Relativistic generalization of Schrodinger equation 薛定谔方程的相对论推广
经典薛定谔方程基于非相对论性的能动关系, 也就是从以下关系
$$
E = \frac{P^2}{2m} + V(\vec r) \quad\to\quad \hat E = \frac{\hat P\cdot \hat P}{2m} + \hat V(\vec r)
$$
利用上面的物理量与算符在位置表象下的表示, 可以得到经典薛定谔方程:
$$
\boldsymbol{i} \hbar \frac{ \partial \psi }{ \partial t }
= 
\left(  -\frac{\hbar^2}{2m}\nabla^2 + V(\vec r) \right) \psi
$$
如果考虑的是相对论性的能动关系
$$
E^2 = (Pc)^2 + (mc^2)^2
$$
将会得到  
$$
\left(  \boldsymbol{i} \hbar \frac{ \partial}{ \partial t } \right)^2 \psi =
\left( - \hbar^2 c^2 \nabla^2 + m^2 c^4 \right) \psi
\quad \to \quad
\left( \frac{1}{c^2} \frac{ \partial^2 }{ \partial t^2 } - \nabla^2 + \frac{m^2 c^2}{\hbar^2} \right) \psi = 0
$$
这就是 $Klein$ - $Gordon$ 方程. 下面尝试用场的方式得到它.
### 2.1.2 Klein-Gordon equation 克莱恩-戈登方程
对于标量场 $\Phi(x^\mu)$, 首先构造拉格朗日函数, 有几个注意点: (1)拉氏量是洛伦兹标量; (2)拉氏量可以相差任意常数, 这个常数可以直接舍去; 同时拉氏量也可以相差整数倍, 这只会让运动方程多出一个常数倍因子, 所以可以直接选定拉氏量的某一项系数为 $1$; (3)候选的标量不高于二阶(指的是导数以及幂次不高于二阶), 诸如 $\Phi^3$, $\Phi\partial^\mu \partial_\mu\Phi$ 之类的项被直接舍弃, 高阶项的引入会使理论变得复杂(高阶理论涉及到微扰和 $Ostrogradski$ 不稳定性), 同时也使得运动方程包含高阶项, 也因此需要更多的初始条件.

于是, 候选的标量就只剩下(穷举):
$$
\Phi \quad
\Phi^2 \quad
\partial_\mu\Phi\partial^\mu\Phi \quad
\partial_\mu\partial^\mu\Phi \quad
\Phi\partial_\mu\partial^\mu\Phi
$$
另外, 作用量写作 $S = \int \mathcal{L}(\Phi, \partial_\mu \Phi, x^\mu) \mathrm{d}x^0\mathrm{d}x^1\mathrm{d}x^2\mathrm{d}x^3$, 标量场的拉格朗日方程写作 $\frac{ \partial  }{ \partial x^\mu }\frac{ \partial \mathcal{L} }{ \partial (\partial_\mu \Phi) } - \frac{ \partial \mathcal{L} }{ \partial \Phi } = 0$, 注意到
$$
\int \partial_\mu\Phi\partial^\mu\Phi \mathrm{d}x^\mu = 
\int \partial^\mu\Phi ~\mathrm{d}\Phi
= 
\underset{=0}{\underbrace{\left. \Phi\partial^\mu\Phi \right|_{-\infty}^{\infty}} }  - \int \Phi\partial_\mu\partial^\mu\Phi \mathrm{d}x^\mu
$$
上式的 $\mu$ 指的是 $0-3$ 中任意一个指标, 不代表求和意义. 可以看出, 由于场传播的速度有上限, 使得 $\partial_\mu\Phi\partial^\mu\Phi$ 和 $\Phi\partial_\mu\partial^\mu\Phi$ 这两项没有区别. 另外 $\Phi$ 这一项只是给运动方程增加了一个常数, 因此也可以忽略. 而对于 $\partial_\mu\partial^\mu\Phi$, 显然它是一个微分项, 比如
$$
\int \partial_0\partial^0\Phi \mathrm{d}x^0\mathrm{d}x^1\mathrm{d}x^2\mathrm{d}x^3
= 
\int \mathrm{d}x^1\mathrm{d}x^2\mathrm{d}x^3 \left. \partial^0\Phi \right|_{-\infty}^{\infty}
=
0
$$
余下的项就只有 $\Phi^2$ 和 $\partial_\mu\Phi\partial^\mu\Phi$, 前者是质量项, 后者是动能项, 这样常系数就只有一个自由度, 一般选取常系数满足:
$$
\mathcal{L} = \frac{1}{2}(\partial_\mu\Phi\partial^\mu\Phi - m^2\Phi^2)
$$
虽然在没有确定 $m$ 是啥之前, 这个系数选取还没有用掉这一个自由度. 也就是说, 这个给定系数跟没给定一样. 先将拉氏量带入拉格朗日方程可以得到
$$
(\partial_\mu\partial^\mu + m^2)\Phi = 0
$$
这就是四维形式的 $Klein$ - $Gordon$ 方程, 将 $1.1$ 节得到的表达式采取自然单位制($\hbar = c =1$)会得到一致的结果.

- ques:  $m$ 是啥? 
考虑平面波解, 也就是 $\Phi(x^\mu)=\Phi_0 e^{\boldsymbol{i} k_\mu x^\mu} = \Phi_0 e^{\boldsymbol{i}\hbar\{\omega t - \vec k\cdot \vec x\}}$, 带入 $K$ - $G$ 方程得到
$$
(-k_\mu k^\mu + m^2)\Phi_0 e^{\boldsymbol{i} k_\mu x^\mu}=0
\quad\to\quad
(k^0)^2 - \sum_i(k^i)^2 = m^2
$$
因为度规的选取不同( (+---)和(-+++) ), 第二个式子可能多出一个负号, 不过这都没影响, 关键是这个方程就是取自然单位制的能动关系:
$$
E^2 = p^2 + m^2
$$
也就是 $m$ 对应着质量.
## 2.2 Dirac field 狄拉克场  


## 2.3 Proca field 普罗卡场
### 2.3.1 Free field 自由场
与 Klein-Gordon 场十分类似, 只是此时的对象变为四维矢量场 $A^\mu$ (或者说自旋为 1 的粒子产生的场), 候选的标量有:
$$
A_\mu A^\mu \quad 
\partial^\mu A_\mu \quad
\partial^\mu A^\nu\partial_\mu A_\nu \quad
\partial^\mu A^\nu \partial_\nu A_\mu
$$
代入四维场的拉格朗日方程 $\frac{ \partial  }{ \partial x^\mu }\frac{ \partial \mathcal{L} }{ \partial (\partial_\mu A^\nu) } - \frac{ \partial \mathcal{L} }{ \partial A^\nu } = 0$, 发现 $\partial^\mu A_\mu$ 只是给运动方程引入了一个常数项, 因此可以忽略. 于是拉氏量就有两个自由度, 可以写作:
$$
\mathcal{L}  = \partial^\mu A^\nu\partial_\mu A_\nu + C_1 \partial^\mu A^\nu \partial_\nu A_\mu + C_2 A^\mu A_\mu
$$
拉格郎日方程写作:
$$
\partial_\mu \partial^\mu A^\nu + C_1 \partial^\nu \partial_\mu A^\mu = C_2 A^\nu
$$
一般选取这两个常数满足:
$$
\frac{1}{2} \partial_\mu (\partial^\mu A^\nu - \partial^\nu A^\mu) = m^2 A^\nu
$$
这被称为 $proca$ 方程. 一般记场强张量/电磁张量 $F^{\mu\nu} = \partial^\mu A^\nu - \partial^\nu A^\mu$, 对于光子 m=0, 可以从上式写成自由电磁场方程:
$$
\partial_\mu F^{\mu\nu} = 0
$$
拉格朗日量也可以改写为:
$$
\begin{aligned}
\mathcal{L} &= \frac{1}{2}(\partial^\mu A^\nu\partial_\mu A_\nu - \partial^\mu A^\nu \partial_\nu A_\mu) \\
&= 
\frac{1}{4}(2\partial^\mu A^\nu\partial_\mu A_\nu - 2\partial^\mu A^\nu \partial_\nu A_\mu) \\
&=
\frac{1}{4}  (\partial^\mu A^\nu - \partial^\nu A^\mu)( \partial_\mu A_\nu - \partial_\nu A_\mu) \\
&=
\frac{1}{4} F^{\mu\nu} F_{\mu\nu} {\color{grey}\ +\ m^2 A^\mu A_\mu}
\end{aligned}
$$
### 2.3.2 Field with charge/current 非自由场
<font color="#00b0f0">这一部分会与电磁场的内容重合.</font>

由上述已知, 自由电磁场的拉氏量是 $\mathcal{L}_{em}=- \frac{1}{4\mu_0 c} F^{\alpha\beta}F_{\alpha\beta}$, 对于场中存在电荷并且带有电荷运动(电流)场景, 需要引入电荷密度 $\rho$ 和电流密度 $\vec j$, 或者说四维电流 $j^\mu = \rho \frac{ d x^\mu }{ d t} =  (\rho c, \vec j )$,  这一项显然要添加到原有的拉氏量当中去, 那么如何添加?   

已经在理论力学当中知道, 带电粒子在电磁场当中的拉氏量的三维形式:  
$$
L = -\frac{mc^2}{\gamma} - q\phi + q\vec v \cdot \vec A
$$
将其改写为四维形式是容易的, 约定 $u^\mu = (\gamma c, \gamma \vec v),\ A^\mu = \left( \frac{\phi}{c}, \vec A \right)$, 度规为(+---):  
$$
\begin{aligned} 
S 
&= \int L \mathrm{d}t \\
&= \int(-mc^2 - q\gamma \phi + q\gamma \vec v \cdot \vec A)\mathrm{d}\tau \\
&= \int (-mc^2 - qu^\mu A_\mu)\mathrm{d}\tau \\
&=
\int -\sum_i m_ic^2 \mathrm{d}\tau - \int  j^\mu A_\mu \mathrm{d}^3x\mathrm{d}t
\end{aligned}
$$
最后一步将 m 改写为 $m_i$ 并求和(因为场当中运动的电荷不止一个), 并利用了狄拉克函数进行改写, 即 $\rho = \sum_i q_i \delta(\vec x - \vec x_i)$.  于是带电荷源的完整的电磁场作用量写作:  
$$
\begin{aligned} 
S 
&= \int L \mathrm{d}t \\
&=
\int -\sum_i m_ic^2 \mathrm{d}\tau +  \int  \left( - \frac{1}{4\mu_0 c} F^{\alpha\beta}F_{\alpha\beta} -\frac{{j^\mu A_\mu}}{c} \right) \mathrm{d}^4x
\\&=
\int \mathcal{L} \mathrm{d}^4x
\end{aligned}
$$
上式使用了 $\mathrm{d}^4x = c~\mathrm{d}t\mathrm{d}x\mathrm{d}y\mathrm{d}z$, 于是完整的拉格朗日密度可以写作:  
$$
\begin{aligned} 
\mathcal{L}
&=
 -\sum_i \frac{m_i\delta(\vec x-\vec x_i)c^2}{\gamma}  - \frac{1}{4\mu_0 c} F^{\alpha\beta}F_{\alpha\beta} -\frac{{j^\mu A_\mu}}{c}
\end{aligned}
$$

## 2.4 Gauge Theory 规范理论









