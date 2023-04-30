Download Link: https://assignmentchef.com/product/solved-csce625-assignment-1-search-bfs-and-lazy-evaluation
<br>
<span style="font-size: 2.61792em; letter-spacing: -1px; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen-Sans, Ubuntu, Cantarell, 'Helvetica Neue', sans-serif;">Question</span>

Consider the following puzzle. It is in the vein of Russell and Norvig’s toy problem on page 73, that they attribute to Donald Knuth.

You are given a pair of numbers: the first is the seed, <em>x</em><sub>0</sub>, and the second the target <em>x<sub>f</sub></em>. You are provided, additionally, with two functions <em>f </em>: R→R and <em>g </em>: R→R.

<table>

 <tbody>

  <tr>

   <td width="124"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>

Puzzle: Write a program to give either the minimal number of function applications (of <em>f </em>and <em>g</em>) needed to reach <em>x<sub>f </sub></em>from <em>x</em><sub>0</sub>, or state that one cannot reach <em>x<sub>f </sub></em>from <em>x</em><sub>0</sub>.

<h1>Approach</h1>

This problem is from <a href="https://nmattia.com/posts/2016-07-31-bfs-tree.html">https://nmattia.com/posts/2016-07-31-bfs-tree.html</a>

In that blog post Nicolas Mattia considers the two functions <em>f </em>and <em>g </em>defined as follows:

<em>f</em>(<em>x</em>) = 2<em>x </em>+ 1            and            <em>g</em>(<em>x</em>) = 3<em>x </em>+ 1<em>.</em>

The author provides code to solve exactly this problem on that page. Actually, that page <em>is </em>code, written in Haskell. (Look up literate programming if you’ve never heard

of it.)

<h2>Task1</h2>

Convert his solution, for those two particular <em>f </em>and <em>g </em>functions, to Scheme. His approach is not quite the same as the straightforward stack-based method given in Russell and Norvig. Instead, it uses Haskell’s lazy evaluation to provide a sort of infinite data structure. You are to do the same thing: implement the search using lazy evaluation.

1

We have Gambit Scheme installed on the compute.cs.tamu.edu server. The page at <a href="http://www.iro.umontreal.ca/~gambit/doc/gambit.html">http://www.iro.umontreal.ca/</a><a href="http://www.iro.umontreal.ca/~gambit/doc/gambit.html">˜</a><a href="http://www.iro.umontreal.ca/~gambit/doc/gambit.html">gambit/doc/gambit.html</a> provides some information that you might find useful in getting up and running with the interpreter and compiler.

By default Scheme uses eager evaluation. You have to make use of the delay and force keywords. Details on this can be found here: <a href="http://www.shido.info/lisp/scheme_lazy_e.html">http://www.shido.info/</a>

<a href="http://www.shido.info/lisp/scheme_lazy_e.html">lisp/scheme_lazy_e.html</a>

(Note that the text in that guide uses Guile, not Gambit Scheme, so the promise? type checking function isn’t available for us. The other functionality is supported, however.)

<h2>Task2</h2>

Reflect on these things:

<ul>

 <li>Consider Knuth’s original problem. That requires more than just an <em>f </em>and <em>g</em>. Can you pose his problem with a modification of your code?</li>

 <li>What properties are needed to ensure that your program is guaranteed to give a solution to the puzzle?</li>

</ul>

2