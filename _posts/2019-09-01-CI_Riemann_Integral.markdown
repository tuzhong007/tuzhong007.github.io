---
layout: post
title: Construction Ideas(THE RIEMANN-STIETJES INTEGRAL)
category: about math
---

<head>
<script type="text/javascript" async
      src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js?config=TeX-MML-AM_CHTML">
    </script>
</head>

<strong>6.6 Theorem</strong> <i>Suppose $$\alpha$$ is a monotonically increasing function on $$[a,b]$$.  f $$\in \mathscr{R}(\alpha)$$ on $$[a,b]$$ if and only if for every $$\epsilon>0$$ there exists a partition P such that</i>

<center>

$$
\begin{equation}
	U(P,f,\alpha)-L(P,f,\alpha)<\epsilon.
\end{equation}
$$

</center>

&#8195;&#8195;This theorem provides a fundamental idea about solving questions like "how to check a function to be Riemann-integrable or not". By definition, we have

<center>

$$
U(P,f,\alpha)-L(P,f,\alpha)=\sum\limits_{i=1}^{n}(M_i-m_i)\Delta\alpha_{i},
$$

</center>

where for a partition P,

<center>

$$
\begin{equation}
\begin{aligned}
M_i&=\sup f(x) \hspace{1cm}(x_{i-1}\leq x \leq x_{i}), \\
m_i&=\inf f(x) \hspace{1cm}(x_{i-1}\leq x \leq x_{i}), \\
\Delta\alpha_{i}&=\alpha(x_{i})-\alpha(x_{i-1}).
\end{aligned}
\end{equation}
$$

</center>

&#8195;&#8195;Given $$\epsilon>0$$. Naturally, we could imagine that if $$f$$ is Riemann-integrable, then $$\sum\limits_{i=1}^{n}(M_i-m_i)\Delta\alpha_{i}$$ should be small enough for some partition P. We hope to construct some P which meet the requirement.


&#8195;&#8195;There is an idea on constructing a suitable P. For each term, we either make $$(M_i-m_i)$$ or $$\Delta\alpha_{i}$$ small. Then this P may suffice.

&#8195;&#8195;The proof of the theorem below should be an example.

<strong>6.8 Theorem</strong> <i>If f is continuous on $$[a, b]$$ then f $$\in \mathscr{R}(\alpha)$$ on $$[a,b]$$.</i>

<strong>Proof</strong> Given $$\epsilon>0$$. Since $$f$$ is continuous, and $$[a,b]$$ is compact, we know $$f$$ is uniformly continuous, i.e., given $$\epsilon>0$$, there exist a $$\delta>0$$ such that $$\forall x,y\in [a,b]$$, if $$d(x,y)<\delta$$, then $$d(f(x),f(y))<\epsilon$$. Hence, if we choose a partition with $$\Delta\alpha_{i}<\delta$$, then $$(M_i-m_i)<\epsilon$$. We thus get

<center>

$$
\begin{equation}
\begin{aligned}
U(P,f,\alpha)-L(P,f,\alpha)&=\sum\limits_{i=1}^{n}(M_i-m_i)\Delta\alpha_{i} \\
&< \epsilon\sum\limits_{i=1}^{n}\Delta\alpha_{i} \\
&= \epsilon (\alpha(b)-\alpha(a)).
\end{aligned}
\end{equation}
$$

</center>

Since $$\epsilon$$ is arbitrary, for each $$\eta>0$$, we pick $$\epsilon$$ which satisfy the inequality $$\epsilon (\alpha(b)-\alpha(a))<\eta$$ . We finally get 

<center>

$$
\begin{equation}
\begin{aligned}
U(P,f,\alpha)-L(P,f,\alpha)<\eta,
\end{aligned}
\end{equation}
$$

</center>

and therefore $$f\in \mathscr{R(\alpha)}$$.


















