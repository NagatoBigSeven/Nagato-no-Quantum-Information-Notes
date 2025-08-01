**量子错误(quantum error)**:
	**比特翻转错误(bit-flip error)**/**X错误(X gate)**: $|0\rangle$变$|1\rangle$，$|1\rangle$变$|0\rangle$，相当于多应用了一次**X门(X gate)**
$$\begin{cases}X|0\rangle = |1\rangle \\ X|1\rangle = |0\rangle\end{cases} \Rightarrow X|\psi\rangle = X(\alpha|0\rangle + \beta|1\rangle) = \alpha X|0\rangle + \beta X|1\rangle = \alpha|1\rangle + \beta|0\rangle = \beta|0\rangle + \alpha|1\rangle$$
	**相位翻转错误(phase-flip error)**: $|0\rangle$不变，$|1\rangle$变$-|1\rangle$，相当于多应用了一次**Z门(Z gate)**
$$\begin{cases}Z|0\rangle = |0\rangle \\ Z|1\rangle = -|1\rangle\end{cases} \Rightarrow Z|\psi\rangle = Z(\alpha|0\rangle + \beta|1\rangle) = \alpha Z|0\rangle + \beta Z|1\rangle = \alpha|0\rangle - \beta|1\rangle$$
**3折量子重复码(3-fold quantum repetition code)**:
	**编码(encoding)**:
$$\begin{cases}|0\rangle_{L} = |000\rangle \\ |1\rangle_{L} = |111\rangle\end{cases} \Rightarrow |\psi\rangle_{L} = \alpha|0\rangle_{L} + \beta|1\rangle_{L} = \alpha|\stackrel{d_{1}d_{2}d_{3}}{000}\rangle + \beta|\stackrel{d_{1}d_{2}d_{3}}{111}\rangle = |\psi\rangle$$
![[3折量子重复码(3-fold Quantum Repetition Code)1.png]]
$$|\psi\rangle = \alpha|0\rangle + \beta|1\rangle$$
$$t_{0} = |\psi\rangle|0\rangle|0\rangle = (\alpha|0\rangle + \beta|1\rangle)|0\rangle|0\rangle = \alpha|000\rangle + \beta|100\rangle$$
$$t_{1} = CNOT_{1, 2}(\alpha|000\rangle + \beta|100\rangle) = \alpha|000\rangle + \beta|110\rangle$$
$$t_{2} = CNOT_{1, 3}(\alpha|000\rangle + \beta|110\rangle) = \alpha|000\rangle + \beta|111\rangle$$
$$\begin{cases}p_{1} = d_{1} \oplus d_{2} \\ p_{2} = d_{2} \oplus d_{3}\end{cases}$$

| X错误(X error)                                        | 码字(codeword)                                   | 校验子(syndrome)$p_{1}p_{2}$ |
| --------------------------------------------------- | ---------------------------------------------- | ------------------------- |
| **无(nil)**: $I \otimes I \otimes I$                 | $\alpha$\|000$\rangle$ + $\beta$\|111$\rangle$ | **00**                    |
| **翻转(flip)第一个量子比特(qubit)**: $X \otimes I \otimes I$ | $\alpha$\|100$\rangle$ + $\beta$\|011$\rangle$ | **10**                    |
| **翻转(flip)第二个量子比特(qubit)**: $I \otimes X \otimes I$ | $\alpha$\|010$\rangle$ + $\beta$\|101$\rangle$ | **11**                    |
| **翻转(flip)第三个量子比特(qubit)**: $I \otimes I \otimes X$ | $\alpha$\|001$\rangle$ + $\beta$\|110$\rangle$ | **01**                    |
![[量子重复码(Quantum Repetition Code.png]]
	**格林博格-霍恩-蔡林格态(Greenberger-Horne-Zeilinger state, $|\text{GHZ}\rangle$)**(abbr. **GHZ态(GHZ state, $|\text{GHZ}\rangle$)**
$$|\text{GHZ}\rangle = \frac{|000\rangle + |111\rangle}{\sqrt{2}}$$
**9位秀尔码(9-bit Shor code)**:
	**编码(encoding)**: 首先用**3折量子重复码(3-fold quantum repetition code)编码(encode)**一次，然后经过一个 **$H^{\otimes 3}$门($H^{\otimes 3}$ gate)**，最后再用**3折量子重复码(3-fold quantum repetition code)编码(encode)** 一次
$$\begin{cases}|0\rangle_{L} = \frac{(|000\rangle + |111\rangle)^{\otimes 3}}{2\sqrt{2}}(\text{i.e.} |0\rangle \rightarrow |000\rangle \rightarrow |+++\rangle \rightarrow \frac{(|0\rangle + |1\rangle)^{\otimes 3}}{2\sqrt{2}} \rightarrow \frac{(|000\rangle + |111\rangle)^{\otimes 3}}{2\sqrt{2}}) \\ |1\rangle_{L} = \frac{(|000\rangle + |111\rangle)^{\otimes 3}}{2\sqrt{2}}(\text{i.e.}|1\rangle \rightarrow |111\rangle \rightarrow |---\rangle \rightarrow \frac{(|0\rangle - |1\rangle)^{\otimes 3}}{2\sqrt{2}} \rightarrow \frac{(|000\rangle - |111\rangle)^{\otimes 3}}{2\sqrt{2}})\end{cases} \Rightarrow |\psi\rangle_{L} = \alpha|0\rangle_{L} + \beta|1\rangle_{L} = \frac{\alpha(|000\rangle + |111\rangle)^{\otimes 3} + \beta(|000\rangle - |111\rangle)^{\otimes 3}}{2\sqrt{2}} = |\psi\rangle$$
![[秀尔码(Shor Code).png]]
**阈值定理(threshold theorem)**: 若量子计算机的物理错误率低于一个特定的阈值，则可以通过量子纠错(quantum error correction, QEC)将逻辑错误率抑制到任意低的水平