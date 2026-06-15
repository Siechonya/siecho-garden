---
{"dg-publish":true,"permalink":"/A_symmetry_自然界的对称性/Applications/ED formulas (2)/","noteIcon":"default","created":"2026-06-15T09:49:53.230+08:00","updated":"2026-06-15T23:22:09.521+08:00","dg-note-properties":{}}
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

### 1.3.2 Multipole expansion (Legendre function) *
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
See [[A_symmetry_自然界的对称性/Applications/Appendix for ED formulas#2 Rotation of harmonics & Wigner $D$-Matrices *\|Appendix for ED formulas#2 Rotation of harmonics & Wigner $D$-Matrices *]].
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
### 1.4.4 Green function 
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
the green function above is so-called 1-st Green function, which satisfies symmetric condition,  
$$
G(\boldsymbol{r}, \boldsymbol{r'}) = G(\boldsymbol{r'}, \boldsymbol{r})
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
> Refer to ppt for several basic examples with boundary.   
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
## 2.1 Magnetic energy
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
Where there is no magnetic monopole term ($1/r$). $\boldsymbol{m}=\frac{1}{2}\oint \boldsymbol{x'}\times\,\mathrm{d}\boldsymbol{I}=I\iint_S \mathrm{d}\boldsymbol{\sigma}'$ is the magnetic dipole moment of the shell (area vector), and $\mathsf{D}_m = I\iint_S \left[ 3(\mathrm{d}\boldsymbol{\sigma}' \boldsymbol{x}' + \boldsymbol{x}' \mathrm{d}\boldsymbol{\sigma}') - 2(\boldsymbol{x}'\cdot\mathrm{d}\boldsymbol{\sigma}')\mathsf{I} \right]$ is the trace-free magnetic quadrupole moment tensor.

- Magnetostatic intensity expansion ($\boldsymbol{H} = -\nabla \psi$)
$$
\boldsymbol{H} = \frac{3(\boldsymbol{m}\cdot\hat{r})\hat{r} - \boldsymbol{m}}{4\mathrm{\pi} r^3} + \frac{{5(\mathsf{D}_m:\hat{r}\hat{r})\hat{r} - 2\mathsf{D}_m\cdot\hat{r}}}{8\mathrm{\pi} r^4} + \cdots
$$
## 2.3 Multipole expansion (vector potential)   
The quadrupole moment of the magnetic field is relatively difficult to calculate and can be skipped. However, the dipole moment needs to be understood.
### 2.3.1 Moment equation for localized current
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
\boldsymbol{A}(\boldsymbol{x}) 
&= \frac{\mu_0}{4\mathrm{\pi}}\int_{V'}  \frac{\boldsymbol{J}(\boldsymbol{x'})}{R} \,\mathrm{d}V'
\\[8pt]
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
# 3 Electromagnetic Radiation  
## 3.1 retarded potential  
- Green function for Wave in infinite space
$$
\partial_\beta\partial^\beta A^\alpha = -\mu_0 J^\alpha,\quad  
\text{under gauge }\partial_\alpha = A^\alpha = 0
$$
$$
\implies
\begin{cases} 
\square G(\bar{x}^\mu) = -\delta^4(\bar{x}^\mu)
\\[10pt]
G(\bar{x}^\mu)\large|_{|\bar{x}^{\mu}| \to \infty} = 0
\end{cases}
$$
where $\bar{x^\mu} = x^\mu - x'^\mu$. For the derivation process, refer to [[A_symmetry_自然界的对称性/杂记/Green Function#2.2 运动电荷的推迟势\|Green Function]] or ppt.  

- Retarded potential
$$
A^\mu(\boldsymbol{x}, t) = \frac{\mu_0}{4\pi } \int \frac{J^\mu(\boldsymbol{x'}, {\color{red}t_r})}{|\boldsymbol{x}-\boldsymbol{x'}|} \mathrm{d}^3x'
$$
or,
$$
\varphi (\boldsymbol{x} , t) = \frac{1}{4\pi \epsilon_0} \int \frac{\rho(\boldsymbol{x'}, t_r)}{|\boldsymbol{x}-\boldsymbol{x'}|} \mathrm{d}^3x'
,\quad
\boldsymbol{A}(\boldsymbol{x}, t) = \frac{\mu_0}{4\pi } \int \frac{\boldsymbol{J}(\boldsymbol{x'}, t_r)}{|\boldsymbol{x}-\boldsymbol{x'}|} \mathrm{d}^3x'
$$
where $t_r = t - \frac{R}{c}$ is the retarded time, and $\boldsymbol{R}=\boldsymbol{x}-\boldsymbol{x'}$. These formulas indicate that the potentials at the field point $x^\mu$ are determined by the source distribution $\boldsymbol{J}^\mu$ at an earlier time $t_r$, accounting for the time $\frac{R}{c}$ required for the electromagnetic signal to travel from the source to the field point.  

Note: retarded potential satisfied Lorenz gauge.

- Retarded EMF (Jefimenko formulas)
$$
\boldsymbol{E}(\boldsymbol{x},t) = -\nabla \varphi(\boldsymbol{x}, t) - \frac{ \partial \boldsymbol{A}(\boldsymbol{x},t) }{ \partial t }
=
\frac{1}{4\pi\epsilon_0}\iiint\left( \underset{\text{coulomb}}{\underbrace{\rho_r \frac{\hat{R}}{R^2}} } + \underset{radiation field}{\underbrace{\dot{\rho}_r \frac{\hat{R}}{cR}-\frac{\dot{\boldsymbol{J}_r}}{R}}} \right)\,\mathrm{d} V
$$
$$
\boldsymbol{B}(\boldsymbol{x},t) = \nabla \times \boldsymbol{A}(\boldsymbol{x},t)
= \frac{\mu_0}{4\pi} \iiint \left( \underset{\text{Biot-Savart}}{\underbrace{ \frac{\boldsymbol{J}_r}{R^2} } }+\underset{\text{radiation field}}{\underbrace{\frac{\dot{\boldsymbol{J}_r}}{cR}} }  \right)\times \hat{R} \,\mathrm{d} V
$$
### 3.1.1 Radiation power definition
- Angular radiation power
$$
\frac{ \mathrm{d} P }{ \mathrm{d} \Omega} = r^2S_r = r^2 \cdot\frac{1}{\mu_0} (\boldsymbol{E}_{\text{rad}}\times \boldsymbol{B}_{\text{rad}}) \cdot \hat{r}
$$
- Total radiation power
$$
P = \oint_{\Omega} \frac{ \mathrm{d} P }{ \mathrm{d} \Omega} \,\mathrm{d}\Omega
$$
- Spherical shell integral (useful when calculating $P$). For $\hat{r}=n_i\hat{e}_i$,  
$$
\oint f(n)\,\mathrm{d}\Omega = 
\left\{
\begin{aligned} 
& 4\pi, & f &= 1 \\[6pt]
& 0, & f &= n_i \\[6pt]
& \frac{4\pi}{3}\delta_{ij}, & f &= n_i n_j \\[6pt]
& 0, & f &= n_i n_j n_k \\[6pt]
& \frac{4\pi}{5} \delta_{(ij}\delta_{kl)}, & f &= n_i n_j n_k n_l \quad \left(\text{where } \delta_{(ij}\delta_{kl)} = \frac{1}{3} (\delta_{ij}\delta_{kl} + \delta_{ik}\delta_{jl} + \delta_{il}\delta_{jk})\right) \\[6pt]
& \vdots & & \vdots \\[6pt]
& 0, & f &= n_{i_1} n_{i_2} \dots n_{i_{2m+1}} \\[6pt]
& \frac{4\pi}{2m+1} \delta_{(i_1 i_2} \delta_{i_3i_4} \dots \delta_{i_{2m-1} i_{2m})}, & f &= n_{i_1} n_{i_2} \dots n_{i_{2m}} \\[6pt]
\end{aligned}
\right.
$$
### 3.1.2 Time-varying dipole
- Density
$$
\rho(\boldsymbol{x'},t) = -\boldsymbol{p}(t)\cdot\nabla\delta^3(\boldsymbol{x'}),
\quad 
\boldsymbol{J}(\boldsymbol{x'},t) = \dot{\boldsymbol{p}}(t) \delta^3(\boldsymbol{x'})
$$
- Potential
$$
\boldsymbol{A}(\boldsymbol{x},t) = \frac{\mu_0}{4\pi} \iiint \frac{{\dot{\boldsymbol{p}}(t-R/c) \delta^3(\boldsymbol{x'})}}{R}\,\mathrm{d}V' = \frac{\mu_0}{4\pi} \frac{\dot{\boldsymbol{p}}_r}{r},
\quad
\boldsymbol{p}_r =\boldsymbol{p}(t-r/c)
$$
$$
\varphi(\boldsymbol{x},t) = - \frac{1}{4\pi\epsilon_0} \nabla \cdot \frac{\boldsymbol{p}_r}{r} = \frac{1}{4\pi\epsilon_0} \left( 
\frac{{\boldsymbol{p}_r \cdot \hat{r}}}{r^2} + \frac{\dot{\boldsymbol{p}}_r\cdot\hat{r}}{cr} 
\right)
$$
- EMF ($r>0$)
$$
\left\{
\begin{align} 
\boldsymbol{E} 
&=
\frac{1}{4\pi\epsilon_0}\left[ 
\frac{3(\boldsymbol{p}_r\cdot\hat{r})\hat{r} - \boldsymbol{p}_r}{r^3} + \frac{3(\dot{\boldsymbol{p}}_r\cdot\hat{r})\hat{r} - \dot{\boldsymbol{p}}_r}{cr^2} + \frac{(\ddot{\boldsymbol{p}}_r\cdot\hat{r})\hat{r} - \ddot{\boldsymbol{p}}_r}{c^2r}
\right]
\\[8pt]
\boldsymbol{B}
&=
\frac{\mu_0}{4\pi} \left( 
\frac{\dot{\boldsymbol{p}}_r}{r^2} + \frac{\ddot{\boldsymbol{p}}_r}{cr}
\right) \times \hat{r}
\end{align}
\right.
$$
- Poynting vector (for directional dipole $\boldsymbol{p}(t)=p(t)\hat{z}$)
$$
\boldsymbol{S} = \frac{1}{\mu_0} \boldsymbol{E}\times\boldsymbol{B} \implies
\left\{
\begin{align} 
S_r
&=
\frac{1}{16\pi^2\epsilon_0}\left[ 
\frac{ \mathrm{d}  }{ \mathrm{d} t} \left( 
\frac{p_r^2}{2r^3} + \frac{p_r\dot{p}_r}{cr^2} + \frac{\dot{p}_r^2}{c^2r}
\right) + \frac{\ddot{p}_r^2}{c^3}
\right] \frac{\sin^2\theta}{r^2}
\\[8pt]
S_\theta
&=
-\frac{1}{32\pi^2\epsilon_0} \frac{ \mathrm{d} }{ \mathrm{d} t}\left[\left(
\frac{p_r}{r} + \frac{\dot{p}_r}{c}
\right)^2\right] \frac{\sin2\theta}{r^3}
\\[8pt]
S_\phi
&= 0
\end{align}
\right.
$$
If $p(t) = p_0 \cos(\omega t)$, after long-time averaging, the result is simple,  
$$
\langle S_\theta \rangle = 0,\quad
\langle S_r \rangle = \frac{p_0^2 \omega^4}{32\pi^2 \epsilon_0 c^3} \frac{\sin^2\theta}{r^2}
$$
$$
\left\langle  \frac{ \mathrm{d} P }{ \mathrm{d} \Omega}  \right\rangle  = r^2\langle S_r \rangle = \frac{p_0^2 \omega^4}{32\pi^2 \epsilon_0 c^3} {\sin^2\theta}
$$
- Complex form of resonant dipole
$$
\boldsymbol{p}(t) = \boldsymbol{p}_0 e^{-\mathrm{i}\omega t},\quad \boldsymbol{p}_0=\boldsymbol{p}_{0R}+\mathrm{i}\boldsymbol{p}_{0L}
$$
For example, consider a charge pair $\pm e$ separated by distance $2 a$, rotating anticlockwise around the origin in the $xy$-plane with constant angular frequency $\omega$ so that the positive and negative charges are $\boldsymbol{r}_\pm(t) = \pm a\cos(\omega t)\hat{x} \pm a\sin(\omega t)\hat{y}$, thus  
$$
\boldsymbol{p}(t) = 2ea(\hat{x} + \mathrm{i}\hat{y}) e^{-\mathrm{i}\omega t}
$$
## 3.2 Resonant radiation  
### 3.2.1 Far field approximation
For infinitely far field $\color{red}r'(source)\ll r(field)$, one finds
$$
t_r = t - \frac{R}{c} \approx t-\frac{r}{c} + \frac{r'}{c}(\hat{r}' \cdot \hat{r}) = \tilde{t}_r + \frac{r'}{c}(\hat{r}' \cdot \hat{r})
\triangleq
t^*
$$
$$
\frac{ \partial t_r }{ \partial t }=1,\quad \nabla t_r = - \frac{\hat{r}}{c} + \frac{1}{c} \mathcal{O}\left( \frac{r'}{r} \right)
$$
> Note: In order to  to maintain consistency with the previous sections and avoid confusion, I consistently use $t_r=t-\frac{R}{c}\approx t^*$ to denote the real retarded time and $\tilde{t}_r=t-\frac{r}{c}$ for its leading-order approximation,  rather than $t_r=t-\frac{R}{c}$ before and $t_r=t-\frac{r}{c}$ here in the class.

Consequently, for any field function in the radiation zone of the form $f(\boldsymbol{x}, t) \approx \frac{1}{r} g(t^*)$, where the leading-order term is $\mathcal{O}(1/r)$, its gradient can be expanded as,
$$
\nabla f = \nabla \left( \frac{1}{r} \right) g(t^*) + \frac{1}{r} g'(t^*) \nabla t^* = -\frac{\hat{r}}{r^2} g(t^*) + (\nabla t^*) \partial_t f
$$
By retaining only the dominant $\mathcal{O}(1/r)$ term, we arrive at the operator equivalence,
$$
\nabla \longleftrightarrow -\frac{\hat{r}}{c}\partial_t
$$
$$
\implies
\boxed{
c\boldsymbol{B} = (\partial_t \boldsymbol{A}) \times \hat{r},\quad
\boldsymbol{E} = c\boldsymbol{B} \times \hat{r}
}
$$
![zz_figure/Pasted image 20260612171813.png\|center\|289](/img/user/zz_figure/Pasted%20image%2020260612171813.png)
Ponyting vector can be calculated as, 
$$
\boxed{
\boldsymbol{S} = \frac{c}{\mu_0} B^2 \hat{r} = \epsilon_0 c E^2 \hat{r}
}
$$
### 3.2.2 Resonant radiation  
For resonant radiation  
$$
\boldsymbol{J}(\boldsymbol{x'},t) = \boldsymbol{J}_0(\boldsymbol{x'}) e^{-\mathrm{i} \omega t}
$$
$$
\implies
\boldsymbol{J}(\boldsymbol{x'}, t^*) 
= \boldsymbol{J}_0(\boldsymbol{x'}) e^{\mathrm{i}(kr - \omega t)  -\mathrm{i}\boldsymbol{k}\cdot\boldsymbol{x'}} 
= \boldsymbol{J}(\boldsymbol{x'},t)  e^{\mathrm{i}(kr - \boldsymbol{k}\cdot\boldsymbol{x'})}
= \boldsymbol{J}(\boldsymbol{x'},\tilde{t}_r)  e^{-\mathrm{i}\boldsymbol{k}\cdot\boldsymbol{x'}}
,\quad
\frac{\boldsymbol{k}}{\omega} = \frac{\hat{r}}{c}
$$
$$
\boxed{
\nabla \longleftrightarrow \mathrm{i}\boldsymbol{k} \longleftrightarrow -\frac{\hat{r}}{c}\partial_t,\quad 
\partial_t \longleftrightarrow -\mathrm{i}\omega
}
$$
Vector potential and EMF (by retaining only the dominant $\mathcal{O}(1/r)$ term),
$$
\boldsymbol{A}(\boldsymbol{x},t) = \frac{\mu_0e^{\mathrm{i} k r}}{4\pi r}\iiint \boldsymbol{J}(\boldsymbol{x'},t)e^{-\mathrm{i} \boldsymbol{k}\cdot\boldsymbol{x'}} \,\mathrm{d}^3x'
$$
$$
\boxed{
\langle \boldsymbol{S} \rangle = \frac{1}{2\mu_0} \Re(\boldsymbol{E}^*\times \boldsymbol{B}) =  \frac{c}{2\mu_0} B^2 \hat{r} = \frac{\epsilon_0c}{2} E^2 \hat{r}
}
$$
where $E$ and $B$ denote the field amplitudes with the factor $e^{\mathrm{i}(kr-\omega t)}$ omitted.
#### Aerial radiation  
For a thin antenna of length $l$, the current distribution forms a standing wave given by,
$$
I(t,z) = I_0 \sin(m\pi - k|z|) e^{-\mathrm{i} \omega t},\quad z\in\left[ -\frac{l}{2}, \frac{l}{2} \right], \ m\triangleq \frac{l}{2\pi/k} = \frac{l}{\lambda}
$$
Vector potential and EMF (by retaining only the dominant $\mathcal{O}(1/r)$ term),  
$$
\boldsymbol{A}(\boldsymbol{x},t) = \frac{\mu_0e^{\mathrm{i} k r}}{4\pi r}\int_{-l/2}^{l/2}\hat{z} I(t,z')e^{-\mathrm{i} kz'\cos\theta} \,\mathrm{d}z'
= \frac{\mu_0I_0e^{\mathrm{i}(kr-\omega t)}}{2\pi kr} \frac{g(\theta)}{\sin\theta} \hat{z},
\quad g(\theta) = \frac{{\cos(m\pi\cos\theta) - \cos (m\pi)}}{\sin\theta}
$$
$$
\boldsymbol{E} = -\mathrm{i} \frac{\mu_0cI_0}{2\pi } \frac{e^{\mathrm{i}(kr-\omega t)}}{r}g(\theta)\hat{\theta},\quad
c\boldsymbol{B} = E\hat{\phi},\quad
\text{linear polarization}
$$
$$
\langle \boldsymbol{S} \rangle =   \frac{\epsilon_0c}{2} E^2 \hat{r} = \frac{\mu_0cI_0^2}{8\pi^2} \frac{g^2(\theta)}{r^2}\hat{r}
$$
 
- Definition: resistance of antenna ($R_\text{rad}$)
$$
\langle P\rangle = \frac{1}{2} I_{\max}^2 R_{\text{rad}}
$$
for short antenna discussed above with $m\ll 1$,
$$
R_{\text{rad}} \approx 20\pi^2 m^2
$$
### 3.2.3 Small source approximation  
Approximation Regime: localized, long-wavelength source in the radiation zone $\color{red}r'(source)\ll\lambda\ll r(field)$ with $\lambda=\frac{2\pi}{k}$ is the wavelength of the radiation. This implies that $\boldsymbol{k}\cdot \boldsymbol{x'}\sim \frac{x'}{\lambda} \ll 1$ and we can taylor-expand $e^{-\mathrm{i} \boldsymbol{k}\cdot\boldsymbol{x'}}$ to obtain,
$$
\begin{align} 
\boldsymbol{A}(\boldsymbol{x},t) 
&= \frac{\mu_0e^{\mathrm{i} k r}}{4\pi r}\iiint \boldsymbol{J}(\boldsymbol{x'},t)e^{-\mathrm{i} \boldsymbol{k}\cdot\boldsymbol{x'}} \,\mathrm{d}^3x'
\\[8pt]&=
\frac{\mu_0 e^{\mathrm{i} k r}}{4\pi r} \left[ \dot{\boldsymbol{p}}(t) + \frac{1}{c}\dot{\boldsymbol{m}}(t) \times \hat{r} + \frac{1}{6c}\hat{r}\cdot\ddot{\mathsf{D}}(t) + \cdots \right]
\\[8pt]&=
\frac{\mu_0}{4\pi r} \left[ \partial_t{\boldsymbol{p}}(\tilde{t}_r) + \frac{1}{c}\partial_t{\boldsymbol{m}}(\tilde{t}_r) \times \hat{r} + \frac{1}{6c}\hat{r}\cdot\partial_t^2{\mathsf{D}}(\tilde{t}_r) + \cdots \right]
\end{align}
$$
$$
\boldsymbol{p} = \int \boldsymbol{x'}\,\mathrm{d}q,\quad 
\boldsymbol{m}=\frac{1}{2}\oint \boldsymbol{x'}\times\,\mathrm{d}\boldsymbol{I}, \quad
\mathsf{D} = \int (3\boldsymbol{x'}\boldsymbol{x'} - r'^2\mathsf{I})\,\mathrm{d}q
$$
#### Electric dipole radiation  
- Potential and EMF
$$
\boldsymbol{A}(\boldsymbol{x},t) = \frac{\mu_0e^{\mathrm{i} kr}}{4\pi r} \dot{\boldsymbol{p}}(t)
\implies
\left\{
\begin{align} 
c\boldsymbol{B} &= \frac{\mu_0e^{\mathrm{i} kr}}{4\pi r} \ddot{\boldsymbol{p}}(t) \times \hat{r}
\\[8pt]
\boldsymbol{E} &= c\boldsymbol{B} \times \hat{r}
\end{align}
\right.
$$
- Radiation
$$
\langle \boldsymbol{S} \rangle =  \frac{c}{2\mu_0} B^2 \hat{r} = \frac{\mu_0}{32\pi^2c} \frac{|\ddot{\boldsymbol{p}} \times \hat{r}|^2}{ r^2}
,\quad
\langle P\rangle = \oint |\langle\boldsymbol{S}\rangle|r^2\,\mathrm{d}\Omega
=\frac{\mu_0}{12\pi c} |\ddot{\boldsymbol{p}}|^2
$$
where $|\ddot{\boldsymbol{p}} \times \hat{r}|$ and $|\ddot{\boldsymbol{p}}|$ denote the amplitudes with the factor $e^{-\mathrm{i}\omega t}$ omitted.  

For example, a directional dipole $\boldsymbol{p}(t) = p_0 e^{-\mathrm{i} \omega t} \hat{z}$ 
$$
c\boldsymbol{B} = -\frac{\mu_0\omega^2p_0}{4\pi r}\sin\theta e^{\mathrm{i}(kr-\omega t)} \hat{\phi},\quad
\boldsymbol{E} = cB \hat{\theta}
$$
$$
\langle \boldsymbol{S} \rangle = \frac{\mu_0 p_0^2 \omega^4}{32\pi^2 c} \frac{\sin^2\theta}{r^2} \hat{r}
,\quad
\langle P\rangle = \frac{\mu_0}{12\pi c}  p_0^2 \omega^4
$$
#### Magnetic dipole radiation  
- Potential and EMF
$$
\boldsymbol{A}(\boldsymbol{x},t) = \frac{\mu_0e^{\mathrm{i} kr}}{4\pi c r} \dot{\boldsymbol{m}}(t) \times \hat{r}
\implies
\left\{
\begin{align} 
\boldsymbol{E} &= -\frac{\mu_0e^{\mathrm{i} kr}}{4\pi c r} \ddot{\boldsymbol{m}}(t) \times \hat{r}
\\[8pt]
c\boldsymbol{B} &= \hat{r} \times \boldsymbol{E}
\end{align}
\right.
$$
- Radiation
$$
\langle \boldsymbol{S} \rangle =  \frac{c}{2\mu_0} B^2 \hat{r} = \frac{\mu_0}{32\pi^2c^3} \frac{|\ddot{\boldsymbol{m}} \times \hat{r}|^2}{ r^2} \hat{r}
,\quad
\langle P\rangle = \frac{\mu_0}{12\pi c^3} |\ddot{\boldsymbol{m}}|^2
$$
where $|\ddot{\boldsymbol{m}} \times \hat{r}|$ and $|\ddot{\boldsymbol{m}}|$ denote the amplitudes with the factor $e^{-\mathrm{i}\omega t}$ omitted.  

For example, a directional dipole $\boldsymbol{m}(t) = m_0 e^{-\mathrm{i} \omega t} \hat{z}$ 
$$
\boldsymbol{E} = \frac{\mu_0\omega^2m_0}{4\pi c r}\sin\theta e^{\mathrm{i}(kr-\omega t)} \hat{\phi},\quad
c\boldsymbol{B} = E \hat{\theta}
$$
$$
\langle \boldsymbol{S} \rangle = \frac{\mu_0 m_0^2 \omega^4}{32\pi^2 c^3} \frac{\sin^2\theta}{r^2} \hat{r}
,\quad
\langle P\rangle = \frac{\mu_0}{12\pi c^3}  m_0^2 \omega^4
$$
#### Electric quadruple radiation *
- Potential and EMF
$$
\boldsymbol{A}(\boldsymbol{x},t) 
=
\frac{\mu_0 e^{\mathrm{i} k r}}{24\pi c r} \hat{r}\cdot\ddot{\mathsf{D}}(t)
\implies
\left\{
\begin{align} 
c\boldsymbol{B} &= 
\frac{\mu_0e^{\mathrm{i} kr}}{24\pi c r} \hat{r} \cdot \dddot{\mathsf{D}} \times \hat{r}
\\[8pt]
\boldsymbol{E} &= c\boldsymbol{B} \times \hat{r}
\end{align}
\right.
$$
- Radiation

$$
\langle \boldsymbol{S} \rangle =  \frac{c}{2\mu_0} B^2 \hat{r} = \frac{\mu_0}{1152\pi^2c^3} \frac{|\hat{r} \cdot \dddot{\mathsf{D}} \times \hat{r}|^2}{ r^2} \hat{r}
,\quad
\langle P\rangle = \frac{\mu_0}{1440\pi c^3} |\dddot{\mathsf{D}}|^2
$$
where $|\hat{r} \cdot \dddot{\mathsf{D}} \times \hat{r}|$ and $|\dddot{\mathsf{D}} |$ denote the amplitudes with the factor $e^{-\mathrm{i}\omega t}$ omitted.  

For example, a planar quadrupole in the $xy$-plane with $\mathsf{D}(t) = \mathsf{D}_0 e^{-\mathrm{i} \omega t}$, where the only non-zero components are $D_{xx} = -D_{yy} = Q_0$,
$$
c\boldsymbol{B} = -\frac{\mathrm{i}\mu_0\omega^3Q_0}{24\pi c r}\sin\theta \left[ \sin(2\phi) \hat{\theta} + \cos\theta \cos(2\phi) \hat{\phi} \right] e^{\mathrm{i}(kr-\omega t)},\quad 
\boldsymbol{E} = -\frac{\mathrm{i}\mu_0\omega^3Q_0}{24\pi c r}\sin\theta \left[ \cos\theta \cos(2\phi) \hat{\theta} - \sin(2\phi) \hat{\phi} \right] e^{\mathrm{i}(kr-\omega t)}
$$
$$
\langle \boldsymbol{S} \rangle = \frac{\mu_0 Q_0^2 \omega^6}{1152\pi^2 c^3} \frac{\sin^2\theta \left[1 - \sin^2\theta\cos^2(2\phi)\right]}{r^2} \hat{r} ,\quad \langle P\rangle = \frac{\mu_0}{720\pi c^3} Q_0^2 \omega^6
$$
## 3.3 Moving point charge  
- Intensity
$$
J^{\alpha}(x^\mu)= ec \int u^{\alpha}(\tau) \delta^{4}(x^\mu-x^\mu_e(\tau)) \,\mathrm{d} \tau = (\rho c, \boldsymbol{J})
$$
$$
\rho(\boldsymbol{x}, t) = e\delta^3(\boldsymbol{x}-\boldsymbol{x}_e(t)),\quad
\boldsymbol{J}(\boldsymbol{x}, t) = e\boldsymbol{v}(t) \delta^3(\boldsymbol{x}-\boldsymbol{x}_e(t))
$$
### 3.3.1 Liénard-Wiechert formulas  
- Liénard-Wiechert potential  
$$
\varphi (\boldsymbol{x} , t) 
=
\frac{1}{4\pi \epsilon_0} \int \frac{\rho(\boldsymbol{x}', t_r)}{|\boldsymbol{x}-\boldsymbol{x'}|} \mathrm{d}^3x'
=
\frac{e}{4\pi \epsilon_0} \left. \frac{ 1 }{ R \left( 1 -\hat{R}\cdot\boldsymbol{\beta} \right) }\right|_{t_r},
\quad
\text{where } t_r = t-\frac{|\boldsymbol{x}-\boldsymbol{x}_e(t_r)|}{c}
$$
$$
\boldsymbol{A}(\boldsymbol{x}, t) = \frac{\mu_0}{4\pi } \int \frac{\boldsymbol{J}(\boldsymbol{x'}, t_r)}{|\boldsymbol{x}-\boldsymbol{x'}|} \mathrm{d}^3x'
=\frac{\boldsymbol{\beta}(t_r)}{c} \varphi(\boldsymbol{x},t)
$$
> proof ? see [[A_symmetry_自然界的对称性/Applications/Appendix for ED formulas#5 Liénard-Wiechert potential\|Appendix for ED formulas#5 Liénard-Wiechert potential]] 

- Liénard-Wiechert EMF 
$$
\begin{align} 
\boldsymbol{E}(\boldsymbol{x}, t) 
&= \frac{e}{4\pi \epsilon_0 (1 -\hat{R}\cdot\boldsymbol{\beta} )^3 } 
\left[ \frac{\hat{R} - \boldsymbol{\beta}}{\gamma^2 R^2 } + \frac{\hat{R} \times \left( (\hat{R} - \boldsymbol{\beta}) \times \dot{\boldsymbol{\beta}} \right)}{c R } \right]_{t_r}
\\[8pt]
c\boldsymbol{B}(\boldsymbol{x}, t) 
&= \hat{R} \times \boldsymbol{E}(\boldsymbol{x}, t)
\end{align}
$$
where $R = |\boldsymbol{x} - \boldsymbol{x}_e(t_r)|$. The first term scales as $\mathcal{O}(1/R^2)$ (velocity field $\boldsymbol{E}_v$), while the second term scales as $\mathcal{O}(1/R)$ (acceleration/radiation field $\boldsymbol{E}_{rad}$).
### 3.3.2 EMF of uniformly moving point charge  
$$
\begin{aligned}
\boldsymbol{E}(\boldsymbol{x}, t) 
&= \frac{e}{4\pi\epsilon_0}
\frac{1-\beta^2}{\bigl(1-\beta^2\sin^2\theta\bigr)^{3/2}}
\frac{\hat{R}(t)}{R^2} 
\\[8pt]
c\boldsymbol{B}(\boldsymbol{x}, t)
&= \boldsymbol{\beta}\times\boldsymbol{E}
\end{aligned}
$$
where $\theta=\left\langle \boldsymbol{R}(t),\boldsymbol{\beta}\right\rangle = \left\langle \hat{R}(t_r)-\boldsymbol{\beta}, \boldsymbol{\beta} \right\rangle$ is the angle between present position $\boldsymbol{R}(t)$ and the velocity. However, this form is seldom used in practical radiation problems as the total radiated power of the field is zero.
### 3.3.3 Radiation of moving point charge  
Radiation field  $\boldsymbol{E}_{rad}, \boldsymbol{B}_{rad}, \hat{R}(t_r)$ form a right-handed orthogonal triad, thus
$$
\boldsymbol{S}(\boldsymbol{x}, t) = \frac{1}{\mu_0} \boldsymbol{E}_{rad} \times \boldsymbol{B}_{rad} = \epsilon_0 c E_{rad}^2 \hat{R}(t_r)
$$
$$
\frac{ \mathrm{d} P }{ \mathrm{d} \Omega} = \frac{ \mathrm{d} W_{rad} }{ \mathrm{d} t_r \mathrm{d}\Omega} = \frac{ \mathrm{d} W_{rad} }{ \mathrm{d} t \mathrm{d}\Omega} \frac{ \partial t }{ \partial t_r }
=
SR^2(t_r)(1-\hat{R}(t_r)\cdot\boldsymbol{\beta})
$$
#### Non-Relativistic Limit $\beta \ll 1$
For the non-relativistic limit ($\beta \ll 1$), $1-\hat{R}(t_r)\cdot\boldsymbol{\beta}\approx 1$ and $\left|\hat{R} \times \left( (\hat{R} - \boldsymbol{\beta}) \times \dot{\boldsymbol{\beta}} \right)| \approx \frac{1}{c}|\hat{R}\times \boldsymbol{a}\right| = \frac{a}{c}\sin\theta$, $\theta=\left\langle \hat{R}(t_r), \boldsymbol{\beta}\right\rangle \approx \left\langle \hat{R}(t), \boldsymbol{\beta}\right\rangle$. This reduces directly to <font color="#245bdb">Larmor's formula</font>,
$$
\frac{ \mathrm{d} P }{ \mathrm{d} \Omega} = \frac{\mu_0e^2}{16\pi^2c} a^2\sin^2\theta,\quad
P = \oint \frac{ \mathrm{d} P }{ \mathrm{d} \Omega}\,\mathrm{d}\Omega = \frac{\mu_0 e^2 }{6\pi c} a^2
$$
> Note: This result is consistent with the instantaneous electric-dipole radiation formula for a single charge. By identifying the dipole moment as $\boldsymbol{p}=e\boldsymbol{x}_e$ (hence $\ddot{\boldsymbol{p}}=e\boldsymbol{a}$), the total power $P=\frac{\mu_0}{6\pi c} |\ddot{\boldsymbol{p}}|^2$ yields identical results. 

#### Relativistic Case $\beta \in (0,1)$
For $\boldsymbol{\beta}\parallel\boldsymbol{a}$ ($\boldsymbol{a}=a_\parallel \hat{a}$), let $\theta=\left\langle \hat{R}(t_r), \boldsymbol{\beta}\right\rangle$. The angular radiation distribution becomes,
$$
\frac{ \mathrm{d} P_\parallel }{ \mathrm{d} \Omega} = 
\frac{\mu_0 e^2 a_\parallel^2}{16\pi^2 c} \frac{\sin^2\theta}{(1 - \beta \cos\theta)^5}
,\quad
P_\parallel = \frac{\mu_0 e^2}{6\pi c} \gamma^6 a_\parallel^2
$$
As $\beta \to 1$ (a bit like $\theta\to 0$), the denominator concentrates the radiation into a sharp forward cone with a characteristic opening angle of $\theta_{\max} \approx \frac{1}{2\gamma}$.   

For $\boldsymbol{\beta} \perp \boldsymbol{a}$ ($\boldsymbol{a}=a_\perp \hat{e}_x,\, \boldsymbol{\beta}=\beta \hat{e}_z$),
$$
\frac{ \mathrm{d} P_\perp }{ \mathrm{d} \Omega} = \frac{\mu_0 e^2 a_\perp^2}{16\pi^2 c} \frac{1}{(1 - \beta \cos\theta)^3} \left[ 1 - \frac{\sin^2\theta \cos^2\phi}{\gamma^2 (1 - \beta \cos\theta)^2} \right]
,\quad
P_\perp = \frac{\mu_0 e^2}{6\pi c} \gamma^4 a_\perp^2 
$$
where $\phi$ is the azimuthal angle. In the ultrarelativistic limit $\beta\to 1$, this expression describes the <font color="#245bdb">synchrotron radiation</font>.  

The angular radiation distributions for the three conditions discussed above are illustrated below,
![zz_figure/Pasted image 20260612160253.png\|center\|831](/img/user/zz_figure/Pasted%20image%2020260612160253.png)  

The fully relativistic generalization (Liénard's formula), is given by  
$$
\frac{ \mathrm{d} P }{ \mathrm{d} \Omega} = \frac{ \mathrm{d} P_\parallel }{ \mathrm{d} \Omega} + \frac{ \mathrm{d} P_\perp }{ \mathrm{d} \Omega} + \frac{\mu_0 e^2 a_\parallel a_\perp}{8\pi^2 c} \frac{(\beta-\cos\theta)\sin\theta\cos\phi}{(1-\beta\cos\theta)^5}
$$
$$
P = P_\parallel +P_\perp 
= \frac{\mu_0 e^2}{6\pi c} \gamma^4\left[ a^2_\perp + \gamma^2 a^2_\parallel \right] 
= \frac{\mu_0 e^2}{6\pi c} \gamma^6\left[ a^2 - \left| {\boldsymbol{\beta} \times \boldsymbol{a}}\right|^2 \right] 
$$
#### 4-radiation momentum *
Refer to [[A_symmetry_自然界的对称性/Applications/ED Formulas#Primary 4-vector / tensor\|ED Formulas#Primary 4-vector]], you could find $P=\frac{\mu_0 e^2}{6\pi c} a^\mu a_\mu$, which is a Lorentz invariant.  

In the particle's instantaneous rest frame, the radiation carries away non-zero energy ($\mathrm{d}E_{\text{rad}} = P \mathrm{d}\tau$) but zero 3-momentum ($\mathrm{d}\boldsymbol{P}_{\text{rad}} = 0$). Thus,  
$$
\left.\frac{\mathrm{d}P^\alpha_{\text{rad}}}{\mathrm{d}\tau}\right|_{rest} = (P/c, 0)  
$$
Covariantly transfer to the laboratory frame yields, 
$$
\frac{\mathrm{d} P^\alpha_{\text{rad}} }{\mathrm{d} \tau} 
= 
\begin{pmatrix} 
\gamma & \gamma \boldsymbol{\beta} \\ \gamma \boldsymbol{\beta} & \mathsf{I} + (\gamma-1) \hat{\beta}\hat{{\beta}}
\end{pmatrix}
\begin{pmatrix} 
{P}/{c}  \\[3pt] 0
\end{pmatrix}
= \frac{P}{c^2} u^\alpha = \frac{\mu_0 e^2}{6\pi c^3} (a^\mu a_\mu) u^\alpha
$$
#### Lorentz Transformation of $\frac{ \mathrm{d} P }{ \mathrm{d} \Omega}$ *
Let $K$ be the laboratory frame and $K'$ be the instantaneous rest frame of the moving particle. Let $\frac{\mathrm{d}P}{\mathrm{d}\Omega}$ denote the angular radiation power emitted per retarded time in $K$, and $\frac{\mathrm{d}P'}{\mathrm{d}\Omega'}$ in $K'$. The angular distribution transforms as,
$$
\frac{\mathrm{d}P}{\mathrm{d}\Omega} = \frac{1}{\gamma^4 (1 - \beta \cos\theta)^3} \frac{\mathrm{d}P'}{\mathrm{d}\Omega'} = \gamma^2 (1 - \beta \cos\theta')^3 \frac{\mathrm{d}P'}{\mathrm{d}\Omega'}
$$
where $\theta$ (or $\theta'$) is the angle between the velocity $\boldsymbol{\beta}$ and the direction of observation in $K$ (or $K'$).   

> proof ? see [[A_symmetry_自然界的对称性/Applications/Appendix for ED formulas#6 Lorentz Transformation of the Angular Distribution of Emitted Radiation Power\|Appendix for ED formulas#6 Lorentz Transformation of the Angular Distribution of Emitted Radiation Power]]

#### Radiation damping *
- EM mass of particles

An accelerating charged particle interacts with its own self-field. In the non-relativistic limit, this defines the electromagnetic mass in terms of the electrostatic self-energy $W_0$ of the charge distribution,
$$
m_{\text{em}} = \frac{4}{3}\frac{W_0}{c^2}
$$
The rest energy of electron is $W_0=\frac{1}{2} \frac{e^2}{4\pi\epsilon_0r_0}$ for the surface charge shell model, and $W_0=\frac{3}{5} \frac{e^2}{4\pi\epsilon _0 r_ 0}$ for the uniformly charged sphere model. Hence, the observed physical mass $m$ becomes,
$$
m = m_0 + m_{\text{em}}
$$
If we assume that the observed mass of electron is entirely electromagnetic (setting $m_0 = 0$), we could define the classical electron radius $r_0$ after ignoring model-dependent geometric factors of order unity,
$$
r_e \sim \frac{e^2}{4\pi\epsilon_0 m c^2} \approx 2.818 \times 10^{-15} \,\text{m}\quad
\text{namely } \frac{e^2}{4\pi\epsilon_0r_0} \approx m c^2
$$
> Why not $W_0=mc^2$? see [[A_symmetry_自然界的对称性/Applications/Appendix for ED formulas#7 The $4/3$ paradox and Poincaré stresses\|Appendix for ED formulas#7The $4/3$ paradox and Poincaré stresses]]


- Radiation damping
  
To account for the continuous radiation of 4-momentum, a self-force term $F^\mu_{\text{rad}}$ must be incorporated into the particle's relativistic equation of motion. This yields the Abraham-Lorentz equation, 
$$
m \frac{\mathrm{d}u^\alpha}{\mathrm{d}\tau} = F^\alpha_{\text{ext}} + F^\alpha_{\text{rad}}
$$
By demanding the kinematic consistency condition $u_\alpha F^\alpha_{\text{rad}} = 0$, the covariant radiation reaction force is derived as,
$$
F^\alpha_{\text{rad}} = \frac{\mu_0 e^2}{6\pi c} \left( \frac{\mathrm{d}a^\alpha}{\mathrm{d}\tau} - \frac{1}{c^2} (a^\mu a_\mu) u^\alpha \right)
$$
In the instantaneous rest frame of the particle (or, approximately, for non-relativistic particles as seen in the lab frame), where $u^\alpha = (c,0)$, $a^\alpha = (0,\boldsymbol{a})$, and $\frac{\mathrm{d}a^\alpha}{\mathrm{d}\tau} = (0,\dot{\boldsymbol{a}})$, the radiation reaction force decomposes into the time and spatial components,
$$
F^0_{\text{rad}} = -\frac{\mu_0 e^2}{6\pi c^2}\,|\boldsymbol{a}|^2, \qquad
\boldsymbol{F}_{\text{rad}} = \frac{\mu_0 e^2}{6\pi c}\,\dot{\boldsymbol{a}} .
$$
The time component $F^0_{\text{rad}}$ gives the irreversible radiated power $cF^0_{\text{rad}} = -\frac{\mu_0 e^2}{6\pi c}|\boldsymbol{a}|^2$, reproducing the Larmor formula. The spatial component is precisely the Schott term, which has no time component in this frame and hence does no work. It encodes a reversible energy exchange with the near-zone induction fields, which can return energy to the particle when the acceleration $\boldsymbol{a}$ changes.
# 4 Electromagnetic waves
## 4.1 EM waves in the medium  
### 4.1.1 Waves equation
- The constitutive relations for a homogeneous, isotropic, lossless linear medium, are  
$$
\boldsymbol{D} = \epsilon \boldsymbol{E}, \quad \boldsymbol{B} = \mu \boldsymbol{H}
$$
- Maxwell equations in the absence of free sources ($\rho_f = 0$, $\mathbf{J}_f = 0$)
$$
\nabla \cdot \boldsymbol{D} = 0,\quad \nabla \cdot \boldsymbol{B} = 0,\quad 
\nabla \times \boldsymbol{E} = -\frac{\partial \boldsymbol{B}}{\partial t},\quad 
\nabla \times \boldsymbol{H} = \frac{\partial \boldsymbol{D}}{\partial t}
$$
- The wave equation
$$
\left( \nabla^2 - \mu\epsilon \, \frac{\partial^2}{\partial t^2} \right) \left\{\begin{matrix} \boldsymbol{E} \\ \boldsymbol{B}\end{matrix}\right\}= 0
$$
The phase and group velocity are,  
$$
v = \frac{1}{\sqrt{\mu\epsilon}} = \frac{c}{n},\quad 
\text{with }
n \equiv \frac{c}{v} = \sqrt{\frac{\mu\epsilon}{\mu_0\epsilon_0}} = \sqrt{\mu_r \epsilon_r}
$$
We usually consider non‑magnetic media ($\mu_r \approx 1$). One has $n \approx \sqrt{\epsilon_r}$.

- Monochromatic plane‑wave solution
$$
\begin{align} 
\boldsymbol{E}(\boldsymbol{r},t) &= \boldsymbol{E}_0 \, e^{\mathrm{i}(\boldsymbol{k}\cdot\boldsymbol{r} - \omega t)} = \boldsymbol{E}_0 e^{i k_\mu x^\mu}
\quad (\text{physical fields are the real part})
\\[4pt]
\boldsymbol{H}(\boldsymbol{r}, t) &= \frac{1}{\omega\mu} \boldsymbol{k}\times\boldsymbol{E},\quad k^2 = \mu\epsilon \, \omega^2
\end{align}
$$
define the intrinsic impedance $Z = \frac{{\omega \mu}}{k} = \sqrt{\frac{\mu}{\epsilon}}$, so $\boldsymbol{H} = \frac{\hat{k}\times\boldsymbol{E}}{Z}$.

- The invariant square of the wave vector $k^\mu = (\omega/c, \boldsymbol{k})$ 
$$
k^\mu k_\mu = \frac{\omega^2}{c^2}\bigl(n^2 - 1\bigr)
$$
In vacuum $n=1$ and $k^\mu k_\mu = 0$, while inside a typical dielectric $n>1$, the wave vector is spacelike ($k^\mu k_\mu > 0$), corresponding to a subluminal phase speed.  
### 4.1.2 Energy (flow)  
- Electromagnetic energy and energy flow  
$$
\begin{align} 
w &= \frac{1}{2}\epsilon\,|\Re(\boldsymbol{E})|^2 + \frac{1}{2}\mu\,|\Re(\boldsymbol{H})|^2 = \epsilon\,|\Re(\boldsymbol{E})|^2 = \mu\,|\Re(\boldsymbol{H})|^2
\\[4pt]
\boldsymbol{S} &= \Re(\boldsymbol{E})\times\Re(\boldsymbol{H}) = \sqrt{\frac{\epsilon}{\mu}} |\Re(\boldsymbol{E})|^2 = wv_\text{p}\hat{k}
\end{align}
$$
The energy transport velocity $\boldsymbol{v} \triangleq |\boldsymbol{S}|/ w$ equals the phase velocity $v_\text{p} = c/n$, which means the energy flows with the wave.

- Average energy and energy flow  
$$
\langle w \rangle = \frac{1}{2}\epsilon\,|\boldsymbol{E}_0|^2 = \frac{1}{2}\epsilon\,\boldsymbol{E}_0^* \cdot \boldsymbol{E}_0
,\quad 
\langle \boldsymbol{S} \rangle = \frac{1}{2}\sqrt{\frac{\epsilon}{\mu}} |\boldsymbol{E}_0|^2 \hat{k} = \langle w\rangle v_\text{p}\hat{k}
$$
### 4.1.3 Scattering and absorption of waves
## 4.2 EM waves on the surface of the medium  
Let medium 1 ($z<0$) and medium 2 ($z>0$) be homogeneous, isotropic, lossless linear dielectrics with parameters $\epsilon_1,\mu_1$ and $\epsilon_2,\mu_2$. The planar interface is the $z=0$ plane, with unit normal $\hat{n}=\hat{z}$ pointing into medium 2. A monochromatic plane wave of angular frequency $\omega$ is incident from medium 1.

### 4.2.1 Laws of reflection and refraction 
- Incident, reflected, and transmitted waves  
$$
\begin{align}
\boldsymbol{E}_i(\boldsymbol{r},t) &= \boldsymbol{E}_{0i}\, e^{\mathrm{i}(\boldsymbol{k}_i\cdot\boldsymbol{r} - \omega t)} \\[4pt]
\boldsymbol{E}_r(\boldsymbol{r},t) &= \boldsymbol{E}_{0r}\, e^{\mathrm{i}(\boldsymbol{k}_r\cdot\boldsymbol{r} - \omega t)} \\[4pt]
\boldsymbol{E}_t(\boldsymbol{r},t) &= \boldsymbol{E}_{0t}\, e^{\mathrm{i}(\boldsymbol{k}_t\cdot\boldsymbol{r} - \omega t)}
\end{align}
$$
with $|\boldsymbol{k}_i| = |\boldsymbol{k}_r| = k_1 = n_1\omega/c$, $|\boldsymbol{k}_t| = k_2 = n_2\omega/c$, and $n_j = \sqrt{\mu_j\epsilon_j/\mu_0\epsilon_0}$. The corresponding magnetic fields are $\boldsymbol{H}_j = (\omega\mu_j)^{-1}\boldsymbol{k}_j\times\boldsymbol{E}_j$ ($j=i,r,t$).

- Boundary condition
$$
\hat{{n}} \times (\boldsymbol{E}_2 - \boldsymbol{E}_1) = 0,\quad
\hat{{n}} \times (\boldsymbol{H}_2 - \boldsymbol{H}_1) = 0
$$
$$
\implies
(\boldsymbol{E}_i + \boldsymbol{E}_r)_{x,y} = (\boldsymbol{E}_t)_{x,y}
\quad
\text{and}
\quad
(\boldsymbol{H}_i + \boldsymbol{H}_r)_{x,y} = (\boldsymbol{H}_t)_{x,y}
$$

- Laws of reflection and refraction

Continuity of the tangential fields at $z=0$ for all $x,t$ requires the phase factors to match,
$$
k_{ix} = k_{rx} = k_{tx},\quad \omega_i=\omega_r=\omega_t=\omega
$$
Assuming the plane of incidence is the $xz$-plane. Since $k_{ix} = k_1\sin\theta_i$, $k_{rx} = k_1\sin\theta_r$, this gives the law of reflection,
$$
\theta_i = \theta_r
$$
With $k_{tx} = k_2\sin\theta_t$ one obtains Snell's law,
$$
n_1\sin\theta_i = n_2\sin\theta_t
$$
### 4.2.2 Fresnel equations *
#### S‑polarization ($\boldsymbol{E}$ perpendicular to the plane of incidence)  
Let $\boldsymbol{E}_{0j} = E_{0j}\hat{y}$. Tangential $\boldsymbol{E}$ and $\boldsymbol{H}$ (using $\boldsymbol{H}_0 = (\omega\mu)^{-1}\boldsymbol{k}\times\boldsymbol{E}_0$) continuity gives,  
$$
E_{0i} + E_{0r} = E_{0t},\quad
\frac{k_1}{\mu_1}(E_{0i} - E_{0r})\cos\theta_i = \frac{k_2}{\mu_2}E_{0t}\cos\theta_t
$$
For simplicity, Let $\alpha\triangleq \frac{\cos\theta_t}{\cos\theta_i}$, $\beta\triangleq\frac{k_2/\mu_2}{k_1/\mu_1}=\frac{Z_1}{Z_2}$. Solving for $r_s \triangleq E_{0r}/E_{0i}$ and $t_s \triangleq E_{0t}/E_{0i}$ gives,
$$
r_s = \frac{{1-\alpha\beta}}{1+\alpha\beta},\quad
t_s = \frac{2}{1+\alpha\beta} = 1 + r_s
$$
#### P‑polarization ($\boldsymbol{E}$ parallel to the plane of incidence)  
Now $\boldsymbol{H}_{0j} = H_{0j}\hat{y}$, with $\boldsymbol{E}_{0j} = -(\omega\epsilon_j)^{-1}\boldsymbol{k}_j\times\boldsymbol{H}_{0j}$,   
$$
E_{0i}\cos\theta_i - E_{0r}\cos\theta_i = E_{0t}\cos\theta_t,\quad
\frac{E_{0i}}{Z_1} + \frac{E_{0r}}{Z_1} = \frac{E_{0t}}{Z_2}
$$
which become
$$
E_{0i} - E_{0r} = \alpha E_{0t},\quad
E_{0i} + E_{0r} = \beta E_{0t}
$$
Solving for $r_p \triangleq E_{0r}/E_{0i}$ and $t_p \triangleq E_{0t}/E_{0i}$ gives
$$
r_p = \frac{\beta-\alpha}{\beta+\alpha},\quad
t_p = \frac{2}{\beta+\alpha}
$$
For non‑magnetic media ($\mu_1\approx\mu_2\approx\mu_0$), $\beta = n_2/n_1$, and these reduce to the standard Fresnel formulas.

- Reflectance and transmittance  
The power normal to the interface (time‑averaged) defines
$$
R = |r|^2,\quad T = \frac{n_2\cos\theta_t}{n_1\cos\theta_i}\,|t|^2
$$
Energy conservation for lossless media ensures $R + T = 1$. At normal incidence ($\theta_i=\theta_t=0$) both polarizations yield
$$
R = \left|\frac{n_1 - n_2}{n_1 + n_2}\right|^2,\quad T = \frac{4n_1 n_2}{(n_1 + n_2)^2}
$$

- Brewster angle  
For P‑polarization, $r_p = 0$ when $n_2\cos\theta_i = n_1\cos\theta_t$. Together with Snell's law this gives
$$
\tan\theta_B = \frac{n_2}{n_1}
$$
At this angle the reflected wave is purely S‑polarized.

- Total internal reflection  
If $n_1 > n_2$, Snell's law gives $\sin\theta_t = (n_1/n_2)\sin\theta_i$. When $\theta_i$ exceeds the critical angle
$$
\theta_c = \arcsin\!\left(\frac{n_2}{n_1}\right)
$$
$\sin\theta_t > 1$ and $\cos\theta_t = \mathrm{i}\sqrt{\sin^2\theta_t-1}$ becomes purely imaginary. The transmitted wave decays exponentially away from the interface (evanescent wave), $|r_s|=|r_p|=1$, and all power is reflected.
## 4.3 EM waves in the conductors    
### 4.3.1 Resonator  

### 4.3.2 Waveguide tube
## 4.4 Lorentz model


