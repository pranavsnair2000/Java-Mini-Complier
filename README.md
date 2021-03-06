# Java-Complier
A primitive compiler for Java implemented using Flex and Bison.

4 of the stages of a compiler are implemented here:
  * Symbol table generation
  * Abstract Syntax tree Generation
  * Intermediate code generation
  * Code optimization

The *test.java* file is taken as input for the first 3 stages, and intermediate code written into *ic.txt* is taken as input within *opt.py*, which performs optimization.

1. The lexical analyzer identifies tokens from the raw input string that is the .java file, after which the parser check for correct syntax(*lexfile.l* and *parsefile.y*). Symbol table is generated by *parsefile.y*. 
2. Syntax tree is generated by *syntax_tree.y*.
3. Intermediate code is generated by *icg.y*.
4. Four code optimization techniques are implemented in *opt.py* 

As this is a primitive compiler, fuctionality is limited.


**note** : 
  * *opt.py* is not tolerant to empty lines and anything other than the intermedieate code itself.
  * Output generated by the icg should be redirected to *ic.txt*.
