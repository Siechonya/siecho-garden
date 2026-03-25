---
{"dg-publish":true,"permalink":"/理力25秋/Answer for HW_10/","noteIcon":"default","created":"2025-12-12T14:48:00.180+08:00","updated":"2025-12-30T11:55:06.870+08:00"}
---



# 1 正则变换
> 本题其实可以看作第二类正则变换，母函数是  
> $$
F_2(q_\alpha, p_\alpha', t) = \sum_\alpha q_\alpha p'_\alpha - f(q_\alpha, t)
$$

采用爱因斯坦求和约定：  

- 广义动量
$$
p'_\alpha = \frac{ \partial L' }{ \partial \dot{q_\alpha} } 
= \frac{ \partial L }{ \partial \dot{q_\alpha} } + \frac{ \partial \dot{{f}} }{ \partial \dot{q_\alpha} } 
= p_\alpha + \frac{ \partial f }{ \partial q_\alpha }
\tag{1}
$$
- 哈密顿量  
$$
\begin{align} 
H'(p'_\alpha,q_\alpha)  
&= p'_\alpha \dot{q_\alpha} - L' \\[4pt]
&= H + \frac{ \partial f }{ \partial q_\alpha } \dot{q_\alpha} - \frac{ \mathrm{d} f}{ \mathrm{d} t}  \\[4pt]
&=
H(p_\alpha,q_\alpha) - \frac{ \partial f }{ \partial t } \tag{2}
\\[4pt]
&\overset{\triangle}{=} H'(p_\alpha + \frac{ \partial f }{ \partial q_\alpha },q_\alpha)
\end{align}
$$
- 哈密顿正则方程  

