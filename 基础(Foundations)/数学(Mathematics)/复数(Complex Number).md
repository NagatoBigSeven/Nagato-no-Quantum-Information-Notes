**虚数单位(imaginary unit)**: **-1**的**算术平方根(arithmetic square root)**
$$i = \sqrt{-1}$$
	**性质(property)**: $i^{2} = -1$
		证明(proof): $i^{2} = (\sqrt{-1})^{2} = -1$
**复数(complex number)** 的**代数表示(algebraic representation)**: $z = a + bi = (a, b)$(其中a, b $\in$ R，**a** 为**实部(real part, $\mathfrak{R}$)**，**b** 为**虚部(imaginary part, $\mathfrak{I}$)**)
**复数(complex number)**:
	**实数(real number)**: **虚部(imaginary part, $\mathfrak{I}$)** 为**0**(**b = 0**)
		**有理数(rational number)**:
			**整数(integer)**:
				**自然数(natural number)**:
					**正整数(positive integer, +ve integer)**
					**零(zero, 0)**
				**负整数(negative integer, -ve integer)**
			**分数(fraction)**
		**无理数(irrational number)**
	**虚数(imaginary number)**: **虚部(imaginary part, $\mathfrak{I}$)** 不为**0**(**b $\neq$ 0**)
		**纯虚数(pure imaginary number)**:  **实部(real part, $\mathfrak{R}$)** 为**0**(**a = 0**)
		...
**复数(complex number)** 的**几何意义**: **复平面(complex plane)** 上的**点(point)Z(a, b)** 或**复平面(complex plane)** 上从**原点(origin)O(0, 0)** 指向**点(point)Z(a, b)** 的**二维向量(2-d vector)$\vec{OZ} = (a, b)$**
**复数(complex number)** 的**向量表示(vector representation)**: **二维实列向量(2-d real column vector)**$z = \begin{bmatrix}a \\ b\end{bmatrix}$
**复数(complex number)** 的**矩阵表示(matrix representation)**: **2 $\times$ 2实矩阵(2 $\times$ 2 real matrix)**$z = \begin{bmatrix}a & -b \\ b & a\end{bmatrix}$
**复数(complex number)** 的**运算(operation)**:
	**加法(addition)**:
		**代数表示(algebraic representation)**: **实部(real part, $\mathfrak{R}$)加实部(real part, $\mathfrak{R}$)** 得**新实部(real part, $\mathfrak{R}$)**，**虚部(imaginary part, $\mathfrak{I}$)加虚部(imaginary part, $\mathfrak{I}$)** 得**新虚部(imaginary part, $\mathfrak{I}$)**
$$z_{1} + z_{2} = (a + bi) + (c + di) = (a + c) + (b + d)i = (a + c, b + d)$$
		**几何意义(geometric meaning)**: **复平面(complex plane)** 上的**向量(vector)**$\vec{OZ_{1}} = (a, b)$ 与**向量(vector)**$\vec{OZ_{2}} = (c, d)$的**和向量(sum vector)**
		**向量表示(vector representation)**: **被加数(augend)** 对应的**二维实列向量(2-d real column vector)加加数(addend)** 对应的**二维实列向量(2-d real column vector)**
$$z_{1} + z_{2} = \begin{bmatrix}a \\ b\end{bmatrix} + \begin{bmatrix}c \\ d\end{bmatrix} = \begin{bmatrix}a + c \\ b + d\end{bmatrix}$$
	**减法(subtraction)**:
		**代数表示(algebraic representation)**: **实部(real part, $\mathfrak{R}$)减实部(real part, $\mathfrak{R}$)** 得**新实部(real part, $\mathfrak{R}$)**，**虚部(imaginary part, $\mathfrak{I}$)减虚部(imaginary part, $\mathfrak{I}$)** 得**新虚部(imaginary part, $\mathfrak{I}$)**
$$z_{1} - z_{2} = (a + bi) - (c + di) = (a - c) + (b - d)i = (a - c, b - d)$$
		**几何意义**: **复平面(complex plane)** 上的**向量(vector)**$\vec{OZ_{1}} = (a, b)$与 **向量(vector)**$\vec{OZ_{2}} = (c, d)$的**差向量(difference vector)**
		**向量表示(vector representation)**: **被减数(minuend)** 对应的**二维实列向量(2-d real column vector)减减数(subtrahend)** 对应的**二维实列向量(2-d real column vector)**
