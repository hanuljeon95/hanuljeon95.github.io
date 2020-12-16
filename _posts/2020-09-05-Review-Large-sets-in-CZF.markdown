---
layout: post
mathjax: true
comments: true
title:  "Review: *Large sets in Constructive set theory* by Albert Ziegler, I"
date:   2020-08-16 03:15:00 +0900
categories: posts set-theory
tags: 
  - set-theory
  - constructive-mathematics
  - large-set-axiom
  - large-cardinal
published: false
---

Large set axiom is a constructive analogue of large cardinals in classical set theory. It is known that ordinals are ill-behaved constructively, and this is the reason why we impose 'large cardinal properties' into sets directly and handle them. This is not even unusual for classical set theoriests, because many properties of large cardinals are intertwined with the property of $V_\kappa$ or $H_\kappa$ for $\kappa$.

There are just a few papers that are dealing with constructive set theory. Thus it is not surprising that relevant references for specific topics on constructive set theory are scarce. Albert Zeigler's doctoral thesis sheds a ray of light on the ignorance of us about large sets. The aim of this post is to summarize and illustrate the main results of Zeigler's thesis. I hope it would be helpful for myself and future readers of his thesis.

Explaining basic notions
------

Chapter 1 and 2 is devoted to explain the main results of the paper and  introductory notions for large sets. I will not go through about all basic notions. The readers could read these chapters directly or consult with relevant references, like the following materials:

> * Aczel, Peter and Rathjen, Michael. "Notes on constructive set theory", Mittag-Leffler Technical Report No. 40, 2000–2001.
> 
> * Aczel, Peter and Rathjen, Michael. *CST book draft*. Book manuscript. Avaliable in https://www1.maths.leeds.ac.uk/~rathjen/book.pdf

Despite that, it is worth to explain that how can we motivate *Relation Reflection Scheme* $\mathsf{RRS}$. Aczel introduced $\mathsf{RRS}$ to extract 'non-choice' principle from the scheme of *relative dependent choice* $\mathsf{RDC}$, which states every class relation on sets satisfies dependent choice.[^1]

$\mathsf{RRS}$ states that every class multi-valued function $R:A\rightrightarrow A$ on a class $A$ and a subset $a\subseteq A$, we can find $b\subseteq A$ such that $a\subseteq b$ and $b$ *reflects* $R$: that is, $R:b\rightrightarrow b$.
As its name suggests, it is a type of reflection scheme. It is not known that $\mathsf{RRS}$ is independent of $\mathsf{CZF}$. Interestingly, Andrew Swan and Ingo Blechschmidt and proved that the strengthening of $\mathsf{RRS}$ called $\mathsf{RRS_2}$ is equivalent with reflection scheme over $\mathsf{IZF}$. The proof can be founded in

> Andrew Swan and Ingo Blechschmidt, *Reflections on reflection for intuitionistic set theories*. Manuscript. Available in https://rawgit.com/iblech/internal-methods/master/paper-reflection.pdf

Behavior of large sets
------

Chapter 3 is short, but interesting chapter. We know that large cardinals are ordered linearly. This is never true constructively: we will see later that there are inaccessible sets $I$ and $J$ such that neither $I\subseteq J$ nor $J\subseteq I$. However, if $I\cap V_2=J\cap V_2$, then $I$ and $J$ are the same. The proof uses coding sets into truth values (which is just a subset of $1=\{0\}$.) Let me describe how the technique of 'coding into truth values' works and the brief description of Zeigler's proof.




Section 4.1 explains when the large set axioms are preserved. It is well-known that small forcing preserves most large cardinal axioms, and this is what Section 4.1 shows. It uses unfamilar notion called *applicative topology*, but we will not use the full structure of it. The definition of applicative topology looks like a mere combination of realizability and formal topology, and the thesis just uses realizability to derive metatheoretic results.

Section 4.2 discusses about the disjunction and existence properties of large set axioms. 

Further behavior of large sets
------



------

[^1] The formal statement is as follows: for every class $A$ and $R\subseteq A\times A$, if $\forall x\in A\exists y\in A (x,y)\in R$ and $a_0\in A$, then we can find a set function $f:\omega\to A$ such that $f(0)=a_0$ and $(f(n),f(n+1))\in R$ for all $n\in\omega$. $\mathsf{RDC}$ is a theorem of $\mathsf{ZF+DC}$ (and possibly $\mathsf{IZF+DC}$), but there is no reason to believe the implication holds over $\mathsf{CZF}$.
