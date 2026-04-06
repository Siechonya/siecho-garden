---
{"dg-publish":true,"permalink":"/EMD26/T/","noteIcon":"default","created":"2026-04-06T14:10:54.279+08:00","updated":"2026-04-06T15:21:00.012+08:00"}
---


# 1 HW 2思考题  
## 1.1 
这个张量怎么有点眼熟，算电磁和引力辐射时貌似会用到
### 1.1.1 
$$
\begin{align} 
T_{ij} &=
\int \delta(r-1) x_ix_j \,\mathrm{d}^3x \\[4pt]
&=
\iint \delta(r-1) x_ix_j r^2 \,\mathrm{d}r \mathrm{d}\Omega \\[4pt]
&=
\int_0^\infty \int_{4\pi} \delta(r-1) \left( \frac{x_i}{r} \right)\left( \frac{x_j}{r} \right) r^4 \,\mathrm{d}r \mathrm{d}\Omega \\[4pt]
&=
\int_{0}^{\infty} r^4 \delta(r - 1) dr \oint n_i n_j d\Omega \\[4pt]
&=
\oint n_i n_j d\Omega
\end{align} 
$$
### 1.1.2 
在旋转变换下，向量 $n_i$ 变为 $n'_i = R_{ik} n_k$，所以
$$
\begin{align} 
T'_{ij} 
&= \oint (R_{ik} n_k) (R_{jl} n_l) \,\mathrm{d}\Omega = R_{ik} R_{jl} \oint n_k n_l d\Omega  \\[4pt]
&=  R_{ik} R_{jl} T_{kl}
\end{align}
$$
### 1.1.3 
见 ppt，$C = \frac{4\pi}{3}$  

### 1.1.4 
第一个利用 $\mathrm{d}\Omega = \sin\theta \mathrm{d}\theta\mathrm{d}\phi$ 即可。  

第二个，根据对称性，可以直接算 z 方向计算： $=\iint \frac{z}{r}\sin\theta \mathrm{d}\theta\mathrm{d}\phi=\iint \frac{r\cos\theta}{r}\sin\theta \mathrm{d}\theta\mathrm{d}\phi =0$

第三个，看讲义  

第四个，被积函数是奇函数，结果为零

第五个，积分结果必须是 $SO(3)$ 下的不变张量，且阶数为四，它必须由克罗内克符号 $\delta$ 组合而成。所有可能的配对方式只有三种：
$$
\oint n_i n_j n_k n_l \,\mathrm{d}\Omega = C (\delta_{ij}\delta_{kl} + \delta_{ik}\delta_{jl} + \delta_{il}\delta_{jk})
$$
注意，由于 $n_i n_j n_k n_l$ 对索引 $i, j, k, l$ 的任意排列都是全对称的，所以这三项前的系数 $C$ 必须相等。先做两次缩并，左边：  
$$
\oint (n_i n_i) (n_k n_k)\,\mathrm{d}\Omega = \oint 1 \cdot 1 \, \mathrm{d}\Omega  = 4\pi
$$
右边：  
$$
(\delta_{ii}\delta_{kk} + \delta_{ik}\delta_{ik} + \delta_{ik}\delta_{ik}) = 9+3+3 = 15
$$
所以 $C=\frac{4\pi}{15}$.  

## 1.2 
略  

## 1.3 
用柱坐标爆算，注意：
$$
\boldsymbol{E} = \frac{e}{4\pi\varepsilon_0} \frac{\gamma \boldsymbol{R}}{[s^2 + \gamma^2(z-vt)^2]^{3/2}}
$$
剩下的懒得写了。


# 2 HW 3思考题  
## 2.1 
### 2.1.1 
验证给定的势函数是否满足 $\boldsymbol{E} = -\nabla \varphi$ 和 $\boldsymbol{B} = \nabla \times \boldsymbol{A}$ 即可
### 2.1.2 
令 $\boldsymbol{u} = \lambda\boldsymbol{x}$，则 $u_i = \lambda x_i$。
$$
\frac{\mathrm{d}}{\mathrm{d}\lambda} F_j(\lambda\boldsymbol{x}) = \frac{\partial F_j}{\partial u_i} \frac{\mathrm{d}u_i}{\mathrm{d}\lambda} = \frac{\partial F_j}{\partial u_i} x_i = \frac{1}{\lambda} \left( x_i \frac{\partial F_j}{\partial x_i} \right) = \frac{1}{\lambda} (\boldsymbol{x} \cdot \nabla) F_j(\lambda\boldsymbol{x})
$$
即：$\frac{\mathrm{d}}{\mathrm{d}\lambda} \boldsymbol{F}(\lambda\boldsymbol{x}) = \frac{1}{\lambda} (\boldsymbol{x} \cdot \nabla) \boldsymbol{F}(\lambda\boldsymbol{x})$。

