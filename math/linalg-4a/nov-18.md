# 

> Theorem
> Let A be a square matrix
> 1. det(elem. row. op (A)) = detA
> => det(RREF(A)) = det(A)
> 2. det(A with 2 rows interchanged) = -detA
> 3. det(A with a row multiplied by k) = kdetA

demoed using row ops -> upper triangular for det of 4x4

> Let A be an nxn matrix
> det(A) = k * det RREF(A) where k!=0
> det A != 0 if RREF(A) = I
> => iff A is invertible

$\begin{bmatrix}\lambda  1 1\\1 \lambda  -1\\1 1 \lambda\end{bmatrix}$

det(A) = $\lambda(\lambda^2 + 1) - (\lambda  + 1) + (1 - \lambda)$
= $\lambda^3  - \lambda$
= $\lambda(\lambda + 1)(\lambda - 1)$
A is invertible $\forall \lambda \notin \{0, -1, 1\}$

> $det(A) = det(A^T)$

> $det(A^{-1}) = \frac1{det(A)} = (det(A))^{-1}$

> $detAB = detA * detB$

> $det(A+B) \neq  detA = detB$

##

> let A be an nxn matrix
> the adjoint/adjugate matrix of A
> is the transpose of the cofactor matrix of A

adj(A) = $\begin{bmatrix}C_{11} C_{12} \dots C_{1n}\\C_{21} C_{22} \dots C_{2n}\\\vdots\\C_{n1} C_{n2} \dots C_{nn}\end{bmatrix}^T$
$\forall   C_{ij} = (i,j)^{th} cofactor of A = (-1)^{i+j}detA_{ij}$
> $A^{-1} = \frac1{detA}adj(A)$
##

> A subset W of $\mathbb{R}^n$
> 1. W contains 0
> $w_1, w_2 \in  W \implies  w_1 + w_2 \in  W$
> $w \in  W \implies  cw in  W \forall c \in \mathbb{R}$

