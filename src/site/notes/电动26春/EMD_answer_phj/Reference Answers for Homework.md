---
{"dg-publish":true,"permalink":"/电动26春/EMD_answer_phj/Reference Answers for Homework/","noteIcon":"default","created":"2026-03-25T12:05:16.502+08:00","updated":"2026-03-25T12:10:47.114+08:00"}
---


# HW 1 %

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/电动26春/EMD_answer_phj/HW1 Answer/#" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">

<div class="markdown-embed-title">

# HW1 Answer

</div>


# 补充题 %
- 证明等式一

$
\begin{align} 
\text{LHS} &= \boldsymbol{b} \cdot (-\mathsf{I}\times \boldsymbol{a}) = -\boldsymbol{b} \times \boldsymbol{a}
= \boldsymbol{a} \times \boldsymbol{b}
\\[8pt]
&=
\boldsymbol{a} \times \mathsf{I} \cdot \boldsymbol{b} = \text{RHS}
\end{align}
$
- 证明等式二 

$
\begin{align} 
\text{LHS} &=
(\boldsymbol{a}\times \mathsf{I}) \cdot (\mathsf{I} \times \boldsymbol{a}) \\[3pt]
&= \boldsymbol{a}\times \left[ \mathsf{I} \cdot (\mathsf{I} \times \boldsymbol{a}) \right] \\[3pt]
&= \boldsymbol{a}\times \mathsf{I} \times \boldsymbol{a} \\[3pt]
&=
(\epsilon_{ijk} a_i \delta_{jn}\hat e_k \hat e_n) \times a_m \hat e_m = \epsilon_{ijk}\epsilon_{nml} \delta_{jn} a_ia_m \hat{e}_k \hat{e_l}
= -\epsilon_{nik}\epsilon_{nml} a_ia_m \hat{e}_k\hat{e}_l
\\[3pt]
&= - \left[ a_ma_m \hat e_k \hat a_l - a_la_k \hat e_k \hat a_l \right] \\[3pt]
&=\text{RHS}
\end{align}
$




</div></div>
  

# HW 2%  

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/电动26春/EMD_answer_phj/HW2 Answer/#2" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">

<div class="markdown-embed-title">

# HW2 Answer

</div>


# 2 补充题   
## 2.1 Kinetic helicity  
对于给定的流速矢量 $\boldsymbol{v} = (\ln s) \hat{z}$，在柱坐标系 $(s, \phi, z)$ 下，
$\begin{align}
\nabla \times \boldsymbol{v}
&=
\frac{1}{s} \begin{vmatrix} \hat s & s \hat \phi & \hat z \\ \partial_s & \partial_\phi &  \partial_z \\ v_s & sv_\phi & v_z \end{vmatrix}
\\[4pt]
&= \left( 0 - 0 \right) \hat{s} + \left( 0 - \frac{\partial \ln s}{\partial s} \right) \hat{\phi} + 0 \hat{z} \\[4pt]
&= -\frac{1}{s} \hat{\phi}
\end{align}$
所以 $\boldsymbol{A} = \boldsymbol{v} \times (\nabla \times \boldsymbol{v})$ 得
$\begin{align}
\boldsymbol{A} 
= (\ln s \hat{z}) \times \left( -\frac{1}{s} \hat{\phi} \right) = \frac{\ln s}{s} \hat{s}
\end{align}
$
其散度为
$\begin{align}
\nabla \cdot \boldsymbol{A} 
= \frac{1}{s} \frac{\partial (s A_s)}{\partial s} + \frac{1}{s} \frac{\partial A_\phi}{\partial \phi} + \frac{\partial A_z}{\partial z} 
= \frac{1}{s} \frac{\partial}{\partial s} \left( s \cdot \frac{\ln s}{s} \right) + 0 + 0 
= \frac{1}{s} \cdot \frac{1}{s} = \frac{1}{s^2}
\end{align}$
旋度为 
$\begin{align}
\nabla \times \boldsymbol{A}  = 0
\end{align}
$

## 2.2 Electrostatic field  
直接计算散度为  
$
\begin{align} 
\nabla \cdot \boldsymbol{E}
&=
\nabla \cdot  \frac{1}{4\pi \epsilon_0} \int \mathrm{d}V' \, \frac{{\rho' \hat{\mathbb{R}}}}{\mathbb{R}^2} \\[4pt]
&=\frac{1}{4\pi \epsilon_0} \int \mathrm{d}V' \, \rho'  \nabla \cdot   \frac{{\hat{\mathbb{R}}}}{\mathbb{R}^2}  \\[4pt]
&=\frac{1}{\epsilon_0} \int \mathrm{d}V' \, \rho' \delta^3(\mathbb{R})  \\[4pt]
&= \frac{\rho}{\epsilon_0}
\end{align}
$
直接计算旋度为  
$
\begin{align} 
\nabla \times \boldsymbol{E}
&=
\nabla \times  \frac{1}{4\pi \epsilon_0} \int \mathrm{d}V' \, \frac{{\rho' \hat{\mathbb{R}}}}{\mathbb{R}^2} \\[4pt]
&=\frac{1}{4\pi \epsilon_0} \int \mathrm{d}V' \, \rho'  \nabla \times  \frac{{\hat{\mathbb{R}}}}{\mathbb{R}^2}  \\[4pt]
&=0
\end{align}
$
## 2.3 Duality invariance  
- method 1

