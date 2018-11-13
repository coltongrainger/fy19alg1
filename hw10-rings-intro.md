---
title: Rings
author: Colton Grainger
date: 2018-11-09
bibliography: /home/colton/Downloads/coltongrainger.bib
macros: true
tikz: true
---

\setcounter{section}{9}

## Assignment due 2018-11-14

### [@DF04, number 7.1.7]

\newcommand{\pf}{\emph{Proof.}\ }
\newcommand{\wts}{\emph{To prove.}\ }
\newcommand{\gvn}{\emph{Given.}\ }
\newcommand{\fore}{($\Rightarrow$)\ }
\newcommand{\back}{($\Leftarrow$)\ }

\wts Okay we want to show that for a ring the center the ring is a subring and furthermore that if a ring is a division ring then the center of the ring is a field.

\gvn $R$, a ring; $Z$, the center of $R$.

\pf Let $r \in R$. Let $x,y \in Z$.
Observe that the center is closed under subtraction.
$$r(y-x) = ry - rx = yr - xr = (y-x)r.$$
Observe that a product of elements in the center is also in the center.
$$rxy = xry = xyr.$$
Thus the center is a subring.
\qedsymbol

\gvn Now suppose our ring is a division ring.

\wts $Z$ is a field.

\pf The center is a commutative ring by above. Let $r \in R$. Then there's $a \in R$ such that $a = r^{-1}$. Let $z \in Z$.
$$az = za \Rightarrow (az)^{-1} = (za)^{-1} \Rightarrow z^{-1}r = rz^{-1}.$$ So the center of the ring is closed under inverses. Thus the center is a division ring.
\qedsymbol 


### [@DF04, number 7.1.11]

\gvn Suppose $R$ is an entire ring. Suppose $x \in R$.

\wts If $x^2 = 1$, then $x = \pm 1$.

\pf Consider $x^2 = 1$ if and only if $(x-1)(x+1) = 0$. Since $R$ has no zero divisors, the conclusion follows. \qedsymbol

### [@DF04, number 7.1.14]

\gvn Let $R$ be a commutative ring with unity. Let $x \in R$ be a nilpotent element such that $$m = \min \{ n \in \NN : x^n =0\}.$$

\wts (a) Either $x$ is zero or a zero divisor. (b) The element $rx$  is nilpotent  for all $r \in R$. (c) The element $1+x$  is a unit in $R$. (d) The sum of any unit $u$ and a nilpotent  element is a unit in $R$.

\pf (a)  If $m = 1$, then $x = 0$. If $m > 1$, then $x$ and $x^{m-1}$ are both nonzero. (b) Observe 
\begin{align*}
( rx )^m &= \underbrace{rx \cdots rx}_{ m \text{ times}}\\
    &= r^mx^m\\
    &=r^m 0\\
    &=0.
\end{align*}
(c) Follows from (d) which is verified by 
$$(u+x)\left(\sum_{n=0}^{m-1}\frac{(-1)^nx^n}{u^{n+1}}\right) = 1.$$
\qedsymbol

### [@DF04, number 7.2.2]

\gvn Let $R$ be a commutative ring with unity. Let $p(x)$ be an element of the polynomial ring $R[x]$.

\wts The polynomial $p(x)$  is a zero divisor if and only if there is a nonzero $b\in R$  such that $bp(x) =0$. 

\pf \fore Clear. If $b \in R[x]$ is nonzero and $bp(x) = 0$, then $p$ is a zero divisor. \back Suppose $g$  is a polynomial of minimal degree such that $g(x)p(x) =0$. As a base case for induction consider $a_n, b_m$  leading coefficients of $p(x)$ and $q(x)$  respectively. Then $a_nb_m =0$. So $\underbrace{a_ng(x)}_{\deg m-1}p(x)=0$. But $g$  was a minimal  zero divisor of $p(x)$, so $a_ng(x) =0$. We proceed by strong induction on $i$. Suppose $a_{n-k}g(x)=0$  for all $k < i$, where $a_j$ is the coefficient of the $j$th term of $p(x)$. Because $g(x)p(x) =0$,  distributing we see $b_m a_{n-i} = 0$. As $\underbrace{a_{n-i}g(x)}_{\deg \le m-1}p(x)=0$ we have $a_{n-i}g(x) = 0$. 

Since for all $i < n$, $a_{n-i}g(x) =0$ implies $a_{n-i}b_m = 0$, we conclude $b_mp(x) =0$. \qedsymbol

### [@DF04, number 7.2.7]

### [@DF04, number 7.2.13]

### [@DF04, number 7.3.22]

### [@DF04, number 7.3.25]

### [@DF04, number 7.3.29]

### [@DF04, number 7.3.34]

### [@DF04, number 7.4.10]

### [@DF04, number 7.4.30]

### [@DF04, number 7.4.37]

## References
