---
title: Revisions for Midterm 1
author: Colton Grainger
date: 2018-10-05
macros: true
bibliography: /home/colton/Downloads/coltongrainger.bib
revised:
---

### [@DF04, number 1.6.23]

Let $G$ be a finite group which possesses an automorphism $\sigma$ such that $\sigma(g) = g$ if and only if $g=1$. If $\sigma^2$ is the identity map from $G$ to $G$, then $G$ is abelian.^[*Hint*. Every element of $G$ can be written in the form $x^{-1}\sigma(x)$. Apply $\sigma$ to such an expression.]

### [@DF04, number 2.4.16]

If $H$ is a proper subgroup of the finite group $G$, then there is a maximal subgroup of $G$ containing $H$. Moreover, if $G = \langle x\rangle$ is a cyclic subgroup of order $n \ge 1$, then a subgroup $H$ is maximal if and only if $H = \langle x^p \rangle$ for some prime $p$ dividing $n$.

### Maximal subgroups in a finite group

A finite group with no more that two maximal subgroups is cyclic.

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
