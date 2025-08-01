量子化(quantization): 物理量的值只能是离散(discrete)的，不能是连续(continuous)的
	例: 能量量子化(quantization of energy)、动量量子化(quantization of momentum)、角动量量子化(quantization of angular momentum)、自旋量子化(quantization of spin)
量子(quantum): 有的物理量是量子化的的粒子
	例: 光子(photon)是量子(quantum)，因为光子(photon)的能量(energy)和自旋(spin)是量子化的；电子(electron)是量子(quantum)，因为电子(electron)的能量和角动量(angular momentum)是量子化的
量子系统(quantum system): 由一个或多个量子(quantum)组成的系统(system)
量子态(quantum state): 量子系统(quantum system)在某一时刻的状态(state)
	基态(basis state)
	叠加态(superposition state): 基态(basis state)的线性组合(linear combination)
**量子态(quantum state)**:
	**波函数(wave function)**
	(\*)**态矢(量)(state vector)****: **向量(vector)**
		**右矢(ket,  $|\cdot\rangle$)**: **列向量(column vector)**
		**左矢(bra, $\langle\cdot|$)**: **行向量(row vector)**
			**左矢(bra, $\langle\cdot|$) = 右矢(ket, $|\cdot\rangle$)的共轭转置(conjugate transpose)**
$$\langle\cdot| = |\cdot\rangle^{\dagger}$$
			**左矢(ket, $\langle\cdot|$)乘右矢(bra, $|\cdot\rangle$) = 内积(inner product)**
$$\langle\cdot|\cdot\rangle = \langle\cdot||\cdot\rangle = |\cdot\rangle^{\dagger}|\cdot\rangle = |\cdot\rangle \cdot |\cdot\rangle = \langle|\cdot\rangle, |\cdot\rangle\rangle$$
	**密度矩阵(density matrix, D)**
**单量子比特系统(single-qubit system)**: 两能级系统(two-level system)
	**量子态(quantum state)**: **模(modulus)** 为**1**的$2^{1} = 2$**维复列向量(2-d complex column vector)**
