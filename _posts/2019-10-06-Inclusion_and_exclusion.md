---
layout: post
title: Inclusion-exclusion
category: about cs
---
<head>
<script type="text/javascript" async
      src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js?config=TeX-MML-AM_CHTML">
    </script>
</head>
&#8195;&#8195;The principle of inclusion-exclusion provides us with a technique for solving problems like couting. For example, how many numbers not exceeding $$1000$$ are divisible by $$7$$ or $$11$$? 

<br>

<i>solution</i>: Let $$A$$ be the set of positive numbers which are not exceeding $$1000$$ and divisible by 7, and let $$B$$ be the set of positive numbers which are not exceeding $$1000$$ and divisible by 11. Define $$\vert A\vert$$ to be the number of elements in $$A$$, we have

<center>

$$
\begin{equation}
    \begin{aligned}
        \vert A\cup B\vert&=\vert A\vert+\vert B\vert-\vert A\cap B\vert \\
        &=\lfloor \frac{1000}{7}\rfloor+\lfloor \frac{1000}{11}\rfloor-\lfloor \frac{1000}{7\times11}\rfloor \\
        &=220.
    \end{aligned}
\end{equation}
$$

</center>

&#8195;&#8195;Thus, the answer should be $$220$$.

&#8195;&#8195;In fact, there's a theorem.
<br>

<strong>Theorem(The principle of inclusion-exclusion) </strong> Let $$A_1, A_2, \dots, A_n$$ be finite sets. Then

<center>

$$
\begin{equation}
    \begin{aligned}
    	\vert\bigcup_{i=1}^{n}A_i\vert&=\sum_{1\le i\le n}\vert A_i\vert -\sum_{1\le i<j\le n}\vert A_i\cap A_j\vert\\
    	&+\sum_{1\le i<j<k\le n}\vert A_i\cap A_j\cap A_k\vert-\cdots+(-1)^{n}\vert \bigcap_{i=1}^{n}A_i\vert.
    \end{aligned}
\end{equation}
$$

</center>

<strong>Sample</strong>: <a href="https://codeforces.com/contest/1228/problem/E">[codeforces 1228E]Another filling the grid</a>

&#8195;&#8195;Let $$S_{i,j}$$ be a collection of situations with i rows and j colomns do not satisfy the condition, that is, for every grid in this i rows or j colomns, its value should be greater than 1. We could use a fomular to calculate this $$\vert S_{i,j}\vert$$:

<center>

$$
\vert S_{i,j}\vert=C_{n}^{i}\times C_{n}^{j}\times (k-1)^{n(i+j)-ij}\times (k-1)^{n^2-n(i+j)+ij}
$$

</center>

&#8195;&#8195;Now we want to obtain $$\vert \bigcup_{i,j}S_{i,j}\vert$$. By observation, we know that $$S_{i,j}=S_{i,0}\cap S_{0,j}$$,  $$S_{i,0}\subset S_{j,0}$$ if $$j<i$$,  $$S_{0,i}\subset S_{0,j}$$ if $$j<i$$ and $$S_{i,j}\cap S_{k,l}=S_{i,0}\cap S_{0,j}\cap S_{k,0}\cap S_{0,l}=S_{max(i,k),max(j,l)}$$. In additional, given the theorem, we can figure out that every  $$S_{i,j}$$ contributes to $$\vert \bigcup_{i,j}S_{i,j}\vert$$ with the coefficient $$(-1)^{i+j}$$. 

&#8195;&#8195;Then apply the theorem, we get

<center>

$$
\vert \bigcup_{i,j}S_{i,j}\vert=\sum_{i=0}^{n}\sum_{j=0}^{n}(-1)^{i+j}\times C_{n}^{i}\times C_{n}^{j}\times (k-1)^{n(i+j)-ij}\times (k-1)^{n^2-n(i+j)+ij},
$$

</center>

note that $$\vert S_{0,0}\vert$$, by fomular, equals to $$k^n$$, which is the total number of ways to fill the grid. And therefore the answer would be this $$\vert \bigcup_{i,j}S_{i,j}\vert$$. The time complexity of the algorithm should be $$O(n^{2}logn)$$.

&#8195;&#8195;The answer is required to take mod. The law of addition and multiplication under mod operation is well known. But this time we used the formular $$C_{n}^{i}=\frac{n!}{(n-i)!i!}$$ to calculate combination, hence the inverse of an element is needed. There is a trick to find the inverse of an element: applying Fermat's little theorem, 

<center>

$$
a^{p-1}\equiv1(mod \hspace{0.2cm}p)
$$

</center>

where $$p$$ is prime, $$(a,p)=1$$. Thus,

<center>

$$
a\times a^{p-2}\equiv 1(mod \hspace{0.2cm}p)
$$

</center>

i.e., $$a^{p-2}$$ is the inverse of $$a$$.
