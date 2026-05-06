---
{"dg-publish":true,"permalink":"/理力25秋/Answer for HW5/","noteIcon":"default","created":"2025-12-01T13:38:11.788+08:00","updated":"2025-11-10T19:24:24.597+08:00"}
---

# 1 相互作用的守恒量（注意使用 Noether 定理）  
- 能量： $L$ 不显含 $t$，得到对于无限小时间平移 $t\to t+\epsilon$，$L$ 将不变，即 $H \equiv \frac{ \partial \mathcal{L} }{ \partial \dot q }  \dot q - \mathcal L  = \frac{1}{2} m_{1} \dot{\vec{r}}_{1}^{2}+\frac{1}{2} m_{2} \dot{\vec{r}}_{2}^{2}+V\left(\left|\vec{r}_{2}-\vec{r}_{1}\right|\right)=const.$ 也不显含时间，即守恒。

- 动量：对于无限小空间平移 $\vec{r}(t) \rightarrow \vec{r}(t)+\vec{\epsilon}$ ，$L' = \frac{1}{2} m_{1} \dot{\vec{r}}_{1}^{2}+\frac{1}{2} m_{2} \dot{\vec{r}}_{2}^{2}-V\left(\left|\vec{r}_{2} + \vec \epsilon -\vec{r}_{1} - \vec\epsilon\right|\right) = L$ 不变，因此变分 $\delta L$ 不变，对应动量守恒。

- 角动量：三维旋转群 $SO(3)$ 的生成元可以写作 $(J_i)_{jk} = -\epsilon_{ijk}$ , 于是欧氏空间中的无限小旋转可表述为
$$
r_i ~\to~ r_i'= e^{\vec \theta \cdot \mathbf{J}_i}\cdot \vec r = \left[\ I+\theta_j (J_i)_{jk} \ \right]r_k = r_i - \epsilon_{ijk}\theta_j r_k =  r_i + \epsilon_{ijk}\theta_k r_j , \quad i=x,y,z
$$
$$
\boxed{
\delta {r}_{i}=\epsilon_{i j k} \theta_{k} {r}_{j} \quad or \quad \delta\vec{r} = -\vec{\theta}\times\vec{r}
}
$$
$$
\delta \dot{r}_{i}=\epsilon_{i j k} \theta_{k} \dot{r}_{j}
$$
由于 $L$ 仅依赖于速度的平方 $\dot{\vec{r}}_{a}^{2},(a=1,2)$ 和相对距离 $|\vec{r}_{2}-\vec{r}_{1}|$，而旋转是正交变换 (<font color="#ff0000">保持长度/距离不变</font>)，即  $\dot{\vec{r}}_{a}^{\prime 2} = \left(\dot{r}_{a,i} + \delta \dot{r}_{a,i}\right)^2 = \dot{r}_{a,i}^2 + 2\dot{r}_{a,i}\delta \dot{r}_{a,i} + O(\theta^2) = \dot{r}_{a,i}^2 + 2\dot{r}_{a,i}\left(\epsilon_{ijk} \theta_k \dot{r}_{a,j}\right) + O(\theta^2)$。由于 $\dot{r}_{a,i}\left(\epsilon_{ijk} \theta_k \dot{r}_{a,j}\right) = \theta_k \left(\epsilon_{ijk} \dot{r}_{a,i} \dot{r}_{a,j}\right) = \theta_k \left(\dot{\vec{r}}_{a} \times \dot{\vec{r}}_{a}\right)_k = 0$，所以 $\dot{\vec{r}}_{a}^{\prime 2} = \dot{\vec{r}}_{a}^{2}$。  

以及，$|\vec{r}_{2}^{\prime} - \vec{r}_{1}^{\prime}|^2 = \left|(\vec{r}_{2} - \vec{\theta} \times \vec{r}_{2}) - (\vec{r}_{1} - \vec{\theta} \times \vec{r}_{1})\right|^2 = |\vec{R} - \vec{\theta} \times \vec{R}|^2 = |\vec{R}|^2+ O(\theta^2) = |\vec{R}|^2$，其中 $\vec{R} = \vec{r}_{2} - \vec{r}_1$，因此势能 $V$ 不变。满足旋转对称性，变分 $\delta L$ 不变，即角动量守恒。

