# Group-ring Lattice
The Group-ring interpretetion can also be used to construct Lattice for NTRU-like cryptosystems.

### Lattice from Group-ring
Let $G = \lbrace a_1,a_2,\cdots a_n \rbrace$ be a group and $R$ be a ring. $R$ is preferably commutative with identity.<br>
The choice of such $R$ is so that few invertible elements may be present in $R$.<br>
Let $RG$ be the group ring. Let $f,g \in RG$ such that $f$ is invertible.<br>
Let $h = f^{-1} * g$ be the Public Key.<br>
Then, $g = f * h$. We can construct similar matrix equations as we did for NTRU.<br>
$f = f * 1 + u * 0$ and $g = f * h + u * q$.<br>
$H = \begin{bmatrix} h_{a_1^{-1}a_1} & h_{a_1^{-1}a_2} & \cdots & h_{a_1^{-1}a_n} \\
                     h_{a_2^{-1}a_1} & h_{a_2^{-1}a_2} & \cdots & h_{a_2^{-1}a_n} \\
                     \cdots \\
                     h_{a_n^{-1}a_1} & h_{a_2^{-1}a_2} & \cdots & h_{a_n^{-1}a_n} \end{bmatrix}$<br>
$\begin{bmatrix} f & g \end{bmatrix} = \begin{bmatrix} f & u \end{bmatrix} * \begin{bmatrix} I_n & H \\ 0_n & qI_n \end{bmatrix}$.<br>
<br>
However if the multiplication is from right, i.e., $f$ and $g$ are column vectors instead of row vectors,<br>
then the equation and structure of $H$ changs a little.<br>
$g = H * f + q * u$ and $H = [h_{a_ia_j^{-1}}]$ instead of $H = [h_{a_i^{-1}a_j}]$.

### Lattice from twisted Group-ring
Will edit later.