证明 $\dot q_\alpha' = \frac{ \partial H' }{ \partial p'_\alpha }  \longleftrightarrow \dot q_\alpha = \frac{ \partial H}{ \partial p_\alpha }$：  
$$
\begin{align}
\dot{q}'_\alpha
= \dot{q}_\alpha
&= \frac{ \partial H' }{ \partial p'_\alpha }|_{q}\\[4pt]
&= \frac{ \partial H' }{ \partial p_\beta }\frac{ \partial p_\beta }{ \partial p'_\alpha }|_{q}
=\frac{ \partial H' }{ \partial p_\beta }\delta_{\alpha\beta} = \frac{ \partial H' }{ \partial p_\alpha }
\\[4pt]
{\small \color{gray}代入(2)式\to}&=
\frac{ \partial H }{ \partial p_\alpha }  - \frac{ \partial }{ \partial p_\alpha } \frac{ \partial f(q_\alpha,t) }{ \partial t } \\[4pt]
&=
\frac{ \partial H }{ \partial p_\alpha } 
\tag{3}
\end{align}
$$
证明 $-\dot{p}'_\alpha = \frac{ \partial H' }{ \partial q'_\alpha } \longleftrightarrow -\dot{p}_\alpha = \frac{ \partial H}{ \partial q_\alpha }$：    

注意到  
$$
p'_\alpha = p_\alpha + \frac{ \partial f }{ \partial q_\alpha }
\quad\Rightarrow\quad
\frac{ \partial p'_\beta }{ \partial q_\alpha } = \frac{ \partial^2 f }{ \partial q_\alpha \partial q_\beta }
\tag{4}
$$
$$
\frac{ \partial H'(p,q) }{ \partial q_\alpha }|_{p} =
\frac{ \partial H' (p',q)}{ \partial q_\alpha }|_{p'} +   \frac{ \partial H'(p',q) }{ \partial p'_\beta } \frac{ \partial p'_\beta }{ \partial q_\alpha }|_{p}
\tag{5}
$$
于是
$$
\begin{align}
-\dot{p}'_\alpha = -\dot p_\alpha -\frac{ \mathrm{d}  }{ \mathrm{d} t} \frac{ \partial f }{ \partial q_\alpha }
&= \frac{ \partial H' }{ \partial q_\alpha }|_{p'}\\[4pt]
{\small \color{gray}代入(5)式\to}&= \frac{ \partial H' }{ \partial q_\alpha }|_{p} - \frac{ \partial H' }{ \partial p'_\beta } \frac{ \partial p'_\beta }{ \partial q_\alpha }|_{p}
\\[4pt]
{\small \color{gray}代入(2)式\to}&=
\frac{ \partial H }{ \partial q_\alpha }  - \frac{ \partial }{ \partial q_\alpha } \frac{ \partial f }{ \partial t } - \frac{ \partial H' }{ \partial p'_\beta } \frac{ \partial p'_\beta }{ \partial q_\alpha } \\[4pt]
{\small \color{gray}代入(3)(4)式\to}&=
\frac{ \partial H }{ \partial q_\alpha } - \underset{=\frac{ \mathrm{d}  }{ \mathrm{d} t} \frac{ \partial f }{ \partial q_\alpha }}{\underbrace{\left( \frac{ \partial }{ \partial q_\alpha } \frac{ \partial f }{ \partial t } + {\color{orange}\dot{q}_\beta\frac{ \partial^2 f }{ \partial q_\alpha \partial q_\beta }} \right)}} \\[4pt]
\end{align}
$$
于是
$$
\frac{ \partial H }{ \partial q_\alpha }=-\dot p_\alpha
\tag{5}
$$
成立，反之同理。  

# 2 球面摆  
#### (1)  
拉氏量
$$
L(\theta,\phi; \dot{\theta},\dot{\phi}) = T -V = \frac{1}{2}ml^2 (\dot{\theta}^2 + \sin^2\theta\dot{\phi}^2 ) + mgl\cos\theta
$$
得到广义动量  
$$
p_\theta = \frac{ \partial L }{ \partial \dot\theta } = ml^2\dot{\theta}
,\quad
p_\phi = \frac{ \partial L }{ \partial \dot\phi } = ml^2\sin^2\theta\dot{\phi}
$$
勒让德变换得到    
$$
H(\theta, \phi; p_\theta, p_\phi) = \theta p_\theta + \phi p_\phi - L
=
\frac{1}{2m}\left( \frac{p_\theta^2}{l^2} + \frac{p_\phi^2}{l^2\sin^2\theta}  \right) - mgl\cos\theta
\tag{6}
$$
#### (2)  
$$
\dot p_\phi = -\frac{ \partial H }{ \partial \phi } = 0
\quad\Rightarrow\quad
\sin^2\theta\dot{\phi} = \text{const}
\tag{7}
$$
$$
\dot p_\theta = -\frac{ \partial H }{ \partial \theta } = -\frac{p_\phi^2\cos\theta}{ml^2\sin^3\theta} + mgl\sin\theta
\quad\Rightarrow\quad
\ddot{\theta} - \dot{\phi}^2\cos\theta\sin\theta - \frac{g}{l}\sin\theta = 0
\tag{8}
$$
#### (3)  
自由度为 $s=2$ ，对于可积系统，运动积分有 $s$ 个<sup>[1]</sup>，即 $H$ ($\because$ 不显含 $t$) 和 $p_\theta$

参见：
> [1] V. I. Arnold, _Mathematical Methods of Classical Mechanics_, chapter 10, §49 :  
> 
> In order to integrate a system of $2n$ ordinary differential equations, we must know $2n$ first integrals. It turns out that if we are given a canonical system of differential equations, it is often sufficient to know only $n$ first integrals-each of them allows us to reduce the order of the system not just by one, but by two.  
> 
> Two functions F 1 and F 2 on a symplectic manifold are in involution if their Poisson bracket is equal to zero. Liouville proved that if, in a system with n degrees of freedom (i.e., with a 2n-dimensional phase space), n independent first integrals in involution are known, then the system is integrable by quadratures.

