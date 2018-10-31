---
title: Nilpotent Groups & Finite Abelian Groups 
author: Colton Grainger
date: 2018-10-28
bibliography: /home/colton/Downloads/coltongrainger.bib
macros: true
tikz: true
---

\setcounter{section}{7}

## Assignment due 2018-10-31

### [@DF04, number 5.2.8]

Let $A$ be a finite abelian group (written multiplicatively) and let $p$ be a prime. Suppose $$A^p = \{ a^p : a \in A\} \quad\text{ and }\quad A_p = \{x : x^p= 1\},$$ so that $A^p$ and $A_p$ are the image and kernel of the $p$th power map $$\phi \colon A \to A \quad \text{ such that }\quad \phi \colon x \mapsto x^p.$$

(a) Prove that $A/A^p \cong A_p$ by showing both are elementary abelian and of the same order.

    *Proof.*^[See also <https://math.stackexchange.com/questions/413470/>, <https://math.stackexchange.com/questions/142589/>.] Observe $A_p = \ker \phi$ and $A/A^p = \mathrm{coker} \phi$. We anticipate a line of argument similar to the rank-nullity theorem from linear algebra.

    By the first isomorphism theorem, $$A/\ker \phi \cong \mathrm{im} \phi \quad \text{ that is } \quad A/A_p \cong A^p \quad \text{ so } \quad \abs{A/A^p} = \abs{A_p}.$$

    To see that both $A_p$ and $A/A^p$ are elementary abelian $p$-groups, check:

    - $A_p \ni x$ implies $x^p = 1$.
    - $A/A^p \ni xA^p$ implies $(xA^p)^p = x^pA^p = 1\cdot A^p$.
    - Since $p$ is prime, the only element in $A_p$, $A/A^p$ of order less than $p$ is the identity.

    We conclude $A_p \cong A/A^p$ as both are elementary abelian $p$-groups of the same order, say, both isomorphic to $(\FF_p)^n$. \qedsymbol

(b) Prove that the number of subgroups of $A$ of order $p$ equals the number of subgroups of $A$ of index $p$, by reducing to the case where $A$ is an elementary abelian $p$-group.

    *Proof.* Since each subgroup of $\ker \phi = A_p$ is cyclic $p$, and each subgroup of $A$ of order $p$ is in $\ker \phi$, our proof reduces to considering the order $p$ subgroups of $A_p$. 

    At the same time, we want to show if $H \le A$ is a subgroup of index $p$, then $A^p \le H$. So let $x \in A^p$. Then $x = a^p$ for some $a$. Suppose by way of contradiction that $x \notin H$. We must then have $a^p \notin H$, whence $a \notin H$ (by closure). Now the quotient group $A/H$ is of order $p$ and cyclic. With $a \notin H$, we can populate the coset space $A/H$ with $\langle a\rangle = H$. But then $$H = (aH)^p = a^p H \quad \text{ implies } \quad a^p \in H, \quad \text{ and so } \quad x \in H,$$
    a contradiction. Thus we must have $A^p \le H$. (By line of reasoning similar to the proof of the universal property for the abelianization of a group by quotienting out the commutator) the third isomorphism theorem implies $$A/H \cong (A/A^p) / (H/A^p).$$ 
    So just as with the kernel $A_p$, with the cokernel $A/A_p$ it suffices to consider the number of index $p$ subgroups in $A/A^p$ to find the number of index $p$ subgroups in $A$.

    Now $A_p \cong A/A^p \cong (\FF_p)^n$. We need show the number of subgroups of order $p$ is the same as the number of subgroups of index $p$. But this boils down to showing that the number of $1$-dimensional  $\FF_p$-vector spaces in $(\FF_p)^n$ is equal to the number of $1$-codimensional (i.e., $n-1$-dimensional) $\FF_p$-vector spaces in $(\FF_p)^n$. Observe both numbers are given by the gaussian binomial coefficient [@Pr11, page 3-5], which is a center symmetric quantity: $${n \choose n-1}_p = {n \choose 1}_p = \frac{1-p^n}{1-p},$$
    as desired. \qedsymbol

### [@DF04, number 5.2.14]

For any group $G$ define the *dual group* $\hat{G}$ of $G$ to be the set of all homomorphisms from $G$ into the multiplicative group of roots of unity in $\CC$. Define a group operation in $\hat{G}$ by pointwise multiplication of functions: if $\chi$ and $\psi$ are homomorphisms from $G$ into the group of roots of unity, then $\chi\psi$ is the homomorphism given by $( \chi\psi)(g) = \chi(g)\psi(g)$ for all $g \in G$.

(a) This operation on $\hat{G}$ makes $\hat{G}$ into an abelian group. 

    *Proof.* To verify that $\hat{G}$ is abelian.

    - $\hat{G}$ is a set closed under the binary operation given by pointwise multiplication.
    - Associativity and commutativity of elements in $\hat{G}$ follows from the same properties of elements in $\CC$.
    - The homomorphism $\mathbf{1}_G \in \hat{G}$ that sends $g \in G$ to $1 \in \CC$ is the identity. 
        - One may check that for all $\chi \in \hat{G}$ and all $g \in G$, $$\mathbf{1}_G\chi(g) = \chi(g) = \chi\mathbf{1}_G(g).$$
    - For each $\chi \in \hat{G}$, the map $\chi^{-1} \in \hat{G}$ given by $g \mapsto (\chi(g))^{-1}$ is the (left and right) inverse to $\chi$. 
        - One may check that for all $g \in G$, $$\chi\chi^{-1}(g) = \mathbf{1}_G(g) = \chi^{-1}\chi(g).$$

    As desired, $\hat{G}$ is seen to be an abelian group. \qedsymbol

(b) If $G$ is a finite abelian group, then $\hat{G} \cong G$. 

    *Proof.* $G$ is a finite abelian group, whence by the fundamental theorem of finitely generated abelian groups $$G = \prod_{j=1}^r\langle x_j \rangle.$$ Suppose $n_i = \abs{x_i}$ and define for each $i$, $$\chi_i \in \hat{G} \quad \text{ such that }\quad \chi_i \colon \prod_{j=1}^{i-1} 1 \times x_j \times \prod_{j=i+1}^r 1 \mapsto e^{2\pi i/n_i}$$ and that $$\prod_{j=1}^{k-1} 1 \times x_k \times \prod_{j=k+1}^r 1 \mapsto e^{0} = 1 \quad \text{ for $k\neq i$}.$$

    We've defined $\chi_i$ on generators of $G$, so on each element of $G$. Now we want to show $\chi_i$ has order $n_i$. Let $g \in G$ and $b \in \NN$. Consider $$\chi_i^b(g) = (\chi_i(g))^b = e^{2\pi i b/n_i} = 1,$$ occurring if and only if $b$ is a multiple of $n_i$. So $\abs{\chi_i} = \min\{ b \in \NN : b = kn_i\} = n_i$. We now identify each $x_i$ with $\prod 1 \times x_i \prod 1$, the coordinate axis generators. 
    
    Observe if $\psi \in \hat{G}$, then we can write $\psi$ uniquely as the product of the $\chi_i$. That is, we consider the image under $\psi$ of each coordinate generator $x_i$: $\psi(x_i) = e^{2 \pi i/ c_i/n_i}$ for some $c_i \in \{0, \ldots, n_i - 1\}$ (if $\psi$ did not map $x_i$ to such a multiple of $e^{2\pi i / n_i}$, we'd obtain the contradiction $1 \neq ( \psi(x_i) )^{n_i} = \psi(1) = 1$. 

    If follows that $\psi = \chi^{c_1}_1\chi^{c_2}_2\cdots \chi^{c_r}_r$. By the recognition theorem for direct products, (maybe abusing notation) $$\bigcap_{j=1}^r \langle \chi_j \rangle  = \{ \mathrm{1}_G\}$$ and $\langle \chi_j \rangle \triangleleft \hat{G}$, so $$\hat{G} = \langle \chi_1 \rangle \times \cdots \times \langle \chi_r \rangle.$$ Now each coordinate axis subgroup of the same index $i$ in $G$ and $\hat{G}$ are isomorphic to $C_{n_i}$, so $G \cong \hat{G}$. See also [@CoCharacters]. \qedsymbol

### [@DF04, number 6.1.7]

Subgroups and quotient groups of nilpotent groups are^[Even in the infinite case.] nilpotent. 

*Proof.* We proceed by lower central series. Let $G$ be nilpotent of class $c$. Then $\gamma_c(G) = \{1\}$. If $H \le G$, then $\gamma_c(H)$ is also trivial. Well, observe that $\gamma_0(H) \le \gamma_0(G)$ and for all $n \ge 1$ we have $$\gamma_n(H) = [H, \gamma_{n-1}(H)] \le [G, \gamma_{n-1}(G)] = \gamma_n(G).$$ So if $\gamma_c(G) = \{1\}$, then $\gamma_c(H) = \{1\}$. Therefore $H$ is nilpotent, of class at most $c$.  

For the quotient, let $N \triangleleft G$ and consider the canonical projection $\pi \colon G \to G/N$. For all $gN \in \gamma_n(G/N)$ there's a $g \in \gamma_n(G)$ such that $g \mapsto_\pi gN$. So the map from $\gamma_n(G)/N$ to $\gamma_n(G/N)$ is onto for all $n$. Whence $G/N$ is nilpotent whenever $G$ is. See also [@CoSolvable]. \qedsymbol

We exhibit a group $G$ which possesses a normal subgroup $H$ such that both $H$ and $G/H$ are nilpotent but $G$ is not nilpotent.

*Demo.* Try $S_3$. Clearly $S_3 / A_3 \cong \ZZ/2\ZZ$ and $A_3 \cong \ZZ/3\ZZ$ are nilpotent. Yet $[S_3, S_3] = A_3$ and $[S_3, A_3] = A_3$, so the lower central series stabilizes away from $\{1\}$.

### [@DF04, number 6.1.10]

$D_{2n}$ is nilpotent if and only if $n$ is a power of $2$.

*Proof.* We know $D_{2n} \cong C_2 \rtimes_\phi C_n$, the semidirect product with the appropriate twist defined $\phi(s)(r) = r^{-1}$.

For contradiction, suppose *both* (i) $n \neq 2^a$ for any $a \in \ZZ_{\ge 0}$ and (ii) $D_2n$ is nilpotent. Now if $s,r \in D_{2n}$ with $\abs{s} =2$, $\abs{r} = n$, then $(\abs{s}, \abs{r}) = 1$. But then [DF04, page 192] $rs = sr$, a contradiction. ("A finite group $G$ is nilpotent if and only if whenever $a,b \in G$ with $(\abs{a},\abs{b}) = 1$, then $ab = ba$.") So $D_{2n}$ isn't nilpotent.

On the other hand, if $n = 2^a$ for some nonnegative integer $a$, then $D_{2n}$ is the direct product of its Sylow subgroups ($D_{2n}$ is a $2$-group!), hence nilpotent. \qedsymbol

### [@DF04, number 6.1.20]

Let $p$ be a prime, let $P$ be a $p$-subgroup of the finite group $G$, let $N$ be a normal subgroup of $G$ whose order is relatively prime to $p$, and let $\bar{G} = G/N$. 

(a) With Frattini's argument, $\N { \bar{G} } { \bar{P} } = \overline{\N G P}$.
(b) From above, $\N{\bar{G}}{\bar{P}} = \overline{\N G P}$.

TODO

### [@DF04, number 6.1.24]

**Definition.** For any group $G$, the *Frattini subgroup* of $G$ (denoted by $\Phi(G)$) is defined to be the intersection of all the maximal subgroups of $G$ (if $G$ has no maximal subgroups, set $\Phi(G) = G$).

Say an element $x$ of $G$ is a *nongenerator* if for every proper subgroup $H$ of $G$, $\langle x, H \rangle$ is also a proper subgroup of $G$. If $\abs{G} > 1$, then $\Phi(G)$ is the set of nongenerators of $G$.

*Given.* A nontrivial group $G$, the set $\sM$ of maximal subgroups of $G$, maximal subsets $M$ in $\sM$.

*To prove.* The intersection of all $M \in \sM$ is $\Phi(G)$.

*Proof.* ($\subset$) Suppose $$x \in \bigcap_{ M \in \sM } M.$$ Then for any $H \lneq G$, there's a maximal $M_H \in \sM$ such that $H \le M$. Since $x \in M_H$, we have $\langle x, H \rangle \le M_H \lneq G$. So $x$ is a *nongenerator*. Thus $x \in \Phi(G)$.

($\supset$) Let $x \in \Phi(G)$. We'll show that $x$ is in every maximal subgroup $M \in \sM$. Since each $M$ is proper, if $x \notin M$, then $\langle x, M \rangle = G$, a contradiction. So $x \in M$. \qedsymbol

### [@DF04, number 6.1.25]

With $G$ be a finite group, $\Phi(G)$ is nilpotent.^[Hint: Use Frattini's Argument to prove that every Sylow subgroup of $\Phi(G)$ is normal in $G$.]

*Given.* A finite group $G$, its Frattini subgroup $\Phi(G)$.

*To prove.* For each prime $p$, for each $P \in \Syl p {\Phi(G)}$, we have $P \triangleleft \Phi(G)$. By the recognition theorem, $\Phi(G)$ will be the product of its Sylow subgroups. We'll conclude that $\Phi(G)$ nilpotent.

*Proof.* Observe that $\Phi(G)$ is characteristic in $G$. (Why? If $\sigma \in \Aut{G}$, then $\sigma$ permutes maximal subgroups. Thus $\sigma$ fixes their intersection $\Phi(G)$.) The hypotheses of the Frattini argument are met---$\Phi(G) \triangleleft G$, $G$ is a finite group, $P \in \Syl p {\Phi(G)}$---so $$G = \Phi(G)N_G(P).$$ It follows^[I've seen other directions for this proof, so this line of reasoning may not pan out.] that $$\Phi(G) = G \cap \Phi(G) = \Phi(G)N_G(P) = N_{\Phi(G)}(P).$$ So $P \triangleleft \Phi(G)$. 

We see every Sylow subgroup of $\Phi(G)$ is normal. With a familiar argument from Lagrange, the intersection of any distinct two Sylow subgroups is trivial. By the recognition theorem for direct products $$\Phi(G) = \prod_{i=q}^r P_i \quad \text{ where } \quad \abs{\Phi(G)} = \prod_{i=1}^r p_i^{a_i} \quad \text{ is the prime factor decomposition with } P_i \in \Syl {p_i} {\Phi(G)}.$$

Since $\Phi(G)$ is the direct product of its Sylow subgroups, $\Phi(G)$ is nilpotent. \qedsymbol

### [@DF04, number 6.1.26]

Suppose $p$ is a prime, $P$ is a finite $p$-group and define $\bar{P} = P / \Phi(P)$.

(a) $\bar{P}$ is an elementary abelian $p$-group.

    *Proof.* We start by finding the order of elements in $\bar{P}$. Let $\bar{x} \in \bar{P}$. Then $\bar{x}^p = x^p \Phi(P)$. We'll now show $x^p \in M$ for all maximal $M$. 
    
    By way of contradiction (similar to [@DF04, number 5.2.8]) suppose that $x^p \notin M$. We're forced to accept $x \notin M$. Now $\abs{P/M} = p$, a prime. Then the quotient $P/M$ is cyclic and of the form $\langle x\rangle M$. But $$1 \cdot M = (xM)^p = x^pM, \text{ so } x^p \in M, \text{ a *contradiction*.}$$ So $x^p \in M$. 
    
    It follows that $x^p \in \Phi(P)$. So every nonidentity element $\bar{x} \in \bar{P}$ has order $p$.

    Now we'll verify the commutativity of $\bar{P}$. Since for each maximal $M \in \sM$ the quotient $P/M$ is cyclic, we must have the commutator embedded: $P^{(1)} \le M$. So $$P^{(1)} \le \bigcap_{M \in \sM} M = \Phi(P).$$ 
    
    We conclude that $\bar{P}$ is elementary abelian.

(b) If $N$ is any normal subgroup of $P$ such that $P/N$ is elementary abelian, then $\Phi(P) \le N$. 

    *To prove.* The Frattini subgroup $\Phi(P)$ is the smallest normal subgroup (of a $p$-group $P$) such that the quotient of $P$ by $\Phi(P)$ is elementary abelian. That is, if $\phi \colon P \to A$ is any group homomorphism of $P$ into elementary abelian $A$, then $\phi$ factors (uniquely!) through $P/\Phi(P)$ and the following diagram commutes.

\begin{center}
\begin{tikzpicture}[every node/.style={fill=white}] % white fill keeps lines from running into labels
\draw[->] (-2,4) -- (1.3,4);
\draw[->] (-2,4) -- (1.3,0.2);
\draw[->,dashed] (2,4) -- (2,0.5);

\node at (-2,4) {$P$};
\node at (0,4.5) {$\pi$};
\node at (2,4) {$P/\Phi(P)$};
\node at (2,0) {$A$};
\node at (2.5,2) {$\exists !$};
\node at (-0.5,1.5) {$\phi$};

\end{tikzpicture}
\end{center}

    *Proof.* Supposing $N$ is a normal subgroup of $P$ such that $P/N$ is elementary abelian, we have $$\prod_{i=1}^r \langle x_i N \rangle.$$ Which subgroups of $P/N$ are maximal? Those generated by $r-1$ of the $x_iN$, call them $M_i/N = \langle x_j N : j \neq i \rangle$. Being subgroups of a direct product each with one coordinate trivial, $$\bigcap_{\forall i} M_i/ N = \{1 \cdot N \}.$$ Then pulling back, $\cap M_i = N$. Note each subgroup $M_i$ is maximal in $P$. Whence $$\Phi(P) \le \bigcap_{\forall i} M_i = N,$$ as desired. Since normal subgroups correspond to homomorphisms out of $P$, the conclusion follows. \qedsymbol

(c) Let $\bar{P}$ be elementary abelian of order $p^r$. From [@DF04, number 6.1.24], it follows that:

    If $\bar{x}_1, \ldots, \bar{x}_r$ are any basis for the $r$-dimensional vector space $\bar{P}$ over $\FF_p$ and if $x_i$ is any element of the coset $\bar{x}_i$, then $P = \langle x_1, \ldots, x_r\rangle$.

    - That is suppose $\bar{P} \cong (\FF_p)^r$ with a basis $\{\bar{x}_i : i = 1, \ldots, r\}$. Suppose $x_i \in \bar{x}_i$ for each $i$. By way of contradiction, suppose $P \neq \langle x_i : i = 1, \ldots, r\rangle$. Then, with out loss of generality, there's a $x_{r+1} \in P \setminus \langle x_i : \forall i \neq r+1 \rangle$ with $x_{r+1} \notin \Phi(P)$. Passing to the quotient, $\langle \bar{x}_{r+1}\rangle \cap \underbrace{\langle \bar{x}_i : \forall i \neq r+1 \rangle}_{\text{a basis?}} = \{1\}$. Contradiction.
    - So $P = \langle x_i : i = 1, \ldots, r \rangle$ as desired.

    Conversely,^[We assume that every minimal generating set for an $r$-dimensional vector space has $r$ elements, i.e., every minimal basis has $r$ elements.] if $y_1, \ldots, y_s$ is any set of generators for $P$, then $s \ge r$. 

    - Let $P = \langle y_1, \ldots, y_s \rangle$. Again for contradiction, suppose $s < r$. Then there's basis of $\bar{P}$ that contains some $\bar{y}_r$ such that $\langle \bar{y}_r \rangle \cap \langle \bar{y}_i : i = 1, \ldots, s \rangle = \{\bar{1}\}$. Choose $y_r \in \bar{y}_r$. Now $y_r \in P$ and $\underbrace{y_r \notin \Phi(P)}_{\bar{y}_r \neq \bar{1}}$, but $P = \langle y_1, \ldots, y_s \rangle = \langle y_1, \ldots, y_s, y_r \rangle$. Therefore $y_r \Phi(P)$, a contradiction. Thus $s \ge r$.

    - Now *Burnside's Basis Theorem* follows: a set $y_1, \ldots, y_s$ is a minimal generators set for $P$ if and only if $\bar{y}_1,\ldots, \bar{y}_s$ is a basis of $\bar{P}$.
    
    - Any minimal generating set for $P$ has $r$ elements.

(d) If $\bar{P}$ is cyclic, then $P$ is too. It follows that if $P/P'$ is cyclic, then so is $P$.

(e) Let $\sigma$ be any automorphism of $P$ of prime order $q$ with $q \neq p$. If $\sigma$ fixes the coset $x\Phi(P)$ then $\sigma$ fixes some element of this coset.^[Hint 1: Note that since $\Phi(P)$ is characteristic in $P$, every automorphism of $P$ induces an automorphism of $P/\Phi(P)$. Hint 2: Use the observation that $\sigma$ acts as a permutation of order $1$ or $q$ on the $p^a$ elements in the coset $x\Phi(P)$.]

(f) With parts (c) and (e), every nontrivial automorphism of $P$ of order prime to $p$ induces prime a nontrivial automorphism on $P/\Phi(P)$. Any group of automorphisms of $P$ which has order prime to $p$ is isomorphic to a subgroup of $\Aut{\bar{P}} = \mathrm{GL}_r(\FF_p)$.

### [@DF04, number 6.1.31]

For any group $G$ a *minimal normal subgroup* is a normal subgroup $M$ of $G$ such that the only normal subgroups of $G$ which are contained in $M$ are $1$ and $M$. We'll show^[Hint: If $M$ is a minimal normal subgroup of $G$, consider its characteristic subgroups: $M'$ and $\langle x^p : x \in M\rangle$.] every minimal normal subgroup of a finite solvable group is an elementary abelian $p$-group for some prime $p$. 

*Given.* A finite solvable group $G$ and a minimal normal subgroup $M \triangleleft G$.

*To prove.* $M$ is an elementary abelian $p$-group, by arguing the commutator subgroup $M'$ is trivial and finding a $p$ for which the image of $M$ under the $p$th power map $M^p$ is also trivial. 

*Proof.* Since $M'$ and $M^p$ are characteristic subgroups of $M$, it suffices only to prove that $M \neq M'$ and, for a prime $p$, $M \neq M^p$.

\begin{center}
\begin{tikzpicture}[every node/.style={fill=white}] % white fill keeps lines from running into labels
\draw[double] (0,3) -- (1,2);
\draw (1,2) -- (0,0);
\draw (0,3) -- (-1,2);
\draw[double]  (-1,2) -- (0,0);

\node at (0,3) {$G$};
\node at (1,2) {$G'$};
\node at (-1,2){$M$};
\node at (0,0) {$M' = \underbrace{M \cap G'}_{\text{verify}}$};
\end{tikzpicture}
\end{center}

By the diamond isomorphism theorem, $$G/G' \cong M/M',$$ which, given the hypothesis that $G$ is solvable, implies $$\{1 \cdot G' \} \lneq G/G', \quad \text{ i.e., } \quad \{1 \cdot M' \} \lneq  M / M'.$$

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
