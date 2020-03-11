---
layout: post
mathjax: true
comments: true
title:  "Axiom of Regularity ― an introduction"
date:   2020-03-12 02:30:00 +0900
categories: Set theory, 집합론
published: true
---

 Beginners of axiomatic set theory encounter a list of ten axioms of Zermelo-Fraenkel set theory (in fact, infinitely many axioms: Separation and Replacement are in fact not merely a single axiom, but a schema of axioms depending on a formula parameter, but it does not matter in this post.) Most of the axioms have a clear meaning, so not hard to accept: for example, Axiom of Pairing states we can find an unordered pair $\{a,b\}$ of $a$ and $b$, and Axiom of Union states we can find a union $\bigcup A$ of a set of sets $A$.
 Axiom of Choice might be a bit unclear and has a long historical debate whether this axiom should be accepted or not. However, we can find various applications of Axiom of Choice, and they provide a practical reason why we believe in Axiom of Choice, though there might be philosophical opposition which I will not cover.

 However, Axiom of Regularity has an unclear statement in a first glance:
> For each non-empty set $x$, there is $y\in x$ such that $x\cap y=\varnothing$.
Most of the readers ― especially those who have not learned axiomatic set theory ― have not seen this strange axiom. It has no non-trivial application to usual mathematics. Moreover, the usual mathematics seems like neutral to this axiom: accepting or denying the axiom does not change almost all of the usual mathematics.

 As a result, this unfortunate axiom is fallen into an abyss of oblivion as Blass mentioned in [1] by
> (...) the axiom of regularity has suffered an even worse fate than the axiom of choice; people don't deny the axiom of regularity, they just ignore it.

 Why set theorists add such an unclear and even seems-like redundant axiom as a part of ZFC? This post aims to explain the reason why. I will explain the meaning of this unfortunate axiom first and introduce its consequences: $\in$-induction and recursion, also called set induction and recursion. Then I will explain the most important consequence of the axiom of regularity: the class of all sets has a hierarchical structure.

 *Throughout this article, $V$ means the class of all sets.* 

----
<!-- Pure sets, meaning : comparing to well-orders -->

 We first analyze a cumbersome description of the axiom of regularity. I will assume that the readers already know about partial orders and well-orderings. Let me rephrase the definiton of well-ordering:
> An order $\prec$ over a set $X$ is *well-ordered* if every non-empty subset $Y$ of $X$ has a minimal element with respect to $\prec$.

 Well-orderedness is a property of orders. Could we generalize well-orderedness for general binary relations? Here is a possible attempt: 
> A binary relation $\prec$, not necessarily an order, is *well-founded* if every non-empty subset $Y$ of $X$ has a $\prec$-minimal element.

 We have to clarify what $\prec$-minimal element does mean: remember the definition of minimal element:
> An element $x\in P$ of a partially ordered set $(P,<)$ is *minimal* if no element $y\in P$ satisfies $y<x$; i.e. no element of $P$ is smaller than $x$.

 We can also generalize the notion of minimality to general binary relations:
> An element $x\in X$ of a set $X$ with a binary relation $\prec$ is *$\prec$-minimal* if no element $y\in P$ satisfies $y\prec x$.

 Now re-examine the statement of the axiom of regularity, with unpacking the set intersection into its definition:
> For each non-empty set $x$, there is $y\in x$ such that no $z\in x$ satisfies $z\in y$; that is, $y$ is a $\in$-minimal element of $x$.

 Especially, every non-empty subset of a given set has a $\in$-minimal element. Therefore, we can say the axiom of regularity a statement asserting that $\in$ is well-founded over any set.

 Since every non-empty *subset* of a class of all sets $V$ has a $\in$-minimal element, we could say $V$ well-founded under $\in$. However, it seems lacking something: $V$ is not a set but a proper class, so it has subclasses that are proper. Thus, it seems like we have to check every *subclass* of $V$ has a $\in$-minimal element.
 Fortunately, our axiom of regularity is sufficient to prove this:
> **Theorem** (ZF) Every non-empty class $C$ has a $\in$-minimal element.

