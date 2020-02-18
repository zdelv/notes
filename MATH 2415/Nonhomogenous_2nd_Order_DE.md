% Nonhomogenous 2nd Order Differential Equations

An equation in the form below is what is called a **nonhomogenous** 2nd order linear differential equation:

(1)
$$
    L[y] = y'' + p(t)y' + q(t)y = g(t)
$$

where $p(t)$, $q(t)$, and $g(t)$ are all continous functions on the interval $I$.

For the equation above, if it is written where $g(t)=0$, for all t, then this equation is the **homogenous** form for the given nonhomogenous differential equation:

(2)
$$
    L[y] = y'' + p(t)y' + q(t)y = 0
$$

We also know given our knowledge of linear systems of equations, that if $Y_1$ and $Y_2$ are solutions to the nonhomogenous linear differential equation (1), then their difference $Y_1 - Y_2$ is a solution to the corresponding linear system of equation (2). In addition, we also know that $Y_1 - Y_2 = c_1y_1(t)+c_2y_2(t)$, given that $y_1$ and $y_2$ form the fundamental set of solutions for equation (2).

Given in other words, the previous paragraph describes that the nonhomogenous equation can directly relate to the homogenous equation and its solutions through simple linear combonations of their solutions. If you have two solutions to the nonhomogenous differential equation, then you can find the fundamental solution to the corresponding homogenous differential equation.

The general (fundamental) solution to the nonhomogenous differential equation (1) is the following:

$$ 
    y = \phi(t) = c_1y_1(t)+c_2y_2(t) + Y(t)
$$
where $y_1$ and $y_2$ form the fundamental set of solutions for the corresponding homogenous equation (2), $c_n$ are arbitrary constants, and $Y(t)$ is any solution to the nonhomogenous equation (1).

----

#### Summary of the above

With all of the work described above, we arrive at the general way we solve nonhomogenous differential equations in the form of equation (1):

1. Find the general solution $c_1y_1 + c_2y_2$ of the corresponding homogenous equation (2). This solution is called the **complementary solution**, denoted as $y_c(t)$.
2. Find any solution $Y(t)$ of the nonhomogenous equation (1). This solution is called the **particular solution**.
3. Form the sum of the functions from 1 and 2 to satsify the general form written above

The ways of finding $y_c(t)$ are general with the way to solve homogenous equations, so that will not be discussed here. Instead, we focus on the nonhomogenous solution, step 2.

----


## 2. Finding the nonhomogenous solution, $Y(t)$

The two methods for finding nonhomogenous solutions mentioned here are the following:
   
1. The method of undetermined coefficients (Section 3.5)
2. The method of variation of parameters (Section 3.6)

### The Method of Undetermined Coefficents

The method of undetermined coefficents is mostly a "guess-and-check" type of solution, where to find $Y(t)$, we make an assumption on the general form for $Y(t)$ and leave the coefficents unspecified. We then substitute this $Y(t)$ into the given nonhomogenous equation in the form of equation (1) and attempt to determine the coefficents that satisfy the equation. If we cannot find coefficents that satisfy the equation, then we must find a new general form for $Y(t)$ and try again.

This method uses mostly brute force and domain knowledge to find a solution, so it's restricted to equations that have relatively simple makeup.


---


##### Example:
Find a particular solution of:

(3)
$$
    y'' - 3y' - 4y = 3e^{2t}
$$

The $Y(t)$ we choose to start with is an exponential, as this is a common form for generic $y^{(n)} = g(t)$ differential equations. We can also notice that taking the derivative of equation (3) returns an exponential each time, which should clue us into what the $Y(t)$ form looks like.

(4)
$$
    Y(t) = Ae^{2t}
$$

Equation (4) is then subtituted into Equation (3), given the following:

$$
    Y'(t) = 2Ae^{2t}, \space \space Y''(t) = 4Ae^{2t}
$$

The obtained equation after substituing the given differentials in is the following:

$$
    \begin{aligned}
    Y''-3Y'-4Y &= 3e^{2t} \\
    (4A-6A-4A)e^{2t}&=3e^{2t} \\
    -6Ae^{2t} &= 3e^{2t}
    \end{aligned}
$$

Given the above equation, we can notice that the only value for A that satisfies it is when $A = -\frac{1}{2}$, therefore the following solution is achieved:

$$
    Y(t) = -\frac{1}{2}e^{2t}
$$


----


#### Summary

To solve a nonhomogenous 2nd order differential equation in the form of equation (1), complete the following steps:

1. Find the general solution to the corresponding homogenous differential equation in the form of equation (2)
2. Ensure that the equation has only sinusoidal functions, exponentials, polynomials, or any sums or products of the preceeding functions. If not, then use the method of variation of parameters.
3. If $g(t)$ can be split into $n$ individual terms - or written as $\sum{g_n(t)}$ - split the problem into $n$ subproblems, each of which have the following form:
$$
    ay'' + by' + cy = g_i(t)
$$
where $i$ runs from 1 to $n$.
4. Assume $Y(t)$ has the equivalent general form for the $g(t)$ given, following Table 4 below:
5. If $Y(t)$ is the same as the solution to the homogenous differential equation, then add an extra $t$ term to $Y(t)$. If this does not fix the error, raise the power of the $t$ term added (eg $t^n \rightarrow t^{n+1}$)
6. If the problem was split into subproblems, solve for each $Y_i(t)$ and add them together to form the particular solution to the nonhomogenous equation.
7. Given your particular solution, $Y(t)$, and the solution to the homogenous equation, $c_1y_1 + c_2y_2$, form the nonhomogenous general solution:
$$
    \phi(t) = c_1y_1 + c_2y_2 + Y(t)
$$
8. Any remaining arbitrary constants can now be solved for using the initial conditions provided.


Table 4:

| $g(t)$ Form | $Y(t)$ Guess |
|---|---|
|$cos(t)$ or $sin(t)$ | $Acos(t)+Bsin(t)$ |
| $e^t$  | $Ae^{t}$ |
|  $\sum{t^n}$ |  $\sum{c_nt^n}$ |