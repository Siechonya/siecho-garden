---
{"dg-publish":true,"permalink":"/理力25秋/Answer for HW3/","noteIcon":"default","created":"2025-12-01T13:33:13.707+08:00","updated":"2025-11-01T11:57:00.765+08:00"}
---

# 1 引力透镜  
定义光程泛函 $\mathcal{S}$ 为：  
$$
\mathcal{S} = \int_{A}^{B} n(\mathbf{r}) \, \mathrm{d}s 
$$
其中 A、B 是光的起点和终点，费马原理指的是，所有连接 A、B 的可能曲线中，只有满足光程的变分为零才是光线走的路径，即：   
$$  
\delta \mathcal{S} = \delta \int_{A}^{B} n(\mathbf{r}) \, \mathrm{d}s = 0   
$$
- <font color="#ff0000">方法一</font>

在本题中，折射率是球对称的，光线始终在一个平面传播，可以采取极坐标：  
$$
\mathcal{S }= \int_{-\infty}^{+\infty} \left( 1 + \frac{\alpha}{r}  \right)\sqrt{1+r^2 \dot\theta^2} \ \mathrm{d}r, \quad \alpha = \frac{GM_\odot}{c^2}\ll 1,~ \dot \theta = \frac{ \mathrm{d} \theta }{ \mathrm{d} r}
$$
$$
L = \left( 1 + \frac{\alpha}{r}  \right)\sqrt{1+r^2 \dot\theta^2}
$$
代入拉格朗日方程 $\frac{ \mathrm{d}  }{ \mathrm{d} r}\left( \frac{ \partial L }{ \partial \dot \theta } \right) - \frac{ \partial L }{ \partial \theta }=0$ 得到：  
$$
\frac{ \partial L }{ \partial \dot \theta } = const. = \left( 1 + \frac{\alpha}{r}  \right) \cdot (1+r^2 \dot\theta^2)^{-1/2} \cdot r^2\dot \theta
$$
这是一个光学守恒量，记为 J，$J = n(r) \cdot \frac{ \mathrm{d} r }{ \mathrm{d} s} \cdot r^2 \frac{ \mathrm{d} \theta }{ \mathrm{d} r} = nr^2\frac{ \mathrm{d} \theta }{ \mathrm{d} s}$，称为光学角动量。在无穷远处，$J = nr^2\frac{ \mathrm{d} \theta }{ \mathrm{d} s}  = n_\infty R_\odot \approx R_\odot =  const.$ ，因为光线始终在一个平面传播，所以弧长微分满足：  
$$
ds^2 = dr^2 + r^2 d\theta^2
\quad\Rightarrow\quad
\left( \frac{dr}{ds} \right)^2 + r^2 \left( \frac{d\theta}{ds} \right)^2 = 1
$$
代入 $n r^2 \frac{d\theta}{ds} = R_\odot$ 得到: 
$$
\left( \frac{dr}{ds} \right)^2 = 1 - \frac{R_\odot^2}{n^2 r^2}
$$
计算光线从无穷远来到近日点 $R_\odot$，再回到无穷远的总角度变化 $\Delta \theta$ ，有：
$$
\Delta \theta = 2 \int_{R_\odot}^{\infty} \frac{d\theta}{dr} dr
$$
由 $\frac{d\theta}{dr} = \frac{d\theta}{ds} / \frac{dr}{ds} = \frac{R_\odot}{n r^2} / \sqrt{1 - \frac{R_\odot^2}{n^2 r^2}}$ ，可得：   
$$
\boxed{
\Delta \theta = 2 \int_{R_\odot}^{\infty} \frac{R_\odot}{n r^2} \frac{1}{\sqrt{1 - \frac{R_\odot^2}{n^2 r^2}}} \mathrm{d}r
}
$$
使用变量代换 $u = 1/r$，则 $dr = -du/u^2$，于是：  
$$
\Delta \theta= 2\int_{\frac{1}{R_\odot}}^{0} \mathrm{d}\theta = 2\int_{0}^{ \frac{1}{R_\odot}} \frac{R_\odot}{n} \frac{\mathrm{d}u}{\sqrt{1 - \frac{R_\odot^2 u^2}{n^2}}}
$$
代入 $n = 1 + \alpha u, ~ \alpha = \frac{GM_\odot}{c^2}\ll 1$，化为：  
$$
\begin{aligned} 
\Delta\theta
&= 2\int_{0}^{1/R_\odot} \frac{R_\odot \mathrm{d}u}{\sqrt{(1+\alpha u)^2 - R_\odot^2 u^2}}
\\&\approx
2\int_{0}^{1/R_\odot} \frac{R_\odot \mathrm{d}u}{\sqrt{1 + 2\alpha u - R_\odot^2 u^2}}
\\&= 2 \int_{0}^{1/R_\odot} \frac{R_\odot \mathrm{d}u}{\sqrt{1 + \frac{\alpha^2}{R_\odot^2} - R_\odot^2 \left( u - \frac{\alpha}{R_\odot^2} \right)^2}}
\\&\approx
2 \int_{0}^{1/R_\odot} \frac{R_\odot \mathrm{d}u}{\sqrt{1 - R_\odot^2 \left( u - \frac{\alpha}{R_\odot^2} \right)^2}}
\\&\approx
2 \int_{-\frac{\alpha}{R_\odot}}^{1} \frac{\mathrm{d}v}{\sqrt{1 - v^2}}
\\&=
2\arcsin v \Big|_{-\alpha/b}^{1} = \pi + 2\arcsin\left(\frac{\alpha}{R_\odot}\right) \approx  \pi + 2\frac{\alpha}{R_\odot}
\end{aligned}
$$
注意，最终的偏折角是 $\delta \theta = \Delta \theta - \pi$ ，减去 $\pi$ 是因为在没有引力时，偏折角是 $\pi$ 而不是 0。所以偏折角：
$$
\delta \theta = \Delta \theta - \pi = \frac{2\alpha}{R_\odot} = \frac{2 GM}{c^2 R_\odot} \approx 4.24 \times 10^{-6} \, \text{rad}  \approx 0.87''
$$

