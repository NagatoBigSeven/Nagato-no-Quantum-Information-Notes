格罗弗问题(Grover's problem): 假设所有n位01串中只有一个串**s**是“高贵”的，试找出之
经典算法(classical algorithm): 依次检查0...0, 0...01, ..., 1...1，最好需要进行1次查询(query)，最坏需要进行$2^{n}$次查询(query)
时间复杂度(time complexity): $O(2^{n})$
量子算法(quantum algorithm):
假设有如下图所示的量子预言机(quantum oracle)$U_{f}$:
![[量子算法(quantum algorithm).png]]
$$U_{f}|\mathbf{x}, y\rangle = U_{f}|\mathbf{x}, y \oplus f(\mathbf{x})\rangle$$
(其中**x** = $\begin{bmatrix}x_{0} \\ x_{1} \\ x_{2} \\ \vdots \\ x_{n - 1}\end{bmatrix}$ $\in$ $\{0, 1\}^{n}$，$x_{0}$, $x_{1}$, ..., $x_{n - 1}$, y $\in$ {0, 1}，$f(\mathbf{x}) = \begin{cases}0\text{, if }\mathbf{x}\neq\mathbf{s} \\ 1\text{, if }\mathbf{x} = \mathbf{s}\end{cases}$)
$$U_{f}\sum_{\mathbf{x}, y}c_{\mathbf{x}y}|\mathbf{x}, y\rangle = \sum_{\mathbf{x}, y}c_{\mathbf{x}y}|\mathbf{x}, y \oplus f(\mathbf{x})\rangle$$
$$|\psi_{0}\rangle = H^{\otimes n}|0 \dots 0\rangle = \frac{1}{\sqrt{2^{n}}}\sum_{\mathbf{x} \in \{0, 1\}^{n}}|\mathbf{x}\rangle$$
$$Input = |\psi_{0}\rangle|0\rangle = \frac{1}{\sqrt{2^{n}}}\sum_{\mathbf{x} \in \{0, 1\}^{n}}|\mathbf{x}, 0\rangle$$
$$Output = U_{f}Input = U_{f}\frac{1}{\sqrt{2^{n}}}\sum_{\mathbf{x} \in \{0, 1\}^{n}}|\mathbf{x}, 0\rangle = \frac{1}{\sqrt{2^{n}}}\sum_{\mathbf{x} \neq \mathbf{s}}|\mathbf{x}, 0\rangle + \frac{1}{\sqrt{2^{n}}}|\mathbf{s}, 1\rangle$$
$$P(\text{the measurement of the last qubit is }|1\rangle) = \frac{1}{2^{n}}$$
时间复杂度(time complexity): 约$O(2^{n})$
优化(optimization): 通过放大(amplify)输入(input)中$|\mathbf{s}\rangle$这一项的振幅(amplitude)，从而提高测量(measurement)到输出(output)为$|\mathbf{s}, 1\rangle$这一项的概率(probability, prob.)?
**格罗弗迭代(Grover's iteration)**: 
	第一步: 翻转$|\mathbf{s}\rangle$的振幅(amplitude): $c_{\mathbf{s}} \leftarrow -c_{\mathbf{s}}$
	第二步: 求所有振幅(amplitude)的算术平均数(arithmetic mean): $\overline{c} = \frac{\sum_{\mathbf{x} = 0}^{2^{n - 1}}c_{\mathbf{x}}}{2^{n}}$
	第三步: 将所有振幅(amplitude)分别关于算术平均数(arithmetic mean)对称: $c_{\mathbf{x}} \leftarrow 2\overline{c} - c_{\mathbf{x}}$
**格罗弗算法(Grover's algorithm)**: 不断进行格罗弗迭代(Grover's iteration)直到$|\mathbf{\mathbf{s}}\rangle$的振幅(amplitude)的模(modulus)的平方$|c_{s}|^{2}$大于$\frac{1}{2}$
时间复杂度(time complexity): 约$O(\sqrt{2^{N}})$
证明(proof):
$$|\psi_{0}\rangle = (H|0\rangle)^{\otimes n} = \frac{1}{\sqrt{2^{n}}}\sum_{\mathbf{x} \neq \mathbf{s}}|\mathbf{x}\rangle + \frac{1}{\sqrt{2^{n}}}|\mathbf{s}\rangle = \frac{1}{\sqrt{N}}\sum_{\mathbf{x} \neq \mathbf{s}}|\mathbf{x}\rangle + \frac{1}{\sqrt{N}}|\mathbf{s}\rangle$$
(其中$N = 2^{n}$)
不难发现$\sum_{\mathbf{x} \neq \mathbf{s}}|\mathbf{x}\rangle$和|$\mathbf{s}$$\rangle$正交(orthogonal)，则\{$\sum_{\mathbf{x} \neq \mathbf{s}}|\mathbf{x}\rangle$, $|s\rangle$\}是$\sum_{\mathbf{x} \neq \mathbf{s}}|\mathbf{x}\rangle$和$|s\rangle$张成的向量空间(vector space)span\{$\sum_{\mathbf{x} \neq \mathbf{s}}$|$\mathbf{x}$$\rangle$\, |s$\rangle$\}(i.e. $2^{n}$维空间($2^{n}$-d space)中的一个过原点(origin)的超平面(hyperplane))的一组正交基(orthogonal basis)
将正交基(orthogonal basis)\{$\sum_{\mathbf{x} \neq \mathbf{s}}|x\rangle$\, $|s\rangle$}归一化(normalization)，得到一组正交归一基(orthonormal basis)\{|$\alpha$$\rangle$, |$\beta$$\rangle$\}
其中
$$\begin{cases}|\alpha\rangle = \frac{1}{\sqrt{N - 1}}\sum_{\mathbf{x} \neq \mathbf{s}}|\mathbf{x}\rangle \\ |\beta\rangle = |\mathbf{s}\rangle\end{cases}$$
$$|\psi_{0}\rangle = \frac{\sqrt{N - 1}}{\sqrt{N}}|\alpha\rangle + \frac{1}{\sqrt{N}}|\beta\rangle$$

在超平面(hyperplane)上以|$\alpha$$\rangle$的方向(direction)为x轴(axis)正方向(positive direction)，以|$\beta$$\rangle$的方向(direction)为y轴(axis)正方向(positive direction)建立平面直角坐标系(Cartesian coordinate system)
|$\psi_{0}$$\rangle$的直角坐标(Cartesian coordinate):
$$|\psi_{0}\rangle = (\frac{\sqrt{N - 1}}{\sqrt{N}}, \frac{1}{\sqrt{N}})$$
|$\psi_{0}$$\rangle$的极径(polar radius):
$$r = \sqrt{x^{2} + y^{2}} = \sqrt{(\frac{\sqrt{N - 1}}{\sqrt{N}})^{2} + (\frac{1}{\sqrt{N}})^{2}} = \sqrt{\frac{N - 1}{N} + \frac{1}{N}} = 1$$
|$\psi_{0}$$\rangle$的极角(polar angle):
$$\begin{cases}\sin{\theta} = \frac{y}{r} = \frac{\frac{1}{\sqrt{N}}}{1} = \frac{1}{\sqrt{N}} \\ \cos{\theta} = \frac{x}{r} = \frac{\frac{\sqrt{N - 1}}{\sqrt{N}}}{1} = \frac{\sqrt{N - 1}}{\sqrt{N}}\end{cases}$$
|$\psi_{0}$$\rangle$的极坐标(polar coordinate):
$$|\psi_{0}\rangle = (1, \theta)$$
第一次格罗弗迭代(Grover's iteration):
翻转|$\mathbf{s}$$\rangle$的振幅(amplitude):
$$|\psi_{0}^{'}\rangle = \frac{1}{\sqrt{N}}\sum_{\mathbf{x} \neq \mathbf{s}}|\mathbf{x}\rangle + \frac{1}{\sqrt{N}}|\mathbf{s}\rangle = \frac{1}{\sqrt{N}}\sum_{\mathbf{x} \neq \mathbf{s}}|\mathbf{x}\rangle - \frac{1}{\sqrt{N}}|\mathbf{s}\rangle = \frac{\sqrt{N - 1}}{\sqrt{N}}|\alpha\rangle - \frac{1}{\sqrt{N}}|\beta\rangle$$
|$\psi_{0}^{'}$$\rangle$的直角坐标(Cartesian coordinate):
$$|\psi_{0}^{'}\rangle = (\frac{\sqrt{N - 1}}{\sqrt{N}}, -\frac{1}{\sqrt{N}})$$
(相当于将$|\psi_{0}\rangle$关于x轴(axis)对称)
|$\psi_{0}^{'}$$\rangle$的极径(polar radius): 1
|$\psi_{0}^{'}$$\rangle$的极角(polar angle): -$\theta$
|$\psi_{0}^{'}$$\rangle$的极坐标(polar coordinate): (1, -$\theta$)
所有振幅(amplitude)的算术平均数(arithmetic mean):
$$\overline{c} = \frac{(N - 1) \cdot \frac{1}{\sqrt{N}} - \frac{1}{\sqrt{N}}}{N} = \frac{N - 2}{N\sqrt{N}}$$
将所有振幅(amplitude)关于算术平均数(arithmetic)对称:
$$|\psi_{1}\rangle = (\frac{2N - 4}{N\sqrt{N}} - \frac{1}{\sqrt{N}})\sum_{\mathbf{x} \neq \mathbf{s}}|\mathbf{x}\rangle + (\frac{2N - 4}{N\sqrt{N}} + \frac{1}{\sqrt{N}})|\mathbf{s}\rangle = \frac{N - 4}{N\sqrt{N}}\sum_{\mathbf{x} \neq \mathbf{s}}|\mathbf{x}\rangle + \frac{3N - 4}{N\sqrt{N}}|\mathbf{s}\rangle = \frac{(N - 4)\sqrt{N - 1}}{N\sqrt{N}}\sum_{\mathbf{x} \neq \mathbf{s}}|x\rangle + \frac{3N - 4}{N\sqrt{N}}|s\rangle$$
|$\psi_{1}$$\rangle$的直角坐标(Cartesian coordinate):
$$(\frac{(N - 4)\sqrt{N - 1}}{N\sqrt{N}}, \frac{3N - 4}{N\sqrt{N}})$$
|$\psi_{1}$$\rangle$的极径(polar radius):
$$r = \sqrt{[\frac{(N - 4)\sqrt{N - 1}}{N\sqrt{N}}]^{2} + (\frac{3N - 4}{N\sqrt{N}})^{2}} = \sqrt{\frac{(N - 4)^{2}(N - 1)}{N^{3}} + \frac{9N^{2} + 24N + 16}{N^{3}}} = \sqrt{\frac{(N^{2} - 8N + 16)(N - 1)}{N^{3}} + \frac{9N^{2} + 24N + 16}{N^{3}}} = \sqrt{\frac{N^{3} - N^{2} - 8N^{2} + 8N + 16N - 16}{N^{3}} + \frac{9N^{2} + 24N + 16}{N^{3}}} = 1$$
|$\psi_{1}$$\rangle$的极角(polar angle):
$$\begin{cases}\sin{\alpha} = \frac{y}{r} = \frac{\frac{3N - 4}{N\sqrt{N}}}{1} = \frac{3N - 4}{N\sqrt{N}} = \frac{3}{\sqrt{N}} - \frac{4}{N\sqrt{N}} = 3\sin{\theta} - 4\sin^{3}{\theta} = \sin{3\theta} \\ \cos{\alpha} = \frac{x}{r} = \frac{\frac{(N - 4)\sqrt{N - 1}}{N\sqrt{N}}}{1} = \frac{(N - 4)\sqrt{N - 1}}{N\sqrt{N}} = \frac{4(N - 1)\sqrt{N - 1}}{N\sqrt{N}} - \frac{3\sqrt{N - 1}}{N\sqrt{N}} = 4\cos^{3}{\theta} - 3\cos{\theta}= \cos{3\theta}\end{cases}$$
$$\alpha = 3\theta$$
|$\psi_{1}$$\rangle$的极坐标(polar coordinate):
$$|\psi_{1}\rangle = (1, 3\theta)$$
(相当于将|$\psi_{0}^{'}$$\rangle$关于|$\psi_{0}$$\rangle$对称)
第二次格罗弗迭代(Grover's iteration):
翻转|$\mathbf{s}$$\rangle$的振幅(amplitude): 相当于将|$\psi_{1}$$\rangle$关于x轴(axis)对称
|$\psi_{1}^{'}$$\rangle$的极坐标(polar coordinate): (1, -3$\theta$)
将所有振幅(amplitude)关于算术平均数(arithmetic mean)对称: 相当于将|$\psi_{1}^{'}$$\rangle$关于|$\psi_{0}$$\rangle$对称
|$\psi_{2}$$\rangle$的极坐标(polar coordinate): (1, 5$\theta$)
不难观察到，每进行一次格罗弗迭代(Grover's iteration)，$|\psi\rangle$与x轴(axis)正方向(positive direction)的夹角(angle)就增大2$\theta$
当|$\mathbf{s}$$\rangle$的振幅(amplitude)的模(modulus)的平方大于$\frac{1}{2}$时，即|$\psi$$\rangle$的纵坐标(y-coordinate)的平方大于$\frac{1}{2}$时，即|$\psi$$\rangle$的纵坐标(y-coordinate)大于$\frac{\sqrt{2}}{2}$时，即|$\psi$$\rangle$与x轴(axis)正方向(positive direction)的夹角(angle)大于$\frac{\pi}{4}$时，停止进行格罗弗迭代(Grover's iteration)
$$n \rightarrow +\infty, \sin{\theta} \rightarrow 0, \sin{\theta} \approx \theta
$$
大约需要进行$\frac{\frac{\pi}{4}}{2\theta} = \frac{\pi}{8\theta} \approx \frac{\pi}{8\sin{\theta}} = \frac{\pi}{\frac{8}{\sqrt{N}}} = \frac{\pi}{8}\sqrt{N}$次格罗弗迭代(Grover's iteration)
因此，格罗弗算法(Grover's algorithm)的时间复杂度(time complexity)约为O($\sqrt{N}$)
证毕(Q(uod). E(rat). D(emonstrandum).)
Q1: 在电路(circuit)中，如何实现在不知道$\mathbf{s}$的情况下翻转|$\mathbf{s}$$\rangle$的振幅(amplitutde)?
A1: 通过辅助量子比特(ancilla qubit)为$|-\rangle$的量子预言机(quantum oracle)$U_{f}$!
证明:
$$\begin{cases}U_{f}c_{\mathbf{s}}|\mathbf{s}\rangle|-\rangle = c_{\mathbf{s}}U_{f}|\mathbf{s}\rangle\frac{|0\rangle - |1\rangle}{\sqrt{2}} = c_{\mathbf{s}}U_{f}\frac{|\mathbf{s}, 0\rangle - |\mathbf{s}, 1\rangle}{\sqrt{2}} = \frac{c_{\mathbf{s}}U_{f}|\mathbf{s}, 0\rangle - c_{\mathbf{s}}U_{f}|\mathbf{s}, 1\rangle}{\sqrt{2}} =  \frac{c_{\mathbf{s}}|\mathbf{s}, 0 \oplus f(\mathbf{s})\rangle - c_{\mathbf{s}}|\mathbf{s}, 1 \oplus f(\mathbf{s})\rangle}{\sqrt{2}} = \frac{c_{\mathbf{s}}|\mathbf{s}, f(\mathbf{s})\rangle - c_{\mathbf{s}}|\mathbf{s}, \lnot f(\mathbf{s})\rangle}{\sqrt{2}} = \frac{c_{\mathbf{s}}|\mathbf{s}, 1\rangle - c_{\mathbf{s}}|\mathbf{s}, 0\rangle}{\sqrt{2}} = c_{\mathbf{s}}|\mathbf{s}\rangle\frac{|1\rangle - |0\rangle}{\sqrt{2}} = -c_{\mathbf{s}}|\mathbf{s}\rangle|-\rangle\text{, if }\mathbf{x} = \mathbf{s} \\ U_{f}c_{\mathbf{x}}|\mathbf{x}\rangle|-\rangle = c_{\mathbf{x}}U_{f}|\mathbf{x}\rangle\frac{|0\rangle - |1\rangle}{\sqrt{2}} = c_{\mathbf{x}}U_{f}\frac{|\mathbf{x}, 0\rangle - |\mathbf{x}, 1\rangle}{\sqrt{2}} = \frac{c_{\mathbf{x}}U_{f}|\mathbf{x}, 0\rangle - c_{\mathbf{x}}U_{f}|\mathbf{x}, 1\rangle}{\sqrt{2}} = \frac{c_{\mathbf{x}}|\mathbf{x}, 0 \oplus f(\mathbf{x})\rangle - c_{\mathbf{x}}|\mathbf{x}, 1 \oplus f(\mathbf{x})\rangle}{\sqrt{2}} = \frac{c_{\mathbf{x}}|\mathbf{x}, f(\mathbf{x})\rangle - c_{\mathbf{x}}|\mathbf{x}, \lnot f(\mathbf{x})\rangle}{\sqrt{2}} = \frac{c_{\mathbf{x}}|\mathbf{x}, 0\rangle - c_{\mathbf{x}}|\mathbf{x}, 1\rangle}{\sqrt{2}} = c_{\mathbf{x}}|\mathbf{x}\rangle\frac{|0\rangle - |1\rangle}{\sqrt{2}} = c_{\mathbf{x}}|\mathbf{x}\rangle|-\rangle\text{, if }\mathbf{x} \neq \mathbf{s}\end{cases}$$
$$U_{f}(\sum_{\mathbf{x} \in \{0, 1\}^{n}}c_{\mathbf{x}}|\mathbf{x}\rangle)|-\rangle = U_{f}\sum_{\mathbf{x} \in \{0, 1\}^{n}}c_{\mathbf{x}}|\mathbf{x}\rangle|-\rangle = U_{f}(\sum_{\mathbf{x} \neq \mathbf{s}}c_{\mathbf{x}}|\mathbf{x}\rangle|-\rangle + c_{\mathbf{s}}|\mathbf{s}\rangle|-\rangle) = U_{f}\sum_{\mathbf{x} \neq \mathbf{s}}c_{\mathbf{x}}|\mathbf{x}\rangle|-\rangle + U_{f}c_{\mathbf{s}}|\mathbf{s}\rangle|-\rangle = \sum_{\mathbf{x} \neq \mathbf{s}}c_{\mathbf{x}}U_{f}|\mathbf{x}\rangle|-\rangle + c_{\mathbf{s}}U_{f}|\mathbf{s}\rangle|-\rangle = \sum_{\mathbf{x} \neq \mathbf{s}}c_{\mathbf{x}}|\mathbf{x}\rangle|-\rangle - c_{\mathbf{s}}|\mathbf{s}\rangle|-\rangle = \sum_{\mathbf{x} \neq \mathbf{s}}(-1)^{0}c_{\mathbf{x}}|\mathbf{x}\rangle|-\rangle + (-1)^{1}c_{\mathbf{s}}|\mathbf{s}\rangle|-\rangle = \sum_{\mathbf{x} \neq \mathbf{s}}(-1)^{f(\mathbf{x})}c_{\mathbf{x}}|\mathbf{x}\rangle|-\rangle + (-1)^{f(\mathbf{s})}c_{\mathbf{s}}|\mathbf{s}\rangle|-\rangle = \sum_{\mathbf{x} \in \{0, 1\}^{n}}(-1)^{f(\mathbf{x})}c_{\mathbf{x}}|\mathbf{x}\rangle|-\rangle = (\sum_{\mathbf{x} \in \{0, 1\}^{n}}(-1)^{f(\mathbf{x})}c_{\mathbf{x}}|\mathbf{x}\rangle)|-\rangle$$
Q1: 在电路(circuit)中，如何实现将所有振幅(amplitude)关于算术平均数(arithmetic mean)对称?
A1: 通过若干个并行(paralleled)和串行(sequential)的常用量子门(quantum gate)!
$$\begin{bmatrix}c_{0 \dots 0} \\ c_{0 \dots 01} \\ \vdots \\ c_{1 \dots 1}\end{bmatrix} = \sum_{\mathbf{x} \in \{0, 1\}^{n}}c_{\mathbf{x}}|\mathbf{x}\rangle \rightarrow \sum_{\mathbf{x} \in \{0, 1\}^{n}}(2\overline{c} - c_{\mathbf{x}})|\mathbf{x}\rangle = \begin{bmatrix}2\overline{c} - c_{0 \dots 0} \\ 2\overline{c} - c_{0 \dots 01} \\ \vdots \\ 2\overline{c} - c_{1 \dots 1}\end{bmatrix} = 2\begin{bmatrix}\overline{c} \\ \overline{c} \\ \vdots \\ \overline{c}\end{bmatrix} - \begin{bmatrix}c_{0 \dots 0} \\ c_{0 \dots 01} \\ \vdots \\ c_{1 \dots 1}\end{bmatrix} = 2\begin{bmatrix}\frac{c_{0 \dots 0} + c_{0 \dots 01} + \dots + c_{1 \dots 1}}{N} \\ \frac{c_{0 \dots 0} + c_{0 \dots 01} + \dots + c_{1 \dots 1}}{N} \\ \vdots \\ \frac{c_{0 \dots 0} + c_{0 \dots 01} + \dots + c_{1 \dots 1}}{N}\end{bmatrix} - \begin{bmatrix}c_{0 \dots 0} \\ c_{0 \dots 01} \\ \vdots \\ c_{1 \dots 1}\end{bmatrix} = 2 \cdot \frac{1}{N}\begin{bmatrix}c_{0 \dots 0} + c_{0 \dots 01} + \dots + c_{1 \dots 1} \\ c_{0 \dots 0} + c_{0 \dots 01} + \dots + c_{1 \dots 1} \\ \vdots \\ c_{0 \dots 0} + c_{0 \dots 01} + \dots + c_{1 \dots 1}\end{bmatrix} - \begin{bmatrix}c_{0 \dots 0} \\ c_{0 \dots 01} \\ \vdots \\ c_{1 \dots 1}\end{bmatrix} = 2 \cdot \frac{1}{N}(\begin{bmatrix}c_{0 \cdots 0} \\ c_{0 \dots 0} \\ \vdots \\ c_{0 \dots 0}\end{bmatrix} + \begin{bmatrix}c_{0 \cdots 01} \\ c_{0 \dots 01} \\ \vdots \\ c_{0 \dots 01}\end{bmatrix} + \dots + \begin{bmatrix}c_{1 \dots 1} \\ c_{1 \dots 1} \\ \vdots \\ c_{1 \dots 1}\end{bmatrix}) - \begin{bmatrix}c_{0 \dots 0} \\ c_{0 \dots 01} \\ \vdots \\ c_{1 \dots 1}\end{bmatrix} = 2 \cdot \frac{1}{N}(c_{0 \dots 0}\begin{bmatrix}1 \\ 1 \\ \vdots \\ 1\end{bmatrix} + c_{0 \dots 01}\begin{bmatrix}1 \\ 1 \\ \vdots \\ 1\end{bmatrix} + \dots + c_{1 \dots 1}\begin{bmatrix}1 \\ 1 \\ \vdots \\ 1\end{bmatrix}) - \begin{bmatrix}c_{0 \dots 0} \\ c_{0 \dots 01} \\ \vdots \\ c_{1 \dots 1}\end{bmatrix} = 2 \cdot \frac{1}{N}\begin{bmatrix}1 & 1 & \cdots & 1 \\ 1 & 1 & \cdots & 1 \\ \vdots & \vdots & \ddots & \vdots \\ 1 & 1 & \cdots & 1\end{bmatrix}\begin{bmatrix}c_{0 \dots 0} \\ c_{0 \dots 01} \\ \vdots \\ c_{1 \dots 1}\end{bmatrix} - \begin{bmatrix}c_{0 \dots 0} \\ c_{0 \dots 01} \\ \vdots \\ c_{1 \dots 1}\end{bmatrix} = 2 \cdot \frac{1}{N}\begin{bmatrix}1 & 1 & \cdots & 1 \\ 1 & 1 & \cdots & 1 \\ \vdots & \vdots & \ddots & \vdots \\ 1 & 1 & \cdots & 1\end{bmatrix}\begin{bmatrix}c_{0 \dots 0} \\ c_{0 \dots 01} \\ \vdots \\ c_{1 \dots 1}\end{bmatrix} - \begin{bmatrix}1 & 0 & \cdots & 0 \\ 0 & 1 & \cdots & 0 \\ \vdots & \vdots & \ddots & 0 \\ 0 & 0 & \cdots & 1\end{bmatrix}\begin{bmatrix}c_{0 \dots 0} \\ c_{0 \dots 01} \\ \vdots \\ c_{1 \dots 1}\end{bmatrix} = (2 \cdot \frac{1}{N}\begin{bmatrix}1 & 1 & \cdots & 1 \\ 1 & 1 & \cdots & 1 \\ \vdots & \vdots & \ddots & \vdots \\ 1 & 1 & \cdots & 1\end{bmatrix} - \begin{bmatrix}1 & 0 & \cdots & 0 \\ 0 & 1 & \cdots & 0 \\ \vdots & \vdots & \ddots & 0 \\ 0 & 0 & \cdots & 1\end{bmatrix})\begin{bmatrix}c_{0 \dots 0} \\ c_{0 \dots 01} \\ \vdots \\ c_{1 \dots 1}\end{bmatrix} = (2A - I_{N})\begin{bmatrix}c_{0 \dots 0} \\ c_{0 \dots 01} \\ \vdots \\ c_{1 \dots 1}\end{bmatrix} = D\begin{bmatrix}c_{0 \dots 0} \\ c_{0 \dots 01} \\ \vdots \\ c_{1 \dots 1}\end{bmatrix}$$
(其中$A = \frac{1}{N}\begin{bmatrix}1 & 0 & \cdots & 0 \\ 0 & 1 & \cdots & 0 \\ \vdots & \vdots & \ddots & 0 \\ 0 & 0 & \cdots & 1\end{bmatrix}$, $I_{N}$为N阶(N-th order)单位(矩)阵(identity matrix), $D = 2A - I_{N}$)
$$A = \frac{1}{N}\begin{bmatrix}1 & 1 & \cdots & 1 \\ 1 & 1 & \cdots & 1\\\vdots & \vdots & \ddots & \vdots \\ 1 & 1 & \cdots & 1\end{bmatrix} = \begin{bmatrix}\frac{1}{N} & \frac{1}{N} & \cdots & \frac{1}{N} \\ \frac{1}{N} & \frac{1}{N} & \cdots & \frac{1}{N}\\\vdots & \vdots & \ddots & \vdots \\ \frac{1}{N} & \frac{1}{N} & \cdots & \frac{1}{N}\end{bmatrix} = \begin{bmatrix}\frac{1}{\sqrt{N}} \\ \frac{1}{\sqrt{N}} \\ \vdots \\ \frac{1}{\sqrt{N}}\end{bmatrix}\begin{bmatrix}\frac{1}{\sqrt{N}} & \frac{1}{\sqrt{N}} & \cdots & \frac{1}{\sqrt{N}}\end{bmatrix} = |\psi_{0}\rangle\langle\psi_{0}| = (H|0\rangle)^{\otimes n}(\langle0|H)^{\otimes n} = H^{\otimes n}|0\rangle^{\otimes n}\langle0|^{\otimes n}H^{\otimes n} = H^{\otimes n}(|0\rangle^{\otimes n}\langle0|)^{\otimes n}H^{\otimes n} = H^{\otimes n}(|0\rangle\langle0|)^{\otimes n}H^{\otimes n}$$
$$D = 2A - I_{N} = 2H^{\otimes n}(|0\rangle\langle0|)^{\otimes n}H^{\otimes n} - I_{N} = 2H^{\otimes n}(|0\rangle\langle0|)^{\otimes n}H^{\otimes n} - H^{\otimes n}I_{N}H^{\otimes n} = H^{\otimes n}[2(|0\rangle\langle0|)^{\otimes n} - I_{N}]H^{\otimes n} = H^{\otimes n}\{2[(X|1\rangle)(\langle1|X)]^{\otimes n} - I_{N}\}H^{\otimes n} = H^{\otimes n}[2(X|1\rangle\langle1|X)^{\otimes n} - I_{N}]H^{\otimes n} = H^{\otimes n}\{2[X(|1\rangle\langle1|)X]^{\otimes n} - I_{N}\}H^{\otimes n} = H^{\otimes n}[2X^{\otimes n}(|1\rangle\langle1|)^{\otimes n}X^{\otimes n} - I_{N}]H^{\otimes n} = H^{\otimes n}[2X^{\otimes n}(|1\rangle\langle1|)^{\otimes n}X^{\otimes n} - X^{\otimes n}I_{N}X^{\otimes n}]H^{\otimes n} = H^{\otimes n}X^{\otimes n}[2(|1\rangle\langle1|)^{\otimes n} - I_{N}]X^{\otimes n}H^{\otimes n} = -H^{\otimes n}X^{\otimes n}[I_{N} - (|1\rangle\langle1|)^{\otimes n}]X^{\otimes n}H^{\otimes n} = -H^{\otimes n}X^{\otimes n}C^{n - 1}ZX^{\otimes n}H^{\otimes n}$$
(其中$C^{n - 1}Z$为前n - 1个量子比特(qubit)为控制比特(control bit)，第n个量子比特(qubit)为目标比特(target bit)的多控Z门(multi-controlled Z gate), $C^{n - 1}Z$ gate)
![[格罗弗算法(Grover's algorithm).png]]
