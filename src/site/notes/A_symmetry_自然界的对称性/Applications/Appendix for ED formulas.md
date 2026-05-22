---
{"dg-publish":true,"permalink":"/A_symmetry_自然界的对称性/Applications/Appendix for ED formulas/","noteIcon":"default","created":"2026-05-20T11:12:27.839+08:00","updated":"2026-05-22T12:03:01.072+08:00","dg-note-properties":{}}
---

> This document supplements some rather complex proof processes within [[A_symmetry_自然界的对称性/Applications/ED Formulas\|ED Formulas]] and [[A_symmetry_自然界的对称性/Applications/ED formulas 2\|ED formulas 2]] 

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




















