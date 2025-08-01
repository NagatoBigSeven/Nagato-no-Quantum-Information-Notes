n位b进制整数转十进制整数:
$$(a_{n - 1}a_{n - 2}...a_{1}a_{0})_{b} = a_{n - 1}b^{n - 1} + a_{n - 2}b^{n - 2} + ... + a_{1}b + a_{0} = \sum_{k = 0}^{n - 1}a_{k}b^{k}$$
(其中n, b $\in$ Z, n $\geq$ 1, b $\geq$ 2, $a_{n - 1}$, $a_{n - 2}$, ..., $a_{1}$, $a_{0}$ $\in$ {0, 1, ..., b - 1})
需要执行n - 1次加法运算和$\frac{n}{2} \cdot (n - 1)$次乘法运算
注: n位b进制整数转十进制整数本质上是求一元n - 1次多项式在b处的值
优化: 霍纳法(Horner's method)/秦九韶算法:
$$(a_{n - 1}a_{n - 2}...a_{1}a_{0})_{b} = a_{n - 1}b^{n - 1} + a_{n - 2}b^{n - 2} + ... + a_{1}b + a_{0} = b(a_{n - 1}b^{n - 2} + a_{n - 2}b^{n - 3} + ... + a_{2}b + a_{1}) + a_{0} = b(b(a_{n - 1}b^{n - 3} + a_{n - 2}b^{n - 4} + ... + a_{3}b + a_{2}) + a_{1}) + a_{0} = ... = b(b(b(b(ba_{n - 1} + a_{n - 2})+ ...) + a_{3}) + a_{2}) + a_{1}) + a_{0}$$
$f_{1} = ba_{n - 1} + a_{n - 2}$
$f_{2} = bf_{1} + a_{n - 3}$
$f_{3} = bf_{2} + a_{n - 4}$
...
$f_{n - 1} = bf_{n - 2} + a_{0}$
只需要执行n - 1次加法运算和n - 1次乘法运算

