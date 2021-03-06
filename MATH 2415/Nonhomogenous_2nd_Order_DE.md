<meta charset="utf-8">
<meta name="theme-color" content="#141518" />
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black">
<link href="https://fonts.googleapis.com/css?family=IBM+Plex+Mono|Roboto|Roboto+Mono" rel="stylesheet">
<link rel="stylesheet" href="../markdeep-style.css">

**Nonhomogenous 2nd Order Differential Equations**

# Nonhomogenous 2nd Order Differential Equations

An equation in the form below is what is called a **nonhomogenous** 2nd order linear differential equation:

$$
    \begin{equation}
    L[y] = y'' + p(t)y' + q(t)y = g(t)
    \end{equation}
$$

where $p(t)$, $q(t)$, and $g(t)$ are all continous functions on the interval $I$.

For the equation above, if it is written where $g(t)=0$, for all t, then this equation is the **homogenous** form for the given nonhomogenous differential equation:

$$
    \begin{equation}
    L[y] = y'' + p(t)y' + q(t)y = 0
    \end{equation}
$$

We also know given our knowledge of linear systems of equations, that if $Y_1$ and $Y_2$ are solutions to the nonhomogenous linear differential equation (1), then their difference $Y_1 - Y_2$ is a solution to the corresponding linear system of equation (2). In addition, we also know that $Y_1 - Y_2 = c_1y_1(t)+c_2y_2(t)$, given that $y_1$ and $y_2$ form the fundamental set of solutions for equation (2).

Given in other words, the previous paragraph describes that the nonhomogenous equation can directly relate to the homogenous equation and its solutions through simple linear combinations of their solutions. If you have two solutions to the nonhomogenous differential equation, then you can find the fundamental solution to the corresponding homogenous differential equation.

The general (fundamental) solution to the nonhomogenous differential equation (1) is the following:

$$ 
    y = \phi(t) = c_1y_1(t)+c_2y_2(t) + Y(t)
$$
where $y_1$ and $y_2$ form the fundamental set of solutions for the corresponding homogenous equation (2), $c_n$ are arbitrary constants, and $Y(t)$ is any solution to the nonhomogenous equation (1).

## Summary of the above

With all of the work described above, we arrive at the general way we solve nonhomogenous differential equations in the form of equation (1):

1. Find the general solution $c_1y_1 + c_2y_2$ of the corresponding homogenous equation (2). This solution is called the **complementary solution**, denoted as $y_c(t)$.
2. Find any solution $Y(t)$ of the nonhomogenous equation (1). This solution is called the **particular solution**.
3. Form the sum of the functions from 1 and 2 to satsify the general form written above

The ways of finding $y_c(t)$ are general with the way to solve homogenous equations, so that will not be discussed here. Instead, we focus on the nonhomogenous solution, step 2.

## Finding the nonhomogenous solution, $Y(t)$

The two methods for finding nonhomogenous solutions mentioned here are the following:
   
1. The method of undetermined coefficients (Section 3.5)
2. The method of variation of parameters (Section 3.6) (Not covered)

### The Method of Undetermined Coefficents

The method of undetermined coefficents is mostly a "guess-and-check" type of solution, where to find $Y(t)$, we make an assumption on the general form for $Y(t)$ and leave the coefficents unspecified. We then substitute this $Y(t)$ into the given **nonhomogenous** equation in the form of equation (1) and attempt to determine the coefficents that satisfy the equation. If we cannot find coefficents that satisfy the equation, then we must find a new general form for $Y(t)$ and try again.

This method uses mostly brute force and domain knowledge to find a solution, so it's restricted to equations that have relatively simple makeup.

!!! example: Example
    Find a particular solution of:

    $$
        \begin{equation}
        y'' - 3y' - 4y = 3e^{2t}
        \end{equation}
    $$

    The $Y(t)$ we choose to start with is an exponential, as this is a common form for generic $y^{(n)} = g(t)$ differential equations. We can also notice that taking the derivative of equation (3) returns an exponential each time, which should clue us into what the $Y(t)$ form looks like.

    $$
        \begin{equation}
        Y(t) = Ae^{2t}
        \end{equation}
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