定义 Riemann-Silberstein 矢量  
$
\boldsymbol{F} = \boldsymbol{E} + \mathrm{i}c \boldsymbol{B}
$
则自由场的 Maxwell 方程组可以写作
$
\mathrm{i}\frac{1}{c}\frac{\partial \vec{F}}{\partial t} = \nabla \times \vec{F},
\quad \nabla \cdot \vec{F} = 0
$
而题中的变换可以表示为  
$
\boldsymbol{F} \to \boldsymbol{F}' = e^{-\mathrm{i}\theta} \boldsymbol{F}
$
可以看出这个多出来的因子 $e^{-\mathrm{i}\theta}$ 能直接挪到 Maxwell 方程组外边，不会影响方程的形式。  

- method 2

题中的变换也可以表示为电磁张量 $F^{\mu\nu}$ 及其对偶张量 $\tilde{F}^{\mu\nu}$ 的线性组合  
$
F'^{\mu\nu} = F^{\mu\nu}\cos\theta + \tilde{F}^{\mu\nu}\sin\theta
$
后面(应该)会学到，自由场的 Maxwell 方程组等价于  
$
\partial_\mu F^{\mu\nu} = \partial_\mu \tilde{F}^{\mu\nu} = 0
$
显然上述的变换不会改变 4-形式的 Maxwell 方程组。

</div></div>
  


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/电动26春/EMD_answer_phj/HW2 Answer/#3" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">

<div class="markdown-embed-title">

# HW2 Answer

</div>


# 3 思考题  
## 3.1 
这个张量怎么有点眼熟，算电磁和引力辐射时貌似会用到
### 3.1.1 
$
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
$
### 3.1.2 
在旋转变换下，向量 $n_i$ 变为 $n'_i = R_{ik} n_k$，所以
$
\begin{align} 
T'_{ij} 
&= \oint (R_{ik} n_k) (R_{jl} n_l) \,\mathrm{d}\Omega = R_{ik} R_{jl} \oint n_k n_l d\Omega  \\[4pt]
&=  R_{ik} R_{jl} T_{kl}
\end{align}
$
### 3.1.3 
见 ppt，$C = \frac{4\pi}{3}$  

### 3.1.4 
第一个利用 $\mathrm{d}\Omega = \sin\theta \mathrm{d}\theta\mathrm{d}\phi$ 即可。  

第二个，根据对称性，可以直接算 z 方向计算： $=\iint \frac{z}{r}\sin\theta \mathrm{d}\theta\mathrm{d}\phi=\iint \frac{r\cos\theta}{r}\sin\theta \mathrm{d}\theta\mathrm{d}\phi =0$

第三个，看讲义  

第四个，被积函数是奇函数，结果为零

第五个，积分结果必须是 $SO(3)$ 下的不变张量，且阶数为四，它必须由克罗内克符号 $\delta$ 组合而成。所有可能的配对方式只有三种：
$
\oint n_i n_j n_k n_l \,\mathrm{d}\Omega = C (\delta_{ij}\delta_{kl} + \delta_{ik}\delta_{jl} + \delta_{il}\delta_{jk})
$
注意，由于 $n_i n_j n_k n_l$ 对索引 $i, j, k, l$ 的任意排列都是全对称的，所以这三项前的系数 $C$ 必须相等。先做两次缩并，左边：  
$
\oint (n_i n_i) (n_k n_k)\,\mathrm{d}\Omega = \oint 1 \cdot 1 \, \mathrm{d}\Omega  = 4\pi
$
右边：  
$
(\delta_{ii}\delta_{kk} + \delta_{ik}\delta_{ik} + \delta_{ik}\delta_{ik}) = 9+3+3 = 15
$
所以 $C=\frac{4\pi}{15}$.  

## 3.2 
略  

## 3.3 
用柱坐标爆算，注意：
$
\boldsymbol{E} = \frac{e}{4\pi\varepsilon_0} \frac{\gamma \boldsymbol{R}}{[s^2 + \gamma^2(z-vt)^2]^{3/2}}
$
剩下的懒得写了。




</div></div>








