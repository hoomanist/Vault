Tags: #Analysis

---
**lemma**: *let $A$ be a countable set, it's [[Lebesgue Measure]], $\lambda(A)$ is zero.* 
**proof**: first we prove that for any $a \in \mathbb{R}$, $\lambda(\{a\}) = 0$ as following:
- $\{a\} \subset [a-\epsilon, a+\epsilon]$, for any $\epsilon$.
- we know that if $A \subset B$ then $\lambda(A) \le \lambda(B)$. therefore $\lambda(\{a\}) \le 2\epsilon$.
- as we chose an arbitrary $\epsilon$ we deduce $\lambda(\{a\}) = 0$.
then we extend this fact to infinite countable sets through the following argument:
$$A = \bigcup_{i \in \mathbb{N}}\{a_i\} \Rightarrow \lambda(A) \le \sum_{i=1}^\infty \lambda({a_i}) = 0$$
and as a measure is ought to be non-negetive we conclude the lemma.

---
**definition**: *let $1_A(x)$ be an indicator function defined such that if $x = A$ it returns 1 otherwise it is equal to zero.*
we can integrate our indicator function with respect to an arbitrary function $P$ that is defined and continous over the limits of integration:
$$\int_X 1_A dP = \int_AdP = P(A)$$
**remark**: [[dirac's delta function]] can act as an indicator function: $1_A(x) = \delta(x-A)$

---
we define an indicator function $1_\mathbb{Q}(x)$ that is equal to 1 if $x \in \mathbb{Q}$. now we integrate it over the real line with respect to our lebesgue measure $\lambda$
$$\int_\mathbb{R}1_\mathbb{Q}d\lambda = \lambda(\mathbb{Q})$$
and as we know that the [[rationals are countable]] by our lemma we can say our integral is zero.

---
#Todo why can you interperet $\lambda(\mathbb{Q})$ as a probability measure though it is obviously not bounded by 1.

---
# References



---
