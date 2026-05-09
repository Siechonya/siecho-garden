---
{"dg-publish":true,"permalink":"/电动26春/EMD_answer_phj/HW Answer/HW6 Answer/","noteIcon":"default","created":"2026-04-17T12:55:27.273+08:00","updated":"2026-05-09T17:21:20.522+08:00","dg-note-properties":{}}
---

[[电动26春/EMD_answer_phj/HW Answer/HW7 Answer\|HW7 Answer]]  

<iframe src="/img/user/%E7%94%B5%E5%8A%A826%E6%98%A5/EMD_answer_phj/HW/electrodynamics06(1).pdf" width="100%" height="900px" title="electrodynamics06(1)" style="border:1px solid #ccc;"></iframe>

# 1 《电磁学与电动力学》(下册)  
- 8.5,8.7~8.12
![zz_figure/Pasted image 20260417153115.png](/img/user/zz_figure/Pasted%20image%2020260417153115.png)  

>  注意到 $(\frac{\omega}{c}, \boldsymbol{k})$ 构成4-矢量，并且光满足 $kc=\omega$，接下来直接用 Lorentz Transformation 就可以得到相对论多普勒频移公式

![zz_figure/Pasted image 20260417154120.png](/img/user/zz_figure/Pasted%20image%2020260417154120.png)  
![zz_figure/Pasted image 20260417154144.png](/img/user/zz_figure/Pasted%20image%2020260417154144.png)  
![zz_figure/Pasted image 20260417154201.png](/img/user/zz_figure/Pasted%20image%2020260417154201.png)  
![zz_figure/Pasted image 20260417154219.png](/img/user/zz_figure/Pasted%20image%2020260417154219.png)  
![zz_figure/Pasted image 20260417154315.png](/img/user/zz_figure/Pasted%20image%2020260417154315.png)  



# 2 补充题  
## 2.1 
![zz_figure/Pasted image 20260417125943.png\|548](/img/user/zz_figure/Pasted%20image%2020260417125943.png)  

### 2.1.1 
利用电磁张量的两个不变量，有如下结论

![zz_figure/a71338f1b9749a2072f496af236c5603.jpg](/img/user/zz_figure/a71338f1b9749a2072f496af236c5603.jpg)

### 2.1.2 
掏出电磁场洛伦兹变换  
![zz_figure/8e80943b7d6db4b61d8ab1b66c38130b.jpg](/img/user/zz_figure/8e80943b7d6db4b61d8ab1b66c38130b.jpg)  
寻找一个速度 $\boldsymbol{v}$ 让E和B叉乘为0，假设  
$$
\boldsymbol{\beta} = \frac{ {\boldsymbol{E}\times \boldsymbol{B}}}{|\boldsymbol{E}\times \boldsymbol{B}|} \beta
$$
Lorentz Transformation变为  
$$
\boldsymbol{E}_\parallel = \boldsymbol{B}_\parallel = 0, \quad \mathbf{E}' = \gamma (\mathbf{E} + \boldsymbol{\beta} \times c\mathbf{B}) ,\quad
c\mathbf{B}' = \gamma (c\mathbf{B} - \boldsymbol{\beta} \times \mathbf{E})
$$
直接硬算得到  
$$
\boldsymbol{E'} \times c\boldsymbol{B'} = \boldsymbol{E} \times c\boldsymbol{B} - \boldsymbol{\beta} E^2 - \boldsymbol{\beta} c^2 B^2 + (\boldsymbol{\beta} \cdot \boldsymbol{E} \times c\boldsymbol{B} ) \boldsymbol{\beta} \triangleq 0 
$$
接下来代入 $\boldsymbol{\beta} = \frac{ {\boldsymbol{E}\times \boldsymbol{B}}}{|\boldsymbol{E}\times \boldsymbol{B}|} \beta$ 发现  
$$
|\boldsymbol{E}\times \boldsymbol{cB}| \beta^2 - (E^2 + c^2 B^2) \beta + |\boldsymbol{E}\times \boldsymbol{cB}|= 0 
$$
所以根据 $(E^2 + c^2 B^2)\geq |\boldsymbol{E}\times \boldsymbol{cB}|$，不难发现 $f(\beta) = |\boldsymbol{E}\times \boldsymbol{cB}| \beta^2 - (E^2 + c^2 B^2) \beta + |\boldsymbol{E}\times \boldsymbol{cB}|$ 在 $\beta \in [0,1]$ 为递减函数，只需要证明 $f(\beta_0)=0, \exists \beta_0\in [0,1]$ 即可，容易发现 $f(0) > 0 ,f(1)<0$，所以该 $\beta_0$ 存在，为  
$$
\beta_0 = \frac{(E^2 + c^2 B^2) - \sqrt{(E^2 + c^2 B^2)^2 - 4 |\boldsymbol{E}\times \boldsymbol{cB}|^2}}{2|\boldsymbol{E}\times \boldsymbol{cB}|}
$$

