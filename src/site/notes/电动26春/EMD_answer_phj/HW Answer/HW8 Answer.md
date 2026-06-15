---
{"dg-publish":true,"permalink":"/电动26春/EMD_answer_phj/HW Answer/HW8 Answer/","noteIcon":"default","created":"2026-06-15T09:49:24.753+08:00","updated":"2026-05-25T21:05:55.867+08:00","dg-note-properties":{}}
---

[[电动26春/EMD_answer_phj/HW Answer/HW9 Answer\|HW9 Answer]]

# 1 textbook  
![zz_figure/Pasted image 20260521161419.png](/img/user/zz_figure/Pasted%20image%2020260521161419.png)  
![zz_figure/Pasted image 20260521161436.png](/img/user/zz_figure/Pasted%20image%2020260521161436.png)  
![zz_figure/Pasted image 20260521161507.png](/img/user/zz_figure/Pasted%20image%2020260521161507.png)  
![zz_figure/Pasted image 20260521161522.png](/img/user/zz_figure/Pasted%20image%2020260521161522.png)  

# 2 补充题  
## 2.1 
拉格朗日方程是
$$
\underset{-\boldsymbol{J} + {\nabla \times \frac{\boldsymbol{B}}{2\mu_0}}}{\underbrace{\frac{ \partial \mathcal{L} }{ \partial \boldsymbol{B} }} }
-\underset{\epsilon_0\partial_t \boldsymbol{E}}{\underbrace{\frac{ \partial  }{ \partial t }\left( \frac{ \partial \mathcal{L} }{ \partial (\partial_t \boldsymbol{B}) } \right)} } 
-\underset{-\frac{{\nabla \times \boldsymbol{B}}}{2\mu_0}}{\underbrace{\partial_i \left( \frac{ \partial \mathcal{L} }{ \partial (\partial_i \boldsymbol{B}) } \right)}} 
=0
$$
$$
\underset{\epsilon_0 \partial_t\boldsymbol{B}+\frac{\epsilon_0}{2}{\nabla \times {\boldsymbol{E}}}}{\underbrace{\frac{ \partial \mathcal{L} }{ \partial \boldsymbol{E} }} }
-\underset{0}{\underbrace{\frac{ \partial  }{ \partial t }\left( \frac{ \partial \mathcal{L} }{ \partial (\partial_t \boldsymbol{E}) } \right)} } 
-\underset{-  {\frac{\epsilon_0}{2}{\nabla \times {\boldsymbol{E}}}}  }{\underbrace{\partial_i \left( \frac{ \partial \mathcal{L} }{ \partial (\partial_i \boldsymbol{E}) } \right)}} 
=0
$$
得到两个旋度方程  
$$
\nabla \times \boldsymbol{E} = - \frac{ \partial \boldsymbol{B} }{ \partial t }
$$
$$
\nabla \times \boldsymbol{B} = \mu_0 \boldsymbol{J} + \frac{1}{c^2} \frac{ \partial \boldsymbol{E} }{ \partial t }
$$
## 2.2 
参见 chapter 4-E 节的 ppt，拉格朗日方程是  
$$
\underset{-\frac{1}{2}\kappa^2\varphi}{\underbrace{\frac{\partial \mathcal{L}}{\partial \varphi^*} } } 
-\underset{-\frac{1}{2}\partial^\mu\varphi}{\underbrace{\partial_\mu \left( \frac{\partial \mathcal{L}}{\partial (\partial_\mu \varphi^*)} \right) } } 
= 0
,\quad \phi = \varphi, \varphi^*
$$
取 $\phi=\varphi^*$ 得到 $\varphi$ 的 Klein-Gordon 方程  
$$
\left( \Box - \kappa^2 \right) \varphi = 0
$$
代入正则能动张量密度  
$$
T^{\mu\nu} = g^{\mu\nu}\mathcal{L} 
-\partial^\mu\varphi   \underset{-\frac{1}{2}\partial^\nu \varphi^*}{\underbrace{\frac{ \partial \mathcal{L} }{ \partial (\partial_\nu \varphi)}} }   
-\partial^\mu \varphi^* \underset{-\frac{1}{2}\partial^\nu\varphi}{\underbrace{\frac{ \partial \mathcal{L} }{ \partial (\partial_\nu \varphi^*)}} } 
$$
得到
$$
T^{\mu\nu} 
=- \frac{1}{2} g^{\mu\nu} \left( \partial_\rho \varphi^* \partial^\rho \varphi + \kappa^2 \varphi^* \varphi \right) +  \frac{1}{2} \left( \partial^\mu \varphi \partial^\nu \varphi^* + \partial^\mu \varphi^* \partial^\nu \varphi \right) 
$$

