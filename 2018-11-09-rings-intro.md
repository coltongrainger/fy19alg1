---
title: Rings Intro
author: Colton Grainger (MATH 6130 Algebra)
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

\gvn $R$, a ring; $Z$, the center of $R$.

\wts The center $Z$ is a subring. If a $R$ is a division ring, then $Z$ is a field.

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
$$az = za \quad \text{ implies } \quad (az)^{-1} = (za)^{-1} \quad \text{ implies } \quad z^{-1}r = rz^{-1}.$$ So the center of the ring is closed under inverses. Thus the center is a division ring.
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

\gvn Let $R$ be a commutative ring with unity $1 \neq 0$ and let $p(x)$ be an element of the polynomial ring $R[x]$.

\wts The polynomial $p(x)$  is a zero divisor if and only if there is a nonzero $b\in R$  such that $bp(x) =0$. 

\pf \fore Clear. If $b \in R[x]$ is nonzero and $bp(x) = 0$, then $p$ is a zero divisor. \back Suppose $g$  is a polynomial of minimal degree such that $g(x)p(x) =0$. As a base case for induction consider $a_n, b_m$  leading coefficients of $p(x)$ and $q(x)$  respectively. Then $a_nb_m =0$. So $$\underbrace{a_ng(x)}_{\deg m-1}p(x)=0.$$ But $g$  was a minimal  zero divisor of $p(x)$, so $a_ng(x) =0$. We proceed by strong induction on $i$. Suppose $a_{n-k}g(x)=0$  for all $k < i$, where $a_j$ is the coefficient of the $j$th term of $p(x)$. Because $g(x)p(x) =0$,  distributing we see $b_m a_{n-i} = 0$. As $$\underbrace{a_{n-i}g(x)}_{\deg \le m-1}p(x)=0$$ we have $a_{n-i}g(x) = 0$. 

Since for all $i < n$, $a_{n-i}g(x) =0$ implies $a_{n-i}b_m = 0$, we conclude $b_mp(x) =0$. \qedsymbol

### [@DF04, number 7.2.7]

\gvn Let $R$ be a commutative ring with unity, let $\sM_n(R)$ be  the ring of  square $n$ by $n$ matrices  with  entries in the ring $R$, let $Z$ be the center of $\sM_n(R)$. Suppose $(z_{ij}) \in Z$.

\wts The center $Z$  is the ring  of scalar matrices isomorphic to $R$.

\pf Let $E_{ij}$ be a "unit" matrix in $\sM_n(R)$ with $i, j$th entry equal to  $1$, and all other entries $0$.  For all $i \in \{1, \ldots, n\}$, we have $$E_{ii}(z_{ij}) =(z_{ij})E_{ii} \text{ implies } z_{ij} = 0 \text{ if } \abs{i-j} >0.$$ For all $k \in \{1, \ldots, n\}$, we have $$E_{1k}(z_{ij}) =(z_{ij})E_{1k} \text{ implies } z_{11} = z_{kk}.$$ So $Z$ is in the subring of scalar diagonal matrices. It's trivial to check that $\lambda I$, a  scalar diagonal   matrix, commutes with any element of $\sM_n(R)$.  Moreover, the homomorphism $\phi \colon R \to \sM_n(R)$  given by $\lambda \mapsto \lambda I$  is an embedding and surjective onto the center $Z$. \qedsymbol




### [@DF04, number 7.2.13]

\gvn  Let $\sK$ be one of the conjugacy classes (which will be denoted $\sK_1, \ldots, \sK_r$) of the finite group $G$. Let $R$  be a commutative ring with unity. Consider the group ring $RG$, with center $Z = Z(RG)$.

\wts (a) $K = \sum_{k_i \in \sK} k_i \in Z$. (b) $\alpha \in Z$ if and only if $\alpha = \sum a_iK_i$ for $a_i \in R$.

\pf

(a) Each element $\sum r_gg \in RG$ commutes with $K$ if and only if $gK = Kg$ for all $g \in G$. The conjugation action of $G$ on its powerset $\sP(G)$ is an inner automorphism on elements, so the conjugacy class $\sK$ is fixed. Because $G$ is finite, conjugation permutes the elements in $\sK$. Thus $gKg^{-1} = K$. 

