---
layout: post
mathjax: true
comments: true
title:  "An example of an ordinal with a non-empty standard parameters"
date:   2026-05-17 18:00:00 -0400
categories: posts 
tags: 
  - set theory
  - inner model theory
published: true
---

The first projectum $\rho^{J_\alpha}_1$ of $J_\alpha$ is the least ordinal $\rho$ such that there is $p\in [\mathrm{Ord]^{<\omega}]$ such that
\\[ \operatorname{Th}^{J_\alpha}_{\Sigma_1}(\rho\cup \{p\}) \notin J_\alpha. \\]
The standard parameter $p^{J_\alpha}_1$ of $J_\alpha$ is the least lexicographical $p\in [\mathrm{Ord}]^{<\omega}}$ satisfying the above formula with $\rho =\rho^{J_\alpha}_1$.

In many easy cases, $p^{J_\alpha}_1 = \varnothing$; Like, when $\alpha=\omega_n^\mathsf{CK}$, least recursively inaccessible, recursively Mahlo, etc. Here let me present an example of $\alpha$ with $p^{J_\alpha}_1\neq \varnothing$.

> **Claim.** Let $\sigma_0<\sigma_1$ be the first two stable ordinals. (That is, $\sigma_0$ is the least stable ordinal, and $\sigma_1$ is the next least stable ordinal.) Then $p^{J_{\sigma_1}}_1 = \{\sigma_0\}$.
>
> *Proof.* Let us recall the following known fact by Barwise (Theorem V.7.8): Let $A$ be the set of $a\in L$ for which there is a $\Sigma_1$-definition of $a$ using parameters $<\gamma$. Then $A=L_\sigma$ for some $\sigma$, and $\sigma$ is the least stable ordinal $\ge \gamma$.
> This shows 
> 
> * $J_{\sigma_0} = \operatorname{Hull}^{J_{\sigma_0}}_{\Sigma_1}(\varnothing)= \operatorname{Hull}^{J_{\sigma_1}}_{\Sigma_1}(\varnothing)$, and 
> 
> *$J_{\sigma_1} = \operatorname{Hull}^{J_{\sigma_1}}_{\Sigma_1}(\sigma_0\cup \{\sigma_0\})$.
>
> We can also see that $J_{\sigma_1} = \operatorname{Hull}^{J_{\sigma_1}}_{\Sigma_1}(\{\sigma_0\})$, so $\rho^{J_{\sigma_i}}_1 = \omega$ for $i=0,1$. We also have that $p^{J_{\sigma_1}}_1\le_\mathrm{lex} \{\sigma_0\}$. $p^{J_{\sigma_1}}_1$ cannot be smaller since if $q\subseteq \sigma_0$ is finite, then $\operatorname{Hull}^{J_{\sigma_1}}_{\Sigma_1}(\{q\}) = J_{\sigma_0}$.