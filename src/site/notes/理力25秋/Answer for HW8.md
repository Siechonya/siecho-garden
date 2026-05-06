---
{"dg-publish":true,"permalink":"/理力25秋/Answer for HW8/","noteIcon":"default","created":"2025-12-01T13:42:45.034+08:00","updated":"2025-11-27T18:20:56.775+08:00"}
---

# 1 双摆  
- 参见朗道力学 $\textsection 23$ 习题 2 
## 1.1 (1)
选取系统为 $m_{1}$ 和 $m_{2}$ ，它有两个自由度，选取广义坐标为 $\varphi_{1}$ 和 $\varphi_{2}$ 。有质点 $m_{1}$ 和 $m_{2}$ 的坐标分别为  $\left(l_{1} \sin \varphi_{1}, l_{1} \cos \varphi_{1}\right),\left(l_{1} \sin \varphi_{1}+\right. \left.l_{2} \sin \varphi_{2}, l_{1} \cos \varphi_{1}+l_{2} \cos \varphi_{2}\right)$  。由此可得 $m_{1}$ 的动能为
$$
T_{1}=\frac{1}{2} m_{1} l_{1}^{2} \dot{\varphi}_{1}^{2}
$$
$m_{2}$ 的动能为
$$
\begin{aligned} 
T_{2}
&=\frac{1}{2} m_{2}\left[l_{1}^{2} \dot{\varphi}_{1}^{2}+l_{2}^{2} \dot{\varphi}_{2}^{2}+2 l_{1} l_{2} \dot{\varphi}_{1} \dot{\varphi}_{2} \cos \left(\varphi_{1}-\varphi_{2}\right)\right]
\\
&\approx \frac{1}{2} m_{2}\left(l_{1}^{2} \dot{\varphi}_{1}^{2}+l_{2}^{2} \dot{\varphi}_{2}^{2}+2 l_{1} l_{2} \dot{\varphi}_{1} \dot{\varphi}_{2}\right)
\\[6pt]
\Rightarrow\quad
T&=T_{1}+T_{2}=\frac{1}{2}\left(m_{1}+m_{2}\right) l_{1}^{2} \dot{\varphi}_{1}^{2}+\frac{1}{2} m_{2} l_{2}^{2} \dot{\varphi}_{2}^{2}+m_{2} l_{1} l_{2} \dot{\varphi}_{1} \dot{\varphi}_{2}
\end{aligned}
$$
于是 $T$ 的惯性系数矩阵 $\boldsymbol{M}$ 为，
$$
\boldsymbol{M}=\left(\begin{array}{ll}
\left(m_{1}+m_{2}\right) l_{1}^{2} & m_{2} l_{1} l_{2} \\
m_{2} l_{1} l_{2} & m_{2} l_{2}^{2}
\end{array}\right)
$$
系统的势能为
$$
\begin{aligned} 
U&=-m_{1} g l_{1} \cos \varphi_{1}-m_{2} g\left(l_{1} \cos \varphi_{1}+l_{2} \cos \varphi_{2}\right)
\\
&\approx \frac{1}{2}\left(m_{1}+m_{2}\right) g l_{1} \varphi_{1}^{2}+\frac{1}{2} m_{2} g l_{2} \varphi_{2}^{2}-\left(m_{1} g l_{1}+m_{2} g l_{1}+m_{2} g l_{2}\right)
\end{aligned}
$$
于是 $U$ 的刚性系数矩阵 $U$ 为
$$
\boldsymbol{U}=\left(\begin{array}{ll}
\left(m_{1}+m_{2}\right) g l_{1} & 0 \\
0 & m_{2} g l_{2}
\end{array}\right)
$$
拉格朗日函数为
$$
L=  \frac{1}{2}\left(m_{1}+m_{2}\right) l_{1}^{2} \dot{\varphi}_{1}^{2}+\frac{1}{2} m_{2} l_{2}^{2} \dot{\varphi}_{2}^{2}+m_{2} l_{1} l_{2} \dot{\varphi}_{1} \dot{\varphi}_{2}- 
\frac{1}{2}\left(m_{1}+m_{2}\right) g l_{1} \varphi_{1}^{2}-\frac{1}{2} m_{2} g l_{2} \varphi_{2}^{2}
$$
其中略去了势能中对运动无影响的常数项．  
## 1.2 (2)
将 $L$ 代入拉格朗日方程得系统的运动微分方程为
$$
\begin{array}{r}
\left(m_{1}+m_{2}\right) l_{1} \ddot{\varphi}_{1}+m_{2} l_{2} \ddot{\varphi}_{2}+\left(m_{1}+m_{2}\right) g \varphi_{1}&=0 \\
l_{1} \ddot{\varphi}_{1}+l_{2} \ddot{\varphi}_{2}+g \varphi_{2}&=0
\end{array}
$$
设方程的解为 $\varphi_{1}=A_{1} \mathrm{e}^{\mathrm{i} \omega t}, \quad \varphi_{2}=A_{2} \mathrm{e}^{\mathrm{i} \omega t}$，将它们代入运动微分方程可以得到
$$
\begin{array}{r}
A_{1}\left(m_{1}+m_{2}\right)\left(g-l_{1} \omega^{2}\right)-A_{2} m_{2} l_{2} \omega^{2}&=0 \\
-A_{1} l_{1} \omega^{2}+A_{2}\left(g-l_{2} \omega^{2}\right)&=0
\end{array}
$$
特征方程为上述方程组的系数行列式等于零，或者 $\operatorname{det}\left(\boldsymbol{U}-\omega^{2} \boldsymbol{M}\right)=0$ ，即
$$
\left|\begin{array}{cc}
\left(m_{1}+m_{2}\right)\left(g-l_{1} \omega^{2}\right) & -m_{2} l_{2} \omega^{2} \\
-m_{2} l_{1} \omega^{2} & m_{2} \left(g-l_{2} \omega^{2}\right)
\end{array}\right|=0
$$
由此可解得本征频率为
$$
\begin{aligned}
\omega_{1,2}^{2}= & \frac{g}{2 m_{1} l_{1} l_{2}} \times 
 \left\{\left(m_{1}+m_{2}\right)\left(l_{1}+l_{2}\right) \pm \sqrt{\left(m_{1}+m_{2}\right)\left[\left(m_{1}+m_{2}\right)\left(l_{1}+l_{2}\right)^{2}-4 m_{1} l_{1} l_{2}\right]}\right\}
