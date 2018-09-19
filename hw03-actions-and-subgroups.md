---
title: Actions and Subgroups
author: Colton Grainger (MATH 6130 Algebra)
date: 2018-09-16
bibliography: /home/colton/Downloads/coltongrainger.bib
macros: true
---

\setcounter{section}{2}

## Assignment due 2018-09-19

### [@DF04, number 2.1.8]

Let $H$ and $K$ be subgroups of a group $G$. $H \cup K$ is a subgroup if and only if either $H \subset K$ or $K \subset H$. 

*Proof.*[^se] ($\Rightarrow$) If $H \subset H$ or $K\subset H$ then $H \cup K$ is $K$ or $H$, hence $H \cup K$ is a subgroup of $G$.

($\Leftarrow$) Suppose $H \cup K$ is a subgroup of $G$. For contradiction, let $H \not\subset K$ and $K \not\subset H$. Then choose $h \in H\setminus K$ and $k \in K\setminus H$. Because $H \cup K$ is closed as a subgroup, we have $hk \in H \cup K$. But in which set $H$ or $K$ is $hk$ an element? Either $hk \in H$, hence $h^{-1}hk \in H$, hence $k \in H$; or $hk \in K$, hence $hkk^{-1} \in K$, hence $h \in K$; which is the desired contradiction. \qedsymbol

[^se]: See <https://math.stackexchange.com/questions/334405/>, "Suppose both $H,K$ are distinct and proper. Then pick $h\in H\setminus K$ and $k\in K\setminus H$. In which of $K$ or $H$ or both does $hk$ lie?"

### [@DF04, number 2.1.9]

Let $G = GL_n(\FF)$ where $\FF$ is an field. We define the *special linear group* 
$$SL_n(\FF) = \{A \in GL_n(\FF) : \det(A) =1\}.$$

Then $SL_n(\FF) \le GL_n(\FF)$.

*Proof.* Knowing that $GL_n(\FF)$ is a group of which $SL_n(\FF)$ is a subset, it suffices to show that $SL_n(\FF)$ is nonempty and closed under products and taking inverses.

- (Nonempty) The identity $n\times n$ matrix $I \in SL_n(\FF)$ since $\det(I) = 1^n =1$.
- (Products) Let $A, B \in SL_n(\FF)$. Then $\det(A) = \det(B) = 1$. So $\det(AB) = \det(A)\det(B) = 1$, thus $AB \in SL_n(\FF)$.
- (Inverses) Let $A \in SL_n(\FF)$. So $\det(A) = 1$, and since $\det(A^{-1}) = \frac{1}{\det(A)} = 1$, we have $A^{-1} \in SL(\FF)$.

So $SL_n(\FF) \le GL_n(\FF)$. \qedsymbol

### [@DF04, number 2.1.14]

The set $\{ x \in D_{2n} : x^2 = 1\}$ is not a subgroup of $D_{2n}$ (where $n\ge 3$).

*Key idea*.[^d2n] The elements of the dihedral group of order $1$ or $2$ are

- the identity,
- any of the $n$ reflections, and 
- if $n$ is even, the rotation by $\pi$.

The set of such elements is not closed under composition.

*Proof.* Consider the presentation $D_{2n} = \langle r, s : r^n  = s^2 = 1, sr^is = r^{-i}\rangle$. If $x \in D_{2n}$, then $x$ can be written as a product of generators $x = r^{i}s^{j}$ where $i \in \{0, \ldots, n-1\}$ and $j \in \{0,1\}$. 

What is $\{ x \in D_{2n} : x^2 = 1\}$? Or writing the elements of $D_{2n}$ as $r^is^j$, for which powers $i$ and $j$ is it true that $(r^i s^j)^2 =1$?

- When $j =0$, we have $r^{2i} = 1$. Because $i < n$ and $n | 2i$, either $i = 0$ or, if $n$ is even, $i \in \{0,\frac{n}{2}\}$.
- When $j =1$, we have $(r^is)^2 = 1$ for all $i$, since $r^i(sr^is) = r^i(r^{-i}) = 1$.

So let $A = \{ x \in D_{2n} : x^2 = 1\}$. We've shown $$A = \left\{1, r^k, r^is :k =0 \text{ or, if $n$ is even, } k = \frac{n}{2},  i \in \{0,\ldots, n-1\} \right\}.$$ To see $A$ is not closed, take $r^2s, rs \in A$. But $(r^2s)(rs) = r^2(srs) = r^2r^{-1} = r \notin A$ (when $n \ge 3$). \qedsymbol