十进制整数转b进制整数: 逆用霍纳法(Horner's method)，即除以b，余数倒序写

b进制小数转十进制小数:
$$(0.a_{-1}a_{-2}...)_{b} = a_{-1}b^{-1} + a_{-2}b^{-2} + ...$$

十进制小数转b进制小数: 乘以b，整数顺序写
注: 十进制小数的b进制小数表示可能不唯一

逻辑门(logic gate): 最简单的数字电路(digital circuit)

| 逻辑门(logic gate)                         | 逻辑函数(logic function)                                                | 真值表(truth table) |      |
| --------------------------------------- | ------------------------------------------------------------------- | ---------------- | ---- |
| 与门(AND gate)/合取(conjunction)            | AND(A, B) = A $\land$ B                                             | 全真为真，一假为假        |      |
| 或门(OR gate)/析取(disjunction)             | OR(A, B) = A $\lor$ B                                               | 一真为真，全假为假        |      |
| 非门(NOT gate)/否定(negation)/反相器(inverter) | NOT(A) = $\lnot$A                                                   | 真变假，假变真          |      |
| 与非门(NAND gate)                          | NAND(A, B) = NOT(AND(A, B)) = $\lnot$(A $\land$ B)                  | 一假为真，全真为假        |      |
| 或非门(NOR gate)                           | NOR(A, B) = NOT(OR(A, B)) = $\lnot$(A $\lor$ B)                     | 全假为真，一真为假        |      |
| 异或门(XOR gate)/不等(not equal)             | XOR(A, B) = A $\oplus$ B $\equiv$ A != B                            | 不同为真，相同为假        | 模2加法 |
| 同或门/异或非门(XNOR gate)/相等(equal)           | XNOR(A, B) = NOT(XOR(A, B)) = $\lnot$(A $\oplus$ B) $\equiv$ A == B | 相同为真，不同为假        |      |

逻辑电路(logic circuit):
扇出(fanout):
$$FANOUT(x) = (x, x)$$
半加器(half adder):
$$HALFADDER(A, B) = (C, S) = (A \land B, A \oplus B)$$
全加器(full adder):
$$FULLADDER(A, B, C_{in}) = (C_{out}, S) = ((A \land B) \lor ((A \oplus B) \land C_{in}), A \oplus B \oplus C_{in})$$

通用逻辑门(universal logic gate): {与门(AND gate), 或门(OR gate), 非门(NOT gate)}、{与非门(NAND gate)}和{或非门(NOR gate)}
Q: 如何证明与非门(NAND gate)是通用逻辑门(universal logic gate)
A:
用与非门(NAND gate)表示非门(NOT gate):
$$NOT(A) = \lnot A = \lnot(A \land A) = NAND(A, A)$$
用与非门(NAND gate)表示与门(AND gate):
$$AND(A, B) = NOT(NAND(A, B)) = NAND(NAND(A, B), NAND(A, B))$$
用与非门(NAND gate)表示或门(OR gate):
$$OR(A, B) = NOT(NOT(OR(A, B))) = NOT(AND(NOT(A), NOT(B))) = NAND(NOT(A), NOT(B)) = NAND(NAND(A, A), NAND(B, B))$$

信息论(information theory): 1个比特(bit, b)最多包含1个比特(bit, b)的信息(information)，最少包含0个比特(bit, b)的信息(bit, b)，若1个比特(bit, b)取0的概率(probability, prob.)为P(0) = p，取1的概率(probability, prob.)为P(1) = 1 - p，则其包含$H_{b}(p) = -plogp-(1 - p)log(1 - p) = -[plogp + (1 - p)log(1 - p)]$个比特(bit, b)的信息(information)
	P(0) = 50%, P(1) = 50% -> 包含1个比特(bit, b)的信息(information)
	P(0) = 100%, P(1) = 0 -> 包含0个比特(bit, b)的信息(information)
	P(0) = 0, P(1) = 100% -> 包含0个比特(bit, b)的信息(information)

兰道尔原理(Landauer's principle): 擦除1个比特(bit, b)的信息(information)至少需要耗散$k_{B}T\ln{2}$的能量(energy)(其中$k_{B}$为波尔兹曼常数(Boltzmann constant)，T为温度(temperature)(单位(unit): 开(尔文)(Kelvin, K)))

可逆门(reversible gate): 双射(bijection/one-to-one and onto) = 单射(injection/one-to-one) + 满射(surjection/onto))
非门(NOT gate)是可逆门(reversible gate)，与门(AND gate)、或门(OR gate)、与非门(NAND gate)、或非门(NOR gate)、异或门(XOR gate)、同或门/异或非门(XNOR gate)均为不可逆门(irreversible gate)
可逆门(reversible gate)不会丢失信息(information)。以非门(NOT gate)为例，输出(output)0唯一对应于输入(input)1，输出(output)1唯一对应于输入(input)0，说明信息(information)在经过非门(NOT gate)变换后没有出现丢失；不可逆门(irreversible gate)会丢失信息(information)，以与非门(NAND gate)为例，输出(output)0唯一对应于输入(input)11，输出(output)1同时对应于输入(input)00、输入(input)01和输入(input)10，说明信息(information)在经过与非门(NAND gate)变换后出现了丢失
可逆门(reversible gate)的输入(input)既可以均为经典比特(classical bit)，也可以均为量子比特(qubit)；不可逆门(irreversible)的输入(input)的输入(input)只能均为经典比特(classical bit)，不能均为量子比特(qubit)。当可逆门(reversible gate)的输入(input)均为量子比特(qubit)时，可逆门(reversible)就是量子门(quantum gate)

非门(NOT gate)是可逆门(reversible gate)
真值表(truth table)

| A   | O   |
| --- | --- |
| 0   | 1   |
| 1   | 0   |
1输入(input)，1输出(input)，1个比特(bit, b)信息(information) -> 1个比特(bit, b)信息(information)
异或门(XOR gate)是不可逆门(irreversible gate)
真值表(truth table):

| A   | B   | O   |
| --- | --- | --- |
| 0   | 0   | 0   |
| 0   | 1   | 1   |
| 1   | 0   | 1   |
| 1   | 1   | 0   |
2输入(input)，1输出(output)，必丢失信息(information)
Q: 如何构建可逆异或门(reversible XOR gate, RXOR gate)?
A: 控制非门(controlled-NOT gate, CNOT gate)!
控制非门(controlled-NOT gate, CNOT gate): 第一个比特(bit)是控制比特(control bit)，第二个比特(control)是目标比特(target bit)。当控制比特(control bit)为1时，将目标比特(target bit)取反，否则保持目标比特(target bit)不变
真值表(truth table):

| Control | Target | Control' = Control | Target = Control $\oplus$ Target |
| ------- | ------ | ------------------ | -------------------------------- |
| 0       | 0      | 0                  | 0                                |
| 0       | 1      | 0                  | 1                                |
| 1       | 0      | 1                  | 1                                |
| 1       | 1      | 1                  | 0                                |
$$CNOT(Control, Target) = (Control, Control \oplus Target)$$
2输入(input)，2输出(output)，2个比特(bit, b)的信息(information) -> 2个比特(bit, b)的信息(information)
与门(AND gate)是不可逆门(irreversible gate)
真值表(truth table):

| A   | B   | O   |
| --- | --- | --- |
| 0   | 0   | 0   |
| 0   | 1   | 0   |
| 1   | 0   | 0   |
| 1   | 1   | 1   |
2输入(input)，1输出(output)，必丢失信息(information)
与非门(NAND gate)是不可逆门(irreversible gate)
真值表(truth table):

| A   | B   | O   |
| --- | --- | --- |
| 0   | 0   | 1   |
| 0   | 1   | 1   |
| 1   | 0   | 1   |
| 1   | 1   | 0   |
2输入(input)，1输出(output)，必丢失信息(information)
Q: 如何构建可逆与门(reversible AND gate)和可逆与非门(reversible NAND gate)?
A: 托佛利门(Toffoli gate, TOF gate)/控-控非门(controlled-controlled-NOT gate, CCNOT gate)!
托佛利门(Toffoli gate, TOF gate)控-控非门(controlled-controlled-NOT gate): 第一个和第二个比特(bit)是控制比特(control bit)，第三个比特(bit)是目标比特(target bit)。当两个控制比特(control bit)均为1时，将目标比特(target bit)取反，否则保持目标比特(target bit)不变
真值表(truth table):

| A   | B   | C   | A' = A | B' = B | C' = C $\oplus$ A $\land$ B |
| --- | --- | --- | ------ | ------ | --------------------------- |
| 0   | 0   | 0   | 0      | 0      | 0                           |
| 0   | 0   | 1   | 0      | 0      | 1                           |
| 0   | 1   | 0   | 0      | 1      | 0                           |
| 0   | 1   | 1   | 0      | 1      | 1                           |
| 1   | 0   | 0   | 1      | 0      | 0                           |
| 1   | 0   | 1   | 1      | 0      | 1                           |
| 1   | 1   | 0   | 1      | 1      | 1                           |
| 1   | 1   | 1   | 1      | 1      | 0                           |
$$TOF(A, B, C) = \begin{cases}\text{(A, B, C), if A = 0 or B = 0} \\ (A, B, \lnot C)\text{, if A = 1 and B = 1}\end{cases} = C \oplus AB$$
$$TOF(A, B, 0) = (A, B, XOR(0, AND(A, B))) = (A, B, AND(A, B))$$
$$TOF(A, B, 1) = (A, B, XOR(1, AND(A, B))) = (A, B, NAND(A, B))$$
3输入(input)，3输出(output)，3比特(bit, b)信息(information) -> 3比特(bit, b)信息(information)
可逆逻辑电路(reversible logic circuit): 完全由可逆门(reversible gate)组成的逻辑电路(logic circuit) v.s. 不可逆逻辑电路(irreversible logic circuit):
半加器(half-adder)由一个与门(AND gate)和一个异或门(XOR gate)组成，因为与门(AND gate)和异或门(XOR gate)均为不可逆门(irreversible gate)，所以半加器(half-adder)是不可逆逻辑电路(irreversible logic circuit)
Q: 如何构建可逆半加器(reversible half-adder)?
A: 用可逆与门(reversible AND gate)代替与门(AND gate)，用可逆异或门(reversible XOR gate, RXOR gate)/控制非门(controlled-NOT gate, CNOT gate)代替异或门(XOR gate)!