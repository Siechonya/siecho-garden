---
{"dg-publish":true,"permalink":"/A_symmetry_自然界的对称性/Applications/ED formulas (2)/","noteIcon":"default","created":"2026-06-15T09:49:53.230+08:00","updated":"2026-06-19T17:06:34.083+08:00","dg-note-properties":{}}
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

- Retarded potential (using Lorenz gauge)
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
\boldsymbol{A}(\boldsymbol{x},t) = \frac{\mu_0}{4\pi} \iiint \frac{{\dot{\boldsymbol{p}}(t-R/c) \delta^3(\boldsymbol{x'})}}{|\boldsymbol{x}-\boldsymbol{x'}|}\,\mathrm{d}V' = \frac{\mu_0}{4\pi} \frac{\dot{\boldsymbol{p}}_r}{r},
\quad
\boldsymbol{p}_r =\boldsymbol{p}(t-r/c)
$$
$$
\varphi(\boldsymbol{x},t) 
=  \frac{1}{4\pi \epsilon_0} \iiint \frac{-\boldsymbol{p}_r\cdot\nabla\delta^3(\boldsymbol{x'})}{|\boldsymbol{x}-\boldsymbol{x'}|} \mathrm{d}V'
= - \frac{1}{4\pi\epsilon_0} \nabla \cdot \frac{\boldsymbol{p}_r}{r} = \frac{1}{4\pi\epsilon_0} \left( 
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
> Note: In order to  to maintain consistency with the previous sections and avoid confusion, I consistently use $t_r=t-\frac{R}{c}\approx t^*$ to denote the real retarded time and $\tilde{t}_r=t-\frac{r}{c}$ for its leading-order approximation,  rather than $t_r=t-\frac{R}{c}$ before but $t_r=t-\frac{r}{c}$ here in the class.

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
where $E$ and $B$ denote the field <font color="#ff0000">amplitudes</font> with the factor $e^{\mathrm{i}(kr-\omega t)}$ omitted.
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
where $|\ddot{\boldsymbol{p}} \times \hat{r}|$ and $|\ddot{\boldsymbol{p}}|$ denote the <font color="#ff0000">amplitudes</font> with the factor $e^{-\mathrm{i}\omega t}$ omitted.  

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
Another example, if $\boldsymbol{p}(t) = p_0 (\hat{e}_x + \mathrm{i}\hat{e}_y)e^{\mathrm{i}\omega t},\ p_0 = ea$ (electron in uniform circular motion),  
$$
c\boldsymbol{B} = \frac{\mu_0\omega^2p_0}{4\pi r} \left( -\mathrm{i}\hat{\theta} + \cos\theta\,\hat{\phi} \right) e^{\mathrm{i}(kr-\omega t)}
,\quad
\boldsymbol{E} = \frac{\mu_0\omega^2p_0}{4\pi r} \left( \cos\theta\,\hat{\theta} + \mathrm{i}\hat{\phi} \right) e^{\mathrm{i}(kr-\omega t)}
$$
$$
\langle \boldsymbol{S} \rangle = \frac{\mu_0 p_0^2 \omega^4}{32\pi^2 c} \frac{1+\cos^2\theta}{r^2} \hat{r}
,\quad
\langle P\rangle = \frac{\mu_0}{12\pi c}  |ea (\hat{e}_x + \mathrm{i}\hat{e}_y)|^2 \omega^4 = \frac{\mu_0p_0^2\omega^4}{6\pi c}
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
where $\theta=\left\langle \boldsymbol{R}(t),\boldsymbol{\beta}\right\rangle$ is the angle between present position and the velocity, the former satisfies,
$$
\boldsymbol{R}(t_r) - \boldsymbol{R}(t) = \boldsymbol{\beta} c(t-t_r), \ \  R(t_r) = c(t-t_r)
\implies
\boldsymbol{R}(t)=\boldsymbol{R}(t_r)-R(t_r)\boldsymbol{\beta}
$$
However, this form is seldom used in practical radiation problems as the total radiated power of the field is zero.
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
### 4.1.1 Wave equation
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
\left( \nabla^2 - \mu\epsilon \, \frac{\partial^2}{\partial t^2} \right) \left\{\begin{matrix} \boldsymbol{E} \\ \boldsymbol{H}\end{matrix}\right\}= 0
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
## 4.2 EM waves on the surface of the medium  
Let medium 1 ($z<0$) and medium 2 ($z>0$) be homogeneous, isotropic, lossless linear dielectrics with parameters $\epsilon_1,\mu_1$ and $\epsilon_2,\mu_2$. The planar interface is the $z=0$ plane, with unit normal $\hat{n}=\hat{z}$ pointing into medium 2. A monochromatic plane wave of angular frequency $\omega$ is incident from medium 1.  
![zz_figure/Pasted image 20260617122216.png\|center\|780](/img/user/zz_figure/Pasted%20image%2020260617122216.png)
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
With $k_{tx} = k_2\sin\theta_t$ one obtains <font color="#245bdb">Snell's law</font>,
$$
n_1\sin\theta_i = n_2\sin\theta_t
$$
### 4.2.2 Fresnel equations *  
In this section, we follow the reflected convention that reflection reverses the sign of the tangential field parallel to the plane of incidence, while preserving the perpendicular tangential field.
#### P‑polarization ($\boldsymbol{E}$ parallel to the plane of incidence)  
Let $\boldsymbol{H}_{0j} = H_{0j}\hat{y}$. Tangential $\boldsymbol{E}$ and $\boldsymbol{H}$ (using $\boldsymbol{H}_0 = (\omega\mu)^{-1}\boldsymbol{k}\times\boldsymbol{E}_0$) continuity gives,  
$$
E_{0i}\cos\theta_i - E_{0r}\cos\theta_i = E_{0t}\cos\theta_t,\quad
\frac{E_{0i}}{Z_1} + \frac{E_{0r}}{Z_1} = \frac{E_{0t}}{Z_2}
$$
For simplicity, here define the parameters $\alpha\triangleq \frac{\cos\theta_t}{\cos\theta_i}$, $\beta \triangleq\frac{k_2/\mu_2}{k_1/\mu_1}=\frac{Z_1}{Z_2}$. Solving for $r_s \triangleq E_{0r}/E_{0i}$ and $t_s \triangleq E_{0t}/E_{0i}$ gives,
$$
E_{0i} - E_{0r} = \alpha_w E_{0t},\quad
E_{0i} + E_{0r} = \beta E_{0t}
$$
Solving for $r_p \triangleq E_{0r}/E_{0i}$ and $t_p \triangleq E_{0t}/E_{0i}$ gives,
$$
r_p = \frac{\beta-\alpha}{\beta+\alpha},\quad
t_p = \frac{2}{\beta+\alpha}
$$
For non‑magnetic media ($\mu_1\approx\mu_2\approx\mu_0$), $\beta = n_2/n_1$, and these reduce to the standard Fresnel formulas.
#### S‑polarization ($\boldsymbol{E}$ perpendicular to the plane of incidence)  
Let $\boldsymbol{E}_{0j} = E_{0j}\hat{y}$. Tangential continuity gives,  
$$
E_{0i} + E_{0r} = E_{0t},\quad
\frac{E_{0i} - E_{0r}}{Z_1}\cos\theta_i = \frac{E_{0t}}{Z_2}\cos\theta_t
$$
which become, 
$$
r_s = \frac{{1-\alpha\beta}}{1+\alpha\beta},\quad
t_s = \frac{2}{1+\alpha\beta}
$$
#### Reflectance and transmittance  
The power normal to the interface (time‑averaged) defines
$$
R =\frac{{\langle S\rangle_{r,z}}}{\langle S\rangle_{i,z}} = |r|^2,\quad T = \frac{{\langle S\rangle_{t,z}}}{\langle S\rangle_{i,z}} =  \frac{Z_1\cos\theta_t}{Z_2\cos\theta_i}\,|t|^2
$$
Energy conservation for lossless media ensures $R + T = 1$. For P or S-polarization,  
$$
R_p = \left(  \frac{\beta-\alpha}{\beta+\alpha} \right)^2
,\quad
R_s = \left( \frac{{1-\alpha\beta}}{1+\alpha\beta} \right)^2
,\qquad
T_p = T_s = \frac{4\alpha^2\beta^2}{(1+\alpha\beta)^2}
$$
#### Brewster angle  
For P‑polarization, if $\theta_i+\theta_t = \frac{\pi}{2}$ (the same as $r_p = 0$ when $\alpha=\beta$) in non‑magnetic media. Together with Snell's law this gives
$$
\tan\theta_B = \frac{n_2}{n_1} = \beta
$$
At this angle the reflected wave is purely S‑polarized.   

- Assuming $n_2>n_1$ ($\beta>1$). For $\theta_i<\theta_B$,
$$
\alpha = \frac{\cos\theta_t}{\cos\theta_i} = \sqrt{1+\tan^2\theta_i-\left( \frac{\tan\theta_i}{\beta} \right)^2} \in (1,\beta)
$$
$$
\implies
r_p>0,\quad r_s<0
$$
The $s$ component is reversed (phase diff $\pi$) while the $p$ component, referred to the reflected convention, appears unflipped. However, the relative phase between the $p$ and $s$ components changes by $\pi$. Hence, the handedness (the sense of rotation from $p$ toward $s$ with thumb along $\boldsymbol{k}$) is reversed: an incident left‑handed ellipse becomes right‑handed upon reflection, and vice versa.

For $\theta_i>\theta_B$, $r_p < 0,\ r_s < 0$, both components are $\pi$ ‑shifted, their relative phase is unchanged, and the handedness remains the same as the incident wave.
#### Total internal reflection  
If $n_1 > n_2$, Snell's law gives $\sin\theta_t = (n_1/n_2)\sin\theta_i$. When $\theta_i$ exceeds the critical angle
$$
\theta_c = \arcsin\!\left(\frac{n_2}{n_1}\right)
$$
$\sin\theta_t > 1$ and $\cos\theta_t = \mathrm{i}\sqrt{\sin^2\theta_t-1}$ becomes purely imaginary. Then $r_s=r_p=1$, the transmitted wave becomes evanescent, and total internal reflection occurs. More about this phenomenon, see [[A_symmetry_自然界的对称性/Applications/Appendix for ED formulas#8 The evanescent wave\|Appendix for ED formulas#8 The evanescent wave]].
## 4.3 EM waves in the conductors   
### 4.3.1 Wave equation
- The constitutive relations for a homogeneous, isotropic, linear conductor,
$$
\boldsymbol{J} = \sigma \boldsymbol{E}, \quad \boldsymbol{D} = \epsilon \boldsymbol{E}, \quad \boldsymbol{B} = \mu \boldsymbol{H}
$$
Also, inside a homogeneous conductor, any initial free charge accumulation decays exponentially to zero on a timescale of $\tau = \epsilon/\sigma$ ($\sim 10^{-19}\,\text{s}$ for copper). We can safely assume $\rho_f \approx 0$.

- Maxwell equations (assuming $e^{-\mathrm{i}\omega t}$ time-dependence)
$$
\nabla \cdot \boldsymbol{E} = 0, \quad \nabla \cdot \boldsymbol{B} = 0
$$
$$
\nabla \times \boldsymbol{E} = \mathrm{i} \omega \mu\boldsymbol{H}, \quad 
\nabla \times \boldsymbol{H} = (\sigma - \mathrm{i} \omega \epsilon)\boldsymbol{E} = -\mathrm{i}\omega\tilde{\epsilon}\boldsymbol{E},\quad
\tilde{\epsilon} = \epsilon + \mathrm{i} \frac{\sigma}{\omega}
$$
- The wave equation
$$
\left( \nabla^2 + \tilde{k}^2 \right) \left\{\begin{matrix} \boldsymbol{E} \\ \boldsymbol{H}\end{matrix}\right\}= 0
,\quad
\tilde{k}^2 = \omega^2\mu\tilde{\epsilon} = \omega^2\mu\epsilon + \mathrm{i}\omega\mu\sigma
$$
To look for plane-wave solutions propagating along the $z$-direction, we write $\tilde{k}$ in terms of its real and imaginary components,
$$
\tilde{k} = \beta_k + \mathrm{i}\alpha_k
$$
$$
\text{with }
\beta_k = \omega \sqrt{\frac{\mu\epsilon}{2}} \left[ \sqrt{1 + \left(\frac{\sigma}{\omega\epsilon}\right)^2} + 1 \right]^{1/2}
,\quad
\alpha_k = \omega \sqrt{\frac{\mu\epsilon}{2}} \left[ \sqrt{1 + \left(\frac{\sigma}{\omega\epsilon}\right)^2} - 1 \right]^{1/2},\quad
( \beta_k^2 - \alpha_k^2 = \omega^2\mu\epsilon, \ 2\alpha_k\beta_k = \omega\mu\sigma )
$$
The plane wave solution propagating along $\hat{z}$ becomes $\boldsymbol{E}(z,t) = \boldsymbol{E}_0 \, e^{-\alpha_k z} \, e^{\mathrm{i}(\beta_k z - \omega t)}$.  
### 4.3.2 Good conductor
- The good conductor limit

A medium behaves as a good conductor when the conduction current heavily dominates over the displacement current, i.e.,
$$
\frac{\sigma\boldsymbol{E}}{{ \partial \boldsymbol{D} }/{ \partial t }} \sim \frac{\sigma}{\omega\epsilon} = (\omega\tau)^{-1} \gg 1
$$
Under this approximation, the expressions for $\beta$ and $\alpha$ converge to the same value, 
$$
\beta_k \approx \alpha_k \approx \sqrt{\frac{\omega\mu\sigma}{2}}
$$
The skin depth (The characteristic distance over which the wave's amplitude $\boldsymbol{E}_0 \, e^{-\alpha_k z}$ attenuates by a factor of $1/e$) is 
$$
\delta \triangleq \frac{1}{\alpha_k} \approx \sqrt{\frac{2}{\omega\mu\sigma}}
$$
> Inside a good conductor, the wave field dies out almost entirely within a few skin depths. For high frequencies, $\delta$ is on the order of micrometers, restricting the fields and currents to the very outer edge of the material.  

- Complex intrinsic impedance
$$
\tilde{Z} = \frac{\omega\mu}{\tilde{k}} = \frac{\omega\mu}{\beta_k + \mathrm{i}\alpha_k}
$$
For a good conductor,
$$
\tilde{Z} \approx \sqrt{\frac{\omega\mu}{\sigma}} \, e^{-\mathrm{i}\pi/4} = \frac{1}{\sigma\delta}(1 - \mathrm{i})
$$
Hence, for the plane wave solution propagating along $\hat{z}$ : $\boldsymbol{E}(z,t) = \boldsymbol{E}_0 \, e^{-\alpha_k z} \, e^{\mathrm{i}(\beta_k z - \omega t)}$,
$$
\boldsymbol{H}(z,t) = \frac{\hat{z}\times\boldsymbol{E}(z,t)}{\tilde{Z}} = E_0\sqrt{\frac{\sigma}{\omega\mu}} \, e^{-\alpha z}\,e^{\mathrm{i}(\beta z - \omega t + \pi/4)}\,\hat{z}\times\boldsymbol{E}_0
$$
Which means: Firstly, $\boldsymbol{H}$ lags behind $\boldsymbol{E}$ by a temporal phase angle of $\pi/4$; Secondly, The magnetic energy density ($\frac{1}{2}\mu|\boldsymbol{H}|^2$) is vastly larger than the electric energy density ($\frac{1}{2}\epsilon|\boldsymbol{E}|^2$) by a factor of $\frac{\sigma}{\omega\epsilon}$, meaning the wave becomes almost purely magnetic.

- Good conductors is good reflectors

Consider an electromagnetic wave in a lossless Medium 1 (air with $n_1 \approx 1$) is incident upon a good conductor (Medium 2, with finite but large $\sigma$). The wave vector $\boldsymbol{k}_t$ in Medium 2 becomes complex,
$$
\tilde{k}_2 =\beta_k + \mathrm{i}\alpha_k \approx \frac{{1+\mathrm{i}}}{\delta}
$$
here $\delta$ is incredibly small, meaning $|k_2| \gg k_1$. As [[A_symmetry_自然界的对称性/Applications/ED formulas (2)#P‑polarization ($ boldsymbol{E}$ parallel to the plane of incidence)\|#P‑polarization ($ boldsymbol{E}$ parallel to the plane of incidence)]], define the complex parameter $\beta$ and $\alpha$,
$$
\tilde{\beta} \triangleq \frac{k _2/\mu _2}{k_ 1/\mu_ 1} \approx \frac{k _2}{k_ 1} = \frac{1+\mathrm{i}}{k_1\delta} ,\quad|\tilde{\beta}|\gg 1
$$
$$
\sin\theta_t = (k_1/k_2)\sin\theta_i\ll1 \implies \theta_t\approx 0
\implies
\alpha \triangleq \frac{\cos\theta_t}{\cos\theta_i} \approx \frac{1}{\cos\theta_i} 
$$
For infinite $\theta_i$: $|\beta| \gg \alpha$. Therefore,
$$
\tilde{r}_p = \frac{\tilde{\beta} - \alpha}{\tilde{\beta} + \alpha} \to 1,\quad
\tilde{r}_s = \frac{1 - \alpha\tilde{\beta}}{1 + \alpha\tilde{\beta}} \to -1
$$
Which means the good conductor reflects nearly all of the incident field back into Medium 1.  

- Boundary condition for good conductor ($\hat{n}$ is pointed to conductor (Medium 2))
$$
\begin{align} 
\hat{{n}} \times \boldsymbol{E} &= 0 \overset{\nabla \cdot \boldsymbol{E}=0}{\implies} \frac{ \partial E_n }{ \partial n } = 0
\\[10pt]
\hat{{n}} \times \boldsymbol{H} &= -\boldsymbol{K}_f
,\quad
\hat{{n}} \cdot \boldsymbol{D} = -\sigma_f
\\[10pt] 
\hat{{n}} \cdot \boldsymbol{H} &= 0 
\overset{\nabla \cdot \boldsymbol{B}=0}{\implies} \frac{ \partial H_{\perp,1} }{ \partial x_{\perp,1} } + \frac{ \partial H_{\perp,2} }{ \partial x_{\perp,2} } = 0
\end{align}
$$
### 4.3.3 Resonator  
Consider a hollow rectangular cavity with dimensions $0 \le x \le a$, $0 \le y \le b$, and $0 \le z \le d$. The fields inside must satisfy the time-harmonic Helmholtz equation $\left(\nabla^2 + k^2\right) \boldsymbol{E} = 0$, where $k = \omega\sqrt{\mu\epsilon}$.  

Applying the separation of variables under the boundary conditions $\hat {{n}} \times \boldsymbol{E} = 0, \ \frac{ \partial E_n }{ \partial n } = 0$ restricts $\boldsymbol{k}$ to discrete values,  
$$
k_x = \frac{l\pi}{a}, \quad k_y = \frac{m\pi}{b}, \quad k_z = \frac{n\pi}{d} \qquad (l, m, n \in \mathbb{N})
$$
where at most one of the integers can be zero for a given mode. This yields the discrete resonant frequencies of the resonator,  
$$
\omega_{lmn} = \frac{\pi}{\sqrt{\mu\epsilon}} \sqrt{\left(\frac{l}{a}\right)^2 + \left(\frac{m}{b}\right)^2 + \left(\frac{n}{d}\right)^2}
$$
### 4.3.4 Waveguide tube  
#### The rectangular waveguide
Consider a hollow waveguide with a rectangular cross-section of width $a$ along the $x$-axis and height $b$ along the $y$-axis, with $a > b$. The inner PEC (perfect electric conductor) walls are located at $x=0, a$ and $y=0, b$. We look for harmonic waves propagating down the tube,
$$
\boldsymbol{E}(\boldsymbol{r},t) = \boldsymbol{E}_0(x,y) \, e^{\mathrm{i}(k_z z - \omega t)}, \quad \boldsymbol{H}(\boldsymbol{r},t) = \boldsymbol{H}_0(x,y) \, e^{\mathrm{i}(k_z z - \omega t)}
$$
which satisfy,  
$$
\left( \frac{\partial^2}{\partial x^2} + \frac{\partial^2}{\partial y^2} - k_z^2 + k^2 \right) \left\{\begin{matrix} \boldsymbol{E}_0 \\ \boldsymbol{H}_0\end{matrix}\right\}  = 0
$$
- <font color="#ff0000">TM Modes (Transverse Magnetic)</font>

For TM waves, the longitudinal magnetic field vanishes ($H_z = 0$), and we solve for $\boldsymbol{E}_0(x,y)$. The boundary conditions are,
$$
\begin{align} 
&\text{at }~ x=0,a:\quad
E_z = E_y = \frac{ \partial E_x }{ \partial x } =0
\\[4pt]
&\text{at }~ y=0,b:\quad
E_z = E_x = \frac{ \partial E_y }{ \partial y } = 0
\end{align}
$$
Applying the separation of variables yields,
$$
\begin{align} 
E_{0z}(x,y) &= A_z \sin\left(\frac{m\pi x}{a}\right) \sin\left(\frac{n\pi y}{b}\right)
\\[8pt]
E_{0x}(x,y) &= A_x \cos\left(\frac{m\pi x}{a}\right) \sin\left(\frac{n\pi y}{b}\right)
\\[8pt]
E_{0y}(x,y) &= A_y \sin\left(\frac{m\pi x}{a}\right) \cos\left(\frac{n\pi y}{b}\right) 
\end{align} 
\qquad (m, n \in \mathbb{N}_0, \text{ and } m+n > 0)
$$
Plunging this back into the Helmholtz equation yields the discrete cutoff wavenumber $k_c$,
$$
k_c^2 = \left(\frac{m\pi}{a}\right)^2 + \left(\frac{n\pi}{b}\right)^2 = k^2 - k_z^2
$$
> Crucial Note: If either $m=0$ or $n=0$, the entire field $E_z$ collapses to zero. Thus, the lowest-order TM mode is the $\text{TM}_{11}$ mode.

- <font color="#ff0000">TE Modes (Transverse Electric)</font>

For TE waves, the longitudinal electric field vanishes ($E_z = 0$), and we solve for $\boldsymbol{H}_0(x,y)$. The boundary condition $\boldsymbol{E}_{\text{tangential}} = 0$ translates via Maxwell's equations into a Neumann boundary condition for $H_z$ (its normal derivative must vanish at the walls),
$$
\begin{align} 
&\text{at }~ x=0,a:\quad
E_y = H_x =0 \implies \frac{\partial H_z}{\partial x} = \frac{ \partial H_y }{ \partial x } =0
\\[4pt]
&\text{at }~ y=0,b:\quad
E_x = H_y = 0 \implies \frac{\partial H_z}{\partial y} = \frac{ \partial H_x }{ \partial y } = 0
\end{align}
$$
This restricts the solutions to,
$$
\begin{align} 
H_{0z}(x,y) &= A'_z \cos\left(\frac{m\pi x}{a}\right) \cos\left(\frac{n\pi y}{b}\right)
\\[8pt]
H_{0x}(x,y) &= A'_x \sin\left(\frac{m\pi x}{a}\right) \cos\left(\frac{n\pi y}{b}\right)
\\[8pt]
H_{0y}(x,y) &= A'_y \cos\left(\frac{m\pi x}{a}\right) \sin\left(\frac{n\pi y}{b}\right) 
\end{align} 
\qquad (m, n \in \mathbb{N}^+)
$$
The cutoff wavenumber $k_c$ shares the exact same algebraic form as the TM modes. However, because cosines do not vanish when their arguments are zero, one of the indices ($m$ or $n$) can safely be zero. Thus, the lowest-order TE mode is the $\text{TE}_{10}$ or $TE_{01}$ mode.

- The Dominant Mode: $\text{TE}_{10}$ 

If $a > b$, the lowest-order TE mode is the $\text{TE}_{10}$ mode,
$$
k_{c,10} = \frac{\pi}{a} \implies \omega_{c,10} = \frac{\pi}{a\sqrt{\mu\epsilon}} < \omega_{c,01}
$$
#### The transverse-longitudinal bridge *  
This formulation serves as a powerful tool for applying boundary conditions, as well as for deriving all remaining field components once a single longitudinal component is determined. 

Using,  
$$
\nabla \times \boldsymbol{E} = \mathrm{i}\omega\mu\boldsymbol{H}
, \quad 
\nabla \times \boldsymbol{H} = -\mathrm{i}\omega\epsilon\boldsymbol{E}
$$
Expanding these equations into Cartesian components (replacing $\partial/\partial z$ with $\mathrm{i}k_z$) yields,  
$$
\begin{align} 
\frac{\partial E_z}{\partial y} - \mathrm{i}k_z E_y &= \mathrm{i}\omega\mu H_x
\\ 
\mathrm{i}k_z E_x - \frac{\partial E_z}{\partial x} &= \mathrm{i}\omega\mu H_y
\\
\frac{\partial E_y}{\partial x} - \frac{\partial E_x}{\partial y} &= \mathrm{i}\omega\mu H_z
\\
\frac{\partial H_z}{\partial y} - \mathrm{i}k_z H_y &= -\mathrm{i}\omega\epsilon E_x
\\
\mathrm{i}k_z H_x - \frac{\partial H_z}{\partial x} &= -\mathrm{i}\omega\epsilon E_y
\\
\frac{\partial H_y}{\partial x} - \frac{\partial H_x}{\partial y} &= -\mathrm{i}\omega\epsilon E_z
\end{align}
$$
By solving the simultaneous pairs (1)-(5) and (2)-(4), we form the algebraic bridge that explicitly expresses the transverse field components $(E_x, E_y, H_x, H_y)$ in terms of the longitudinal components $(E_z, H_z)$,  
$$
\begin{align} 
E_x &= \frac{\mathrm{i}}{k_c^2} \left( k_z \frac{\partial E_z}{\partial x} + \omega\mu \frac{\partial H_z}{\partial y} \right) \quad 
\\[4pt] 
E_y &= \frac{\mathrm{i}}{k_c^2} \left( k_z \frac{\partial E_z}{\partial y} - \omega\mu \frac{\partial H_z}{\partial x} \right) \quad 
\\[4pt] 
H_x &= \frac{\mathrm{i}}{k_c^2} \left( k_z \frac{\partial H_z}{\partial x} - \omega\epsilon \frac{\partial E_z}{\partial y} \right) \quad
\\[4pt]
H_y &= \frac{\mathrm{i}}{k_c^2} \left( k_z \frac{\partial H_z}{\partial y} + \omega\epsilon \frac{\partial E_z}{\partial x} \right)
\end{align}
$$
#### The general waveguide *
Now we take a hollow tube of any arbitrary cross-section shape into account.   

To do this efficiently without solving all 6 components of $\boldsymbol{E}$ and $\boldsymbol{H}$ simultaneously, we split the del operator and the fields into transverse ($t$) and longitudinal ($z$) components,
$$
\nabla = \nabla_t + \hat{z}\frac{\partial}{\partial z} = \nabla_t + \mathrm{i}k_z\hat{z}
$$
$$
\boldsymbol{E} = \boldsymbol{E}_t + E_z\hat{z},\quad \boldsymbol{H} = \boldsymbol{H}_t + H_z\hat{z}
$$
By substituting these split forms back into Maxwell's curl equations ($\nabla \times \boldsymbol{E} = \mathrm{i}\omega\mu\boldsymbol{H}$ and $\nabla \times \boldsymbol{H} = -\mathrm{i}\omega\epsilon\boldsymbol{E}$) and separating the components orthogonal to $\hat{z}$, one obtains,
$$
\begin{align} \boldsymbol{E}_t &= \frac{\mathrm{i}}{k_c^2} \left( k_z \nabla_t E_z - \omega\mu \, \hat{z} \times \nabla_t H_z \right) 
\\[4pt] 
\boldsymbol{H}_t &= \frac{\mathrm{i}}{k_c^2} \left( k_z \nabla_t H_z + \omega\epsilon \, \hat{z} \times \nabla_t E_z \right) \end{align}
$$
where $k_c^2 \triangleq k^2 - k_z^2 = \mu\epsilon\omega^2 - k_z^2$.

Thus, once you solve the 2D scalar Helmholtz equation $\left(\nabla_t^2 + k_c^2\right) \left\{\begin{matrix} E_{0z} \\ H_{0z}\end{matrix}\right\} = 0$ for a given boundary, taking spatial derivatives ($\nabla_t$) instantly yields the entire transverse field structure.

- The Impossibility of TEM Modes in Hollow Tubes

A TEM (Transverse Electromagnetic) wave requires both $E_z = 0$ and $H_z = 0$. Looking at the general decomposition formulas above, if $E_z=H_z=0$, then $\boldsymbol{E}_t$ and $\boldsymbol{H}_t$ would instantly become zero unless $k_c^2 = 0$.

If $k_c^2 = 0$, the transverse electric field reduces to a static-like potential problem: $\nabla_t^2 \Phi = 0$ with $\boldsymbol{E}_t = -\nabla_t \Phi$. For a hollow, single-conductor tube, the entire bounding perimeter forms a single, continuous equipotential surface. By the uniqueness theorem of electrostatics, $\Phi = \text{constant}$ everywhere inside, meaning $\boldsymbol{E}_t = 0$.

Thus, TEM waves cannot exist inside a hollow, single-conductor waveguide.
#### Dispersion characteristics
For any chosen mode with a cutoff wavenumber $k_c$, the longitudinal propagation constant is,
$$
k_z = \sqrt{k^2 - k_c^2} = \sqrt{\mu\epsilon}\sqrt{\omega^2 - \omega_c^2},\quad
\omega_c = \frac{k_c}{\sqrt{\mu\epsilon}}
$$
If $\omega > \omega_c$, $k_z$ is real. The wave propagates freely, while for $\omega < \omega_c$, $k_z = \mathrm{i}\alpha$ becomes purely imaginary. The fields decay exponentially as $e^{-\alpha z}$.

Because the wave bounces off the walls rather than traveling in a straight line, the phase fronts and the energy transport move along the axis at different speeds:

- Phase Velocity
$$
v_p \triangleq \frac{\omega}{k_z} = \frac{c_m}{\sqrt{1 - (\omega_c/\omega)^2}} > c_m, \quad c_m = \frac{1}{\sqrt{\mu\epsilon}}
$$
- Group Velocity
$$
v_g \triangleq \frac{\mathrm{d}\omega}{\,\,\mathrm{d}k_z} = c_m \sqrt{1 - \left(\frac{\omega_c}{\omega}\right)^2} < c_m
$$
and 
$$
v_p \cdot v_g = c_m^2
$$
## 4.4 Lorentz model *
The Lorentz model treats a bound electron in a dielectric as a damped harmonic oscillator driven by the local electric field. We use the same time convention as above, $e^{-\mathrm{i}\omega t}$.
### 4.4.1 Equation of motion for a bound electron
Let $\boldsymbol{x}$ be the displacement of an electron relative to the positive nucleus. For a monochromatic field $\boldsymbol{E}(t)=\boldsymbol{E}_0 e^{-\mathrm{i}\omega t}$,
$$
m\frac{\mathrm{d}^2\boldsymbol{x}}{\mathrm{d}t^2}+m\gamma\frac{\mathrm{d}\boldsymbol{x}}{\mathrm{d}t}+m\omega_0^2\boldsymbol{x}=-e\boldsymbol{E}(t)
$$
where $\omega_0$ is the natural frequency of the bound electron and $\gamma$ is the damping rate. Therefore,
$$
\boldsymbol{x}_0=-\frac{e/m}{\omega_0^2-\omega^2-\mathrm{i}\gamma\omega}\boldsymbol{E}_0
$$
The induced dipole moment of one atom is,
$$
\boldsymbol{p}_0=-e\boldsymbol{x}_0=\frac{e^2/m}{\omega_0^2-\omega^2-\mathrm{i}\gamma\omega}\boldsymbol{E}_0
\triangleq \alpha(\omega)\boldsymbol{E}_0
$$
Thus the atomic polarizability is,
$$
\alpha(\omega)=\frac{e^2/m}{\omega_0^2-\omega^2-\mathrm{i}\gamma\omega}
$$
### 4.4.2 Electric susceptibility and dielectric function
If the number density of oscillators is $N$, then
$$
\boldsymbol{P}=N\boldsymbol{p}=\epsilon_0\chi_e(\omega)\boldsymbol{E}
$$
so that
$$
\chi_e(\omega)=\frac{Ne^2}{\epsilon_0m}\frac{1}{\omega_0^2-\omega^2-\mathrm{i}\gamma\omega}
=\frac{\omega_p^2}{\omega_0^2-\omega^2-\mathrm{i}\gamma\omega},
\qquad
\omega_p^2\triangleq\frac{Ne^2}{\epsilon_0m}
$$
For several resonance modes,
$$
\chi_e(\omega)=\frac{Ne^2}{\epsilon_0m}\sum_j\frac{f_j}{\omega_{0j}^2-\omega^2-\mathrm{i}\gamma_j\omega},
\qquad \sum_j f_j \approx 1
$$
where $f_j$ is the oscillator strength. The complex permittivity is,
$$
\tilde{\epsilon}(\omega)=\epsilon_0\big[1+\chi_e(\omega)\big]
$$
and for a non-magnetic dielectric,
$$
\tilde{n}^2(\omega)=1+\chi_e(\omega)
$$
Writing $\chi_e=\chi'+\mathrm{i}\chi''$ for a single resonance gives,
$$
\chi'=\omega_p^2\frac{\omega_0^2-\omega^2}{(\omega_0^2-\omega^2)^2+\gamma^2\omega^2},
\qquad
\chi''=\omega_p^2\frac{\gamma\omega}{(\omega_0^2-\omega^2)^2+\gamma^2\omega^2}
$$
The real part $\chi'$ determines dispersion, while the imaginary part $\chi''>0$ determines absorption.
### 4.4.3 Dispersion and absorption  
#### Absorption
For weak absorption, write $\tilde{n}=n+\mathrm{i}\kappa$. A plane wave propagating in the $+z$ direction is then,
$$
\boldsymbol{E}(z,t)=\boldsymbol{E}_0 e^{\mathrm{i}(\tilde{n}\omega z/c-\omega t)}
=\boldsymbol{E}_0 e^{-\kappa\omega z/c}e^{\mathrm{i}(n\omega z/c-\omega t)}
$$
so the intensity obeys,
$$
I(z)=I_0e^{-a_{\rm abs}z},
\qquad
a_{\rm abs}=\frac{2\kappa\omega}{c}
$$
The time-averaged absorbed power density is,
$$
\big\langle p_{\rm abs}\big\rangle=\frac{\omega}{2}\epsilon_0\chi''|\boldsymbol{E}_0|^2
=\frac{\omega}{2}\mathrm{Im}(\tilde{\epsilon})|\boldsymbol{E}_0|^2
$$
Near $\omega\approx\omega_0$, $\chi''$ has a peak and the wave is strongly absorbed. Away from resonance, $\chi''$ becomes small and the medium is approximately transparent, but $\chi'$ still varies with frequency, producing dispersion.  
#### (Anomalous) dispersion  
For a weakly absorbing dielectric, $\kappa\ll n$, or equivalently $\chi''\ll \chi'$. From $\tilde{n}^2=(n+\mathrm{i}\kappa)^2=1+\chi'+\mathrm{i}\chi''$ one obtains,
$$
n^2-\kappa^2=1+\chi',\qquad 2n\kappa=\chi''
$$
Therefore, in the weak-absorption limit $\kappa\ll n$,
$$
n(\omega)\approx \sqrt{1+\chi'(\omega)},\qquad
\kappa(\omega)\approx \frac{\chi''(\omega)}{2n(\omega)}
$$
Only for a dilute or weakly polarizable medium, $|\chi_e|\ll1$, can one further expand
$$
n\approx 1+\frac{1}{2}\chi',\qquad \kappa\approx \frac{1}{2}\chi''
$$
The frequency dependence of $n(\omega)$ is called dispersion. The phase velocity and group velocity are,
$$
v_p=\frac{\omega}{k}=\frac{c}{n(\omega)},
\qquad
v_g=\frac{\mathrm{d}\omega}{\mathrm{d}k}
=\frac{c}{n+\omega\frac{\mathrm{d}n}{\mathrm{d}\omega}}
$$
For the Lorentz oscillator,
$$
\chi'(\omega)=\omega_p^2\frac{\omega_0^2-\omega^2}{(\omega_0^2-\omega^2)^2+\gamma^2\omega^2}
$$
Hence, below resonance ($\omega<\omega_0$), usually $\chi'>0$ and $n>1$; above resonance ($\omega>\omega_0$), $\chi'<0$ and $n$ decreases. Near resonance, let $\delta\triangleq\omega-\omega_0$ and assume $|\delta|\ll\omega_0$, then
$$
\omega_0^2-\omega^2\approx -2\omega_0\delta
$$
and
$$
\chi'(\omega)\approx -\frac{2\omega_p^2}{\omega_0}\frac{\delta}{4\delta^2+\gamma^2},
\qquad
\chi''(\omega)\approx \frac{\omega_p^2\gamma}{\omega_0}\frac{1}{4\delta^2+\gamma^2}
$$
Therefore, in the resonant absorption band,
$$
\left.\frac{\mathrm{d}\chi'}{\mathrm{d}\omega}\right|_{\omega=\omega_0}
\approx -\frac{2\omega_p^2}{\omega_0\gamma^2}<0
$$
so that
$$
\frac{\mathrm{d}n}{\mathrm{d}\omega}<0
$$
This region is called <font color="#ff0000">anomalous dispersion</font>. In contrast, away from strong absorption bands, one usually has,
$$
\frac{\mathrm{d}n}{\mathrm{d}\omega}>0
$$
which is called normal dispersion.

> Note: Strong anomalous dispersion appears together with strong absorption. Therefore, even if the formal expression for $v_g$ becomes larger than $c$ or negative near resonance, it does not represent superluminal information transfer; in this region the pulse is strongly distorted and the simple transparent-medium group-velocity picture breaks down. Causality links absorption and dispersion through the [Kramers–Kronig relations - Wikipedia](https://en.wikipedia.org/wiki/Kramers%E2%80%93Kronig_relations).
### 4.4.4 Drude model as the free-electron limit
For free electrons in a metal or plasma, the restoring force vanishes, i.e. $\omega_0=0$. Then, 
$$
\chi(\omega)=-\frac{\omega_p^2}{\omega^2+\mathrm{i}\gamma\omega}
$$
$$
\tilde{\epsilon}_r(\omega) 
\triangleq \frac{\tilde{\epsilon}(\omega)}{\epsilon_0}
=1-\frac{\omega_p^2}{\omega^2+\mathrm{i}\gamma\omega}
$$
In the collisionless limit $\gamma\to0$,
$$
\tilde{\epsilon}_r(\omega)=1-\frac{\omega_p^2}{\omega^2}
$$
Thus, for $\omega<\omega_p$, $\tilde{\epsilon}_r<0$ and the wave cannot propagate in the bulk; for $\omega>\omega_p$, $\tilde{\epsilon}_r>0$ and the wave can propagate.
## 4.5 Scattering and absorption of waves *  
 #todo  