$$z_{1} - z_{2} = \begin{bmatrix}a \\ b\end{bmatrix} - \begin{bmatrix}c \\ d\end{bmatrix} = \begin{bmatrix}a - c \\ b - d\end{bmatrix}$$
	**乘法(multiplication)**:
		**代数表示(algebraic representation)**: **实部(real part, $\mathfrak{R}$)乘实部(real part, $\mathfrak{R}$)减虚部(imaginary part, $\mathfrak{I}$)乘虚部(imaginary part, $\mathfrak{I}$)** 得**新实部(real part, $\mathfrak{R}$)**，**实部(real part, $\mathfrak{R}$)** 与**虚部(imaginary part, $\mathfrak{I}$)交叉相乘后相加** 得**新虚部(imaginary part, $\mathfrak{I}$)**
$$z_{1}z_{2} = (a + bi)(c + di) = ac + adi + bci + bdi^{2} = ac + adi + bci - bd = (ac - bd) + (ad + bc)i = (ac - bd, ad + bc)$$
		**向量表示(vector representation)**: 不是**被乘数(multiplicand)** 对应的**二维实列向量(2-d real column vector)乘以乘数(multiplier)** 对应的**二维实列向量(2-d real column vector)**，因为二者维度不匹配，而是**被乘数(multiplicand)** 对应的**2 $\times$ 2实矩阵(2 $\times$ 2 real matrix)乘以乘数(multiplier)** 对应的**二维实列向量(2-d real column vector)**
$$z_{1}z_{2} = \begin{bmatrix}a & -b \\ b & a\end{bmatrix}\begin{bmatrix}c \\ d\end{bmatrix} = \begin{bmatrix}ac - bd \\ bc + ad\end{bmatrix} = \begin{bmatrix}ac - bd \\ ad + bc\end{bmatrix}$$
	**除法(division)**:
		**代数表示(algebraic representation)**:
$$\frac{z_{1}}{z_{2}} = \frac{a + bi}{c + di} = \frac{(a + bi)(c - di)}{(c + di)(c - di)} = \frac{ac - adi + bci - bdi^{2}}{c^{2} - d^{2}i^{2}} = \frac{ac - adi + bci + bd}{c^{2} + d^{2}} = \frac{(ac + bd) + (bc - ad)i}{c^{2} + d^{2}} = \frac{1}{c^{2} + d^{2}}(ac + bd, bc - ad)$$
		**向量表示(vector representation)**: 不是**被除数(dividend)** 对应的**二维实列向量(2-d real column vector)除以除数(divisor)** 对应的**二维实列向量(2-d real column vector)**，因为**向量(vector)无除法(division)**，而是**除数(divisor)** 对应的**2 $\times$ 2实矩阵(2 $\times$ 2 real matrix)** 的**逆(矩阵)(inverse( matrix))乘以被除数(dividend)** 对应的**二维实列向量(2-d real column vector)**
$$\frac{z_{1}}{z_{2}} = z_{2}^{-1}z_{1} = \begin{bmatrix}c & -d \\ d & c\end{bmatrix}^{-1}\begin{bmatrix}a \\ b\end{bmatrix} = \frac{1}{c^{2} + d^{2}}\begin{bmatrix}c & d \\ -d & c\end{bmatrix}\begin{bmatrix}a \\ b\end{bmatrix} = \frac{1}{c^{2} + d^{2}}(\begin{bmatrix}ac + bd \\ -ad + bc\end{bmatrix}) = \frac{1}{c^{2} + d^{2}}\begin{bmatrix}ac + bd \\ bc - ad\end{bmatrix}$$
**模(modulus)**:
	**代数表示(algebraic representation)**: **实部(real part, $\mathfrak{R}$)** 与**虚部(imaginary part, $\mathfrak{I}$)** 的 **平方和(sum of squares)** 的**算术平方根(arithmetic square root)**
$$|z| = \sqrt{a^{2} + b^{2}}$$
	**几何意义**: **原点(origin)** 到**点(point)Z(a, b)** 的**欧几里得距离(Euclidean distance)**，即**向量(vector)$\vec{OZ} = (a, b)$** 的**长度(length)**
