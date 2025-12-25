---
{"dg-publish":true,"permalink":"/理力25秋/Answer for HW_14_15/","noteIcon":"default","created":"2025-12-25T10:08:52.296+08:00","updated":"2025-12-25T16:09:14.787+08:00"}
---



# 1 HW 14  
## 1.1 规则运动  
根据角速度和欧拉角的关系直接计算可得
$$
\vec{\omega}_{本体系} = \begin{bmatrix} \dot{\varphi}\sin\theta\sin\psi+\dot{\theta}\cos\psi \\ \dot{\varphi}\sin\theta\cos\psi - \dot{\theta}\sin\psi \\ \dot{\varphi}\cos\theta + \dot{\psi}  \end{bmatrix}
=
\begin{bmatrix} a\sin\theta_0\sin(\psi_0+ct) \\ -a\sin\theta_0\cos(\psi_0+ct) \\ a\cos\theta_0 + c  \end{bmatrix}
$$

## 1.2 这是一道微改的考试原题  
(2016) 五、(15 分) 质量为 $m$ , 半长轴 $a$ 、半短轴为 $b$ 的椭圆形匀质盘绕通过其中心且在盘平面内的固定轴 $e_{A O}$ 作匀速转动, 角速度为 $\omega_{0}$。转轴与㮋圆半长轴的夹角为 $\alpha$, 转轴质量可以忽略。
(1) 求主转动惯量;
(2) 写出角速度在主轴系中的分量;  
本题：(3) 写出匀质盘的转动动能.
原题：(3)' 求该椭圆盘所受到力矩。   
![zz_figure/Pasted image 20251225115402.png](/img/user/zz_figure/Pasted%20image%2020251225115402.png)
[[zz_Excalidraw/Drawing 2024-11-14 11.23.13.excalidraw\|Drawing 2024-11-14 11.23.13.excalidraw]]

解：以椭圆盘中心 O 为原点，建立如图所示的主轴坐标系 (右手系)，  $e_{1}$  沿短轴方向，  $e_{3}$  沿长轴方向,  $e_{2}$  垂直纸面向里。转动角速度在此主轴系的分量为 $\omega_{1}=-\omega_{0} \sin \alpha, \omega_{2}=0, \omega_{3}=\omega_{0} \cos \alpha$. 因为匀速转动, 所以  $\dot{\omega}_{1}=\dot{\omega}_{2}=\dot{\omega}_{3}=0$ 

*(1)* 直接计算给出
$$
I_{1}=\iint \rho\left (y^{2}+z^{2}\right) d s=\frac{m}{\pi a b} \iint z^{2} d x d z=\frac{m}{\pi a b} \int_{-a}^{a} z^{2} d z \int_{-b \sqrt{1-z^{2} / a^{2}}}^{b \sqrt{1-z^{2} / a^{2}}} d x=
 \frac{2 m}{\pi a} \int_{-a}^{a} z^{2} \sqrt{1-\frac{z^{2}}{a^{2}}} d z 
 $$
令
$$
\begin{array}{c}
\mathrm{z}=\operatorname{acos} \frac{\theta}{2} \\
I_{1}=\frac{m a^{2}}{4 \pi} \int_{0}^{2 \pi} \frac{1-\cos 2 \theta}{2} d \theta=\frac{m a^{2}}{4}
\end{array}
$$

类似地, $I_{3}=\frac{m b^{2}}{4},\ I_2=I_1 + I_3 =\frac{m}{4}(a^2+b^2)$.

*(2)* 转动角速度在此主轴系的分量为
$$
 \omega_{1}=-\omega_{0} \sin \alpha, \omega_{2}=0, \omega_{3}=\omega_{0} \cos \alpha . 因为匀速转动, 所以  \dot{\omega}_{1}=\dot{\omega}_{2}=\dot{\omega}_{3}=0 
 $$

*(3)*  在主轴系中，  
$$
T = \frac{1}{2} (I_1 \omega_1^2 + I_2 \omega_2^2 + I_3 \omega_3^2)
$$
得到  
$$
T = \frac{1}{8}m\omega_0^2 (a^2 \sin^2 \alpha + b^2 \cos^2 \alpha)
$$

