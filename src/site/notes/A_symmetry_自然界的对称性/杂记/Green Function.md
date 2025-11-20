---
{"dg-publish":true,"permalink":"/A_symmetry_自然界的对称性/杂记/Green Function/","noteIcon":"default","created":"2025-11-19T12:10:15.473+08:00","updated":"2025-11-19T20:59:11.639+08:00"}
---

# 1 格林函数的引入  
记 $\mathbf{L}$ 为一般的微分算符，对于形如  
$$
\mathbf{L} u(x^\sigma) = f(x^\sigma), \quad x^\sigma \in \mathbb{R}, \quad \sigma=0,1,2\dots,n
$$
的微分方程，可以写出其基本解方程为：  
$$
\mathbf{L} G(x^\sigma, x'^\sigma) = \delta^n(x^\sigma - x'^\sigma)
$$
从中得到的基本解一般称为格林函数，容易证明，  
$$
u(x^\sigma) = \int_{\mathbb{R}^n} G(x^\sigma, x'^\sigma) f(x'^\sigma) ~\mathrm{d}^nx' 
$$
为原方程的解。
# 2 实例  
## 2.1 真空静电场  
静电场满足的泊松方程  
$$
\nabla^2 \varphi(\boldsymbol{x}) = - \frac{\rho(\boldsymbol{x})}{\epsilon_0}
$$
对应的格林函数满足  
$$
\nabla^2 G = \delta (\boldsymbol{x} - \boldsymbol{x}')
$$
方便起见，记 $\bar{\boldsymbol{x}} = \boldsymbol{x} - \boldsymbol{x}'$，上式变为 $\nabla^2 G(\bar x, \bar y, \bar z) = \delta (\bar x, \bar y, \bar z)$，对其做 Fourier 变换，即  
$$
\tilde{G}(\alpha,\beta,\gamma) = \iiint_{\mathbb{R}^3} G(\bar x, \bar y, \bar z) e^{-i(\alpha \hat x +\beta \hat y + \gamma \hat z)} \mathrm{d} \hat x \mathrm{d} \hat y \mathrm{d} \hat z
$$
得到  
$$
-(\alpha^2 + \beta^2 + \gamma^2) \tilde{G } = 1 
\quad\Rightarrow \quad
\tilde{G } = -\frac{1}{\rho^2}, \quad \rho^2 = \alpha^2 + \beta^2 + \gamma^2
$$

## 2.2 Klein-Gorden 方程  
## 2.3 运动电荷的推迟势  
## 2.4 弱引力波









