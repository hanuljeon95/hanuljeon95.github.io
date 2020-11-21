---
layout: post
mathjax: true
comments: true
title:  "A useful lemma for multivalued functions over $\mathsf{CZF}$"
date:   2020-08-30 03:15:00 +0900
categories: posts constructive-mathematics set-theory
tags: 
  - constructive-mathematics
  - constructive-set-theory
  - set-theory
published: true
---

The following lemma is frequently used when tackling Strong collection or Subset collection, but curiously, it is not formulated in a concrete way. I found this is useful, so I formulated a separate lemma in [1]. I post it as a separate post for availability:

> **Lemma.** Let $R: A\rightrightarrows B$ be a multi-valued function. Define $\mathcal{A}(R) : A\rightrightarrows A\times B$ by
> \\[\mathcal{A}(R) = \{\langle a,\langle a,b\rangle\rangle \mid \langle a,b\rangle \in R\},\\]
> then the following holds:
> 
> 1. $\mathcal{A}(R) : A\rightrightarrows S\iff R\cap S:A\rightrightarrows B$,
> 
> 2. $\mathcal{A}(R) : A\leftleftarrows S\iff S\subseteq R$.


*Proof.* 
For the first statement, observe that $\mathcal{A}(R): A\rightrightarrows S$ is equivalent to
\\[\forall a\in A \exists s\in S :\langle a,s\rangle \in \mathcal{A}(R).\\]
By the definition of $\mathcal{A}$, this is equivalent to

\\[\forall a\in A \exists s\in S [\exists b\in B: s=\langle a,b\rangle \land \langle a,b\rangle\in R].\\]

We can see that the above statement is in fact equivalent to $\forall a\in A\exists b\in B : \langle a,b\rangle\in R\cap S$, which means $R\cap S : A\rightrightarrows B$.
	
The proof of the second statement is also analogous: $\mathcal{A}(R): A\leftleftarrows S$ is equivalent to
\\[\forall s\in S \exists a\in A :\langle a,s\rangle \in \mathcal{A}(R).\\]
By unpacking $\mathcal{A}$, we have
\\[\forall s\in S \exists a\in A : [\exists b\in B : s=\langle a,b\rangle \in R].\\]
We can see that it readily implies and equivalent to $S\subseteq R$.

References
-----

1. Hanul Jeon, "The axiom of double complement and its counterparts." Manuscript [avaliable in the author's webpage](../files/doublecomplement_draft.pdf).