*(3)'* 由欧拉动力学方程
$$
\left\{\begin{array}{l}
I_{1} \dot{\omega}_{1}-\left (I_{2}-I_{3}\right) \omega_{2} \omega_{3}=N_{1} \\
I_{2} \dot{\omega}_{2}-\left (I_{3}-I_{1}\right) \omega_{3} \omega_{1}=N_{2} \\
I_{3} \dot{\omega}_{3}-\left (I_{1}-I_{2}\right) \omega_{1} \omega_{2}=N_{3}
\end{array}\right.
$$
可得  $N_{1}=N_{3}=0, N_{2}=\left (I_{1}-I_{3}\right) \omega_{3} \omega_{1}=-\frac{m\left (a^{2}-b^{2}\right)}{4} \omega_{0}^{2} \sin \alpha \cos \alpha$, 圆盘所受到的力矩大小为 $\frac{m\left (a^{2}-b^{2}\right)}{4} \omega_{0}^{2} \sin \alpha \cos \alpha$ ，方向为沿 $-e_{2}$.  

## 1.3 匀质圆柱  
朗道：
![zz_figure/Pasted image 20251225130139.png](/img/user/zz_figure/Pasted%20image%2020251225130139.png)
接下来，微振动的拉氏量：  
$$
L = \frac{3}{4}\mu (R-a)^2 \dot{\varphi}^2 + \frac{1}{2} \mu g(R-a)\varphi^2
$$
得到拉格朗日方程  
$$
\frac{3}{2}\mu (R-a)^2 \ddot{\varphi} - \mu g(R-a)\varphi = 0
$$
$$
\ddot{\varphi} - \frac{2g}{3(R-a)} \varphi = 0
$$
$$
\omega = \sqrt{\frac{2g}{3(R-a)}}
$$
附鞠国兴解读：
![zz_figure/Pasted image 20251225125429.png](/img/user/zz_figure/Pasted%20image%2020251225125429.png)  
![zz_figure/Pasted image 20251225125447.png](/img/user/zz_figure/Pasted%20image%2020251225125447.png)

## 1.4 均质圆锥  
朗道：  
![zz_figure/Pasted image 20251225131333.png](/img/user/zz_figure/Pasted%20image%2020251225131333.png)
鞠国兴解读：  
![zz_figure/Pasted image 20251225131359.png](/img/user/zz_figure/Pasted%20image%2020251225131359.png)  
![zz_figure/Pasted image 20251225131409.png](/img/user/zz_figure/Pasted%20image%2020251225131409.png)  

## 1.5 滚动的匀质圆锥
朗道：  
![zz_figure/Pasted image 20251225131903.png](/img/user/zz_figure/Pasted%20image%2020251225131903.png)  
![zz_figure/Pasted image 20251225131915.png](/img/user/zz_figure/Pasted%20image%2020251225131915.png)

## 1.6 均质正方体  
注意到  
$$
I = \begin{bmatrix} A & B & B \\ B & A & B \\ B & B & A \end{bmatrix}, \quad \text{其中 } A = \frac{2}{3}Ma^2, B = -\frac{1}{4}Ma^2
$$
则特征方程  
$$
\begin{vmatrix} A-\lambda & B & B \\ B & A-\lambda & B \\ B & B & A-\lambda \end{vmatrix} = 0
$$
$$
(A + 2B - \lambda) \begin{vmatrix} 1 & 1 & 1 \\ B & A-\lambda & B \\ B & B & A-\lambda \end{vmatrix} = 0
$$

$$
(A + 2B - \lambda) \begin{vmatrix} 0 & 0 & 1 \\ 0 & A-\lambda-B & B \\ B-A+\lambda & B-A+\lambda & A-\lambda \end{vmatrix} = 0
$$
显然 $\lambda_1 = A + 2B$，$\lambda_{2,3} = A - B$，即 $\lambda_1 = \frac{1}{6}Ma^2$，$\lambda_{2,3} = \frac{11}{12}Ma^2$，三个主轴方向：  
$$
\mathbf{v}_1 = \frac{1}{\sqrt{3}} \begin{bmatrix} 1 \\ 1 \\ 1 \end{bmatrix}, \quad
\mathbf{v}_2 = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 \\ -1 \\ 0 \end{bmatrix}, \quad
\mathbf{v}_3 = \mathbf{v}_1 \times \mathbf{v}_2 = \frac{1}{\sqrt{6}} \begin{bmatrix} 1 \\ 1 \\ -2 \end{bmatrix}
$$

# 2 HW 15   
## 2.1 欧拉陀螺   
#### (1)
回忆，在推导题目给定的(1)式时，假定了惯性系的 z 轴为守恒角动量 $\vec{L}$ 的方向，所以，在本体系中  
$$
\vec{L} = R_\psi R_\theta R_\varphi \begin{bmatrix} 0 \\ 0 \\ L  \end{bmatrix}
= \begin{bmatrix} L\sin\theta\sin\psi \\ L\sin\theta\cos\psi \\ L\cos\theta  \end{bmatrix}
= \begin{bmatrix} I_1 \omega_0 \cos(\Omega t + \alpha) \\ I_1 \omega_0 \sin(\Omega t + \alpha) \\ I_3 \omega_{30}  \end{bmatrix}
$$
这里
$$
\omega_0 = \sqrt{\omega^2 - \omega_{30}^2}=\frac{L\sin\theta}{I_1}, \ \Omega = -\dot{\psi} = const
$$
所以  
$$
L =  \frac{I_3\omega_{30}}{\cos\theta} = I_1 \dot{\varphi}
$$
或者  
$$
L =  \frac{I_3\omega_{30}}{\cos\theta} = \frac{I_3}{\cos\theta} \cdot \frac{I_1}{I_1 - I_3} \dot{\psi}
$$
#### (2)
对称欧拉陀螺是规则运动的，已知在本体系中  
$$
\vec{\omega}_{Body} = \begin{bmatrix} \omega_0 \cos(\Omega t + \alpha) \\ \omega_0 \sin(\Omega t + \alpha) \\  \omega_{30}  \end{bmatrix}
$$
记实验系坐标轴 x,y,z，将角速度在 z 轴投影得到  
$$
\omega_z = \frac{\vec{\omega} \cdot \vec{L}}{L} = \frac{I_1 \omega_1^2 + I_1 \omega_2^2 + I_3 \omega_3^2}{L} = \frac{I_1 \omega_0^2 + I_3 \omega_{30}^2}{L}  = L \left( \frac{\sin^2\theta_0}{I_1} + \frac{\cos^2\theta_0}{I_3} \right)
$$
或者直接计算
$$
\vec{\omega}_{Lab} = \begin{bmatrix} \dot{\psi}\sin\theta\sin\varphi+\dot{\theta}\cos\varphi \\ -\dot{\psi}\sin\theta\cos\varphi + \dot{\theta}\sin\varphi \\ \dot{\psi}\cos\theta + \dot{\varphi}  \end{bmatrix}
= \begin{bmatrix} L \sin\theta_0 \cos\theta_0 (\frac{1}{I_3} - \frac{1}{I_1}) \sin\varphi(t) \\ -L \sin\theta_0 \cos\theta_0 (\frac{1}{I_3} - \frac{1}{I_1}) \cos\varphi(t) \\ L (\frac{\sin^2\theta_0}{I_1} + \frac{\cos^2\theta_0}{I_3}) \end{bmatrix}
$$
## 2.2 共面性质
本体系中  
$$
\vec{\omega} = \begin{bmatrix} \omega_0 \cos\alpha \\ \omega_0 \sin \alpha \\  \omega_{30}  \end{bmatrix}
,\quad
\vec{e_z} = \begin{bmatrix} 0 \\ 0 \\ 1  \end{bmatrix}
,\quad
\vec{L} = \begin{bmatrix} I_1 \omega_0 \cos\alpha \\ I_1 \omega_0 \sin \alpha \\ I_3 \omega_{30}  \end{bmatrix}
,\quad \alpha = \alpha(t)
$$

所以  
$$
(\vec{\omega}\times \vec{e_z}) \cdot \vec{L} 
=  \begin{bmatrix} \omega_0 \sin\alpha \\ -\omega_0 \cos\alpha \\ 0 \end{bmatrix} \cdot \begin{bmatrix} I_1 \omega_0 \cos\alpha \\ I_1 \omega_0 \sin \alpha \\ I_3 \omega_{30}  \end{bmatrix}
=0
$$
所以三者共面。
## 2.3 均质盘旋转  
![zz_figure/Pasted image 20251225144045.png](/img/user/zz_figure/Pasted%20image%2020251225144045.png)

## 2.4 这是一道真题  
![zz_figure/Pasted image 20251225145044.png](/img/user/zz_figure/Pasted%20image%2020251225145044.png)
[[zz_Excalidraw/Drawing 2024-11-14 14.15.10.excalidraw\|Drawing 2024-11-14 14.15.10.excalidraw]]

(1)    
$$
H = \frac{p_\theta^2}{2I_1} + V_{eff} (\theta), \quad V_{eff} (\theta) = \frac{(p_\varphi - p_\psi\cos\theta)^2}{2I_1 \sin^2\theta} + \frac{p_\psi^2}{2I_3} + mgl\cos\theta
$$
根据循环坐标得到运动积分  
$$
p_\psi = const, \quad p_\varphi = const.
$$
以及 H 不显含 t：  
$$
H \equiv E = const
$$

(2)
$$
\begin{gather}
\mathrm{S}=-E t+p_{\phi} \phi+p_{\psi} \psi+W_{\theta}(\theta) \\[10pt]
\frac{1}{2 I_{1}}\left\{\frac{\left(p_{\phi}-p_{\psi} \cos \theta\right)^{2}}{\sin ^{2} \theta}+\left(\frac{d W_{\theta}}{d \theta}\right)^{2}\right\}+\frac{p_{\psi}^{2}}{2 I_{3}}+m g l \cos \theta=E \\[10pt]
\Rightarrow \frac{d W_{\theta}}{d \theta}= \sqrt{2 I_{1}\left(E-\frac{p_{\psi}^{2}}{2 I_{3}}-m g l \cos \theta\right)-\frac{\left(p_{\phi}-p_{\psi} \cos \theta\right)^{2}}{\sin ^{2} \theta}} \\[10pt]
\Rightarrow \mathrm{~S}=-E t+p_{\phi} \phi+p_{\psi} \psi + \int \sqrt{2 I_{1}\left(E-\frac{p_{\psi}^{2}}{2 I_{3}}-m g l \cos \theta\right)-\frac{\left(p_{\phi}-p_{\psi} \cos \theta\right)^{2}}{\sin ^{2} \theta}} d \theta
\end{gather}
$$
运动积分：  
$$
\xi = \frac{\partial S}{\partial E} = -t + \int \frac{I_1 \, d\theta}{\sqrt{2 I_{1}\left(E - \frac{p_{\psi}^{2}}{2 I_{3}} - mgl \cos \theta\right) - \frac{\left(p_{\phi} - p_{\psi} \cos \theta\right)^{2}}{\sin ^{2} \theta}}}
\Rightarrow \theta(t)
$$
$$
Q_\phi = \frac{\partial S}{\partial p_\phi} = \phi - \int \frac{(p_{\phi} - p_{\psi} \cos \theta) / \sin^2 \theta}{\sqrt{2 I_{1}(E - \frac{p_{\psi}^{2}}{2 I_{3}} - mgl \cos \theta) - \frac{(p_{\phi} - p_{\psi} \cos \theta)^{2}}{\sin ^{2} \theta}}} d\theta
\Rightarrow \phi(\theta)
$$
$$
Q_\psi = \frac{\partial S}{\partial p_\psi} = \psi - \int \frac{\frac{I_1 p_\psi}{I_3} - \frac{(p_\phi - p_\psi \cos \theta)\cos \theta}{\sin^2 \theta}}{\sqrt{2 I_{1}(E - \frac{p_{\psi}^{2}}{2 I_{3}} - mgl \cos \theta) - \frac{(p_{\phi} - p_{\psi} \cos \theta)^{2}}{\sin ^{2} \theta}}} d\theta 
\Rightarrow 
\psi(\theta)
$$

另一道类似的：

(2021) 五、(25 分）拉格朗日陀螺为在重力场中的对称刚体  $\left (I_{1}=I_{2} \neq I_{3}\right)$  。它的拉格朗日量为:    
 $$
 \mathcal L=   \frac{I_{1}}{2}\left (\dot{\theta}^{2}+\dot{\varphi}^{2} \sin ^{2} \theta\right)+\frac{I_{3}}{2}(\dot{\psi}+\dot{\varphi} \cos \theta)^{2}-m g l \cos \theta
 $$
(1)根据 $\mathcal L$ 的对称性，找出系统的三个守恒量并说明理由;  
(2)根据刚体的欧拉动力学方程, 证明广义动量  $p_{\varphi}$  和 $p_{\psi}$  为运动积分。

*(1)* 拉格朗日量  $L$  不显含时间, 因此哈密顿量  $H=E$  为守恒量。另外,  $\psi, \varphi$  为循环坐标, 因此正则动量  $p_{\psi}, p_{\varphi}$ 为运动积分, 即:  
$$
\boxed{
\begin{array}{c}
\frac{I_{1}}{2}\left(\dot{\theta}^{2}+\dot{\varphi}^{2} \sin ^{2} \theta\right)+\frac{I_{3}}{2}(\dot{\psi}+\dot{\varphi} \cos \theta)^{2}-m g l \cos \theta=E=\text { const } . \\
p_{\psi}=\frac{\partial L}{\partial \dot{\psi}}=I_{3}(\dot{\psi}+\dot{\varphi} \cos \theta)=\text { const } . \\
p_{\varphi}=\frac{\partial L}{\partial \dot{\varphi}}=\left(I_{3} \cos ^{2} \theta+I_{1} \sin ^{2} \theta\right) \dot{\varphi}+I_{3} \dot{\psi} \cos \theta=\text { const }
\end{array}
}
$$
*(2)* 力矩的方向显然同时垂直于刚体的 $z$ 轴和实验室系的 $z^{\prime}$ 方向, 因此,  
$$
N_{3}=0,\quad N_{3'}=0
$$
根据欧拉动力学公式有:  
$$
I_{3} \dot{\omega}_{3}-\left(I_{1}-I_{2}\right) \omega_{1} \omega_{2}=I_{3} \dot{\omega}_{3}=0
$$
即  
$$
p_{\psi}=L_{3}=I_{3} \omega_{3}=I_{3}(\dot{\psi}+\dot{\varphi} \cos \theta)=\text { const } .
$$
另外,  
$$
\frac{d}{d t}\left(L_{3^{\prime}}\right)=N_{3^{\prime}}=0
$$
易得：  
$$
p_{\varphi}=L_{3 \prime}=\left(I_{3} \cos ^{2} \theta+I_{1} \sin ^{2} \theta\right) \dot{\varphi}+I_{3} \dot{\psi} \cos \theta=\text { const. }
$$
其中刚体绕实验室系的  $z^{\prime}$  轴的转动惯量为:  
$$
I_{3 \prime}=I_{3} \cos ^{2} \theta+I_{1} \sin ^{2} \theta
$$


## 2.5 这也是一道考试原题      
![zz_figure/例题_8_1735188880970_edit_2610390595185489.png](/img/user/zz_figure/%E4%BE%8B%E9%A2%98_8_1735188880970_edit_2610390595185489.png)

也可以由角动量的进动角速度 $\Omega = \omega_0 = \frac{N}{J \sin \theta} = \frac{N}{I_3\omega_0}$ 得到, 
$$
N = \omega_0 \cdot I_3 \omega_0 = \frac{1}{2}mr\omega_0^2 = N_{水平面对圆盘支持力} - mg
$$
附 :  

> [!info] 角动量进动和外力力矩的关系  
> 
> 对于 $z$ 方向力矩，不需要考虑，它只对角动量的自转起作用。只考虑垂直于 $z$ 方向的力矩 $M$。
> ![zz_figure/Pasted image 20251225153320.png](/img/user/zz_figure/Pasted%20image%2020251225153320.png)
> 如图，角动量守恒:$$\Delta J = Jsin\theta \Delta \varphi = M \Delta t\quad\to\quad\Omega = \frac{\Delta\varphi}{\Delta t} = \frac{M}{J \sin \theta}$$
> 可以发现有效力矩指向 $x$ 方向。进动周期: $$T_p = \frac{2\pi}{\Omega}$$

## 2.6 这题作为第三小问考过  
注意到  
$$
H = \frac{p_\theta^2}{2I_1} + V_{eff} (\theta), \quad V_{eff} (\theta) = \frac{(p_\varphi - p_\psi\cos\theta)^2}{2I_1 \sin^2\theta} + \frac{p_\psi^2}{2I_3} + mgl\cos\theta
$$
$$
p_\theta = I_1 \dot{\theta}
$$
在 $\theta=const$ 时，$\dot{\varphi} = \frac{ \partial H }{ \partial p_\varphi } = f(\theta) = const$ 自动成立，所以条件只有 $p_\theta \sim \dot{\theta} = 0$，此时  
$$
E = {V_{eff}}_{min}
$$
即  
$$
\frac{ \mathrm{d} V_{eff} }{ \mathrm{d} \theta} = 0
$$
应当有解。



一个圆锥密度均匀为 $\rho$ , 总质量 $M$, 底部的圆半径为 $R$ , 高为 $h$ 。
(1). 求相对于圆雉顶点的主转动惯量 $I_{1}, I_{2}, I_{3}$ .
(2). 以圆雉顶点为固定点, 求重力场中, 该重对称陀螺的拉氏量及三个守恒量方程.
(3). 重对称陀螺也能均匀进动 (章动角 $\theta$ 和进动角速度 $\dot{\phi}$ 保持不变)。以圆锥顶点为固定点, 求该重对称陀螺可以均匀进动的角速度  $\dot{\phi}$ , 并给出均匀进动的存在性条件

(1) 选取 $z$ 轴为垂直于底面的对称轴的坐标系, 原点在底面中心。得：
$$
I_{1}=I_{2}=\frac{3}{20} M\left(R^{2}+4 h^{2}\right), \quad I_{3}=\frac{3}{10} M R^{2}
$$
tips : 积分时使用平行轴定理
$$
\begin{array}{c}
I_{1}=\int_{0}^{h}\left[\frac{1}{4} d m \cdot r^{2}+d m \cdot z^{2}\right] \\
d m=\rho \pi r^{2} d z, \quad r=\frac{R}{h} z, \quad M=\frac{1}{3}\pi R^2h
\end{array}
$$
(2) 刚体的质心高度 : 
$$
l=\frac{\int_{0}^{h} z\cdot r^2 d z}{\int_{0}^{h} r^2 d z}=\frac{3}{4} h
$$
刚体的拉格朗日量为
$$
L=\frac{I_{1}}{2}\left(\dot{\theta}^{2}+\dot{\phi}^{2} \sin ^{2} \theta\right)+\frac{I_{3}}{2}(\dot{\psi}+\dot{\phi} \cos \theta)^{2}-\frac{3}{4} m g h \cos \theta
$$

三个守恒量分别为:
$$
\begin{array}{c}
E=\frac{I_{1}}{2}\left(\dot{\theta}^{2}+\dot{\phi}^{2} \sin ^{2} \theta\right)+\frac{I_{3}}{2}(\dot{\psi}+\dot{\phi} \cos \theta)^{2}+\frac{3}{4} m g h \cos \theta \\
P_{\phi}=\frac{\partial L}{\partial \dot{\phi}}=\left(I_{1} \sin ^{2} \theta+I_{3} \cos ^{2} \theta\right) \dot{\phi}+I_{3} \cos \theta \dot{\psi}=\text { const } . \\
P_{\psi}=\frac{\partial L}{\partial \dot{\psi}}=I_{3}(\dot{\psi}+\dot{\phi} \cos \theta)=I_{3} \omega_{3}=\text { const }
\end{array}
$$
(3) <font color="#ff0000">解法一</font>:

根据欧拉-拉格朗日方程, 得到 $\theta$ 方向的运动方程为:
$$
I_{1} \ddot{\theta}=\left(I_{1} \cos \theta \dot{\phi}^{2}-I_{3} \omega_{3} \dot{\phi}+3 M g h / 4\right) \sin \theta
= \frac{ \mathrm{d} V_{eff} }{ \mathrm{d} \theta}
$$
均匀进动时,  $\ddot{\theta}=0, \theta=\theta_{0}$, 因此,
$$
I_{1} \cos \theta \dot{\phi}^{2}-I_{3} \omega_{3} \dot{\phi}+3 M g h / 4=0
$$
这是关于  $\dot{\phi}$  的二次方程，方程有解的条件：
$$
\Delta=\left(I_{3} \omega_{3}\right)^{2}-3 M g h I_{1} \cos \theta_{0} \geq 0
$$
即：
$$
\omega_{3} \geq \frac{\sqrt{3 M g h I_{1} \cos \theta_{0}}}{I_{3}}
$$
<font color="#ff0000">解法二</font> :   

根据上面三个守恒量, 得到 $\theta$ 方向的运动满足:
$$
\begin{array}{c}
\frac{I_{1}}{2} \dot{\theta}^{2}=E^{\prime}-V_{e f f}(\theta) \\
E^{\prime}=E-\frac{P_{\psi}^{2}}{2 I_{3}} \\
V_{e f f}(\theta)=\frac{\left(P_{\phi}-P_{\psi} \cos \theta\right)^{2}}{2 I_{1} \sin ^{2} \theta}+\frac{3}{4} m g h \cos \theta
\end{array}
$$
均匀进动的条件为 $V_{e f f}(\theta)$  取极小值, 即:
$$
\begin{array}{c}
E^{\prime}=V_{e f f}\left(\theta_{0}\right) \\
\left.\frac{d V_{e f f}(\theta)}{d \theta} \right\rvert\, \theta=\theta_{0}=0
\end{array}
$$
令:
$$
\begin{array}{c}
\alpha=\frac{2 E^{\prime}}{I_{1}}, \quad \beta=\frac{3 m g h}{2 I_{1}}, \quad a=\frac{P_{\psi}}{I_{1}}, 
\quad b=\frac{P_{\phi}}{I_{1}},\quad u=cos\theta \\
\dot{u}^{2}=\left(1-u^{2}\right)(\alpha-\beta u)-(b-a u)^{2} \equiv f(u)
\end{array}
$$
另有:
$$
\dot{\phi}=\frac{(b-a u)}{1-u^{2}}
$$
由 $f\left(u_{0}\right)=0$ , 得到:
$$
\alpha-\beta u_{0}=\frac{\left(b-a u_{0}\right)^{2}}{\left(1-u_{0}^{2}\right)}
$$
由 $f^{\prime}\left(u_{0}\right)=0$ , 得到:
$$
\frac{\beta}{2}=\frac{a\left(b-a u_{0}\right)}{\left(1-u_{0}^{2}\right)}-\frac{u_{0}\left(\alpha-\beta u_{0}\right)}{\left(1-u_{0}^{2}\right)}
$$
利用:
$$
\dot{\phi}_{0}=\frac{\left(b-a u_{0}\right)}{1-u_{0}^{2}}
$$
得到：
$$
\frac{\beta}{2}=a \dot{\phi}_{0}-u_{0} \dot{\phi}_{0}^{2}
$$
这是关于 $\dot{\phi}_{0}$ 的二次方程，方程有解的条件是：
$$
\Delta=a^{2}-2 \beta u_{0} \geq 0
$$
即：
$$
\omega_{3} \geq \frac{\sqrt{3 M g h \cos \theta_{0} I_{1}}}{I_{3}}
$$
