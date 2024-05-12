Tags: #MathematicalPhysics


# Laplace Transform

### 1- Integral Transforms
pair of functions can be related through an integral in following form:
$$G(\alpha) = \int^b_a K(\alpha,s)F(s)ds$$
and we say is $G(\alpha)$ is the integral Transform of $F(s)$ with Kernel $K(\alpha,s)$. this operation is a mapping of a function in $s$-space to one in $\alpha$-space. for example in [[Qunatum Mechanics]] we use an integral transform to map a wave function in position space to one in momentum space(1).
### 2- Laplace Transform
we define a laplace transform as follows:
$$\mathcal{L}\{f(t)\} = \int_0^\infty e^{-st}f(t)dt$$
it turns a real-valued function in time-domain into a complex valued function in frequency domain. it means that instead of showing particular value of a function with respect to a variable, it shows how a value is distributed across a variety of frequencies(2).
laplace transform is analogous to a power series(3). suppose we have a function $f(x)$ that can be expanded to a power series:
$$
f(x) = \sum_n a_nx^n
$$
now what if we extend this summation to be continous;
$$
f(x) = \int a(t)x^tdt
$$
and if we arbitrary choose x to be equal to $e^{-s}$ we'll arrive at laplace transform.
### 3- Relation to Fourier Transform
Fourier Transform gives us frequencies of sinusoids that comprise a function. meaning that if we have a function f:
$$F(\omega) = \mathcal{F}\{f(t)\} = \int^\infty_0f(t)e^{-i \omega t}dt $$
$F(\omega)$ gives frequencies of the infinite number of sinusoids that will add up to the original function. now if we make a change in variables in the laplace transform what will we have?(4)
suppose that $s = \alpha + i\omega$ then:

$$\mathcal{L}\{f(t)\} = \int^\infty_0f(t)e^{(\alpha + i\omega)t}dt = \mathcal{F}\{f(t)e^{\alpha t}\}$$
now if we calculate this for a function we will have some poles. some infinitly long spikes in the graph. if we say $z$ is a point where $\mathcal{L}\{f(z)\} = 0$ , then the real part of $z$ is the power of an exponential and it's imaginary part is frequency of the sinusoide that comprise the original function.
if the region of convergence(to the right of axis of the poles) contains imaginary axis we can calculate the fourier transform from our laplace transform.
### 4- Applications
 0oouhutfrt
**Evaluating Improper Integrals**
let $\mathcal{L}\{f(t)\} = F(s)$
$$
\partial_s\mathcal{L}\{\frac{f(t)}{t}\} = \partial_s\int_0^\infty\frac{f(t)}{t}e^{-st}dt = - F(s)
$$
so
$$
\mathcal{L}\{\frac{f(t)}{t}\} =\int^\infty_0e^{-st}\frac{f(t)}{t}dt= \int^\infty_sF(s^\prime)ds^\prime
$$
and by taking the limit $s \to 0$ we have:
$$
\int^\infty_0\frac{f(t)}{t}dt= \int^\infty_0F(s^\prime)ds^\prime
$$
which can be used to calculate many integral, most famously [[Dirichlet Integral]]($sin(t)/t$)(5).
**Partition Function**
[[Partition Function]] is a function of temperature that encodes how probability is distributed between different [[microstates]](6). it is the normalizing factor of probabilities of different energy levels of microstates:$$\sum_{s}P_s= \sum_s\frac{1}{Z}e^{-\beta E_S}=1$$
where $Z$ is the partition function and $\beta=\frac{1}{k_bT}$. therefore:
$$Z = \sum_ie^{-\beta E_i}$$
the partition function is also defined as the laplace transform of density of states function taking it from energy domain to $\beta$ domain. density of states function is number of microstates with a specific energy level defined as following:
$$
g(E) = \int^\infty_0\delta(E^\prime(x) - E)dx
$$
where $\delta$ is [[dirac's delta function]] and $E^\prime$ gives the energy content of a specific microstate(it's basicly summing over number of microstates that have energy content equal to a given energy level)(7). so the partition function is:
$$
Z(\beta) = \mathcal{L}\{ g(E) \}= \int_0^\infty e^{-\beta E}g(E)dE
$$
the importance of partition function is the fact that for every [[canonical ensamble]] you can find macroscopic quantities such as pressure or [[entropy]] using it or it's derivatives.

---
# References
- 1- George B. Arfken & others, Mathematical Methods for Physicists: A Comprehensive Guide, 7th Edition - p.963
- 2- [Laplace Transform](https://en.wikipedia.org/wiki/Laplace_transform)
- 3- [What is the physical meaning of a laplace transform](https://physics.stackexchange.com/questions/300309/what-is-the-physical-meaning-of-a-laplace-transform)
- 4- [What does the Laplace Transform really tell us?](https://www.youtube.com/watch?v=n2y7n6jw5d0&t=22s)
- 5- [Dirichlet integral#Laplace Transform](https://en.wikipedia.org/wiki/Dirichlet_integral#Laplace_transform)
- 6- [Partition Function#meaning and significance](https://en.wikipedia.org/wiki/Partition_function_(statistical_mechanics)#Meaning_and_significance)
- 7- R.K.Pathria, Statistical Mechanics, 4th Edition - p.53
---
