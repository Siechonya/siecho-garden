---
{"dg-publish":true,"permalink":"/A_symmetry_自然界的对称性/Applications/Notes for General Relativity/","noteIcon":"default","created":"2025-03-12T22:28:08.600+08:00","updated":"2025-12-03T18:47:51.317+08:00"}
---

# 1 Convention  
- natural unit system, Einstein's summation convention
- Minkowski metric $(-+++)$
$$
\eta_{\mu\nu} = \begin{bmatrix} -1 &   &   &   \\    & 1 &   &   \\   &   & 1 &   \\   &   &   & 1 \end{bmatrix}
$$
- Curvature
$$
R_{\mu\nu\lambda}^\rho(this\ document) = -\Gamma_{\mu\nu,\lambda}^\rho + \Gamma_{\mu\lambda,\nu}^\rho + \Gamma_{\mu\lambda}^\sigma \Gamma_{\sigma\nu}^\rho - \Gamma_{\mu\nu}^\sigma \Gamma_{\sigma\lambda}^\rho
= -R_{\mu\nu\lambda}^\rho (Weinberg)
$$
$$
R_{\mu\nu} = R_{\mu\nu\lambda}^\lambda
$$
- Christoffel symbols
$$
\Gamma^\lambda_{\mu\nu} = \frac{1}{2} g^{\lambda\rho} (g_{\mu\rho,\nu} + g_{\nu\rho,\mu} - g_{\mu\nu,\rho})
$$
$$
g_{\alpha\beta;\mu} = 0
$$
# 2 $f(R)$ Gravity & Field Eqn.  
> refer to [F(R) theories of gravitation - Scholarpedia](http://www.scholarpedia.org/article/F%28R%29_theories_of_gravitation)  

The total action of the known gravitational system is:
$$
S = \int \left[ f(R) + 16\pi G \cdot \mathcal{L}_m \right] \sqrt{-g} ~\mathrm{d}^4 x 
$$
In $f(R)$ gravity, the field equations are obtained by varying with respect to the metric and not treating the connection independently. The main steps are the same as in the case of the variation of the Hilbert-Einstein action but there are also some important differences.

The variation of the determinant is
$$
\delta \sqrt{-g}=-\frac{1}{2} \sqrt{-g} g_{\mu \nu} \delta g^{\mu \nu}, \quad here \ g = \det(g_{\mu\nu})
$$
The Ricci scalar is defined as
$$
R=g^{\mu \nu} R_{\mu \nu} .
$$
Therefore the variation with respect to the inverse metric $g^{\mu \nu}$ is given by
$$
\delta R=R_{\mu \nu} \delta g^{\mu \nu}+g^{\mu \nu} \delta R_{\mu \nu}
\overset{Palatini\ Eqn.}{=}R_{\mu \nu} \delta g^{\mu \nu}+g^{\mu \nu}\left((\delta \Gamma_{\rho \mu}^{\rho})_{;\nu} - \delta (\Gamma_{\nu \mu}^{\rho})_{ ;\rho}\right)
\tag{1}
$$
Since $\delta \Gamma^{\lambda}_{~\mu \nu}$ is the difference of two connections, it should transform as a tensor. Therefore, using $\Gamma^\lambda_{\mu\nu} = \frac{1}{2} g^{\lambda\rho} (g_{\mu\rho,\nu} + g_{\nu\rho,\mu} - g_{\mu\nu,\rho})$ and $\delta g^{\alpha\beta} = -g^{\mu\alpha}g^{\nu\beta}\delta g_{\mu\nu}$, it can be written as
$$
\delta \Gamma_{\mu \nu}^{\lambda}=\frac{1}{2} g^{\lambda \alpha}\left((\delta g_{\alpha \nu})_{;\mu}+(\delta g_{\alpha \mu})_{;\nu}-( \delta g_{\mu \nu})_{;\alpha} \right) .
$$
Substituting into the $Eqn. (1)$ yeilds:
$$
\delta R=R_{\mu \nu} \delta g^{\mu \nu}+
\underset{g^{\mu\nu}\delta R_{\mu\nu}}{\underbrace{  (\delta g^{\mu \nu})_{;\mu;\nu} - \square (g_{\mu \nu}\delta g^{\mu \nu})}}
$$
where "${;\mu}$" is the covariant derivative and $\square f=g^{\alpha\beta} f_{;\alpha;\beta}$ is the D'Alembert operator acting on the function $f$. Let us consider now a generic analytic function $f(R)$ obeying the variational principle $\delta \int d^{4} x \sqrt{-g} f(R)=0$. We have
$$
\begin{align}
\delta \int d^{4} x \sqrt{-g} f(R)
&=\int d^{4} x[\delta(\sqrt{-g}) f(R)+\sqrt{-g} \delta(f(R))] \\
&=\int d^{4} x \sqrt{-g}\left[f^{\prime}(R) R_{\mu \nu}-\frac{1}{2} g_{\mu \nu} f(R)\right] \delta g^{\mu \nu}+\int d^{4} x \sqrt{-g} f^{\prime}(R) g^{\mu \nu} \delta R_{\mu \nu}
\end{align}
$$
For the second item, performing integration by parts ($\int \mathrm{d}^4x \sqrt{-g} A^\mu_{;\mu}B = \underset{divergence \ term}{\underbrace{\int \mathrm{d}^4x \sqrt{-g} (A^\mu B)_{;\mu}} }  - \int \mathrm{d}^4x \sqrt{-g} A^\mu B_{;\mu}$, $\because A^\mu_{;\mu} =  \frac{1}{\sqrt{-g}}(\sqrt{-g} A^\mu)_{,\mu}$) and *ignoring the divergence term* will lead to
$$
\begin{aligned} 
\int d^{4} x \sqrt{-g} f^{\prime}(R) g^{\mu \nu} \delta R_{\mu \nu}
&=\int d^{4} x \sqrt{-g} ~ f^{\prime}(R) ((\delta g^{\mu \nu})_{;\mu;\nu} - \square (g_{\mu \nu}\delta g^{\mu \nu})) \\
&={\color{red}+}\int d^{4} x \sqrt{-g} ~ (f^{\prime}(R)_{;\mu;\nu} - g_{\mu \nu}\square f^{\prime}(R) ) \delta g^{\mu\nu}
\end{aligned}
$$
Thus  
$$
\begin{align}
\delta \int d^{4} x \sqrt{-g} f(R)
=\int d^{4} x \sqrt{-g}\left[
f^{\prime}(R) R_{\mu \nu}-\frac{1}{2} g_{\mu \nu} f(R) +  f^{\prime}(R)_{;\mu;\nu} - g_{\mu \nu}\square f^{\prime}(R)
\right] \delta g^{\mu \nu} 
\end{align}
$$
On the other hand, the variation of the action of the material part is
$$
\delta S_m = \delta \int 16\pi G \cdot \mathcal{L}_m  \sqrt{-g} ~\mathrm{d}^4 x = -8\pi G \int\mathrm{d}^4x\sqrt{-g}~ T_{\mu\nu} \delta g^{\mu\nu}
$$
Yield the $f(R)~ Field ~Eqn.$:  
$$
-f^{\prime} R_{\mu \nu}+\frac{1}{2} g_{\mu \nu} f  - f^{\prime}_{;\mu;\nu} + g_{\mu \nu}\square f^{\prime}
= -8\pi G  T_{\mu\nu}
$$
Substituting $f(R) = -R$ into the above eqn., one find  
$$
R_{\mu \nu}-\frac{1}{2} g_{\mu \nu} R= -8\pi G  T_{\mu\nu}
$$
That's So-called Hilbert-Einstein Field Equation.

















