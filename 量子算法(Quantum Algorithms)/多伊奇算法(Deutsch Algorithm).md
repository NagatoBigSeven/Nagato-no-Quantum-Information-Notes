**多伊奇问题(Deutsch problem)**: 给定一个要么是常函数(constant function)(i.e. 输出(output)均为0或均为1)要么是平衡函数(balanced function)(i.e. 输出(output)一半为0一半为1)的布尔函数(boolean function)$f: \{0, 1\} -> \{0, 1\}$，判断它是常函数(constant function)还是平衡函数(balanced function)
例:
	f(0) = 0, f(1) = 0 $\Rightarrow$ f(x)是常函数(constant function)
	f(0) = 1, f(1) = 1 $\Rightarrow$ f(x)是常函数(constant function)
	f(0) = 0, f(1) = 1 $\Rightarrow$ f(x)是平衡函数(balanced function)
	f(0) = 1, f(1) = 0 $\Rightarrow$ f(x)是平衡函数(balanced function)
经典算法(classical algorithm): 分别计算f(0)和f(1)，需要进行2次运算
**多伊奇(D)算法(D(eutsch) algorithm)**: 只需要进行1次运算
![[多伊奇算法(Deutsch algorithm).png]]
假设有如上图所示的量子预言机(quantum oracle)$U_{f}$:
$$U_{f}|x, y\rangle = |x, y \oplus f(x)\rangle$$
(其中x, y $\in$ {0, 1})
$$\begin{cases}U_{f}|00\rangle = |0, 0 \oplus f(0)\rangle = |0, f(0)\rangle \\ U_{f}|01\rangle = |0, 1 \oplus f(0)\rangle = |0, \lnot f(0)\rangle \\ U_{f}|10\rangle = |1, 0 \oplus f(1)\rangle = |1, f(1)\rangle \\ U_{f}|11\rangle = |1, 1 \oplus f(1)\rangle = |1, \lnot f(1)\rangle\end{cases}$$
$$U_{f}(c_{00}|00\rangle + c_{01}|01\rangle + c_{10}|10\rangle + c_{11}|11\rangle) = c_{00}U_{f}|00\rangle + c_{01}U_{f}|01\rangle + c_{10}U_{f}|10\rangle + c_{11}U_{f}|11\rangle = c_{00}|0, f(0)\rangle + c_{01}|0, \lnot f(0)\rangle + c_{10}|1, f(1)\rangle + c_{11}|1, \lnot f(1)\rangle$$
$$|\psi_{0}\rangle = |01\rangle$$
$$|\psi_{1}\rangle = H|0\rangle H|1\rangle = \frac{|0\rangle + |1\rangle}{\sqrt{2}} \frac{|0\rangle - |1\rangle}{\sqrt{2}} = \frac{|00\rangle - |01\rangle + |10\rangle - |11\rangle}{2}$$
$$|\psi_{2}\rangle = U_{f}|\psi_{1}\rangle = U_{f}\frac{|00\rangle - |01\rangle + |10\rangle - |11\rangle}{2} = \frac{U_{f}|00\rangle - U_{f}|01\rangle + U_{f}|10\rangle - U_{f}|11\rangle}{2} = \frac{|0, f(0)\rangle - |0, \lnot f(0)\rangle + |1, f(1)\rangle - |1, \lnot f(1)\rangle}{2} = \frac{|0\rangle(|f(0)\rangle - |\lnot f(0)\rangle + |1\rangle(|f(1)\rangle - |\lnot f(1)\rangle)}{2} = \frac{1}{2}\sum_{x = 0}^{1}|x\rangle(|f(x)\rangle - |\lnot f(x)\rangle)$$
$$|f(x)\rangle - |\lnot f(x)\rangle = \begin{cases}(|0\rangle - |1\rangle) = (-1)^{0}(|0\rangle - |1\rangle)\text{, if f(x) = 0} \\ (|1\rangle - |0\rangle) = -(|0\rangle - |1\rangle) = (-1)^{1}(|0\rangle - |1\rangle)\text{, if f(x) = 1}\end{cases} = (-1)^{f(x)}(|0\rangle - |1\rangle)$$
$$|\psi_{2}\rangle = \frac{1}{2}\sum_{x = 0}^{1}(-1)^{f(x)}|x\rangle(|0\rangle - |1\rangle) = \frac{(-1)^{f(0)}|0\rangle(|0\rangle - |1\rangle) + (-1)^{f(1)}|1\rangle(|0\rangle - |1\rangle)}{2} = \frac{(-1)^{f(0)}|0\rangle + (-1)^{f(1)}|1\rangle}{\sqrt{2}}\frac{|0\rangle - |1\rangle}{\sqrt{2}} = (-1)^{f(0)}\frac{|0\rangle + (-1)^{f(1) - f(0)}|1\rangle}{\sqrt{2}}\frac{|0\rangle - |1\rangle}{\sqrt{2}} = \begin{cases}(-1)^{f(0)}\frac{|0\rangle + |1\rangle}{\sqrt{2}}\frac{|0\rangle - |1\rangle}{\sqrt{2}}\text{, if f(0) = f(1)} \\ (-1)^{f(0)}\frac{|0\rangle - |1\rangle}{\sqrt{2}}\frac{|0\rangle - |1\rangle}{\sqrt{2}}\text{, if f(0) }\neq\text{ f(1)}\end{cases}$$
$$|\psi_{3}\rangle = \begin{cases}(-1)^{f(0)}H(\frac{|0\rangle + |1\rangle}{\sqrt{2}})\frac{|0\rangle - |1\rangle}{\sqrt{2}} \\ (-1)^{f(0)}H(\frac{|0\rangle - |1\rangle}{\sqrt{2}})\frac{|0\rangle - |1\rangle}{\sqrt{2}}\end{cases} = \begin{cases}(-1)^{f(0)}|0\rangle\frac{|0\rangle - |1\rangle}{\sqrt{2}}\text{, if f(0) = f(1)} \\ (-1)^{f(0)}|1\rangle\frac{|0\rangle - |1\rangle}{\sqrt{2}}\text{, if f(0) }\neq\text{ f(1)}\end{cases}$$
$$|\psi_{3L}\rangle = \begin{cases}(-1)^{f(0)}|0\rangle\text{, if f(0) = f(1)} \\ (-1)^{f(0)}|1\rangle\text{, if f(0) }\neq\text{ f(1)}\end{cases} = (-1)^{f(0)}|f(0) \oplus f(1)\rangle$$
若测量(measurement)到$|\psi_{3L}\rangle$为$|0\rangle$，则f(x)为常函数(constant function)，若测量(measurement)到$|\psi_{3L}\rangle$为$|1\rangle$，则f(x)为平衡函数(balanced function)

(推广)多伊奇(D)-约萨(J)问题(D(eutsch)-J(osza) problem): 给定一个要么是常函数(constant function)要么是平衡函数(balanced function)的布尔函数(boolean)$f: \{0, 1\}^{n} -> \{0, 1\}$，判断它是常函数(constant function)还是平衡函数(balanced function)
经典算法(classical algorithm): 最好需要进行2次运算，最坏需要进行$2^{n - 1}$ + 1次运算
多伊奇(D)-约萨(J)算法(D(eutsch)-J(ozsa) algorithm): 只需要进行1次运算
![[多伊奇-约萨算法(Deutsch-Jozsa algorithm).png]]