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

The first projectum $\rho^{J_\alpha}\_1$ of $J_\alpha$ is the least ordinal $\rho$ such that there is $p\in \[\mathrm{Ord}]^{<\omega}\]$ such that

$$\operatorname{Th}^{J_\alpha}_{\Sigma_1}(\rho\cup \{p\}) \notin J_\alpha.$$

The standard parameter $p^{J_\alpha}\_1$ of $J\_\alpha$ is the least lexicographical $p\in\[\mathrm{Ord}^{<\omega}}\]$ satisfying the above formula with $\rho =\rho^{J\_\alpha}\_1$.

In many easy cases, $p^{J\_\alpha}\_1 = \varnothing$; Like, when $\alpha=\omega\_n^\mathsf{CK}$, least recursively inaccessible, recursively Mahlo, etc. Here let me present an example of $\alpha$ with $p^{J\_\alpha}_1\neq \varnothing$.

> **Claim.** Let $\sigma\_0<\sigma\_1$ be the first two stable ordinals. (That is, $\sigma\_0$ is the least stable ordinal, and $\sigma_1$ is the next least stable ordinal.) Then $p^{J_{\sigma\_1}}\_1 = \{\sigma\_0\}$.
>
> *Proof.* Let us recall the following known fact by Barwise (Theorem V.7.8): Let $A$ be the set of $a\in L$ for which there is a $\Sigma_1$-definition of $a$ using parameters $<\gamma$. Then $A=L\_\sigma$ for some $\sigma$, and $\sigma$ is the least stable ordinal $\ge \gamma$.
> This shows 
> 
> * $J\_{\sigma\_0} = \operatorname{Hull}^{J\_{\sigma_0}}\_{\Sigma\_1}(\varnothing)= \operatorname{Hull}^{J\_{\sigma\_1}}_{\Sigma\_1}(\varnothing)$, and 
> 
> * $J\_{\sigma\_1} = \operatorname{Hull}^{J\_{\sigma\_1}}\_{\Sigma\_1}(\sigma\_0\cup \{\sigma\_0\})$.
>
> We can also see that $J\_{\sigma\_1} = \operatorname{Hull}^{J\_{\sigma_1}}\_{\Sigma\_1}(\{\sigma\_0\})$, so $\rho^{J\_{\sigma\_i}}\_1 = \omega$ for $i=0,1$. We also have that $p^{J\_{\sigma\_1}}\_1\le\_\mathrm{lex} \\{\sigma_0\\}$. $p^{J_{\sigma_1}}_1$ cannot be smaller since if $q\subseteq \sigma_0$ is finite, then $\operatorname{Hull}^{J\_{\sigma\_1}}\_{\Sigma\_1}(\{q\}) = J\_{\sigma\_0}$.