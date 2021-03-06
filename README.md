# About

Collection of notes and exercise attempts from working through Structure and Interpretation of Computer Programs (SICP), a textbook by professors Harold Abelson and Gerald Jay Sussman with Julie Sussman. As the title suggests, I am going through the book to get another take on how to build programs in the future.

- 📓 You can find a copy of SICP provided by MIT [here](https://web.mit.edu/6.001/6.037/sicp.pdf)
- ✏ The notes and attempts are done in with Org mode in [Doom Emacs](https://github.com/doomemacs/doomemacs).
- 🎾 Code snippets are written in [Racket](https://racket-lang.org/), a dialect of Lisp
- 📦 Using SICP package to run primitives expected by MIT scheme not found in Racket
- 📦 In the exercises which involved recursion I often used the "trace" package which printed out the function calls and its arguments

# 🌟 Highlights

- Chapter 1: 
    * models for computation:
      - substitution
      - applicative vs normal order
    * different types of recursion: linear (stack grows) and iterative (keeps track of state) recursion
    * tree recursion (procedure makes two recursive calls which is combined)
    * procedures can be used as arguments
    * procedures can be used as return values
      - accomplished using the lambda keyword
    * In Lisp, procedures are treated as first class elements meaning:
      - can be named by variables
      - passed as arugments
      - used as return values
      - included in data structures
    
- Chapter 2: 
    * What is data? 
      - It is not enough to say data is whatever is implemented with constructors and selectors (i.e. procedures)
      - Data must also include conditions that must be fulfilled in order to be a valid representation (analogous to business logic?)
    * data as functions
      - introduction to lambda calculus 
    * key to organizing programs is to clearly represent the signal flow structure
    * higher order functions: reduce, accumulate, fold
    
    * performance benefits when choosing structure to represent data:
      - unordered lists vs ordered lists vs trees 
      
    * Goals for programs is to have "abstraction barriers"
      - Abstraction barrier: Isolate the underlying representation of the data objects
      - But consider having different representations of the same data; how will the program know which corresponding procedure to call
    * Dispatching:
      - tagging data
      - check tag then call procedure
    * Data directed programming:
      - weaknesses of dispatching (i.e. not additive) include:
        - all procedure implementations for every type must be known beforehand
        - needing unique procedure names for every type (despite being similar functionality in real world)
      - creating a table of procedure to be called vs type
      - implement this table through generic procedures and packages 
      
- Chapter 3
  * Assignment: 
    - can introduce state with the let keyword
    - set! keyword is for modifying a variable
    - procedures which act on the variable (with set!) are also defined in let environment
    - then with messaging-passing; we can modify state of variable accordingly
    
    - begin procudere is useful for grouping sequences of procedures
    
  * Benefits of assignment:
    - Great for modelling computational objects whose state changes over time
  * Costs of assignment:
    - With assignments we cannot be sure a procedure with the same arguments to the same function will produce the same result
    - Programming with no assignments is referred to as *functional* programming
    - order of evaluation of subexpressions matter with assigments (i.e. right to left or left to right)

