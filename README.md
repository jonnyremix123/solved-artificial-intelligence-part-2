Download Link: https://assignmentchef.com/product/solved-artificial-intelligence-part-2
<br>
<strong>Path to Safety (Game)</strong>

<ul>

 <li><strong><em>About the game: </em></strong></li>

</ul>

Given an MxN board, the goal of the game is to move from the ‘Start’ square and safely reach the ‘Finish’ square. In order to “safely” reach the finish square, you can’t pass through any squares containing bombs. You should also try to collect as many stars as possible in your path. The game has several levels; each level is different in configuration and some levels have more than one path. For example, the level shown in the opposite figure has <strong>3</strong> possible safe paths. The shortest path contains 1 star while the longest contains 3.

<ul>

 <li><strong><em>What you are required to do: </em></strong></li>

</ul>

You will be given a prolog source file containing the level data (like the file attached with this document) and you are required to make a prolog program that produces a list of moves for each possible safe path from the start to the finish square and states the number of stars that can be collected in each path. Your prolog source file should only contain the predicates and rules needed by the solver; however, it shouldn’t define any facts about the level configuration.

<ul>

 <li><strong><em>A sample test case: </em></strong></li>

</ul>

This test case shows the sample input that should be entered and what the output should look like. Notice that this output is the output produced when we run the solver on the level shown in the first figure.

<table width="621">

 <tbody>

  <tr>

   <td width="621">?- load_files(“C:/ Level3.pl”). %the level file (test case) given by your TA true?- load_files(“C:/ Solver.pl”). %the file containing your program true?- play(Moves,Stars). %the user will only enter this predicate (play/2) Moves = [right, down, down, right, up],Stars = 2 ;Moves = [right, down, down, right, right, up, left],Stars = 3 ;Moves = [right, down, right], Stars = 1 ; false.</td>

  </tr>

 </tbody>

</table>

<ul>

 <li><strong><em>The structure of the input file: </em></strong></li>

</ul>

You will find the level file (for the level in the first   figure)        attached     with this document. All level files will have the same structure shown in the opposite figure. A level file contains the following predicates:

<ul>

 <li><strong>dim/2:</strong> the dimensions of the board.</li>

 <li><strong>start/1:</strong> the start square.</li>

 <li><strong>end/1:</strong> the finish square.</li>

 <li><strong>bomb/1:</strong> the square that contains a bomb.</li>

 <li><strong>start/1:</strong> the square that contains a star.</li>

</ul>

You will notice that each square is represented by a list containing 2 elements;

the index of the row and the index of the column in which this square is located. Level files will have the <strong>same structure</strong> (same predicate names, number of arguments), however they will have <strong>different data</strong> (different dimensions, start/end locations, different numbers and locations of bombs and stars). <strong>You are not allowed to change the structure of the level file</strong>; you should adjust your program to work with this structure.

<strong><em> </em></strong>





