---
title: Nilpotent Groups & Finite Abelian Groups 
author: Colton Grainger
date: 2018-10-28
bibliography: /home/colton/Downloads/coltongrainger.bib
macros: true
tikz: true
---

\setcounter{section}{6}

\providecommand{\Syl}[2]{\mathrm{Syl}_{ #1 }\left( #2 \right)}
\providecommand{\N}[2]{N_{ #1 }\left( #2 \right)}
\providecommand{\C}[2]{C_{ #1 }\left( #2 \right)}
\providecommand{\Aut}[1]{\mathrm{Aut}\left({ #1 }\right)}

## Assignment due 2018-10-31

### [@DF04, number 5.2.8]

Construct a nonabelian group of order $75$. Classify all groups of order $75$ (there are three of them).^[Hint: show the non-abelian group is unique, as in [@DF04, number 5.2.6]. Also not the classification of groups of order $pq^2$ with $p$ not dividing $q-1$ is quite similar.]

### Classifying the groups of order $60$ [@DF04, number 5.2.14]

Let $G$ be a group of order $60$, let $P$ be a Sylow $5$-subgroup of $G$, and let $Q$ be a Sylow $3$-subgroup of $G$.

(a) If $P$ is not normal in $G$, then $G \cong A_5$.

(b) If $P \triangleleft G$ but $Q$ is not normal in $G$, then^[Hint: Show in this case that $P \le Z(G)$, $G/P \cong A_4$, and a Sylow $2$-subgroup $T$ of $G$ is normal and $TQ  \cong A_4$.] $G \cong A_4 \times Z_5$.

(c) If both $P$ and $Q$ are normal in $G$, then $G \cong Z_15 \rtimes T$, where $T \cong Z_4$ or $Z_2 \times Z_2$. In this case, there are six isomorphism types when $T$ is cyclic (one abelian) and there are five isomorphism types when $T$ is the Klein $4$-group (one abelian).^[Hint: Use the same ideas as in the classifications of groups of order $20$ and $30$.]

### [@DF04, number 6.1.7]

Subgroups and quotient groups of nilpotent groups are^[Even in the infinite case.] nilpotent. We exhibit a group $G$ which possesses a normal subgroup $H$ such that both $H$ and $G/H$ are nilpotent but $G$ is not nilpotent.

### [@DF04, number 6.1.10]

$D_{2n}$ is nilpotent if and only if^[Hint: if $G$ is a finite group, $\{p_i\}_1^s$ is the set of distinct primes dividing $\abs{G}$, and $P_i \in \Syl{p_i}G$, then $P_i \triangleleft G$. Recall that [@DF04, page 192] a finite group $G$ is nilpotent if and only if whenever $a,b \in G$ with $(\abs{a},\abs{b}) = 1$, then $ab = ba$.] $n$ is a power of $2$.

### [@DF04, number 6.1.20]

Let $p$ be a prime, let $P$ be a $p$-subgroup of the finite group $G$, let $N$ be a normal subgroup of $G$ whose order is relatively prime to $p$, and let $\bar{G} = G/N$. 

(a) With Frattini's argument, $\N { \bar{G} } { \bar{P} } = \overline{\N G P}$.
(b) From above, $\N{\bar{G}}{\bar{P}} = \overline{\N G P}$.

### [@DF04, number 6.1.24]

Say an element $x$ of $G$ is a *nongenerator* if for every proper subgroup $H$ of $G$, $\langle x, H \rangle$ is also a proper subgroup of $G$. If $\abs{G} > 1$, then $\Phi(G)$ is the set of nongenerators of $G$.

**Definition.** For any group $G$, the *Frattini subgroup* of $G$ (denoted by $\Phi(G)$) is defined to be the intersection of all the maximal subgroups of $G$ (if $G$ has no maximal subgroups, set $\Phi(G) = G$).

### [@DF04, number 6.1.25]

With $G$ be a finite group, $\Phi(G)$ is nilpotent.^[Hint: Use Frattini's Argument to prove that every Sylow subgroup of $\Phi(G)$ is normal in $G$.]

### [@DF04, number 6.1.26]

Suppose $p$ is a prime, $P$ is a finite $p$-group and define $\bar{P} = P / \Phi(P)$.

(a) $\bar{P}$ is an elementary abelian $p$-group.^[Hint: demonstrate first $P' \le \Phi(P)$ and that $x^p \in \Phi(P)$ for all $x \in P$.]

(b) If $N$ is any normal subgroup of $P$ such that $P/N$ is elementary abelian, then $\Phi(P) \le N$. We state this as a universal property with homomorphisms and commutative diagrams.

(c) Let $\bar{P}$ be elementary abelian of order $p^r$. From [@DF04, number 6.1.24], it follows that:

    - If $\bar{x}_1, \ldots, \bar{x}_r$ are any basis for the $r$-dimensional vector space $\bar{P}$ over $\FF_p$ and if $x_i$ is any element of the coset $\bar{x}_i$, then $P = \langle x_1, \ldots, x_r\rangle$.

    - Conversely,^[We assume that every minimal generating set for an $r$-dimensional vector space has $r$ elements, i.e., every minimal basis has $r$ elements.] if $y_1, \ldots, y_s$ is any set of generators for $P$, then $s \ge r$. 

    - Now *Burnside's Basis Theorem* follows: a set $y_1, \ldots, y_s$ is a minimal generators set for $P$ if and only if $\bar{y}_1,\ldots, \bar{y}_s$ is a basis of $\bar{P}$.
    
    - Any minimal generating set for $P$ has $r$ elements.

(d) If $\bar{P}$ is cyclic, then $P$ is too. It follows that if $P/P'$ is cyclic, then so is $P$.

(e) Let $\sigma$ be any automorphism of $P$ of prime order $q$ with $q \neq p$. If $\sigma$ fixes the coset $x\Phi(P)$ then $\sigma$ fixes some element of this coset.^[Hint 1: Note that since $\Phi(P)$ is characteristic in $P$, every automorphism of $P$ induces an automorphism of $P/\Phi(P)$. Hint 2: Use the observation that $\sigma$ acts as a permutation of order $1$ or $q$ on the $p^a$ elements in the coset $x\Phi(P)$.]

(f) With parts (c) and (e), every nontrivial automorphism of $P$ of order prime to $p$ induces prime a nontrivial automorphism on $P/\Phi(P)$. Any group of automorphisms of $P$ which has order prime to $p$ is isomorphic to a subgroup of $\Aut{\bar{P}} = \mathrm{GL}_r(\FF_p)$.

### [@DF04, number 6.1.31]

For any group $G$ a *minimal normal subgroup* is a normal subgroup $M$ of $G$ such that the only normal subgroups of $G$ which are contained in $M$ are $1$ and $M$. We'll show^[Hint: If $M$ is a minimal normal subgroup of $G$, consider its characteristic subgroups: $M'$ and $\langle x^p : x \in M\rangle$.] every minimal normal subgroup of a finite solvable group is an elementary abelian $p$-group for some prime $p$. 

### Classifying simple groups (without Feit--Thompson!)

If order of group is greater than $60$ and less than or equal to $100$, then it is only simple if it is abelian.

## References