[^d2n]: See <https://math.stackexchange.com/questions/126639/>, "We can think of this geometrically, or use a presentation  ..."; see also <https://groupprops.subwiki.org/wiki/Element_structure_of_dihedral_groups>.

### [@DF04, number 2.2.6]

Let $H$ be a subgroup of the group $G$. 

(a) $H \le N_G(H)$. We show that this is not necessarily true if $H$ is not a subgroup.

(b) $H \le C_G(H)$ if and only if $H$ is abelian.

### [@DF04, number 2.2.10]

Let $H$ be a subgroup of order $2$ in $G$. Then $N_G(H) = C_G(H)$. Also, if $N_G(H) = G$, then $H \le Z(G)$.

### [@DF04, number 2.2.12]

Let $R$ be the set of all polynomials with integer coefficients in the independent variables $\{x_j\}_1^4$. That is, members of $R$ are finite sums of elements of the form $ax_1^{r_1}x_2^{r_2}x_3^{r_3}x_4^{r_4}$ where $a \in \ZZ$ and $r_j \in \ZZ_{\ge 0}$.

Each $\sigma \in S_4$ gives a permutation of $\{x_1, x_2, x_3, x_4\}$ by defining $\sigma \cdot x_j = x_{\sigma(j)}$. This extends naturally to a map from $R$ to $R$ by defining $$\sigma\cdot p(x_1,x_2,x_3,x_4) = p(x_{\sigma(1)},x_{\sigma(2)},x_{\sigma(3)},x_{\sigma(4)})$$ for all $p(x_1,x_2,x_3,x_4) \in R$ (that is, $\sigma$ simply permutes the indices of the variables). 

(a) Let $p = p(x_1,x_2,x_3,x_4)$ be the polynomial 
$$12x_1^5x_2^7x_4 - 18x_2^3x_3 + 11x_1^6x_2x_3^3x_4^{23}$$
and consider the permutations $\sigma = (1 \, 2 \, 3\, 4)$ and $\tau = (1\, 2\, 3)$. We compute:

    - $\sigma \cdot p$
    - $\tau \cdot (\sigma \cdot p)$
    - $(\tau \circ \sigma)\cdot p$
    - $(\sigma \circ \tau)\cdot p$

(b) This definition gives a left subgroup action of $S_4$ on $R$.
(c) We exhaustively list all permutations in $S_4$ that stabilize $x_4$. They form a subgroup isomorphic to $S_3$.
(d) We list all permutations in $S_4$ that stabilize $x_1 + x_2$. They form an abelian subgroup of order $4$.
(e) We list all permutations in $S_4$ that stabilize $x_1x_2 + x_3x_4$. They  form a subgroup isomorphic to the dihedral group of order $8$.
(f) The permutations in $S_4$ that stabilize the element $(x_1 + x_2)(x_3 + x_4)$ are the same as those in part (e).

### [@DF04, number 2.3.25]

Let $G$ be a cyclic group of order $n$ and let $k$ be an integer relatively prime to $n$. The map $x \mapsto x^k$ is surjective.

### [@DF04, number 2.4.3]

If $H$ is an abelian subgroup of a group $G$ then $\langle H, Z(G)\rangle$ is abelian.

We exhibit an abelian subgroup of $H$ of $G$ such that $\langle H, C_G(H)\rangle$ is *not* abelian.

### [@DF04, number 2.4.12]

The subgroup^[Hint: find the order of this subgroup.] of upper triangular matrices in $GL_3(\FF_2)$ is isomorphic to the dihedral group of order $8$.

### [@DF04, number 2.4.15]

There's a proper subgroup of $\QQ$ which is not cyclic.

### [@DF04, number 2.4.16]

A subgroup $M$ of a group $G$ is called a *maximal subgroup* if $M \neq G$ and the only subgroups of $G$ which contain $M$ are $M$ itself and $G$.

(a) If $H$ is a proper subgroup of the finite group $G$, then there is a maximal subgroup of $G$ containing $H$.
(b) The subgroup of all rotations in a dihedral group is a maximal subgroup.
(c) If $G = \langle x\rangle$ is a cyclic sugroup of order $n \ge 1$, then a subgroup $H$ is maximal if and only if $H = \langle x^p \rangle$ for some prime $p$ dividing $n$.

### Maximal subgroups in a finite group

A finite group with no more that two maximal subgroups is cyclic.

## References
