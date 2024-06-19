---
layout: post
mathjax: true
comments: true
title:  "Models of set theory and absoluteness"
date:   2020-08-30 03:15:00 +0900
categories: posts set-theory
tags: 
  - set-theory
published: false
---

*(This post is heavily based on [1] that introduces a basic concept of forcing.)*

It seems like that most mathematicians believe in the unique mathematical universe (if they are platonist), and most idealistic concept of mathematics is absolute and settled in this conceptual, but true universe. It is widely accepted that most mathematics is based on Zermelo-Fraenkel set theory with Choice ($\mathsf{ZFC}$), hence we may think the true mathematical universe also validates $\mathsf{ZFC}$. Since our set theory reflects the unique notion of the universe, it was natural to think that every mathematical statement is provable or refutable from $\mathsf{ZFC}$. It might be the reason why Cantor belived the continuum hypothesis is decidable over $\mathsf{ZFC}$, but his effort was ended in vain.

It turns out that $\mathsf{ZFC}$ does not prove or refute any random mathematical statement, by Gödel's famous incompleteness theorem. 

However, Cohen's forcing introdues the necessarity of the reason why we need more than one universe:[^1] he constructs a new universe (or a model of $\mathsf{ZFC}$, formally,) by adding a new set into an old universe, so that the new universe invalidates the continuum hypothesis.

We have a various type of universes (we will use the word *universe* to denote models of $\mathsf{ZFC}$ in this post), and it is natural to ask there is a concrete example of 


Proving independence - Why do we need more than one model of set theory?
--------

As mentioned earlier, proving the indenpendence of the continuum hypothesis begot forcing, and it is a procedure to create a new universe from an old universe. Why do need to produce a new model of $\mathsf{ZFC}$, and how is it related to independence results? Let me explain why.

The readers might know how groups or fields are defined: a list of axioms are given (called the axioms of groups or fields), and they are defined as structures that satisfy the given list of axioms. These axioms allow to prove basic facts on groups or fields, like $xx^{-1}=e$ on groups or $x\cdot 0=0$ on fields.

Now consider a sophomore who tried to prove the existence of $\sqrt{-1}$ just from the axiom of fields. We know that this pitiful sophomore ends up with nothing: we cannot prove or disprove it from the axioms of fields. Why? We know that the structure of reals or complexes form fields, and the former does not have $\sqrt{-1}$ while the latter does.

Let me formalize and generalize this idea.



[^1]: Some readers might disagree on that various set-theoretic techniques like forcing and inner model do not falsify the concept of single universe. I will not go through this disputation. Readers who are interested in the relevant discussion could refer [2].

References
-----

1. Hanul Jeon, "What is Forcing?" (Korean) Manuscript for *Madmathematics semiar* (2015), 51-76.
1. Antos, Carolin, et al. "Multiverse conceptions in set theory." *Synthese* 192.8 (2015): 2463-2488.
1. Chow, Timothy Y. "A beginner’s guide to forcing." *Communicating mathematics* 479 (2009): 25-40.
