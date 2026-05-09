---
{"dg-publish":true,"permalink":"/电动26春/EMD_answer_phj/HW Answer/HW5 Answer/","noteIcon":"default","created":"2026-04-04T20:23:03.688+08:00","updated":"2026-05-09T17:21:08.718+08:00","dg-note-properties":{}}
---

[[电动26春/EMD_answer_phj/HW Answer/HW6 Answer\|HW6 Answer]]  

<iframe src="/img/user/%E7%94%B5%E5%8A%A826%E6%98%A5/EMD_answer_phj/HW/electrodynamics05.pdf" width="100%" height="900px" title="electrodynamics05" style="border:1px solid #ccc;"></iframe>
# 1 《电磁学与电动力学》（下册）
![zz_figure/Pasted image 20260404212053.png](/img/user/zz_figure/Pasted%20image%2020260404212053.png)  
![zz_figure/Pasted image 20260404212116.png](/img/user/zz_figure/Pasted%20image%2020260404212116.png)
![zz_figure/Pasted image 20260404212137.png](/img/user/zz_figure/Pasted%20image%2020260404212137.png)  

###### 8.4 可以借助最后一个思考题来解决  
四维速度 $U^\mu$ 和四维加速度 $A^\mu$ 定义为 $U^\mu = \frac{\mathrm{d}x^\mu}{\mathrm{d}\tau} = (\gamma c, \gamma \boldsymbol{v}) \implies U^\mu U_\mu = -c^2$，$A^\mu = \frac{\mathrm{d} U^\mu}{\mathrm{d} \tau} = \gamma \frac{\mathrm{d}}{\mathrm{d} t} (\gamma c, \gamma \boldsymbol{v}) = (\gamma \beta a, \gamma\boldsymbol{a}) \implies A^\mu A_\mu = a^2$。

前三年，运动的兄弟的世界线满足双曲关系  
$$
\left( x+\frac{c^2}{a} \right)^2 - (ct)^2 = \left(\frac{c^2}{a}\right)^2
$$
这里的 $a=g$，对 $U^\mu U_\mu = -c^2$，假设其参数化为  
$$
U^0 = c \cosh \phi, \quad U^1 = c \sinh \phi, \quad U^2 = U^3 = 0
$$
$$
\implies
A^\mu = \frac{\mathrm{d} U^\mu}{\mathrm{d}\tau} = \left( c \sinh \phi \frac{\mathrm{d}\phi}{\mathrm{d}\tau}, c \cosh \phi \frac{\mathrm{d}\phi}{\mathrm{d}\tau} \right)
$$
$$
\implies
A^\mu A_\mu = c^2 \left( \frac{\mathrm{d}\phi}{\mathrm{d}\tau} \right)^2 = a^2 \implies 
\frac{\mathrm{d}\phi}{\mathrm{d}\tau} = \frac{a}{c}~(\text{此处取正分支})
$$
设 $\tau=0$ 时 $\phi=0$ 积分得到：
$$
\phi(\tau) = \frac{a\tau}{c}
$$
所以 $U^0 = c \cosh \left( \frac{a\tau}{c} \right), \quad U^1 = c \sinh \left( \frac{a\tau}{c} \right), \quad U^2 = U^3 = 0$，进而按4速度的定义得到
$$
\frac{\mathrm{d}t}{\mathrm{d}\tau} = \frac{U^0}{c}= \cosh\left(\frac{a\tau}{c}\right)
$$
设 $t(0)=0$：
$$
\implies 
\boxed{
t(\tau) = \frac{c}{a} \sinh\left(\frac{a\tau}{c}\right)
}
$$
同理按4速度的定义得到
$$
\frac{\mathrm{d}x}{\mathrm{d}\tau} = U^1 = c \sinh \phi = c \sinh\left(\frac{a\tau}{c}\right)
$$
直接对 $\tau$ 积分得到：
$$
\boxed
{x(\tau) = \frac{c^2}{a} \cosh\left(\frac{a\tau}{c}\right) + \frac{c^2}{a}}
$$
这样就给出了bro的参数化世界线。下面给一个例子，绘制了运动的bro的世界线：  
![zz_figure/Pasted image 20260414145843.png](/img/user/zz_figure/Pasted%20image%2020260414145843.png)
```desmos-graph 
left=-1;right=10
top=24;bottom=-3
---
(x+2)^2 - y^2 =4|x>0|5>y>0|green
(x-2-3.3852*2)^2 - (y-10)^2 =4|3.3852*2>x>3.3852|10>y>5|red
(x-2-3.3852*2)^2 - (y-10)^2 =4|3.3852*2>x>3.3852|15>y>10|blue
(x+2)^2 - (y-20)^2 =4|3.3852>x>0|20>y>15|orange
```