$$|\psi\rangle = \alpha |0\rangle + \beta|1\rangle = \alpha\begin{bmatrix}1 \\ 0\end{bmatrix} + \beta\begin{bmatrix}0 \\ 1\end{bmatrix} = \begin{bmatrix}\alpha \\ 0\end{bmatrix} + \begin{bmatrix}0 \\ \beta\end{bmatrix} = \begin{bmatrix}\alpha \\ \beta\end{bmatrix}$$
	(其中**态0(ket 0, $|0\rangle = \begin{bmatrix}1 \\ 0\end{bmatrix}$)** 和**态1(ket 1, $|1\rangle = \begin{bmatrix}0 \\ 1\end{bmatrix}$)** 为**标准基态(canonical/standard basis state)/Z基态(Z-basis state)**；$\alpha$和$\beta$为**振幅(amplitude)**，均为**复数(complex number)**(i.e. $\alpha$, $\beta$ $\in$ $\mathbb{C}$)，**不全为0**(i.e. $\alpha$ $\neq$ 0或$\beta$ $\neq$ 0)，满足**归一化(normalization)** 条件(i.e. $|\alpha|^{2} + |\beta|^{2} = 1$)
	**基(basis)**:
		**标准基(canonical/standard basis)/Z基(Z-basis)**$\{|0\rangle, |1\rangle\}$:
			**性质(property)**: **正交归一基(orthonormal basis)**
				正交(orthogonal):
$$\langle1|0\rangle = \langle0|1\rangle = 0$$
				归一(normal):
$$\begin{cases}\langle0|0\rangle = 1 \\ \langle1|1\rangle = 1\end{cases}$$
		**对角基(diagonal basis)**/**X基(X-basis)**/**阿达马基(Hadamard basis)**$\{|+\rangle = \frac{|0\rangle + |1\rangle}{\sqrt{2}}, |-\rangle = \frac{|0\rangle - |1\rangle}{\sqrt{2}}\}$:
			**性质(property)**: **正交归一基(orthonormal basis)**
				证明(proof):
					基(basis):
$$\begin{cases}|+\rangle = \frac{|0\rangle + |1\rangle}{\sqrt{2}} \\ |-\rangle = \frac{|0\rangle - |1\rangle}{\sqrt{2}}\end{cases} \Leftrightarrow \begin{cases}|0\rangle = \frac{|+\rangle + |-\rangle}{\sqrt{2}} \\ |1\rangle = \frac{|+\rangle - |-\rangle}{\sqrt{2}}\end{cases}$$
					正交(orthogonal):
$$\langle-|+\rangle = \langle+|-\rangle = \frac{\langle0|+\langle1|}{\sqrt{2}}\frac{|0\rangle - |1\rangle}{\sqrt{2}} = \frac{\langle0|0\rangle - \langle0|1\rangle + \langle1|0\rangle - \langle1|1\rangle}{2} = \frac{1 - 0 + 0 - 1}{2} = 0$$
					归一(normal):
$$\begin{cases}\langle+|+\rangle = \frac{\langle0| + \langle1|}{\sqrt{2}}\frac{|0\rangle + |1\rangle}{\sqrt{2}} = \frac{\langle0|0\rangle + \langle0|1\rangle + \langle1|0\rangle + \langle1|1\rangle}{2} = \frac{1 + 0 + 0 + 1}{2} = 1 \\ \langle-|-\rangle = \frac{\langle0| - \langle1|}{\sqrt{2}}\frac{|0\rangle - |1\rangle}{\sqrt{2}} = \frac{\langle0|0\rangle - \langle0|1\rangle - \langle1|0\rangle + \langle1|1\rangle}{\sqrt{2}} = \frac{1 - 0 - 0 + 1}{2} = 1\end{cases}$$
		**Y基(Y-basis)**$\{|+i\rangle = \frac{|0\rangle + i|1\rangle}{\sqrt{2}}, |-i\rangle = \frac{|0\rangle - i|1\rangle}{\sqrt{2}}\}$:
			**性质(property)**: **正交归一基(orthonormal basis)**:
				证明(proof):
					基(basis):
$$\begin{cases}|+i\rangle = \frac{|0\rangle + i|1\rangle}{\sqrt{2}} \\ |-i\rangle = \frac{|0\rangle - i|1\rangle}{\sqrt{2}}\end{cases} \Leftrightarrow \begin{cases}|0\rangle = \frac{|+i\rangle + |-i\rangle}{\sqrt{2}} \\ |1\rangle = \frac{|+i\rangle - |-i\rangle}{\sqrt{2}i}\end{cases}$$
					正交(orthogonal):
$$\langle+i|-i\rangle = \frac{\langle0| - i\langle1|}{\sqrt{2}}\frac{|0\rangle - i|1\rangle}{\sqrt{2}} = \frac{\langle0|0\rangle - i\langle0|1\rangle + i\langle1|0\rangle + i^{2}\langle1|1\rangle}{2} = \frac{1 - 0 + 0 - 1}{2} = 0$$
$$\langle-i|+i\rangle = \overline{\langle+i|-i\rangle} = \overline{0} = 0$$
					归一(normal):
$$\begin{cases}\langle+i|+i\rangle = \frac{\langle0| - i\langle1|}{\sqrt{2}}\frac{|0\rangle + i|1\rangle}{\sqrt{2}} = \frac{\langle0|0\rangle + i\langle0|1\rangle - i\langle1|0\rangle - i^{2}\langle1|1\rangle}{2} = \frac{1 + 0 - 0 + 1}{2} = 1 \\ \langle-i|-i\rangle = \frac{\langle0| + i\langle1|}{\sqrt{2}}\frac{|0\rangle - i|1\rangle}{\sqrt{2}} = \frac{\langle0|0\rangle - i\langle0|1\rangle + i\langle1|0\rangle - i^{2}\langle1|1\rangle}{2} = \frac{1 - 0 + 0 + 1}{2} = 1\end{cases}$$
$$|\psi\rangle = \alpha|0\rangle + \beta|1\rangle = \alpha^{'}|+\rangle + \beta^{'}|1\rangle = \alpha^{''}|+i\rangle + \beta^{''}|-i\rangle$$
		注: $\{-|0\rangle, -|1\rangle\}$, $\{|0\rangle, |+\rangle\}$等也为基(basis)
	**投影算子(projection operator)**:
		$P_{0} = |0\rangle\langle0|$: 取$|\psi\rangle$在$|0\rangle$**方向(direction)** 上的分量，即将$|\psi\rangle$**投影(project)** 到$|0\rangle$**方向(direction)** 上，即取$|\psi\rangle$在$|0\rangle$**方向(direction)** 上的分量
$$P_{0}|\psi\rangle = (|0\rangle\langle0|)|\psi\rangle = (\langle0|\psi\rangle)|0\rangle = \alpha|0\rangle$$
			证明(proof):
$$P_{0}|\psi\rangle = (|0\rangle\langle0|)|\psi\rangle = (|0\rangle\langle0|)(\alpha|0\rangle + \beta|1\rangle) = (|0\rangle\langle0|)(\alpha|0\rangle) + (|0\rangle\langle0|)(\beta|1\rangle) = \alpha(|0\rangle\langle0|)|0\rangle + \beta(|0\rangle\langle0|)|1\rangle = \alpha|0\rangle(\langle0|0\rangle) + \beta|0\rangle(\langle0|1\rangle) = \alpha|0\rangle$$
		$P_{1} = |1\rangle\langle1|$: 取$|\psi\rangle$在$|1\rangle$**方向(direction)** 上的分量，即将$|\psi\rangle$**投影(project)** 到$|1\rangle$**方向(direction)** 上，即
$$P_{1}|\psi\rangle = (|1\rangle\langle1|)|\psi\rangle = (\langle1|\psi\rangle)|1\rangle = \beta|1\rangle$$
			证明(proof):
$$P_{1}|\psi\rangle = (|1\rangle\langle1|)|\psi\rangle = (|1\rangle\langle1|)(\alpha|0\rangle + \beta|1\rangle) = (|1\rangle\langle1|)(\alpha|0\rangle) + (|1\rangle\langle1|)(\beta|1\rangle) = \alpha(|1\rangle\langle1|)|0\rangle + \beta(|1\rangle\langle1|)|1\rangle = \alpha|1\rangle(\langle1|0\rangle) + \beta|1\rangle(\langle1||1\rangle) = \beta|1\rangle$$
			注:
				$|1\rangle\langle0|$: 取$|\psi\rangle$在$|0\rangle$**方向(direction)** 上的分量的**线性组合系数(linear combination coefficient)** 作为在$|1\rangle$**方向(direction)** 上的分量的**线性组合系数(linear combination coefficient)**
$$(|1\rangle\langle0|)|\psi\rangle = (\langle0|\psi\rangle)|1\rangle = \alpha|1\rangle$$
					证明(proof):
$$(|1\rangle\langle0|)|\psi\rangle = (|1\rangle\langle0|)(\alpha|0\rangle + \beta|1\rangle) = (|1\rangle\langle0|)(\alpha|0\rangle) + (|1\rangle\langle0|)(\beta|1\rangle) = \alpha(|1\rangle\langle0|)|0\rangle + \beta(|1\rangle\langle0|)|1\rangle = \alpha|1\rangle(\langle0|0\rangle) + \beta|1\rangle(\langle0|1\rangle) = \alpha|1\rangle$$
				$|0\rangle\langle1|$: 取$|\psi\rangle$在$|1\rangle$**方向(direction)** 上的分量的**线性组合系数(linear combination coefficient)** 作为在$|0\rangle$**方向(direction)** 上的分量的**线性组合系数(linear combination coefficient)**
$$(|0\rangle\langle1|)|\psi\rangle = (\langle1|\psi\rangle)|0\rangle = \beta|0\rangle$$
					证明(proof):
$$(|0\rangle\langle1|)|\psi\rangle = (|0\rangle\langle1|)(\alpha|0\rangle + \beta|1\rangle) = (|0\rangle\langle1|)(\alpha|0\rangle) + (|0\rangle\langle1|)(\beta|1\rangle) = \alpha(|0\rangle\langle1|)|0\rangle + \beta(|0\rangle\langle1|)|1\rangle = \alpha|0\rangle(\langle1|0\rangle) + \beta|0\rangle(\langle1|1\rangle) = \beta|0\rangle$$
		$|+\rangle\langle+|$: 取$|\psi\rangle$在$|+\rangle$**方向(direction)** 上的分量，即将$|\psi\rangle$**投影(project)** 到$|+\rangle$**方向(direction)** 上
$$(|+\rangle\langle+|)|\psi\rangle = (\langle+|\psi\rangle)|+\rangle = \alpha^{'}|+\rangle$$
			证明(proof):
$$(|+\rangle\langle+|)|\psi\rangle = (|+\rangle\langle+|)(\alpha^{'}|+\rangle + \beta^{'}|-\rangle) = (|+\rangle\langle+|)(\alpha^{'}|+\rangle) + (|+\rangle\langle+|)(\beta^{'}|-\rangle) = \alpha^{'}(|+\rangle\langle+|)|+\rangle + \beta^{'}(|+\rangle\langle+|)|-\rangle = \alpha^{'}|+\rangle(\langle+|+\rangle) + \beta^{'}|+\rangle(\langle+|-\rangle) = \alpha^{'}|+\rangle$$
		$|-\rangle\langle-|$: 取$|\psi\rangle$在$|-\rangle$**方向(direction)** 上的分量，即将$|\psi\rangle$**投影(project)** 到$|-\rangle$**方向(direction)** 上
$$(|-\rangle\langle-|)|\psi\rangle = (\langle-|\psi\rangle)|-\rangle = \beta^{'}|-\rangle$$
			证明(proof):
$$(|-\rangle\langle-|)|\psi\rangle = (|-\rangle\langle-|)(\alpha^{'}|+\rangle + \beta^{'}|-\rangle) = (|-\rangle\langle-|)(\alpha^{'}|+\rangle) + (|-\rangle\langle-|)(\beta^{'}|-\rangle) = \alpha^{'}(|-\rangle\langle-|)|+\rangle + \beta^{'}(|-\rangle\langle-|)|-\rangle = \alpha^{'}|-\rangle(\langle-|+\rangle) + \beta^{'}|-\rangle(\langle-|-\rangle) = \beta^{'}|-\rangle$$
			注:
				$|+\rangle\langle0|$: 取$|\psi\rangle$在$|0\rangle$**方向(direction)** 上的分量的**线性组合系数(linear combination coefficient)** 作为在$|+\rangle$**方向(direction)** 上的分量的**线性组合系数(linear combination coefficient)**
$$(|+\rangle\langle0|)|\psi\rangle = (\langle0|\psi\rangle)|+\rangle = \alpha|+\rangle$$
					证明(proof):
$$(|+\rangle\langle0|)|\psi\rangle = (|+\rangle\langle0|)(\alpha|0\rangle + \beta|1\rangle) = (|+\rangle\langle0|)(\alpha|0\rangle) + (|+\rangle\langle0|)(\beta|1\rangle) = \alpha(|+\rangle\langle0|)|0\rangle + \beta(|+\rangle\langle0|)|1\rangle = \alpha|+\rangle(\langle0|0\rangle) + \beta|+\rangle(\langle0|1\rangle) = \alpha|+\rangle$$
				$|-\rangle\langle1|$: 取$|\psi\rangle$在$|1\rangle$**方向** 上的分量的**线性组合系数(linear combination coefficient)** 作为在$|-\rangle$**方向(direction)** 上的分量的**线性组合系数(linear combination coefficient)**
$$(|-\rangle\langle1|)|\psi\rangle = (\langle1|\psi\rangle)|-\rangle = \beta|-\rangle$$
					证明(proof):
$$(|-\rangle\langle1|)|\psi\rangle = (|-\rangle\langle1|)(\alpha|0\rangle + \beta|1\rangle) = \alpha(|-\rangle\langle1|)|0\rangle + \beta(|-\rangle\langle1|)|1\rangle = \alpha|-\rangle(\langle1|0\rangle) + \beta|-\rangle(\langle1|1\rangle) = \beta|-\rangle$$
	**测量(measurement)** 和**坍缩(collapse)**:
		**测量(measurement)前**，**量子态(quantum state)** 由所有**基态(ground state)** 以各自的**振幅(amplitude)** 为**概率幅(probability amplitude)** **叠加(superpose)** 而成，是不确定的；**测量(measurement)后**，**量子态(state)** 会**坍缩(collapse)** 到某个**基态(ground state)** 上，是确定的
		某个**基态(ground state)** 被**测量(measurement)** 到的**概率(probability)** 是其**振幅(amplitude)** 的**模(modulus)** 的**平方(square)**
			以**标准基(canonical/standard basis)/Z基(Z-basis)**$\{|0\rangle, |1\rangle\}$为**基(basis)**:
$$|\psi\rangle = \alpha|0\rangle + \beta|1\rangle \Rightarrow \begin{cases}P(|0\rangle) = |\alpha|^{2} \\ P(|1\rangle) = |\beta|^{2}\end{cases}$$
			以**正交归一基(orthonormal basis)**$\{|+\rangle, |-\rangle\}$为**基(basis)**:
$$|\psi\rangle = \alpha^{'}|+\rangle + \beta^{'}|-\rangle \Rightarrow \begin{cases}P(|+\rangle) = |\alpha^{'}|^{2} \\ P(|-\rangle) = |\beta^{'}|^{2}\end{cases}$$
	**布洛赫球(Bloch sphere)**:
$$|\psi\rangle = \alpha|0\rangle + \beta|1\rangle(\text{其中}|\alpha| \geq 0, |\beta| \geq 0, |\alpha|^{2} + |\beta|^{2} = 1)$$
$$\text{设}\begin{cases}|\alpha| = \cos{\frac{\theta}{2}}, \mathrm{arg}(\alpha) = \phi_{1} \\ |\beta| = \sin{\frac{\theta}{2}}, \mathrm{arg}(\beta) = \phi_{2}\end{cases}(\text{其中}\theta \in [0, \pi])$$
$$\text{则}\begin{cases}\alpha = |\alpha|e^{i\phi_{1}} = e^{i\phi_{1}}\cos{\frac{\theta}{2}} \\ \beta = |\beta|e^{i\phi_{2}} = e^{i\phi_{2}}\sin{\frac{\theta}{2}}\end{cases}$$
$$\text{则}|\psi\rangle = \alpha|0\rangle + \beta|1\rangle = e^{i\phi_{1}}|0\rangle\cos{\frac{\theta}{2}} + e^{i\phi_{2}}|1\rangle\sin{\frac{\theta}{2}} = e^{i\phi_{1}}[|0\rangle\cos{\frac{\theta}{2}} + e^{i(\phi_{2} - \phi_{1})}|1\rangle\sin{\frac{\theta}{2}}] \stackrel{\text{discard global amplitude $e^{i\phi_{1}}$ will not change the probability distribution of measurement results}}{\equiv} |0\rangle\cos{\frac{\theta}{2}} + e^{i(\phi_{2} - \phi_{1})}|1\rangle\sin{\frac{\theta}{2}} \stackrel{\phi_{2} - \phi_{1} \rightarrow \phi}{=} |0\rangle\cos{\frac{\theta}{2}} + e^{i\phi}|1\rangle\sin{\frac{\theta}{2}} = \begin{bmatrix}1 \\ 0\end{bmatrix}\cos{\frac{\theta}{2}} + e^{i\phi}\begin{bmatrix}0 \\ 1\end{bmatrix}\sin{\frac{\theta}{2}} = \begin{bmatrix}\cos{\frac{\theta}{2}} \\ 0\end{bmatrix} + \begin{bmatrix}0 \\ e^{i\phi}\sin{\frac{\theta}{2}}\end{bmatrix} = \begin{bmatrix}\cos{\frac{\theta}{2}} \\ e^{i\phi}\sin{\frac{\theta}{2}}\end{bmatrix}$$
	丢弃**全局振幅(global amplitude)** 前，**量子态(quantum state)** 是**二维复空间(2-d complex space, $\mathbb{C}^{2}$)** 中**长度(length)** 为**1** 的**二维列向量(2-d column vector)**，即**四维实空间(4-d real space, $\mathbb{R}^{4}$)** 中**长度(length)** 为**1** 的**四维列向量(4-d column vector)**；丢弃**全局振幅(global amplitude)** 后，**量子态(quantum state)** 是**一维实空间(1-d real space, $\mathbb{R}$)** 与**一维复空间(complex space, $\mathbb{C}$)** 的**笛卡尔积(Cartesian product)** 中**长度(length)** 为**1** 的**二维列向量(2-d column vector)**，即**三维实空间(3-d real space, $\mathbb{R}^{3}$)** 中**长度(length)** 为**1** 的**三维列向量(3-d column vector)**，因此可以与**单位球(unit sphere)**$x^{2} + y^{2} + z^{2} = 1$上的**点(point)** **one-to-one and onto**，规定**量子态(quantum state)**$|0\rangle\cos{\frac{\theta}{2}} + e^{i\phi}|1\rangle\sin{\frac{\theta}{2}}$的**球坐标(spherical coordinate)** 为 **(1, $\theta$, $\phi$)**，称**量子态(quantum state)**$|0\rangle\cos{\frac{\theta}{2}} + e^{i\phi}|1\rangle\sin{\frac{\theta}{2}}$为**量子态(quantum state)**$|\psi\rangle = \alpha|0\rangle + \beta|1\rangle$的**纯态(pure state)**，**单位球(unit sphere)**$x^{2} + y^{2} + z^{2} = 1$为**布洛赫球(Bloch sphere)**
		**性质(property)**:
			$|0\rangle$位于**布洛赫球(Bloch sphere)** 与**z轴(z-axis)正半轴** 的**交点**(i.e. **布洛赫球(Bloch sphere)** 的**北极点(north pole point)**)
				证明(proof):
$$|0\rangle\cos{\frac{\theta}{2}} + e^{i\phi}|1\rangle\sin{\frac{\theta}{2}} = |0\rangle \Rightarrow \cos{\frac{\theta}{2}} = 1 \Rightarrow \frac{\theta}{2} = 0 \Rightarrow \theta = 0$$
			$|1\rangle$位于**布洛赫球(Bloch sphere)** 与**z轴(z-axis)负半轴** 的**交点**(i.e. **布洛赫球(Bloch sphere)** 的**南极点(north pole point)**)
				证明(proof):
$$|0\rangle\cos{\frac{\theta}{2}} + e^{i\phi}|1\rangle\sin{\frac{\theta}{2}} = |1\rangle \Rightarrow \cos{\frac{\theta}{2}} = 0 \Rightarrow \frac{\theta}{2} = \frac{\pi}{2} \Rightarrow \theta = \pi \Rightarrow e^{i\phi}\sin{\frac{\theta}{2}} = e^{i\phi} = 1 \Rightarrow \phi = 0$$
			$|+\rangle$位于**布洛赫球(Bloch sphere)** 与**x轴(x-axis)正半轴** 的**交点**
				证明(proof):
$$|0\rangle\cos{\frac{\theta}{2}} + e^{i\phi}|1\rangle\sin{\frac{\theta}{2}} = |+\rangle = \frac{|0\rangle + |1\rangle}{\sqrt{2}} = \frac{\sqrt{2}}{2}|0\rangle + \frac{\sqrt{2}}{2}|1\rangle \Rightarrow \cos{\frac{\theta}{2}} = \frac{\sqrt{2}}{2} \Rightarrow \frac{\theta}{2} = \frac{\pi}{4} \Rightarrow \theta = \frac{\pi}{2} \Rightarrow e^{i\phi}\sin{\frac{\theta}{2}} = \frac{\sqrt{2}}{2}e^{i\phi} = \frac{\sqrt{2}}{2} \Rightarrow e^{i\phi} = 1 \Rightarrow \phi = 0$$
			$|-\rangle$位于**布洛赫球(Bloch sphere)** 与**x轴(x-axis)负半轴** 的**交点**
				证明(proof):
$$\cos{\frac{\theta}{2}}|0\rangle + e^{i\phi}|1\rangle\sin{\frac{\theta}{2}} = |-\rangle = \frac{|0\rangle - |1\rangle}{\sqrt{2}} = \frac{\sqrt{2}}{2}|0\rangle - \frac{\sqrt{2}}{2}|1\rangle \Rightarrow \cos{\frac{\theta}{2}} = \frac{\sqrt{2}}{2} \Rightarrow \frac{\theta}{2} = \frac{\pi}{4} \Rightarrow \theta = \frac{\pi}{2} \Rightarrow e^{i\phi}\sin{\frac{\theta}{2}} = \frac{\sqrt{2}}{2}e^{i\phi} = -\frac{\sqrt{2}}{2} \Rightarrow e^{i\phi} = -1 \Rightarrow \phi = \pi$$
			$|+i\rangle$位于**布洛赫球(Bloch sphere)** 与**y轴(y-axis)正半轴** 的**交点**
				证明(proof):
$$|0\rangle\cos{\frac{\theta}{2}} + e^{i\phi}|1\rangle\sin{\frac{\theta}{2}} = |+i\rangle = \frac{|0\rangle + i|1\rangle}{\sqrt{2}} = \frac{\sqrt{2}}{2}|0\rangle + \frac{\sqrt{2}}{2}i|1\rangle \Rightarrow \cos{\frac{\theta}{2}} = \frac{\sqrt{2}}{2} \Rightarrow \frac{\theta}{2} = \frac{\pi}{4} \Rightarrow \theta = \frac{\pi}{2} \Rightarrow e^{i\phi}\sin{\frac{\theta}{2}} = \frac{\sqrt{2}}{2}e^{i\phi} = \frac{\sqrt{2}}{2}i \Rightarrow e^{i\phi} = i \Rightarrow \phi = \frac{\pi}{2}$$
		$|-i\rangle$位于**布洛赫球(Bloch sphere)** 与**y轴(y-axis)负半轴** 的**交点**上
				证明(proof):
$$|0\rangle\cos{\frac{\theta}{2}} + e^{i\phi}|1\rangle\sin{\frac{\theta}{2}} = \frac{|0\rangle - i|1\rangle}{\sqrt{2}} = \frac{\sqrt{2}}{2}|0\rangle - \frac{\sqrt{2}}{2}i|1\rangle \Rightarrow \cos{\frac{\theta}{2}} = \frac{\sqrt{2}}{2} \Rightarrow \frac{\theta}{2} = \frac{\pi}{4} \Rightarrow \theta = \frac{\pi}{2} \Rightarrow e^{i\phi}\sin{\frac{\theta}{2}} = \frac{\sqrt{2}}{2}e^{i\phi} = -\frac{\sqrt{2}}{2}i \Rightarrow e^{i\phi} = -i \Rightarrow \phi = \frac{3\pi}{2}$$
		**布洛赫球(Bloch sphere)** 上的**旋转变换(rotation transformation)**:
			在**布洛赫球(Bloch sphere)** 上绕**z轴(z-axis)**(i.e. $\vec{z} = \vec{OZ} = (0, 0, 1)$，其中点O(0, 0, 0)为原点(origin)，点Z(0, 0, 1)为z轴(z-axis)与布洛赫球(Bloch sphere)的上交点)**旋转(rotate)**$\varphi$**弧度(radian)**:
$$(1, \theta, \phi) = |0\rangle\cos{\frac{\theta}{2}} + e^{i\phi}|1\rangle\sin{\frac{\theta}{2}} \rightarrow |\psi^{'}\rangle = (1, \theta, \phi + \varphi) = |0\rangle\cos{\frac{\theta}{2}} + e^{i(\phi + \varphi)}|1\rangle\sin{\frac{\theta}{2}}$$
				**矩阵表示(matrix representation)**:
$$R(\varphi) = \begin{bmatrix}1 & 0 \\ 0 & e^{i\varphi}\end{bmatrix} \equiv R_{z}(\varphi) = \begin{bmatrix}e^{-i\frac{\varphi}{2}} & 0 \\ 0 & e^{i\frac{\varphi}{2}}\end{bmatrix} = I\cos{\frac{\varphi}{2}} - iZ\sin{\frac{\varphi}{2}} = e^{-i\frac{\varphi}{2}Z}$$
					证明(proof):
$$|0\rangle\cos{\frac{\theta}{2}} + e^{i(\phi + \varphi)}|1\rangle\sin{\frac{\theta}{2}} = \begin{bmatrix}\cos{\frac{\theta}{2}} \\ e^{i(\phi + \varphi)}\sin{\frac{\theta}{2}}\end{bmatrix} = \begin{bmatrix}\cos{\frac{\theta}{2}} \\ 0\end{bmatrix} + \begin{bmatrix}0 \\ e^{i(\phi + \varphi)}\sin{\frac{\theta}{2}}\end{bmatrix} = \cos{\frac{\theta}{2}}\begin{bmatrix}1 \\ 0\end{bmatrix} + e^{i\phi}\sin{\frac{\theta}{2}}\begin{bmatrix}0 \\ e^{i\varphi}\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & e^{i\varphi}\end{bmatrix}\begin{bmatrix}\cos{\frac{\theta}{2}} \\ e^{i\phi}\sin{\frac{\theta}{2}}\end{bmatrix} = R(\varphi)|\psi\rangle$$
$$R(\varphi) = \begin{bmatrix}1 & 0 \\ 0 & e^{i\varphi}\end{bmatrix} = e^{i\frac{\varphi}{2}}\begin{bmatrix}e^{-i\frac{\varphi}{2}} & 0 \\ 0 & e^{i\frac{\varphi}{2}}\end{bmatrix} \stackrel{\text{discard gobal amplitude $e^{i\frac{\varphi}{2}}$ will not change the probability distribution of measurement results}}{\equiv} \begin{bmatrix}e^{-i\frac{\varphi}{2}} & 0 \\ 0 & e^{i\frac{\varphi}{2}}\end{bmatrix} = R_{z}(\varphi)$$
$$R_{z}(\varphi) = \begin{bmatrix}e^{-i\frac{\varphi}{2}} & 0 \\ 0 & e^{i\frac{\varphi}{2}}\end{bmatrix} = \begin{bmatrix}\cos{(-\frac{\varphi}{2})} + i\sin{(-\frac{\varphi}{2})} & 0 \\ 0 & \cos{\frac{\varphi}{2}} + i\sin{\frac{\varphi}{2}}\end{bmatrix} = \begin{bmatrix}\cos{\frac{\varphi}{2}} - i\sin{\frac{\varphi}{2}} & 0 \\ 0 & \cos{\frac{\varphi}{2}} + i\sin{\frac{\varphi}{2}}\end{bmatrix} = \begin{bmatrix}\cos{\frac{\varphi}{2}} & 0 \\ 0 & \cos{\frac{\varphi}{2}}\end{bmatrix} - \begin{bmatrix}i\sin{\frac{\varphi}{2}} & 0 \\ 0 & -i\sin{\frac{\varphi}{2}}\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & 1\end{bmatrix}\cos{\frac{\varphi}{2}} - i\begin{bmatrix}1 & 0 \\ 0 & -1\end{bmatrix}\sin{\frac{\varphi}{2}} = I\cos{\frac{\varphi}{2}} - iZ\sin{\frac{\varphi}{2}}$$
$$e^{-i\frac{\varphi}{2}Z} = I + (-\frac{i\varphi}{2}Z) + \frac{(-\frac{i\varphi}{2}Z)^{2}}{2!} + \frac{(-\frac{i\varphi}{2}Z)^{3}}{3!} + \dots + \frac{(-\frac{i\varphi}{2}Z)^{2n}}{(2n)!} + \frac{(-\frac{i\varphi}{2}Z)^{2n + 1}}{(2n + 1)!} = I - i(\frac{\varphi}{2})Z - \frac{(\frac{\varphi}{2})^{2}}{2!}I + i\frac{(\frac{\varphi}{2})^{3}}{3!}Z + \dots + \frac{(-1)^{n}(\frac{\varphi}{2})^{2n}}{(2n)!}I - i\frac{(-1)^{n}(\frac{\varphi}{2})^{2n + 1}}{(2n + 1)!}Z = [I - \frac{(\frac{\varphi}{2})^{2}}{2!}I + \dots + \frac{(-1)^{n}(\frac{\varphi}{2})^{2n}}{(2n)!}I] - [i\frac{\varphi}{2}Z - i\frac{(\frac{\varphi}{2})^{3}}{3!}Z + \dots + i\frac{(\frac{\varphi}{2})^{2n + 1}}{(2n + 1)!}Z] = [1 - \frac{(\frac{\varphi}{2})^{2}}{2!} + \dots + \frac{(-1)^{n}(\frac{\varphi}{2})^{2n}}{(2n)!}]I - i[(\frac{\varphi}{2}) - \frac{(\frac{\varphi}{2})^{3}}{3!} + \dots + \frac{(-1)^{n}(\frac{\varphi}{2})^{2n + 1}}{(2n + 1)!}]Z = I\cos{\frac{\varphi}{2}} - iZ\sin{\frac{\varphi}{2}}$$
			在**布洛赫球(Bloch sphere)** 上绕**x轴(x-axis)**(i.e. $\vec{x} = \vec{OX} = (1, 0, 0)$，其中点O(0, 0, 0)为原点(origin)，点X(1, 0, 0)为x轴(x-axis)与布洛赫球(Bloch sphere)的上交点)**旋转(rotate)**$\varphi$**弧度(radian)**:
				**矩阵表示(matrix representation)**:
$$R_{x}(\varphi) = \begin{bmatrix}\cos{\frac{\varphi}{2}} & -i\sin{\frac{\varphi}{2}} \\ -i\sin{\frac{\varphi}{2}} & \cos{\frac{\varphi}{2}}\end{bmatrix} = I\cos{\frac{\varphi}{2}} - iX\sin{\frac{\varphi}{2}} = e^{-i\frac{\varphi}{2}X}$$
				证明(proof): 类比**布洛赫球(Bloch sphere)** 上绕**z轴(z-axis)** 的**旋转变换(rotation transformation)**
			在**布洛赫球(Bloch sphere)** 上绕**y轴(y-axis)**(i.e. $\vec{y} = \vec{OY} = (0, 1, 0)$，其中点O(0, 0, 0)为原点(origin)，点Y(0, 1, 0)为y轴(y-axis)与布洛赫球(Bloch sphere)的上交点)**旋转(rotate)**$\varphi$**弧度(radian)**:
				**矩阵表示(matrix representation)**:
$$R_{y}(\varphi) = \begin{bmatrix}\cos{\frac{\varphi}{2}} & -\sin{\frac{\varphi}{2}} \\ \sin{\frac{\varphi}{2}} & \cos{\frac{\varphi}{2}}\end{bmatrix} = I\cos{\frac{\varphi}{2}} - iY\sin{\frac{\varphi}{2}} = e^{-i\frac{\varphi}{2}Y}$$
				证明(proof): 类比在**布洛赫球(Bloch sphere)** 上绕**z轴(z-axis)** 的**旋转变换(rotation transformation)**
			(推广)在**布洛赫球(Bloch sphere)** 上绕**任意轴(axis)**(i.e. $\vec{n} = \vec{ON} = (n_{x}, n_{y}, n_{z}) = (n_{x}, 0, 0) + (0, n_{y}, 0) + (0, 0, n_{z}) = n_{x}(1, 0, 0) + n_{y}(0, 1, 0) + n_{z}(0, 0, 1) = n_{x}\vec{x} + n_{y}\vec{y} + n_{z}\vec{z}$，其中点O(0, 0, 0)为原点(origin)，点$N(n_{x}, n_{y}, n_{z})$为布洛赫球(Bloch sphere)上的任意一点)**旋转(rotate)**$\varphi$**弧度(radian)**:
				**矩阵表示(matrix representation)**:
$$R_{\vec{n}}(\varphi) = I\cos{\frac{\varphi}{2}} - i\sigma_{\vec{n}}\sin{\frac{\varphi}{2}} = e^{-i\frac{\varphi}{2}\sigma_{\vec{n}}}(\text{其中}\sigma_{\vec{n}} = n_{x}X + n_{y}Y + n_{z}Z)$$
				证明(proof): 类比**布洛赫球(Bloch sphere)** 上绕**z轴(z-axis)** 的**旋转变换(rotation transformation)**
			**Z-Y-Z分解(Z-Y-Z decomposition)**: **布洛赫球(Bloch sphere)** 上绕**任意轴(axis)** 的**旋转变换(rotation transformation)** 可以**分解(decompose)** 成一次绕**z轴(z-axis)** 的**旋转变换(rotation transformation)**，一次绕**y轴(y-axis)** 的**旋转变换(rotation transformation)** 和一次绕**z轴(z-axis)** 的**旋转变换(rotation transformation)**
	**张量积(tensor product)**:
$$\begin{cases}|0\rangle \otimes |0\rangle = \begin{bmatrix}1 \\ 0\end{bmatrix} \otimes \begin{bmatrix}1 \\ 0\end{bmatrix} = \begin{bmatrix}1\begin{bmatrix}1 \\ 0\end{bmatrix} \\ 0\begin{bmatrix}1 \\ 0\end{bmatrix}\end{bmatrix} = \begin{bmatrix}1 \\ 0 \\ 0 \\ 0\end{bmatrix} = |00\rangle \\ |0\rangle \otimes |1\rangle = \begin{bmatrix}1 \\ 0\end{bmatrix} \otimes \begin{bmatrix}0 \\ 1\end{bmatrix} = \begin{bmatrix}1\begin{bmatrix}0 \\ 1\end{bmatrix} \\ 0\begin{bmatrix}0 \\ 1\end{bmatrix}\end{bmatrix} = \begin{bmatrix}0 \\ 1 \\ 0 \\ 0\end{bmatrix} = |01\rangle \\ |1\rangle \otimes |0\rangle = \begin{bmatrix}0 \\ 1\end{bmatrix} \otimes \begin{bmatrix}1 \\ 0\end{bmatrix} = \begin{bmatrix}0\begin{bmatrix}1 \\ 0\end{bmatrix} \\ 1\begin{bmatrix}1 \\ 0\end{bmatrix}\end{bmatrix} = \begin{bmatrix}0 \\ 0 \\ 1 \\ 0\end{bmatrix} = |10\rangle \\ |1\rangle \otimes |1\rangle = \begin{bmatrix}0 \\ 1\end{bmatrix} \otimes \begin{bmatrix}0 \\ 1\end{bmatrix} = \begin{bmatrix}0\begin{bmatrix}0 \\ 1\end{bmatrix} \\ 1\begin{bmatrix}0 \\ 1\end{bmatrix}\end{bmatrix} = \begin{bmatrix}0 \\ 0 \\ 0 \\ 1\end{bmatrix} = |11\rangle\end{cases} \Rightarrow |\psi_{1}\rangle \otimes |\psi_{2}\rangle = (\alpha_{1}|0\rangle + \beta_{1}|1\rangle) \otimes (\alpha_{2}|0\rangle + \beta_{2}|1\rangle) = \alpha_{1}\alpha_{2}|00\rangle + \alpha_{1}\beta_{2}|01\rangle + \beta_{1}\alpha_{2}|10\rangle + \beta_{1}\beta_{2}|11\rangle$$
	**性质(property)**:
$$(|0\rangle + |1\rangle)^{\otimes n} = (|0\rangle + |1\rangle) \otimes \dots \otimes (|0\rangle + |1\rangle) = |0 \dots 0\rangle + |0 \dots 01\rangle + |1 \dots 1\rangle = \sum_{x \in \{0, 1\}^{n}}|x\rangle = \sum_{x = 0}^{2^{n} - 1}|x\rangle$$
**双量子比特系统(double-qubit system)**: 四能级系统(four-level system)
	**量子态(quantum state)**: **模(modulus)** 为**1**的$2^{2} = 4$**维复列向量(4-d complex column vector)**
$$|\psi\rangle = \sum_{s \in \{0, 1\}^{2}}c_{s}|s\rangle = c_{00}|00\rangle + c_{01}|01\rangle + c_{10}|10\rangle + c_{11}|11\rangle = c_{00}\begin{bmatrix}1 \\ 0 \\ 0 \\ 0\end{bmatrix} + c_{01}\begin{bmatrix}0 \\ 1 \\ 0 \\ 0\end{bmatrix} + c_{10}\begin{bmatrix}0 \\ 0 \\ 1 \\ 0\end{bmatrix} + c_{11}\begin{bmatrix}0 \\ 0 \\ 0 \\ 1\end{bmatrix} = \begin{bmatrix}c_{00} \\ 0 \\ 0 \\ 0\end{bmatrix} + \begin{bmatrix}0 \\ c_{01} \\ 0 \\ 0\end{bmatrix} + \begin{bmatrix}0 \\ 0 \\ c_{10} \\ 0\end{bmatrix} + \begin{bmatrix}0 \\ 0 \\ 0 \\ c_{11}\end{bmatrix} = \begin{bmatrix}c_{00} \\ c_{01} \\ c_{10} \\ c_{11}\end{bmatrix}$$
	(其中**态00(ket zero zero, $|00\rangle$ = $\begin{bmatrix}1 \\ 0 \\ 0 \\ 0\end{bmatrix}$)**, **态01(ket zero one, $|01\rangle$ = $\begin{bmatrix}0 \\ 1 \\ 0 \\ 0\end{bmatrix}$)**, **态10(ket one zero, $|10\rangle$ = $\begin{bmatrix}0 \\ 0 \\ 1 \\ 0\end{bmatrix}$)** 和**态11(ket one one, $|11\rangle$ = $\begin{bmatrix}0 \\ 0 \\ 0 \\ 1\end{bmatrix}$)** 为**标准基态(canonical/standard basis state)**；$c_{00}$, $c_{01}$, $c_{10}$, $c_{11}$为**振幅(amplitude)**，均为**复数(complex number)**(i.e. $c_{00}$, $c_{01}$, $c_{10}$, $c_{11}$ $\in$ $\mathbb{C}$)，**不全为0**(i.e. $c_{00}$ $\neq$ 0或$c_{01}$ $\neq$ 0或$c_{10}$ $\neq$ 0或$c_{11}$ $\neq$ 0)，满足**归一化(normalization)** 条件(i.e. $|c_{00}|^{2} + |c_{01}|^{2} + |c_{10}|^{2} + |c_{11}|^{2} = \sum_{\mathbf{s} \in \{0, 1\}^{2}}|c_{\mathbf{s}}|^{2} = 1$))
	**基(basis)**:
		**标准基(canonical/standard basis)**: $\{|00\rangle, |01\rangle, |10\rangle, |11\rangle\}$
			**性质(property)**: **正交归一基(orthonormal basis)**
				正交(orthogonal):
$$\begin{cases}\langle01|00\rangle = \langle00|01\rangle = 0 \\ \langle10|00\rangle = \langle00|10\rangle = 0 \\ \langle11|00\rangle = \langle00|11\rangle = 0 \\ \langle10|01\rangle = \langle01|10\rangle = 0 \\ \langle11|01\rangle = \langle01|11\rangle = 0 \\ \langle11|10\rangle = \langle10|11\rangle = 0\end{cases}$$
				归一(normal):
$$\begin{cases}\langle00|00\rangle = 1 \\ \langle01|01\rangle = 1 \\ \langle10|10\rangle = 1 \\ \langle11|11\rangle = 1\end{cases}$$
		**贝尔基(Bell basis)**: $\{|\Phi^{+}\rangle = \frac{|00\rangle + |11\rangle}{\sqrt{2}}, |\Phi^{-}\rangle = \frac{|00\rangle - |11\rangle}{\sqrt{2}}, |\Psi^{+}\rangle = \frac{|01\rangle + |10\rangle}{\sqrt{2}}, |\Psi^{-}\rangle = \frac{|01\rangle - |10\rangle}{\sqrt{2}}\}$
			**性质(property)**: **正交归一基(orthonormal basis)**
				证明(proof):
					基(basis):
$$\begin{cases}|\Phi^{+}\rangle = \frac{|00\rangle + |11\rangle}{\sqrt{2}} \\ |\Phi^{-}\rangle = \frac{|00\rangle - |11\rangle}{\sqrt{2}} \\ |\Psi^{+}\rangle = \frac{|01\rangle + |10\rangle}{\sqrt{2}} \\ |\Psi^{-}\rangle = \frac{|01\rangle - |10\rangle}{\sqrt{2}}\end{cases} \Leftrightarrow \begin{cases}|00\rangle = \frac{|\Phi^{+}\rangle + |\Phi^{-}\rangle}{\sqrt{2}} \\ |01\rangle = \frac{|\Psi^{+}\rangle + |\Psi^{-}\rangle}{\sqrt{2}} \\ |10\rangle = \frac{|\Psi^{+}\rangle - |\Psi^{-}\rangle}{\sqrt{2}} \\ |11\rangle = \frac{|\Phi^{+}\rangle - |\Phi^{-}\rangle}{\sqrt{2}}\end{cases}$$
					正交(orthogonal): 略
					归一(normal): 略
			**纠缠门(entangling gate)**: 制备**贝尔态(Bell state)** 的**量子电路(quantum circuit)**
![[贝尔态(Bell State).png]]
$$|00\rangle \rightarrow |\Phi^{+}\rangle$$
				证明(proof):
$$CNOT \ H|0\rangle|0\rangle = CNOT|+\rangle|0\rangle = CNOT\frac{|0\rangle + |1\rangle}{\sqrt{2}}|0\rangle = CNOT\frac{|00\rangle + |10\rangle}{\sqrt{2}} = \frac{CNOT|00\rangle + CNOT|10\rangle}{\sqrt{2}} = \frac{|00\rangle + |11\rangle}{\sqrt{2}} = |\Phi^{+}\rangle$$
$$|10\rangle \rightarrow |\Phi^{-}\rangle$$
				证明(proof):
$$CNOT\ H|1\rangle|0\rangle = CNOT|-\rangle|0\rangle = CNOT\frac{|0\rangle - |1\rangle}{\sqrt{2}}|0\rangle = CNOT\frac{|00\rangle - |10\rangle}{\sqrt{2}} = \frac{CNOT|00\rangle - CNOT|10\rangle}{\sqrt{2}} = \frac{|00\rangle - |11\rangle}{\sqrt{2}} = |\Phi^{-}\rangle$$
$$|01\rangle \rightarrow |\Psi^{+}\rangle$$
				证明(proof):
$$CNOT \ H|0\rangle|1\rangle = CNOT|+\rangle|1\rangle = CNOT\frac{|0\rangle + |1\rangle}{\sqrt{2}}|1\rangle = CNOT\frac{|01\rangle + |11\rangle}{\sqrt{2}} = \frac{CNOT|01\rangle + CNOT|11\rangle}{\sqrt{2}} = \frac{|01\rangle + |10\rangle}{\sqrt{2}} = |\Psi^{+}\rangle$$
$$|11\rangle \rightarrow |\Psi^{-}\rangle$$
$$CNOT \ H|1\rangle|1\rangle = CNOT|-\rangle|1\rangle = CNOT\frac{|0\rangle - |1\rangle}{\sqrt{2}}|1\rangle = CNOT\frac{|01\rangle - |11\rangle}{\sqrt{2}} = \frac{CNOT|01\rangle - CNOT|11\rangle}{\sqrt{2}} = \frac{|01\rangle - |10\rangle}{\sqrt{2}} = |\Psi^{-}\rangle$$
	**测量(measurement)**:
$$|\psi\rangle = c_{00}|00\rangle + c_{01}|01\rangle + c_{10}|10\rangle + c_{11}|11\rangle \Rightarrow \begin{cases}P(|00\rangle) = |c_{00}|^{2} \\ P(|01\rangle) = |c_{01}|^{2} \\ P(|10\rangle) = |c_{10}|^{2} \\ P(|11\rangle) = |c_{11}|^{2}\end{cases}$$
	**可分离态(separable state)**: 可以写成两个**单量子比特系统(single-qubit system)** 的**量子态(quantum state)** 的**张量积(tensor product)** 的**多量子比特系统(multi-qubit system)** 的**量子态(quantum state)** v.s. **纠缠态(entangled state)**: 不可以写成两个**单量子比特系统(single-qubit system)** 的**量子态(quantum state)** 的**张量积(tensor product)** 的**多量子比特系统(multi-qubit system)** 的**量子态(quantum state)**
**三量子比特系统(triple-qubit system)**: 八能级系统(eight-level system)
	**量子态(quantum state)**: **模** 为**1**的$2^{3} = 8$**维复列向量(complex column vector)**
$$|\psi\rangle = \sum_{s \in \{0, 1\}^{3}}c_{s}|s\rangle = c_{000}|000\rangle + c_{001}|001\rangle + c_{010}|010\rangle + c_{011}|011\rangle + c_{100}|100\rangle + c_{101}|101\rangle + c_{110}|110\rangle + c_{111}|111\rangle = c_{000}\begin{bmatrix}1 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0\end{bmatrix} + c_{001}\begin{bmatrix}0 \\ 1 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0\end{bmatrix} + c_{010}\begin{bmatrix}0 \\ 0 \\ 1 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0\end{bmatrix} + c_{011}\begin{bmatrix}0 \\ 0 \\ 0 \\ 1 \\ 0 \\ 0 \\ 0 \\ 0\end{bmatrix} + c_{100}\begin{bmatrix}0 \\ 0 \\ 0 \\ 0 \\ 1 \\ 0 \\ 0 \\ 0\end{bmatrix} + c_{101}\begin{bmatrix}0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 1 \\ 0 \\ 0\end{bmatrix} + c_{110}\begin{bmatrix}0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 1 \\ 0\end{bmatrix} + c_{111}\begin{bmatrix}0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 1\end{bmatrix} = \begin{bmatrix}c_{000} \\ 0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0\end{bmatrix} + \begin{bmatrix}0 \\ c_{001} \\ 0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0\end{bmatrix} + \begin{bmatrix}0 \\ 0 \\ c_{010} \\ 0 \\ 0 \\ 0 \\ 0 \\ 0\end{bmatrix} + \begin{bmatrix}0 \\ 0 \\ 0 \\ c_{011} \\ 0 \\ 0 \\ 0 \\ 0\end{bmatrix} + \begin{bmatrix}0 \\ 0 \\ 0 \\ 0 \\ c_{100} \\ 0 \\ 0 \\ 0\end{bmatrix} + \begin{bmatrix}0 \\ 0 \\ 0 \\ 0 \\ 0 \\ c_{101} \\ 0 \\ 0\end{bmatrix} + \begin{bmatrix}0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0 \\ c_{110} \\ 0\end{bmatrix} + \begin{bmatrix}0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0 \\ c_{111}\end{bmatrix} = \begin{bmatrix}c_{000} \\ c_{001} \\ c_{010} \\ c_{011} \\ c_{100} \\ c_{101} \\ c_{110} \\ c_{111}\end{bmatrix}$$
	(其中**态000(ket zero zero zero, $|000\rangle$ = $\begin{bmatrix}1 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0\end{bmatrix}$)**、**态001(ket zero zero one, $|001\rangle$ = $\begin{bmatrix}0 \\ 1 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0\end{bmatrix}$)**、**态010(ket zero zero one, $|010\rangle$ = $\begin{bmatrix}0 \\ 0 \\ 1 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0\end{bmatrix}$)**、**态011(ket zero one one, $|011\rangle$ = $\begin{bmatrix}0 \\ 0 \\ 0 \\ 1 \\ 0 \\ 0 \\ 0 \\ 0\end{bmatrix}$)**、**态100(ket one zero zero, $|100\rangle$ = $\begin{bmatrix}0 \\ 0 \\ 0 \\ 0 \\ 1 \\ 0 \\ 0 \\ 0\end{bmatrix}$)**、**态101(ket one zero one, $|101\rangle$ = $\begin{bmatrix}0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 1 \\ 0 \\ 0\end{bmatrix}$)**、**态110(ket one one zero, $|110\rangle$ = $\begin{bmatrix}0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 1 \\ 0\end{bmatrix}$)** 和**态111(ket one one one, $|111\rangle$ = $\begin{bmatrix}0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 1\end{bmatrix}$)** 为**标准基态(canonical/standard basis state)**；$c_{000}$, $c_{001}$, $c_{010}$, $c_{011}$, $c_{100}$, $c_{101}$, $c_{110}$, $c_{111}$为**振幅(amplitude)**，均为**复数(complex number)**(i.e. $c_{000}$, $c_{001}$, $c_{010}$, $c_{011}$, $c_{100}$, $c_{101}$, $c_{110}$, $c_{111}$ $\in$ $\mathbb{C}$)，**不全为0**(i.e. $c_{000}$ $\neq$ 0或$c_{001}$ $\neq$ 0或$c_{010}$ $\neq$ 0或$c_{011}$ $\neq$ 0或$c_{100}$ $\neq$ 0或$c_{101}$ $\neq$ 0或$c_{110}$ $\neq$ 0或$c_{111}$ $\neq$ 0)，且满足**归一化(normalization)** 条件(i.e. $|c_{000}|^{2} + |c_{001}|^{2} + |c_{010}|^{2} + |c_{011}|^{2} + |c_{100}|^{2} + |c_{101}|^{2} + |c_{110}|^{2} + |c_{111}|^{2} = \sum_{\mathbf{s} \in \{0, 1\}^{3}}|c_{\mathbf{s}}|^{2} = 1$))
	**测量(measurement)**: $$|\psi\rangle = c_{000}|000\rangle + c_{001}|001\rangle + c_{010}|010\rangle + c_{011}|011\rangle + c_{100}|100\rangle + c_{101}|101\rangle + c_{110}|110\rangle + c_{111}|111\rangle \Rightarrow \begin{cases}P(|000\rangle) = |c_{000}|^{2} \\ P(|001\rangle) = |c_{001}|^{2} \\ P(|010\rangle) = |c_{010}|^{2} \\ P(|011\rangle) = |c_{011}|^{2} \\ P(|100\rangle) = |c_{100}|^{2} \\ P(|101\rangle) = |c_{101}|^{2} \\ P(|110\rangle) = |c_{110}|^{2} \\ P(|111\rangle) = |c_{111}|^{2}\end{cases}$$
**n量子比特系统(n-qubit system)**: n能级系统(n-level system)
	**量子态(quantum state)**: **模(modulus)** 为**1**的$2^{n}$**维复列向量($2^{n}$-d complex column vector)**
$$|\psi\rangle = \sum_{s \in \{0, 1\}^{n}}c_{s}|s\rangle = c_{0\dots0}|0\dots0\rangle + c_{0\dots01}|0\dots01\rangle + \dots + c_{1\dots1}|1\dots1\rangle = c_{0\dots0}\begin{bmatrix}1 \\ 0 \\ \vdots \\ 0\end{bmatrix} + c_{0\dots01}\begin{bmatrix}0 \\ 1 \\ \vdots \\ 0\end{bmatrix} + \dots + c_{1\dots1}\begin{bmatrix}0 \\ 0 \\ \vdots \\ 1\end{bmatrix} = \begin{bmatrix}c_{0\dots0} \\ 0 \\ \vdots \\ 0\end{bmatrix} + \begin{bmatrix}0 \\ c_{0\dots01} \\ \vdots \\ 0\end{bmatrix} + \dots + \begin{bmatrix}0 \\ 0 \\ \vdots \\ c_{1\dots1}\end{bmatrix} = \begin{bmatrix}c_{0\dots0} \\ c_{0\dots01} \\ \vdots \\ c_{1\dots1}\end{bmatrix}$$
	(其中**态0...0(ket zero ... zero, $|0\dots0\rangle$ = $\begin{bmatrix}1 \\ 0 \\ \vdots \\ 0\end{bmatrix}$)**, **态0...01(ket zero ... zero one, $|0\dots01\rangle$ = $\begin{bmatrix}0 \\ 1 \\ 0 \\ \vdots \\ 0\end{bmatrix})$**, $\dots$, **态1...1(ket one ... one, $|1\dots1\rangle$ = $\begin{bmatrix}0 \\ \vdots \\ 0 \\ 1\end{bmatrix}$)** 为**标准基态(canonical/standard basis state)**；$c_{0\dots0}$, $c_{0\dots01}$, $\dots$, $c_{1\dots1}$为**振幅(amplitude)**，均为**复数(complex number)**(i.e. $c_{0\dots0}$, $c_{0\dots01}$, $\dots$, $c_{1\dots1}$ $\in$ $\mathbb{C}$)，**不全为0**(i.e. $c_{0\dots0}$ $\neq$ 0或$c_{0\dots01}$ $\neq$ 0或$\dots$或$c_{1\dots1}$ $\neq$ 0)，且满足**归一化(normalization)** 条件(i.e. $|c_{0\dots0}|^{2} + |c_{0\dots01}|^{2} + |c_{1\dots1}|^{2} = \sum_{\mathbf{s} \in \{0, 1\}}^{n}|c_{\mathbf{s}}|^{2} = 1$))
	**测量(measurement)**:
$$\begin{cases}P(|0\dots0\rangle) = |c_{0\dots0}|^{2} \\ P(|0\dots01\rangle) = |c_{0\dots01}|^{2} \\ \dots \\ P(|1\dots1\rangle) = |c_{1\dots1}|^{2}\end{cases}$$

**量子门(quantum gate)**: **酉变换(unitary transformation)**
**一元量子门(single-qubit quantum gate)**: 2 $\times$ 2**酉矩阵(unitary matrix)**
	**恒等门(identity gate)**/**I门(I gate)**: $|0\rangle$和$|1\rangle$均不变
$$I|x\rangle = |x\rangle(\text{其中}x \in \{0, 1\}) = \begin{cases}I|0\rangle = |0\rangle \\ I|1\rangle = |1\rangle\end{cases} \Rightarrow I(\alpha|0\rangle + \beta|1\rangle) \stackrel{\text{linearity}}{=} \alpha I|0\rangle + \beta I|1\rangle = \alpha|0\rangle + \beta|1\rangle$$
		**矩阵表示(matrix representation)**: **二阶单位(矩)阵(second-order identity matrix, $I_{2}$)**
$$I = I_{2} = \begin{bmatrix}1 & 0 \\ 0 & 1\end{bmatrix}$$
			证明(proof):
$$I = \begin{bmatrix}I|0\rangle & I|1\rangle\end{bmatrix} = \begin{bmatrix}|0\rangle & |1\rangle\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & 1\end{bmatrix}$$
		**算子表示(operator representation)**:
$$I = |0\rangle\langle0| + |1\rangle\langle1| = |+\rangle\langle+| + |-\rangle\langle-|$$
			证明(proof):
$$|0\rangle\langle0| + |1\rangle\langle1| = \begin{bmatrix}1 \\ 0\end{bmatrix}\begin{bmatrix}1 & 0\end{bmatrix} + \begin{bmatrix}0 \\ 1\end{bmatrix}\begin{bmatrix}0 & 1\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & 0\end{bmatrix} + \begin{bmatrix}0 & 0 \\ 0 & 1\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & 1\end{bmatrix}$$
$$|+\rangle\langle+| + |-\rangle\langle-| = \begin{bmatrix}\frac{1}{\sqrt{2}} \\ \frac{1}{\sqrt{2}}\end{bmatrix}\begin{bmatrix}\frac{1}{\sqrt{2}} & \frac{1}{\sqrt{2}}\end{bmatrix} + \begin{bmatrix}\frac{1}{\sqrt{2}} \\ -\frac{1}{\sqrt{2}}\end{bmatrix}\begin{bmatrix}\frac{1}{\sqrt{2}} & -\frac{1}{\sqrt{2}}\end{bmatrix} = \begin{bmatrix}\frac{1}{2} & \frac{1}{2} \\ \frac{1}{2} & \frac{1}{2}\end{bmatrix} + \begin{bmatrix}\frac{1}{2} & -\frac{1}{2} \\ -\frac{1}{2} & \frac{1}{2}\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & 1\end{bmatrix}$$
	**(泡利-)X门((Pauli-)X gate)**: $|0\rangle$变$|1\rangle$, $|1\rangle$变$|0\rangle$
$$X|x\rangle = |\lnot x\rangle(\text{其中}x \in \{0, 1\}) = \begin{cases}X|0\rangle = |1\rangle \\ X|1\rangle = |0\rangle\end{cases} \Rightarrow X(\alpha|0\rangle + \beta|1\rangle) \stackrel{\text{linearity}}{=} \alpha X|0\rangle + \beta X|1\rangle= \alpha|1\rangle + \beta|0\rangle = \beta|0\rangle + \alpha|1\rangle$$
		**矩阵表示(matrix representation)**: **泡利矩阵(Pauli matrix)**$\sigma_{x}$/$\sigma_{1}$
$$X = \sigma_{X} = \sigma_{1} = \begin{bmatrix} 0 & 1 \\ 1 & 0\end{bmatrix}$$
			证明(proof):
$$X = \begin{bmatrix}X|0\rangle & X|1\rangle\end{bmatrix} = \begin{bmatrix}|1\rangle & |0\rangle\end{bmatrix} = \begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix}$$
		**算子表示(operator representation)**:
$$X = |1\rangle\langle0| + |0\rangle\langle1| = |+\rangle\langle+| - |-\rangle\langle-|$$
			证明(proof):
$$|1\rangle\langle0| + |0\rangle\langle1| = \begin{bmatrix}0 \\ 1\end{bmatrix}\begin{bmatrix}1 & 0\end{bmatrix} + \begin{bmatrix}1 \\ 0\end{bmatrix}\begin{bmatrix}0 & 1\end{bmatrix} = \begin{bmatrix}0 & 0 \\ 1 & 0\end{bmatrix} + \begin{bmatrix}0 & 1 \\ 0 & 0\end{bmatrix} = \begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix}$$
$$|+\rangle\langle+| - |-\rangle\langle-| = \begin{bmatrix}\frac{1}{\sqrt{2}} \\ \frac{1}{\sqrt{2}}\end{bmatrix}\begin{bmatrix}\frac{1}{\sqrt{2}} & \frac{1}{\sqrt{2}}\end{bmatrix} - \begin{bmatrix}\frac{1}{\sqrt{2}} \\ -\frac{1}{\sqrt{2}}\end{bmatrix}\begin{bmatrix}\frac{1}{\sqrt{2}} & -\frac{1}{\sqrt{2}}\end{bmatrix} = \begin{bmatrix}\frac{1}{2} & \frac{1}{2} \\ \frac{1}{2} & \frac{1}{2}\end{bmatrix} - \begin{bmatrix}\frac{1}{2} & -\frac{1}{2} \\ -\frac{1}{2} & \frac{1}{2}\end{bmatrix} = \begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix}$$
		**X门(X gate)** 进行的**酉变换(unitary transformation)** 是将**量子态(quantum state)** 的**纯态(pure state)** 在**布洛赫球(Bloch sphere)** 上绕**x轴(x-axis)旋转(rotate)**$180^{\circ}$的 **旋转变换(rotation transformation)**
			证明(proof):
$$X(|0\rangle\cos{\frac{\theta}{2}} + e^{i\phi}|1\rangle\sin{\frac{\theta}{2}}) = X|0\rangle\cos{\frac{\theta}{2}} + e^{i\phi}X|1\rangle\sin{\frac{\theta}{2}} = |1\rangle\cos{\frac{\theta}{2}} + e^{i\phi}|0\rangle\sin{\frac{\theta}{2}} = e^{i\phi}|0\rangle\sin{\frac{\theta}{2}} + |1\rangle\cos{\frac{\theta}{2}} = e^{i\phi}(|0\rangle + e^{-i\phi}|1\rangle\sin{\frac{\theta}{2}}) \stackrel{\text{discard global amplitude $e^{-i\phi}$ will not change the probability distribution of measurement results}}{\equiv} = |0\rangle\sin{\frac{\theta}{2}} + e^{-i\phi}|1\rangle\cos{\frac{\theta}{2}} = |0\rangle\cos(\frac{\pi}{2} - \frac{\theta}{2}) + e^{-i\phi}|1\rangle\sin(\frac{\pi}{2} - \frac{\theta}{2}) = |0\rangle\cos{\frac{\pi - \theta}{2}} + e^{-i\phi}|1\rangle\sin{\frac{\pi - \theta}{2}}$$
$$\begin{cases}x = r\sin{\theta}\cos{\phi} = \sin{\theta}\cos{\phi} \\ y = r\sin{\theta}\sin{\phi} = \sin{\theta}\sin{\phi} \\ z = r\cos{\theta} = \cos{\theta}\end{cases} \rightarrow \begin{cases}x^{'} = r\sin(\pi - \theta)\cos(-\phi) = \sin{\theta}\cos{\phi} = x\\ y^{'} = r\sin(\pi - \theta)\sin(-\phi) = -\sin{\theta}\sin{\phi} = -y \\ z^{'} = r\cos(\pi -\theta) = -\cos{\theta} = -z\end{cases}$$
	(推广)**$R_{x}$门($R_{x}$ gate)**:
		**矩阵表示(matrix representation)**:
$$R_{x}(\varphi) = \begin{bmatrix}\cos{\frac{\varphi}{2}} & -i\sin{\frac{\varphi}{2}} \\ -i\sin{\frac{\varphi}{2}} & \cos{\frac{\varphi}{2}}\end{bmatrix} = I\cos{\frac{\varphi}{2}} - iX\sin{\frac{\varphi}{2}} = e^{-i\frac{\varphi}{2}X}$$
			证明(proof): 略
		**性质(property)1**:
$$R_{x}(0) = I$$
			证明(proof):
$$R_{x}(0) = \begin{bmatrix}\cos{0} & -i\sin{0} \\ -i\sin{0} & \cos{0}\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & 1\end{bmatrix} = I$$
		**性质(property)2**:
$$R_{x}(\varphi + \varphi^{'}) = R_{x}(\varphi)R_{x}(\varphi^{'})$$
			证明(proof):
$$R_{x}(\varphi)R_{x}(\varphi^{'}) = \begin{bmatrix}\cos{\frac{\varphi}{2}} & -i\sin{\frac{\varphi}{2}} \\ -i\sin{\frac{\varphi}{2}} & \cos{\frac{\varphi}{2}}\end{bmatrix}\begin{bmatrix}\cos{\frac{\varphi^{'}}{2}} & -i\sin{\frac{\varphi^{'}}{2}} \\ -i\sin{\frac{\varphi^{'}}{2}} & \cos{\frac{\varphi^{'}}{2}}\end{bmatrix} = \begin{bmatrix}\cos{\frac{\varphi}{2}}\cos{\frac{\varphi^{'}}{2}} + i^{2}\sin{\frac{\varphi}{2}}\sin{\frac{\varphi^{'}}{2}} & -i\sin{\frac{\varphi}{2}}\cos{\frac{\varphi^{'}}{2}} - i\cos{\frac{\varphi}{2}}\sin{\frac{\varphi^{'}}{2}} \\ -i\sin{\frac{\varphi}{2}}\cos{\frac{\varphi^{'}}{2}} - i\cos{\frac{\varphi}{2}}\sin{\frac{\varphi^{'}}{2}} & \cos{\frac{\varphi}{2}}\cos{\frac{\varphi^{'}}{2}} + i^{2}\sin{\frac{\varphi}{2}}\sin{\frac{\varphi^{'}}{2}}\end{bmatrix} = \begin{bmatrix}\cos{\frac{\varphi}{2}}\cos{\frac{\varphi^{'}}{2}} - \sin{\frac{\varphi}{2}}\sin{\frac{\varphi^{'}}{2}} & -i\sin{\frac{\varphi}{2}}\cos{\frac{\varphi^{'}}{2}} - i\cos{\frac{\varphi}{2}}\sin{\frac{\varphi^{'}}{2}} \\ -i\sin{\frac{\varphi}{2}}\cos{\frac{\varphi^{'}}{2}} - i\cos{\frac{\varphi}{2}}\sin{\frac{\varphi^{'}}{2}} & \cos{\frac{\varphi}{2}}\cos{\frac{\varphi^{'}}{2}} - \sin{\frac{\varphi}{2}}\sin{\frac{\varphi^{'}}{2}}\end{bmatrix} = \begin{bmatrix}\cos{\frac{\varphi + \varphi^{'}}{2}} & -i\sin{\frac{\varphi + \varphi^{'}}{2}} \\ -i\sin{\frac{\varphi + \varphi^{'}}{2}} & \cos{\frac{\varphi + \varphi^{'}}{2}}\end{bmatrix} = R_{x}(\varphi + \varphi^{'})$$
		**$R_{x}$门($R_{x}$ gate)** 进行的**酉变换(unitary transformation)** 是将**量子态(quantum state)** 的**纯态(pure state)** 在**布洛赫球(Bloch sphere)** 上绕**x轴(axis)旋转(rotate)** **任意度(degree)** 的**旋转变换(rotation transformation)**
			证明(proof): 略
	**(泡利-)Y门((Pauli-)Y gate)**:
$$Y|x\rangle = (-1)^{x}i|\lnot x\rangle(\text{其中}x \in \{0, 1\}) = \begin{cases}Y|0\rangle = i|1\rangle \\ Y|1\rangle = -i|0\rangle\end{cases} \Rightarrow Y(\alpha|0\rangle + \beta|1\rangle) = \alpha Y|0\rangle + \beta Y|1\rangle = \alpha i|1\rangle - \beta i|0\rangle = -\beta i|0\rangle + \alpha i|1\rangle$$
		**矩阵表示(matrix representation)**: 
$$Y = \sigma_{y} = \sigma_{2} = \begin{bmatrix}0 & -i \\ i & 0\end{bmatrix}$$
			证明(proof):
$$Y = \begin{bmatrix}Y|0\rangle & Y|1\rangle\end{bmatrix} = \begin{bmatrix}i|1\rangle & -i|0\rangle\end{bmatrix} = \begin{bmatrix}0 & -i \\ i & 0\end{bmatrix}$$
		**算子表示(operator representation)**:
$$Y = |+i\rangle\langle+i| - |-i\rangle\langle-i|$$
			证明(proof):
$$|+i\rangle\langle+i| - |-i\rangle\langle-i| = \begin{bmatrix}\frac{1}{\sqrt{2}} \\ \frac{i}{\sqrt{2}}\end{bmatrix}\begin{bmatrix}\frac{1}{\sqrt{2}} & -\frac{i}{\sqrt{2}}\end{bmatrix} - \begin{bmatrix}\frac{1}{\sqrt{2}} \\ -\frac{i}{\sqrt{2}}\end{bmatrix}\begin{bmatrix}\frac{1}{\sqrt{2}} & \frac{i}{\sqrt{2}}\end{bmatrix} = \begin{bmatrix}\frac{1}{2} & -\frac{i}{2} \\ \frac{i}{2} & -\frac{i^{2}}{2}\end{bmatrix} - \begin{bmatrix}\frac{1}{2} & \frac{i}{2} \\ -\frac{i}{2} & -\frac{i^{2}}{2}\end{bmatrix} = \begin{bmatrix}0 & -i \\ i & 0\end{bmatrix}$$
		**Y门(Y gate)** 进行的**酉变换(unitary transformation)** 是将**量子态(quantum state)** 的**纯态(pure state)** 在**布洛赫球(Bloch sphere)** 上绕**y轴(y-axis)旋转(rotate)** $180^{\circ}$的**旋转变换(rotation transformation)**
			证明(proof): 略
		**性质(property)1**: $Y = iXZ$
			证明(proof):
$$iXZ = i\begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix}\begin{bmatrix}1 & 0 \\ 0 & -1\end{bmatrix} = i\begin{bmatrix}0 & -1 \\ 1 & 0\end{bmatrix} = \begin{bmatrix}0 & -i \\ i & 0\end{bmatrix}$$
		**性质(property)2**: $XYX = -Y$
			证明(proof):
$$XYX = \begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix}\begin{bmatrix}0 & -i \\ i & 0\end{bmatrix}\begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix} = \begin{bmatrix}i & 0 \\ 0 & -i\end{bmatrix}\begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix} = \begin{bmatrix}0 & i \\ -i & 0\end{bmatrix} = -\begin{bmatrix}0 & -i \\ i & 0\end{bmatrix} = -Y$$
		**性质(property)3**: $XY = -YX$
			证明(proof):
$$XY + YX = \begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix}\begin{bmatrix}0 & -i \\ i & 0\end{bmatrix} + \begin{bmatrix}0 & -i \\ i & 0\end{bmatrix}\begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix} = \begin{bmatrix}i & 0 \\ 0 & -i\end{bmatrix} + \begin{bmatrix}-i & 0 \\ 0 & i\end{bmatrix} = \begin{bmatrix}0 & 0 \\ 0 & 0\end{bmatrix} = O \Leftrightarrow XY = -YX$$
	(推广)**$R_{y}$门($R_{y}$ gate)**:
		**矩阵表示(matrix representation)**:
$$R_{y}(\varphi) = \begin{bmatrix}\cos{\frac{\varphi}{2}} & -\sin{\frac{\varphi}{2}} \\ \sin{\frac{\varphi}{2}} & \cos{\frac{\varphi}{2}}\end{bmatrix} = I\cos{\frac{\varphi}{2}} - iY\sin{\frac{\varphi}{2}} = e^{-i\frac{\varphi}{2}Y}$$
			证明(proof): 略
		**性质(property)1**:
$$R_{y}(0) = I$$
			证明(proof):
$$R_{y}(0) = \begin{bmatrix}\cos{0} & -\sin{0} \\ \sin{0} & \cos{0}\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & 1\end{bmatrix} = I$$
		**性质(property)2**:
$$R_{y}(\varphi + \varphi^{'}) = R_{y}(\varphi)R_{y}(\varphi^{'})$$
			证明(proof):
$$R_{y}(\varphi)R_{y}(\varphi) = \begin{bmatrix}\cos{\frac{\varphi}{2}} & -\sin{\frac{\varphi}{2}} \\ \sin{\frac{\varphi}{2}} & \cos{\frac{\varphi}{2}}\end{bmatrix}\begin{bmatrix}\cos{\frac{\varphi^{'}}{2}} & -\sin{\frac{\varphi^{'}}{2}} \\ \sin{\frac{\varphi^{'}}{2}} & \cos{\frac{\varphi^{'}}{2}}\end{bmatrix} = \begin{bmatrix}\cos{\frac{\varphi}{2}}\cos{\frac{\varphi^{'}}{2}} - \sin{\frac{\varphi}{2}}\sin{\frac{\varphi^{'}}{2}} & -\sin{\frac{\varphi}{2}\cos{\frac{\varphi^{'}}{2}} - \cos{\frac{\varphi}{2}}}\sin{\frac{\varphi^{'}}{2}} \\ \sin{\frac{\varphi}{2}\cos{\frac{\varphi^{'}}{2}}} + \cos{\frac{\varphi}{2}}\sin{\frac{\varphi^{'}}{2}} & \cos{\frac{\varphi}{2}}\cos{\frac{\varphi^{'}}{2}} - \sin{\frac{\varphi}{2}}\sin{\frac{\varphi^{'}}{2}}\end{bmatrix} = \begin{bmatrix}\cos{\frac{\varphi + \varphi^{'}}{2}} & -\sin{\frac{\varphi + \varphi^{'}}{2}} \\ \sin{\frac{\varphi + \varphi^{'}}{2}} & \cos{\frac{\varphi + \varphi^{'}}{2}}\end{bmatrix} = R_{y}(\varphi + \varphi^{'})$$
		**性质(property)3**:
$$XR_{y}(\varphi)X = R_{y}(-\varphi)$$
			证明(proof):
$$XR_{y}(\varphi)X = \begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix}\begin{bmatrix}\cos{\frac{\varphi}{2}} & -\sin{\frac{\varphi}{2}} \\ \sin{\frac{\varphi}{2}} & \cos{\frac{\varphi}{2}}\end{bmatrix}\begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix} = \begin{bmatrix}\sin{\frac{\varphi}{2}} & \cos{\frac{\varphi}{2}} \\ \cos{\frac{\varphi}{2}} & -\sin{\frac{\varphi}{2}}\end{bmatrix}\begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix} = \begin{bmatrix}\cos{\frac{\varphi}{2}} & \sin{\frac{\varphi}{2}} \\ -\sin{\frac{\varphi}{2}} & \cos{\frac{\varphi}{2}}\end{bmatrix} = \begin{bmatrix}\cos{(-\frac{\varphi}{2})} & -\sin{(-\frac{\varphi}{2})} \\ \sin{(-\frac{\varphi}{2})} & \cos{(-\frac{\varphi}{2})}\end{bmatrix} = R_{x}(-\varphi)$$
		$R_{y}$门($R_{y}$ gate)进行的**酉变换(unitary transformation)** 是将**量子态(quantum state)** 的**纯态(pure state)** 在**布洛赫球(Bloch sphere)** 上绕**y轴(y-axis)旋转(rotate)任意度(degree)** 的**旋转变换(rotation transformation)**
	**(泡利-)Z门((Pauli-)Z gate)**: $|0\rangle$不变，$|1\rangle$变$-|1\rangle$
$$Z|x\rangle = (-1)^{x}|x\rangle(\text{其中}x \in \{0, 1\}) = \begin{cases}Z|0\rangle = |0\rangle \\ Z|1\rangle = -|1\rangle\end{cases} \Rightarrow Z(\alpha|0\rangle + \beta|1\rangle) \stackrel{\text{linearity}}{=} \alpha Z|0\rangle + \beta Z|1\rangle = \alpha|0\rangle - \beta|1\rangle$$
		**矩阵表示(matrix representation)**: **泡利矩阵(Pauli matrix)**$\sigma_{z}$/$\sigma_{3}$
$$Z = \sigma_{z} = \sigma_{3} = \begin{bmatrix}1 & 0 \\ 0 & - 1\end{bmatrix}$$
			证明(proof):
$$Z = \begin{bmatrix}Z|0\rangle & Z|1\rangle\end{bmatrix} = \begin{bmatrix}|0\rangle & -|1\rangle\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & -1\end{bmatrix}$$
		**算子表示(operator representation)**:
$$Z = |0\rangle\langle0| - |1\rangle\langle1|$$
			证明(proof):
$$|0\rangle\langle0| - |1\rangle\langle1| = \begin{bmatrix}1 \\ 0\end{bmatrix}\begin{bmatrix}1 & 0\end{bmatrix} - \begin{bmatrix}0 \\ 1\end{bmatrix}\begin{bmatrix}0 & 1\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & 0\end{bmatrix} - \begin{bmatrix}0 & 0 \\ 0 & 1\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & -1\end{bmatrix} = $$
		**Z门(X gate)** 进行的**酉变换(unitary transformation)** 是将**量子态(quantum state)** 的**纯态(pure state)** 在**布洛赫球(Bloch sphere)** 上绕**z轴(z-axis)旋转(rotate)**$180^{\circ}$的**旋转变换(rotation transformation)**
			证明(proof):
$$Z(|0\rangle\cos{\frac{\theta}{2}} + e^{i\phi}|1\rangle\sin{\frac{\theta}{2}}) = Z|0\rangle\cos{\frac{\theta}{2}} + e^{i\phi}Z|1\rangle\sin{\frac{\theta}{2}} = |0\rangle\cos{\frac{\theta}{2}} - e^{i\phi}|1\rangle\sin{\frac{\theta}{2}} = |0\rangle\cos{\frac{\theta}{2}} + e^{i(\pi + \phi)}|1\rangle$$
$$\begin{cases}x = r\sin{\theta}\cos{\phi} = \sin{\theta}\cos{\phi} \\ y = r\sin{\theta}\sin{\phi} = \sin{\theta}\sin{\phi} \\ z = r\cos{\theta} = \cos{\theta}\end{cases} \rightarrow \begin{cases}x^{'} = r\sin{\theta}\cos(\pi + \phi) = -\sin{\theta}\cos{\phi} = -x \\ y^{'} = r\sin{\theta}\sin(\pi + \phi) = -\sin{\theta}\sin{\phi} = -y \\ z^{'} = r\cos{\theta} = z\end{cases}$$
			**性质(property)**: $XZX = -Z$
$$XZX = \begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix}\begin{bmatrix}1 & 0 \\ 0 & -1\end{bmatrix}\begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix} = \begin{bmatrix}0 & -1 \\ 1 & 0\end{bmatrix}\begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix} = \begin{bmatrix}-1 & 0 \\ 0 & 1\end{bmatrix} = -\begin{bmatrix}1 & 0 \\ 0 & -1\end{bmatrix} = -Z$$
	(推广)**$R_{z}$门($R_{z}$ gate)**:
		**矩阵表示(matrix representation)**:
$$R_{z}(\varphi) = \begin{bmatrix}e^{-i\frac{\varphi}{2}} & 0 \\ 0 & e^{i\frac{\varphi}{2}}\end{bmatrix} = I\cos{\frac{\varphi}{2}} - iZ\sin{\frac{\varphi}{2}} = e^{-i\frac{\varphi}{2}Z}$$
		**性质(property)1**:
$$R_{z}(0) = I$$
			证明(proof):
$$R_{z}(0) = \begin{bmatrix}e^{0} & 0 \\ 0 & e^{0}\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & 1\end{bmatrix} = I$$
		**性质(property)2**:
$$R_{z}(\varphi + \varphi^{'}) = R_{z}(\varphi)R_{z}(\varphi^{'})$$
			证明(proof):
$$R_{z}(\varphi)R_{z}(\varphi^{'}) = \begin{bmatrix}e^{-i\frac{\varphi}{2}} & 0 \\ 0 & e^{i\frac{\varphi}{2}}\end{bmatrix}\begin{bmatrix}e^{-i\frac{\varphi^{'}}{2}} & 0 \\ 0 & e^{i\frac{\varphi^{'}}{2}}\end{bmatrix} = \begin{bmatrix}e^{-i\frac{\varphi + \varphi^{'}}{2}} & 0 \\ 0 & e^{i\frac{\varphi + \varphi^{'}}{2}}\end{bmatrix} = R_{z}(\varphi + \varphi^{'})$$
		**性质(property)3**:
$$XR_{z}(\varphi)X = R_{z}(-\varphi)$$
			证明(proof):
$$XR_{z}(\varphi)X = \begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix}\begin{bmatrix}e^{-i\frac{\varphi}{2}} & 0 \\ 0 & e^{i\frac{\varphi}{2}}\end{bmatrix}\begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix} = \begin{bmatrix}0 & e^{i\frac{\varphi}{2}} \\ e^{-i\frac{\varphi}{2}} & 0\end{bmatrix}\begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix} = \begin{bmatrix}e^{i\frac{\varphi}{2}} & 0 \\ 0 & e^{-i\frac{\varphi}{2}}\end{bmatrix} = \begin{bmatrix}e^{-i(-\frac{\varphi}{2})} & 0 \\ 0 & e^{i(-\frac{\varphi}{2})}\end{bmatrix} = R_{z}(-\varphi)$$
		$R_{z}$门($R_{z}$ gate)进行的**酉变换(unitary matrix)** 是将**量子态(quantum state)** 的**纯态(pure state)** 在**布洛赫球(Bloch sphere)** 上绕**z轴(axis)旋转(rotate)任意度(degree)** 的**旋转变换(rotation transformation)**
	**S门(S gate)**: $|0\rangle$不变，$|1\rangle$变$i|1\rangle$
$$S|x\rangle = i^{x}|x\rangle(\text{其中}x \in \{0, 1\}) = \begin{cases}S|0\rangle = |0\rangle \\ S|1\rangle = i|1\rangle\end{cases} \Rightarrow S|\psi\rangle = S(\alpha|0\rangle + \beta|1\rangle) \stackrel{\text{linearity}}{=} \alpha S|0\rangle + \beta S|1\rangle = \alpha|0\rangle + \beta i|1\rangle$$
		**矩阵表示(matrix representation)**:
$$S = \begin{bmatrix}1 & 0 \\ 0 & i\end{bmatrix}$$
			证明(proof):
$$S = \begin{bmatrix}S|0\rangle & S|1\rangle\end{bmatrix} = \begin{bmatrix}|0\rangle & i|1\rangle\end{bmatrix} = \begin{bmatrix}1 & 0\\ 0 & i\end{bmatrix}$$
		**算子表示(operator representation)**:
$$S = |0\rangle\langle0| + i|1\rangle\langle1|$$
			证明(proof):
$$|0\rangle\langle0| + i|1\rangle\langle1| = \begin{bmatrix}1 \\ 0\end{bmatrix}\begin{bmatrix}1 & 0\end{bmatrix} + i\begin{bmatrix}0 \\ 1\end{bmatrix}\begin{bmatrix}0 & 1\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & 0\end{bmatrix} + i\begin{bmatrix}0 & 0 \\ 0 & 1\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & 0\end{bmatrix} + \begin{bmatrix}0 & 0 \\ 0 & i\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & i\end{bmatrix}$$
		**S门(S gate)** 进行的**酉变换(unitary transformation)** 是将**量子态(quantum state)** 的**纯态(pure state)** 在**布洛赫球(Bloch sphere)** 上绕**z轴(z-axis)旋转(rotate)**$90^{\circ}$ 的**旋转变换(rotation transformation)**
			证明(proof):
$$S = \begin{bmatrix}1 & 0 \\ 0 & i\end{bmatrix} = \begin{bmatrix}e^{i0} & 0 \\ 0 & e^{i\frac{\pi}{2}}\end{bmatrix} = e^{i\frac{\pi}{4}}\begin{bmatrix}e^{-i\frac{\pi}{4}} & 0 \\ 0 & e^{i\frac{\pi}{4}}\end{bmatrix} = e^{i\frac{\pi}{4}}R_{z}(\frac{\pi}{2})$$
	**T门(T gate)**: $|0\rangle$不变，$|1\rangle$变$e^{i\frac{\pi}{4}}|1\rangle$
$$T|x\rangle = e^{xi\frac{\pi}{4}}|x\rangle(\text{其中}x \in \{0, 1\}) = \begin{cases}T|0\rangle = |0\rangle \\ T|1\rangle = e^{i\frac{\pi}{4}}|1\rangle\end{cases} \Rightarrow T|\psi\rangle = T(\alpha|0\rangle + \beta|1\rangle) \stackrel{linearity}{=} \alpha T|0\rangle + \beta T|1\rangle = \alpha|0\rangle + \beta e^{i\frac{\pi}{4}}|1\rangle$$
		**矩阵表示(matrix representation)**:
$$T = \begin{bmatrix}1 & 0 \\ 0 & e^{\frac{i\pi}{4}}\end{bmatrix}$$
			证明(proof):
$$T = \begin{bmatrix}T|0\rangle & T|1\rangle\end{bmatrix} = \begin{bmatrix}|0\rangle & e^{i\frac{\pi}{4}}|1\rangle\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & e^{i\frac{\pi}{4}}\end{bmatrix}$$
		**算子表示(operator representation)**:
$$T = |0\rangle\langle0| + e^{i\frac{\pi}{4}}|1\rangle\langle1|$$
			证明(proof):
$$|0\rangle\langle0| + e^{i\frac{\pi}{4}}|1\rangle\langle1| = \begin{bmatrix}1 \\ 0\end{bmatrix}\begin{bmatrix}1 & 0\end{bmatrix} + e^{i\frac{\pi}{4}}\begin{bmatrix}0 \\ 1\end{bmatrix}\begin{bmatrix}0 & 1\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & 0\end{bmatrix} + e^{i\frac{\pi}{4}}\begin{bmatrix}0 & 0 \\ 0 & 1\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & 0\end{bmatrix} + \begin{bmatrix}0 & 0 \\ 0 & e^{i\frac{\pi}{4}}\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & e^{i\frac{\pi}{4}}\end{bmatrix}$$
		**T门(T gate)** 进行的**酉变换(unitary transformation)** 是将**量子态(quantum state)** 的**纯态(pure state)** 在**布洛赫球(Bloch sphere)** 上绕**z轴(z-axis)旋转(rotate)**$45^{\circ}$的**旋转变换(rotation transformation)**
			证明(proof):
$$T = \begin{bmatrix}1 & 0 \\ 0 & e^{i\frac{\pi}{4}}\end{bmatrix} = e^{i\frac{\pi}{8}}\begin{bmatrix}e^{-i\frac{\pi}{8}} & 0 \\ 0 & e^{i\frac{\pi}{8}}\end{bmatrix} = e^{i\frac{\pi}{8}}R_{z}(\frac{\pi}{4})$$
	(推广)**相位偏移门(phase shift gate)**/**R门(R gate)**: $|0\rangle$不变，$|1\rangle$变$e^{i\theta}|1\rangle$
$$R(\theta)|x\rangle = e^{xi\theta}|x\rangle(\text{其中}x \in \{0, 1\}) = \begin{cases}R(\theta)|0\rangle = |0\rangle \\ R(\theta)|1\rangle = e^{i\theta}|1\rangle\end{cases} \Rightarrow R(\theta)|\psi\rangle = R(\theta)(\alpha|0\rangle + \beta|1\rangle) \stackrel{\text{linearity}}{=} \alpha R(\theta)|0\rangle + \beta R(\theta)|1\rangle = \alpha|0\rangle + \beta e^{i\theta}|1\rangle$$
		**矩阵表示(matrix representation)**: $|0\rangle$不变，$|1\rangle$变$e^{i\theta}|1\rangle$
$$R(\theta) = \begin{bmatrix}1 & 0 \\ 0 & e^{i\theta}\end{bmatrix}$$
			证明(proof):
$$R(\theta) = \begin{bmatrix}R(\theta)|0\rangle & R(\theta)|1\rangle\end{bmatrix} = \begin{bmatrix}|0\rangle & e^{i\theta}|1\rangle\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & e^{i\theta}\end{bmatrix}$$
		**算子表示(operator representation)**:
$$R(\theta) = |0\rangle\langle0| + e^{i\theta}|1\rangle\langle1|$$
			证明(proof):
$$|0\rangle\langle0| + e^{i\theta}|1\rangle\langle1| = \begin{bmatrix}1 \\ 0\end{bmatrix}\begin{bmatrix}1 & 0\end{bmatrix} + e^{i\theta}\begin{bmatrix}0 \\ 1\end{bmatrix}\begin{bmatrix}0 & 1\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & 0\end{bmatrix} + e^{i\theta}\begin{bmatrix}0 & 0 \\ 0 & 1\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & 0\end{bmatrix} + \begin{bmatrix}0 & 0 \\ 0 & e^{i\theta}\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & e^{i\theta}\end{bmatrix}$$
		**R门(R gate)** 进行的**酉变换(unitary transformation)** 是将**量子态(quantum state)** 的**纯态(pure state)** 在**布洛赫球(Bloch sphere)** 上绕**z轴(z-axis)旋转(rotate)**$\theta$**弧度(radian)旋转变换(rotation transformation)**
			证明(proof):
$$R(\theta) = \begin{bmatrix}1 & 0 \\ 0 & e^{i\theta}\end{bmatrix} = e^{i\frac{\theta}{2}}\begin{bmatrix}e^{-i\frac{\theta}{2}} & 0 \\ 0 & e^{i\frac{\theta}{2}}\end{bmatrix} = e^{i\frac{\theta}{2}}R_{z}(\theta)$$
	**阿达马门/H门(Hadamard gate, H gate)**: $|0\rangle$变$|+\rangle$，$|1\rangle$变$|-\rangle$
$$H|x\rangle = \frac{|0\rangle + (-1)^{x}|1\rangle}{\sqrt{2}}(\text{其中}x \in \{0, 1\}) = \begin{cases}H|0\rangle = \frac{|0\rangle + |1\rangle}{\sqrt{2}} = |+\rangle \\ H|1\rangle = \frac{|0\rangle - |1\rangle}{\sqrt{2}} = |-\rangle\end{cases} \Rightarrow H|\psi\rangle = H(\alpha|0\rangle + \beta|1\rangle) \stackrel{\text{linearity}}{=} \alpha H|0\rangle + \beta H|1\rangle = \alpha\frac{|0\rangle + |1\rangle}{\sqrt{2}} + \beta\frac{|0\rangle - |1\rangle}{\sqrt{2}} = \frac{\alpha + \beta}{\sqrt{2}}|0\rangle + \frac{\alpha - \beta}{\sqrt{2}}|1\rangle$$
		**矩阵表示(matrix representation)**:
$$H = \frac{1}{\sqrt{2}}\begin{bmatrix}1 & 1 \\ 1 & -1\end{bmatrix} = \begin{bmatrix}\frac{1}{\sqrt{2}} & \frac{1}{\sqrt{2}} \\ \frac{1}{\sqrt{2}} & -\frac{1}{\sqrt{2}}\end{bmatrix}$$
			证明(proof):
$$H = \begin{bmatrix}H|0\rangle & H|1\rangle\end{bmatrix} = \begin{bmatrix}|+\rangle & |-\rangle\end{bmatrix} = \begin{bmatrix}\frac{|0\rangle + |1\rangle}{\sqrt{2}} & \frac{|0\rangle - |1\rangle}{\sqrt{2}}\end{bmatrix} = \begin{bmatrix}\frac{\begin{bmatrix}1 \\ 0\end{bmatrix} + \begin{bmatrix}0 \\ 1\end{bmatrix}}{\sqrt{2}} & \frac{\begin{bmatrix}1 \\ 0\end{bmatrix} - \begin{bmatrix}0 \\ 1\end{bmatrix}}{\sqrt{2}}\end{bmatrix} = \begin{bmatrix}\frac{\begin{bmatrix}1 \\ 1\end{bmatrix}}{\sqrt{2}} & \frac{\begin{bmatrix}1 \\ -1\end{bmatrix}}{\sqrt{2}}\end{bmatrix} = \frac{1}{\sqrt{2}}\begin{bmatrix}1 & 1 \\ 1 & -1\end{bmatrix} = \begin{bmatrix}\frac{1}{\sqrt{2}} & \frac{1}{\sqrt{2}} \\ \frac{1}{\sqrt{2}} & -\frac{1}{\sqrt{2}}\end{bmatrix}$$
		**算子表示(operator representation)**:
$$H = |+\rangle\langle0| + |-\rangle\langle1| = |+H\rangle\langle+H| - |-H\rangle\langle-H|(\text{其中}\begin{cases}|+H\rangle = \frac{\sqrt{2 + \sqrt{2}}}{2}|0\rangle + \frac{\sqrt{2 - \sqrt{2}}}{2}|1\rangle = |0\rangle\cos{\frac{\pi}{8}} + |1\rangle\sin{\frac{\pi}{8}} \\ |-H\rangle = \frac{\sqrt{2 - \sqrt{2}}}{2}|0\rangle - \frac{\sqrt{2 + \sqrt{2}}}{2}|1\rangle = |0\rangle\cos{\frac{3\pi}{8}} - |1\rangle\sin{\frac{3\pi}{8}}\end{cases})$$
			证明(proof):
$$|+\rangle\langle0| + |-\rangle\langle1| = \begin{bmatrix}\frac{1}{\sqrt{2}} \\ \frac{1}{\sqrt{2}}\end{bmatrix}\begin{bmatrix}1 & 0\end{bmatrix} + \begin{bmatrix}\frac{1}{\sqrt{2}} \\ -\frac{1}{\sqrt{2}}\end{bmatrix}\begin{bmatrix}0 & 1\end{bmatrix} = \begin{bmatrix}\frac{1}{\sqrt{2}} & 0 \\ \frac{1}{\sqrt{2}} & 0\end{bmatrix} + \begin{bmatrix}0 & \frac{1}{\sqrt{2}} \\ 0 & -\frac{1}{\sqrt{2}}\end{bmatrix} = \begin{bmatrix}\frac{1}{\sqrt{2}} & \frac{1}{\sqrt{2}} \\ \frac{1}{\sqrt{2}} & -\frac{1}{\sqrt{2}}\end{bmatrix}$$
				略
	**阿达马门(Hadamard gate)** 进行的**酉变换(unitary matrix)** 是将**量子态(quantum state)** 的**纯态(pure state)** 在**布洛赫球(Bloch sphere)** 上绕**平面xOz的一、三象限角平分线旋转(rotate)**$180^{\circ}$的**旋转变换(rotation transformation)**
		**性质(property)1**:
$$HXH = Z$$
			证明(proof):
$$HXH = \frac{1}{\sqrt{2}}\begin{bmatrix}1 & 1 \\ 1 & -1\end{bmatrix}\begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix}\frac{1}{\sqrt{2}}\begin{bmatrix}1 & 1 \\ 1 & -1\end{bmatrix} = \frac{1}{2}\begin{bmatrix}1 & 1 \\ -1 & 1\end{bmatrix}\begin{bmatrix}1 & 1 \\ 1 & -1\end{bmatrix} = \frac{1}{2}\begin{bmatrix}2 & 0 \\ 0 & -2\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & -1\end{bmatrix} = Z$$
		**性质(property)2**:
$$HYH = -Y$$
			证明(proof):
$$HYH = \frac{1}{\sqrt{2}}\begin{bmatrix}1 & 1 \\ 1 & -1\end{bmatrix}\begin{bmatrix}0 & -i \\ i & 0\end{bmatrix}\frac{1}{\sqrt{2}}\begin{bmatrix}1 & 1 \\ 1 & -1\end{bmatrix} = \frac{1}{2}\begin{bmatrix}1 & 1 \\ 1 & -1\end{bmatrix}\begin{bmatrix}0 & -i \\ i & 0\end{bmatrix}\begin{bmatrix}1 & 1 \\ 1 & -1\end{bmatrix} = \frac{1}{2}\begin{bmatrix}i & -i \\ -i & -i\end{bmatrix}\begin{bmatrix}1 & 1 \\ 1 & -1\end{bmatrix} = \frac{1}{2}\begin{bmatrix}0 & 2i \\ -2i & 0\end{bmatrix} = \begin{bmatrix}0 & i \\ -i & 0\end{bmatrix} = -\begin{bmatrix}0 & -i \\ i & 0\end{bmatrix} = -Y$$
		**性质(property)3**:
$$HZH = X$$
			证明(proof):
$$HZH = \frac{1}{\sqrt{2}}\begin{bmatrix}1 & 1 \\ 1 & -1\end{bmatrix}\begin{bmatrix}1 & 0 \\ 0 & -1\end{bmatrix}\frac{1}{\sqrt{2}}\begin{bmatrix}1 & 1 \\ 1 & -1\end{bmatrix} = \frac{1}{2}\begin{bmatrix}1 & -1 \\ 1 & 1\end{bmatrix}\begin{bmatrix}1 & 1 \\ 1 & -1\end{bmatrix} = \frac{1}{2}\begin{bmatrix}0 & 2 \\ 2 & 0\end{bmatrix} = \begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix} = X$$
	注: **X门(X gate)、Y门(Y gate)、Z门(Z gate)和阿达马门(Hadamard gate)** 的**矩阵(matrix)** 均为**对合矩阵(involutory matrix)** 和**埃尔米特矩阵(Hermitian matrix)**
		证明(proof):
$$\begin{cases}X^{2} = XX = \begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix}\begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & 1\end{bmatrix} = I \\ X^{\dagger} = \begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix}^{\dagger} = \overline{\begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix}}^{T} = \begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix}^{T} = \begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix} = X\end{cases}$$$$\begin{cases}Y^{2} = YY = \begin{bmatrix}0 & -i \\ i & 0\end{bmatrix}\begin{bmatrix}0 & -i \\ i & 0\end{bmatrix} = \begin{bmatrix}-i^{2} & 0 \\ 0 & -i^{2}\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & 1\end{bmatrix} = I \\ Y^{\dagger} = \begin{bmatrix}0 & -i \\ i & 0\end{bmatrix}^{\dagger} = \overline{\begin{bmatrix}0 & -i \\ i & 0\end{bmatrix}}^{T} = \begin{bmatrix}0 & i \\ -i & 0\end{bmatrix}^{T} = \begin{bmatrix}0 & -i \\ i & 0\end{bmatrix} = Y\end{cases}$$ $$\begin{cases}Z^{2} = ZZ = \begin{bmatrix}1 & 0 \\ 0 & -1\end{bmatrix}\begin{bmatrix}1 & 0 \\ 0 & -1\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & 1\end{bmatrix} = I \\ Z^{\dagger} = \begin{bmatrix}1 & 0 \\ 0 & -1\end{bmatrix}^{\dagger} = \overline{\begin{bmatrix}1 & 0 \\ 0 & -1\end{bmatrix}}^{T} = \begin{bmatrix}1 & 0 \\ 0 & -1\end{bmatrix}^{T} = \begin{bmatrix}1 & 0 \\ 0 & -1\end{bmatrix} = Z\end{cases}$$
$$\begin{cases}H^{2} = HH = \frac{1}{\sqrt{2}}\begin{bmatrix}1 & 1 \\ 1 & -1\end{bmatrix}\frac{1}{\sqrt{2}}\begin{bmatrix}1 & 1 \\ 1 & -1\end{bmatrix} = \frac{1}{2}\begin{bmatrix}1 & 1 \\ 1 & -1\end{bmatrix}\begin{bmatrix}1 & 1 \\ 1 & -1\end{bmatrix} = \frac{1}{2}\begin{bmatrix}2 & 0 \\ 0 & 2\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & 1\end{bmatrix} = I \\ H^{\dagger} = (\frac{1}{\sqrt{2}}\begin{bmatrix}1 & 1 \\ 1 & -1\end{bmatrix})^{\dagger} = \frac{1}{\sqrt{2}}\begin{bmatrix}1 & 1 \\ 1 & -1\end{bmatrix}^{\dagger} = \frac{1}{\sqrt{2}}\overline{\begin{bmatrix}1 & 1 \\ 1 & -1\end{bmatrix}}^{T} = \frac{1}{\sqrt{2}}\begin{bmatrix}1 & 1 \\ 1 & -1\end{bmatrix}^{T} = \frac{1}{\sqrt{2}}\begin{bmatrix}1 & 1 \\ 1 & -1\end{bmatrix} = H\end{cases}$$
	(推广)**万能量子门(universal quantum gate)**——**U门(U gate)**:
		**矩阵表示(matrix representation)**:
$$U = \begin{bmatrix}u_{00} & u_{01} \\ u_{10} & u_{11}\end{bmatrix}$$
			证明(proof): 略
		**U门(U gate)** 进行的**酉变换(unitary transformation)** 是将**量子态(quantum state)** 的**纯态(pure state)** 在**布洛赫球(Bloch sphere)** 上绕**任意轴(axis)** 旋转**任意度(degree)** 的**旋转变换(rotation transformation)**
		**构造(construction)**: 根据**Z-Y-Z分解(Z-Y-Z decomposition)**，只需要先经过一个$R_{z}$**门($R_{z}$ gate)**，接着经过一个$R_{y}$**门($R_{y}$ gate)**，然后经过一个$R_{z}$**门($R_{z}$ gate)**，最后经过一个**R门(R gate)**
$$U = e^{i\alpha}R_{z}(\beta)R_{y}(\gamma)R_{z}(\delta) = e^{i\alpha}\begin{bmatrix}e^{-i\frac{\beta}{2}} & 0 \\ 0 & e^{i\frac{\beta}{2}}\end{bmatrix}\begin{bmatrix}\cos{\frac{\gamma}{2}} & -\sin{\frac{\gamma}{2}} \\ \sin{\frac{\gamma}{2}} & \cos{\frac{\gamma}{2}}\end{bmatrix}\begin{bmatrix}e^{-i\frac{\delta}{2}} & 0 \\ 0 & e^{i\frac{\delta}{2}}\end{bmatrix} = e^{i\alpha}\begin{bmatrix}e^{-i\frac{\beta}{2}}\cos{\frac{\gamma}{2}} & -e^{-i\frac{\beta}{2}}\sin{\frac{\gamma}{2}} \\ e^{i\frac{\beta}{2}}\sin{\frac{\gamma}{2}} & e^{i\frac{\beta}{2}}\cos{\frac{\gamma}{2}}\end{bmatrix}\begin{bmatrix}e^{-i\frac{\delta}{2}} & 0 \\ 0 & e^{i\frac{\delta}{2}}\end{bmatrix} = e^{i\alpha}\begin{bmatrix}e^{i(-\frac{\beta}{2} - \frac{\delta}{2})}\cos{\frac{\gamma}{2}} & -e^{i(-\frac{\beta}{2} + \frac{\delta}{2})}\sin{\frac{\gamma}{2}} \\ e^{i(\frac{\beta}{2} - \frac{\delta}{2})}\sin{\frac{\gamma}{2}} & e^{i(\frac{\beta}{2} + \frac{\delta}{2})}\cos{\frac{\gamma}{2}}\end{bmatrix} = \begin{bmatrix}e^{i(\alpha - \frac{\beta}{2} - \frac{\delta}{2})}\cos{\frac{\gamma}{2}} & -e^{i(\alpha - \frac{\beta}{2} + \frac{\gamma}{2})}\sin{\frac{\gamma}{2}} \\ e^{i(\alpha + \frac{\beta}{2} - \frac{\delta}{2})}\sin{\frac{\gamma}{2}} & e^{i(\alpha + \frac{\beta}{2} + \frac{\delta}{2})}\cos{\frac{\gamma}{2}}\end{bmatrix}$$
			例:
