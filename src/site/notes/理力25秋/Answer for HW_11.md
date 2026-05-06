---
{"dg-publish":true,"permalink":"/理力25秋/Answer for HW_11/","noteIcon":"default","created":"2025-12-12T14:48:50.101+08:00","updated":"2025-12-18T10:55:13.247+08:00"}
---

# 1 正则变换  
#### (1)  
题为相空间的旋转变换  
$$
\begin{bmatrix} Q  \\  P \end{bmatrix}
= 
\begin{bmatrix} \cos t & -\sin t \\  \sin t & \cos t \end{bmatrix} \begin{bmatrix} q  \\  p \end{bmatrix}
$$
易证  
$$
[Q,P] = [q\cos t,p\cos t] + [-p\sin t, q \sin t] = [q, p ] = 1
$$
所以为正则变换。
#### (2)  
根据  
$$
p = -Q\sin t + P\cos t = -(q\cos t -p\sin t)\sin t + P\cos t
$$
得到  
$$
\frac{ \partial F_2(q,P) }{ \partial q } = p(q,P) = -q \tan t+ \frac{P}{\cos t}
$$
同理  
$$
\frac{ \partial F_2 }{ \partial P } = Q = \frac{q}{\cos t} - P\tan t
$$
采用折线积分，   
$$
F_2(q,P;t) = \int \left( -q \tan t+ \frac{P}{\cos t} \right)\mathrm{d}q + f(P,t) = -\frac{q^2}{2}\tan t + \frac{Pq}{\cos t} + f(P,t)
$$
$$
\frac{ \partial F_2 }{ \partial P } = \frac{q}{\cos t} + f'(P,t)_P = \frac{q}{\cos t} - P\tan t
$$
得到 $f(P,t) = -\frac{P^2}{2}\tan t +\varphi(t)$，即 $F_2(q,P;t)=-\frac{q^2 + P^2}{2}\tan t + \frac{Pq}{\cos t} +\varphi(t)$。则哈密顿函数变为  
$$
\tilde{H}(Q,P;t) = H + \frac{ \partial F_2 }{ \partial t } = \varphi'(t)
$$

#### (3)
正则方程  
$$
\dot{P} = -\frac{ \partial \tilde{H} }{ \partial Q } = 0, \ \ \dot{Q} = \frac{ \partial \tilde{H} }{ \partial P } = 0
$$
记 $Q(t)\equiv Q_0,P(t)\equiv P_0$，根据变换有：  
$$
q(t) = Q_0\cos t + P_0 \sin t, \ \ p(t) = -Q_0 \sin t + P_0 \cos t
$$
于是 $q(0)=Q_0,p(0)=P_0$，得到   
$$
q(t) = q(0)\cos t + p(0) \sin t, \ \ p(t) = -q(0) \sin t + p(0) \cos t
$$
# 2 保辛条件  
##### 常规方法
采用第一类生成函数 $F(q,Q,t)$，采用爱因斯坦求和约定，对于 $n$ 维情形：  
$$
[Q_\alpha,Q_\beta] = [P_\alpha,P_\beta]=0
$$
是易证的，这里略去，下面证明 $[Q_\alpha,P_\beta]=\delta_{\alpha\beta}$，已知
$$
P_\beta = -\frac{ \partial F }{ \partial Q_\beta }
$$
两边对 $p_\gamma$ 求导  
$$
\frac{ \partial P_\beta }{ \partial p_\gamma} = - \frac{ \partial^2 F }{ \partial Q_\beta\partial Q_\sigma }\frac{ \partial Q_\sigma }{ \partial q_\gamma }
$$
两边对 $q_\gamma$ 求导  
$$
\frac{ \partial P_\beta }{ \partial q_\gamma } = -\frac{ \partial^2 F }{ \partial Q_\beta \partial q_\gamma } -\frac{ \partial^2 F }{ \partial Q_\beta \partial Q_\sigma } \frac{ \partial Q_\sigma }{ \partial q_\gamma }
$$
于是  
$$
\begin{align} 
[Q_\alpha, P_\beta] &=
\frac{ \partial Q_\alpha }{ \partial  q_\gamma} \frac{ \partial P_\beta }{ \partial  p_\gamma} - \frac{ \partial Q_\alpha }{ \partial  p_\gamma} \frac{ \partial P_\beta }{ \partial  q_\gamma} \\[4pt]
&=
-\frac{ \partial Q_\alpha }{ \partial  q_\gamma} \frac{ \partial^2 F }{ \partial Q_\beta\partial Q_\sigma }\frac{ \partial Q_\sigma }{ \partial q_\gamma } + \frac{ \partial Q_\alpha }{ \partial  p_\gamma} \left( \frac{ \partial^2 F }{ \partial Q_\beta \partial q_\gamma } +\frac{ \partial^2 F }{ \partial Q_\beta \partial Q_\sigma } \frac{ \partial Q_\sigma }{ \partial q_\gamma } \right) \\[4pt]
&=
-\left( \frac{ \partial Q_\alpha }{ \partial  q_\gamma}\frac{ \partial Q_\sigma }{ \partial q_\gamma }-\frac{ \partial Q_\alpha }{ \partial  p_\gamma} \frac{ \partial Q_\sigma }{ \partial q_\gamma } \right)  \frac{ \partial^2 F }{ \partial Q_\beta\partial Q_\sigma } + \frac{ \partial Q_\alpha }{ \partial  p_\gamma}  \frac{ \partial^2 F }{ \partial Q_\beta \partial q_\gamma } \\[4pt]
&=
-[Q_\alpha,Q_\sigma]  \frac{ \partial^2 F }{ \partial Q_\beta\partial Q_\sigma } + \frac{ \partial Q_\alpha }{ \partial  p_\gamma}  \frac{ \partial^2 F }{ \partial Q_\beta \partial q_\gamma } \\[4pt]
&=
0+ \frac{ \partial Q_\alpha }{ \partial  p_\gamma}  \frac{ \partial p_\gamma }{ \partial Q_\beta } \\[4pt]
&=
\delta_{\alpha\beta}
\end{align}
$$
成立。  

