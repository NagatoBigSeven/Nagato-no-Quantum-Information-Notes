**向量空间(vector space)**: 对**加法(addition)** 和**数乘(scalar multiplication)** **封闭** 的**集合(set)**
$$\begin{cases}\forall u, v \in V, u + v \in V \\ \forall v \in V, \forall c \in \mathbb{F}, cv \in V\end{cases}$$
**向量(vector)**: 有序的一堆数
	**行向量(row vector)**: $\mathbf{r} = \begin{bmatrix}r_{1}, r_{2}, \dots, r_{n}\end{bmatrix}(\text{其中}r_{1}, r_{2}, \dots, r_{n} \in \begin{cases}\mathbb{R}\text{, if }\mathbf{r} \in \mathbb{R}^{n} \\ \mathbb{C}\text{, if }\mathbf{r} \in \mathbb{C}^{n}\end{cases})$
	**(\*)列向量(column vector)**: $\mathbf{c} = \begin{bmatrix}c_{1} \\ c_{2} \\ \vdots \\ c_{n}\end{bmatrix}(\text{其中}c_{1}, c_{2}, \dots, c_{n} \in \begin{cases}\mathbb{R}\text{, if }\mathbf{c} \in \mathbb{R}^{n} \\ \mathbb{C}\text{, if }\mathbf{c} \in \mathbb{C}^{n}\end{cases})$
	**范数(norm)**:
		**L1范数(L1 norm, $||\cdot||_{1}$)**/**曼哈顿范数(Manhattan norm)**/**绝对值范数**:
$$||\mathbf{x}||_{1} = |x_{1}| + |x_{2}| + \dots + |x_{n}| = \sum_{i = 1}^{n}|x_{i}|$$
		**(\*)L2范数(L2 norm, $||\cdot||_{2}$)**/**欧几里得范数(Euclidean norm)**/**模/长度(modulus/length, $|\cdot|$)**:
$$||\mathbf{x}||_{2} = \sqrt{|x_{1}|^{2} + |x_{2}|^{2} + \dots + |x_{n}|^{2}} = \sqrt{\sum_{i = 1}^{n}|x_{i}|^{2}}$$
		$\dots$
		**Ln范数(Ln norm, $||\cdot||_{n}$)**:
$$||\mathbf{x}||_{n} = \sqrt[n]{|x_{1}|^{n} + |x_{2}|^{n} + \dots + |x_{n}|^{n}} = \sqrt[n]{\sum_{i = 1}^{n}|x_{i}|^{n}}$$
		**L$\infty$范数**(**L$\infty$ norm, $||\cdot||_{\infty}$)**
	**运算(operation)**:
		**加法(addition)**:
$$\mathbf{u} + \mathbf{v} = \begin{bmatrix}u_{1} \\ u_{2} \\ \vdots \\ u_{n}\end{bmatrix} + \begin{bmatrix}v_{1} \\ v_{2} \\ \vdots \\ v_{n}\end{bmatrix} = \begin{bmatrix}u_{1} + v_{1} \\ u_{2} + v_{2} \\ \vdots \\ u_{n} + v_{n}\end{bmatrix}$$
			**运算律**:
				**交换律(commutative law)**: $\mathbf{u} + \mathbf{v} = \mathbf{v} + \mathbf{u}$
					证明(proof):
$$\mathbf{u} + \mathbf{v} = \begin{bmatrix}u_{1} \\ u_{2} \\ \vdots \\ u_{n}\end{bmatrix} + \begin{bmatrix}v_{1} \\ v_{2} \\ \vdots \\ v_{n}\end{bmatrix} = \begin{bmatrix}u_{1} + v_{1} \\ u_{2} + v_{2} \\ \vdots \\ u_{n} + v_{n}\end{bmatrix} = \begin{bmatrix}v_{1} + u_{1} \\ v_{2} + u_{2} \\ \vdots \\ v_{n} + u_{n}\end{bmatrix} = \begin{bmatrix}v_{1} \\ v_{2} \\ \vdots \\ v_{n}\end{bmatrix} + \begin{bmatrix}u_{1} \\ u_{2} \\ \vdots \\ u_{n}\end{bmatrix} = \mathbf{v} + \mathbf{u}$$
				**结合律(associative law)**: $(\mathbf{u} + \mathbf{v}) + \mathbf{w} = \mathbf{u} + (\mathbf{v} + \mathbf{w})$
					证明(proof):
