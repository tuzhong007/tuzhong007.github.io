---
layout: post
title: linear transformations and derivatives(FUNCTIONS OF SERVERAL VARIABLES)
category: about math
---
<head>
<script type="text/javascript" async
      src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js?config=TeX-MML-AM_CHTML">
    </script>
</head>

<strong>Linear transformations</strong> A mapping $$L$$ from a vector space $$V$$ into a vector space $$W$$ is said to be a <i>linear transformation</i> if

<center>
$$
\begin{equation}    	\begin{aligned}          	L(\alpha \textbf{v}_{1}+\beta \textbf{v}_{2})=    	\alpha L(\textbf{v}_{1})+\beta L(\textbf{v}_{2})	\end{aligned}\end{equation}
$$
</center>

for all $$\textbf{v}_{1} ,\textbf{v}_{2} \in V$$ and for all scalars $$\alpha$$ and $$\beta$$.

&#8195;&#8195;In fact, for every linear transformation there exists a matrix corresponding to it.

&#8195;&#8195;Consider a linear transformation $$L$$ from $$V$$ into $$W$$, where $$V$$ and $$W$$ are vector spaces of dimension $$n$$ and $$m$$, respectively. Let $$E=\{\textbf{v}_{1} ,\textbf{v}_{2}, \dots, \textbf{v}_{n}\}$$ be an ordered basis for $$V$$ and $$F=\{\textbf{w}_{1} ,\textbf{w}_{2}, \dots, \textbf{w}_{m}\}$$ be an ordered basis for $$W$$. Let $$L$$ be a linear transformation mapping $$V$$ into $$W$$. If $$\textbf{v}$$ is any vector in $$V$$, then we can express $$\textbf{v}$$ in terms of the basis $$E$$:

<center>
$$
\begin{equation}    	\begin{aligned}          	\textbf{v}=\sum_{j=1}^{n}x_{j} \textbf{v}_{j}.	\end{aligned}\end{equation}
$$
</center>
&#8195;&#8195;For $$j=1,2,\dots,n$$, let $$\textbf{a}_{j}=(a_{1j},a_{2j},\dots,a_{mj})^{T}$$ be the coordinate vector of  $$L(\textbf{v}_{j})$$ with respect to $$\{\textbf{w}_{1} ,\textbf{w}_{2}, \dots, \textbf{w}_{m}\}$$; i.e.,
<center>
$$
\begin{equation}    	\begin{aligned}          	L(\textbf{v}_{j})=\sum_{k=1}^{m}a_{kj} \textbf{w}_{k}.	\end{aligned}\end{equation}
$$
</center>
Then, 
<center>
$$
\begin{equation}    	\begin{aligned}          	L(\textbf{v})&=L(\sum_{j=1}^{n}x_{j} \textbf{v}_{j}) \\    	&=\sum_{j=1}^{n}x_{j}L(\textbf{v}_{j}) \\    	&=\sum_{j=1}^{n}x_{j}(\sum_{k=1}^{m}a_{kj} \textbf{w}_{k}) \\    	&=\sum_{k=1}^{m}(\sum_{j=1}^{n}x_{j}a_{kj}) \textbf{w}_{k}.	\end{aligned}\end{equation}
$$
</center>

&#8195;&#8195;If we let $$A=(a_{ij})=(\textbf{a}_{1},\textbf{a}_{2},\dots,\textbf{a}_{n})$$ and $$y_{i}=\sum_{j=1}^{n}x_{j}a_{kj}$$, then
<center>
$$
\begin{equation}    	\begin{aligned}          	\textbf{y}_{i}=(y_{1},y_{2},\dots,y_{m})^{T}=A\textbf{x}	\end{aligned}\end{equation}
$$
</center>
is the coordinate vector of $$L(\textbf{v})$$ with respect to $$\{\textbf{w}_{1} ,\textbf{w}_{2}, \dots, \textbf{w}_{m}\}$$. We therefore find a corresponding matrix $$A$$ to $$L(V,W)$$.

<b>Derivatives</b>

&#8195;&#8195;If $$f$$ is a real function with domain $$(a,b) \subset R^{1}$$ and if $$x\in (a,b)$$, then $$f'(x)$$ is usually defined to be the real number

<center>
$$
\begin{equation}    	\begin{aligned}          	\lim_{h\rightarrow0} \frac{f(x+h)-f(x)}{h},	\end{aligned}\end{equation}
$$
</center>
provided, of course, that the limit exists. Thus

<center>
$$
\begin{equation}    	\begin{aligned}          	f(x+h)-f(x)=f'(x)h+r(h)	\end{aligned}\end{equation}
$$
</center>

where the "remainder" $$r(h)$$ is small, in the sense that
<center>
$$
\begin{equation}    	\begin{aligned}          	\lim_{h\rightarrow0} \frac{r(h)}{h}=0.	\end{aligned}\end{equation}
$$
</center>

&#8195;&#8195;Note that the equality above might indicate that the difference $$f(x+h)-f(x)$$ could be approximated by a <i>linear function</i> $$f'(x)h$$. The point is, we could also regard the derivative of $$f$$, this linear function, as a <i>linear operator</i> on $$R^{1}$$ which takes $$h$$ to $$f'(x)h$$.

&#8195;&#8195;Then we can naturally extend the concept of derivative to a higher dimensional space. In this case the derivative of function $$\textbf{f}$$ should be a linear transformation, or, equivalently, a matrix.

<b>9.11 Definition</b> Suppose $$E$$ is an open set in $$R^{n}$$, $$\textbf{f}$$ maps $$E$$ into $$R^{m}$$, and $$\textbf{x}\in E$$. If there exists a linear transformation $$A$$ of $$R^{n}$$ into $$R^{m}$$ such that

<center>
$$
\begin{equation}    	\begin{aligned}          	\lim_{\textbf{h}\rightarrow0}     	\frac{\vert \textbf{f}(\textbf{x}+\textbf{h})-    	\textbf{f}(\textbf{x})-    	A\textbf{h}\vert}    	{\vert\textbf{h}\vert}=\textbf{0},	\end{aligned}\end{equation}
$$
</center>

then we say that $$\textbf{f}$$ is <i>differentiable</i> at $$\textbf{x}$$, and we write

<center>
$$
\begin{equation}    	\begin{aligned}          	\textbf{f}'(\textbf{x})=A.	\end{aligned}\end{equation}
$$
</center>

{% include post.html %}

  
