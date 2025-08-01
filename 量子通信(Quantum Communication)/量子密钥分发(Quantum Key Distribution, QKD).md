**经典通信(classical communication)**: **密文(ciphertext)** 是一串**经典比特(classical bit)**，**窃听者(eavesdropper)夏娃(Eve)** 可以在不被**发送者(sender)爱丽丝(Alice)** 和**接收者(receiver)鲍勃(Bob)** 发现的前提下观看并重发**密文(ciphertext)**
	**一次性密码本协议(one-time pad protocol, OTP protocol)**:
		**加密(encryption)**:
$$E = T \oplus K$$
		**解密(decryption)**:
$$T = E \oplus K$$
			证明(proof):
$$E \oplus K = (T \oplus K) \oplus K = T \oplus (K \oplus K) = T \oplus 0 = T$$
		(其中**T** 为**明文(plaintext)**，**E** 为**密文(ciphertext)**，**K** 为**密钥(key)**，三者均为**长度(length)** 为**n**的**01串(01 string)**)

**量子不可克隆定理(quantum no-cloning theorem)**: **不可能精确复制任何未知的量子态(quantum state)**
	证明(proof): 反证法(proof by contradiction)
		假设**量子不可克隆定理(quamtum no-cloning theorem)** 不成立，即**可以精确复制任何未知的量子态(quantum state)**，即存在**量子门(quantum state)U**，使得$U|\psi\rangle = |\psi\rangle|\psi\rangle$
		设$|\psi\rangle = \alpha|0\rangle + \beta|1\rangle$
$$U|\psi\rangle = U(\alpha|0\rangle + \beta|1\rangle) = \alpha U|0\rangle + \beta U|1\rangle = \alpha|00\rangle + \beta|11\rangle = \alpha^{2}|00\rangle + \alpha\beta|01\rangle + \alpha\beta|10\rangle + \beta^{2}|11\rangle = (\alpha|0\rangle + \beta|1\rangle)(\alpha|0\rangle + \beta|1\rangle) = |\psi\rangle|\psi\rangle \Rightarrow \begin{cases}\alpha^{2} = \alpha \\ \alpha\beta = 0 \\ \beta^{2} = \beta\end{cases} \Rightarrow \alpha = \beta = 0$$
		而$\alpha$和$\beta$不能同时为0，矛盾

**量子通信(quantum communication)**: **密文(ciphertext)** 是一串**量子比特(qubit)**，根据**量子不可克隆定理(quantum no-cloning theorem)**，**窃听者(eavesdropper)夏娃(Eve)** 不可能在不被**发送者(sender)爱丽丝(Alice)** 和**接收者(receiver)鲍勃(Bob)** 发现的前提下观看并重发**密文(ciphertext)**
	**BB84协议(BB84 protocol)**:
		**基(basis)**:
			$+$**基($+$ basis)**: $+ = \{|\rightarrow\rangle = |0\rangle = \begin{bmatrix}1 \\ 0\end{bmatrix}, |\uparrow\rangle = |1\rangle = \begin{bmatrix}0 \\ 1\end{bmatrix}\}$
			$\times$**基($\times$ basis)**: $\times = \{|\nwarrow\rangle = -|-\rangle = \frac{1}{\sqrt{2}}\begin{bmatrix}-1 \\ 1\end{bmatrix}, |\nearrow\rangle = |+\rangle = \frac{1}{\sqrt{2}}\begin{bmatrix}1 \\ 1\end{bmatrix}\}$
$$\begin{cases}|\rightarrow\rangle = |0\rangle = \frac{|+\rangle + |-\rangle}{\sqrt{2}} = \frac{|\nearrow\rangle - |\nwarrow\rangle}{\sqrt{2}} \\ |\uparrow\rangle = |1\rangle = \frac{|+\rangle - |-\rangle}{\sqrt{2}} = \frac{|\nearrow\rangle + |\nwarrow\rangle}{\sqrt{2}}\end{cases}$$
$$\begin{cases}|\nwarrow\rangle = -|-\rangle = \frac{|1\rangle - |0\rangle}{\sqrt{2}} = \frac{|\uparrow\rangle - |\rightarrow\rangle}{\sqrt{2}} \\ |\nearrow\rangle = |+\rangle = \frac{|0\rangle + |1\rangle}{\sqrt{2}} = \frac{|\rightarrow\rangle + |\uparrow\rangle}{\sqrt{2}}\end{cases}$$
		**加密(encryption)**: **发送者(sender)爱丽丝(Alice)** 对于**明文(plaintext)** 的每个**量子比特(qubit)** 均随机选择一组**基(basis)** 进行**加密(encryption)**，然后将**密文(ciphertext)** 通过**公共频道(public channel)** 发送给**接收者(receiver)鲍勃(Bob)**。

| 明文(plaintext) | 密文                     | (ciphertext)              |
| ------------- | ---------------------- | ------------------------- |
|               | $+$基($+$ basis)        | $\times$基($\times$ basis) |
| \|$0\rangle$  | \|$\rightarrow\rangle$ | \|$\nearrow\rangle$       |
| \|$1\rangle$  | \|$\uparrow\rangle$    | \|$\nwarrow\rangle$       |
		**解密(decryption)**: **接受者(receiver)鲍勃(Bob)** 对于**密文(cipher text)** 的每个**量子比特(qubit)** 均随机选择一组**基(basis)** 进行**解密(decryption)**。**发送者(sender)爱丽丝(Alice)** 与**接收者(receiver)鲍勃(Bob)** 通过**公共信道(public channel)** 逐个**量子比特(qubit)** 比较**加密(encrypt)** 和**解密(decrypt)** 每个**量子比特(qubit)** 时选择的**基(basis)**，若**基(basis)** 相同，则理论上**量子比特(qubit)加密(encryption)前** 的**量子态(quantum state)** 与**解密(decryption)后** 的**量子态(quantum state)** 一定相同； 若**基(basis)** 不同，则理论上**量子比特(qubit)加密(encryption)前** 的**量子态(quantum state)** 与**解密(decryption)后** 的**量子态(quantum state)** 一定不同。**发送者(sender)爱丽丝(Alice)** 和**接收者(receiver)鲍勃(Bob)** 各自保留**基(basis)** 相同的那部分**量子比特(qubit)**，从中随机选择一半数量的**量子比特(qubit)** 通过**公共信道(public channel)** 比较其**加密(encryption)前** 和**解密(decryption)后** 的**量子态(quantum state)** 是否相同，若不相同的百分比不超过阈值，则说明只有**噪声(noise)**，没有**窃听者(eavesdropper)夏娃(Eve)** 的存在，可以重复上述步骤继续**通信(communication)**；若不相同的百分比超过阈值，则说明除**噪声(noise)** 外还有**窃听者(eavesdropper)夏娃(Eve)** 的存在，应当立即停止**通信(communication)**