# 2 补充题  
## 2.1 
显然  
$$
T^\alpha{}_\beta = \begin{pmatrix} -2 & 0 & 1 & -1 \\ 1 & 0 & 3 & 2 \\ 1 & 1 & 0 & 0 \\ 2 & 1 & 1 & 2 \end{pmatrix}
,\quad
T_\alpha{}^\beta = \begin{pmatrix} -2 & 0 & -1 & 1 \\ -1 & 0 & 3 & 2 \\ -1 & 1 & 0 & 0 \\ -2 & 1 & 1 & 2 \end{pmatrix}
$$
$$
T^{(\alpha\beta)} = \begin{pmatrix} 2 & -0.5 & 0 & -1.5 \\ -0.5 & 0 & 2 & 1.5 \\ 0 & 2 & 0 & 0.5 \\ -1.5 & 1.5 & 0.5 & 2 \end{pmatrix}
,\quad
T^{[\alpha\beta]} = \begin{pmatrix} 0 & 0.5 & 1 & 0.5 \\ -0.5 & 0 & 1 & 0.5 \\ -1 & -1 & 0 & -0.5 \\ -0.5 & -0.5 & 0.5 & 0 \end{pmatrix}
$$
$$
T^\alpha{}_\alpha = 0, \quad X^\alpha X_\alpha = 7,\quad X_\alpha T^{\alpha\beta} = (4, -2, 5, -1)
$$
## 2.2 
$$
\Delta s^2 = -50 < 0, \quad  \text{类时}
$$
所以不可能同时发生，可能同地发生。设新惯性系 $K'$ 相对于 $K$ 的速度为 $\vec{v}$，直接根据 $\Delta \boldsymbol{r}' = 0$ 和洛伦兹变换可知
$$\boldsymbol{v} = \frac{c \Delta \vec{r}}{\Delta ct} = -\left( \frac{1}{2}, \frac{1}{2}, 0 \right)c, \quad v = \frac{\sqrt{2}}{2} c \approx 0.707c$$
## 2.3 
中微子速度接近光速，所以  
$$
\Delta t = \frac{L}{v_\min} - \frac{L}{v_{\max}} \approx \frac{L\Delta v}{c^2} \implies \Delta v \approx c\left( \Delta t / \frac{L}{c} \right)
= c(12\text{~s} / 1.6\times 10^5 \text{~years}) \approx 2.4 \times 10^{-12} c
$$
中微子和光到达时间相差为  
$$
\Delta t' = \frac{L}{v} - \frac{L}{c} \approx \frac{L}{c} \cdot \frac{{c-v}}{c} \approx 1\text{~h} \implies {c-v} \approx 10^{-9} c
$$
## 2.4 
你可以直接计算积分  
$$
\Delta \tau = \int_A^B \sqrt{1-\frac{v^2(t)}{c^2}} \,\mathrm{d}t
$$
来解决此题。更简单的方法是，首先计算交点  
$$
\frac{ct_B}{4} = \frac{at_B^2}{2} \implies t_B = \frac{c}{2a} \implies v_\max = at_B = \frac{c}{2}
$$
即第二条世界线的最大速度为 $\frac{c}{2}$，意味着第二只钟是类时的，课上讲到“类时的世界线中直线的固有时最大”，所以第一只钟显示更长的固有时。


