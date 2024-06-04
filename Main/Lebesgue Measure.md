Tags: #Analysis
### What is a measure?
what is length? 19th century mathematicians tried to define length in a rigorous way so they would have methods to integrate special curves like [[Koch's Snowflakes]] or [[weierstrass's function]]. 
they started by listing what characters a notion of length(or area, volume, ...) should have (for $\Omega \subseteq \mathbb{R}^n$):
- possiblity $M(\Omega) = 0$ (e.g. a single point)
- possiblity $M(\Omega) = \infty$ (for when $\Omega = \mathbb{R}^n$)
- $M(\Omega) \ge 0$
- $M(A) \le M(B)$ if $A \subseteq B$
- $M(A)+M(B)$ if $A\cap B = \emptyset$
but it is proven that there is no such function as it's existance would contradict [[Zorn's Lemma]]. so we can only define a measure function for special subsets of $\mathbb{R}^n$ known as "measurable sets". Lebesgue Measure is one of such functions.
---
### properties of measurable sets
the concept of a measurable set by definition should obey following rules:
- (*Borel Property*) Every open set is measurable, as is every closed set
- (Complementarity) If $\Omega$ is measurable then $\mathbb{R}^n - \Omega$ is also measurable
- (Boolean algebra property) if $(\Omega_j)_{j\in J}$ is any finite collection of measurable sets then it's union and intersection are also measurable.
- ($\sigma$-algebra property) if $(\omega_j)_{j\in J}$ are any countable infinite collection of measurable sets then it's union and intersection are also measurable.
---
### Picture of a Lebesgue measure
it is provable that with a concept of measurable set we can define a unique function with following properties:
- $\lambda(\emptyset) = 0$
- $\lambda(\Omega) \in [0, +\infty]$ if $\Omega$ is measurable
- if $A \subseteq B$ and they are both measurable, $\lambda(A) \le \lambda(B)$
- the unit cube $[0, 1]^n = \{ (x_1, \dots, x_n) \in \mathbb{R}^n \}$'s measure is 1
- $\Omega$ is measurable and $x\in \mathbb{R}^n$, then $x + \Omega := \{ x +y : y\in \Omega\}$ is also measurable and $\lambda(x+\Omega) = \lambda(\Omega)$
- $\lambda(\bigcup_j A_j) = \sum_j \lambda(A_j)$
---
### Lebesgue Outer measure
for any closed box $B = \prod_{i=1}^n [a_i, b_i]$ we define volume of our box as:
$$vol(B) = \prod_{i=1}^n(b_i-a_i)$$
now we define that a collection of boxes $(B_j)_{j\in J}$ *covers* $\Omega$ if and only if $\Omega \subseteq \bigcup_{j\in J}B_j$ and $J$ is countable.
armed with this definition we define *outer measure* as:
$$\lambda^*(\Omega) := \inf\{\sum^\infty_{j=1}vol(B_j)\}$$
we can see this definition satisfies every wanted property of lebesgue measure except the last one(additivity).

---
### From Outer measure to Lebesgue Measure Proper
cases that lebesgue outer measure doesn't satisfy addiditivity are rather rare and are constructed as pathological cases using the axiom of choice.
we use a criteration named "Caratheodory criteration"
to distinguish these special cases.
let $E$ be a subset of euclidean n-space if caratheodory criteration hold, the following identity holds for every subset $A$ of $\mathbb{R}^n$:$$\lambda^*(A) = \lambda^*(A\cap E) + \lambda^*(A-E)$$if caratheodory criteration holds then:
$$\lambda(E) = \lambda^*(E)$$
where $\lambda$ is proper lebesgue measure.

---
# References
- [Lebesgue Measue](https://en.wikipedia.org/wiki/Lebesgue_measure)
- Terenece Tao, Analysis II, 1st Edition
---
