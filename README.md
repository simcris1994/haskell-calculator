# Haskell Expression Evaluator
Haskell program that parses and evaluates mathematical expressions. 

Supported expressions:
  addition
  multiplication
  division
  derivative
  sine/cosine
  
The operations are given as a string input to the program, which will then attempt to parse the string into a custom defined data type and evaluate it.

The grammar of the input is defined in Parse.y - using Happy (https://www.haskell.org/happy/), the parser generator for Haskell, which outputs a parser based on the given grammar (BNF).

The program will go through several intermediate stages, evaluating the given expression until it reaches a final expression that can no longer be reduced, e.g.:
  (5 * (x + 1)) =
  ((5 * x) + (5 * 1)) =
  (5 * x + 5)
  
  
![haskell1](https://user-images.githubusercontent.com/7521620/139597449-e761529c-6cd7-4bad-a334-e7eef203db94.PNG)
![haskell2](https://user-images.githubusercontent.com/7521620/139597451-cde9725b-dcf2-4fc7-aff8-0a710fee1030.PNG)
