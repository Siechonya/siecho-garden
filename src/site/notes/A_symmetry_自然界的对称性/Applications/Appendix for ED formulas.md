---
{"dg-publish":true,"permalink":"/A_symmetry_自然界的对称性/Applications/Appendix for ED formulas/","noteIcon":"default","created":"2026-05-20T11:12:27.839+08:00","updated":"2026-05-25T19:43:34.496+08:00","dg-note-properties":{}}
---

> This document supplements some rather complex proof processes within [[A_symmetry_自然界的对称性/Applications/ED Formulas\|ED Formulas]] and [[A_symmetry_自然界的对称性/Applications/ED formulas (2)\|ED formulas (2)]] 

# 1 $\iiint_V \boldsymbol{E}(\boldsymbol{x}) \,\mathrm{d}^3x = -\frac{\boldsymbol{p}}{3\epsilon_0}$  
Let $V$ be a spherical volume of radius $R$ that completely encloses all charges, meaning the charge density $\rho(\boldsymbol{x}')$ vanishes for all $r' > R$. Without loss of generality, we place the coordinate origin at the center of the sphere $V$. According to Coulomb's law, the electric field $\boldsymbol{E}(\boldsymbol{x})$ at any field point $\boldsymbol{x}$ inside the sphere is given by the volume integral over the source coordinates $\boldsymbol{x}'$:
$$
\boldsymbol{E}(\boldsymbol{x}) = \frac{1}{4\pi\varepsilon_0} \int_{V} \rho(\boldsymbol{x}') \frac{\boldsymbol{x} - \boldsymbol{x}'}{|\boldsymbol{x} - \boldsymbol{x}'|^3} \, \mathrm{d}^3x'
$$
We want to evaluate the volume integral of $\boldsymbol{E}(\boldsymbol{x})$ over the entire sphere $V$:
$$
\int_V \boldsymbol{E}(\boldsymbol{x}) \, \mathrm{d}^3x = \frac{1}{4\pi\varepsilon_0} \int_V \left[ \int_{V} \rho(\boldsymbol{x}') \frac{\boldsymbol{x} - \boldsymbol{x}'}{|\boldsymbol{x} - \boldsymbol{x}'|^3} \, \mathrm{d}^3x' \right] \mathrm{d}^3x
$$
Since the region of integration is bounded and the charge distribution is well-behaved, we can apply Fubini's theorem to switch the order of the volume integrals over $\mathrm{d}^3x$ and $\mathrm{d}^3x'$:
$$
\int_V \boldsymbol{E}(\boldsymbol{x}) \, \mathrm{d}^3x = \frac{1}{4\pi\varepsilon_0} \int_{V} \rho(\boldsymbol{x}') \left[ \int_V \frac{\boldsymbol{x} - \boldsymbol{x}'}{|\boldsymbol{x} - \boldsymbol{x}'|^3} \, \mathrm{d}^3x \right] \mathrm{d}^3x'
$$
Let us denote the inner vector integral as $\boldsymbol{I}(\boldsymbol{x}')$:
$$
\boldsymbol{I}(\boldsymbol{x}') = \int_V \frac{\boldsymbol{x} - \boldsymbol{x}'}{|\boldsymbol{x} - \boldsymbol{x}'|^3} \, \mathrm{d}^3x
$$
We recognize that the integrand can be expressed as the negative gradient with respect to the field point $\boldsymbol{x}$: 
$$
\frac{\boldsymbol{x} - \boldsymbol{x}'}{|\boldsymbol{x} - \boldsymbol{x}'|^3} = -\nabla \left( \frac{1}{|\boldsymbol{x} - \boldsymbol{x}'|} \right)
$$
Substituting this identity into $\boldsymbol{I}(\boldsymbol{x}')$ and applying a corollary of the divergence theorem (converting a volume integral of a gradient into a closed surface integral), we obtain:
$$\boldsymbol{I}(\boldsymbol{x}') = -\int_V \nabla \left( \frac{1}{|\boldsymbol{x} - \boldsymbol{x}'|} \right) \mathrm{d}^3x = -\oint_{\partial V} \frac{1}{|\boldsymbol{x} - \boldsymbol{x}'|} \hat{\boldsymbol{n}} \, \mathrm{d}A$$
where $\partial V$ represents the bounding spherical surface at $r = R$, and $\hat{\boldsymbol{n}}$ is the outward unit normal vector. On this spherical surface, the field point is $\boldsymbol{x} = R\hat{\boldsymbol{x}}$ (where $\hat{\boldsymbol{x}}$ is the radial unit vector $\hat{\boldsymbol{r}}$), and the area element is $\mathrm{d}A = R^2 \, \mathrm{d}\Omega$. Thus, the integral becomes
$$\boldsymbol{I}(\boldsymbol{x}') = -R^2 \oint_{r=R} \frac{1}{|\boldsymbol{x} - \boldsymbol{x}'|} \hat{\boldsymbol{x}} \, \mathrm{d}\Omega$$
Because all charges are enclosed within the sphere, the source point always lies inside ($r' < R$), while the field point in the surface integral lies exactly on the boundary ($r = R$). Since $r' < r$, we can expand the reciprocal distance $1/|\boldsymbol{x} - \boldsymbol{x}'|$ into a series of Legendre polynomials:
$$\frac{1}{|\boldsymbol{x} - \boldsymbol{x}'|} = \sum_{l=0}^{\infty} \frac{(r')^l}{R^{l+1}} P_l(\cos\gamma)$$
where $\gamma$ is the angle between $\boldsymbol{x}$ and $\boldsymbol{x}'$.

To evaluate the solid angle integral, we temporarily align the $z$-axis along the direction of $\boldsymbol{x}'$, making $\gamma = \theta$ (the standard polar angle). The unit vector $\hat{\boldsymbol{x}}$ expands in Cartesian components as:
$$
\hat{\boldsymbol{x}} = \sin\theta\cos\phi \hat{\boldsymbol{i}} + \sin\theta\sin\phi \hat{\boldsymbol{j}} + \cos\theta \hat{\boldsymbol{k}}
$$
Integrating over the azimuthal angle $\phi$ from $0$ to $2\pi$, the terms containing $\cos\phi$ and $\sin\phi$ vanish identically due to periodicity. The only surviving component is along the $\hat{\boldsymbol{k}}$ direction (which is the direction of $\hat{\boldsymbol{x}}'$):
$$
\oint_{r=R} \frac{1}{|\boldsymbol{x} - \boldsymbol{x}'|} \hat{\boldsymbol{x}} \, \mathrm{d}\Omega = \hat{\boldsymbol{x}}' \int_0^{2\pi} \mathrm{d}\phi \int_0^\pi \left[ \sum_{l=0}^{\infty} \frac{(r')^l}{R^{l+1}} P_l(\cos\theta) \right] \cos\theta \sin\theta \, \mathrm{d}\theta
$$
Noting that $\cos\theta = P_1(\cos\theta)$, we invoke the orthogonality condition for Legendre polynomials:
$$
\int_0^\pi P_l(\cos\theta) P_1(\cos\theta) \sin\theta \, \mathrm{d}\theta = \frac{2}{2(1)+1}\delta_{l,1} = \frac{2}{3}\delta_{l,1}
$$
Hence, only the $l = 1$ term yields a non-zero contribution to the infinite series:
$$
\oint_{r=R} \frac{1}{|\boldsymbol{x} - \boldsymbol{x}'|} \hat{\boldsymbol{x}} \, \mathrm{d}\Omega = \hat{\boldsymbol{x}}' \cdot 2\pi \cdot \frac{r'}{R^2} \cdot \frac{2}{3} = \frac{4\pi}{3R^2} (r'\hat{\boldsymbol{x}}') = \frac{4\pi}{3R^2} \boldsymbol{x}'
$$
Substituting this result back into the expression for $\boldsymbol{I}(\boldsymbol{x}')$, the radius $R^2$ cancels out smoothly:
$$
\boldsymbol{I}(\boldsymbol{x}') = -R^2 \left( \frac{4\pi}{3R^2} \boldsymbol{x}' \right) = -\frac{4\pi}{3} \boldsymbol{x}'
$$
We now feed $\boldsymbol{I}(\boldsymbol{x}')$ back into our original total electric field volume integral:
$$
\int_V \boldsymbol{E}(\boldsymbol{x}) \, \mathrm{d}^3x = -\frac{1}{3\varepsilon_0} \int_{V} \rho(\boldsymbol{x}') \boldsymbol{x}' \, \mathrm{d}^3x'
$$
By definition, the total electric dipole moment $\boldsymbol{p}$ of the localized charge distribution with respect to our chosen origin is:
$$
\boldsymbol{p} = \int_{V} \rho(\boldsymbol{x}') \boldsymbol{x}' \, \mathrm{d}^3x'
$$
Replacing the integral with $\boldsymbol{p}$, we arrive at:
$$
\int_V \boldsymbol{E}(\boldsymbol{x}) \, \mathrm{d}^3x = -\frac{\boldsymbol{p}}{3\varepsilon_0}
$$
# 2 Rotation of harmonics & Wigner $D$-Matrices *
Spherical harmonics $Y_l^m(\theta, \varphi)$ form a $(2l+1)$-dimensional irreducible representation of $\mathrm{SO}(3)$. Under a coordinate rotation $\mathcal{R}$ parameterized by the Euler angles $(\alpha, \beta, \gamma)$, the total angular momentum quantum number $l$ remains invariant because the rotation operator commutes with the total angular momentum squared: $[\mathcal{R}, \boldsymbol{L}^2] = 0$. However, the azimuthal projection undergoes a linear transformation.

The transformed spherical harmonic in the rotated frame can be expressed as a linear combination of the original basis functions,
$$
Y_l^{m}(\theta', \varphi') = \sum_{m'=-l}^l D_{m'm}^l(\alpha, \beta, \gamma) Y_l^{m'}(\theta, \varphi)
$$
where $D_{m'm}^l(\alpha, \beta, \gamma)$ are the elements of the Wigner $D$-matrix. We find that the entire rotation operator can be directly written as $\mathcal{R}(\alpha, \beta, \gamma) = e^{-\mathrm{i}\alpha L_z} e^{-\mathrm{i}\beta L_y} e^{-\mathrm{i}\gamma L_z}$. Thus, Wigner $D$-matrix can be factorized into a product of exponentials and Wigner's small $d$-matrix,
$$
D_{m'm}^l(\alpha, \beta, \gamma) =  \langle l, m' | e^{-\mathrm{i}\alpha L_z} \, e^{-\mathrm{i}\beta L_y} \, e^{-\mathrm{i}\gamma L_z} | l, m \rangle = e^{-\mathrm{i}m'\alpha} d_{m'm}^l(\beta) e^{-\mathrm{i}m\gamma}
$$
Here, Wigner's small $d$-matrix $d_{m'm}^l(\beta)$ describes the rotation around the $y$-axis,
$$
d_{m'm}^l(\beta) = \langle l, m' | e^{-\mathrm{i}\beta L_y} | l, m \rangle
$$
Since spatial rotations preserve the norm of the state space, the Wigner $D$-matrix is strictly unitary,
$$
\sum_{m=-l}^l D_{m k}^{l*}(\alpha, \beta, \gamma) D_{m n}^l(\alpha, \beta, \gamma) = \delta_{kn}
$$
In particular, when the second projection index is set to zero ($m=0$), the Wigner $D$-matrix simplifies directly to a spherical harmonic,  
$$
D_{m'0}^l(\alpha, \beta, 0) = \sqrt{\frac{4\pi}{2l+1}} Y_l^{m'*}(\beta, \alpha)
$$
Let $\gamma$ denote the angle between the points $(\theta',\varphi')$ and $(\theta,\varphi)$ on the spherical surface. By first rotating the coordinate system anticlockwise by an angle of $\varphi'$ about the $z$-axis and then by an angle of $\theta'$ about the $y$-axis, one find,
$$
P_l(\cos\gamma) 
= \sqrt{\frac{4\pi}{2l+1}} Y_l^0 (\gamma, 0) 
= \sqrt{\frac{4\pi}{2l+1}} \sum_{m'=-l}^{l} D_{m'0}^l(\varphi', \theta', 0)Y_l^{m'}(\theta, \varphi)
= \frac{4\pi}{2l+1} \sum_{m=-l}^l Y_{l}^{m*}(\theta',\varphi') Y_{l}^m(\theta, \varphi)
$$
For ex., consider a frame's anticlockwise $90^\circ$ rotation around the $y$-axis ($\alpha = 0, \beta = \pi/2, \gamma = 0$) within the $l=1$ subspace. The Wigner small $d$-matrix evaluates to,
$$
d^1_{m'm}\left(\frac{\pi}{2}\right)
= \begin{pmatrix} \cos^2\frac{\beta}{2} & -\frac{\sin\beta}{\sqrt{2}} & \sin^2\frac{\beta}{2} \\[5pt] \frac{\sin\beta}{\sqrt{2}} & \cos\beta & -\frac{\sin\beta}{\sqrt{2}} \\[5pt] \sin^2\frac{\beta}{2} & \frac{\sin\beta}{\sqrt{2}} & \cos^2\frac{\beta}{2} \end{pmatrix}_{\beta=\frac{\pi}{2}}
= \begin{pmatrix} \frac{1}{2} & -\frac{1}{\sqrt{2}} & \frac{1}{2} \\[5pt] \frac{1}{\sqrt{2}} & 0 & -\frac{1}{\sqrt{2}} \\[5pt] \frac{1}{2} & \frac{1}{\sqrt{2}} & \frac{1}{2} \end{pmatrix}
$$
where rows and columns map to $m', m = 1, 0, -1$ respectively. We construct the linear combination $Y_1^{x}(\theta, \varphi) \equiv \frac{-Y_1^{1} + Y_1^{-1}}{\sqrt{2}}\propto \sin\theta\cos\varphi\propto \frac{x}{r}$. The rotation gives,
$$
Y_1^{0}(\theta', \varphi') = \sum_{m'=-1}^1 d^1_{m'0} Y_1^{m'}(\theta,\varphi)= Y_1^{x}(\theta, \varphi)  \propto \cos\theta' = \frac{z'}{r}
$$
Consequently, an anticlockwise rotation of the frame by $\beta = \pi/2$ around the $+y$-axis maps the old $x$-axis onto the new $z'$-axis ($x \to z'$). This means the original $x$-oriented dipole $Y_1^{x}(\theta, \varphi)$ transforms directly into a $z'$-oriented dipole $Y_1^{0}(\theta', \varphi')$.

Finally, the Wigner $D$-matrix and small $d$-matrix elements can be computed analytically using the built-in `WignerD` function in Wolfram Mathematica (MMA), with the following syntax,
$$
\begin{aligned}
D_{m'm}^l(\alpha, \beta, \gamma) &\implies \texttt{WignerD[\{l, mp, m\}, }\alpha\texttt, \beta\texttt, \gamma\texttt{]} \\[5pt]
d_{m'm}^l(\beta) &\implies \texttt{WignerD[\{l, mp, m\}, }\beta\texttt{]}
\end{aligned}
$$
Btw, the result from MMA differs by a transpose from the discussion above, but we still follow the same convention as Wikipedia and most textbooks.



















