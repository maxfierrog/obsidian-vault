**Monday Nov 14, 2022** #math #analysis 

---

### Requires

1. [[Homogenous Second Order Linear Ordinary Differential Equations]]

---

### Objective

Find solutions to $ay'' + by' + cy = g(x)$ when $g(x) \neq 0$, which is the non-homogenous case of a second order linear differential equation. 

---

### Associated Homogenous Problem

Assume $y_p$ is a fixed particular solution to $ay_p'' + by_p' + cy_p = g(x)$. Assume $y$ is another such solution. It then follows that $ay'' + by' + c = g(x)$ and $ay_p'' + by_p' + c = g(x)$ by construction. We then consider $y_h = y - y_b$, which provides
$$
\begin{align*}
ay_h'' + by_h' + c & = a(y - yp)'' + b(y - y_p)' + c \\
& = (ay'' + by' + c) - (ay_p'' + by_p' + c) \\
& = g(x) - g(x) \\
& = 0.
\end{align*}
$$
This shows that $y_h$ is a solution to the associated homogenous problem (often called complementary problem) $ag'' + bg' + cg = 0$.

##### Significance

This implies that if $y_p$ is a fixed particular solution to $ay'' + by' +cy = g(x)$, then $y_a = y_c + y_b$ is a **general** solution to $ay'' + by' +cy = g(x)$, where $y_c$ is a general solution to the associated homogenous problem $ag'' + bg' + cg = 0$.

---

### Strategy

Therefore, to find a general solution to $ay'' + by' +cy = g(x)$, we employ the following strategy:

1. Find a general solution $y_h$ to the associated homogenous problem $ay'' + by' +cy = 0$.
2. Find any particular $y_p$ solution to $ay'' + by' +cy = g(x)$.
3. Obtain a general solution $y = y_h + y_p$ to the problem $ay'' + by' +cy = g(x)$.

---

### Finding Particular Solutions

To find a particular solution to $ay'' + by' +cy = g(x)$, we consider that derivatives of exponential, trigonometric, and polynomial functions are also functions of the same class. So heuristically, if $g(x)$ is a combination of such functions, we should search for a particular solution $y_p$ of the same form.

##### Basic Example

For $y'' - 5y' + 6y = 2xe^x$, we have that $g(x)$ is a combination of a linear polynomial and an exponential. This motivates us to try the following in order to find a particular solution $y_p$:

$y_p = (Ax + B)e^x$
$y_p' = (Ax + A + B)e^x$
$y_p'' = (Ax + 2A + B)e^x$

$\implies y_p'' - 5y_p' + 6y_p = (2Ax - 3A + 2B)e^x = 2xe^x$
$\implies A = 1, \; B = \frac{3}{2}$
$\implies y_p = (x + \frac{3}{2})e^x$.

##### For $g(x) = P_m(x)e^{kx}$

To find a particular solution to $ay'' + by' + cy = P_m(x)e^{kx}$, where $P_m(x)$ is a polynomial of degree $m$, we try the above process with $y_p = x^s(A_0 + A_1x + \cdots + A_mx^m)e^{kx}$, where:

1. $s = 0$ if $k$ is not a solution to $ar^2 + br + c = 0$
2. $s = 1$ if $k$ is a non-repeated solution to $ar^2 + br + c = 0$
3. $s = 2$ if $k$ is a repeated solution to $ar^2 + br + c = 0$ 

... https://www.youtube.com/watch?v=8-i9DTFlmQc&t=2s&ab_channel=AlexanderPaulin


