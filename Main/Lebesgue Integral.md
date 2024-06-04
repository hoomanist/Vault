Tags: #Analysis
### measurable functions
let $\Omega$ be a measurable subset of $\mathbb{R}^n$ and let $f: \Omega \to \mathbb{R}^m$
be a function. a function $f$ is measurable if and only if $f^{-1}(V)$ is measurable for every open set $V \subseteq \mathbb{R}^m$. for $m=n=1$ we can rephrase our definition as $\{x\in X : f(x) > \alpha\}$ is measurable for any $\alpha \in \mathbb{R}$.
these measurable functions are those that can be integrated in sense of Lebesgue measure. Continuous functions, monotone functions, step functions, semicontinuous functions, Riemann-integrable functions, and functions of bounded variation are all Lebesgue measurable.

---
### Simple Functions
we begin our definition of lebesgue integral by considering a special subclass of measurable functions known as simple functions.
$f: \Omega \to \mathbb{R}$ is considered simple if the image $f(\Omega)$ is finite. in other words, there exists a finite number of real numbers $c_1, c_2, \dots, c_N$ such that for every $x \in \Omega$ we have $f(x) = c_i$ for some $1 \le i \le N$

---
### Lebesgue Integral of simple functions
we define lebesgue integral $\int_\Omega f d\lambda$ as: $$\int_\Omega f d\lambda:= \sum_{m\in f(\Omega); m>0}m\lambda(\{x\in\Omega:f(x)=m\})$$
for example if we want to integrate a function $f$ which equals 3 on the interval $[1, 2]$ and 4 on the interval $(2, 4)$ and is zero everywhere else. then $$\int_\Omega fd\lambda = 3\times\lambda([1,2]) + 4\times\lambda((2,4)) = 3 \times 1 + 4 \times 2 = 11$$
this definition comes from the fact that every simple function can be written as a finite sum of indicator functions where $S_k$ are disjoint measurable sets:$$\int (\sum_k a_k 1_{S_k})d\lambda = \sum_ka_k\int 1_{S_k}d\lambda = \sum_ka_k\lambda(S_k)$$

---
### Lebesgue Integral of any measurable function
first we define lebesgue integral for non-negetive functions:$$\int_\Omega f\ d\lambda = \sup\{\int_\Omega s\ d\lambda : 0\le s\le f,\ s \ \text{ is simple}  \}$$
now for signed functions we split positive parts and negetive parts: $$
\begin{align}
f^+(x) &= \begin{cases} f(x)\hphantom{-} & \text{if } f(x) > 0, \\ 0 & \text{otherwise}, \end{cases} \\
f^-(x) &= \begin{cases} -f(x) & \text{if }  f(x) < 0, \\ 0 & \text{otherwise}. \end{cases}
\end{align}$$
now lebesgue integral of $f$ is: $$\int_\Omega f\ d\lambda = \int_\Omega f^+\ d\lambda - \int_\Omega f^-\ d\lambda$$


---
# References



---
