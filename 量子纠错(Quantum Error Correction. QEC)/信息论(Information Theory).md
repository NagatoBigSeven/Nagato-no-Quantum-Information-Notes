**香农熵(Shannon entropy, H)**(a.k.a.**信源熵(source entropy)**)(**单位(unit): 比特(bit, b)**): **信息(information)不确定性(uncertainty)的量度(measurement)**
$$H(X) = -p_{X}(x_{1})\log_{2}{p_{X}(x_{1})} - p_{X}(x_{2})\log_{2}{p_{X}(x_{2})} - \dots - p_{X}(x_{n})\log_{2}{p_{X}(x_{n})} = -\sum_{i = 1}^{n}p_{X}(x_{i})\log_{2}{p_{X}(x_{i})}$$
(其中**X**称为**信源(source)**，是一个**离散随机变量(discrete random variable)**(i.e. **字符型变量(char variable)**)；$x_{1}$, $x_{2}$, $\dots$, $x_{n}$为其所有可能的取值(i.e. **字符(character)**)；$p_{X}(\cdot)$为其**概率质量函数(probability mass function, pmf)**)
**编码(coding)**: **字符(character)** $\rightarrow$ **01串(bit string)**
	**唯一可解码编码(uniquely decodable coding)**:
		**前缀无关编码(prefix-free coding)**(abbr. **前缀编码(prefix coding)**): **任何码字(codeword)都不是其他码字(codeword)的前缀(prefix)** v.s. $\dots$
		**等长编码/固定长度编码(fixed-length coding)** v.s. **变长编码/可变长度编码(variable-length coding)**
	$\dots$
