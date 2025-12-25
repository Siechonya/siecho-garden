---
{"dg-publish":true,"permalink":"/理力25秋/Answer for HW_13/","noteIcon":"default","created":"2025-12-18T10:56:36.074+08:00","updated":"2025-12-25T20:14:53.908+08:00"}
---

# 1 三维各向同性谐振子  
本题的哈密顿量表示的是一个 3-D 各向同性的谐振子，因此轨道是一个椭圆，该椭圆所在的平面经过原点。很容易发现，直角坐标中三个坐标的变化周期比是 $1:1:1$，柱坐标中是 $T_\rho:T_z:T_\theta=\frac{1}{2} : 1: 1$，球坐标中是 $T_r:T_\theta:T_\varphi = \frac{1}{2 } :1 :1$。所以，结果可以直接猜到：  
$$
H = \omega(J_x + J_y + J_z) = \omega (2J_\rho + J_\theta + J_z) = \omega (2J_r+J_\theta + J_\varphi)
$$
接下来是更严格的求解。
## 1.1 直角坐标  
已知基本关系：  
$$
L=\frac{m}{2}\left(\dot{x}^{2}+\dot{y}^{2}+ \dot{z}^{2} \right)- \frac{1}{2}m\omega^2 r^2
$$
$$
\vec{p}= \frac{ \partial L }{ \partial \dot{\vec{r}} } = m\dot{\vec{r}} 
$$
$$
H = \frac{p^2}{2m} + \frac{1}{2}m\omega^2r^2
$$
于是 $H-J$ 方程为  
$$
\frac{1}{2m}\left[\left(\frac{\partial S_0}{\partial x}\right)^2 + \left(\frac{\partial S_0}{\partial y}\right)^2 + \left(\frac{\partial S_0}{\partial z}\right)^2\right] + \frac{1}{2}m\omega^2(x^2 + y^2 + z^2) = E
$$
可以令 $S_{0}=S_x(x)+S_y(y) + S_z(z)$ ，代入上式，有
$$
\left[\frac{1}{2m}\left(\frac{dS_x}{dx}\right)^2 + \frac{1}{2}m\omega^2x^2\right] + \left[\frac{1}{2m}\left(\frac{dS_y}{dy}\right)^2 + \frac{1}{2}m\omega^2y^2\right] + \left[\frac{1}{2m}\left(\frac{dS_z}{dz}\right)^2 + \frac{1}{2}m\omega^2z^2\right] = E
$$
于是分离变量有  
$$
\left[\frac{1}{2m}\left(\frac{dS_i}{dx_i}\right)^2 + \frac{1}{2}m\omega^2 x_i^2\right] = E_i, \quad i = x,y,z
$$
作用变量  
$$
J_i = \frac{1}{2\pi} \oint p_i \mathrm{d}x_i, \quad 
p_i = \frac{ \partial S }{ \partial x_i } = \frac{ \mathrm{d} S_i }{ \mathrm{d} x_i}
= \sqrt{2mE_i - m^2\omega^2x_i^2}
$$
注意到取 $\left(\frac{dS_i}{dx_i}\right)^2=0$，可以得到运动范围 $x_i \in [-A_i,A_i],A_i = \sqrt{\frac{2E_i}{m\omega^2}}$，于是  
$$
J_i = \frac{1}{2\pi} \cdot 2 \int_{-A_i}^{A_i} \sqrt{2mE_i - m^2\omega^2x_i^2} ~\mathrm{d}x_i = \frac{E_i}{\omega},\quad i = x,y,z
$$
上面这个积分实际上就是 $\left[\frac{p_i^2}{2m} + \frac{1}{2}m\omega^2 x_i^2\right] = E_i$ 这个相空间椭圆的面积 $S$ 除以 $2\pi$，即：$J_i = \frac{1}{2\pi}S = \frac{1}{2\pi} \cdot\pi \sqrt{2mE_i \cdot \frac{2E_i}{m\omega^2}} = \frac{E_i}{\omega}$。所以新的哈密顿量为  
$$
H = \omega(J_x + J_y + J_z)
$$
角频率  
$$
\omega_i = \frac{ \partial H }{ \partial J_i } = \omega, \quad i = x,y,z
$$

