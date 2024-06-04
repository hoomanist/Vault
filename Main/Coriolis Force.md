Tags: #classicalmechanics

# Coriolis Force
Consider two frames of reference. one of them is rotating with respect to other one and that one is an [[inertial frame]]. suppose the angular velocity of the rotating frame is $\omega$, there is a fictitious force acting on objects that are in motion with respect to the rotating frame named Coriolis Force which is given by: $$F_{coriolis} = -2m(\vec{\omega} \times \vec{v^{\prime}})$$
where $\vec{v^\prime}$ is velocity of object with respect to the rotating reference frame.

### Derivation

we denote the fixed frame with basis vectors ${\hat{i}^\prime, \hat{j}^\prime, \hat{k}^\prime}$ and the rotating frame with ${\hat{i}, \hat{j}, \hat{k}}$. as basis vectors of rotating frame are rotating with angular velocity $\omega$ we can have calculate time derivative of these basis vectors: $\frac{d \hat{i}}{dt} = \omega \times \hat{i}$ and same for $\hat{j}$ and $\hat{k}$.
now if $R$ is Coordinate Vector in fixed frame and $r$ is Coordinate Vector in rotating frame we can say: $$R = R_0 + r$$where $R_0$ is Coordinate Vector of rotating coordinate system with respect to the fixed frame and by differentiating it we have:
$$\displaylines{\frac{dR}{dt} = \frac{dR_0}{dt} + \frac{dx}{dt}\hat{i}+ \frac{dy}{dt}\hat{j}+ \frac{dz}{dt}\hat{k} + x\frac{d\hat{i}}{dt}+ y\frac{d\hat{j}}{dt}+ z\frac{d\hat{k}}{dt}\\=v+\vec{\omega}\times R_0 + x\vec{\omega}\times\hat{i}+ y\vec{\omega}\times\hat{j}+ z\vec{\omega}\times\hat{k}\\=v+\vec{\omega}\times R_0 + \vec{\omega}\times r = v + \vec{\omega}\times R}$$
 and by differentiating again we can have our acceleration:
 $$
 \displaylines{
 \frac{d^2R}{dt^2} = \frac{d}{dt}(v + \vec{\omega}\times R)= \frac{d}{dt}(\frac{dx}{dt}\hat{i}+\frac{dy}{dt}\hat{j}+\frac{dz}{dt}\hat{k}+\vec{\omega}\times R)
 \\=\vec{a} +\frac{dx}{dt}(\vec{\omega}\times\hat{i})+\frac{dy}{dt}(\vec{\omega}\times\hat{j})+\frac{dz}{dt}(\vec{\omega}\times\hat{k})
 \\=\vec{a}+2\vec{\omega}\times \vec{v} + \vec{\omega}\times (\vec{\omega}\times R) 
 }
 $$
 where the second part is the coriolis acceleration which by Newton's Second Law we can turn into Coriolis Force.
---
# References

- R.A.Admas, Calculus: A Complete Course, Section 11.2
- [Coriolis force](https://en.wikipedia.org/wiki/Coriolis_force)

---
در سنه 2024/04/28 میلادی مرقوم فرمودیم