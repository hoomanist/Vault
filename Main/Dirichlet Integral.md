### 1. the integral and it's integrablity
dirichlet integral is an improper integral of form:
$$\int^\infty_0\frac{sin x}{x}dx = \frac{\pi}{2}$$
it's not absolutely convergent so $|\frac{sin x}{x}|$ isn't convergent therefore it's not in sense of [[lebesgue integral]] integrable but is [[riemann integrable]].
### 2. solving with feynman's trick
we write our integral as a new function:
$$f(s) = \int_0^\infty \frac{sin t}{t}e^{-st}dt$$
then we calculate it's derivative:
$$\frac{df}{ds}=\int^\infty_0\partial_se^{-st}\frac{sint}{t}dt = -\int^\infty_0sin(t)e^{-st}dt = -\frac{1}{1+s^2}$$
then by integrating with respect to s we'll have:
$$
f(s) = A - tan^{-1}(s)
$$
where we can find $A$ by finding the limit of $f(s)$ as $s$ approches infinity:
$$
\lim_{s\to\infty}f(s) = A -\lim_{s\to\infty} tan^{-1}(s) = 0 \Rightarrow A = \lim_{s\to\infty} tan^{-1}(s) = \frac{\pi}{2}
$$
and by setting s = 0 we'll have the original integral recovered:
$$
f(0) = \int^\infty_0\frac{\sin t}{t}dt = \frac{\pi}{2} - \tan^{-1}(0) = \frac{\pi}{2}
$$
### 3. by using [[laplace transform]]
$$
\int_0^\infty \frac{\sin t}{t}dt = \lim_{s\to0} \int^\infty_s \mathcal{L}\{\sin t\}dt = \lim_{s\to0}\int^\infty_s\frac{dt}{1+t^2} = \frac{\pi}{2}
$$