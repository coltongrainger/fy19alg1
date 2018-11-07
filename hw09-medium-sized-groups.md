---
title: Groups of Medium Order
author: Colton Grainger
date: 2018-11-02
bibliography: /home/colton/Downloads/coltongrainger.bib
macros: true
tikz: true
---

\setcounter{section}{8}

## Assignment due 2018-11-07

### Counting elements [@DF04, number 6.2.4]

There are no simple groups of order $80, 351, 3875, 5313$.

*Demonstration.* Suppose for contradiction that $G$ is a simple group of order $80, 351, 3875$, or $5313$. Applying Sylow's theorem and counting elements, we see:

- $80 = 2^4 \cdot 5$. Then $n_2 = 5$ and $n_5 = 16$. How many elements in $G$ are *not* of order $5$? Precisely $80 - 64 = 16$. Since a Sylow $2$ subgroup contains $16$ elements (none of which have order $5$), we must have $n_2 = 1$, a contradiction.

- $351 = 3^3 \cdot 13$. Then $n_3 = 13$ and $n_{ 13 } = 27$. How many elements are not of order $13$? Precisely $351 - 324 = 27$. Yet each Sylow $3$-subgroup has $27$ elements. So $n_3$ must be $1$, a contradiction.

- $3875 = 5^3 \cdot 31$. Then $n_5 = 31$ and $n_{ 31 } = 125$. Now there are $3875 - 3750$ elements of order $31$. We're forced to accept $n_5 = 1$, a contradiction.

- $5313 = 3 \cdot 7 \cdot 11 \cdot 23$. Then $n_7 \ge 253$, $n_{ 11 } \ge 23$, and $n_{ 23 } \ge 231$. Then the number of non-identity elements in $G$ from the Sylow $7$, $11$, and $23$ subgroups must be greater than or equal to $6600$---too big! \qedsymbol

### A special case of Burnside's N/C theorem [@DF04, number 6.2.5]

Let $G$ be a solvable group of order $pm$, where $p$ is a prime not dividing $m$, and let $P \in \Syl p G$. If $\N G P = P$, then $G$ has a normal subgroup of order $m$. (How is the hypothesis of the solvability of $G$ used?)

### Exploiting subgroups of small index [@DF04, number 6.2.6]

There are no simple groups of order $2205, 4125, 5103, 6545$, or $6435$.

*Demonstration.* Suppose for contradiction that $G$ is a simple group of order $80, 351, 3875$, or $5313$. Applying Sylow's theorem and considering subgroups of small index, we see:

- $2205 = 3^2 \cdot 5 \cdot 7^2$. Now $n_7 = 15$, $n_5 \ge 21$, and $n_3 \ge 7$. We'll only need $n_7 = 15$ for a contradiction. Since $7^2 \nmid n_7 -1$, there exist distinct Sylow $7$-subgroups $P$ and $R$ such that $P \cap R$ is of index $7$ in $P$ and $R$. Now denoting $N = N_G(P \cap R)$, we see $P, R \le N$, thus $7^2 \mid \abs{N}$. 

    - Since $P$ and $R$ are distinct, we've got to have $\abs{N} > 7^2$. 
    - Now the minimum permissible index of a proper subgroup in $G$ is $\min\{k : \abs{G} \text{ divides } k!\} = 14$. 
    - The above two points imply $N$ has index greater than $14$ and less than $45$. Thus $\abs{N} = 3 \cdot 7^2$. 
    - Applying Sylow's theorem to $N$, $n_7(N) = 1$, which is absurd!---$P$ and $R$ are distinct Sylow $7$-subgroups of $N$.

- $4125 = 3 \cdot 5^3 \cdot 11$. Then $n_5 = 11$. But the minimal permissible index is $\min\{k : \abs{G} \text{ divides } k!\} = 15$. Consider $[G : N_G(P_{11})] = 11$ for a contradiction.

- $5103 = 3^6 \cdot 7$. Then $n_3 = 7$.  If $5103 \mid k!$, then $k \ge 15$. But $[G : N_G(P_3)] = 7$.

- $6545 = 5 \cdot 7 \cdot 11 \cdot 17$. Then $n_5 = 11$. If $6545 \mid k!$, then $k \ge 17$. Yet $[G : N_G(P_5)] = 11$.

- $6435 = 3^2 \cdot 5 \cdot 11 \cdot 13$. Again, $n_5 = 11$. If $6435 \mid k!$, then $k \ge 13$. Yet, again, $[G : N_G(P_5)] = 11$. \qedsymbol

### Permutation representations [@DF04, number 6.2.7]

There are no simple groups of order $1755$ or $5265$.

