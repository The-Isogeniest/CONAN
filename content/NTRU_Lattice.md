# NTRU Lattice
Out of all the attacks proposed on NTRU, the lattice based attack is by far the best in present day literature.

### NTRU Public Key
Let $T(r_1,r_2) = \lbrace f \in \frac{\mathbb{Z}[X]}{<X^N-1>} \rbrace$ such that $r_1$ coefficients in $f$ are $1$, $r_2$ coefficients in $f$ are $-1$ and remaining coefficients in $f$ are $0$.
The set $T(r_1,r_2)$ is known as the set of ternary polynomials, as the coefficients of these polynomias only take $3$ different values.<br>
Now let $d = \lfloor \frac{N}{3} \rfloor$. It is observed that with high probability, the elements of $T(d,d)$ are invertible in $\frac{\mathbb{Z}_q[X]}{<X^N-1>}$ and $\frac{\mathbb{Z}_p[X]}{<X^N-1>}$.<br>
Let $f \in T(d,d)$ and $g \in T(d+1,d)$.<br>
Let $h = f^{-1} * g$ (mod $q$).<br>
The polynomial $h$ is the public key.

### Lattice construction from Public Key
Let $h = f^{-1} * g$ (mod $q$) be a Public Key for NTRU cryptosystem.<br>
Then, $g = f*h$ (mod $q$) $\Rightarrow g = f*h + q*u$, for some $u \in \frac{\mathbb{Z}[X]}{<X^N-1>}$.<br>
Also, $f = 1*f + 0*u$.<br>
Thus, consider the matrix equation,<br>
$\begin{bmatrix} f_0 & f_1 & \cdots & f_{N-1} & g_0 & g_1 & \cdots & g_{N-1} \end{bmatrix} = 
 \begin{bmatrix} f_0 & f_1 & \cdots & f_{N-1} & u_0 & u_1 & \cdots & u_{N-1} \end{bmatrix} * 
 \begin{bmatrix} 1 & 0 & \cdots & 0 & h_0 & h_1 & \cdots & h_{N-1} \\
                 0 & 1 & \cdots & 0 & h_{N-1} & h_0 & \cdots & h_{N-2} \\
                 \cdots \\
                 0 & 0 & \cdots & 1 & h_1 & h_2 & \cdots & h_0 \\
                 0 & 0 & \cdots & 0 & q & 0 & \cdots & 0 \\
                 0 & 0 & \cdots & 0 & 0 & q & \cdots & 0 \\
                 \cdots \\
                 0 & 0 & \cdots & 0 & 0 & 0 & \cdots & q \\
 \end{bmatrix}$.<br>
 
