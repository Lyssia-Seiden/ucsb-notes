# lecture 3 (? i cant count)

## recap

> matrix def

> matrix size def

> REF + RREF

> gauss-jordan elimination (row reduction algorithm)
linear system -> augmented matrix -> row reductions -> {R}REF -> soln.

## new stuff

> pivot position
a pivot position in a matrix is the location in that matrix that corresponds to a leading 1 in RREF of that matrix

> pivot column
column of that matrix that contains a pivot position

### ex

v pivot
1  4  5
-1 -2 -1
-2 -3  0
^ pivot column
=>
 1  4  5
 0  2  4
 0  5  10
    ^ new pivot column
 a_22 is now pivot

### ex

> Solve the system
>        x_2 + x_3 = 0
> x_1 - 3x_2 - x_3 = 5
> x_1 - 2x_2       = 2
> using gauss-jordan

       x_2 + x_3 = 0
x_1 - 3x_2 - x_3 = 5
x_1 - 2x_2       = 2
-> augmented matrix
0  1  1 | 0
1 -3 -1 | 5
1 -2  0 | 2

1 -3 -1 | 5
0  1  1 | 0
1 -2  0 | 2

1 -3 -1 | 5
0  1  1 | 0
0  1  1 | -3

1 -3 -1 | 5
0  1  1 | 0
0  0  0 | -3

R3 => 0 = -3 \therefore contradiction \therefore inconsistent

### ex

2 0 -4 | 0
-6 3 0 | 1
0 1 -1 | 3
1 1 -3 | 3

1 1 -3  | 3
0 -2 2  | -6
0 9 -18 | 19
0 1 -1  | 3

1 0 -2  | 0
0 1 -1  | 3
0 0 0   | 0
0 0 -9  | -8

1 0 -2  | 0
0 1 -1  | 3
0 0 1   | 8/9
0 0 0   | 0

1 0 0   | 16/9
0 1 0   | 35/9
0 0 1   | 8/9
0 0 0   | 0

x_1 = 16/9
x_2 = 35/9
x_3 = 8/9

> if an augmented matrix has a row of the form `[0 0 ... 0 | b]` where `b != 0` there is no solution and the system is inconsistent

> if a l.s. is consistent
> 1. it has a unique solution <=> there are no free variables <=> all variables are basic
> 2. it has infinitely many solutions <=> there are one or more free variables <=> not all variables are leading

> if a l.s. is inconsistent, there are no solutions

### ex

determine for which values of k the system has {0, 1, \inf} solutions

17 k+2 5k^2-10 | 6k+8
0    1  2k^2-3 | k+1
0    0   k^2-4 | 3k+6

no solutions for k =  2
unique soln  for k != 2
inf solns    for k = -2

## vector equations

### Notation

we denote the n-dimensional Real Euclidian space as **R**^n
ie. **R**^2 is the xy coordinate plane, **R**^3 is xyz real space

we represent points in one of these spaces by a column vector
`[a_1 a_2 ... a_n]^T`

### addition

v = [a_1 a_2 ... a_n]^T
w = [w_1 w_2 ... w_n]^T

v + w = [a_1 + w_1 a_2 + w_2 ... a_n + w_n]^T

### scalar multiplication

c \in **R** v = [v_1 v_2 ... v_n]^T
cv = [cv_1 cv_2 ... cv_n]^T

### Geometric intuition

addition is following one vector than another,
multiplication is scaling while maintaining direction
you watched 3b1b yk how it is

parallelogram law of vectors, addition is commutative