1. 证明 $\boldsymbol{B} = \nabla \times \boldsymbol{A}$：
$$\nabla \times \boldsymbol{A} = -\int_0^1 \lambda \nabla \times (\boldsymbol{x} \times \boldsymbol{B}(t, \lambda\boldsymbol{x})) \,\mathrm{d}\lambda$$
利用 $\nabla\times(\vec A\times \vec B)=(\vec B\cdot\nabla)\vec A+(\nabla\cdot\vec B)\vec A-(\vec A\cdot\nabla)\vec B-(\nabla\cdot\vec A)\vec B$，注意此时 $\nabla \cdot \boldsymbol{B} = 0$ 且 $(\boldsymbol{x} \cdot \nabla) \boldsymbol{B}_{\lambda} = \lambda \frac{\mathrm{d}}{\mathrm{d}\lambda} \boldsymbol{B}_{\lambda}$：
$$\nabla \times (\boldsymbol{x} \times \boldsymbol{B}_{\lambda}) = \boldsymbol{x}\cdot 0 - \boldsymbol{B}_{\lambda}\cdot 3 + \boldsymbol{B}_{\lambda} - \lambda \frac{\mathrm{d}}{\mathrm{d}\lambda} \vec{B}_{\lambda} = -2\boldsymbol{B}_{\lambda} - \lambda \frac{\mathrm{d}}{\mathrm{d}\lambda} \boldsymbol{B}_{\lambda}$$
角标 $\lambda$ 没有其他含义，只是表示 $\lambda$ 作为当前函数的自变量之一。上式代入积分：
$$
\nabla \times \boldsymbol{A} = \int_0^1 (2\lambda \boldsymbol{B}_{\lambda} + \lambda^2 \frac{\mathrm{d}}{\mathrm{d}\lambda} \boldsymbol{B}_{\lambda})\, \mathrm{d}\lambda 
= \int_0^1 \frac{\mathrm{d}}{\mathrm{d}\lambda} (\lambda^2 \boldsymbol{B}(t, \lambda\boldsymbol{x})) \,\mathrm{d}\lambda = [\lambda^2 \boldsymbol{B}(t, \lambda\boldsymbol{x})]_0^1 = \boldsymbol{B}(t, \boldsymbol{x})
$$
2. 证明 $\boldsymbol{E} = -\nabla \varphi - \partial_t \boldsymbol{A}$：

利用 $\nabla (\vec A\cdot \vec B)=\vec A\times(\nabla\times\vec B)+\vec B\times(\nabla\times\vec A)+(\vec A\cdot\nabla)\vec B+(\vec B\cdot\nabla)\vec A$ 计算 $\nabla \varphi$：
$$\nabla \varphi = -\int_0^1 \nabla (\boldsymbol{x} \cdot \boldsymbol{E}_{\lambda}) d\lambda = -\int_0^1 [\boldsymbol{E}_{\lambda} + (\boldsymbol{x} \cdot \nabla)\boldsymbol{E}_{\lambda} + \boldsymbol{x} \times (\nabla \times \boldsymbol{E}_{\lambda})] \,\mathrm{d}\lambda$$
利用法拉第定律 $\nabla_u \times \boldsymbol{E} = -\partial_t \boldsymbol{B}$，得 $\nabla \times \boldsymbol{E}_{\lambda} = -\lambda \partial_t \boldsymbol{B}_{\lambda}$：
$$\nabla \varphi = -\int_0^1 [\boldsymbol{E}_{\lambda} + \lambda \frac{\mathrm{d}}{\mathrm{d}\lambda} \boldsymbol{E}_{\lambda} - \lambda \boldsymbol{x} \times \partial_t \boldsymbol{B}_{\lambda}] \,\mathrm{d}\lambda = -\int_0^1 \frac{\mathrm{d}}{\mathrm{d}\lambda}(\lambda \boldsymbol{E}_{\lambda}) \,\mathrm{d}\lambda + \partial_t \int_0^1 \lambda \boldsymbol{x} \times \boldsymbol{B}_{\lambda} \,\mathrm{d}\lambda$$
$$\nabla \varphi = -\boldsymbol{E}(t, \boldsymbol{x}) - \partial_t \boldsymbol{A} \implies \boldsymbol{E} = -\nabla \varphi - \partial_t \boldsymbol{A}$$
证毕。
## 2.2 
磁矢势满足 $U(1)$ 规范：  
$\boldsymbol{A} \to \boldsymbol{A}' = \boldsymbol{A} + \nabla \Lambda$。

将变换后的 $\vec{A}'$ 同样进行分解，由于 $\nabla \Lambda$ 本身是一个梯度场（无旋），它完全属于纵向分量。根据亥姆霍兹分解的唯一性：
$$\boldsymbol{A}'_\parallel + \boldsymbol{A}'_\perp = (\boldsymbol{A}_\parallel + \nabla \Lambda) + \boldsymbol{A}_\perp$$
横向分量 $\boldsymbol{A}_\perp$ 在规范变换下保持不变（即它是规范无关的）。  
$$\boldsymbol{B} = \nabla \times \boldsymbol{A} = \nabla \times (\boldsymbol{A}_\parallel + \boldsymbol{A}_\perp) = 0 + \nabla \times \boldsymbol{A}_\perp = \nabla \times \boldsymbol{A}_\perp$$
可以看到，磁场完全由 $\boldsymbol{A}_\perp$ 决定。
## 2.3 
参考 ppt  


