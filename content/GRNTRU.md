# GR-NTRU (Group Ring NTRU)
It is observed that the Group-ring structure is very useful for generalizing and creating lattices for NTRU and NTRU-like cryptosystems.

### Group Ring Definition
Let $R$ be a ring and $G = \lbrace g_1,g_2,\ldots,g_n \rbrace$ be a finite group of order $n$. 
Then, the group ring of $G$ over $R$ is.<br>
$RG = \lbrace \sum\limits_{i=1}^{n}r_{g_i}g_i | r_{g_i} \in R, 1 \leq i \leq n \rbrace$<br>
The addition and multiplication operations in the $GR$ are given as follows-<br>
$r+s = \sum\limits_{i=1}^{n} (r_{g_i} + s_{g_i})g_i$<br>
$r*s = \sum\limits_{i=1}^{n} (\sum\limits_{g_h * g_k = g_i} r_{g_h}s_{g_k})g_i$

### NTRU as a Group-ring
Another perspective of NTRU defined over the ring $ℤ[X]/<X^N-1>$ is to consider it as the Group-ring $ℤC_N$, where $C_N = \lbrace 1,x,x^2,...x^{N-1} \rbrace$ is the cyclic group of order $N$.
