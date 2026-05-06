---
{"dg-publish":true,"permalink":"/A_symmetry_自然界的对称性/Applications/ED Formulas/","noteIcon":"default","created":"2026-05-05T22:59:56.629+08:00","updated":"2026-05-06T12:25:09.068+08:00"}
---


# Symbol Convention%  
- In accordance with _ISO 80000-2_, the following font conventions are employed:
	- Scalars and components for vectors or tensors are represented by lightface italic type ($a, \phi, a_i, T_{ij}$).
	- Vectors are represented by boldface italic type ($\boldsymbol{a}, \boldsymbol{\omega}$).
	- Second-order tensors are represented by boldface sans-serif type ($\mathsf{T}, \mathsf{I}$).
- Operators & Constants: Roman (upright) type is used for fixed mathematical constants (e.g., Pi $\mathrm{\pi}$, the imaginary unit $\mathrm{i}$) and differential operators (e.g., the differential $\mathrm{d}$ in $\mathrm{d}x$).
- Calculus Notation: For integrals, a thin space (`\,`) is used to separate the integrand from the differential operator, e.g., $\int f(x) \, \mathrm{d}x$.
- Minkowski Metric: The Minkowski metric tensor $\eta_{\mu\nu}$ is defined using the _mostly-plus_ signature convention:
$$
\eta_{\mu\nu} = \operatorname{diag}(-1, +1, +1, +1)
$$
Consequently, the invariant spacetime interval is given by $ds^2 = -c^2dt^2 + dx^2 + dy^2 + dz^2$.

# 1 Preparatory Math.   
## 1.1 Vector and tensor analysis (Euclidean geometry)  
### 1.1.1 Basics  
- Kronecker & Levi-Civita symbols
$$
\delta_{ij} = \hat{e}_i \cdot \hat{e}_j, \quad \epsilon_{ijk} = (\hat{e}_i \times \hat{e}_j) \cdot \hat{e}_k \Leftrightarrow \hat{e}_i \times \hat{e}_j = \epsilon_{ijk} \hat{e}_k
$$
- Determinant
$$
\epsilon_{lmn}\det \mathsf{A_{3\times 3}} = \epsilon_{ijk}A_{il}A_{jm}A_{kn} = \epsilon_{ijk}A_{li}A_{mj}A_{nk} 
$$
$$
\implies 
\det \mathsf{A}_{3\times 3} = \frac{1}{6} \epsilon_{ijk} \epsilon_{lmn} A_{il} A_{jm} A_{kn}
\quad \text{or} \quad
\det \mathsf{A}_{3\times 3} = \epsilon_{ijk} A_{i1} A_{j2} A_{k3} = \epsilon_{ijk} A_{1i} A_{2j} A_{3k} 
$$

