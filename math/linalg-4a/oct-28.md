#

~5 true/false
4-5 questions to "work out"
1 ?? question

4x6in notecard
bring ID

## recap

l.t. represented by standard matrices $T:\mathbb{R}^n\rightarrow\mathbb{R}^m$

##

$T:\mathbb{R}^n\rightarrow\mathbb{R}^m$
domain $\rightarrow$ codomain
Im(T) is the set of all $T(x), x\in\mathbb{R}^n$, range of T
> let T be a linear transformation
> 1. T is surjective if 
> $\forall b\in \mathbb{R}^m \exists x\in \mathbb{R}^n s.t. T(x) = b$
> 2. we say that T is injective if $\forall b\in \mathbb{R}^m \exists  at most one x\in \mathbb{R}^n s.t. T(x) = b$
surjective $\Leftrightarrow$ onto
injective $\Leftrightarrow$ one-to-one

consider the projection transformation
$T([x_1, x_2]^T) \rightarrow [x_1, 0]^T$
is T surjective?
$\forall[y_1, y_2]\in codomain \exists  preimage in \mathbb{R}^2 s.t. T is preserved?$
no, $\nexists [x_1, x_2]^T s.t. T([x_1, x_2]^T) = [0, 1]^T$
$\therefore  T is not surjective$

is T injective?
no, $T([1, 1]^T) = T([1, 2]^T) = [1, 0]^T$

> T is bijective iff surjective and injective

###

let T $\mathbb{R}^n \rightarrow  \mathbb{R}^m$ be a l.t.
s.t. only the 0 vector in $\mathbb{R}^n$ gets mapped to the 0 vector in $\mathbb{R}^m$
is T injective?

Let $x_1, x_2 \in  \mathbb{R}^n s.t. T(x_1) = T(x_2)$
$ T(x_1) - T(x_2) = 0 \in  \mathbb{R}^n$
$T(x_1 - x_2) = 0$
$T(x_1 - x_2) = T(0)$
$x_1 - x_2 = 0$
$x_1 = x_2$
$\therefore  T must be injective Q.E.D.$

###

consider the l.t. $T. \mathbb{R}^4 \rightarrow  \mathbb{R}^3  x \rightarrow  Ax$
where $A = \begin{bmatrix}1 3 5 7\\3 5 7 9\\5 7 9 3\end{bmatrix}$
is T injective?

T(x) = 0 $\implies$  x = 0
$Ax = 0 \implies  x = 0$
only solution to Ax = 0 is the trivial one
the linear system has no free variables

$\begin{bmatrix}1 3 5 7 | 0\\3 5 7 9 | 0\\5 7 9 3 | 0\end{bmatrix}$

Ax = 0 has infinitely many solutions
$\implies $ nonzero vectors are mapped to the 0 vector
$\therefore  T is not injective Q.E.D.$

###


consider the l.t. $T. \mathbb{R}^4 \rightarrow  \mathbb{R}^3  x \rightarrow  Ax$
where $A = \begin{bmatrix}1 3 5 7\\3 5 7 9\\5 7 9 3\end{bmatrix}$
is T surjective?

$T is surjective \iff  \forall b \in  \mathbb{R}^3 the system Ax = b has at least one solution$
$\iff  RREF(A) has a leading 1 in every row$

$\begin{bmatrix}1 3 5 7 | 0\\0 -4 -8 -12 | 0\\0 -8 -16 -32 | 0\end{bmatrix}$

$\begin{bmatrix}1 3 5 7 | 0\\0 1 2 3 | 0\\0 1 2 4 | 0\end{bmatrix}$

$\begin{bmatrix}1 0 -1 0 | 0\\0 1 2 0 | 0\\0 0 0 1 | 0\end{bmatrix}$

there is a leading 1 in every row, $\therefore  T is surjective Q.E.D.$

###

Theorem: 
> Let $T: \mathbb{R}^n \rightarrow  \mathbb{R}^m be a l.t.$ with matrix A
> 1. T is injective$\iff $ Ax = 0 has a unique solution (the trivial solution)
> $\iff $ columns of A are linearly independent
> $\iff $ RREF(A) has a leading 1 in every column
> 2. T surjective$\iff $ RREF(A) has a leading 1 in every row, ie no inconsistencies
> $\iff  columns of A span \mathbb{R}^m$

Remark
$Let T: \mathbb{R}^n \rightarrow  \mathbb{R}^m be a l.t.$
1. $if n > m \implies  T cannot be injective, free variables$
2. $if n < m \implies  T cannot be surjective, more possible outputs than inputs$
3. $if n = m then T is surjective\iff  T is injective$

### Examples

Let T: $\mathbb{R}^3 \rightarrow  \mathbb{R}^4$
s.t. $[x_1, x_2, x_3]^T \rightarrow  [x_1, x_1 + x_2, x_2 + x_3, x_3]^T$
Determine whether T is surjective and/or injective
m > n, $\therefore $ T is not surjective

$T(x) = \begin{bmatrix}1 0 0\\1 1 0\\0 1 1\\0 0 1\end{bmatrix}x$

$= \begin{bmatrix}1 0 0\\0 1 0\\0 0 1\\0 0 0\end{bmatrix}x$

leading 1 in every column $\therefore $ T is injective

