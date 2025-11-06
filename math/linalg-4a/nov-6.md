# 

## properties of transpose

1. $(A^T)^T$ = A
2. $(A + B)^T = A^T + B^T$
3. $(rA)^T = rA^T$
4. $(AB)^T = B^TA^T$

## matrix inverses

> let A be an nxn matrix
> A is s.t.b. invertible
> if $\exists$ an nxn matrix B
> s.t. AB = I = BA
> B is the inverse of A
> notated as $A^{-1} = B$

### e.g.

A = $\begin{bmatrix}1 2\\3 4\end{bmatrix}$
then $A^{-1} = \begin{bmatrix}-2 1\\3/2 -1/2\end{bmatrix}$
$AA^{-1} = I$

how to compute
observe 
$A^{-1} = \begin{bmatrix}-2 1\\3/2 -1/2\end{bmatrix}$

$A^{-1} = \frac1{-2}\begin{bmatrix}4 -2\\-3 1\end{bmatrix}$

$A^{-1} = \frac1{4 - 6}\begin{bmatrix}4 -2\\-3 1\end{bmatrix}$

$A^{-1} = \frac1{4 - (2*3)}\begin{bmatrix}4 -2\\-3 1\end{bmatrix}$

A = $\begin{bmatrix}1 2\\3 4\end{bmatrix}$

flip diagonal, negate off-diagonal
multiply by 1 over some number -> the determinate
$det(A) = (1 * 4) - (2 * 3)$
$\forall A \in \mathbb{R}^2 s.t. det(A) \neq 0$
$s.t. A = \begin{bmatrix}a b\\c d\end{bmatrix}$
$det(A) = ad - bc$
$A^{-1} = \frac1{det(A)}\begin{bmatrix}d -b\\-c a\end{bmatrix}$

> Theorem
> $A is invertible iff det(A) \neq 0$
> $\implies  A^{-1} = \frac1{det(A)}\begin{bmatrix}d -b\\-c a\end{bmatrix}$

if A is invertible, A is non-singular

### e.g.

A =
1 2
1 2

det(A) = 2 - 2 = 0
$\therefore  A^{-1} dne$

## larger matrices

> Theorem
> algorithm for finding $A^{-1}$
> 
> let A be an nxn matrix
> to find $A^{-1}$ construct the augmented matrix $[A | I_n]$
> and manipulate into RREF
> 1. if RREF($[A | I_n]$) is of the form $[I_n | B]$ A^{-1} = B
> 2. if RREF($[A | I_n]$) is not of the form $[I_n | B]$ then A is not invertible

### e.g.

is $A = \begin{bmatrix}1 1 1\\2 3 2\\3 8 2\end{bmatrix}$ invertible?
$\begin{bmatrix}1 1 1 | 1 0 0\\2 3 2 | 0 1 0\\3 8 2 | 0 0 1\end{bmatrix}$

$\begin{bmatrix}1 1 1 | 1 0 0\\0 1 0 | -2 1 0\\0 5 -1 | -3 0 1\end{bmatrix}$

$\begin{bmatrix}1 0 1 | 3 -1 0\\0 1 0 | -2 1 0\\0 0 -1 | 2 -5 1\end{bmatrix}$

$\begin{bmatrix}1 0 0 | 5 -6 1\\0 1 0 | -2 1 0\\0 0 1 | -2 5 -1\end{bmatrix}$

in the form $[I_n | B] \therefore  A^{-1} exists$
$A^{-1} = \begin{bmatrix}5 -6 1\\-2 1 0\\-2 5 -1\end{bmatrix}$
~~this is different than what she got but i think i'm right~~
top left and bottom left wrong

check $AA^{-1}$
i aint doing that by hand rn

### e.g.

$A = \begin{bmatrix}1 -2 1\\4 -7 3\\-2 6 -4\end{bmatrix}$

$A = \begin{bmatrix}1 -2 1 | 1 0 0\\0 1 -1 | -4 1 0\\0 2 -2 | 2 0 1\end{bmatrix}$

$A = \begin{bmatrix}1 0 -1 | -7 2 0\\0 1 -1 | -4 1 0\\0 0 0 | 10 -2 1\end{bmatrix}$
not invertible

## properties of inverses

1. if A is invertible, then $A^{-1}$ is also invertible and the inverse of $A^{-1}$ is A
2. if A&B are invertible matrices of the same size then $(AB)^{-1} = B^{-1}A^{-1}$
$(B^{-1}A^{-1})(AB) = B^{-1}(A^{-1}A)B = B^{-1}IB = B^{-1}B = I$
works the other way by similar reasoning

### remark

consider the system $Ax = b where A is invertible$
$A^{-1}Ax = A^{-1}b$
$x = A^{-1}b$

### e.g.

solve the system:
x + y + z = 0
2x + 3y + 2z = -2
3x + 8y + 2z = 3

$A\begin{bmatrix}x\\y\\z\end{bmatrix} = \begin{bmatrix}0\\-2\\3\end{bmatrix}$

$A^{-1} = \begin{bmatrix}10 -6 1\\-2 1 0\\-7 5 -1\end{bmatrix}$
the system has a unique soln given by 
$\begin{bmatrix}x\\y\\z\end{bmatrix} = \begin{bmatrix}10 -6 1\\-2 1 0\\-7 5 -1\end{bmatrix}\begin{bmatrix}0\\-2\\3\end{bmatrix}$

$\begin{bmatrix}x\\y\\z\end{bmatrix} = \begin{bmatrix}15\\-2\\-13\end{bmatrix}$

### e.g.

without computing the inverse, is A invertible?
$A = \begin{bmatrix}1 -2 1\\4 -7 3\\-2 6 -4\end{bmatrix}$
$[1 4 -2]^T + [-2 -7 6]^T + [1 3 4]^T = [0 0 0]^T$
$\therefore  cols of A is not l.i.$

## linear transformations

> Theorem
> given A and B $\in \mathbb{R}^{nxn}$
> let T $\in \mathbb{R}^n \rightarrow  \mathbb{R}^n$
> be a l.c.
> we say T is invertible if $\exists$ a l.c.
> S $\in \mathbb{R}^n \rightarrow  \mathbb{R}^n$
> s.t. S(T(x)) = x $\forall x \in \mathbb{R}^n$
> s.t. T(S(x)) = x $\forall x \in \mathbb{R}^n$

## exercise for the reader

$let T: \mathbb{R}^2 \rightarrow  \mathbb{R}^2
> be the l.t. which rotates a vector $\in \mathbb{R}^2$
> anticlockwise about the origin by an angle $\theta$
> find $T^{-1}$