## 1.2 柱坐标  
已知基本关系：  
$$
L=\frac{m}{2}\left(\dot{\rho}^{2}+\rho^{2} \dot{\theta}^{2}+\dot{z}^2\right) - \frac{1}{2}m\omega^2(\rho^2+z^2)
$$
$$
\begin{aligned}
p_{\rho} & =\frac{\partial L}{\partial \dot{\rho}}=m \dot{\rho} \\
p_{z} & =\frac{\partial L}{\partial \dot{z}}=m \dot{z} \\
p_{\theta} & =\frac{\partial L}{\partial \dot{\theta}}=m \rho^{2} \dot{\theta} 
\end{aligned}
$$
$$
H=\frac{1}{2 m}\left(p_{\rho}^{2}+\frac{p_{\theta}^{2}}{\rho^{2}}+p_{z}^{2}\right)+\frac{1}{2}m\omega^2(\rho^2+z^2)
$$
于是 $H-J$ 方程为  
$$
\frac{1}{2 m}\left(\frac{\partial S_{0}}{\partial \rho}\right)^{2}+\frac{1}{2}m\omega^2(\rho^2+z^2)+\frac{1}{2 m \rho^{2}}\left(\frac{\partial S_{0}}{\partial \theta}\right)^{2}+\frac{1}{2 m}\left(\frac{\partial S_{0}}{\partial z}\right)^{2}=E 
$$
可以令 $S_{0}=p_{\theta} \theta+S_{\rho}(\rho)+S_{z}(z)$ ，代入上式，分离变量有  
$$
\frac{ \mathrm{d} S_{\theta} }{ \mathrm{d} \theta} \equiv p_{\theta}
$$
$$
\frac{1}{2}m\omega^2z^2+\frac{1}{2 m}\left(\frac{\mathrm{d} S_{z}}{\mathrm{d} z}\right)^{2}=E_z
$$
$$
\frac{1}{2}m\omega^2\rho^2+ \frac{p_\theta^{2}}{2 m \rho^{2}} +\frac{1}{2 m}\left(\frac{\mathrm{d} S_{\rho}}{\mathrm{d} \rho}\right)^{2}=E_\rho
$$
作用量  
$$
J_\theta = \frac{1}{2\pi} \oint p_\theta \mathrm{d}\theta = p_\theta
$$
$$
J_z = \frac{1}{2\pi} \oint p_z \mathrm{d} z = \frac{E_z}{\omega}
$$
$$
\begin{align} 
J_\rho &= \frac{1}{2\pi} \oint p_\rho \mathrm{d} \rho \\[4pt]
&=
\frac{1}{\pi} \int_{\rho_{min}}^{\rho_{max}} \sqrt{2mE_\rho - m^2\omega^2\rho^2-  \frac{p_\theta^{2}}{\rho^{2}}} ~\mathrm{d}\rho \\[4pt]
&=
\frac{E_\rho}{2\omega} - \frac{|J_\theta|}{2}
\end{align}
$$
最后一个积分其实可以与 $\rho_{min,max}$ 无关，详见[[#附录%]]。于是  
$$
H = E_\rho + E_z = \omega (2J_\rho + |J_\theta| + J_z)
$$
$$
\omega_i = \frac{ \partial H }{ \partial J_i } = 2\omega, ~~\omega \cdot \text{sign}(J_\theta), ~~\omega, \quad i=\rho,\theta,z
$$
## 1.3 球坐标
已知基本关系：  
$$
L=\frac{m}{2}\left(\dot{r}^{2}+r^{2} \dot{\theta}^{2}+r^{2} \dot{\varphi}^{2} \sin ^{2} \theta\right)-V(r, \theta, \varphi)
,\quad V(r) = \frac{1}{2}m\omega^2r^2
$$
$$
\begin{aligned}
p_{r} & =\frac{\partial L}{\partial \dot{r}}=m \dot{r} \\
p_{\theta} & =\frac{\partial L}{\partial \dot{\theta}}=m r^{2} \dot{\theta} \\
p_{\varphi} & =\frac{\partial L}{\partial \dot{\varphi}}=m r^{2} \dot{\varphi} \sin ^{2} \theta
\end{aligned}
$$
$$
H=\dot{r} p_{r}+\dot{\theta} p_{\theta}+\dot{\varphi} p_{\varphi}-L=\frac{1}{2 m}\left(p_{r}^{2}+\frac{p_{\theta}^{2}}{r^{2}}+\frac{p_{\varphi}^{2}}{r^{2} \sin ^{2} \theta}\right)+V(r, \theta, \varphi)
$$
于是 $H-J$ 方程为  
$$
\frac{1}{2 m}\left(\frac{\partial S_{0}}{\partial r}\right)^{2}+\frac{1}{2}m\omega^2r^2+\frac{1}{2 m r^{2}}\left(\frac{\partial S_{0}}{\partial \theta}\right)^{2}+\frac{1}{2 m r^{2} \sin ^{2} \theta}\left(\frac{\partial S_{0}}{\partial \varphi}\right)^{2}=E 
$$
可以令 $S_{0}=p_{\varphi} \varphi+S_{r}(r)+S_{\theta}(\theta)$ ，代入上式，分离变量有  
$$
\frac{ \mathrm{d} S_\varphi }{ \mathrm{d} \varphi} \equiv p_\varphi
$$
$$
\left(\frac{\mathrm{d} S_{\theta}}{\mathrm{~d} \theta}\right)^{2}+\frac{p_{\varphi}^{2}}{\sin ^{2} \theta}=L^2
$$
$$
\frac{1}{2 m}\left(\frac{\mathrm{~d} S_{r}}{d r}\right)^{2}+\frac{1}{2}m\omega^2r^2+\frac{L^2}{2 m r^{2}}=E
$$
作用量  
$$
J_\varphi =  \frac{1}{2\pi} \oint p_\varphi \mathrm{d}\varphi = p_\varphi
$$
$$
\begin{align} 
J_\theta &=  \frac{1}{2\pi} \oint p_\theta \mathrm{d}\theta \\[4pt]
&=
\frac{1}{\pi} \int_{\theta_{min}}^{\theta_{max}} \sqrt{L^2-\frac{p_{\varphi}^{2}}{\sin ^{2} \theta}} ~\mathrm{d}\theta \\[4pt]
&=
\frac{1}{\pi} \int_{\arcsin|\frac{p_\varphi}{L}|}^{\pi-\arcsin|\frac{p_\varphi}{L}|} \sqrt{L^2-\frac{p_{\varphi}^{2}}{\sin ^{2} \theta}} ~\mathrm{d}\theta \\[4pt]
&=
L - |p_\varphi|
\end{align}
$$
$$
J_r = \frac{1}{2\pi} \oint p_r \mathrm{d}r = \frac{1}{\pi} \int_{r_{min}}^{r_{max}} \sqrt{2mE + 2m^2\omega^2 r^2 - \frac{L^2}{r^2}} \mathrm{d}r = - 2\pi i (Res(0) + Res(\infty)) = \frac{E}{2\omega} - \frac{L}{2}
$$
最后一个积分的计算方式和柱坐标的 $J_\rho$ 类似。就得到  
$$
H =E = \omega (2J_r+J_\theta + |J_\varphi|)
$$
$$
\omega_i = \frac{ \partial H }{ \partial J_i } = 2\omega,~~\omega,~~\omega \cdot \text{sign}(J_\varphi), \quad i = r,\theta,\varphi
$$
# 2 位力定理  
直接计算：
$$
\begin{align} 
I_r + I_\theta
&= \int m\dot{r}\,\mathrm{d}r + \int mr^2\dot{\theta} \mathrm{d}\theta \\[4pt]
&=
\int_0^T (m\dot{r}^2 + mr^2\dot{\theta}^2)\, \mathrm{d}t, \quad T为运动周期
\\[4pt]
&=
2\int_0^T E_k\,\mathrm{d}t,\quad E_k 为动能
\\[4pt]
&=
2T \cdot \frac{1}{T}\int_0^T E_k\,\mathrm{d}t = 2T \langle E_k\rangle
\end{align}
$$
根据位力定理，$\langle E_k\rangle = -\frac{1}{2} \langle V\rangle$，所以
$$
\begin{align} 
I_r + I_\theta
&= -T \langle V\rangle
\\[4pt]
&=
\int_0^T \frac{k}{r}\,\mathrm{d}t 
\end{align}
$$
成立。  
# 3 平面谐振子  
## 3.1 
$$
I_i =  \frac{1}{2\pi}\oint p_i \mathrm{d}x = \frac{1}{2\pi} \int_0^{T_i} \omega_i \dot{x_i}^2 \mathrm{d}t,\quad i=x,y
$$
所以  
$$
2\,\langle E_k  \rangle = 2\pi\,(\frac{I_x}{T_x} + \frac{I_y}{T_y})
$$
根据位力定理  
$$
\langle V \rangle = \langle E_k \rangle
$$
所以  
$$
E \equiv \langle V \rangle + \langle E_k \rangle =  2\pi\,(\frac{I_x}{T_x} + \frac{I_y}{T_y})
$$
## 3.2 
$$
\omega_i = \frac{ \partial E }{ \partial I_i } = \frac{2\pi}{T_i} = \dot{\varphi}_i, \quad i=x,y
$$
$$
\Rightarrow \quad \varphi_i = \omega_i t + \varphi_{i0}
$$
$$
\Rightarrow 
E =  \omega_x I_x + \omega_y I_y = \frac{1}{2}m\omega_x^2 A_x^2 + \frac{1}{2}m\omega_y^2 A_y^2 \quad \Rightarrow \quad A_i = \sqrt{\frac{2 I_i}{m \omega_i}}
$$
所以  
$$
x_i = A_i \cos(\omega_i t + \varphi_{i0}) = \sqrt{\frac{2 I_i}{m \omega_i}}\cos\varphi_i, \quad i=x,y
$$
## 3.3 
如上，代入 $\varphi_i = \omega_i t + \varphi_{i0}$ 即可。 
## 3.4 
这是一个李萨如图形。 

![zz_figure/Pasted image 20251219170743.png](/img/user/zz_figure/Pasted%20image%2020251219170743.png)

# 4 变长单摆    
$$
E = \frac{1}{2} ml^2\dot{\theta}^2 - mgl\cos\theta \sim  \frac{1}{2} ml^2\dot{\theta}^2 + \frac{1}{2} mgl{\theta}^2 
= \frac{p_\theta^2}{2ml^2} + \frac{1}{2} mgl\theta^2
$$
作用量  
$$
J = \frac{1}{2\pi} \oint p_\theta \, \mathrm{d}\theta = \frac{1}{2\pi} \cdot \pi \sqrt{2ml^2E \cdot \frac{2}{mgl}E}
= {E}\sqrt{\frac{l}{g}}
$$
得到  
$$
E\sqrt{l} \equiv J \sqrt{g}
$$
为绝热/浸渐不变量。

# 附录%  
来处理这个丑陋的积分
$$
J_\rho = \frac{1}{2\pi} \oint p_\rho \mathrm{d}\rho = \frac{1}{2\pi} \oint \sqrt{2mE_\rho - \frac{J_\theta^2}{\rho^2} - m^2\omega^2\rho^2} ~\mathrm{d}\rho
$$
令 $u = \rho^2$，$\mathrm{d}\rho = \frac{\mathrm{d}u}{2\sqrt{u}}$：
$$
\begin{align}
J_\rho &= \frac{1}{2\pi} \oint \sqrt{2mE_\rho - \frac{J_\theta^2}{u} - m^2\omega^2 u} ~ \frac{\mathrm{d}u}{2\sqrt{u}} \\[4pt]
&= \frac{1}{4\pi} \int_{u_1}^{u_2} \frac{\sqrt{-m^2\omega^2 u^2 + 2mE_\rho u - J_\theta^2}}{u} ~\mathrm{d}u
\end{align}
$$
设被积函数为 $f(u) = \frac{\sqrt{R(u)}}{u}$，$R(u) = -m^2\omega^2 u^2 + 2mE_\rho u - J_\theta^2$，上式中 $u_{1,2}$ 是 $R(u)=0$ 的两个正实根，因此积分路径是复平面上包裹 $u_{1,2}$ 连线 (即割线) 的闭合曲线。根据留数定理，包裹割线的回路积分等于包裹复平面上除割线以外所有奇点（原点 $u=0$ 和无穷远点 $u=\infty$）留数之和的负值：
$$
J_\rho = \frac{1}{4\pi} \cdot (-2\pi i) \left[ \text{Res}(f, 0) + \text{Res}(f, \infty) \right] = -\frac{i}{2} \left[ \text{Res}(f, 0) + \text{Res}(f, \infty) \right]
$$
在 $u \to 0$ 附近，展开 $\sqrt{R(u)}$：
$$
\sqrt{R(u)} = \sqrt{-J_\phi^2 + 2mE_\rho u - m^2\omega^2 u^2} = \sqrt{-J_\phi^2} \sqrt{1 - \left(\frac{2mE_\rho}{J_\theta^2}u + O(u^2)\right)}
$$
为保证积分路径的相位正常，需要改写根号为  
$$
\sqrt{R(u)} = e^\frac{{\phi_1+\phi_2}}{2} \sqrt{-J_\theta^2 + 2mE_\rho u - m^2\omega^2 u^2} ,\quad \phi_i = arg(u-u_i)
$$
当积分路径为正常地沿实轴 $u_1 \to u_2$ 积分时，相位 $\frac{{\phi_1+\phi_2}}{2}=\frac{{-\pi+\pi}}{2}=0$。注意这里不能选用根号的另一个分支 $\frac {{\phi_1+\phi_2}} {2}+\pi$，这会令积分得到的 $J_\rho<0$，不符合物理意义，因为 $J_\rho = \frac{1}{2\pi} \oint p_\rho \mathrm{d}\rho$ 为相空间中闭合轨迹的面积，须大于 0。 

采用留数和上述积分围道时，在 $u \to 0$ 附近得到
$$
f(u) = \frac{|J_\theta|}{u} \left( 1 - \frac{mE_\rho}{J_\theta^2}u +O(u^2) \right) e^\frac{{\phi_1+\phi_2 + \pi}}{2}
$$
此时 $\phi_i=arg(0-u_i)=\pi$，即 $e^\frac{{\phi_1+\phi_2 + \pi}}{2}=-i$，因此，
$$
\text{Res}(f, 0) = - i|J_\theta|
$$
在 $u \to \infty$ 附近：
$$
\begin{align} 
\sqrt{R(u)} 
&= \sqrt{-m^2\omega^2 u^2 \left( 1 - \frac{2mE_\rho}{m^2\omega^2 u} + \frac{J_\theta^2}{m^2\omega^2 u^2} \right)}  \\[6pt]
&= m\omega u \left( 1 - \frac{2E_\rho}{m\omega^2 u} + O\left( \frac{1}{u^2} \right)\right)^{1/2}  e^\frac{{\phi_1+\phi_2 + \pi}}{2} 
\end{align}
$$

此时  
$$
\begin{align} 
f\left( \frac{1}{u} \right) = {u}{\sqrt{R\left( \frac{1}{u} \right)}} 
&\approx m\omega \left( 1 - \frac{2E_\rho}{m\omega^2 } u + O\left( u^2 \right)\right)^{1/2}  {\color {red}e^\frac{{\phi_1+\phi_2 + \pi}}{2} }
\\[4pt]
&\approx
{\color{red}{-i}}m\omega  \left( 1 + \frac{E_\rho u}{m\omega^2 } \right)
\end{align}
$$
于是
$$
\text{Res}(f(u), \infty) = -\text{Res}\left( \frac{f\left( \frac{1}{u} \right)}{u^2}, 0 \right) = \frac{iE_\rho}{\omega}
$$
将两个留数代回 $J_\rho$ 的公式：
$$
\begin{align} 
J_\rho = -\frac{i}{2} \left( - i|J_\theta| + \frac{iE_\rho}{\omega} \right)
= - \frac{1}{2}|J_\theta| + \frac{E_\rho}{2\omega}
\end{align}
$$
这就是积分的最终结果。你也可以尝试用实积分求解，会得到相同的答案。