*Proof.* Take any $x\in C$ and consider $y=\\{z\in x\mid z\in C\\}$. If $y$ is empty, then $x$ is $\in$-minimal element of $C$. If not, then $y$ is not empty and $y$ has a $\in$-minimal element, namely $w$. We can see be definition that $w$ is $\in$-minimal element of $C$.

----
<!-- Consequence : set induction and rank of sets -->
 We formulated well-foundedness by mimicing well-orderedness. Therefore, we could expect well-foundedness resembles well-orderedness. For example, no well-ordered set allows infinitely decreasing chains. We can say the same thing for well-founded sets:
> **Theorem** Let $\prec$ be a well-founded relation over a set $X$. Then there is no infinite $\prec$-decreasing sequence over $X$; that is, no sequence $\langle x_n\mid n\in\omega\rangle$ over $X$ satisfies $x_0\succ x_1\succ x_2\succ\cdots$.

*Proof.* Let $\langle x_n\mid n\in\omega\rangle$ be an infinite $\prec$-decreasing sequence over $X$. Let $y$ be a $\prec$-minimal element of $\\{x_n\mid n\in\omega\\}$. Since $y=x_m$ for some $m$ and $x_m\succ x_{m+1}$, we have a contradiction.

 Especially, we have
> **Corollary** (ZF) There is no $\in$-decreasing sequence; that is, no $\langle x_n\mid n\in\omega\rangle$ satisfies $x_0\ni x_1\ni x_2\ni\cdots$.

 This corollary excludes *ill-founded* sets (i.e. sets that make $\in$ not well-founded) from the universe $V$ of all sets. Especially, no set $x$ can satisfy $x\in x$.  

<!-- induction and recursion -->

 Well-orderedness has useful consequences: for example, every well-ordered set allows transfinite induction and transfinite recursion. The same holds for general well-founded relations, not only for well-ordered sets:

> **Theorem** (Well-founded induction)
> 
> Let $(X,\prec)$ be a set with a well-founded relation $\prec$ and assume that
> \\[\forall x\in X [\forall y\in X: y\prec x\to \phi(y)]\to \phi(x)\\]
> holds for a formula $\phi(x)$. Then $\phi(x)$ holds for all $x\in X$.

(Remark: $X$ need not be a set; hence $X$ can be a proper class. We need to modify the proof slightly, however, to not to assume $X$ be a set. I will leave this modification to the readers.)

*Proof.* Assume the contrary that $\lnot\phi(x)$ holds for some $x\in X$.
Since $\prec$ is well-founded, the set $\\{x\in X \mid \lnot\phi(x)\\}$ has a $\prec$-minimal element, say it $a$. We can see that no $b\prec a$ satisfy $\lnot\phi(x)$, so $b\prec a$ implies $\phi(b)$. By the assumption, however, it implies $\phi(a)$, a contradiction.

 Remind that the axiom of regularity states $\in$ is well-founded over $V$. Therefore, we have
> **Corollary** ($\in$-induction) If $(\forall y\in x \phi(y))\to \phi(x)$ holds for all $x$, then $\phi(x)$ holds for all $x$.

 What is the meaning of the well-founded induction? Let me remind the transfinite induction for ordinals. Its statement is as follows:
> Assume that
> \\[\forall \alpha\in\mathrm{Ord} [\forall \beta\in\mathrm{Ord}: \beta<\alpha\to \phi(\beta)]\to \phi(\alpha)\\]
> holds for a formula $\phi(\alpha)$. Then $\phi(\alpha)$ holds for all ordinal $\alpha$.

 Here $\mathrm{Ord}$ be the class of all ordinals. The assumption in the statement means "if $\phi$ holds for all ordinals less than $\alpha$, then $\phi(\alpha)$ holds". Therefore, a less formal description of the transfinite induction is
> Assume that if $\phi(\beta)$ holds for all predecessors of $\alpha$, then $\phi(\alpha)$ holds. Then $\phi$ holds for all ordinals.

 The meaning of the well-founded induction does not deviate from that of the transfinite induction: the well-founded induction states if we know the validity of $\phi(y)$ for all $y\prec x$ implies $\phi(x)$, then $\phi(x)$ holds for all $x$. It allows us inductive proof on a structure of sets, but I will postpone introducing its example.

