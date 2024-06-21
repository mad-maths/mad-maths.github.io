---
layout: post
title: <div class="text-center"> The dreaded Tensor Product </div>
tags: [Tensors, tensor product, simple explanantion of tensor product]
date: 2024-06-16
author: Kashish Jaswani
mathjax: true
---
Throughout the texts I have encountered until now, the dreaded symbol $\otimes$ has popped up everywhere and my first real encounter with the 'Tensor Product' 
occured when I was dipping my toes into Representation Theory. In my efforts to understand this new mystical object, I scoured the internet 
and quickly realised that there are many interpretations of the tensor.

This and upcoming blog posts is an attempt to make the different definitions easy to understand, and to show that they are not so different after all.

This post assumes basic knowledge of vector spaces, basis and quotienting (will be covered).

$\textbf{We begin by defining a free vector space-}$

Given a set S, the free vector space over $\mathbb{F}$ on S is the set of all finite formal sums of elements of S over $\mathbb{F}$. 
Denote it by $V(S)$

For example - 
1. Let S = {x}   
   Then, $V(S)$ = {ax $|$ a $\in$ R}.
   
   Note, V(S) $\cong$ $\mathbb{R}$ $\cong$ $\mathbb{R}$ x.

3. Take S = R.
   
   $V(S)$ = $\{a_1v_1 + a_2v_2... + a_nv_n\}$

Note that we cannot combine $a_1v_1 + a_2v_2...a_nv_n$ using normal rules of multiplication since $v_1, v_2..,v_n$ are linearly independent. 

So, in a free vector space, each element of the set is considered as a basis vector, and each element is hence a finite sum of these basis vectors. Hence, this is a very large vector space. 

$\textbf{Now we will look at the construction of tensor products:}$

Consider the set S = {v $\ast$ w, v $\in$ V, w $\in$ W}

Note that here, the $\ast$ is just a symbol, do not think of it as an operation.

To make this clear, consider V = $\mathbb{R}^3$ and W = $\mathbb{R}^3$.

Then an elements of the set S looks like,
$$
\begin{bmatrix} 
1 \\ 
5 \\ 
2
\end{bmatrix} 
\ast  
\begin{bmatrix} 
2 \\ 
3 \\ 
8
\end{bmatrix}
$$
with no way of simplifying these.

Now consider $V(S)$ = span{v $\ast$ w, v $\in$ V, w $\in$ W}. 

Let $V(S) = V \ast W.$ 

An example element of $V \ast W$ is

2 $$
\begin{bmatrix} 
1 \\
5 \\ 
2
\end{bmatrix}
$$ $\ast$ $
\begin{bmatrix} 
8 \\
12 \\
32 
\end{bmatrix}
$
but again, we are dealing with formal sums, so there is absolutely no way to simplify this. 

To re-emphasize, every single element of S serves as a basis element of this set, indicating that this is a very huge set we are dealing with. 

It is from this huge set, we get our tensor product space. Let us see how - 

Looking at the space $V \ast W$, it will be 'nice' if the elements satisfied some properties which align with our intuition of multiplication. For example, in the previous element it 'feels' like we should be able to multiply 2 or factor out a 4.

So, we consider the following set, 
I = 
{% raw %}
$span\[ \begin{cases} 
     (cv) \ast w - c(v \ast w)
     v \ast (cw) - c(v \ast w)
     (v_1 + v_2) \ast w - (v_1 \ast w) + (v_2 \ast w)
     v \ast (w_1 + w_2) - (v \ast w_1) - (v \ast w_2)
   \end{cases}
\]$
{% endraw %}
and now finally, let,
<center>
$V \otimes W = \frac{V \ast W}{I}$. 
</center>

To demonstrate how the desired properties are satisfied, we take the element 

$(cv) \ast w - c(v \ast w) + I \in V \ast W$ for all $v \in V$ and $w \in W$. 

By definition of I, $(cv) \ast w - c(v \ast w) \in I$

Hence, $(cv) \ast w - c(v \ast w) = 0$

and, $(cv) \ast w = c(v \ast w)$.

We can verify all other properties in a similar fashion.

Each element of $V \otimes W$ is an equivalence class which looks like ($v \ast w) + I$, which we will now denote by $v \otimes w$.

<center> $\textbf{We have gotten our desired tensor product space.}$ </center>