$$(\mathbf{u} + \mathbf{v}) + \mathbf{w} = (\begin{bmatrix}u_{1} \\ u_{2} \\ \vdots \\ u_{n}\end{bmatrix} + \begin{bmatrix}v_{1} \\ v_{2} \\ \vdots \\ v_{n}\end{bmatrix}) + \begin{bmatrix}w_{1} \\ w_{2} \\ \vdots \\ w_{n}\end{bmatrix} = \begin{bmatrix}u_{1} + v_{1} \\ u_{2} + v_{2} \\ \vdots \\ u_{n} + v_{n}\end{bmatrix} + \begin{bmatrix}w_{1} \\ w_{2} \\ \vdots \\ w_{n}\end{bmatrix} = \begin{bmatrix}u_{1} + v_{1} + w_{1} \\ u_{2} +v_{2} + w_{2} \\ \vdots \\ u_{n} + v_{n} + w_{n}\end{bmatrix} = \begin{bmatrix}u_{1} \\ u_{2} \\ \vdots \\ u_{n}\end{bmatrix} + \begin{bmatrix}v_{1} + w_{1} \\ v_{2} + w_{2} \\ \vdots \\ v_{n} + w_{n}\end{bmatrix} = \begin{bmatrix}u_{1} \\ u_{2} \\ \vdots \\ u_{n}\end{bmatrix} + (\begin{bmatrix}v_{1} \\ v_{2} \\ \vdots \\ v_{n}\end{bmatrix} + \begin{bmatrix}w_{1} \\ w_{2} \\ \vdots \\ w_{n}\end{bmatrix}) = \mathbf{u} + (\mathbf{v} + \mathbf{w})$$
		**减法(subtraction)**:
$$\mathbf{u} - \mathbf{v} = \begin{bmatrix}u_{1} \\ u_{2} \\ \vdots \\ u_{n}\end{bmatrix} - \begin{bmatrix}v_{1} \\ v_{2} \\ \vdots \\ v_{n}\end{bmatrix} = \begin{bmatrix}u_{1} - v_{1} \\ u_{2} - v_{2} \\ \vdots \\ u_{n} - v_{n}\end{bmatrix}$$
		**数乘(scalar multiple)**:
$$c\mathbf{u} = c\begin{bmatrix}u_{1} \\ u_{2} \\ \vdots \\ u_{n}\end{bmatrix} = \begin{bmatrix}cu_{1} \\ cu_{2} \\ \vdots \\ cu_{n}\end{bmatrix}(\text{其中}c \in \begin{cases}\mathbb{R}\text{, if }\mathbf{u} \in \mathbb{R}^{n} \\ \mathbb{C}\text{, if }\mathbf{u} \in \mathbb{C}^{n}\end{cases})$$
			**运算律**:
				**结合律(associative law)**: $(\lambda\mu)\mathbf{u} = \lambda(\mu\mathbf{u}) = \mu(\lambda\mathbf{u})$
					证明(proof):
$$(\lambda\mu)\mathbf{u} = (\lambda\mu)\begin{bmatrix}u_{1} \\ u_{2} \\ \vdots \\ u_{n}\end{bmatrix} = \begin{bmatrix}(\lambda\mu)u_{1} \\ (\lambda\mu)u_{2} \\ \vdots \\ (\lambda\mu)u_{n}\end{bmatrix} = \begin{bmatrix}\lambda\mu u_{1} \\ \lambda\mu u_{2} \\ \vdots \\ \lambda\mu u_{n}\end{bmatrix} = \begin{bmatrix}\lambda(\mu u_{1}) \\ \lambda(\mu u_{2}) \\ \vdots \\ \lambda(\mu u_{n})\end{bmatrix} = \lambda\begin{bmatrix}\mu u_{1} \\ \mu u_{2} \\ \vdots \\ \mu u_{n}\end{bmatrix} = \lambda(\mu\begin{bmatrix}u_{1} \\ u_{2} \\ \vdots \\ u_{n}\end{bmatrix}) = \lambda(\mu\mathbf{u})$$
$$\text{同理，}(\lambda\mu)\mathbf{u} = \mu(\lambda \mathbf{u})$$
				**分配律(distributive law)**:
					$(\lambda + \mu)\mathbf{u} = \lambda\mathbf{u} + \mu\mathbf{u}$
						证明(proof):
$$(\lambda + \mu)\mathbf{u} = (\lambda + \mu)\begin{bmatrix}u_{1} \\ u_{2} \\ \vdots \\ u_{n}\end{bmatrix} = \begin{bmatrix}(\lambda + \mu)u_{1} \\ (\lambda + \mu)u_{2} \\ \vdots \\ (\lambda + \mu)u_{n}\end{bmatrix} = \begin{bmatrix}\lambda u_{1} + \mu u_{1} \\ \lambda u_{2} + \mu u_{2} \\ \vdots \\ \lambda u_{n} + \mu u_{n}\end{bmatrix} = \begin{bmatrix}\lambda u_{1} \\ \lambda u_{2} \\ \vdots \\ \lambda u_{n}\end{bmatrix} + \begin{bmatrix}\mu u_{1} \\ \mu u_{2} \\ \vdots \\ \mu u_{n}\end{bmatrix} = \lambda\begin{bmatrix}u_{1} \\ u_{2} \\ \vdots \\ u_{n}\end{bmatrix} + \mu\begin{bmatrix}u_{1} \\ u_{2} \\ \vdots \\ u_{n}\end{bmatrix} = \lambda\mathbf{u} + \mu\mathbf{u}$$
					$\lambda(\mathbf{u} + \mathbf{v}) = \lambda\mathbf{u} + \lambda\mathbf{v}$
						证明(proof):
