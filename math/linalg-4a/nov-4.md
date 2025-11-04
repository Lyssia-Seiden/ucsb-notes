# matrix algebra

## Matrix addition

> Let A and B be mxn matrices with real entries
> The sum A + B is an mxn matrix with entries that are the sum of the corresponding entries in A and B

## Scalar multiplication

> Let $c\in\mathbb{R}$ and let A be an mxn matrix
> cA is an mxn matrix 
> where each entry is the corresponding entry of A multiplied by c

## properties

let A B and C be matrices of size mxn
let r and s be scalars

### commutativity of addition
A+B = B+A

### associativity of addition
(A+B)+C=A+(B+C)

### distributivity
r(A+B) = rA+rB
(r+s)A = rA+sA
r(sA) = (rs)A

### additive identity
A + 0 = A

## matrix multiplication

if A is an mxn matrix,
then multiplication by A defines a linear transformation
T: $\mathbb{R}^n \rightarrow  \mathbb{R}^m$

> if A is an mx**n** matrix
> and B is an **n**xp matrix
> AB is the standard matrix of
> the composition of transformations of A and B
> $T_{A}\circ T_{B} : \mathbb{R}^p \rightarrow  \mathbb{R}^m$
sidenote unicode really doesnt have subscript letters?

$let AB = [Ta \circ Tb(e_1) Ta \circ Tb(e_2) ... p]$
$B = [v_1 v_2 ... v_p]$

$AB = [Av_1 Av_2 ... Av_p]$

e.g.
$A = \begin{bmatrix}1 2\\3 4\\5 6\end{bmatrix}$

$B = \begin{bmatrix}1 0\\7 -1\end{bmatrix}$

then
col 1
$\begin{bmatrix}1 2\\3 4\\5 6\end{bmatrix}\begin{bmatrix}1\\7\end{bmatrix}$

$\begin{bmatrix}1*1 + 2*7\\3*1 + 4*7\\5*1 + 6*7\end{bmatrix}$

$\begin{bmatrix}15\\31\\47\end{bmatrix}$

col 2

$\begin{bmatrix}1 2\\3 4\\5 6\end{bmatrix}\begin{bmatrix}0\\-1\end{bmatrix}$

$\begin{bmatrix}1*0 + 2*-1\\3*0 + 4*-1\\5*0 + 6*-1\end{bmatrix}$

$\begin{bmatrix}-2\\-4\\-6\end{bmatrix}$

$AB = \begin{bmatrix}15 -2\\31 -4\\47 -6\end{bmatrix}$

another method - rows by columns

recall: $A = \begin{bmatrix}u_1\\u_2\\\vdots\\u_m\end{bmatrix}$
$and x\in \mathbb{R}^m$
$then Ax = \begin{bmatrix}u_1\cdot x\\u_2\cdot x\\\vdots\\u_m\cdot x\end{bmatrix}$

$A = \begin{bmatrix}u_1\\u_2\\\vdots\\u_m\end{bmatrix}$
$B = \begin{bmatrix}v_1 v_2 \dots v_p\end{bmatrix}$
$AB = \begin{bmatrix}u_1\cdot v_1 u_1\cdot v_2 ... u_1\cdot v_p\\u_2\cdot v_1 and so on\end{bmatrix}$


$\begin{bmatrix}1 2\\3 4\end{bmatrix}\begin{bmatrix}1 -1 0\\3 0 2\end{bmatrix}$

$\begin{bmatrix}{1*1 + 2*3} {1*-1 + 2*0} {1*0 + 2*2}\\{3*1 + 4*3} {3*-1 + 4*0} {3*0 + 4*2}\end{bmatrix}$

$\begin{bmatrix}{7} {-1} {4}\\{15} {-3} {8}\end{bmatrix}$

## matmul properties

let A B and C be matrices of appropriate sizes
s.t. the following operations are defined

### associative

A(BC) = (AB)C

### distributive

A(B+C) = AB + AC
(B+C)A = BA + CA

### distributive over scalars

r(AB) = (rA)B = A(rB) $\forall r\in\mathbb{R}$

### multiplicative identity

$I_nA_{nxp} = A = A_{mxn}I_n$
if A is square then AI = IA

## non properties

AB $\neq$ BA
stretch x by 2, then rotate pi/2 ccw
$[1 0]^T goes to [0 2]^T$
rotate pi/2 ccw, then stretch x by 2
$[1 0]^T goes to [0 1]^T$

AB = 0 !$\implies$ A = 0 or B = 0

0 1 | 0 2
0 0 | 0 0
=>
0 0
0 0

AB = AC $!\not\implies$ B = C
BA = CA $!\not\implies $ B = C

> $A^T swaps the columns and rows of A$

