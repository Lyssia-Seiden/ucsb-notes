# First class

I'm crashing this so tbd how things go.
Hw due fridays.
Midterm on 30 oct.

Syllabus recap.
4A covers first 6 chapters of linear algebra w/ apps (see syllabus).

Thr 12-3 office hours.


## Def: Linear equation
- expression including '='
- no exponents > 1

A linear equation in `n` variables,
(x_1, x_2, etc),
can be written as:
a_1*x_1, a_2*x_2, ..., a_n*x_n = b
where a_i and b are either real or complex.

### Ex

- 2x_1 + 4x_2 + 10 = x_2
=> 2x_1 + 3x_2 = -10

- x_2 = 2sqrt(6) - 3x_1 + x_3
=> 3x_1 + x_2 - x_3 = 2sqrt(6)

- 3x_1 - x_3 = 2sqrt(6)
(in this case, 0 * x^2)

## Def: Systems of Linear Equations

AKA Linear System

A collection of linear equations involving the same variables.

### Ex

2x_1 - x_2 + x_3 = 8
x_1       - 4x_3 = -1

## Def: Solution to Linear System

A solution to a linear system in `n` variables is a set of `n` numbers
which when substituted for in for the variables satisfies the system.

### Ex

Solve the following systems:

```
x - y = 0
3x - y = 2
```

```
-2x = -2
```

```x = 1```

```
1 - y = 0
```

```y = 1```

therefore the solution to the system:
[x y]^T = [1 1]^T
(unique solution)

```
x + y = 0
3x + 3y = 0
```
collapses to
```
x + y = 0
```

```
x = -y
```

therefore the solution of this linear system
[x y]^T = [-t t]^T forall t in `R`

infinitely many solutions ^

```
x + 2y = 0
-2x - 4y = 3
```

```
2x + 4y = 0
-2x - 4y = 3
```

```
0 = 3 \#
```

contradiction \therefore this linear system has no solution. 

such a linear system is s.t.b. (said to be) inconsistent.
the reverse is true; a system w/ solutions is s.t.b. consistent.

## Geometric Interpretation

The solution of a system of `n` linear equations in 2 variables x and y
is equivalent to
The intersection of `n` lines in the (x y) plane.

when given more equations (or lines), all must intersect at a single point.
this is equivalent to satisfying all 3 equations.

### Ex - `n` = 3

```
x - y + z = 4
2x+2y     = 0
5x+2y +3z = 9
```
replace R2 with R2 - 2R1
```
x - y + z = 4
0x+4y -2z = -8
5x+2y +3z = 9
```
R3 -= 5R1
```
x - y + z = 4
0x+4y -2z = -8
7x+0y -2z = -11
```
R2 /= 4
```
x - y + z = 4
0x+ y-0.5z= -2
7x+0y -2z = -11
```
R1 += R2
```
x +0y+0.5z = 2
0x+ y-0.5z = -2
7x+0y -2z = -11
```
R3 -= 7R2
```
x +0y+0.5z = 2
0x+ y-0.5z = -2
0x+0y+3/2z = -3
```
R3 *= 2/3
```
 x+0y+0.5z = 2
0x+ y-0.5z = -2
0x+0y+   z = 2
```
R2 += 0.5R3
R1 -= 0.5R3
```
 x+0y+  0z = 1
0x+ y+  0z = -1
0x+0y+   z = 2
```
[x y z]^T = [1 -1 2]^T
is the unique solution of this linear system.

### Ex

```
 x +  y +  z = 0
3x -  y      = 1
4x      +  z = 2
```
```
 x +  y +  z = 0
0x - 4y - 3z = 1
0x - 4y - 3z = 2
```
contradiction R2 - R3:
```
0 = -1 \#
```