$$\lambda(\mathbf{u} + \mathbf{v}) = \lambda(\begin{bmatrix}u_{1} \\ u_{2} \\ \vdots \\ u_{n}\end{bmatrix} + \begin{bmatrix}v_{1} \\ v_{2} \\ \vdots \\ v_{n}\end{bmatrix}) = \lambda\begin{bmatrix}u_{1} + v_{1} \\ u_{2} + v_{2} \\ \vdots \\ u_{n} + v_{n}\end{bmatrix} = \begin{bmatrix}\lambda(u_{1} + v_{1}) \\ \lambda(u_{2} + v_{2}) \\ \vdots \\ \lambda(u_{n} + v_{n})\end{bmatrix} = \begin{bmatrix}\lambda u_{1} + \lambda v_{1} \\ \lambda u_{2} + \lambda v_{2} \\ \vdots \\ \lambda u_{n} + \lambda v_{n}\end{bmatrix} = \begin{bmatrix}\lambda u_{1} \\ \lambda u_{2} \\ \vdots \\ \lambda u_{n}\end{bmatrix} + \begin{bmatrix}\lambda v_{1} \\ \lambda v_{2} \\ \vdots \\ \lambda v_{n}\end{bmatrix} = \lambda\begin{bmatrix}u_{1} \\ u_{2} \\ \vdots \\ u_{n}\end{bmatrix} + \lambda\begin{bmatrix}v_{1} \\ v_{2} \\ \vdots \\ v_{n}\end{bmatrix} = \lambda\mathbf{u} + \lambda\mathbf{v}$$
		**内积(inner product)**:
$$\langle\mathbf{u}, \mathbf{v}\rangle = \mathbf{u} \cdot \mathbf{v} = \begin{cases}\mathbf{u}^{T}\mathbf{v} = \begin{bmatrix}u_{1} & u_{2} & \dots & u_{n}\end{bmatrix}\begin{bmatrix}v_{1} \\ v_{2} \\ \vdots \\ v_{n}\end{bmatrix} = u_{1}v_{1} + u_{2}v_{2} + \dots + u_{n}v_{n}\text{, if }\mathbf{u}, \mathbf{v} \in \mathbb{R}^{n} \\ \mathbf{u}^{\dagger}\mathbf{v} = \begin{bmatrix}\overline{u_{1}} & \overline{u_{2}} & \dots & \overline{u_{n}}\end{bmatrix}\begin{bmatrix}v_{1} \\ v_{2} \\ \vdots \\ v_{n}\end{bmatrix} = \overline{u_{1}}v_{1} + \overline{u_{2}}v_{2} + \dots + \overline{u_{n}}v_{n}\text{, if }\mathbf{u}, \mathbf{v} \in \mathbb{C}^{n}\end{cases}$$
		**运算律**:
			**交换律(commutative law)**:
				在**n维实空间(n-d real space, $\mathbb{R}^{n}$)** 中，**满足** **交换律(commutative law)**: $\langle\mathbf{u}, \mathbf{v}\rangle = \mathbf{u} \cdot \mathbf{v} = \mathbf{v} \cdot \mathbf{u} = \langle\mathbf{v}, \mathbf{u}\rangle(\text{其中}\mathbf{u}, \mathbf{v} \in \mathbb{R}^{n})$
					证明(proof):
$$\langle\mathbf{u}, \mathbf{v}\rangle = \mathbf{u} \cdot \mathbf{v} = \mathbf{u}^{T}\mathbf{v} = \begin{bmatrix}u_{1} & u_{2} & \dots & u_{n}\end{bmatrix}\begin{bmatrix}v_{1} \\ v_{2} \\ \vdots \\ v_{n}\end{bmatrix} = u_{1}v_{1} + u_{2}v_{2} + \dots + u_{n}v_{n} = v_{1}u_{1} + v_{2}u_{2} + \dots + v_{n}u_{n} = \begin{bmatrix}v_{1} & v_{2} & \dots & v_{n}\end{bmatrix}\begin{bmatrix}u_{1} \\ u_{2} \\ \vdots \\ u_{n}\end{bmatrix} = \mathbf{v}^{T}\mathbf{u} = \mathbf{v} \cdot \mathbf{u} = \langle\mathbf{v}, \mathbf{u}\rangle$$
				在**n维复空间(n-d complex space, $\mathbb{C}^{n}$)** 中，**不满足** **交换律(commutative law)**: $\langle\mathbf{u}, \mathbf{v}\rangle = \mathbf{u} \cdot \mathbf{v} \neq \mathbf{v} \cdot \mathbf{u} = \langle\mathbf{v}, \mathbf{u}\rangle(\text{其中}\mathbf{u}, \mathbf{v} \in \mathbb{C}^{n})$
					证明(proof):
