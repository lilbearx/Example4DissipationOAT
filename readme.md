# Collective dephase and individual dephase in One Axis Twisting(OAT) <br>

OAT Hamiltonian : 

$$H = \chi J_z^2$$

Master equation :

$$
\dot{\rho}(t)=-\frac i\hbar[H(t),\rho(t)]+\sum_n\frac12\left[2C_n\rho(t)C_n^\dagger-\rho(t)C_n^\dagger C_n-C_n^\dagger C_n\rho(t)\right]
$$

Initial state :

$$
|\psi\rangle = |\theta = \pi/2, \phi = 0\rangle
$$

| Collapse operators | Decay rate  | 
| :--------  | :-----  |
| $J_-$ | $\gamma_c$ |
| $\sigma_-^i$ | $\gamma_i$  |


在使用julia的QuantumCumulants库时尝试研究单轴扭曲模型哈密顿量下，原子的集体衰退以及单个原子的衰退的动力学过程。
在使用集体算符描述系统哈密顿量时，无法有合适的算符描述单个原子的衰退。而在计算方程组时，集体算符其期望值的绝对值往往随着原子系综粒子数的增加而增加，
这使得在计算偏微分方程组时，其积累的误差会增加，这意味着在短时间内计算的准确度不再可信。
而使用全同粒子用不同的索引来表示原子时，集体耗散算符无法顺利的表示并且计算，但是采用这一方式的好处在于，整个需要计算的数据往往都在-1到1之间，这意味着误差积累往往会比较小。
总结而言需要解决的问题在于：
- [ ]  集体算符表示下，是否有合适的算法或者合适的处理方式是得误差积累尽可能的小。
- [ ]  全同粒子索引表示下，表示出集体耗散算符的形式。

Qutip的piqs里面写的程序有点牛了，能够用Dicke空间描述原子各自的耗散。
- [ ] 了解一下piqs是如何生产刘维尔算符的。