(b) \fore Suppose $\alpha = \sum a_iK_i$. Then 
$$\sum_i a_iK_i\sum_g r_g g = \sum_i \left( \sum_g r_g a_i K_i g \right) = \sum_i \left( \sum_g r_g a_i g K_i \right) = \sum_g r_g g\sum_i a_iK_i$$ so $\alpha \in Z$. \back Say $\alpha \in Z$. We can write $\alpha$ as the sum over conjugacy classes $\{k_{n_i}\}$ of elements in $G$: $$\alpha = \sum_i \left(\sum_{n_i} a_{n_i} k_{n_i}\right).$$
For each $i$, $G$ acts transitively on by conjugation on $\{k_{n_i}\}$. Fix $i$. For all $n_i$, transitivity of conjugation implies $a_{n_i} = a_i$ for some $a_i \in R$. We conclude $\alpha = \sum a_i K_i$. \qedsymbol

### [@DF04, number 7.3.22]

\gvn A ring $R$, an element $a \in R$, the sets $M = \{x \in R: ax =0\}$ and $N=\{x\in R: xa = 0\}$, and a left ideal $L$.

\wts (a) $M$ is a right ideal, $N$ is a left ideal. (b) $I$ is an ideal.

\pf

(a) First to argue that $M$ is a subring.

    - Nonempty: $0 \in M$. 
    - Closed under subtraction and multiplication: If $x, y \in M$, then $a(x-y) = ax -ay =0$ and also $a(xy) = (ax)y =0$.

    Moreover, if $r \in R$, then $a(xr) = 0$, so $xr \in M$. Thus $M$ is a right ideal. That $N$ is a left ideal follows similarly. 

(b) For each $a \in L$, let $M_a$ be the right ideal of left annihilators of $a$. Observe $$I = \bigcap_{a\in L} M_a$$ is a subring. Moreover, $I$ is closed under right multiplication as the $M_a$ are right ideals. Now let $r \in R$, $x \in I$, and $a \in L$. Because $rxa =0$, $rx \in \cap M_a = I.$ \qedsymbol

### [@DF04, number 7.3.25]

\gvn Let $R$  be a commutative ring with unity.

\wts The binomial theorem: for all $a,b \in R$, $(a+b)^n = \sum_{k=0}^n {n\choose k} a^{k}b^{n-k}$.

\pf Here's the crux of the argument: For all $k<n$, we have $${n \choose k} +{n\choose k+1} = {n+1 \choose k+1}.$$ We can proceed by induction and reindex the sums to exploit the above identity.

*Base*. Consider $(a+b)^1 = {1\choose 0}a^0b^1 + {1 \choose 1}a^1b^0$.

*Inductive step.* Suppose true for $n \in \NN$. Then 
\begin{align*}
(a+b)^{n+1} &= \left(\sum_{k=0}^n {n\choose k} a^{k}b^{n-k}\right)(a+b)\\
    &= a^{n+1} + \sum_{k=1}^n  {n\choose k-1}  a^{k}b^{n+1-k}  + \sum_{k=1}^n{n \choose k} a^k b^{n+1 -k} + b^{n+1}\\
    &= a^{n+1} + \sum_{k=1}^n{n+1\choose k}    a^{k}b^{n+1-k}  + b^{n+1}\\
    &= \sum_{k=0}^{n+1}{n+1 \choose k}a^k b^{n+1-k}.
\end{align*}
\qedsymbol

### [@DF04, number 7.3.29]

