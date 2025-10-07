# lectureureure

## recap

vectors are column things, parallelogram
properties of $\mathbb{R}^n$
add any two vectors component wise
^ commutative

## properties of vectors

$\forall  vectors u and v \in  \mathbb{R}^n$
u + v = v + u
$\forall  vectors u, v, and w \in  \mathbb{R}^n$
(u + v) + w = u + (v + w)
$\forall  vectors u \in  \mathbb{R}^n$
u + 0 = u
$\forall  vectors u \in  \mathbb{R}^n$
u + (-u) = (-u) + u = 0
$\forall  vectors u and v \in  \mathbb{R}^n and c \in  \mathbb{R}$
c(u + v) = cu + cv
$\forall  vectors u \in  \mathbb{R}^n and c, d \in  \mathbb{R}$
(c + d)u = cu + du
$\forall  vectors u \in  \mathbb{R}^n and c, d \in  \mathbb{R}$
(cd)u = c(du)
$\forall  vectors u \in  \mathbb{R}^n$
u * 1 = 1 * u = u

## linear combination and spanning sets

> a linear combination of vectors $v_1$, $v_2$, ..., $v_n$ is another vector of a specific form:
> $c_1v_1 + c_2v_2 + ... c_nv_n where c_i \in  \mathbb{R}  \forall  i$

eg.
$let v_1, v_2 \in  \mathbb{R}^n$
$2v_1 + v_2 is a l.c. of v_1 and v_2$
$c_1 = 2 & c_2 = 1$
eg.
$\sqrt{2}v_1 + \frac32v_2 is a l.c. of v_1 and v_2$
eg.
$3v_1 is a l.c. of v_1 and v_2 (c_2 = 0)$
$0 is a l.c. of v_2 and v_2 (c_1 = c_2 = 0)$

q.
$is b = \begin{bmatrix} 2\\ 4\\ 6 \end{bmatrix} a l.c. of v_1 = \begin{bmatrix} 2\\ 1\\ -1 \end{bmatrix} and v_2 = \begin{bmatrix} 1\\ 2\\ -3 \end{bmatrix}$

$=>$

$ b = c_1v_1 + c_2v_2$

$=>$
$$$
2c_1 + c_2 = 2\\
 c_1 + 2c_2 = 4\\
-c_1 - 3c_2 = 6
$$$

$ solve; if consistent, b is a l.c. of v_1 and v_2$

$$$\begin{bmatrix}
2 1 | 2\\
1 2 | 4\\
-1 -3 | 6
\end{bmatrix}$$$
$$$\begin{bmatrix}
1 2 | 4\\
0 -3 | -6\\
0 -1 | 10
\end{bmatrix}$$$
$$$\begin{bmatrix}
1 2 |  4\\
0 1 | -10\\
0 0 | -36\\
\end{bmatrix}$$$
$the last row represents 0 = 12, which is a contradiction \therefore  inconsistent$
$ inconsistency implies c is not a linear combination of v_1 and v_2 Q.E.D.$

## vector equations

> a vector equation is an equation of the form:
> $c_1v_1 + c_2v_2 + ... + c_nv_n = \vec{b}$
> where $c_i \in  \mathbb{R} and v_i \in  \mathbb{R}^n  \forall  i$

this vector equation has a soltuion if and only if: 
the augmented matrix given by $\begin{bmatrix} v_1 v_2 \dots  v_n | \vec{b} \end{bmatrix}$ is consistent

## spans & spanning sets

> $let \vec{v_1}, \vec{v_2}, ..., \vec{v_m} \in  \mathbb{R}^n$
> $the span (spanning set) of these vectors is a subset of \mathbb{R}^n$
> $consisting of all vectors that are linear combinations of \vec{v_1}, \vec{v_2}, ..., \vec{v_m}$
### notation

> $span\{\vec{v_1}, \vec{v_2}, ..., \vec{v_m}\}$
> $ = all vectors of the form c_1\vec{v_1} + c_2\vec{v_2} + ... + c_m\vec{v_m}$
> where $c_i \in  \mathbb{R}  \forall  i$

eg.

$\begin{bmatrix}4\\11\end{bmatrix} = c_1\begin{bmatrix}2\\-3\end{bmatrix} + c_2\begin{bmatrix}5\\1\end{bmatrix}$

$$$\begin{bmatrix}
2 5 | 4\\
-3 1 | 11
\end{bmatrix}$$$

$$$\begin{bmatrix}
1 5/2 | 2\\
0 -3/2 | 9
\end{bmatrix}$$$
$$$\begin{bmatrix}
1 5/2 | 2\\
0 1 | -6
\end{bmatrix}$$$

$$$\begin{bmatrix}
1 0 | -13\\
0 1 | -6
\end{bmatrix}$$$
^ messed up arithmetic but it *is* consistent
$ system has a solution \therefore  is consistent \therefore  \vec{b} is in the span$

$\begin{bmatrix}4\\11\end{bmatrix} \in  span\{\begin{bmatrix}2\\-3\end{bmatrix} + \begin{bmatrix}5\\1\end{bmatrix}\}$

eg.
$\begin{bmatrix} 2\\4\\6\end{bmatrix}\notin span\{ \begin{bmatrix} 2\\1\\-1\end{bmatrix}, \begin{bmatrix} 1\\2\\3\end{bmatrix} \}$
^ idk what this is tryna do tbh

> $span\{\begin{bmatrix}1\\1\end{bmatrix}\} = c\begin{bmatrix}1\\1\end{bmatrix} \forall  c \in  \mathbb{R}$
because span of a vector in $\mathbb{R}^2$ is the line through that vector and the origin

4. 
$span\{\begin{bmatrix}1\\0\\0\end{bmatrix},\begin{bmatrix}0\\1\\0\end{bmatrix}\}  = \mathbb{R}^2 (in particular xy plane)$
$=> \begin{bmatrix}c_1\\c_2\\0\end{bmatrix} \forall  c_1, c_2 \in  \mathbb{R}$

eg.
$span\{\begin{bmatrix}1\\0\\0\end{bmatrix},\begin{bmatrix}0\\1\\0\end{bmatrix},\begin{bmatrix}0\\0\\1\end{bmatrix}\}$
$=> \mathbb{R}^3 or normal 3d space$
$=>\begin{bmatrix}c_1\\c_2\\c_3\end{bmatrix} \forall c_1,c_2,c_3 \in  \mathbb{R}$
^ this set of 3 vectors is called the **generating set** of $\mathbb{R}^3$
these vectors are **linearly independent** and the **basis** of $\mathbb{R}^3$
more on allat later!
or from 3b1b...