$$\langle\mathbf{u}, \mathbf{v}\rangle = \mathbf{u} \cdot \mathbf{v} = \mathbf{u}^{\dagger}\mathbf{v} = \begin{bmatrix}\overline{u_{1}} & \overline{u_{2}} & \dots & \overline{u_{n}}\end{bmatrix}\begin{bmatrix}v_{1} \\ v_{2} \\ \vdots \\ v_{n}\end{bmatrix} = \overline{u_{1}}v_{1} + \overline{u_{2}}v_{2} + \dots + \overline{u_{n}}v_{n} \neq \overline{v_{1}}u_{1} + \overline{v_{2}}u_{2} + \dots + \overline{v_{n}}u_{n} = \begin{bmatrix}\overline{v_{1}} & \overline{v_{1}} & \dots & \overline{v_{n}}\end{bmatrix}\begin{bmatrix}u_{1} \\ u_{2} \\ \vdots \\ u_{n}\end{bmatrix} = \mathbf{v}^{\dagger}\mathbf{u} = \mathbf{v} \cdot \mathbf{u} = \langle\mathbf{v}, \mathbf{u}\rangle$$
		**性质(property)**:
			**共轭对称性(conjugate symmetry)**: $\langle\mathbf{u}, \mathbf{v}\rangle = \mathbf{u} \cdot \mathbf{v} = \overline{\mathbf{v} \cdot \mathbf{u}} = \overline{\langle\mathbf{v}, \mathbf{u}\rangle}(\text{其中}\mathbf{u}, \mathbf{v} \in \mathbb{C}^{n})$
				证明(proof):
$$\langle\mathbf{u}, \mathbf{v}\rangle = \mathbf{u} \cdot \mathbf{v} = \mathbf{u}^{\dagger}\mathbf{v} = \begin{bmatrix}\overline{u_{1}} & \overline{u_{2}} & 
\dots & \overline{u_{n}}\end{bmatrix}\begin{bmatrix}v_{1} \\ v_{2} \\ \vdots \\ v_{n}\end{bmatrix} = \overline{u_{1}}v_{1} + \overline{u_{2}}v_{2} + \dots + \overline{u_{n}}v_{n} = v_{1}\overline{u_{1}} + v_{2}\overline{u_{2}} + \dots + v_{n}\overline{u_{n}} = \overline{\overline{v_{1}}u_{1} + \overline{v_{2}}u_{2} + \dots + \overline{v_{n}}u_{n}} = \overline{\begin{bmatrix}\overline{v_{1}} & \overline{v_{2}} & \dots & \overline{v_{n}}\end{bmatrix}\begin{bmatrix}u_{1} \\ u_{2} \\ \vdots \\ u_{n}\end{bmatrix}} = \overline{\mathbf{v}^{\dagger}\mathbf{u}} = \overline{\mathbf{v} \cdot \mathbf{u}} = \overline{\langle\mathbf{v}, \mathbf{u}\rangle}$$
	**模(modulus)**:
$$||\mathbf{u}|| = \sqrt{\langle\mathbf{u}, \mathbf{u}\rangle} = \sqrt{\mathbf{u} \cdot \mathbf{u}} = \begin{cases}\sqrt{\mathbf{u}^{T}\mathbf{u}} = \sqrt{\begin{bmatrix}u_{1} & u_{2} & \dots & u_{n}\end{bmatrix}\begin{bmatrix}u_{1} \\ u_{2} \\ \vdots \\ u_{n}\end{bmatrix}} = \sqrt{u_{1}^{2} + u_{2}^{2} + \dots + u_{n}^{2}}\text{, if }\mathbf{u} \in \mathbb{R}^{n} \\ \sqrt{\mathbf{u}^{\dagger}\mathbf{u}} = \sqrt{\begin{bmatrix}\overline{u_{1}} & \overline{u_{2}} & \dots & \overline{u_{n}}\end{bmatrix}\begin{bmatrix}u_{1} \\ u_{2} \\ \vdots \\ u_{n}\end{bmatrix}} = \sqrt{\overline{u_{1}}u_{1} + \overline{u_{2}}u_{2} + \dots + \overline{u_{n}}u_{n}} = \sqrt{|u_{1}|^{2} + |u_{2}|^{2} + \dots + |u_{n}|^{2}}\text{, if }\mathbf{u} \in \mathbb{C}^{n}\end{cases}$$
	**线性组合(linear combination)**:
$$c_{1}\mathbf{u_{1}} + c_{2}\mathbf{u_{2}} + \dots + c_{m}\mathbf{u_{m}} = c_{1}\begin{bmatrix}u_{11} \\ u_{12} \\ \vdots \\ u_{1n}\end{bmatrix} + c_{2}\begin{bmatrix}u_{21} \\ u_{22} \\ \vdots \\ u_{2n}\end{bmatrix} + \dots + c_{m}\begin{bmatrix}u_{m1} \\ u_{m2} \\ \vdots \\ u_{mn}\end{bmatrix} = \begin{bmatrix}c_{1}u_{11} \\ c_{1}u_{12} \\ \vdots \\ c_{1}u_{1n}\end{bmatrix} + \begin{bmatrix}c_{2}u_{21} \\ c_{2}u_{22} \\ \vdots \\ c_{2}u_{2n}\end{bmatrix} + \dots + \begin{bmatrix}c_{m}u_{m1} \\ c_{m}u_{m2} \\ \vdots \\ c_{m}u_{mn}\end{bmatrix} = \begin{bmatrix}c_{1}u_{11} + c_{2}u_{21} + \dots + c_{m}u_{m1} \\ c_{1}u_{12} + c_{2}u_{22} + \dots + c_{m}u_{m2} \\ \vdots \\ c_{1}u_{1n} + c_{2}u_{2n} + \dots + c_{m}u_{mn}\end{bmatrix}(\text{其中}c_{1}, c_{2}, \dots, c_{m} \in \begin{cases}\mathbb{R}\text{, if }\mathbf{u_{1}}, \mathbf{u_{2}}, \dots, \mathbf{u_{m}} \in \mathbb{R}^{n} \\ \mathbb{C}\text{, if }\mathbf{u_{1}}, \mathbf{u_{2}}, \dots, \mathbf{u_{m}} \in \mathbb{C}^{n}\end{cases})$$
	**线性无关(linear independence)**: $c_{1}\mathbf{u_{1}} + c_{2}\mathbf{u_{2}} + \dots + c_{m}\mathbf{u_{m}} = \mathbf{0}(\text{其中}c_{1}, c_{2}, \dots, c_{m} \in \begin{cases}\mathbb{R}\text{, if }\mathbf{u_{1}}, \mathbf{u_{2}}, \dots, \mathbf{u_{m}} \in \mathbb{R}^{n} \\ \mathbb{C}\text{, if }\mathbf{u_{1}}, \mathbf{u_{2}}, \dots, \mathbf{u_{m}} \in \mathbb{C}^{n}\end{cases})$ **有唯一零解** v.s. **线性相关(linear dependence)**: $c_{1}\mathbf{u_{1}} + c_{2}\mathbf{u_{2}} + \dots + c_{m}\mathbf{u_{m}} = \mathbf{0}(\text{其中}c_{1}, c_{2}, \dots, c_{m} \in \begin{cases}\mathbb{R}\text{, if }\mathbf{u_{1}}, \mathbf{u_{2}}, \dots, \mathbf{u_{m}} \in \mathbb{R}^{n} \\ \mathbb{C}\text{, if }\mathbf{u_{1}}, \mathbf{u_{2}}, \dots, \mathbf{u_{m}} \in \mathbb{C}^{n}\end{cases})$ **有无数解**
	**基(basis, $\{\mathbf{u_{1}}, \mathbf{u_{2}}, \dots, \mathbf{u_{m}}\}$)**: $\mathbf{u_{1}}$, $\mathbf{u_{2}}$, $\dots$, $\mathbf{u_{m}}$ **线性无关(linearly independent)** 且$\mathrm{span}\{\mathbf{u_{1}}, \mathbf{u_{2}}, \dots, \mathbf{u_{m}}\} = V$
		**正交基(orthogonal basis)**: $\{\mathbf{u_{1}}, \mathbf{u_{2}}, \dots, \mathbf{u_{m}}\}$ 为**向量空间(vector space)V**的一组**基(basis)**，且$\mathbf{u_{1}}$, $\mathbf{u_{2}}$, $\dots$, $\mathbf{u_{m}}$**两两正交(orthogonal)**(i.e. **两两内积(inner product)** 为**0**)
$$\langle\mathbf{u_{i}}, \mathbf{u_{j}}\rangle = 0(\text{其中}i \neq j, 1 \leq i, j \leq m)$$
			**正交归一基(orthonormal basis)**: $\{\mathbf{u_{1}}, \mathbf{u_{2}}, \dots, \mathbf{u_{m}}\}$为**向量空间(vector space)V**的一组**基(basis)**，且$\mathbf{u_{1}}$, $\mathbf{u_{2}}$, $\dots$, $\mathbf{u_{m}}$的**模(modulus)** 均为**1**(i.e. **自己与自己内积(inner product)** 为**1**)
$$(\langle\mathbf{u_{i}}, \mathbf{u_{j}}\rangle = 0(\text{其中}i \neq j, 1 \leq i, j \leq m)\text{且}||\mathbf{u_{i}}|| = \sqrt{\langle\mathbf{u_{i}}, \mathbf{u_{i}}\rangle} = 1 \Leftrightarrow \langle\mathbf{u_{i}, \mathbf{u_{i}}}\rangle = 1(\text{其中}1 \leq i \leq m)) \Leftrightarrow \langle\mathbf{u_{i}, \mathbf{u_{j}}}\rangle = \delta_{ij} = \begin{cases}1\text{, if }i = j \\ 0\text{, if }i \neq j\end{cases}(\text{其中}1 \leq i, j \leq m)$$
			(其中$\delta_{ij} = \begin{cases}1\text{, if }i = j \\ 0\text{, if }i \neq j\end{cases}$为**克罗内克$\delta$函数(Kronecker delta function)**)
