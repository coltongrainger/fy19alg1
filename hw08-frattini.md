---
title: Nilpotent Groups & Finite Abelian Groups 
author: Colton Grainger
date: 2018-10-28
bibliography: /home/colton/Downloads/coltongrainger.bib
macros: true
tikz: true
---

\setcounter{section}{6}

## Assignment due 2018-10-31

### [@DF04, number 5.2.8]

Let $A$ be a finite abelian group (written multiplicatively) and let $p$ be a prime. Suppose $$A^p = \{ a^p : a \in A\} \quad\text{ and }\quad A_p = \{x : x^p= 1\}\},$$ so that $A^p$ and $A_p$ are the image and kernel of the $p$th power map $$\phi \colon A \to A \quad \text{ such that }\quad \phi x \mapsto x^p.$$

(a) Prove that $A/A^p \cong A_p$ by showing both are elementary abelian and of the same order.
(b) Prove that the number of subgroups of $A$ of order $p$ equals the number of subgroups of $A$ of index $p$, by reducing to the case where $A$ is an elementary abelian $p$-group.

^[<https://math.stackexchange.com/questions/413470/>, <https://math.stackexchange.com/questions/142589/>]

[@Pr11, page 3-5]

### [@DF04, number 5.2.14]

For any group $G$ define the *dual group* $\hat{G}$ of $G$ to be the set of all homomorphisms from $G$ into the multiplicative group of roots of unity in $\CC$. Define a group operation in $\hat{G}$ by pointwise multiplication of functions: if $\chi$ and $\psi$ are homomorphisms from $G$ into the group of roots of unity, then $\chi\psi$ is the homomorphism given by $( \chi\psi)(g) = \chi(g)\psi(g)$ for all $g \in G$.

(a) Show that this operation on $\hat{G}$ makes $\hat{G}$ into an abelian group. 

    Hint: show that the identity is the map $g \mapsto 1$ for all $g \in G$ and that the inverse of $\chi \in \hat{G}$ is the map $g \mapsto \chi(g)^{-1}$.

(b) If $G$ is a finite abelian group, prove that $\hat{G} \cong G$. 

    Hint: Write $G$ as $\langle x_1\rangle \times \cdots \times \langle x_r \rangle$ and if $n_i = \abs{x_i}$, define $\chi_i$ to be the homomorphism which sends $x_i$ to $e^{2\pi i/n_i}$ and sends $x_j$ to $1$ for all $j \neq i$. Then show that $\chi_i$ has order $n_i$ in $\hat{G}$ and that $\hat{G} = \langle \chi_1 \rangle \times \cdots \times \langle x_r \rangle$.

[@CoCharacters]

### [@DF04, number 6.1.7]

Subgroups and quotient groups of nilpotent groups are^[Even in the infinite case.] nilpotent. We exhibit a group $G$ which possesses a normal subgroup $H$ such that both $H$ and $G/H$ are nilpotent but $G$ is not nilpotent.

[@CoSolvable]

### [@DF04, number 6.1.10]

$D_{2n}$ is nilpotent if and only if^[Hint: if $G$ is a finite group, $\{p_i\}_1^s$ is the set of distinct primes dividing $\abs{G}$, and $P_i \in \Syl{p_i}G$, then $P_i \triangleleft G$. Recall that [@DF04, page 192] a finite group $G$ is nilpotent if and only if whenever $a,b \in G$ with $(\abs{a},\abs{b}) = 1$, then $ab = ba$.] $n$ is a power of $2$.

### [@DF04, number 6.1.20]

Let $p$ be a prime, let $P$ be a $p$-subgroup of the finite group $G$, let $N$ be a normal subgroup of $G$ whose order is relatively prime to $p$, and let $\bar{G} = G/N$. 

(a) With Frattini's argument, $\N { \bar{G} } { \bar{P} } = \overline{\N G P}$.
(b) From above, $\N{\bar{G}}{\bar{P}} = \overline{\N G P}$.

TODO

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

*Given.* A finite solvable group $G$ and a minimal normal subgroup $M \triangleleft G$.

*To prove.* $M$ is an elementary abelian $p$-group, by arguing the commutator subgroup $M'$ is trivial and finding a $p$ for which the image of $M$ under the $p$th power map $M^p$ is also trivial. 

*Proof.* Since $M'$ and $M^p$ are characteristic subgroups of $M$, it suffices only to prove that $M \neq M'$ and, for a prime $p$, $M \neq M^p$. By the diamond isomorphism theorem, $$G/G' \cong M/M',$$ which, given the hypothesis that $G$ is solvable, implies $$\{1 \cdot G' \} \lneq G/G', \quad \text{ i.e., } \quad \{1 \cdot M' \} \lneq  M / M'.$$

\begin{center}
\begin{tikzpicture}[every node/.style={fill=white}] % white fill keeps lines from running into labels

	\draw[double] (0,6) -- (2,4);
    \draw (2,4) -- (0,2);
    \draw (0,6) -- (-2,4);
	\draw[double]  (-2,4) -- (0,2);

	\node at (0,6) {$G$};
	\node at (2,4) {$G'$};
	\node at (-2,4){$M$};
	\node at (0,2) {$M' = \underbrace{M \cap G'}_{\text{verify}}$};
\end{tikzpicture}
\end{center}

We see $M'$ is a proper normal subgroup of $M$. By the minimal normal hypothesis, $M'$ must be trivial. It follows that $M$ is abelian.

Now to find $p$ such that $M^p$ is also trivial. Take the smallest prime $p$ dividing the order $\abs{M}$. By Cauchy's theorem, there's a cyclic group $\langle x\rangle$ of order $p$ in $M$. But then there's $x' \in \langle x \rangle$ such that $x' \in M \setminus M^p$. We see $$M \neq M^p\quad\text{ thus }\quad M^p = \{1\}.$$ We conclude $M$ is elementary abelian. \qedsymbol

### Classifying simple groups (without Feit--Thompson!)

Suppose $G$ is a group and $60 < \abs{G} \le 100$. If $G$ is simple, then $G$ is abelian.

*Proof.* Consider $G$ a group of order $n \in \{61, \ldots, 100\}$. We'll cast out from consideration all groups that are either abelian, or that contain nontrivial proper normal subgroups.

- We won't consider any $p$-group $P$ as 

    - either $P$ is cyclic (thus abelian) or
    - $P$ is nilpotent (thus solvable, thus not simple).

- We won't consider any group $H$ of order $pq$, $p^2q$, or $pqr$, for primes $p, q, r$, as

    - by Sylow's theorem, each such $H$ has a nontrivial proper normal subgroup.

- We won't consider any group $J$ of order $p^a q^b$, for $p, q$ primes, as

    - we'll then have reason to prove Burnside's lemma in [DF04, chapter 12],
    - thus showing all groups of order $p^a q^b$ are solvable (thus not simple).

What remains?

- $\abs{G} = 84 = 2^2 \cdot 3 \cdot 7$.

    - By Sylow's theorem, $n_7 = 1$, so $H_7 \triangleleft G$, thus $G$ is not simple.

- $\abs{G} = 90 = 2\cdot 3^2 \cdot 5$.

    - Now $n_5 \in \{1,6\}$, $n_3 \in \{1,10\}$, and $n_2 \in \{1,3,5,9,15,45\}$.
    - Suppose each $n_i > 1$ or we're done.
    - Counting nontrivial elements, we're forced to accept the $3$-subgroups of the form $(\ZZ/3\ZZ)^2$.
    - By above, we're also forced to accept $45$ Sylow $2$-subgroups, as $$90= \abs{G} = \underbrace{1}_{\text{order }1} + \underbrace{45}_{2} + \underbrace{20}_{3} + \underbrace{24}_{6}.$$
    - So consider $G$ acting by conjugation on the coset space $G/H_5$.
        - We've the permutation representation $\phi \colon G \to S_6$. 
        - Suppose $\ker \phi = N$.
        - What's $N$?
            - $N \le N_G(H_5)$.
            - $N \neq G$ as then $H_5 \triangleleft G$, a contradiction.
            - So $N$ must be $\{1\}$.
        - Then "$G \le S_6$" by identification of $G$ with its image.
            - Wherefore $G \le A_6$ since $G$ has no subgroup of index $2$
            - But $A_6$ cannot have a subgroup of index $4$ as $360 \nmid 4!$,
            - i.e., there's only a trivial action of $A_6$ on the coset space $A_6/G$
            - which gives *another contradiction.*
        - Therefore $N \neq \{1\}$.
            - So $\{1\} < \ker \phi \triangleleft G$.
    - So if $\abs{G} = 90$, then $G$ has a normal subgroup.

Given the hypotheses, we've demonstrated that if $G$ is simple, then $G$ is abelian. \qedsymbol

## References