# 3 思考题  
## 3.1 
$$
\Delta s'^2 = g^{\alpha\beta}\mathrm{d}x'_\alpha\mathrm{d}x'_\beta 
= g^{\rho\sigma} \mathrm{d}x_\rho\mathrm{d}x_\sigma 
= g^{\rho\sigma}\Lambda_\rho{}^\alpha \Lambda_\sigma{}^\beta \mathrm{d}x_\alpha\mathrm{d}x_\beta
$$
$$
\implies  g^{\alpha\beta} = g^{\rho\sigma}\Lambda_\rho{}^\alpha \Lambda_\sigma{}^\beta 
$$
$$
\Lambda^\gamma{}_\beta \Lambda_\gamma{}^\alpha =g^{\gamma\mu} g_{\beta\nu} \Lambda_\mu{}^{\nu} \Lambda_\gamma{}^\alpha = g_{\beta\nu}g^{\nu\alpha} = \delta^\alpha_\beta
$$
## 3.2 SO(3)
令矩阵为 $J = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix}$，注意到 $J^2 = \begin{pmatrix} -1 & 0 \\ 0 & -1 \end{pmatrix} = -I_{2 \times 2}$，$J^3 = -J$，$J^4 = I_{2 \times 2}$，所以利用泰勒级数展开：
$$
e^{-\theta J} = I - \theta J + \frac{\theta^2}{2!} J^2 - \frac{\theta^3}{3!} J^3 + \dots = (\cos\theta) I - (\sin\theta) J = \begin{pmatrix} \cos\theta & \sin\theta \\ -\sin\theta & \cos\theta \end{pmatrix}
$$
所以
$$
\Lambda(\theta) = \begin{pmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & \cos\theta & \sin\theta \\ 0 & 0 & -\sin\theta & \cos\theta \end{pmatrix}
$$
因为 $[K, K] = 0$：
$$
\Lambda(\theta_1)\Lambda(\theta_2) = e^{-\theta_1 K} \circ e^{-\theta_2 K} = e^{-(\theta_1 + \theta_2)K + \frac{1}{2}[-\theta_1K, -\theta_2K] + \cdots} = \Lambda(\theta_1 + \theta_2)
$$
证明完毕。
## 3.3 $SO(1,3)^\uparrow$
令 $k_x = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}$，根据 $\Lambda_x = e^{\xi \Omega_x}$ 可以得到其 $Lie$ 群表示, 注意到 $k_x^2=I_{2\times 2}$ :
$$
 \begin{aligned}
\Lambda_{x}(\xi)  =\mathrm{e}^{\xi k_{x}}
&=\sum_{n=0}^{\infty} \frac{\xi^{n} k_{x}^{n}}{n!}=\sum_{n=0}^{\infty} \frac{\xi^{2 n}}{(2 n)!} \underbrace{k_{x}^{2 n}}_{=1}+\sum_{n=0}^{\infty} \frac{\xi^{2 n+1}}{(2 n+1)!} \underbrace{k_{x}^{2 n+1}}_{=k_{x}} \\
& =\left(\sum_{n=0}^{\infty} \frac{\xi^{2 n}}{(2 n)!}\right) I+\left(\sum_{n=0}^{\infty} \frac{\xi^{2 n+1}}{(2 n+1)!}\right) k_{x} \\ \\
& =\left(\begin{array}{cc}
\cosh (\xi) & 0 \\
0 & \cosh (\xi)
\end{array}\right)+\left(\begin{array}{cc}
0 & \sinh (\xi) \\
\sinh (\xi) & 0
\end{array}\right) \\ \\
& =\left(\begin{array}{cc}
\cosh (\xi) & \sinh (\xi) \\
\sinh (\xi) & \cosh (\xi)
\end{array}\right)
\end{aligned}
$$
即 :
$$
\Lambda_x(\phi) = \left(\begin{array}{cc}
\mathrm{ch} \xi & \mathrm{sh} \xi & &\\
\mathrm{sh} \xi & \mathrm{ch} \xi & & \\
& & 1 & \\
& & & 1
\end{array}\right)
$$
同样的逻辑，因为生成元矩阵 $\Omega$ 与其自身对易：
$$
\Lambda(\xi_1)\Lambda(\xi_2) = e^{-\xi_1 \Omega} e^{-\xi_2 \Omega} = e^{-(\xi_1 + \xi_2)\Omega} = \Lambda(\xi_1 + \xi_2)
$$
这也反映了沿同一方向的两个洛伦兹提升，其快度是直接相加的。

## 3.4 
对于 $O(1,3)$ 群元 $\Lambda_1, \Lambda_2$： 
$$
\Lambda^T g \Lambda = g
$$
- 验证群的封闭性。
$$
\Lambda^T g \Lambda = (\Lambda_1 \Lambda_2)^T g (\Lambda_1 \Lambda_2) 
= \Lambda_2^T (\Lambda_1^T g \Lambda_1) \Lambda_2
=\Lambda_2^T g \Lambda_2
=g
$$
所以 $\Lambda_1 \Lambda_2 \in O(3,1)$。  

- 验证群的逆元存在性。

首先确定 $\Lambda$ 是可逆的。对定义式 $\Lambda^T \eta \Lambda = \eta$ 两边取行列式：
$$
\det(\Lambda^T) \det(\eta) \det(\Lambda) = \det(\eta)
$$
由于 $\det(\eta) \neq 0$（其值为 $-1$），且 $\det(\Lambda^T) = \det(\Lambda)$，可得：
$$
(\det\Lambda)^2 = 1 \implies \det\Lambda = \pm 1
$$
行列式不为 0，说明 $\Lambda$ 必定存在逆矩阵 $\Lambda^{-1}$。  

