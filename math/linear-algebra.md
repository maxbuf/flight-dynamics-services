# Linear algebra

## Linear systems

### Gauss's Method

**(_Definition_) Gauss's Method** A linear combination of $x_{1}, \dots, x_{n}$ has the form

$$a_{1}x_{1} + a_{2}x_{2} + a_{3}x_{3} + \dots + a_{n}x_{n}$$

where the numbers $a_{1}, \dots, a_{n} \in \mathbb{R}$ are the combination's _coefficients_. A _linear equation_ in the variables $x_{1}, \dots, x_{n}$ has the form $a_{1}x_{1} + a_{2}x_{2} + a_{3}x_{3} + \dots + a_{n}x_{n} = d$ where $d \in \mathbb{R}$ is the _constant_.

An n-tuple $(s_{1}, s_{2}, \dots, s_{n}) \in \mathbb{R}$ is a _solution_ of, or _satisfies_, that equation if substituting the numbers $s_{1}, \dots, s_{n}$ for the variables gives a true statement: $a_{1}s_{1} + a_{2}s_{2} + \dots + a_{n}s_{n} = d$. A _system of linear equations_

$$
\begin{aligned}
a_{1,1}x_{1} + a_{1,2}x_{2} + \dots + a_{1,n}x_{n} &= d_{1} \\
a_{2,1}x_{1} + a_{2,2}x_{2} + \dots + a_{2,n}x_{n} &= d_{2} \\
&\vdots \\
a_{m,1}x_{1} + a_{m,2}x_{2} + \dots + a_{m,n}x_{n} &= d_{m}
\end{aligned}
$$

has the solution $(s_{1}, s_{2}, \dots, s_{n})$ if that n-tuple is a solution of all the equations.

Note:

- Finding the set of all solutions is _solving_ the system
- Gauss's Method (or _Gaussian elimination_ or _linear elimination_) always works
- Gauss's Method never loses solutions nor does it ever pick extraneous solutions: A tuple is a solution to the system before we apply the method if and only if it is a solution after

---

**(_Theorem_) Gauss's Method** If a linear system is changed to another by one of these operations

  1. an equation is swapped with another
  2. an equation has both sides multiplied by a **nonzero** constant
  3. an equation is replaced by the sum of itself and a multiple of **another**

then the two systems have the same set of solutions.

**(_Definition_)** The three operations theorem are the _elementary reduction operations_, or _row operations_, or _Gaussian operations_. They are _swapping_, _multiplying by a scalar_ (or _rescaling_), and _row combination_.

Note:

- Abbreviate "row i" by $\rho_{i}$ (this is the Greek letter rho, pronounced aloud as “row”)
- The point of Gauss's Method is to use the elementary reduction operations to set up back-substitution

**(_Definition_)** In each row of a system, the first variable with a nonzero coefficient is the row's leading variable. A system is in _echelon form_ if each leading variable is to the right of the leading variable in the row above it, except for the leading variable in the first row, and any rows with all-zero coefficients are at the bottom.

Note:

- A linear system can fail to have any solution at all (the solution set is empty)
- A linear system can also fail to have a unique solution by having many solutions
- If we reach echelon form without a contradictory equation (e.g., $0 = -3$), and each variable is a leading variable in its row, the system has a unique solution and we find it by back substitution
- If we reach echelon form without a contradictory equation, and there is
not a unique solution (at least one variable is not a leading variable), then the system has many solutions

### Describing the solution set

## Credits

[1] J. Hefferon, *Linear Algebra*, 4th ed. Colchester, VT, USA: Orthogonal Publishing L3C, 2020. [Online]. Available: http://joshua.smcvt.edu/linearalgebra.