*Demonstration.* Suppose for contradiction that $G$ is a simple group of order $1755$ or $5265$. Applying Sylow's theorem and considering normalizers, we see:

- $1755 = 3^3 \cdot 5 \cdot 13$. Then $n_3 = 13$, $n_5 = 351$, and $n_{13} = 27$. Letting $G$ act by conjugation on a Sylow $3$-subgroup of index $13$, we identify $G$ with its image in $S_{ 13 }$ under the permutation representation afforded by the group action. Since $G$ has no index $2$ subgroup, $G \le A_{13}$. Let $H_{13} \in \Syl {13} G$. Because $27 = n_{13} = [G : N_G(H_{13})]$, we have $\abs{\N G {H_{13}}} = 65$. Yet also $\abs{N_{A_{13}}(H_{13})} = \frac12 \abs{N_{A_{13}}(H_{13})} = 78$---a contradiction! For $65 \nmid 78$.

- $5265 = 3^4 \cdot 5 \cdot 13$. Therefore $n_3 = 13$, $n_5 = 351$, and $n_{13} = 27$. As before, let $G$ act by conjugation on a Sylow $3$-subgroup of index $13$. Again, identify $G \le A_{13}$. Let $H_{13} \in \Syl {13} G$. Then $\abs{ N_G(H_{13}) } = 195$. But the normalizer of $H_{13}$ in $S_{13}$ has order $78$. We ought to have $N_G(H_{13}) \le N_{S_{13}}(H_{13})$, but Lagrange's theorem would imply $195 \mid 78$---a contradiction! \qedsymbol

### Playing Sylow subgroups [@DF04, number 6.2.10]

There are no simple groups of order $4095, 4389, 5313$, or $6669$.

*Demonstration.* Suppose for contradiction that $G$ is a simple group of order $4095, 4389, 5313$, or $6669$. Applying Sylow's theorem and considering different $p$-subgroups, we see:

- $4095 = 3^2 \cdot 5 \cdot 7 \cdot 13$. (This one's anomalous, unless I've made a mistake.) We're forced to have a Sylow $13$-normal subgroup.

    - By Sylow's theorem, $n_3 \in \{1, 7, 13, 91\}$, $n_5 \in \{1, 6, 21\}$, $n_7 \in \{1, 15\}$, yet $n_{13} = 1$.

