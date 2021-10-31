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
