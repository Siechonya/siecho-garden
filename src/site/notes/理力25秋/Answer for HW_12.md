---
{"dg-publish":true,"permalink":"/理力25秋/Answer for HW_12/","noteIcon":"default","created":"2025-12-12T14:48:02.868+08:00","updated":"2025-12-25T10:09:53.689+08:00"}
---

# 1 三维各向同性谐振子：球坐标  
已知基本关系：  
$$
L=\frac{m}{2}\left(\dot{r}^{2}+r^{2} \dot{\theta}^{2}+r^{2} \dot{\varphi}^{2} \sin ^{2} \theta\right)-V(r, \theta, \varphi)
,\quad V(r) = \frac{1}{2}kr^2
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
\frac{1}{2 m}\left(\frac{\partial S_{0}}{\partial r}\right)^{2}+\frac{1}{2}kr^2+\frac{1}{2 m r^{2}}\left(\frac{\partial S_{0}}{\partial \theta}\right)^{2}+\frac{1}{2 m r^{2} \sin ^{2} \theta}\left(\frac{\partial S_{0}}{\partial \varphi}\right)^{2}=E 
$$
$\varphi$ 是循环坐标，所以记  $\frac{\partial S_{0}}{\partial \varphi}$  为一常数 $p_{\varphi}$，分离变量得到  
$$
\left(\frac{\partial S_{0}}{\partial \theta}\right)^{2}+\frac{p_{\varphi}^{2}}{\sin ^{2} \theta}=2 m r^{2}\left\{E-\frac{1}{2 m}\left(\frac{\partial S_{0}}{\partial r}\right)^{2}-\frac{1}{2}kr^2\right\}
$$
可以令 $S_{0}=p_{\varphi} \varphi+S_{1}(r)+S_{2}(\theta)$ ，代入上式，有
$$
\left(\frac{\mathrm{d} S_{2}}{\mathrm{~d} \theta}\right)^{2}+\frac{p_{\varphi}^{2}}{\sin ^{2} \theta}=2 m r^{2}\left\{E-\frac{1}{2 m}\left(\frac{\mathrm{~d} S_{1}}{\mathrm{~d} r}\right)^{2}-\frac{1}{2}kr^2\right\} 
$$
上式两边分别为 $\theta$ 和 $r$ 的函数，于是有
$$
\left(\frac{\mathrm{d} S_{2}}{\mathrm{~d} \theta}\right)^{2}+\frac{p_{\varphi}^{2}}{\sin ^{2} \theta}=\beta
$$
$$
\frac{1}{2 m}\left(\frac{\mathrm{~d} S_{1}}{d r}\right)^{2}+\frac{1}{2}kr^2+\frac{\beta}{2 m r^{2}}=E
$$
由以上两式可得
$$
\begin{align}
&S_{1}=\int \sqrt{2 m\left[E-\frac{1}{2}kr^2-\frac{\beta}{2 m r^{2}}\right]} \mathrm{d} r \\[6pt]
&S_{2}=\int \sqrt{\beta-\frac{p_{\varphi}^{2}}{\sin ^{2} \theta}} \mathrm{~d} \theta 
\end{align}
$$
$$
\Rightarrow \quad
S=-Et + p_{\varphi} \varphi+  \int \sqrt{2 m\left[E-\frac{1}{2}kr^2-\frac{\beta}{2 m r^{2}}\right]} \mathrm{d} r +
\int \sqrt{\beta-\frac{p_{\varphi}^{2}}{\sin ^{2} \theta}} \mathrm{~d} \theta 
$$
于是可以给出三个新的运动积分  
$$
\xi = -t + \frac{ \partial S_0 }{ \partial E } 
= -t + \int \cdots
\quad\Longrightarrow \quad
r=r(t)
$$
$$
Q_{\beta} =  \frac{ \partial S_0 }{ \partial \beta } 
= \int \cdots
\quad\Longrightarrow \quad
f(r(t),\theta)=0 
\quad\Longrightarrow \quad
\theta(t)
$$
$$
Q_{\varphi}  = \frac{ \partial S_0 }{ \partial p_\varphi } 
= \int \cdots
\quad\Longrightarrow \quad
g(\varphi,\theta(t)) = 0
\quad\Longrightarrow \quad
\varphi(t)
$$
三个坐标对时间的依赖关系都在以上三个积分表达式当中。特别的，如果选取 $\theta\equiv\frac{\pi}{2}$，上述结果会退化在 x-y 平面上的椭圆的极坐标形式，并且坐标原点位于椭圆正中心。
# 2 三维各向同性谐振子：笛卡尔坐标  
类似地，已知基本关系：  
$$
L=\frac{m}{2}\left(\dot{x}^{2}+\dot{y}^{2}+ \dot{z}^{2} \right)- \frac{1}{2}kr^2
$$
$$
\vec{p}= \frac{ \partial L }{ \partial \dot{\vec{r}} } = m\dot{\vec{r}} 
$$
$$
H = \frac{p^2}{2m} + \frac{1}{2}kr^2
$$
于是 $H-J$ 方程为  
$$
\frac{1}{2m}\left[\left(\frac{\partial S_0}{\partial x}\right)^2 + \left(\frac{\partial S_0}{\partial y}\right)^2 + \left(\frac{\partial S_0}{\partial z}\right)^2\right] + \frac{1}{2}k(x^2 + y^2 + z^2) = E
$$
可以令 $S_{0}=S_x(x)+S_y(y) + S_z(z)$ ，代入上式，有
$$
\left[\frac{1}{2m}\left(\frac{dS_x}{dx}\right)^2 + \frac{1}{2}kx^2\right] + \left[\frac{1}{2m}\left(\frac{dS_y}{dy}\right)^2 + \frac{1}{2}ky^2\right] + \left[\frac{1}{2m}\left(\frac{dS_z}{dz}\right)^2 + \frac{1}{2}kz^2\right] = E
$$
于是有  
$$
\left[\frac{1}{2m}\left(\frac{dS_i}{dx_i}\right)^2 + \frac{1}{2}kx_i^2\right] = E_i, \quad i = x,y,z
$$
积分得到  
$$
S_i(x_i) = \int  \sqrt{2m E_i - mkx_i^2} \, \mathrm{d}x_i
$$
选取 $E_x,E_y,E_z$ 作为独立运动积分得到
$$
S =-Et +S_0 =  -(E_x + E_y +E_z)t + \int  \sqrt{2m E_x - mkx^2} \, \mathrm{d}x + \int  \sqrt{2m E_y - mky^2} \, \mathrm{d}y + \int  \sqrt{2m E_z - mkz^2} \, \mathrm{d}z
$$
新的广义坐标(假设 $\omega = \sqrt{k/m},A_i^2 = \frac{2E_i}{m\omega^2}$)：  
$$
\begin{align} 
Q_x 
= \frac{ \partial S }{ \partial E_x } 
&= -t + \int \frac{m}{\sqrt{2m E_x - mkx^2}} \, \mathrm{d}x 
\\[6pt]
&= -t + \int \frac{1}{\sqrt{2 E_x/m - \omega^2 x^2}} \, \mathrm{d}x 
\\[6pt]
&=
-t+\frac{1}{\omega} \arcsin\left(\frac{x}{A_x}\right) 
\end{align}
$$
得到简谐振动方程  
$$
x = A_x\sin(\omega t + Q_x) = \sqrt{\frac{2E_x}{m\omega^2}}\sin (\omega t + Q_x ) = \sqrt{\frac{2E_x}{k}}\sin (\sqrt{k/m} t + Q_x )
$$
另外两个方向同理。如果你选取 $E$ 作为其中一个独立运动积分，比如 $E_x,E_y,E$，将会让计算变得复杂，但是结论是一致的，这种选择会给出：  
$$
\begin{align} 
&Q_x = \frac{ \partial S_0 }{ \partial E_x }
= \int \frac{m}{\sqrt{2m E_x - mkx^2}} \, \mathrm{d}x - \int \frac{m}{\sqrt{2m (E-E_x-E_y) - mkz^2}} \, \mathrm{d}z
\\[6pt]
&\qquad\qquad\quad=\frac{1}{\omega} \arcsin\left(\frac{x}{A_x}\right) - \frac{1}{\omega} \arcsin\left(\frac{z}{A_z}\right)
\\[20pt]
&Q_y = \frac{ \partial S_0 }{ \partial E_y }
=\frac{1}{\omega} \arcsin\left(\frac{y}{A_y}\right) - \frac{1}{\omega} \arcsin\left(\frac{z}{A_z}\right)
\\[20pt]
&Q_E = -t + \frac{ \partial S_0 }{ \partial E } 
= -t + \int \frac{m}{\sqrt{2m E_z - mkz^2}} \, \mathrm{d}z \\[6pt]
&\qquad\qquad\qquad\quad~= -t+\frac{1}{\omega} \arcsin\left(\frac{x}{A_x}\right)
\end{align}
$$

