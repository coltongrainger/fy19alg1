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

### 10 push-ups [@DF04, number 6.2.4]

There are no simple groups of order $80, 351, 3875, 5313$.

*Demonstration.* Suppose for contradiction that $G$ is a simple group of order $80, 351, 3875$, or $5313$. Applying Sylow's theorem and counting elements, we see:

- $80 = 2^4 \cdot 5$. Then $n_2 = 5$ and $n_5 = 16$. How many elements in $G$ are *not* of order $5$? Precisely $80 - 64 = 16$. Since a Sylow $2$ subgroup contains $16$ elements (none of which have order $5$), we must have $n_2 = 1$, a contradiction.

- $351 = 3^3 \cdot 13$. Then $n_3 = 13$ and $n_13 = 27$. How many elements are not of order $13$? Precisely $351 = 324 = 27$. Yet each Sylow $3$-subgroup has $27$ elements. So $n_3$ must be $1$, a contradiction.

- $3875 = 5^3 \cdot 31$. Then $n_5 = 31$ and $n_31 = 125$. Now there are $3875 - 3750$ elements of order $31$. We're forced to accept $n_5 = 1$, a contradiction.

- $5313 = 3 \cdot 7 \cdot 11 \cdot 23$. Then $n_7 \ge 253$, $n_11 \ge 23$, and $n_23 \ge 231$. Then the number of non-identity elements in $G$ from the Sylow $7$, $11$, and $23$ subgroups must be greater than or equal to $6600$---that's too big!

### A special case of Burnside's N/C theorem [@DF04, number 6.2.5]

Let $G$ be a solvable group of order $pm$, where $p$ is a prime not dividing $m$, and let $P \in \Syl p G$. If $\N G P = P$, then $G$ has a normal subgroup of order $m$. (How is the hypothesis of the solvability of $G$ used?)

### [@DF04, number 6.2.6]

There are no simple groups of order $2205, 4125, 5103, 6545$, or $6435$. (Exploit subgroups of small index.)

### [@DF04, number 6.2.7]

There are no simple groups of order $1755$ or $5265$. (With Sylow $3$-subgroups, show $G \le S_{13}$. Then consider the normalizer of a Sylow $13$-subgroup.)

### [@DF04, number 6.2.10]

There are no simple groups of order $4095, 4389, 5313$, or $6669$. (Play $p$-subgroups off against each other.)

### [@DF04, number 6.2.12]

There are no simple groups of order $9555$. (Consider $Q \in \Syl {13} G$ and let $P \in \Syl 7 {\N G Q}$. Can it be that $Q \triangleleft \N G P$?)

### [@DF04, number 6.2.22]

Suppose over all pairs of distinct Sylow $p$-subgroups of $G$, we have $P$ and $R$ chosen with $\abs{P \cap R}$ maximal. Then $\N G {P \cap R}$ is **NOT** a $p$-group.

### [@DF04, number 6.2.25]

Let $G$ be a simple group of order $p^2qr$ where all $p, q, r$ are prime. Then $\abs{G} = 60$. (So $G \cong A_5$.)

\newpage

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

See also [@We40]:

> But this “practical” application is insignificant. What is crucial is there be *laws*. It is obvious that the residues of $m$ form an arithmetic progression of increment $m$, for if $a$ is a residue, it is the same for all $mx + a$; however it is beautiful and surprising that the prime numbers $p$ for which $m$ is a residue are precisely those which belong to certain arithmetic progressions of increment $4m$; for the others $m$ is a non-residue; and what is even more amazing, if one recalls on the other hand that the distribution of prime numbers in any given arithmetic progression $Ax + B$ (which one knows from Dirichlet will have an infinity of primes as long as $A$ and $B$ are relatively prime) does not follow any other known law other than a statistical one (the approximate number of primes which are less than $T$, which, for a given $A$, is the same for any $B$ prime to $A$) and appears, for each concrete case that one examines numerically, to be as “random” as a list of numbers generated by a roulette wheel.

## References