在等式 $\Lambda^T \eta \Lambda = \eta$ 左边乘以 $(\Lambda^T)^{-1}$，右边乘以 $\Lambda^{-1}$：
$$
LHS = (\Lambda^T)^{-1} (\Lambda^T g \Lambda) \Lambda^{-1} = g = RHS =  (\Lambda^T)^{-1} g \Lambda^{-1} =(\Lambda^{-1})^T g \Lambda^{-1}
$$
因此 $\Lambda^{-1} \in O(3,1)$。
## 3.5 
### 3.5.1 
成立

1. 封闭性（乘法）：
    - 如果 $\Lambda_1, \Lambda_2 \in SO(1,3)^\uparrow$，那么他们的行列式均为 1，则 $\det(\Lambda_1\Lambda_2) = \det\Lambda_1 \det\Lambda_2 = 1 \times 1 = 1$。
    - 对于性质 $\Lambda^0{}_0 \ge 1$，两个正规变换的乘积依然是正规的（这可以通过柯西-施瓦茨不等式证明，见后续 [[电动26春/EMD_answer_phj/HW Answer/HW5 Answer#3.5.3 若 $ Lambda_1, Lambda_2$ 满足 $( Lambda_1) 0_0 ge 1$ 且 $( Lambda_2) 0_0 ge 1$，则它们的乘积 $ Lambda = Lambda_1 Lambda_2$ 的分量 $ Lambda 0_0$ 也必然满足 $ Lambda 0_0 ge 1$。\|#3.5.3 若 $ Lambda_1, Lambda_2$ 满足 $( Lambda_1) 0_0 ge 1$ 且 $( Lambda_2) 0_0 ge 1$，则它们的乘积 $ Lambda = Lambda_1 Lambda_2$ 的分量 $ Lambda 0_0$ 也必然满足 $ Lambda 0_0 ge 1$。]]）。
    - 因此，乘积依然属于该子集。
2. 逆元存在性：
    - 如果 $\det\Lambda = 1$，则 $\det(\Lambda^{-1}) = 1$。
    - 对于性质 $\Lambda^0{}_0 \ge 1$，$\Lambda_0{}^0 = g_{0\alpha}g^{0\beta}\Lambda^\alpha{}_\beta=g_{00}g^{00}\Lambda^0{}_0=\Lambda^0{}_0\geq1$。
    - 因此，逆元依然属于该子集。

### 3.5.2 

不成立。

除了包含单位矩阵的分支 $SO(1,3)^\uparrow$ 以外，其余三个子集均不构成群。比如，假设我们取子集 $\Sigma_i = \mathcal{P} SO(1,3)^\uparrow ,~( \det=-1, \Lambda^0{}_0 \ge 1 )$，选取 $\Lambda_1,\Lambda_2 \in \Sigma_i$，则 $\det \Lambda_1 = \det \Lambda_2 = -1$，它们的乘积 $\Lambda_1 \Lambda_2$ 的行列式为 $(-1) \times (-1) = 1$，落回了单位分支 $SO(1,3)^\uparrow$ 中。


#### 3.5.3 若 $\Lambda_1, \Lambda_2$ 满足 $(\Lambda_1)^0{}_0 \ge 1$ 且 $(\Lambda_2)^0{}_0 \ge 1$，则它们的乘积 $\Lambda = \Lambda_1 \Lambda_2$ 的分量 $\Lambda^0{}_0$ 也必然满足 $\Lambda^0{}_0 \ge 1$。
对于任何 $\Lambda \in O(3,1)$，取 $\Lambda^T g \Lambda = g$ 的00分量得：
$$
(\Lambda^0{}_0)^2 - \sum_{i=1}^3 (\Lambda^0{}_i)^2 = 1 \implies (\Lambda^0{}_0)^2 = 1 + \sum_{i=1}^3 (\Lambda^0{}_i)^2 \geq 1
$$
所以，可以定义对于 $SO(1,3)^\uparrow$ 群元，$\Lambda^0{}_0 \ge 1$ 。

令 $\vec{a}=(~(\Lambda_1)^0{}_1, (\Lambda_1)^0{}_2, (\Lambda_1)^0{}_3~)$，$\vec{b}=(~(\Lambda_2)^1{}_0, (\Lambda_2)^2{}_0, (\Lambda_2)^3{}_0~)$ 其模长满足：
$$
|\vec{a}|^2 = \sum_{i=1}^3 ((\Lambda_1)^0{}_i)^2 = ((\Lambda_1)^0{}_0)^2 - 1
,\quad
|\vec{b}|^2 = \sum_{i=1}^3 ((\Lambda_2)^i{}_0)^2 = ((\Lambda_2)^0{}_0)^2 - 1
$$
又，乘积矩阵 $\Lambda = \Lambda_1 \Lambda_2$ 的左上角元素为：
$$
\Lambda^0{}_0 = (\Lambda_1)^0{}_\mu (\Lambda_2)^\mu{}_0 = (\Lambda_1)^0{}_0 (\Lambda_2)^0{}_0 + \sum_{i=1}^3 (\Lambda_1)^0{}_i (\Lambda_2)^i{}_0=(\Lambda_1)^0{}_0 (\Lambda_2)^0{}_0 + \vec{a} \cdot \vec{b}
$$
根据柯西-施瓦茨不等式 $|\vec{a} \cdot \vec{b}| \le |\vec{a}| |\vec{b}|$，有：
$$
(\Lambda_1)^0{}_0 (\Lambda_2)^0{}_0 - \Lambda^0{}_0 \leq |\Lambda^0{}_0 - (\Lambda_1)^0{}_0 (\Lambda_2)^0{}_0 | = |\vec{a} \cdot \vec{b}| \leq |\vec{a}| |\vec{b}|
\implies
\Lambda^0{}_0 \ge (\Lambda_1)^0{}_0 (\Lambda_2)^0{}_0 - |\vec{a}| |\vec{b}|
$$

代入刚才的模长公式：  
$$
\Lambda^0{}_0 \ge (\Lambda_1)^0{}_0 (\Lambda_2)^0{}_0 - \sqrt{((\Lambda_1)^0{}_0)^2 - 1} \sqrt{((\Lambda_2)^0{}_0)^2 - 1}
\triangleq xy - \sqrt{x^2 - 1}\sqrt{y^2 - 1},\quad x, y \ge 1
$$
因为  
$$
\begin{align} 
(\sqrt{x^2 - 1}\sqrt{y^2 - 1})^2
&=
x^2y^2 - y^2 - x^2 +1 
\leq
x^2y^2 - 2xy +1
=
(xy-1)^2
\end{align}
$$
所以总是有 $xy \ge \sqrt{x^2 - 1}\sqrt{y^2 - 1} + 1$，因此 $\Lambda^0{}_0 \ge 1$。


### 3.5.3 
当一个粒子在它的瞬时共动参考系（Momentarily Comoving Reference Frame，MCRF）中感受到的固有加速度 $a$ 为常数时，它在实验室坐标系下的运动轨迹并不是抛物线，而是双曲线。  

首先，力 $F$ 定义为动量的变化率：
$$
F = \frac{\mathrm{d}p}{\mathrm{d} t}= \frac{\mathrm{d}}{\mathrm{d}t}(m\gamma v)
$$
在 MCRF 中，物体感受到的力满足由牛二定律 $F = ma$。所以有：
$$
ma = \frac{\mathrm{d}}{\mathrm{d}t}(m\gamma v) \implies a = \frac{\mathrm{d}}{\mathrm{d}t}(\gamma v)
$$
其中 $\frac{ \mathrm{d} v }{ \mathrm{d} t}$ 是实验系测得的加速度。设 $t=0$ 时，$v=0$，对运动方程进行积分： 
$$
\frac{v}{\sqrt{1-v^2/c^2}} = at \implies v(t) = \frac{at}{\sqrt{1 + (at/c)^2}}
$$
世界线即轨迹 $x(t)$。对速度 $v(t) = \frac{dx}{dt}$ 再次积分。设 $t=0$ 时，$x =0$：
$$
x(t)
= \int_0^t \frac{at'}{\sqrt{1 + (at'/c)^2}} \,\mathrm{d}t' = \frac{c^2}{a} \sqrt{1 + \left(\frac{at}{c}\right)^2} - \frac{c^2}{a}
$$
改写上述方程，可以得到 $x$ 和 $t$ 的双曲线关系：
$$
\left( x+\frac{c^2}{a} \right)^2 - (ct)^2 = \left(\frac{c^2}{a}\right)^2
$$
![zz_figure/Pasted image 20260406164447.png](/img/user/zz_figure/Pasted%20image%2020260406164447.png)
```desmos-graph
left=-1;right=10
top=10;bottom=-3
---
(x+2)^2 - y^2 =4
```


