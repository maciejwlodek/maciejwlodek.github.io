---
layout: post
title:  "Tikz Tool"
date:   2019-09-03 2:41:13 -0400
categories: projects
---

<p align="left" style="margin-left: 15%; margin-right: 15%">

During the Spring 2019 semester, I was taking AMS 301 among other courses. That class included graph theory, and since I use $\LaTeX$ to type up all of my homeworks, I needed to be able to draw 
graphs in $\LaTeX$. This meant I either had to use the Tikz/PGF package or draw everything by hand and scan the images. Obviously, the former is much neater, but it proved very tedious, especially for 
more complex graphs when the default positioning schema used in Tikz proved insufficient to my needs and I had to provide more precise 
locations of nodes and edges. For this reason, I created <a href="https://github.com/maciejwlodek/tikz-pgf-tool">TikzTool</a>, a program that allows one to draw graphs and automatically export 
them to Tikz/PGF code that may be used in $\LaTeX$. 

The user simply places down nodes in the desired positions and draw edges between pairs of nodes (the edges may be directed or undirected). The color, size, stroke width, etc. of each node and each edge 
may be customized. In addition, nodes may be given labels, and these labels may be positioned as needed. 

</p>

<img src="/assets/images/tikz1.PNG" />

<p align="left" style="margin-left: 15%; margin-right: 15%">

Additionally, I needed to have a functionality to draw curved edges, because sometimes they are necessary, i.e. to demonstrate planarity of various graphs. I accomplished this by turning each edge to a 
cubic Bezier curve, and allowing the user to move the control nodes for each edge as desired. Therefore, any straight or curved edge is possible to be drawn.

</p>

<img src="/assets/images/tikz2.PNG" />

<p align="left" style="margin-left: 15%; margin-right: 15%">


After the graph is input, the user may generate Tikz code for use in LaTeX. For example, the following is the generated Tikz 
for the above graph. 

</p>
 
<!-- {%highlight plaintext %}
{% raw %}
\begin{tikzpicture}[auto, node distance=3cm, every loop/.style={},
                    thick,main node/.style={circle,draw,font=\sffamily\small}, label distance=0mm] 
\definecolor{nodecolor}{rgb}{0.0,1.0,0.0} 
\definecolor{strokecolor}{rgb}{0.0,0.0,1.0} 
\definecolor{edgestrokecolor}{rgb}{1.0,0.0,0.0} 
\tikzset{vertex/.style = {shape=circle, fill=nodecolor!69, inner sep=0pt, draw=strokecolor!100, line width=1.0pt, minimum size=10pt}}
\tikzset{edge/.style = {line width=1.0pt, draw=edgestrokecolor!100, ->,> = latex'}}
\def\labels{{"", "1", "2", "3", "4"}};
\def\labelPositions{{,  90,  90, 270,  90}};
\def\numNodes{4};
\def\coords{{{,}, {-0.97, 3.79}, {-2.98, 0.16}, {0.65, 0.56}, {2.66, 2.18}}};
\def\numEdges{5};
\def\edges{{{,}, {2,1}, {3,1}, {1,4}, {3,4}, {2,3}}};
\def\controls{{{,,,}, {-0.58,1.85,-3.53,3.06}, {0.92,1.74,-1.37,1.89}, {0.24,3.26,1.44,2.73}, {1.32,1.11,1.99,1.64}, 
{-1.77,0.30,-1.26,1.79}}};
\def\getFirstNode#1{\pgfmathtruncatemacro{\nodeA}{\edges[#1][0]}};
\def\getSecondNode#1{\pgfmathtruncatemacro{\nodeB}{\edges[#1][1]}};
\def\getLabelAngle#1{\pgfmathtruncatemacro{\angle}{\labelPositions[#1]}};
   %DRAW THE NODES WITH LABELS
   \foreach \phi in {1,...,\numNodes}{
      \getLabelAngle{\phi};
      \node[vertex, label={\angle:\pgfmathparse{\labels[\phi]}\pgfmathresult}] (\phi) at (\coords[\phi][0], \coords[\phi][1]) {};
   }
   %DRAW THE EDGES
   \foreach \psi in {1,...,\numEdges}{
      \getFirstNode{\psi};
      \getSecondNode{\psi};
      \draw[edge] (\nodeA) .. controls (\controls[\psi][0], \controls[\psi][1]) and (\controls[\psi][2], \controls[\psi][3]) .. 
(\nodeB);
   }
\end{tikzpicture}
{% endraw %}
{% endhighlight %} -->

<img src="/assets/images/tikzCode.PNG" />

<p align="left" style="margin-left: 15%; margin-right: 15%">

Seeing how much code there is for just a simple 4 node graph makes my motivation for making this tool quite clear. 

Now, we may finally put this into a LaTeX document.


</p>

<img src="/assets/images/tikz3.PNG" />


