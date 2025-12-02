# eigen

## recap

rank A = dim. col. A
nullity A = dim. null space of A
pivot cols of A form basis of col. A
coordinate vector $[x]_\beta$

## change of basis

let $u_1 = [1 -1 0]^T and u_2 = [1 0 -1]^T$
let $V = span\{u_1, u_2\}$
$\beta  = \{u_1, u_2\} is a basis of V$
now consider $v_1 = [2 -1 -1]^T, v_2 = [0 -1 1]^T$
observe $v_1 = u_1 + u_2 and v_2 = u_1 - u_2$
$\therefore  v_1 & v_2 \in  V$
l.i. bc not scalar multiples

$\gamma  = \{v_1, v_2\} is also a basis of V$
let $x \in  V s.t. [x]_\beta = [5 3]^T$
$\implies  x = 5u_1 + 3u_2$

what is $[x]_\gamma$
multiply by change of basis matrix
write $u_1 and u_2 in terms of v_1 and v_2$
$u_1 = \frac12 v_1 - \frac12 v_2$
$\implies  [u_1]_\gamma = [1/2 -1/2]^T$

$u_2 = \frac12 v_1 + \frac12 v_2$
$\implies  [u_2]_\gamma = [1/2 1/2]^T$

consider the matrix $\begin{bmatrix}\[u_1\]_\gamma \[u_2\]_\gamma\end{bmatrix}$
change of basis matrix from $\beta  to \gamma$
$A = \begin{bmatrix}1/2 1/2\\-1/2 1/2\end{bmatrix}$
$Ax = \begin{bmatrix}1/2 1/2\\-1/2 1/2\end{bmatrix}\begin{bmatrix}5\\3\end{bmatrix}$
$Ax = \begin{bmatrix}5/2 + 3/2\\-5/2 + 3/2\end{bmatrix}$
$Ax = \begin{bmatrix}4\\-1\end{bmatrix}$

$A notated as P_\beta^\gamma$
^ mightve swapped gamma and beta there

## eigenvalues and eigenvectors

Eigen -> german for "inherent property of"

> let A be an nxn matrix
> a nonzero vector $x \in  \mathbb{R}^n$
> is called an eigenvector of A
> iff $\exists \lambda \in \mathbb{R} s.t. Ax = \lambda x$
> $\implies  \lambda  is an eigenvalue of A corresponding to x$

### e.g.

$\begin{bmatrix}1 1\\1 1\end{bmatrix}, u = [1 1]^T, v = [-1 1]^T$
$Au = [1 1]^T = 2u$
$\implies  u is an eigenvector of A$
$\implies  2 is the eigenvalue of A corresponding to u$
$Av = [0 0]^T = 0v$
$\implies  v is an eigenvector of A$
$\implies  0 is the eigenvalue of A corresponding to u$
$\implies  A is not invertible$

### more properties

$\lambda  may be complex, see rotaton matrix$
> x is an eigenvalue of A
> $Ax = \lambda x$
> $Ax - \lambda x = 0$
> $(A - \lambda I_n)x = 0$
> $A - \lambda I_n is not invertible$
> $det(A - \lambda I_n) = 0$
to solve for $\lambda$, solve for the determinant in terms of $\lambda$ as shown above

### e.g.

$A = \begin{bmatrix}1 2\\4 3\end{bmatrix}$
find all eigenvalues of A
$det(A - \lambda I_2) = 0 \forall \lambda$
$det(\begin{bmatrix}1-\lambda  2\\4 3-\lambda\end{bmatrix}) = 0$
$(1 - \lambda)(3 - \lambda) - 8 = 0$
$\lambda^2 - 4\lambda  - 5 = 0$
$(\lambda - 5)(\lambda + 1) = 0$
$\lambda  = 5, -1$
^ eigenvalues

#### eigenvalues $\implies $  eigenvectors

$\lambda  = 5$
$\implies  Ax = 5x$
$\implies  Ax - 5x = 0$
$\implies  (A - 5I_2)x = 0$
$\implies  A - 5I_2 = 0$
$\implies  \begin{bmatrix}-4 2\\4 -2\end{bmatrix} = 0$
$\implies  \begin{bmatrix}-4 2 | 0\\4 -2 | 0\end{bmatrix}$
$\implies  \begin{bmatrix}1 -1/2 | 0\\0 0 | 0\end{bmatrix}$
$\implies  x_1 = \frac{s}2, x_2 = s$
$\implies  x = s\begin{bmatrix}1/2\\1\end{bmatrix}$
$\implies  cx \forall  c \in  \mathbb{R} is an eigenvalue corresponding to the eigenvalue 5$
#### relation to null spaces

if $x is an eigenvector of A$
$x \in  null(A - \lambda I_n)$
eigenvectors are the basis vectors of the null matrix

