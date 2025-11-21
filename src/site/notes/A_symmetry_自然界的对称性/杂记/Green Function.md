---
{"dg-publish":true,"permalink":"/A_symmetry_自然界的对称性/杂记/Green Function/","noteIcon":"default","created":"2025-11-19T12:10:15.473+08:00","updated":"2025-11-21T21:44:44.139+08:00"}
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
u(x^\sigma) = \int_{\mathbb{R}^n} G(x^\sigma, x'^\sigma) f(x'^\sigma) ~\mathrm{d}^nx' \tag{1}
$$
{ #f56309}


为原方程的解。
# 2 实例  
## 2.1 真空静电场  
静电场满足的泊松方程  
$$
\nabla^2 \varphi(\boldsymbol{x}) = - \frac{\rho(\boldsymbol{x})}{\epsilon_0}
$$
对应的格林函数满足  
$$
\nabla^2 G = \delta^3 (\boldsymbol{x} - \boldsymbol{x}')
$$
方便起见，记 ${\boldsymbol{r}} = \boldsymbol{x} - \boldsymbol{x}'=  (\underset{x-x'}{\underbrace{\bar x}}, \bar y, \bar z)$, ${\boldsymbol{\rho}} = (\alpha, \beta, \gamma)$，上式变为 $\nabla^2 G({\boldsymbol{r}}) = \delta^3 ({\boldsymbol{r}})$，记，对上式做 Fourier 变换，即  
$$
\begin{aligned} 
\tilde{G}(\alpha,\beta,\gamma) 
&= \iiint_{\mathbb{R}^3} G(\bar x, \bar y, \bar z) e^{-i(\alpha \bar x +\beta \bar y + \gamma \bar z)} \mathrm{d} \bar x \mathrm{d} \bar y \mathrm{d} \bar z
=  \iiint_{\mathbb{R}^3} G({\boldsymbol{r}}) e^{-i {\boldsymbol{\rho}}\cdot{\boldsymbol{r}}} \mathrm{d}^3 {\boldsymbol{r}}   \\[6pt]
G(\bar x, \bar y, \bar z) 
&=\frac{1}{(2\pi)^3} \iiint_{\mathbb{R}^3} \tilde{G}({\boldsymbol{r}}) e^{i(\bar x \alpha + \bar y\beta + \bar z \gamma)} \mathrm{d} \alpha \mathrm{d}\beta \mathrm{d}\gamma
=\frac{1}{(2\pi)^3} \iiint_{\mathbb{R}^3} \tilde{G}({\boldsymbol{r}}) e^{i{\boldsymbol{\rho}}\cdot{\boldsymbol{r}}} \mathrm{d}^3 {\boldsymbol{\rho}}
\end{aligned}
$$
正变换得到  
$$
-(\alpha^2 + \beta^2 + \gamma^2) \tilde{G } = 1 
\quad\Rightarrow \quad
\tilde{G } = -\frac{1}{\rho^2}, \quad \rho^2 = \alpha^2 + \beta^2 + \gamma^2
$$
于是反变换($RFT$)并采取球坐标  
$$
\theta = \langle \boldsymbol{\rho}, \bar{\boldsymbol{r}} \rangle
,\quad
\alpha = \rho \sin\theta \cos\varphi , \quad
\beta = \rho\sin\theta \sin \varphi ,\quad
\gamma = \rho \cos\theta
$$
得到：  
$$
\begin{aligned} 
G(\bar x, \bar y, \bar z) 
&=
-\frac{1}{(2\pi)^3} \iiint_{\mathbb{R}^3} \frac{e^{i(\rho r \cos\theta)}}{\rho^2} \cdot \rho^2 \sin\theta ~\mathrm{d} {{\rho}} \mathrm{d} \theta \mathrm{d}\varphi \\[4pt]
&=
-\frac{1}{(2\pi)^2} \int_0^{+\infty} \mathrm{d}\rho\int_0^\pi {e^{i\rho r \cos\theta}} \sin\theta ~\mathrm{d} {{\rho}} \mathrm{d} \theta \\[4pt]
&=
-\frac{1}{2\pi^2 r} \int_0^{+\infty} \frac{{\sin r\rho}}{\rho} ~\mathrm{d} \rho  \\[4pt]
&=
-\frac{1}{4\pi r}
\end{aligned}
$$
于是根据式 [[#^f56309|(1)]] 得到势函数为
$$
\begin{aligned} 
\varphi(x,y,z) &=
\end{aligned}
$$


## 2.2 Klein-Gorden 方程  
## 2.3 运动电荷的推迟势  
## 2.4 弱引力波







