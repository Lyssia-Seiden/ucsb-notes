# null and col spaces

${0} is always a subspace of \mathbb{R}^n$
$\mathbb{R}^n is always a subspace of itself$
solution to a homogeneous linear system is a subspace of the input space
this is the null space

> defn
> 1. let A be an nxn matrix
> the null space of A
> is the set
> null A = $\{x \in  \mathbb{R}^n | Ax = 0 \}$
> it is a subspace of $\mathbb{R}^n$
> this is also known as the kernel of the corresponding l.c.

> let $T: \mathbb{R}^n \rightarrow  \mathbb{R}^m$
> be a linear transformation
> the null space of T aka the kernel of T is
> ker T = null T = $\{x \in  \mathbb{R}^n | T(x) = 0 \}$
> if A is the standard matrix of T
> $T(x) = Ax$
> $\implies  null T = null A$
> $\implies  null T is a subspace of \mathbb{R}^n$
### e.g.

find the null space of
$T([x y z]^T) = \begin{bmatrix}{x + y + z}\\{x + 2y + 3z}\end{bmatrix}$
$A = \begin{bmatrix}1 1 1\\1 2 3\end{bmatrix}$

$\begin{bmatrix}1 1 1\\1 2 3\end{bmatrix}x = 0$

$\begin{bmatrix}1 1 1 | 0\\1 2 3 | 0\end{bmatrix}$

$\begin{bmatrix}1 0 -1 | 0\\0 1 2 | 0\end{bmatrix}$

null space is $\{ [x y z]^T s.t. x = t, y = -2t, z = t \}$
## e.g.

let A be an nxn invertible matrix
what is null A?
{0}

###

in general if A is an mxn matrix
null A {0} iff Ax = 0
has a unique solution x = 0
iff RREF(A) has a pivot in every column

##

let $v_1, v_2, ..., v_r \in  \mathbb{R}^n$
let $w = span{v_1, v_2, ..., v_r}$
then w is a subspace of $\mathbb{R}^n$

soln

$0 \in  w$ becaues all coeffs can be 0
$w_1 = c_1v_1 + ... + c_rv_r$
$w_2 = d_1v_1 + ... + d_rv_r$
$w_1 + w_2 = (c_1 + d_1)v_1 + ... + (c_r + d_r)v_r \in  w$
scalar multiplication works by similar reasoning

## column space

> the column space of an mxn matrix A is
> col A = span { columns of A }
> this is a subspace of $\mathbb{R}^m$

> let T be a l.c. repr by A mxn
> the image of T
> Im T = $\{ T(X)\in \mathbb{R}^m | x\in \mathbb{R}^n \}$
> $= \{ Ax | x\in \mathbb{R}^n \}$
> is col space of A

## basis of a subspace

> let W be a subspace of $\mathbb{R}^n$
> the set $v_1 ... v_r$
> is a basis of W if
> 1. $span\{v_1 ... v_r\} = w$
> 2. $\{v_1 ... v_r\}$ is linearly independant

### theorem

> if W is a subspace of $\mathbb{R}^n$
> then W has a basis
> any 2 bases of W have
> the same number of vectors
> = the dimension of W

### e.g.

$A = \begin{bmatrix}1 3 3 2 -0\\-2 -2 2 -8 2\\2 3 0 7 1\\3 4 -1 11 -8\end{bmatrix}$

$= \begin{bmatrix}1 0 -3 5 0\\0 1 2 -1 0\\0 0 0 0 1\\0 0 0 0 0\end{bmatrix}$

$\{v_1 v_2 v_5\}  spans the col space of A$