**共轭(conjugate)**:
	**代数表示(algebraic representation)**: **实部(real part, $\mathfrak{R}$)不变**，**虚部(imaginary part, $\mathfrak{I}$)** 变为原来的**相反数**
$$\overline{z} = a - bi = (a, -b)$$
	**几何意义**: 将**点(point)Z(a, b)**(i.e. **向量(vector)**$\vec{OZ} = (a, b)$)**关于x轴(x-axis)对称** 到**点(point)Z'(a, -b)**(i.e. **向量(vector)**$\vec{OZ^{'}} = (a, -b)$)
	**性质(property)1**: **复数(complex number)** 与**共轭(conjugate)** 之**积(product)** 等于**模(modulus)** 的**平方(square)**
$$z\overline{z} = |z|^{2}$$
		证明(proof):
$$z\overline{z} = (a + bi)(a - bi) = a^{2} - b^{2}i^{2} = a^{2} + b^{2} = |z|^{2}$$
	**性质(property)2**: **和(sum)** 的**共轭(conjugate)** 等于**共轭(conjugate)** 的**和(sum)**
$$\overline{z_{1} + z_{2}} = \overline{z_{1}} + \overline{z_{2}}$$
		证明(proof):
$$\overline{z_{1} + z_{2}} = \overline{(a + bi) + (c + di)} = \overline{(a + c) + (b + d)i} = (a + c) - (b + d)i = (a - bi) + (c - di) = \overline{z_{1}} + \overline{z_{2}}$$
	**性质(property)3**: **积(product)** 的**共轭(conjugate)** 等于**共轭(conjugate)** 的**积(product)**
$$\overline{z_{1}z_{2}} = \overline{z_{1}} \cdot \overline{z_{2}}$$
		证明(proof):
$$\overline{z_{1}z_{2}} = \overline{(a + bi)(c + di)} = \overline{(ac - bd) + (ad + bc)i} = (ac - bd) - (ad + bc)i = (ac + bdi^{2}) - (ad + bc)i = (ac - adi) - (bci - bdi^{2}) = a(c - di) - bi(c - di) = (a - bi)(c - di) = \overline{z_{1}} \cdot \overline{z_{2}}$$
**复数(complex number)** 的**三角表示(trigonometric representation)**:
$$z = a + bi = \sqrt{a^{2} + b^{2}}(\frac{a}{\sqrt{a^{2} + b^{2}}} + \frac{b}{\sqrt{a^{2} + b^{2}}}i) = |z|(\frac{a}{|z|} + \frac{b}{|z|}) \stackrel{\begin{cases}r = |z| = \sqrt{a^{2} + b^{2}} \\ \cos{\theta} = \frac{a}{r} = \frac{a}{|z|} = \frac{a}{\sqrt{a^{2} + b^{2}}} \\ \sin{\theta} = \frac{b}{r} = \frac{b}{|z|} = \frac{b}{\sqrt{a^{2} + b^{2}}}\end{cases}}{=} r(\cos{\theta} + i\sin{\theta}) = (r, \theta)$$
(其中$\theta$为**复数(complex number)z** 的**辐角(argument, $\arg(\cdot)$)**，即以**x轴(x-axis)非负半轴** 为**始边**，**射线OZ** 为**终边**的角)
再论**复数(complex number)乘法(multiplication)**:
	**三角表示(trigonometric representation)**: **模(modulus)乘模(modulus)** 得**新模(modulus)**，**辐角(argument, $\arg(\cdot)$)加辐角(argument, $\arg(\cdot)$)** 得**新辐角(argument, $\arg(\cdot)$)**
$$z_{1}z_{2} = r_{1}r_{2}[\cos{(\theta_{1} + \theta_{2}) + i\sin{(\theta_{1} + \theta_{2})}}] = (r_{1}r_{2}, \theta_{1} + \theta_{2})$$
		证明(proof):
