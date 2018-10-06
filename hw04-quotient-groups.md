---
title: Quotient Groups
author: Colton Grainger (MATH 6130 Algebra)
date: 2018-09-19
bibliography: /home/colton/Downloads/coltongrainger.bib
macros: true
---

\newcommand{\order}[1]{\left\lvert{#1}\right\rvert}
\setcounter{section}{3}

## Assignment due 2018-09-26

### [@DF04, number 2.5.12]

The group $Z_2 \times Z_4 = \langle a,b | a^2 = b^4 =1, ab = ba\rangle$ of order $8$ has three subgroups of order $4$. They are $\langle a,b^2 \rangle \cong V_4$, $\langle b\rangle \cong Z_4$, and $\langle ab\rangle \cong Z_4$.

Here's the lattice^[TODO, use TikZ. See, e.g., <https://tex.stackexchange.com/questions/47392/how-to-draw-a-poset-hasse-diagram-using-tikz> or <https://ctan.math.washington.edu/tex-archive/graphics/pgf/contrib/tikz-cd/tikz-cd-doc.pdf>.] of subgroups of $Z_2 \times Z_4$, with each subgroup expressed in terms of at most two generators.

```
         Z_2 x Z_4
        /     \   \
       /       \   \
    <a,b^2>    <b> <ab>
    /    | \    |  /
   /     |  \   | /
<ab^2>  <a>  <b^2>
    \    |    /
     \   |   /
      \  |  /
        {1}
```

### [@DF04, number 2.5.13]

The group $Z_2 \times Z_8 = \langle x,y : x^2 = y^8 = 1, xy = yx\rangle$ has order $16$ has three subgroups of order $8$. They are $\langle x, y^2\rangle \cong Z_2 \times Z_4$, $\langle y \rangle \cong Z_8$, and $\langle xy \rangle \cong Z_8$. 

Here's the lattice of subgroups of $Z_2 \times Z_8$.
```
              Z_2 x Z_8
            /      \   \
           /        \   \
        <x, y^2>    <y> <xy>
       /   |    \    |  /
      /    |     \   | /
     /     |      \  |/
  <x,y^4>  <xy^2>  <y^2>
  |   |  \    \    /
  |   |   \    \  /
  |   |    \    \/
  |   |     \   /
<x>  <xy^4> <y^4>
  \    |     /
   \   |    /
    \  |   /
     \ |  / 
      {1}
```

### [@DF04, number 2.5.14]

Let $M$ be the (*modular*) group of order $16$ with the following presentation:

$$\langle u, v : u^2 = v^8 = 1, vu = uv^5 \rangle$$

$M$ has three subgroups of order $8$, they are 

$\langle u,v^2 \rangle$, $\langle v\rangle$, $\langle uv \rangle$. 

One can show the lattice of subgroups of $M$ is the same as the lattice of subgroups of $Z_2 \times Z_8$, replacing everywhere $x$ with $u$ and $y$ with $v$.

However, $Z_2 \times Z_8$ is abelian but $M$ is not. Hence the two groups are not isomorphic.

### [@DF04, number 3.1.11]

Let $\FF$ be a field and consider the subgroup of upper triangular matrices in $GL_2(\FF)$, $$G = \left\{\begin{pmatrix} a & b \\ 0 & c \end{pmatrix} : a, b, c \in \FF, ac \neq 0 \right\}.$$

Note that for all $A,B \in G$ we have $$AB = \begin{pmatrix}a & b\\ & c\end{pmatrix}\begin{pmatrix} d & e\\ & f\end{pmatrix} = \begin{pmatrix}ad & b+e\\ & cf\end{pmatrix}.$$

(a) The map $\phi: \begin{pmatrix} a & b \\ 0 & c \end{pmatrix} \mapsto a$ is a surjective homomorphism from $G$ onto $\FF^\times$ (the multiplicative group of nonzero elements in $\FF$). We describe the fibers and kernel of $\phi$.

  - $\phi$ is well defined and onto, noting $A_{1,1} \in \FF^\times$ for all $A \in G$.
  - $\phi$ is a homomorphism as for all $A,B \in G$ we have that $\phi(AB) = A_{1,1}B_{1,1} = \phi(A)\phi(B)$.
  - For $x \in \FF^\times$ we have $$\phi^{-1} = \left\{\begin{pmatrix} x & b \\ & c \end{pmatrix} c \neq 0\right\},$$
    in particular $\ker{\phi} = \left\{\begin{pmatrix} 1 & b \\ & c \end{pmatrix} c \neq 0\right\}$

(b) The map $\psi: \begin{pmatrix} a & b \\ 0 & c \end{pmatrix} \mapsto (a,c)$ is a surjective homomorphism from $G$ onto $\FF^\times \times \FF^\times$. We describe the fibers and kernel of $\psi$.
  
  - $\phi$ again is well defined and onto.
  - $\phi$ is a homomorphism as for all $A,B \in G$ we have that $$\phi(AB) = (A_{1,1}B_{1,1}, A_{2,2}B_{2,2}) = (A_{1,1}, A_{2,2})\cdot(B_{1,1}, B_{2,2}) = \phi(A)\phi(B).$$
  - For $(x,y) \in \FF^\times \times \FF^\times$, note $\phi^{-1}\left\{\begin{pmatrix} x & b \\ & y\end{pmatrix}\right\}$ and in particular $\ker{\phi} = \left\{\begin{pmatrix} 1 & b \\ & 1\end{pmatrix}\right\}$.

(c) Let $H$ be the subgroup of unit upper triangular matrices[^uut] in $GL_2(\FF)$. Then $H \cong \FF$ (the additive group). 

[^uut]: A *unit* upper triangular matrix is an upper triangular matrix with $1$ in each diagonal entry. In the $2\times 2$ case, the unit upper triangular matrices are completely determined by the element $b \in \FF$ in row $1$, column $2$. The isomorphism should be clear.

  - Consider the map $\phi \colon H \to \FF$ defined by $\begin{pmatrix} 1 & b \\ & 1\end{pmatrix} \mapsto b$.
  - Here $\phi$ is well defined and onto.
  - For $A, B \in H$, note that $\phi(AB) = A_{1,2}+ B_{1,2} = \phi(A) + \phi(B)$, so $\phi$ is a homomorphism.
  - Lastly, observe $\ker{\phi} =  \begin{pmatrix} 1 & 0 \\ & 1\end{pmatrix}$, whence the kernel is trivial and $\phi$ is an isomorphism. 
  - We conclude that $H \cong \FF$.

### [@DF04, number 3.1.19]

\newcommand{\h}[1]{\overline{#1}}

Let $M$ be the modular group of order $16$ and let $\h{M} = M/\langle v^4\rangle$ be the quotient of $M$ by the (normal) subgroup generated by $v^4$.

(a) The order of $\h M$ is $8$. Consider that the order of $\langle v^4 \rangle$ in $M$ is $2$, whence there are $8$ left cosets of $\langle v^4 \rangle$ in $M$, and these cosets are the distinct elements of $\h M$.

(b) Each element of $\h M$ is of the form $\h u^a\h v^b$ for some integers $a$ and $b$. Why? Suppose $\h x \in \h M$, then $\h x$ is a coset of $\langle v^4 \rangle$ in $M$. If $x$ is a representative of $\h x = \{ x, xv^4\}$. Suppose $x = u^a v^c$ (any element of $M$ can be written in such form). To take advantage of the quotient structure, notice that $u^a v^{c+4} \{1, v^4\} = u^a v^c \{v^4, 1\}$. Generalizing, we write $\h x = \h{u}^a \h{v}^b$ where $b$ is the least residue of $c$ modulo $4$.

(c) The order of each of the elements in part (b) is given. 

  - $\h v$, $\h{uv}$, $\h{v}^3$, $\h{u}\h{v}^3$ of order $4$
  - $\h u$, $\h{v}^2$, $\h{uv}$, $\h{u}\h{v}^2$ of order $2$
  - $\h 1$ the identity

(d) We reduce the following elements of $\h M$ to their "least residue" (i.e., to the form $\h{u}^a\h{v}^b$).

    - $\h{vu} = \h{uv}$
    - $\h{uv^{ -2 }u} = \h{v}^2$
    - $\h{u^{-1}v^{-1}uv} = \h 1$

(e) $\h M \cong Z_2 \times Z_4$. How come? Let $\phi \colon \h{M} \to Z_2 \times Z_4$ be defined by $\phi(\h{u}^a \h{v}^b) = (a,b)$.

  - $\phi$ is here well defined and surjective, for there's a $\h{u}^a \h{v}^b$ for each $a \in \{0,1\}$ and $b\in \{0,1,2,3\}$.
  - $\phi$ is a homomorphism when we consider at multiplication of $\h x$ in $\h M$ is addition in the exponents.
  - Now $\ker{\phi} = \{\h{u}^0, \h{v}^0\}$ is trivial.
  - Whence $\phi$ is an isomorphism of groups.

### [@DF04, number 3.1.22]

(a) If $H$ and $K$ are normal subgroups of a group $G$ then their intersection $H \cap K$ is also a normal subgroup of $G$. 

*Proof.* Let $G$ act on itself by conjugation. What's the normalizer of $H \cap K$ in $G$? It's $\{g \in G : gxg^{-1} \in H \cap K, \text{ for all } x \in H \cap K\}$.

Both $H$ and $K$ are normal in $G$, hence $x \in H \cap K$ implies every element $g$ of $G$ conjugates $x$ into $H$ and also $K$. Therefore the normalizer of $H \cap K$ in $G$ is $G$ itself, hence $H \cap K$ is normal. \qedsymbol

(b) The intersection of an arbitrary nonempty collection of normal subgroups of a group is a normal subgroup. 

*Proof.* Let $H_\lambda$ be normal in $G$ for all $\lambda \in \Lambda$. Suppose $x \in H_\lambda$ for all $\lambda$. Then for every $g \in G$, by normality of $H_\lambda$ we have $gxg^{-1} \in H_\lambda$. Whence for all $g \in G$, $gxg^{-1} \in \cap H_\lambda$. So the normalizer of $\cap H_\lambda$ in $G$ is $G$ itself. \qedsymbol

### [@DF04, number 3.1.36]

If $G/Z(G)$ is cyclic then $G$ is abelian.^[If $G/Z(G)$ is cyclic with generator $xZ(G)$, every element of $G$ can be written in the form $x^a z$ for some integer $a \in \ZZ$ and some element $z \in Z(G)$.]

*Proof.* Choose a generator of the cyclic group $G/ Z(G)$, say the coset $xZ(G)$ for some $x \in G$. Now let $g \in G$, so the coset $gZ(G) \in G/Z(G) = \langle xZ(G)\rangle$. Hence for some $a \in \ZZ$ we have $gZ(G) = x^a Z(G)$. By definition of a coset, we have $y,w \in Z(G)$ such that 
\begin{align*}
gw &= x^ay, &\text{ hence} \\
g &= x^ayw^{-1}, &\text{ hence} \\
gw &= x^az, &\text{ for $yw^{-1} = z \in Z(G)$.}
\end{align*}

Every element of $G$ has such a representation. Now $G$ is abelian because for any two $g,h \in G$, we have $n, m \in Z(G)$ such that $gh = x^a n x^b m = x^{a+b} nm = x^b m x^a n = hg$, exploiting that $n,m$ commute. \qedsymbol

### [@DF04, number 3.1.41]

Let $G$ be a group. Then *commutator subgroup* $N = \langle x^{-1}y^{-1}xy : x,y \in G \rangle$ is a normal subgroup of $G$, also for which the quotient group $G/N$ is abelian.

*Proof.* Suppose the word $x_1 \cdots x_n \in N$ and consider an element $g \in G$. We'll conjugate the word by $g$ and show that it lies in the commutator subgroup.

Consider that strategically inserting $g^{-1}g$ into the conjugate word produces $g x_1 \cdots x_n g^{-1} = g x_1 g^{-1} \cdots g x_n g^{-1}$. Take the individual segment $g x_i g^{-1}$, which explodes to $ga_i^{-1}b_i^{-1}a_i b_i g^{-1}$ since $x_i$ is a commutator. Again inserting $g^{-1}g$ into the conjugate of the segment, we have $(ga_ig^{-1})^{-1}(gb_ig^{-1})^{-1}(ga_i g^{-1})(g b_i g^{-1})$ which is itself a commutator in $N$. 

So the conjugate $g x_1 \cdots x_n g^{-1}$ is the product of commutators, and thus in $N$. We conclude that the normalizer of $N$ is $G$ is all of $G$, so $N$ is normal in $G$. 

Now to show that $G/N$ is abelian, let $g,h \in G$. Since $g^{-1}h^{-1}gh \in N$, we have $(hg)^{-1}gh \in N$. Thus $(hg)^{-1} gh N = 1 N$, and because $N$ is normal we have the equality of cosets $gh N = hg N$. So $G/N$ is abelian.\qedsymbol

### [@DF04, number 3.2.4]

A finite abelian group has a subgroup of order $n$ for each positive divisor $n$ of its order.[^finite]

*Proof.* We proceed by strong induction on the order of the group. 

For small orders of the group $G$, say $1,2,3$ and $4$, the claim is obviously true. It's trivial to check for ${1}, Z_2, Z_3$ and we (exhaustively) list that both $Z_4$ and $V_4$ have subgroups of orders $1,2$ and $4$.

\providecommand{\abs}[1]{\lvert #1 \rvert}

Now suppose for all $k \leq \abs{G}$ a finite abelian group of order $k$ has subgroups of order $d$ for every positive integer $d$ such that $d | k$. 

Let $d$ be a proper divisor of $n = \abs{G}$. If $d=1$ the trivial subgroup of $G$ will do. So assume that $d \neq 1$ and choose a prime $p$ in the factorization of $d$. 

*Assuming* Cauchy's theorem, there's a (cyclic) subgroup $\langle x \rangle$ of $G$ of order $p$. The subgroup $\langle x \rangle$ is normal in $G$ because $\langle x \rangle$ is abelian. 

We have the natural homomorphism $\pi \colon G \to G/\langle x \rangle$, where $\abs{G/\langle x \rangle} = \frac{n}{p}$. By the inductive hypothesis, there's a subgroup $H$ of $G/\langle x\rangle$ of order $\frac{d}{p}$. 

Now consider $K = \pi^{-1}(H)$. Since $H$ is a group, the inverse image $K \le G$ in the domain. The restriction of $\pi$ to $K$ is a surjective homomorphism onto $H$ with kernel $\langle x \rangle$. Now $K / \langle x \rangle \cong H$ by the first isomorphism theorem, hence $$\frac{\abs{K}}{\abs{\langle x \rangle}} = \abs{H} \text{ and thus } \abs{K} = \frac{d}{p}\cdot p = d.$$ 
\qedsymbol

[^finite]: Notably, I consulted (1) “If $G$ is abelian, it has a subgroup in every order of $|G|$'s divisors?” <https://math.stackexchange.com/q/1352384/> (2) “every Abelian group is a converse lagrange theorem group” <https://math.stackexchange.com/q/910426/>.

### [@DF04, number 3.2.9]

A proof of Cauchy's theorem.^[Due to James McKay (*Another proof of Cauchy's group theorem*, Amer. Math. Monthly, 66(1959), p. 119)]

Let $G$ be a finite group and let $p$ be a prime dividing $\order{G}$. Let $\sS$ denote the set of $p$-tuples of elements of $G$ the product of whose coordinates is $1$: 
$$S\sS = \left\{(x_1 , x_2, \ldots, x_p) : x_i \in G \text{ and } x_1x_2 \cdots x_p = 1\right\}.$$

(a) $\sS$ has $\order{G}^{p-1}$ elements, hence has order divisible by $p$. Why? Of $\abs{G}$ elements, choose $p-1$ with repetitions, and such that the product of the $p$ elements is $1$, we must take the unique inverse $x_p = (x_1 \cdots x_{p-1})^{-1}$. So $\abs{\sS} = \abs{G}^{p-1}$. By Fermat's little theorem, $p$ divides $\abs{G}^{p-1}$.

For notation's sake, let $C_p$ (considered as a subgroup of the symmetric group on $p$ letters) act on $\sS$ by $$\sigma(x_1, \ldots, x_p) \mapsto (x_{\sigma(1)}, \ldots, x_{\sigma(p)}).$$ Now we identify each cyclic permutation shifting $j$ entries right of every $\alpha \in \sS$ with $\sigma^j(\alpha)$ where for $j \in \ZZ$ $\sigma^j$ is the $p$-cycle $(1\, 2\, \cdots p)^j$. Now the action is faithful, and additionally for all $j \in ZZ$ and all $\alpha \in \sS$ we know $\sigma^j(\alpha) \in \sS$ since $x_p$ remains nested in cyclic order between $x_{p-1} and x_1$.

Define the relation $\sim$ on $\sS$ by letting $\alpha \sim \beta$ if $\beta$ is a cyclic permutation of $\alpha$. 

(b) We've shown a cyclic permutation of an element of $S$ is again an element of $\sS$.

(c) $\sim$ is an equivalence relation on S. Why? 

  - $\sigma^0(\alpha) = \alpha$ gives reflexivity,
  - $\sigma^{-k}(\beta) = \alpha$ whenever $\sigma^j(\alpha) = \beta$ gives symmetry, and lastly 
  - for $\sigma^j(\alpha) = \beta$, $\sigma^k(\beta) = \gamma$ then $\sigma^{k+j}(\alpha) = \gamma$.

(d) An equivalence class in $\sS$ contains a single element if and only if it is of the form $(x, x, \ldots, x)$ with $x^p = 1$.

Note that $\sigma^j$ stabilizes elements of the form $(x, x, \ldots, x)$ for all $j \in \ZZ$. Now if $\alpha \in \sS$ is not of the form $(x, x, \ldots, x)$ then the equivalence class in $\alpha$ has $p$ distinct elements, because $\sigma^j(\alpha) = \alpha$ if and only if $j \in \ZZ/p\ZZ$. There are no more distinct elements in $\alpha$'s equivalence class than those already conspicuous, namely $\alpha, \sigma(\alpha), \ldots, \sigma^{p-1}(\alpha)$.

(e) Every equivalence class has order $1$ or $p$ (note that p is a prime). Whence $\order{G}^{p-1} = k + pd$, where $k$ is the number of classes of size $1$ and $d$ is the number of classes of size $p$.

Since $\sS$ is partitioned by $\sim$, summing the elements in each class will produce $\abs{G}^{p-1}$. Well, an $\h{\alpha} \in \sS/\sim$ has size $1$ or $p$. Say there are $k$ classes of size $1$ and $d$ classes of size $p$. Thus $\abs{G}^{p-1} = k + dp$.

(f) Since $\{(1, 1, \ldots , 1)\}$ is an equivalence class of size $1$, from (e) there must be a nonidentity element $x$ in $G$ with $x^p = 1$, that is, $G$ contains an element of order $p$. 

Since $p$ divides $\abs{G}^{p-1}$ we must have that $p$ divides $k + dp$ hence $p | k$. Because $k > 1$, we have $k = mp$ for some integer $m \neq 0$, so there's a non-identity element $x \in G$ with $x^p = 1$.

### [@DF04, number 3.2.18]

Let $G$ be a finite group, let $H$ be a subgroup of $G$ and let $N \trianglelefteq G$. If $\order{H}$ and $\order{G : N}$ are relatively prime then $H \le N$.

*Proof.* Consider the natural projection $\pi \colon G \to G/N$. Since $H \le G$, we have $\pi(H) \le G/N$. So $\abs{\pi(H)}$ divides $|G:N|$. Now note that $\abs{\pi(H)}$ divides $\abs{H}$ (it's "like" a subgroup). Because the greatest common divisor of $|G:N|$ and $\abs{H}$ is $1$, we have $\abs{\pi(H)} = 1$, whence $H \le \ker{\pi} = N$.
\qedsymbol

### Minimal and maximal subgroups

Suppose $N$ is a nontrivial abelian subgroup of $G$, minimal with the property that it is normal in $G$. Let $H$ be a proper subgroup of $G$ such that $NH=G$. The intersection of $N$ with $H$ is trivial and $H$ is a maximal subgroup of $G$.

*Proof.* Consider the natural homomorphism $\pi$ onto the group $G/N$. I claim $H \cap N \subset \ker{\pi} = N$, and noting that $N$ is abelian, we have that $H \cap N$ is normal in $N$. Since $N$ is minimal normal we have that $H \cap N = \{1\}$ or $H \cap N = N$. But because $H$ is a proper subgroup of $G$, there's some $g \in G$ for which $gN \not\subset \pi^{-1}(H)$, so $H \cap N \neq \ker{\pi} = N$. Whence $H \cap N$ is seen to be trivial.

## References
