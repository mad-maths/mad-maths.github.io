---
layout: post
title: <div class="text-center"> Tensor Products - part 3 </div>
tags: [Tensors, tensor product, explanantion of tensor product]
date: 2024-06-26
author: Kashish Jaswani
mathjax: true
---
My previous blog posts covered the two definitions of tensor products. In this one we look at a mapping which shows that these two seemingly
different approaches are in fact the same.


From here onwards, we by denote [$V \otimes W$] as the space defined through quotienting, and ($V \otimes W$) the space defined as maps on the dual spaces.

Consider <center> $\kappa$ : [$V \otimes W] \rightarrow$ ($V \otimes W$) where 

$\kappa([v \otimes w]) = (v \otimes w)(\psi, \tau) = \psi(v)\tau(w)$
</center>
for $\psi \in V'$ and $\tau \in W'$.
It is important to notice that here, we are sending an equivalence class to a corresponding function.

Now, we check if this is an isomorphism.
1. Is it \textbf{one-one}?


We pick  $v_1,v_2 \in V$ and $w_1, w_2 \in W$ such that $\psi(v_1), \tau(w_1), \psi(v_2),\tau(w_2) \neq 0$.
Let $\kappa([v_1 \otimes w_1]) = \kappa([v_2 \otimes w_2])$
$\Rightarrow$  $(v_1 \otimes w_1)(\psi, \tau) = (v_2 \otimes w_2)(\psi, \tau)$ 
$\Rightarrow$ $\psi(v_1)\tau(w_1) = \psi(v_2)\tau(w_2)$ -- (i)\\
From (i) we can conclude the following,
$\psi(v_1) = \psi(k_1v_2)$ where $k_1$ = $\frac{\tau(w_2)}{\tau(w_1)}$ and
$\tau(w_2) = \psi(k_2w_1)$ where $k_2$ = $\frac{\psi(v_1)}{\psi(v_2)}$
Note that $k_1$ = $k_2$ = k.
Using linearity, $\psi(v_1 - kv_2) = 0$ and
$\tau(w_2 - kw_1) = 0$ 
Since this is true for all $\psi \in V'$ and $\tau \in W'$, we can conclude that 
$v_1 = kv_2$ and $w_2 = kv_1$.

We have shown that $v_1 \otimes w_1$ = $k(v_2 \otimes w_1$) and
$v_2 \otimes w_2$ = $k(v_2 \otimes w_1$).
Hence, both are in the same equivalence class, and we have our desired result. 

2. Is it \textbf{onto}? 

Take any ($v \otimes w) \in (V \otimes W)$.
Its pre-image is the equivalence class [$v \otimes w$].

3. Is it a \textbf{homomorphism}?
$\kappa([v_1 \otimes w_1] + [v_2 \otimes w_2]) 
= (v_1 \otimes w_1 + v_2 \otimes w_2)(\psi, \tau)$
$= (v_1 \otimes w_1)(\psi, \tau) + (v_2 \otimes w_2)(\psi, \tau)$
$= \kappa([v_1 \otimes w_1]) + \kappa([v_2 \otimes w_2]) $.

<center> \textbf{We have our desired isomorphism.} </center>