- <font color="#ff0000">方法二</font>

法二从三维情形出发，这只是为了展示光线传播方程。将弧长微分 ds 改写为： 
$$
ds = \sqrt{\left( \frac{dx}{ds} \right)^2 + \left( \frac{dy}{ds} \right)^2 + \left( \frac{dz}{ds} \right)^2} \mathrm{d}s 
= \sqrt{ \frac{ \mathrm{d} \mathbf{ r} }{ \mathrm{d} s} \cdot \frac{ \mathrm{d} \mathbf{ r} }{ \mathrm{d} s}} \, \mathrm{d}s
$$
显然 $\sqrt{ \frac{ \mathrm{d} \mathbf{ r} }{ \mathrm{d} s} \cdot \frac{ \mathrm{d} \mathbf{ r} }{ \mathrm{d} s}}$ 等于 1，但是不妨碍我们把 $\frac{ \mathrm{d} \mathbf{ r} }{ \mathrm{d} s}$ 凑成一个参数。于是光程可表示： 
$$   
\mathcal{S} = \int_{t_A}^{t_B}  L(\mathbf{r}, \frac{ \mathrm{d} \mathbf{ r} }{ \mathrm{d} s} , s) \, \mathrm{d}s ,  \quad 
L(\mathbf{r}, \frac{ \mathrm{d} \mathbf{ r} }{ \mathrm{d} s}, s) 
= n(\mathbf{r}) \cdot \sqrt{ \frac{ \mathrm{d} \mathbf{ r} }{ \mathrm{d} s} \cdot \frac{ \mathrm{d} \mathbf{ r} }{ \mathrm{d} s}} 
$$
代入 Euler-Lagrange 方程 $\color{red}\frac{d}{ds} \left( \frac{\partial L}{\partial \frac{ \mathrm{d} \mathbf{ r} }{ \mathrm{d} s}} \right) = \frac{\partial L}{\partial \mathbf{r}}$，可以得到
$$
\frac{ \mathrm{d}  }{ \mathrm{d} s} 
\left[  n(r) {\frac{\frac{ \mathrm{d} \mathbf{ r} }{ \mathrm{d} s}}{\sqrt{\frac{ \mathrm{d} \mathbf{ r} }{ \mathrm{d} s} \cdot \frac{ \mathrm{d} \mathbf{ r} }{ \mathrm{d} s}}}}
\right]
= \frac{ \partial n(\mathbf{ r}) }{ \partial \mathbf{ r} }
$$
也就是光线传播方程：  
$$
\boxed{
\frac{\mathrm{d}}{\mathrm{d}s} \left( n(\mathbf{r}) \cdot \frac{\mathrm{d} \mathbf{r}}{\mathrm{d} s} \right) = \nabla n 
}
$$
在本题中，折射率是球对称的，光线始终在一个平面传播，入射光线在无穷远处，瞄准半径为 $R_\odot$。此时 $\nabla n$ 只有径向分量（因为球对称，折射率只有径向梯度），于是  
$$
\begin{aligned}
\frac{\mathrm{d}}{\mathrm{d}s} \left( n(\mathbf{r}) \cdot \frac{\mathrm{d} \mathbf{r}}{\mathrm{d} s} \right)_\theta &= 0\\
& \Rightarrow\quad
\frac{ \mathrm{d} n }{ \mathrm{d} s}\frac{\mathrm{d} \mathbf{r}}{\mathrm{d} s}{\Huge|}_\theta + n \frac{ \mathrm{d}^2 \mathbf{ r} }{ \mathrm{d}^2 s}{\Huge|}_\theta= 0\\
& \Rightarrow\quad
\frac{ \mathrm{d} n }{ \mathrm{d} s} \cdot r\frac{ \mathrm{d} \theta }{ \mathrm{d} s} + n\left( r\frac{ \mathrm{d}^2 \theta }{ \mathrm{d}^2 s} + 2 \frac{ \mathrm{d} r }{ \mathrm{d} s}\frac{ \mathrm{d} \theta }{ \mathrm{d} s} \right)
= 0\\
&\overset{\times r}\Rightarrow\quad
\frac{ \mathrm{d}   }{ \mathrm{d} s}\left( nr^2\frac{ \mathrm{d} \theta }{ \mathrm{d} s} \right) = 0 \\
&\Rightarrow\quad
nr^2\frac{ \mathrm{d} \theta }{ \mathrm{d} s}  = n_\infty R_\odot \approx R_\odot =  const.
\end{aligned}
$$
这是光学角动量（守恒），剩余的步骤和法一一致。
# 2 最小回转面  
曲线绕 x 轴旋转的表面积为
$$
S=2 \pi \int_{0}^{x_{1}} y d s=2 \pi \int_{0}^{x_{1}} y \sqrt{1+y^{\prime 2}} d x,\quad L = y \sqrt{1+y^{\prime 2}}
$$
代入 Euler-Lagrange 方程 $\frac{d}{dx} \left( \frac{\partial L}{\partial y' } \right) = \frac{\partial L}{\partial y}$ 并化简得到：
$$
yy' = 1+y'^2
$$
这正是悬链线方程，解为 $y = a \cosh \frac{x - b}{a}$。
# 3 修正最速降  
设 v 是沿着这条曲线的速率，则降落一段弧长 $\mathrm{d} s$ 所需的时间为 $\mathrm{d} s / v$ ，其中
$$
\mathrm{d} s=\sqrt{\mathrm{d} x^{2}+\mathrm{d} y^{2}}, \quad v=\sqrt{v_{0}^{2}+2 g y}
$$
运动所需时间为
$$
t_{12}=
\int_{1}^{2} \frac{\mathrm{d}s}{v}
=
\int_{1}^{2} \frac{\sqrt{1+\dot{x}^{2}}}{\sqrt{2 g y+v_{0}^{2}}} \mathrm{~d} y
$$
令 $f=\frac{\sqrt{1+\dot{x}^{2}}}{\sqrt{2 g y+v_{0}^{2}}}$，则 $\frac{\partial f}{\partial \dot{x}}=\frac{\dot{x}}{\sqrt{2 g y+v_{0}^{2}} \sqrt{1+\dot{x}^{2}}}$，$\frac{\partial f}{\partial x}=0$，代入 Euler-Lagrange 方程中得到
$$
\frac{\partial f}{\partial \dot{x}}=\frac{\dot{x}}{\sqrt{2 g y+v_{0}^{2}} \sqrt{1+\dot{x}^{2}}}=\left(2 g c_{1}\right)^{-1 / 2}
\quad\to\quad
\dot{x}=\frac{\mathrm{d} x}{\mathrm{~d} y}=\sqrt{\frac{y+v_{0}^{2} / 2 g}{c_{1}-y-v_{0}^{2} / 2 g}}
$$
这和课本(秦敢那本)第 20 页方程(16)差一个平移，令  $y+v_{0}^{2} / 2 g=c_{1} \sin ^{2} \theta$  ，则最终可得最速落径的参数方程
$$
\left\{\begin{array}{l}
x=c_{1}\left(\theta-\frac{1}{2} \sin 2 \theta\right)+c_{2} \\
y+{\color{red}v_{0}^{2} / 2 g}=c_{1} \sin ^{2} \theta
\end{array}\right.
$$
其尖端点的高度要高出 $\frac{v_0^2}{2g}$。
# 4 圆滚线  
## 4.1 （a）  
选取参量如下图所示
![zz_figure/Pasted image 20250926185631.png](/img/user/zz_figure/Pasted%20image%2020250926185631.png)
那么拉格朗日量可以写作：  
$$
L = T - V = \frac{1}{2}m {\dot x}^2 - \frac{1}{2} \frac{g}{R} (x^2 + d^2)
$$
代入拉格朗日方程得到：  
$$
\ddot x + \frac{g}{R} x = 0
$$
正是简谐振动方程，$t_0 = \pi \sqrt{\frac{R}{g}}$。  
## 4.2 （b）  
还是先把所费的时间写成泛函形式：  
$$
t = \int \frac{\mathrm{d}s}{v} = \int \frac{\sqrt{1+r^2 \left( \frac{ \mathrm{d} \theta }{ \mathrm{d} r} \right)^2}~\mathrm{d}r} {\sqrt{\frac{2g}{R}(R^2 - r^2)}}
$$
第二个等号用到了单位质量物体的能量守恒 $\frac{1}{2}v^2 + \frac{g}{2R}r^2 = 0+\frac{g}{2 R}R^2$。于是拉氏量：  
$$
L = \sqrt{\frac{{1+r^2 \left( \frac{ \mathrm{d} \theta }{ \mathrm{d} r} \right)^2}}{R^2 - r^2}}
$$
代入拉格朗日-欧拉方程 $\frac{ \mathrm{d}   }{ \mathrm{d} r}\left( \frac{ \partial L }{ \partial \frac{ \mathrm{d} \theta }{ \mathrm{d} r} }\right) - \frac{ \mathrm{d} L }{ \mathrm{d} \theta} =0$ 得到：  
$$
\frac{r^2}{\sqrt{(R^2-r^2)(r'^2(\theta)+r^2)}} = \frac{r_0}{\sqrt{R^2 - r_0^2}} =  const. ，\quad r_0 = r|_{\theta=0}
$$
积分得到(2)式。取 $\Delta \theta = 2 \cdot \theta|_{r=R^-}$ 得到(3)式。  
## 4.3 （c）  
把（4）代入（2）就得到（6），反解（4）得到（5）。接下来看为什么（5）和（6）描述圆内滚轮线（现在变成了纯几何问题）。首先命名参量如下图：  
![zz_figure/Pasted image 20251011152228.png](/img/user/zz_figure/Pasted%20image%2020251011152228.png)
根据几何关系，有：  
$$
r^2
= (R-a)^2 + a^2 - 2(R-a)a\cos\phi \overset{a=\frac{1}{2}(R-r_0)}
= \frac{1}{2}(R^2 +r^2_0) - \frac{1}{2}(R^2 - r^2_0)\cos\phi
$$
注意图中 $\phi = \pi - \varphi$ 。以及再根据几何关系：   
$$
\begin{aligned} 
a\phi &= R\alpha \\
\frac{a}{\sin( \theta - \alpha)} &= \frac{{R-a}}{\sin(\varphi - (\theta-\alpha))} = \frac{{R-a}}{\sin(\phi +(\theta-\alpha))}
\end{aligned}
\quad\Rightarrow\quad
\frac{{R-r_0}}{\sin \left( \theta - \left( \frac{1}{2}-\frac{r_0}{2R} \right)\phi \right)} = \frac{{R+r_0}}{\sin \left(  \left( \frac{1}{2}+\frac{r_0}{2R} \right)\phi + \theta \right)}
$$
$$
\Rightarrow\quad \tan\theta = {\frac{{\frac{R}{r_0}\tan \frac{\phi}{2}-\tan \frac{r_0}{2R}\phi}}{1 +{\frac{R}{r_0}\tan \frac{\phi}{2}\tan \frac{r_0}{2R}\phi}}}
$$
$$
\Rightarrow\quad
\tan\left( \theta+\frac{r_0}{2R}\phi \right) = \frac{R}{r_0}\tan  \frac{\phi}{2}
$$
即（6）式。  

## 4.4 （d）  
由（5）可得：  
$$
\frac{{R^2-r^2}}{r^2} = \frac{{2(R^2 - r_0^2)\cos^2\phi}}{(R^2 +r^2_0) - (R^2 - r^2_0)\cos\phi}
\tag{4.1}
$$
由（6）可得：  
$$
\frac{ \mathrm{d} \theta }{ \mathrm{d} \phi} = \frac{r_0}{2R} \frac{{(R^2 - r_0^2)\cos^2 \frac{\phi}{2}}}{R^2\sin^2 \frac{\phi}{2} + r_0^2\cos^2 \frac{\phi}{2}}
\tag{4.2}
$$
根据 $v^2dt^2 = dr^2 + r^2 d\theta^2$：   
$$
\frac{v^2}{\dot \theta^2} = (\frac{ \mathrm{d} r }{ \mathrm{d} \theta})^2 + r^2
$$
上式联立单位质量物体的能量守恒 $v^2= \frac{g}{R}(R^2-r^2)$ 得到  
$$
\frac{ \mathrm{d} \theta }{ \mathrm{d} t} = \sqrt{\frac{{\frac{g}{R}(R^2-r^2)}}{(\frac{ \mathrm{d} r }{ \mathrm{d} \theta})^2 + r^2}}
$$
将（1）代入上式得到  
$$
\frac{ \mathrm{d} \theta }{ \mathrm{d} t} 
= 
\sqrt{\frac{g}{R}} \frac{{R^2-r^2}}{r^2} \frac{r_0}{\sqrt{R^2 - r_0^2}}
$$
将本小题一开始得到的（4.1）代入上式，并用（4.2）将 $\theta$ 替换为 $\phi$，得到：  
$$
\phi = \sqrt{\frac{g}{R}} \cdot \frac{\sqrt{R^2-r_0^2}}{2R} \cdot t = 2\pi \frac{ t}{\tau}
$$
合肥到北京的纬度差 $\theta \approx 8^\circ$，让滚轮转一圈那么 $R \cdot 8^\circ = 2\pi \cdot \frac{1}{2}(R-r_0)$ 得到 $\frac{r_0}{R} = 0.956R$，于是  
$$
\frac{\tau}{\tau_0} = \sqrt{1-0.956^2} \approx 0.29
$$
# 5 测地线  
## 5.1 （a）  
平面内的线元 $\mathrm{d} s=\left(\mathrm{d} x^{2}+\mathrm{d} y^{2}\right)^{\frac{1}{2}}=\sqrt{1+\dot{y}^{2}} \mathrm{~d} x,~ \dot y = \frac{ \mathrm{d} y }{ \mathrm{d} x}$，则 $s=\int_{1}^{2} \sqrt{1+\dot{y}^{2}} \mathrm{~d} x$，对其求极值。令 $f=\sqrt{1+\dot{y}^{2}}$，则
$$
\frac{\partial f}{\partial \dot{y}}=\frac{\dot{y}}{\sqrt{1+\dot{y}^{2}}}, \quad \frac{\partial f}{\partial y}=0
$$
代入欧拉方程 $\frac{\mathrm{d}}{\mathrm{d} x}\left(\frac{\partial f}{\partial \dot{y}}\right)-\frac{\partial f}{\partial y}=0$ 中，即 $\frac{\partial f}{\partial \dot{y}}=\frac{\dot{y}}{\sqrt{1+\dot{y}^{2}}}=  const.$，所以
$$
\dot{y}=C_{1}, \quad y=C_{1} x+C_{2}
$$
正是直线。
## 5.2 （b）
柱面的线元
$$
\mathrm{d} s=\left(R^{2} \mathrm{~d} \theta^{2}+\mathrm{d} z^{2}\right)^{\frac{1}{2}}=\sqrt{\dot{z}^{2}+R^{2}} \mathrm{~d} \theta,~
\dot z = \frac{ \mathrm{d} z }{ \mathrm{d} \theta}
$$
则 $s=\int_{1}^{2} \sqrt{\dot{z}^{2}+R^{2}} \mathrm{~d} \theta$，对其求极值．令 $f=\sqrt{\dot{z}^{2}+R^{2}}$，则
$$
\frac{\partial f}{\partial \dot{z}}=\frac{\dot{z}}{\sqrt{\dot{z}^{2}+R^{2}}}, \quad \frac{\partial f}{\partial z}=0
$$
代入欧拉方程 $\frac{\mathrm{d}}{\mathrm{d} x}\left(\frac{\partial f}{\partial \dot{z}}\right)-\frac{\partial f}{\partial z}=0$ 中，即 $\frac{\partial f}{\partial \dot{z}}=\frac{\dot{z}}{\sqrt{\dot{z}^{2}+R^{2}}}=  const.$，所以
$$
\dot{z}=C_{1}, \quad z=C_{1} \theta+C_{2}
$$
即螺旋线。  
## 5.3 （c）  
在每个点的邻域里，两者都是欧氏空间，即局部欧氏空间。
# 6 GR测地线  
## 6.1 （a）  
（10）式给出我们需要的拉氏量：  
$$
L = \frac{1}{2} g_{\mu\nu} \dot x^\mu \dot x^\nu,\quad \dot x ~表示~ \frac{ \mathrm{d} x }{ \mathrm{d} s}
$$
代入拉格朗日方程 $\frac{d}{ds}\left( \frac{\partial L}{\partial \dot{x}^\rho} \right) - \frac{\partial L}{\partial x^\rho} = 0$，利用 $g_{\mu\nu} = g_{\nu\mu}$，注意度规是坐标 $x^\lambda$ 的函数，有
$$
\frac{\partial L}{\partial \dot{x}^\rho} = \frac{1}{2} \left( g_{\rho\nu} \dot{x}^\nu + g_{\mu\rho} \dot{x}^\mu \right) = g_{\rho\mu} \dot{x}^\mu 
$$
$$
\to\quad \frac{ \mathrm{d}   }{ \mathrm{d} s} \frac{\partial L}{\partial \dot{x}^\rho} =
\frac{d}{ds}\left( g_{\rho\mu} \dot{x}^\mu \right) = g_{\rho\mu} \ddot{x}^\mu + \frac{\partial g_{\rho\mu}}{\partial x^\sigma} \dot{x}^\sigma \dot{x}^\mu
$$
以及  
$$
\frac{\partial L}{\partial x^\rho} = \frac{1}{2} \frac{\partial g_{\mu\nu}}{\partial x^\rho} \dot{x}^\mu \dot{x}^\nu
$$
代入拉格朗日方程得到：  
$$
\begin{aligned} 
g_{\rho\mu} \ddot{x}^\mu 
&= -\left[ \frac{\partial g_{\rho\mu}}{\partial x^\sigma} \dot{x}^\sigma \dot{x}^\mu - \frac{1}{2} \frac{\partial g_{\mu\nu}}{\partial x^\rho} \dot{x}^\mu \dot{x}^\nu \right] \\
&=
-\frac{1}{2}\left[ \frac{\partial g_{\rho\mu}}{\partial x^\sigma} \dot{x}^\sigma \dot{x}^\mu  + \frac{\partial g_{\rho\mu}}{\partial x^\sigma} \dot{x}^\sigma \dot{x}^\mu- \frac{1}{2} \frac{\partial g_{\mu\nu}}{\partial x^\rho} \dot{x}^\mu \dot{x}^\nu \right] \\
&=
-\frac{1}{2} \left[
\frac{\partial g_{\rho\mu}}{\partial x^\nu} \dot{x}^\nu \dot{x}^\mu + \frac{\partial g_{\rho\nu}}{\partial x^\mu} \dot{x}^\mu \dot{x}^\nu
-\frac{\partial g_{\mu\nu}}{\partial x^\rho} \dot{x}^\mu \dot{x}^\nu
\right]
\end{aligned}
$$
在最后一个等号中，使用了指标替换，第一项 $\sigma\to\nu$，第二项 $\mu\to\nu,\sigma\to\mu$，因为都是缩并的指标，所以只是相当于给指标换了个名字。结合克里斯托费尔符号定义：
$$
\Gamma_{\mu, \rho\sigma} \equiv 
\frac{1}{2} \left( \frac{\partial g_{\mu\rho}}{\partial x^\sigma} + \frac{\partial g_{\mu\sigma}}{\partial x^\rho} - \frac{\partial g_{\rho\sigma}}{\partial x^\mu} \right) 
$$
$$
\Rightarrow
2\Gamma_{\rho, \mu\nu} = 
\frac{\partial g_{\rho\mu}}{\partial x^\nu}  + \frac{\partial g_{\rho\nu}}{\partial x^\mu} 
-\frac{\partial g_{\mu\nu}}{\partial x^\rho} 
$$
最终得测地线方程：  
$$
g_{\rho\mu} \frac{d^2 x^\mu}{ds^2} = - \Gamma_{\rho, \mu\nu} \frac{dx^\mu}{ds} \frac{dx^\nu}{ds} 
$$
两边同时乘 $g^{\lambda\rho}$ 可以得到  
$$
\frac{d^2 x^\lambda}{ds^2} + \Gamma_{\mu\nu}^\lambda \frac{dx^\mu}{ds} \frac{dx^\nu}{ds} = 0
$$
## 6.2 （b）  
狭义相对论的闵氏空间中，度规是常数，所以联络为 0，测地线退化成：  
$$
\frac{d^2 x^\lambda}{ds^2} = 0
$$
即：  
$$
\frac{d x^\lambda}{ds} = c_\lambda
$$
即  
$$
t = c_0 s +t_0,\quad \mathbf{r} = \mathbf{ c} s + \mathbf{ r_0}
\quad\to\quad
\mathbf{ r} = \mathbf{ v}(t-t_0) + \mathbf{r_0}
$$
也就是直线。






