---
layout: post
mathjax: true
comments: true
title:  "Infinite decreasing $\\in$-chains and the axiom of coutable choice"
date:   2020-08-16 03:15:00 +0900
categories: posts set-theory
tags: 
  - set-theory
  - axiom-of-choice
  - axiom-of-regularity
published: true
---

It is well-known that the axiom of regularity is equivalent that there is no $\in$-decreasing sequence: in other words, there is no sequence $\langle x_n\mid n<\omega\rangle$ such that $x_0\ni x_1\ni x_2\ni\cdots$. However, the proof of the equivalence needs the axiom of choice. One direction is easy and does not need any form of the axiom of choice. The other remaining direction ― which asks we can prove the axiom of regularity from the absence of $\in$-decreasing sequences ― needs the axiom of dependent choice. 

We may ask whether the axiom of dependent choice is the best. Mendelson [1] showed that the use of the axiom of choice is necessary for the proof. However, his model also does not satisfy the axiom of countable choice. Let me describe his construction in modern terms (and this is necessary for further discussions).

We want to construct a model which invalidates the axiom of regularity, while it still does not have an $\in$-decreasing sequence. The axiom of regularity states that $\in$ is well-founded so that every structure $(A,\in)$ has a minimal element. We can break the axiom of regularity by adding an ill-founded set $X$ into the ground model. However, it is also possible that the new set $X$ contains an $\in$-infinite sequence. We do want to avoid it as possible, but how? Since our goal is to show an independence result from the axiom of choice, looking at non-choice sets is a good start point.

There are various examples of non-choice sets, like amorphous sets. We will choose ordered Mostowski model because the model contains a linearly orderable set $(J,<)$ that does not contain any countable increasing or decreasing sequences. Hence we will add an ill-founded set $X$ such that $(X,\in)$ is *isomorphic to* $(J,<)$.

How can we add the desired set, however? Brian [2] studied well about how to add an ill-founded set into a universe. His paper concentrates on the models of $\mathsf{ZFC}$ except for foundation, but his method can be extended to choiceless settings. The main ingredient we need is the following theorem that is effectively given by Brian:
> **Theorem.** (Brian) Working over ZF with a proper class of atoms, let $J$ be a collection of atoms. Assume that $\theta: J \to \mathrm{WF}[J]$ is a *good system*, that is, $\theta$ is injective and $\theta(x)=S_x\cup J_x$ for some pure set $S_x\in \mathrm{WF}$ and $J_x\subseteq J$. Then there is a model $(M_\theta,\epsilon)$ of ZF without foundation, that contains a copy of $V$ and $J$, such that 
> \\[ x\epsilon y\iff V[J]\models x\in \theta(y) \\]
> for all $x,y\in J$.
> Moreover, if the model satisfies \\(\mathsf{AC}_{\kappa}\\) or \\(\mathsf{DC}_{\kappa}\\), then so does \\(M_\theta\\).

(Here $\mathrm{WF}$ is the class of all well-founded sets, a.k.a., pure sets.)

Assume that we have an ordered Mostowski set $(J,<)$ in the ground model. Consider the good system $\theta:A\to \mathrm{WF}[J]$ given by
\\[ \theta(x)=\\{y\in J \mid y<x\\} \\]
Let $(M_\theta,\epsilon)$ be the model given by Brian's theorem. Then $x<y$ iff $x\in y$. Therefore $(J,\in)$ is a counterexample of the axiom of regularity.

It remains to show the following fact:
> **Theorem.** There is no infinite $\in$-decreasing chain in $M_\theta$.

The following internal recursion theorem, which is also established by Brian, is useful to prove the theorem:
> **Lemma.** Let $F:M_\theta\times M_\theta\to M_\theta$ and $F':J\to M_\theta$ be an internal class function. Then there is a unique $G:M_\theta\to M_\theta$, which is definable in $M_\theta$, such that $G(x)=F'(x)$ for all $x\in J$ and $G(x)=F(x, G\upharpoonright x)$ for all $x\in M_\theta\setminus J$.

We will define an internal rank function as follows: $\rho(x)=0$ for $x\in J$, and
\\[ \rho(x) = \sup\\{\rho(y)+1\mid y\epsilon x\\} \\]
for other sets $x\in M_\theta\setminus J$. Then $\rho(x)$ is always an ordinal. Moreover, we have

> **Lemma.** If $x\epsilon y$ then either $x,y\in J$ or $\rho(x)<\rho(y)$.
>
> *Proof.* Assume that $x\in y$ and $y\notin J$. (If $x\notin J$, then we have $y\notin J$ automatically, so we do not need to consider this case.) Then the conclusion is direct by definition.

We are ready to prove our theorem:
> *Proof of the Theorem.* Assume that $\langle x_n\mid n<\omega\rangle$ be an $\epsilon$-decreasing sequence. If $x_n\notin J$ for all $n<\omega$, then we have an infinite decreasing sequence of ordinals.
> Hence we have some $n<\omega$ such that $x_n\in J$. We can see that $x_m\in J$ for all $m\ge n$, so we have an infinite decreasing sequence on the ordered Mostowski set, which is impossible.

Unfortunately, the above model does not satisfy the axiom of countable choice: it is known that if $\mathfrak{m}$ is the cardinality of the ordered Mostowski set, then $2^\mathfrak{m}$ is not Dedekind-infinite. (See [3] for details.) Despite that, the same method can be used to prove the independence result still holds even under the axiom of countable choice or its stronger form $\mathsf{AC}_\lambda$.

Fix a regular cardinal $\kappa$ and start from the permutation model given by Theorem 8.12. of [3]. This model contains a set of atoms $J$ with a partial order $<$. Moreover, the permutation model also satisfies the followings:

* It satisfies $\mathsf{AC}_\lambda$ for all $\lambda<\kappa$, and
* $(J,<)$ has no infinite branch.

Consider a good system $\theta$ defined by $\theta(x)=\\{y\in J\mid y>x\\}$ and a model $(M_\theta,\epsilon)$ given by $\theta$. Then $x\epsilon y$ iff $x>y$. By the same argument described above, the resulting model has no $\in$-decreasing sequences.

References
-----

1. Mendelson, E. "The Axiom of Fundierung and the Axiom of Choice." *Archiv für math. Logik und Grundlagenfors* 4 (1958), 67-70.
1. Brian, Will. "Non-well-founded extensions of V." *Mathematical Logic Quarterly* 159, 3 (2013), 167-176.
1. Jech, Thomas J. *The axiom of choice*. Courier Corporation, 2008.