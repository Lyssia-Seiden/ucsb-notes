# aaaa

$consider A = [a_1 a_2 ... a_n] and b\in \mathbb{R}^m$
When is Ax = b solvable?
Reduce [A | b] -> [A' | d] for $d\in \mathbb{R}^m$
if A' has a zero row, $[0 0 ... 0 | d_l] d_l != 0$
no solutions

> Let A be an m x n matrix
> The following are equivalent
> $\forall b \in \mathbb{R}^m, the matrix eqn Ax = b has a solution$
> $\forall b \in \mathbb{R}^m, b is a l.c. of the columns of A$
> $Span\{a_1, a_2, ..., a_n\} = \mathbb{R}^m where a_i are columns of A$
> A' has a pivot position in every row

##

Let A be an m x n matrix with m > n
is An = b solvable $\forall b \in \mathbb{R}^m$

A: no, there are more equations than unknowns

$\begin{bmatrix}**a** b c | b_1\\d **e** f | b_2\\g h **i** | b_3\\j k l | b_4\end{bmatrix}$

$j k l must be 0s, which means b_4 = 0, which is not true \forall b \in \mathbb{R}^m$
##

Let A be an m x n matrix with m < n
is An = b solvable $\forall b \in \mathbb{R}^m$

A: no, there are more equations than unknowns

$\begin{bmatrix}**a** b c d | b_1\\e **f** g h | b_2\\i j **k** l | b_3\end{bmatrix}$

this is solvable, there is at least one free variable

## Homogeneous linear systems

> a l.s. is homogeneous
> if its augmented matrix is of the form
> $[A | 0]$

This is the augmented matrix of $Ax = 0$
e.g.
$x_1 - 3x_2 - x_3 + x_4 = 0$
$x_2 + x_3 = 0$

## solutions of h.l.s.

Remark: h.l.s. Ax = 0 always has one solution, x = 0
this is called the trivial solution

if x != 0 is also a solution, the l.s. is said to have a nontrivial solution

Theorem
> A h.l.s. can have
> 1. exactly 1 solution, x = 0
> 2. infinitely many solutions $\implies$  free variables

##

determine whether the following h.l.s. has nontrivial solutions
$A = \begin{bmatrix}1 3 -5\\1 4 -8\\-3 -7 9\end{bmatrix}$

$\begin{bmatrix}1 3 -5 | 0\\0 1 -3 | 0\\0 2 -6 | 0\end{bmatrix}$

$\begin{bmatrix}1 0 4 | 0\\0 1 -3 | 0\\0 0 0 | 0\end{bmatrix}$

there is a free variable, therefore there are infinite solutions, therefore there are nontrivial solutions

## 

$\begin{bmatrix}1 3 -1 1 | 0\\0 1 1 0 | 0\end{bmatrix}$

$\begin{bmatrix}1 0 -4 1 | 0\\0 1 1 0 | 0\end{bmatrix}$
$x_3 and x_4 are free$

$x_1 = 4r - s$
$x_2 = -r$

$x = \begin{bmatrix}4\\-1\\1\\0\end{bmatrix}r + \begin{bmatrix}-1\\0\\0\\1\end{bmatrix}s$

soln. $Span\{\begin{bmatrix}4\\-1\\1\\0\end{bmatrix} + \begin{bmatrix}-1\\0\\0\\1\end{bmatrix}\}$

##

now consider Ax = b
let $x_h$ be a particular solution of Ax = 0
let $x_p$ be a particular solution of Ax = b
then $x_h + x_p$ is also a solution of Ax = b

if $x_p is a solution of Ax = b, Ax_p = b$
if $x_h is a solution of Ax = 0, Ax_h = 0$
$ Ax_p + Ax_h = b + 0$
$A(x_p + x_h) = b + 0$
$A(x_p + x_h) = b$

###


$\begin{bmatrix}1 3 -1 1 | 5\\0 1 1 0 | 2\end{bmatrix}$

$\begin{bmatrix}1 0 -4 1 | -1\\0 1 1 0 | 2\end{bmatrix}$
soln x = [-1 2 0 0] + r[4 -1 1 0 + s[-1 0 0 1]

##

 > $The vectors v_1, v_2, ..., v_n \in \mathbb{R}^m$
 > $are linearly dependant if \exists $
 > constants $c_1, c_2, ..., c_n$ not all zero s.t.
 > $c_1v_1 + c_2v_2 + ... + c_nv_n = 0$

