---
{"dg-publish":true,"permalink":"/_Documents/references/1-3 Appendix C/","noteIcon":"default","created":"2025-08-09T21:45:19.054+08:00","updated":"2025-08-14T21:49:25.009+08:00"}
---

The momentum diffusion rate can be transformed into an energy diffusion rate and thus used to obtain the timescale for energization. The conversion can be obtained from the definition of the diffusion coefficients in the Fokker-Planck equation  
$$
D_{pp} = \frac{\langle (\Delta p)^2 \rangle}{2\Delta t} \tag{C1}
$$
In the relativistic limit the total energy $W$ is given by  
$$
W^2 = p^2 c^2 + m_0^2 c^4 = (E + E_0)^2 \tag{C2}
$$
so  
$$
p^2 c^2 = E(E + 2E_0) \tag{C3}
$$
One could obtain the same results by  
$$
p=\gamma m_0 v
,\quad
E=(\gamma-1) m_0 c^2
,\quad
E_0 = m_0 c^2
\tag{add}
$$
where $E$ and $E_0$ are the kinetic and rest mass energies, respectively. Differentiating equation (C3) gives an expression for $\Delta p$ 
$$
pc^2 \Delta p = (E + E_0)\Delta E
$$
And hence  
$$
\frac{1}{p^2} D_{pp} = \frac{1}{p^2} \frac{\langle (\Delta p)^2 \rangle}{2\Delta t} = \frac{(E + E_0)^2}{(E + 2E_0)^2 } \frac{1}{E^2} D_{EE} 
\tag{C4}
$$
Hence  
$$
\frac{1}{E^2} D_{EE} = \frac{(E + 2E_0)^2}{(E + E_0)^2} \left( \frac{1}{p^2} D_{pp} \right) \tag{C5}
$$
Similarly, the mixed energy pitch angle diffusion rate is given by  
$$
\frac{1}{E^2} D_{E\alpha} = \frac{(E + 2E_0)}{(E + E_0)^2} \left( \frac{1}{p^2} D_{p\alpha} \right) \tag{C6}
$$