### The General Cases for 2nd Order Nonhomogenous DEs

Given that the general form for a 2nd Order Nonhomogenous differential equation is the following:

$$
    \begin{equation}
    ay'' + by' + cy = g(t)
    \end{equation}
$$

and that the characteristic equation has the following form:

$$
    \begin{equation}
    ar^2 + br + c = 0
    \end{equation}
$$

We discuss below three possible cases for the form of the **particular** solution for the DE, given that $g(t)$ and the roots, $r_1$ and $r_2$ have certain forms.

!!! case: Case 1: $g(t) = P_n(t)$
   1. When $r_1 \not = r_2$:
        $$
            y_p = A_nt^n + A_{n-1}t^{n-1} + \dots + A_1t + A_0
        $$
   2. When $r_1=0$ OR $r_2=0$:
        $$
            y_p = t(A_nt^n + A_{n-1}t^{n-1} + \dots + A_1t + A_0)
        $$
   3. When $r_1=r_2=0$:
        $$
            y_p = t^2(A_nt^n + A_{n-1}t^{n-1} + \dots + A_1t + A_0)
        $$

!!! example: Example for Case 1
    $$
        y'' - y' = t^2
    $$
    The roots to this equation are given by the characteristic equation (6) above, and are $r_1=0$ and $r_2=1$. Given the roots, we know the two solutions to the homogenous equation are $y_1=0$ and $y_2=e^{rt}$.

    From this, we can arrive at the particular solution:
    $$
        y_p = t(At^2 + Bt + C)
    $$

!!! case: Case 2: $g(t) = e^{\alpha t}P_n(t)$
    1. When $r_1\not = \alpha$ and $r_2\not = \alpha$:
        $$
            y_p = e^{\alpha t}(A_nt^n + \dots + A_0)
        $$
    2. When $r_1= \alpha$ OR $r_2= \alpha$:
        $$
            y_p = te^{\alpha t}(A_nt^n + \dots + A_0)
        $$
    3. When $r_1=r_2=\alpha$:
        $$
            y_p = t^2e^{\alpha t}(A_nt^n + \dots + A_0)
        $$ 

!!! example: Examples for Case 2:
    **Example 1**: 
    $$
        y'' - y' = te^{2t}
    $$
    The roots to the characteristic equation are $r_1=0$ and $r_2=1$. The two solutions are $y_1=1$ and $y_2=e^t$. Given that $\alpha = 2$ we know that neither of our two roots are equal, therefore, case 2.1 applies.
    $$
        y_p = e^{2t}(At + B)
    $$

    **Example 2**:
    $$
        y'' - y' = te^{t}
    $$
    The roots are the same as Example 1 but $\alpha$ is now $1$, therefore $r_2=\alpha$. Case 2.2 applies here and the particular solution is the following:
    $$
        y_p = te^{2t}(At + B)
    $$

    **Example 3**:
    $$
        y'' - 2y' + y = te^t
    $$
    The roots are $r_1=1$ and $r_2=1$. The two solutions to the homogenous equation are $y_1=e^t$ and $y_2=te^t$. There are repeated roots, and both equal $\alpha$, therefore case 2.3 applies:
    $$
        y_p = t^2e^t(At+B)
    $$

    **Example 4**:
    $$
        y'' - 2y' + y = te^{2t}
    $$
    The roots are are the same as Example 3, but $\alpha$ is now $2$. This is the same case as Example 1, case 1.1, therefore the same solution applies:
    $$
        y_p = e^{2t}(At+B)
    $$