$$z_{1}z_{2} = r_{1}(\cos{\theta_{1}} + i\sin{\theta_{1}})r_{2}(\cos{\theta_{2}} + i\sin{\theta_{2}}) = r_{1}r_{2}(\cos{\theta_{1}} + i\sin{\theta_{1}})(\cos{\theta_{2}} + i\sin{\theta_{2}}) = r_{1}r_{2}[(\cos{\theta_{1}}\cos{\theta_{2}} - \sin{\theta_{1}}\sin{\theta_{2}}) + i(\sin{\theta_{1}}\cos{\theta_{2}} + \cos{\theta_{1}}\sin{\theta_{2}})] = r_{1}r_{2}[\cos(\theta_{1} + \theta_{2}) + \sin(\theta_{1} + \theta_{2})] = (r_{1}r_{2}, \theta_{1} + \theta_{2})$$
	**几何意义**: 将**向量(vector)**$\vec{OZ_{1}}$绕**原点(origin)O(0, 0)逆时针(counterclockwise)旋转(rotate)**$\theta_{2}$，**长度(length)** 变为原来的$r_{2}$**倍**
再论**复数(complex number)除法(division)**:
	**三角表示(trigonometric representation)**: **模(modulus)除以模(modulus)** 得**新模(modulus)**，**辐角(argument, $\arg(\cdot)$)减辐角(argument, $\arg(\cdot)$)** 得**新辐角(argument, $\arg(\cdot)$)**
$$\frac{z_{1}}{z_{2}} = \frac{r_{1}}{r_{2}}[\cos{(\theta_{1} - \theta_{2})} + i\sin{(\theta_{1} - \theta_{2})}] = (\frac{r_{1}}{r_{2}}, \theta_{1} - \theta_{2})$$
		证明(proof):
$$\frac{z_{1}}{z_{2}} = \frac{r_{1}(\cos{\theta_{1} + i\sin{\theta_{1}}})}{r_{2}(\cos{\theta_{2}} + i\sin{\theta_{2}})} = \frac{r_{1}}{r_{2}} \cdot \frac{(\cos{\theta_{1}}\cos{\theta_{2}} + \sin{\theta_{1}}\sin{\theta_{2}}) + i(\sin{\theta_{1}}\cos{\theta_{2}} - \cos{\theta_{1}}\sin{\theta_{2}})}{\sin^{2}{\theta_{2}} + \cos^{2}{\theta_{2}}} = \frac{r_{1}}{r_{2}}[\cos(\theta_{1} - \theta_{2}) + i\sin(\theta_{1} - \theta_{2})] = (\frac{r_{1}}{r_{2}}, \theta_{1} - \theta_{2})$$
	**几何意义**: 将**向量(vector)**$\vec{OZ_{1}}$的模绕**原点(origin)O(0, 0)顺时针(clockwise)旋转(rotate)**$\theta_{2}$，**长度(length)** 变为原来的$\frac{1}{r_{2}}$
**欧拉公式(Euler's formula)**:
$$e^{ix} = \cos{x} + i\sin{x}$$
即$e^{ix}$是**模(modulus)** 为**1**，**辐角(argument, $\arg(\cdot)$)** 为**x** 的**复数(complex number)**，是**复平面(complex plane)** 内以**原点(origin)** 为**圆心(center)** 的**单位圆(unit circle)** 上的一个**点(point)**
	证明(proof):
$$e^{ix} = 1 + ix + \frac{(ix)^{2}}{2!} + \frac{(ix)^{3}}{3!} + \dots + \frac{(ix)^{2n}}{(2n)!} + \frac{(ix)^{2n + 1}}{(2n + 1)!} = 1 + ix - \frac{x^{2}}{2!} - \frac{ix^{3}}{3!} + \dots + \frac{(-1)^{n}x^{2n}}{(2n)!} + \frac{i(-1)^{n}x^{2n + 1}}{(2n + 1)!} = [1 - \frac{x^{2}}{2} + \dots + \frac{(-1)^{n}x^{2n}}{(2n)!}] + [ix - \frac{ix^{3}}{3!} + \frac{i(-1)^{n}x^{2n + 1}}{(2n + 1)!}] = [1 + ix + \dots + \frac{(-1)^{n}x^{2n}}{(2n)!}] + i[x - \frac{x^{3}}{3!} + \dots + \frac{(-1)^{n}x^{2n + 1}}{(2n + 1)!}] = \cos{x} + i\sin{x}$$

**n阶单位根(n-th root of unity)**: **一元n次方程(equation)$x^{n} = 1$** 在**复数域(complex field)** 内的**解(solution)**，共**n**个
$$x^{n} = 1 = e^{2k\pi i}, k \in Z \Rightarrow x = e^{\frac{2k\pi i}{n}}, k = 0, 1, 2, \dots, n - 1$$