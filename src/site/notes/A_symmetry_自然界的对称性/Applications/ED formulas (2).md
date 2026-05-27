---
{"dg-publish":true,"permalink":"/A_symmetry_自然界的对称性/Applications/ED formulas (2)/","noteIcon":"default","created":"2026-05-20T09:48:38.906+08:00","updated":"2026-05-27T15:13:53.274+08:00","dg-note-properties":{}}
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

---  


</div></div>


---

# 1 Electrostatic Field    
## 1.1 Multipole expansion  
- Consider electrostatic potential expansion at an external observation point $\boldsymbol{x}$, with localized charge source $\rho(\boldsymbol{x'})$ confined within a volume $V'$, and $\boldsymbol{R}=\boldsymbol{x}-\boldsymbol{x'}, r=|\boldsymbol{x}|(field), r'=|\boldsymbol{x'}|(source)$, then
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
Where $Q=\int \mathrm{d}q = \int \rho(\boldsymbol{x'})\,\mathrm{d} V'$ is total charge, $\boldsymbol{p}=\int \boldsymbol{x'}\,\mathrm{d}q$ is electric dipole moment, $\mathsf{D} = \int (3\boldsymbol{x'}\boldsymbol{x'} - r'^2\mathsf{I})\,\mathrm{d}q$ is electric quadrupole moment.  
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
Q\varphi\Big|_\boldsymbol{x}+ \boldsymbol{p}\cdot \nabla \varphi\Big|_\boldsymbol{x} + \frac{1}{6}\mathsf{D}:\nabla\nabla \varphi\Big|_{\boldsymbol{x}}
=
(Q\varphi)\Big|_\boldsymbol{x}- (\boldsymbol{p}\cdot \boldsymbol{E})\Big|_\boldsymbol{x} - \frac{1}{6}(\mathsf{D}:\nabla\boldsymbol{E})\Big|_{\boldsymbol{x}}
$$
Note that $Q=\int \mathrm{d}q = \int \rho(\boldsymbol{\xi})\,\mathrm{d} V$, $\boldsymbol{p}=\int \boldsymbol{\xi}\,\mathrm{d}q$, $\mathsf{D} = \int(3\boldsymbol{\xi}\boldsymbol{\xi} - \xi^2\mathsf{I})\,\mathrm{d}q$ are intrinsic properties of the small charged body itself, not the external source.  

Furthermore, The total electrostatic force $\boldsymbol{F}$ acting on the small charged body is, 
$$
\boldsymbol{F} = -\nabla  U
= Q\boldsymbol{E}_{\text{ext}}\Big|_\boldsymbol{x} + (\boldsymbol{p}\cdot\nabla)\boldsymbol{E}_{\text{ext}}\Big|_\boldsymbol{x} + \frac{1}{6}(\mathsf{D}:\nabla\nabla)\boldsymbol{E}_{\text{ext}}\Big|_\boldsymbol{x} + \cdots 
$$
The total force moment $\boldsymbol{N}$ acting on the small charged body about its center $\boldsymbol{x}$ is,  
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
And the first few spherical harmonics are,  
$$
\begin{aligned} 
Y_0^0(\theta, \varphi) &= \sqrt{\frac{1}{4\pi}}, \\[6pt] Y_1^0(\theta, \varphi) &= \sqrt{\frac{3}{4\pi}} \cos\theta, \quad Y_1^1(\theta, \varphi) = -\sqrt{\frac{3}{8\pi}} \sin\theta \,\mathrm{e}^{\mathrm{i}\varphi}, 
\\[6pt] Y_2^0(\theta, \varphi) &= \sqrt{\frac{5}{16\pi}} (3\cos^2\theta - 1), \quad Y_2^1(\theta, \varphi) = -\sqrt{\frac{15}{8\pi}} \sin\theta\cos\theta \,\mathrm{e}^{\mathrm{i}\varphi}, \quad Y_2^2(\theta, \varphi) = \sqrt{\frac{15}{32\pi}} \sin^2\theta \,\mathrm{e}^{2\mathrm{i}\varphi}, 
\\[6pt] Y_3^0(\theta, \varphi) &= \sqrt{\frac{7}{16\pi}} (5\cos^3\theta - 3\cos\theta), \quad Y_3^1(\theta, \varphi) = -\sqrt{\frac{21}{64\pi}} (5\cos^2\theta - 1)\sin\theta \,\mathrm{e}^{\mathrm{i}\varphi}, 
\\[3pt] Y_3^2(\theta, \varphi) &= \sqrt{\frac{105}{32\pi}} \cos\theta\sin^2\theta \,\mathrm{e}^{2\mathrm{i}\varphi}, \quad Y_3^3(\theta, \varphi) = -\sqrt{\frac{35}{64\pi}} \sin^3\theta \,\mathrm{e}^{3\mathrm{i}\varphi} 
\\[3pt] \cdots 
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

### 1.3.2 Multipole expansion *
By using the Legendre generating function, one finds
$$
\frac{1}{R} = \frac{1}{|\boldsymbol{x}-\boldsymbol{x'}|} = \sum_{l=0}^\infty  \frac{r_<^l}{r^{l+1}_>} P_l(\cos\gamma), \quad \gamma=\arccos\frac{\boldsymbol{x}\cdot\boldsymbol{x'}}{|\boldsymbol{x}\cdot\boldsymbol{x'}|},\  \quad r_< = \min(x,x'), \ r_> = \max(x,x')
$$
$$
P_l(\cos\gamma) = 2\pi \cdot \frac{2}{2l+1} \cdot \sum_{m=-l}^l Y_{l}^{m*}(\theta',\varphi') Y_{l}^m(\theta, \varphi)
$$
Consider a localized charge distribution $\rho(\boldsymbol{x'})$ confined within a volume $V'$. The exact electrostatic potential $\Phi(\boldsymbol{x})$ at an external observation point $\boldsymbol{x}$ (where $r = |\boldsymbol{x}| > r' = |\boldsymbol{x'}|$, hence $r_< = r'$ and $r_> = r$) is given by,
$$
\Phi(\boldsymbol{x}) 
= \frac{1}{4\pi\varepsilon_0} \int_{V'} \frac{\rho(\boldsymbol{x'})}{|\boldsymbol{x}-\boldsymbol{x'}|} \,\mathrm{d}^3x' 
= \frac{1}{4\pi\varepsilon_0} \sum_{l=0}^\infty \frac{1}{r^{l+1}} \int_{V'} \rho(\boldsymbol{x'}) (r')^l P_l(\cos\gamma) \,\mathrm{d}^3x'
$$
- <font color="#ff0000">Monopole Term (Point Charge)</font>. For $l=0$, since $P_0(\cos\gamma) = 1$, the first term simplifies to:
$$
\Phi^{(0)}(\boldsymbol{x}) = \frac{1}{4\pi\varepsilon_0 r} \int_{V'} \rho(\boldsymbol{x'}) \,\mathrm{d}^3x'
= \frac{1}{4\pi\varepsilon_0} \frac{q}{r},
\quad
\text{with }q = \int_{V'} \rho(\boldsymbol{x'}) \,\mathrm{d}^3x'
$$
- <font color="#ff0000">Dipole Term</font>. For $l=1$, since $P_1(\cos\gamma) = \cos\gamma = \frac{\boldsymbol{x}\cdot\boldsymbol{x'}}{r r'}$, the second term becomes:
$$
\Phi^{(1)}(\boldsymbol{x}) 
= \frac{1}{4\pi\varepsilon_0 r^2} \int_{V'} \rho(\boldsymbol{x'}) r' \left( \frac{\boldsymbol{x}\cdot\boldsymbol{x'}}{r r'} \right) \,\mathrm{d}^3x'
= \frac{1}{4\pi\varepsilon_0} \frac{\boldsymbol{p}\cdot\hat{\boldsymbol{r}}}{r^2}
$$
$$
\text{with }
\boldsymbol{p} = \int_{V'} \rho(\boldsymbol{x'}) \boldsymbol{x'} \,\mathrm{d}^3x'
$$
- <font color="#ff0000">Quadrupole Term</font>. For $l=2$, since $P_2(\cos\gamma) = \frac{1}{2}(3\cos^2\gamma - 1)$, substituting $\cos\gamma$ into the expression yields:
$$
\begin{align} 
\Phi^{(2)}(\boldsymbol{x}) 
&= \frac{1}{4\pi\varepsilon_0 r^3} \int_{V'} \rho(\boldsymbol{x'}) (r')^2 \cdot \frac{1}{2}\left[ 3\frac{(\boldsymbol{x}\cdot\boldsymbol{x'})^2}{r^2(r')^2} - 1 \right] \,\mathrm{d}^3x' 
\\[8pt]
&= \frac{1}{8\pi\varepsilon_0 r^5} x_i x_j \int_{V'} \rho(\boldsymbol{x'}) \left[ 3x'_i x'_j - \delta_{ij}(r')^2 \right] \,\mathrm{d}^3x'
\\[8pt]
&= \frac{1}{4\pi\varepsilon_0} \frac{1}{2r^5} \sum_{i,j} D_{ij} x_i x_j
\\[8pt]
&=\frac{{\mathsf{D}:\hat{r}\hat{r}}}{8\mathrm{\pi} \epsilon_0 r^3} 
\end{align}
$$
$$
\text{with }
D_{ij} = \int_{V'} \rho(\boldsymbol{x'}) \left[ 3x'_i x'_j - \delta_{ij}(r')^2 \right] \,\mathrm{d}^3x'
$$
And extending to $l=3, 4, \dots$  yields the octupole ($l=3$), hexadecapole ($l=4$), and more high $2^l$-pole moments $\ldots$  
### 1.3.3 Rotation of harmonics & Wigner $D$-Matrices *
Refer to [[A_symmetry_自然界的对称性/Applications/Appendix for ED formulas#2 Rotation of harmonics & Wigner $D$-Matrices *\|Appendix for ED formulas#2 Rotation of harmonics & Wigner $D$-Matrices *]].
## 1.4 Method: separation of variables  
<span style="color:#ff0000; font-size: 1.2em;">For this section, everyone is advised to review more example problems.</span>
### 1.4.1 Cartesian coordinate system
- The fundamental solution of Laplace's equation $\nabla^2 \varphi = 0$
$$
\frac{{\nabla^2 \varphi}}{\varphi} = \frac{1}{X}\frac{ \mathrm{d}^2 X }{ \mathrm{d} x^2} + \frac{1}{Y}\frac{ \mathrm{d}^2 Y }{ \mathrm{d} y^2} + \frac{1}{Z}\frac{ \mathrm{d}^2 Z }{ \mathrm{d} z^2} = 0
$$
Let:
$$
\frac{1}{X}\frac{ \mathrm{d}^2 X }{ \mathrm{d} x^2} = -k_x^2, \quad \frac{1}{Y}\frac{ \mathrm{d}^2 Y }{ \mathrm{d} y^2} = -k_y^2, \quad \frac{1}{Z}\frac{ \mathrm{d}^2 Z }{ \mathrm{d} z^2} = k_z^2
,\quad
k_z^2 = k_x^2 + k_y^2
$$
> Note: The sign of the separation constant is entirely determined by the boundary conditions: directions bounded in space require a negative sign to yield trigonometric functions that can zero out at both boundaries, while directions extending to infinity require a positive sign to yield exponential functions (such as the wave propagating in the z-direction).  

In directions where the separation constant is negative (e.g., $x, y$),
$$  
X(x) = A \cos(k_x x) + B \sin(k_x x)
$$
In the direction where the separation constant is positive (e.g., $z$),
$$
Z(z) = C \cosh(k_z z) + D \sinh(k_z z)
$$
See the thought from ppt int [[A_symmetry_自然界的对称性/Applications/Appendix for ED formulas#3 Example 2D Laplace Equation in a Rectangular Pipe\|Appendix for ED formulas#3 Example 2D Laplace Equation in a Rectangular Pipe]].

### 1.4.2 Cylindrical coordinate system
- The fundamental solution of Laplace's equation $\nabla^2 \varphi = 0$
$$
\frac{1}{s R}\frac{\mathrm{d}}{\mathrm{d}s}\left(s \frac{\mathrm{d}R}{\mathrm{d}s}\right) + \frac{1}{s^2 \Phi}\frac{\mathrm{d}^2 \Phi}{\mathrm{d}\phi^2} + \frac{1}{Z}\frac{\mathrm{d}^2 Z}{\mathrm{d}z^2} = 0
$$
- $z$-direction equation: $\frac{1}{Z}\frac{\mathrm{d}^2 Z}{\mathrm{d}z^2} = k^2 \implies Z(z) = e^{\pm kz}$ (or monotonic hyperbolic functions)
-  $\phi$-direction equation: $\frac{1}{\Phi}\frac{\mathrm{d}^2 \Phi}{\mathrm{d}\phi^2} = -\nu^2 \implies \Phi(\phi) = A\cos(\nu \phi) + B\sin(\nu \phi)$

> Note: Since $\phi$ possesses a $2\pi$ periodicity in physical space (i.e., $\Phi(\phi) = \Phi(\phi + 2\pi)$), the separation constant $\nu$ must be an integer.

-  $s$-direction equation (Bessel Equation): $\frac{\mathrm{d}^2R}{\mathrm{d}s^2} + \frac{1}{s}\frac{\mathrm{d}R}{\mathrm{d}s} + \left(k^2 - \frac{\nu^2}{s^2}\right)R = 0$

The solutions to this equation are the Bessel functions of the first kind $J_\nu(ks)$  and the Bessel functions of the second kind (Neumann functions) $N_\nu(ks)$ . If the physical domain includes the origin ($s = 0$), the coefficient of $N_\nu(ks)$ must be 0 because $N_\nu(ks) \to -\infty$ as $s \to 0$.  

- Axisymmetric & $z$-Independent Case ($\nu = 0, k = 0$)

The Laplace equation collapses to a 1D ODE:   
$$  
\frac{\mathrm{d}}{\mathrm{d}s}\left(s \frac{\mathrm{d}\varphi}{\mathrm{d}s}\right) = 0 \implies \frac{\mathrm{d}^2 \varphi}{\mathrm{d}s^2} + \frac{1}{s}\frac{\mathrm{d}\varphi}{\mathrm{d}s} = 0   
$$
- $z$-Independent Case (General Solution for $k = 0$): 

The problem reduces to a 2D Laplace equation in polar coordinates, where the radial equation transitions from a Bessel equation to an Euler-Cauchy equation:   
$$   
s^2 \frac{\mathrm{d}^2R}{\mathrm{d}s^2} + s \frac{\mathrm{d}R}{\mathrm{d}s} - \nu^2 R = 0   
$$
the general solution for $k=0$ is obtained by superimposing all possible harmonic components:   
$$  
\varphi(s, \phi) = \underset{\text{as }\nu=0}{\underbrace{A_0 + B_0 \ln s} } + \sum_{\nu=1}^{\infty} \left(A_\nu s^\nu + B_\nu s^{-\nu}\right) \cos(\nu\phi) + \sum_{\nu=1}^{\infty} \left(C_\nu s^\nu + D_\nu s^{-\nu}\right) \sin(\nu\phi)   
$$
### 1.4.3 Spherical coordinate system
In the spherical coordinate system $(r, \theta, \phi)$, Laplace's equation is given by:
$$
\nabla^2 \varphi = \frac{1}{r^2}\frac{\partial}{\partial r}\left(r^2 \frac{\partial \varphi}{\partial r}\right) + \frac{1}{r^2\sin\theta}\frac{\partial}{\partial \theta}\left(\sin\theta \frac{\partial \varphi}{\partial \theta}\right) + \frac{1}{r^2\sin^2\theta}\frac{\partial^2 \varphi}{\partial \phi^2} = 0
$$
Let the solution be $\varphi(r, \theta, \phi) = R(r)\Theta(\theta)\Phi(\phi)$. Usually, the angular parts are combined and expressed in terms of spherical harmonics (See [[A_symmetry_自然界的对称性/杂记/3-D Laplace Equation And Spherical Harmonic Function\|3-D Laplace Equation And Spherical Harmonic Function]]).

- Radial Equation
$$
\frac{\mathrm{d}}{\mathrm{d}r}\left(r^2 \frac{\mathrm{d}R}{\mathrm{d}r}\right) = l(l+1)R \implies R(r) = A r^l + B r^{-(l+1)}
$$
  where $l$ is a non-negative integer.

- Angular Equation
    - Azimuthal angle $\phi$ direction: Similar to the cylindrical system, the solution is $e^{\pm im\phi}$ (where $m$ is an integer, and $|m| \le l$).
    - Polar angle $\theta$ direction: Corresponds to the associated Legendre equation, whose solutions are the associated Legendre polynomials $P_l^m(\cos\theta)$.

- Axisymmetric Systems ($\partial / \partial \phi = 0 \implies m=0$)
$$
\varphi(r, \theta) = \sum_{l=0}^{\infty} \left( A_l r^l + \frac{B_l}{r^{l+1}} \right) P_l(\cos\theta)
$$
- General Case Solution
$$ 
\varphi(r, \theta, \phi) = \sum_{l=0}^{\infty} \sum_{m=-l}^{l} \left( A_{lm} r^l + \frac{B_{lm}}{r^{l+1}} \right) Y_l^m(\theta, \phi)
$$
$$
\left[ \frac{1}{\sin\theta}\frac{\partial}{\partial \theta}\left(\sin\theta \frac{\partial}{\partial \theta} \right) + \frac{1}{\sin^2\theta}\frac{\partial^2 }{\partial \phi^2} \right] Y_l^m = -l(l+1)Y_l^m
,\quad
\frac{\partial^2 }{\partial \phi^2} Y_l^m = -m^2 Y_l^m
$$
### 1.4.4 Green function *  
- Main equation
$$
\nabla^2 \varphi(\boldsymbol{r}) = -\frac{\rho(\boldsymbol{r})}{\epsilon_0}
$$
$$
\nabla^2 G(\boldsymbol{r}, \boldsymbol{r}') = -\frac{\delta(\boldsymbol{r} - \boldsymbol{r}')}{\epsilon_0}
$$
- Fundamental solution in infinite space,
$$ G_0(\boldsymbol{r}, \boldsymbol{r}') = \frac{1}{4\pi\epsilon_0|\boldsymbol{r} - \boldsymbol{r}'|}$$
$$
\varphi(\boldsymbol{r}) = \int \rho(\boldsymbol{r}')G(\boldsymbol{r},\boldsymbol{r}')\,\mathrm{d}^3r'
$$
- With boundaries (Dirichlet condition):

When $\varphi|_S = \varphi_0(\boldsymbol{r})$, and the Green's function satisfies
$$
\nabla^2 G(\boldsymbol{r},\boldsymbol{r}') = -\frac{\delta(\boldsymbol{r}-\boldsymbol{r}')}{\epsilon_0}, \qquad G(\boldsymbol{r},\boldsymbol{r}')|_{\boldsymbol{r}\in S} = 0
$$
then the solution for any volume charge density $\rho$ is,
$$ 
\varphi(\boldsymbol{r}) = \int_V \rho(\boldsymbol{r}') G(\boldsymbol{r},\boldsymbol{r}') \, \mathrm{d}^3r' - \epsilon_0 \oint_S \varphi_0(\boldsymbol{r}') \frac{\partial G(\boldsymbol{r},\boldsymbol{r}')}{\partial n'} \, \mathrm{d}S' 
$$

- With boundaries (Neumann condition):

When $\frac{\partial\varphi}{\partial n}|_S = g(\boldsymbol{r})$, the Neumann Green's function $G_N$ satisfies
$$
\nabla^2 G_N(\boldsymbol{r},\boldsymbol{r}') = -\frac{\delta(\boldsymbol{r}-\boldsymbol{r}')}{\epsilon_0}, \qquad \left.\frac{\partial G_N}{\partial n}\right|_{\boldsymbol{r}\in S} = -\frac{1}{\epsilon_0 S}
$$
the potential is,
$$
\varphi(\boldsymbol{r}) = \int_V \rho(\boldsymbol{r}') G_N(\boldsymbol{r},\boldsymbol{r}') \, \mathrm{d}^3r' + \epsilon_0 \oint_S g(\boldsymbol{r}') G_N(\boldsymbol{r},\boldsymbol{r}') \, \mathrm{d}S' + \langle\varphi\rangle_S
$$
where $\langle\varphi\rangle_S$ is the average potential on the boundary.  

> Refer to [[A_symmetry_自然界的对称性/杂记/Green Function\|Green Function]] for several basic examples in infinite space.
## 1.5 Cases
- If all charges are contained within the sphere $V$ (see [[A_symmetry_自然界的对称性/Applications/Appendix for ED formulas#1 $ iiint_V boldsymbol{E}( boldsymbol{x}) , mathrm{d} 3x = - frac{ boldsymbol{p}}{3 epsilon_0}$\|Appendix for ED formulas#1 $ iiint_V boldsymbol{E}( boldsymbol{x}) , mathrm{d} 3x = - frac{ boldsymbol{p}}{3 epsilon_0}$]] or T 2.3 in the textbook)
$$
\iiint_V \boldsymbol{E}(\boldsymbol{x}) \,\mathrm{d}^3x = -\frac{\boldsymbol{p}}{3\epsilon_0}
$$
- An ellipsoid uniformly charged with Q (in the principal inertia axis frame)  
$$
D_{11} = \frac{Q}{5}(2a_1^2 - a_2^2 - a_3^2), \quad D_{22} = \cdots, \quad D_{i\neq j} = 0
$$
# 2 Magnetostatic Field  
## 2.1 magnetic energy
#todo
## 2.2 Multipole expansion (scalar potential)
### 2.2.1 magnetic scalar potential *
- Without free/conductive current
$$
\nabla \times \boldsymbol{H} = \boldsymbol{J}_f \implies
\nabla \times \boldsymbol{H} = 0, \quad \boldsymbol{H} = -\nabla \psi
$$
then for linear media $\boldsymbol{B} = \mu \boldsymbol{H}$,
$$
\nabla \cdot \boldsymbol{H}=0
\implies
\nabla^2 \psi = 0
$$
Consequently, the multipole expansion can be applied to magnetic scalar potential $\psi$ to derive $\boldsymbol{H}$ as well.  

For a current-carrying coil,  
$$
\psi(\boldsymbol{x}) = -\frac{I}{4\pi} \Omega, \quad \Omega= - \iint_S \frac{{\hat{R}\cdot\mathrm{d}\sigma'}}{R^2}
$$
where $\boldsymbol{S} = \frac{1}{2} \oint_C \boldsymbol{x'} \times \mathrm{d}\boldsymbol{l'}$ is the arbitrary geometric vector area enclosed by the current loop, and $\Omega$ is the solid angle of the surface $S$ with respect to field point $\boldsymbol{x}$.
### 2.2.2 Multipole expansion
- Consider magnetostatic potential expansion at an external observation point $\boldsymbol{x}$, with localized current coil/source $\boldsymbol{J}(\boldsymbol{x'})$ confined within a volume $V'$, and $\boldsymbol{R}=\boldsymbol{x}-\boldsymbol{x'}, r=|\boldsymbol{x}|(field), r'=|\boldsymbol{x'}|(source)$, then
$$
\begin{align} 
\frac{1}{R}=\frac{1}{|\boldsymbol{x}-\boldsymbol{x}'|} = e^{-\boldsymbol{x'}\cdot \nabla} \frac{1}{r} 
&= 
\left[ 1 - \boldsymbol{x'}\cdot \nabla + \cdots \right] \frac{1}{r} 
=\frac{1}{r} - \boldsymbol{x'}\cdot \nabla \frac{1}{r} + \cdots
\end{align}
$$
$$
\Downarrow
$$
$$
\begin{align} 
\psi(\boldsymbol{x}) 
= \frac{I}{4\pi} \iint_S \frac {{\hat{R}\cdot\mathrm{d}\boldsymbol{\sigma}'}} {R^2} 
&= -\frac{I}{4\pi} \iint_S \mathrm{d}\boldsymbol{\sigma}' \cdot \nabla \left( \frac{1}{R} \right) \\[8 pt] 
&= -\frac{I}{4\pi} \left[ \left(\iint_S \mathrm{d}\boldsymbol{\sigma}'\right)\cdot\nabla - \left(\iint_S \mathrm{d}\boldsymbol{\sigma}'\boldsymbol{x}'\right):\nabla\nabla + \cdots \right] \frac{1}{r} \\[8 pt] 
&= \frac {{\boldsymbol{m}\cdot \hat{r}} }{4\mathrm{\pi} r^2} + \frac {{\mathsf{D}_m:\hat{r}\hat{r}} }{8\mathrm{\pi} r^3} + \cdots 
\end{align}
$$
Where there is no magnetic monopole term ($1/r$). $\boldsymbol{m}=I\iint_S \mathrm{d}\boldsymbol{\sigma}'$ is the magnetic dipole moment of the shell (area vector), and $\mathsf{D}_m = I\iint_S \left[ 3(\mathrm{d}\boldsymbol{\sigma}' \boldsymbol{x}' + \boldsymbol{x}' \mathrm{d}\boldsymbol{\sigma}') - 2(\boldsymbol{x}'\cdot\mathrm{d}\boldsymbol{\sigma}')\mathsf{I} \right]$ is the trace-free magnetic quadrupole moment tensor.

- Magnetostatic intensity expansion ($\boldsymbol{H} = -\nabla \psi$)
$$
\boldsymbol{H} = \frac{3(\boldsymbol{m}\cdot\hat{r})\hat{r} - \boldsymbol{m}}{4\mathrm{\pi} r^3} + \frac{{5(\mathsf{D}_m:\hat{r}\hat{r})\hat{r} - 2\mathsf{D}_m\cdot\hat{r}}}{8\mathrm{\pi} r^4} + \cdots
$$
## 2.3 Multipole expansion (vector potential)   
The quadrupole moment of the magnetic field is relatively difficult to calculate and can be skipped. However, the dipole moment needs to be understood.
### 2.3.1 Moment equation for localized current *
Using $\nabla \cdot (\boldsymbol{J}\boldsymbol{r}) = (-\partial_t \rho)\boldsymbol{r} + \boldsymbol{J}$,  
$$
\iiint_V \boldsymbol{J}\,\mathrm{d}V = \dot{\boldsymbol{p}},\quad \boldsymbol{p} = \iiint_V \boldsymbol{r}\,\mathrm{d}q
$$
Using $\nabla \cdot (\boldsymbol{J}\boldsymbol{r}\boldsymbol{r}) = (-\partial_t\rho) \boldsymbol{r}\boldsymbol{r} + \boldsymbol{J}\boldsymbol{r}+\boldsymbol{r}\boldsymbol{J}$,  
$$
\iiint_V \boldsymbol{J}\boldsymbol{r} = \boldsymbol{m}\times \mathsf{I} + \frac{1}{6}\dot{\mathsf{D}} + \frac{1}{6}\dot{g}\mathsf{I}
$$
where $\boldsymbol{m} = \frac{1}{2}\iiint_V (\boldsymbol{r}\times \boldsymbol{J})\,\mathrm{d}V$ is magnetic dipole moment, $\mathsf{D} = \int (3\boldsymbol{r}\boldsymbol{r} - r^2\mathsf{I})\,\mathrm{d}q$ is electric quadrupole moment, and $g = \iiint r^2\,\mathrm{d}q$ is the trace of the second spatial moment of the charge distribution.

for steady current, using $\partial_t \rho = 0$,  
$$
\iiint_V \boldsymbol{J}\,\mathrm{d}V = 0
$$
$$
\iiint_V \boldsymbol{J}\boldsymbol{r}\,\mathrm{d}V = \boldsymbol{m}\times \mathsf{I} \quad \implies \quad \iiint_V J_i r_j \,\mathrm{d}V = -\epsilon_{ijk}m_k
$$
### 2.3.2 Multipole expansion *
- Consider magnetostatic potential expansion at an external observation point $\boldsymbol{x}$, with localized current source $\boldsymbol{J}(\boldsymbol{x'})$ confined within a volume $V'$, and $\boldsymbol{R}=\boldsymbol{x}-\boldsymbol{x'}, r=|\boldsymbol{x}|(field), r'=|\boldsymbol{x'}|(source)$, then
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
\boldsymbol{A}(\boldsymbol{x}) = \frac{\mu_0}{4\mathrm{\pi}}\int_{V'}  \frac{\boldsymbol{J}(\boldsymbol{x'})}{R} \,\mathrm{d}V'
&=
\frac{\mu_0}{4\mathrm{\pi}}\left\{  \frac{1}{r}\int_{V'} \boldsymbol{J}(\boldsymbol{x'})\,\mathrm{d}V' + \frac{1}{r^3} \int_{V'} \boldsymbol{J}(\boldsymbol{x'})\boldsymbol{x'}\,\mathrm{d}V'  \cdot \boldsymbol{x} 
+\frac{1}{6} \int_{V'} \boldsymbol{J}(\boldsymbol{x'}) \left[ (3\boldsymbol{x'}\boldsymbol{x'}-r'^2 \mathsf{I}): \nabla\nabla \frac{1}{r}\right] \,\mathrm{d}V' + \cdots\right\}
\\[8pt]
{\small\color{gray}\text{using Coulomb Gauge}\to}&=
\frac{\mu_0}{4\pi r^3} (\boldsymbol{m}\times\mathsf{I})\cdot \boldsymbol{x} + \frac{\mu_0}{24\pi} \nabla \times \frac{\mathsf{D}_m\cdot\boldsymbol{x}}{r^3} + \cdots
\\[8pt]
&=
\frac{\mu_0}{4\pi r^2} (\boldsymbol{m}\times\hat{r}) - \frac{\mu_0}{8\pi r^3} \hat{r}\times (\mathsf{D}_m\cdot\hat{r}) + \cdots
\end{align}
$$
Where $\boldsymbol{m} = \frac{1}{2}\int_{V'} (\boldsymbol{x'} \times \boldsymbol{J}(\boldsymbol{x'}))\,\mathrm{d}V'$ is the magnetic dipole moment, and $\mathsf{D}_m = \int_{V'} \bigl[(\boldsymbol{x}'\times\boldsymbol{J})\boldsymbol{x}' +\boldsymbol{x}'(\boldsymbol{x}'\times\boldsymbol{J})\bigr]\,\mathrm{d}V'$ is the trace-free magnetic quadrupole moment tensor.

- Magnetostatic intensity expansion
$$
\boldsymbol{B}(\boldsymbol{x}) = \nabla \times \boldsymbol{A}
=\frac{\mu_0}{4\pi r^3} \left[ 3(\boldsymbol{m}\cdot\hat{r})\hat{r} - \boldsymbol{m} \right] + \frac{\mu_0}{8\pi r^4} \left[ {5(\mathsf{D}_m:\hat{r}\hat{r})\hat{r} - 2\mathsf{D}_m\cdot\hat{r}} \right] + \cdots
$$
### 2.3.3 Cases  
- Ring current
$$
\boldsymbol{m} = I \boldsymbol{S}
$$
where $\boldsymbol{S} = \frac{1}{2} \oint_C \boldsymbol{r} \times \mathrm{d}\boldsymbol{l}$ is the geometric vector area enclosed by the current loop.

- Moving point charge, using $\boldsymbol{J}(\boldsymbol{r}) = q \boldsymbol{v} \delta(\boldsymbol{r} - \boldsymbol{r}_e)$,
$$
\boldsymbol{m} = \frac{q}{2m_p} \boldsymbol{L}
$$
where $\boldsymbol{L} = m_p (\boldsymbol{r} \times \boldsymbol{v})$ is the orbital angular momentum.  

- Rotating charged body, using $\boldsymbol{J} = \rho_e (\boldsymbol{\omega} \times \boldsymbol{r})$, and for any rigid body with $\frac{\rho_e}{\rho_m} \equiv \frac{Q}{M}$,
$$
\boldsymbol{m} = \frac{Q}{2M} \boldsymbol{L}
,\quad
\boldsymbol{L} = \int \rho_m(\boldsymbol{r} \times \boldsymbol{v}) \,\mathrm{d}V = I_m \boldsymbol{\omega}
$$
where $I_m$ is the moment of inertia tensor. For a sphere with constant $\rho_e=\frac{Q}{4\pi a^3/3}$, $I_m = \frac{2}{5}M a^2$, thus
$$
\boldsymbol{m}= \frac{1}{5} Qa^2\boldsymbol{\omega}
$$
for a spherical shell with constant $\sigma_e=\frac{Q}{4\pi a^2}$, $I_m = \frac{2}{3}M a^2$, thus
$$
\boldsymbol{m} = \frac{1}{2}\oint(\boldsymbol{r}\times\boldsymbol{K})\,\mathrm{d}\sigma
= \frac{1}{3} Qa^2\boldsymbol{\omega}
$$
- If all currents are contained within the sphere $V$ (see [[A_symmetry_自然界的对称性/Applications/Appendix for ED formulas#1 $ iiint_V boldsymbol{E}( boldsymbol{x}) , mathrm{d} 3x = - frac{ boldsymbol{p}}{3 epsilon_0}$\|Appendix for ED formulas #1 $ iiint_V boldsymbol{E}( boldsymbol{x}) , mathrm{d} 3x = - frac{ boldsymbol{p}}{3 epsilon_0}$]])
$$
\iiint_V \boldsymbol{B}(\boldsymbol{x}) \,\mathrm{d}^3x = \frac{2\mu_0}{3}\boldsymbol{m}
$$
## 2.4 Small current-carrying conductor in magnetic field  
Assuming the spatial size of the current-carrying body $\boldsymbol{x}$ is so small compared with the distance to the source $\boldsymbol{x'}$ which generates the magnetic field that $\nabla\times\boldsymbol{B}_{\text{ext}} = 0$ and $\nabla\cdot\boldsymbol{B}_{\text{ext}}=0$ within the body. Let $\boldsymbol{\xi}$ be the relative coordinate of a current element $\boldsymbol{J}(\boldsymbol{\xi})\,\mathrm{d}V$ from the body's center $\boldsymbol{x}$. The interaction magnetic energy $U=\int \boldsymbol{J}(\boldsymbol{\xi})\cdot\boldsymbol{A}(\boldsymbol{x}+\boldsymbol{\xi})\,\mathrm{d}V$ of the small body is,
$$
U \approx
\boldsymbol{m}\cdot\boldsymbol{B}_{\text{ext}}\Big|_{\boldsymbol{x}} 
+ \frac{1}{6}\,\mathsf{D}_m : \nabla\boldsymbol{B}_{\text{ext}}\Big|_{\boldsymbol{x}} 
+ \cdots
$$
Note that $\boldsymbol{m}=\frac{1}{2}\int (\boldsymbol{\xi}\times\boldsymbol{J}(\boldsymbol{\xi}))\,\mathrm{d}V$ and $\mathsf{D}_m$ are the magnetic dipole and quadrupole moment tensor, which are intrinsic properties of the small current-carrying body itself, not the external source.  

Furthermore, for a system with constant currents, the total magnetostatic force $\boldsymbol{F}$ acting on the small current-carrying body is given by the generalized force relation $\boldsymbol{F} = +\nabla U$ (why use "+"? see [[A_symmetry_自然界的对称性/Applications/Appendix for ED formulas#4 Physical Interpretation of the Sign and Energy Definitions *\|Appendix for ED formulas#4 Physical Interpretation of the Sign and Energy Definitions *]]),
$$
\boldsymbol{F} = +\nabla U
= (\boldsymbol{m}\cdot\nabla)\boldsymbol{B}_{\text{ext}}\Big|_\boldsymbol{x} + \frac{1}{6}(\mathsf{D}_m:\nabla\nabla)\boldsymbol{B}_{\text{ext}}\Big|_\boldsymbol{x} + \cdots 
$$
For a current loop/coil $\boldsymbol{m}=I\boldsymbol{S}$,  
$$
\boldsymbol{m}\cdot\nabla\boldsymbol{B} = I\nabla (\boldsymbol{B}\cdot\boldsymbol{S}) = I\nabla \Phi 
$$
The total force moment $\boldsymbol{N}$ acting on the small current-carrying body about its center $\boldsymbol{x}$ is,  
$$
\boldsymbol{N} = \int \boldsymbol{\xi} \times \left(\boldsymbol{J}(\boldsymbol{\xi}) \times \boldsymbol{B}_{\text{ext}}(\boldsymbol{x}+\boldsymbol{\xi})\right)\,\mathrm{d}V 
=
\boldsymbol{m} \times \boldsymbol{B}_{\text{ext}} + \cdots
$$
# 3 EM Wave  


# 4 Electromagnetic Radiation
## 4.1 Fields of a moving point charge