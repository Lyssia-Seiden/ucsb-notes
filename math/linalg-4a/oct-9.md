# crashing 

## recap

> linear combination of vectors
given $v_1, v_2, ..., v_m$, a l.c. is in the form $c_1v_1 + c_2v_2 + ... + c_mv_m \forall  c_i \in  \mathbb{R}$
> span of $v_1, v_2, ..., v_m$
set of all l.c. of $v_1, v_2, ..., v_m$

e.g.
find the equaiton of the plane spanned by $v_1 = \begin{bmatrix}1\\1\\1\end{bmatrix} & v_2 = \begin{bmatrix}2\\1\\0\end{bmatrix}$
let $[x y z]^T$ be a vector spanned by $v_1 and v_2$ 

$\implies  \exists c_1, c_2 \in \mathbb{R} [x y z]^T = c_1v_1 + c_2v_2$

$c_1 +2c_2 = x$
$c_1 + c_2 = y$
$c_1 = z$

$\begin{bmatrix}1 2 | x\\1 1 | y\\1 0 | z\end{bmatrix}$

$\begin{bmatrix}1 0 | z\\0 1 | y - z\\0 2 | x - z\end{bmatrix}$

$\begin{bmatrix}1 0 | z\\0 1 | y - z\\0 0 | x + z - 2y\end{bmatrix}$

$plane is given by x - 2y + z = 0$

e.g.
$find the eqs. describing the space spanned by the vectors [1 3 0 2]^T & [0 1 1 1]^T in \mathbb{R}^4$
$\begin{bmatrix}1 0 | x\\3 0 | y\\0 1 | z\\2 1 | w\end{bmatrix}$

$\begin{bmatrix}1 0 | x\\0 0 | y - 3x\\0 1 | z\\0 1 | w - 2x\end{bmatrix}$

$\begin{bmatrix}1 0 | x\\0 0 | y - 3x\\0 1 | z\\0 0 | w - 2x - z\end{bmatrix}$

$\begin{bmatrix}1 0 | x\\0 1 | z\\0 0 | y - 3x\\0 0 | w - 2x - z\end{bmatrix}$

$\begin{bmatrix}1 0 | x\\0 1 | z\\0 0 | -5x + y - z + w\\0 0 | w - 2x - z\end{bmatrix}$

$space spanned by the vectors is defined by -5x + y - z + w = 0$

^ maybe shouldnt have combined them?
## Matrix vector products

> Matrix equtation $Ax = b$
> Let A be an $m x n$ matrix
> With columns $a_1, a_2, ..., a_n$ each in $\mathbb{R}^m$
> & $x = [x_1 x_2 ... c_n]^T \in  \mathbb{R}^n$
> The product $Ax$ is defined as
> $Ax = x_1a_1 + x_2a_2 + ... + x_na_n$
> $\Longleftrightarrow  [a_1 a_2 ... a_n][x_1 x_2 ... x_n]^T$
> number of columns in A = number of entries in x

e.g.
$A = \begin{bmatrix}1 2\\3 4\\5 6\end{bmatrix} x = [7 8]^T$

$Ax = \begin{bmatrix}1 2\\3 4\\5 6\end{bmatrix}\begin{bmatrix}7\\8\end{bmatrix}$

$Ax = 7\begin{bmatrix}1\\3\\5\end{bmatrix} + 8\begin{bmatrix}2\\4\\6\end{bmatrix}$

$Ax = \begin{bmatrix}7+16\\21+32\\35+48\end{bmatrix}$

$Ax = \begin{bmatrix}23\\53\\83\end{bmatrix}$

e.g.
$let v_1, v_2, v_3 be vectors in \mathbb{R}^3$
write the linear combination 3v_1 + 2v_2 - 5v_3 as a matrix vector product

$V = [v_1 v_2 v_3]$

$V\begin{bmatrix}3\\2\\-5\end{bmatrix}$

$[v_1 v_2 v_3]\begin{bmatrix}3\\2\\-5\end{bmatrix}$

## Dot product

> If v is a vector $[v_1 v_2 ... v_n]^T & w = [w_1 w_2 ... w_n]^T$
> their dot product is $v\cdot w = v_1w_1 + v_2w_2 + ... + v_nw_n$ 

### Alternate way to computer Ax

let $A = \begin{bmatrix}u_1\\u_2\\\vdots\\u_m\end{bmatrix}$
then $Ax = \begin{bmatrix}u_1\cdot x\\u_2\cdot x\\\vdots\\u_m\cdot x\end{bmatrix}$
e.g.
$\begin{bmatrix}1 2\\3 4\\5 6\end{bmatrix}\begin{bmatrix}7\\8\end{bmatrix}$

$\begin{bmatrix}7*1+8*2\\7*3+8*4\\7*5+8*6\end{bmatrix}$

$\begin{bmatrix}7+16\\21+32\\35+48\end{bmatrix}$

$\begin{bmatrix}23\\53\\83\end{bmatrix}$

###

observe we can write a linear system in $x_1, x_2, ..., x_n$
with the augmented matrix $[A|b]$
as both
1. as a vector equation $x_1a_1 + x_2a_2 + ... + x_na_n = b$
where $a_i are columns of A \forall i$
2. as a matrix equation $Ax = b$
where $x = [x_1 x_2 ... x_n]^T$

Q consider $A=\begin{bmatrix}1 0 0\\0 1 0\\0 0 1\end{bmatrix}$
A $Ax = \begin{bmatrix}1 0 0\\0 1 0\\0 0 1\end{bmatrix}\begin{bmatrix}x_1\\x_2\\x_3\end{bmatrix}$

$Ax = \begin{bmatrix}1x_1 0x_2 0x_2\\0x_1 1x_2 0x_3\\0x_1 0x_2 1x_3\end{bmatrix}$

$Ax = \begin{bmatrix}x_1\\x_2\\x_3\end{bmatrix} = x$

> $A = \begin{bmatrix}1 0 \dots  0\\0 1 \dots  0\\\vdots  \vdots  \ddots  0\\0 0 \dots  1\end{bmatrix} = I "identity"$

### Props of Ax

1. $A(x + y) = Ax + Ay$
2. $A(cx) = c(Ax)$

ex
$A = \begin{bmatrix}1 1 -1\\2 1 3\\3 1 4\end{bmatrix} x= [1 1 1]^T y = [1 0 1]^T c = 5$

