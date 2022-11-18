**Monday Nov 14, 2022** #math #analysis

---

### Objective
  
Find solutions to $ay'' + by' + cy = g(x)$. This is the form of a second order linear differential equation. It is homogenous in the case where $g(x)$ is the zero-function, which means we are finding solutions to $ay'' + by' + cy = 0$. 

---

### Linear Independence 

Two functions, $f(x)$ and $g(x)$, are linearly independent only when $f(x) \neq c_1 \cdot g(x) \wedge g(x) \neq c_2 \cdot f(x)$ for any $c_1, c_2$. 

##### Examples

1. The function $f(x) = sin(x)$ is **linearly independent** to $g(x) = cos(x)$ because  $sin(x) = c \cdot cos(x) \implies tan(x) = c$, which necessitates $c$ to be non-constant.

2. The function $f(x) = e^x$ is **linearly dependent** to $g(x) = e^{x + 1}$ because $e^x = e^1 \cdot e^x \implies e = c$.

3. The functions $f(x) = e^{r_1x}$ and $g(x) = e^{r_2x}$ are **linearly independent** when $r_1 \neq r_2$ because, without loss of generality, $e^{r_1x} = c \cdot e^{r_2x} \implies c = e^{(r_1 - r_2)x}$, which is non-constant. ^fe2a2f

---

### Lemma 1

If $y_1, y_2$ are linearly independent solutions to $ay'' + by' + cy = 0$, then a general solution is $y(x) = c_1y_1(x) + c_2y_2(x)$.

##### Significance

To find a general solution to $ay'' + by' + cy = g(x)$, it will suffice to find two linearly independent solutions.

##### Example

To find a solution for $y'' - 3y' + 2y = 0$, consider solutions of the form $y = e^{rx}$.

$y = e^{rx}$ 
$\iff r^2e^{rx} - 3re^{rx} + 2e^{rx} = 0$ 
$\iff e^{rx}(r^2 - 3r + 2) = 0$.

Since $e^{rx} > 0$ for all $x \in \mathbb{R}$, we have that $r^2 - 3r + 2 = 0 \iff r = 1$ or $r = 2$. Because we have found two possible solutions of the form $y = e^{rx}$ (which we showed are linearly independent), a general solution is $y(x) = c_1 \cdot e^{x} + c_2 \cdot e^{2x}$.

##### Significance

When considering solutions of the form $y = e^{rx}$, can see that finding solutions to $ay'' + by' + cy = 0$ is closely related to finding solutions to $ar^2 + br + c = 0$ by the chain rule. In the case above, $r^2 - 3r + 2 = 0$ is called the 'characteristic' or 'auxiliary' equation of $y'' - 3y' + 2y = 0$. 

---

### Conclusion

To find solutions to homogenous second order differential equations of the form $ay'' + by' + cy = 0$ we consider the following cases:

1. If $ar^2 + br + c = 0$ has **two real solutions** $r_1$ and $r_2$, then a general solution to $ay'' + by' + cy = 0$ is $y(x) = c_1e^{r_1x} + c_2e^{r_2x}$, where $c_1, c_2 \in \mathbb{R}$.

2. If $ar^2 + br + c = 0$ has **a single real solution** $r_1$, then a general solution to $ay'' + by' + cy = 0$ is $y(x) = c_1e^{r_1x} + c_2xe^{r_1x}$, where $c_1, c_2 \in \mathbb{R}$.

3. If $ar^2 + br + c = 0$ has **non-real solutions** $a \pm bi$ (e.g. $a = 1$, $b = 0$, and $c = 1$), then a general solution to $ay'' + by' + cy = 0$ is $y(x) = c_1e^{ax}cos(bx) + c_2e^{ax}sin(bx)$, where $c_1, c_2 \in \mathbb{R}$.
