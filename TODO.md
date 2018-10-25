---
title: TODO and to-revise
author: Colton Grainger
date: 2018-10-05
macros: true
bibliography: /home/colton/Downloads/coltongrainger.bib
revised: 2018-10-19
---

### Minimal and maximal subgroups

Suppose $N$ is a nontrivial abelian subgroup of $G$, minimal with the property that it is normal in $G$. Let $H$ be a proper subgroup of $G$ such that $NH=G$. The intersection of $N$ with $H$ is trivial and $H$ is a maximal subgroup of $G$.

### [@DF04, number 3.1.40]

\newcommand{\h}[1]{\overline{#1}}

Let $G$ be a group, let $N$ be a normal subgroup of $G$ and let $\h G = G/N$. The elements $\h x$ and $\h y$ commute in $\h G$ if and only if $x^{-1}y^{-1}xy  \in N$.

### [@DF04, number 3.4.7]

If $G$ is a finite group and $H \triangleleft G$, then there is a composition series of $G$ one of whose terms in $H$. 

### [@DF04, number 3.4.11]

If $H$ is a nontrivial normal subgroup of the solvable group $G$, then there is a nontrivial subgroup $A$ of $H$ with $A \triangleleft G$ and $A$ abelian. 

### [@DF04, number 3.5.6]

The group $H = \langle (1\, 3), (1\, 2\, 3\, 4)\rangle$ is a proper subgroup of $S_4$. We give the isomorphism type of $H$. 

### [@DF04, number 3.5.10]

We find a composition series for $A_4$, and argue that $A_4$ is not solvable. 

### [@DF04, number 4.1.9]

Assume $G$ acts transitively on the finite set $A$ and let $H$ be a normal subgroup of $G$. Let $\sO_1, \sO_2, \ldots, \sO_r$ be the distinct orbits of $H$ on $A$.

(a) $G$ permutes the sets $\sO_1, \sO_2, \ldots, \sO_r$ in the sense that for each $g \in G$ and each $i \in \{1, \ldots, r\}$ there is a $j$ such that $g\sO_i = \sO_j$, where $g\sO = \{g(a) : a \in \sO\}$. Then $G$ is transitive on $\{\sO_1, \ldots, \sO_r\}$. Furthermore, all orbits of $H$ on $A$ have the same cardinality.

(b) If $a \in \sO_1$, then $\abs{\sO_1} = \abs{H : H \cap \mathrm{Stab}_{G}(a)}$. Furthermore, $r = \abs{G : H\mathrm{Stab}_{G}(a)}$.

### [@DF04, number 4.4.20]

For any finite group $P$, let $d(P)$ be the minimum^[For example, $d(P) = 1$ if and only if $P$ is a nontrivial cyclic group and $d(Q_8) = 2$.] number of generators of $P$. Let $m(P)$ be the maximum of the integers $d(A)$ as $A$ runs^[For example, $m(Q_8) = 1$ and $m(D_8) = 2$.] over all *abelian* subgroups of $P$. Define the *Thompson subgroup* of $P$ as $$J(P) = \langle A : A \text{ is an abelian subgroup of $P$ with } d(A) = m(P)\rangle.$$

(a) $J(P)$ is a characteristic subgroup of $P$.
(b) For each of the following groups $P$, we exhaustively list all abelian subgroups $A$ of $P$ that satisfy $d(A) = m(P)$.

- $Q_8$
- $D_8$
- $D_{16}$
- $QD_{16}$ (the quasidihedral group of order $16$)

### Classification of simple groups of size less than 60
 
If a simple group has order less than $60$, then it is abelian.

*Given.* The set $\sS$ of all groups $G$ such that $1 \le \abs{G} \le 59$.

*To show.* Exhaustively, that each group $G$ in $\sS$ is abelian or not simple. 

*Demonstration.*

- The trivial group $\{1\}$ is not simple, by definition of simple as having no *nontrivial* proper normal subgroup.
- By Lagrange's theorem, groups of prime order are cyclic, therefore abelian.
- By the class equation, groups of prime power order $p^\alpha$ for $p$ prime and $\alpha \in \ZZ_{\ge 0}$ have non-trivial centers.
    - Either center of the group is the group itself and the group is abelian, or
    - or the center of the group is a (normal) nontrivial proper subgroup, in which case the group is not simple.
- By the lemma below, groups of order $pq$   (where $p$ and $q$ are primes) are not simple.
- By the lemma below, groups of order $p^2q$  (where $p$ and $q$ are primes) are not simple.
- What orders of groups in $\sS$ remain to be discussed?

order | prime factorization
----- | -------------------
24 | $2^3 \cdot 3$
30 | $2 \cdot 3 \cdot 5$
36 | $2^2 \cdot 3^2$
40 | $2^2 \cdot 3^2$
42 | $2 \cdot 3 \cdot 7$
48 | $2^4 \cdot 3$
60 | $2^2\cdot 3 \cdot 7$

**Lemma.** Groups of order $pq$ (where $p$ and $q$ are primes) are not simple. Moreover, groups of order $p^2q$ are also not simple.

### [@DF04, number 5.5.23]

Let $K$ and $L$ be groups, let $n$ be a positive integer, let $\rho \colon K \to S_n$ be a homomorphism and let $H$ be the direct product of $n$ copies of $L$. From [@DF04, number 5.1.8], we constructed an injective homomorphism $\psi$ from $S_n$ into $\Aut{H}$ by letting the elements of $S_n$ permute the $n$ factors of $H$. The compositions $\psi \circ \rho$ is a homomorphism from $G$ into $\Aut{H}$. The *wreath product* of $L$ by $K$ is the semidirect product $H \rtimes_\psi K$ with respect to this homomorphism and is denoted by $L \wr K$. Note this wreath product depends on the choice of permutation representation $\rho$ of $K$ --- if none is given explicitly, then $\phi$ is assumed to be the left regular representation of $K$.

(a) Assume $K$ and $L$ are finite groups and $\rho$ is the left regular representation of $K$. We find $\abs{L \wr K}$ in terms of $\abs{K}$ and $\abs{L}$.

(b) Let $p$ be a prime, let $K = L = Z_p$. Suppose $\rho$ is the left regular representation of $K$. Then $Z_p \wr Z_p$ is a non-abelian subgroup of order $p^{p+1}$ and is isomorphic to a Sylow $p$-subgroup of $S_{p^2}$. [The $p$ copies of $Z_p$ whose direct products makes up $H$ may be represented by $p$ disjoint $p$-cycles; these are cyclically permuted by $K$.]
