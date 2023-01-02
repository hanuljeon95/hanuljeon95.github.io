---
layout: post
mathjax: true
comments: true
title:  "Post-CHEESE: list of other open problems"
date:   2023-01-01 23:20:00 -0500
categories: posts  set-theory
tags: 
  - set-theory
  - classical-realizability
published: true
---

After [CHEESE workshop](http://karagila.org/cheese/), I had a short discussion with Richard Matthews, and we listed some open problems that might be interesting for future studies. I posted this list with Matthews' permission. I also added my own problems that were not mentioned during the discussion.

1. Work over $\mathsf{ZF}$, suppose that $X$ is a transitive model of second-order $\mathsf{ZF}^-$, the theory obtained from the second-order $\mathsf{ZF}$ by removing Powerset and adding the second-order Collection. Then do we have $X=H(\kappa)$ for $\kappa=\mathrm{Ord}\cap X$?
   
   Here we define $H(\kappa)$ by the set of all $x$ such that there is no surjection from $\operatorname{trcl}(x)$ to $\kappa$. $H(\kappa)$ is a set by [AK18].[^1] Note that $\kappa$ is regular:
  
   > *Proof.* Suppose that $\kappa$ is singular and $f\colon \alpha\to\kappa$ is a cofinal map such for some $\alpha<\kappa$. Then $\alpha\in X$, and by the second-order Replacement, the image of $f$ is a member of $X$. Thus $X$ thinks there is a cofinal set of $\mathrm{Ord}$, but $\mathsf{ZF^-}$ proves there is no such set. 
   
   Also, if $X$ is *any* model of second-order $\mathsf{ZF}^-$, then $X$ is well-founded, thus we can consider its Mostowski collapse instead.

1. Can we find a better upper bound for the consistency strength of $\mathsf{ZF^-}_j$ with $j\colon V\to V$? How about with the cofinality of $j$? The current upper bound for $\mathsf{ZF^-}_j$ with $j\colon V\to V$ is $\mathsf{ZFC}$ with $\mathrm{I}_1$, but I believe we can derive a sharp bound in terms of $\mathsf{KM}$ with a form of Wholeness axiom. Regarding the cofinality of $j$, there is no known bound in terms of $\mathsf{ZFC}$ with large cardinals. 

1. Does $\mathsf{Con(ZF+WA)}$ prove $\mathsf{Con(ZFC+WA)}$?
  This problem is related to how to force Choice while preserving very large cardinals, usually beyond supercompactness.

1. Work over $\mathsf{ZF^-}_j$ with a cofinal elementary embedding $j\colon V\to V$ with a critical point $\kappa$. Then the successor cardinal $\lambda^+$ of $\lambda=j^\omega(\kappa)$ exists?
   
   Matthews [M22] proves $\mathsf{ZFC}^-\_j$ with $j\colon V\to V$ cannot be cofinal if $V_\kappa$ exists. Hayut (on the last day of CHEESE) proved that the cofinal $j$ does not exist even if we do not assume the existence of $V_\kappa$.

1. Is there any good way to produce a model of $\mathsf{ZF}^-_j$ with $j\colon V\to V$ from $\mathsf{ZF}$ with a Reinhardt cardinal? Currently, there is no known way for it.
   
   As an associated question, we may ask the following: Suppose that there is a Reinhardt cardinal (or rank Berkely cardinal). Then do we have a proper class of regular cardinals $\gamma$ such that $H(\gamma)$ is a model of second-order $\mathsf{ZF^-}$?

----

Here is list of my own questions:

1. Which theory is stronger than the other? $\mathsf{ZF}^-_j$ with a cofinal $j\colon V\to V$, and $\mathsf{CZF}$ with a Reinhardt embedding. What makes this question interesting is that $\mathsf{CZF}$ proves a Reinhardt embedding $j\colon V\to V$ is cofinal. [Z14]
   
   (The rough idea of the proof in [Z14] is approximating $V_\alpha$ using Subset Collection. $\mathsf{CZF}$ itself does not prove $V_\alpha$ is a set, but $\mathsf{CZF}$ can prove its set-approximation exists.)

1. Can we define a constructive analogue of a Berkeley cardinal?

----

## References

* [AK21]  David Asperó and Asaf Karagila, **Dependent choice, properness, and generic absoluteness.** *Rev. Symb. Log.* 14 (2021), no. 1, 225–249.
* [M22] Richard Matthews, **Taking Reinhadt's Power Away.** *J. Symb. Log.* 87 (2022), no. 4, 1643–1662.
* [Z14] Albert Ziegler, **Large sets in constructive set theory.** PhD Thesis, University of Leeds, 2014.

----

[^1]: Here our definition of $H(\kappa)$ is slight different from that of [AK21].