**平均码(字)长(度)(average codeword length, L)**:
$$L = \sum_{i = 1}^{n}p_{i}l_{i}$$
**香农第一定理(Shannon's first theorem)**——**无噪信道信源编码定理**(简称**无噪编码定理(noiseless coding theorem)** 或**信源编码定理(source coding theorem)**): **无噪信道(noiseless channel)中，信源字母表(source alphabet)的唯一可解码编码(uniquely decodable coding)的平均码(字)长(度)(average codeword length, L)的理论下限是信源(source)的香农熵(Shannon entropy, H)**
$$\forall{L}, L \geq H(X), \text{且}\exists{L_{0}}, \text{ s.t. }H(X) \leq L_{0} < H(X) + 1$$
**哈夫曼编码(Huffman coding)**: **最优的变长前缀编码(optimal variable-length prefix coding)**
	**哈夫曼树(Huffman tree)**
**信道(channel)**:
	**无噪信道(noiseless channel)**
	**有噪信道(noisy channel)**:
		**离散无记忆信道(discrete memoryless channel, DMC)**:
			**二进制信道(binary channel, BC)**:
				**二进制对称信道(binary symmetric channel, BSC)**:
					**误码率(error rate)**: **p**
					**条件概率(conditional probability)**:
$$\begin{cases}P(Y = 0 \mid X = 0) = P(Y = 1 \mid X = 1) = 1 - p \\ P(Y = 1 \mid X = 0) = P(Y = 0 \mid X = 1) = p\end{cases}$$
					**转移概率矩阵(transition probability matrix, $P(y \mid x)$)**(abbr. **转移矩阵(transition probability)**/**概率矩阵(probability matrix)**): $2 \times 2$**矩阵(matrix)**
$$P(y \mid x) = \begin{bmatrix}P(0 \mid 0) & P(0 \mid 1) \\ P(1 \mid 0) & P(1 \mid 1)\end{bmatrix} = \begin{bmatrix}1 - p & p \\ p & 1 - p\end{bmatrix}$$
![[二进制对称信道(Binary Symmetric Channel, BSC).jpg]]
				**Z信道(Z-channel)**:
					**条件概率(conditional probability)**:
$$\begin{cases}P(0 \mid 0) = 1 \\ P(1 \mid 0) = 0 \\ P(1 \mid 1) = 1 - p \\ P(0 \mid 1) = p\end{cases}$$
						**转移概率矩阵(transition probability matrix, $P(y \mid x)$)**: $2 \times 2$**矩阵(matrix)**
$$P(y \mid x) = \begin{bmatrix}P(Y = 0 \mid X = 0) & P(Y = 0 \mid X = 1) \\ P(Y = 1 \mid X = 0) & P(Y = 1 \mid X = 1)\end{bmatrix} = \begin{bmatrix}1 & p \\ 0 & 1 - p\end{bmatrix}$$
![[Z信道(Z-channel).jpg]]
			**二进制擦除信道(binary erasure channel, BEC)**:
				**条件概率(conditional probability)**:
$$\begin{cases}P(Y = 0 \mid X = 0) = P(Y = 1 \mid X = 1) = 1 - p \\ P(Y = 1 \mid X = 0) = P(Y = 0 \mid X = 1) = 0 \\ P(Y = \perp \mid X = 0) = P(Y = \perp \mid X = 1) = p\end{cases}$$
				**转移概率矩阵(transition probability matrix, $P(y \mid x)$)**: $3 \times 2$**矩阵(matrix)**
$$P(y \mid x) = \begin{bmatrix}P(Y = 0 \mid X = 0) & P(Y = 0 \mid X = 1) \\ P(Y = 1 \mid X = 0) & P(Y = 1 \mid X = 1) \\ P(Y = \perp \mid X = 0) & P(Y = \perp \mid X = 1)\end{bmatrix} = \begin{bmatrix}1 - p & 0 \\ 0 & 1 - p \\ p & p\end{bmatrix}$$

![[二进制擦除信道(Binary Erasure Channel, BEC).jpg]]
		$\dots$
**检错纠错码(error detection and correction code)**:
	**n折重复码(n-fold repetition code)**:
		**3折重复码(3-fold repetition code)**(n.b. **n** 为**奇数(odd number)**):
			**编码(coding)**: 将**每个数据位(data bit)重复(repeat)3次**
$$d_{1}d_{2}d_{3}d_{4} \rightarrow d_{1}d_{1}d_{1} \ d_{2}d_{2}d_{2} \ d_{3}d_{3}d_{3} \ d_{4}d_{4}d_{4}$$
			**解码(decoding)**: **少数服从多数多数(majority rule)**
				**3**个**0**，**0**个**1**: **000** $\rightarrow$ **0**
				**2**个**0**，**1**个**1**: **001**/**010**/**100** $\rightarrow$ **0**
				**1**个**0**，**2**个**1**: **011**/**101**/**110** $\rightarrow$ **1**
				**0**个**0**，**3**个**1**: **111** $\rightarrow$ **1**
			**二进制对称信道(binary symmetric channel, BSC)** 应用**3折重复码(3-fold repetition code)纠错(error correction)** 后的**误码率(error ratio)**:
$$P(\text{bit correct}) = (1 - p)^{3} + {{3} \choose {1}}p(1 - p)^{2}$$
$$P(\text{block correct}) = P^{4}(\text{bit correct}) = [(1 - p)^{3} + {{3} \choose {1}}p(1 - p)^{2}]^{4}$$
$$P(\text{block error}) = 1 - P(\text{block correct}) = 1 - [(1 - p)^{3} + {{3} \choose {1}}p(1 - p)^{2}]^{4}$$
			**码率(code rate, R)**:
$$R = \frac{k}{n} = \frac{1}{3}$$
		注: **n折重复码(n-fold correction code)最多纠正(correct)**$\lfloor\frac{n - 1}{2}\rfloor$**位(bit, b)错误(error)**
	**汉明码(~~Hon Ming~~Hamming code)**:
		**(7, 4)汉明码((7, 4) Hamming code)**:
			**编码(coding)**: **每4个数据位(data bit)** 计算**3个校验位(parity bit)**，**共7位(bit, b)码字(codeword)**
$$d_{1}d_{2}d_{3}d_{4} \rightarrow p_{1}p_{2}d_{1}p_{3}d_{2}d_{3}d_{4}$$(其中$\begin{cases}p_{1} = d_{1} \oplus d_{2} \oplus d_{4} \\ p_{2} = d_{1} \oplus d_{3} \oplus d_{4} \\ p_{3} = d_{2} \oplus d_{3} \oplus d_{4}\end{cases}$)
			**解码(decoding)**: **每7位(bit, b)码字(codeword)** 计算**3位综合征(syndrome)**
$$\begin{cases}s_{1} = p_{1}^{'} \oplus d_{1}^{'} \oplus d_{2}^{'} \oplus d_{4}^{'} \\ s_{2} = p_{2}^{'} \oplus d_{1}^{'} \oplus d_{3}^{'} \oplus d_{4}^{'} \\ s_{3} = p_{3}^{'} \oplus d_{2}^{'} \oplus d_{3}^{'} \oplus d_{4}^{'}\end{cases}$$

| 校验子(syndrome)$s_{3}s_{2}s_{1}$ | 错误位(error bit) |
| ------------------------------ | -------------- |
| **000**                        | **nil**        |
| **001**                        | $p_{1}$        |
| **010**                        | $p_{2}$        |
| **100**                        | $p_{3}$        |
| **011**                        | $d_{1}$        |
| **101**                        | $d_{2}$        |
| **110**                        | $d_{3}$        |
| **111**                        | $d_{4}$        |
			**二进制对称信道(binary symmetric channel, BSC)** 应用 **(7, 4)汉明码(Hamming code)** 后的**误码率(error ratio)**:
$$P(\text{block correct}) = (1 - p)^{7} + {{7} \choose {1}}p(1 - p)^{6}$$
$$P(\text{block error}) = 1 - P(\text{block correct}) = 1 - [(1 - p)^{7} + {{7} \choose {1}}p(1 - p)^{6}]$$
			**码率(code rate, R)**:
$$R = \frac{k}{n} = \frac{4}{7}$$
 **信道容量(channel capacity, C)**(**单位(unit): 比特/次信道使用(bit per channel use, b/channel use)**): **有噪信道(noisy channel)单位时间内可可靠传输的最大信息量**
	 **离散无记忆信道(discrete memoryless channel, DMC)**:
$$C = \max_{p_{X}}I(X;Y) = \max_{p_{X}}[H(X) + H(Y) - H(X;Y)]$$
	(其中**X**为**信源(source)**，**Y**为**信宿(sink)**，$p_{X}$为**信源(source)X** 的**概率质量函数(probability mass function, pmf)**；**I(X;Y)** 为**信源(source)X** 与**信宿(sink)Y** 之间的**互信息(mutual information, MI)**)
		**二进制对称信道(binary symmetric channel, BSC)**:
$$C = 1 - H(p)$$
		(其中$H(p) = -p\log_{2}{p} - (1 - p)\log_{2}(1 - p)$为**二元熵函数(binary entropy function)**)
**香农第二定理(Shannon's second theorem)**——**有噪信道编码定理(noisy channel coding theorem)**: **有噪信道(noisy channel)中，信息的可靠传输速率(rate, R)的理论上限是信道容量(channel capacity, C)**
$$\text{若}R \leq C, \text{则存在一组编码方案(coding scheme)使得}\lim_{n \to \infty}P_{e}^{(n)} = 0$$
