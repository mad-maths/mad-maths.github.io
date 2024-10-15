---
layout: post
title: <div class="text-center"> Tensor Products - universal property </div>
tags: [Tensors, tensor product, explanantion of tensor product]
date: 2024-07-10
author: Kashish Jaswani
mathjax: true
---
It is usually hard to define a well defined function on a tensor product space because we deal with equivalence classes instead of elements. But, we can do this using the universal property, which says that,

(let $V, W, U$ be vector spaces over a field $\mathbb{F}$) 
Given a bi-linear map f : $V$ $\times$ $W$ $\rightarrow$ $U$, there exists a unique linear map 

$\hat{f} : V \otimes W$ $\rightarrow U$ such that $\hat{f} \circ T = f$

The easier function to define here is,
$T : V$ $\times$ $W \rightarrow V \otimes W$. 
Earlier in the text we verified that this is a bi-linear function.

Given a bi-linear map f : $V$ $\times$ $W$ $\rightarrow$ $U$.
Now we define function g : $V \ast W \rightarrow U$. This function should be easier to define, as the inputs are elements, not equivalence classes. 

Let g($\sum a_i v_i \ast w_i$) = $\sum a_i$ f($v_i,w_i$), g becomes a linear map.
Using the bi-linearity of f, we can show that $g|_I$ = 0, where I is the set considered before. 

Finally, define $\hat{f}(v \otimes w) = g(v \ast w$).
We need to check if $\hat{f}$ is well defined,
$\hat{f}(x + I)$ = g(x) where x is a coset
Any other coset representation looks like,
$\hat{f}(x + i + I)$ = g(x) + g(i) = g(x).

The uniqueness of $\hat{f}$ can be verified easily. 

Hence, we have a well defined unique map on a tensor product space, construction of which seemed difficult earlier. 
