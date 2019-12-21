---
layout: post
title: problem concerning euler constant
category: about math
---
<head>
<script type="text/javascript" async
      src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js?config=TeX-MML-AM_CHTML">
    </script>
</head>

Recently when I was browsing MSE, I came across a question about Euler constant. 

 The problem is:
<blockquote>
How to show that
<center>
$$
\lim_{n\to\infty}\left[\sum^n_{k=1}\frac{1}{k}-\ln(n)\right]=0.5772\ldots
$$
</center>
No clue at all. Need help! Appreciated!
</blockquote>
 
However, a certain part of the second answer confused me. 

>
<strong>Abel's partial summation technique:</strong>
<br>
Let $$A(n) = \displaystyle \sum_{k=1}^n a(k)$$. We then have
<blockquote>
<center>
$$
 \begin{align*}
\sum_{n=1}^{N} a(n) f(n) & = \sum_{n=1}^{N} f(n) (A(n)- A(n-1)) = \sum_{n=1}^{N} A(n) f(n) - \sum_{n=1}^{N} A(n-1) f(n)\\
& = \sum_{n=1}^{N} A(n)f(n) - \sum_{n=0}^{N-1} A(n) f(n+1)\\
& = A(N)f(N) - A(0) f(1) - \sum_{n=1}^{N-1} A(n) (f(n+1)-f(n))
\end{align*}
$$
</center>
(The above is nothing but the discrete version of integration by parts).
$$
\sum_{n=1}^{N} a(n) f(n) = \int_{1^-}^{N^+} f(t) d(A(t)) =  f(t) A(t) \rvert_{1^-}^{N^+} - \int_{1^-}^{N^+} A(t) f'(t) dt
$$
(The second integral can be interpreted as a Riemann-Stieltjes integral.)
</blockquote>
<a href="https://math.stackexchange.com/questions/344314/showing-that-lim-n-to-infty-sumn-k-1-frac1k-lnn-0-5772-ldots?noredirect=1&lq=1">Here is the original post.</a>

&#8195;&#8195;The first part is clear. But for the second part, the equation $$\displaystyle 
\sum_{n=1}^{N} a(n) f(n) = \displaystyle \int_{1^-}^{N^+} f(t) d(A(t))$$ in particular, I was suprised to see such a peculiar expression of integral which I cann't recognize at all and that a discrete summation could be turned into an integral so easily. So I asked Mr.Zhou Ruisong for help. He deemed that $$\displaystyle \int_{1^-}^{N^+} f(t) d(A(t))$$ stood for $$\displaystyle \lim_{a\rightarrow 1^{-}} \lim_{b \rightarrow N^{+}} \int_{a^-}^{b^+} f(t) d(A(t))$$ and that $$A(n)=A(\lfloor n\rfloor)$$ for real $$n$$, but with uncertainty. Along with his two sensible assumptions, I tried to wrote down a proof of the formular.
<br><br>
<strong>Proof</strong>
Assume that $$A:\mathbb{R}\rightarrow\mathbb{R}$$ and $$A(n)=A(\lfloor n\rfloor)$$ for real $$n$$, $$f:\mathbb{R}\rightarrow\mathbb{R}$$ is continuous.

&#8195;&#8195;Let's consider the integer inteval $$[1,N]$$.

&#8195;&#8195;Given $$\epsilon>0$$. Let a partition $$P=\{x_0,x_1,\dots,x_n\}$$ s.t. $$U(f,P,A)-L(f,P,A)<\epsilon$$,
<br>
$$x_{i-1}<x_{i}$$  $$\forall i\in [1,n]$$, $$x_{0}=1-a$$ where $$a\in (0,1)$$, $$x_{n}=N+b$$ where $$b\in (0,1)$$ and $$\{x\vert x=k-\frac{1}{2},k\in \mathbb{N}^{*}\cap [1,N+1]\}\subset P$$.

&#8195;&#8195;Then,

<center>

$$
\begin{align*}\Bigg \vert \sum_{i=1}^{n} f(t_i)\big [ A(x_i)- A(x_{i-1})\big ] - \int_{1-a}^{N+b} fdA \Bigg \vert < \epsilon \qquad \forall t_{i}\in[x_{i-1},x_{i}].\end{align*}
$$

</center>

&#8195;&#8195;In particular, we let $$t_{i}=\lfloor x_{i}\rfloor$$ if $$x_{i-1}<\lfloor x_{i}\rfloor < x_{i}$$. Thus,

<center>
$$
\sum_{i=1}^{n} f(t_i)\big [ A(x_i)- A(x_{i-1})\big ]=\sum_{i=1}^{N} f(i)\big [ A(i)- A(i-1)\big ].
$$
</center>

&#8195;&#8195;Hence,
<center>
$$
\begin{align*}	\Bigg \vert \sum_{i=1}^{n} f(t_i)\big [ A(x_i)- A(x_{i-1})\big ] - \int_{1-a}^{N+b} fdA \Bigg \vert=    \Bigg \vert \sum_{i=1}^{N} f(i)\big [ A(i)- A(i-1)\big ] - \int_{1-a}^{N+b} fdA \Bigg \vert < \epsilon.\end{align*}
$$
</center>

&#8195;&#8195;Since $$\epsilon$$ is arbitrary, we get 

<center>
$$
\begin{align*}    \sum_{i=1}^{N} f(i)\big [ A(i)- A(i-1)\big ] =\int_{1-a}^{N+b} fdA.\end{align*}
$$
</center>
&#8195;&#8195;Finally, letting $$N+b \rightarrow N^{+}$$, $$1-a \rightarrow 1^{-}$$, we obtain 

<center>
$$
\begin{align*}    \sum_{i=1}^{N} f(i)\big [ A(i)- A(i-1)\big ] =\int_{1^{-}}^{N^{+}} fdA,\end{align*}
$$
</center>
which is the desired result.

(Afterwards I discovered that $$1^{-}$$ denotes $$1-\epsilon$$, where $$\epsilon>0$$ is arbitrarily small and $$N^{+}$$ denotes $$N+\epsilon$$, where $$\epsilon>0$$ is arbitrarily small, according to the other answer of the author. The idea of the proof remains unchanged, though.)

{% include post.html %}