##### 微分形式
题目给出单位矩阵的辛形式保持不变：  
$$
\Omega = dp_1 \wedge dq_1 + dp_2 \wedge dq_2 =  dP_1 \wedge dQ_1 + dP_2 \wedge dQ_2 = \Omega'
$$
那么  
$$
\begin{align} 
\Omega \wedge \Omega 
&= (dp_1 \wedge dq_1 + dp_2 \wedge dq_2) \wedge (dp_1 \wedge dq_1 + dp_2 \wedge dq_2)  \\[4pt]
&=
 (dp_1 \wedge dq_1) \wedge (dp_1 \wedge dq_1) + (dp_1 \wedge dq_1) \wedge (dp_2 \wedge dq_2) + (dp_2 \wedge dq_2) \wedge (dp_1 \wedge dq_1) + (dp_2 \wedge dq_2) \wedge (dp_2 \wedge dq_2) \\[4pt]
&=
(dp_1 \wedge dq_1) \wedge (dp_2 \wedge dq_2) + (dp_2 \wedge dq_2) \wedge (dp_1 \wedge dq_1)\\[4pt]
&=
2 \cdot (dp_1 \wedge dq_1) \wedge (dp_2 \wedge dq_2) \\[4pt]
&=
2d\tau
\end{align}
$$
即相空间体积元也保持不变，注意到  
$$
dQ_1 \wedge dQ_2 \wedge dP_1 \wedge dP_2 = \left| \frac{\partial (Q_1, Q_2, P_1, P_2)}{\partial (q_1, q_2, p_1, p_2)} \right| \cdot dq_1 \wedge dq_2 \wedge dp_1 \wedge dp_2
$$
所以雅可比行列式为 1：  
$$
\left| \frac{\partial (Q_1, Q_2, P_1, P_2)}{\partial (q_1, q_2, p_1, p_2)} \right| = 1
$$

# 3 嗯算题
大二时写过这题。用直角坐标算会比我的计算更简单，

![zz_figure/note_理力A_27_1764934766457.png](/img/user/zz_figure/note_%E7%90%86%E5%8A%9BA_27_1764934766457.png)
![zz_figure/note_理力A_28_1764934773156.png](/img/user/zz_figure/note_%E7%90%86%E5%8A%9BA_28_1764934773156.png)













