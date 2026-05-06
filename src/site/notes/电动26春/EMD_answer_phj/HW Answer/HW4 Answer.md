---
{"dg-publish":true,"permalink":"/电动26春/EMD_answer_phj/HW Answer/HW4 Answer/","noteIcon":"default","created":"2026-03-27T23:31:18.902+08:00","updated":"2026-04-07T16:45:02.966+08:00","dg-note-properties":{}}
---

[[电动26春/EMD_answer_phj/HW Answer/HW5 Answer\|HW5 Answer]]

![zz_figure/Pasted image 20260328123830.png](/img/user/zz_figure/Pasted%20image%2020260328123830.png)  
![zz_figure/Pasted image 20260328123845.png](/img/user/zz_figure/Pasted%20image%2020260328123845.png)  
![zz_figure/Pasted image 20260328123900.png](/img/user/zz_figure/Pasted%20image%2020260328123900.png)  

# 1 补充题  
## 1.1 
已知能量和动量密度满足   
$$
\begin{align} 
w&= \frac{1}{2}\left( \epsilon_0E^2 + \frac{B^2}{\mu_0} \right) \geq \sqrt{\frac{\epsilon_0}{\mu_0}} EB, \quad{仅当\epsilon_0E^2 + \frac{B^2}{\mu_0}时取等号}
\\[4pt]
cg&= \frac{P}{c} = \sqrt{\frac{\epsilon_0}{\mu_0}} |\boldsymbol{E} \times \boldsymbol{B} | \leq  \sqrt{\frac{\epsilon_0}{\mu_0}} EB, \quad{仅当\boldsymbol{E} \perp \boldsymbol{B}时取等号}
\end{align}
$$
所以当局部每一点均成立 $\boldsymbol{E} \perp \boldsymbol{B}$, $E=cB$, 且 $\boldsymbol{g}$ 方向不变时, 对全空间积分得到 $W = cG$。  
## 1.2 
以中点为原点，连线为z轴建立柱坐标系，电荷坐标 $(0,0,\pm a)$，则中垂面上任意一点的电场沿着柱坐标 $\hat{s}$ 方向
$$
E_s = 2 \cdot \frac{q}{4\pi\epsilon_0 {s^2+a^2}} \cdot \frac{s}{\sqrt{s^2+a^2}} = \frac{q}{2\pi\epsilon_0} \frac{s}{ ({s^2+a^2})^{3/2}}
$$
考虑上半平面受到的作用力，$\hat{n} = -\hat{e}_z$，所以  
$$
F_z = \oint_{z=0} \mathrm{d}\boldsymbol{\sigma} \cdot \mathsf{T} = - \int_0^\infty 2\pi s \,\mathrm{d}s\, T_{zz}
$$
其中  
$$
T_{zz} = \epsilon_0 \left( E_zE_z - \frac{1}{2}\delta_{zz} E^2 \right) = \frac{q^2}{8\pi^2\epsilon_0} \frac{s^2}{ ({s^2+a^2})^{3}}
$$
所以  
$$
\begin{align} 
F_z  &= \int_0^{+\infty}  \frac{q^2}{4\pi\epsilon_0} \frac{s^3}{ ({s^2+a^2})^{3}} \,\mathrm{d}s \\[4pt]
{\color{gray} u = s^2 +a^2 \to}
&=\frac{q^2}{8\pi\epsilon_0} \int_{a^2}^{+\infty}  \frac{{u-a^2}}{u^3} \,\mathrm{d}u \\[4pt]
&=-\frac{q^2}{8\pi\epsilon_0} \left.\left[ -\frac{1}{u} + \frac{a^2}{2u^2} \right] \right|_{a^2}^{\infty} \\[4pt]
&=\frac{q^2}{4\pi \epsilon_0 (2a)^2}
\end{align}
$$

# 2 思考题  
## 2.1 磁偶极子/带电旋转球
### 2.1.1 
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
### 2.1.2 
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
### 2.1.3 
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
## 2.2 电子经典球壳模型
### 2.2.1 
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

### 2.2.2 
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


### 2.2.3 
通常在经典模型中，由于 $\omega a \ll c$ 的预期，磁能项 $W_M$ 远小于静电能 $W_E$。我们先忽略 $W_M$：

由 $W \approx \frac{e^2}{8\pi\epsilon_0 a} = m_e c^2$ 得 $a = \frac{e^2}{8\pi\epsilon_0 m_e c^2}$ (即经典电子半径)；由角动量公式 $\frac{\mu_0 e^2 a \omega}{18\pi} = \frac{\hbar}{2}$ 得 $\omega = \frac{9\pi \hbar}{\mu_0 e^2 a}$。以及
$$v = \omega a = \frac{9\pi \hbar}{\mu_0 e^2} = \frac{9\pi \hbar \epsilon_0 c^2}{e^2}$$
利用精细结构常数 $\alpha = \frac{e^2}{4\pi\epsilon_0 \hbar c} \approx \frac{1}{137}$，上式可改写为：
$$v = \frac{9}{4 \alpha} c \approx \frac{9 \times 137}{4} c \approx {308 c}$$
这个速度远远超越了光速，是没有意义的，回过头来再用 $W\approx W_M =  \frac{\mu_0 e^2 \omega^2 a}{36\pi} = m_e c^2$ 也没什么意义。另外，据说将电子视为刚体，通过转动惯量来计算角动量，也会得到类似的结论（得到赤道角速度为一百多倍光速）。






