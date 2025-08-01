引理(lemma): 向电路中的任意一根或几根导线上的任意一个或几个位置添加任意数量的**I门(I gate)** 得到的新电路与原电路是等效的
双量子比特系统(double-qubit system)中的两个并行的一元量子门(single-qubit quantum gate): 4 $\times$ 4酉矩阵(unitary matrix)，即两个一元量子门(single-qubit quantum gate)对应的2 $\times$ 2酉矩阵(unitary matrix)的张量积(tensor product)
	一元量子门(single-qubit quantum gate)U在导线(wire)1上，一元量子门(single-qubit quantum gate)V在导线(wire)2上:
$$U|x\rangle \otimes V|y\rangle = (U \otimes V) \cdot |xy\rangle$$
		证明(proof): 逆用张量积(tensor product)的混合乘积性质
$$U_{1}/U^{(1)} \cdot V_{2}/V^{(2)} = U \otimes V$$
	一元量子门(single-qubit quantum gate)V在导线(wire)1上，一元量子门(single-qubit quantum gate)U在导线(wire)2上:
$$V|x\rangle \otimes U|y\rangle = (V \otimes U) \cdot |xy\rangle\rangle$$
	(逆用张量积(tensor product)的混合乘积性质)
$$V_{1}/V^{(1)} \cdot U_{2}/U^{(2)} = V \otimes U$$
(推广)n量子比特系统(n-qubit system)中的n个并行的一元量子门(single-qubit quantum gate): $2^{n}$ $\times$ $2^{n}$酉矩阵(unitary matrix)，即n个一元量子门(single-qubit quantum gate)对应的2 $\times$ 2酉矩阵(unitary matrix)的张量积(tensor product)
	一元量子门(single-qubit quantum gate)U在导线(wire)i上，可认为其他导线(wire)上各有一个I门(I gate):
$$U_{i}/U^{(i)} = I^{\otimes (i - 1)} \otimes U \otimes I^{\otimes (n - i)}$$
	一元量子门(single-qubit quantum gate)U在导线(wire)i上，一元量子门(single-qubit quantum gate)V在导线(wire)j(其中i < j)上，可认为其他导线(wire)上各有一个I门(I gate):
$$U_{i}/U^{(i)} \cdot V_{j}/V^{(j)} = I^{\otimes (i - 1)} \otimes U \otimes I^{\otimes (j - i - 1)} \otimes V \otimes I^{\otimes (n - j)}$$
	一元量子门(single-qubit quantum gate)V在导线(wire)i上，一元量子门(single-qubit quantum gate)U在导线(wire)j(其中i < j)上，可认为其他导线(wire)上各有一个I门(I gate):
$$V_{i}/V^{(i)} \cdot U_{j}/U^{(j)} = I^{\otimes (i - 1)} \otimes V \otimes I^{\otimes (j - i - 1)} \otimes U \otimes I^{\otimes (n - j)}$$
	二元量子门(double-qubit quantum gate)U在两条相邻的导线(wire)i和j(其中i < j且j = i + 1)上，可认为其他导线(wire)上各有一个I门(I gate):
$$\begin{cases}U_{i, j}/U^{(i, j)} = I^{\otimes (i - 1)} \otimes U_{1, 2} \otimes I^{\otimes (n - j)} \\ U_{j, i}/U^{(j, i)} = I^{\otimes (i - 1)} \otimes U_{2, 1} \otimes I^{\otimes (n - j)}\end{cases}$$
	注: 若二元量子门(double-qubit quantum gate)U在两条不相邻的导线(wire)i和j(其中i < j)上，则不可认为其他导线(wire)上各有一个I门(I gate)
