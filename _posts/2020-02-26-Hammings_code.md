---
layout: default
title: Hamming's Code
cover-img: /assets/img/path.jpg
thumbnail-img: /assets/img/thumb.png
share-img: /assets/img/path.jpg
tags: [Hamming,code,error correction]
author: Kashish Jaswani
---
<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-AMS-MML_HTMLorMML">

</script>

"Damn it, if the machine can detect an error, why can't it locate the position of the error and correct it?"

This frustration led to the first ever error correcting code, which opened up new ideas in the field of error correction.
Before Richard Hamming came up with his code, even the thought of 'error-correcting codes' seemed absurd, out-of-question. 

When I came across this code, the simple-genius of it all surprised me. Let us look at what this code does.

We work in $\mathbb{F_2}^{7}$ where a codeword $\textbf{c}$ is of the form ${c_1,c_2...c_7}$. 
(Each $c_i$ is either 0 or 1)

The sender chooses the codeword such that the following three properties are satisfied - 
1. $c_1 + c_3 + c_5 + c_7$ = 0
2. $c_2 + c_3 + c_6 + c_7$ = 0
3. $c_4 + c_5 + c_6 + c_7$ = 0

Let the received word be $\textbf{x} = {x_1,x_2,..,x_7}$
Calculate the following values,
1. $z_1 = x_1 + x_3 + x_5 + x_7$
2. $z_2 = x_2 + x_3 + x_6 + x_7$
3. $z_3 = x_4 + x_5 + x_6 + x_7$

Observe the relationship between the two sets of equations.

Now we see something interesting happen. If our sent codeword matches the received word (no errors occur in transmission), then $z_1, z_2$ and $z_3$ should all be equal to 0.

But if a single error occurs, even then this code can detect where the error is. How?
Let's take an example.

Suppose our third bit ($c_3$) was flipped during transmission, hence there is an error in the third place ($x_3$).
This means $z_1$ and $z_2$ will be equal to 1 (here, addition is modulo 2). 
Note that then $z_1 + 2z_2$ = 3, the error term. (normal addition)

Taking another example, 
Suppose our sixth bit ($c_6$) was flipped during transmission, hence there is an error in the third place ($x_6$).
This means $z_2$ and $z_3$ will be equal to 1 (here, addition is modulo 2). 
Note that then $2z_2 + 4z_3$ = 6, the error term. (normal addition)

Testing it out for more terms, we arrive at the beautiful result, that the error digit can be found out by simply calculating -
$z_1 + 2z_2 + 4z_3$!
