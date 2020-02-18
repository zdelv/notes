% Lecture 2020-02-17

### 3.7 Mechanical and Electrical Vibrations

#### Vibration Equation
We seek to understand the solutions for the following equation, which describes the movement of a vibrating mass on a spring, or other similar actions:
$$
    mu''+\gamma u'+ku=F(t)
$$

##### Undampted Free Vibrations
$F(t)=0$ (no external force applied) and the mass is undamped, meaning $\gamma=0$

The equation above then reduces to the following:

$$
    mu''+ku=0
$$

and has a characteristic equation of the following form:

$$
    mr^2 + k = 0
$$

with roots $r=\plusmn \sqrt{k/m}$. Thus the general solution is the following:

$$
    u = A\cos(\omega_0 t) + B\sin(\omega_0 t)
$$

where $\omega_0 = \sqrt{k/m}$. If the initial conditions for the mass are given, the values for $A$ and $B$ can be found. 

We also wish to analyze this solution further by comparing it to the following equation:

$$
    u = R\cos(\delta)\cos(\omega_0 t) + R\sin(\delta)\sin(\omega_0 t)
$$

This equation was created with the following transformations:

$$
    \begin{aligned}
    A &= R\cos(\delta) \\
    B &= R\sin(\delta) \\
    \space \\
    R &= \sqrt{A^2 + B^2} \\
    \tan(\delta) &= \frac{B}{A}
    \end{aligned}
$$



From the above equations, we find that the **period** of the motion is:
$$
    T=\frac{2\pi}{\omega_0}
$$

$\omega_0$ is the circular frequency, $R$ is the maximum displacement and the amplitude of the wave, and $\delta$ is the phase, or the offset of the wave from its natural position (eg offset from $0\degree$)

##### Damped Free Vibrations
Vibration equation without any applied force, $F(t)=0$
$$
    mu''+\gamma u'+ku = 0
$$

$$
    r_1,r_2=\frac{-\gamma \plusmn \sqrt{\gamma^2-4km}}{2m} \space (\text{Quadratic})
$$

The solution for $u$ has one of the following forms given the above determinant:
$$
    \begin{aligned}
    \gamma^2-4km>0,&\space u=Ae^{r_1t}+Be^{r_2t}\\
    \gamma^2-4km=0,&\space u=(A+B)e^{-\gamma t/2m}\\
    \gamma^2-4km<0,&\space u=e^{-\gamma t/2m}(A\cos(\mu t)+B\sin(\mu t)) \\
                    &\mu=\frac{1}{2m}(4km-\gamma^2)^{1/2} > 0
    \end{aligned}
$$


###### Example 1
Find the general solution of the following problem:

$$
    u'' + 2u' + 5u = 0, \space u(0)=1, \space u'(0)=1
$$

We first find the roots:

$$
    r^2 + 2r + 5 = 0
$$

$$
    \begin{aligned}
    r_1,r_2=\frac{-2 \plusmn \sqrt{2^2-4(1\cdot5)}}{2\cdot1}
    \end{aligned}
$$

$$
    \gamma = -1 \plusmn 2i
$$

Plugging these into our general form for the 2nd order differential equation with non-real roots, we get the following 


---

NEVER FINISHED EXAMPLE

---


### 3.8 Force Periodic Vibrations


###### Example 3

$$
    u''+\omega^2u=F_0\cos(\omega t)
$$

We first find the complementary solution, which is given by the following equations:
$$
    \begin{matrix}
    r^2+\omega^2r = 0 \\
    r_1,r_2 =\frac{-\omega^2 \plusmn \sqrt{(\omega^2)^2-4(1\cdot0})}{2\cdot1}
    \end{matrix}
$$
$$
    u_c = C_1\cos(\omega_0 t) + C_2\sin(\omega_0 t)
$$

**Case 1**: When $\omega \not= \omega_0$

Particular Solution:
$$
    \begin{aligned}
    u_p&=A\cos(\omega t) + B\sin(\omega t) \\
    u''_p&=-A\omega^2\cos(\omega t)-B\omega^2\sin(\omega t)
    \end{aligned}
$$

Plug Particular + Derivatives into the Complementary
$$
    \begin{aligned}
    F_0\cos(\omega t)&=u''+\omega^2u \\
    F_0\cos(\omega t)&=(-A\omega^2\cos(\omega t)-B\omega^2\sin(\omega t))+\omega^2(A\cos(\omega t) + B\sin(\omega t))\\
    F_0\cos(\omega t)&=A(\omega_0^2-\omega^2)\cos(\omega t) + B(\omega_0^2-\omega^2)\sin(\omega t)
    \end{aligned}
$$

Solve for $A$ and $B$ by comparing the coefficents on both sides of the equation:

$$
    \begin{aligned}
    \cos(\omega t):&\space A(\omega_0^2-\omega^2)=F_0 \\
    \sin(\omega t):&\space B(\omega_0^2 - \omega^2)=0 \\
    \end{aligned}
$$

$$
    \begin{aligned}
    A &= \frac{F_0}{\omega_0^2-\omega^2} \\
    B &= 0 
    \end{aligned}
$$

With $A$ and $B$ solved for, we now have the particular solution:

$$
    u_p = \frac{F_0}{\omega_0^2-\omega^2}\cos(\omega t)
$$

Add the particular solution to the complementary solution to get the general solution

$$
    u = C_1\cos(\omega_0 t) + C_2\sin(\omega_0 t) + \frac{F_0}{\omega_0^2-\omega^2}\cos(\omega t)
$$

If we assume $u(0)=0$, $u'(0)=0$, then we can solve for $C_n$:

$$
    \begin{aligned}
    C_1 &= -\frac{F_0}{\omega_0^2-\omega^2} \\
    C_2 &= 0 \\
    \end{aligned}
$$

$$
    \begin{aligned}
    u &= \frac{F_0}{\omega_0^2-\omega^2}(\cos(\omega t) - \cos(\omega_0 t)) \\
      &= \frac{2F_0}{\omega_0^2-\omega^2}\cdot\sin(\frac{\omega_0+\omega}{2}t)\cdot\sin(\frac{\omega_0-\omega}{2}t)
    \end{aligned}
$$