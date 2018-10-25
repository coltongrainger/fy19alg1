---
title: Conjugacy classes and automorphisms
author: Colton Grainger (MATH 6130 Algebra)
date: 2018-10-05
bibliography: /home/colton/Downloads/coltongrainger.bib
macros: true
tikz: true
---

\providecommand{\Aut}[1]{\mathrm{Aut}\left({ #1 }\right)}

\setcounter{section}{5}

## Assignment due 2018-10-17

### [@DF04, number 4.2.9]

If $p$ is a prime and $G$ is a group of order $p^\alpha$ for some $\alpha \in \NN$, then every subgroup of index $p$ is normal in $G$. Therefore every group of order $p^2$ has a normal subgroup of order $p$.

*Given.* A group $G$ of order $p^\alpha$ with $p$ prime and $\alpha \in \NN$.

*To prove.* Every subgroup of index $p$ is normal in $G$.

*Proof à la carte.* (We proved this in class as an application of the third isomorphism theorem; it's also in the text as a corollary of Cayley's theorem.)

Suppose $H \le G$ and $\abs{G : H} = p$. Let $\pi_H$ be the permutation representation $\pi \colon G \to S_G$ afforded by left multiplication of the cosets of $H$ in $G$, let $K = \ker \pi_H$, and let $\abs{H:K} = k$. Now $\abs{G:K} = \abs{G:H}\abs{H:K} = pk$. Since $H$ has $p$ left cosets, $G/K$ is isomorphic to a subgroup of $S_p$ be the first isomorphism theorem. By Lagrange's theorem, $pk = \abs{G/K}$ divides $p = \abs{G/H}$. Thus $k$ divides $(p-1)!$ But all the prime divisors of $k$ are at least as large as $p$. With $p$ chosen minimally, we're forced to accept $k = 1$, so $K = H$, and therefore $H \triangleleft G$. \qedsymbol

*Given.* A group $G$ of order $p^2$.

*To prove.* There exists a subgroup $H$ of $G$ where $\abs{H} = p$.

*Proof.* By Cauchy's theorem, there's an element of order $p$ in $G$, call it $x$. Now $\abs{G : \langle x \rangle} = p^2/p = p$. By the result à la carte, $\langle x \rangle$ is normal in $G$. \qedsymbol

### [@DF04, number 4.2.11]

Let $G$ be a finite group and let $\pi \colon G \to S_G$ be the left regular representation. If $x$ is an element of $G$ of order $n$ and $\abs{G} = mn$, then $\pi(x)$ is a product of $m$ $n$-cycles. Therefore $\pi(x)$ is an odd permutation if and only if $\abs{x}$ is even and $\frac{\abs{G}}{\abs{x}}$ is odd.

*Given.* A finite group $G$ of order $mn$, an element $x$ of order $n$, and the left regular representation $\pi \colon G \to S_G$, arising from the action of $G$ on itself by left multiplication.

*To prove.* The permutation $\pi(x)$ is a product of $m$ disjoint $n$-cycles.

*Proof.* Since $x$ has order $n$, the cyclic subgroup $\langle x \rangle$ has index $mn/n = m$ in $G$. Now choose $m$ representatives $\{g_i\}_{i=1}^m$ from the *right* cosets $\langle x\rangle \backslash G$. Observe that each coset $\langle x \rangle g_i$ is recovered by $n$ repeated left multiplications by $x$, that is, $$\langle x \rangle g_i = \bigcup_{j \in \ZZ} x^j g_i  = \bigsqcup_{j=1}^n x_j g_i \text{ for all } g_i.$$ 

We'll now argue $\pi(x)$ is a product of $m$ $n$-cycles by writing each element of $G$ in the form $\pi^j(x) ( g_i ) = x^j g_i$ and counting. Our goal is to recover $G$ as a disjoint union of the images of the representatives $p_1, \ldots, p_m$ under the action of $\pi^j(x)$ for $j = 1, \ldots, n$. So, $$G = \bigsqcup_{i=1}^m \bigsqcup_{j=1}^n x^j g_i = \bigsqcup_{i=1}^m \bigsqcup_{j=1}^n \pi^j(x)(g_i).$$ We conclude that $\pi(x)$ is the product of $m$ $n$-cycles. \qedsymbol

*Corollary.* For a finite group $G$, a left regular representation $\pi \colon G \to S_G$, and an element $x \in G$, the permutation $\pi(x)$ is odd if and only if $\abs{x}$ is even and $\abs{G}/\abs{x}$ is odd.

*Proof.* With the lemma below, $\pi(x)$ is odd if and only if its cycle type contains an odd number of even integers, which occurs precisely when the disjoint cycle representation of $\pi(x)$ is a factorization containing an odd number of even length cycles. Well, borrowing notation from the proof above, $$\text{ the cycle type of $\pi(x)$ is $\underbrace{(n,n, \ldots, n)}_{m \text{ times}}$.}$$ So $\pi(x)$ is odd if and only if $\abs{G}/\abs{x} = m$ is odd and $\abs{x} = n$ is even. \qedsymbol

**Lemma**. A permutation $\sigma \in S_G$ is odd if an only if an odd number of the $\tau_i$ in the disjoint cycle decomposition of $\sigma$ have even cycle length.

*Proof*. The sign of a permutation is a group homomorphism $\epsilon \colon S_G \to \{-1,1\}$. Now for $\sigma \in S_G$ with disjoint cycle decomposition $\sigma = \tau_1 \tau_2 \cdots \tau_m$, we have $\epsilon(\sigma) = -1$ if and only if $\epsilon(\tau_1)\epsilon(\tau_2) \cdots \epsilon(\tau_m) = -1$ if and only if an odd number of the $\tau_i$ are of even cycle length. \qedsymbol

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

*Given.* Primes $p$ and $q$ (WLOG $p < q$), a group $G$ of order $pq$, a group $K$ of order $p^2q$.

*To prove.* Both $G$ and $K$ posses normal nontrivial proper subgroups.

*Proof.*

### [@DF04, number 4.3.13]

The only finite group with exactly two conjugacy classes is isomorphic to the cyclic group $C_2$. 

(That $C_2$ has two conjugacy classes is clear: they are the singletons $\{1\}$ and $\{-1\}$. We'll focus on uniqueness---showing that $C_2$ is (up to isomorphism) the *only* group with exactly two conjugacy classes.)

*Given.* A finite group $G$ with exactly two conjugacy classes.

*To prove.* $G$ is isomorphic to $C_2$.

*Proof.*^[Keith Conrad [@CoConjugation] presents a general case for any finite number of conjugacy classes. Vipul Naik does so too here: <https://groupprops.subwiki.org/wiki/There_are_finitely_many_finite_groups_with_bounded_number_of_conjugacy_classes>.] Consider the class equation $$\abs{G} = \frac{\abs{G}}{ \abs{ C_G(g_1) } } + \frac{\abs{G}}{\abs{ C_G(g_2) }}.$$ By hypothesis $G \neq \{1\}$. It follows that each $C_G(g_i)$ contains at least two elements, $1$ and $g_i$. Now let $n_1  = \abs{ C_G(g_1) }$ and $n_2 = \abs{ C_G(g_2) }$, and without loss of generality suppose $n_1 \le n_2$. To satisfy the class equation, we must have $$1  = \frac1{n_1} + \frac1{ n_2 }.$$ Then $1 \le \frac2{ n_2 }$, so $n_1 \le 2$. Moreover $n_2 \le \frac{1}{1 - \frac12} = 2.$ Therefore $n_1 = 2$ and $n_2 = 2$. 

So for both of the representatives $g_i$ in $G$, we have $C_G(g) = {1, g}$. Certainly one of the $g_i$ is the identity $1$. The other is its own inverse, distinct from the identity.^[Why is the other forced to be its own inverse? This argument is awfully myopic.] Therefore $G \cong C_2$. \qedsymbol

### [@DF04, number 4.3.19]

Assume $H$ is a normal subgroup of $G$, $\sK$ is a conjugacy class of $G$ contained in $H$ and $x \in \sK$. We show $\sK$ is a union of $k$ conjugacy classes of equal size in $H$, where $k = \abs{G : HC_G(x)}$. 

*Given*. $H \triangleleft G$, $\sK$ a conjugacy class of $G$, $\sK \subset H$.

*To prove*. For $x \in \sK$, we have that $\sK$ is a union of $k = \abs{G : H C_G(x)}$ conjugacy classes in $H$.

*Proof.* $G$ acts transitively by conjugation on $\sK$---for every pair of elements $a$ and $b$ in $\sK$ is conjugate to the other in $G$. Now recall from the previous assignment [@DF04, number 4.1.9]:

> [When] $G$ acts transitively on the finite set $A$ and $H$ is a normal subgroup of $G$, with $\sO_1, \sO_2, \ldots, \sO_k$ the distinct orbits of $H$ on $A$, we have that 
>
> (a) $G$ is transitive on $\{\sO_1, \ldots, \sO_k\}$ and all orbits of $H$ on $A$ have the same cardinality.

Therefore, in our specific case, $G$ acts transitively on the orbits of the conjugation action of $H$ on $\sK$. If these orbits of $H$ on $\sK$ are denoted $\sO_1, \ldots,\sO_k$, then $\abs{\sO_1} = \cdots = \abs{\sO_k}$.

We now want to show that the number of such orbits $k = \abs{G : HC_G(x)}$. Perhaps relabelling indices, let $x \in \sO_1 \subset \sK$. Citing again [@DF04, number 4.1.9], we have:

> (b) If $a \in \sO_1$, then $\abs{\sO_1} = \abs{H : H \cap \Stab{G}{a}}$. Furthermore, $k = \abs{G : H\Stab{G}{a}}$.

In our specific case, both $G$ and $H$ act on $\sK$ by conjugation. We thus recognize $\Stab{G}{a} = C_G(a)$ for points $a$ in $\sK$. That $k = \abs{G : HC_G(x)}$ is immediate. For clarity of argument, however, we'll find $k$ directly from the diamond isomorphism theorem, ignoring^[I had to revise it anyways.] the result [@DF04, number 4.1.9] (b) .

Onwards! Consider the centralizer of $x$ in $G$ and $C_G(x)$ and $H \triangleleft G$. Now by the diamond isomorphism theorem we have the lattice

\begin{center}
\begin{tikzpicture}[every node/.style={fill=white}] % white fill keeps lines from running into labels

	\draw[double] (0,6) -- (2,4);
    \draw (2,4) -- (0,2);
    \draw (0,6) -- (-2,4);
	\draw[double]  (-2,4) -- (0,2);

	\node at (0,6) {$HC_G(x)$};
	\node at (2,4) {$H$};
	\node at (-2,4){$C_G(x)$};
	\node at (0,2) {$C_H(x)$};

\end{tikzpicture}
\end{center}

where we've observed that $C_H(x) = \{h \in H: hx = xh\} = \{g \in G: g \in H \text{ and } gx = xg\} = H \cap C_G(x)$ for the bottom node. As a consequence of the diamond isomorphism theorem, 
$$\frac{HC_G(x)}{H} \cong \frac{C_G(x)}{C_H(x)} \quad\text{ therefore }\quad \abs{HC_G(x)} = \frac{\abs{C_G(x)}\abs{H}}{\abs{C_H(x)}}.$$ 
By orbit stabilizer for the action of $G$ and $H$ on $\sK$,
$$\abs{\sK} = \frac{\abs{G}}{\abs{C_G(x)}} \quad\text{ and, zooming in to action of $H$, }\quad \abs{\sO_1} = \frac{\abs{H}}{\abs{C_H(x)}}.$$
Noting $\sK$ is the union of disjoint orbits $\sO_i$ of the same size, we find $k = \frac{\abs{\sK}}{\abs{\sO_1}}$ as follows
\begin{align*}
k &= \abs{\sK}\cdot\frac{1}{\abs{\sO_1}}\\
  &= \frac{\abs{G}}{\abs{C_G(x)}} \cdot \frac{\abs{C_H(x)}}{\abs{H}}\\
  &= \frac{\abs{G}}{\abs{HC_G(x)}}\\
  &= \abs{G : HC_G(x)}.
\end{align*}
Therefore $\sK$ is the union of $\abs{G:HC_G(x)}$ equally sized orbits of $H$. \qedsymbol

**Corollary.** A conjugacy class in $S_n$ that consists of even permutations is either a single conjugacy class under the action of $A_n$ or is a union of two classes of the same size in $A_n$.

*Proof.* Say that $\sK$ is a conjugacy class of $S_n$ that consists of only even permutations. We recognize $A_n$ is normal in $S_n$, so the hypotheses of the previous result are satisfied our specific case. Thus, $\sK$ is the union $\abs{A_nC_G(x)}$ equally sized orbits of $A_n$ acting by conjugation on $\sK$. Since $$\frac{n!}{2} = \abs{A_n} \le \abs{A_nC_G(x)}$$ we must have the index of $A_n C_G(x)$ in $S_n$ either $1$ or $2$. \qedsymbol

### [@DF04, number 4.3.23]

If $M$ is a maximal subgroup of $G$ then either $N_G(M) = M$ or $N_G(M) = G$. Therefore, if $M$ is a maximal subgroup of $G$ that is not normal in $G$ then the number of nonidentity elements of $G$ that are contained in conjugates of $M$ is at most $(\abs{M} -1)\cdot \abs{G:M}$.

*Given.* A maximal subgroup $M$ of $G$. 

*To prove.* Either $N_G(M) = M$ or $N_G(M) = G$. Also, the number of non-identity elements of $G$ that are contained contained in conjugates of $M$ is at most $(\abs{M} -1)\cdot \abs{G:M}$.

*Proof.* Since $M \le N_G(M) \le G$ and $M$ is maximal in $G$, either $N_G(M) = M$ or $N_G(M) = G$. Now to put an upper bound on the number of nonidentity elements of $G$ contained in conjugates of $M$, assuming $M$ is *not* normal in $G$. The key idea is to note that conjugation is an automorphism of $G$, so any conjugate $gMg^{-1}$ is isomorphic to $M$. Since the identity is only conjugate to itself, the number of non-identity elements in each conjugate $gMg^{-1}$ is $\abs{M}-1$. We can partition $G$ into $\abs{G: M}$ disjoint left cosets of $M$, but we can't partition $G$ into conjugates of $M$, for conjugation fixes the identity element. So we have at most $(\abs{M} - 1)$ non-identity elements of $M$ to work with. Since the index of $M$ in $G$ is $\abs{G : M}$, we conclude there are at most $(\abs{M} - 1)\abs{G : M}$ distinct non-identity elements of $G$ in conjugates of $M$. \qedsymbol

### [@DF04, number 4.3.24]

Assume $H$ is a proper subgroup of the finite group $G$. Then $G$ is not the union of the conjugates of any proper subgroup, i.e., $$G \neq \bigcup_{g \in G} gHg^{-1}.$$

*Proof.* If $G$ is a proper subgroup of $G$, then $H \le M$ for some maximal subgroup $M \le G$. By [@DF04, 4.3.23], 

\begin{align*}
\abs{ \bigcup_{g \in G} gHg^{-1} } &\le (\abs{M} -1)\abs{G : M}\\
    &= \abs{G} \cdot \frac{\abs{M}-1}{\abs{M}}\\ 
    &< \abs{G}.
\end{align*}
We conclude that $G$ is not the union of conjugates of the proper subgroup $H$. \qedsymbol

### The size of each conjugacy class in $S_n$ [@DF04, number 4.3.33]

Let $\sigma$ be a permutation in $S_n$ and let $m_1, \ldots, m_s$ be *distinct* integers that appear in the cycle type of $\sigma$ (including $1$-cycles). For each $i \in \{1, 2, \ldots, s\}$ assume $\sigma$ has $k_i$ cycles of length $m_i$ (so that $\sum_{i=1}^s k_i m_i = n$). Then the number of conjugates of $\sigma$ is $$\frac{n!}{(k_1!m_1^{k_1})(k_2!m_2^{k_2})\cdots(k_s!m_s^{k_s})}.$$

*Proof.* Suppose $\sigma \in S_n$ is as described above. Place out parentheses according to the cycle type of $\sigma$. There are $n!$ ordered arrangements of exactly $n$ distinct indices without repetition into the parentheses.^[Being polite: We assume the parentheses are not nested, we require there are $n$ total positions in between all the pairs, and we also assume that the parentheses are open and closed ecumenically.]  

Now cyclic permutations of indices in a set of parentheses are equivalent, so for each $m_i$ cycle in $\sigma$ we mod out the $n!$ arrangements by $m_i^{k_i}$, the number of cyclic permutations of indices affecting equivalent arrangements of the indices in the $m_i$ cycles.

Furthermore, permutations of the order in which order disjoint cycles are listed in the cycle decomposition of $\sigma$ are equivalent, so for each $k_i$, we mod out $n! \big/ \left(\prod_{i=1}^s m_i^{k_i}\right)$ by the possible reorderings $k_i!$ for each $k_i$ that's the number of $m_i$-length cycles appearing in the decomposition of $\sigma$.

Therefore, the number of distinct conjugates of $\sigma$ in $S_n$ is given by $$n\big/ \left(\prod_{i=1}^s k_i! m_i^{k_i}\right) = \frac{n!}{(k_1!m_1^{k_1})(k_2!m_2^{k_2})\cdots(k_s!m_s^{k_s})}.$$

**Examples.** If $n \ge m$ then the number of $m$-cycles in $S_n$ is given by $$\frac{n(n-1)(n-2)\ldots(n-m+1)}{m}.$$ If $n \ge 4$ then the number of permutations in $S_n$ that are the product of two disjoint $2$-cycles is $n(n-1)(n-2)(n-3)/8$. The later will come into use as a base case for determining the order of the conjugacy classes of elements with order $2$ in $S_n$

### [@DF04, number 4.4.3]

\providecommand{\Aut}[1]{\mathrm{Aut}\left( #1 \right)}
\providecommand{\inn}[1]{\mathrm{inn}\left( #1 \right)}
\providecommand{\Inn}[1]{\mathrm{Inn}\left( #1 \right)}

Under any automorphism of $D_8$, $r$ has at most $2$ possible images and $s$ has at most $4$ possible images. Thence $\abs{\Aut{D_8}} \le 8$.

*Demonstration.* Suppose $\phi$ is an automorphism of $D_8$. Now $\phi$ preserves some structural group properties, e.g., elements of an order are mapped to elements of the same order. Hence 
$$ r \mapsto r \text{ or } r^3 \text{, which are elements of order $4$}.$$ 
Note we cannot have $s \mapsto r^2$ for then $$\phi(\underbrace{rs}_{\abs{rs} = 2}) \neq \phi(r)\phi(s) = \underbrace{r^3 \text{ or } r}_{\text{order }4}.$$

Therefore, by order considerations
$$ s \mapsto s, rs, r^2s, r^3s.$$

Now $\phi$ is determined by the images of the generators $r$ and $s$. Observe the are at most $2\cdot 4$ distinct choices for these images. Hence $\abs{\Aut{D_8}} \le 8$. \qedsymbol

### [@DF04, number 4.4.8]

Suppose $G$ is a group with subgroups $H$ and $K$ where $H \le K$.

(b) If $H$ is characteristic in $K$ and $K$ is characteristic in $G$, then $H$ is characteristic in $G$. Thence the *Viergruppe* $V_4$ is characteristic in $S_4$.

*Proof.* For each $\phi \in \Aut{G}$, observe $\phi \vert_K$ is automorphism of $K$. Note $\phi\vert_K(H) = H$ because $H \mathrm{char} K$. Extending back to $\phi$, we have $\phi(H) = H$, as desired to show $H \mathrm{char} G$. \qedsymbol

In the specific case of $V_4$ characteristic in $A_4$, characteristic in $S_4$, transitivity implies $V_4$ is characteristic in $S_4$.

To show the first two relations, say $\phi \in \Aut{G}$. Note $V_4 = \langle (1 \, 2)(3\, 4), (1\,3)(2\,4)\rangle$. The automorphism $\phi$ maps conjugate elements to eachother. By the lattice isomorphism theorem, $V_4  = \phi(V_4) = \langle \phi((1 \, 2)(3\, 4)), \phi((1\,3)(2\,4))\rangle$. For the second relation, suppose $\psi \in \Aut{S_4}$. By order considerations, $\psi$ must map any two distinct $3$-cycles in $A_4$ to other distinct $3$-cycles in $A_4$. Therefore $\psi(A_4) = \langle \psi((i_1 i_2 i_3)), \psi((j_1 j_2 j_3)) \rangle = A_4$, since $3$-cycles generate $A_4$. 

We have seen $V_4$ is characteristic in $A_4$ is characteristic in $S_4$. Hence $V_4$ is characteristic in $S_4$.

(c) If $H$ is normal in $K$ and $K$ is characteristic in $G$, then $H$ need not be normal in $G$.

Consider $H = \langle (1\, 2)(3\, 4)\rangle$, $K = V_4$, and $G = A_4$. Since $V_4$ is abelian, $H$ is normal in $V_4$. Yet for $\sigma = (1\, 2\, 3) \in A_4$, conjugation by $\sigma$ of $H$ produces the element $(1\,3)(2\,4) \notin H$. So $H \not\triangleleft A_4$.

### [@DF04, number 4.4.18]

For $n \neq 6$ every automorphism of $S_n$ is inner. Fix an integer $n \ge 2$ with $n \neq 6$.

(a) The automorphism group of a group $G$ permutes the conjugacy classes of $G$, i.e., for each $\sigma \in \Aut{G}$ and each conjugacy class $\sK$ of $G$ the set $\sigma(\sK)$ is also a conjugacy class of $G$.

*Given.* A group $G$, its automorphism group $\Aut{G}$, and the collection $\Omega = \{ \sK:\text{ conjugacy classes in $G$} \}$.

*To prove.* If $\sigma \in \Aut{G}$ and $\sK \in \Omega$, then $\sigma(\sK) \in \Omega$.

*Proof.* Suppose $a$ and $b$ are conjugate elements in $G$. Then for some $g \in G$, $a = gbg^{-1}$. Consider the image under automorphism, $\sigma(a) = \sigma(g)\sigma(b)\sigma(g)^{-1}$. So $\sigma(a)$ and $\sigma(b)$ are conjugate. 

Pairwise conjugacy of the points in the image of $\sK$ under $\sigma$ implies $\sigma(\sK) \subset \sF \in \Omega$. Now to show $\sF \subset \sigma(\sK)$. Let $c \in \sF$. Then $\sigma(a) = hch^{-1}$ for some $h \in G$. Applying the inverse automorphism $\sigma^{-1}$, we see $a$ is conjugate to $\sigma^{-1}(c)$, thus $\sigma^{-1}(c) \in \sK$. Thus $\sigma^{-1}(\sF) \subset \sK$. Applying $\sigma$, we conclude $\sF \subset \sigma(\sK)$.

(b) Let $\sK$ be the conjugacy class of transpositions in $S_n$ and let $\sK'$ be the conjugacy class of any element of order $2$ in $S_n$ that is not a transposition. Then $\abs{\sK} \neq \abs{\sK'}$. Furthermore, any automorphism of $S_n$ sends transpositions to transpositions. 


If $n < 4$ the only elements of order $2$ are transpositions. Therefore $\sK' = \emptyset$. So suppose $n \ge 4$. Elements of order $2$ in $S_n$ that are not transpositions are products of $k$ many disjoint $2$-cycles. We observe $2 \le 2 \le \left \lceil{n}\right \rceil$. 

We now show $\abs{\sK} \neq \abs{\sK '}$ for all $n, k$ with the exception of $(n,k) = (6,3)$, for which there are $15$ elements in both the conjugacy class $\sK$ of transpositions and in the class $\sK' = \{\text{products of $3$ disjoint $2$-cycles}\}$.

We generate a heatmap plot of the value $\abs{\sK'} - \abs{\sK}$, where both are defined:

```
dim = 10
A = np.full([dim,dim], float('nan'))
for n in np.arange(2,b):
    for k in np.arange(2,int(n/2.0)+1):
        A[n,k] = -(n*(n-1)/2) + np.math.factorial(n)/(np.math.factorial(k)*2**k)
```

![heat](/home/colton/fy/19/alg1/size-diff.png)

By previous exercise, we have $$\abs{\sK} = \frac{n(n-1)}{2} \quad \text{ and } \quad \abs{\sK'} = \frac{n!}{k!2^k}.$$

The heatmap provides a base case, and it's clear that $\abs{\sK'}$ strictly dominates $\abs{\sK}$ for, say, $n \ge 9$ and $k \ge 4$. 

Since $\sigma$ must preserve the order of both conjugacy classes and elements in them, we see that $\sigma$ stabilizes the set $\sK$ of transpositions, as desired.

(c) For each $\sigma \in \Aut{S_n}$ we have $$\sigma \colon (1\, 2) \mapsto (a\, b_2), \quad\quad \sigma \colon (1\, 3) \mapsto (a\, b_3), \quad\ldots, \quad \sigma \colon (1\, n) \mapsto (a\, b_n)$$ for some distinct integers $a, b_2, b_3, \ldots, b_n \in \{1, 2, \ldots, n\}$.
(d) Therefore $(1\, 2), (1\, 3), \ldots, (1\, n)$ generate $S_n$. Furthermore $S_n$ is uniquely determined by its action on these elements. Then by (c), $S_n$ has at *most* $n!$ automorphisms. We conclude that $\Aut{S_n} = \mathrm{Inn}(S_n)$ for $n \neq 6$.

### [@DF04, number 4.4.20]

TODO 

For any finite group $P$, let $d(P)$ be the minimum^[For example, $d(P) = 1$ if and only if $P$ is a nontrivial cyclic group and $d(Q_8) = 2$.] number of generators of $P$. Let $m(P)$ be the maximum of the integers $d(A)$ as $A$ runs^[For example, $m(Q_8) = 1$ and $m(D_8) = 2$.] over all *abelian* subgroups of $P$. Define the *Thompson subgroup* of $P$ as $$J(P) = \langle A : A \text{ is an abelian subgroup of $P$ with } d(A) = m(P)\rangle.$$

(a) $J(P)$ is a characteristic subgroup of $P$.
(b) For each of the following groups $P$, we exhaustively list all abelian subgroups $A$ of $P$ that satisfy $d(A) = m(P)$.

- $Q_8$
- $D_8$
- $D_{16}$
- $QD_{16}$ (the quasidihedral group of order $16$)


## References

<!---
### Keywords

- automorphisms
    - images under
    - inner
    - outer
- conjugacy
    - conjugates of a subgroup
    - conjugacy classes
    - index in the group
    - structure, e.g., in $A_n$
- descriptors for subgroups
    - *proper*
    - *maximal*
    - *Thompson*
    - *abelian*
    - *characteristic*
--->