- $4389 = 3 \cdot 7 \cdot 11 \cdot 19$. Let $Q \in \Syl {11} G$. Then $\N G Q = 3 \cdot 11$. Let $P \in \Syl 3 {\N G Q}$. Since $3 \nmid 11 - 1$, we have $P \triangleleft \N G Q$. So $Q \le \N G P$. By Lagrange's theorem, $11\mid \abs{\N G P}$. Observing that $P \in \Syl 3 G$, we must have $11 \nmid n_3$ (the number of Sylow $3$-subgroups is the index of the normalizer of $P$). It follows that $n_3 = 7$ or $19$.

    - If $n_3 = 7$, then $\abs{ \N G P} = 3 \cdot 11 \cdot 19$. So $Q \le \N G P$. Moreover, $Q \triangleleft \N G P$ (applying Sylow's theorem to $\N G P$. But then $\abs{ \N G P } \neq 3 \cdot 11$---a contradiction.
    - If $n_3 = 19$, then $\abs{ \N G P} = 3 \cdot 7 \cdot 11$. We see again that $Q \triangleleft \N G P$, leading to the same contradiction (which is what?).

- $5313  = 3 \cdot 7 \cdot 11 \cdot 23$. Let $Q \in \Syl {11} G$. Then $\abs{ \N G Q }  = 3 \cdot 7 \cdot 11$. Let $P \in \Syl 7 {\N G Q}$.

    - For $\abs{G} = 5313$, we must have $n_7(G) = 253$.
    - Applying Sylow's theorem to $\N G Q$, we see $P \triangleleft \N G Q$. So $Q  \le \abs{ \N G P}$. 
    - Thus $11$ divides $\N G P$. Moreover, $11 \nmid n_7$---a contradiction! For $11 \mid 253$.

- $6669 = 3^3 \cdot 13 \cdot 19$. We must have $n_{19} = 39$. Now let $Q \in \Syl{13} G$. 

    - Then $\abs{\N G Q } = 13 \cdot 19$. Let $P \in \Syl { 19} {\N G Q}$. 
    - Since $13 \nmid 19 -1$, we have a familiar $pq$ group, and $P \triangleleft \N G Q$. Therefore $Q \le \N G P$. 
    - By Lagrange, $13 \mid \abs{ \N G P}$. But $13 \nmid n_{19}$---a contradiction! For $13 \mid 39$. \qedsymbol

### Studying normalizers of Sylow subgroups [@DF04, number 6.2.12]

There are no simple groups of order $9555$.

*Demonstration*. Suppose $G$ is a simple group and $\abs{G}  = 9555 = 3 \cdot 5 \cdot 7^2 \cdot 13$. 

- We have $n_3 = 91$, $n_5 = 91$ or $1911$, $n_7 = 15$, and $n_{13} = 105$. 
- Let $Q \in \Syl { 13 } G$. Let $P \in \Syl 7 {\N G Q}$. 
- Then $\abs{\N G Q} = 91 = 7 \cdot 13$ as $n_{13} = 105$. 
- Sylow's theorem implies $n_7(\N G Q) = 1$, so $P \triangleleft \N G Q$.
    - Thence $Q \le \N G P$.
- Let $P^* \in \Syl 7 G$ such that $P \le P^*$. 
    - Now $7 = \abs{ P } \lneq \abs{ P^*} = 7^2$. 
    - Thus $\N {P^*} P = P^*$.
    - Moreover $\N {P^*} P \le \N G P$.
- It follows that $\langle Q, P^*\rangle \le \N G P$.
- By Lagrange's theorem then $7^2 \cdot 13 \mid \abs{\N G P}$.
    - Applying Sylow's theorem to the three cases for the order of $\N G P$ (it must be $7^2 \cdot 13$, $7^2 \cdot 5 \cdot 13$, or $3 \cdot 7^2 \cdot 13$) we see $Q \triangleleft \N G P$. 
    - So $\N G P \le \N G Q$.
    - By Lagrange, $7^2 \cdot 13 \mid \abs{ \N G Q}$.
    - Then $[ G : \N G Q] \mid 3 \cdot 5$. 
    - But $Q$ is a Sylow $13$-subgroup, and $n_{13} = 105$, a contradiction. \qedsymbol

### [@DF04, number 6.2.22]

Suppose over all pairs of distinct Sylow $p$-subgroups of $G$, we have $P$ and $R$ chosen with $\abs{P \cap R}$ maximal. Then $\N G {P \cap R}$ is **NOT** a $p$-group.

### [@DF04, number 6.2.25]

Let $G$ be a simple group of order $p^2qr$ where all $p, q, r$ are prime. Then $\abs{G} = 60$. (So $G \cong A_5$.)

### [@DF04, number 6.3.10]

We aim to exhibit an outer automorphism of $S_6$. Let 
\begin{align*}
t_1' &= (1\, 2)(3\, 4)(5\, 6), \\
t_2' &= (1\, 4)(2\, 5)(3\, 6),\\
t_3' &= (1\, 3)(2\, 4)(5\, 6),\\
t_4' &= (1\, 2)(3\, 6)(4\, 5),\\
t_5' &= (1\, 4)(2\, 3)(5\, 6).
\end{align*}

We claim $t_1', \ldots, t_5'$ satisfy the following relations:
\begin{align*}
(t_i')^2 &= 1 \text{ for all $i$},\\
(t_i't_j')^2 &= 1 \text{ for all $i$ and $j$ with $\abs{i - j} \ge 2$, and} \\
(t_i't_{i+1}')^3 &=1 \text{ for all $i \in \{1,2,3,4\}$}
\end{align*}

Further, $S_6 = \langle t_1', \ldots, t_5' \rangle$ and the map 
$$(1\,2) \mapsto t_1', \quad (2\, 3) \mapsto t_2', \quad (3\, 4) \mapsto t_3', \quad (4\, 5) \mapsto t_4', \quad (5\,6) \mapsto t_5'$$ 
extends to an automorphism of $S_6$ (which is not inner).

### [@DF04, number 6.3.12]

Let $S$ be a set and $c$ a positive integer. Formulate the notion of a free nilpotent group on $S$ of nilpotence class $c$ and prove it has the appropriate universal property with respect to the nilpotent groups of class less than or equal to $c$.

### [@DF04, number 6.3.14]

Prove that $G = \langle x, y : x^3 = y^3 = (xy)^3 = 1\rangle$ is an infinite group as follows. Let $p$ be a prime congruent to $1 \mod 3$ and let $G_p$ be the non-abelian group of order $3p$. Let $a,b \in G_p$ with $\abs{a} = p$ and $\abs{b} = 3$. 

- Both $ab$ and $ab^2$ have order $3$.
- $G_p$ is a homomorphic image of $G$.
- $G$ is therefore an infinite group, as there are infinitely many primes $p \equiv 1 \mod 3$. 

## References
