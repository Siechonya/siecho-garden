---
{"dg-publish":true,"permalink":"/A_symmetry_自然界的对称性/Applications/ED formulas 2/","noteIcon":"default","created":"2026-05-20T09:48:38.906+08:00","updated":"2026-05-22T10:58:28.096+08:00","dg-note-properties":{}}
---



<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/A_symmetry_自然界的对称性/Applications/ED Formulas/#symbol-convention" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">

<div class="markdown-embed-title">

# Symbol Convention

</div>


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
Consequently, the invariant spacetime interval is given by $\mathrm{d}s^2 = -c^2\mathrm{d}t^2 + \mathrm{d}x^2 + \mathrm{d}y^2 + \mathrm{d}z^2=-\mathrm{d}\tau^2$.  
- Lorentz transformation
$$
K'\to K:\quad
x^\alpha = \Lambda^{\alpha}_{~~\beta} x'^\beta
$$
For $x$-axis boost (where $K'$ moves with velocity $v\hat{e}_x$ relative to $K$), the transformation matrix $\Lambda$ is:
$$
\Lambda^\alpha_{~~\beta} = \begin{bmatrix} \gamma & \gamma\beta &  &  \\  \gamma\beta & \gamma &  &  \\  &  &  1 &  \\  &  &  & 1 \end{bmatrix}
$$


</div></div>



# 1 Static Electric Field    
## 1.1 Multipole expansion  
- Electrostatic potential expansion ($\boldsymbol{R}=\boldsymbol{x}-\boldsymbol{x'}, r=|\boldsymbol{x}|(field), r'=|\boldsymbol{x'}|(source)$)
$$
\begin{align} 
\frac{1}{R}=\frac{1}{|\boldsymbol{x}-\boldsymbol{x}'|} = e^{-\boldsymbol{x'}\cdot \nabla} \frac{1}{r} 
&= 
\left[ 1 - \boldsymbol{x'}\cdot \nabla + \frac{1}{2!}(\boldsymbol{x'}\boldsymbol{x'}:\nabla\nabla) + \cdots \right] \frac{1}{r} \\[8pt]
{\color{gray}{\small \mathsf{I}: \nabla\nabla \frac{1}{r}=0} \implies}&=
\frac{1}{r} - \boldsymbol{x'}\cdot \nabla \frac{1}{r} + \frac{1}{6} (3\boldsymbol{x'}\boldsymbol{x'}-r'^2 \mathsf{I}): \nabla\nabla \frac{1}{r} + \cdots
\end{align}
$$
$$
\Downarrow
$$
$$
\begin{align} 
\varphi(\boldsymbol{x}) = \frac{1}{4\mathrm{\pi} \epsilon_0}\int \frac{\mathrm{d}q}{R}
&=
\frac{1}{4\mathrm{\pi} \epsilon_0} \left[ {Q}- \boldsymbol{p}\cdot\nabla + \frac{1}{6} \mathsf{D}:\nabla\nabla + \cdots\right] \frac{1}{r}
\\[8pt]
&=
\frac{Q}{4\mathrm{\pi} \epsilon_0 r} + \frac{{\boldsymbol{p}\cdot \hat{r}}}{4\mathrm{\pi} \epsilon_0 r^2} + \frac{{\mathsf{D}:\hat{r}\hat{r}}}{8\mathrm{\pi} \epsilon_0 r^3} + \cdots
\end{align}
$$
Where $Q=\int \mathrm{d}q = \int \rho(\boldsymbol{x'})\,\mathrm{d} V$ is total charge, $\boldsymbol{p}=\int \boldsymbol{x'}\,\mathrm{d}q$ is electric dipole moment, $\mathsf{D} = \int (3\boldsymbol{x'}\boldsymbol{x'} - r'^2\mathsf{I})\,\mathrm{d}q$ is electric quadrupole moment.  
- Electrostatic intensity expansion
$$
\boldsymbol{E} = -\nabla \varphi
=
\frac{Q\hat{r}}{4\mathrm{\pi} \epsilon_0 r^2} + \frac{3(\boldsymbol{p}\cdot\hat{r})\hat{r} - \boldsymbol{p}}{4\mathrm{\pi} \epsilon_0 r^3} + \frac{{5(\mathsf{D}:\hat{r}\hat{r})\hat{r} - 2\mathsf{D}\cdot\hat{r}}}{8\mathrm{\pi} \epsilon_0 r^4} + \cdots
$$
## 1.2 Small charged body in electric field  
Assuming the charge of charged bodies $\boldsymbol{x}$ is so small compared with the source $\boldsymbol{x'}$ which generates the electric field that $\nabla^2\varphi(\boldsymbol{x})=0$. Let $\boldsymbol{\xi}$ be the relative coordinate of a charge element $\mathrm{d}q$ from the body's center $\boldsymbol{x}$. The potential energy $U=\int \varphi(\boldsymbol{x}+\boldsymbol{\xi}) \,\mathrm{d} q$ of the small body is,
$$
U \approx
Q\varphi|_\boldsymbol{x}+ \boldsymbol{p}\cdot \nabla \varphi|_\boldsymbol{x} + \frac{1}{6}\mathsf{D}:\nabla\nabla \varphi|_{\boldsymbol{x}}
=
(Q\varphi)|_\boldsymbol{x}- (\boldsymbol{p}\cdot \boldsymbol{E})|_\boldsymbol{x} - \frac{1}{6}(\mathsf{D}:\nabla\boldsymbol{E})|_{\boldsymbol{x}}
$$
Note that $Q=\int \mathrm{d}q = \int \rho(\boldsymbol{\xi})\,\mathrm{d} V$, $\boldsymbol{p}=\int \boldsymbol{\xi}\,\mathrm{d}q$, $\mathsf{D} = \int(3\boldsymbol{\xi}\boldsymbol{\xi} - \xi^2\mathsf{I})\,\mathrm{d}q$ are intrinsic properties of the small charged body itself, not the external source.  

Furthermore, The total electrostatic force $\boldsymbol{F}$ acting on the small charged body is 
$$
\boldsymbol{F} = -\nabla  U
= Q\boldsymbol{E}_{\text{ext}}\Big|_\boldsymbol{x} + (\boldsymbol{p}\cdot\nabla)\boldsymbol{E}_{\text{ext}}\Big|_\boldsymbol{x} + \frac{1}{6}(\mathsf{D}:\nabla\nabla)\boldsymbol{E}_{\text{ext}}\Big|_\boldsymbol{x} + \cdots 
$$
The total electrostatic torque $\boldsymbol{N}$ acting on the small charged body about its center $\boldsymbol{x}$ is,  
$$
\boldsymbol{N} = \int \boldsymbol{\xi} \times \boldsymbol{E}_{\text{ext}}(\boldsymbol{x}+\boldsymbol{\xi})\,\mathrm{d}q 
=
\boldsymbol{p} \times \boldsymbol{E}_{\text{ext}} + \frac{1}{3} \nabla \cdot (\mathsf{D}\times \boldsymbol{E}_{\text{ext}}) + \cdots
$$
## 1.3 Spherical harmonic expansion  
### 1.3.1 Orthonormal Complete Set of Functions
#### Definition
- Orthonormality
$$ 
\int_{a}^{b} \psi_n^*(x) \psi_m(x) \,\mathrm{d}x = \delta_{nm} ,\quad
\text{with Integration Limits }[a,b] 
$$
- Completeness: Any square-integrable function $f(x)$ can be expanded as
$$ 
f(x) = \sum_n C_n \psi_n(x), \quad \text{where } C_n = \int_a^b \psi^*_n(x)f(x)\,\mathrm{d}x 
$$
which implies
$$
\sum_n \psi_n^*(x')\psi_n(x) = \delta(x-x')
$$
#### Trigonometric & Complex Exponential Functions
$$
\psi_n(x) = \frac{1}{\sqrt{a}} \sin \frac{n\pi x}{a}, \quad \frac{1}{\sqrt{a}} \cos \frac{n\pi x}{a}, \quad \frac{1}{\sqrt{2a}} \exp\left(\mathrm{i}\frac{n\pi x}{a}\right),\quad \text{with Integration Limits }[-a,a] 
$$
Note: $n\in\mathbb{N}_+$ for sine set; $n\in\mathbb{N}$ for cosine set; $n\in\mathbb{Z}$ for complex set.  
#### Legendre Polynomials
$$
\psi_l(x) = \sqrt{\frac{2l+1}{2}} P_l(x),
\quad  l\in\mathbb{N},\ 
\text{with Integration Limits }[-1,1]
$$
$$
P_l(x) = \frac{1}{2^l l!} \frac{ \mathrm{d}^l }{ \mathrm{d} x^l} (x^2-1)^l =
\begin{cases} 
1,\quad l=0 \\[5pt]
x,\quad l=1 \\[5pt]
\frac{1}{2}(3x^2-1) , \quad l=2\\[5pt]
\frac{1}{2}(5x^3-3x) ,\quad l=3\\[5pt]
\cdots
\end{cases}
$$
#### Spherical Harmonics
$$
\psi_{lm}(\theta, \varphi) = Y_l^m(\Omega) = \sqrt{\frac{1}{2\pi} \frac{2l+1}{2} \frac{(l-m)!}{(l+m)!}} ~P_l^m(\cos\theta) e^{\mathrm{i}m\varphi}, 
$$
$$
l \in \mathbb{N}, \ m \in \mathbb{Z} \ \text{\&} \ |m| \le l,\ 
\text{with }\theta \in [0, \pi], \ \varphi \in [0, 2\pi]
$$
$$
P_l^m(x) = (-1)^m(1-x^2)^{\frac{m}{2}} \frac{ \mathrm{d}^m }{ \mathrm{d} x^m} P_l(x), \ \text{for }m\geq0
$$
For negative $m$, the relations are given by:  
$$
P_l^{-m}(x) = (-1)^m \frac{(l-m)!}{(l+m)!} P_l^m(x) \quad \text{or} \quad Y_l^{-m}(\theta, \varphi) = (-1)^m Y_l^{m*}(\theta, \varphi)
$$
The first few associated Legendre functions are, 
$$
\begin{aligned}
P_0^0(x) &= 1, \\[3pt]
P_1^0(x) &= x, \quad P_1^1(x) = -\sqrt{1 - x^2}, \\[3pt]
P_2^0(x) &= \frac{1}{2}(3 x^2 - 1), \quad P_2^1(x) = -3 x\sqrt{1 - x^2}, \quad P_2^2(x) = 3(1 - x^2), \\[2pt]
P_3^0(x) &= \frac{1}{2}(5 x^3 - 3 x), \quad P_3^1(x) = -\frac{3}{2}(5 x^2 - 1)\sqrt{1 - x^2}, \quad
P_3^2(x) = 15 x(1 - x^2), \quad P_3^3(x) = -15(1 - x^2)^{3/2}  \\[2pt]
\cdots
\end{aligned}
$$
- Orthonormality
$$ 
\oint Y_{l'}^{m'*}(\Omega) Y_l^m(\Omega) \,\mathrm{d}\Omega = \delta_{ll'}\delta_{mm'}
$$
- Completeness
$$
\sum_{l=0}^{+\infty}\sum_{m=-l}^{l} Y_{l}^{m}(\Omega') Y_l^m(\Omega) = \delta(\Omega-\Omega') = \delta(\cos\theta - \cos\theta')\delta(\varphi-\varphi')
$$
#### Multipole expansion* using basic functions



## 1.4 Cases
- If all charges are contained within the sphere $V$ (see [[A_symmetry_自然界的对称性/Applications/Appendix for ED formulas#1 $ iiint_V boldsymbol{E}( boldsymbol{x}) , mathrm{d} 3x = - frac{ boldsymbol{p}}{3 epsilon_0}$\|Appendix for ED formulas]])
$$
\iiint_V \boldsymbol{E}(\boldsymbol{x}) \,\mathrm{d}^3x = -\frac{\boldsymbol{p}}{3\epsilon_0}
$$
- An ellipsoid uniformly charged with Q (in the principal inertia axis frame)
$$
D_{11} = \frac{Q}{5}(2a_1^2 - a_2^2 - a_3^2), \quad D_{22} = \cdots, \quad D_{i\neq j} = 0
$$


# 2 Static Magnetic Field  
# 3 EM Wave

# 4 Electromagnetic Radiation
## 4.1 Fields of a moving point charge