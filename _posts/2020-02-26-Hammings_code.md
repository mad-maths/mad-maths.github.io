---
layout: post
title: Hamming's Code
cover-img: /assets/img/path.jpg
thumbnail-img: /assets/img/thumb.png
share-img: /assets/img/path.jpg
tags: [Hamming,code,error correction]
author: Kashish Jaswani
---

"Damn it, if the machine can detect an error, why can't it locate the position of the error and correct it?"

This frustration led to the first ever error correcting code, which opened up new ideas in the field of error correction.
Before Richard Hamming came up with his code, even the thought of 'error-correcting codes' seemed absurd, out-of-question. 

When I came across this code, the simple-genius of it all surprised me. Let us look at what this code does.

We work in $\mathbb{F_2}^{7}$ where a codeword $\textbf{c}$ is of the form ${c_1,c_2...c_7}$. 
(Each $c_i$ is either 0 or 1)

We chose our codeword such that the following three properties are satisfied - 
1. $c_1 + c_3 + c_5 + c_7$ = 0
2. $c_2 + c_3 + c_6 + c_7$ = 0
3. $c_4 + c_5 + c_6 + c_7$ = 0

  
5. 
