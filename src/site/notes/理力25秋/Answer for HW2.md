---
{"dg-publish":true,"permalink":"/理力25秋/Answer for HW2/","noteIcon":"default","created":"2025-12-01T13:32:49.903+08:00","updated":"2025-11-01T11:57:00.759+08:00"}
---


# 1 
- <font color="#ff0000">方法一：最小势能原理</font>

![zz_figure/5d462ccb8e30f1fb6629cbdba906a0a4.jpg](/img/user/zz_figure/5d462ccb8e30f1fb6629cbdba906a0a4.jpg)  
- <font color="#ff0000">方法二：虚功原理</font>

以圆锥顶点为原点，竖直向下为 z 轴正方向，所以弹性圈的半径为 $r = z\tan\alpha$，弹性圈上的质点坐标是：  
$$
\vec r_i = z\hat e_z +z\tan\alpha \hat e_r
$$
由 $\delta \hat e_r = \theta\delta \hat e_\theta$，于是虚位移满足：  
$$
\delta \vec r_i = \delta z \hat{e_z} + \delta z \tan\alpha \hat{e_r} + z\tan\alpha \delta\theta \hat{e_\theta}
$$
拉伸后弹性圈的长度变为 $2\pi z \tan\alpha$，得到弹性圈上的一小段圆心角 $\mathrm{d}\theta$ 的圆弧受到的弹力是：  
$$
T_i = 2T\sin \frac{\mathrm{d}\theta}{2} \approx T\mathrm{d}\theta = k(2\pi z \tan\alpha - l){\mathrm{d}\theta}
$$
得到其受到的主动力(重力+弹性力)是：
$$
\vec F_i =  \frac{\mathrm{d}\theta}{2\pi} m g \hat{e_z} - {\mathrm{d}\theta}\cdot k(2\pi z \tan\alpha - l)\hat{e_r}
$$
根据虚功原理：  
$$
0 = \sum_i \vec F_i \cdot \delta \vec r_i = \mathrm{d}\theta \delta z \left( \frac{mg}{2\pi} - \tan\alpha  k(2\pi z \tan\alpha - l) \right)
$$
$$
\Rightarrow z = \frac{{mg + 2\pi kl \tan\alpha}}{k(2\pi\tan\alpha)^2}
$$
> [!info]
> 两种方法都只适用于系统处于<font color="#ff0000">平衡</font>的情况，在非平衡时，虚功原理进化为达朗贝尔原理，最小势能原理进化为拉格朗日方程。
# 2 
以沿斜面向下为 x 正方向，圆柱转过的角度为 $\theta$，转动惯量为 $I = \frac{1}{2}mR^2$，约束条件 $\dot x = R \dot \theta$，柱心的虚位移是 $\delta x$，圆柱上某个质点的位置分解为质心位置+到质心的位移 $\vec r_i = x\hat e_x +\vec r_i'$：  
$$
\vec F_i = m_i \vec g
$$
$$
\dot {\vec r_i} = \dot x\hat e_x + r_i'\dot\theta\hat e_\theta
\quad\Rightarrow\quad
\ddot {\vec r_i} = \ddot x\hat e_x + r_i'\ddot\theta\hat e_\theta - r_i'\dot\theta^2\hat e'_{r_i}
=R\ddot\theta e_x + r_i'\ddot\theta\hat e_\theta - \vec r_i'\dot\theta^2
$$
$$
\delta \vec r_i = \delta x\hat e_x + r_i' \delta \theta \hat e_\theta 
$$
根据达朗贝尔原理（主动力和惯性力的虚功和为 0）：  
$$
\begin{aligned}
0 &= \sum_i (\vec F_i - m_i \ddot{\vec r_i}) \cdot \delta{\vec r_i} \\
&=
Mg\sin\alpha\delta x - \sum_i  m_i (\ddot x\hat e_x + \ddot{\vec r_i'}) \cdot \delta(x\hat e_x +\vec r_i') \\
&=
Mg\sin\alpha\delta x - M\ddot x \delta x - 0 - 0 - \sum_i  m_i  \ddot{\vec r_i'} \cdot \delta\vec r_i'
\end{aligned}
$$
其中最后一项：  
$$
\begin{aligned} 
\sum_i  m_i  \ddot{\vec r_i'} \cdot \delta\vec r_i' &=
\sum_i  m_i ( r_i'\ddot\theta\hat e_\theta - \vec r_i'\dot\theta^2) \cdot r_i' \delta \theta \hat e_\theta \\
&=
\sum_i  m_i  {r'_i}^2 \ddot\theta \delta \theta \\
&=
I\ddot\theta \delta \theta
\end{aligned}
$$
得到：  
$$
Mg\sin\alpha\delta x - M\ddot x \delta x - I\ddot\theta \delta \theta= 0
$$
根据约束 $\delta x = R \delta \theta，\ddot x = R\ddot \theta$ 得到：  
$$
\delta x \left( Mg\sin\alpha  - M\ddot x - \frac{I\ddot{x}}{R^2} \right) = 0
\quad\Rightarrow\quad
\ddot x = \frac{Mg\sin\alpha}{M +\frac{1}{2}M} = \frac{2}{3}g\sin\alpha
$$
这是质心的运动方程，圆柱上质点只需要多加一个向心加速度。
# 3 
![zz_figure/Pasted image 20250918200705.png](/img/user/zz_figure/Pasted%20image%2020250918200705.png)

当系统处于稳定状态时，在圆盘的旋转参考系中，  
$$
\begin{aligned}  
x=l\cos\theta,~~ y = l\sin\theta
\quad &\Rightarrow \quad
\dot x=-l\dot\theta\sin\theta,~~ \dot y = l\dot\theta\cos\theta \\
&\Rightarrow \quad
\ddot x=-l(\ddot\theta\sin\theta +\dot\theta^2 \cos\theta),
~~ \ddot y = l(\ddot\theta\cos\theta - \dot\theta^2\sin\theta)
\end{aligned}
$$
$$
\delta x = -l\sin\theta \delta \theta,~~ \delta y = l\cos\theta\delta\theta
$$
$$
\vec F = m\omega^2 (\vec R +\vec l )，惯性离心力
$$
于是：  
$$
\begin{aligned}
0 &= (\vec F - m \ddot{\vec r}) \cdot \delta{\vec r} \\
&= (F_x - m\ddot x)\delta x + (F_y - m\ddot y)\delta y \\
&=
-m[\omega^2R + l\cos\theta +l(\ddot\theta\sin\theta +\dot\theta^2 \cos\theta)]l\sin\theta \delta \theta + 
m[l\sin\theta - l(\ddot\theta\cos\theta - \dot\theta^2\sin\theta)]l\cos\theta\delta\theta
\end{aligned}
$$
化简得到：  
$$
0 =l \ddot \theta +{\omega^2R}\sin\theta
$$
等价于在 $\vec g= -\omega^2\vec R$ 引力场中的运动。  







