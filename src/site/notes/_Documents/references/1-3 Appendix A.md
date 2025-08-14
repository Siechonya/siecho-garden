---
{"dg-publish":true,"permalink":"/_Documents/references/1-3 Appendix A/","noteIcon":"","created":"2025-08-08T00:16:24.374+08:00","updated":"2025-08-14T21:49:14.055+08:00"}
---

The elements of the diffusion matrix, $D$, are given by  
$$
\begin{align}
D_{\alpha\alpha} = \sum_{n=-\infty}^{\infty} \int_0^\infty k_\perp dk_\perp D_{\alpha\alpha}^{nk_\perp} \tag{A1} 
\\
D_{\alpha p} = D_{p\alpha} = \sum_{n=-\infty}^{\infty} \int_0^\infty k_\perp dk_\perp D_{\alpha p}^{nk_\perp} \tag{A2}
\\
D_{pp} = \sum_{n=-\infty}^{\infty} \int_0^\infty k_\perp dk_\perp D_{pp}^{nk_\perp} \tag{A3}
\end{align}
$$
For each harmonic resonance number $n$ and $k_\perp$, the pitch-angle diffusion coefficient $D_{\alpha\alpha}^{nk_\perp}$ is given by  
$$
D_{\alpha\alpha}^{nk_\perp} 
= \lim_{V\to\infty} \frac{q_\sigma^2}{4\pi V} 
\left. \left[ \frac{n\Omega_\sigma/(\gamma\omega) - \sin^2\alpha}{\cos\alpha} \right]^2 \frac{|\Theta_{nk}|^2}{\left| v_\parallel - \frac{\partial \omega}{\partial k_\parallel} \right|} \right|_{k_\parallel} \tag{A4}
$$
The right-hand side of equation (A4) is evaluated at the resonant parallel wave number $k_\parallel$ and frequency $\omega$ that satisfies the resonance condition  
$$
\omega - k_\parallel v_\parallel = n\Omega_\sigma/\gamma \tag{A5}
$$
The value of $\Theta_{nk}$ is given by  
$$
\Theta_{nk} = \frac{v_\parallel}{v_\perp} E_{k, \parallel} J_n + \frac{E_{k, L} J_{n-1} + E_{k, R} J_{n+1}}{\sqrt{2}} \tag{A6}
$$
where $J_n$ is the n-th order Bessel function with argument $k_\perp p_\perp /(m_\sigma \Omega_\sigma)$, and the Fourier transform of the wave electric field has been written in terms of its parallel $E_{k,\parallel}$, left-hand $E_{k, L}$, and right-hand $E_{k, R}$, components, with  
$$
\begin{align}
E_{k, L} = \frac{1}{\sqrt{2}} \left( E_{k, x} + iE_{k, y} \right) \tag{A7}
\\
E_{k, R} = \frac{1}{\sqrt{2}} \left( E_{k, x} - iE_{k, y} \right) \tag{A8}
\end{align}
$$
From equations A7 and A8, we can easily solve for $E_{k,x}$ and $E_{k,y}$:
$$
E_{k,x} = \frac{1}{\sqrt{2}}(E_{k,L} + E_{k,R})
, \quad
E_{k,y} = \frac{1}{i\sqrt{2}}(E_{k,L} - E_{k,R})
\tag{add}
$$
Using cold plasma theory, $E_{k, L}$ and $E_{k, R}$ can be rewritten in terms of $E_{k,\parallel}$, the refractive index $\mu$, the wave-normal angle $\psi$, and the Stix parameters $R, L, S,D,$ and $P$ [Lyons, 1974b], to give  
$$
\begin{align}
E_{k,L} =\left( \frac{\mu^2 \sin^2\psi - P}{\mu^2 \sin\psi \cos\psi}\right) \left( 1 - \frac{D}{(\mu^2 - S)} \right) \frac{E_{k,\parallel}}{\sqrt{2}} \tag{A9}
\\
E_{k,R} = \left(\frac{\mu^2 \sin^2\psi - P}{\mu^2 \sin\psi \cos\psi}\right) \left( 1 + \frac{D}{(\mu^2 - S)} \right) \frac{E_{k,\parallel}}{\sqrt{2}} \tag{A10}
\end{align}
$$
> The Stix parameters are defined as:
> $$  \begin{align}
R &= 1 - \sum_\sigma \frac{\omega_{p\sigma}^2}{\omega(\omega - \Omega_\sigma)}
\\
 L &= 1 - \sum_\sigma \frac{\omega_{p\sigma}^2}{\omega(\omega + \Omega_\sigma)}
\\
P &= 1 - \sum_\sigma \frac{\omega_{p\sigma}^2}{\omega^2}
 \\
 S &= \frac{R+L}{2}
 \\
 D &= \frac{R-L}{2} 
\end{align}
\tag{add}
 $$

