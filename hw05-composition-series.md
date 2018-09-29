---
title: Isomorphism Theorems and Composition Series
author: Colton Grainger (MATH 6130 Algebra)
date: 2018-09-29
bibliography: /home/colton/Downloads/coltongrainger.bib
macros: true
---

\setcounter{section}{4}

## Assignment due 2018-10-03

### [@DF04, number 3.3.6]

Let $M = \langle v,u \rangle$ be the modular group of order $16$. 

- Using the lattice isomorphism theorem, we sketch the lattice of subgroups of $M/\langle v^4\rangle$ and decide the isomorphism type of this group.
- We describe which group of order 8 has the same lattice as $M/\langle v^4\rangle$.
- We give the generators and relations for $M/\langle v^4\rangle$.
- We decide the isomorphism type of $M/\langle v^4\rangle$.

### [@DF04, number 3.3.7]

Let $M$ and $N$ be normal subgroups of $G$ such that $G = MN$. Considering the lattice of $G$, we have that $G/(M \cap N) \cong (G/M) \times (G/N)$. 

### [@DF04, number 3.3.9]

Let $p$ be a prime and let $G$ be a group of order $p^a m$ where $p$ does not divide $m$. Further, let $P$ be a subgroup of $G$ of order $p^a$ and $N$ is a normal subgroup of $G$ order $p^b n$, where $p$ does not divide $n$. Then $\abs{P \cap N} = p^b$ and $\abs{PN/N} = p^{a-b}$. 

(The subgroup $P$ of $G$ is called a *Sylow p-subgroup* of $G$. Hence, the intersection of any Sylow p-subgroup of $G$ with a normal subgroup $N$ is a Sylow *p*-subgroup of $N$.)

### [@DF04, number 3.3.10]

A subgroup $H$ of a finite group $G$ is called a *Hall subgroup* of $G$ if its index in $G$ is relatively prime to its order: $(\abs{G : H}, \abs{H}) = 1$. If $H$ is a Hall subgroup of $G$ and $N \triangleleft G$, then $H \cap N$ is a Hall subgroup of $N$ and $HN/ N$ is a Hall subgroup of $G/N$.

### [@DF04, number 3.4.2]

We exhibit all $3$ composition series for $Q_8$ and all $7$ composition series for $D_8$. We list the composition factors in each case.

### [@DF04, number 3.4.7]

If $G$ is a finite group and $H \triangleleft G$, then there is a composition series of $G$ one of whose terms in $H$.

### [@DF04, number 3.4.11]

If $H$ is a nontrivial normal subgroup of the solvable group $G$, then there is a nontrivial subgroup $A$ of $H$ with $A \triangleleft G$ and $A$ abelian.

### [@DF04, number 3.5.6]

The group $H = \langle (1\, 3), (1\, 2\, 3\, 4)\rangle$ is a proper subgroup of $S_4$. We give the isomorphism type of $H$.

### [@DF04, number 3.5.10]

We find a composition series for $A_4$, and argue that $A_4$ is not solvable.

### [@DF04, number 4.1.7]

Let $G$ be a transitive permutation group on the finite set $A$. A *block* is a nonempty subset $B$ of $A$ such that for all $\sigma \in G$ either $\sigma(B) = B$ or $\sigma(B) \cap B = \emptyset$ (where $\sigma(B)$ is the set $\{\sigma(b) : b \in B\}$).

\newcommand{\Stab}[2]{\mathrm{Stab}_{#1}\left( #2 \right)}

(a) If $B$ is a block containing the element $a$ of $A$, then the set $\Stab{G}{B}$ defined by $\{\sigma \in G : \sigma(B) = B\}$ is a subgroup of $B$.

(b) If $B$ is a block and $\sigma_1(B), \sigma_2(B), \ldots, \sigma_n(B)$ are all the distinct images of $B$ under the elements of $G$, then these form a partition of $A$.

(c) A (transitive) group $G$ on a set $A$ is said to be *primitive* if the only blocks in $A$ are the trivial ones. The sets of size $1$ and $\abs{A}$. We demonstrate that $S_4$ is primitive on $A = \{1, 2, 3, 4\}$. Further, $D_8$ is not primitive as a permutation group on the four vertices of a square.

(d) The transitive group $G$ is primitive on $A$ if and only if for each $a \in A$, the only subgroups of $G$ containing $\Stab{G}{a}$ are $\Stab{G}{a}$ and $G$ (i.e., $\Stab{G}{A}$ is a *maximal* subgroup of $G$).^[Hint: use part (a).]

### [@DF04, number 4.1.9]

Assume $G$ acts transitively on the finite set $A$ and let $H$ be a normal subgroup of $G$. Let $\sO_1, \sO_2, \ldots, \sO_r$ be the distinct orbits of $H$ on $A$.

(a) $G$ permutes the sets $\sO_1, \sO_2, \ldots, \sO_r$ in the sense that for each $g \in G$ and each $i \in \{1, \ldots, r\}$ there is a $j$ such that $g\sO_i = \sO_j$, where $g\sO = \{g(a) : a \in \sO\}$. Then $G$ is transitive on $\{\sO_1, \ldots, \sO_r\}$. Furthermore, all orbits of $H$ on $A$ have the same cardinality.

(b) If $a \in \sO_1$, then $\abs{\sO_1} = \abs{H : H \cap \Stab{G}{a}}$. Furthermore, $r = \abs{G : H\Stab{G}{a}}$. [We draw the sublattice describing the second isomorphism theorem for the subgroups of $H$ and $\Stab{G}{a}$ of $G$, noting that $H \cap \Stab{G}{a} = \Stab{H}{a}$.]

## References
