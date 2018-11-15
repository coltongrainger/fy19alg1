---
title: TODO and to-revise
author: Colton Grainger
date: 2018-10-05
macros: true
bibliography: /home/colton/Downloads/coltongrainger.bib
revised: 2018-11-13
tikz: true
---

### Minimal and maximal subgroups

Suppose $N$ is a nontrivial abelian subgroup of $G$, minimal with the property that it is normal in $G$. Let $H$ be a proper subgroup of $G$ such that $NH=G$. The intersection of $N$ with $H$ is trivial and $H$ is a maximal subgroup of $G$.

### [@DF04, number 3.1.40]

\newcommand{\h}[1]{\overline{#1}}

Let $G$ be a group, let $N$ be a normal subgroup of $G$ and let $\h G = G/N$. The elements $\h x$ and $\h y$ commute in $\h G$ if and only if $x^{-1}y^{-1}xy  \in N$.

### [@DF04, number 3.4.7]

If $G$ is a finite group and $H \triangleleft G$, there is a composition series of $G$ one of whose terms in $H$. 

### [@DF04, number 3.4.11]

If $H$ is a nontrivial normal subgroup of the solvable group $G$, there is a nontrivial subgroup $A$ of $H$ with $A \triangleleft G$ and $A$ abelian. 

### [@DF04, number 3.5.10]

We find a composition series for $A_4$, and argue that $A_4$ is not solvable. 

### [@DF04, number 4.1.9]

Assume $G$ acts transitively on the finite set $A$ and let $H$ be a normal subgroup of $G$. Let $\sO_1, \sO_2, \ldots, \sO_r$ be the distinct orbits of $H$ on $A$.

(a) $G$ permutes the sets $\sO_1, \sO_2, \ldots, \sO_r$ in the sense that for each $g \in G$ and each $i \in \{1, \ldots, r\}$ there is a $j$ such that $g\sO_i = \sO_j$, where $g\sO = \{g(a) : a \in \sO\}$. Then $G$ is transitive on $\{\sO_1, \ldots, \sO_r\}$. Furthermore, all orbits of $H$ on $A$ have the same cardinality.

(b) If $a \in \sO_1$, then $\abs{\sO_1} = \abs{H : H \cap \mathrm{Stab}_{G}(a)}$. Furthermore, $r = \abs{G : H\mathrm{Stab}_{G}(a)}$.

### [@DF04, number 4.4.20]

For any finite group $P$, let $d(P)$ be the minimum^[For example, $d(P) = 1$ if and only if $P$ is a nontrivial cyclic group and $d(Q_8) = 2$.] number of generators of $P$. Let $m(P)$ be the maximum of the integers $d(A)$ as $A$ runs^[For example, $m(Q_8) = 1$ and $m(D_8) = 2$.] over all *abelian* subgroups of $P$. Define the *Thompson subgroup* of $P$ as $$J(P) = \langle A : A \text{ is an abelian subgroup of $P$ with } d(A) = m(P)\rangle.$$

(a) $J(P)$ is a characteristic subgroup of $P$.
(b) For each of the following groups $P$, we exhaustively list all abelian subgroups $A$ of $P$ that satisfy $d(A) = m(P)$: $Q_8$, $D_8$, $D_{16}$, $QD_{16}$ (the quasidihedral group of order $16$).

### [@DF04, number 6.2.25]

Let $G$ be a simple group of order $p^2qr$ where all $p, q, r$ are prime. Then $\abs{G} = 60$.

*Proof sketch.* By Feit-Thomposon, $G$ must be of even order. Suppose that $p$ is not $2$. Then by "Erik's lemma", if $G$ is a group of order $2k$ where $k$ is odd, then $G$ has a normal subgroup. Considering that $p^2qr$ could be written as $2k$ with $k$ odd if $p \neq 2$, we must have $p = 2$. 

Without loss of generality, assume $q < r$. We can thus bound $n_r \in \{ 2q, 4q\}$. We want to show $n_r  = 2q$. If we *could do so*, then we'd be able to consider $P \in \Syl 2 G$. From here, we *could* argue that $p^2 \equiv 1 \pmod q$. Thence we'd find $q \mid (p-1)$ or $q \mid (p + 1)$. Lastly, we'd observe $q = 2 + 1$. Moreover, if we could limit $n_r$ to be $2q$, then we'd be forced by congruence, namely $rn + 1 = 2q$, to accept that $r = 5$. \qedsymbol

### [@DF04, number 5.5.23]

Let $K$ and $L$ be groups, let $n$ be a positive integer, let $\rho \colon K \to S_n$ be a homomorphism and let $H$ be the direct product of $n$ copies of $L$. From [@DF04, number 5.1.8], we constructed an injective homomorphism $\psi$ from $S_n$ into $\Aut{H}$ by letting the elements of $S_n$ permute the $n$ factors of $H$. The compositions $\psi \circ \rho$ is a homomorphism from $G$ into $\Aut{H}$. The *wreath product* of $L$ by $K$ is the semidirect product $H \rtimes_\psi K$ with respect to this homomorphism and is denoted by $L \wr K$. Note this wreath product depends on the choice of permutation representation $\rho$ of $K$ --- if none is given explicitly, then $\phi$ is assumed to be the left regular representation of $K$.

(a) Assume $K$ and $L$ are finite groups and $\rho$ is the left regular representation of $K$. We find $\abs{L \wr K}$ in terms of $\abs{K}$ and $\abs{L}$.

(b) Let $p$ be a prime, let $K = L = Z_p$. Suppose $\rho$ is the left regular representation of $K$. Then $Z_p \wr Z_p$ is a non-abelian subgroup of order $p^{p+1}$ and is isomorphic to a Sylow $p$-subgroup of $S_{p^2}$. [The $p$ copies of $Z_p$ whose direct products makes up $H$ may be represented by $p$ disjoint $p$-cycles; these are cyclically permuted by $K$.]


### [@DF04, number 6.1.20]

Let $p$ be a prime, let $P$ be a $p$-subgroup of the finite group $G$, let $N$ be a normal subgroup of $G$ whose order is relatively prime to $p$, and let $\bar{G} = G/N$. 

(a) With Frattini's argument, $\N { \bar{G} } { \bar{P} } = \overline{\N G P}$.
(b) From above, $\N{\bar{G}}{\bar{P}} = \overline{\N G P}$.

<!---
### Characters of finite abelian groups [@CoCharthy]

2. Let $G$ be a finite nonabelian simple group. Show the only group homomorphism $\chi\colon G \to S_1$ is the trivial map.
--->

### [@DF04, number 6.3.12]

Let $S$ be a set and $c$ a positive integer. Formulate the notion of a free nilpotent group on $S$ of nilpotence class $c$ and prove it has the appropriate universal property with respect to the nilpotent groups of class less than or equal to $c$.

*Formulation*. The free nilpotent group on $S$ of nilpotence class $c$, denoted $N_c(S)$, ought to be given by the presentation $\langle S \vert \gamma_c(F(S)) \rangle$ where $\gamma_c(F(S)) = [F(S), \gamma_{c-1}(S)]$. From the presentation, there's a surjection $\pi \colon F(S) \to N_c(S)$.

*Universal property*. Let $G$ be a nilpotent group of class $c$. Let $\phi \colon S \to G$ be a map of sets. Then there's a unique $\Psi \colon N_c(S) \to G$ such that the following diagram commutes:

\begin{center}
\begin{tikzpicture}[every node/.style={fill=white}] % white fill keeps lines from running into labels
\draw[->] (-2,2) -- (1.3,2);
\draw[->] (-2,2) -- (1.3,0.2);
\draw[->,dashed] (2,2) -- (2,0.5);

\node at (-2,2) {$S$};
\node at (0,2.3) {$\pi\circ \iota$};
\node at (2,2) {$N_c(S)$};
\node at (2,0) {$G$};
\node at (2.5,1) {$\exists ! \Psi$};
\node at (-0.5,0.7) {$\phi$};

\end{tikzpicture}
\end{center}

*Proof.*^[I consulted Erik, Hunter, Chris, and <https://terrytao.wordpress.com/2009/12/21/the-free-nilpotent-group/> for this problem. The proof here is hardly sufficient, I'll admit---something to revise.] Observe $\Phi(\gamma_c(F(S))) \le \gamma_{c}(G)$ as $\Phi([F(S), \gamma_{c-1}(F(S))]) = [\Phi(F(S)), \Phi(\gamma_{c-1}(F(S)))] \le \gamma_c (G) = 1$. \qedsymbol

### [@DF04, number 6.3.14]

Prove that $G = \langle x, y : x^3 = y^3 = (xy)^3 = 1\rangle$ is an infinite group as follows. Let $p$ be a prime congruent to $1 \mod 3$ and let $G_p$ be the non-abelian group of order $3p$. Let $a,b \in G_p$ with $\abs{a} = p$ and $\abs{b} = 3$. 

- Both $ab$ and $ab^2$ have order $3$.
- $G_p$ is a homomorphic image of $G$.
- $G$ is therefore an infinite group, as there are infinitely many primes $p \equiv 1 \mod 3$. 