- Contraction identities
$$
\epsilon_{ijk}\epsilon_{imn}=\delta_{jm}\delta_{kn}-\delta_{jn}\delta_{km}, 
\quad  \epsilon_{ijk} \epsilon_{ij n} = 2\delta_{kn},
\quad  \epsilon_{ijk} \epsilon_{ijk} = 3! = 6 
$$
> [!info] More generally*
> $$
\epsilon_{ijk} \epsilon_{lmn} = \det\begin{pmatrix}
\delta_{il} & \delta_{im} & \delta_{in} \\
\delta_{jl} & \delta_{jm} & \delta_{jn} \\
\delta_{kl} & \delta_{km} & \delta_{kn}
\end{pmatrix}
> $$
> High-dimensional case:  
> $$  
> \epsilon_{i_1i_2\cdots i_n} \epsilon_{j_1j_2\cdots j_n} = \det\begin{pmatrix}
\delta_{i_1j_1} & \delta_{i_1j_2} & \cdots & \delta_{i_1j_n} \\
\delta_{i_2j_1} & \delta_{i_2j_2} & \cdots & \delta_{i_2j_n} \\
\vdots & \vdots & \ddots & \vdots \\
\delta_{i_nj_1} & \delta_{i_nj_2} & \cdots & \delta_{i_nj_n}
\end{pmatrix} \triangleq \delta_{i_1 i_2 \dots i_n}^{j_1 j_2 \dots j_n} \,\text{(Generalized Kronecker delta)}
> $$
- Axial Vector / Pseudovector
$$
A_{i}' = \det(\mathsf{R}) R_{ij} A_i, \quad \mathsf{R} \in O(3)
$$
- Symmetric-Antisymmetric decomposition
$$
T_{ij} = T_{(ij)} + T_{[ij]} = \frac{{T_{ij} + T_{ji}}}{2} +  \frac{{T_{ij} - T_{ji}}}{2}
$$
- Double Contraction (adopt to the proximity rule)
$$
\mathsf{A} : \mathsf{B} \triangleq A_{ij} B_{ji} = \operatorname{tr}(\mathsf{A} : \mathsf{B})
$$
### 1.1.2 Cross & dot product
- Scalar Triple product
$$
\boldsymbol{a}\cdot (\boldsymbol{b}\times \boldsymbol{c}) = \boldsymbol{b}\cdot (\boldsymbol{c}\times \boldsymbol{a}) = \boldsymbol{c}\cdot (\boldsymbol{a}\times \boldsymbol{b})
$$
- Vector Triple product / BAC-CAB formula
$$
\boldsymbol{a}\times (\boldsymbol{b} \times \boldsymbol{c}) = \boldsymbol{b}\boldsymbol{a}\cdot \boldsymbol{c} - \boldsymbol{c}\boldsymbol{a}\cdot \boldsymbol{b}
\quad\text{or}\quad
(\boldsymbol{b} \times \boldsymbol{c})\times \boldsymbol{a} = \boldsymbol{c}\boldsymbol{a}\cdot \boldsymbol{b} - \boldsymbol{b}\boldsymbol{a}\cdot \boldsymbol{c}
$$
- Lagrange's identity
$$
(\boldsymbol{a} \times \boldsymbol{b}) \cdot (\boldsymbol{c} \times \boldsymbol{d}) = (\boldsymbol{a} \cdot \boldsymbol{c})(\boldsymbol{b} \cdot \boldsymbol{d}) - (\boldsymbol{a} \cdot \boldsymbol{d})(\boldsymbol{b} \cdot \boldsymbol{c})
$$
- Associative Law (the tensor remains centered in the contraction)
$$
\boldsymbol{a} \cdot \mathsf{T} \cdot \boldsymbol{b} = (\boldsymbol{a} \cdot \mathsf{T}) \cdot \boldsymbol{b} = \boldsymbol{a} \cdot (\mathsf{T} \cdot \boldsymbol{b})
$$
$$
\boldsymbol{a} \cdot \mathsf{T} \times \boldsymbol{b} = (\boldsymbol{a} \cdot \mathsf{T}) \times \boldsymbol{b} = \boldsymbol{a} \cdot (\mathsf{T} \times \boldsymbol{b})
$$
$$
\boldsymbol{a} \times \mathsf{T} \times \boldsymbol{b} = (\boldsymbol{a} \times \mathsf{T}) \times \boldsymbol{b} = \boldsymbol{a} \times (\mathsf{T} \times \boldsymbol{b}), \quad \mathsf{T} \in \mathbb{R}^n \otimes \mathbb{R}^n \cdots \otimes \mathbb{R}^n
$$
- Cross $\to$ Dot
$$
\boldsymbol{\omega}\times \mathsf{I} = \mathsf{I} \times \boldsymbol{\omega} 
= \begin{pmatrix} 0 & -\omega_3 & \omega_2 \\ \omega_3 & 0 &  -\omega_1 \\ -\omega_2 & \omega_1 & 0 \end{pmatrix}
\triangleq \mathsf{\Omega} 
\quad\Leftrightarrow\quad 
\mathsf{\Omega}_{ij} = \epsilon_{ikj}\omega_k 
\implies 
\boldsymbol{\omega} \times \boldsymbol{v} = \mathsf{\Omega} \cdot \boldsymbol{v}, ~\forall \boldsymbol{v} \in \mathbb{R}^n
$$
### 1.1.3 $\nabla$  
#### Differential operations 
- Coordinate Component Expansion of Differential Operators
$$
\operatorname{grad} \Phi \triangleq \hat{e}_i \partial_i \Phi
$$
$$
\operatorname{div} \boldsymbol{v} \triangleq (\hat{e}_i \partial_i) \cdot \boldsymbol{v} = \partial_i v_i
$$
$$
\operatorname{rot} \boldsymbol{v} ~ (\text{or} \operatorname{curl}) \triangleq (\hat{e}_i \partial_i) \times \boldsymbol{v} = \epsilon_{ijk} (\partial_j v_k) \hat{e}_i
= \left|\begin{matrix} \hat{e}_1 & \hat{e}_2 & \hat{e}_3 \\ \partial_1 & \partial_2 & \partial_3 \\ v_1 & v_2 & v_3 \end{matrix}\right|
$$
$$
\nabla^2  \Phi =  \nabla \cdot \nabla  \Phi = \sum_i \partial_i^2 \Phi
$$
- Two critical indentities
$$
\nabla \times\nabla  \varphi = 0,\quad \nabla \cdot (\nabla \times \boldsymbol{a}) = 0
$$
- Leibniz Rule
$$
\begin{align} 
\nabla(\varphi \psi) &= (\nabla \varphi) \psi + \varphi(\nabla \psi)
\\[5pt]
\nabla(\boldsymbol{a} \cdot \boldsymbol{b}) &= \boldsymbol{a} \cdot \nabla \boldsymbol{b} + \boldsymbol{b} \cdot \nabla \boldsymbol{a} + \boldsymbol{a} \times (\nabla \times \boldsymbol{b}) + \boldsymbol{b} \times (\nabla \times \boldsymbol{a})
\\[5pt]&\implies
\boldsymbol{a} \times (\nabla \times \boldsymbol{a}) = \frac{1}{2} \nabla (\boldsymbol{a}\cdot\boldsymbol{a}) - \boldsymbol{a}\cdot \nabla \boldsymbol{a}
\end{align}
$$
$$
\begin{align} \nabla(\varphi \boldsymbol{a}) &= (\nabla \varphi) \boldsymbol{a} + \varphi (\nabla \boldsymbol{a})  
\\[5pt]
\nabla \cdot (\varphi \boldsymbol{a}) &= (\nabla \varphi) \cdot \boldsymbol{a} + \varphi (\nabla \cdot \boldsymbol{a})
\\[5pt]
\nabla \times (\varphi \boldsymbol{a}) &= (\nabla \varphi) \times \boldsymbol{a} + \varphi (\nabla \times \boldsymbol{a})
\end{align}
$$
$$
\begin{align} 
\nabla (\boldsymbol{a} \times \boldsymbol{b}) &= (\nabla \boldsymbol{a}) \times \boldsymbol{b} - (\nabla \boldsymbol{b}) \times \boldsymbol{a}
\\[5pt]
\nabla \cdot (\boldsymbol{a} \times \boldsymbol{b}) &= (\nabla \times \boldsymbol{a}) \cdot \boldsymbol{b} - (\nabla \times \boldsymbol{b}) \cdot \boldsymbol{a}
\\[5pt]
\nabla \times (\boldsymbol{a} \times \boldsymbol{b}) &= (\nabla \cdot \boldsymbol{b} + \boldsymbol{b} \cdot \nabla) \boldsymbol{a} - (\nabla \cdot \boldsymbol{a} + \boldsymbol{a} \cdot \nabla) \boldsymbol{b}
\end{align}
$$
$$
\begin{align} 
\nabla \cdot (\varphi \mathsf{T}) &= (\nabla \varphi) \cdot \mathsf{T} + \varphi (\nabla \cdot \mathsf{T})
\\[5pt]
\nabla \cdot (\boldsymbol{a} \cdot \mathsf{T}) &= (\nabla \boldsymbol{a}) : \mathsf{T} + \boldsymbol{a} \cdot (\nabla \cdot \mathsf{T})
\end{align}
$$
$$
\begin{align} 
\nabla \cdot (\boldsymbol{a}\boldsymbol{b}) &= (\nabla \cdot \boldsymbol{a}) \boldsymbol{b} + (\boldsymbol{a} \cdot \nabla) \boldsymbol{b}
\\[5pt]
\nabla \cdot (\boldsymbol{a}\boldsymbol{b}\boldsymbol{c}) &= (\nabla \cdot \boldsymbol{a}) \boldsymbol{b}\boldsymbol{c} + (\boldsymbol{a} \cdot \nabla\boldsymbol{b}) \boldsymbol{c} + \boldsymbol{b}\boldsymbol{a}\cdot \nabla \boldsymbol{c}
\end{align} 
$$
$$
\nabla \times (\boldsymbol{a} \times \boldsymbol{b}) 
= \nabla \cdot (\boldsymbol{b}\boldsymbol{a} - \boldsymbol{a}\boldsymbol{b})
= (\nabla \cdot \boldsymbol{b}+\boldsymbol{b}\cdot\nabla)\boldsymbol{a} - (\nabla \cdot \boldsymbol{a}+\boldsymbol{a}\cdot\nabla)\boldsymbol{b}
$$
- Taylor Series in Operator Form
$$
\varphi(\boldsymbol{x}+\boldsymbol{\epsilon}) = e^{\boldsymbol{\epsilon}\cdot\nabla} \varphi(\boldsymbol{x})
= \left[ 1 + (\boldsymbol{\epsilon}\cdot\nabla) + \frac{1}{2!}(\boldsymbol{\epsilon}\cdot\nabla)^2 + \frac{1}{3!}(\boldsymbol{\epsilon}\cdot\nabla)^3 + \cdots \right] \varphi(\boldsymbol{x})
$$
here:  
$$
\frac{1}{2} (\boldsymbol{\epsilon}\cdot\nabla)(\boldsymbol{\epsilon}\cdot\nabla) \varphi(\boldsymbol{x}) = \frac{1}{2} \epsilon_i \epsilon_j \frac{\partial^2 \varphi}{\partial x_i \partial x_j},\quad
\frac{1}{6} (\boldsymbol{\epsilon}\cdot\nabla)^3 \varphi(\boldsymbol{x}) = \frac{1}{6} \epsilon_i \epsilon_j \epsilon_k \frac{\partial^3 \varphi}{\partial x_i \partial x_j \partial x_k},\quad
\cdots
$$
$T(\boldsymbol{\epsilon}) = e^{\boldsymbol{\epsilon}\cdot\nabla}$ is so-called "Translation Operator" in quantum mechanics or lie group ($\hat{T}(\boldsymbol{\epsilon}) = e^{\frac{\mathrm{i}}{\hbar} \boldsymbol{\epsilon} \cdot \hat{\boldsymbol{p}}}$).  