\newcommand{\Nil}[1]{\mathfrak{N}\left(#1\right)}

\gvn Let $R$  be a commutative ring with unity $1\neq 0$, let $\Nil R$ be its nilradical.

\wts $\Nil R$ is an ideal.

\pf $0 \in \Nil R$, so its nonempty. Let $x,y \in \Nil R$. There exist $m,n \in \NN$ such that $x^n = y^m = 0$. Let $\ell = 2\max \{m,n\}$. Applying the binomial theorem, $$(x+y)^\ell = \sum_{k=1}^\ell {\ell \choose k} x^{k}y^{\ell-k}  = \underbrace{0+\cdots + 0}_{\ell \text{ times}}$$ as for all $k\in \{0,\ldots, \ell\}$ either $x^k$ or $y^{\ell -k}$ will be $0$. Observe also $(xy)^{\min\{m,n\}} = 0$. So $\Nil R$ is an ideal. \qedsymbol

### [@DF04, number 7.3.34]

\gvn Let $R$ be a ring with unity $1\neq 0$. Let $I,J$ be ideals of $R$.

\wts (a) If $K$ is an ideal such that $I \cup J \subset K \subset I+J$, then $K=I+J$. (b) $IJ$ is an ideal contained in $I\cap J$. (c) The containment in (b) may be proper. (d) If $R$ happens to be commutative, then we have equality in (b).

\pf 

(a) $I, J \subset I+J$. Suppose $K$ is as above. Let $x+y \in I+J$. Observe $x,y \in K$. So $x+y \in K$ and thus $I+J \in K$.

(b) Immediately from its definition, $IJ$ is nonempty and closed under addition. Let $\sum_1^n x_iy_i \in IJ$ an $r \in R$. Then
$$r\sum_1^n x_iy_i \sum_1^n \underbrace{(rx_i)}_{\in I}y_i \in IJ.$$ So $IJ$ is an ideal. Moreover, $I,J$ are ideals, so $\sum_1^n \underbrace{x_i y_i}_{\in I \cup J} \in I\cup J$. Thus $IJ \subset I \cup J$.

(c) Consider $I=J=n\ZZ$ for $n \in \ZZ_{\ge 2}$. Observe $IJ = n^2\ZZ$, yet $I\cap J = n\ZZ$.

(d) Suppose $R$ is a commutative^[Is this hypothesis necessary?] unital ring with comaximal ideals $I$ and $J$. Let $z \in I\cap  J$. Now $z \in I+J$ also, so there are $x,y$ in $I,J$ respectively such that $x+y = z$. Then $z = x1 + 1y \in IJ$. \qedsymbol


### [@DF04, number 7.4.10]

\gvn Let $R$ be commutative unital ring, let $P$ be a prime ideal of $R$. Suppose $P$ is entire (i.e., contains no zero divisors).

\wts $R$ is entire.

\pf Say $ab =0$. Then with $ab + P = (a+P)(b+P) =0$. Since $P$ is prime, $R/P$ is entire. Wlog, $a+P = P$, so $a \in P$. As $P$ is an ideal we have $ab \in P$. As $P$ is entire $ab = 0$ implies $b=0$. \qedsymbol

### [@DF04, number 7.4.30] 

\gvn Let $R$ be a commutative unital ring, let $I$ be an ideal of $R$, let $\mathrm{rad} I$ be the radical of $I$.

\newcommand{\rad}[1]{\mathrm{rad}\, #1}

\wts (a) $\rad I$ is an ideal containing $I$. (b) $\rad I /I = \Nil {R/I}$.

\pf (a) $I \subset \rad I$ by definition. Let $x,y \in \rad I$. Say that $n$ and $m$ are the minimal powers required such that $x^n, y^m\in \rad I$. Let $\ell = \min\{n,m\}$ and $k = 2\max\{n,m\}$. Observe
$$(xy)^\ell = x^\ell y^\ell \in I, \quad (x+y)^k = \sum_{j=0}^k {k\choose j}x^j y^{k-j} \in I.$$
So $\rad I$ is a subring. Moreover, if $r \in R$, then $(rx)^n = r^nx^n \in I$. 
So $\rad I$ is an ideal. (b) Let $x + I \in \rad I / I$. Then $(x+I)^n = x^n +I = I$. So $x+I \in \Nil {R/I}$. To show the other containment, run the same argument in reverse. \qedsymbol

### [@DF04, number 7.4.37]

\newcommand{\fm}{\mathfrak{m}}
\newcommand{\fn}{\mathfrak{n}}
\newcommand{\fa}{\mathfrak{a}}

\gvn Let $R$ be a commutative unital ring.

\wts $R$ is a local ring with maximal ideal $\fm$ if and only if $R \setminus \fm = R^*$ is the multiplicative group of units.

\pf \fore Say $R \setminus \fm$ is not a unit. Then the principal ideal generated by $x$ is contained in another maximal ideal $\fn \neq \fm$, which is a contradiction, as $R$ is a local ring. So $x$ is a unit. \back Suppose $R \setminus R^*$ is an ideal $\fm$. Consider $\fa$ a proper ideal of $R$. We have 
$$\fa \cap R^* =\emptyset \quad \text{implies}\quad R\setminus R^* \supset \fa.$$
Thus $\fm \supset \fa$, demonstrating $\fm$ is the unique maximal ideal of $R$. \qedsymbol

## References