$$\text{当}\alpha = 0, \beta = -\frac{\pi}{2}, \delta = \frac{\pi}{2}\text{时, }U = R_{z}(-\frac{\pi}{2})R_{y}(\gamma)R_{z}(\frac{\pi}{2}) = \begin{bmatrix}\cos{\frac{\gamma}{2}} & -e^{\frac{\pi}{2}}\sin{\frac{\gamma}{2}} \\ e^{-i\frac{\pi}{2}}\sin{\frac{\gamma}{2}} & \cos{\frac{\gamma}{2}}\end{bmatrix} = \begin{bmatrix}\cos{\frac{\gamma}{2}} & -i\sin{\frac{\gamma}{2}} \\ -i\sin{\frac{\gamma}{2}} & \cos{\frac{\gamma}{2}}\end{bmatrix} = R_{x}(\gamma)$$
### 二、二元量子门(double-qubit quantum gate):
**控制非门(controlled-NOT gate, CNOT gate)**: 当**控制量子比特(control qubit)** 为$|1\rangle$时，**翻转(flip)目标量子比特(target qubit)**，即对**目标量子比特(target qubit)** 应用**X门(X gate)**，否则保持**目标量子比特(target qubit)** 不变，即对**目标量子比特(target qubit)** 应用**I门(I gate)**(n.b. **控制非门(controlled-NOT gate, CNOT gate)** 即**控制X门(controlled-X gate, CX gate)**)
	**第一个量子比特(qubit)** 为**控制量子比特(control qubit)**，**第二个量子比特(qubit)** 为**目标量子比特(target qubit)** 的**控制非门(controlled-NOT gate, CNOT gate)**:
$$CNOT|x, y\rangle = |x\rangle X^{x}|y\rangle = |x, x \oplus y\rangle(\text{其中}x, y \in \{0, 1\}) = \begin{cases}CNOT|00\rangle = |00\rangle \\ CNOT|01\rangle = |01\rangle \\ CNOT|10\rangle = |11\rangle \\ CNOT|11\rangle = |10\rangle\end{cases} \Rightarrow CNOT|\psi\rangle = CNOT(c_{00}|00\rangle + c_{01}|01\rangle + c_{10}|10\rangle + c_{11}|11\rangle) \stackrel{\text{linearity of linear transformation}}{=} c_{00}CNOT|00\rangle + c_{01}CNOT|01\rangle + c_{10}CNOT|10\rangle + c_{11}CNOT|11\rangle = c_{00}|00\rangle + c_{01}|01\rangle + c_{10}|11\rangle + c_{11}|10\rangle = c_{00}|00\rangle + c_{01}|01\rangle + c_{11}|01\rangle + c_{10}|11\rangle$$
		**矩阵表示(matrix representation)**:
$$CNOT = \begin{bmatrix}I \\ & X\end{bmatrix} = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 &  1 & 0\end{bmatrix}$$
			证明(proof):
$$CNOT = \begin{bmatrix}CNOT|00\rangle & CNOT|01\rangle & CNOT|10\rangle & CNOT|11\rangle\end{bmatrix} = \begin{bmatrix}|00\rangle & |01\rangle & |11\rangle & |10\rangle\end{bmatrix} = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0\end{bmatrix}$$
		**算子表示(operator representation)**:
$$CNOT = |0\rangle\langle0| \otimes I + |1\rangle\langle1| \otimes X$$
			证明(proof):
$$|0\rangle\langle0| \otimes I + |1\rangle\langle1| \otimes X = \begin{bmatrix}1 \\ 0\end{bmatrix}\begin{bmatrix}1 & 0\end{bmatrix} \otimes I + \begin{bmatrix}0 \\ 1\end{bmatrix}\begin{bmatrix}0 & 1\end{bmatrix} \otimes X = \begin{bmatrix}1 & 0 \\ 0 & 0\end{bmatrix} \otimes I + \begin{bmatrix}0 & 0 \\ 0 & 1\end{bmatrix} \otimes X = \begin{bmatrix}I & \\ & O\end{bmatrix} + \begin{bmatrix}O & \\ & X\end{bmatrix} = \begin{bmatrix}I & \\ & X\end{bmatrix}$$
	**第二个量子比特(qubit)** 为**控制量子比特(control qubit)**，**第一个量子比特(qubit)** 为**目标量子比特(target qubit)** 的**控制非门(controlled-NOT gate, $CNOT_{2, 1}$ gate)**:
$$CNOT_{2, 1}|x, y\rangle = X^{y}|x\rangle |y\rangle = |y \oplus x, y\rangle(\text{其中}x, y \in \{0, 1\}) = \begin{cases} CNOT_{2, 1}|00\rangle = |00\rangle\\ CNOT_{2, 1}|01\rangle = |11\rangle \\ CNOT_{2, 1}|10\rangle = |10\rangle \\ CNOT_{2, 1}|11\rangle = |01\rangle\end{cases} \Rightarrow CNOT_{2, 1}|\psi\rangle = CNOT_{2, 1}(c_{00}|00\rangle + c_{01}|01\rangle + c_{10}|10\rangle + c_{11}|11\rangle) \stackrel{\text{linearity}}{=} c_{00}CNOT_{2, 1}|00\rangle + c_{01}CNOT_{2, 1}|01\rangle + c_{10}CNOT_{2, 1}|10\rangle + c_{11}CNOT_{2, 1}|11\rangle = c_{00}|00\rangle + c_{01}|11\rangle + c_{10}|10\rangle + c_{11}|01\rangle = c_{00}|00\rangle + c_{11}|01\rangle + c_{10}|10\rangle + c_{01}|11\rangle$$
		**矩阵表示(matrix representation)**:
$$CNOT_{2, 1} = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0 \\ 0 & 1 & 0 & 0\end{bmatrix}$$
			证明(proof):
$$CNOT_{2, 1} = \begin{bmatrix}CNOT_{2, 1}|00\rangle & CNOT_{2, 1}|01\rangle & CNOT_{2, 1}|10\rangle & CNOT_{2, 1}|11\rangle\end{bmatrix} = \begin{bmatrix}|00\rangle & |11\rangle & |10\rangle & |01\rangle\end{bmatrix} = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0 \\ 0 & 1 & 0 & 0\end{bmatrix}$$
		**算子表示(operator representation)**:
$$CNOT_{2, 1} = I \otimes |0\rangle\langle0| + X \otimes |1\rangle\langle1|$$
			证明(proof):
$$I \otimes |0\rangle\langle0| + X \otimes |1\rangle\langle1| = I \otimes \begin{bmatrix}1 \\ 0\end{bmatrix}\begin{bmatrix}1 & 0\end{bmatrix} + X \otimes \begin{bmatrix}0 \\ 1\end{bmatrix}\begin{bmatrix}0 & 1\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & 1\end{bmatrix} \otimes \begin{bmatrix}1 & 0 \\ 0 & 0\end{bmatrix} + \begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix} \otimes \begin{bmatrix}0 & 0 \\ 0 & 1\end{bmatrix} = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0\end{bmatrix} + \begin{bmatrix}0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0\end{bmatrix} = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0 \\ 0 & 1 & 0 & 0\end{bmatrix}$$
	注: **控制非门(controlled-NOT gate)** 有**两种**，因为**第一个量子比特(qubit)** 为**控制量子比特(control qubit)**，**第二个量子比特(qubit)** 为**目标量子比特(target qubit)** 的**控制非门(controlled-NOT gate)** 和**第二个量子比特(qubit)** 为**控制量子比特(control qubit)**，**第一个量子比特(qubit)** 为**目标量子比特(target qubit)** 的**控制非门(controlled NOT gate)** 的**矩阵表示(matrix representation)** 并非只相差一个**全局振幅(global amplitude)**。
	两种**控制非门(controlled-NOT gate, CNOT gate)** 的**矩阵(matrix)** 均为**对合矩阵(involutory matrix)** 和**埃尔米特矩阵(Hermitian matrix)**
		证明(proof):
$$\begin{cases}CNOT^{2} = CNOT \cdot CNOT = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0\end{bmatrix}\begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0\end{bmatrix} = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1\end{bmatrix} = I \\ CNOT^{\dagger} = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0\end{bmatrix}^{\dagger} = \overline{\begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0\end{bmatrix}}^{T} = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0\end{bmatrix}^{T} = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0\end{bmatrix} = CNOT\end{cases}$$
$$\begin{cases}CNOT_{2, 1}^{2} = CNOT_{2, 1} \cdot CNOT_{2, 1} = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0 \\ 0 & 1 & 0 & 0\end{bmatrix}\begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0 \\ 0 & 1 & 0 & 0\end{bmatrix} = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1\end{bmatrix} = I \\ CNOT_{2, 1}^{\dagger} = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0 \\ 0 & 1 & 0 & 0\end{bmatrix}^{\dagger} = \overline{\begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0 \\ 0 & 1 & 0 & 0\end{bmatrix}}^{T} = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0 \\ 0 & 1 & 0 & 0\end{bmatrix}^{T} = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0 \\ 0 & 1 & 0 & 0\end{bmatrix} = CNOT_{2, 1}\end{cases}$$
**控制Z门(controlled-Z gate, CZ gate)**: 当**控制量子比特(control qubit)** 为$|1\rangle$时，对**目标量子比特(target qubit)** 应用**Z门(Z gate)**，否则保持**目标量子比特(target qubit)** 不变，即对**目标量子比特(target qubit)** 应用**I门(I gate)**
	**第一个量子比特(qubit)** 为**控制量子比特(control qubit)**，**第二个量子比特(qubit)** 为**目标量子比特(target qubit)** 的**控制Z门(controlled-Z gate, CZ gate)**:
$$CZ|x, y\rangle = |x\rangle Z^{x}|y\rangle = |x\rangle(-1)^{xy}|y\rangle = (-1)^{xy}|x, y\rangle(\text{其中}x, y \in \{0, 1\}) = \begin{cases} CZ|00\rangle = |00\rangle \\ CZ|01\rangle = |01\rangle \\ CZ|10\rangle = |10\rangle \\ CZ|11\rangle = -|11\rangle\end{cases} \Rightarrow CZ|\psi\rangle = CZ(c_{00}|00\rangle + c_{01}|01\rangle + c_{10}|10\rangle + c_{11}|11\rangle) \stackrel{\text{linearity}}{=} c_{00}CZ|00\rangle + c_{01}CZ|01\rangle + c_{10}CZ|10\rangle + c_{11}CZ|11\rangle = c_{00}|00\rangle + c_{01}|01\rangle + c_{10}|10\rangle - c_{11}|11\rangle$$
		**矩阵表示(matrix representation)**:
$$CZ = \begin{bmatrix}I \\ & Z\end{bmatrix} = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & -1\end{bmatrix}$$
			证明(proof):
$$CZ = \begin{bmatrix}CZ|00\rangle & CZ|01\rangle & CZ|10\rangle & CZ|11\rangle\end{bmatrix} = \begin{bmatrix}|00\rangle & |01\rangle & |10\rangle & -|11\rangle\end{bmatrix} = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & -1\end{bmatrix}$$
		**算子表示(operator representation)**:
$$CZ = |0\rangle\langle0| \otimes I + |1\rangle\langle1| \otimes Z$$
			证明(proof):
$$|0\rangle\langle0| \otimes I + |1\rangle\langle1| \otimes Z = \begin{bmatrix}1 \\ 0\end{bmatrix}\begin{bmatrix}1 & 0\end{bmatrix} \otimes I + \begin{bmatrix}0 \\ 1\end{bmatrix}\begin{bmatrix}0 & 1\end{bmatrix} \otimes Z = \begin{bmatrix}1 & 0 \\ 0 & 0\end{bmatrix} \otimes I + \begin{bmatrix}0 & 0 \\ 0 & 1\end{bmatrix} \otimes Z = \begin{bmatrix}I & \\ & O\end{bmatrix} + \begin{bmatrix}O & \\ & Z\end{bmatrix} = \begin{bmatrix}I & \\ & Z\end{bmatrix} = CZ$$
	**第二个量子比特(qubit)** 为**控制量子比特(control qubit)**，**第一个量子比特(qubit)** 为**目标量子比特(target qubit)** 的**控制Z门(controlled-Z gate, $CZ_{2, 1}$ gate)**:
$$CZ_{2, 1}|x, y\rangle = Z^{y}|x\rangle|y\rangle = (-1)^{xy}|x\rangle|y\rangle = (-1)^{xy}|x, y\rangle(\text{其中}x, y \in \{0, 1\}) = \begin{cases}CZ_{2, 1}|00\rangle = |00\rangle \\ CZ_{2, 1}|01\rangle = |01\rangle \\ CZ_{2, 1}|10\rangle = |10\rangle \\ CZ_{2, 1}|11\rangle = -|11\rangle\end{cases} \Rightarrow CZ_{2, 1}|\psi\rangle = CZ_{2, 1}(c_{00}|00\rangle + c_{01}|01\rangle + c_{10}|10\rangle + c_{11}|11\rangle) \stackrel{\text{linearity}}{=} c_{00}CZ_{2, 1}|00\rangle + c_{01}CZ_{2, 1}|01\rangle + c_{10}CZ_{2, 1}|10\rangle + c_{11}CZ|11\rangle = c_{00}|00\rangle + c_{01}|01\rangle + c_{10}|10\rangle - c_{11}|11\rangle$$
		**矩阵表示(matrix representation)**:
$$CZ_{2, 1} = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & -1\end{bmatrix}$$
			证明(proof):
$$CZ_{2, 1} = \begin{bmatrix}CZ_{2, 1}|00\rangle & CZ_{2, 1}|01\rangle & CZ_{2, 1}|10\rangle & CZ_{2, 1}|11\rangle\end{bmatrix} = \begin{bmatrix}|00\rangle & |01\rangle & |10\rangle & -|11\rangle\end{bmatrix} = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & -1\end{bmatrix}$$
		**算子表示(operator representation)**:
$$CZ_{2, 1} = I \otimes |0\rangle\langle0| + Z \otimes |1\rangle\langle1|$$
			证明(proof):
$$I \otimes |0\rangle\langle0| + Z \otimes |1\rangle\langle1| = I \otimes \begin{bmatrix}1 \\ 0\end{bmatrix}\begin{bmatrix}1 & 0\end{bmatrix} + Z \otimes \begin{bmatrix}0 \\ 1\end{bmatrix}\begin{bmatrix}0 & 1\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & 1\end{bmatrix} \otimes \begin{bmatrix}1 & 0 \\ 0 & 0\end{bmatrix} + \begin{bmatrix}1 & 0 \\ 0 & -1\end{bmatrix} \otimes \begin{bmatrix}0 & 0 \\ 0 & 1\end{bmatrix} = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0\end{bmatrix} + \begin{bmatrix}0 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & -1\end{bmatrix} = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & -1\end{bmatrix} = CZ_{2, 1}$$
	注: **控制Z门(controlled-Z gate, CZ gate)** 只有一种，因为**第一个量子比特(qubit)** 为**控制量子比特(control qubit)**，**第二个量子比特(qubit)** 为**目标量子比特(target qubit)** 的**控制Z门(controlled-Z gate, CZ gate)** 和**第二个量子比特(qubit)** 为**控制量子比特(control qubit)**，**第一个量子比特(qubit)** 为**目标量子比特(target qubit)** 的**控制Z门(controlled-Z gate, CZ gate)** 的**矩阵表示(matrix representation)** 完全相同。因此，**控制Z门(controlled-Z gate, CZ gate)** 的**控制量子比特(control qubit)** 和**目标量子比特(target qubit)** 可以随意选择
	**控制Z门(controlled-Z gate)** 的**矩阵(matrix)** 为**对合矩阵(involutory matrix)** 和**埃尔米特矩阵(Hermitian matrix)**
		证明(proof):
$$\begin{cases}CZ^{2} = CZ \cdot CZ = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & -1\end{bmatrix}\begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & -1\end{bmatrix} = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1\end{bmatrix} = I \\ CZ^{\dagger} = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & -1\end{bmatrix}^{\dagger} = \overline{\begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & -1\end{bmatrix}}^{T} = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & -1\end{bmatrix}^{T} = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & -1\end{bmatrix} = CZ\end{cases}$$
	[[量子门的并行(Parallelism of Quantum Gates)]]
	**控制非门(controlled-NOT gate, CNOT gate)** 与**控制Z门(controlled-Z gate, CZ gate)** 之间的相互转化:
		可以通过在**控制非门(controlled-NOT gate, CNOT gate)** 的**目标量子比特(target qubit)** 所在的**导线(wire)** 的头尾各添加一个**阿达马门(Hadamard gate)** 来构造**控制Z门(controlled-Z gate, CZ gate)**，因为$HXH = Z$
			证明(proof):
$$\begin{cases}(I \otimes H)CNOT(I \otimes H) = (I \otimes H)(|0\rangle\langle0| \otimes I + |1\rangle\langle1| \otimes X)(I \otimes H) = (I \otimes H)(|0\rangle\langle0| \otimes I)(I \otimes H) + (I \otimes H)(|1\rangle\langle1| \otimes X)(I \otimes H) = I|0\rangle\langle0|I \otimes HIH + I|1\rangle\langle1|I \otimes HXH = |0\rangle\langle0| \otimes I + |1\rangle\langle1| \otimes Z = CZ \\ (H \otimes I)CNOT_{2, 1}(H \otimes I) = (H \otimes I)(I \otimes |0\rangle\langle0| + X \otimes |1\rangle\langle1|)(H \otimes I) = (H \otimes I)(I \otimes |0\rangle\langle0|)(H \otimes I) + (H \otimes I)(X \otimes |1\rangle\langle1|)(H \otimes I) = HIH \otimes I|0\rangle\langle0|I + HXH \otimes I|1\rangle\langle1|I = I \otimes |0\rangle\langle0| + Z \otimes |1\rangle\langle1| = CZ\end{cases}$$
		也可以通过先选择**控制Z门(controlled-Z gate)** 的一个**量子比特(qubit)** 为**控制量子比特(control qubit)**，另一个**量子比特(qubit)** 为**目标量子比特(target qubit)**，然后在**目标量子比特(target qubit)** 所在的**导线(wire)** 的头尾各添加一个**阿达马门(Hadamard gate)** 来构造**控制非门(controlled-NOT gate)**，因为$HZH = X$
			证明(proof):
$$\begin{cases}(I \otimes H)CZ(I \otimes H) = (I \otimes H)(|0\rangle\langle0| \otimes I + |1\rangle\langle1| \otimes Z)(I \otimes H) = (I \otimes H)(|0\rangle\langle0| \otimes I)(I \otimes H) + (I \otimes H)(|1\rangle\langle1| \otimes Z)(I \otimes H) = I|0\rangle\langle0|I \otimes HIH + I|1\rangle\langle1|I \otimes HZH = |0\rangle\langle0| \otimes I + |1\rangle\langle1| \otimes X = CNOT \\ (H \otimes I)CZ(H \otimes I) = (H \otimes I)(I \otimes |0\rangle\langle0| + Z \otimes |1\rangle\langle1|)(H \otimes I) = (H \otimes I)(I \otimes |0\rangle\langle0|)(H \otimes I) + (H \otimes I)(Z \otimes |1\rangle\langle1|)(H \otimes I) = HIH \otimes I|0\rangle\langle0|I + HZH \otimes I|1\rangle\langle1|I = I \otimes |0\rangle\langle0| + X \otimes |1\rangle\langle1| = CNOT_{2, 1}\end{cases}$$
	**S门(S gate)** 与$R_{z}(\frac{\pi}{2})$**门($R_{z}(\frac{\pi}{2})$ gate)** 是等效的，因为二者的**矩阵表示(matrix representation)** 只相差一个**全局振幅(global amplitude)**；**控制S门(controlled-S gate, CS gate)** 与**控制$R_{z}(\frac{\pi}{2})$门(controlled-$R_{z}(\frac{\pi}{2})$ gate, $CR_{z}(\frac{\pi}{2})$ gate)** 是不等效的，因为二者的**矩阵表示(matrix representation)** 并非只相差一个**全局振幅(global amplitude)**。
