---
layout: post
title: Latex and Jekyll
description: Ecologist, Physicist, and Teacher
tags: [jekyll, latex, website]
---

This is my first website and as a result I am learning something new with every post.  I am using Jekyll, a static site generator build on ruby, for two reasons.

1. I have heard wonderful things about it.
2. It works with [github pages](https://pages.github.com/), so you can host your Jekyll site for free.

The setup has been pretty painless, even for someone with little prior experience with HTML, CSS, or Ruby.  I am familiar with git however, which has been a huge help.  I simply cloned [someone else's code](https://github.com/poole/poole), and began to modify it to my own liking. 

> For those unfamiliar with git, there are many wonderful online [tutorials](https://try.github.io/levels/1/challenges/1).  I have a github account---[capecodcid](https://github.com/capecodcid/) (which I use less than I should).  On my own computer I use a combination of the command line and [gitbox](http://www.gitboxapp.com/) to manage my repositories.

My advice is to start with something simple.  There are some really beautiful [Jekyll themes](https://github.com/ColeTownsend/Balzac-for-Jekyll), but start simple. 

The first thing I needed to figure out how to do is to use [MathJax](http://www.mathjax.org/) to render LaTeX equations.  I will be writing a lot of math and I want it to look good!

$$
G_{\mu \nu} + \Lambda g_{\mu \nu} = \frac{8\pi G}{c^4}T_{\mu \nu}
$$

> This is the famous Einstein Field Equation, which captures the key idea of General Relativity---local curvature in spacetime is equal to the local momentum and energy in that spacetime.  Matter and energy bend space!

Boom!  I am not sure why things are orange, but at least everything is typesetting correctly.  So what did I have to do to get this to work?  There are two parts.  First, you need to tell your webpage where to find MathJax.  Second, you need to make sure that your markdown parser recognizes that something is LaTeX.  So here was my procedure:

* I added the following line of code to `head.html` in my `_includes` folder.  It could equivalently go in `default.html`.  It just needs to be somewhere it will get run.  This simply instructs the browser to go grab the latest MathJax javascript.

{% highlight html %}
<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>
{% endhighlight %}

* I changed the markdown parser to `kramdown` which recognizes anything between two sets of `$$` as a LaTeX equation and not regular markdown.  To do this I first had to install kramdown,

{% highlight ruby %}
gem install kramdown
{% endhighlight %}

and then I added the following line to my `_config.yml` file.

{% highlight Text only %}
markdown:         kramdown
{% endhighlight %}

Voila!  It works.  It even supports inline equations like $$\sum_{n=1}^{\infty} \frac{1}{n^2} = \frac{\pi^2}{6}$$.  Not just need to figure out how to change the coloring.



