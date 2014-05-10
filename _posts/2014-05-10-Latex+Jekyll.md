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

\begin{equation}
\label{EFE}
G_{\mu \nu} + \Lambda g_{\mu \nu} = \frac{8\pi G}{c^4}T_{\mu \nu}
\end{equation}