$$S = \begin{bmatrix}1 & 0 \\ 0 & i\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & e^{i\frac{\pi}{2}}\end{bmatrix} = e^{i\frac{\pi}{4}}\begin{bmatrix}e^{-i\frac{\pi}{4}} & 0 \\ 0 & e^{i\frac{\pi}{4}}\end{bmatrix} = e^{i\frac{\pi}{4}}R_{z}(\frac{\pi}{2})$$
$$CS = |0\rangle\langle0| \otimes I + |1\rangle\langle1| \otimes S = \begin{bmatrix}1 \\ 0\end{bmatrix}\begin{bmatrix}1 & 0\end{bmatrix} \otimes I + \begin{bmatrix}0 \\ 1\end{bmatrix}\begin{bmatrix}0 & 1\end{bmatrix} \otimes S = \begin{bmatrix}1 & 0 \\ 0 & 0\end{bmatrix} \otimes I + \begin{bmatrix}0 & 0 \\ 0 & 1\end{bmatrix} \otimes S = \begin{bmatrix}I \\ & O\end{bmatrix} + \begin{bmatrix}O \\ & S\end{bmatrix} = \begin{bmatrix}I \\ & S\end{bmatrix} \neq \begin{bmatrix}I \\ & R_{z}(\frac{\pi}{2})\end{bmatrix} = \begin{bmatrix}I \\ & O\end{bmatrix} + \begin{bmatrix}O \\ & R_{z}(\frac{\pi}{2})\end{bmatrix} = \begin{bmatrix}1 & 0 \\ 0 & 0\end{bmatrix} \otimes I + \begin{bmatrix}0 & 0 \\ 0 & 1\end{bmatrix} \otimes R_{z}(\frac{\pi}{2}) = \begin{bmatrix}1 \\ 0\end{bmatrix}\begin{bmatrix}1 & 0\end{bmatrix} \otimes I + \begin{bmatrix}0 \\ 1\end{bmatrix}\begin{bmatrix}0 & 1\end{bmatrix} \otimes R_{z}(\frac{\pi}{2}) = |0\rangle\langle0| \otimes I + |1\rangle\langle1| \otimes R_{z}(\frac{\pi}{2}) = CR_{z}(\frac{\pi}{2})$$
	可以通过在**控制S门(controlled-S gate, CS gate)** 的**控制量子比特(control qubit)** 所在的导线(wire)的尾添加一个$R(-\frac{\pi}{4})$**门($R(-\frac{\pi}{4})$ gate)** 来构造**控制$R_{z}(\frac{\pi}{2})$门(controlled-$R_{z}(\frac{\pi}{2})$ gate, $CR_{z}(\frac{\pi}{2})$ gate)**，因为**S门(S gate)** 比$R_{z}(\frac{\pi}{2})$**门($R_{z}(\frac{\pi}{2})$ gate)** 多了一个**振幅(amplitude)**$e^{i\frac{\pi}{4}}$，当**控制量子比特(control qubit)** 为$|0\rangle$时，**控制量子比特(control qubit)** 所在的**导线(wire)** 上的$R(-\frac{\pi}{4})$**门($R(-\frac{\pi}{4})$ gate)** 不会对**控制量子比特(control qubit)** 产生任何作用；当**控制量子比特(control qubit)** 为$|1\rangle$时，**控制量子比特(control qubit)** 所在的**导线(wire)** 上的$R(-\frac{\pi}{4})$**门($R(-\frac{\pi}{4})$ gate)** 会为**控制量子比特(control qubit)** 添加一个**振幅(amplitude)**$e^{-i\frac{\pi}{4}}$
		证明(proof):
$$[(|0\rangle\langle0| + e^{-i\frac{\pi}{4}}|1\rangle\langle1|) \otimes I]CS = [(|0\rangle\langle0| + e^{-i\frac{\pi}{4}}|1\rangle\langle1|) \otimes I](|0\rangle\langle0| \otimes I + |1\rangle\langle1| \otimes S) = [(|0\rangle\langle0| + e^{-i\frac{\pi}{4}}|1\rangle\langle1|) \otimes I](|0\rangle\langle0| \otimes I) + [(|0\rangle\langle0| + e^{-i\frac{\pi}{4}}|1\rangle\langle1|) \otimes I](|1\rangle\langle1| \otimes S) = (|0\rangle\langle0| + e^{-i\frac{\pi}{4}}|1\rangle\langle1|)(|0\rangle\langle0|) \otimes I^{2} + (|0\rangle\langle0| + e^{-i\frac{\pi}{4}}|1\rangle\langle1|)(|1\rangle\langle1|) \otimes IS = [(|0\rangle\langle0|)^{2} + e^{-i\frac{\pi}{4}}(|1\rangle\langle1|)(|0\rangle\langle0|)] \otimes I + [(|0\rangle\langle0|)(|1\rangle\langle1|) + e^{-i\frac{\pi}{4}}(|1\rangle\langle1|)^{2}] \otimes S = |0\rangle\langle0| \otimes I + e^{-i\frac{\pi}{4}}|1\rangle\langle1| \otimes S = |0\rangle\langle0| \otimes I + |1\rangle\langle1| \otimes (e^{-i\frac{\pi}{4}}S) = |0\rangle\langle0| \otimes I + |1\rangle\langle1| \otimes R_{z}(\frac{\pi}{2}) = CR_{z}(\frac{\pi}{2})$$
(推广)**万能控制门(universal controlled gate)**——**控制U门(controlled-U gate, CU gate)**: 当**控制量子比特(control qubit)** 为$|1\rangle$时，对**目标量子比特(target qubit)** 应用**U门(U gate)**，否则保持**目标量子比特(target qubit)** 不变，即对**目标量子比特(target qubit)** 应用**I门(I gate)**
	**第一个量子比特(qubit)** 为**控制量子比特(control qubit)**，**第二个量子比特(qubit)** 为**目标比特(target qubit)** 的**控制U门(controlled-U gate, CU gate)**:
$$CU|x, y\rangle = |x\rangle U^{x}|y\rangle(\text{其中}x, y \in \{0, 1\}) = \begin{cases}CU|00\rangle = |00\rangle \\ CU|01\rangle = |01\rangle \\ CU|10\rangle = |1\rangle U|0\rangle = |1\rangle(u_{00}|0\rangle + u_{10}|1\rangle) = u_{00}|10\rangle + u_{10}|11\rangle \\ CU|11\rangle = |1\rangle U|1\rangle = |1\rangle(u_{01}|0\rangle + u_{11}|1\rangle) = u_{01}|10\rangle + u_{11}|11\rangle\end{cases} \Rightarrow CU|\psi\rangle = CU(c_{00}|00\rangle + c_{01}|01\rangle + c_{10}|10\rangle + c_{11}|11\rangle) \stackrel{\text{linearity}}{=} c_{00}CU|00\rangle + c_{01}CU|01\rangle + c_{10}CU|10\rangle + c_{11}CU|11\rangle = c_{00}|00\rangle + c_{01}|01\rangle + c_{10}(u_{00}|10\rangle + u_{10}|11\rangle) + c_{11}(u_{01}|10\rangle + u_{11}|11\rangle) = c_{00}|00\rangle + c_{01}|01\rangle + (c_{10}u_{00} + c_{11}u_{01})|10\rangle + (c_{10}u_{10} + c_{11}u_{11})|11\rangle$$
		**矩阵表示(matrix representation)**:
$$CU = \begin{bmatrix}I & \\ & U\end{bmatrix} = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & u_{00} & u_{01} \\ 0 & 0 & u_{10} & u_{11}\end{bmatrix}$$
			证明(proof):
$$U = \begin{bmatrix}U|00\rangle & U|01\rangle & U|10\rangle & U|11\rangle\end{bmatrix} = \begin{bmatrix}|00\rangle & |01\rangle & u_{00}|10\rangle + u_{10}|11\rangle & u_{01}|10\rangle + u_{11}|11\rangle\end{bmatrix} = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & u_{00} & u_{01} \\ 0 & 0 & u_{10} & u_{11}\end{bmatrix}$$
		**算子表示(operator representation)**:
$$CU = |0\rangle\langle0| \otimes I + |1\rangle\langle1| \otimes U$$
			证明(proof):
$$|0\rangle\langle0| \otimes I + |1\rangle\langle1| \otimes U = \begin{bmatrix}1 \\ 0\end{bmatrix}\begin{bmatrix}1 & 0\end{bmatrix} \otimes I + \begin{bmatrix}0 \\ 1\end{bmatrix}\begin{bmatrix}0 & 1\end{bmatrix} \otimes U = \begin{bmatrix}1 & 0 \\ 0 & 0\end{bmatrix} \otimes I + \begin{bmatrix}0 & 0 \\ 0 & 1\end{bmatrix} \otimes U = \begin{bmatrix}I & \\ & O\end{bmatrix} + \begin{bmatrix}O & \\ & U\end{bmatrix} = \begin{bmatrix}I & \\ & U\end{bmatrix}$$
	**第二个量子比特(qubit)** 为**控制量子比特(control qubit)**，**第一个量子比特(qubit)** 为**目标量子比特(target qubit)** 的**控制U门(controlled-U gate, $CU_{2, 1}$ gate)**:
$$CU_{2, 1}|x, y\rangle = U^{y}|x\rangle|y\rangle(\text{其中}x, y \in \{0, 1\}) = \begin{cases}CU_{2, 1}|00\rangle = |00\rangle \\ CU_{2, 1}|01\rangle = U|0\rangle \otimes |1\rangle = (u_{00}|0\rangle + u_{10}|1\rangle) \otimes |1\rangle = u_{00}|01\rangle + u_{10}|11\rangle \\ CU_{2, 1}|10\rangle = |10\rangle \\ CU_{2, 1}|11\rangle = U|1\rangle \otimes |1\rangle = (u_{01}|0\rangle + u_{11}|1\rangle) \otimes |1\rangle = u_{01}|01\rangle + u_{11}|11\rangle\end{cases} \Rightarrow U_{2, 1}|\psi\rangle = U_{2, 1}(c_{00}|00\rangle + c_{01}|01\rangle + c_{10}|10\rangle + c_{11}|11\rangle) \stackrel{\text{linearity}}{=} c_{00}U_{2, 1}|00\rangle + c_{01}U_{2, 1}|01\rangle + c_{10}U_{2, 1}|10\rangle + c_{11}U_{2, 1}|11\rangle = c_{00}|00\rangle + c_{01}(u_{00}|01\rangle + u_{10}|11\rangle) + c_{10}|10\rangle + c_{11}(u_{01}|01\rangle + u_{11}|11\rangle) = c_{00}|00\rangle + (c_{01}u_{00} + c_{11}u_{01})|01\rangle + c_{10}|10\rangle + (c_{01}u_{10} + c_{11}u_{11})|11\rangle$$
		**矩阵表示(matrix representation)**:
$$CU_{2, 1} = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & u_{00} & 0 & u_{01} \\ 0 & 0 & 1 & 0 \\ 0 & u_{10} & 0 & u_{11}\end{bmatrix}$$
			证明(proof):
$$CU_{2, 1} = \begin{bmatrix}CU_{2, 1}|00\rangle & CU_{2, 1}|01\rangle & CU_{2, 1}|10\rangle & CU_{2, 1}|11\rangle\end{bmatrix} = \begin{bmatrix}|00\rangle & u_{00}|01\rangle + u_{10}|11\rangle & |10\rangle & u_{01}|01\rangle + u_{11}|11\rangle\end{bmatrix} = \begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & u_{00} & 0 & u_{01} \\ 0 & 0 & 1 & 0 \\ 0 & u_{10} & 0 & u_{11}\end{bmatrix}$$
		 **算子表示(operator representation)**:
 $$CU_{2, 1} = I \otimes |0\rangle\langle0| + U \otimes |1\rangle\langle1|$$
			 证明(proof):
$$I \otimes |0\rangle\langle0| + U \otimes |1\rangle\langle1| = I \otimes E_{00} + U \otimes E_{11} = \begin{bmatrix}E_{00} & \\ & E_{00}\end{bmatrix} + \begin{bmatrix}u_{00}E_{11} & u_{01}E_{11} \\ u_{10}E_{11} & u_{11}E_{11}\end{bmatrix} = \begin{bmatrix}E_{00} + u_{00}E_{11} & u_{01}E_{11} \\ u_{10}E_{11} & E_{00} + u_{11}E_{11}\end{bmatrix} = \begin{bmatrix}1 \\ & u_{00} & & u_{01} \\ & & 1 \\ & u_{10} & & u_{11}\end{bmatrix} = CU_{2, 1}$$
	**构造(construction)**: 以**第一个量子比特(qubit)** 为**控制量子比特(control qubit)**，**第二个量子比特(qubit)** 为**目标量子比特(target qubit)** 的**控制U门(controlled-U gate)** 为例:
![[控制U门(controlled-U gate, CU gate).png]]
	令$A = R_{z}(\beta)R_{y}(\frac{\gamma}{2})$, $B = R_{y}(-\frac{\gamma}{2})R_{z}(-\frac{\delta + \beta}{2}), C = R_{z}(\frac{\delta - \beta}{2})$
$$ABC = R_{z}(\beta)R_{y}(\frac{\gamma}{2})R(-\frac{\gamma}{2})R(-\frac{\delta + \beta}{2})R(\frac{\delta - \beta}{2}) = R_{z}(\beta)R(-\beta) = I$$
$$e^{i\alpha}AXBXC = e^{i\alpha}R_{z}(\beta)R_{y}(\frac{\gamma}{2})XR_{y}(-\frac{\gamma}{2})R_{z}(-\frac{\delta + \beta}{2})XR_{z}(\frac{\delta - \beta}{2}) = e^{i\alpha}R_{z}(\beta)R_{y}(\frac{\gamma}{2})XR_{y}(\frac{\gamma}{2})IR_{z}(-\frac{\delta + \beta}{2})XR_{z}(\frac{\delta - \beta}{2}) = e^{i\alpha}R_{z}(\beta)R_{y}(\frac{\gamma}{2})XR_{y}(-\frac{\gamma}{2})XXR_{z}(-\frac{\delta + \beta}{2})XR_{z}(\frac{\delta - \beta}{2}) = e^{i\alpha}R_{z}(\beta)R_{y}(\frac{\gamma}{2})R_{y}(\frac{\gamma}{2})R_{z}(\frac{\delta + \beta}{2})R_{z}(\frac{\delta - \beta}{2}) = e^{i\alpha}R_{z}(\beta)R_{y}(\gamma)R_{z}(\delta) = U$$
### 三、三元量子门(triple-qubit quantum gate):
**托佛利门(Toffoli gate, TOF gate)/控-控非门(controlled-controlled-NOT gate, CCNOT gate)**: 当**两个控制量子比特(control qubit)** 均为|1$\rangle$时，**翻转(flip)目标量子比特(target qubit)**，即对**目标量子比特(target qubit)** 应用**X门(X gate)**，否则保持**目标量子比特(target qubit)** 不变(n.b. **控-控非门(controlled-controlled-NOT gate, CCNOT gate)** 即**控-控-X门(controlled-controlled-X gate)**)
	**第一个量子比特(qubit)** 和**第二个量子比特(qubit)** 为**控制量子比特(control qubit)**，**第三个量子比特(qubit)** 为**目标量子比特(target qubit)** 的**托佛利门(Toffoli gate, TOF gate)**:
$$TOF|x, y, z\rangle = |x\rangle|y\rangle X^{xy}|z\rangle = |x, y, xy \oplus z\rangle(\text{其中}x, y, z \in \{0, 1\}) = \begin{cases}TOF|000\rangle = |000\rangle \\ TOF|001\rangle = |001\rangle \\ TOF|010\rangle = |010\rangle \\ TOF|011\rangle = |011\rangle \\ TOF|100\rangle = |100\rangle \\ TOF|101\rangle = |101\rangle \\ TOF|110\rangle = |111\rangle \\ TOF|111\rangle = |110\rangle\end{cases} \Rightarrow TOF(c_{000}|000\rangle + c_{001}|001\rangle + c_{010}|010\rangle + c_{011}|011\rangle + c_{100}|100\rangle + c_{101}|101\rangle + c_{110}|110\rangle + c_{111}|111\rangle) \stackrel{\text{linearity}}{=} c_{000}TOF|000\rangle + c_{001}TOF|001\rangle + c_{010}TOF|010\rangle + c_{011}TOF|011\rangle + c_{100}TOF|100\rangle + c_{101}TOF|101\rangle + c_{110}TOF|110\rangle + c_{111}TOF|111\rangle = c_{000}|000\rangle + c_{001}|001\rangle + c_{010}|010\rangle + c_{011}|011\rangle + c_{100}|100\rangle + c_{101}|101\rangle + c_{110}|111\rangle + c_{111}|110\rangle = c_{000}|000\rangle + c_{001}|001\rangle + c_{010}|010\rangle + c_{011}|011\rangle + c_{100}|100\rangle + c_{101}|101\rangle + c_{111}|110\rangle + c_{110}|111\rangle$$
		**矩阵表示(matrix representation)**:
$$TOF = \begin{bmatrix}1 & 0 & 0 & 0 & 0 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 & 0 & 0 & 0 & 0 \\ 0 & 0 & 1 & 0 & 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 1 & 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 & 1 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 & 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 0 & 0 & 0 & 0 & 1 \\ 0 & 1 & 0 & 0 & 0 & 0 & 1 & 0\end{bmatrix}$$
			证明(proof):
$$TOF = \begin{bmatrix}TOF|000\rangle & TOF|001\rangle & TOF|010\rangle & TOF|011\rangle & TOF|100\rangle & TOF|101\rangle & TOF|110\rangle & TOF|111\rangle\end{bmatrix} = \begin{bmatrix}|000\rangle & |001\rangle & |010\rangle & |011\rangle & |100\rangle & |101\rangle & |111\rangle & |110\rangle\end{bmatrix} = \begin{bmatrix}1 & 0 & 0 & 0 & 0 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 & 0 & 0 & 0 & 0 \\ 0 & 0 & 1 & 0 & 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 1 & 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 & 1 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 & 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 0 & 0 & 0 & 0 & 1 \\ 0 & 0 & 0 & 0 & 0 & 0 & 1 & 0\end{bmatrix}$$