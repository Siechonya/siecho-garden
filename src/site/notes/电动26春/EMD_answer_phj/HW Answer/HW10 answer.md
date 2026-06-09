---
{"dg-publish":true,"permalink":"/电动26春/EMD_answer_phj/HW Answer/HW10 answer/","noteIcon":"default","created":"2026-05-30T20:34:05.808+08:00","updated":"2026-06-09T16:30:25.897+08:00","dg-note-properties":{}}
---

[[电动26春/EMD_answer_phj/HW Answer/HW11 Answer\|HW11 Answer]]
# 1 textbook  
3.2, 3.6, 3.10, 3.11, 5.3  
![zz_figure/Pasted image 20260602174606.png](/img/user/zz_figure/Pasted%20image%2020260602174606.png)  
![zz_figure/Pasted image 20260602174624.png](/img/user/zz_figure/Pasted%20image%2020260602174624.png)  
![zz_figure/Pasted image 20260602174643.png](/img/user/zz_figure/Pasted%20image%2020260602174643.png)  
![zz_figure/Pasted image 20260602174656.png](/img/user/zz_figure/Pasted%20image%2020260602174656.png)  
![zz_figure/Pasted image 20260602174719.png](/img/user/zz_figure/Pasted%20image%2020260602174719.png)  
![zz_figure/Pasted image 20260602174737.png](/img/user/zz_figure/Pasted%20image%2020260602174737.png)  
![zz_figure/Pasted image 20260602174753.png](/img/user/zz_figure/Pasted%20image%2020260602174753.png)  

# 2 补充题  
![zz_figure/Pasted image 20260602175034.png](/img/user/zz_figure/Pasted%20image%2020260602175034.png)  

推迟势为，  
$$
\boldsymbol{A}=\boldsymbol{A}_z = \frac{\mu_0}{4\pi}\int_{-\infty}^{+\infty} \frac{I(t_r)}{R}\,\mathrm{d}z 
,\quad
R = \sqrt{s^2+z^2}
$$
代入 $I(t_r) = k t_r \cdot\Theta\left( t - \frac{\sqrt{s^2+z^2}}{c} \right)$ 得到，  
$$
A_z(s, t) = \frac{\mu_0 k}{4\pi} \cdot  \int_{-z_\max}^{z_{\max}} \left[ \frac{t}{\sqrt{s^2+z^2}} - \frac{1}{c} \right] \,\mathrm{d}z
,\quad
z_{\max} = \sqrt{(ct)^2 - s^2}
$$
$$
\implies
A_z(s, t) = \frac{\mu_0 k}{2\pi} \left[ t \operatorname{arccosh}\left( \frac{ct}{s} \right) - \frac{\sqrt{(ct)^2 - s^2}}{c} \right] \Theta(ct - s) 
$$
因为电势 $\varphi=const$，所以在 $ct>s$ 时电磁场为
$$
\boldsymbol{E} = -\frac{\partial A_z}{\partial t} \hat{z}= -\frac{\mu_0 k}{2\pi} \operatorname{arccosh}\left( \frac{ct}{s} \right) \hat{z}
$$
$$
\boldsymbol{B} = \nabla \times \boldsymbol{A} 
= -\frac{ \partial A_z }{ \partial s }\hat{\phi} 
= \frac{\mu_0 kt}{2\pi s} \sqrt{1 - \left(\frac{s}{ct}\right)^2} \,\hat{\phi}
$$
在 $s\ll ct$ 时，保留零阶项 $\sqrt{(ct)^2-s^2}  \approx ct$，由 $\ln\left( \frac{ct + \sqrt{(ct)^2-s^2}}{s} \right) = \operatorname{arccosh}\left( \frac{ct}{s} \right)$ 得到   
$$
A_z \approx \frac{\mu_0 k}{2\pi} \left[ t \ln\left(\frac{2ct}{s}\right) - t \right] = \frac{\mu_0 kt}{2\pi} \left[ \ln\left(\frac{2ct}{s}\right) - 1 \right]$$
$$
\boldsymbol{E}(s, t) \approx -\frac{\mu_0 k}{2\pi} \ln\left( \frac{2ct}{s} \right) \hat{z}
$$
$$
\boldsymbol{B}(s, t) \approx \frac{\mu_0 I(t)}{2\pi s} \hat{\phi}
$$

$$
t \ln\left( \frac{ct + \sqrt{(ct)^2-s^2}}{ct - \sqrt{(ct)^2-s^2}} \right) - 2\frac{\sqrt{(ct)^2 - s^2}}{c}
$$
