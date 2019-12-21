---
layout: post
title: relations between some double sequences and series of functions(SEQUENCE AND SERIES OF FUNCTIONS)
category: about math
---
<head>
<script type="text/javascript" async
      src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js?config=TeX-MML-AM_CHTML">
    </script>
</head>


<strong>8.3 Theorem</strong> <i> Given a double sequence $$\{a_{i,j}\}$$, $$i=1,2,3,\ldots, j=1,2,3,\ldots,$$ suppose that </i>

<center>

$$
\begin{equation}	\sum_{j=1}^{\infty}\vert a_{i,j}\vert=b_i\hspace{1cm}(i=1,2,3,\ldots)\end{equation}
$$

</center>

<i>and $$ \sum b_i$$ converges. Then</i>
<center>
$$
\begin{equation}	\sum_{i=1}^{\infty}\sum_{j=1}^{\infty}a_{i,j}=	\sum_{j=1}^{\infty}\sum_{i=1}^{\infty}a_{i,j}.\end{equation}
$$
</center>

<strong>Proof</strong> Let $$E$$ be a countable set, consisting of the points $$x_0, x_1, x_2, \ldots,$$ and suppose $$x_{n} \rightarrow  x_{0}$$ as $$n \rightarrow \infty$$. Define

<center>

$$
\begin{equation}	\begin{aligned}		f_i(x_n)&=\sum_{j=1}^{n}a_{i,j} \hspace{1cm}(i,n=1,2,3,\ldots),\\		f_i(x_0)&=\sum_{j=1}^{\infty}a_{i,j} \hspace{1cm}(i=1,2,3,\ldots),\\		g(x)&=\sum_{i=1}^{\infty}f_{i}(x) \hspace{1cm}(x\in E).	\end{aligned}\end{equation}
$$

</center>

And they are pretty well-defined. Since

<center>

$$
\begin{equation}	\lim_{n\rightarrow\infty} f_i(x_n)=f_i(x_0)\end{equation}
$$

</center>

and

<center>

$$
\begin{equation}	\lim_{n \rightarrow \infty}x_n=x_0,\end{equation}
$$

</center>

$$f_i$$ is continuous at $$x_{0}$$. In addition, since

<center>

$$
\begin{equation}	f_i(x_0)\leq \sum_{j=1}^{\infty}\vert a_{i,j}\vert=b_i\hspace{1cm}(i=1,2,3,\ldots),\\	f_i(x_n)\leq \sum_{j=1}^{\infty}\vert a_{i,j}\vert=b_i\hspace{1cm}(i=1,2,3,\ldots),\end{equation}
$$

</center>

and  $$ \sum b_i$$ converges, we know that $$g(x)=\sum f_i$$ converges uniformly, thus $$g$$ is continuous at $$x_{0}$$ too. The continuity of $$g$$ implies that

<center>

$$
\begin{equation}	\begin{aligned}		\lim_{n \rightarrow  \infty}g(x_n)&=g(x_0), \\		g(x_0)=\sum_{i=1}^{\infty}\sum_{j=1}^{\infty}a_{i,j}&=\lim_{n \rightarrow  \infty}g(x_n)=\lim_{n \rightarrow  \infty}\sum_{i=1}^{\infty}\sum_{j=1}^{n}a_{i,j}.	\end{aligned}\end{equation}
$$

</center>

&#8195;&#8195;Note that 

<center>

$$
\begin{equation}	g(x_n)=\sum_{i=1}^{\infty}\sum_{j=1}^{n}a_{i,j}	=\sum_{j=1}^{n}\sum_{i=1}^{\infty}a_{i,j},\end{equation}
$$

</center>

which can be proved by using the mathematical induction. 

&#8195;&#8195;Firstly, it's obivious that the equation is correct when $$n=1$$. Assume that it holds for $$n=k(k\in N^{*})$$. i.e.,

<center>

$$
\begin{equation}	g(x_k)=\sum_{i=1}^{\infty}\sum_{j=1}^{k}a_{i,j}=	\sum_{j=1}^{k}\sum_{i=1}^{\infty}a_{i,j},\end{equation}
$$

</center>

and then consider the situation where $$n=k+1$$. Since

<center>

$$
\begin{equation}	\begin{aligned}		g(x_{k+1})&=\sum_{i=1}^{\infty}\sum_{j=1}^{k+1}a_{i,j}=		\sum_{i=1}^{\infty}\sum_{j=1}^{k}a_{i,j}+\sum_{i=1}^{\infty}a_{i,k+1}\\		&=\sum_{j=1}^{k}\sum_{i=1}^{\infty}a_{i,j}+\sum_{i=1}^{\infty}a_{i,k+1}\\		&=\sum_{j=1}^{k+1}\sum_{i=1}^{\infty}a_{i,j},	\end{aligned}\end{equation}
$$

</center>

hence we conclude that 

<center>

$$
\begin{equation}	g(x_n)=\sum_{i=1}^{\infty}\sum_{j=1}^{n}a_{i,j}	=\sum_{j=1}^{n}\sum_{i=1}^{\infty}a_{i,j}.\end{equation}
$$

</center>

&#8195;&#8195;Thus, 

<center>

$$
\begin{equation}	\begin{aligned}		g(x_0)=\sum_{i=1}^{\infty}\sum_{j=1}^{\infty}a_{i,j}&=\lim_{n \rightarrow  \infty}g(x_n)=\lim_{n \rightarrow  \infty}\sum_{i=1}^{\infty}\sum_{j=1}^{n}a_{i,j}\\		&=\lim_{n \rightarrow  \infty}\sum_{j=1}^{n}\sum_{i=1}^{\infty}a_{i,j}\\		&=\sum_{j=1}^{\infty}\sum_{i=1}^{\infty}a_{i,j},	\end{aligned}\end{equation}
$$

</center>

i.e.,

<center>

$$
\begin{equation}	\sum_{i=1}^{\infty}\sum_{j=1}^{\infty}a_{i,j}=	\sum_{j=1}^{\infty}\sum_{i=1}^{\infty}a_{i,j}.\end{equation}
$$

</center>



























{% include post.html %}