The Maxwell-Faraday equation in Fourier space is:
$$
\mathbf{k} \times \mathbf{E}_k = \omega \mathbf{B}_k
\quad\to\quad
|E_{k,\perp}| = c|\mathbf{B_k}|
\tag{add}
$$
and  
$$
|\mathbf{E}_k|^2 = |E_{k,\parallel}|^2 + |E_{k,\perp}|^2 = |E_{k,x}|^2 + |E_{k,y}|^2 
\tag{add}
$$
Thus, $E_{k,\parallel}$ can be written as a function of the magnitude of the Fourier transform of the wave magnetic field at each $\mathbf{k}$, namely $|\mathbf{B}_k|$:  
$$
|E_{k,\parallel}|^2 = \frac{c^2 |\mathbf{B}_k|^2}{\mu^2} \cdot
\left[ \left( \frac{R - L}{2(\mu^2 - S)} \right)^2  \left(\frac{\mu^2 \sin^2\psi - P}{\mu^2 \sin\psi \cos\psi} \right)^2+ \left( \frac{P}{\mu^2 \sin\psi} \right)^2 \right]^{-1} \tag{A11}
$$
Combining these results gives  
$$
|\Theta_{nk}|^2 = \frac{c^2 |\mathbf{B}_k|^2}{\mu^2} |\Phi_{n,k}|^2 \tag{A12}
$$
with  
$$
\begin{align}
|\Phi_{n,k}|^2 
&= 
\frac{
\left\{ 
\left[
\left( \frac{\mu^2 - L}{\mu^2 - S} \right) J_{n+1} + \left( \frac{\mu^2 - R}{\mu^2 - S} \right) J_{n-1}
\right]
\left( \frac{\mu^2 \sin^2\psi - P}{2\mu^2} \right) + \cot\alpha \sin\psi \cos\psi J_n 
\right\}^2
}
{
\left( \frac{R - L}{2(\mu^2 - S)} \right)^2 
\left(\frac{P - \mu^2 \sin^2\psi}{\mu^2}\right)^2 + \left( \frac{P\cos\psi}{\mu^2} \right)^2
\tag{A13}
}
\end{align}
$$
We assume that the wave magnetic field can be described by [Lyons, 1974b]  
$$
|\mathbf{B}_k|^2 = \frac{V}{N(\omega)} B^2(\omega) g(\psi) \tag{A14}
$$
with  
$$
N(\omega) = \frac{1}{2\pi^2} \int_{X_\text{min}}^{X_\text{max}} g(X) 
\left|J\left( \frac{k_\perp, k_\parallel}{\omega, X} \right)\right|
k_\perp \mathrm{d}X \tag{A15}
$$
Here $B^2(\omega)$ is the wave magnetic field intensity squared per unit frequency and $g(X)$ gives the variation of wave magnetic field energy with wave normal angle,  
$$
\begin{aligned}
g(X)= 
\begin{cases}
\exp\left[-\left(\frac{X - X_{m}}{X_{w}}\right)^{2}\right]   &  X_{\min} \leq X \leq X_{\max}
\\ 
0   &  \text{otherwise}, with~ X=\tan(\psi)
\end{cases}
\end{aligned} \tag{add}
$$
Using the cold plasma dispersion relation $\mathcal{D}(k, \omega, X) = 0$, and the Jacobian $J\left( \frac{k_\parallel, k_\perp}{\omega, X} \right)$, A15 can be rewritten to obtain the equation (see [[_Documents/references/1-3 Appendix B\|1-3 Appendix B]]):  
$$
N(\omega)=\frac{1}{2\pi^{2}}\int_{X_{\min}}^{X_{\max}}\frac{g(X)k^{2}}{(1 + X^{2})^{\frac{3}{2}}}\frac{\partial \mathcal{D}}{\partial\omega}\left[\frac{\partial \mathcal{D}}{\partial k}\right]^{-1}X\mathrm{d}X
\tag{add}
$$
Combining equations (A1)–(A3), (A4), and (A12) and transforming the integrals from $k_\perp$ to $X$ leads to the final form of the diffusion coefficients' expression:  
$$
\boxed{
\begin{align}
D_{\alpha\alpha} &= \sum_{n = n_{l}}^{n_{h}} \int_{X_{\min}}^{X_{\max}} XdXD_{\alpha\alpha}^{nX} \\ 
D_{\alpha p} &= D_{p\alpha} = \sum_{n = n_{l}}^{n_{h}} \int_{X_{\min}}^{X_{\max}} XdXD_{\alpha p}^{nX} \\ 
D_{pp} &= \sum_{n = n_{l}}^{n_{h}} \int_{X_{\min}}^{X_{\max}} XdXD_{pp}^{nX}
\end{align} 
}
$$
with  
$$
\begin{align}
D_{\alpha\alpha}^{nX} &= \sum_{i} \frac{q_{\sigma}^{2} \omega_{i}^{2}}{4\pi(1 + X^{2})N(\omega_{i})} \left[ \frac{n\Omega_{\sigma}/(\gamma\omega_{i}) - \sin^{2}\alpha}{\cos\alpha} \right]^{2} 
\cdot \left. B^{2}(\omega_{i})g(X) \frac{|\Phi_{n,k}|^2}{\left|v_{\parallel} - \frac{\partial\omega}{\partial k_{\parallel}}\right|}\right|_{k_{||i}}
\\
D_{\alpha p}^{nX} &= D_{\alpha\alpha}^{nX} \left[ \frac{\sin\alpha\cos\alpha}{n\Omega_{\sigma}/(\gamma\omega_{i}) - \sin^{2}\alpha} \right]_{k_{||i}} 
\\
D_{pp}^{nX} &= D_{\alpha\alpha}^{nX} \left[ \frac{\sin\alpha\cos\alpha}{n\Omega_{\sigma}/(\gamma\omega_{i}) - \sin^{2}\alpha} \right]_{k_{||i}}^{2} 
\end{align}
$$