# 2 阿特伍德机的对称性  
假设中间 $3m$ 的滑轮坐标为 $z$，那么绳长不变约束是：
$$
x+y+z=C \quad\Longrightarrow\quad
\dot z = -\dot x - \dot y
$$
于是拉氏量是：  
$$
\begin{aligned} 
L &= \frac{1}{2} (4m\dot x^2 + 3m\dot z^2 + m\dot{y}^2) - mg(4x+3z + y) \\[4pt]
&\equiv
\frac{1}{2} \left( 4m\dot x^2 + 3m (\dot{x}+\dot{y})^2 + m\dot{y}^2 \right) - mg(x-2y) \\[4pt]
&=
\frac{1}{2}m (7\dot{x}^2 + 6\dot{x}\dot{y}+ 4\dot{y}^2) - mg(x-2y)
\end{aligned}
$$
假设在平移 $x \to x' = x + \epsilon,\ y \to y' = y + k\epsilon,\ k=\frac{y_\epsilon}{x_\epsilon}$ 下满足对称性：  
$$
\begin{aligned}  
0 = \delta L = L' - L
&\approx 
\frac{\partial L}{\partial x} \delta x + \frac{\partial L}{\partial y} \delta y + \frac{\partial L}{\partial \dot{x}} \delta \dot{x} + \frac{\partial L}{\partial \dot{y}} \delta \dot{y}\\[4pt]
&=
 \frac{\partial L}{\partial x}\epsilon + \frac{\partial L}{\partial y} k\epsilon  \\[4pt]
&= mg (2k - 1) \epsilon
\end{aligned}
$$
得到 $k=\frac{y_\epsilon}{x_\epsilon}=\frac{1}{2}$，另外，Noether 定理给出的守恒荷的表达式是：  
$$
\boxed{
J = \sum_\alpha \frac{ \partial \mathcal{L} }{ \partial \dot q_\alpha }  \delta q_\alpha - G + \int^t \frac{ \partial \mathcal{L} }{ \partial t } \delta t ~dt
}
$$
在这里后两项为 0，于是守恒荷是：  
$$
\begin{aligned} 
J &=\sum_\alpha \frac{ \partial \mathcal{L} }{ \partial \dot q_\alpha }  \delta q_\alpha 
=
p_x\delta x + p_y \delta y \\[4pt]
&=
m(7\dot{x} + 3\dot{y})\epsilon + m(4\dot{y} + 3\dot{x}) \cdot \frac{1}{2}\epsilon\\[4pt]
&=
\frac{1}{2}m\epsilon (17\dot{x} + 10 \dot{y})
\end{aligned}
$$
对应的守恒量就是 $2p_x + p_y = m (17\dot{x} + 10 \dot{y})$。
# 3 电荷在电磁场中运动的对称性  
#### (a)  
直接代入(3)到(1)得到拉氏量在 boost 下不变：
$$
\begin{aligned} 
L' &= \frac{m}{2} \left(-\dot{t_\epsilon}^{2}+\dot{x_\epsilon}^{2}\right) \\[4pt]
&= \frac{m}{2} \left(- (\cosh \epsilon \dot{t} - \sinh\epsilon\dot{x})^{2}+(-\sinh\epsilon\dot{t}+ \cosh \epsilon \dot{x})^{2}\right)
\\[4pt]
&= \frac{m}{2}\left(-\dot{t}^{2}+\dot{x}^{2}\right) = L
\end{aligned}
$$
为了找到守恒荷，可以将无限小 boost 视为一种平移，即取 $\epsilon\to 0$：  
$$
\begin{bmatrix} t_\epsilon  \\  x_\epsilon \end{bmatrix}
=
\begin{bmatrix} \cosh\epsilon & -\sinh\epsilon \\  -\sinh\epsilon & \cosh\epsilon \end{bmatrix}\begin{bmatrix} t  \\  x \end{bmatrix}
\approx
\begin{bmatrix} 1 & -\epsilon \\  -\epsilon & 1 \end{bmatrix} \begin{bmatrix} t  \\  x \end{bmatrix}
$$
也即  
$$
\delta t = -\epsilon x,\ \delta x = -\epsilon t
$$
于是守恒荷是：  
$$
\begin{aligned} 
J &=\sum_\alpha \frac{ \partial \mathcal{L} }{ \partial \dot q_\alpha }  \delta q_\alpha 
=
p_x\delta x + p_t \delta t \\[4pt]
&=
m\dot{x}\cdot (-\epsilon t) - m\dot{t} \cdot (-\epsilon x) \\[4pt]
&=
\epsilon m ( -\dot{x}t + \dot{t}x)
\end{aligned}
$$
对应的守恒量就是 $m ( -\dot{x}t + \dot{t}x)$。  
> [!note] 该守恒量的物理含义
> 假设有多个粒子，将 x 选取为系统质心的坐标，在题示拉氏量所表示的自由运动下，$x=x_0 + vt\to \dot{x} =v\dot{t}$，于是守恒量 $m ( -\dot{x}t + \dot{t}x)=m(\dot{t} x-(\dot{t} v) t) =m \dot{t}(x-v t) = const. \to x=x_0 + vt$，恰好前后相容，即系统的惯性中心保持匀速运动（更一般的，我们常说这个守恒量反映能量中心保持匀速运动，因为 $E=mc^2$），这个守恒量其实没什么意思。  
> 

