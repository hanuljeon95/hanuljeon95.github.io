---
layout: post
mathjax: true
comments: true
title:  "Axiom of Regularity ― an introduction"
date:   2020-02-14 23:00:00 +0900
categories: Set theory, 집합론
published: false
---

 Beginners of axiomatic set theory encounter a list of ten axioms of Zermelo-Fraenkel set theory (in fact, infinitely many axioms: Separation and Replacement are in fact not merely a single axiom, but a schema of axioms depending on a formula parameter, but it does not matter in this post.) Most of the axioms have a clear meaning, so not hard to accept: for example, Axiom of Pairing states we can find an unordered pair $\{a,b\}$ of $a$ and $b$, and Axiom of Union states we can find a union $\bigcup A$ of a set of sets $A$.
 Axiom of Choice might be a bit unclear and has a long historical debate whether this axiom should be accepted or not. However, we can find various applications of Axiom of Choice, and they provide a practical reason why we believe in Axiom of Choice, though there might be philosophical opposition which I will not cover.

 However, Axiom of Regularity has an unclear statement in a first glance:
> For each non-empty set $x$, there is $y\in x$ such that $x\cap y=\varnothing$.
Most of the readers ― especially those who have not learned axiomatic set theory ― have not seen this strange axiom. It has no non-trivial application to usual mathematics. Moreover, the usual mathematics seems like neutral to this axiom: accepting or denying the axiom does not change almost all of the usual mathematics.

 As a result, this unfortunate axiom is fallen into an abyss of oblivion as Blass mentioned in [1] by
> (...) the axiom of regularity has suffered an even worse fate than the axiom of choice; people don't deny the axiom of regularity, they just ignore it.

 Why set theorists add such an unclear and even seems-like redundant axiom as a part of ZFC? This post aims to explain the reason why.

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

*Proof.* Take any $x\in C$ and consider $y=\{z\in x\mid z\in C\}$. If $y$ is empty, then $x$ is $\in$-minimal element of $C$. If not, then $y$ is not empty and $y$ has a $\in$-minimal element, namely $w$. We can see be definition that $w$ is $\in$-minimal element of $C$.

----
<!-- Consequence : set induction and rank of sets -->
 We formulated well-foundedness by mimicing well-orderedness. Therefore, we could expect well-foundedness resembles well-orderedness. For example, no well-ordered set allows infinitely decreasing chains. We can say the same thing for well-founded sets:
> **Theorem** Let $\prec$ be a well-founded relation over a set $X$. Then there is no infinite $\prec$-decreasing sequence over $X$; that is, no sequence $\langle x_n\mid n\in\omega\rangle$ over $X$ satisfies $x_0\succ x_1\succ x_2\succ\cdots$.
*Proof.* Let $\langle x_n\mid n\in\omega\rangle$ be an infinite $\prec$-decreasing sequence over $X$. Let $y$ be a $\prec$-minimal element of $\{x_n\mid n\in\omega\}$. Since $y=x_m$ for some $m$ and $x_m\succ x_{m+1}$, we have a contradiction.

Especially, we have
> **Corollary** (ZF) There is no $\in$-decreasing sequence; that is, no $\langle x_n\mid n\in\omega\rangle$ satisfies $x_0\ni x_1\ni x_2\ni\cdots$.

<!-- Have to explain: no decreasing in-sequence -->

 Well-orderedness has useful consequences: for example, every well-ordered set allows transfinite induction and transfinite recursion. The same holds for general well-founded relations, not only for well-ordered sets:

> **Theorem** (Well-founded induction)
> 
> Let $(X,\prec)$ be a set with a well-founded relation $\prec$. 





<!-- Historical Account -->

<!-- Set-theoretic hierarchy -->

<!-- References -->

----

[1] Andreas Blass, *The interaction between Category theory and Set theory*. 
[2] Penelope Maddy, *Believing the axioms I*.