\end{aligned}
$$
将上式再代入运动微分方程可以得到 $A_2 = \alpha_{1,2} A_1$，$\alpha$ 大概率是一坨丑陋的常数式子(这里偷个懒)，它们简单写是：
$$
\alpha_1 =  \frac{l_{1} \omega_{1}^{2}}{g-l_{2} \omega_{1}^{2}} ,\quad
\alpha_2 = \frac{l_{1} \omega_{2}^{2}}{g-l_{2} \omega_{2}^{2}} 
$$
于是  
$$
\begin{bmatrix} \varphi_1 \\  \varphi_2 \end{bmatrix}
=
\begin{bmatrix} A_1|_{\omega_1} & A_1|_{\omega_2} \\  A_2|_{\omega_1} & A_2|_{\omega_2} \end{bmatrix}
\begin{bmatrix}  \mathrm{e}^{\mathrm{i} \omega_1 t} \\   \mathrm{e}^{\mathrm{i} \omega_2 t} \end{bmatrix}_{real}
= 
\begin{bmatrix} A_1|_{\omega_1} & A_1|_{\omega_2} \\  A_2|_{\omega_1} & A_2|_{\omega_2} \end{bmatrix}
\begin{bmatrix}  \cos( \omega_1 t + \phi_1) \\   \cos( \omega_2 t + \phi_2) \end{bmatrix}
$$
记 $C_1 = A_1|_{\omega_1}, C_2 = A_1|_{\omega_2}$，上式变为  
$$
\begin{bmatrix} \varphi_1 \\  \varphi_2 \end{bmatrix}
= 
\begin{bmatrix} C_1 & C_2 \\  \alpha_1 C_1 &  \alpha_2 C_2 \end{bmatrix}
\begin{bmatrix}  \cos( \omega_1 t + \phi_1) \\   \cos( \omega_2 t + \phi_2) \end{bmatrix}
$$
## 1.3 (3)  
反解上式得到简振坐标   
$$
\begin{bmatrix} Q_1 \\  Q_2 \end{bmatrix}
= 
\begin{bmatrix}  C_1 \cos( \omega_1 t + \phi_1) \\   C_2 \cos( \omega_2 t + \phi_2) \end{bmatrix}
=
\begin{bmatrix} 1 & 1 \\  \alpha_1  &  \alpha_2  \end{bmatrix}^{-1}
\begin{bmatrix} \varphi_1 \\  \varphi_2 \end{bmatrix}
=
\frac{1}{\alpha_2 - \alpha_1}\begin{bmatrix} \alpha_2 & -1 \\  -\alpha_1  &  1  \end{bmatrix}
\begin{bmatrix} \varphi_1 \\  \varphi_2 \end{bmatrix}
$$
对于 $l_1=l_2=l,m_1=m_2=m$ 的情况会很简单，变成  
$$
\begin{bmatrix} Q_1 \\  Q_2 \end{bmatrix}
=
\frac{\sqrt{2}}{4}\begin{bmatrix} \sqrt 2 & -1 \\  \sqrt 2  &  1  \end{bmatrix}
\begin{bmatrix} \varphi_1 \\  \varphi_2 \end{bmatrix}
$$
# 2 耦合谐振子  
$L=\frac{1}{2} m_{1} \dot{x}^{2}-\frac{1}{2} k_{1} x^{2}+\frac{1}{2} m_{2} \dot{y}^{2}-\frac{1}{2} k_{2} y^{2}+\alpha x y$ 代入拉格朗日方程得到  
$$
\begin{aligned} 
m_1 \ddot{x} + k_1 x - \alpha y &=0 \\
m_2 \ddot{y} + k_2 y - \alpha x &=0
\end{aligned}
$$
代入 $x,y=a,b \times \cos (\omega t)$ 得到系数方程  
$$
\begin{aligned} 
(-m_1 \omega^2 + k_1)a - \alpha b &= 0 \\
- \alpha a + (-m_2 \omega^2 + k_2)b & = 0
\end{aligned}
$$
得到久期方程  
$$
\left|\begin{array}{cc}
-m_1 \omega^2 + k_1 & -\alpha \\
- \alpha  & -m_2 \omega^2 + k_2
\end{array}\right|=0
$$
解得本征频率  
$$
\begin{aligned} 
\omega_{1,2}^2 
&= \frac{m_1k_2+m_2k_1 \pm \sqrt{(m_1k_2+m_2k_1)^2 - 4m_1m_2(k_1k_2 - \alpha^2)}}{2m_1m_2} \\[4pt]
&= \frac{m_1k_2+m_2k_1 \pm \sqrt{(m_1k_2-m_2k_1)^2 + 4 \alpha^2m_1m_2  }}{2m_1m_2}
\end{aligned}
$$
将上式代回系数方程得到， $b = \beta_{1,2} \cdot a$，其中  
$$
\beta_{1,2} = \frac{{-m_1 \omega_{1,2}^2 + k_1}}{\alpha} = - \frac{m_1k_2-m_2k_1 \pm \sqrt{(m_1k_2-m_2k_1)^2 + 4m_1m_2 \alpha^2}}{2m_2 \alpha}
$$
于是  
$$
\begin{bmatrix} x \\  y \end{bmatrix}
=
\begin{bmatrix} a|_{\omega_1} & a|_{\omega_2} \\  b|_{\omega_1} & b|_{\omega_2} \end{bmatrix}
\begin{bmatrix}  \cos( \omega_1 t + \phi_1) \\   \cos( \omega_2 t + \phi_2) \end{bmatrix}
$$
记 $C_1 = a|_{\omega_1}, C_2 = a|_{\omega_2}$，上式变为  
$$
\begin{bmatrix} x \\ y \end{bmatrix}
= 
\begin{bmatrix} C_1 & C_2 \\  \beta_1 C_1 &  \beta_2 C_2 \end{bmatrix}
\begin{bmatrix}  \cos( \omega_1 t + \phi_1) \\   \cos( \omega_2 t + \phi_2) \end{bmatrix}
$$
反解上式得到简振坐标  
$$
\begin{bmatrix} Q_1 \\  Q_2 \end{bmatrix}
= 
\begin{bmatrix}  C_1 \cos( \omega_1 t + \phi_1) \\   C_2 \cos( \omega_2 t + \phi_2) \end{bmatrix}
=
\begin{bmatrix} 1 & 1 \\  \beta_1  &  \beta_2  \end{bmatrix}^{-1}
\begin{bmatrix} x \\  y \end{bmatrix}
=
\frac{1}{\beta_2 - \beta_1}\begin{bmatrix} \beta_2 & -1 \\  -\beta_1  &  1  \end{bmatrix}
\begin{bmatrix} x \\  y \end{bmatrix}
\propto
\begin{bmatrix}  \frac{{-m_1 \omega_{2}^2 + k_1}}{\alpha} & -1 \\  \frac{{m_1 \omega_{1}^2 - k_1}}{\alpha}  &  1  \end{bmatrix}
\begin{bmatrix} x \\  y \end{bmatrix}
$$
对于 $k_1=k_2=k,m_1=m_2=m$ 的情况会很简单，变成  
$$
\begin{bmatrix} Q_1 \\  Q_2 \end{bmatrix}
=
\frac{\sqrt{2}}{2}\begin{bmatrix} 1 & 1 \\  1  &  -1  \end{bmatrix}
\begin{bmatrix} x \\  y \end{bmatrix}
$$
# 3 平面谐振子  
- 参见朗道力学 $\textsection 23$ 习题3 
-  或 [[理力25秋/Answer for HW7#(a) 线性力 $ vec{F}=-k vec{r}$, $U= frac{1}{2}kr 2$\|HW7-1 T3 (a)]]  
- 或令上一题中的 $\alpha=m_2=0$ .

朗道：

![zz_figure/Pasted image 20251115171259.png](/img/user/zz_figure/Pasted%20image%2020251115171259.png)
![zz_figure/Pasted image 20251115171308.png](/img/user/zz_figure/Pasted%20image%2020251115171308.png)
![zz_figure/Pasted image 20251115171324.png](/img/user/zz_figure/Pasted%20image%2020251115171324.png)  


