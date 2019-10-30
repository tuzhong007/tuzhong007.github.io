---
layout: post
title: a problem arised when using mathematical induction
category: about math
---
<head>
<script type="text/javascript" async
      src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js?config=TeX-MML-AM_CHTML">
    </script>
</head>

&#8195;&#8195;When I was tring to work out the proof of 
<a href="https://tuzhong007.github.io/about%20math/2019/10/26/relation-between-some-double-sequnces-and-series-of-functions.html">the theorem 8.3(Dominated convergence theorem)</a>, in one step I applied the mathematical induction to show that 
<center>
$$
\begin{equation}	\sum_{i=1}^{\infty}\sum_{j=1}^{n}a_{i,j}	=\sum_{j=1}^{n}\sum_{i=1}^{\infty}a_{i,j}.\end{equation}
$$
</center>
&#8195;&#8195;Then it occurs to me, that why can't I just simply letting $$n\rightarrow \infty$$ and get the intended result? After thinking for a while(referring to 4 days), I maybe understood eventually. The reason is that when $$n\rightarrow \infty$$, the series must include infinitely many terms. And since there is not an $$n$$ s.t. $$n+1=\infty$$, the situation where the series includes infinitely many terms can't be reached by the recursion process of the mathematical induction.

<br>
{% include post.html %}