# 3 HW 4思考题  
## 3.1 磁偶极子/带电旋转球
### 3.1.1 
球壳上的面电流密度 $\boldsymbol{K}(\boldsymbol{x}')$ 是由表面电荷随球壳转动产生的，其表达式为：
$$
\boldsymbol{K}(\boldsymbol{x}') = \sigma_0 \boldsymbol{v} = \sigma_0 (\boldsymbol{\omega} \times \boldsymbol{x}')
$$
其中 $\boldsymbol{x}'$ 为球壳上的源点位置矢量，且 $|\boldsymbol{x}'| = a$。所以磁矢势为
$$
\begin{align} 
\boldsymbol{A}(\boldsymbol{x}) 
&= \frac{\mu_0}{4\pi} \oint_S \frac{\sigma_0 (\boldsymbol{\omega} \times \boldsymbol{x}')}{|\boldsymbol{x} - \boldsymbol{x}'|} \,\mathrm{d}\sigma' 
\\[4pt]
&=\frac{\mu_0 \sigma_0}{4\pi} \boldsymbol{\omega} \times \oint_S \frac{\boldsymbol{x}'}{|\boldsymbol{x} - \boldsymbol{x}'|} \,\mathrm{d}\sigma'
\\[4pt]
\end{align}
$$
令积分部分为 $\boldsymbol{I} = \oint_S \frac{\boldsymbol{x}'}{|\boldsymbol{x} - \boldsymbol{x}'|} \,\mathrm{d}\sigma'$。设 $\boldsymbol{x}' = a \hat{\boldsymbol{r}}'$，面元 $\,\mathrm{d}\sigma' = a^2 \,\mathrm{d}\Omega'$。球坐标系下（参见 [[A_symmetry_自然界的对称性/杂记/3-D Laplace Equation And Spherical Harmonic Function#4.1 函数 $ frac{1}{ vec{r}- vec{a} }$ 的勒让德系数\|3-D Laplace Equation And Spherical Harmonic Function#4.1 函数 $ frac{1}{ vec{r}- vec{a} }$ 的勒让德系数]]）：
$$
\frac{1}{|\boldsymbol{x}-\boldsymbol{x'}|} = \sum_{l=0}^\infty  \frac{r_<^l}{r^{l+1}_>} P_l(\cos\gamma), \quad \gamma=\arccos\frac{\boldsymbol{x}\cdot\boldsymbol{x'}}{|\boldsymbol{x}\cdot\boldsymbol{x'}|},\  \quad r_< = \min(x,x'), \ r_> = \max(x,x')
$$
则
$$\boldsymbol{I} = a^3 \sum_{l=0}^{\infty} \frac{r_<^l}{r_>^{l+1}} \oint_S P_l(\cos\gamma) \hat{\boldsymbol{r}}' \,\mathrm{d}\Omega'$$
由于 $\hat{\boldsymbol{r}}'$ 可以看作是由 $l=1$ 的球谐函数线性组合而成，根据正交性，只有 $l=1$ 的项对应的积分不为零。当 $l=1$ 时，$P_1(\cos\gamma) = \cos\gamma = \hat{\boldsymbol{r}} \cdot \hat{\boldsymbol{r}}'$，故：
$$\boldsymbol{I} = a^3 \frac{r_<}{r_>^2} \oint_S (\hat{\boldsymbol{r}} \cdot \hat{\boldsymbol{r}}') \hat{\boldsymbol{r}}' \,\mathrm{d}\Omega'$$
利用课上的 $\oint_S \hat{\boldsymbol{r}}' \hat{\boldsymbol{r}}' \,\mathrm{d}\Omega' = \frac{4\pi}{3} \mathsf{I}$，得到：
$$\boldsymbol{I} = a^3 \frac{r_<}{r_>^2} \frac{4\pi}{3} \hat{\boldsymbol{r}} = \frac{4\pi a^3}{3} \frac{r_<}{r_>^2} \hat{\boldsymbol{r}}$$
所以
$$
\boldsymbol{A}(\boldsymbol{x}) = \frac{\mu_0 \sigma_0}{4\pi} \boldsymbol{\omega} \times \left( \frac{4\pi a^3}{3} \frac{r_<}{r_>^2} \hat{\boldsymbol{r}} \right) = \frac{\mu_0 \sigma_0 a^3}{3} \frac{r_<}{r_>^2} (\boldsymbol{\omega} \times \hat{\boldsymbol{r}})
$$
$$
\boldsymbol{A}_{in}(\boldsymbol{x}) = \frac{\mu_0 \sigma_0 a^3}{3} \frac{r}{a^2} (\boldsymbol{\omega} \times \frac{\boldsymbol{x}}{r}) = {\frac{\mu_0 \sigma_0 a}{3} (\boldsymbol{\omega} \times \boldsymbol{x})}, \quad r< a
$$
$$
\boldsymbol{A}_{out}(\boldsymbol{x}) = \frac{\mu_0 \sigma_0 a^3}{3} \frac{a}{r^2} (\boldsymbol{\omega} \times \frac{\boldsymbol{x}}{r}) = {\frac{\mu_0 \sigma_0 a^4}{3 r^3} (\boldsymbol{\omega} \times \boldsymbol{x})}, \quad r>a
$$
### 3.1.2 
磁感应强度由 $\boldsymbol{B} = \nabla \times \boldsymbol{A}$ 给出。利用 $\nabla \times (\boldsymbol{\omega} \times \boldsymbol{x}) = \boldsymbol{\omega}(\nabla \cdot \boldsymbol{x}) - (\boldsymbol{\omega} \cdot \nabla)\boldsymbol{x} = 3\boldsymbol{\omega} - \boldsymbol{\omega} = 2\boldsymbol{\omega}$，可得：
$$
\boldsymbol{B}_{in} = \nabla \times \left[ \frac{\mu_0 \sigma_0 a}{3} (\boldsymbol{\omega} \times \boldsymbol{x}) \right] = {\frac{2}{3} \mu_0 \sigma_0 a \boldsymbol{\omega}}  
$$
对于球外场，利用 $\nabla \times (f\boldsymbol{V}) = \nabla f \times \boldsymbol{V} + f(\nabla \times \boldsymbol{V})$，设 $f(r) = r^{-3}$，$\boldsymbol{V} = \boldsymbol{\omega} \times \boldsymbol{x}$：
$$\nabla(r^{-3}) \times (\boldsymbol{\omega} \times \boldsymbol{x}) = -3r^{-4}\hat{\boldsymbol{r}} \times (\boldsymbol{\omega} \times \boldsymbol{x}) = -3r^{-5} \boldsymbol{x} \times (\boldsymbol{\omega} \times \boldsymbol{x})$$
展开三重叉积 $\boldsymbol{x} \times (\boldsymbol{\omega} \times \boldsymbol{x}) = \boldsymbol{\omega}(\boldsymbol{x} \cdot \boldsymbol{x}) - \boldsymbol{x}(\boldsymbol{x} \cdot \boldsymbol{\omega}) = r^2\boldsymbol{\omega} - r^2(\boldsymbol{\omega} \cdot \hat{\boldsymbol{r}})\hat{\boldsymbol{r}}$，所以
$$\nabla \times \left( \frac{\boldsymbol{\omega} \times \boldsymbol{x}}{r^3} \right) = -3r^{-5}[r^2\boldsymbol{\omega} - r^2(\boldsymbol{\omega} \cdot \hat{\boldsymbol{r}})\hat{\boldsymbol{r}}] + r^{-3}(2\boldsymbol{\omega}) = \frac{1}{r^3} [3(\boldsymbol{\omega} \cdot \hat{\boldsymbol{r}})\hat{\boldsymbol{r}} - \boldsymbol{\omega}]$$
代入系数，得到球外的磁场分布：
$$\boldsymbol{B}_{out} = {\frac{\mu_0 \sigma_0 a^4}{3 r^3} [3(\boldsymbol{\omega} \cdot \hat{\boldsymbol{r}})\hat{\boldsymbol{r}} - \boldsymbol{\omega}]}$$
显然这是一个磁偶极子场，其磁矩为 $\boldsymbol{m} = \frac{4\pi}{3}\sigma_0 \boldsymbol{\omega} a^4$。
### 3.1.3 
和课上带电球受力的求解类似，我们选择包围整个上半空间（$z > 0$）的闭合曲面 $S$。这个闭合曲面包括无穷远处的半球面（$r \to \infty, z > 0$）和赤道平面（$z = 0$）。

由于在无穷远处，偶极子磁场 $B \propto 1/r^3$，所以张量分量 $T \propto 1/r^6$。而无穷远半球面的面积元 $\mathrm{d}a \propto r^2$，因此当 $r \to \infty$ 时，无穷远半球面上的积分项趋近于 $0$。

所以，我们只需要计算在赤道平面（$z=0$）上的积分。对于上半空间，面元向量为 $\mathrm{d}\boldsymbol{a} = -\hat{\boldsymbol{z}} \,\mathrm{d}a$。

由于对称性，赤道面上的磁力只可能有 $z$ 分量（径向受力相互抵消）：
$$F_z = \int_{z=0} (\mathsf{T} \cdot \mathrm{d}\boldsymbol{a})_z = \int_{z=0} T_{zz} (-\mathrm{d}a) = -\int_{z=0} T_{zz} \,\mathrm{d}a$$
麦克斯韦应力张量的纯磁场部分定义为 $T_{ij} = \frac{1}{\mu_0} \left( B_i B_j - \frac{1}{2}\delta_{ij}B^2 \right)$：
$$T_{zz}^{in} = \frac{1}{2\mu_0} \left( \frac{2}{3} \mu_0 \sigma_0 a \omega \right)^2 = \frac{2}{9} \mu_0 \sigma_0^2 a^2 \omega^2$$
所以
$$F_{z}^{in} = -\int_0^a \left( \frac{2}{9} \mu_0 \sigma_0^2 a^2 \omega^2 \right) 2\pi r \,\mathrm{d}r = -\frac{4\pi}{9} \mu_0 \sigma_0^2 a^2 \omega^2 \left[ \frac{1}{2}r^2 \right]_0^a = {-\frac{2\pi}{9} \mu_0 \sigma_0^2 a^4 \omega^2}$$
在赤道面上（$\boldsymbol{\omega} \cdot \hat{\boldsymbol{r}} = 0$），外部磁场退化为 $\boldsymbol{B}_{out} = -\frac{\mu_0 \sigma_0 a^4 \omega}{3r^3} \hat{\boldsymbol{z}}$：
$$T_{zz}^{out} = \frac{1}{2\mu_0} \left( -\frac{\mu_0 \sigma_0 a^4 \omega}{3r^3} \right)^2 = \frac{\mu_0 \sigma_0^2 a^8 \omega^2}{18 r^6}$$
所以
$$F_{z}^{out} = -\int_a^\infty \left( \frac{\mu_0 \sigma_0^2 a^8 \omega^2}{18 r^6} \right) 2\pi r \,\mathrm{d}r = -\frac{\pi}{9} \mu_0 \sigma_0^2 a^8 \omega^2 \int_a^\infty r^{-5} \,\mathrm{d}r =-\frac{\pi}{36} \mu_0 \sigma_0^2 a^4 \omega^2$$
最终得到
$$F_z = F_{z}^{in} + F_{z}^{out} = {-\frac{\pi}{4} \mu_0 \sigma_0^2 a^4 \omega^2}$$
负号代表方向朝下（南半球方向），即两半球之间相互吸引。
## 3.2 电子经典球壳模型
### 3.2.1 
对于半径为 $a$、电量为 $e$ 的均匀带电球壳，球内电场为 $0$，球外电场为 $E = \frac{e}{4\pi\epsilon_0 r^2}$，$\sigma_0=\frac{e}{4\pi a^2}$，
$$W_E = \int_{a}^{\infty} \frac{1}{2}\epsilon_0 E^2 (4\pi r^2) \mathrm{d}r = \frac{e^2}{8\pi\epsilon_0 a}$$
利用上一题结论，内部磁场 $B_{in} = \frac{\mu_0 e \omega}{6\pi a}$，外部为偶极场。

> [!info] $W_M = \frac{1}{2} \oint \boldsymbol{A} \cdot \boldsymbol{K} \mathrm{d}a$
> $$\int_{all} \frac{B^2}{2\mu_0} \mathrm{d}V = \frac{1}{2\mu_0} \int \boldsymbol{B} \cdot (\nabla \times \boldsymbol{A}) \mathrm{d}V$$
> 利用分部积分：
> $$\int \boldsymbol{B} \cdot (\nabla \times \boldsymbol{A}) \mathrm{d}V = \int \boldsymbol{A} \cdot (\nabla \times \boldsymbol{B}) \mathrm{d}V + \oint_{\infty} (\boldsymbol{A} \times \boldsymbol{B}) \cdot \mathrm{d}\boldsymbol{S}$$
> 对于局域分布的源，无穷远处的表面积分为 0。代入安培环路定理 $\nabla \times \boldsymbol{B} = \mu_0 \boldsymbol{J}$：
> $$\int_{all} \frac{B^2}{2\mu_0} \mathrm{d}V = \frac{1}{2\mu_0} \int \boldsymbol{A} \cdot (\mu_0 \boldsymbol{J}) \mathrm{d}V = \frac{1}{2} \int \boldsymbol{A} \cdot \boldsymbol{J} \mathrm{d}V$$

已知球面上的矢量势为 $\boldsymbol{A}(a) ={\frac{\mu_0 \sigma_0 a}{3} (\boldsymbol{\omega} \times \boldsymbol{x})}= \frac{\mu_0 e \omega a \sin\theta}{12\pi} \hat{\boldsymbol{\phi}}$，面电流密度为 $\boldsymbol{K} =\sigma_0 \boldsymbol{v} = \sigma_0 a\sin\theta \omega= \frac{e \omega \sin\theta}{4\pi a} \hat{\boldsymbol{\phi}}$。所以磁能：    
$$W_M = \frac{1}{2} \int_0^\pi \left( \frac{\mu_0 e \omega a \sin\theta}{12\pi} \right) \left( \frac{e \omega \sin\theta}{4\pi a} \right) (2\pi a^2 \sin\theta) \mathrm{d}\theta = \frac{\mu_0 e^2 \omega^2 a}{36\pi}$$  
总能量
$$W = \frac{e^2}{8\pi\epsilon_0 a} + \frac{\mu_0 e^2 \omega^2 a}{36\pi}$$

### 3.2.2 
磁矩 $\boldsymbol{m} = \frac{4\pi}{3}\sigma_0 \boldsymbol{\omega} a^4=\frac{1}{3}e\boldsymbol{\omega}a^2$，电磁场角动量  
$$
\boldsymbol{L} = \int \boldsymbol{r} \times \boldsymbol{g} \,\mathrm{d}V =  \int \boldsymbol{r} \times (\epsilon_0 \boldsymbol{E} \times \boldsymbol{B}) \,\mathrm{d}V
$$
由于球内 $E=0$，角动量只存在于球外，计算动量部分：  
$$\boldsymbol{E} \times \boldsymbol{B} = \left( \frac{e}{4\pi\epsilon_0 r^2} \hat{\boldsymbol{r}} \right) \times \left( \frac{\mu_0}{4\pi r^3} [- \boldsymbol{m}] \right) = \frac{\mu_0 e}{16\pi^2 \epsilon_0 r^5} (\boldsymbol{m} \times \hat{\boldsymbol{r}})$$
所以，被积函数的矢量部分是： 
$$\hat{\boldsymbol{r}} \times (\boldsymbol{m} \times \hat{\boldsymbol{r}}) = \boldsymbol{m}(\hat{\boldsymbol{r}} \cdot \hat{\boldsymbol{r}}) - \hat{\boldsymbol{r}}(\hat{\boldsymbol{r}} \cdot \boldsymbol{m}) = \boldsymbol{m} - \hat{\boldsymbol{r}}(\hat{\boldsymbol{r}} \cdot \boldsymbol{m})$$
代入到求解角动量的积分得到
$$
\boldsymbol{L} = \frac{\mu_0 e}{16\pi^2} \int_{a}^{\infty} \frac{1}{r^4} r^2\, \mathrm{d}r \int_{\Omega} [\boldsymbol{m} - \hat{\boldsymbol{r}}(\hat{\boldsymbol{r}} \cdot \boldsymbol{m})]\, \mathrm{d}\Omega
$$
拆解该积分当中的每一项有：  
$$
\int_{a}^{\infty} r^{-2} \, \mathrm{d}r = \frac{1}{a}
$$
$$
\int \boldsymbol{m} \,\mathrm{d}\Omega = 4\pi \boldsymbol{m}
$$
$$
\int \hat{\boldsymbol{r}}(\hat{\boldsymbol{r}} \cdot \boldsymbol{m})\,\mathrm{d}\Omega =\int (\mathsf{I} \cdot \boldsymbol{m}) \,\mathrm{d}\Omega
= \frac{4\pi}{3} \boldsymbol{m}
$$
所以最终得到旋转球壳的场角动量为：
$$
\boldsymbol{L} = \frac{\mu_0 e}{16\pi^2} \cdot \frac{1}{a} \cdot \frac{8\pi}{3} \boldsymbol{m} = \frac{\mu_0 e}{6\pi a} \boldsymbol{m}
={\frac{\mu_0 e^2 a}{18\pi} \boldsymbol{\omega}}
$$


### 3.2.3 
通常在经典模型中，由于 $\omega a \ll c$ 的预期，磁能项 $W_M$ 远小于静电能 $W_E$。我们先忽略 $W_M$：

由 $W \approx \frac{e^2}{8\pi\epsilon_0 a} = m_e c^2$ 得 $a = \frac{e^2}{8\pi\epsilon_0 m_e c^2}$ (即经典电子半径)；由角动量公式 $\frac{\mu_0 e^2 a \omega}{18\pi} = \frac{\hbar}{2}$ 得 $\omega = \frac{9\pi \hbar}{\mu_0 e^2 a}$。以及
$$v = \omega a = \frac{9\pi \hbar}{\mu_0 e^2} = \frac{9\pi \hbar \epsilon_0 c^2}{e^2}$$
利用精细结构常数 $\alpha = \frac{e^2}{4\pi\epsilon_0 \hbar c} \approx \frac{1}{137}$，上式可改写为：
$$v = \frac{9}{4 \alpha} c \approx \frac{9 \times 137}{4} c \approx {308 c}$$
这个速度远远超越了光速，是没有意义的，回过头来再用 $W\approx W_M =  \frac{\mu_0 e^2 \omega^2 a}{36\pi} = m_e c^2$ 也没什么意义。另外，据说将电子视为刚体，通过转动惯量来计算角动量，也会得到类似的结论（得到赤道角速度为一百多倍光速）。


# 4 HW 5思考题  
## 4.1 
$$
\Delta s'^2 = g^{\alpha\beta}\mathrm{d}x'_\alpha\mathrm{d}x'_\beta 
= g^{\rho\sigma} \mathrm{d}x_\rho\mathrm{d}x_\sigma 
= g^{\rho\sigma}\Lambda_\rho{}^\alpha \Lambda_\sigma{}^\beta \mathrm{d}x_\alpha\mathrm{d}x_\beta
$$
$$
\implies  g^{\alpha\beta} = g^{\rho\sigma}\Lambda_\rho{}^\alpha \Lambda_\sigma{}^\beta 
$$
$$
\Lambda^\gamma{}_\beta \Lambda_\gamma{}^\alpha =g^{\gamma\mu} g_{\beta\nu} \Lambda_\mu{}^{\nu} \Lambda_\gamma{}^\alpha = g_{\beta\nu}g^{\nu\alpha} = \delta^\alpha_\beta
$$
## 4.2 SO(3)
令矩阵为 $J = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix}$，注意到 $J^2 = \begin{pmatrix} -1 & 0 \\ 0 & -1 \end{pmatrix} = -I_{2 \times 2}$，$J^3 = -J$，$J^4 = I_{2 \times 2}$，所以利用泰勒级数展开：
$$
e^{-\theta J} = I - \theta J + \frac{\theta^2}{2!} J^2 - \frac{\theta^3}{3!} J^3 + \dots = (\cos\theta) I - (\sin\theta) J = \begin{pmatrix} \cos\theta & \sin\theta \\ -\sin\theta & \cos\theta \end{pmatrix}
$$
所以
$$
\Lambda(\theta) = \begin{pmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & \cos\theta & \sin\theta \\ 0 & 0 & -\sin\theta & \cos\theta \end{pmatrix}
$$
因为 $[K, K] = 0$：
$$
\Lambda(\theta_1)\Lambda(\theta_2) = e^{-\theta_1 K} \circ e^{-\theta_2 K} = e^{-(\theta_1 + \theta_2)K + \frac{1}{2}[-\theta_1K, -\theta_2K] + \cdots} = \Lambda(\theta_1 + \theta_2)
$$
证明完毕。
## 4.3 $SO(1,3)^\uparrow$
令 $k_x = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}$，根据 $\Lambda_x = e^{\xi \Omega_x}$ 可以得到其 $Lie$ 群表示, 注意到 $k_x^2=I_{2\times 2}$ :
$$
 \begin{aligned}
\Lambda_{x}(\xi)  =\mathrm{e}^{\xi k_{x}}
&=\sum_{n=0}^{\infty} \frac{\xi^{n} k_{x}^{n}}{n!}=\sum_{n=0}^{\infty} \frac{\xi^{2 n}}{(2 n)!} \underbrace{k_{x}^{2 n}}_{=1}+\sum_{n=0}^{\infty} \frac{\xi^{2 n+1}}{(2 n+1)!} \underbrace{k_{x}^{2 n+1}}_{=k_{x}} \\
& =\left(\sum_{n=0}^{\infty} \frac{\xi^{2 n}}{(2 n)!}\right) I+\left(\sum_{n=0}^{\infty} \frac{\xi^{2 n+1}}{(2 n+1)!}\right) k_{x} \\ \\
& =\left(\begin{array}{cc}
\cosh (\xi) & 0 \\
0 & \cosh (\xi)
\end{array}\right)+\left(\begin{array}{cc}
0 & \sinh (\xi) \\
\sinh (\xi) & 0
\end{array}\right) \\ \\
& =\left(\begin{array}{cc}
\cosh (\xi) & \sinh (\xi) \\
\sinh (\xi) & \cosh (\xi)
\end{array}\right)
\end{aligned}
$$
即 :
$$
\Lambda_x(\phi) = \left(\begin{array}{cc}
\mathrm{ch} \xi & \mathrm{sh} \xi & &\\
\mathrm{sh} \xi & \mathrm{ch} \xi & & \\
& & 1 & \\
& & & 1
\end{array}\right)
$$
同样的逻辑，因为生成元矩阵 $\Omega$ 与其自身对易：
$$
\Lambda(\xi_1)\Lambda(\xi_2) = e^{-\xi_1 \Omega} e^{-\xi_2 \Omega} = e^{-(\xi_1 + \xi_2)\Omega} = \Lambda(\xi_1 + \xi_2)
$$
这也反映了沿同一方向的两个洛伦兹提升，其快度是直接相加的。

## 4.4 
对于 $O(1,3)$ 群元 $\Lambda_1, \Lambda_2$： 
$$
\Lambda^T g \Lambda = g
$$
- 验证群的封闭性。
$$
\Lambda^T g \Lambda = (\Lambda_1 \Lambda_2)^T g (\Lambda_1 \Lambda_2) 
= \Lambda_2^T (\Lambda_1^T g \Lambda_1) \Lambda_2
=\Lambda_2^T g \Lambda_2
=g
$$
所以 $\Lambda_1 \Lambda_2 \in O(3,1)$。  

- 验证群的逆元存在性。

首先确定 $\Lambda$ 是可逆的。对定义式 $\Lambda^T \eta \Lambda = \eta$ 两边取行列式：
$$
\det(\Lambda^T) \det(\eta) \det(\Lambda) = \det(\eta)
$$
由于 $\det(\eta) \neq 0$（其值为 $-1$），且 $\det(\Lambda^T) = \det(\Lambda)$，可得：
$$
(\det\Lambda)^2 = 1 \implies \det\Lambda = \pm 1
$$
行列式不为 0，说明 $\Lambda$ 必定存在逆矩阵 $\Lambda^{-1}$。  

在等式 $\Lambda^T \eta \Lambda = \eta$ 左边乘以 $(\Lambda^T)^{-1}$，右边乘以 $\Lambda^{-1}$：
$$
LHS = (\Lambda^T)^{-1} (\Lambda^T g \Lambda) \Lambda^{-1} = g = RHS =  (\Lambda^T)^{-1} g \Lambda^{-1} =(\Lambda^{-1})^T g \Lambda^{-1}
$$
因此 $\Lambda^{-1} \in O(3,1)$。
## 4.5 
### 4.5.1 
成立

1. 封闭性（乘法）：
    - 如果 $\Lambda_1, \Lambda_2 \in SO(1,3)^\uparrow$，那么他们的行列式均为 1，则 $\det(\Lambda_1\Lambda_2) = \det\Lambda_1 \det\Lambda_2 = 1 \times 1 = 1$。
    - 对于性质 $\Lambda^0{}_0 \ge 1$，两个正规变换的乘积依然是正规的（这可以通过柯西-施瓦茨不等式证明，见后续 [[EMD26/T#3.5.3 若 $ Lambda_1, Lambda_2$ 满足 $( Lambda_1) 0_0 ge 1$ 且 $( Lambda_2) 0_0 ge 1$，则它们的乘积 $ Lambda = Lambda_1 Lambda_2$ 的分量 $ Lambda 0_0$ 也必然满足 $ Lambda 0_0 ge 1$。\|#3.5.3 若 $ Lambda_1, Lambda_2$ 满足 $( Lambda_1) 0_0 ge 1$ 且 $( Lambda_2) 0_0 ge 1$，则它们的乘积 $ Lambda = Lambda_1 Lambda_2$ 的分量 $ Lambda 0_0$ 也必然满足 $ Lambda 0_0 ge 1$。]]）。
    - 因此，乘积依然属于该子集。
2. 逆元存在性：
    - 如果 $\det\Lambda = 1$，则 $\det(\Lambda^{-1}) = 1$。
    - 对于性质 $\Lambda^0{}_0 \ge 1$，$\Lambda_0{}^0 = g_{0\alpha}g^{0\beta}\Lambda^\alpha{}_\beta=g_{00}g^{00}\Lambda^0{}_0=\Lambda^0{}_0\geq1$。
    - 因此，逆元依然属于该子集。

### 4.5.2 

不成立。

除了包含单位矩阵的分支 $SO(1,3)^\uparrow$ 以外，其余三个子集均不构成群。比如，假设我们取子集 $\Sigma_i = \mathcal{P} SO(1,3)^\uparrow ,~( \det=-1, \Lambda^0{}_0 \ge 1 )$，选取 $\Lambda_1,\Lambda_2 \in \Sigma_i$，则 $\det \Lambda_1 = \det \Lambda_2 = -1$，它们的乘积 $\Lambda_1 \Lambda_2$ 的行列式为 $(-1) \times (-1) = 1$，落回了单位分支 $SO(1,3)^\uparrow$ 中。


#### 3.5.3 若 $\Lambda_1, \Lambda_2$ 满足 $(\Lambda_1)^0{}_0 \ge 1$ 且 $(\Lambda_2)^0{}_0 \ge 1$，则它们的乘积 $\Lambda = \Lambda_1 \Lambda_2$ 的分量 $\Lambda^0{}_0$ 也必然满足 $\Lambda^0{}_0 \ge 1$。
对于任何 $\Lambda \in O(3,1)$，取 $\Lambda^T g \Lambda = g$ 的00分量得：
$$
(\Lambda^0{}_0)^2 - \sum_{i=1}^3 (\Lambda^0{}_i)^2 = 1 \implies (\Lambda^0{}_0)^2 = 1 + \sum_{i=1}^3 (\Lambda^0{}_i)^2 \geq 1
$$
所以，可以定义对于 $SO(1,3)^\uparrow$ 群元，$\Lambda^0{}_0 \ge 1$ 。

令 $\vec{a}=(~(\Lambda_1)^0{}_1, (\Lambda_1)^0{}_2, (\Lambda_1)^0{}_3~)$，$\vec{b}=(~(\Lambda_2)^1{}_0, (\Lambda_2)^2{}_0, (\Lambda_2)^3{}_0~)$ 其模长满足：
$$
|\vec{a}|^2 = \sum_{i=1}^3 ((\Lambda_1)^0{}_i)^2 = ((\Lambda_1)^0{}_0)^2 - 1
,\quad
|\vec{b}|^2 = \sum_{i=1}^3 ((\Lambda_2)^i{}_0)^2 = ((\Lambda_2)^0{}_0)^2 - 1
$$
又，乘积矩阵 $\Lambda = \Lambda_1 \Lambda_2$ 的左上角元素为：
$$
\Lambda^0{}_0 = (\Lambda_1)^0{}_\mu (\Lambda_2)^\mu{}_0 = (\Lambda_1)^0{}_0 (\Lambda_2)^0{}_0 + \sum_{i=1}^3 (\Lambda_1)^0{}_i (\Lambda_2)^i{}_0=(\Lambda_1)^0{}_0 (\Lambda_2)^0{}_0 + \vec{a} \cdot \vec{b}
$$
根据柯西-施瓦茨不等式 $|\vec{a} \cdot \vec{b}| \le |\vec{a}| |\vec{b}|$，有：
$$
(\Lambda_1)^0{}_0 (\Lambda_2)^0{}_0 - \Lambda^0{}_0 \leq |\Lambda^0{}_0 - (\Lambda_1)^0{}_0 (\Lambda_2)^0{}_0 | = |\vec{a} \cdot \vec{b}| \leq |\vec{a}| |\vec{b}|
\implies
\Lambda^0{}_0 \ge (\Lambda_1)^0{}_0 (\Lambda_2)^0{}_0 - |\vec{a}| |\vec{b}|
$$

代入刚才的模长公式：  
$$
\Lambda^0{}_0 \ge (\Lambda_1)^0{}_0 (\Lambda_2)^0{}_0 - \sqrt{((\Lambda_1)^0{}_0)^2 - 1} \sqrt{((\Lambda_2)^0{}_0)^2 - 1}
\triangleq xy - \sqrt{x^2 - 1}\sqrt{y^2 - 1},\quad x, y \ge 1
$$
因为  
$$
\begin{align} 
(\sqrt{x^2 - 1}\sqrt{y^2 - 1})^2
&=
x^2y^2 - y^2 - x^2 +1 
\leq
x^2y^2 - 2xy +1
=
(xy-1)^2
\end{align}
$$

所以总是有 $xy \ge \sqrt{x^2 - 1}\sqrt{y^2 - 1} + 1$，因此 $\Lambda^0{}_0 \ge 1$。


### 4.5.3 
当一个粒子在它的瞬时共动参考系（Momentarily Comoving Reference Frame，MCRF）中感受到的固有加速度 $a$ 为常数时，它在实验室坐标系下的运动轨迹并不是抛物线，而是双曲线。  

首先，力 $F$ 定义为动量的变化率：
$$
F = \frac{\mathrm{d}p}{\mathrm{d} t}= \frac{\mathrm{d}}{\mathrm{d}t}(m\gamma v)
$$
在 MCRF 中，物体感受到的力满足由牛二定律 $F = ma$。所以有：
$$
ma = \frac{\mathrm{d}}{\mathrm{d}t}(m\gamma v) \implies a = \frac{\mathrm{d}}{\mathrm{d}t}(\gamma v)
$$
其中 $\frac{ \mathrm{d} v }{ \mathrm{d} t}$ 是实验系测得的加速度。设 $t=0$ 时，$v=0$，对运动方程进行积分： 
$$
\frac{v}{\sqrt{1-v^2/c^2}} = at \implies v(t) = \frac{at}{\sqrt{1 + (at/c)^2}}
$$
世界线即轨迹 $x(t)$。对速度 $v(t) = \frac{dx}{dt}$ 再次积分。设 $t=0$ 时，$x =0$：
$$
x(t)
= \int_0^t \frac{at'}{\sqrt{1 + (at'/c)^2}} \,\mathrm{d}t' = \frac{c^2}{a} \sqrt{1 + \left(\frac{at}{c}\right)^2} - \frac{c^2}{a}
$$
改写上述方程，可以得到 $x$ 和 $t$ 的双曲线关系：
$$
\left( x+\frac{c^2}{a} \right)^2 - (ct)^2 = \left(\frac{c^2}{a}\right)^2
$$










