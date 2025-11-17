# 

> If T $\mathbb{R}^n \rightarrow  \mathbb{R}^n$ is a l.t. with standard matrix A
> T is invertible iff A is invertible
> and the standard matrix of $T^{-1}$ is $A^{-1}$

## determinants

det(A) where A is 1x1 = $a_{11}$
det(A) where A is 2x2 = $a_{11}a_{22} - a_{12}a_{21}$
det(A) where A is 3x3 = $a_{11}a_{22}a_{33} + a_{12}a_{23}a_{31} + a_{13}a_{21}a_{32} - a_{13}a_{22}a_{31} - a_{11}a_{23}a_{32} - a_{12}a_{21}a_{33}$
Sorrus' Rule
take tl->br diagonals, wrapping, and add as positive terms
take bl->tr diagonals, wrapping, and subtract as negative terms

##

> Let A be an nxn matrix for n >= 2
> with entries $a_{11} ... a_{nn}$
> the (i,j)th cofactor of A
> is $C_{ij} = (-1)^{i+j} + det(A_{ij}) where 1 \leq i \leq n and 1 \leq j \leq n$
> where $A_{ij}$ is the matrix obtained from A by removing the ith row and jth column

e.g.
$A = \begin{bmatrix}1 3 6 2\\9 1 3 0\\9 2 2 0\\5 0 0 3\end{bmatrix}$
compute $C_{23}$
$A_{23} = \begin{bmatrix}1 3 2\\9 2 0\\5 0 3\end{bmatrix}$
$det(C_{23}) = -95$
$C_{23} = (-1)^{2+3}(-95)$
$C_{23} = 95$

> $det(A) = a_{11}C_{11} + a_{12}C_{12} + ... + a_{1n}C_{1n}$

e.g.
$\begin{bmatrix}1 3 4\\5 0 2\\2 -1 3\end{bmatrix}$

$\begin{bmatrix}+ - +\\1 3 4\\5 0 2\\2 -1 3\end{bmatrix}$

$C_{11} = 2$
$C_{12} = -11$
$C_{13} = -5$

$det(A) = 2 + 3(-11) + 4(-5)$
$det(A) = -51$

> $\forall A \in \mathbb{R}^{nxn}$
> $det(A) = a_{i1}C_{i1} + a_{i2}C_{i2} + ... + a_{in}C_{in}$
> $det(A) = a_{1j}C_{1j} + a_{2j}C_{2j} + ... + a_{nj}C_{nj}$

e.g.
$det(\begin{bmatrix}1 3 4\\5 1 2\\2 -1 3\end{bmatrix}$
$det(\begin{bmatrix}1 3 4 +\\5 0 2 -\\2 -1 3 +\end{bmatrix}$
$= 4(-5) -2(-7) + 3(-15)$
$= -51$

> def upper triangular matrices
> a square matrix is upper triangular
> if all entries below the diagonal are 0

similarly
> a square matrix is lower triangular if all entries above the diagonal are zero

e.g.
$\begin{bmatrix}3 7 3 1\\0 5 6 8\\0 0 -1 7\\0 0 0 10\end{bmatrix}$
using first column for finding det
$det(A) = 3 * det(\begin{bmatrix}5 6 8\\0 -1 7\\0 0 10\end{bmatrix})$

$det(A) = 3 * 5 * det(\begin{bmatrix}-1 7\\0 10\end{bmatrix})$

$det(A) = 3 * 5 * -10$

det(A) where A is triangular is just product of diagonal

swapping any two rows in a matrix negates the determinant