**张量积(tensor product)/克罗内克积(Kronecker product)**:
$$\begin{cases}A = \begin{bmatrix}a_{0, 0} & \cdots & a_{0, n - 1} \\ \vdots & \ddots & \vdots \\ a_{m - 1, 0} & \cdots & a_{m - 1, n - 1}\end{bmatrix}_{m \times n} \\ B = \begin{bmatrix}b_{0, 0} & \cdots & b_{0, q - 1} \\ \vdots & \ddots & \vdots \\ b_{p - 1, 0} & \cdots & b_{p - 1, q - 1}\end{bmatrix}_{p \times q}\end{cases} \Rightarrow A \otimes B = \begin{bmatrix}a_{0, 0}B & \cdots & a_{0, n - 1}B \\ \vdots & \ddots & \vdots \\ a_{m - 1, 0}B & \cdots & a_{m - 1, n - 1}B\end{bmatrix}_{mp \times nq}$$

运算律(operation law):
	不满足交换律(communicative law):
$$A \otimes B \neq B \otimes A$$
	满足结合律(associative law):
$$(\lambda|A\rangle) \otimes |B\rangle = \lambda(|A\rangle \otimes |B\rangle) = |A\rangle(\lambda |B\rangle)$$
$$(A \otimes B) \otimes C = A \otimes B \otimes C = A \otimes (B \otimes C)$$
	满足分配律(distributive law):
		满足左分配律(left distributive law):
$$|A\rangle \otimes (|B\rangle + |C\rangle) = |A\rangle \otimes |B\rangle + |A\rangle \otimes |C\rangle$$
		(其中B和C大小相同)
		满足右分配律(right distributive law):
$$(|A\rangle + |B\rangle) \otimes |C\rangle = |A\rangle \otimes C + |B\rangle \otimes |C\rangle$$
		(其中B和C大小相同)
	混合乘积性质:
$$(A \otimes B) \cdot (C \otimes D) = (A \cdot C) \otimes (B \cdot D)$$
	(其中A $\cdot$ C和B $\cdot$ D存在)
$$(A \otimes B \otimes C) \cdot (D \otimes E \otimes F) = (A \cdot D) \otimes (B \cdot E) \otimes (C \cdot F)$$
		证明(proof):
$$(A \otimes B \otimes C) \cdot (D \otimes E \otimes F) = [A \otimes (B \otimes C)] \cdot [D \otimes (E \otimes F)] = (A \cdot D) \otimes [(B \otimes C) \cdot (E \otimes F)] = (A \cdot D) \otimes [(B \cdot E) \otimes (C \cdot F)] = (A \cdot D) \otimes (B \cdot E) \otimes (C \cdot F)$$
	(其中A $\cdot$ D, B $\cdot$ E和C $\cdot$ F存在)
	推论(corollary):
$$(A_{1} \otimes A_{2} \otimes \dots \otimes A_{n}) \cdot (B_{1} \otimes B_{2} \otimes ... \otimes B_{n}) = (A_{1} \cdot B_{1}) \otimes (A_{2} \cdot B_{2}) \otimes \dots \otimes (A_{n} \cdot B_{n})$$
	(条件略)

两个向量空间(vector space)的张量积(tensor product):

$$V \otimes W = \text{span}\{v_{i} \otimes w_{j}\}$$
(其中1 $\leq$ i $\leq$ m, 1 $\leq$ j $\leq$ n)
两个向量空间(vector space)的笛卡尔积(Cartesian product):
已知V = span{$v_{1}$, $v_{2}$, ..., $v_{m}$}, W = span{$w_{1}$, $w_{2}$, ..., $w_{n}$}
$$V \times W = \{(v, w) | v \in V, w \in W\} = \{v \otimes w | v \in V, w \in W\}$$

两个向量空间(vector space)的笛卡尔积(Cartesian product)是两个向量空间(vector space)的张量积(tensor product)的真子集(proper subset):
$$V \times W \subsetneq V \otimes W$$
**线性变换(linear transformation)**: 一个**向量空间(vector space)** 到另一个**向量空间(vector space)** 的**线性映射(linear mapping)**
$$V \stackrel{T}{\rightarrow} W$$
	**线性(linearity)**:
$$\begin{cases}T(\mathbf{0}) = T(\mathbf{0}) \\ T(\mathbf{u} + \mathbf{v}) = T(\mathbf{u}) + T(\mathbf{v}) \\ T(c\mathbf{u}) = cT(\mathbf{v})\end{cases}$$
	**n维复空间(n-d complex space)** 到**m维复空间(m-d complex space)** 的**线性变换(linear transformation)**:
$$\mathbb{C}^{n} \stackrel{T}{\rightarrow} \mathbb{C}^{m}$$
		**代数表示(algebraic representation)**:
$$T(\mathbf{v}) = \mathbf{A}\mathbf{v}$$
		(其中**A**为**m $\times$ n复矩阵(m $\times$ n complex matrix)**)
**仿射变换(affine transformation)**: **线性变换(linear transformation)** + **平移变换(translation transformation)**
$$V \stackrel{T}{\rightarrow} W$$
	**性质(property)**:
		保持**共线性(colinearity)**、**平行性(parallelism)** 和**平行线段的长度比**
	**n维复空间(n-d complex space)** 到**m维复空间(m-d complex space)** 的**仿射变换(affine transformation)**:
$$\mathbb{C}^{n} \stackrel{T}{\rightarrow} \mathbb{C}^{m}$$
		**代数表示(algebraic representation)**:
$$T(\mathbf{v}) = \mathbf{A}\mathbf{v} + \mathbf{b} \Leftrightarrow \begin{bmatrix}T(\mathbf{v}) \\ 1\end{bmatrix} = \begin{bmatrix}\mathbf{A} & \mathbf{b} \\ 0 \dots 0 & 1\end{bmatrix}\begin{bmatrix}\mathbf{v} \\ 1\end{bmatrix}$$
		(其中**A** 为**m $\times$ n复矩阵(m $\times$ n complex matrix)**，$\mathbf{b}$为**m维复向量(m-d complex vector)**)
		例: **平移变换(translation transformation)**、**旋转变换(rotation transformation)**、**缩放变换(scaling transformation)**、**错切变化(shearing transformation)**
矩阵(matrix)A:
$$A = \begin{bmatrix}a_{0, 0} & a_{0, 1} & \cdots & a_{0, n - 1} \\ a_{1, 0} & a_{1, 1} & \cdots & a_{1, n - 1} \\ \vdots & \vdots & \ddots & \vdots \\ a_{m - 1, 0} & a_{m - 1, 1} & \cdots & a_{m - 1, n - 1}\end{bmatrix}_{m \times n}$$
矩阵(matrix)A的转置(transpose)$A^{T}$: $A^{T}_{i, j} = A_{j, i}$
$$A^{T} = \begin{bmatrix}a_{0, 0} & a_{1, 0} & \cdots & a_{m - 1, 0} \\ a_{0, 1} & a_{1, 1} & \cdots & a_{m - 1, 1} \\ \vdots & \vdots & \ddots & \vdots \\ a_{0, n - 1} & a_{1, n - 1} & \cdots & a_{m - 1, n - 1}\end{bmatrix}_{n \times m}$$
矩阵(matrix)A的共轭(conjugate)$\overline{A}$: $\overline{A}_{i, j} = \overline{A_{i, j}}$
$$\overline{A} = \begin{bmatrix}\overline{a_{0, 0}} & \overline{a_{0, 1}} & \dots & \overline{a_{0, n - 1}} \\ \overline{a_{1, 0}} & \overline{a_{1, 1}} & \dots & \overline{a_{1, n - 1}} \\ \vdots & \vdots & \ddots & \vdots \\ \overline{a_{m - 1, 0}} & a_{m - 1, 1} & \dots & \overline{a_{m - 1, n - 1}}\end{bmatrix}_{m \times n}$$
矩阵(matrix)A的共轭转置(conjugate transpose)$A^{\dagger}$/伴随(矩阵)(adjoint( matrix))adjA/$A^{*}$: $A^{\dagger}_{i, j} = \overline{A_{j, i}}$
$$A^{\dagger} = \overline{A}^{T} = \overline{A^{T}} = \begin{bmatrix}\overline{a_{0, 0}} & \overline{a_{1, 0}} & \cdots & \overline{a_{m - 1, 0}} \\ \overline{a_{0, 1}} & \overline{a_{1, 1}} & \cdots & \overline{a_{m - 1, 1}} \\ \vdots & \vdots & \ddots & \vdots \\ \overline{a_{0, n - 1}} & \overline{a_{1, n - 1}} & \cdots & \overline{a_{m - 1, n - 1}}\end{bmatrix}_{n \times m}$$
**可逆矩阵(invertible matrix)**: $\exists$$A^{-1}$ s.t. $A^{-1}A = AA^{-1} = I$的复矩阵(complex matrix)
	注: 可逆矩阵(invertible matrix)必为方阵(squared matrix)
(特化)**对合矩阵(involutory matrix)**: 自逆(self-inverse)的复矩阵(complex matrix)，即逆(矩阵)(inverse( matrix))为本身的复矩阵(complex matrix)
$$A^{2} = I\text{，即}A^{-1} = A$$
	注: 对合矩阵(involutory matrix)必为方(块矩)阵(squared matrix)

