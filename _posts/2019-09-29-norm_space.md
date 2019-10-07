---
layout: post
title: norm space(SEQUENCE AND SERIES OF FUNCTIONS)
category: about math
---

<head>
<script type="text/javascript" async
      src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js?config=TeX-MML-AM_CHTML">
    </script>
</head>

&#8195;After studying some global properties of series of functions, the concept of norm space furnished a new version to describe them.

<strong>7.14 Definition</strong> If $$X$$ is a metric space, $$\mathscr{C}(X)$$ will denote the set of all complex-valued, continuous, bounded    functions with domain $$X$$.

&#8195;&#8195;We associate with each $$f\in\mathscr{C}(X)$$ its <i>supremum norm</i>

<center>

$$
\Vert f\Vert=\sup\limits_{x\in X}\vert f(x)\vert.
$$

</center>

If $$h=f+g$$, then

<center>

$$
\vert h(x)\vert \leq \vert f(x)\vert+\vert g(x)\vert\leq \vert f\vert+\vert g\vert
$$

</center>

for all $$x\in X$$. Hence

<center>

$$
\Vert f+g\Vert \leq \Vert f\Vert+\Vert g\Vert.
$$

</center>

&#8195;&#8195;If we define the distance between $$f\in\mathscr{C}(X)$$ and $$g\in\mathscr{C}(X)$$ to be $$\Vert f-g\Vert$$, it follows that $$\mathscr{C}(X)$$ becomes a metric space.



&#8195;&#8195;A new version mentioned above, is that we can restate some previous theorems as follows:

&#8195;&#8195;<i>A sequence $$\{f_n\}$$ converges to f with respect to the metric of $$\mathscr{C}(X)$$ if and only if $$f_n\rightarrow f$$ uniformly on $$X$$.</i>

&#8195;&#8195;This is an example of the <i>supremum norm</i>.  We could also define some different norms, like:

<center>


$$
\Vert f\Vert=(\int_{0}^{1}\vert f(x)\vert^{p}dx)^{1/p},
$$
</center>



where $$X=[0,1]$$.

{% include post.html %}
