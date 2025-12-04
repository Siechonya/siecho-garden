---
{"dg-publish":true,"permalink":"/理力25秋/Answer for HW9/","noteIcon":"default","created":"2025-11-22T14:34:14.410+08:00","updated":"2025-12-04T10:13:01.388+08:00"}
---

# 1 阻尼振动  
参见朗道 $\textsection 26$  

- 注意：鞠国兴的解少了一个齐次通解，即 $\ddot x+2\lambda \dot{x} + \omega_0^2 x =0$ 的解（分为欠阻尼、临界阻尼、过阻尼三种情形）。

![zz_figure/Pasted image 20251122194136.png](/img/user/zz_figure/Pasted%20image%2020251122194136.png)  
![zz_figure/Pasted image 20251122194154.png](/img/user/zz_figure/Pasted%20image%2020251122194154.png)
# 2 
如果没学过《数学物理方法》，不建议做这题。

对于微分算符 $\mathbf{L}=\frac{ \mathrm{d}^2  }{ \mathrm{d} t^2} + 2\lambda \frac{ \mathrm{d}  }{ \mathrm{d} t} + \omega_0^2$：
$$
\mathbf{L}[x] = \ddot{x} + 2\lambda \dot{x} + \omega_0^2 x = \frac{f}{m} \cos(\gamma t)
$$
根据基本解方法，格林函数 $G(t, t')$ 满足以下方程：
$$
\mathbf{L} G = \delta(t - t')
$$
在物理中 $t'$ 是激励出现(比如电荷、驱动力、热流)的时刻，$t$ 是系统响应(比如电磁场 $\boldsymbol{E}$ 的改变)的时刻，因此 $t\geq t'$。现在有两条路线可以求出格林函数：  

- <font color="#ff0000">方法一</font>：

齐次("homogeneous")方程 $\ddot{x} + 2\lambda \dot{x} + \omega_0^2 x = 0$ 的解为：
$$
x_h(t) = C_1 e^{-\lambda t} \cos(\omega_d t) + C_2 e^{-\lambda t} \sin(\omega_d t),\quad \text{with} ~~ \omega_{d} = \sqrt{\omega_0^2 - \lambda^2}
$$
注意，格林函数方法是不能求解齐次方程的，除非给定初始和边界条件。可以发现，在 $t > t'$ 时，格林函数满足的方程就是齐次方程，所以可以假设  
$$
G(t, t')= e^{-\lambda (t-t')} [A \cos(\omega_d (t-t')) + B \sin(\omega_d (t-t'))]
$$
因果律要求 $t\geq t'$，否则不存在物理解(格林函数为 0)，所以可以假设 $G(t=t'^{-},t'^{-})=0$ 得到 $A=0$。进一步要求格林函数为有界连续函数，所以  
$$
\int_{t'^{-}}^{t'^{+}} 2\lambda \dot{G} dt =\int_{t'^{-}}^{t'^{+}} \omega_0^2 G dt = 0
$$
$$
\Rightarrow\quad
\dot{G}(t'^{+}) - \dot{G}(t'^{-}) =
\int_{t'^{-}}^{t'^{+}} \left( \ddot{G} + 2\lambda \dot{G} + \omega_0^2 G \right) dt = \int_{t'^{-}}^{t'^{+}} \delta(t - t') dt = 1
$$
根据该跳跃条件得到  
$$
B=\frac{1}{\omega_d}
$$
于是：  
$$
G(t, t') = \frac{e^{-\lambda (t - t')}}{\omega_d} \sin(\omega_d (t - t'))
$$
- <font color="#ff0000">方法二</font>：Fourier 变换(标准方法)

对上式进行傅里叶变换，得到：  
$$
\left[ -\omega^2 + 2\lambda (i\omega) + \omega_0^2 \right] \tilde G(\omega) = e^{-i\omega t'}
\quad \Rightarrow \quad
\tilde G(\omega) = \frac{e^{-i\omega t'}}{\omega_0^2 - \omega^2 + i (2\lambda \omega)}
$$
然后傅里叶反变换，以得到格林函数：  
$$
G(t, t') = \frac{1}{2\pi} \int_{-\infty}^{\infty} G(\omega) e^{i\omega t} d\omega = \frac{1}{2\pi} \int_{-\infty}^{\infty} \frac{e^{i\omega (t - t')}}{\omega_0^2 - \omega^2 + i (2\lambda \omega)} d\omega
$$
这是一个复积分，被积函数存在奇点 $\omega_0^2 - \omega^2 + i (2\lambda \omega)=0$。假设系统处于欠阻尼 ($0<\lambda < \omega_0$) 状态，这是最常见的情况，那么得到的奇点都在上半复平面：  
$$
\omega_{1,2} = \pm\omega_d + i\lambda
$$
因果律要求 $t\geq t'$，所以根据留数定理：
$$
\begin{aligned} 
G(t, t') 
&= \frac{1}{2\pi} (2\pi i) \sum_{k=1}^2 \text{Res}(\omega_k) 
=
\frac{1}{2\pi} (2\pi i) \sum_{k=1}^2
\left. \frac{e^{i\omega (t - t')}}{\frac{d}{d\omega} ( \omega_0^2 - \omega^2 + i 2\lambda \omega)} \right|_{\omega=\omega_k} \\[6pt]
&\overset{一通爆算}{=}
\frac{e^{-\lambda (t - t')}}{\omega_d} \sin(\omega_d (t - t'))
\end{aligned}
$$
与方法一一致。特解(稳态解) $x_p(t)$ 由积分 $x_p(t) = \int_{-\infty}^{t} G(t, t') F(t') dt'$ 给出：  
$$
\begin{aligned} 
x_p(t) 
&=
\int_{-\infty}^{t} \frac{e^{-\lambda(t-t')}}{\omega_d} \sin(\omega_d (t-t')) \cdot \frac{f}{m} \cos(\gamma t') dt' 
\\[6pt] &\overset{二通爆算}{=}
\frac{f/m}{\sqrt{(\omega_0^2 - \gamma^2)^2 + (2\lambda \gamma)^2}} \cos(\gamma t - \phi)
\end{aligned}
$$
$$
滞后相位 :
\phi=\left\{\begin{array}{ll}
\arctan \left(\frac{2 \lambda \gamma}{\omega_{0}^{2}-\gamma^{2}}\right) & \left(\omega_{0}^{2}>\gamma^{2}\right) \\
\arctan \left(\frac{2 \lambda \gamma}{\omega_{0}^{2}-\gamma^{2}}\right)+\pi & \left(\omega_{0}^{2}<\gamma^{2}\right)
\end{array}\right.
$$
最终解为 $x = x_p + x_h$。  

> 格林函数的一些其他的例子参见 [[A_symmetry_自然界的对称性/杂记/Green Function\|Green Function]]。
# 3 强迫振动
参见朗道 $\textsection 22$ 习题 2  

##### 前置结论：  
![zz_figure/Pasted image 20251122200844.png](/img/user/zz_figure/Pasted%20image%2020251122200844.png)  
![zz_figure/Pasted image 20251122200907.png](/img/user/zz_figure/Pasted%20image%2020251122200907.png)  

##### 本题
![zz_figure/Pasted image 20251122200046.png](/img/user/zz_figure/Pasted%20image%2020251122200046.png)  
![zz_figure/Pasted image 20251122200101.png](/img/user/zz_figure/Pasted%20image%2020251122200101.png)



