---
{"dg-publish":true,"permalink":"/电动26春/EMD_answer_phj/HW Answer/HW7 Answer/","noteIcon":"default","created":"2026-04-24T17:44:57.258+08:00","updated":"2026-05-02T23:40:55.606+08:00"}
---


# 1 Relativistic Collision
## 1.1 
Refer to the total momentum conservation, one yield  
$$
\frac{Q}{c} = \gamma M v
$$
Similarly, energy's conserved  
$$
Q+mc^2 = \gamma Mc^2
$$
Thus  
$$
v = \frac{Qc}{Q+mc^2}
\tag{1}
$$
Using the relativistic invariant $E^2 = M^2c^4 + p^2c^2$, one can obtain that  
$$
(Q+mc^2)^2 = M^2c^4 + Q^2
$$
So the rest mass of the complex is  
$$
M = m\sqrt{1 + \frac{2Q}{mc^2}} \tag{2}
$$
## 1.2 
The atom recoils with momentum equal to the photon's momentum, $p_{atom} = p_{photon} = \frac{Q}{c}$, So energy's conservation yield that
$$
Mc^2 = Q + \sqrt{(mc^2)^2 + (p_{atom}c)^2} = Q + \sqrt{(mc^2)^2 + Q^2}
$$
Since $Mc^2 - mc^2 = Q_0$,
$$
Mc^2 = Q + \sqrt{(Mc^2 - Q_0)^2 + Q^2}
$$
Thus
$$
Q = Q_0 \left( 1 - \frac{Q_0}{2Mc^2} \right) 
$$
The photon energy $Q$ is slightly less than the lost rest energy $Q_0$ because a small portion of the energy must go into the kinetic energy of the recoiling atom.
# 2 Photon Rocket
## 2.1 
Use subscript ' $p$ ' to indicate the photons emitted, refer tor the energy and momentum conservation,  
$$
mc^2 = \gamma fm c^2 + E_{p},\quad P_p = \gamma fm v, \quad \text{with}~ E_p = P_p c
$$
Thus  
$$
f = [\gamma(1+\beta)]^{-1} = \sqrt{\frac{{1-\beta}}{1+\beta}}
$$
## 2.2 
$$
\gamma = 10  = \sqrt{\frac{1}{1-\beta^2}} \implies  f = \sqrt{\frac{1 - \sqrt{0.99}}{1 + \sqrt{0.99}}}  \approx 0.0501 
$$
Namely $\beta = \sqrt{0.99} \approx 1 \to f =  [\gamma(1+\beta)]^{-1} \approx \frac{1}{2\gamma}$.
## 2.3 
Because the rocket is effectively "consuming" its own mass to change velocity at each step, one can find the symmetry relation  
$$
f_{total} = f^4 \approx 6\times 10^{-6}
$$
# 3 Energy-Momentum Conservation
For a time interval in an arbitrary inertial frame, The problem say that we have the energy conservation as follows,
$$
\Delta P'^0 = \Delta P^0 = \frac{1}{c} [E(t+\Delta t) - E(t)] = 0
$$
So according to the Lorentz transformation in x-axis (x-boost):
$$
\Delta P^{0'} = \gamma \left( \Delta P^0 - \frac{v}{c} \Delta P^1 \right)  \implies \Delta P^1 =0
$$
By choosing frames moving along the $y$ and $z$ axes, one can similarly prove:
$$
\Delta P^2 = 0 \quad \text{and} \quad \Delta P^3 = 0
$$
# 4 Energy-Momentum Tensor of Pure Radiation
For free E.D. field in the problem, the energy-momentum tensor is  
$$
T^{\mu\nu} = \begin{bmatrix} \frac{1}{2}\epsilon_0(E^2 + c^2B^2) & \frac{1}{\mu_0 c} \boldsymbol{E} \times \boldsymbol{B} \\  \frac{1}{\mu_0 c} \boldsymbol{E} \times \boldsymbol{B} & \frac{1}{2}\epsilon_0(E^2 + c^2B^2)\delta_{ij} - \epsilon_0 (\boldsymbol{E}\boldsymbol{E} + c^2 \boldsymbol{B}\boldsymbol{B}) \end{bmatrix}
$$
where one find obviously 
$$
T^{\mu\nu} =  \begin{pmatrix} 1 & 0 & 0 & 1 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 1 & 0 & 0 & 1 \end{pmatrix} \epsilon_0 E_0^2 \cos^2 k(z - ct)
$$
For a wave traveling in the $z$ -direction, the momentum flux is also only in the $z$ -direction, so only $T^{zz}$ is none-zero in the maxwell stress tensor. 
# 5 Particle in the E.D. Field
## 5.1 
Since for $H = \int L_t \,\mathrm{d}t = \int L_\tau \,\mathrm{d}\tau$, where 
$$
\mathrm{d} \tau = \frac{\mathrm{d}t}{\gamma}
$$
One obtain that  
$$
L_t = \frac{L_\tau}{\gamma} = -mc^2\sqrt{1-\frac{v^2}{c^2} } + e\boldsymbol{A}\cdot\boldsymbol{v} - e\varphi
$$
substitute to the Euler-Lagrange equation $\frac{d}{dt} \frac{\partial L}{\partial \boldsymbol{v}} - \frac{\partial L}{\partial \boldsymbol{r}} =0$, one find  
$$
\frac{\mathrm{d}}{\mathrm{d}t} \gamma m \boldsymbol{v} = e \left( -\nabla \varphi - \frac{\partial \boldsymbol{A}}{\partial t} \right) + e\boldsymbol{v} \times \boldsymbol{B} = e\boldsymbol{E} + e\boldsymbol{v} \times \boldsymbol{B}
$$
## 5.2 
Use the Legendre Transformation and $\boldsymbol{p}=\gamma m \boldsymbol{v} = \boldsymbol{P} - e\boldsymbol{A}, \boldsymbol{P} = \frac{ \partial L }{ \partial \boldsymbol{v} }$, the Hamiltonian can be calculated as
$$
H = \boldsymbol{p} \cdot \boldsymbol{v} - L = \sqrt{c^2(\boldsymbol{P} - e\boldsymbol{A})^2 + (mc^2)^2} + e\varphi
$$
## 5.3 
For Non-relativistic approximation ($\beta \ll 1$), we also have $\gamma \beta \ll 1$. Thus
$$
L_t  = -mc^2\sqrt{1-\frac{v^2}{c^2} } + e\boldsymbol{A}\cdot\boldsymbol{v} - e\varphi \approx 
-mc^2 +
\frac{1}{2} mv^2 + e\boldsymbol{A}\cdot\boldsymbol{v} - e\varphi 
$$
$$
H = \sqrt{c^2(\boldsymbol{P} - e\boldsymbol{A})^2 + (mc^2)^2} + e\varphi \approx  mc^2 + \frac{(\boldsymbol{P} - e\boldsymbol{A})^2}{2m} + e\varphi 
$$
where the constant rest energy $mc^2$ can be ignored.
