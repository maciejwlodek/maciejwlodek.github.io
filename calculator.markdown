---
layout: post
title:  "Graphing calculator"
date:   2019-08-30 20:31:34 -0400
categories: hsprojects
---

<!-- <li><a href="https://github.com/{{ site.github_username| cgi_escape | escape 
}}/Graphing-calculator"><svg class="svg-icon"><use xlink:href="{{ 
'/assets/minima-social-icons.svg#github' | relative_url }}"></use></svg> <span 
class="username">Graphing Calculator</span></a></li> -->

<p align="left" style="margin-left: 15%; margin-right:15%">

In high school, one of my first larger coding projects was a simple graphing calculator that I wrote 
in Java using Swing. You may find the source code <a href="https://github.com/maciejwlodek/Graphing-calculator">here</a>.

<!--- <a href="" target="_blank"><img src="/assets/images/graphing-calculator.PNG" /></a> --->

It supported 
the five 
standard 
arithmetic operations $(+,-,\cdot,/,\hat{})$, as well as the following special functions:
$ \sin, \cos, \tan, \arcsin, \arccos, \arctan, \ln, \log, \sqrt{x}, | x |, \lfloor x \rfloor, \lceil x 
\rceil, \Gamma(x),$ and $ e^x $
(where $\Gamma(x)$ is the <a href="https://en.wikipedia.org/wiki/Gamma_function">gamma function</a>, defined by $\Gamma(x) = \int_{0}^{\infty} 
t^{x-1}e^{-t}dt$.)

In addition, it supported graphing the derivative of an inputted function. 

Besides graphing, it also had the capability of computing infix or postfix expressions involving the 
above operations and functions.

Here are a few sample graphs.

This is the graph of $\sin(x^2)\cdot \cos(x^3)$:

</p>

<img src="/assets/images/graph1.PNG" />

This is third order Fourier series approximation of the square wave:

<img src="/assets/images/graph2.PNG" />

This is the derivative of $\ln(\Gamma(x))$, otherwise known as the <a href="https://en.wikipedia.org/wiki/Digamma_function">digamma function</a>:

<img src="/assets/images/graph3.PNG" />


