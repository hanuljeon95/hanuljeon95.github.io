---
layout: post
mathjax: true
comments: true
title:  "Recursive analogue of a measurable cardinal?"
date:   2024-05-19 15:30:00 -0400
categories: posts 
tags: 
  - set theory
  - constructive mathematics
  - large cardinal
published: true
---

 Large cardinals at a low level have a *recursive* (or admissible) analogues. For example, admissible ordinals for regular cardinals, recursively inaccessible ordinals for inaccessible cardinals, recursively Mahlo ordinals for Mahlo cardinals, and $\Pi_3$-reflecting ordinals for weakly compact cardinals. We may ask if there is an admissible analogue for larger large cardinals, for example, measurable cardinals.

 One way to see a possible answer to the question is to view countable large ordinals through constructive set theory: More precisely, constructive set theories also have *large set axioms* corresponding to large cardinal axioms.

 But we need to set up which constructive set theory we are going to use since there are at least two non-equivalent constructive set theories: One is called $\mathsf{IZF}$, and the other is called $\mathsf{CZF}$. I will not give their formulations as you may find them from the Stanford Philosophy encyclopedia, but here are the notable differences between them we should know: $\mathsf{IZF}$ and its extensions tend to be equiconsistent with their extensions by the law of excluded middle, but extensions of $\mathsf{CZF}$ are usually very weak. For example,

$\mathsf{CZF}$ and $\mathsf{KP}$ are equiconsistent.
$\mathsf{CZF}$ plus "every set is contained in a regular set" is equiconsistent with $\mathsf{KP}$ plus "there is a proper class of admissible ordinals."
$\mathsf{CZF}$ plus "every set is contained in an inaccessible set" is equiconsistent with $\mathsf{KP}$ plus "there is a proper class of recursively inaccessible ordinals."
$\mathsf{CZF}$ plus "every set is contained in a Mahlo set" is equiconsistent with $\mathsf{KP}$ plus "there is a proper class of recursively Mahlo ordinals," and so on.
 However, the law of excluded middle turns $\mathsf{CZF}$ to $\mathsf{ZF}$, and large set axioms to the corresponding large cardinal axioms. For example, one can see that $\mathsf{ZF}$ + "there is an inaccessible set" is equiconsistent with $\mathsf{ZF}$ + "there is an inaccessible cardinal."[^1]

 Then, could it be possible to track what a recursive analogue for a measurable should be? We have no clear idea how to define a recursive analogue for measurable cardinals, but it is relatively easy to define a constructive analogue that I call *critical sets*, which is a 'critical point' of an elementary embedding $j\colon V\to M$. Of course, the notion of a critical point does not make sense in a constructive manner since we cannot say 'the least ordinal blah blah' over a constructive setting.[^2] Thus let us take the following definition:

> **Definition.** A set $K$ is *critical* if there is an elementary embedding $j\colon V\to M$ such that $K\in j(K)$ and $j(x)=x$ for all $x\in K$.

One might think that $\mathsf{CZF}$ with a critical set should have a low consistency strength as other large set axioms do. However, it turns out that $\mathsf{CZF}$ with a critical set exceeds the strength of $\mathsf{ZF}$ and more!

> **Theorem.** (J. and Matthews) $\mathsf{CZF}$ with a critical set implies the consistency of $\mathsf{ZFC + BTEE}$ plus set induction for $j$-formulas, where $\mathsf{BTEE}$ is Corazza's *Basic Theory of Elementary Embedding*, which proves 'there is an $n$-ineffable cardinal' for each (meta-)natural number $n$.

The previous theorem hints that if there is a recursive analogue for measurable cardinals, then it should be very large. Then what is a good candidate? I guess $0^\sharp$ should have this role: $0^\sharp$ is a *theory* for $L$ with countably many indiscernibles, and if $0^\sharp$ exists, then there is a proper class of indiscernibles for $L$. The first indiscernible is still countable (in $V$, not in $L$), and there is an elementary embedding $j\colon L\to L$ moving the indiscernible. I believe an affirmative answer to the following question bolsters the claim "$0^\sharp$ as a recursive analogue for a measurable:"

> **Question.** Are the following theories equiconsistent?
> 
> 1. $\mathsf{KP}$ + $0^\sharp$ exists. 
> 1. $\mathsf{CZF}$ + There is a non-trivial $\Sigma$-elementary embedding.[^3]

-----

[^1]: An inaccessible set may not precisely be a set of the form $V_\kappa$ for an inaccessible cardinal by the choice of the definition. The definition of an inaccessible set I implicitly used in this article is "a regular set satisfying the Regular Extension Axiom." This version of an inaccessible set becomes a transitive model of $\mathsf{ZF}$ plus "there is a proper class of regulars" over $\mathsf{ZF}$. However, $\mathsf{ZF}$ does not prove $V_\kappa$ thinks there is a proper class of regular cardinals for an inaccessible $\kappa$.

[^2]: For example, "Every subset of an ordinal has the least element" implies a form of excluded middle.

[^3]: The reason for choosing a $\Sigma$-elementary embedding instead of the full elementary embedding is rather technical: I once tried to generalize Passman's result on the first-order logic of $\mathsf{CZF}$ to its extension by large set axioms, and especially for critical sets. However,  the current method seems to refuse the generalization for the full elementary embedding. There might be some fine structural reason for the difficulty.