<!-- recursion: make no comparison with ordinal version -->
We sometimes define a function on natural numbers and ordinals *recursively*. The nature of recursion of them heavily relies on the induction principle over $\mathbb{N}$ and ordinals.
Since well-founded relations allows its own induction, we might expect it allows recursion, and this is true. I will state it without any proof:

> **Theorem.** (Well-founded recursion) Let $G:V\to V$ be a class function and $(X,\prec)$ be a well-founded class such that
$\operatorname{ext}\_\prec(x)=\\{y\in X : y\prec x\\}$ is always a set for $x\in X$.
Then there is a function $F:X\to V$ such that $F(x) := G(F\upharpoonright \operatorname{ext}\_\prec(x))$.

Some readers might wonder the meaning of $F\upharpoonright \operatorname{ext}\_\prec(x))$. Reminding set-theoretic definition of function might be helpful to get its meaning: $F\upharpoonright \operatorname{ext}\_\prec(x))$ is a set of all pairings $\langle y, F(y)\rangle$ for all predessors $y$ of $x$. Therefore, we can say $F(x)$ is defined from the value of predecessors of $x$ under $F$.

<!-- Set-theoretic hierarchy -->
One of important consequence of the axiom of regularity is it provides a hierarchical structure of $V$:
define the collection $\langle V_\alpha\mid \alpha\in\mathrm{Ord}\rangle$ recursively as follows:

* $V_0=\varnothing$,
* $V_{\alpha+1} = \mathcal{P}(V_\alpha)$ (where $\mathcal{P}(X)$ is a power set of $X$.)
* $V_\delta = \bigcup_{\alpha<\delta} V_\alpha$ for limit $\delta$.

It is easy to see that $\langle V_\alpha\mid \alpha\in\mathrm{Ord}\rangle$ is an increasing family of sets.

We call the union of all $V_\alpha$s a *collection of all pure sets*: elements of the class are called "pure sets" because they are constructed from the empty set, not involving with any peculiar sets (like Quine atoms -- sets satisfying $x=\\{x\\})$) or urelements -- objects that could be elements but not sets.

Since the axiom of regularity gets rid of these peculiar sets, we may expect the axiom of regularity proves every set is a pure set: that is, $V=\bigcup_{\alpha\in\mathrm{Ord}} V_\alpha$:

> **Theorem.** $V=\bigcup_{\alpha\in\mathrm{Ord}} V_\alpha$. That is, every set is a pure set.

*Proof.* We will prove it by using $\in$-induction we have proved. Assume that every element of $x$ is a member of some $V_\alpha$. For each $y\in x$, associate the ordinal $\alpha_y$ satisfying $y\in V_{\alpha_y}$. It is like to require the axiom of choice in the first glance, but in fact, we can in fact define $\alpha_y$ in a canonical way by letting
\\[\alpha_y=\min \\{\alpha\mid y\in V_\alpha\\}.\\]
Now take $\alpha=\sup\\{\alpha_y\mid y\in x\\}$. I will claim that $x\in V_{\alpha+1}$: by definition of $\alpha_y$, we have $x\subseteq \bigcup_{y\in x} V_{\alpha_y}\subseteq V_\alpha$. That is, we have $x\subseteq V_\alpha$, and $x\in V_{\alpha+1}$ follows from the definition of $V_{\alpha+1}$.

<!-- Rank of sets -->
The hierarchical structure of $V$ allows us to impose a *rank* of sets: every set appears in some $V_\alpha$ as the hierarchy grows up, and some sets do not appear before to develop the hierarchy enough. This "how much" can be used to measure the complexity of sets.
> **Definition.** The rank $\operatorname{rank} x$ of $x$ is the least ordinal $\alpha$ such that $x\subseteq V_\alpha$.

It is not hard to check that $\operatorname{rank} \alpha=\alpha$ for all ordinal $\alpha$.

