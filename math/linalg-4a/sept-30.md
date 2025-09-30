# Sept 30 - Lecture 2

## Recap

see journal

row reduction:
add multiples of each row to other rows to eliminate variables

### Goal today: Systems -> Matrices

## Matrices

### Defn. Matrix

an `n` by `m` matrix is a rectangular array with `m` rows and `n` columns.

see journal

`m x n` is the size of the matrix

a_{ij} is the `ij`th entry of the matrix.
`i`th row, `j`th column.
our course will use mainly real numbers.

2 x 3
$\begin{bmatrix}
1 & 2 & 3\\
-4 & 5 & 7
\end{bmatrix}$


$\begin{bmatrix}
1
\end{bmatrix}$


$\begin{bmatrix}
1 & 2 & 3\\
0 & 0 & 1\\
0 & 0 & 0
\end{bmatrix}$

### Relating linear systems

Consider a system of `m` linear equations in `n` variables,
x_1, x_2, ..., x_n

$
\begin{bmatrix}
a_{11}x_1, a_{12}x_2, ..., a_{1n}x_n,\\
a_{21}x_1, a_{22}x_2, ..., a_{2n}x_n,\\
..., ..., ..., ....,\\
a_{m1}x_1, a_{m2}x_2, ..., a_{mn}x_n,
\end{bmatrix}
=
=
\begin{bmatrix}
b_1,\\
b_2,\\
...,\\
b_m,
\end{bmatrix}
$

encode the information of the system in its **associated augmented matrix**.

augment by adding RHS.
see journal.

### Row Reduction in matrices

#### Elementary Row Operations

1. Row replacement:
    R_i replaced by R_i + cR_j
2. Row interchange:
    R_i <--> R_j 
3. Row scaling:
    R_i *= c, c != 0

Goal: make matrix **row reduced echelon form**

#### Row Echelon Form (REF)

A matrix is s.t.b. REF if
1. all zero rows are at the bottom
2. the first nonzero entry of each row is to the right of the first nonzero entry of the previous row
3. all entries in a column below a leading entry are 0

see journal

#### Row Reduced Echelon Form (RREF)

A matrix is s.t.b. RREF if
1. it is REF
2. the leading entry of each nonzero row is 1
(leading 1)
3. if a column contains a leading 1, all other entries of that column are 0

see journal

#### Row Reduction / Gauss-Jordan Elimination Algorithm

Given a linear system
1. Construct associated augmented matrix **A**
2. Via elementary row operations, convert **A** to RREF
3. Immediate solution

> Transforming a matrix into REF is called Gaussian elimination

see journal

leading variables in an RREF matrix are called "basic" variables.
this is x_1 and x_3 in journal example.
others are the "free" variables.
this is x_2 and x_4 in journal example.

#### Theorem: RREFs are unique

> Each matrix is row equivalent to exactly 1 matrix in RREF

> Matrices A and B are row equivalent if 
> ∃ a finite sequence of elementary row operations on A that result in B