**对称矩阵(symmetric matrix)**: 自转置(self-transpose)的复矩阵(complex matrix)，即转置(transpose)为本身的复矩阵(complex matrix)
$$A^{T} = A \Leftrightarrow A_{i, j} = A^{T}_{j, i} = A_{j, i}$$
	注: 对称矩阵(symmetric matrix)必为方(块矩)阵(squared matrix)，且关于主对角线(main diagonal)对称
(推广)**埃尔米特矩阵(Hermitian matrix)**: 自伴随(self-adjoint)的复矩阵(complex matrix)，即伴随(adjoint)/共轭转置(conjugate transpose)为本身的复矩阵(complex matrix)
$$A^{\dagger}/adjA/A^{*}/A^{H} = A_{i, j} = \overline{A^{\dagger}_{j, i}} = \overline{A_{j, i}}$$
	注: 埃尔米特矩阵(Hermitian matrix)必为方(块矩)阵(square matrix)，关于主对角线(main diagonal)共轭对称且主对角线(main diagonal)上的元素均为实数(real number)
注: 实对称矩阵(real symmetric matrix) $\subset$ 埃尔米特矩阵(Hermitian matrix)

**正交矩阵(orthogonal matrix)**: 逆(矩阵)(inverse( matrix))为转置(transpose)的实矩阵(real matrix)
$$Q^{T}Q = QQ^{T} = I\text{，即}Q^{-1} = Q^{T}$$
	注: 正交矩阵(orthogonal matrix)必为方(块矩)阵(square( matrix))
	性质(property): 正交矩阵(orthogonal matrix)的所有列向量(column vector)都是正交归一(orthonormal)的，所有行向量(row vector)也都是正交归一(orthonormal)的
		(以2 $\times$ 2正交矩阵(orthogonal matrix)为例)
$$\begin{cases}\mathbf{r_{1}} \cdot \mathbf{r_{2}} = q_{00}q_{10} + q_{01}q_{11} = 0 \\ ||\mathbf{r_{1}}|| = \sqrt{q_{00}^{2} + q_{01}^{2}} = 1 \\ ||\mathbf{r_{2}}|| = \sqrt{q_{10}^{2} + q_{11}^{2}} = 1\end{cases} \Leftarrow Q = \begin{bmatrix}q_{00} & q_{01} \\ q_{10} & q_{11}\end{bmatrix} \Rightarrow \begin{cases}\mathbf{c_{1}} \cdot \mathbf{c_{2}} = q_{00}q_{01} + q_{10}q_{11} = 0 \\ ||\mathbf{c_{1}}|| = \sqrt{q_{00}^{2} + q_{10}^{2}} = 1 \\ ||\mathbf{c_{2}}|| = \sqrt{q_{01}^{2} + q_{11}^{2}} = 1\end{cases}$$
	正交矩阵(orthogonal matrix)对应的线性变换(linear transformation)为**正交变换(orthogonal transformation)**，正交变换(orthogonal transformation)不会改变向量(vector)的长度(length)
$$||Q\mathbf{v}|| = ||\mathbf{v}||$$
(推广)**酉矩阵/幺正矩阵(unitary matrix)**: 逆(矩阵)(inverse( matrix))为伴随(adjoint)/共轭转置(conjugate transpose)的复矩阵(complex matrix)
$$U^{\dagger}U = UU^{\dagger} = I\text{，即}U^{-1} = U^{\dagger}$$
	注: 酉矩阵(unitary matrix)必为方(块矩)阵(square matrix)
	性质(property): 酉矩阵(unitary matrix)的所有列向量(column vector)都是正交归一(orthonormal)的，所有行向量(row vector)也都是正交归一(orthonormal)的
		(以2 $\times$ 2正交矩阵(orthogonal matrix)为例)
$$\begin{cases}\mathbf{r_{1}} \cdot \mathbf{r_{2}} = u_{00}u_{10} + u_{01}u_{11} \\ ||\mathbf{r_{1}}|| = \sqrt{u_{00}^{2} + u_{01}^{2}} \\ ||\mathbf{r_{2}}|| = \sqrt{u_{10}^{2} + u_{11}^{2}}\end{cases} \Leftarrow U = \begin{bmatrix}u_{00} & u_{01} \\ u_{10} & u_{11}\end{bmatrix} \Rightarrow \begin{cases}\mathbf{c_{1}} \cdot \mathbf{c_{2}} = u_{00}u_{01} + u_{10}u_{11} \\ ||\mathbf{c_{1}}|| = \sqrt{u_{00}^{2} + u_{10}^{2}} \\ ||\mathbf{c_{2}}|| = \sqrt{u_{01}^{2} + u_{11}^{2}}\end{cases}$$
	酉矩阵(unitary matrix)对应的线性变换(linear transformation)为**酉变换(unitary transformation)**，酉变换不会改变向量(vector)的长度(length)
$$||U\mathbf{v}|| = ||\mathbf{v}||$$
注: 对合矩阵(involutory matrix)、埃尔米特矩阵(Hermitian matrix)和酉矩阵(unitary matrix)知二推一

克罗内克