!!! case: Case 3 $g(t) = P_n(t)e^{\alpha t}\cos(\beta t)$ OR $g(t) = P_n(t)e^{\alpha t}\sin(\beta t)$
    1. $r \not = \alpha \pm \beta i$
        $$
            y_p = (A_nt^n + \dots + A_0)e^{\alpha t}\cos(\beta t) + (B_nt^n + \dots + B_0)e^{\alpha t}\sin(\beta t)
        $$
    2. $r = \alpha \pm \beta i$
        $$
            y_p = t(A_nt^n + \dots + A_0)e^{\alpha t}\cos(\beta t) + t(B_nt^n + \dots + B_0)e^{\alpha t}\sin(\beta t)
        $$
        

!!! example: Examples for Case 3:
    **Example 1**:
    $$
        y'' - 2y' + 5y = e^t \cos(2t)
    $$
    The roots to the homogenous equation are $r=1 \pm 2i$. Thus, we now know that $\alpha=1$, $\beta=2$ and $\alpha \pm \beta i = 1 \pm 2i = r$. This then means that we use case 3.12for the particular solution:
    $$
        y_p = Ate^t\cos(2t) + Bte^t\sin(2t) 
    $$

    **Example 2**:
    $$
        y'' - 2y' + 5y = e^{2t} \sin(2t)
    $$
    The roots are the same as Example 1, but now $\alpha=2$ and therefore $\alpha \pm \beta i = 2 \pm 2i \not = r$. The case we use is 3.1 and the particular solution is then:
    $$
        y_p = Ae^t\cos(2t) + Be^t\sin(2t) 
    $$

    **Example 3**:
    $$
        y'' - 2y' + 5y = e^t \cos(t)
    $$
    The roots are the same as Examples 1 and 2, but now both $\alpha$ and $\beta$ equal $1$. Therefore $\alpha \pm \beta i = 1 \pm 1i \not = r$. We still use case 3.1 and the particular solution is the following:
    $$
        y_p = Ae^t\cos(t) + Be^t\sin(t)
    $$

    **Example 4**:
    $$
        y'' + y = t\cos(t)
    $$
    The roots to the homogenous equation are $r=\pm i$, $\alpha = 0$, and $\beta = 1$. Therefore $\alpha \pm \beta i = \pm 1i = \pm i = r$. The case we use is case 3.2 and the particular solution is the following:
    $$
        y_p = t\cos(t)(A_1t+A_0) + t\sin(t)(B_1t+B_0)
    $$

    **Example 5**:
    $$
        y'' + y = t\cos(2t)
    $$
    The roots are the same as Example 4, but now $\beta=2$ and therefore $\alpha \pm \beta i = \pm 2i \not = r$. We then use case 3.1 and the particular solution is the following:
    $$
        y_p = \cos(t)(A_1t+A_0) + \sin(t)(B_1t+B_0)
    $$

## Summary

To solve a nonhomogenous 2nd order differential equation in the form of equation (1), complete the following steps:

1. Find the general solution to the corresponding homogenous differential equation in the form of equation (2)
2. Ensure that the equation has only sinusoidal functions, exponentials, polynomials, or any sums or products of the preceeding functions. If not, then use the method of variation of parameters (not covered).
3. Use the above cases explained in section [The General Cases for 2nd Order Nonhomogenous DEs] to find the particular solution.
4. Given your particular solution, $Y(t)$, and the solution to the homogenous equation, $c_1y_1 + c_2y_2$, form the nonhomogenous general solution:
    $$
        y = \phi(t) = c_1y_1 + c_2y_2 + y_p(t)
    $$
5. Any remaining arbitrary constants can now be solved for using the initial conditions provided.

<!-- Markdeep: --><style class="fallback">body{visibility:hidden;white-space:pre;font-family:monospace}</style><script src="markdeep.min.js" charset="utf-8"></script><script src="https://casual-effects.com/markdeep/latest/markdeep.min.js" charset="utf-8"></script><script>window.alreadyProcessedMarkdeep||(document.body.style.visibility="visible")</script>