<!-- Axiom of collection -->
We can make use of the hierarchical aspects of the universe to strenghten the axiom of replacement: 

> **Theorem.** Let $C(x)$ be a class indexed by $x\in A$ for some set $A$. If $C(x)$ is not empty for each $x\in X$, then there is a  family of non-empty sets $\\{\hat{C}(x) \mid x\in X\\}$ such that $\hat{C}(x)\subseteq C(x)$.

*Proof.* For each $x\in X$, define $\alpha_x$ by
\\[\alpha_x := \min \\{\alpha \mid C(x)\cap V_\alpha\neq\varnothing\\}.\\]
Now define $\hat{C}(x):= V_{\alpha_x}\cap C(x)$. We can see that $\\{\hat{C}(x)\mid x\in X\\}$ is a desired family of sets.

The technique used in the theorem -- collecting elements of $C(x)$ of least available rank -- is called *Scott's trick*: we apply it to reduce collection of classes to a collection of sets.
 For example, consider the Russellian definition of cardinals: define $a\sim b$ if and only if there is a bijection between $a$ and $b$. Hence we define cardinals as members of $V/\sim$; that is, cardinals are equivalence class up to the equipotency relation $\sim$.
Unfortunately, $V/\sim$ is ill-formed: each "member" of $V/\sim$ is a proper class, so we cannot collect all of them into a single class. 

Hopefully, we can resolve the problem by applying Scott's trick. Collect the following sets for each $x\in V$ instead of collecting the full equivalence classes:
\\[[x]_\sim := \\{y \mid x\sim y \text{ and if $x\sim z$ then $\operatorname{rank} z\le \operatorname{rank} y$ }\\}.\\]

By the same argument used in the previous proof, we can see that $[x]\_\sim$ is a set for each set $x$.
Moreover, every member of $[x]\_\sim$ has the same size with $x$, so we can say $[x]\_\sim$ "represents" the cardinal of $x$.

Russellian definition of cardinals is useful in choiceless set theory: the usual definition of cardinals -- defining it as initial ordinals -- breaks down if we do not have the axiom of choice. We do not know every set is equipotent with an initial ordinal, so there might be sets whose cardinal is not represented by initial ordinals.
The Russellian definition does not involve initial ordinals and the axiom of choice, and it forms cardinals from sets directly. Thus this definition works even if we do not have the axiom of choice.

I have not seen any application of collection outside of logic: in fact, the usual mathematics hardly uses the full power of ZFC.
However, the Axiom of Collection is important to do set theory: for example, set theorists construct various models of ZFC via forcing or inner model. The construction includes verifying axioms of ZFC over the models, and checking the validity of Collection is sometimes easier than that of the Replacement.

Let me digress a little from the main topic of this article: the readers might ask whether the axiom of collection can be proven without the axiom of regularity. The answer seems negative: [Karagila](https://math.stackexchange.com/a/1619246/53976) described how to construct a model of $\mathsf{ZFC}$ without regularity and collection, by using permutation model. 

<!-- Historical Account -->
I will finish this post by mentioning the historical aspect of the main character: the axiom of regularity. 
The following explanation is mainly due to [2] and [3].

A weak form of the axiom of regularity $x\notin x$ was introduced in 1906 by Zermelo to avoid Russell's paradox. However, he realized that restricting Full separation is sufficient to the paradox, so he abandoned it in 1908. In 1917, Mirimanoff studied ordinary sets, which we called as pure sets. However, he did not suggest every set must be pure.
Von Neumann introduced an axiom in 1925 to exclude some ill-founded sets, but this axiom is not sufficient to show every set is pure. He introduced the modern form of the axiom of regularity in 1928. However, it was Zermelo who adopt Regularity as an axiom of set theory first.

<!-- References -->

----

**References**

[1] Andreas Blass, *The interaction between Category theory and Set theory.*.

[2] Penelope Maddy, *Believing the axioms I.*

[3] Adam Rieger, *Paradox, ZF, and the Axiom of Foundation.*

[4] Harry Altman, *How can one prove the axiom of collection in ZFC without using the axiom of foundation?*
(retrived: 2020-03-12 02:56 +0900)