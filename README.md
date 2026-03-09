# Regex Parser, Interpreter and Visualiser

## Synopsis

This project is a standalone regex **parser, interpreter \& visualizer** for an expressive regular language (subset of `POSIX`):  

```  

r1,r2 ::= ε | a | . | r1* | r1+ | r? | (r1 | r2) | r1r2 

```  

- I.e. Empty-String, Literals, Literal-Wildcards, Kleene, Plus, Optional, Or and Concatenation. 

The whole process of
1. parsing of the regular expression
2. creation of a non-deterministic finite automaton (NFA) via *Thompson's construction*
3. translation of the NFA into a deterministic finite automaton (DFA) via *powerset construction*
4. full-match-check by interpreting the input-string on the DFA
5. creation of a visualization of the DFA and the interpretation of the input

is manually done from first principles in the backend. 


## Remark 

This project is supposed to be a lightweight, accessible and open-source learning website to improve the understanding of **formal languages and automatons**.

It is based on a purely-Haskell backend, utilising [scotty](https://hackage.haskell.org/package/scotty) and [parsec](https://hackage.haskell.org/package/parsec), which supplies a minimalistic Javascript-frontend.


The source code for both the frontend and backend can be found here:  
   
- [frontend](https://github.com/FunktionellByra/regex_frontend)  
- [backend](https://github.com/FunktionellByra/regex_backend)  
