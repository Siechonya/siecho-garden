---
{"dg-publish":true,"permalink":"/A_symmetry_自然界的对称性/Applications/Appendix for ED formulas/","noteIcon":"default","created":"2026-06-15T09:49:53.224+08:00","updated":"2026-06-14T21:35:27.140+08:00","dg-note-properties":{}}
---

> This document supplements some rather complex proof processes within [[A_symmetry_自然界的对称性/Applications/ED Formulas\|ED Formulas]] and [[A_symmetry_自然界的对称性/Applications/ED formulas (2)\|ED formulas (2)]] 

# 1 $\iiint_V \boldsymbol{E}(\boldsymbol{x}) \,\mathrm{d}^3x = -\frac{\boldsymbol{p}}{3\epsilon_0}$  
<font color="#ff0000">Let</font> $V$ be a spherical volume of radius $R$ that completely encloses all charges, meaning the charge density $\rho(\boldsymbol{x}')$ vanishes for all $r' > R$. Without loss of generality, we place the coordinate origin at the center of the sphere $V$. According to Coulomb's law, the electric field $\boldsymbol{E}(\boldsymbol{x})$ at any field point $\boldsymbol{x}$ inside the sphere is given by the volume integral over the source coordinates $\boldsymbol{x}'$,
$$
\boldsymbol{E}(\boldsymbol{x}) = \frac{1}{4\pi\varepsilon_0} \int_{V} \rho(\boldsymbol{x}') \frac{\boldsymbol{x} - \boldsymbol{x}'}{|\boldsymbol{x} - \boldsymbol{x}'|^3} \, \mathrm{d}^3x'
$$
We want to evaluate the volume integral of $\boldsymbol{E}(\boldsymbol{x})$ over the entire sphere $V$,
$$
\int_V \boldsymbol{E}(\boldsymbol{x}) \, \mathrm{d}^3x = \frac{1}{4\pi\varepsilon_0} \int_V \left[ \int_{V} \rho(\boldsymbol{x}') \frac{\boldsymbol{x} - \boldsymbol{x}'}{|\boldsymbol{x} - \boldsymbol{x}'|^3} \, \mathrm{d}^3x' \right] \mathrm{d}^3x
$$
Since the region of integration is bounded and the charge distribution is well-behaved, we can apply Fubini's theorem to switch the order of the volume integrals over $\mathrm{d}^3x$ and $\mathrm{d}^3x'$,
$$
\int_V \boldsymbol{E}(\boldsymbol{x}) \, \mathrm{d}^3x = \frac{1}{4\pi\varepsilon_0} \int_{V} \rho(\boldsymbol{x}') \left[ \int_V \frac{\boldsymbol{x} - \boldsymbol{x}'}{|\boldsymbol{x} - \boldsymbol{x}'|^3} \, \mathrm{d}^3x \right] \mathrm{d}^3x'
$$
Let us denote the inner vector integral as $\boldsymbol{I}(\boldsymbol{x}')$,
$$
\boldsymbol{I}(\boldsymbol{x}') = \int_V \frac{\boldsymbol{x} - \boldsymbol{x}'}{|\boldsymbol{x} - \boldsymbol{x}'|^3} \, \mathrm{d}^3x
$$
We recognize that the integrand can be expressed as the negative gradient with respect to the field point $\boldsymbol{x}$,
$$
\frac{\boldsymbol{x} - \boldsymbol{x}'}{|\boldsymbol{x} - \boldsymbol{x}'|^3} = -\nabla \left( \frac{1}{|\boldsymbol{x} - \boldsymbol{x}'|} \right)
$$
Substituting this identity into $\boldsymbol{I}(\boldsymbol{x}')$ and applying a corollary of the divergence theorem (converting a volume integral of a gradient into a closed surface integral), we obtain,
$$\boldsymbol{I}(\boldsymbol{x}') = -\int_V \nabla \left( \frac{1}{|\boldsymbol{x} - \boldsymbol{x}'|} \right) \mathrm{d}^3x = -\oint_{\partial V} \frac{1}{|\boldsymbol{x} - \boldsymbol{x}'|} \hat{\boldsymbol{n}} \, \mathrm{d}A$$
where $\partial V$ represents the bounding spherical surface at $r = R$, and $\hat{\boldsymbol{n}}$ is the outward unit normal vector. On this spherical surface, the field point is $\boldsymbol{x} = R\hat{\boldsymbol{x}}$ (where $\hat{\boldsymbol{x}}$ is the radial unit vector $\hat{\boldsymbol{r}}$), and the area element is $\mathrm{d}A = R^2 \, \mathrm{d}\Omega$. Thus, the integral becomes,
$$\boldsymbol{I}(\boldsymbol{x}') = -R^2 \oint_{r=R} \frac{1}{|\boldsymbol{x} - \boldsymbol{x}'|} \hat{\boldsymbol{x}} \, \mathrm{d}\Omega$$
Because all charges are enclosed within the sphere, the source point always lies inside ($r' < R$), while the field point in the surface integral lies exactly on the boundary ($r = R$). Since $r' < r$, we can expand the reciprocal distance $1/|\boldsymbol{x} - \boldsymbol{x}'|$ into a series of Legendre polynomials,
$$\frac{1}{|\boldsymbol{x} - \boldsymbol{x}'|} = \sum_{l=0}^{\infty} \frac{(r')^l}{R^{l+1}} P_l(\cos\gamma)$$
where $\gamma$ is the angle between $\boldsymbol{x}$ and $\boldsymbol{x}'$.

To evaluate the solid angle integral, we temporarily align the $z$-axis along the direction of $\boldsymbol{x}'$, making $\gamma = \theta$ (the standard polar angle). The unit vector $\hat{\boldsymbol{x}}$ expands in Cartesian components as,
$$
\hat{\boldsymbol{x}} = \sin\theta\cos\phi \hat{\boldsymbol{i}} + \sin\theta\sin\phi \hat{\boldsymbol{j}} + \cos\theta \hat{\boldsymbol{k}}
$$
Integrating over the azimuthal angle $\phi$ from $0$ to $2\pi$, the terms containing $\cos\phi$ and $\sin\phi$ vanish identically due to periodicity. The only surviving component is along the $\hat{\boldsymbol{k}}$ direction (which is the direction of $\hat{\boldsymbol{x}}'$),
$$
\oint_{r=R} \frac{1}{|\boldsymbol{x} - \boldsymbol{x}'|} \hat{\boldsymbol{x}} \, \mathrm{d}\Omega = \hat{\boldsymbol{x}}' \int_0^{2\pi} \mathrm{d}\phi \int_0^\pi \left[ \sum_{l=0}^{\infty} \frac{(r')^l}{R^{l+1}} P_l(\cos\theta) \right] \cos\theta \sin\theta \, \mathrm{d}\theta
$$
Noting that $\cos\theta = P_1(\cos\theta)$, we invoke the orthogonality condition for Legendre polynomials,
$$
\int_0^\pi P_l(\cos\theta) P_1(\cos\theta) \sin\theta \, \mathrm{d}\theta = \frac{2}{2(1)+1}\delta_{l,1} = \frac{2}{3}\delta_{l,1}
$$
Hence, only the $l = 1$ term yields a non-zero contribution to the infinite series,
$$
\oint_{r=R} \frac{1}{|\boldsymbol{x} - \boldsymbol{x}'|} \hat{\boldsymbol{x}} \, \mathrm{d}\Omega = \hat{\boldsymbol{x}}' \cdot 2\pi \cdot \frac{r'}{R^2} \cdot \frac{2}{3} = \frac{4\pi}{3R^2} (r'\hat{\boldsymbol{x}}') = \frac{4\pi}{3R^2} \boldsymbol{x}'
$$
Substituting this result back into the expression for $\boldsymbol{I}(\boldsymbol{x}')$, the radius $R^2$ cancels out smoothly,
$$
\boldsymbol{I}(\boldsymbol{x}') = -R^2 \left( \frac{4\pi}{3R^2} \boldsymbol{x}' \right) = -\frac{4\pi}{3} \boldsymbol{x}'
$$
We now feed $\boldsymbol{I}(\boldsymbol{x}')$ back into our original total electric field volume integral,
$$
\int_V \boldsymbol{E}(\boldsymbol{x}) \, \mathrm{d}^3x = -\frac{1}{3\varepsilon_0} \int_{V} \rho(\boldsymbol{x}') \boldsymbol{x}' \, \mathrm{d}^3x'
$$
By definition, the total electric dipole moment $\boldsymbol{p}$ of the localized charge distribution with respect to our chosen origin is,
$$
\boldsymbol{p} = \int_{V} \rho(\boldsymbol{x}') \boldsymbol{x}' \, \mathrm{d}^3x'
$$
Replacing the integral with $\boldsymbol{p}$, we arrive at,
$$
\int_V \boldsymbol{E}(\boldsymbol{x}) \, \mathrm{d}^3x = -\frac{\boldsymbol{p}}{3\varepsilon_0}
$$
<font color="#ff0000">Next</font>, we consider the alternative case where all charges lie entirely outside the spherical volume $V$, meaning the charge density $\rho(\boldsymbol{x}')$ vanishes for all $r' \le R$. According to Coulomb's law, the electric field $\boldsymbol{E}(\boldsymbol{x})$ at any field point $\boldsymbol{x}$ inside the sphere is given by the volume integral over the external source coordinates $\boldsymbol{x}'$,
$$
\boldsymbol{E}(\boldsymbol{x}) = \frac{1}{4\pi\varepsilon_0} \int_{V_{\text{ext}}} \rho(\boldsymbol{x}') \frac{\boldsymbol{x} - \boldsymbol{x}'}{|\boldsymbol{x} - \boldsymbol{x}'|^3} \, \mathrm{d}^3x'
$$
We want to evaluate the volume integral of $\boldsymbol{E}(\boldsymbol{x})$ over the entire sphere $V$,
$$
\int_V \boldsymbol{E}(\boldsymbol{x}) \, \mathrm{d}^3x = \frac{1}{4\pi\varepsilon_0} \int_V \left[ \int_{V_{\text{ext}}} \rho(\boldsymbol{x}') \frac{\boldsymbol{x} - \boldsymbol{x}'}{|\boldsymbol{x} - \boldsymbol{x}'|^3} \, \mathrm{d}^3x' \right] \mathrm{d}^3x
$$
Since the region of integration is bounded and the charge distribution is well-behaved, we can apply Fubini's theorem to switch the order of the volume integrals over $\mathrm{d}^3x$ and $\mathrm{d}^3x'$ again,
$$
\int_V \boldsymbol{E}(\boldsymbol{x}) \, \mathrm{d}^3x = \frac{1}{4\pi\varepsilon_0} \int_{V_{\text{ext}}} \rho(\boldsymbol{x}') \left[ \int_V \frac{\boldsymbol{x} - \boldsymbol{x}'}{|\boldsymbol{x} - \boldsymbol{x}'|^3} \, \mathrm{d}^3x \right] \mathrm{d}^3x'
$$
Let us also denote the inner vector integral as $\boldsymbol{I}(\boldsymbol{x}')$,
$$
\boldsymbol{I}(\boldsymbol{x}') = \int_V \frac{\boldsymbol{x} - \boldsymbol{x}'}{|\boldsymbol{x} - \boldsymbol{x}'|^3} \, \mathrm{d}^3x
$$
We recognize that the integrand can be expressed as the negative gradient with respect to the field point $\boldsymbol{x}$,
$$
\frac{\boldsymbol{x} - \boldsymbol{x}'}{|\boldsymbol{x} - \boldsymbol{x}'|^3} = -\nabla \left( \frac{1}{|\boldsymbol{x} - \boldsymbol{x}'|} \right)
$$
Substituting this identity into $\boldsymbol{I}(\boldsymbol{x}')$ and applying a corollary of the divergence theorem (converting a volume integral of a gradient into a closed surface integral), we obtain,
$$\boldsymbol{I}(\boldsymbol{x}') = -\int_V \nabla \left( \frac{1}{|\boldsymbol{x} - \boldsymbol{x}'|} \right) \mathrm{d}^3x = -\oint_{\partial V} \frac{1}{|\boldsymbol{x} - \boldsymbol{x}'|} \hat{\boldsymbol{n}} \, \mathrm{d}A$$
where $\partial V$ represents the bounding spherical surface at $r = R$, and $\hat{\boldsymbol{n}}$ is the outward unit normal vector. On this spherical surface, the field point is $\boldsymbol{x} = R\hat{\boldsymbol{x}}$ (where $\hat{\boldsymbol{x}}$ is the radial unit vector $\hat{\boldsymbol{r}}$), and the area element is $\mathrm{d}A = R^2 \, \mathrm{d}\Omega$. Thus, the integral becomes,
$$
\boldsymbol{I}(\boldsymbol{x}') = -R^2 \oint_{r=R} \frac{1}{|\boldsymbol{x} - \boldsymbol{x}'|} \hat{\boldsymbol{x}} \, \mathrm{d}\Omega
$$
Because all charges lie outside the sphere, the source point always lies exterior ($r' > R$), while the field point in the surface integral lies exactly on the boundary ($r = R$). Since $r < r'$, we can expand the reciprocal distance $1/|\boldsymbol{x} - \boldsymbol{x}'|$ into a series of Legendre polynomials,
$$
\frac{1}{|\boldsymbol{x} - \boldsymbol{x}'|} = \sum_{l=0}^{\infty} \frac{R^l}{(r')^{l+1}} P_l(\cos\gamma)
$$
where $\gamma$ is the angle between $\boldsymbol{x}$ and $\boldsymbol{x}'$.

To evaluate the solid angle integral, we temporarily align the $z$-axis along the direction of $\boldsymbol{x}'$, making $\gamma = \theta$ (the standard polar angle). The unit vector $\hat{\boldsymbol{x}}$ expands in Cartesian components as,
$$
\hat{\boldsymbol{x}} = \sin\theta\cos\phi \hat{\boldsymbol{i}} + \sin\theta\sin\phi \hat{\boldsymbol{j}} + \cos\theta \hat{\boldsymbol{k}}
$$
Integrating over the azimuthal angle $\phi$ from $0$ to $2\pi$, the terms containing $\cos\phi$ and $\sin\phi$ vanish identically due to periodicity. The only surviving component is along the $\hat{\boldsymbol{k}}$ direction (which is the direction of $\hat{\boldsymbol{x}}'$),
$$
\oint_{r=R} \frac{1}{|\boldsymbol{x} - \boldsymbol{x}'|} \hat{\boldsymbol{x}} \, \mathrm{d}\Omega = \hat{\boldsymbol{x}}' \int_0^{2\pi} \mathrm{d}\phi \int_0^\pi \left[ \sum_{l=0}^{\infty} \frac{R^l}{(r')^{l+1}} P_l(\cos\theta) \right] \cos\theta \sin\theta \, \mathrm{d}\theta
$$
Noting that $\cos\theta = P_1(\cos\theta)$, we invoke the orthogonality condition for Legendre polynomials:
$$\int_0^\pi P_l(\cos\theta) P_1(\cos\theta) \sin\theta \, \mathrm{d}\theta = \frac{2}{2(1)+1}\delta_{l,1} = \frac{2}{3}\delta_{l,1}$$
Hence, only the $l = 1$ term yields a non-zero contribution to the infinite series,
$$
\oint_{r=R} \frac{1}{|\boldsymbol{x} - \boldsymbol{x}'|} \hat{\boldsymbol{x}} \, \mathrm{d}\Omega = \hat{\boldsymbol{x}}' \cdot 2\pi \cdot \frac{R}{(r')^2} \cdot \frac{2}{3} = \frac{4\pi R}{3(r')^2} \hat{\boldsymbol{x}}' = \frac{4\pi R}{3(r')^3} \boldsymbol{x}'
$$
Substituting this result back into the expression for $\boldsymbol{I}(\boldsymbol{x}')$, the variable factors yield,
$$
\boldsymbol{I}(\boldsymbol{x}') = -R^2 \left( \frac{4\pi R}{3(r')^3} \boldsymbol{x}' \right) = -\frac{4\pi R^3}{3(r')^3} \boldsymbol{x}'
$$
We now feed $\boldsymbol{I}(\boldsymbol{x}')$ back into our original total electric field volume integral,
$$
\int_V \boldsymbol{E}(\boldsymbol{x}) \, \mathrm{d}^3x = \frac{1}{4\pi\varepsilon_0} \int_{V_{\text{ext}}} \rho(\boldsymbol{x}') \left[ -\frac{4\pi R^3}{3(r')^3} \boldsymbol{x}' \right] \mathrm{d}^3x' = \frac{4\pi R^3}{3} \left[ \frac{1}{4\pi\varepsilon_0} \int_{V_{\text{ext}}} \rho(\boldsymbol{x}') \frac{-\boldsymbol{x}'}{(r')^3} \, \mathrm{d}^3x' \right]
$$
By definition, the electric field $\boldsymbol{E}(0)$ evaluated at the origin (the center of the sphere) produced by the external charge distribution is given by,
$$
\boldsymbol{E}(0) = \frac{1}{4\pi\varepsilon_0} \int_{V_{\text{ext}}} \rho(\boldsymbol{x}') \frac{\mathbf{0} - \boldsymbol{x}'}{|\mathbf{0} - \boldsymbol{x}'|^3} \, \mathrm{d}^3x' = \frac{1}{4\pi\varepsilon_0} \int_{V_{\text{ext}}} \rho(\boldsymbol{x}') \frac{-\boldsymbol{x}'}{(r')^3} \, \mathrm{d}^3x'
$$
Replacing the integral with $\boldsymbol{E}(0)$, we arrive at,
$$
\int_V \boldsymbol{E}(\boldsymbol{x}) \, \mathrm{d}^3x = \frac{4\pi R^3}{3} \boldsymbol{E}(0) = V \boldsymbol{E}(0)
$$
<font color="#ff0000">Now</font>, If all currents are contained within the sphere $V$, according to the Biot-Savart law, the magnetic field $\boldsymbol{B}(\boldsymbol{x})$ at any field point $\boldsymbol{x}$ inside the sphere is given by the volume integral over the localized current density $\boldsymbol{J}(\boldsymbol{x}')$,
$$
\boldsymbol{B}(\boldsymbol{x}) = \frac{\mu_0}{4\pi} \int_{V} \boldsymbol{J}(\boldsymbol{x}') \times \frac{\boldsymbol{x} - \boldsymbol{x}'}{|\boldsymbol{x} - \boldsymbol{x}'|^3} \, \mathrm{d}^3x'
$$
We want to evaluate the volume integral of $\boldsymbol{B}(\boldsymbol{x})$ over the entire sphere $V$,
$$
\int_V \boldsymbol{B}(\boldsymbol{x}) \, \mathrm{d}^3x = \frac{\mu_0}{4\pi} \int_V \left[ \int_{V} \boldsymbol{J}(\boldsymbol{x}') \times \frac{\boldsymbol{x} - \boldsymbol{x}'}{|\boldsymbol{x} - \boldsymbol{x}'|^3} \, \mathrm{d}^3x' \right] \mathrm{d}^3x
$$
Since the region of integration is bounded and the current distribution is well-behaved, we can apply Fubini's theorem to switch the order of the volume integrals over $\mathrm{d}^3x$ and $\mathrm{d}^3x'$,
$$
\int_V \boldsymbol{B}(\boldsymbol{x}) \, \mathrm{d}^3x = \frac{\mu_0}{4\pi} \int_{V} \left[ \int_V \boldsymbol{J}(\boldsymbol{x}') \times \frac{\boldsymbol{x} - \boldsymbol{x}'}{|\boldsymbol{x} - \boldsymbol{x}'|^3} \, \mathrm{d}^3x \right] \mathrm{d}^3x'
$$
Because the inner integral is performed with respect to the field coordinates $\boldsymbol{x}$, the current density $\boldsymbol{J}(\boldsymbol{x}')$ treats it as a constant vector factor. Thus, we can pull $\boldsymbol{J}(\boldsymbol{x}')$ out of the inner integration while carefully maintaining the vector cross product structure,
$$
\int_V \boldsymbol{B}(\boldsymbol{x}) \, \mathrm{d}^3x = \frac{\mu_0}{4\pi} \int_{V} \boldsymbol{J}(\boldsymbol{x}') \times \left[ \int_V \frac{\boldsymbol{x} - \boldsymbol{x}'}{|\boldsymbol{x} - \boldsymbol{x}'|^3} \, \mathrm{d}^3x \right] \mathrm{d}^3x'
$$
We immediately recognize that the vector integral inside the brackets is identical to the inner integral $\boldsymbol{I}(\boldsymbol{x}')$ defined in the electrostatic case,
$$
\boldsymbol{I}(\boldsymbol{x}') = \int_V \frac{\boldsymbol{x} - \boldsymbol{x}'}{|\boldsymbol{x} - \boldsymbol{x}'|^3} \, \mathrm{d}^3x
$$
Since all currents are enclosed within the sphere, the source point always lies inside ($r' < R$). We can directly substitute our previously derived result for $\boldsymbol{I}(\boldsymbol{x}')$ when $r' < R$, which is $\boldsymbol{I}(\boldsymbol{x}') = -\frac{4\pi}{3} \boldsymbol{x}'$,
$$
\int_V \boldsymbol{B}(\boldsymbol{x}) \, \mathrm{d}^3x = \frac{\mu_0}{4\pi} \int_{V} \boldsymbol{J}(\boldsymbol{x}') \times \left( -\frac{4\pi}{3} \boldsymbol{x}' \right) \mathrm{d}^3x'
$$
Using the anticommutativity of the cross product ($\boldsymbol{A} \times (-\boldsymbol{B}) = \boldsymbol{B} \times \boldsymbol{A}$), the negative sign is smoothly absorbed by reversing the order of the vectors,
$$
\int_V \boldsymbol{B}(\boldsymbol{x}) \, \mathrm{d}^3x = \frac{\mu_0}{3} \int_{V} \boldsymbol{x}' \times \boldsymbol{J}(\boldsymbol{x}') \, \mathrm{d}^3x'
$$
By definition, the total magnetic dipole moment $\boldsymbol{m}$ of the localized current distribution is given by,
$$
\boldsymbol{m} = \frac{1}{2} \int_{V} \boldsymbol{x}' \times \boldsymbol{J}(\boldsymbol{x}') \, \mathrm{d}^3x'
$$
Replacing the integral with $2\boldsymbol{m}$, we arrive at the final result,
$$
\int_V \boldsymbol{B}(\boldsymbol{x}) \, \mathrm{d}^3x = \frac{2\mu_0}{3}\boldsymbol{m}
$$
<font color="#ff0000">Next</font>, we consider the alternative case where all currents lie entirely outside the spherical volume $V$, meaning the current density $\boldsymbol{J}(\boldsymbol{x}')$ vanishes for all $r' \le R$. According to the Biot-Savart law, the magnetic field $\boldsymbol{B}(\boldsymbol{x})$ at any field point $\boldsymbol{x}$ inside the sphere is given by the volume integral over the external source coordinates $\boldsymbol{x}'$,
$$
\boldsymbol{B}(\boldsymbol{x}) = \frac{\mu_0}{4\pi} \int_{V_{\text{ext}}} \boldsymbol{J}(\boldsymbol{x}') \times \frac{\boldsymbol{x} - \boldsymbol{x}'}{|\boldsymbol{x} - \boldsymbol{x}'|^3} \, \mathrm{d}^3x'
$$
We evaluate the volume integral of $\boldsymbol{B}(\boldsymbol{x})$ over the entire sphere $V$, and switch the order of integration via Fubini's theorem,
$$
\int_V \boldsymbol{B}(\boldsymbol{x}) \, \mathrm{d}^3x = \frac{\mu_0}{4\pi} \int_{V_{\text{ext}}} \boldsymbol{J}(\boldsymbol{x}') \times \left[ \int_V \frac{\boldsymbol{x} - \boldsymbol{x}'}{|\boldsymbol{x} - \boldsymbol{x}'|^3} \, \mathrm{d}^3x \right] \mathrm{d}^3x'
$$
Because all currents lie outside the sphere, the source point always satisfies $r' > R$. Utilizing the corresponding external result for the inner integral $\boldsymbol{I}(\boldsymbol{x}') = -\frac{4\pi R^3}{3(r')^3} \boldsymbol{x}'$, we substitute it back into the equation,
$$
\int_V \boldsymbol{B}(\boldsymbol{x}) \, \mathrm{d}^3x = \frac{\mu_0}{4\pi} \int_{V_{\text{ext}}} \boldsymbol{J}(\boldsymbol{x}') \times \left[ -\frac{4\pi R^3}{3(r')^3} \boldsymbol{x}' \right] \mathrm{d}^3x'
$$
Applying the anticommutativity of the cross product to eliminate the negative sign yields,
$$
\int_V \boldsymbol{B}(\boldsymbol{x}) \, \mathrm{d}^3x = \frac{4\pi R^3}{3} \left[ \frac{\mu_0}{4\pi} \int_{V_{\text{ext}}} \frac{\boldsymbol{x}' \times \boldsymbol{J}(\boldsymbol{x}')}{(r')^3} \, \mathrm{d}^3x' \right]
$$
By definition, the magnetic field $\boldsymbol{B}(0)$ evaluated at the center of the sphere produced by the external current distribution is given by,
$$
\boldsymbol{B}(0) = \frac{\mu_0}{4\pi} \int_{V_{\text{ext}}} \boldsymbol{J}(\boldsymbol{x}') \times \frac{\mathbf{0} - \boldsymbol{x}'}{|\mathbf{0} - \boldsymbol{x}'|^3} \, \mathrm{d}^3x' = \frac{\mu_0}{4\pi} \int_{V_{\text{ext}}} \frac{\boldsymbol{x}' \times \boldsymbol{J}(\boldsymbol{x}')}{(r')^3} \, \mathrm{d}^3x'
$$
Replacing the bracketed integral with $\boldsymbol{B}(0)$, we arrive at,
$$
\int_V \boldsymbol{B}(\boldsymbol{x}) \, \mathrm{d}^3x = \frac{4\pi R^3}{3} \boldsymbol{B}(0) = V \boldsymbol{B}(0)
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
# 3 Example: 2D Laplace Equation in a Rectangular Pipe
An infinitely long rectangular conducting pipe is formed by four mutually insulated plates. Three of the plates are maintained at zero potential, while the fourth is kept at a constant potential $V_0$. Find the electrostatic potential inside the pipe?

Let the cross-section of the pipe have a width $a$ along the $x$-axis and a height $b$ along the $y$-axis. Due to translational symmetry along the infinite length ($z$-axis), $\frac{\partial \varphi}{\partial z} = 0$. The problem reduces to a 2D domain: $x \in [0, a]$ and $y \in [0, b]$. The boundary conditions are:
$$
\varphi(0, y) = 0,\quad\varphi(a, y) = 0,\quad\varphi(x, 0) = 0,\quad\varphi(x, b) = V_0
$$
The potential inside the charge-free pipe satisfies the 2D Laplace equation, Substituting $\varphi(x, y) = X(x)Y(y)$ and dividing by $\varphi$ yields,
$$
\frac{\partial^2 \varphi}{\partial x^2} + \frac{\partial^2 \varphi}{\partial y^2} = 0
\implies
\frac{1}{X}\frac{\mathrm{d}^2 X}{\mathrm{d}x^2} + \frac{1}{Y}\frac{\mathrm{d}^2 Y}{\mathrm{d}y^2} = 0
$$
Since the $x$-direction is bounded on both ends and requires zero potential at the boundaries, it must yield an oscillatory (trigonometric) solution. Thus, we assign a negative separation constant $-k^2$ to the $x$-term:
$$X''(x) + k^2 X(x) = 0,\quad Y''(y) - k^2 Y(y) = 0$$
The general solution for $X(x)$ is $X(x) = A \sin(kx) + B \cos(kx)$. Applying the boundary conditions yields the discrete eigenvalues,
$$
k_n = \frac{n\pi}{a}, \quad (n = 1, 2, 3, \ldots)
\implies
X_n(x) = \sin\left(\frac{n\pi x}{a}\right)
$$
For the $y$-direction, the general solution to $Y''(y) - k_n^2 Y(y) = 0$ is expressed via hyperbolic functions as $Y(y) = C \sinh(k_n y) + D \cosh(k_n y)$. Imposing the base boundary condition $Y(0) = 0 \implies D = 0$, leaving $Y_n(y) = \sinh\left(\frac{n\pi y}{a}\right)$.

Invoking the principle of linear superposition, the total potential inside the pipe is represented as the infinite series:
$$
\varphi(x, y) = \sum_{n=1}^{\infty} A_n \sin\left(\frac{n\pi x}{a}\right) \sinh\left(\frac{n\pi y}{a}\right)
$$
To determine the remaining coefficients $A_n$, we apply the final inhomogeneous boundary condition at the top plate $y = b$,
$$\varphi(x, b) = \sum_{n=1}^{\infty} A_n \sinh\left(\frac{n\pi b}{a}\right) \sin\left(\frac{n\pi x}{a}\right) = V_0$$
Exploiting the orthogonality of the sine functions over the interval $[0, a]$, we project the constant potential $V_0$ into its Fourier components,
$$
A_n \sinh\left(\frac{n\pi b}{a}\right) = \frac{2}{a} \int_0^a V_0 \sin\left(\frac{n\pi x}{a}\right) \,\mathrm{d}x = \frac{2V_0}{n\pi} \left[1 - (-1)^n\right]
$$
This integral vanishes for all even integers $n$. For odd integers, letting $n = 2m+1$ (where $m = 0, 1, 2, \dots$), the non-zero coefficients are isolated as,
$$
A_{2m+1} = \frac{4V_0}{(2m+1)\pi \sinh\left(\frac{(2m+1)\pi b}{a}\right)}
$$
Substituting $A_{2m+1}$ back into the generalized series provides the final analytical solution for the potential distribution inside the rectangular pipe,
$$
\varphi(x, y) = \frac{4V_0}{\pi} \sum_{m=0}^{\infty} \frac{1}{2m+1} \frac{\sinh\left(\frac{(2m+1)\pi y}{a}\right)}{\sinh\left(\frac{(2m+1)\pi b}{a}\right)} \sin\left(\frac{(2m+1)\pi x}{a}\right)
$$
# 4 Physical Interpretation of the Sign and Energy Definitions *  
The choice of a positive sign in the generalized force relation $\boldsymbol{F} = +\nabla U$ arises from the thermodynamics of systems with <font color="#ff0000">constant</font> currents, which differs fundamentally from electrostatic systems. Two distinct definitions of magnetic interaction energy exist depending on the physical constraints of the system,

- Passive Mechanical Potential Energy ($U_{\text{mech}} = -\boldsymbol{m}\cdot\boldsymbol{B}$)
	- This definition treats the magnetic dipole as a rigid, isolated system with fixed currents where no external energy exchange occurs during displacement. In this case, the mechanical work is done entirely at the expense of this potential energy, preserving the classical relation $\boldsymbol{F} = -\nabla U_{\text{mech}}$.

- Field Interaction Energy ($U_{\text{field}} = +\boldsymbol{m}\cdot\boldsymbol{B}$)
	- This is derived directly from the macroscopic field energy expression $\int \boldsymbol{J}\cdot\boldsymbol{A}\,\mathrm{d}V$. Here, the currents $\boldsymbol{J}$ are held strictly constant during any displacement. To maintain constant currents against the back-EMF induced by the motion, external power supplies must perform work on the system.

A more explicit comparison is presented here. In an electric field with fixed charges, when an electric dipole is displaced, <font color="#245bdb">the charge distribution remains naturally invariant</font>, and no external energy is required to maintain the charges. Consequently, the mechanical work is done entirely at the expense of the electrostatic potential energy, satisfying the classical mechanical relation $\boldsymbol{F} = -\nabla U_{\text{e,field}}$, where $U_{\text{e,field}} = -\boldsymbol{p}\cdot\boldsymbol{E}$.
  
But in a magnetic field with fixed currents, when a loop (magnetic dipole) undergoes displacement, <font color="#245bdb">the variation in magnetic flux induces an electromotive force within the circuit which tends to change the current inrensity</font>. To maintain a constant current $\boldsymbol{J}$ within the loop, the external power supplies maintaining the current must perform work against this induced EMF. The work done by the sources $\mathrm{d}W_{\text{source}}$ is precisely twice the mechanical work performed $\mathrm{d}W_{\text{mech}}$ ($\mathrm{d}W_{\text{source}} = 2\mathrm{d}W_{\text{mech}}$), which leads to $\boldsymbol{F} = +\nabla U_{\text{m,field}}$.

To prove the relation $\boldsymbol{F} = +\nabla U_{\text{field}}$ and demonstrate the mechanism of the external sources, consider a system of two circuits with constant currents $I_1$ and $I_2$, self-inductances $L_1$ and $L_2$, and mutual inductance $M$. The total magnetic energy of the system is,
$$
W = \frac{1}{2}L_1 I_1^2 + \frac{1}{2}L_2 I_2^2 + M I_1 I_2
$$
When circuit $I$ undergoes a virtual displacement $\mathrm{d}\boldsymbol{x}$, the mutual inductance changes by $\mathrm{d}M$. The mechanical work done by the magnetic force is,
$$
\mathrm{d}W_{\text{mech}} = \boldsymbol{F}\cdot\mathrm{d}\boldsymbol{x} = I_1 I_2 \mathrm{d}M
$$
Concurrently, the changing magnetic flux induces electromotive forces in both circuits due to Faraday's law,
$$
\mathcal{E} = -\frac{ \mathrm{d} \Phi }{ \mathrm{d} t} \implies
\mathcal{E}_{1,\text{ind}} = -I_2 \frac{\mathrm{d}M}{\mathrm{d}t}, \quad \mathcal{E}_{2,\text{ind}} = -I_1 \frac{\mathrm{d}M}{\mathrm{d}t}
$$
To maintain constant currents, the external power sources must counteract these induced EMFs, performing work equal to,
$$
\mathrm{d}W_{\text{source}} = \left(-\mathcal{E}_{1,\text{ind}} I_1 - \mathcal{E}_{2,\text{ind}} I_2\right)\mathrm{d}t = 2 I_1 I_2 \mathrm{d}M = 2 \mathrm{d}W_{\text{mech}}
$$
The change in the stored field energy $\mathrm{d}U_{\text{field}}$ is the difference between the energy supplied by the sources and the mechanical work performed,
$$
\mathrm{d}U_{\text{field}} = \mathrm{d}W_{\text{source}} - \mathrm{d}W_{\text{mech}} = 2\mathrm{d}W_{\text{mech}} - \mathrm{d}W_{\text{mech}} = +\mathrm{d}W_{\text{mech}}
$$
Since $\mathrm{d}U_{\text{field}} = \nabla U_{\text{field}}\cdot\mathrm{d}\boldsymbol{x}$ and $-\mathrm{d}U_{\text{mech}} = \mathrm{d}W_{\text{mech}} = \boldsymbol{F}\cdot\mathrm{d}\boldsymbol{x}$, it follows that,
$$
\boldsymbol{F} = +\nabla U_{\text{field}}
$$
# 5 Liénard-Wiechert potential  
Here $t_r=t-\frac{|\boldsymbol{x}-\boldsymbol{x'}|}{c}$, thus
$$
\begin{align} 
\varphi (\boldsymbol{x} , t) 
&=
\frac{1}{4\pi \epsilon_0} \int \frac{\rho(\boldsymbol{x}', t_r)}{|\boldsymbol{x}-\boldsymbol{x'}|} \mathrm{d}^3x'
\\[8pt]&=
\frac{e}{4 \pi \epsilon_{0}} \int d^{3} x^{\prime} \frac{\delta^{3}\left(\boldsymbol{x}^{\prime}-\boldsymbol{x}_{e}\left(t-\frac{\left|\boldsymbol{x}-\boldsymbol{x}^{\prime}\right|}{c}\right)\right)}{\left|\boldsymbol{x}-\boldsymbol{x}^{\prime}\right|}
\\[8pt]&=
\frac{e}{4\pi \epsilon_0} \int  \mathrm{d}^3x' \int \frac{   \delta^{3}\left(\boldsymbol{x}^{\prime}-\boldsymbol{x}_{e}(s)\right)    }{|\boldsymbol{x}-\boldsymbol{x'}|} \delta\left( s-\left( t-\frac{|\boldsymbol{x}-\boldsymbol{x'}|}{c} \right) \right)  \,\mathrm{d}s
\\[8pt]&=
\frac{e}{4\pi \epsilon_0} \int \frac{  \delta\left( s-\left( t-\frac{|\boldsymbol{x}-\boldsymbol{x}_e(s)|}{c} \right) \right)  }{|\boldsymbol{x}-\boldsymbol{x}_e(s)|}\,\mathrm{d}s,
\quad \boldsymbol{R}(s,\boldsymbol{x}) \triangleq \boldsymbol{x} - \boldsymbol{x}_e(s)
\\[8pt]&=
\frac{e}{4\pi \epsilon_0} \int \frac{  \delta\left( s-t^* \right)  }{|\boldsymbol{x}-\boldsymbol{x}_e(s)| \cdot \left| {\partial\left( s-\left( t-\frac{|\boldsymbol{x}-\boldsymbol{x}_e(s)|}{c} \right) \right)}/{\partial s} \right|_{t^*} }  \,\mathrm{d}s,\quad
\left[ s-\left( t-\frac{|\boldsymbol{x}-\boldsymbol{x}_e(s)|}{c} \right) \right]_{t^*}=0
\\[8pt]&=
\frac{e}{4\pi \epsilon_0} \int \frac{  \delta\left( s-t^* \right)  }{|\boldsymbol{x}-\boldsymbol{x}_e(s)|  \left( 1-\hat{R}(t^*)\cdot\boldsymbol{\beta}(t^*) \right) }  \,\mathrm{d}s
\\[8pt]&=
\frac{e}{4\pi \epsilon_0}  \frac{ 1 }{  {R}(t^*) -\boldsymbol{R}(t^*)\cdot\boldsymbol{\beta}(t^*) }
\end{align}
$$
To understand the additional factor $1-\hat{R}(t^*)\cdot\boldsymbol{\beta}(t^*)$ compared with the electrostatic potential of stationary charge point $e$, differentiating $t^* = t-\frac{|\boldsymbol{x}-\boldsymbol{x}_e(t^*)|}{c}$ leads to,
$$
\mathrm{d} t=\mathrm{d} t^*+\frac{1}{c} \frac{\partial R(\boldsymbol{x},t^*)}{\partial t^*} \mathrm{~d} t^*=(1-\hat{R} \cdot \boldsymbol{\beta})|_{t^*} \,\mathrm{d} t^*
$$
$$
\implies
\mathrm{d} t^*= \left.\frac{\mathrm{d} t}{1-\hat{R} \cdot \boldsymbol{\beta}}\right|_{t^*}
$$
# 6 Lorentz Transformation of the Angular Distribution of Emitted Radiation Power
Let $K$ be the laboratory frame and $K'$ be the instantaneous rest frame of the moving particle. Let $\frac{\mathrm{d}P}{\mathrm{d}\Omega}$ denote the angular radiation power emitted per retarded time in $K$, and $\frac{\mathrm{d}P'}{\mathrm{d}\Omega'}$ in $K'$. The angular distribution transforms as,
$$
\frac{\mathrm{d}P}{\mathrm{d}\Omega} = \frac{1}{\gamma^4 (1 - \beta \cos\theta)^3} \frac{\mathrm{d}P'}{\mathrm{d}\Omega'} = \gamma^2 (1 - \beta \cos\theta')^3 \frac{\mathrm{d}P'}{\mathrm{d}\Omega'}
$$
where $\theta$ (or $\theta'$) is the angle between the velocity $\boldsymbol{\beta}$ and the direction of observation in $K$ (or $K'$).   

The emitted radiation energy $\mathrm{d}W$ and its momentum $\mathrm{d}\boldsymbol{p}$ form a four-momentum vector $\mathrm{d}p^\mu = (\mathrm{d}W/c, \mathrm{d}\boldsymbol{p})$ for the radiation field. Since the radiation propagates at the speed of light, the momentum magnitude satisfies $|\mathrm{d}\boldsymbol{p}| = \mathrm{d}W/c$, and its component along the direction of motion is $\mathrm{d}p_\parallel = (\mathrm{d}W/c)\cos\theta$. Under the Lorentz transformation from $K$ to $K'$, the energy transforms as,
$$
\mathrm{d}W' = \gamma (\mathrm{d}W - v \mathrm{d}p_\parallel) = \gamma \mathrm{d}W (1 - \beta \cos\theta)
$$
Inverting this relation yields the radiation energy expressed in the laboratory frame,
$$
\mathrm{d}W = \frac{\mathrm{d}W'}{\gamma (1 - \beta \cos\theta)}
$$
Meanwhile, the retarded time interval $\mathrm{d}t_r$ represents the time duration of the emission process measured in the laboratory frame $K$. Because the particle is instantaneously at rest in $K'$, the time interval $\mathrm{d}t_r'$ is identical to the particle's proper time interval $\mathrm{d}\tau$. According to time dilation, the time intervals in the two frames are related by,
$$
\mathrm{d}t_r = \gamma \mathrm{d}\tau = \gamma \mathrm{d}t_r'
$$
From the relativistic aberration of light, the relationship between $\theta'$ and $\theta$ is given by,
$$
\cos\theta' = \frac{\cos\theta - \beta}{1 - \beta \cos\theta}
$$
We have proved the formula in the homework. Differentiating both sides yields,
$$
-\sin\theta' \mathrm{d}\theta' = \frac{-\sin\theta (1 - \beta \cos\theta) - (\cos\theta - \beta)(\beta \sin\theta)}{(1 - \beta \cos\theta)^2} \mathrm{d}\theta = -\frac{\sin\theta (1 - \beta^2)}{(1 - \beta \cos\theta)^2} \mathrm{d}\theta
= -\frac{\sin\theta \mathrm{d}\theta}{\gamma^2 (1 - \beta \cos\theta)^2}
$$
Since the system possesses azimuthal symmetry around the axis of motion, the azimuthal angle is invariant under the Lorentz boost ($\mathrm{d}\phi = \mathrm{d}\phi'$). Consequently, the differential solid angle $\mathrm{d}\Omega = \sin\theta \mathrm{d}\theta \mathrm{d}\phi$ transforms as,
$$
\mathrm{d}\Omega' = \frac{\mathrm{d}\Omega}{\gamma^2 (1 - \beta \cos\theta)^2} \implies \mathrm{d}\Omega = \gamma^2 (1 - \beta \cos\theta)^2 \mathrm{d}\Omega'
$$
Substituting the three transformation relations obtained above into the definition of angular radiation power gives,
$$
\frac{\mathrm{d}P}{\mathrm{d}\Omega} = \frac{\mathrm{d}W}{\mathrm{d}t_r \mathrm{d}\Omega} = \frac{\frac{\mathrm{d}W'}{\gamma (1 - \beta \cos\theta)}}{\left( \gamma \mathrm{d}t_r' \right) \left( \gamma^2 (1 - \beta \cos\theta)^2 \mathrm{d}\Omega' \right)}
$$
Combining the identical algebraic factors in the denominator yields,
$$
\frac{\mathrm{d}P}{\mathrm{d}\Omega} = \frac{1}{\gamma^4 (1 - \beta \cos\theta)^3} \frac{\mathrm{d}W'}{\mathrm{d}t_r' \mathrm{d}\Omega'} = \frac{1}{\gamma^4 (1 - \beta \cos\theta)^3} \frac{\mathrm{d}P'}{\mathrm{d}\Omega'}
$$
The relationship between $\theta'$ and $\theta$ can also be written as $\cos\theta = \frac{\cos\theta' + \beta}{1 + \beta \cos\theta'}$, substituting this into the tracking factor yields,
$$1 - \beta \cos\theta = 1 - \beta \left( \frac{\cos\theta' + \beta}{1 + \beta \cos\theta'} \right) = \frac{1 + \beta \cos\theta' - \beta \cos\theta' - \beta^2}{1 + \beta \cos\theta'} = \frac{1 - \beta^2}{1 + \beta \cos\theta'} = \frac{1}{\gamma^2 (1 + \beta \cos\theta')}$$
Plugging this expression back into the denominator of the power transformation formula gives,
$$
\frac{\mathrm{d}P}{\mathrm{d}\Omega} = \gamma^2 (1 + \beta \cos\theta')^3 \frac{\mathrm{d}P'}{\mathrm{d}\Omega'}
$$
# 7 The $4/3$ paradox and Poincaré stresses
The relation $m_{\text{em}} = \frac{4}{3}\frac{W_0}{c^2}$ is odds with Einstein's mass-energy equivalence $E=mc^2$. This discrepancy arises because the electromagnetic energy-momentum tensor alone cannot describe a closed, conserved system: a static charge distribution would fly apart under Coulomb repulsion, and the integrated four‑momentum fails to be a Lorentz four‑vector.

To stabilize the classical electron, non‑electromagnetic binding forces must exist. Henri Poincaré introduced these as Poincaré stresses, which contribute additional mechanical energy and stress. The mechanical work required to hold the charge together supplies an energy $W_{\text{mech}} = \frac{1}{3}W_0$. Summing the electromagnetic and mechanical parts, the total rest energy $W_{\text{tot}}$ and the observed mass $m$ perfectly restore the covariant relation
$$
W_{\text{tot}} = W_0 + W_{\text{mech}} = \frac{4}{3}W_0 = m c^2
$$
Thus the $4/3$ factor is an artifact of neglecting the Poincaré stresses necessary for structural stability. We now derive the precise contribution $W_{\text{mech}} = \frac{1}{3}W_0$ from the local conservation of the total energy-momentum tensor.

In the electron’s rest frame the system is static and stable. The total tensor $T^{\mu\nu} = T_{\text{em}}^{\mu\nu} + T_{\text{mech}}^{\mu\nu}$ must satisfy $\partial_\mu T^{\mu\nu}=0$. For the spatial components ($\nu=j=1,2,3$) this gives,
$$
\partial_i T^{ij} = \partial_i (T_{\text{em}}^{ij} + T_{\text{mech}}^{ij}) = 0
$$
Using the identity $T^{ij} = \partial_k (T^{ik} x^j) - (\partial_k T^{ik}) x^j$ together with the symmetry and static conservation $\partial_k T^{ik}=0$ ($\because \partial_0 =0$), we obtain,
$$
\int_{\mathbb{R}^3} T^{ij} d^3x = \int_{\mathbb{R}^3} \partial_k (T^{ik} x^j) d^3x = 0
$$
where the second equality follows from Gauss’s theorem and the localized nature of the fields $\partial_0=0$. Taking the trace of this spatial tensor equation yields,
$$
\int_{\mathbb{R}^3} \sum_{i=1}^3 T_{\text{em}}^{ii} d^3x + \int_{\mathbb{R}^3} \sum_{i=1}^3 T_{\text{mech}}^{ii} d^3x = 0
$$
For a static electric field the Maxwell stress tensor is,
$$
T_{\text{em}}^{ij} = -\epsilon_0 \left( E^i E^j - \frac{1}{2}\delta^{ij} E^2 \right)
$$
so that its spatial trace becomes,
$$
\sum_{i=1}^3 T_{\text{em}}^{ii} = -\epsilon_0 \left( E^2 - \frac{3}{2}E^2 \right) = \frac{1}{2}\epsilon_0 E^2 = w_0 
$$
where $w_0$ is the electrostatic energy density. Integrating over all space gives the total electrostatic self‑energy,
$$
W_0 = \int_{\mathbb{R}^3} \sum_{i=1}^3 T_{\text{em}}^{ii} d^3x = \int_{\mathbb{R}^3} w_0 d^3x 
$$
Poincaré modelled the stabilizing force as a Lorentz‑invariant scalar pressure $P$, described by the covariant tensor,
$$
T_{\text{mech}}^{\mu\nu} = P g^{\mu\nu} 
$$
In the rest frame this yields $T_{\text{mech}}^{00} = -P$ and $\sum_{i=1}^3 T_{\text{mech}}^{ii} = 3P$. Substituting the electromagnetic and mechanical traces into the vanishing trace condition gives,
$$
W_0 + \int_{\mathbb{R}^3} 3P d^3x = 0 \quad\Longrightarrow\quad \int_{\mathbb{R}^3} P d^3x = -\frac{1}{3}W_0 
$$
The total rest mechanical energy is the volume integral of the mechanical energy density,
$$
W_{\text{mech}} = \int_{\mathbb{R}^3} T_{\text{mech}}^{00} d^3x = \int_{\mathbb{R}^3} (-P) d^3x = \frac{1}{3}W_0 
$$
Combining the electromagnetic and mechanical contributions, the total rest energy of the stabilized electron becomes,
$$
W_{\text{tot}} = W_0 + W_{\text{mech}} = W_0 + \frac{1}{3}W_0 = \frac{4}{3}W_0 
$$
Recalling that $m_{\text{em}} = \frac{4}{3}\frac{W_0}{c^2}$, we obtain,
$$
W_{\text{tot}} = m_{\text{em}} c^2
$$
Once the Poincaré stresses required for mechanical stability are properly included, the total energy and momentum transform together as a genuine Lorentz four‑vector $P^\mu = (W_{\text{tot}}/c, \mathbf{P}_{\text{tot}})$, completely resolving the classical $4/3$ paradox.



