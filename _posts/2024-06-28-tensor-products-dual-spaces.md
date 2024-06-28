---
layout: post
title: <div class="text-center"> Tensor Products - part 2 </div>
tags: [Tensors, dual spaces, tensor product, explanantion of tensor product]
date: 2024-06-28
author: Kashish Jaswani
mathjax: true
---
$\textbf{What is the dual space?}$

Given a vector space $V$, a linear functional is of the form f : $V \rightarrow \mathbb{F}$.

The dual space, denoted by $V'$ is defined as <center> $V' = \{f | f : V \rightarrow \mathbb{F}\}$ </center> this is a vector space under function addition and scalar multiplication. 

Now, to motivate this definition of the tensor product, we need to understand what a tensor product is trying to accomplish.

We are trying to find a natural way of multiplying elements of two vector spaces. Here 'natural' means that the multiplication properties that we expect should be satisfied (such as distributivity).  

Let us see how. 

$\textbf{What are bi-linear functionals?}$ 

Given two vector spaces $V$ and $W$, a bi-linear functional is a map <center> $\beta$ : $V$ $\otimes$ $W \rightarrow \mathbb{F}$ </center> which is linear in both its arguments. 

The set of all such maps forms the vector space $B(V,W)$.

Following is an example - 

1. Fix $v \in V$, and consider the mapping
<center> $T : V'$ x $\mathbb{F} \rightarrow \mathbb{F}$ </center>
<center> $T(\psi,k) = k  \psi(v)$ </center> 
T is a bi-linear functional on $V'$ x $\mathbb{F}$

2. Let <center> $\beta$ : $V$ x $V' \rightarrow \mathbb{F}$ </center>

<center> $\beta(v,\psi) = \psi(v)$ </center>

$\beta$ is a bi-linear functional on $V$ x $V'$. 

Intuitively, dim($B(V,W)$) = dim($V$)dim($W$) = mn. 

While it will not be proved here, it is easy to see that every linear functional can be written as a (m x n) matrix, and every (m x n) matrix can be associated to a linear functional. These two spaces are isomorphic, so they have the same dimension. \\

(why do we need basis free?????) 

So, to make a basis free definition, we define tensor products in the following unconventional way - 

The space $V \otimes W$ = $B(V',W')$, which are the bilinear functionals on the space $V'$ x $W'$.

Each element of this space is denoted by [$v \otimes w$] and defined as, <center> [$v \otimes w$]($\psi$, $\tau$) = $\psi$(v)$\tau$(w) </center> where $\psi \in V'$ and $\tau \in W'.$

The space $B(V',W')$ also has dimension as mn. This is because a vector space and its dual has the same dimension. 

Using the given definition we can check that the space satisfies the following properties - 

1. $(v_1 + v_2) \otimes w = (v_1 \otimes w) + (v_2 \otimes w)$

2. $v \otimes (w_1 + w_2) = (v \otimes w_1) + (v \otimes w_2)$ 

3. $(\lambda v) \otimes w = \lambda(v \otimes w)$ 

4. $v \otimes (\lambda w) = \lambda(v \otimes w)$.