#### (b) 
同理，根据 $\delta t = -\epsilon x,\ \delta x = -\epsilon t \to \delta \dot{t} = -\epsilon \dot{x},\ \delta \dot{x} = -\epsilon \dot{t}$，已经知道 $\frac{m}{2}\left(-\dot{t}^{2}+\dot{x}^{2}\right) = L$ 在 boost 下不变，所以只需考虑 $L_{e} = e\left(-\varphi \dot{t}+\frac{1}{c} A \dot{x}\right)$，这里 $\frac{ \mathrm{d} G(x^\mu,\tau) }{ \mathrm{d} \tau} = \delta L_e$ 而不是为 0，是因为题目要求让作用量不变，而不是让拉氏量不变：  
$$
\begin{aligned}  
\frac{ \mathrm{d} G(x^\mu,\tau) }{ \mathrm{d} \tau} = \delta L_e = L_e' - L_e 
&\approx 
\frac{ \partial L_e }{ \partial \dot{x}^\mu } \delta \dot{x}^\mu + \frac{ \partial L_e }{ \partial {x}^\mu } \delta {x}^\mu
\\[4pt]
&=
\frac{\partial L_e}{\partial \dot{t}}(-\epsilon \dot{x}) + \frac{\partial L}{\partial \dot{x}} (-\epsilon {t}) +  \frac{\partial L_e}{\partial {t}}(-\epsilon {x}) + \frac{\partial L}{\partial {x}} (-\epsilon {t})  \\[4pt]
&= 
-\epsilon e\left[  -\varphi \dot{x} + A\dot{t}  - \frac{ \partial \varphi }{ \partial t }\dot{t}x + \frac{ \partial A }{ \partial t }\dot{x}x - \frac{ \partial \varphi }{ \partial x }\dot{t}t+ \frac{ \partial A }{ \partial x } \dot{x} t\right] \\[4pt]
&=
-\epsilon e \left\{  \dot{t} \left(  
A - \frac{ \partial \varphi }{ \partial t } x - \frac{ \partial \varphi }{ \partial x }t
\right)  
- \dot{x} \left(   
\varphi -  \frac{ \partial A }{ \partial t }x - \frac{ \partial A }{ \partial x } t
\right)\right\}
\end{aligned}
$$
即
$$
\mathrm{d}G = -\epsilon e \left\{
\left(  
A - \frac{ \partial \varphi }{ \partial t } x - \frac{ \partial \varphi }{ \partial x }t
\right)   \mathrm{d}t
- \left(   
\varphi -  \frac{ \partial A }{ \partial t }x - \frac{ \partial A }{ \partial x } t
\right)\mathrm{d}x
\right\}
$$
这是一个全微分，所以需要满足：  
$$
\frac{ \partial  }{ \partial x }\left(  
A - \frac{ \partial \varphi }{ \partial t } x - \frac{ \partial \varphi }{ \partial x }t
\right)
=
-\frac{ \partial  }{ \partial t } \left(   
\varphi -  \frac{ \partial A }{ \partial t }x - \frac{ \partial A }{ \partial x } t
\right)
$$
即  
$$
x\frac{ \partial  }{ \partial t } \left( \frac{ \partial \varphi }{ \partial x } + \frac{ \partial A }{ \partial t } \right) + t \frac{ \partial  }{ \partial x } \left( \frac{ \partial \varphi }{ \partial x } + \frac{ \partial A }{ \partial t } \right) = 0
$$
注意到 2 维时空中 $E=-\nabla \varphi-\frac{\partial A}{\partial t} = -\frac{\partial \varphi}{\partial x}-\frac{\partial A}{\partial t}$，上式变为：  
$$
x \frac{\partial E}{\partial t}+t \frac{\partial E}{\partial x}=0
$$
这是一个一阶线性齐次偏微分方程，可以使用特征线法来求解这个方程，特征线的微分方程为：
$$
\frac{d x}{t}=\frac{d t}{x} = \frac{dE}{0} 
\quad\Longrightarrow\quad  
x d x=t d t , \ dE|_{沿着特征线} = 0
\quad\Longrightarrow\quad
x^{2}-t^{2}=C
$$
可知 $E$ 在特征线上是常数，所以 $E$ 必须满足：
$$
{E}({x}, {t})={f}\left({x}^{2}-{t}^{2}\right) = f(s^2) = -\frac{\partial \varphi}{\partial x}-\frac{\partial A}{\partial t}
$$
即电场本身就是洛伦兹不变的，特征线就是世界线 $s^2 = -t^2 + x^2$。  

注意，加入电磁场后，广义动量变为
$$
p_\mu = \frac{ \partial L }{ \partial \dot{x}^\mu } = -m {\dot{x}_\mu} - e A_\mu
$$
$$
\Rightarrow\quad  \begin{aligned} 
p_t &= - m\dot{t} - e\varphi  \\
p_x  &= m \dot{x} + e{A}
\end{aligned}
$$
于是守恒荷是：  
$$
\begin{aligned} 
J &=\sum_\alpha \frac{ \partial \mathcal{L} }{ \partial \dot q_\alpha }  \delta q_\alpha - G  \\[4pt]
&=
p_x\delta x + p_t \delta t -G \\[4pt]
&
= m ( -\dot{x}t + \dot{t}x) - e (t A - x \phi) - G
\end{aligned}
$$















