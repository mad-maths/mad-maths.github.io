---
layout: post
title: <div class="text-center"> Hamming's Code </div>
tags: [Hamming,code,error correction]
date: 2024-06-11
author: Kashish Jaswani
thumbnail-img: /assets/img/hamming.jpg
mathjax: true
---
"Damn it, if the machine can detect an error, why can't it locate the position of the error and correct it?"

This frustration led to the first ever error correcting code, which opened up new ideas in the field of error correction.
Before Richard Hamming came up with his code, even the thought of 'error-correcting codes' seemed absurd, out-of-question. 

When I came across this code, the simple-genius of it all surprised me, and I get more excited every time I tell anyone about it. So, it is only fair to talk about this code in my first blog post. Here we go.

We work in ${F_2}^{7}$, which means that a codeword  $\textbf{c}$ is of the form ${c_1,c_2...c_7}$ and each $c_i$ is either 0 or 1.

The sender chooses the codeword such that the following three properties are satisfied - 
1. $c_1 + c_3 + c_5 + c_7$ = 0
2. $c_2 + c_3 + c_6 + c_7$ = 0
3. $c_4 + c_5 + c_6 + c_7$ = 0

Let the received word be $\textbf{x} = {x_1,x_2,..,x_7}$

Calculate the following values,
1. $z_1 = x_1 + x_3 + x_5 + x_7$
2. $z_2 = x_2 + x_3 + x_6 + x_7$
3. $z_3 = x_4 + x_5 + x_6 + x_7$

In these equations, addition is modulo 2. 

Observe the relationship (particularly, the indices) between the two sets of equations.

Now we see something interesting happen.

If our sent codeword matches the received word (no errors occur in transmission), then $z_1, z_2$ and $z_3$ should all be equal to 0.

But if a single error occurs, even then this code can detect where the error is. 

How?
Let's take an example.

Suppose our third bit ($c_3$) was flipped during transmission, hence there is an error in the third place ($x_3$).
This means $z_1$ and $z_2$ will be equal to 1. 
Note that then $z_1 + 2z_2$ = 3, the error term (normal addition).

Taking another example, 
Suppose our sixth bit ($c_6$) was flipped during transmission, hence there is an error in the third place ($x_6$).
This means $z_2$ and $z_3$ will be equal to 1. 
Note that then $2z_2 + 4z_3$ = 6, the error term (normal addition).

Testing it out for more terms, we arrive at the beautiful result, that the error digit can be found out by simply calculating - 

$z_1 + 2z_2 + 4z_3$ !


References - 
1. Lecture notes on Coding and Cryptography, by T.W. Korner.
2. The holder of copyright for the image is unknown, but it was taken from [here](https://archon.library.illinois.edu/archives/index.php?p=digitallibrary/digitalcontent&id=11804)
And [click here](https://docs.google.com/forms/d/e/1FAIpQLSeTZiwy-FhSm6Jk_lOAh74DxcmLywZS7RfJDOryZvTaj1gYbA/viewform?usp=sf_link) to subscribe to this blog.

