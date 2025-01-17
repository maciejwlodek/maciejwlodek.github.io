---
layout: post
title:  "Gomoku game"
date:   2019-08-31 22:46:54 -0400
categories: hsprojects
---

<li><a href="https://github.com/{{ site.github_username| cgi_escape | escape 
}}/Gomoku"><svg class="svg-icon"><use xlink:href="{{ 
'/assets/minima-social-icons.svg#github' | relative_url }}"></use></svg> <span 
class="username">Gomoku</span></a></li>




For my AP Computer Science class in 11$^{th}$ grade, I created a Gomoku game. Gomoku is a Japanese board game dating back thousands of years. The game is played by two players who take turns playing 
stones on a grid. The first 
player to get five consecutive stones in a row, column, or diagonal wins the game. Typically the game is played on a $15\times 15$ grid, though my program allowed one to choose any size board from 
$8\times 8$ to $16\times 16$. There was a single player 
mode, allowing the user to play against a simple AI with 3 difficulty levels, or there was a two-player mode. I named the AI that I programmed <em>AlphaGomoku</em> in honor of Google DeepMind's 
<em>AlphaGo</em>, a 
go-playing AI (Go is a different, and infinitely more complex game than Gomoku). <em>AlphaGo</em> had 
debuted just a few months earlier, defeating Korean professional Lee Sedol (it was the first time in history a computer was able to defeat a top Go professional). Needless to say, my AI wasn't quite as 
good at Gomoku as <em>AlphaGo</em> was at Go, and it did not use any sort of the machine learning techniques employed by <em>AlphaGo</em>. However, despite all that it did manage to defeat me a few 
times.

All of the played games were saved and could be replayed later in order to aid with game 
analysis. This way, a player could reanalyze won and lost games, and use this to learn and get better. 

The GUI looked like this:

<!--- <a href="" target="_blank"><img src="/assets/images/graphing-calculator.PNG" /></a> --->

<img src="/assets/images/gomoku.PNG" />

In addition, one could customize the game board and stones.

<img src="/assets/images/gomoku-color.PNG" />
