Tags: #classicalmechanics 
### Introduction
Drag Force is a force caused by interaction of an object with a fluid which is usually in opposite direction of object's velocity (although not always as in the case with airplane lift). it has two categories:
 - *Linear Drag*: which is caused by [[viscousity]] of our fluid and is proportional to object's velocity.
 - Quadratic Drag: it is the result of acceleration of fluid molecules sorrounding our object and terbulance in fluid's flow. and it is proportional to square of object's velocity.
we can define a number known as [[Reynolds number]] which indicates whether Linear Drag is Dominant or Quadratic Drag:$$R_e  = \frac{\rho v L}{\mu}$$
if this number is large it means that Quadratic Term is much larger so we can ignore linear force and vice versa.
### Horizontal motion with Quadratic Drag
suppose some object is moving along $x$ axis with an initial velocity and no force effecting it except Drag Force. by using newton's second law we'll have:$$m\frac{dv}{dt} = - Cv^2$$ where $C$ is a constant. we can use seperation of variables on it:
$$m\int^v_{v_0}\frac{dv^\prime}{{v^\prime}^2} = -C\int^t_0dt $$
so we can write $v(t)$ as:
$$v(t) = \frac{v_0}{1+\frac{Cv_0t}{m}}$$
here $\frac{m}{Cv_0}$ is special time denoted by $\tau$ and represents the time where our velocity is half of initial velocity. also by integration we can find $x(t)$$$x(t) = x_0 + \int^t_0v(t^\prime)dt^\prime = v_0\tau\ln(1 +t/\tau)$$
### Vertical motion with Quadratic Drag
now suppose our motion is a free fall with an initial velocity and also a Drag Force. newton's second law gives us:
$$m\frac{dv}{dt} = mg - Cv^2$$
before solving it let's consider terminal velocity($v_{ter}$) which is the velocity where two terms on the right balance out and our velocity remains constant:
$$v_{ter} = \sqrt{\frac{mg}{C}}$$
now we can rewrite our differential equation as following:
$$\dot{v}=g(1-\frac{v^2}{v_{ter}^2})$$
and by using seperation of variables we reach:
$$\frac{v_{ter}}{g}\tanh^{-1}{(\frac{v}{v_{ter}})} = t$$
this solved for $v$:$$v = v_{ter}\tanh{(\frac{gt}{v_{ter}})}$$
you can also integerate to get $y(t)$
### Horizontal and Vertical Motion in Quadratic Drag
equation of motion for a projectile subject to Quadratic Drag is:
$$m\mathbf{\dot{v}} = m\mathbf{g} - cv^2\mathbf{\hat{v}}$$
resolving this into it's horizontal and vertical components:
$$\begin{cases}
m\dot{v}_x = -cv_x\sqrt{v_x^2+v_y^2} \\
m\dot{v}_y = -mg - cv_y\sqrt{v_x^2+v_y^2}
\end{cases}
$$
this is a system of coupled differential equations because both equations are dependent on our unknown functions. 
our problem is that this systems is proven be unsolvable analytically. meaning we can only approximate it numerically(e.g. with NDSolve in Mathematica).