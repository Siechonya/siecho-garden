---
{"dg-publish":true,"permalink":"/_Documents/references/1-3 Appendix B/","noteIcon":"default","created":"2025-12-01T12:16:37.187+08:00","updated":"2025-08-14T21:49:20.323+08:00"}
---

For $k_\perp = k_\perp (\omega, X) = k\sin\psi$ and $k_\parallel = k_\parallel(\omega, X) =k \cos\psi$, the Jacobian is given by  
$$
\left| J\left( \frac{k_\perp, k_\parallel}{\omega, X} \right) \right|
= \begin{vmatrix} \frac{\partial k_\perp}{\partial \omega} & \frac{\partial k_\perp}{\partial X} 
\\ 
\frac{\partial k_\parallel}{\partial \omega} & \frac{\partial k_\parallel}{\partial X} \end{vmatrix}
\tag{B1}
$$
Using the standard rules for manipulating derivatives (e.x., Chain rule) gives  
$$
\left. \frac{\partial k_\perp}{\partial \omega} \right|_X = \sin\psi \left. \frac{\partial k}{\partial \omega} \right|_X \tag{B2}
$$
and  
$$
\begin{align}
\left. \frac{\partial k_\parallel}{\partial \omega} \right|_X 
= \cos\psi \left. \frac{\partial k}{\partial \omega} \right|_X + k \left. \frac{\partial (\cos\psi)}{\partial X} \right|_\omega \tag{B3}
\\[6pt]
= \cos\psi \left. \frac{\partial k}{\partial \omega} \right|_X - k \sin\psi \cos^2\psi \tag{B4}
\end{align}
$$
Similarly,  
$$
\begin{align}
\left. \frac{\partial k_\perp}{\partial X} \right|_\omega 
&= \sin\psi \left. \frac{\partial k}{\partial X} \right|_\omega + k \cos^3\psi
\tag{B5}
\\[6pt]
\left. \frac{\partial k_\perp}{\partial X} \right|_\omega 
&= \cos\psi \left. \frac{\partial k}{\partial X} \right|_\omega \tag{B6}
\end{align}
$$
Combining these results gives the Jacobian as  
$$
\left| J\left( \frac{k_\perp, k_\parallel}{\omega, X} \right) \right| = -k \cos^2\psi \left. \frac{\partial k}{\partial \omega} \right|_X 
\tag{B7}
$$
The derivative term, $\frac{\partial k}{\partial \omega}$, in the above equation can be found by differentiating the dispersion relation $\mathcal{D} (k, \omega, X) = 0$ to give  
$$
\frac{d\mathcal{D} }{d\omega} = \frac{\partial \mathcal{D} }{\partial \omega} + \frac{\partial \mathcal{D} }{\partial k} \frac{\partial k}{\partial \omega} = 0 \tag{B8}
$$
so  
$$
\left| J\left( \frac{k_\perp, k_\parallel}{\omega, X} \right) \right|
= k \cos^2\psi \frac{\partial \mathcal{D}}{\partial \omega} \left( \frac{\partial \mathcal{D}}{\partial k} \right)^{-1} \tag{B9}
$$
Thus in [[_Documents/references/1-3 Appendix A\|1-3 Appendix A]], one find
$$
\begin{align}
N(\omega) 
&= \frac{1}{2\pi^2} \int_{X_\text{min}}^{X_\text{max}} g(X) 
\left|J\left( \frac{k_\perp, k_\parallel}{\omega, X} \right)\right|
k_\perp \mathrm{d}X
\\[8pt]
&=\frac{1}{2\pi^{2}}\int_{X_{\min}}^{X_{\max}}\frac{g(X)k^{2}}{(1 + X^{2})^{\frac{3}{2}}}\frac{\partial \mathcal{D}}{\partial\omega}\left[\frac{\partial \mathcal{D}}{\partial k}\right]^{-1}X\mathrm{d}X
\tag{add}
\end{align}
$$
