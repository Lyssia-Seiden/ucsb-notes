# crashing out

## A.
1. A vector in $\mathbb{R}^3$ has both direction and magnitude
True, all vectors do

2. The sum of two vectors in $\mathbb{R}^n$ is always in $\mathbb{R}^n$
True

3. The span of a single nonzero vector in $\mathbb{R}^3$ is always a plane
False

4. If **b** is a linear combination of $a_1, a_2$, then $**b** \in  Span\{a_1, a_2\}$
True

5. $Span\{a_1, a_2, a_3\}$ is always all of $\mathbb{R}^3$
False

## B.

1. Let
u = $\start{bmatrix}2\\-1\\3\end{bmatrix}$ v = \start{bmatrix}-1\\4\\2\end{bmatrix} w = \start{bmatrix}0\\2\\-2\end{bmatrix}$

## C

$a_1 = \begin{bmatrix}1\\2\\1\end{bmatrix} a_2 = \begin{bmatrix}2\\-1\\0\end{bmatrix} b = \begin{bmatrix}3\\5\\1\end{bmatrix}$
$\begin{bmatrix}1 2 | 3\\2 -1 | 5\\1 0 | 1\end{bmatrix}$

$\begin{bmatrix}1 0 | 1\\0 2 | 2\\0 -1 | 3\end{bmatrix}$


$\begin{bmatrix}1 0 | 1\\0 1 | 1\\0 0 | 4\end{bmatrix}$

$inconsistent \implies  b \notin  Span\{a_1, b_1\}$

## D

5.

$A = \begin{bmatrix}1 2 0\\0 1 1\\2 3 4\end{bmatrix} b_1 = [3 2 8]^T b_2 = [2 0 ]^T$
$\begin{bmatrix}1 2 0 | 3\\0 1 1 | 2\\2 3 4 | 8\end{bmatrix}$

$\begin{bmatrix}1 2 0 | 3\\0 1 1 | 2\\0 -1 4 | 2\end{bmatrix}$

$\begin{bmatrix}1 0 -2 | -1\\0 1 1 | 2\\0 0 1 | \frac45\end{bmatrix}$

$\begin{bmatrix}1 0 0 | \frac35\\0 1 0 | \frac65\\0 0 1 | \frac45\end{bmatrix}$

$system is consistent \therefore  x \in  Span\{A}$


$\begin{bmatrix}1 2 0 | 2\\0 1 1 | 0\\2 3 4 | 1\end{bmatrix}$

$\begin{bmatrix}1 2 0 | 2\\0 1 1 | 0\\0 -1 4 | -3\end{bmatrix}$

$\begin{bmatrix}1 0 -2 | 2\\0 1 1 | 0\\0 0 1 | -3/5\end{bmatrix}$

$\begin{bmatrix}1 0 0 | 4/5\\0 1 0 | 3/5\\0 0 1 | -3/5\end{bmatrix}$

$system is consistent \therefore  x \in  Span\{A\}$

6.

$\begin{bmatrix}1 -1 | 2\\0 3 | 3\\2 1 | 5\end{bmatrix}$

$\begin{bmatrix}1 -1 | 2\\0 3 | 3\\0 3 | 1\end{bmatrix}$

$\begin{bmatrix}1 -1 | 2\\0 3 | 3\\0 0 | -2\end{bmatrix}$

$inconsistent \therefore  v_3 \notin  Span\{v_1, v_2\}$