#### Integral operations  
- Coordinate-independent definition
$$
\mathrm{d}\varphi(\boldsymbol{r}) = \nabla \varphi \cdot \mathrm{d} \boldsymbol{l}
$$
$$
\nabla \cdot \boldsymbol{F} \triangleq \lim_{ V \to 0 } \left[ \frac{1}{V} \oint_{\partial V} \boldsymbol{F}\cdot\mathrm{d}\boldsymbol{S} \right]
$$
$$
\hat{n} \cdot (\nabla \times \boldsymbol{F}) \triangleq \lim_{ S \to 0 } \left[ \frac{1}{S} \oint_{\partial S} \boldsymbol{F}\cdot \mathrm{d}\boldsymbol{l} \right]
$$
- Fundamental theorem of gradients
$$
\int_P^Q \mathrm{d}\boldsymbol{l} \cdot \nabla \boxed{\rule{0pt}{1.5ex}\hspace{0.3em}} = \left. \boxed{\rule{0pt}{1.5ex}\hspace{0.3em}} \right|_P^Q
,\quad
\boxed{\rule{0pt}{1.5ex}\hspace{0.3em}} = \varphi, \boldsymbol{a}, \mathsf{T} , \dots
$$
$$
\implies
\oint_C \mathrm{d}\boldsymbol{l} \cdot \nabla \boxed{\rule{0pt}{1.5ex}\hspace{0.3em}} = 0 \quad\text{(conservative field)}
$$
- Generalized Gauss's Theorem
$$
\iiint_V \mathrm{d}V\, \nabla \boxed{\rule{0pt}{1.5ex}\hspace{0.3em}}  = \oint_{\partial V} \mathrm{d}\boldsymbol{\sigma} \,\boxed{\rule{0pt}{1.5ex}\hspace{0.3em}}
,\quad
\boxed{\rule{0pt}{1.5ex}\hspace{0.3em}} = \varphi, \times\boldsymbol{a}, \cdot \boldsymbol{a}, \times \mathsf{T} \dots
,\quad
\text{with}~ \mathrm{d}\boldsymbol{\sigma} = \boldsymbol{n} \, \mathrm{d}S
$$
$$
\implies \oint_{\partial V} \mathrm{d}\boldsymbol{\sigma} = 0
$$
$$
\text{also}  \implies
\nabla \boxed{\rule{0pt}{1.5ex}\hspace{0.3em}} = \lim_{ V \to 0 } \left[ \frac{1}{V} \oint_{\partial V}  \mathrm{d}\boldsymbol{\sigma} \,\boxed{\rule{0pt}{1.5ex}\hspace{0.3em}} \right]
\implies
\left\{\begin{align}
\nabla \varphi &= \lim_{ V \to 0 } \left[ \frac{1}{V} \oint_{\partial V}  \mathrm{d}\boldsymbol{\sigma} \,\varphi \right]
\\[5pt]
\nabla \cdot \boldsymbol{F} &= \lim_{ V \to 0 } \left[ \frac{1}{V} \oint_{\partial V}  \mathrm{d}\boldsymbol{\sigma} \, \cdot \boldsymbol{F} \right] \quad \text{(Classic Gauss)}
\\[5pt]
\nabla \times \boldsymbol{F} &= \lim_{ V \to 0 } \left[ \frac{1}{V} \oint_{\partial V}  \mathrm{d}\boldsymbol{\sigma} \,\times \boldsymbol{F} \right]
\end{align}\right.
$$
In Gauss's Divergence Theorem $\iiint_V \mathrm{d}V\, \nabla \cdot \boldsymbol{F}= \oint_{\partial V} \mathrm{d}\boldsymbol{\sigma}  \cdot \boldsymbol{F}$, if $\boldsymbol{F} = \varphi\nabla \psi$, one find the Green's first identity:
$$
\int_V \mathrm{d}V [\varphi\nabla^2 \psi + \nabla \varphi \cdot \nabla \psi] = \oint_{\partial V} \mathrm{d}\boldsymbol{\sigma} \cdot \varphi\nabla \psi
$$
and substituting $\boldsymbol{F} = \varphi\nabla \psi - \psi\nabla \varphi$ yields the Green's second identity:
$$
\int_V \mathrm{d}V [\varphi\nabla^2 \psi - \psi \nabla^2 \varphi] = \oint_{\partial V} \mathrm{d}\boldsymbol{\sigma} \cdot [\varphi\nabla \psi - \psi\nabla \varphi]
$$
- Generalized Stokes' Theorem
$$
\oint_S (\mathrm{d}\boldsymbol{\sigma} \times \nabla) \boxed{\rule{0pt}{1.5ex}\hspace{0.3em}} = \oint_{\partial S} \mathrm{d}\boldsymbol{l}\, \boxed{\rule{0pt}{1.5ex}\hspace{0.3em}}
,\quad
\boxed{\rule{0pt}{1.5ex}\hspace{0.3em}} = \varphi, \times\boldsymbol{a}, \cdot \boldsymbol{a}, \times \mathsf{T} \dots
$$
$$
\implies 
\oint_{\partial S} \mathrm{d}\boldsymbol{l} \cdot \boldsymbol{F}
= \oint_S (\mathrm{d}\boldsymbol{\sigma} \times \nabla)  \cdot \boldsymbol{F}
= \oint_S \mathrm{d}\boldsymbol{\sigma} \cdot (\nabla  \times \boldsymbol{F})
\quad \text{(Classic Stokes)}
$$
#### Helmholtz decomposition  
For any continuous differentiable vector field $\boldsymbol{F}$, if $\lim_{ r \to \infty } r\boldsymbol{F}(\boldsymbol{x})\to 0$,
$$
\begin{align} 
\boldsymbol{F} 
&= \underset{\text{longitudinal/irrotational part}}{\underbrace{ -\nabla \varphi}} 
+ \underset{\text{transverse/solenoidal part}}{\underbrace{\nabla \times \boldsymbol{A}}}
\\[8pt]
&= -\frac{1}{4\pi} \nabla \int \frac{{\nabla' \cdot \boldsymbol{F}(\boldsymbol{x}')}}{|\boldsymbol{x}-\boldsymbol{x}'|}\,\mathrm{d}V' + \frac{1}{4\pi} \nabla \times \int \frac{{\nabla' \times \boldsymbol{F}(\boldsymbol{x}')}}{|\boldsymbol{x}-\boldsymbol{x}'|}\,\mathrm{d}V'
\end{align}
$$
for static magnetic field, Biot-Savart Law:  
$$
\implies 
\boldsymbol{B}(\boldsymbol{x}) = \frac{1}{4\pi} \nabla \times \int \frac{{\mu_0 \boldsymbol{J}(\boldsymbol{x}')}}{|\boldsymbol{x}-\boldsymbol{x}'|}\,\mathrm{d}V'
=
\frac{\mu_0}{4\pi} \int \frac{{\boldsymbol{J}(\boldsymbol{x}') \times (\boldsymbol{x}-\boldsymbol{x}')}}{|\boldsymbol{x}-\boldsymbol{x}'|^3}\,\mathrm{d}V'
,\quad
\boldsymbol{x}:\text{field}; ~ \boldsymbol{x}':\text{source}
$$
for static electric field, Coulomb's Law  
$$
\implies
\boldsymbol{E}(\boldsymbol{x}) 
= -\frac{1}{4\pi} \nabla \int \frac{\rho(\boldsymbol{x}')/\varepsilon_0}{|\boldsymbol{x}-\boldsymbol{x}'|} \,\mathrm{d}V' 
= \frac{1}{4\pi\varepsilon_0} \int \frac{\rho(\boldsymbol{x}') (\boldsymbol{x}-\boldsymbol{x}')}{|\boldsymbol{x}-\boldsymbol{x}'|^3} \,\mathrm{d}V' 
$$
### 1.1.4 Cases  
- Determinant
$$
\det(\boldsymbol{a}\boldsymbol{b}) = 0,\quad
\det(\mathsf{I} + \boldsymbol{a}\boldsymbol{b}) = 1+\boldsymbol{a} \cdot \boldsymbol{b}
$$
- For $r=|\boldsymbol{r}|, \, \boldsymbol{r}=(x,y,z) = r_i\hat{e}_i = r \hat{r}$ & $\nabla$
$$
\nabla r = \hat{r}, \quad \nabla \boldsymbol{r} = \mathsf{I}, \quad \nabla \cdot \boldsymbol{r} = 3, \quad \nabla \times \boldsymbol{r} = 0
$$
$$
\nabla \times \hat{r} = 0, \quad \nabla \cdot \hat{r} = \frac{2}{r}, \quad \nabla \hat{r} = \frac{{\mathsf{I}-\hat{r}\hat{r}}}{r},\quad
\nabla \times [f(r)\hat{r}] = 0
$$
$$
\nabla^2 \left( -\frac{1}{r} \right) 
= \nabla \cdot \left( \frac{\hat{r}}{r^2} \right) = 4\mathrm{\pi} \delta^3(\boldsymbol{r}),~~
\nabla \frac{1}{r} = - \frac{\hat{r}}{r^2} 
,~~
\nabla \frac{\hat{r}}{r^2} = \frac{{\mathsf{I}-3\hat{r}\hat{r}}}{r^3} + \frac{4\pi\delta^3(\boldsymbol{x})}{3}\mathsf{I}
$$
- Double Contraction (adopt to the proximity rule)
$$
\mathsf{I}: \boldsymbol{a}\boldsymbol{b} = \boldsymbol{a} \cdot \boldsymbol{b}, \quad
\mathsf{I}: \nabla \boldsymbol{a} = \nabla \cdot \boldsymbol{a}
$$
- $\nabla$
$$
\nabla \cdot \varphi \mathsf{I} = \nabla \varphi
$$
$$
\nabla \cdot (\mathsf{T} \times \boldsymbol{r}) = -\boldsymbol{r} \times (\nabla \cdot \mathsf{T}) , \quad \text{with}~ T_{ij} = T_{ji}
$$
### 1.1.5 $\nabla$ in the orthogonal curvilinear coordinates   
#### Definition
In this section, we adopt $\boldsymbol{e}_i$ rather than $\hat{e}_i$ to indicate that the basis vectors are orthogonal but not normalized: $\boldsymbol{e}_i = h_i \hat{e}_i ~(\text{no summation})$. Replace the Cartesian coordinate values $(x_1, x_2, x_3)$ with the Curvilinear coordinate values $(u_1, u_2, u_3)$. 

- Lamé Parameters
$$
h_i = \left| \frac{ \partial \boldsymbol{r} }{ \partial u_i } \right|, 
\quad
H = \prod_{i=1}^{3}h_i,
\quad 
\hat{e}_i= \frac{{ \partial \boldsymbol{r} }/{ \partial u_i }}{\left| { \partial \boldsymbol{r} }/{ \partial u_i } \right|} = \frac{1}{h_i}  \frac{ \partial \boldsymbol{r} }{ \partial u_i } = \frac{1}{h_i} \boldsymbol{e}_i
\quad(\text{no summation})
$$
for Cylindrical coordinates, $\boldsymbol{r} = (\rho \cos\phi, \rho \sin\phi, z)$:  
$$
h_\rho,~h_\phi,~ h_z = 1,~ \rho,~1 
\quad\text{and}\quad
\begin{cases}
\hat{e}_\rho = \frac{1}{h_\rho} \frac{\partial \boldsymbol{r}}{\partial \rho} = (\cos\phi, \sin\phi, 0) \\[3pt]
\hat{e}_\phi = \frac{1}{h_\phi} \frac{\partial \boldsymbol{r}}{\partial \phi} = (-\sin\phi, \cos\phi, 0) \\[3pt]
\hat{e}_z = \frac{1}{h_z} \frac{\partial \boldsymbol{r}}{\partial z} = (0, 0, 1) 
\end{cases}
$$
for Spherical coordinates, $\boldsymbol{r} = (r \sin\theta \cos\phi, r \sin\theta \sin\phi, r \cos\theta)$:
$$
h_r,~h_\theta,~ h_\phi =1,~r,~ r\sin\theta 
\quad\text{and}\quad
\begin{cases} 
\hat{e}_r = \frac{1}{h_r} \frac{\partial \boldsymbol{r}}{\partial r} = (\sin\theta\cos\phi, \sin\theta\sin\phi, \cos\theta) \\[3pt]
\hat{e}_\theta = \frac{1}{h_\theta} \frac{\partial \boldsymbol{r}}{\partial \theta} = (\cos\theta\cos\phi, \cos\theta\sin\phi, -\sin\theta) \\[3pt] 
\hat{e}_\phi = \frac{1}{h_\phi} \frac{\partial \boldsymbol{r}}{\partial \phi} = (-\sin\phi, \cos\phi, 0) 
\end{cases}
$$
#### $\nabla$ 
- Coordinate Component Expansion of Differential Operators
$$
\operatorname{grad}\Phi = \sum_i\frac{1}{h_i} \boldsymbol{e}_i \partial_i \Phi = \hat{e}_i \partial_i \Phi
$$
$$
\operatorname{div} \boldsymbol{v} 
= \sum_i\frac{1}{H} \partial_i \left( \frac{H v_i}{h_i} \right)
= \frac{1}{h_1 h_2 h_3} \left[ \frac{\partial}{\partial u_1}(h_2 h_3 v_1) + \frac{\partial}{\partial u_2}(h_3 h_1 v_2) + \frac{\partial}{\partial u_3}(h_1 h_2 v_3) \right] 
$$
$$
\operatorname{curl} \boldsymbol{v}
= \frac{1}{h_1 h_2 h_3} 
\begin{vmatrix} 
h_1 \hat{e}_1 & h_2 \hat{e}_2 & h_3 \hat{e}_3 \\[4pt] 
\dfrac{\partial}{\partial u_1} & \dfrac{\partial}{\partial u_2} & \dfrac{\partial}{\partial u_3} \\[4pt] 
h_1 v_1 & h_2 v_2 & h_3 v_3 
\end{vmatrix}
$$
$$
\nabla^2 v = \nabla \cdot \nabla v = \sum_k \frac{1}{H} \partial_k\left( \frac{H}{h_k}(\nabla v)_k \right) = \sum_k\frac{1}{H} \partial_k\left( \frac{H}{h_k}\partial_k^2 v \right)
$$
- The differential identity of the basis vector
$$
\nabla u_i = \hat{e}_i = \frac{\boldsymbol{e}_i}{h_i},\quad
\nabla \times \frac{\boldsymbol{e}_i}{h_i} = \nabla \times \hat{e}_i = 0,\quad
\nabla \cdot \frac{h_i\boldsymbol{e}_i}{H} = 0
\quad(\text{no summation})
$$
- For Cylindrical coordinates, $\boldsymbol{r} = (r \cos\phi, r \sin\phi, z)$
$$
\begin{aligned}
&\nabla v = \boldsymbol{e}_r \frac{\partial v}{\partial r}  + \boldsymbol{e}_\theta \frac{1}{r} \frac{\partial v}{\partial \theta} + \boldsymbol{e}_z \frac{\partial v}{\partial z}  \\[6pt]
&\nabla \cdot \boldsymbol{v} = \frac{1}{r} \frac{\partial}{\partial r}(r v_r) + \frac{1}{r} \frac{\partial v_\theta}{\partial \theta} + \frac{\partial v_z}{\partial z}  \\[6pt]
&\nabla \times \boldsymbol{v} = \frac{1}{r} \begin{vmatrix} \boldsymbol{e}_r & r \boldsymbol{e}_\theta & \boldsymbol{e}_z \\ \frac{\partial}{\partial r} & \frac{\partial}{\partial \theta} & \frac{\partial}{\partial z} \\ v_r & r v_\theta & v_z \end{vmatrix}  \\[6pt]
&\nabla^2 v= \frac{1}{r} \frac{\partial}{\partial r} \left( r \frac{\partial v}{\partial r} \right) + \frac{1}{r^2} \frac{\partial^2 v}{\partial \theta^2} + \frac{\partial^2 v}{\partial z^2} 
\end{aligned}
$$
- For Spherical coordinates, $\boldsymbol{r} = (r \sin\theta \cos\varphi, r \sin\theta \sin\varphi, r \cos\theta)$
$$
\begin{aligned} 
&\nabla v = \boldsymbol{e}_r \frac{\partial v}{\partial r} + \boldsymbol{e}_\theta \frac{1}{r} \frac{\partial v}{\partial \theta} + \boldsymbol{e}_\varphi \frac{1}{r \sin \theta} \frac{\partial v}{\partial \varphi} \\[6pt]
&\nabla \cdot \boldsymbol{v} = \frac{1}{r^2} \frac{\partial}{\partial r}(r^2 v_r) + \frac{1}{r \sin \theta} \frac{\partial}{\partial \theta} (\sin \theta v_\theta) + \frac{1}{r \sin \theta} \frac{\partial v_\varphi}{\partial \varphi}  \\[6pt]
&\nabla \times \boldsymbol{v} = \frac{1}{r^2 \sin \theta} \begin{vmatrix} \boldsymbol{e}_r & r \boldsymbol{e}_\theta & r \sin \theta \boldsymbol{e}_\varphi \\ \frac{\partial}{\partial r} & \frac{\partial}{\partial \theta} & \frac{\partial}{\partial \varphi} \\v_r & r v_\theta & r \sin \theta v_\varphi \end{vmatrix}  \\[6pt]
&\nabla^2 v = \frac{1}{r^2} \frac{\partial}{\partial r} \left( r^2 \frac{\partial v}{\partial r} \right) + \frac{1}{r^2 \sin \theta} \frac{\partial}{\partial \theta} \left( \sin \theta \frac{\partial v}{\partial \theta} \right) + \frac{1}{r^2 \sin^2 \theta} \frac{\partial^2 v}{\partial \varphi^2} 
\end{aligned}
$$
## 1.2 Dirac $\delta$ function  
### 1.2.1 Definition
- 1D definition
$$
\int_\mathbb{R} \delta(x-a) \varphi(x)\,\mathrm{d}x = \varphi(a)
\implies
\int_\mathbb{R} \delta^{(n)}(x-a) \varphi(x)\,\mathrm{d}x = (-1)^n\varphi^{(n)}(a)
$$
$$
\implies \int_\mathbb{R} \delta^{(n)}(x-a) \,\mathrm{d}x = 
\begin{cases}
1, n=1 \\[2pt]
0, n>1
\end{cases}
$$
$$
\delta(x) = \frac{\mathrm{d}}{\mathrm{d}x} \Theta(x), \quad  \Theta(x) = \begin{cases} 0, & x < 0 \\ 1, & x > 0 \end{cases}
$$
- 3D definition
$$
\delta^3(\boldsymbol{x}-\boldsymbol{a}) = \delta(x_1 - a_1) \delta(x_2-a_2) \delta(x_3-a_3)
$$
$$
\implies
\int_{\mathbb{R}^3} \delta^3(\boldsymbol{x}-\boldsymbol{a}) \varphi(\boldsymbol{x})\,\mathrm{d}^3x = \varphi(\boldsymbol{a})
$$
$$
\int_{\mathbb{R}^3} \partial^\alpha \delta^3(\boldsymbol{x}-\boldsymbol{a}) \varphi(\boldsymbol{x}) \, \mathrm{d}^3x = (-1)^{\alpha} \partial^\alpha \varphi(\boldsymbol{a})
,\quad\text{with}
~\partial^\alpha = \left( \frac{ \partial  }{ \partial x_1} \right)^{\alpha_1}\left( \frac{ \partial  }{ \partial x_2} \right)^{\alpha_2}\left( \frac{ \partial  }{ \partial x_3} \right)^{\alpha_3}, \alpha = \alpha_1 + \alpha_2 + \alpha_3
$$
$$
\implies
\int_{\mathbb{R}^3} [\nabla \delta^3(\boldsymbol{x}-\boldsymbol{a})] \varphi(\boldsymbol{x}) \, \mathrm{d}^3x = -\nabla \varphi(\boldsymbol{a})
$$
$$
\implies \int_{\mathbb{R}^3} [\nabla \delta^3(\boldsymbol{x}-\boldsymbol{a})] \cdot \boldsymbol{A}(\boldsymbol{x}) \, \mathrm{d}^3x = -(\nabla \cdot \boldsymbol{A})|_{\boldsymbol{x}=\boldsymbol{a}}
$$
$$
\implies
\int_{\mathbb{R}^3} [\nabla^2 \delta^3(\boldsymbol{x}-\boldsymbol{a})] \varphi(\boldsymbol{x}) \, \mathrm{d}^3x = \nabla^2 \varphi(\boldsymbol{a})
$$
### 1.2.2 Fundamental characteristics
$$
x\delta(x) = 0,\quad x^n \delta^{(n)}(x) = (-1)^n n! \delta(x),\quad x_i\delta^3(\boldsymbol{x}) = 0,\quad x_i\partial_j \delta^3(\boldsymbol{x}) = - \delta_{ij} \delta^3(\boldsymbol{x})
$$
for $f(x) : \mathbb{R} \to \mathbb{R}$, one find
$$
\delta(f(x)) = \sum_n \frac{\delta(x-x_i)}{\left| f'(x_i) \right|}, \quad \text{with}~ f(x_i)=0, f'(x_i)\neq 0
$$
for $f(\boldsymbol{x}):\mathbb{R}^n\to \mathbb{R}$ 
$$
\int_{\mathbb{R}^n} g(\boldsymbol{x}) \delta(f(\boldsymbol{x})) \, \mathrm{d}^n\boldsymbol{x} = \int_{f(\boldsymbol{x})=0} \frac{g(\boldsymbol{x})}{|\nabla f(\boldsymbol{x})|} \, \mathrm{d}S
, \quad \text{with}~ \nabla f(\boldsymbol{x}_i)\neq 0
$$
for $\boldsymbol{F}(\boldsymbol{x}):\mathbb{R}^n\to \mathbb{R}^n$ 
$$
\delta(\boldsymbol{F}(\boldsymbol{x})) 
= \sum_{i} {\delta(\boldsymbol{x} - \boldsymbol{x}_i)}
{\Huge/}{\left|
\frac{ \partial (F_1,F_2,\dots, F_n) }{ \partial (x_1,x_2,\dots, x_n) }
\right|_{\boldsymbol{x} = \boldsymbol{x}_i}}
, \quad \text{with}~ \boldsymbol{F}(\boldsymbol{x}_i)=0, \det\left(\frac{\partial F_i}{\partial x_j}\right) \neq 0
$$
$\implies$ for the orthogonal curvilinear coordinates
$$
\delta^3(\boldsymbol{x}-\boldsymbol{x}') = \frac{1}{H} \delta^3(\boldsymbol{u} - \boldsymbol{u}')
$$

### 1.2.3 Cases  
- the point dipole (Electric dipole or magnetic dipole)  
Let the point dipole be at the origin, and its charge density distribution is: 
$$
\rho(\boldsymbol{x}) = -\boldsymbol{p} \cdot \nabla \delta^3(\boldsymbol{x})
$$
Because the total charge is zero,  
$$
Q = \int_{\mathbb{R}^3} \rho(\boldsymbol{x}) \, \mathrm{d}^3x = \int_{\mathbb{R}^3} [-\boldsymbol{p} \cdot \nabla \delta^3(\boldsymbol{x})] \, \mathrm{d}^3x
= - \left( -\boldsymbol{p} \cdot \int_{\mathbb{R}^3} \delta^3(\boldsymbol{x}) \nabla(1) \, \mathrm{d}^3x \right) 
=0
$$
and the first-order moment (dipole moment) is $\boldsymbol{p}$,  
$$
\begin{align} 
\boldsymbol{d} &= \int \boldsymbol{x} \rho(\boldsymbol{x})\, \mathrm{d}^3x
= \int_{\mathbb{R}^3} \boldsymbol{x} [-\boldsymbol{p} \cdot \nabla \delta^3(\boldsymbol{x})] \,\mathrm{d}^3x\\[4pt]
&= \int_{\mathbb{R}^3} \boldsymbol{x} \left[ -p_i \frac{ \partial \delta^3 }{ \partial x_i } \right] \,\mathrm{d}^3x
= - p_i \int_{\mathbb{R}^3} \boldsymbol{x}\frac{ \partial \delta^3 }{ \partial x_i } \,\mathrm{d}^3x\\[4pt]
&= p_i ~\left.\frac{ \partial \boldsymbol{x} }{ \partial x_i } \right|_{\boldsymbol{x}=0}
= p_i \hat{e}_i = \boldsymbol{p}
\end{align}
$$
# 2 Fundamentals of Electromagnetism  
## 2.1 Maxwell's equation (in cosmos)  
- In cosmos
$$
\left\{
\begin{aligned} 
\nabla \cdot \boldsymbol{E} &= \frac{\rho}{\epsilon_0} &&(\text{Gauss's Law}) 
\\[4pt]
\nabla \cdot \boldsymbol{B} &= 0 &&(\text{Gauss's Law for Magnetism}) 
\\[4pt]
\nabla \times \boldsymbol{E} &= -\frac{ \partial \boldsymbol{B} }{ \partial t }  &&(\text{Faraday Law})
\\[4pt]
\nabla \times \boldsymbol{B} &= \mu_0 \boldsymbol{J} + \frac{1}{c^2} \frac{ \partial \boldsymbol{E} }{ \partial t }  &&(\text{Ampere-Maxwell Law})
\\[4pt]
\end{aligned}
\right.
$$
with $c=\frac{1}{\sqrt{\mu_0\epsilon_0}}$.
- In media
$$
\left\{ \begin{aligned} 
\nabla \cdot \boldsymbol{D} &= \rho_f && (\text{Gauss's Law}) 
\\[4pt] 
\nabla \cdot \boldsymbol{B} &= 0 && (\text{Gauss's Law for Magnetism}) 
\\[4pt]
\nabla \times \boldsymbol{E} &= -\frac{\partial \boldsymbol{B}}{\partial t} && (\text{Faraday's Law}) 
\\[4pt] 
\nabla \times \boldsymbol{H} &= \boldsymbol{J}_f + \frac{\partial \boldsymbol{D}}{\partial t} && (\text{Ampere-Maxwell Law}) 
\end{aligned} \right. 
$$
or   
$$
\nabla \cdot \boldsymbol{E} = \frac{{\rho_f + \rho_p}}{\epsilon_0}, \quad \rho_p = - \nabla \cdot \boldsymbol{P}
$$
$$
\nabla \times \boldsymbol{B} = \mu_0 (\boldsymbol{J}_f + \boldsymbol{J}_M + \boldsymbol{J}_P) + \frac{1}{c^2} \frac{ \partial \boldsymbol{E} }{ \partial t } 
=
\mu_0 \left( \boldsymbol{J}_f + \nabla \times \boldsymbol{M} + \frac{ \partial \boldsymbol{P} }{ \partial t } \right) + \frac{1}{c^2} \frac{ \partial \boldsymbol{E} }{ \partial t } 
$$

- Lorentz force
$$
\frac{ \mathrm{d} \boldsymbol{p} }{ \mathrm{d} t} = q\boldsymbol{E} + q\boldsymbol{v}\times \boldsymbol{B}
$$
- Ohm law
$$
\boldsymbol{j} = \sigma \left(  \underset{\text{constitutive term}}{\underbrace{\boldsymbol{E}}} 
+ \underset{\text{convective term}}{\underbrace{\boldsymbol{u}\times \boldsymbol{B}}} 
- \underset{\text{hall term}}{\underbrace{\frac{1}{ne}\boldsymbol{j}\times\boldsymbol{B}}} 
+ \underset{\text{electron pressure term}}{\underbrace{\frac{\nabla p_e}{ne}}} 
- \underset{\text{inertial term}}{\underbrace{\frac{m_e}{ne^2} \frac{\partial \boldsymbol{j}}{\partial t}}}
+\underset{\text{more and more}}{\underbrace{\cdots}} \right)
$$
## 2.2 Polarization and magnetization
- Polarization and magnetization intensity
$$
\boldsymbol{D} = \epsilon_0 \boldsymbol{E} + \boldsymbol{P},\quad
\boldsymbol{H} = \frac{1}{\mu_0} \boldsymbol{B} - \boldsymbol{M}
$$
for linear isotropic media,  
$$
\boldsymbol{D} = \epsilon \boldsymbol{E}
,\quad
\boldsymbol{H} = \frac{1}{\mu} \boldsymbol{B}
$$
- Charge / Current
$$
\left\{ \begin{aligned} 
\boldsymbol{J}_P &= \frac{ \partial \boldsymbol{P} }{ \partial t } &&(\text{Polarizing Current})
\\[4pt] 
\boldsymbol{J}_M &= \nabla \times \boldsymbol{M},~ \boldsymbol{K}_M  = \hat{n}\times (\boldsymbol{M}_1 - \boldsymbol{M}_2) && (\text{Magnetizing Current}) 
\\[4pt]
\rho_p &= -\nabla \cdot \boldsymbol{P},~ \boldsymbol{\sigma}_p = \hat{n} \cdot (\boldsymbol{P}_1 - \boldsymbol{P}_2) && (\text{Polarizing Charge}) 
\end{aligned} \right. 
$$
## 2.3 Boundary conditions  
- In cosmos ($\hat{n} = \hat{n}_{1\to 2}$) 
$$
\epsilon_0 (\boldsymbol{E}_2 - \boldsymbol{E}_1) \cdot \hat{\boldsymbol{n}} = \sigma,\quad
(\boldsymbol{B}_2 - \boldsymbol{B}_1) \cdot \hat{\boldsymbol{n}} = 0,\quad
\hat{\boldsymbol{n}} \times (\boldsymbol{E}_2 - \boldsymbol{E}_1) = 0,\quad
\frac{1}{\mu_0} \hat{\boldsymbol{n}} \times (\boldsymbol{B}_2 - \boldsymbol{B}_1) = \boldsymbol{K}
$$
or simply  
$$
{\epsilon_0}(\boldsymbol{E}_2 -\boldsymbol{E}_1) = \sigma \hat{n}, \quad
\frac{1}{\mu_0}(\boldsymbol{B}_2 -\boldsymbol{B}_1) = \boldsymbol{K}\times \hat{n}
$$
- In media
$$
(\boldsymbol{D}_2 - \boldsymbol{D}_1) \cdot \hat{\boldsymbol{n}} = \sigma_f,\quad
(\boldsymbol{B}_2 - \boldsymbol{B}_1) \cdot \hat{\boldsymbol{n}} = 0,\quad
\hat{\boldsymbol{n}} \times (\boldsymbol{E}_2 - \boldsymbol{E}_1) = 0,\quad
\hat{\boldsymbol{n}} \times (\boldsymbol{H}_2 - \boldsymbol{H}_1) = \boldsymbol{K}_f
$$
or  
$$
\epsilon_0 (\boldsymbol{E}_2 - \boldsymbol{E}_1) \cdot \hat{\boldsymbol{n}} = \sigma_f + \sigma_p,\quad
(\boldsymbol{B}_2 - \boldsymbol{B}_1) \cdot \hat{\boldsymbol{n}} = 0,\quad
\hat{\boldsymbol{n}} \times (\boldsymbol{E}_2 - \boldsymbol{E}_1) = 0,\quad
\frac{1}{\mu_0} \hat{\boldsymbol{n}} \times (\boldsymbol{B}_2 - \boldsymbol{B}_1) = \boldsymbol{K}_f + \boldsymbol{K}_M
$$
with $\boldsymbol{J}_P = \frac{ \partial \boldsymbol{P} }{ \partial t }=0$.  

## 2.4 Electromagnetic potential
- Definition
$$
\boldsymbol{E} = -\nabla \varphi - \frac{ \partial \boldsymbol{A} }{ \partial t },\quad
\boldsymbol{B} = \nabla \times \boldsymbol{A}
$$
- Coulomb gauge
$$
\mathfrak{C} \triangleq \nabla \cdot \boldsymbol{A} = 0
$$
- Lorentz gauge
$$
\mathfrak{L} \triangleq \nabla \cdot \boldsymbol{A} + \frac{1}{c^2} \frac{ \partial \varphi }{ \partial t } = 0
$$
- Gauge invariance
$$
\varphi' = \varphi - \frac{ \partial \psi }{ \partial t }, \quad 
\boldsymbol{A}' = \boldsymbol{A} + \nabla \psi 
$$
- Electromagnetic potential equation
$$
\begin{align} 
\square \varphi + \partial_t \mathfrak{L} &= -\frac{\rho}{\epsilon_0}\\[3pt]
\square \boldsymbol{A} - \nabla \mathfrak{L} &= -\mu_0 \boldsymbol{J}
\end{align}
$$
with $\square \triangleq \nabla^2 - \frac{1}{c^2} \frac{ \partial^2 }{ \partial t^2 }~\text{(d'Alembert operator)}$.  
## 2.5 EM Wave  
### 2.5.1 Wave equation
- Wave equation for free time-varying field
$$
\square \boldsymbol{E} = 0,\quad \square \boldsymbol{B} = 0
$$
- Definition: phase of monochromatic wave
$$
\phi = \boldsymbol{k}\cdot\boldsymbol{x} - \omega t
$$
- Dispersion relation
$$
\omega = kc
$$
$$
\implies v_p = \frac{\omega}{k} = c,\quad
v_g = \frac{ \mathrm{d} \omega }{ \mathrm{d} k} = c
$$
### 2.5.2 Polarization  
- Real description
$$
E_1 = A_1 \cos\phi,\quad E_2 = A_2 \cos(\phi + \delta)
$$
$$
\implies 
\left( \frac{E_1}{A_1} \right)^2 + \left( \frac{E_2}{A_2} \right)^2 - 2 \frac{{E_1E_2}}{A_1A_2} \cos \delta = \sin^2\delta
$$
for certain $\boldsymbol{k}\cdot\boldsymbol{x}$,  
$$
E_1 = A_1 \cos \omega t,\quad E_2 = A_2 \cos(\omega t - \delta)
$$
$$
\implies
\begin{cases}
\sin\delta > 0, \quad \text{Right-hand} \\[5pt]
\sin\delta < 0, \quad \text{Left-hand}
\end{cases}
$$
- Complex description
$$
\tilde{E}_1 = A_1 e^{\mathrm{i} \phi} , \quad  \tilde E_2 = A_2 e^{\mathrm{i} (\phi +\delta)}
$$
for certain $\boldsymbol{k}\cdot\boldsymbol{x}$,  
$$
\tilde E_1 = A_1 e^{\mathrm{i} (-\omega t)} , \quad \tilde E_2 = A_2 e^{\mathrm{i} ( -\omega t +\delta)}
$$
define the degree of polarization  
$$
\tilde R = \frac{\tilde{E}_2}{\tilde{E}_1} = \frac{A_2}{A_1} e^{\mathrm{i} \delta}
$$
$$
\implies
\begin{cases}
\operatorname{Im}\tilde R > 0, \quad \text{Right-hand} \\[5pt]
\operatorname{Im}\tilde R < 0, \quad \text{Left-hand}
\end{cases}
$$
- Circularly polarized basis vectors
$$
\begin{cases}
\hat{e}_+ \triangleq \frac{{\hat{e}_1 + \mathrm{i} \hat{e}_2}}{\sqrt{2}}, \quad \text{Right-hand} \\[5pt]
\hat{e}_- \triangleq \frac{{\hat{e}_1 - \mathrm{i} \hat{e}_2}}{\sqrt{2}}, \quad \text{Left-hand}
\end{cases}
$$
satisfy 
$$
\hat{e}_- = \hat{e}_+^*, \quad \hat{e}^*_\pm \cdot \hat{e}_\pm = 1, \quad \hat{e}_\pm \cdot \hat{e}_\pm =0
$$
Monochromatic waves can be transformed from 2D Cartesian coordinates to circularly polarized coordinates,  
$$
\boldsymbol{E} = \boldsymbol{E}_0 e^{\mathrm{i} \phi} = (E_+\hat{e}_+ + E_- \hat{e}_-) e^{\mathrm{i}\phi},\quad
E_\pm = \hat{e}_\pm^* \cdot \boldsymbol{E}_0
$$
### 2.5.3 Complex description  
for $\tilde{E}_1 = A_1 e^{\mathrm{i} \phi} ,  \tilde E_2 = A_2 e^{\mathrm{i} (\phi +\delta)}$, if $A_{1,2}$ is independent with $(t,\boldsymbol{x})$,
$$
\nabla \longrightarrow \mathrm{i}\boldsymbol{k}, \quad
\nabla \cdot \longrightarrow \mathrm{i}\boldsymbol{k} ~\cdot, \quad
\nabla \times \longrightarrow \mathrm{i}\boldsymbol{k} \times, \quad
\frac{\partial}{\partial t} \longrightarrow -\mathrm{i}\omega
$$
- Long - term average: for $\tilde{f} = \tilde{f}_0 e^{-\mathrm{i}\omega t}, \tilde{g} = \tilde{g}_0 e^{-\mathrm{i}\omega t}$,
$$
\langle \Re[\tilde{f}] \cdot \Re[\tilde{g}] \rangle = \frac{1}{2} \Re[\tilde{f}_0 \tilde{g}_0^*]
$$
In the vector scenario,
$$
\langle \Re[\tilde{\boldsymbol{f}}] \cdot \Re[\tilde{\boldsymbol{g}}] \rangle = \frac{1}{2} \Re[\tilde{\boldsymbol{f}} \cdot \tilde{\boldsymbol{g}}^*]
,\quad
\langle \Re[\tilde{\boldsymbol{f}}] \times \Re[\tilde{\boldsymbol{g}}] \rangle = \frac{1}{2} \Re[\tilde{\boldsymbol{f}} \times \tilde{\boldsymbol{g}}^*]
$$
## 2.6 Conservation / Continuity equation
- Charge conservation
$$
\nabla \cdot \boldsymbol{j} + \frac{\partial \rho}{\partial t} = 0
$$
- Energy conservation
$$
-\frac{ \partial \varepsilon }{ \partial t } = \nabla \cdot \boldsymbol{S} + \boldsymbol{f} \cdot \boldsymbol{v}
$$
with EMF (electromagnetic field) energy, Poynting vector and Lorentz force
$$
\varepsilon = \frac{1}{2}\epsilon_0 E^2 + \frac{B^2}{2\mu_0},~~
\boldsymbol{S} = \frac{1}{\mu_0} \boldsymbol{E} \times \boldsymbol{B},~~
\boldsymbol{f} = \rho_e \boldsymbol{E} + \boldsymbol{J} \times \boldsymbol{B}
$$
- Momentum conservation
$$
-\frac{ \partial \boldsymbol{g} }{ \partial t } = \nabla \cdot \mathsf{T} + \boldsymbol{f}
$$
with EMF momentum and Maxwell stress tensor
$$
\boldsymbol{g} = \epsilon_0 \boldsymbol{E} \times \boldsymbol{B} = \boldsymbol{S}/c^2,\quad
\mathsf{T}_M  = -\mathsf{T} = -\varepsilon \mathsf{I} + \left( \epsilon_0 \boldsymbol{E}\boldsymbol{E} + \frac{\boldsymbol{B}\boldsymbol{B}}{\mu_0} \right)
$$
In a steady state where the electromagnetic momentum is constant over time, the total force acting on the particles within volume $V$ can be expressed as
$$
\boldsymbol{F} =  \iiint_V \boldsymbol{f}\,\mathrm{d}V = -\oint_{\partial V} \mathrm{d}\boldsymbol{\sigma}\cdot \mathsf{T}
$$
- Angular momentum conservation
$$
-\frac{ \partial  }{ \partial t } (\boldsymbol{r}\times \boldsymbol{g} ) = \underset{=\boldsymbol{r} \times (\nabla \cdot \mathsf{T})}{\underbrace{\nabla \cdot (\boldsymbol{r} \times \mathsf{T}) }}+ \boldsymbol{r}\times \boldsymbol{f}
$$
- In linear homogeneous media
	- Charge conservation
$$
\nabla \cdot \boldsymbol{j}_f + \frac{\partial \rho_f}{\partial t} = 0, \quad
\nabla \cdot (\boldsymbol{j}_P +\boldsymbol{j}_M) + \frac{\partial \rho_p}{\partial t} = 0
$$
Energy conservation (Poynting's Theorem in Media)
$$
\frac{ \partial \varepsilon }{ \partial t } = \nabla \cdot \boldsymbol{S} + \boldsymbol{j}_f \cdot \boldsymbol{E}
$$
with EMF energy and Poynting vector and Lorentz force
$$
\varepsilon = \frac{1}{2}(\boldsymbol{E} \cdot \boldsymbol{D} + \boldsymbol{B} \cdot \boldsymbol{H}),~~
\boldsymbol{S} = \boldsymbol{E} \times \boldsymbol{H}
$$
Momentum conservation  
$$
\frac{ \partial \boldsymbol{g} }{ \partial t } = \nabla \cdot \mathsf{T} + \boldsymbol{f}_f
$$
with EMF momentum (Minkowski form), Maxwell stress tensor and Lorentz force acting on <font color="#ff0000">free</font> particles
$$
\boldsymbol{g} = \boldsymbol{D} \times \boldsymbol{B}, \quad
\mathsf{T}_M = -\mathsf{T} = -\varepsilon \mathsf{I} + (\boldsymbol{E}\boldsymbol{D} + \boldsymbol{H}\boldsymbol{B}),\quad
\boldsymbol{f}_f = \rho_f \boldsymbol{E} + \boldsymbol{J}_f \times \boldsymbol{B}
$$
In a steady state where the electromagnetic momentum is constant over time, the total force on <font color="#ff0000">free</font> particles within volume V is  
$$
\boldsymbol{F}_f = \iiint_V \boldsymbol{f}_f \,\mathrm{d}V = -\oint_{\partial V} \mathrm{d}\boldsymbol{\sigma} \cdot \mathsf{T}
$$
Angular momentum conservation
$$
\frac{ \partial }{ \partial t } (\boldsymbol{r} \times \boldsymbol{g}) = \nabla \cdot (\boldsymbol{r} \times \mathsf{T}) + \boldsymbol{r} \times \boldsymbol{f}_f
$$
For inhomogeneous media  
$$
\boldsymbol{f}_{total} = \boldsymbol{f}_f - \frac{1}{2} E^2 \nabla \epsilon - \frac{1}{2} H^2 \nabla \mu
$$
# 3 Special Relativity & Tensor analysis (Minkowski spacetime)   
## 3.1 Fundamental definition  
$$
(g)_{\alpha\beta} = (g)^{\alpha\beta} = diag(-1,+1,+1,+1)_{\alpha\beta}
$$
- Primary 4-vector
$$
x^\alpha = (ct, \boldsymbol{x}), \quad 
u^\alpha = \frac{ \mathrm{d} x^\alpha }{ \mathrm{d} \tau} = \gamma (c, \boldsymbol{v}),\quad 
a^\alpha = \frac{ \mathrm{d} u^\alpha }{ \mathrm{d} \tau} 
= \left( {\gamma^4} (\boldsymbol{\beta} \cdot \boldsymbol{a}), \gamma^2 \boldsymbol{a} + {\gamma^4} (\boldsymbol{\beta} \cdot \boldsymbol{a}) \boldsymbol{\beta} \right)
$$
$$
u^\alpha u_\alpha = -c^2,\quad a^\mu u_\mu =0
$$
The accelerated speed in the instantaneous co-moving frame is $\boldsymbol{a}_{in}$, 
$$
a^\mu a_\mu = |\boldsymbol{a}_{in}|^2 = \gamma^4 \left[ |\boldsymbol{a}|^2 + \gamma^2 (\boldsymbol{\beta} \cdot \boldsymbol{a})^2\right]
\implies
|\boldsymbol{a}_{in}| = 
\begin{cases} 
\gamma^2 a, \boldsymbol{\beta} \perp \boldsymbol{a} \\[4pt]
\gamma^3 a, \boldsymbol{\beta} \parallel \boldsymbol{a}
\end{cases}
$$
- Primary characteristics of metric
$$
g_{\alpha\beta}g^{\beta\gamma} = \delta_\alpha^\gamma
$$
- Lorentz transformation  
$$
\mathrm{d} s^2 = g_{\alpha\beta} \mathrm{d}x^\alpha \mathrm{d}x^\beta = \mathrm{d}x_\alpha\mathrm{d}x^\beta = -c^2\mathrm{d}t^2 + |\mathrm{d}\boldsymbol{x}|^2 = -c^2\mathrm{d}\tau^2
$$
Christoffel symbols (the first kind)*
$$
\Gamma_{\rho\mu\nu} = \frac{1}{2} \left( \frac{\partial g_{\rho\mu}}{\partial x^\nu} + \frac{\partial g_{\rho\nu}}{\partial x^\mu} - \frac{\partial g_{\mu\nu}}{\partial x^\rho} \right)
= g_{\alpha\beta} \frac{ \partial^2 x'^\alpha }{ \partial x^\nu \partial x^\mu } \frac{ \partial x'^\beta }{ \partial x^\rho } = 0
$$
$$
\implies
x'^\alpha = \Lambda^{\alpha}_{~~\beta} x^\beta + a^\alpha
$$
the inverse of the matrix $\Lambda^\alpha_{~~\beta}$ is $\Lambda_{\beta}^{~~\alpha}$:  
$$
(\Lambda^{-1})^\mu_{~~\alpha} = g_{\alpha\beta} \Lambda^\beta_{~~\nu}g^{\nu\mu} = \Lambda_\alpha^{~~\mu}
$$
$$
\Lambda^\alpha_{~~\beta} \Lambda_\alpha^{~~\gamma} = \delta_\beta^\gamma \quad \text{or} \quad \Lambda^\alpha_{~~\gamma} \Lambda_\beta^{~~\gamma} = \delta_\beta^\alpha
$$
for $x$-axis boost:  
$$
\Lambda^\alpha_{~~\beta} = \begin{bmatrix} \gamma & \gamma\beta &  &  \\  \gamma\beta & \gamma &  &  \\  &  &  1 &  \\  &  &  & 1 \end{bmatrix},\quad
\Lambda^{~~\alpha}_{\beta} = \begin{bmatrix} \gamma & -\gamma\beta &  &  \\  -\gamma\beta & \gamma &  &  \\  &  &  1 &  \\  &  &  & 1 \end{bmatrix}
$$
for general boost   
$$

$$
Metric invariance condition   
$$
\boxed{g_{\alpha\beta} \Lambda^{\alpha}_{~~\mu} \Lambda^{\beta}_{~~\nu} = g_{\mu\nu}}
$$
$$
\implies
g^{\mu\nu} \Lambda^{\alpha}_{~~\mu} \Lambda^{\beta}_{~~\nu} = g^{\alpha\beta},\quad
g_{\alpha\beta} \Lambda_{\mu}^{~~\alpha}\Lambda_\nu^{~~\beta} = g_{\mu\nu},\quad
g^{\mu\nu} \Lambda_{\mu}^{~~\alpha}\Lambda_\nu^{~~\beta} = g^{\alpha\beta}
$$



- The Proper Orthochronous Lorentz Group*
The Full Lorentz Group $O(1,3)$ consists of all transformations that preserve the Minkowski metric. From the property $\Lambda^T \eta \Lambda = \eta$ above, it follows that $|\det(\Lambda)|=1, |\Lambda^0_{~~0}|\geq 1$.  $O(1,3)$ is a Lie group that possesses four disjoint, connected components. It can be expressed as the union of the Proper Orthochronous Lorentz Group $SO(1,3)^\uparrow$ (the identity component) and its cosets:
$$
\mathcal{P} = diag(1,-1,-1,-1),~~\mathcal{T}=diag(-1,1,1,1)
$$
$$
O(1,3) = \{SO(1,3)^\uparrow,\ \mathcal{P} SO(1,3)^\uparrow,\ \mathcal{T} SO(1,3)^\uparrow,\ \mathcal{P} \mathcal{T} SO(1,3)^\uparrow \}
$$
Infinitesimal Lorentz transformation  
$$
\Lambda^\mu_{~~\nu} = \delta^\mu_{\nu} + \omega^\mu_{~~\nu}
,\quad
\text{with}~
\omega^\mu_{~~\nu} = \begin{pmatrix} 0 & \beta_x & \beta_y & \beta_z \\ \beta_x & 0 & \theta_z & -\theta_y \\ \beta_y & -\theta_z & 0 & \theta_x \\ \beta_z & \theta_y & -\theta_x & 0 \end{pmatrix}
$$
$$
K' \to K:\quad x^\alpha = \Lambda^\alpha_{~~\beta}x'^\beta = \begin{bmatrix} ct' + \boldsymbol{\beta}\cdot\boldsymbol{x}' \\  \boldsymbol{x}' + \boldsymbol{\beta}ct' - \boldsymbol{\theta}\times\boldsymbol{x}' \end{bmatrix}
$$
For infinite transformation $\Omega = \lim_{ n \to \infty } n\omega$, 
$$
\Lambda = \\lim_{ n \to \infty } \left( 1+\frac{\Omega}{n} \right)^n = e^\Omega = \sum_{k=0}^{\infty} \frac{\Omega^k}{k!}
=
\begin{cases}
\begin{bmatrix} 1 & 0 & 0 & 0 \\ 0 & \cos\theta & \sin\theta & 0 \\ 0 & -\sin\theta & \cos\theta & 0 \\ 0 & 0 & 0 & 1 \end{bmatrix}, &\text{z-axis rotation} \\[4pt]
\begin{bmatrix} ~~\mathrm{ch} \phi & ~~\mathrm{sh} \phi & &\\
~~\mathrm{sh} \phi & ~~\mathrm{ch} \phi & & \\
& & ~1 & \\
& & & ~1 \end{bmatrix}, &\text{x-axis boost} ,\text{ with }\tanh \phi = \beta
\end{cases}
$$
![Pasted image 20260506122206.png](/img/user/Pasted%20image%2020260506122206.png)

# 4 Lagrangian Formulation of the EM Field  

# 5 Static Electric Field
# 6 Static Magnetic Field  
# 7 EM Wave

# 8 Electromagnetic Radiation
## 8.1 Fields of a Moving Point Charge






